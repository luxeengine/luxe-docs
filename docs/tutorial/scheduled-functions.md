![](../images/luxe-dark.svg){width="96em"}

# scheduled functions

!!! example "outcome"
    In this step we'll use the world clock to schedule
    a function at some point in the future, and break open the jar.

## opening the jar

The next mechanic is opening the jar. This fits easily into the code we already have, we'll add a check to `enter_terminal`/`exit_terminal` and a check to `update_interaction`.

### terminal enter/exit

At the end of `enter_terminal` we'll add the check for the terminal id:

```js hl_lines="7 8 9 10"
enter_terminal(terminal) {

  ...

    //if we're holding the decoded jar, and we're in range of the
    //terminal that matches the jar symbol, we can open the jar
  if(_jar_state == State.in_hand_unlocked && id == _jar_symbol) {
    make_jar_shine(true)
    _jar_state = State.in_hand_openable
  }

} //enter_terminal
```

And like before, in `exit_terminal` we undo those changes, by adding to the end:

```js hl_lines="6 7 8 9"
exit_terminal(terminal) {

  ...

    //if the jar was unlocked, also reset the state
  if(_jar_state == State.in_hand_openable && id == _jar_symbol) {
    make_jar_shine(false)
    _jar_state = State.in_hand_unlocked
  }

} //exit_terminal
```

### the interaction

Inside `update_interaction`, we'll call a new method called `open_jar()`:

```js hl_lines="1 17 18 19"
open_jar() {
  
}

update_interaction() {

  var interacted = Input.event_ended(Inputs.interact)

  if(interacted && _jar_state == State.collectable) {
    collect_jar()
  }    
  
  if(interacted && _jar_state == State.in_hand_unlockable) {
    unlock_jar()
  }

  if(interacted && _jar_state == State.in_hand_openable) {
    open_jar()
  }

} //update_interaction
```

### open jar setup

There's a few things we want to do when we open the jar.

What we want to have happen, is the jar flies away from the player slowly, like up and to the right,
as if it was moving on it's own. We use the `Move` modifier to do that, and make a
temporary target entity to move toward. 

When it gets there, we'll clean up that target entity, play a jar breaking animation, 
create a lid that flies off using physics, and create a firefly that follows the player.

When the jar breaking animation ends, we'll destroy the jar instance, scramble the terminals, and schedule a new jar.

Phew. We'll do this in steps though. 

The starting part is all familiar stuff! Create an entity, play animations, that kinda thing:

```js
open_jar() {

    //update the jar state
  _jar_state = State.opened

    //stop the jar from shining
  make_jar_shine(false)

    //turn off the bobbing animation
  Anim.stop_all(_jar, true)

    //get the current jar position
  var pos = Transform.get_pos_world(_jar)
    //unlink the jar from the player first
  Transform.unlink(_jar)
    //set the position for the jar, which now refers 
    //to world space since the jar has no parent
    //this makes the jar stay in the same place
  Transform.set_pos(_jar, pos.x, pos.y, pos.z)

    //create a target entity for the jar to move toward
  var target = Entity.create(_world, "jar.target")
    //give it a transform
  Transform.create(target)
    //calculate the offset based on the facing direction
  var flip = Sprite.get_flip_h(_player)
  var offset = -24
  if(flip) offset = 24
    //move the target to somewhere up and right (or up and left)
  Transform.set_pos(target, pos.x + offset, pos.y + 16, pos.z)

    //now we grab the symbol on the jar
  var symbol = Prototype.get_named(_jar, "visual.symbol")
    //fade it out!
  var fade = Anim.play(symbol, "anim/fade")
  Anim.set_rate(symbol, fade, Anim.get_rate(symbol, fade) * -1)

    //and indicate we've done something to the jar
  create_interact(_active_terminal)
  create_interact(symbol)

} //open_jar
```

If you collect the jar, you'll now be able to unlock it using the symbol terminal, and then open it using the terminal with the matching symbol (if you go to the wrong terminal it won't shine or interact).

You'll notice that the jar just kinda stops following the player and does nothing. We'll add the move next!

<video preload="auto" autoplay controls="" loop="loop" style="max-width:100%; width:auto; margin:auto; display:block;">  
  <source src="../../images/tutorial/intro/wrap-up-2.mp4" type="video/mp4"></source>
</video>

### a floaty jar

To make the jar move, we need a `Move` modifier attached to it.
At the top of our file, we add another import, 

```js hl_lines="4"
import "random" for Random
import "arcade: modifier/arcade" for Arcade, CollisionEvent, ShapeType
import "inputs" for Inputs
import "modifier/move" for Move
```

