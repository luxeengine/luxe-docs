![](../images/luxe-dark.svg){width="96em"}

# wrapping up part #1

!!! example "outcome"
    In this step, we'll use everything we have already learnt to 
    wrap up the gameplay mechanics. This includes interacting with the terminals,
    unlocking and opening the jar, and exiting the level.

!!! note ""
    The rest of the tutorial is largely just code to finish the mechanics!

!!! tip "continue in the code editor"

## jar gameplay mechanics

In this area of our game, you pick up a jar which has scrambled symbols on it.

You take the jar to the terminal with the same scrambled symbols, and interact with it.
This unlocks the jar by decoding the symbol of the jar. Once the symbol is known,
you take it to the matching terminal and interact with it, which opens the jar.

## unlocking the jar 

### interaction setup

The next step for our jar mechanics is unlocking the jar. To do that,
we'll implement another condition using the `interacted` variable in `update_interaction()`.

Add another method called `unlock_jar()` and we call it from `update_interaction()`.

Take note that the state we check for the jar is `State.in_hand_unlockable`, which we haven't set yet.

```js hl_lines="1 13 14 15"
unlock_jar() {
  
}

update_interaction() {

  var interacted = Input.event_ended(Inputs.interact)

  if(interacted && _jar_state == State.collectable) {
    collect_jar()
  }    
  
  if(interacted && _jar_state == State.in_hand_unlockable) {
    unlock_jar()
  }

} //update_interaction
```

### terminal enter/exit 

Now, when does the jar change states from `State.in_hand_locked` => `State.in_hand_unlockable`?

This happens when the player is in range of the terminal with the scrambled symbols! 

So let's start by implementing a method that is called when the player enters or exits a terminal.

Inside `area1.wren` we had a method called `update_terminals`, which fades them in and out.
We add two calls to two new methods in there, which will be how we keep track.

```js hl_lines="1 5 21 24"
enter_terminal(terminal) {

}

exit_terminal(terminal) {

}

update_terminals() {
  
  var range = 48
  var player_x = Transform.get_pos_x(_player)

    //for each terminal, check if the player is in range
  _terminals.each {|terminal|
    var terminal_x = Transform.get_pos_x(terminal)
    var min = terminal_x - range
    var max = terminal_x + range
    var in_range = Math.within_range(player_x, min, max)
    if(in_range) {
      enter_terminal(terminal)
      fade(terminal, Fade.In)
    } else {
      exit_terminal(terminal)
      fade(terminal, Fade.Out)
    }
  }

} //update_terminals
```

Before we move forward, let's add one more field to the class to keep track of which terminal we're in range of.
In `setup_terminals()` we add a single line to initialize a field called `_active_terminal`.

```js hl_lines="3"
setup_terminals() {
  
  _active_terminal = null
  _terminals = Tags.list(_world, Name.terminal)
  scramble_terminals()

} //setup_terminals
```

### the enter state

The `fade` method, called right after the `enter_terminal` method, sets the `visible` key in
the terminal `Values` modifier. If we check that value, we can make sure our code for entering
only happens the first time they're in range, or the first time they're out of range.
If that's not the case, we just return and do nothing.

We also want to keep track of `_active_terminal`, which let's us know which terminal we're in range of when
an interaction happens. 

And, when we configured the terminals, we gave them an id stored in the `Values` modifier. This is
what we'll use to tell the terminals apart. The terminal with an id of 0 is the one we want for unlocking the jar.

This makes up our whole enter terminal method:

```js
enter_terminal(terminal) {

    //since visible will be set by fade(), we can use it to do this once only
  var visible = Values.get(terminal, Name.visible, false)
  if(visible) return

    //keep track of the terminal we're in range of
  _active_terminal = terminal

    //fetch the terminal id from the Values modifier
  var id = Values.get(terminal, Name.id, -1)

    //if we're holding a locked jar, and we're in range
    //of the symbol decoding terminal (id 0), change state.
    //we also animate the jar to indicate that there is interaction
  if(_jar_state == State.in_hand_locked && id == 0) {
    make_jar_shine(true)
    _jar_state = State.in_hand_unlockable
  }

} //enter_terminal
```

### the exit state

When you leave a terminal, we have to reset anything we changed.
This is quite similar to enter, but reversing those changes:

```js
exit_terminal(terminal) {

    //since visible will be set by fade(), we can use it to do this once only
  var visible = Values.get(terminal, Name.visible, false)
  if(!visible) return

    //reset the terminal we're in range of
  _active_terminal = null

    //fetch the terminal id from the Values modifier
  var id = Values.get(terminal, Name.id, -1)

    //if the jar was locked we set it back
  if(_jar_state == State.in_hand_unlockable && id == 0) {
    make_jar_shine(false)
    _jar_state = State.in_hand_locked
  }

} //exit_terminal
```

### the interaction

Now, back to our interaction with the jar.

When a jar is decoded, we just pick a random number (either 1 or 2) and keep track of it.
To keep track we'll want to add a new field called `_jar_symbol` and set it to `-1`.
We'll do this inside `setup_jar()`

!!! note ""
    The value of -1 has no special meaning, it's just not 0 or 1 or 2, which all do have meaning for us.
    This is often called a "sentinel value". 


```js hl_lines="5"
setup_jar() {
  _jar = null
  _jar_state = State.none
  _jar_flip = false
  _jar_symbol = -1
}
```

We'll also want to reset it when we create a new jar. Inside `create_jar` we'll add the same line:

```js hl_lines="7"
create_jar() {

  if(_jar) Entity.destroy(_jar)

  _jar = Prototype.create(_world, "prototype/jar", "jar")
  _jar_state = State.none
  _jar_symbol = -1

  ...
}
```

