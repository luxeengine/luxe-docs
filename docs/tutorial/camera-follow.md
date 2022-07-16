![](../images/luxe-dark.svg){width="96em"}

# camera follow

!!! example "outcome"
    In this step we'll see how to move the camera around, 
    fix the player being in the air, and add some limits
    to where we can move and how.

## that floating player...

Previously when we made our player we set it to center screen. This made sense when it was on
a black background suspended in the void, but now that we have a background it would make sense
to put them on the ground where they're expected to be.

For now, we'll set the position in code explicitly, but further down we'll grab an entity from the scene
to use as a spawn point.

There's a few other things we can do while here:

  - move the player to the ground plane to fit the background
  - make it so that the player position is always snapped to 1 pixel
  - fix the origin so that the player position is at the bottom center

In the `create_player` function in our code, we'll go back to where the player entity is created, 
and we'll update the position and add add 2 lines for the rest.

For **`Transform.set_pos`** we change the y value to `26`. This value comes from the background image distance I'd want to set the player.

Also for `Transform.set_pos`, we added a `z` value and set it to `2` to control the `depth` of the sprite.
This will be relevant later when we add more stuff to the background behind the player. We can leave the x value for now.

```js hl_lines="10 14 16"
create_player() {

    //create an entity
  _player = Entity.create(app.world, "player")
    //get the material for the player from the Assets
  var material = Assets.material("material/player")
    //attach a Sprite to the entity to display it
  Sprite.create(_player, material, 58, 136)
    //set the origin to center bottom
  Sprite.set_origin(_player, 0.5, 0)
    //attach a Transform to the entity to position it
  Transform.create(_player)
    //set the position to the center of the screen
  Transform.set_pos(_player, app.world_width/2, 26, 2)
    //make sure the positions used are always snapped to 1 pixel
  Transform.set_snap(_player, 1, 1)

  ...

} //create_player
```

**fixing the sprite origin**   
For the sprite to be centered on x, but positioned along the bottom, we use **`Sprite.set_origin`**.
As before, this value is `0...1` range and `0, 0` is bottom left. So we want `0.5` and `0` to make the 
position of the sprite be at their feet.

**snapping to whole pixels**   
And finally, if the player isn't snapped to whole numbers in a pixel art game, it can cause visual artifacts.
We always want the position that the sprite uses to be rounded, so we can use **`Transform.set_snap`** which does it for us. 
Any time we set a value for the position, regardless of what it is, it will be snapped for us.

The snap values are in world space, and we want our player to be snapped to 1 pixel on `x` and `y`. 

And with that, our player looks a lot better in the scene.

![](../images/tutorial/intro/camera-follow-0.png){: loading=lazy }

## limiting our movement

When you click to move, you can go off screen if you click at the edges. We'll want to clamp
that so that you can only move within a reasonably defined range, set by the level.

The values used are taken from the background image again, and for now we'll 
type them directly in the code and change that later.

Inside the `tick` function, where our movement happens, we'll add two lines to fix that.

```js hl_lines="4 5"
if(Input.mouse_state_released(MouseButton.left)) {

    //limit movement to the area within our level
  if(mouse.x < 45) mouse.x = 45
  if(mouse.x > 836) mouse.x = 836

    //move the target to the destination
  Transform.set_pos(_move_target, mouse.x, mouse.y)

    //make the player face the direction we want to move
    //by asking the math class for the 2D direction between
    //the player, and the destination mouse position 
  var direction = Math.dir2D(mouse, Transform.get_pos(_player))
    //If we're not standing at the destination, flip based on
    //whether the direction x value is on the right hand side (> 0)
  if(direction.x != 0) Sprite.set_flip_h(_player, direction.x > 0)

    //ask the move system to move us to the target
  Move.to(_player, _move_target, _move_speed)

}
```

Now if we try go off the left edge, it looks like we get stuck against the wall.
We can't test the other side until the camera follows the player, so let's do that next.

![](../images/tutorial/intro/camera-follow-1.png){: loading=lazy }

## moving the camera

We already know how to move the camera, we can use `Transform.set_pos`!
All we need is an entity... which the project outline has created for us called `app.camera`.
This is the camera used to display the game world, and it is an entity with a `Camera` and a `Transform` attached.

### camera offset

There are some things to keep in mind though, the camera has it's origin bottom left, at `0, 0`.

