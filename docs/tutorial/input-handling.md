![](../images/luxe-dark.svg){width="96em"}

# input handling in luxe

!!! example "outcome"
    In this step we'll rearrange our code a bit, and then
    respond to mouse clicks to move our character around.

For this step, we'll continue editing the code for the game.

## refactoring our player

Before we get to input, let's do some quick housekeeping and make it so we
can access our `player`outside of the `ready` function.

When we created our player in `ready` before, we stored the Entity in a variable.

```js
var player = Entity.create(app.world, "player")
```

This variable exists only in the `ready` function, 
although we probably want to access the player in other functions as well.
To do that we need to store the value inside a _field_ rather than just a variable.

!!! note ""
    A _field_ is a variable that can be seen by any function in the same class. 

Here is how that looks. We remove the `var` in front, and add an underscore character.
The underscore signifies that this is a field and exists for the whole class to see. 
We then use the `_player` variable to access the player from elsewhere.

```js
_player = Entity.create(app.world, "player")
```

Let's move our player creation into it's own function.

We'll **create a new function** just below the ready function called `create_player`, 
**move our player creation code** into it, and then edit the code to 
**use `_player` instead of `player`**. 

!!! note ""
    A function in Wren is called a _method_ when it's part of a class. 

This is what the empty method looks like, we can add it just below `ready`.

```js

construct ready() {
  ...
} //ready

create_player() {
  
  //move player code into here

} //create_player
```

We move the player code in by copy and pasting the code from `ready` into our new method.
While we're there, take note that we've renamed to `_player`.

```js
create_player() {

    //create an entity
  _player = Entity.create(app.world, "player")
    //get the material for the player from the Assets
  var material = Assets.material("material/player")
    //attach a Sprite to the entity to display it
  Sprite.create(_player, material, 64, 128)
    //attach a Transform to the entity to position it
  Transform.create(_player)
    //set the position to the center of the screen
  Transform.set_pos(_player, app.world_width/2, app.world_height/2)

} //create_player
```

Once we've done that, we can call `create_player()` from `ready`, 
which behaves exactly the same as before. This is how it looks together.

```js hl_lines="16"
class Game is Ready {

  construct ready() {

    super("ready!")

    app = App.new()
    
      //set the background color to black
    app.color = [0, 0, 0, 1]

      //load the background scene
    Scene.load(app.world, "scene/area1")

      //create the player entity
    create_player()

  } //ready

  create_player() {

      //create an entity
    _player = Entity.create(app.world, "player")
      //get the material for the player from the Assets
    var material = Assets.material("material/player")
      //attach a Sprite to the entity to display it
    Sprite.create(_player, material, 64, 128)
      //attach a Transform to the entity to position it
    Transform.create(_player)
      //set the position to the center of the screen
    Transform.set_pos(_player, app.world_width/2, app.world_height/2)

  } //create_player

  ...
} //Game
```

---

## input basics

There's two main forms of interacting with the `Input` system.

You can use the direct key or mouse values, or you can bind several keys to named events, 
like making a single event called `"jump"` that's bound to gamepad, keyboard and mouse.
Named events are good for accessibility since they can be remapped, and provide multiple defaults. 

Typically you'd want to use events, but for debugging and prototyping it can be convenient to query directly. 

There are two ways to get input information from luxe:

- input queries - good for prototypes and reactive input (query changes frequently)
- input callbacks - good for general purpose use where input is connected once

For this tutorial, we'll use the query version for now but we'll use named input events later in the tutorial.

!!! note ""
    There's a wip refactor of input events that makes them nicer to use. For now we'll use the direct approach.

## input queries

It can often be convenient to query the state of `Input` directly (especially while prototyping or debugging), 
e.g to find out if a particular mouse button is currently being held down, or if a certain key was pressed this frame.
This is polling the `Input` system and responding to the current state, "immediate" style.

The `Input` API provides these queries and they're typically called during an update/tick part of your game. 
To query the mouse position for example, you can call `Input.mouse_x()` and `Input.mouse_y()`.

Named events use `event_began`, `event_ended` and `event_active`,
and there's a `down`, `pressed` and `released` option for `mouse`, `key` and `gamepad` input. 

<small>:todo: the naming is all inconsistent between pressed/released/down/up/began/ended etc.</small>

```js
tick(delta) {
  
  if(Input.key_state_down(Key.up)) {
    System.print("holding down the up key")
  }

  if(Input.mouse_state_released(MouseButton.left)) {
    System.print("mouse left released this frame")
  }

  //'jump' could be bound to several things:
  //left click, Z, space bar, gamepad button 0
  if(Input.event_began("jump")) {
    System.print("jumped!")
  }

} //tick
```

??? summary "input callbacks"
    We can also connect a callback function to a particular type of event
    and the `Input` system will notify us when that type has occurred.
    The `InputType` has various events for mouse, keys and gamepad.


    ```js
    Input.listen_for(InputType.key_down) {|key, scan, repeat, mod|
      if(repeat) return //we only care about the first press down
      if(key == Key.space) {
        System.print("space was pressed")
      }
    }
    ```

    We can do similar for named events:
    ```js
    Input.listen_for_event("interact") {|event|
      System.print("interacted with something...")
    }
    ```

## making the player move

The project outline includes a custom modifier for moving the player around on screen.
The movement modifier offers some functions we can call to move the player to a destination, which is 
a 2D coordinate in _world units_ (world space). 

!!! note ""
    Since the focus of this tutorial is learning to use luxe, we're not going to implement movement code.

Our next goal is to make the player move when you click the mouse, and they'll move to where you clicked.

### coordinate spaces

We can easily get the mouse position with `Input.mouse_x()` and `Input.mouse_y()`, but these values are 
relative to _the window_. `0,0` is top left, and they go up to `window width, window height`. The values we 
want are meant to be in _world space_, the mouse is in _screen space_/_window_space_. 

