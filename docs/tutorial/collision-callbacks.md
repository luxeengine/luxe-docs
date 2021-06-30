![](../images/luxe-dark.svg){width="96em"}

# collision callbacks

!!! example "outcome"
    In this step we'll see how to use a collision callback, 
    to understand how they work generally, and we'll start
    keeping track of the state the jar is in, so we can
    implement the rest of the gameplay.

## player collider

In order for the player to be able to collide with the jar collider, we need to add a collider to the player as well.
The player is created in code, so we'll add some code in the `create_player` method in `game.wren`.

Before we can use the `Arcade` modifier though, we need to import it, we can do this at the top of the file. 
We'll also import an enum for a type of shape from the same place, and one for the type of collision event.

```js hl_lines="3"
import "outline/app" for App
import "modifier/move" for Move
import "arcade: modifier/arcade" for Arcade, ShapeType
```

!!! note ""
    Import and assets from modules are specified in the form of `module: file` or `module: folder/file`.
    so `arcade: modifier/arcade` is a file called `arcade.wren`, inside a `modifier` folder in the `arcade` module.

Now we can use the Arcade class to create the collider on the player. Same as usual, we attach it with `create`.

```js hl_lines="11 13 15 17"
create_player() {

  ...

    //create an animation modifier to play animations
  Anim.create(_player)
    //play the idle animation asset
  Anim.play(_player, "anim/player.idle")

    //create a collider for collision
  Arcade.create(_player)
    //we'll use a circle shape
  Arcade.set_shape_type(_player, ShapeType.circle)
    //the radius is well defined
  Arcade.set_radius(_player, 32)
    //make sure it's not solid, since it behaves as a trigger
  Arcade.set_solid(_player, false)

} //create_player
```

If you run the game and then enable the debug view again, you'll see the player now has a circle collider at the base of the player.
This is how we'll know when the player is close enough to the jar to pick it up.

![](../images/tutorial/intro/player-collision-0.png){: loading=lazy }

## prototype contents

Our jar prototype contains an entity for the collider shape, which is what we want to attach a callback to. 
We need to grab the entity, which we can do with `Prototype.get_named(prototype: Entity, name: String)`.

Inside `create_jar` in `area1.wren` at the end of the method, we'll add a line to do that.

```js hl_lines="6"
create_jar() {

  ...

    //fetch the collider entity from the jar prototype
  var collider = Prototype.get_named(_jar, "collider.collect")

} //create_jar
```

## collision callbacks

The goal here is to not just understand how collision callbacks work for `arcade`, 
but the concepts involved apply to most collision libraries, including the built in bigger physics modifiers in luxe.

Specifically, we want to be intentional about what we're colliding with. 
For example, the jar has a rectangle collider we added in editor, and it has a pickup circle collider.
If we're not careful, we'll respond to collision events with the jar itself, so we want to isolate the logic to just include the player.

Often collision libraries provide filters, but it's not all that complicated, we just ignore anything that isn't the player.

`Arcade` provides a `add_collision_callback` method that we can use to listen for when it collides with stuff.

This will call a method `on_jar_overlap` we'll implement next. We hand it the `other` entity (the one we collided with), 
and the `event` which is an arcade `CollisionEvent` for `begin`/`end` and `overlap`. The `overlap` event is 
sent every frame that the two colliders overlap, and the others are self explaining.

```js hl_lines="6"
create_jar() {

  ...

    //fetch the collider entity from the jar prototype
  var collider = Prototype.get_named(_jar, "collider.collect")
    //listen for collisions with the jar
  Arcade.add_collision_callback(collider) {|entity, other, state, normal, overlap|
    on_jar_overlap(event, other)
  }

} //create_jar
```

We'll add `on_jar_overlap` and inside it, we'll just print the information from the collisions.

!!! note ""
    The Strings.get is a bit awkward, but when you get strings back from the engine like a name, 
    at the moment you need to ask for the actual string, since what it returned is a hashed value (number) 
    that represents the string. 

```js
on_jar_overlap(event, other) {

  var type = CollisionEvent.name(event)
  var name = Strings.get(Entity.get_name(other))
  System.print("jar collide type '%(type)' with entity '%(name)'")

} //on_jar_overlap
```

When you create a jar, it'll now print a lot of noise to the console. You'll see the jar collider is colliding with the jar itself and the ground.