That means if we want the camera to keep the player in the _center_ of the screen, we need to offset the position.
This offset is based on half of the view area shown on screen, and we've already used it before, `app.world_width/2`.

If we wanted to center the player we can do something like this. 
If we add this in `ready`, it would look the same as before, since the player is already centered.
If we add this to the top of `tick`, the camera would follow the player, but not very smoothly.

```js
var x = Transform.get_pos_x(_player)
var offset = (app.world_width/2).floor
Transform.set_pos_x(app.camera, x - offset)
```

### smoother follow

Smooth camera movement in a pixel art game has quite a bit of nuance to it, but the tutorial is set up to allow it.
We'll gloss over a tiny bit of detail here since our focus is on learning luxe and not camera smoothing.

First, we'll need to make sure the camera is also snapped to whole pixels. We'll use `Transform.set_snap` again, 
this time we can do it in the ready function. 

```js hl_lines="10"
construct ready() {

  super("ready!")

  app = App.new()

    //set the background color
  app.color = [0,0,0,1]
    //make sure the camera is snapped to whole pixels
  Transform.set_snap(app.camera, 1, 1)

  Scene.load(app.world, "scene/area1")

  create_player()

} //ready
```

Next we're going to make a method in our class called `update_camera(delta)`, 
which we'll call from the `tick` function after our movement code.

```js hl_lines="5 6 7 17"
construct ready() {
  ...
} //ready

update_camera(delta) {
  
} //update_camera

tick(delta) {

  var mouse = app.mouse

  if(Input.mouse_state_released(MouseButton.left)) {
    ...
  }

  update_camera(delta)

  if(Input.key_state_released(Key.escape)) {
    IO.shutdown()
  }

} //tick
```

### a little lerp goes a long way

Now we're going to do a small amount of maths to smoothly follow the player.
To do this we'll use `Math.lerp`, which is _linear interpolation_, which just means 
"change a value smoothly over time, linearly".

To start, we'll calculate our offset we mentioned above, relative to the player.


```js hl_lines="4 6"
update_camera(delta) {

    //the camera is positioned half the view away
  var offset = (app.world_width / 2).floor
    //this is the target move position for the camera
  var target = Transform.get_pos_x(_player) - offset

} //update_camera
```

Now we can interpolate our current x value, to the one we want to be at (`target`) over time.

```js
var new_pos = Math.lerp(pos.x, target, delta)
```

The `Math.lerp` method returns a value between the first argument (`pos.x`) and the second argument (`target`)
based on the third argument (often called `t`, like time). 

This `t` argument is a value between `0...1`, if it is `0` you get the first value (pos.x) and if it is `1` you get the second (target).
A value of 0.5 would bring you halfway between the two.

What we want to do is move the camera a little bit closer to the player each frame, which is why we do it inside of `tick`, 
which is called once per frame. 

For `t`, if we pass a small value like `0.1`, they'll move 10% closer each frame (because 1 is 100% to the goal). Notice that
this means _10% of the distance still to go_, which means it will slow down as it gets closer, because the distance moved gets smaller.

Normally we also want things to be independent of our frame rate, so we multiply speeds by `delta`. In this case, we're ok with a speed of `1`, so we can just pass `delta` into the `t` value, which is the same as `1 * delta`. 

!!! note ""
    If you change this to `2 * delta` the camera will arrive much sooner, and if you make it less like `0.5 * delta` the camera will take longer to catch up to the player.

We'll also add a check to make sure we arrive and don't bounce around the target value. This `0.3` value was chosen arbitrarily.

```js hl_lines="9 11 13"
update_camera(delta) {

    //the camera is positioned half the view away
  var offset = (app.world_width / 2).floor
    //this is the target move position for the camera
  var target = Transform.get_pos_x(_player) - offset

    //get the current camera position
  var pos = ...
    //interpolate the current pos to the target pos 
  var new_pos = Math.lerp(pos.x, target, delta)
    //if we're close enough, stop trying
  if((new_pos - target).abs < 0.3) new_pos = target

} //update_camera
```

### updating the position

!!! note ""
    For reasons, we want to interpolate the _unsnapped_ value of the camera position, not the snapped one.
    We can do this with the (wip) `Transform.get_pos_world_unsnapped(app.camera)` function.
    This returns the x position without snapping applied. This is our _current_ position.

