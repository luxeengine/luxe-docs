# luxe release notes

## 2021.0.5

- latest SDL - 2.0.14
- latest emsdk - 2.0.25
- Draw - fix rect_detailed for y+ up and clamped radius
- Draw - add rect detailed example/test to sample
- LX - fix bug serializing vectors of bool

## 2021.0.4

- Fix Assets class being special, so now it gets proper completion
- Docs + types for code completion for several classes
  - Assets, Anim, Assert, Strings, Audio, Color
  - modules: containers, draw, editor, events, game, id, sat2d
- UI - add commit event to text fields
- UI - text field now cancels input on escape, commits on enter, and can tab forward
- UI - recursively handle UI events properly, so no events are lost
- Sprite - in editor, update size on changing material automatically
- Assets - import for sprite shows warnings for existing content not errors
- Transform - add `set_snap(x, y)`

## 2021.0.3

Minor breaking change: If you had a constructor that returns any value (including `this`), that's invalid.
Often you can just convert to `static new() {}` or similar and have an internal `construct` method instead.

- `Str.fixed` now uses a reliable format where 0.1 remains 0.1 instead of 0.1000001231
- add `Str.vec` which formats a vec using Str.fixed
- `LX` now stringifies numbers using `Str.fixed` with 6 digits precision (:todo: configurable)
- Wren - clean up attributes spam
- Wren - latest version of 0.4.0 https://github.com/wren-lang/wren/releases/tag/0.4.0
- Wren - fix crashy behaviour in much bigger projects due to unitialized value
- Wren - fix newlines being different based on file newlines within strings
- Anim - Sprite frames track resets material on reset
- Anim - Sprite frames track now sets the material if it's not a match, as intended
- Anim - Sprite frames track allow inverted ranges for start/end index
- Anim - Sprite values track now allows animating sprite properties as a curve
- Anim - Transform - relative animations now work as intended
- Anim - add `set_interval_time`, sets the time in 0...1 range for a live anim
- Anim - add `track_get_range`/`track_set_range`, sets the range for a track in a live anim
- Anim - `play`/`play_only` now error properly if you pass a null asset id
- Anim - fix crash when animation modifier accessed an old entity
- World - when requesting a system, return a new one if not present (instead of error)
- Transform - fix some ways to set a position not respecting snap
- Transform - fix unlink without a parent asserting, error properly instead
- Transform - fix linking to self being an infinite loop + crash, error properly instead
- Transform - add experimental `get_pos_world_unsnapped`
- Runtime - add `engine.runtime.quit` setting, if false, quit will do nothing and fire an event
- Render - add error for missing material basis on `Material.create`
- UI - add `UI.make` experimentally (it's like spawn but returns a properly sized container)
- Sprite - initial annotations for completion/docs
- Math - add `dir2D(pos, target)`

## 2021.0.2

- Windows - fix resize/moving a window from blocking the game
- Wren - add annotations (available at runtime as SomeClass.meta)
- Wren - add raw string literal """like this""", can cross lines and include anything
- Wren - add list.remove(item)
- Wren - add experimental way to call a function by name
- Transform - fix bugs due to use of euler in animation track
- Transform - add global default snap setting e.g pixels `engine.transform.snap = [1,1,0]`
- Transform - experiment with applying transforms on spawning prototypes more
- World - clean up some memory properly
- IO - fix creating paths across drive boundaries, fixes launcher
- LX - add raw string support to lx files
- LX - escape some json content correctly when saving json
- Mesh - fix a bug where changing the mesh asset could crash if done a certain way
- Runtime - queued ticks will process recursively queued ticks correctly now
- String - add indent(string) and indent_strip(string) for convenience
- Outline - add vscode default tasks to empty outline
- Tiles - add Tile.get/Tile.set for storing values on a tile
- Color - add hex(value, alpha)
- Result - add Result type experimentally
- World - modifiers have find_entity(relative_entity, uuid) for finding entities
- Camera - if no default camera exists when one is created, set it as default
- UI - fix obscure timing issue with dead controls being marked
- UI - add `Control.destroy_children(control)`
- Wren - fix infinite loop in some parsing cases
- Wren - error on missing imports up front
- Wren - warn on single quote strings
- Wren - warn when imports mismatch case
- Math - vector angle between `angle(v1, v2, up)`
- fix some dev mode issues
- fix crash when asset reloading fails to compile
- add debug file to find issues in lx parse till there's real errors

## 2021.0.1

- UI - fix nasty text focus bug (eduardo, bach)
- UI - when setting text, error properly on not-a-string
- Render - add atlas API and assets for atlas support
- Sprite - add atlas support via Sprite.create(entity, atlas, atlas_image_id)
- Sprite - add origin setting (0.5, 0.5 center default. 0,0 is bottom left)
- Anim - Sprite track now has proper frame based information instead of keys
- Bytes - subscript [] returns uint8 (instead of int8) as intended
- Render - add window_hide(state)
- Render - add `engine.runtime.window.allow_screensaver` to not block
- Render - add VertexInputRate for per instance vs per vert
- Render - add get/set_instance_count for geometry
- Shaders - add pixel perfect aspect upscaling shader for outlines
- Shaders - add input.view.time to shaders
- World - add proper errors on invalid material for Sprite
- Samples - add previews and sample.lx for new launcher
- Deploy - add experimental custom icon support + a default icon
- Compiler - print success status
- Docs - work on tutorial

## 2021.0.0

- Fix major font rendering bug.... 
- Fix filewatch again
- Scripts - add an error for missing imports
- Game - add `Frame.schedule` for calling functions in future, absolute time
- World - add `World.schedule` for calling functions in future, world relative time
- World - add Camera.cull and some tools for frustum culling when rendering
- World - add World.render with a second camera to cull with (can be same as render cam)
- World - experimental render view descriptors
- Settings - add `has` query
- UI - add `UIList.can_scroll`
- UI - add `UIWindow.get_collapsed`
- UI - fix some event ids being stomped
- UI - fix events being sent to parents even if they didn't want them
- UI - visual polish for several things
- Math - add `dist2D` for non vector
- Anim - transform tracks now have an absolute flag
- Anim - fix reverse rate not working as intended. reverse now works again
- Material - add depth bias setting to basis
- Expand color class with some constants, hsv functions and lerp
- Render - explore plural tags for render layers
- Regex - fix bugs and update lib for utf8 support + for substitutions 

## 2020.3.5

#### stability fixes

There were a few vague crashes that happened occasionally when running a (bigger) project, and re-running normally worked.
This was introduced not long ago by mistake when I was testing the new native lx parser. 

All instances of weird behaviour have been found and fixed, so things are back to being stable + reliable again.
I've also optimized a couple places for script compilation to be much more snappy when iterating.

#### lots of physics work

For 7DFPS I was making a physics game, that necessitated a bunch of work on physics.
Instead of doing the minimum, I took the opportunity to implement the intended filtering + collision model,
add collision callbacks, physics materials, and body settings assets.

This filtering model is based on "ignore/overlap/collide" being the 3 settings for a body. 
When two bodies overlap, the "least" type is used. e.g ignore vs collide = ignore. overlap vs collide = overlap.
This means any body can be collidable (solid) or overlapping (triggers, etc).

The callbacks send events for overlap `begin`, `active`, and `end`. 
A collide event is also sent if the result is `collide`.

These are only applied to 3D at the moment, but the same code + model applies to 2D and will make it's way there soon.

#### lots of transform work

Similiarly, I needed some special transformation stuff, so instead of just adding the one I needed I added a
lot of the fundamentals for dealing with transforms. This is still based on the idea that transforms should be
possible to use without resorting to math constructs like matrix or quaternions. Lot of progress here!

There's lots to see otherwise: 

- Window - Fix fullscreen to be borderless windowed, add alt+enter handling
- Scripts - optimize recompilation a lot for faster iteration
- Wren - 0.4.0 - changes here - https://github.com/wren-lang/wren/releases/tag/0.4.0-pre
- Wren - fix corruption in GC due to an unmarked value I added
- Wren - fix potential access of uninitializd memory
- Wren - fix corruption in GC due LX parsing - https://github.com/wren-lang/wren/issues/869
- Draw - add `Draw.cross(context, x, y, z, radius, angle, style)`
- Draw - add simple ring variant `Draw.ring(context, ox, oy, oz, radius, smoothness, style)`
- Math - Add `Math.length(vec)`, `Math.length_sq(vec)`, `Math.length_sq2D(vec)`
- Math - Add `Math.angle(vec, other_vec)`
- String - fix `Str.fixed(string, precision)` affecting the number
- Assets - Meshes now auto triangulate, so no need to triangulate inputs
- Assets - Mesh compiler prints more useful nested info for choosing a node
- Physics 3D - fix bugs when editing physics bodies in editor (tilman)
- Physics 3D - add body config asset
- Physics 3D - add collider materials asset
- Physics 3D - fix mesh collider when meshes were indexed
- Physics 3D - fix mesh internal seam collisions for smooth collisions
- Physics 3D - add mesh MeshColliderType for controlling behaviour
- Physics 3D - add callbacks for overlap + collide events
- Physics 3D - add initial wip filtering for collide/overlap/ignore
- Physics - Fix debug vis in editor
- UI - add `UIText.select_all(control)`
- Transform - fix look_at when linked to another transform (tilman)
- Transform - fix bugs in world rotation setting (tilman)
- Transform - add `rotate_around(entity, x, y, z, axis_x, axis_y, axis_z, degrees)`
- Transform - add `rotate_around_world(entity, x, y, z, axis_x, axis_y, axis_z, degrees)`
- Transform - add `world_point_to_local(entity, x, y, z)`
- Transform - add `local_point_to_world(entity, x, y, z)`
- Transform - add `local_dir_to_world(entity, x, y, z)`
- Transform - add `world_dir_to_local(entity, x, y, z)`
- Transform - add `local_vector_to_world(entity, x, y, z)`
- Transform - add `world_vector_to_local(entity, x, y, z)`
- Transform - add `set_rotation_slerp(entity, from, to, t)`
- Transform - add `set_rotation_slerp_world(entity, from, to, t)`
- Transform - add `set_rotation_slerp_angle_axis(entity, axis, from, to, t)`
- Transform - add `set_rotation_slerp_angle_axis_world(entity, axis, from, to, t)`
- Transform - add `rotate_angle_axis_slerp(entity, axis, angle_amount)`
- Transform - add `rotate_angle_axis_slerp_world(entity, axis, angle_amount)`

## 2020.3.4

- Runtime - allow background_sleep to affect headless apps
- World - add Scene.entity_forget for moving entities around manually
- UI - don't abort on > 1000 events (can happen when file dialog is up)
- Compiler - add transient concept for compiling transient data in editor

## 2020.3.3

- Wren - add continue keyword to use in loops
- Wren - skip type-style annotations in several places
- Wren - method arity checks are now reported as an error where possible
- Wren - method max parameters is now a compile time check
- Wren - improvements to the script check parsing + graceful failure
- Math - `random_point_in_unit_circle` streamlined by ronja
- Input - fix `Input.set_mouse_capture` to work as intended across platforms (tilman)
- Input - add `Input.mouse_x_rel()`/`Input.mouse_y_rel()` for capture use
- LX - add a stringify to json flag for strict json output
- UI - fix crash when control is destroyed while another is captured (ronja)
- UI - fix events not being cancelled for listeners (ronja)
- UI - fix a rogue wrenalyzer complaint about UIWindowChange (ronja)
- Assets - auto generated images have a `generate_mipmaps_at_load` added
- Camera - set2D/set3D for less confusion (set2D uses x/y/w/h and converts internally)
- Render - Resource IDs like images are passed to debug tools (e.g renderdoc)
- Render - Fix material override bug being wrong on web
- Render - Refactor FBO handling to be more strictly conformant (webgl2)
- Render - fix some issues running headless builds
- IO - fix http server issue on some platforms (tilman)

## 2020.3.2

- IO - add logging for failure to create directories
- Anim - fix validation of animations so script errors happen (eva)
- UI - fix destroyed controls not updating marked state (ronja)
- UI - fix relative mouse offsets being wrong (ronja)
- UI - fix crash when marked update finds destroyed controls
- UI - custom events now have proper cancellable IDs and can be cancelled
- UI - fix bug where captured controls lose events due to new marked fix
- UI - fix scroll areas not updating when resized, they do now
- Render - fix bug in opengl backend causing many sprites to fail (jonathan)
- Transform - add change callbacks `listen(entity, fn)` / `listen_all(world, fn)` 
- World - add `World.valid(world)`

## 2020.3.1

- Wren - Allow newline before a dot so you can do fluent syntax
- Wren - List now has `indexOf(item)` and `swap(index, other)`
- Wren - Num now has `var max = 3.max(7)`, `.min(other)` and `num.clamp(0, 1)`
- Astar - add 2D pathfinding API 
- Anim - fix crashing when the entity an autoplay was queued for is gone
- Settings - fix string settings being stored as bool (??)
- luxe: pqueue - add MinPQ and MaxPQ priority queues
- Lists - `binary_search_first`, `remove_where`, `index_of_where` args
- Render - add vsync flag (`engine.render.vsync` now works)
- Render - pass layer can now use a basis
- Render - pass layer can now access `.dest` directly
- Render - add `Render.submit_fn`
- Render - backend fixes for some incorrect strings (shader errors)
- Render - fix important viewport bug 
- Render - can now correctly render to cubemaps
- Render - can now correctly render to mip levels of images
- Render - add missing `Image.destroy` and `Image.valid`
- Render - add `view_inverse`, `proj_inverse`, and more to `View` inputs
- Runtime - filewatch fixes + also now respects dupes, ignores for N frames
- Runtime - fix a bunch of plugin bugs while testing a rust plugin
- Input - fix `set_mouse_capture(state)` capturing cursor like FPS games need
- World - add optional `into` arg to `World.world_point_to_view`
- World - add `World.set_default(world)`/`World.get_default()`
- World - add `Modifiers.has_system_in_world(modifier_id, world)`
- World - wip: `Entity.valid` checked for modifier tick before sending
- World - Transform now has `sync_world(world)` and `sync(entity)`
- UI - Fix custom events firing incorrectly (ronja)
- UI - Fix Text taking focus when things are above it (like editor scene buttons)
- UI - Fix text rendering (button/window/text/label) being delayed by a rendered frame
- UI - querying label metrics is now accurate at all times (brody)
- UI - Fix layout bugs (update recommendation from layout dev)
- UI - Fix enter/exit only happening on mouse move, and exit other bugs (ronja)
- docs - fix how to for `random` (jonathan)
- docs - document `Assets` API
- docs - document `luxe: containers`/`Lists`/`MapOrdered` API
- docs - document `luxe: draw`/`LineCap`/`LineJoin`/`PathStyle`/ API
- docs - document `luxe: editor`/`Editor` API
- docs - document `luxe: events`/`Events` API
- docs - document `luxe: game`/`Frame`/`Ready` API
- docs - document `luxe: id`/`ID` API

## 2020.3.0

Time for some clean up, yay project changes!

#### new game class

In it's simplest form, a game class
before 2020.3.0 looked like this:
```js
import "luxe: game" for Game
class game is Game {
  construct ready() {
    System.print("ready!")
  }
}
```

This has changed to the following, as a more final form. 
Notes: the `super` is required, the base class is now `Ready`, 
       and the actual class is called `Game`.
```js
import "luxe: game" for Ready
class Game is Ready {
  construct ready() {
    super("ready!") //or just super() is fine
  }
}
```

#### New project class
Similarly, the project class has been finalized too.
Before 2020.3.0:
```js
import "luxe: project" for Project
class project is Project {
  construct new(target) {}
}
```

And after: The base class is `Entry`, the actual class is `Project`, 
and the constructor is called `entry` too.
```js
import "luxe: project" for Entry
class Project is Entry {
  construct entry(target) {}
}
```

#### Access your Game class
You can now reach the live instance of your game class anywhere.

Just use `import "luxe: game" for Game`, this variable contains your game instance.
For example, `Game.app` would be accessible from other scripts now.

#### default input maps
Previously input maps weren't loaded by the editor and the template didn't have one.
This is better now, if you set `engine.input.entry` in your entry settings file,
then the editor + the game will automatically load this input config for you. 

This means for example, previewing a scene in editor would work with the arcade module again,
since it used input maps for input but there wasn't any loaded before.

#### New main loop
**Renaming**: Note that `World.tick_world` was renamed to `World.tick`, 
and `World.tick_systems` was removed. We just use `World.tick` now.

The main loop is getting closer to done too, so you now have access
to it from anywhere and can schedule callbacks within it. 
You can access it via `luxe: game` for `Frame` atm. 
The system is a work in progress, but useful so far.

The loop works based on sections, and at the moment those are predefined by luxe.
They are `begin, init, sim, visual, end` in that order. Sim being simulation, as in the update function.

You can use `Frame.on`, `Frame.before` and `Frame.after` to place callbacks in or around
a section. These ones are recurring callbacks and happen every tick, they return a handle 
that can be used with `Frame.off` to remove them.

The other ones are once off callbacks.
`Frame.queue` will run the callback at the end of the section that's running.
`Frame.next` will run the callback at the start of a frame (before any sections)
and `Frame.end` will runt the callback right at the end of the current frame (after all sections).

As an example, empty project outline and samples now use it to update and render worlds.
**Note that you don't need to change anything** in your project, it should still work as before even if you don't use this new form.
```js
//update our worlds
  Frame.on(Frame.sim) {|delta|
    World.tick(_world, delta)
    World.tick(_ui_world, delta)
  }
//render our worlds
  Frame.on(Frame.visual) {|delta|
    World.render(_world, _camera, "game", {"clear_color":_color})
    World.render(_ui_world, _ui_camera, "ui")
  }
```

#### Animation events
Animation tracks now have events, default ones, custom ones and a tick event.

The default events are `start` and `complete` which fire when an animation
begins playing and when it ends (via stop or otherwise). Note that these are 
for the entire animation, not a particular track.

For tracks, if you set `tick_event = true` in your anim asset for that track, 
it will fire an event every time the animation is updated. This means you can
now use an animation track to drive other things directly. Example below.

The track also can have a list of custom events, which behave like keyframes.
In this example, the animation is 0...1 on the timeline, but in the middle and quarter
of the way through, a custom event will get fired each time that time is crossed.
This let's you respond to keyframes directly, such as playing sounds or effects at key points.
_(note that an audio track is still coming, but this means you can use them already)._

```js
events = [
  { time=0.25 event="quarter" }
  { time=0.5 event="middle" }
]
```

**Listening to the events**   
The event handler is set on an animation instance, one that is returned from `Anim.play`.
In the example below, the animation is fading in a mesh, but I'm using the tick event to also
scale the mesh based on the values in the animation curve. 
You can see it in action here: https://i.imgur.com/uYHNbOS.mp4
```js
var anim = Anim.play(entity, "anims/example")
Anim.on_event(entity, anim) {|entity, anim, time, value, track_type, track, event|
  //event will be `tick`, `start`, `complete` or a custom value.
  if(Strings.get(event) == "tick" && Entity.valid(entity)) {
    var scale = 9.5 + (0.5 * value)
    Transform.set_scale(entity, scale, scale, scale)
  }
}
```

#### UI Layout API

There's a new modifier for doing dynamic layout with UI.
It's documented in the [layout tutorial here](../tutorial/ui/basic-layout).

#### Material changes
The format of the material basis has changed a bit. 
Some of the changes are a warning and some are an error.
You can look at the default assets to see more examples, but here's the changes:

Write mask used to be a string, and is now a map, like `write_mask = { red=true green=true blue=true alpha=true }`. Any values left out will mean false, so `write_mask = { red=true }` will write only to the red channel. 

`samplers` have been removed, images are now a regular input and not in a separate section. This affects the basis file (`.material_basis.lx`), the material instances (`.material.lx`) and the `Material.set_image`/`Material.get_image` API. 

Images are accessed by name (not index like before), like other material inputs, so the API is now `Material.set_input(material, "sprite.image", image)` and `var image = Material.get_input_image(material, "sprite.image")`.

Before (this is from `sprite.material_basis.lx`):

```js
samplers = {
  sprite.image = {
    index = 0
    type = "image2D"
    sampler_state = "linear_repeat"
  }
}
inputs = {
  sprite.uv = {
    type = "float4"
    value = [0 0 1 1]
  }
  ...
```

After:

```js
inputs = {
  sprite.image = {
    type = "image"
    value = {
      type = "image2D"
      sampler_state = "linear_repeat"
    }
  }
  sprite.uv = {
    type = "float4"
    value = [0 0 1 1]
  }
  ...
```

That's the basis, this is the material instances (this is from `logo.material.lx`):
```js
material = {
  basis = "luxe: material_basis/sprite"
  samplers = { 0 = "luxe: image/logo" }
  inputs = {
    sprite.color = [1 1 1 1]
    sprite.uv = [0 0 1 1]
  }
}
```

After:

```js
material = {
  basis = "luxe: material_basis/sprite"
  inputs = {
    sprite.image = "luxe: image/logo"
    sprite.color = [1 1 1 1]
    sprite.uv = [0 0 1 1]
  }
}
```

- docs - add wren intro
- docs - expand rendering concepts page
- docs - add UI basics + custom controls tutorial
- docs - document `UIEvent` 
- input - add `all` node for convenience
- project - fix .luxeignore folders, `path/` now ignores path
- project - project class refactored and cleaned up
- project - added injected settings to entry settings 
- project - magic settings: `project.name`, `project.version`, `project.package`
- project - magic setting `project.build_type`, one of `dev` or `release`
- outline - add default input map so e.g `arcade` just works
- samples - clear out old samples that were wrong, update ones that stay
- API - block in `Set` concept which will get used soon in more places
- game - add `engine.input.entry`, entry input asset to load
- game - main loop now running as sections with ranges + priorities
- game - main loop now accessible via `Frame` in `luxe: game`
- game - add `Frame.next`, `Frame.end` and `Frame.queue`
- game - game class refactored and cleaned up
- game - `luxe: game` for `Game`,`Renderer` for access from anywhere
- build - cache binary hash of binaries, so new builds trigger rebuilds
- world - renamed `World.tick_world` -> `World.tick`
- world - remove `World.tick_systems`, just `World.tick` is enough
- world - `Scene` scripts use `new(world)` + don't take an arg from `Scene.load`
- world - add `World.clear(world)` which empties the world
- world - fix bug in `Entity.create` causing an internal assert (Whuop)
- tiles - add `get_color` and `set_color` per tile, in data + editor as well
- render - fix missing arg in Image.redefine (Ronja)
- render - material now has stencil refs (basis->material->geo)
- render - text now uses an array of images for fonts
- render - fixed bug with text bounds + vertical align being inverted
- render - mesh data in assets can specify stencil refs
- ui - add UIWindowChange for window change events 
- ui - add layout helper (code only atm)
- ui - removed 'root' concepts in rendering, fixing several bugs + more efficient
- ui - `Control.set_events` is now plural, returns ID for `Control.unset_events`
- ui - fix `enter` and `exit` meaning something different, now works as intended
- ui - fix scroll handles stealing focus even when not visible (Ronja)
- ui - add `UI.set_material_basis(ui, solid, text)`
- strings - removed old `Glob` API (use `IO.wildcard_match(needle, haystack)`)
- material - shader library can now be specified per stage
- material - remove old samplers concepts + API (`Material.get_image/set_image`)
- material - write mask now a map `write_mask = { red=true green=true blue=true alpha=true }`
- anim - tracks now have custom events `events=[{ time=0.5 event="event" }, ...]`
- anim - anim now fires `start` and `complete` events on begin/end
- anim - use `Anim.on_event` + `|entity, anim, time, value, track_type, track, event|`
- log - fix bug in log error checking that caused an SDL_RW error on log.txt
- wren - add `Num.tau`, on instances: `num.max(val)`, `num.min(val)`, `num.clamp(min,max)`. 

## 2020.2.0 

Because of breaking changes, it's time for 2020.2.x
Note that there may be a few more changes related to the same work in 2020.2.x, 
it will always be clear what is changed.

#### UI Controls  
All UI controls (except Control itself, for now) now have 
the UI prefix for consistency. That means `Button` becomes 
`UIButton`, `Panel` => `UIPanel` etc. 

#### Image API
Previously the Image API was minimal and tucked under `Render.image_*`.
`luxe: render` now has a proper `Image` class with a bunch of queries,
a destroy function which was missing, and a `redefine` function, for
resizing or recreating the same handle under a new ImageDesc.

#### Transform API
Some of the 2D focused APIs, namely `Transform.set_depth` changed to 
`set_depth2D`, as well as `get_depth2D`. `set_angle2D` now has `get_angle2D`,
and in both cases a `_world` variant for world vs local space exists too.

- paths - fix for windows mklink needing root first (bin link)
- Added 2D depth + angle get/set for world + local
- modifiers tick in order of their priority (tilman)
- material inputs fix potential bug for defaults
- UI controls renamed
- UI canvas now requires a camera (technically was optional before)
- UI - text was flickering weirdly on some GPUs (ronja)
- UI - renamed entity arg to ui_entity for clarity

## 2020.1.2

- wren - fix some stack issues causing false script errors
- modules - fix some crashes in weird old code
- filewatch - fix some crashes due to pulling the rug on uv
- filewatch - paths normalized for consistency
- filewatch - fix bugs in add/remove e.g (bool same = strcmp(a,b))
- docs - document assert usage
- docs - update some sprite usage docs for clarity (eduardo)
- Lists.add_unique now returns true/false (true if added)
- ui - label now has color_hover options
- lx - add apply

## 2020.1.1

- block in Render.submit_now()
- Str.path uses native path normalization for consistency
- new luxe root folder support
- fix newlines in descriptions for modifiers
- `luxe: events` now uses proper hash combining
- webgl1 support fixes, including new shader support

## 2020.1.0

Another big release, lots of changes not listed likely...

#### new versioning
The new 2020.x.x format is in use. 
luxe 2020.1.x is compatible with editor 2020.1.x, 
and will generally be stable or minor changes.
This means any 2020.1.x update is safe, 
where 2020.2.x might change bigger things.

#### new project.modules.lx
This file tracks dependencies and metadata, including
the version of luxe your project is using.

#### latest wren
Previously luxe was a few years behind wren for reasons.
It's now using the latest version.

#### new prototypes
The new runtime based prototypes are online and 
mostly working, variants too. They're editable in the editor
and can be spawned and created from there. Modifiers can be 
attached to instances once spawned, and overrides applied.
There's also a newer api for dealing with the inner elements.
Prototypes are now also an entity that is returned.

#### Y+ is now up in 2D
Matches with 3D, fixes math to be consistent with trig functions,
makes animation curves not upside down, and much more.
Note that UI is still y+ down from top left origin.

#### updated samples
Many samples were migrated for Y+ up and moved to system tests.
This means they're a bit easier to read and understand, 
have a readme and more. The sample template is now 
also part of the API meaning samples share the same code.

#### `_luxe.data` is gone, `.luxe` is used
Delete `_luxe.data` from any project, it will error on random issues.


#### changes
- audio - latest soloud
- script - fix clang windows + computed gotos (faster)
- script - fix memory leak on certain (failed) file reads
- script - fix leaks from scripts loaded to wren
- assets - fix size limit of 2gb on parcels
- lx - API usage now tracks source names for better errors
- lx - fix keys with dots in working with get/set/remove
- lx - now using native LX parser, much faster overall
- io - add time_since_epoch_utc
- io - add hash file
- events - add clear_all for tag
- spaces - in user names shouldn't break anymore
- shaders - add ref keyword
- text - fix many alignment and layout bugs
- anim - fix memory leaks on certain tracks
- anim - interpolation is now per key, fallback to track
- anim - layers -> tracks
- anim - fix autoplay happening too early, fixes crashes
- anim - fix major bug on anim stop, affecting other anims
- tags - fix bug when removing tag that doesn't exist crashes
- draw - added rect detailed
- draw - circle conventions made consistent
- draw - fix circles having off by one error
- draw - ui - text now uses unique material, so no glitching
- transform - fix bug where linked entities stayed on destroy
- transform - add get_link/get_linked
- transform - add get/set world component wise
- transform - add set_euler_*_world
- transform - add get_euler_*_world
- transform - links in data are now uuid, not name
- transform - initial snap setting (for pixel snap, set to 1)
- UI - added draw rect detailed
- UI - add render mode settings (in world vs to image)
- UI - now works as intended in world space automatically
- UI - control/scroll/list: add get index for control
- UI - fix bug when control is invalid breaks further events
- UI - add window text/title size, redefine set_collapsed
- UI - fix dead entities existing in the UI <-> entity map
- UI - fix entities not destroying UI on destroy
- UI - fix render data cleanup on destroy
- bytes - add BytesWriter
- outlines - empty - add cameras to defaults
- deploy - fix luxe path when version is dev
- project - use **project.modules.lx** for dependencies
- project - now uses native wildcard, speeds up a lot
- `luxe: array` - renamed to `luxe: containers`
- Lists - add prepend/append
- added `luxe: test`, initial unit testing basis
- modules - version solver integrated (not active yet)
- text - Text.get_extents(entity) (no args)
- text - add get/set material
- modifiers - fix bug where path doesn't exist on create (tilman)
- modifiers - fix cached build state being wrong, now reliable
- modifiers - blocks are now refactored for the new workflow
- string - add quick wrap() helper
- string - add path_is_absolute
- input - add Input.deadzone(x, y, zone) for convenience
- scenes - fix multiple modifiers of same type in many layers
- scenes - fix compiling scenes from modules
- shape2d - add destroy
- shape2d - add get_bounds
- phys3d - add capsule shape
- phys3d - add cast_shape
- phys3d - add set_allow_rotation
- phys3d - add query_sphere and query_box
- phys3d - fix major bug in debug mode vs release (scaling)
- tiles - add get_all
- tiles - add get all with visual
- tiles - fix bugs with pairing functions on web target
- tiles - fix bug with tile not changing
- values - add has_key
- values - fix editor changing values
- values - add clear
- math - add random_point_in_unit_circle
- math - add smoothstep, smootherstep, weighted_avg
- math - add map_linear, nearest_power_of_two, within_range
- math - add wrap_radians, wrap_angle, lerp_angle, angle_delta
- render - add trilinear sampler states
- render - add material input blocks
- render - refactor material inputs for consistency and usage
- render - render pass layers now use material inputs (breaking)
- render - layers + images now have a display_id (renderdoc)
- image - add generate_mips flag in image.lx
- image - load before basis since they can be used as defaults now
- settings - load settings before game.wren
- build - fix script compiler error about a newline after a dot

## 1.0.0-dev.86

- tiles - fixed crash on querying empty tilemap for tags
- tiles - fixed crash in removing tiles in editor
- script - allow release builds access to modules opt in

## 1.0.0-dev.85

- io - added file watch events on desktop
- log - try more resilient log writes over cwd
- log - add log level control from entry settings
- settings - add Settings.apply
- render - blocked in image redefinition for later
- world - add `Scene.entity_list`
- world - add `Prototype.entity_list`
- modifiers - require 'class' field in modifier.lx
- modifiers - prevent using keywords in fields (tilman)
- modifiers - fix bugs in modifiers with booleans
- moduler - disable old auto download properly

## 1.0.0-dev.84

- docs - new docs for `Sprite`, `Anim` and more.
- settings - add background_sleep setting to window
- debug - fixed wren debugger on linux
- sat2d - fix returns no overlap on missed circle collision
- render - fix crash accessing out of bounds images
- tiles - add Tile api for set/get tile size
- tiles - fixed internal data desync as depth/coord change
- wren - fixed += etc not being allowed by script compiler

## 1.0.0-dev.83

- web - web deploy should work again
- world - Scene, Layer, Prototype now exist (not on World.*)
- anim - renamed animation layers -> tracks
- text - fixed vertical align with bounds > 1 line
- render - added sort_by_z, sort_by_z_reverse, none
- build - fixed bug causing run to fail on prior errors
- build - fixed jump to error for project.luxe files
- docs - added link to wren in workflow
- docs - added a few more tutorials
- docs - cleaned up some details
- Sprite - added `Sprite.contains(entity, x, y)`
- ui - scroll handles block mouse events leaking
- engine - added event stream for e.g resized

## 1.0.0-dev.82

- anim - system refactored, data changed. see samples!
- anim - return instance handles, api uses them now
- anim - repeats renamed to play_count
- anim - loop=true/false added to data files
- anim - added anim modifier, with auto play list
- anim - fixed transform anims in edit mode
- anim - add reset on stop, so state can be reverted
- anim - add y range (so y can be relative or absolute)
- anim - add play_only for solo playing
- tiles - fix bugs in painting tiles
- camera - add get/set default for a world
- camera - get_fov_vertical, get_near, get_far, get_aspect
- camera - get_projection
- entity - Entity.world -> Entity.get_world
- world - systems have a priorty to sort by (temporary)
- transform - add get_rotation_matrix
- transform - add look at, set angle axis, rotate angle axis
- transform - scene load now tries linking objects on load
- mesh - add control over enabled and active mesh levels
- mesh - add level/element count getters
- ui - select all with cmd-a/ctrl-a in text fields
- ui - add component-wise size getters for controls
- ui - fix controls crossing UI canvas owners
- ui - add engine.ui.debug_vis setting
- ui - add input graph node setting to canvas
- ui - add window close/collapse functions
- ui - add canvas enumeration
- sat2d - fix shape sweeps, poly vs poly edge case
- sat2d - return intersected, normals for sweeps
- physics - don't simulate in edit mode
- physics2d - now using bullet only, liquidfun is gone
- physics2d - refactor APIs a lot. Body2D. see samples
- physics3d - blocking in 3d apis
- bytes - add clear, write_uuid
- math - add distance for vectors, lerp
- string - fix for fixed function broke on non decimals
- assets - string data loaded in release builds
- assets - wip packable modules
- io - added zip_decompress for byte decompression
- settings - fixed bool type (fullscreen flag now works)
- window - x/y positions can be set from settings
- window - engine.runtime.window.display for which monitor
- render - better error messages in several places
- render - fix array images internally (data driven atm)
- render - added array types to material inputs/shaders
- render - send camera pos and world matrix to shaders
- render - add image generate mipmaps helper
- render - add tick to renderer script
- render - add R and RG image types
- wren - experimental debugger support via vscode
- wren - added Num log2 and exp
- wren - fixed script compiler missing new fields
- wren - optimized script compiling, more reliable now
- wren - added `+= -= /= *= &= |= >>= <<= ^= %=`

## 1.0.0-dev.81

- web builds are back (`luxe deploy --target web`)
- image - add api for getting bytes from an image
- camera - add apis for get/set matrices
- camera - add look at, clip to world and world to clip
- tiles - apis for grabbing tiles by tag and depth
- fonts - fix accessing invalid pages sometimes
- bytes - fix `pos=` assertions
- fix CI for linux builds + include linux build

## 1.0.0-dev.80

- important world bug fixes
- added settings.lx loading 

## 1.0.0-dev.79

- update samples and readmes for samples

## 1.0.0-dev.78

- fixed custom modifiers
- lots of other stuff