And inside `create_jar` we attach it to the jar:

```js hl_lines="12"
create_jar() {

  if(_jar) Entity.destroy(_jar)

  _jar = Prototype.create(_world, "prototype/jar", "jar")
  _jar_state = State.none

  var jar_start = Entity.get_named(_world, "jar.start")
  var jar_pos = Transform.get_pos(jar_start)
  Transform.set_pos(_jar, jar_pos.x, jar_pos.y, jar_pos.z)

  Move.create(_jar)

  Anim.create(_jar)

  ...

} //create_jar
```

Now we can use it from `open_jar`, at the end. 
We'll add a new method called `break_jar` and call it from inside the function that Move calls for us when arriving.

In break jar, we'll play the jar opening animtion on the jar visual. 

!!! note ""
    At the moment we need to also update the sprite size to match the animation.

```js hl_lines="1 4 5 6 16 17 18 19"
break_jar() {

    //get the jar visual, and play the breaking animation
  var visual = Prototype.get_named(_jar, "visual")
  var open = Anim.play(visual, "anim/jar.open")
  Sprite.set_size(visual, 32, 32)

} //break_jar

open_jar() {

  ...

    //move to the target, with 0,0 offset, and a speed of 8 pixels per second
    //when we arrive, clean up, and break the jar
  Move.to(_jar, target, [0,0], 8) {
    Entity.destroy(target)
    break_jar()
  }

} //open_jar
```

Now when we open the jar, it floats away from the player, and then breaks open.

<video preload="auto" autoplay controls="" loop="loop" style="max-width:100%; width:auto; margin:auto; display:block;">  
  <source src="../../images/tutorial/intro/wrap-up-3.mp4" type="video/mp4"></source>
</video>

### the jar cycle

When the breaking animations ends, we'll call a new method called `next_jar()`:

```js hl_lines="1 13 14 15 16 17"
next_jar() {

} //next_jar

break_jar() {
  
    //get the jar visual, and play the breaking animation
  var visual = Prototype.get_named(_jar, "visual")
  var open = Anim.play(visual, "anim/jar.open")
  Sprite.set_size(visual, 32, 32)

    //wait for the open animation to end
  Anim.on_event(visual, open) {|entity, anim, time, value, track_type, track, event|
    if(event == AnimEvent.complete) {
      next_jar()        
    } //if complete
  } //anim on_event

} //break_jar
```

Inside `next_jar` we can destroy the jar itself, and scramble the terminals so that the next jar is random again.

What we also do is schedule a function to be called in the future using `World.schedule(world: World, time_from_now: Num, fn: Fn)`.
This will call our function in `time_from_now` seconds. We can use a random number to make it slightly more random.

!!! note ""
    Because we used `World` to schedule this function, it's subject to the rate that the world is updating. For example if we slow down or speed up the world time, or pause it, the function will happen according to that rate. You can use `Frame.schedule` from `luxe: game` to schedule against unscaled time.

We only want to create a new jar if the player needs one to finish the area. In this case, the player needs to open 3 jars to free
3 fireflies. If there aren't 3 fireflies, we create a new jar. The fireflies are tagged with the `firefly` name which is how we check how many there are.

```js
next_jar() {

    //destroy the jar
  Entity.destroy(_jar)
  _jar = null
    
    //randomize the terminals, so the next jar is different
  scramble_terminals()

    //if there aren't 3 fireflies, create another jar
  var fireflies = Tags.list(_world, Name.firefly)
  if(fireflies.count < 3) {
    var delay = RNG.float(2, 5)
    World.schedule(_world, delay) { create_jar() }
  }

} //next_jar
```

At the moment we don't have any fireflies, so this will just keep creating jars. The video shows this in motion.

You'll notice that the terminal all the way to the left was the decoding terminal, but after the jar opened it was a static terminal.
This is because we scrambled them so the player has to find the right terminal.

<video preload="auto" autoplay controls="" loop="loop" style="max-width:100%; width:auto; margin:auto; display:block;">  
  <source src="../../images/tutorial/intro/wrap-up-4.mp4" type="video/mp4"></source>
</video>

## creating a lid

We're going to add a new method called `create_lid()` and call it from the `break_jar` method:

```js hl_lines="1 12"
create_lid() {

}

break_jar() {
  
    //get the jar visual, and play the breaking animation
  var visual = Prototype.get_named(_jar, "visual")
  var open = Anim.play(visual, "anim/jar.open")
  Sprite.set_size(visual, 32, 32)

  create_lid()

    //wait for the open animation to end
  Anim.on_event(visual, open) {|entity, anim, time, value, track_type, track, event|
    if(event == AnimEvent.complete) {
      next_jar()        
    } //if complete
  } //anim on_event

} //break_jar
```