We can use `Transform.set_pos_x` to update the position, and for other reasons, 
we'll want to call `Transform.sync(app.cammera)` after that. This will make sure the camera has the latest position.

```js hl_lines="16 18"
update_camera(delta) {

    //the camera is positioned half the view away
  var offset = (app.world_width / 2).floor
    //this is the target move position for the camera
  var target = Transform.get_pos_x(_player) - offset

    //if we want smooth camera movement, we need to use
    //the unsnapped position to move the camera
  var pos = Transform.get_pos_world_unsnapped(app.camera)
    //interpolate the current pos to the target pos 
  var new_pos = Math.lerp(pos.x, target, delta)
    //if we're close enough, stop trying
  if((new_pos - target).abs < 0.3) new_pos = target
    //update the camera position
  Transform.set_pos_x(app.camera, new_pos)
    //make sure the camera view is updated from the transform
  Transform.sync(app.camera)

} //update_camera
```

!!! tip "run the game to see the results"

If you run the game you should see something similar to this. 
And, as you'll notice, we can see outside the area, so we also want to limit the camera which we'll do next.

<video preload="auto" autoplay controls="" loop="loop" style="max-width:100%; width:auto; margin:auto; display:block;">  
  <source src="../../images/tutorial/intro/camera-follow-2.mp4" type="video/mp4"></source>
</video>

## fetching an entity

Limiting the camera position is fairly simple, but instead of using a fixed size, let's read
the size of the background image we created. To do that, we need access to the `background_image` entity 
that we created in a previous step of the tutorial, which is loaded via `Scene.load`. 

There are a couple ways to do this, but for now we'll use the simplest, which is `Entity.get_named(world: World, name: String)`.
Since we know the name, and we know there is only one entity named background, this works for now.

We'll add a single line to our `ready` function to grab it from `app.world`, which is the game world where the scene is loaded.
And we'll store it in a field called `_background` so we can reference it later.

```js hl_lines="13"
construct ready() {

  super("ready!")

  app = App.new()

    //set the background color
  app.color = [0,0,0,1]
    //make sure the camera is snapped to whole pixels
  Transform.set_snap(app.camera, 1, 1)

  Scene.load(app.world, "scene/area1")
  _background = Entity.get_named(app.world, "background_image")

  create_player()

} //ready
```

## limiting the camera

The camera x position on the left side is limited to `0`, which makes that side easy.
The right hand side of the level is based on the width of the background image `Sprite`.

And, as before, we have a camera offset to consider, but this time it's not half the view, it's the entire view area.
Once we have the min and max values, we can use the Wren `value.clamp(min, max)` method on a number to clamp a value.

```js hl_lines="9 11"
update_camera(delta) {

    //the camera is positioned half the view away
  var offset = (app.world_width / 2).floor
    //this is the target move position for the camera
  var target = Transform.get_pos_x(_player) - offset

    //the game area is based on the background size
  var area_width = Sprite.get_width(_background) - app.world_width
    //so don't let it go outside the area
  target = Math.clamp(target, 0, area_width)

    //if we want smooth camera movement, we need to use
    //the unsnapped position to move the camera
  var pos = Transform.get_pos_world_unsnapped(app.camera)
    //interpolate the current pos to the target pos 
  var new_pos = Math.lerp(pos.x, target, delta)
    //if we're close enough, stop trying
  if((new_pos - target).abs < 0.3) new_pos = target
    //update the camera position
  Transform.set_pos_x(app.camera, new_pos)
    //make sure the camera view is updated from the transform
  Transform.sync(app.camera)

} //update_camera
```

!!! tip "run the game to see the results"

You'll see now the camera is locked to the area bounds, and we can't move too far to the right based on our earlier limits for the player movement.

<video preload="auto" autoplay controls="" loop="loop" style="max-width:100%; width:auto; margin:auto; display:block;">  
  <source src="../../images/tutorial/intro/camera-follow-3.mp4" type="video/mp4"></source>
</video>

## fixing the player start

In the beginning part, we hardcoded a value for the player y position, and put them center screen. 
For this area, we also actually want the player to start on the other side of the area.

A better way to achieve this is to make the start position part of the area itself using the editor, and then fetch that from the scene after loading.
The editor side should be familiar by now, we'll make an entity for the start position of the player, attach a `Transform`, set it's position and save the scene. The code side is the same as before, we'll use `Entity.get_named` again for this.

