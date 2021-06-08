# UI in luxe

!!! note "work in progress"
    The UI has parts that are still being defined, but the basics are there.

## UI is a Modifier

UI exists within a `World`, and is attached to an `Entity` like other modifiers.
This means that a UI can easily follow the entity if it is moved.

When you create a UI on an `Entity`, you're creating a _canvas_.
A canvas is like an isolated little space, dedicated to elements within that canvas.

These elements are called _controls_, a canvas is a container for _controls_. 
UI controls don't belong to the world (they are not entities), they belong to the canvas.
We'll see how that looks below.

A canvas also has it's own coordinate space, where 0,0 is top left for the origin,
and Y values increase downward. This is different from world space, where Y+ is up.

## Creating a canvas

To create a UI, we need an entity to attach it to.

When we attach the UI, we also give it a camera, which it will use to calculate input.
That means if your object is in a 3D world, input should work as expected without extra effort.

```js
var ui = Entity.create(app.world, "ui")
var x = 0
var y = 0
var w = 500 //these are in world units
var h = 500
var depth = 0
UI.create(ui, x, y, w, h, depth, app.camera)
```

## Creating a control

Now that we have a canvas, we can create controls inside it.
Controls are positioned relative to the canvas unless they're a child of another control.
Controls have a `bounds`, which is a rectangle, and is also top left, y+ going down.

Let's create a panel, as a background, so we can see our canvas.

To create a control, we pass in the canvas that it will be created in. Once created, we can configure it.
The first step is usually setting the size or the bounds, via `Control.set_bounds(control, x,y,w,h)`.

```js
//we'll use the same w/h from above
var bg = UIPanel.create(ui)
Control.set_bounds(bg, 0,0,w,h)
UIPanel.set_color(bg, [0,0,0,0.25])
```

So here we can see that we got a panel control in return from `create`.   
This value is an instance of a control that belongs to this canvas.

## Committing UI Changes

Now, this part is important.   

A [concept](../../../guide/concepts#commit) that luxe uses is the `commit` concept.

UI is a great example of this concept, where you want to make several changes
to the UI that could be expensive, or could have dependencies (like layout being relative).

**Once you've made a series of changes, you MUST call commit to finalize them.**

In fact, in this example, if you don't, nothing will render! 
So we must call `UI.commit(ui)` to make sure it shows up.

## Controls and Specialized Controls

All controls are a `Control`, but not all controls are a `UIPanel`.

Controls like `UIPanel` _specialize_ a control, and offer their own API
on top of the `Control` API, like `UIPanel.set_color`. The `Control` API
is valid for all controls, regardless of their type, but specialized controls 
only work with the same API that their create function is from.

Let's also create a button that takes up the upper right hand side of our canvas.
This would be half the size on width and height, and be positioned at the middle of the canvas on x.
We'll use this to hook up an event!

```js
var button = UIButton.create(ui)
Control.set_bounds(button, w/2, 0, w/2, h/2)
UIButton.set_text(button, "click!")
```

## Control events

When we have a control, we can listen for events on that control and respond to them as needed. 
Like our button will have a `UIEvent.release` event when clicked.

```js
Control.set_events(button) {|event|
  if(event.type == UIEvent.release) {
    System.print("The button was clicked! x %(event.x) y %(event.y)")
  }
}
```

There are [many default events](../../../api/world/#uievent) for a control, but it's possible for controls to send custom events too. Some events are dependent on settings like `Control.set_allow_input`/`Control.set_allow_keys`, which determine if a control will receive mouse and keyboard input. 

You can also print the events to see what kind of events are happening and when:

```js
Control.set_events(button) {|event|
  System.print("event from button %(event)")
}
```

## Empty controls as containers

If you don't use a specialized `create` function, 
you get a blank control that has all the default behaviours of a control, 
like input and bounds.

A blank control is often used as a container to make groups, 
so you can easily refer to a single control to move a bunch of controls.

## Full example

```js
import "luxe: io" for IO
import "luxe: game" for Ready
import "luxe: input" for Input, Key
import "luxe: world" for UI, UIEvent, Entity
import "luxe: ui" for UIButton, Control, UILabel, UISlider, UIPanel

import "outline/app" for App

class Game is Ready {

  construct ready() {

    super("ready!")

    app = App.new()

    var ui = Entity.create(app.world, "ui")
    var x = 0
    var y = 0
    var w = 500 //these are in world units
    var h = 500
    var depth = 0
    UI.create(ui, x, y, w, h, depth, app.camera)

    var bg = UIPanel.create(ui)
    Control.set_bounds(bg, 0,0,w,h)
    UIPanel.set_color(bg, [0,0,0,0.25])

    //we'll use the ui w/h from above
    var button = UIButton.create(ui)
    Control.set_bounds(button, w/2, 0, w/2, h/2)
    UIButton.set_text(button, "click!")

    Control.set_events(button) {|event|
      if(event.type == UIEvent.release) {
        System.print("The button was clicked! x %(event.x) y %(event.y)")
      }
    }

    //create a blank container
    var container = Control.create(ui)
    Control.set_bounds(container, 0, h/2, 128, 32)
    
    //create a background as well
    var container_bg = UIPanel.create(ui)
    Control.set_bounds(container_bg, 0,0,128,32)
    UIPanel.set_color(container_bg, [0,0,0,1])

    //create some controls to put inside it
    var label = UILabel.create(ui)
        Control.set_bounds(label, 4, 0, 64, 30)
        UILabel.set_text(label, "progress")
    var slider = UISlider.create(ui)
        Control.set_bounds(slider, 64, 10, 60, 10)

    //now add them to the container
    Control.child_add(container, container_bg)
    Control.child_add(container, label)
    Control.child_add(container, slider)

    UI.commit(ui)

  } //ready

  tick(delta) {

    if(Input.key_state_released(Key.escape)) {
      IO.shutdown()
    }

  } //tick

  app { _app }
  app=(v) { _app=v }

} //Game
```

## Debug Visualization

In your settings file (like `outline/settings.settings.lx`), we can specify a debug flag
that will draw outlines for each control, and show some info about what controls are hovered.
Inside the settings file, put `engine.ui.debug_vis = true` at the root. 

Also relevant: A `Control` doesn't have a name by default, you have to set one using `Control.set_id(control, "some name")`.


## Final Note: Specialized Containers

Some containers are specialized because they provide additional behaviour.
UIList and UIScroll are two examples of such controls, as the both provide scrolling.

In both cases, adding a child (via `Control.child_add`) to the control itself _does not_ count 
as adding it to the container, but is treated as a regular child of the control. 
You would need to use `UIScroll.add(scroll, control)` or `UIList.add(scroll, control)` instead.

**why?**    
Imagine you had a scroll area (or a list), and you wanted to place a button on the top right. 
You wouldn't want this button to scroll as part of the container, but instead be fixed at the top.
If the scroll used `Control.child_add` it wouldn't have a way (currently) to distinguish this type
of child, from one you did want to scroll around as part of the container.

!!! note "potential change"
    This behaviour may change, as I think it's got its own set of quirks.
