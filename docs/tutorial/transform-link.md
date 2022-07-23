![](../images/luxe-dark.svg){width="96em"}

# transform link

!!! example "outcome"
    In this step we'll see how to use a named input event to pick up the jar 
    and interact with the terminals. We'll also use `Transform.link` to make the 
    jar follow the player as they move around.

## input events

In [Input Handling](../input-handling) we mentioned there are named input events.

We're going to add a named input event named `interact` which we'll bind to some keys.

!!! note ""
    At the moment this is more manual data files than UI based. There will be a
    nice UI on top as well!

### adding a named event

In your code editor, looking inside `outline/inputs.input.lx` you'll find an input map
with a few existing entries.

```js
input = {
  map = {
    left = { keys = ["key_a", "left"] }
    right = { keys = ["key_d", "right"] }
    up = { keys = ["key_w", "up"] }
    down = { keys = ["key_s", "down"] }

    //we'll add one here

    next = {
      keys = ["key_x", "up", "key_w", "space", "enter", "escape"]
      mouse = ["left", "right"]
    }
  }
}
```

We'll add one called interact. 
Each of these is a list, so we'll bind it to the ++space++ key and the ++c++ key.
We'll also bind ++rbutton++ on the mouse and the first button on the gamepad.

!!! note ""
    The key names match the [Key](../../api/input/#key) class from `luxe: input` in the API.
    Note that atm gamepad buttons are numbers, but will be clearer later.

```js hl_lines="8 9 10 11 12"
input = {
  map = {
    left = { keys = ["key_a", "left"] }
    right = { keys = ["key_d", "right"] }
    up = { keys = ["key_w", "up"] }
    down = { keys = ["key_s", "down"] }

    interact = {
      keys = ["space", "key_c"]
      mouse = ["right"]
      gamepad = [0]
    }

    next = {
      keys = ["key_x", "up", "key_w", "space", "enter", "escape"]
      mouse = ["left", "right"]
    }
  }
}
```

### using the named event

To use the named event we use `Input.event_ended(event: String)`, which is still using the query style (rather than callback style).

This is another good use case for an enum, the outline has already provided one in a file called `inputs.wren`. 
This file contains nothing unfamiliar, we just make those names available via a class:

```js

class Inputs {
  static left     { "left" }
  static right    { "right" }
  static up       { "up" }
  static down     { "down" }
  static interact { "interact" }
  static next     { "next" }
}
```

Import that in our `area1.wren` file at the top and it's ready to use:

```js hl_lines="3"
import "random" for Random
import "arcade: modifier/arcade" for Arcade, CollisionEvent, ShapeType
import "inputs" for Inputs
```

Because we're using the query style, we'll want to check for the event every frame, inside `tick`.
Inside the `tick` method of our `area1.wren` file, we'll call a new method called `update_interaction()`.
This is where we'll check for all interactions in this area of the game.

```js hl_lines="3 11"
update_interaction() {

  var interacted = Input.event_ended(Inputs.interact)

} //update_interaction

tick(delta) {

  if(!_player) return

  update_interaction()

  ...

} //tick
```

## collecting the jar

### interact with the jar

Previously we created a `_jar_state` field and stored a `State` in it. 
We'll use this and the `interacted` variable from above to react to different things.

If the jar is collectable (we're in range) and we interact with it, 
we call a new method called `collect_jar()` which we'll implement next.

```js hl_lines="1 9 10 11"
collect_jar() {

}

update_interaction() {

  var interacted = Input.event_ended(Inputs.interact)

  if(interacted && _jar_state == State.collectable) {
    collect_jar()
  }

} //update_interaction
```

### updating jar state

To start with collecting the jar, we've got a few things to do:

First we'll update the `_jar_state` field. 
Second, we'll turn off the shine animation for the jar.

And then we'll disable physics for the jar. 
Since we are gonna control the position of the jar,
we don't want gravity affecting it.

```js hl_lines="4 7 10"
collect_jar() {

    //We now have the jar in our hand (but it's locked)
  _jar_state = State.in_hand_locked

    //turn off the animation for now, we'll need it again later
  make_jar_shine(false)

    //turn off physics for the jar so that it follows the player
  Arcade.set_dynamic(_jar, false)

} //collect_jar
```

### transform spaces

When you link two transforms together, it means that the one will be connected to the other one.
This is often referred to as a parent/child relationship, where the parent affects the child transform.
If the parent changes position, all children follow, and all children of their children and so on.

We use `Transform.link(entity: Entity, target: Entity)` to connect the jar to the player.
The jar would be the entity, the target would be the player. 

When the jar is connected, its transform values like position become relative to the parent. When position
is `0,0` the child matches the parent position exactly. If it was `-10, 0` it would be 10 units to the left of the parent,
regardless of where the parent was positioned (assuming no scale/rotation on the parent). 

!!! note ""
    This difference is called `world space` versus `local space`. Local space is relative to the parent, world space is relative to the world.
    When a transform has no link, its local space = world space. By default, methods operate on local space,
    but you can use methods like `Transform.set_pos_world` to explicitly refer to world space instead.

### linking the transforms

We have two steps here, one is to link the jar to the player.
The second step is to update the local position to match our expectations.
To do that we just set the position normally, but with a value relative to the player.

Since the player can face different directions, and we want the jar to be hovering in front of the player,
we'll offset it by 16 units (pixels in our case) to whichever side matches the player direction. 
We can ask the player sprite for the flip value to decide.

```js hl_lines="14 15 18 21"
collect_jar() {

    //We now have the jar in our hand (but it's locked)
  _jar_state = State.in_hand_locked

    //turn off the animation for now, we'll need it again later
  make_jar_shine(false)

    //turn off physics for the jar so that it follows the player
  Arcade.set_dynamic(_jar, false)

    //we'll offset the position of the jar based 
    //on the direction the player is facing
  var offset = -16
  if(Sprite.get_flip_h(_player)) offset = 16

    //link the jar to the player, so that it follows them around
  Transform.link(_jar, _player)
    //set the jar position. This position is now relative to the player,
    //so we use our offset for the x value, and a fixed value for the y
  Transform.set_pos(_jar, offset, 40)

} //collect_jar
```

### bobbing the jar

To make it look a bit more like the jar is hovering being held by the player, we'll apply an animation to the jar itself.

Before we can play an animation on it, we'll have to add an animation modifier to the jar. 
Inside `create_jar` we'll do just that with `Anim.create`:

```js hl_lines="11"
create_jar() {

  if(_jar) Entity.destroy(_jar)

  _jar = Prototype.create(_world, "prototype/jar", "jar")

  var jar_start = Entity.get_named(_world, "jar.start")
  var jar_pos = Transform.get_pos(jar_start)
  Transform.set_pos(_jar, jar_pos.x, jar_pos.y, jar_pos.z)

  Anim.create(_jar)

  Arcade.create(_jar)
  ...

} //create_jar
```

And back inside `collect_jar()` at the end, we'll play the animation:

```js hl_lines="6 7"
collect_jar() {
  
  ...

    //Make the jar bounce a little up and down
  var bob = Anim.play(_jar, "anim/bob")
  Anim.set_rate(_jar, bob, 0.5)

} //collect_jar
```

!!! tip "run the game and collect the jar"

<video preload="auto" autoplay controls="" loop="loop" style="max-width:100%; width:auto; margin:auto; display:block;">  
  <source src="../../images/tutorial/intro/transform-link-0.mp4" type="video/mp4"></source>
</video>

### fading the symbols

Currently the symbols on the jar are always visible. 
Instead, we want to set those to invisible in the prototype, and then fade them in when the jar is collected.

Again inside `collect_jar()` at the end, we'll play the fade animation on the symbol:

```js hl_lines="10 11"
collect_jar() {
  
  ...

    //Make the jar bounce a little up and down
  var bob = Anim.play(_jar, "anim/bob")
  Anim.set_rate(_jar, bob, 0.5)

    //Fade the symbol on the jar in, so we can see it
  var symbol = Prototype.get_named(_jar, "visual.symbol")
  Anim.play(symbol, "anim/fade")

} //collect_jar
```

In the luxe editor, open the prototype from the world context, and set the Sprite color value to `1 1 1 0` on the `visual.symbol` entity.

![](../images/tutorial/intro/transform-link-1.png){: loading=lazy }

This will mean the symbols aren't visible when creating the jar, but will fade in when we collect the jar.

<video preload="auto" autoplay controls="" loop="loop" style="max-width:100%; width:auto; margin:auto; display:block;">  
  <source src="../../images/tutorial/intro/transform-link-2.mp4" type="video/mp4"></source>
</video>

### fixing the offset

You'll notice that when the player faces either direction and collects the jar, the offset is correct.
When the player moves and faces the other direction, it becomes offset on the wrong side.

To fix that there's two things to consider. The first is that the jar overlap code is still running
while we're holding the jar, which we don't want. We'll add a simple check to `on_jar_overlap` to prevent that.

Because the state enum value is just a number, we can use `>` to skip the overlap code when not in the `none` or `pickupable` state.

```js hl_lines="4"
on_jar_overlap(event, other) {

  if(other != _player) return
  if(_jar_state > State.pickupable) return

  ...

} //on_jar_overlap
```

Now we can add some new code that runs every frame to keep the jar in place.
We'll start by making a helper method that returns true if the player is holding the jar.
This will use simple checks:

```js
should_jar_follow_player() {
  if(_jar_state == State.collecting) return true
  if(_jar_state == State.in_hand_locked) return true
  if(_jar_state == State.in_hand_unlockable) return true
  if(_jar_state == State.in_hand_unlocked) return true
  if(_jar_state == State.in_hand_openable) return true
  return false
}
```

We'll create a method called `update_jar`, and call it from `tick`.

There's a few things: we don't want to access the jar if it doesn't exist yet.
This is what `Entity.valid(entity: Entity)` is for.

Then we check if we should follow the player. 

And finally, we set the x position. We only set x because the y position
is being changed by the bob animation, and we don't want it to be changed from here.

```js hl_lines="21"
update_jar() {

    //Don't do anything with no jar
  if(Entity.valid(_jar) == false) return
    //Don't do anything if we're not holding the jar
  if(should_jar_follow_player() == false) return

    //offset the position of the jar based 
    //on the direction the player is facing
  var offset = -16
  if(Sprite.get_flip_h(_player)) offset = 16
  Transform.set_pos_x(_jar, offset)

} //update_jar

tick(delta) {

  if(!_player) return

  update_interaction()
  update_jar()

  ...

} //tick
```

<video preload="auto" autoplay controls="" loop="loop" style="max-width:100%; width:auto; margin:auto; display:block;">  
  <source src="../../images/tutorial/intro/transform-link-3.mp4" type="video/mp4"></source>
</video>

## next up

In the next steps we'll start to wrap up the gameplay using everything we've already learnt, adding a fade in,
interacting with the terminals and exiting the level.