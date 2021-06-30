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
    At the moment this is more manual data files than UI based. It'll be a
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

Previously we 