When the jar breaks open, it'd be nice to have a lid fly off and fall to the ground.
Doing this uses everything we've learned so far and looks like this:

```js
create_lid() {

    //the lid entity
  var lid = Entity.create(_world, "jar.lid")
    //attach a sprite for the lid
  Sprite.create(lid, Assets.material("material/jar.lid"), 10, 6)

    //position it on the jar
  var pos = Transform.get_pos(_jar)
  Transform.create(lid)
  Transform.set_pos(lid, pos.x, pos.y + 4, 3)

    //calculate a random velocity for the lid 
    //to fly away with, using the player facing 
  var flip = Sprite.get_flip_h(_player)
  var sign = -1
  if(flip) sign = 1
  var velocity = [
    RNG.int(32 * sign, 64 * sign), //x
    RNG.int(128, 180)              //y
  ]

    //attach and configure the arcade physics modifier 
  Arcade.create(lid)
  Arcade.set_shape_type(lid, ShapeType.circle)
  Arcade.set_radius(lid, 5)
  Arcade.set_vel(lid, velocity)
  Arcade.set_acc(lid, [0, -400])
  Arcade.set_drag(lid, [1, 1])
  Arcade.set_restitution(lid, 0.6)

    //attach an animation to fade the lid out
  Anim.create(lid)
    //wait 4 seconds before fading out,
    //and when complete, destroy the lid
  World.schedule(_world, 4) {
    var fade = Anim.play(lid, "anim/fade")
    Anim.set_rate(lid, fade, Anim.get_rate(lid, fade) * -1)
    Anim.on_event(lid, fade) {|entity, anim, time, value, track_type, track, event|
      if(event == AnimEvent.complete) {
        Entity.destroy(lid)
      } //complete event
    } //Anim.on_event
  } //World.schedule

} //create_lid
```

Now when a jar opens, we get a lid flying away in a satisfying way, bouncing and then disappearing.

<video preload="auto" autoplay controls="" loop="loop" style="max-width:100%; width:auto; margin:auto; display:block;">  
  <source src="../../images/tutorial/intro/create-lid-0.mp4" type="video/mp4"></source>
</video>

## creating a firefly

Like with the lid, we're going to add a new method called `create_firefly()` and call it from the `break_jar` method:

```js hl_lines="1 10"
create_firefly() {

}

break_jar() {

  ...
  
  create_lid()
  create_firefly()

  ...

} //break_jar
```


```js
create_firefly() {

    //instance the firefly prototype
  var firefly = Prototype.create(_world, "prototype/firefly", "firefly")

    //get the positions for the jar and player
    //and move the firefly to match the jar position
  var player_pos = Transform.get_pos(_player)
  var pos = Transform.get_pos(_jar)
  Transform.set_pos(firefly, pos.x, pos.y, 4)

    //add a tag to the firefly
  Tags.create(firefly)
  Tags.add(firefly, "firefly")

    //calculate some random offsets and speed
  var follow_offset = [
    RNG.int(-32, 32),     //x
    136+RNG.int(-32, -8)  //y
  ]
  var follow_y = player_pos.y + follow_offset.y
  var follow_speed = RNG.int(36, 48)
  
    //attach a move modifier and make it follow the player
    //using the offset we calculated
  Move.create(firefly)
  Move.follow(firefly, _player, follow_offset, follow_speed)

    //create an animation on the visual
  var visual_fly = Prototype.get_named(firefly, "visual.fly")
  Anim.create(visual_fly)

    //make the fly bob up and down
  var bob_fly = Anim.play(visual_fly, "anim/bob")
    //start at a random time, so that all 
    //fireflies aren't animating in synced
  Anim.set_interval_time(visual_fly, bob_fly, RNG.float())
    //bob at slightly different speeds
  Anim.set_rate(visual_fly, bob_fly, RNG.float(0.25, 0.5))
    //make the firefly bob 2 pixels up or down
  Anim.track_set_range(visual_fly, bob_fly, "bob", -2, 2)

} //create_firefly
```

Now when we open a jar, we get a new firefly that follows us around!
They have just enough variation to behave slightly different with low effort.

<video preload="auto" autoplay controls="" loop="loop" style="max-width:100%; width:auto; margin:auto; display:block;">  
  <source src="../../images/tutorial/intro/create-firefly-0.mp4" type="video/mp4"></source>
</video>