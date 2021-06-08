
# Moving a sprite around

## Input queries

There are a few ways to handle input, all useful in different situations. We'll start with the most direct and simple form, and go from there.

The first type of input handling we'll look at, we call _input queries_. This means asking the `Input` system a question, and getting a response in return.

!!! note ""
    Make sure you import `Input` and `Key` at the top of your file.
    ```js
    import "luxe: input" for Input, Key
    ```

## The tick function

Inside your `game.wren` file, you'll find a tick function which looks something like this:
```js

tick(delta) {
  ...
}
```

This function is called for you by luxe, once per game update. In here, you can do logic that will happen continuously (like moving our sprite).

## Mouse queries

To find out where the mouse currently is, in relation to the window, we query `:::js Input.mouse_x()` and `:::js Input.mouse_y()`. 

It's important to note that the mouse is relative to the window, but our game world likely has a different coordinate space. To use the values, we want to convert it into world space first, using the camera. This 
handles any differences and makes the values the ones we'd expect.

```js
var mouse = Camera.screen_point_to_world(app.camera, Input.mouse_x(), 
                                                     Input.mouse_y())
```

When we created our sprite in the first step of the tutorial, we also created a `Transform` modifier on our entity. We'll use this again to move the sprite around, and make it follow the mouse. We'll put this at the top of our tick function.

```js
tick(delta) {
  var mouse = Camera.screen_point_to_world(app.camera, Input.mouse_x(), 
                                                       Input.mouse_y())
  Transform.set_pos(player, mouse.x, mouse.y)
  ...
}
```

## Key queries

Instead of following the mouse, let's change it so our sprite moves left when we press keys. 

We can query `:::js Input.key_state_down(key)`, which returns true if the given key is held down during this tick. 

!!! note ""
    The `:::js Key` class has many identifiers used to specify which key we mean, such as `:::js Key.space`, `:::js Key.right`.

```js
  //We ask the transform modifier
  //for the current x position
var x = Transform.get_pos_x(_logo)
  //if the left key is being held down
  //we move left by 100 units per second.
  //(The * delta makes it per second)
if(Input.key_state_down(Key.left)) {
  Transform.set_pos_x(_logo, (x - 100) * delta)
}
```

Feel free to add `Key.down`, `Key.up` and `Key.right` to the example above.

!!! note ""
    Other key queries include `Input.key_state_pressed(key)`, which lets us know if the key has just been pressed this tick. And, we have `Input.key_state_released(key)` for finding out if a key was just released. Both of these will only be true for one tick, where as `Input.key_state_down` will be true every tick that the key is held down.

We'll look at the other forms of input handling in a later tutorial. The [Input API](/api/#input) documentation has a lot of info if you want to peek ahead.

For now, we'll move on to creating a world around our sprite, via scenes.