How do we convert these values to world space? The answer is a bit dependent on how the game works. 
Our project outline has already accounted for this, and provides `app.mouse_to_world(x: Num, y:Num)`
which converts mouse input values to world space. We'll use that!

The important thing to note here is that _multiple coordinate spaces exist_, and it helps to know that going in.

??? summary "converting technical details"
    For a pixel art game like the one we're making, the **world size on screen** is a fixed value, like `640x360`.
    Our game is scaled and centered in the window, and if there's extra space letter or pillar boxes are added.
    This means there's space _around_ the game area in the window that we need to account for.
    
    The project outline calculates the size of the game area within the window while keeping scaling in mind,
    and then offsets and scales the mouse position to account for those details.

    Once the position is found within our game region _in screen space_, 
    we use the `Camera.screen_point_to_world` function below to convert from 
    screen space to world space. Screen space is `0,0` top left, with `y+` going downwards. 
    Our world space is `0,0` bottom left, with `y+` going upward. 
    This function converts between them safely for us.

    ```js
    Camera.screen_point_to_world(camera: Entity, x:Num, y:Num)
    ```

    And here's how the mouse is adjusted:

    ```js
    mouse_to_world(mx, my) {

      var region = game_region
      var ratio_x = region.z / width
      var ratio_y = region.w / height

      mx = (mx - region.x) / ratio_x
      my = (my - region.y) / ratio_y

      my = my.floor
      mx = mx.floor

      return Camera.screen_point_to_world(_camera, mx, my)

    }
    ```
  
### attach the movement modifier

To make our player Entity moveable, we'll want to attach the move modifier.
The move modifier is provided by the project outline, and we have access to it
since it is already imported for us at the top of `game.wren`, like this: `import "modifier/move" for Move`.

To attach the modifier we use the same pattern as before, `Move.create(_player)`.

We'll add that to our `create_player()` function at the end. 
We'll also make sure the player only moves on the x axis.

```js hl_lines="15 18"
create_player() {

    //create an entity
  _player = Entity.create(app.world, "player")
    //get the material for the player from the Assets
  var material = Assets.material("material/player")
    //attach a Sprite to the entity to display it
  Sprite.create(_player, material, 64, 128)
    //attach a Transform to the entity to position it
  Transform.create(_player)
    //set the position to the center of the screen
  Transform.set_pos(_player, app.world_width/2, app.world_height/2)

    //make the player able to move around easily
  Move.create(_player)
    //limit their movement to the x axis only, 
    //by not allowing the Y axis when moving
  Move.allow_y(_player, false)
  
} //create_player
```

### move on click

The `Move` modifier provides `Move.to(entity: Entity, destination: Entity)`.
This function takes an entity as a destination, so we'll create a target
entity that we'll move around. 

Back inside our `create_player` method, we'll add three more lines to create this target,
as well as keep track of our movement speed so it's easy to change later.

```js hl_lines="21 24 26"
create_player() {

    //create an entity
  _player = Entity.create(app.world, "player")
    //get the material for the player from the Assets
  var material = Assets.material("material/player")
    //attach a Sprite to the entity to display it
  Sprite.create(_player, material, 64, 128)
    //attach a Transform to the entity to position it
  Transform.create(_player)
    //set the position to the center of the screen
  Transform.set_pos(_player, app.world_width/2, app.world_height/2)

    //make the player able to move around easily
  Move.create(_player)
    //limit their movement to the x axis only, 
    //by not allowing the Y axis when moving
  Move.allow_y(_player, false)

    //we move at 80 pixels per second
  _move_speed = 80
    //create a target we can move toward, 
    //which we'll move to the mouse position when clicking
  _move_target = Entity.create(app.world, "player.move")
    //make sure it has a position
  Transform.create(_move_target)

} //create_player
```

For now, we'll use the simplest form of input and add some code to our `tick` function.
The tick function is called once every frame, and is where we can do update logic.

When the left mouse button is released, we move our target, and ask `Move` to move us there.

```js hl_lines="9 10 11 12"
tick(delta) {

    //this is the world space mouse position
  var mouse = app.mouse

    //when left mouse is released, move the player to the 
    //clicked destination, by first moving our target there
    //and then asking the move modifier to move us to it
  if(Input.mouse_state_released(MouseButton.left)) {
    Transform.set_pos(_move_target, mouse.x, mouse.y)
    Move.to(_player, _move_target, _move_speed)
  }

  if(Input.key_state_released(Key.escape)) {
    IO.shutdown()
  }

} //tick
```

!!! tip "run the game and click around to move the player"

### facing the right direction

If you click to the right of the character, they'll move but be facing the wrong way.
The `Sprite` modifier has a `Sprite.set_flip_h(entity: Entity, flipped: Bool)` function that
we'll use to change the direction. 

We'll use the `Math` class (imported for you already via `import "luxe: math" for Math`) to
find out the direction we want to move, and if we're moving right, flip the character.

```js hl_lines="6 9"
if(Input.mouse_state_released(MouseButton.left)) {

    //make the player face the direction we want to move
    //by asking the math class for the 2D direction between
    //the player, and the destination mouse position 
  var direction = Math.dir2D(mouse, Transform.get_pos(_player))
    //If we're not standing at the destination, flip based on
    //whether the direction x value is on the right hand side (> 0)
  if(direction.x != 0) Sprite.set_flip_h(_player, direction.x > 0)

  Transform.set_pos(_move_target, mouse.x, mouse.y)
  Move.to(_player, _move_target, _move_speed)
} 
```

!!! tip "run the game again to see the results"

## next up

In the next step, we'll learn to animate things using the `Anim` modifier.