Since we're already doing this, let's do all of these at the same time:

  - the player start position 
  - the min and max positions the player can walk
  - the min and max positions for the camera (rather than using the image size)

!!! tip "open the `scene/area1` scene in the editor"

The first step, **make a new layer** in our area1 scene, and call it `area`. This is a layer for "things related to the area itself".
We'll create 5 entities, and give them the following names and `Transform` `x, y` values:

  - **player.start** - `740, 26`
  - **player.min**   - `45, 26`
  - **player.max**   - `836, 26`
  - **camera.min**   - `0, 0`
  - **camera.max**   - `960, 0`

![](../images/tutorial/intro/camera-follow-4.png){: loading=lazy }
  
### fetching the entities

Since we're doing a lot more now, let's start by moving this logic into a new method called `load_area()` and call that from `ready` instead.

There's one important factor now: we need to create the player **before** loading the area, because the area will need to refer to the player later.

Inside that method, we'll fetch each of the entities, and store their positions in fields we can reach elsewhere in the class.
We're storing the limits in a vector, like this `[min, max]`, and we only care about the `x` value. The start point is just the position we'll store.

```js hl_lines="13 17"
construct ready() {

  super("ready!")

  app = App.new()

    //set the background color
  app.color = [0,0,0,1]
    //make sure the camera is snapped to whole pixels
  Transform.set_snap(app.camera, 1, 1)

  create_player()
  load_area()

} //ready

load_area() {

  Scene.load(app.world, "scene/area1")

  var player_start = Entity.get_named(app.world, "player.start")
  var player_min = Entity.get_named(app.world, "player.min")
  var player_max = Entity.get_named(app.world, "player.max")
  var camera_min = Entity.get_named(app.world, "camera.min")
  var camera_max = Entity.get_named(app.world, "camera.max")
  
  _player_start = Transform.get_pos(player_start)

  _player_limits = [
    Transform.get_pos_x(player_min),
    Transform.get_pos_x(player_max)
  ]

  _camera_limits = [
    Transform.get_pos_x(camera_min),
    Transform.get_pos_x(camera_max)
  ]

} //load_area
```

### updating the camera

We can change the code inside `update_camera` to clamp to our new limits.
Don't forget the camera offset on the max value.

```js hl_lines="8"
update_camera(delta) {

    //the camera is positioned half the view away
  var offset = (app.world_width / 2).floor
    //this is the target move position for the camera
  var target = Transform.get_pos_x(_player) - offset
    //don't let the camera go outside the area
  target = target.clamp(_camera_limits.x, _camera_limits.y - app.world_width)

  ...
}
```

### updating the player limits

Inside our tick function, we update the limits as well to use the new values.

```js hl_lines="8 9"
tick(delta) {

  var mouse = app.mouse

  if(Input.mouse_state_released(MouseButton.left)) {

      //limit movement to the area within our level
    if(mouse.x < _player_limits.x) mouse.x = _player_limits.x
    if(mouse.x > _player_limits.y) mouse.x = _player_limits.y

    ...
  }

  ...
```

### updating the player start

Previously, we set the player position inside of `create_player`, which won't work since we're now creating the player, and then loading the area.
If we try to access the `_player_start` value inside `create_player`, it's too early. 

Instead, we'll create a method called `reset_player` to move the player to the start location, which we can use later if needed to reset the area.
We call it _after_ loading the area.

```js hl_lines="14 18"
construct ready() {

  super("ready!")

  app = App.new()

    //set the background color
  app.color = [0,0,0,1]
    //make sure the camera is snapped to whole pixels
  Transform.set_snap(app.camera, 1, 1)

  create_player()
  load_area()
  reset_player()

} //ready

reset_player() {

    //set the position to the player start position
  Transform.set_pos(_player, _player_start.x, _player_start.y, 2)

} //reset_player
```

!!! tip "run the game to see the results"

With that all done, you'll also notice the camera starts off screen and zooms over the player, which is a nice effect.
(Later we'll add a fade in so it feels smoother).

<video preload="auto" controls="" style="max-width:100%; width:auto; margin:auto; display:block;">  
  <source src="../../images/tutorial/intro/camera-follow-5.mp4" type="video/mp4"></source>
</video>


## next up

In the next step, we'll start with the gameplay of interacting with the terminals and learn another way to fetch entities from the world.