Now we can implement the decoding!
When the player presses `interact` when in range of the symbol decoding terminal,
the `unlock_jar()` method is called. 

Here's the steps for unlocking: set the jar state, stop the jar from shining, 
pick a random number to decide on which symbol the jar will be, make the jar display that symbol.

!!! note ""
    The UV uses the `random` variable direction, which is `0` or `1`, not `_jar_symbol`, which is `1` or `2`.

This is how that looks!

```js
unlock_jar() {

    //start by updating the state
  _jar_state = State.in_hand_unlocked

    //no longer need to animate
  make_jar_shine(false)

    //get a random number that's either 0 or 1
  var random = RNG.int(2)
    //terminal with an id of 0 is the one that decodes,
    //so we add 1 to our random number to start at 1 
  _jar_symbol = 1 + random

    //fetch the symbol from the jar prototype
  var symbol = Prototype.get_named(_jar, "visual.symbol")
    //stop the symbol animation, reset state
  Anim.stop_all(symbol, true)
    //update the UVs to match our symbol.
    //since the image contains 2 symbols side by side,
    //each one takes up 0.5 of the image.
    //for symbol 0: 0 * 0.5 => 0+0.5   which is 0 => 0.5
    //for symbol 1: 1 * 0.5 => 0.5+0.5 which is 0.5 -> 1
  var x = random * 0.5
  Sprite.set_uv(symbol, x, 0, x + 0.5, 1)
  
} //unlock_jar
```

### the result

And that's it, the jar will now pick a random symbol to display when we interact with the symbol decoding terminal.

Did you notice when it happened? It's quite hard to notice! 

We'll fix that next by making an interaction animation we can reuse any time an interaction happens.

<video preload="auto" autoplay controls="" loop="loop" style="max-width:100%; width:auto; margin:auto; display:block;">  
  <source src="../../images/tutorial/intro/wrap-up-0.mp4" type="video/mp4"></source>
</video>

## interact animation

The project outline comes with an animation intended to be displayed on the terminal that we're
interacting with, as well as the thing that's interacted with it (like the jar).

When played at the same time it gives the player a visual indication that something happened,
since feedback is quite important for the gameplay to be clearer.

We'll add a method called `create_interact(sprite)` which does things we're familiar with.

The only new concept here is `Anim.on_event(entity: Entity, anim: Anim, fn: Fn)`. 
This let's us know when an animation has completed. Since these interact animations are temporary,
we want to clean them up as soon as the animation finished.

```js
create_interact(sprite) {

    //don't do anything if the entity is invalid
  if(Entity.valid(sprite) == false) return

    //instance a prototype of the terminal interaction
  var interact = Prototype.create(_world, "prototype/terminal.interact", "terminal.interact")

    //attach it to the sprite, so that if the sprite moves, the animation follows
  Transform.link(interact, sprite)

    //center the animation on the sprite 
  var center_x = (Sprite.get_width(sprite)/2).floor
  var center_y = (Sprite.get_height(sprite)/2).floor
  Transform.set_pos(interact, center_x, center_y)

    //grab the visual to play the animation
  var visual = Prototype.get_named(interact, "visual")
  var anim = Anim.play_only(visual, "anim/terminal.interact")

    //ask the animation to tell us when it ends, so we can destroy this entity
  Anim.on_event(visual, anim) {|entity, anim, time, value, track_type, track, event|
    if(event == AnimEvent.complete) {
      Entity.destroy(interact)
    }
  }

} //create_interact
```

At the end of `unlock_jar`, we'll call this new method twice: once for the jar and once for the active terminal.

```js hl_lines="5 6"
unlock_jar() {

  ...

  create_interact(_jar)
  create_interact(_active_terminal)
  
} //unlock_jar
```

Now when we unlock the jar, it's a lot clearer that something happened.

<video preload="auto" autoplay controls="" loop="loop" style="max-width:100%; width:auto; margin:auto; display:block;">  
  <source src="../../images/tutorial/intro/wrap-up-1.mp4" type="video/mp4"></source>
</video>

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

### completing the jar cycle

When the breaking animations ends, we can destroy the jar itself, and scramble the terminals so that the next jar is random again.
These are familiar.

What we do next is schedule a function to be called in the future using `World.schedule(world: World, time_from_now: Num, fn: Fn)`.
This will call our function in `time_from_now` seconds. We can use a random number to make it slightly more random.

We only want to create a new jar if the player needs one to finish the area. In this case, the player needs to open 3 jars to free
3 fireflies. If there aren't 3 fireflies, we create a new jar. The fireflies are tagged with the `firefly` name which is how we check how many there are.

```js hl_lines="9"
break_jar() {
  
    //get the jar visual, and play the breaking animation
  var visual = Prototype.get_named(_jar, "visual")
  var open = Anim.play(visual, "anim/jar.open")
  Sprite.set_size(visual, 32, 32)

    //wait for the open animation to end
  Anim.on_event(visual, open) {|entity, anim, time, value, track_type, track, event|
    if(event == AnimEvent.complete) {

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

    } //if complete

  } //anim on_event

} //break_jar
```

At the moment we don't have any fireflies, so this will just keep creating jars, but this is how it looks now.
You'll notice that the terminal all the way to the left was the decoding terminal, but after the jar opened it was a static terminal.
This is because we scrambled them so the player has to find the right terminal.

<video preload="auto" autoplay controls="" loop="loop" style="max-width:100%; width:auto; margin:auto; display:block;">  
  <source src="../../images/tutorial/intro/wrap-up-4.mp4" type="video/mp4"></source>
</video>


