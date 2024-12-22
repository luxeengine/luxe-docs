![](../../images/luxe-dark.svg){width="96em"}

# Custom controls

## custom control = blank control

More specifically, 

**a custom control is a blank control that has been specialized**.

This is exactly how the built in controls work too.
There are two behaviours that separate a custom control from a custom one:

- response to built in events (and optionally emitting new events)
- the rendering behaviour of a control

## custom behaviour

We can use `Control.set_process(control, function)` to handle built in events,
and then implement custom behaviour and events based on them.

Let's make a nonsense example, a control that emits a change event based 
on which quadrant the input is in. We'll make a helper function that returns one.

```js
get_quadrant(x,y,w,h, input_x, input_y) {
  var mid_x = (x + w*0.5)
  var mid_y = (y + h*0.5)
  
  var is_left = input_x > x && input_x <= mid_x
  var is_right = input_x > mid_x && input_x < (x + w)
  var is_top = input_y > y && input_y <= mid_y
  var is_bottom = input_y > mid_y && input_y < (y + h)

  if(is_left && is_top)     return 0
  if(is_right && is_top)    return 1
  if(is_right && is_bottom) return 2
  if(is_left && is_bottom)  return 3

  return -1
} //get_quadrant
```

### Quadrant change event

Now we can make our control behave this way, and fire a user facing event.
Note that we need to call `Control.set_allow_input` so that we get the move event.
```js
var custom = Control.create(ui)
Control.set_allow_input(custom, true)
Control.set_process(custom) {|control, state, event, x,y,w,h|
  if(event.control != control) return //required

    //we respond to a move event
  if(event.type == UIEvent.move) {
    var quadrant = get_quadrant(x,y,w,h, event.x,event.y)
    if(quadrant != -1) {
      UI.events_emit(control, UIEvent.change, quadrant)
    }
  } //move event
} //set_process
```

This example is interesting, but it doesn't _remember_ what quadrant it was in,
so it sends the event any time the mouse moves, regardless of if there was a _change_ in quadrant.

### Persistent state

To fix that, we'll use that `state` value that's being passed into our process function.
To do that, we can store any value we want in there, via `Control.set_state_data(control, data)`.
That means we could store a class with variables, or just a single value like a number.

For this example, we'll store the quadrant itself to keep it simple.

```js
var custom = Control.create(ui)
Control.set_allow_input(custom, true)
Control.set_state_data(custom, -1) //no quadrant
Control.set_process(custom) {|control, state, event, x,y,w,h|
  if(event.control != control) return //required

  if(event.type == UIEvent.move) {
    var current_quadrant = state
    var new_quadrant = get_quadrant(x,y,w,h, event.x,event.y)
    if(new_quadrant != current_quadrant) {
      UI.events_emit(control, UIEvent.change, quadrant)
      Control.set_state_data(custom, new_quadrant) 
    }
  } //move event
} //set_process
```

There, now the event only fires when there's an actual change.

### Our specialized API

Since we've made a control that behaves in a specialized way, we should make
it available via an idiomatic `create` function.

```js
class Quadrant {
  static create(ui) {
    //our create lives here now
    var custom = Control.create(ui)
    Control.set_allow_input(custom, true)
    // ... continued
    // ...
    // then return our new control
    return custom
  } //create
} //Quadrant
```

### The user facing side 

The user of our quadrant control can now create one, 
and would use the regular event callback to handle our custom event. 
In this example we've reused the `change` event and given it meaning for our control.

```js
var quadrant = Quadrant.create(ui)
Control.set_event(quadrant) {|event|
  if(event.type == UIEvent.change) {
    Log.print("quadrant changed! now `%(event.change)`")
  }
}
```

## custom rendering

Similar to the `Control.set_process()` function, there exists a `Control.set_render()` function too.
Let's make our control draw a colored box showing the active quadrant. This extends what we have so far,
we just add a custom render function as well.

### displaying the active quad

```js
var colors = [[1,0,0,1], [0,1,0,1], [0,0,1,1], [1,1,1,1], [0,0,0,1]]

Control.set_render(custom) {|control, state, x,y,w,h|
  //depth is relative in UI, so we ask for depth 0 
  //relative to our control to draw at.
  var depth = UI.draw_depth_of(control, 0) 

  var angle = 0         //just for clarity / no magic numbers
  var quadrant = state  //remember we're just storing a number

  //if no quadrant, just draw a black box covering the whole control
  if(quadrant == -1) {

    UI.draw_quad(control, x, y, depth, w, h, angle, colors[4])

  } else {

    var mid_x = w*0.5
    var mid_y = h*0.5

    var box_x = x
    var box_y = y
    var box_w = mid_x
    var box_h = mid_y

    if(quadrant == 1 || quadrant == 2) box_x = box_x + mid_x
    if(quadrant == 2 || quadrant == 3) box_y = box_y + mid_y
    
    UI.draw_quad(control, 
      box_x, box_y, depth, 
      box_w, box_h, 
      angle, colors[quadrant])

  } //has quadrant
} //set_render
```

### more drawing

There are several drawing functions, [found here in the UI API](../../../api/world/#ui). 

They offer drawing either solid or outlined versions of basic shapes similar 
to the [Draw API](../../tutorials/draw-and-input/index.md). There's also text and images as you'd expect.

One side effect of this style of rendering, is that you have access to state outside of the control.

That includes game state, player state, and more. If your control was doing custom rendering, 
there's no need for it to be updated with (for example) the number of plants a player has watered,
because you can read it directly, it will always show the latest value.