```js
jar collide type 'overlap' with entity 'jar'
jar collide type 'begin' with entity 'collider.ground'
jar collide type 'overlap' with entity 'jar'
jar collide type 'overlap' with entity 'collider.ground'
jar collide type 'overlap' with entity 'jar'
```

We only care about the player, so we just ignore anything else.

```js
on_jar_overlap(event, other) {

  if(other != _player) return

  var type = CollisionEvent.name(event)
  var name = Strings.get(Entity.get_name(other))
  System.print("jar collide type '%(type)' with entity '%(name)'")

} //on_jar_overlap
```

This will print only when the player comes close to the jar. 
We're almost ready to pick up the jar.

```js
jar collide type 'begin' with entity 'player'
jar collide type 'overlap' with entity 'player'
jar collide type 'end' with entity 'player'
```

## jar states

The logic in our game is based on the jar being in a certain state, like none,
ready to be picked up, picked up and locked, unlocked and ready to open.

We'll add another enum for the state of the jar:

```js
class State {
  static none                 { 0 }
  static pickupable           { 1 }
  static collectable          { 2 }
  static collecting           { 3 }
  static in_hand_locked       { 4 }
  static in_hand_unlockable   { 5 }
  static in_hand_unlocked     { 6 }
  static in_hand_openable     { 7 }
  static opened               { 8 }
}
```

And inside the `new` method of our scene script in `area1.wren`, we add a new call to set up the state of the jar.
While we're there, we add the `setup_jar` method at the same time, initializing some values, including the `_jar_state` field.

```js hl_lines="7 11"
construct new(world) {

  _world = world
  _player = Entity.get_named(_world, Name.player)
  
  setup_terminals()
  setup_jar()

} //new

setup_jar() {
  _jar = null
  _jar_state = State.none
  _jar_flip = false
}
```

Inside `on_jar_overlap` we're gonna update the `_jar_state` based on whether we're in range or not.
If the overlap callback event is `begin` or `overlap`, it means we're close enough to pick up the jar.

We'll set the jar state to `pickupable` when we're not in range, and `collectable` when we're in range.

!!! note ""
    If it's just on the ground, it's a pickup, but we can't collect it just yet. Once we're in range it can be collected.
    This is the distinction between the two!

```js
on_jar_overlap(event, other) {

  if(other != _player) return

    //if it's a begin or overlap, we can interact with the jar
  var can_interact = state != CollisionEvent.end

    //pickupable means it's on the floor but we're not in range, 
    //e.g we can go pick it up. collectable is when we're in range
  var goal_state = State.collectable
  if(can_interact == false) goal_state = State.pickupable

    //already in the goal state? nothing to do
  if(_jar_state == goal_state) return

    //store the state we're changing to
  _jar_state = goal_state

} //on_jar_overlap
```

## making the jar shine

To show the player that the jar can be picked up, we'll animate it with a nice shiny animation.

This is fairly familiar, we'll add a method called `make_jar_shine`, and inside we'll 
grab the visual entity from the prototype, and play an animation on it! 

If we're not in range, we want to stop all animations on the visual of the jar, 
and reset the state. The anim modifier has this method for that: `Anim.stop_all(entity: Entity, reset: Bool)`.

```js hl_lines="20 24"
on_jar_overlap(event, other) {

  if(other != _player) return

    //if it's a begin or overlap, we can interact with the jar
  var can_interact = event != CollisionEvent.end

    //pickupable means it's on the floor but we're not in range, 
    //e.g we can go pick it up. collectable is when we're in range
  var goal_state = State.collectable
  if(can_interact == false) goal_state = State.pickupable

    //already in the goal state? nothing to do
  if(_jar_state == goal_state) return

    //store the state we're changing to
  _jar_state = goal_state

    //show the animation if we can interact with it 
  make_jar_shine(can_interact)

} //on_jar_overlap

make_jar_shine(must_shine) {

    //fetch the visual from the jar
  var visual = Prototype.get_named(_jar, "visual")
    //if we must shine, play the animation to do that!
  if(must_shine) {
    Anim.play(visual, "anim/jar.shine")
  } else {
    Anim.stop_all(visual, true)
  }

} //make_jar_shine
```

Now when we come near the jar, it animates to indicate interactivity.

<video preload="auto" autoplay controls="" loop="loop" style="max-width:100%; width:auto; margin:auto; display:block;">  
  <source src="../../images/tutorial/intro/collision-callbacks-0.mp4" type="video/mp4"></source>
</video>

## next up

We're gonna pick up the jar, unlock it, and open it using the jar states. 