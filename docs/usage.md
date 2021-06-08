
## luxe: assets

### Assets
The `Assets` services is how you access loaded assets, and query if an asset is loaded.
The primary use for this at the moment is the accessors like `Assets.image`, and finding out 
if an asset is loaded via `Assets.has_image`. 

Note that the asset system is a work in progress and is not final. 
There are several accessors missing, for example, fonts are often referenced 
as a string, not via `Assets.font("fonts/name")`. Later, all assets will be unified into this form as intended.

Also, they're supposed to be able to reload dynamically, many can't currently. And remember the input
to the asset system is compiled assets, not the assets themselves. 

Finally, there are functions in the API that shouldn't be used directly (they aren't listed here.)

---

#### image(**id**: `Any`) -> Image
Return a loaded image by id.
```js
var image = Assets.image("image/player")
System.print("width: %(Image.get_width(image))")
```

#### bytes(**id**: `Any`) -> String
Returns the data stored as bytes. 
A Wren `String` is also a byte sequence, used via `string.bytes`.

**Note** That unlike other assets, bytes are stored by name _with_ extension.
For example if you put a file called `data/hello.txt` in your project,
you would access it via `var data = Assets.bytes("data/hello.txt")`.

This is because the extension might be meaningful to the user of the bytes,
for example loading an image based on png vs jpg extension would be impossible
if we don't know the extension of the data. Because bytes are "opaque", as in, 
we don't care what they store, we just store them for you to access, we keep the extension.
```js
var text = Assets.bytes("data/hello.txt")
System.print(text) //prints the contents of the file (the contents at compile time).
```

#### material(**id**: `Any`) -> Material
Returns a loaded material by id.
```js
var material = Assets.material("material/player")
Sprite.set_material(player, material)
```

#### atlas(**id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### font_page(**id**: `Any`, **page**: `Any`) -> Image
Returns the image for a particular page in a font. `page` is an index (starting at 0).

For example, if the font has several glyphs and stores 2 pages,
we can see what the pages contain using this function and assigning the image somewhere visible.
```js
var image = Assets.font_page("fonts/lato", 0)
```

#### lx(**id**: `Any`) -> Map
Returns the LX parsed representation of a `bytes` asset.
This is convenience for `Assets.bytes` followed by `LX.parse`.
Returns null if the asset isn't found, or if parsing failed.

See `Assets.bytes`, as bytes require an extension.
```js
//assuming our data contains { speaker="sara" message="follow me." }
var dialog = Assets.lx("dialog/hello.lx")
var speaker = dialog["speaker"]
var message = dialog["message"]
System.print("%(speaker): %(message)")
```

#### unload_shader_library(**id**: `Any`) -> None
Unloads the shader library with the given id.
```js
Assets.unload_shader_library("assets/shaders")
```

#### has_shader_library(**id**: `Any`) -> Bool
Returns true if a shader library with this id is loaded, or false otherwise.
```js
var exists = Assets.has_shader_library("assets/shaders")
```

#### unload_image(**id**: `Any`) -> None
Unloads the image with the given id.
```js
Assets.unload_image("image/player")
```

#### has_image(**id**: `Any`) -> Image
Returns true if an image with this id is loaded, or false otherwise.
```js
var exists = Assets.has_image("image/player")
```

#### unload_material_basis(**id**: `Any`) -> None
Unloads the material basis with the given id.
```js
Assets.unload_material_basis("basis/example")
```

#### has_material_basis(**id**: `Any`) -> Bool
Returns true if a material basis with this id is loaded, or false otherwise.
```js
var exists = Assets.has_material_basis("basis/example")
```

#### has_font(**id**: `Any`) -> Bool
Returns true if a font with this id is loaded, or false otherwise.
```js
var exists = Assets.has_font("font/lato")
```

#### compile_font(**from**: `Any`, **to**: `Any`, **ranges**: `Any`, **page_w**: `Any`, **glyph_w**: `Any`, **verbose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### unload_material(**id**: `Any`) -> None
Unloads the material with the given id.
```js
Assets.unload_material_basis("material/player")
```

#### has_material(**id**: `Any`) -> Bool
Returns true if a material with this id is loaded, or false otherwise.
```js
var exists = Assets.has_material("material/player")
```

#### unload_bytes(**id**: `Any`) -> Bool
Unloads the bytes with the given id.
```js
Assets.unload_bytes("data/hello.txt")
```

#### has_bytes(**id**: `Any`) -> Bool
Returns true if a bytes asset with this id is loaded, or false otherwise.
```js
var exists = Assets.has_bytes("data/hello.txt")
```

#### unload_settings(**id**: `Any`) -> None
Unloads the settings with the given id.
```js
Assets.unload_settings("settings/area1")
```

#### has_settings(**id**: `Any`) -> Bool
Returns true if a settings asset with this id is loaded, or false otherwise.
```js
var exists = Assets.has_settings("settings/area1")
```

#### load_atlas(**id**: `Any`, **path**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### unload_atlas(**id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### has_atlas(**id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_atlas(**id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### load_physics(**id**: `Any`, **path**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### unload_physics(**id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### has_physics(**id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### unload_prototype(**id**: `Any`) -> None
Unloads the prototype with the given id.
```js
Assets.unload_prototype("proto/tree")
```

#### has_prototype(**id**: `Any`) -> Bool
Returns true if a prototype with this id is loaded, or false otherwise.
```js
var exists = Assets.has_prototype("proto/tree")
```

#### unload_scene(**id**: `Any`) -> None
Unloads the scene with the given id.
```js
ssets.unload_scene("scene/area1")
```

#### has_scene(**id**: `Any`) -> Bool
Returns true if a scene with this id is loaded, or false otherwise.
```js
var exists = Assets.has_scene("scene/area1")
```

#### has_input(**id**: `Any`) -> Bool
Returns true if an input asset with this id is loaded, or false otherwise.
```js
var exists = Assets.has_input("input/player")
```

#### unload_anim(**id**: `Any`) -> None
Unloads the animation with the given id.
```js
Assets.unload_anim("anim/jump")
```

#### has_anim(**id**: `Any`) -> Bool
Returns true if an animation with this id is loaded, or false otherwise.
```js
var exists = Assets.has_anim("anim/jump")
```

#### unload_mesh(**id**: `Any`) -> None
Unloads the mesh with the given id.
```js
Assets.unload_mesh("mesh/cube")
```

#### has_mesh(**id**: `Any`) -> Bool
Returns true if a mesh with this id is loaded, or false otherwise.
```js
var exists = Assets.has_mesh("mesh/cube")
```

#### unload_tiles(**id**: `Any`) -> None
Unloads the tilemap with the given id.
```js
Assets.unload_tiles("tiles/caves")
```

#### has_tiles(**id**: `Any`) -> Bool
Returns true if a tilemap with this id is loaded, or false otherwise.
```js
var exists = Assets.has_tiles("tiles/caves")
```

#### unload_ui(**id**: `Any`) -> None
Unloads the ui asset with the given id.
```js
Assets.unload_ui("ui/menu")
```

#### has_ui(**id**: `Any`) -> Bool
Returns true if a ui asset with this id is loaded, or false otherwise.
```js
var exists = Assets.has_ui("ui/menu")
```

#### has_modifier(**id**: `Any`) -> Bool
Returns true if a modifier with this id is loaded, or false otherwise.
```js
var exists = Assets.has_modifier("moddifier/player")
```

#### unload_input(**id**: `Any`) -> None
Unloads the input asset with the given id.
```js
Assets.unload_input("input/player")
```

## luxe: astar

### AStar
:todo: desc

---

#### MAX -> unknown
:todo: desc
```js
//:todo: example
```

#### MAX=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### path2D(**start**: `Any`, **end**: `Any`, **cost_get_fn**: `Any`, **neighbors_get_fn**: `Any`, **heuristic_fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: bytes

### Byter
:todo: desc

---

#### pos -> unknown
:todo: desc
```js
//:todo: example
```

#### inner -> unknown
:todo: desc
```js
//:todo: example
```

#### new(**size**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### bytes() -> unknown
:todo: desc
```js
//:todo: example
```

#### write_string(**string**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_string(**string**: `Any`, **length**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_string_aligned4(**string**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_int8(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_uint8(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_int16(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_int32(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_int64(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_uint16(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_uint32(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_uint64(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_float32(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_float64(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_uuid(**uuid**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Bytes
:todo: desc

---

#### new(**elements**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### length -> unknown
:todo: desc
```js
//:todo: example
```

#### [index : Any] -> unknown
:todo: desc
```js
//:todo: example
```

#### [index : Any]=(value : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**string**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_from(**other**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### copy(**other**: `Any`, **at**: `Any`, **length**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### copy(**other**: `Any`, **to**: `Any`, **from**: `Any`, **length**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_string(**at**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_string(**at**: `Any`, **value**: `Any`, **length**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_string(**at**: `Any`, **length**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_int8(**at**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_int16(**at**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_int32(**at**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_int64(**at**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_uint8(**at**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_uint16(**at**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_uint32(**at**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_uint64(**at**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_float32(**at**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_float64(**at**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_int8(**at**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_int16(**at**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_int32(**at**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_int64(**at**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_uint8(**at**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_uint16(**at**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_uint32(**at**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_uint64(**at**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_float32(**at**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_float64(**at**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get(**at**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set(**at**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### bytes() -> unknown
:todo: desc
```js
//:todo: example
```

#### clear() -> unknown
:todo: desc
```js
//:todo: example
```

#### padding(**length**: `Any`, **align**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### padding(**length**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### BytesReader
:todo: desc

---

#### pos -> unknown
:todo: desc
```js
//:todo: example
```

#### pos=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### bytes -> unknown
:todo: desc
```js
//:todo: example
```

#### new(**source_bytes**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**string**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### skip(**count**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### check_bounds(**to_read**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_string(**length**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_int8() -> unknown
:todo: desc
```js
//:todo: example
```

#### get_int16() -> unknown
:todo: desc
```js
//:todo: example
```

#### get_int32() -> unknown
:todo: desc
```js
//:todo: example
```

#### get_int64() -> unknown
:todo: desc
```js
//:todo: example
```

#### get_uint8() -> unknown
:todo: desc
```js
//:todo: example
```

#### get_uint16() -> unknown
:todo: desc
```js
//:todo: example
```

#### get_uint32() -> unknown
:todo: desc
```js
//:todo: example
```

#### get_uint64() -> unknown
:todo: desc
```js
//:todo: example
```

#### get_float32() -> unknown
:todo: desc
```js
//:todo: example
```

#### get_float64() -> unknown
:todo: desc
```js
//:todo: example
```

### BytesWriter
:todo: desc

---

#### pos -> unknown
:todo: desc
```js
//:todo: example
```

#### pos=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### capacity -> unknown
:todo: desc
```js
//:todo: example
```

#### bytes -> unknown
:todo: desc
```js
//:todo: example
```

#### inner -> unknown
:todo: desc
```js
//:todo: example
```

#### new(**initial_length**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### resize(**new_capacity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### ensure(**write_length**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_string(**string**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_string(**string**: `Any`, **length**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_string_aligned4(**string**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_int8(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_uint8(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_int16(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_int32(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_int64(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_uint16(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_uint32(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_uint64(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_float32(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_float64(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_uuid(**uuid**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Floats
:todo: desc

---

#### new(**elements**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### length -> unknown
:todo: desc
```js
//:todo: example
```

#### capacity -> unknown
:todo: desc
```js
//:todo: example
```

#### size -> unknown
:todo: desc
```js
//:todo: example
```

#### [index : Any] -> unknown
:todo: desc
```js
//:todo: example
```

#### [index : Any]=(value : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### resize(**elements**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get(**at**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set(**at**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set(**list**: `Any`, **at**: `Any`, **list_offset**: `Any`, **count**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set(**list**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### ortho(**left**: `Any`, **top**: `Any`, **right**: `Any`, **bottom**: `Any`, **near**: `Any`, **far**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### perspective(**fov_vertical**: `Any`, **aspect**: `Any`, **near**: `Any`, **far**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### transform(**px**: `Any`, **py**: `Any`, **pz**: `Any`, **rx**: `Any`, **ry**: `Any`, **rz**: `Any`, **sx**: `Any`, **sy**: `Any`, **sz**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Uint16
:todo: desc

---

#### new(**elements**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### length -> unknown
:todo: desc
```js
//:todo: example
```

#### [index : Any] -> unknown
:todo: desc
```js
//:todo: example
```

#### [index : Any]=(value : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### get(**at**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set(**at**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set(**list**: `Any`, **at**: `Any`, **list_offset**: `Any`, **count**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set(**list**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: input

### GamepadEvent
:todo: desc

---

#### unknown -> unknown
:todo: desc
```js
//:todo: example
```

#### device_added -> unknown
:todo: desc
```js
//:todo: example
```

#### device_removed -> unknown
:todo: desc
```js
//:todo: example
```

#### device_remapped -> unknown
:todo: desc
```js
//:todo: example
```

#### name(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### InputBind
:todo: desc

---

#### unknown -> unknown
:todo: desc
```js
//:todo: example
```

#### key_state -> unknown
:todo: desc
```js
//:todo: example
```

#### mouse_state -> unknown
:todo: desc
```js
//:todo: example
```

#### mouse_axis -> unknown
:todo: desc
```js
//:todo: example
```

#### touch_state -> unknown
:todo: desc
```js
//:todo: example
```

#### touch_axis -> unknown
:todo: desc
```js
//:todo: example
```

#### gamepad_state -> unknown
:todo: desc
```js
//:todo: example
```

#### gamepad_axis -> unknown
:todo: desc
```js
//:todo: example
```

#### name(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### InputCh
:todo: desc

---

#### none -> unknown
:todo: desc
```js
//:todo: example
```

#### c01 -> unknown
:todo: desc
```js
//:todo: example
```

#### c02 -> unknown
:todo: desc
```js
//:todo: example
```

#### c03 -> unknown
:todo: desc
```js
//:todo: example
```

#### c04 -> unknown
:todo: desc
```js
//:todo: example
```

#### c05 -> unknown
:todo: desc
```js
//:todo: example
```

#### c06 -> unknown
:todo: desc
```js
//:todo: example
```

#### c07 -> unknown
:todo: desc
```js
//:todo: example
```

#### c08 -> unknown
:todo: desc
```js
//:todo: example
```

#### c09 -> unknown
:todo: desc
```js
//:todo: example
```

#### c10 -> unknown
:todo: desc
```js
//:todo: example
```

#### c11 -> unknown
:todo: desc
```js
//:todo: example
```

#### c12 -> unknown
:todo: desc
```js
//:todo: example
```

#### c13 -> unknown
:todo: desc
```js
//:todo: example
```

#### c14 -> unknown
:todo: desc
```js
//:todo: example
```

#### c15 -> unknown
:todo: desc
```js
//:todo: example
```

#### c16 -> unknown
:todo: desc
```js
//:todo: example
```

#### all -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### InputEvent
:todo: desc

---

#### new() -> unknown
:todo: desc
```js
//:todo: example
```

#### type -> unknown
:todo: desc
```js
//:todo: example
```

#### key -> unknown
:todo: desc
```js
//:todo: example
```

#### scan -> unknown
:todo: desc
```js
//:todo: example
```

#### repeat -> unknown
:todo: desc
```js
//:todo: example
```

#### mod -> unknown
:todo: desc
```js
//:todo: example
```

#### x -> unknown
:todo: desc
```js
//:todo: example
```

#### y -> unknown
:todo: desc
```js
//:todo: example
```

#### dx -> unknown
:todo: desc
```js
//:todo: example
```

#### dy -> unknown
:todo: desc
```js
//:todo: example
```

#### x_rel -> unknown
:todo: desc
```js
//:todo: example
```

#### y_rel -> unknown
:todo: desc
```js
//:todo: example
```

#### value -> unknown
:todo: desc
```js
//:todo: example
```

#### value1 -> unknown
:todo: desc
```js
//:todo: example
```

#### value2 -> unknown
:todo: desc
```js
//:todo: example
```

#### state -> unknown
:todo: desc
```js
//:todo: example
```

#### touch_id -> unknown
:todo: desc
```js
//:todo: example
```

#### axis -> unknown
:todo: desc
```js
//:todo: example
```

#### button -> unknown
:todo: desc
```js
//:todo: example
```

#### gamepad -> unknown
:todo: desc
```js
//:todo: example
```

### InputNode
:todo: desc

---

#### node -> unknown
:todo: desc
```js
//:todo: example
```

### InputState
:todo: desc

---

#### unknown -> unknown
:todo: desc
```js
//:todo: example
```

#### began -> unknown
:todo: desc
```js
//:todo: example
```

#### active -> unknown
:todo: desc
```js
//:todo: example
```

#### ended -> unknown
:todo: desc
```js
//:todo: example
```

#### name(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### InputType
:todo: desc

---

#### none -> unknown
:todo: desc
```js
//:todo: example
```

#### key_down -> unknown
:todo: desc
```js
//:todo: example
```

#### key_up -> unknown
:todo: desc
```js
//:todo: example
```

#### text -> unknown
:todo: desc
```js
//:todo: example
```

#### mouse_down -> unknown
:todo: desc
```js
//:todo: example
```

#### mouse_up -> unknown
:todo: desc
```js
//:todo: example
```

#### mouse_move -> unknown
:todo: desc
```js
//:todo: example
```

#### mouse_wheel -> unknown
:todo: desc
```js
//:todo: example
```

#### touch_down -> unknown
:todo: desc
```js
//:todo: example
```

#### touch_up -> unknown
:todo: desc
```js
//:todo: example
```

#### touch_move -> unknown
:todo: desc
```js
//:todo: example
```

#### gamepad_axis -> unknown
:todo: desc
```js
//:todo: example
```

#### gamepad_down -> unknown
:todo: desc
```js
//:todo: example
```

#### gamepad_up -> unknown
:todo: desc
```js
//:todo: example
```

#### gamepad_device -> unknown
:todo: desc
```js
//:todo: example
```

#### name(**type**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Input
:todo: desc

---

#### key_down(**key**: `Any`, **scan**: `Any`, **repeat**: `Any`, **mod**: `Any`, **timestamp**: `Any`, **window_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### key_up(**key**: `Any`, **scan**: `Any`, **mod**: `Any`, **timestamp**: `Any`, **window_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### text(**text**: `Any`, **start**: `Any`, **length**: `Any`, **type**: `Any`, **timestamp**: `Any`, **window_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### mouse_down(**x**: `Any`, **y**: `Any`, **button**: `Any`, **timestamp**: `Any`, **window_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### mouse_up(**x**: `Any`, **y**: `Any`, **button**: `Any`, **timestamp**: `Any`, **window_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### mouse_move(**x**: `Any`, **y**: `Any`, **x_rel**: `Any`, **y_rel**: `Any`, **timestamp**: `Any`, **window_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### mouse_wheel(**x**: `Any`, **y**: `Any`, **timestamp**: `Any`, **window_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### touch_down(**x**: `Any`, **y**: `Any`, **touch_id**: `Any`, **timestamp**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### touch_up(**x**: `Any`, **y**: `Any`, **touch_id**: `Any`, **timestamp**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### touch_move(**x**: `Any`, **y**: `Any`, **dx**: `Any`, **dy**: `Any`, **touch_id**: `Any`, **timestamp**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### gamepad_axis(**gamepad**: `Any`, **axis**: `Any`, **value**: `Any`, **timestamp**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### gamepad_down(**gamepad**: `Any`, **button**: `Any`, **value**: `Any`, **timestamp**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### gamepad_up(**gamepad**: `Any`, **button**: `Any`, **value**: `Any`, **timestamp**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### gamepad_device(**gamepad**: `Any`, **name**: `Any`, **type**: `Any`, **timestamp**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### deadzone(**x**: `Any`, **y**: `Any`, **zone**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### define_event(**bind_type**: `Any`, **name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### define_event(**bind_type**: `Any`, **name**: `Any`, **args**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### undefine_event(**bind_type**: `Any`, **name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### undefine_event(**name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### listen_for(**type**: `Any`, **at_node**: `Any`, **fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### listen_for(**type**: `Any`, **fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### unlisten(**type**: `Any`, **fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### unlisten(**type**: `Any`, **at_node**: `Any`, **fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### listen_for_event(**name**: `Any`, **at_node**: `Any`, **fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### listen_for_event(**name**: `Any`, **fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### unlisten_for_event(**name**: `Any`, **fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### unlisten_for_event(**name**: `Any`, **at_node**: `Any`, **fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### event_active(**name**: `Any`, **at_node**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### event_began(**name**: `Any`, **at_node**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### event_ended(**name**: `Any`, **at_node**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### event_active(**name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### event_began(**name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### event_ended(**name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### key_state_down(**key**: `Any`, **at_node**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### key_state_pressed(**key**: `Any`, **at_node**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### key_state_released(**key**: `Any`, **at_node**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_state_down(**scan**: `Any`, **at_node**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_state_pressed(**scan**: `Any`, **at_node**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_state_released(**scan**: `Any`, **at_node**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### mouse_state_down(**button**: `Any`, **at_node**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### mouse_state_pressed(**button**: `Any`, **at_node**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### mouse_state_released(**button**: `Any`, **at_node**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### mouse_state_released(**button**: `Any`, **at_node**: `Any`, **channels**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### gamepad_state_down(**gamepad**: `Any`, **button**: `Any`, **at_node**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### gamepad_state_pressed(**gamepad**: `Any`, **button**: `Any`, **at_node**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### gamepad_state_released(**gamepad**: `Any`, **button**: `Any`, **at_node**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### gamepad_state_axis(**gamepad**: `Any`, **axis**: `Any`, **at_node**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### key_state_down(**key**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### key_state_pressed(**key**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### key_state_released(**key**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_state_down(**scan**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_state_pressed(**scan**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_state_released(**scan**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### mouse_state_down(**button**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### mouse_state_released(**button**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### mouse_state_pressed(**button**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### mouse_x() -> unknown
:todo: desc
```js
//:todo: example
```

#### mouse_y() -> unknown
:todo: desc
```js
//:todo: example
```

#### mouse_x_rel() -> unknown
:todo: desc
```js
//:todo: example
```

#### mouse_y_rel() -> unknown
:todo: desc
```js
//:todo: example
```

#### set_mouse_capture(**state**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_mouse_capture() -> unknown
:todo: desc
```js
//:todo: example
```

#### gamepad_state_down(**gamepad**: `Any`, **button**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### gamepad_state_pressed(**gamepad**: `Any`, **button**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### gamepad_state_released(**gamepad**: `Any`, **button**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### gamepad_state_axis(**gamepad**: `Any`, **axis**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### define_node_front(**id**: `Any`, **type**: `Any`, **channels**: `Any`, **plus**: `Any`, **minus**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### define_node_back(**id**: `Any`, **type**: `Any`, **channels**: `Any`, **plus**: `Any`, **minus**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### define_node_after(**other**: `Any`, **id**: `Any`, **type**: `Any`, **channels**: `Any`, **plus**: `Any`, **minus**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### define_node_before(**other**: `Any`, **id**: `Any`, **type**: `Any`, **channels**: `Any`, **plus**: `Any`, **minus**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### node_defined(**node**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### undefine_node(**id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### channels_active(**at_node**: `Any`, **channels**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### channels_active(**at_node**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### channels_state(**at_node**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### channels_at(**at_node**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### channels_plus_at(**at_node**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### channels_minus_at(**at_node**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### channels_set(**at_node**: `Any`, **channels**: `Any`, **plus**: `Any`, **minus**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### channels_add(**at_node**: `Any`, **plus**: `Any`, **minus**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### channels_remove(**at_node**: `Any`, **plus**: `Any`, **minus**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### channels_add_plus(**at_node**: `Any`, **plus**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### channels_add_minus(**at_node**: `Any`, **minus**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### channels_remove_plus(**at_node**: `Any`, **plus**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### channels_remove_minus(**at_node**: `Any`, **minus**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### channels_set(**at_node**: `Any`, **channels**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### channels_set_plus(**at_node**: `Any`, **plus**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### channels_set_minus(**at_node**: `Any`, **minus**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Key
:todo: desc

---

#### unknown -> unknown
:todo: desc
```js
//:todo: example
```

#### enter -> unknown
:todo: desc
```js
//:todo: example
```

#### escape -> unknown
:todo: desc
```js
//:todo: example
```

#### backspace -> unknown
:todo: desc
```js
//:todo: example
```

#### tab -> unknown
:todo: desc
```js
//:todo: example
```

#### space -> unknown
:todo: desc
```js
//:todo: example
```

#### exclaim -> unknown
:todo: desc
```js
//:todo: example
```

#### quotedbl -> unknown
:todo: desc
```js
//:todo: example
```

#### hash -> unknown
:todo: desc
```js
//:todo: example
```

#### percent -> unknown
:todo: desc
```js
//:todo: example
```

#### dollar -> unknown
:todo: desc
```js
//:todo: example
```

#### ampersand -> unknown
:todo: desc
```js
//:todo: example
```

#### quote -> unknown
:todo: desc
```js
//:todo: example
```

#### leftparen -> unknown
:todo: desc
```js
//:todo: example
```

#### rightparen -> unknown
:todo: desc
```js
//:todo: example
```

#### asterisk -> unknown
:todo: desc
```js
//:todo: example
```

#### plus -> unknown
:todo: desc
```js
//:todo: example
```

#### comma -> unknown
:todo: desc
```js
//:todo: example
```

#### minus -> unknown
:todo: desc
```js
//:todo: example
```

#### period -> unknown
:todo: desc
```js
//:todo: example
```

#### slash -> unknown
:todo: desc
```js
//:todo: example
```

#### key_0 -> unknown
:todo: desc
```js
//:todo: example
```

#### key_1 -> unknown
:todo: desc
```js
//:todo: example
```

#### key_2 -> unknown
:todo: desc
```js
//:todo: example
```

#### key_3 -> unknown
:todo: desc
```js
//:todo: example
```

#### key_4 -> unknown
:todo: desc
```js
//:todo: example
```

#### key_5 -> unknown
:todo: desc
```js
//:todo: example
```

#### key_6 -> unknown
:todo: desc
```js
//:todo: example
```

#### key_7 -> unknown
:todo: desc
```js
//:todo: example
```

#### key_8 -> unknown
:todo: desc
```js
//:todo: example
```

#### key_9 -> unknown
:todo: desc
```js
//:todo: example
```

#### colon -> unknown
:todo: desc
```js
//:todo: example
```

#### semicolon -> unknown
:todo: desc
```js
//:todo: example
```

#### less -> unknown
:todo: desc
```js
//:todo: example
```

#### equals -> unknown
:todo: desc
```js
//:todo: example
```

#### greater -> unknown
:todo: desc
```js
//:todo: example
```

#### question -> unknown
:todo: desc
```js
//:todo: example
```

#### at -> unknown
:todo: desc
```js
//:todo: example
```

#### leftbracket -> unknown
:todo: desc
```js
//:todo: example
```

#### backslash -> unknown
:todo: desc
```js
//:todo: example
```

#### rightbracket -> unknown
:todo: desc
```js
//:todo: example
```

#### caret -> unknown
:todo: desc
```js
//:todo: example
```

#### underscore -> unknown
:todo: desc
```js
//:todo: example
```

#### backquote -> unknown
:todo: desc
```js
//:todo: example
```

#### key_a -> unknown
:todo: desc
```js
//:todo: example
```

#### key_b -> unknown
:todo: desc
```js
//:todo: example
```

#### key_c -> unknown
:todo: desc
```js
//:todo: example
```

#### key_d -> unknown
:todo: desc
```js
//:todo: example
```

#### key_e -> unknown
:todo: desc
```js
//:todo: example
```

#### key_f -> unknown
:todo: desc
```js
//:todo: example
```

#### key_g -> unknown
:todo: desc
```js
//:todo: example
```

#### key_h -> unknown
:todo: desc
```js
//:todo: example
```

#### key_i -> unknown
:todo: desc
```js
//:todo: example
```

#### key_j -> unknown
:todo: desc
```js
//:todo: example
```

#### key_k -> unknown
:todo: desc
```js
//:todo: example
```

#### key_l -> unknown
:todo: desc
```js
//:todo: example
```

#### key_m -> unknown
:todo: desc
```js
//:todo: example
```

#### key_n -> unknown
:todo: desc
```js
//:todo: example
```

#### key_o -> unknown
:todo: desc
```js
//:todo: example
```

#### key_p -> unknown
:todo: desc
```js
//:todo: example
```

#### key_q -> unknown
:todo: desc
```js
//:todo: example
```

#### key_r -> unknown
:todo: desc
```js
//:todo: example
```

#### key_s -> unknown
:todo: desc
```js
//:todo: example
```

#### key_t -> unknown
:todo: desc
```js
//:todo: example
```

#### key_u -> unknown
:todo: desc
```js
//:todo: example
```

#### key_v -> unknown
:todo: desc
```js
//:todo: example
```

#### key_w -> unknown
:todo: desc
```js
//:todo: example
```

#### key_x -> unknown
:todo: desc
```js
//:todo: example
```

#### key_y -> unknown
:todo: desc
```js
//:todo: example
```

#### key_z -> unknown
:todo: desc
```js
//:todo: example
```

#### capslock -> unknown
:todo: desc
```js
//:todo: example
```

#### f1 -> unknown
:todo: desc
```js
//:todo: example
```

#### f2 -> unknown
:todo: desc
```js
//:todo: example
```

#### f3 -> unknown
:todo: desc
```js
//:todo: example
```

#### f4 -> unknown
:todo: desc
```js
//:todo: example
```

#### f5 -> unknown
:todo: desc
```js
//:todo: example
```

#### f6 -> unknown
:todo: desc
```js
//:todo: example
```

#### f7 -> unknown
:todo: desc
```js
//:todo: example
```

#### f8 -> unknown
:todo: desc
```js
//:todo: example
```

#### f9 -> unknown
:todo: desc
```js
//:todo: example
```

#### f10 -> unknown
:todo: desc
```js
//:todo: example
```

#### f11 -> unknown
:todo: desc
```js
//:todo: example
```

#### f12 -> unknown
:todo: desc
```js
//:todo: example
```

#### printscreen -> unknown
:todo: desc
```js
//:todo: example
```

#### scrolllock -> unknown
:todo: desc
```js
//:todo: example
```

#### pause -> unknown
:todo: desc
```js
//:todo: example
```

#### insert -> unknown
:todo: desc
```js
//:todo: example
```

#### home -> unknown
:todo: desc
```js
//:todo: example
```

#### pageup -> unknown
:todo: desc
```js
//:todo: example
```

#### delete -> unknown
:todo: desc
```js
//:todo: example
```

#### end -> unknown
:todo: desc
```js
//:todo: example
```

#### pagedown -> unknown
:todo: desc
```js
//:todo: example
```

#### right -> unknown
:todo: desc
```js
//:todo: example
```

#### left -> unknown
:todo: desc
```js
//:todo: example
```

#### down -> unknown
:todo: desc
```js
//:todo: example
```

#### up -> unknown
:todo: desc
```js
//:todo: example
```

#### numlockclear -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_divide -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_multiply -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_minus -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_plus -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_enter -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_1 -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_2 -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_3 -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_4 -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_5 -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_6 -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_7 -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_8 -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_9 -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_0 -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_period -> unknown
:todo: desc
```js
//:todo: example
```

#### application -> unknown
:todo: desc
```js
//:todo: example
```

#### power -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_equals -> unknown
:todo: desc
```js
//:todo: example
```

#### f13 -> unknown
:todo: desc
```js
//:todo: example
```

#### f14 -> unknown
:todo: desc
```js
//:todo: example
```

#### f15 -> unknown
:todo: desc
```js
//:todo: example
```

#### f16 -> unknown
:todo: desc
```js
//:todo: example
```

#### f17 -> unknown
:todo: desc
```js
//:todo: example
```

#### f18 -> unknown
:todo: desc
```js
//:todo: example
```

#### f19 -> unknown
:todo: desc
```js
//:todo: example
```

#### f20 -> unknown
:todo: desc
```js
//:todo: example
```

#### f21 -> unknown
:todo: desc
```js
//:todo: example
```

#### f22 -> unknown
:todo: desc
```js
//:todo: example
```

#### f23 -> unknown
:todo: desc
```js
//:todo: example
```

#### f24 -> unknown
:todo: desc
```js
//:todo: example
```

#### execute -> unknown
:todo: desc
```js
//:todo: example
```

#### help -> unknown
:todo: desc
```js
//:todo: example
```

#### menu -> unknown
:todo: desc
```js
//:todo: example
```

#### select -> unknown
:todo: desc
```js
//:todo: example
```

#### stop -> unknown
:todo: desc
```js
//:todo: example
```

#### again -> unknown
:todo: desc
```js
//:todo: example
```

#### undo -> unknown
:todo: desc
```js
//:todo: example
```

#### cut -> unknown
:todo: desc
```js
//:todo: example
```

#### copy -> unknown
:todo: desc
```js
//:todo: example
```

#### paste -> unknown
:todo: desc
```js
//:todo: example
```

#### find -> unknown
:todo: desc
```js
//:todo: example
```

#### mute -> unknown
:todo: desc
```js
//:todo: example
```

#### volumeup -> unknown
:todo: desc
```js
//:todo: example
```

#### volumedown -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_comma -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_equalsas400 -> unknown
:todo: desc
```js
//:todo: example
```

#### alterase -> unknown
:todo: desc
```js
//:todo: example
```

#### sysreq -> unknown
:todo: desc
```js
//:todo: example
```

#### cancel -> unknown
:todo: desc
```js
//:todo: example
```

#### clear -> unknown
:todo: desc
```js
//:todo: example
```

#### prior -> unknown
:todo: desc
```js
//:todo: example
```

#### return2 -> unknown
:todo: desc
```js
//:todo: example
```

#### separator -> unknown
:todo: desc
```js
//:todo: example
```

#### out -> unknown
:todo: desc
```js
//:todo: example
```

#### oper -> unknown
:todo: desc
```js
//:todo: example
```

#### clearagain -> unknown
:todo: desc
```js
//:todo: example
```

#### crsel -> unknown
:todo: desc
```js
//:todo: example
```

#### exsel -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_00 -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_000 -> unknown
:todo: desc
```js
//:todo: example
```

#### thousandsseparator -> unknown
:todo: desc
```js
//:todo: example
```

#### decimalseparator -> unknown
:todo: desc
```js
//:todo: example
```

#### currencyunit -> unknown
:todo: desc
```js
//:todo: example
```

#### currencysubunit -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_leftparen -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_rightparen -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_leftbrace -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_rightbrace -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_tab -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_backspace -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_a -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_b -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_c -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_d -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_e -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_f -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_xor -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_power -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_percent -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_less -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_greater -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_ampersand -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_dblampersand -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_verticalbar -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_dblverticalbar -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_colon -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_hash -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_space -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_at -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_exclam -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_memstore -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_memrecall -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_memclear -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_memadd -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_memsubtract -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_memmultiply -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_memdivide -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_plusminus -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_clear -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_clearentry -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_binary -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_octal -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_decimal -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_hexadecimal -> unknown
:todo: desc
```js
//:todo: example
```

#### lctrl -> unknown
:todo: desc
```js
//:todo: example
```

#### lshift -> unknown
:todo: desc
```js
//:todo: example
```

#### lalt -> unknown
:todo: desc
```js
//:todo: example
```

#### lmeta -> unknown
:todo: desc
```js
//:todo: example
```

#### rctrl -> unknown
:todo: desc
```js
//:todo: example
```

#### rshift -> unknown
:todo: desc
```js
//:todo: example
```

#### ralt -> unknown
:todo: desc
```js
//:todo: example
```

#### rmeta -> unknown
:todo: desc
```js
//:todo: example
```

#### mode -> unknown
:todo: desc
```js
//:todo: example
```

#### audionext -> unknown
:todo: desc
```js
//:todo: example
```

#### audioprev -> unknown
:todo: desc
```js
//:todo: example
```

#### audiostop -> unknown
:todo: desc
```js
//:todo: example
```

#### audioplay -> unknown
:todo: desc
```js
//:todo: example
```

#### audiomute -> unknown
:todo: desc
```js
//:todo: example
```

#### mediaselect -> unknown
:todo: desc
```js
//:todo: example
```

#### www -> unknown
:todo: desc
```js
//:todo: example
```

#### mail -> unknown
:todo: desc
```js
//:todo: example
```

#### calculator -> unknown
:todo: desc
```js
//:todo: example
```

#### computer -> unknown
:todo: desc
```js
//:todo: example
```

#### ac_search -> unknown
:todo: desc
```js
//:todo: example
```

#### ac_home -> unknown
:todo: desc
```js
//:todo: example
```

#### ac_back -> unknown
:todo: desc
```js
//:todo: example
```

#### ac_forward -> unknown
:todo: desc
```js
//:todo: example
```

#### ac_stop -> unknown
:todo: desc
```js
//:todo: example
```

#### ac_refresh -> unknown
:todo: desc
```js
//:todo: example
```

#### ac_bookmarks -> unknown
:todo: desc
```js
//:todo: example
```

#### brightnessdown -> unknown
:todo: desc
```js
//:todo: example
```

#### brightnessup -> unknown
:todo: desc
```js
//:todo: example
```

#### displayswitch -> unknown
:todo: desc
```js
//:todo: example
```

#### kbdillumtoggle -> unknown
:todo: desc
```js
//:todo: example
```

#### kbdillumdown -> unknown
:todo: desc
```js
//:todo: example
```

#### kbdillumup -> unknown
:todo: desc
```js
//:todo: example
```

#### eject -> unknown
:todo: desc
```js
//:todo: example
```

#### sleep -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### name(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Mod
:todo: desc

---

#### none -> unknown
:todo: desc
```js
//:todo: example
```

#### lshift -> unknown
:todo: desc
```js
//:todo: example
```

#### rshift -> unknown
:todo: desc
```js
//:todo: example
```

#### lctrl -> unknown
:todo: desc
```js
//:todo: example
```

#### rctrl -> unknown
:todo: desc
```js
//:todo: example
```

#### lalt -> unknown
:todo: desc
```js
//:todo: example
```

#### ralt -> unknown
:todo: desc
```js
//:todo: example
```

#### lmeta -> unknown
:todo: desc
```js
//:todo: example
```

#### rmeta -> unknown
:todo: desc
```js
//:todo: example
```

#### num -> unknown
:todo: desc
```js
//:todo: example
```

#### caps -> unknown
:todo: desc
```js
//:todo: example
```

#### mode -> unknown
:todo: desc
```js
//:todo: example
```

#### ctrl -> unknown
:todo: desc
```js
//:todo: example
```

#### shift -> unknown
:todo: desc
```js
//:todo: example
```

#### alt -> unknown
:todo: desc
```js
//:todo: example
```

#### meta -> unknown
:todo: desc
```js
//:todo: example
```

### ModState
:todo: desc

---

#### new() -> unknown
:todo: desc
```js
//:todo: example
```

#### value=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### value -> unknown
:todo: desc
```js
//:todo: example
```

#### none -> unknown
:todo: desc
```js
//:todo: example
```

#### lshift -> unknown
:todo: desc
```js
//:todo: example
```

#### rshift -> unknown
:todo: desc
```js
//:todo: example
```

#### lctrl -> unknown
:todo: desc
```js
//:todo: example
```

#### rctrl -> unknown
:todo: desc
```js
//:todo: example
```

#### lalt -> unknown
:todo: desc
```js
//:todo: example
```

#### ralt -> unknown
:todo: desc
```js
//:todo: example
```

#### lmeta -> unknown
:todo: desc
```js
//:todo: example
```

#### rmeta -> unknown
:todo: desc
```js
//:todo: example
```

#### num -> unknown
:todo: desc
```js
//:todo: example
```

#### caps -> unknown
:todo: desc
```js
//:todo: example
```

#### mode -> unknown
:todo: desc
```js
//:todo: example
```

#### ctrl -> unknown
:todo: desc
```js
//:todo: example
```

#### shift -> unknown
:todo: desc
```js
//:todo: example
```

#### alt -> unknown
:todo: desc
```js
//:todo: example
```

#### meta -> unknown
:todo: desc
```js
//:todo: example
```

### MouseButton
:todo: desc

---

#### unknown -> unknown
:todo: desc
```js
//:todo: example
```

#### left -> unknown
:todo: desc
```js
//:todo: example
```

#### middle -> unknown
:todo: desc
```js
//:todo: example
```

#### right -> unknown
:todo: desc
```js
//:todo: example
```

#### four -> unknown
:todo: desc
```js
//:todo: example
```

#### five -> unknown
:todo: desc
```js
//:todo: example
```

#### six -> unknown
:todo: desc
```js
//:todo: example
```

#### seven -> unknown
:todo: desc
```js
//:todo: example
```

#### eight -> unknown
:todo: desc
```js
//:todo: example
```

#### name(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Scan
:todo: desc

---

#### unknown -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_a -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_b -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_c -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_d -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_e -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_f -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_g -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_h -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_i -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_j -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_k -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_l -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_m -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_n -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_o -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_p -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_q -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_r -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_s -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_t -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_u -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_v -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_w -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_x -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_y -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_z -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_1 -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_2 -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_3 -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_4 -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_5 -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_6 -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_7 -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_8 -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_9 -> unknown
:todo: desc
```js
//:todo: example
```

#### scan_0 -> unknown
:todo: desc
```js
//:todo: example
```

#### enter -> unknown
:todo: desc
```js
//:todo: example
```

#### escape -> unknown
:todo: desc
```js
//:todo: example
```

#### backspace -> unknown
:todo: desc
```js
//:todo: example
```

#### tab -> unknown
:todo: desc
```js
//:todo: example
```

#### space -> unknown
:todo: desc
```js
//:todo: example
```

#### minus -> unknown
:todo: desc
```js
//:todo: example
```

#### equals -> unknown
:todo: desc
```js
//:todo: example
```

#### leftbracket -> unknown
:todo: desc
```js
//:todo: example
```

#### rightbracket -> unknown
:todo: desc
```js
//:todo: example
```

#### backslash -> unknown
:todo: desc
```js
//:todo: example
```

#### nonushash -> unknown
:todo: desc
```js
//:todo: example
```

#### semicolon -> unknown
:todo: desc
```js
//:todo: example
```

#### apostrophe -> unknown
:todo: desc
```js
//:todo: example
```

#### grave -> unknown
:todo: desc
```js
//:todo: example
```

#### comma -> unknown
:todo: desc
```js
//:todo: example
```

#### period -> unknown
:todo: desc
```js
//:todo: example
```

#### slash -> unknown
:todo: desc
```js
//:todo: example
```

#### capslock -> unknown
:todo: desc
```js
//:todo: example
```

#### f1 -> unknown
:todo: desc
```js
//:todo: example
```

#### f2 -> unknown
:todo: desc
```js
//:todo: example
```

#### f3 -> unknown
:todo: desc
```js
//:todo: example
```

#### f4 -> unknown
:todo: desc
```js
//:todo: example
```

#### f5 -> unknown
:todo: desc
```js
//:todo: example
```

#### f6 -> unknown
:todo: desc
```js
//:todo: example
```

#### f7 -> unknown
:todo: desc
```js
//:todo: example
```

#### f8 -> unknown
:todo: desc
```js
//:todo: example
```

#### f9 -> unknown
:todo: desc
```js
//:todo: example
```

#### f10 -> unknown
:todo: desc
```js
//:todo: example
```

#### f11 -> unknown
:todo: desc
```js
//:todo: example
```

#### f12 -> unknown
:todo: desc
```js
//:todo: example
```

#### printscreen -> unknown
:todo: desc
```js
//:todo: example
```

#### scrolllock -> unknown
:todo: desc
```js
//:todo: example
```

#### pause -> unknown
:todo: desc
```js
//:todo: example
```

#### insert -> unknown
:todo: desc
```js
//:todo: example
```

#### home -> unknown
:todo: desc
```js
//:todo: example
```

#### pageup -> unknown
:todo: desc
```js
//:todo: example
```

#### delete -> unknown
:todo: desc
```js
//:todo: example
```

#### end -> unknown
:todo: desc
```js
//:todo: example
```

#### pagedown -> unknown
:todo: desc
```js
//:todo: example
```

#### right -> unknown
:todo: desc
```js
//:todo: example
```

#### left -> unknown
:todo: desc
```js
//:todo: example
```

#### down -> unknown
:todo: desc
```js
//:todo: example
```

#### up -> unknown
:todo: desc
```js
//:todo: example
```

#### numlockclear -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_divide -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_multiply -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_minus -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_plus -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_enter -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_1 -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_2 -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_3 -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_4 -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_5 -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_6 -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_7 -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_8 -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_9 -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_0 -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_period -> unknown
:todo: desc
```js
//:todo: example
```

#### nonusbackslash -> unknown
:todo: desc
```js
//:todo: example
```

#### application -> unknown
:todo: desc
```js
//:todo: example
```

#### power -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_equals -> unknown
:todo: desc
```js
//:todo: example
```

#### f13 -> unknown
:todo: desc
```js
//:todo: example
```

#### f14 -> unknown
:todo: desc
```js
//:todo: example
```

#### f15 -> unknown
:todo: desc
```js
//:todo: example
```

#### f16 -> unknown
:todo: desc
```js
//:todo: example
```

#### f17 -> unknown
:todo: desc
```js
//:todo: example
```

#### f18 -> unknown
:todo: desc
```js
//:todo: example
```

#### f19 -> unknown
:todo: desc
```js
//:todo: example
```

#### f20 -> unknown
:todo: desc
```js
//:todo: example
```

#### f21 -> unknown
:todo: desc
```js
//:todo: example
```

#### f22 -> unknown
:todo: desc
```js
//:todo: example
```

#### f23 -> unknown
:todo: desc
```js
//:todo: example
```

#### f24 -> unknown
:todo: desc
```js
//:todo: example
```

#### execute -> unknown
:todo: desc
```js
//:todo: example
```

#### help -> unknown
:todo: desc
```js
//:todo: example
```

#### menu -> unknown
:todo: desc
```js
//:todo: example
```

#### select -> unknown
:todo: desc
```js
//:todo: example
```

#### stop -> unknown
:todo: desc
```js
//:todo: example
```

#### again -> unknown
:todo: desc
```js
//:todo: example
```

#### undo -> unknown
:todo: desc
```js
//:todo: example
```

#### cut -> unknown
:todo: desc
```js
//:todo: example
```

#### copy -> unknown
:todo: desc
```js
//:todo: example
```

#### paste -> unknown
:todo: desc
```js
//:todo: example
```

#### find -> unknown
:todo: desc
```js
//:todo: example
```

#### mute -> unknown
:todo: desc
```js
//:todo: example
```

#### volumeup -> unknown
:todo: desc
```js
//:todo: example
```

#### volumedown -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_comma -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_equalsas400 -> unknown
:todo: desc
```js
//:todo: example
```

#### international1 -> unknown
:todo: desc
```js
//:todo: example
```

#### international2 -> unknown
:todo: desc
```js
//:todo: example
```

#### international3 -> unknown
:todo: desc
```js
//:todo: example
```

#### international4 -> unknown
:todo: desc
```js
//:todo: example
```

#### international5 -> unknown
:todo: desc
```js
//:todo: example
```

#### international6 -> unknown
:todo: desc
```js
//:todo: example
```

#### international7 -> unknown
:todo: desc
```js
//:todo: example
```

#### international8 -> unknown
:todo: desc
```js
//:todo: example
```

#### international9 -> unknown
:todo: desc
```js
//:todo: example
```

#### lang1 -> unknown
:todo: desc
```js
//:todo: example
```

#### lang2 -> unknown
:todo: desc
```js
//:todo: example
```

#### lang3 -> unknown
:todo: desc
```js
//:todo: example
```

#### lang4 -> unknown
:todo: desc
```js
//:todo: example
```

#### lang5 -> unknown
:todo: desc
```js
//:todo: example
```

#### lang6 -> unknown
:todo: desc
```js
//:todo: example
```

#### lang7 -> unknown
:todo: desc
```js
//:todo: example
```

#### lang8 -> unknown
:todo: desc
```js
//:todo: example
```

#### lang9 -> unknown
:todo: desc
```js
//:todo: example
```

#### alterase -> unknown
:todo: desc
```js
//:todo: example
```

#### sysreq -> unknown
:todo: desc
```js
//:todo: example
```

#### cancel -> unknown
:todo: desc
```js
//:todo: example
```

#### clear -> unknown
:todo: desc
```js
//:todo: example
```

#### prior -> unknown
:todo: desc
```js
//:todo: example
```

#### return2 -> unknown
:todo: desc
```js
//:todo: example
```

#### separator -> unknown
:todo: desc
```js
//:todo: example
```

#### out -> unknown
:todo: desc
```js
//:todo: example
```

#### oper -> unknown
:todo: desc
```js
//:todo: example
```

#### clearagain -> unknown
:todo: desc
```js
//:todo: example
```

#### crsel -> unknown
:todo: desc
```js
//:todo: example
```

#### exsel -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_00 -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_000 -> unknown
:todo: desc
```js
//:todo: example
```

#### thousandsseparator -> unknown
:todo: desc
```js
//:todo: example
```

#### decimalseparator -> unknown
:todo: desc
```js
//:todo: example
```

#### currencyunit -> unknown
:todo: desc
```js
//:todo: example
```

#### currencysubunit -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_leftparen -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_rightparen -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_leftbrace -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_rightbrace -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_tab -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_backspace -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_a -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_b -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_c -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_d -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_e -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_f -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_xor -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_power -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_percent -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_less -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_greater -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_ampersand -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_dblampersand -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_verticalbar -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_dblverticalbar -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_colon -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_hash -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_space -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_at -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_exclam -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_memstore -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_memrecall -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_memclear -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_memadd -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_memsubtract -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_memmultiply -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_memdivide -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_plusminus -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_clear -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_clearentry -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_binary -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_octal -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_decimal -> unknown
:todo: desc
```js
//:todo: example
```

#### kp_hexadecimal -> unknown
:todo: desc
```js
//:todo: example
```

#### lctrl -> unknown
:todo: desc
```js
//:todo: example
```

#### lshift -> unknown
:todo: desc
```js
//:todo: example
```

#### lalt -> unknown
:todo: desc
```js
//:todo: example
```

#### lmeta -> unknown
:todo: desc
```js
//:todo: example
```

#### rctrl -> unknown
:todo: desc
```js
//:todo: example
```

#### rshift -> unknown
:todo: desc
```js
//:todo: example
```

#### ralt -> unknown
:todo: desc
```js
//:todo: example
```

#### rmeta -> unknown
:todo: desc
```js
//:todo: example
```

#### mode -> unknown
:todo: desc
```js
//:todo: example
```

#### audionext -> unknown
:todo: desc
```js
//:todo: example
```

#### audioprev -> unknown
:todo: desc
```js
//:todo: example
```

#### audiostop -> unknown
:todo: desc
```js
//:todo: example
```

#### audioplay -> unknown
:todo: desc
```js
//:todo: example
```

#### audiomute -> unknown
:todo: desc
```js
//:todo: example
```

#### mediaselect -> unknown
:todo: desc
```js
//:todo: example
```

#### www -> unknown
:todo: desc
```js
//:todo: example
```

#### mail -> unknown
:todo: desc
```js
//:todo: example
```

#### calculator -> unknown
:todo: desc
```js
//:todo: example
```

#### computer -> unknown
:todo: desc
```js
//:todo: example
```

#### ac_search -> unknown
:todo: desc
```js
//:todo: example
```

#### ac_home -> unknown
:todo: desc
```js
//:todo: example
```

#### ac_back -> unknown
:todo: desc
```js
//:todo: example
```

#### ac_forward -> unknown
:todo: desc
```js
//:todo: example
```

#### ac_stop -> unknown
:todo: desc
```js
//:todo: example
```

#### ac_refresh -> unknown
:todo: desc
```js
//:todo: example
```

#### ac_bookmarks -> unknown
:todo: desc
```js
//:todo: example
```

#### brightnessdown -> unknown
:todo: desc
```js
//:todo: example
```

#### brightnessup -> unknown
:todo: desc
```js
//:todo: example
```

#### displayswitch -> unknown
:todo: desc
```js
//:todo: example
```

#### kbdillumtoggle -> unknown
:todo: desc
```js
//:todo: example
```

#### kbdillumdown -> unknown
:todo: desc
```js
//:todo: example
```

#### kbdillumup -> unknown
:todo: desc
```js
//:todo: example
```

#### eject -> unknown
:todo: desc
```js
//:todo: example
```

#### sleep -> unknown
:todo: desc
```js
//:todo: example
```

#### app1 -> unknown
:todo: desc
```js
//:todo: example
```

#### app2 -> unknown
:todo: desc
```js
//:todo: example
```

#### MAX -> unknown
:todo: desc
```js
//:todo: example
```

### TextEvent
:todo: desc

---

#### unknown -> unknown
:todo: desc
```js
//:todo: example
```

#### edit -> unknown
:todo: desc
```js
//:todo: example
```

#### input -> unknown
:todo: desc
```js
//:todo: example
```

#### name(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: io

### Flags
:todo: desc

---

#### new(**args**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### all() -> unknown
:todo: desc
```js
//:todo: example
```

#### has(**flag**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### value(**flag**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### value(**flag**: `Any`, **require**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### values(**flag**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### values(**flag**: `Any`, **require**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: lx

### LX
:todo: desc

---

#### parse_bytes(**source_name**: `Any`, **bytes**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### read(**path**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### read(**source_id**: `Any`, **path**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### parse(**data**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### parse(**source_path**: `Any`, **data**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### apply(**from**: `Any`, **to**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### clone(**lx**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### equal(**lxA**: `Any`, **lxB**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### delta(**lxA**: `Any`, **lxB**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### delta_apply(**lx**: `Any`, **delta**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### delta_unapply(**lx**: `Any`, **delta**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### key_get(**lx**: `Any`, **key**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### key_get_via_list(**lx**: `Any`, **key**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### key_remove(**lx**: `Any`, **key**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### key_remove_via_list(**lx**: `Any`, **key**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### key_set(**lx**: `Any`, **key**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### key_set_via_list(**lx**: `Any`, **key**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### stringify(**root**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### stringify(**root**: `Any`, **spaces**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### stringify(**root**: `Any`, **spaces**: `Any`, **with_root**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### stringify_to_bytes(**root**: `Any`, **max_size**: `Any`, **spaces**: `Any`, **with_root**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write(**contents**: `Any`, **path**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write(**contents**: `Any`, **path**: `Any`, **spaces**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### write(**contents**: `Any`, **path**: `Any`, **spaces**: `Any`, **with_root**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### stringify_to_file(**root**: `Any`, **path**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### stringify_to_file(**root**: `Any`, **path**: `Any`, **spaces**: `Any`, **with_root**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### flatten(**lx**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### flatten(**lx**: `Any`, **delimiter**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: mat4

### Matrix
:todo: desc

---

#### new() -> unknown
:todo: desc
```js
//:todo: example
```

#### m -> unknown
:todo: desc
```js
//:todo: example
```

#### ortho(**left**: `Any`, **right**: `Any`, **top**: `Any`, **bottom**: `Any`, **near**: `Any`, **far**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### pos_x -> unknown
:todo: desc
```js
//:todo: example
```

#### pos_y -> unknown
:todo: desc
```js
//:todo: example
```

#### pos_z -> unknown
:todo: desc
```js
//:todo: example
```

#### pos_x=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### pos_y=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### pos_z=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### pos -> unknown
:todo: desc
```js
//:todo: example
```

#### pos=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### scale_x -> unknown
:todo: desc
```js
//:todo: example
```

#### scale_y -> unknown
:todo: desc
```js
//:todo: example
```

#### scale_z -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: math

### Math
:todo: desc

---

#### length(**x**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### length(**x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### length(**vec**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### length2D(**vec**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### length_sq(**x**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### length_sq(**x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### length_sq(**vec**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### length_sq2D(**vec**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### dot(**x**: `Any`, **y**: `Any`, **z**: `Any`, **other_x**: `Any`, **other_y**: `Any`, **other_z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### dot(**x**: `Any`, **y**: `Any`, **other_x**: `Any`, **other_y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### dot(**vec**: `Any`, **other**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### dot2D(**vec**: `Any`, **other**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### cross(**a**: `Any`, **b**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### angle(**from**: `Any`, **to**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### angle(**v1**: `Any`, **v2**: `Any`, **up**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### normalize2D(**vec**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### normalize(**vec**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### dist(**x**: `Any`, **y**: `Any`, **z**: `Any`, **other_x**: `Any`, **other_y**: `Any`, **other_z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### dist(**vec**: `Any`, **other**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### dist2D(**vec**: `Any`, **other**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### dist2D(**x**: `Any`, **y**: `Any`, **other_x**: `Any`, **other_y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### dir2D(**pos**: `Any`, **target**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### rotate(**vec**: `Any`, **ox**: `Any`, **oy**: `Any`, **angle**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### ray_intersect_plane(**plane_x**: `Any`, **plane_y**: `Any`, **plane_z**: `Any`, **normal_x**: `Any`, **normal_y**: `Any`, **normal_z**: `Any`, **ray_x**: `Any`, **ray_y**: `Any`, **ray_z**: `Any`, **ray_dir_x**: `Any`, **ray_dir_y**: `Any`, **ray_dir_z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### closest_point_on_plane(**plane_x**: `Any`, **plane_y**: `Any`, **plane_z**: `Any`, **normal_x**: `Any`, **normal_y**: `Any`, **normal_z**: `Any`, **point_x**: `Any`, **point_y**: `Any`, **point_z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### closest_point_on_line(**line_x**: `Any`, **line_y**: `Any`, **line_z**: `Any`, **line_end_x**: `Any`, **line_end_y**: `Any`, **line_end_z**: `Any`, **point_x**: `Any`, **point_y**: `Any`, **point_z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### in_rect(**x**: `Any`, **y**: `Any`, **rx**: `Any`, **ry**: `Any`, **rw**: `Any`, **rh**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### overlaps(**x0**: `Any`, **y0**: `Any`, **w0**: `Any`, **h0**: `Any`, **x1**: `Any`, **y1**: `Any`, **w1**: `Any`, **h1**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### sign(**x**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### sign0(**x**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### atan2(**y**: `Any`, **x**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### degrees(**radians**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### radians(**degrees**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### clamp(**value**: `Any`, **a**: `Any`, **b**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### min(**a**: `Any`, **b**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### max(**a**: `Any`, **b**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### floor_around_zero(**a**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### ceil_around_zero(**a**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### fixed(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### fixed(**value**: `Any`, **precision**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### angle_delta(**a**: `Any`, **b**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### lerp(**a**: `Any`, **b**: `Any`, **t**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### lerp_angle(**a**: `Any`, **b**: `Any`, **t**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### weighted_avg(**value**: `Any`, **target**: `Any`, **slowness**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### within_range(**value**: `Any`, **start_range**: `Any`, **end_range**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### wrap_angle(**degrees**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### wrap_angle(**degrees**: `Any`, **lower**: `Any`, **upper**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### wrap_radians(**radians**: `Any`, **lower**: `Any`, **upper**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### nearest_power_of_two(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### map_linear(**value**: `Any`, **a1**: `Any`, **a2**: `Any`, **b1**: `Any`, **b2**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### smoothstep(**x**: `Any`, **min**: `Any`, **max**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### smootherstep(**x**: `Any`, **min**: `Any`, **max**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### random_point_in_unit_circle(**rng**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: pqueue

### MaxPQ
:todo: desc

---

#### value -> unknown
:todo: desc
```js
//:todo: example
```

#### count -> unknown
:todo: desc
```js
//:todo: example
```

#### new() -> unknown
:todo: desc
```js
//:todo: example
```

#### new(**get_priority_fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### add(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### pop() -> unknown
:todo: desc
```js
//:todo: example
```

#### peek() -> unknown
:todo: desc
```js
//:todo: example
```

#### sift_up(**index**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### sift_down(**index**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### MinPQ
:todo: desc

---

#### value -> unknown
:todo: desc
```js
//:todo: example
```

#### count -> unknown
:todo: desc
```js
//:todo: example
```

#### new() -> unknown
:todo: desc
```js
//:todo: example
```

#### new(**get_priority_fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### add(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### pop() -> unknown
:todo: desc
```js
//:todo: example
```

#### peek() -> unknown
:todo: desc
```js
//:todo: example
```

#### sift_up(**index**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### sift_down(**index**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: regex

## luxe: render

### Atlas
:todo: desc

---

#### create(**size**: `Any`, **material**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy(**atlas**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### valid(**atlas**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_size(**atlas**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_material(**atlas**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### rect_add(**atlas**: `Any`, **atlas_image_id**: `Any`, **frame**: `Any`, **rect**: `Any`, **rotated**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### rect_remove(**atlas**: `Any`, **atlas_image_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### rect_get_frame(**atlas**: `Any`, **atlas_image**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### rect_get_rect(**atlas**: `Any`, **atlas_image**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### rect_get_rotated(**atlas**: `Any`, **atlas_image**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### BlendFactor
:todo: desc

---

#### zero -> unknown
:todo: desc
```js
//:todo: example
```

#### one -> unknown
:todo: desc
```js
//:todo: example
```

#### source_color -> unknown
:todo: desc
```js
//:todo: example
```

#### one_minus_source_color -> unknown
:todo: desc
```js
//:todo: example
```

#### source_alpha -> unknown
:todo: desc
```js
//:todo: example
```

#### one_minus_source_alpha -> unknown
:todo: desc
```js
//:todo: example
```

#### destination_color -> unknown
:todo: desc
```js
//:todo: example
```

#### one_minus_destination_color -> unknown
:todo: desc
```js
//:todo: example
```

#### destination_alpha -> unknown
:todo: desc
```js
//:todo: example
```

#### one_minus_destination_alpha -> unknown
:todo: desc
```js
//:todo: example
```

#### source_alpha_saturated -> unknown
:todo: desc
```js
//:todo: example
```

#### blend_color -> unknown
:todo: desc
```js
//:todo: example
```

#### one_minus_blend_color -> unknown
:todo: desc
```js
//:todo: example
```

#### blend_alpha -> unknown
:todo: desc
```js
//:todo: example
```

#### one_minus_blend_alpha -> unknown
:todo: desc
```js
//:todo: example
```

#### invalid -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### BlendOperation
:todo: desc

---

#### add -> unknown
:todo: desc
```js
//:todo: example
```

#### subtract -> unknown
:todo: desc
```js
//:todo: example
```

#### reverse_subtract -> unknown
:todo: desc
```js
//:todo: example
```

#### min -> unknown
:todo: desc
```js
//:todo: example
```

#### max -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### ColorWriteMask
:todo: desc

---

#### none -> unknown
:todo: desc
```js
//:todo: example
```

#### red -> unknown
:todo: desc
```js
//:todo: example
```

#### green -> unknown
:todo: desc
```js
//:todo: example
```

#### blue -> unknown
:todo: desc
```js
//:todo: example
```

#### alpha -> unknown
:todo: desc
```js
//:todo: example
```

#### all -> unknown
:todo: desc
```js
//:todo: example
```

#### invalid -> unknown
:todo: desc
```js
//:todo: example
```

#### from_map(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### CompareFunction
:todo: desc

---

#### never -> unknown
:todo: desc
```js
//:todo: example
```

#### less -> unknown
:todo: desc
```js
//:todo: example
```

#### equal -> unknown
:todo: desc
```js
//:todo: example
```

#### less_equal -> unknown
:todo: desc
```js
//:todo: example
```

#### greater -> unknown
:todo: desc
```js
//:todo: example
```

#### not_equal -> unknown
:todo: desc
```js
//:todo: example
```

#### greater_equal -> unknown
:todo: desc
```js
//:todo: example
```

#### always -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### ComputeLayerDesc
:todo: desc

---

#### new() -> unknown
:todo: desc
```js
//:todo: example
```

#### compute_id -> unknown
:todo: desc
```js
//:todo: example
```

#### compute_id=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### dispatch_type -> unknown
:todo: desc
```js
//:todo: example
```

#### dispatch_type=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### x -> unknown
:todo: desc
```js
//:todo: example
```

#### x=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### y -> unknown
:todo: desc
```js
//:todo: example
```

#### y=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### z -> unknown
:todo: desc
```js
//:todo: example
```

#### z=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

### CullMode
:todo: desc

---

#### none -> unknown
:todo: desc
```js
//:todo: example
```

#### front -> unknown
:todo: desc
```js
//:todo: example
```

#### back -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Geometry
:todo: desc

---

#### create(**primitive**: `Any`, **material**: `Any`, **index_count**: `Any`, **index_type**: `Any`, **index_buffer**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create(**primitive**: `Any`, **material**: `Any`, **vert_count**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy(**geo**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### valid(**geo**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_world_matrix(**geo**: `Any`, **world**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_vertex_buffer(**geo**: `Any`, **index**: `Any`, **vertex_buffer**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_vertex_buffer(**geo**: `Any`, **index**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_index_buffer(**geo**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_instance_count(**geo**: `Any`, **count**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_instance_count(**geo**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_vert_count(**geo**: `Any`, **count**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_material(**geo**: `Any`, **material**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_stencil_references(**geo**: `Any`, **back**: `Any`, **front**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_stencil_reference(**geo**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_aabb(**geo**: `Any`, **center_x**: `Any`, **center_y**: `Any`, **center_z**: `Any`, **radius_x**: `Any`, **radius_y**: `Any`, **radius_z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_world_obb(**geo**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_vert_count(**geo**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_material(**geo**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### obb_intersect_ray(**geo**: `Any`, **ray_x**: `Any`, **ray_y**: `Any`, **ray_z**: `Any`, **ray_dir_x**: `Any`, **ray_dir_y**: `Any`, **ray_dir_z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### layer_include_add(**geo**: `Any`, **layer_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### layer_include_remove(**geo**: `Any`, **layer_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### layer_exclude_add(**geo**: `Any`, **layer_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### layer_exclude_remove(**geo**: `Any`, **layer_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Image
:todo: desc

---

#### create(**desc**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### redefine(**image**: `Any`, **desc**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy(**name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### valid(**name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_resource(**name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### generate_mipmaps(**image**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### update(**image**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`, **level**: `Any`, **slice**: `Any`, **bytes**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_type(**image**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_width(**image**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_height(**image**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_depth(**image**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_pixel_format(**image**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_mipmap_levels(**image**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_array_length(**image**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_sample_count(**image**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_bytes(**image**: `Any`, **into_bytes**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### ImageDesc
:todo: desc

---

#### display_id -> unknown
:todo: desc
```js
//:todo: example
```

#### display_id=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### type -> unknown
:todo: desc
```js
//:todo: example
```

#### type=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### pixel_format -> unknown
:todo: desc
```js
//:todo: example
```

#### pixel_format=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### width -> unknown
:todo: desc
```js
//:todo: example
```

#### width=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### height -> unknown
:todo: desc
```js
//:todo: example
```

#### height=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### depth -> unknown
:todo: desc
```js
//:todo: example
```

#### depth=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### mipmap_levels -> unknown
:todo: desc
```js
//:todo: example
```

#### mipmap_levels=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### array_length -> unknown
:todo: desc
```js
//:todo: example
```

#### array_length=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### sample_count -> unknown
:todo: desc
```js
//:todo: example
```

#### sample_count=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### new() -> unknown
:todo: desc
```js
//:todo: example
```

### ImageType
:todo: desc

---

#### invalid -> unknown
:todo: desc
```js
//:todo: example
```

#### image1D -> unknown
:todo: desc
```js
//:todo: example
```

#### image1DArray -> unknown
:todo: desc
```js
//:todo: example
```

#### image2D -> unknown
:todo: desc
```js
//:todo: example
```

#### image2DArray -> unknown
:todo: desc
```js
//:todo: example
```

#### image2DMultisample -> unknown
:todo: desc
```js
//:todo: example
```

#### imageCube -> unknown
:todo: desc
```js
//:todo: example
```

#### imageCubeArray -> unknown
:todo: desc
```js
//:todo: example
```

#### image3D -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### name(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### IndexType
:todo: desc

---

#### none -> unknown
:todo: desc
```js
//:todo: example
```

#### u16 -> unknown
:todo: desc
```js
//:todo: example
```

#### u32 -> unknown
:todo: desc
```js
//:todo: example
```

#### size_of(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### LayerCompute
:todo: desc

---

#### new(**path**: `Any`, **inputs**: `Any`, **images**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create_material(**inputs**: `Any`, **images**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### LayerPass
:todo: desc

---

#### new(**path**: `Any`, **pass**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create_dest(**pass**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create_material(**pass**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### LoadAction
:todo: desc

---

#### dont_care -> unknown
:todo: desc
```js
//:todo: example
```

#### load -> unknown
:todo: desc
```js
//:todo: example
```

#### clear -> unknown
:todo: desc
```js
//:todo: example
```

### Material
:todo: desc

---

#### create(**basis_type**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### clone(**material**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy(**material**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### valid(**material**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### undefine(**name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_source_id(**material**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_source_id(**material**: `Any`, **source_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_stencil_references(**material**: `Any`, **back**: `Any`, **front**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_stencil_reference(**material**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_input_image(**material**: `Any`, **name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### has_input(**material**: `Any`, **name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### is_input_array(**material**: `Any`, **name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_input(**material**: `Any`, **name**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### define(**name**: `Any`, **desc**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### MaterialDesc
:todo: desc

---

#### new() -> unknown
:todo: desc
```js
//:todo: example
```

#### vertex_format -> unknown
:todo: desc
```js
//:todo: example
```

#### vertex_format=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### vertex -> unknown
:todo: desc
```js
//:todo: example
```

#### vertex=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### fragment -> unknown
:todo: desc
```js
//:todo: example
```

#### fragment=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### geometry -> unknown
:todo: desc
```js
//:todo: example
```

#### geometry=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### depth_bias_enabled -> unknown
:todo: desc
```js
//:todo: example
```

#### depth_bias_enabled=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### depth_bias -> unknown
:todo: desc
```js
//:todo: example
```

#### depth_bias=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### depth_bias_slope_scale -> unknown
:todo: desc
```js
//:todo: example
```

#### depth_bias_slope_scale=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### depth_test -> unknown
:todo: desc
```js
//:todo: example
```

#### depth_test=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### depth_write -> unknown
:todo: desc
```js
//:todo: example
```

#### depth_write=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### depth_compare -> unknown
:todo: desc
```js
//:todo: example
```

#### depth_compare=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_test -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_test=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### write_mask -> unknown
:todo: desc
```js
//:todo: example
```

#### write_mask=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### blending -> unknown
:todo: desc
```js
//:todo: example
```

#### blending=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### alpha_blend -> unknown
:todo: desc
```js
//:todo: example
```

#### alpha_blend=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### rgb_blend -> unknown
:todo: desc
```js
//:todo: example
```

#### rgb_blend=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### src_alpha -> unknown
:todo: desc
```js
//:todo: example
```

#### src_alpha=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### src_rgb -> unknown
:todo: desc
```js
//:todo: example
```

#### src_rgb=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### dest_alpha -> unknown
:todo: desc
```js
//:todo: example
```

#### dest_alpha=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### dest_rgb -> unknown
:todo: desc
```js
//:todo: example
```

#### dest_rgb=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### blend_color -> unknown
:todo: desc
```js
//:todo: example
```

#### blend_color=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### cull -> unknown
:todo: desc
```js
//:todo: example
```

#### cull=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### winding -> unknown
:todo: desc
```js
//:todo: example
```

#### winding=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### layers -> unknown
:todo: desc
```js
//:todo: example
```

#### layers=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### inputs -> unknown
:todo: desc
```js
//:todo: example
```

#### inputs=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### blocks -> unknown
:todo: desc
```js
//:todo: example
```

#### blocks=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_back_failure_stencil -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_back_failure_stencil=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_back_failure_depth -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_back_failure_depth=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_back_pass_depth_stencil -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_back_pass_depth_stencil=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_back_compare -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_back_compare=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_back_mask_read -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_back_mask_read=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_back_mask_write -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_back_mask_write=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_back_reference -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_back_reference=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_front_failure_stencil -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_front_failure_stencil=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_front_failure_depth -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_front_failure_depth=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_front_pass_depth_stencil -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_front_pass_depth_stencil=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_front_compare -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_front_compare=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_front_mask_read -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_front_mask_read=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_front_mask_write -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_front_mask_write=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_front_reference -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil_front_reference=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

### MaterialFunction
:todo: desc

---

#### library -> unknown
:todo: desc
```js
//:todo: example
```

#### library=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### function -> unknown
:todo: desc
```js
//:todo: example
```

#### function=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### new() -> unknown
:todo: desc
```js
//:todo: example
```

### MaterialInput
:todo: desc

---

#### name -> unknown
:todo: desc
```js
//:todo: example
```

#### name=(name : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### type -> unknown
:todo: desc
```js
//:todo: example
```

#### type=(type : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### value -> unknown
:todo: desc
```js
//:todo: example
```

#### value=(value : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### count -> unknown
:todo: desc
```js
//:todo: example
```

#### count=(count : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### new() -> unknown
:todo: desc
```js
//:todo: example
```

#### new(**name**: `Any`, **type**: `Any`, **value**: `Any`, **count**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### new(**name**: `Any`, **type**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### init(**name**: `Any`, **type**: `Any`, **value**: `Any`, **count**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### MaterialInputBlock
:todo: desc

---

#### get_defined(**name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### has_input(**block**: `Any`, **name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### is_input_array(**block**: `Any`, **name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set(**block**: `Any`, **name**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### MaterialInputImage
:todo: desc

---

#### image -> unknown
:todo: desc
```js
//:todo: example
```

#### image=(image : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### type -> unknown
:todo: desc
```js
//:todo: example
```

#### type=(type : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### sampler -> unknown
:todo: desc
```js
//:todo: example
```

#### sampler=(value : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### new() -> unknown
:todo: desc
```js
//:todo: example
```

#### new(**in_image**: `Any`, **in_sampler**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### new(**in_image**: `Any`, **in_sampler**: `Any`, **in_type**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### MaterialInputType
:todo: desc

---

#### invalid -> unknown
:todo: desc
```js
//:todo: example
```

#### bool -> unknown
:todo: desc
```js
//:todo: example
```

#### bool2 -> unknown
:todo: desc
```js
//:todo: example
```

#### bool3 -> unknown
:todo: desc
```js
//:todo: example
```

#### bool4 -> unknown
:todo: desc
```js
//:todo: example
```

#### int -> unknown
:todo: desc
```js
//:todo: example
```

#### int2 -> unknown
:todo: desc
```js
//:todo: example
```

#### int3 -> unknown
:todo: desc
```js
//:todo: example
```

#### int4 -> unknown
:todo: desc
```js
//:todo: example
```

#### uint -> unknown
:todo: desc
```js
//:todo: example
```

#### uint2 -> unknown
:todo: desc
```js
//:todo: example
```

#### uint3 -> unknown
:todo: desc
```js
//:todo: example
```

#### uint4 -> unknown
:todo: desc
```js
//:todo: example
```

#### float -> unknown
:todo: desc
```js
//:todo: example
```

#### float2 -> unknown
:todo: desc
```js
//:todo: example
```

#### float3 -> unknown
:todo: desc
```js
//:todo: example
```

#### float4 -> unknown
:todo: desc
```js
//:todo: example
```

#### mat4 -> unknown
:todo: desc
```js
//:todo: example
```

#### image -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### name(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### size_of(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### default_of(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### PassLayerDesc
:todo: desc

---

#### new() -> unknown
:todo: desc
```js
//:todo: example
```

#### display_id -> unknown
:todo: desc
```js
//:todo: example
```

#### display_id=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### dest -> unknown
:todo: desc
```js
//:todo: example
```

#### dest=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### basis -> unknown
:todo: desc
```js
//:todo: example
```

#### basis=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### inputs -> unknown
:todo: desc
```js
//:todo: example
```

#### inputs=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### targets -> unknown
:todo: desc
```js
//:todo: example
```

#### targets=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### vertex=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### vertex -> unknown
:todo: desc
```js
//:todo: example
```

#### fragment=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### fragment -> unknown
:todo: desc
```js
//:todo: example
```

#### clear_color -> unknown
:todo: desc
```js
//:todo: example
```

#### clear_color=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### clear_depth -> unknown
:todo: desc
```js
//:todo: example
```

#### clear_depth=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### blending -> unknown
:todo: desc
```js
//:todo: example
```

#### blending=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### depth_test -> unknown
:todo: desc
```js
//:todo: example
```

#### depth_test=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

### PixelFormat
:todo: desc

---

#### invalid -> unknown
:todo: desc
```js
//:todo: example
```

#### rgb8Unorm -> unknown
:todo: desc
```js
//:todo: example
```

#### rgb8Unorm_srgb -> unknown
:todo: desc
```js
//:todo: example
```

#### rgb8Snorm -> unknown
:todo: desc
```js
//:todo: example
```

#### rgb8Uint -> unknown
:todo: desc
```js
//:todo: example
```

#### rgb8Sint -> unknown
:todo: desc
```js
//:todo: example
```

#### rgb16Unorm -> unknown
:todo: desc
```js
//:todo: example
```

#### rgb16Snorm -> unknown
:todo: desc
```js
//:todo: example
```

#### rgb16Uint -> unknown
:todo: desc
```js
//:todo: example
```

#### rgb16Sint -> unknown
:todo: desc
```js
//:todo: example
```

#### rgb16Float -> unknown
:todo: desc
```js
//:todo: example
```

#### rgb32Uint -> unknown
:todo: desc
```js
//:todo: example
```

#### rgb32Sint -> unknown
:todo: desc
```js
//:todo: example
```

#### rgb32Float -> unknown
:todo: desc
```js
//:todo: example
```

#### rgba8Unorm -> unknown
:todo: desc
```js
//:todo: example
```

#### rgba8Unorm_srgb -> unknown
:todo: desc
```js
//:todo: example
```

#### rgba8Snorm -> unknown
:todo: desc
```js
//:todo: example
```

#### rgba8Uint -> unknown
:todo: desc
```js
//:todo: example
```

#### rgba8Sint -> unknown
:todo: desc
```js
//:todo: example
```

#### rgba16Unorm -> unknown
:todo: desc
```js
//:todo: example
```

#### rgba16Snorm -> unknown
:todo: desc
```js
//:todo: example
```

#### rgba16Uint -> unknown
:todo: desc
```js
//:todo: example
```

#### rgba16Sint -> unknown
:todo: desc
```js
//:todo: example
```

#### rgba16Float -> unknown
:todo: desc
```js
//:todo: example
```

#### rgba32Uint -> unknown
:todo: desc
```js
//:todo: example
```

#### rgba32Sint -> unknown
:todo: desc
```js
//:todo: example
```

#### rgba32Float -> unknown
:todo: desc
```js
//:todo: example
```

#### r11g11b10Float -> unknown
:todo: desc
```js
//:todo: example
```

#### bgra8Unorm -> unknown
:todo: desc
```js
//:todo: example
```

#### bgra8Unorm_srgb -> unknown
:todo: desc
```js
//:todo: example
```

#### depth16Unorm -> unknown
:todo: desc
```js
//:todo: example
```

#### depth32Float -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil8 -> unknown
:todo: desc
```js
//:todo: example
```

#### depth24Unorm_stencil8 -> unknown
:todo: desc
```js
//:todo: example
```

#### depth32Float_stencil8 -> unknown
:todo: desc
```js
//:todo: example
```

#### bc1_rgba -> unknown
:todo: desc
```js
//:todo: example
```

#### bc3_rgba -> unknown
:todo: desc
```js
//:todo: example
```

#### r8Unorm -> unknown
:todo: desc
```js
//:todo: example
```

#### r8Snorm -> unknown
:todo: desc
```js
//:todo: example
```

#### r8Uint -> unknown
:todo: desc
```js
//:todo: example
```

#### r8Sint -> unknown
:todo: desc
```js
//:todo: example
```

#### rg8Unorm -> unknown
:todo: desc
```js
//:todo: example
```

#### rg8Snorm -> unknown
:todo: desc
```js
//:todo: example
```

#### rg8Uint -> unknown
:todo: desc
```js
//:todo: example
```

#### rg8Sint -> unknown
:todo: desc
```js
//:todo: example
```

#### r16Uint -> unknown
:todo: desc
```js
//:todo: example
```

#### r16Sint -> unknown
:todo: desc
```js
//:todo: example
```

#### r16Float -> unknown
:todo: desc
```js
//:todo: example
```

#### rg16Uint -> unknown
:todo: desc
```js
//:todo: example
```

#### rg16Sint -> unknown
:todo: desc
```js
//:todo: example
```

#### rg16Float -> unknown
:todo: desc
```js
//:todo: example
```

#### r32Uint -> unknown
:todo: desc
```js
//:todo: example
```

#### r32Sint -> unknown
:todo: desc
```js
//:todo: example
```

#### r32Float -> unknown
:todo: desc
```js
//:todo: example
```

#### rg32Uint -> unknown
:todo: desc
```js
//:todo: example
```

#### rg32Sint -> unknown
:todo: desc
```js
//:todo: example
```

#### rg32Float -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### name(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Primitive
:todo: desc

---

#### point -> unknown
:todo: desc
```js
//:todo: example
```

#### line -> unknown
:todo: desc
```js
//:todo: example
```

#### line_strip -> unknown
:todo: desc
```js
//:todo: example
```

#### triangle -> unknown
:todo: desc
```js
//:todo: example
```

#### triangle_strip -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Render
:todo: desc

---

#### dispatch(**library**: `Any`, **function**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### submit(**set**: `Any`, **target_path**: `Any`, **target_resource**: `Any`, **target_region**: `Any`, **mat_proj**: `Any`, **mat_view**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### submit_now(**set**: `Any`, **target_path**: `Any`, **target_resource**: `Any`, **target_region**: `Any`, **mat_proj**: `Any`, **mat_view**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### submit_fn(**set**: `Any`, **target_path**: `Any`, **target_resource**: `Any`, **target_region**: `Any`, **mat_proj**: `Any`, **mat_view**: `Any`, **settings**: `Any`, **fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create_set() -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy_set(**set**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### valid_set(**set**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_add(**set**: `Any`, **geo**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_remove(**set**: `Any`, **geo**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_get_geometry(**set**: `Any`, **into**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_get_count(**set**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create_path() -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy_path(**path**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### valid_path(**path**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### window_w() -> unknown
:todo: desc
```js
//:todo: example
```

#### window_h() -> unknown
:todo: desc
```js
//:todo: example
```

#### window_state() -> unknown
:todo: desc
```js
//:todo: example
```

#### window_focus() -> unknown
:todo: desc
```js
//:todo: example
```

#### window_hide(**state**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### drawable_w() -> unknown
:todo: desc
```js
//:todo: example
```

#### drawable_h() -> unknown
:todo: desc
```js
//:todo: example
```

#### drawable_ratio() -> unknown
:todo: desc
```js
//:todo: example
```

#### get_path_vertices(**into_pos**: `Any`, **offset_pos**: `Any`, **stride_pos**: `Any`, **into_color**: `Any`, **offset_color**: `Any`, **stride_color**: `Any`, **points**: `Any`, **color**: `Any`, **thickness**: `Any`, **cap**: `Any`, **join**: `Any`, **closed**: `Any`, **miter_limit**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_path_vertex_count(**points**: `Any`, **thickness**: `Any`, **cap**: `Any`, **join**: `Any`, **closed**: `Any`, **miter_limit**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### push_render_dest(**dest**: `Any`, **into**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### path_add_render_layers(**path**: `Any`, **name**: `Any`, **layers_add**: `Any`, **layer**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### path_add_render_layers(**path**: `Any`, **name**: `Any`, **layers_add**: `Any`, **layers_exclude**: `Any`, **layer**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### path_add_render_layer(**path**: `Any`, **name**: `Any`, **layer**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### path_add_compute_layer(**path**: `Any`, **name**: `Any`, **layer**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### path_add_pass_layer(**path**: `Any`, **name**: `Any`, **dest**: `Any`, **material**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### path_remove(**path**: `Any`, **name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### path_update(**path**: `Any`, **name**: `Any`, **layer**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### define_compute(**name**: `Any`, **library**: `Any`, **function**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### undefine_compute(**name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### undefine_sampler_state(**name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### define_sampler_state(**name**: `Any`, **desc**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### define_vertex_format(**name**: `Any`, **desc**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### undefine_vertex_format(**name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### define_resource(**name**: `Any`, **image**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### resource_get_image(**name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### undefine_resource(**name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create_vertex_buffer(**data**: `Any`, **length**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### vertex_buffer_get_size(**vertex_buffer**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### vertex_buffer_get_data(**vertex_buffer**: `Any`, **into**: `Any`, **length**: `Any`, **offset**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### vertex_buffer_replace(**vertex_buffer**: `Any`, **data**: `Any`, **length**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### vertex_buffer_update(**vertex_buffer**: `Any`, **data**: `Any`, **length**: `Any`, **data_src_offset**: `Any`, **dest_offset**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy_vertex_buffer(**vertex_buffer**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create_index_buffer(**data**: `Any`, **length**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### index_buffer_get_size(**index_buffer**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### index_buffer_get_data(**index_buffer**: `Any`, **into**: `Any`, **length**: `Any`, **offset**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### index_buffer_replace(**index_buffer**: `Any`, **data**: `Any`, **length**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### index_buffer_update(**index_buffer**: `Any`, **data**: `Any`, **length**: `Any`, **data_src_offset**: `Any`, **dest_offset**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy_index_buffer(**index_buffer**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create_text(**material**: `Any`, **default_size**: `Any`, **default_font**: `Any`, **default_color**: `Any`, **render_set**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy_text(**text**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### text_attr_clear(**text**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### text_set_text_buffer(**text**: `Any`, **string**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### text_set_attr(**text**: `Any`, **start**: `Any`, **length**: `Any`, **key**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### text_set_pos(**text**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### text_set_align(**text**: `Any`, **align**: `Any`, **align_vertical**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### text_set_bounds(**text**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### text_commit(**text**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### text_get_geometry(**text**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### text_get_extents(**text**: `Any`, **offset**: `Any`, **count**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### text_get_extents(**text**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### text_set_text(**text**: `Any`, **string**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### kVertexAttributes -> unknown
:todo: desc
```js
//:todo: example
```

#### kColorTargets -> unknown
:todo: desc
```js
//:todo: example
```

#### kMaterialLayerTargets -> unknown
:todo: desc
```js
//:todo: example
```

#### kMaterialInputs -> unknown
:todo: desc
```js
//:todo: example
```

#### kStencilUnset -> unknown
:todo: desc
```js
//:todo: example
```

### RenderDest
:todo: desc

---

#### target_region -> unknown
:todo: desc
```js
//:todo: example
```

#### color -> unknown
:todo: desc
```js
//:todo: example
```

#### depth -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil -> unknown
:todo: desc
```js
//:todo: example
```

#### color=(color : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### depth=(depth : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### stencil=(stencil : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### new() -> unknown
:todo: desc
```js
//:todo: example
```

### RenderDestColor
:todo: desc

---

#### render_target -> unknown
:todo: desc
```js
//:todo: example
```

#### render_target=(render_target : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### clear_color -> unknown
:todo: desc
```js
//:todo: example
```

#### clear_color=(clear_color : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### load_action -> unknown
:todo: desc
```js
//:todo: example
```

#### load_action=(load_action : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### store_action -> unknown
:todo: desc
```js
//:todo: example
```

#### store_action=(store_action : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### level -> unknown
:todo: desc
```js
//:todo: example
```

#### level=(level : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### slice -> unknown
:todo: desc
```js
//:todo: example
```

#### slice=(slice : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### depth -> unknown
:todo: desc
```js
//:todo: example
```

#### depth=(depth : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### new() -> unknown
:todo: desc
```js
//:todo: example
```

### RenderDestDepth
:todo: desc

---

#### render_target -> unknown
:todo: desc
```js
//:todo: example
```

#### render_target=(render_target : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### clear_depth -> unknown
:todo: desc
```js
//:todo: example
```

#### clear_depth=(clear_depth : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### load_action -> unknown
:todo: desc
```js
//:todo: example
```

#### load_action=(load_action : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### store_action -> unknown
:todo: desc
```js
//:todo: example
```

#### store_action=(store_action : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### level -> unknown
:todo: desc
```js
//:todo: example
```

#### level=(level : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### slice -> unknown
:todo: desc
```js
//:todo: example
```

#### slice=(slice : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### depth -> unknown
:todo: desc
```js
//:todo: example
```

#### depth=(depth : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### new() -> unknown
:todo: desc
```js
//:todo: example
```

### RenderDestStencil
:todo: desc

---

#### render_target -> unknown
:todo: desc
```js
//:todo: example
```

#### render_target=(render_target : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### clear_stencil -> unknown
:todo: desc
```js
//:todo: example
```

#### clear_stencil=(clear_stencil : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### load_action -> unknown
:todo: desc
```js
//:todo: example
```

#### load_action=(load_action : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### store_action -> unknown
:todo: desc
```js
//:todo: example
```

#### store_action=(store_action : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### level -> unknown
:todo: desc
```js
//:todo: example
```

#### level=(level : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### slice -> unknown
:todo: desc
```js
//:todo: example
```

#### slice=(slice : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### depth -> unknown
:todo: desc
```js
//:todo: example
```

#### depth=(depth : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### new() -> unknown
:todo: desc
```js
//:todo: example
```

### RenderLayerDesc
:todo: desc

---

#### display_id -> unknown
:todo: desc
```js
//:todo: example
```

#### display_id=(display_id : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### sort -> unknown
:todo: desc
```js
//:todo: example
```

#### sort=(sort : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### material_override -> unknown
:todo: desc
```js
//:todo: example
```

#### material_override=(material_override : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### dest -> unknown
:todo: desc
```js
//:todo: example
```

#### dest=(dest : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### new() -> unknown
:todo: desc
```js
//:todo: example
```

### RenderPathContext
:todo: desc

---

#### new(**path**: `Any`, **settings**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### path -> unknown
:todo: desc
```js
//:todo: example
```

#### layer_render(**name**: `Any`, **render_layer_desc**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### layers_render(**name**: `Any`, **layers_add**: `Any`, **render_layer_desc**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### layers_render(**name**: `Any`, **layers_add**: `Any`, **layers_exclude**: `Any`, **render_layer_desc**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### layer_pass(**pass_layer_desc**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### layer_compute(**name**: `Any`, **compute_layer_desc**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get(**key**: `Any`, **default**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set(**key**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### RenderViewDesc
:todo: desc

---

#### target -> unknown
:todo: desc
```js
//:todo: example
```

#### target=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### target(**v**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### path -> unknown
:todo: desc
```js
//:todo: example
```

#### path=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### path(**v**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### region -> unknown
:todo: desc
```js
//:todo: example
```

#### region=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### region(**v**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### settings -> unknown
:todo: desc
```js
//:todo: example
```

#### settings=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### settings(**v**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### new(**target_resource**: `Any`, **target_path**: `Any`, **target_region**: `Any`, **target_settings**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### new() -> unknown
:todo: desc
```js
//:todo: example
```

### SamplerAddressMode
:todo: desc

---

#### clamp_to_edge -> unknown
:todo: desc
```js
//:todo: example
```

#### repeat -> unknown
:todo: desc
```js
//:todo: example
```

#### mirror_repeat -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### SamplerMinMagFilter
:todo: desc

---

#### nearest -> unknown
:todo: desc
```js
//:todo: example
```

#### linear -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### SamplerMipFilter
:todo: desc

---

#### none -> unknown
:todo: desc
```js
//:todo: example
```

#### nearest -> unknown
:todo: desc
```js
//:todo: example
```

#### linear -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### SamplerState
:todo: desc

---

#### new() -> unknown
:todo: desc
```js
//:todo: example
```

#### address_r -> unknown
:todo: desc
```js
//:todo: example
```

#### address_r=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### address_s -> unknown
:todo: desc
```js
//:todo: example
```

#### address_s=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### address_t -> unknown
:todo: desc
```js
//:todo: example
```

#### address_t=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### filter_min -> unknown
:todo: desc
```js
//:todo: example
```

#### filter_min=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### filter_mag -> unknown
:todo: desc
```js
//:todo: example
```

#### filter_mag=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### filter_mip -> unknown
:todo: desc
```js
//:todo: example
```

#### filter_mip=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

### SortType
:todo: desc

---

#### front_to_back -> unknown
:todo: desc
```js
//:todo: example
```

#### back_to_front -> unknown
:todo: desc
```js
//:todo: example
```

#### sort_by_z -> unknown
:todo: desc
```js
//:todo: example
```

#### sort_by_z_reverse -> unknown
:todo: desc
```js
//:todo: example
```

#### none -> unknown
:todo: desc
```js
//:todo: example
```

### StencilOperation
:todo: desc

---

#### keep -> unknown
:todo: desc
```js
//:todo: example
```

#### zero -> unknown
:todo: desc
```js
//:todo: example
```

#### replace -> unknown
:todo: desc
```js
//:todo: example
```

#### increment_clamp -> unknown
:todo: desc
```js
//:todo: example
```

#### decrement_clamp -> unknown
:todo: desc
```js
//:todo: example
```

#### invert -> unknown
:todo: desc
```js
//:todo: example
```

#### increment_wrap -> unknown
:todo: desc
```js
//:todo: example
```

#### decrement_wrap -> unknown
:todo: desc
```js
//:todo: example
```

#### invalid -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### StoreAction
:todo: desc

---

#### dont_care -> unknown
:todo: desc
```js
//:todo: example
```

#### store -> unknown
:todo: desc
```js
//:todo: example
```

### TextAlign
:todo: desc

---

#### left -> unknown
:todo: desc
```js
//:todo: example
```

#### center -> unknown
:todo: desc
```js
//:todo: example
```

#### right -> unknown
:todo: desc
```js
//:todo: example
```

#### top -> unknown
:todo: desc
```js
//:todo: example
```

#### bottom -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### name(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### VertexAttr
:todo: desc

---

#### new(**name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### name -> unknown
:todo: desc
```js
//:todo: example
```

#### name=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### format -> unknown
:todo: desc
```js
//:todo: example
```

#### format=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### offset -> unknown
:todo: desc
```js
//:todo: example
```

#### offset=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### buffer_index -> unknown
:todo: desc
```js
//:todo: example
```

#### buffer_index=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

### VertexAttrFormat
:todo: desc

---

#### invalid -> unknown
:todo: desc
```js
//:todo: example
```

#### bool -> unknown
:todo: desc
```js
//:todo: example
```

#### bool2 -> unknown
:todo: desc
```js
//:todo: example
```

#### bool3 -> unknown
:todo: desc
```js
//:todo: example
```

#### bool4 -> unknown
:todo: desc
```js
//:todo: example
```

#### int -> unknown
:todo: desc
```js
//:todo: example
```

#### int2 -> unknown
:todo: desc
```js
//:todo: example
```

#### int3 -> unknown
:todo: desc
```js
//:todo: example
```

#### int4 -> unknown
:todo: desc
```js
//:todo: example
```

#### uint -> unknown
:todo: desc
```js
//:todo: example
```

#### uint2 -> unknown
:todo: desc
```js
//:todo: example
```

#### uint3 -> unknown
:todo: desc
```js
//:todo: example
```

#### uint4 -> unknown
:todo: desc
```js
//:todo: example
```

#### float -> unknown
:todo: desc
```js
//:todo: example
```

#### float2 -> unknown
:todo: desc
```js
//:todo: example
```

#### float3 -> unknown
:todo: desc
```js
//:todo: example
```

#### float4 -> unknown
:todo: desc
```js
//:todo: example
```

#### double -> unknown
:todo: desc
```js
//:todo: example
```

#### double2 -> unknown
:todo: desc
```js
//:todo: example
```

#### double3 -> unknown
:todo: desc
```js
//:todo: example
```

#### double4 -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### size_of(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### VertexFormat
:todo: desc

---

#### new() -> unknown
:todo: desc
```js
//:todo: example
```

#### attributes -> unknown
:todo: desc
```js
//:todo: example
```

#### attributes=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### layouts -> unknown
:todo: desc
```js
//:todo: example
```

#### layouts=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

### VertexInputRate
:todo: desc

---

#### vertex -> unknown
:todo: desc
```js
//:todo: example
```

#### instance -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### VertexLayout
:todo: desc

---

#### new() -> unknown
:todo: desc
```js
//:todo: example
```

#### stride -> unknown
:todo: desc
```js
//:todo: example
```

#### stride=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

### Winding
:todo: desc

---

#### clockwise -> unknown
:todo: desc
```js
//:todo: example
```

#### counter_clockwise -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: result

### Result
:todo: desc

---

#### Ok -> unknown
:todo: desc
```js
//:todo: example
```

#### Err -> unknown
:todo: desc
```js
//:todo: example
```

#### ok(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### err(**err**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### kind -> unknown
:todo: desc
```js
//:todo: example
```

#### value -> unknown
:todo: desc
```js
//:todo: example
```

#### new(**kind**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### err(**fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### then(**fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### isOk -> unknown
:todo: desc
```js
//:todo: example
```

#### isErr -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: sat2D

### SAT2D

#### sweep_shape(**shape1**: `Any`, **shape2**: `Any`, **vel**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### raycast_ray(**ray1**: `Any`, **ray2**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### raycast_rays(**ray**: `Any`, **rays**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### raycast_shape(**ray**: `Any`, **shape**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### raycast_shapes(**ray**: `Any`, **shapes**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: semver

### Comparator
:todo: desc

---

#### value -> unknown
:todo: desc
```js
//:todo: example
```

#### semver -> unknown
:todo: desc
```js
//:todo: example
```

#### operator -> unknown
:todo: desc
```js
//:todo: example
```

#### loose -> unknown
:todo: desc
```js
//:todo: example
```

#### any -> unknown
:todo: desc
```js
//:todo: example
```

#### new(**comp**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### new(**comp**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create(**comp**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### inverted() -> unknown
:todo: desc
```js
//:todo: example
```

#### test(**version**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### parse(**comp**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### debug(**a**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### intersects(**comp**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### intersects(**comp**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### SemVer
:todo: desc

---

#### SPEC -> unknown
:todo: desc
```js
//:todo: example
```

#### loose -> unknown
:todo: desc
```js
//:todo: example
```

#### version -> unknown
:todo: desc
```js
//:todo: example
```

#### major -> unknown
:todo: desc
```js
//:todo: example
```

#### minor -> unknown
:todo: desc
```js
//:todo: example
```

#### patch -> unknown
:todo: desc
```js
//:todo: example
```

#### prerelease -> unknown
:todo: desc
```js
//:todo: example
```

#### raw -> unknown
:todo: desc
```js
//:todo: example
```

#### new(**version**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### new(**version**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create(**version**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### format() -> unknown
:todo: desc
```js
//:todo: example
```

#### !=(**other**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### ==(**other**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### <=(**other**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### >=(**other**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### >(**other**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### <(**other**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### inc(**release**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### inc(**release**: `Any`, **identifier**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### compare(**other**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### inc(**version**: `Any`, **release**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### inc(**version**: `Any`, **release**: `Any`, **identifier**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### inc(**version**: `Any`, **release**: `Any`, **loose**: `Any`, **identifier**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### parse(**version**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### parse(**version**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### valid(**version**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### valid(**version**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### clean(**version**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### clean(**version**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### diff(**version1**: `Any`, **version2**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### major(**a**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### major(**a**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### minor(**a**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### minor(**a**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### patch(**a**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### patch(**a**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### prerelease(**a**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### prerelease(**a**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### compare(**a**: `Any`, **b**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### compare(**a**: `Any`, **b**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### rcompare(**a**: `Any`, **b**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### rcompare(**a**: `Any`, **b**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### sort(**list**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### sort(**list**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### rsort(**list**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### rsort(**list**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### gt(**a**: `Any`, **b**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### gt(**a**: `Any`, **b**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### lt(**a**: `Any`, **b**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### lt(**a**: `Any`, **b**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### gte(**a**: `Any`, **b**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### gte(**a**: `Any`, **b**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### lte(**a**: `Any`, **b**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### lte(**a**: `Any`, **b**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### eq(**a**: `Any`, **b**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### eq(**a**: `Any`, **b**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### neq(**a**: `Any`, **b**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### neq(**a**: `Any`, **b**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### cmp(**a**: `Any`, **op**: `Any`, **b**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### cmp(**a**: `Any`, **op**: `Any`, **b**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### max_satisfying(**versions**: `Any`, **range**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### max_satisfying(**versions**: `Any`, **range**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### min_satisfying(**versions**: `Any`, **range**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### min_satisfying(**versions**: `Any`, **range**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### satisfies(**version**: `Any`, **range**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### satisfies(**version**: `Any`, **range**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### valid_range(**range**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### valid_range(**range**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### ltr(**version**: `Any`, **range**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### ltr(**version**: `Any`, **range**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### gtr(**version**: `Any`, **range**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### gtr(**version**: `Any`, **range**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### outside(**version**: `Any`, **range**: `Any`, **hilo**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### outside(**version**: `Any`, **range**: `Any`, **hilo**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### debug(**a**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### compare_main(**other**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### first_not_zero(**a**: `Any`, **b**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### first_not_zero(**a**: `Any`, **b**: `Any`, **c**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### compare_pre(**other**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### compare_identifiers(**a**: `Any`, **b**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### SemVerRange
:todo: desc

---

#### any -> unknown
:todo: desc
```js
//:todo: example
```

#### empty -> unknown
:todo: desc
```js
//:todo: example
```

#### debug(**a**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set -> unknown
:todo: desc
```js
//:todo: example
```

#### loose -> unknown
:todo: desc
```js
//:todo: example
```

#### range -> unknown
:todo: desc
```js
//:todo: example
```

#### raw -> unknown
:todo: desc
```js
//:todo: example
```

#### isEmpty -> unknown
:todo: desc
```js
//:todo: example
```

#### isAny -> unknown
:todo: desc
```js
//:todo: example
```

#### new(**range**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### new(**range**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create(**range**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### format() -> unknown
:todo: desc
```js
//:todo: example
```

#### union(**other**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### intersects(**range**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### intersects(**range**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### pick_not_infinite(**a**: `Any`, **b**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### pick_infinite(**a**: `Any`, **b**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### comparator_intersection(**a**: `Any`, **b**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### intersection(**other**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### inverted() -> unknown
:todo: desc
```js
//:todo: example
```

#### subset_contains(**other**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### subset_contains(**other**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### subset_of(**other**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### subset_of(**other**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### subset(**needle**: `Any`, **haystack**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### subset(**needle**: `Any`, **haystack**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### test(**version**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### is_x(**id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### test_set(**set**: `Any`, **version**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### parse_range(**range**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### parse_comparator(**comp**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### replace_carets(**comp**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### replace_caret(**comp**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### replace_tildes(**comp**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### replace_tilde(**comp**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### replace_x_ranges(**comp**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### replace_x_range(**comp**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### replace_stars(**comp**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### SemVerSubset
:todo: desc

---

#### subset(**needle**: `Any`, **haystack**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### subset(**needle**: `Any`, **haystack**: `Any`, **loose**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### gen_interval(**comparators**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### orderEq(**v1**: `Any`, **v2**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### orderGt(**v1**: `Any`, **v2**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### orderLt(**v1**: `Any`, **v2**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### isSubset(**needle**: `Any`, **haystack**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### SemVerSubsetInterval
:todo: desc

---

#### left -> unknown
:todo: desc
```js
//:todo: example
```

#### right -> unknown
:todo: desc
```js
//:todo: example
```

#### leftValue -> unknown
:todo: desc
```js
//:todo: example
```

#### rightValue -> unknown
:todo: desc
```js
//:todo: example
```

#### new(**left**: `Any`, **leftValue**: `Any`, **rightValue**: `Any`, **right**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: settings

### Settings
:todo: desc

---

#### apply(**settings_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### unapply(**settings_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### forget(**key**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### has(**key**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get(**key**: `Any`, **default**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_string(**key**: `Any`, **value**: `Any`, **length**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_number(**key**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_bool(**key**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_float2(**key**: `Any`, **x**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_float3(**key**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_float4(**key**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set(**key**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### SettingsType
:todo: desc

---

#### unknown -> unknown
:todo: desc
```js
//:todo: example
```

#### boolean -> unknown
:todo: desc
```js
//:todo: example
```

#### number -> unknown
:todo: desc
```js
//:todo: example
```

#### string -> unknown
:todo: desc
```js
//:todo: example
```

#### float2 -> unknown
:todo: desc
```js
//:todo: example
```

#### float3 -> unknown
:todo: desc
```js
//:todo: example
```

#### float4 -> unknown
:todo: desc
```js
//:todo: example
```

#### name(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: shape2D

### Ray2D
:todo: desc

---

#### create(**start**: `Any`, **end**: `Any`, **type**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set(**ray**: `Any`, **start**: `Any`, **end**: `Any`, **type**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_start(**ray**: `Any`, **start**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_end(**ray**: `Any`, **end**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_type(**ray**: `Any`, **type**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_start(**ray**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_end(**ray**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_type(**ray**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Ray2DType
:todo: desc

---

#### finite -> unknown
:todo: desc
```js
//:todo: example
```

#### infinite_end -> unknown
:todo: desc
```js
//:todo: example
```

#### infinite -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### name(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Shape2D
:todo: desc

---

#### create_poly(**pos**: `Any`, **angle**: `Any`, **scale**: `Any`, **verts**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create_ngon(**pos**: `Any`, **angle**: `Any`, **scale**: `Any`, **sides**: `Any`, **radius**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create_rect(**pos**: `Any`, **angle**: `Any`, **scale**: `Any`, **size**: `Any`, **centered**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create_circle(**pos**: `Any`, **angle**: `Any`, **scale**: `Any`, **radius**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy(**shape**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_pos(**shape**: `Any`, **pos**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_rotation(**shape**: `Any`, **angle**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_scale(**shape**: `Any`, **scale**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_type(**shape**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_pos(**shape**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_bounds(**shape**: `Any`, **into**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_rotation(**shape**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_scale(**shape**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_verts(**shape**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_radius(**shape**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Shape2DType
:todo: desc

---

#### poly -> unknown
:todo: desc
```js
//:todo: example
```

#### circle -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### name(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: string

### Str
:todo: desc

---

#### split_lines(**string**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### split(**string**: `Any`, **delim**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### indent_strip(**string**: `String`) -> unknown
:todo: desc
```js
//:todo: example
```

#### indent(**string**: `String`) -> unknown
:todo: desc
```js
//:todo: example
```

#### trim(**string**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### compare(**a**: `Any`, **b**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### replace(**string**: `Any`, **sub**: `Any`, **repl**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### vec(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### vec(**value**: `Any`, **precision**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### vec(**value**: `Any`, **precision**: `Any`, **sep**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### fixed(**number**: `Any`, **precision**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### fixed(**number**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### fixed(**number**: `Any`, **precision**: `Any`, **padded**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### hex(**number**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### binary(**number**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### binary(**number**: `Any`, **bit_width**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### path_is_absolute(**path**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### path_directory(**path**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### path_filename(**path**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### path_extension(**path**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### path_extensionless(**path**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### bytes_formatted(**byte_count**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### bytes_formatted(**byte_count**: `Any`, **precision**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### upper(**string**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### lower(**string**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### wrap(**string**: `Any`, **column**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### path(**path**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: terminal

### Terminal
:todo: desc

---

#### new() -> unknown
:todo: desc
```js
//:todo: example
```

#### red -> unknown
:todo: desc
```js
//:todo: example
```

#### cyan -> unknown
:todo: desc
```js
//:todo: example
```

#### reset -> unknown
:todo: desc
```js
//:todo: example
```

#### pink -> unknown
:todo: desc
```js
//:todo: example
```

#### purple -> unknown
:todo: desc
```js
//:todo: example
```

#### lime -> unknown
:todo: desc
```js
//:todo: example
```

#### dim -> unknown
:todo: desc
```js
//:todo: example
```

#### green -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: test

### BaseMatchers
:todo: desc

---

#### new(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### value -> unknown
:todo: desc
```js
//:todo: example
```

#### not -> unknown
:todo: desc
```js
//:todo: example
```

#### toBe(**klass**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### toBeFalse -> unknown
:todo: desc
```js
//:todo: example
```

#### toBeTrue -> unknown
:todo: desc
```js
//:todo: example
```

#### toBeNull -> unknown
:todo: desc
```js
//:todo: example
```

#### toEqual(**other**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### toEqualDeeply(**other**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### ConsoleReporter
:todo: desc

---

#### new() -> unknown
:todo: desc
```js
//:todo: example
```

#### print_colors=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### epilogue() -> unknown
:todo: desc
```js
//:todo: example
```

#### runnableSkipped(**skippable**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### suiteStart(**title**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### suiteEnd(**title**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### testStart(**runnable**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### testEnd(**runnable**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### testPassed(**runnable**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### testFailed(**runnable**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### testError(**runnable**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Expectation
:todo: desc

---

#### new(**passed**: `Any`, **message**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### passed -> unknown
:todo: desc
```js
//:todo: example
```

#### message -> unknown
:todo: desc
```js
//:todo: example
```

### FiberMatchers
:todo: desc

---

#### new(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### toBeARuntimeError -> unknown
:todo: desc
```js
//:todo: example
```

#### toBeARuntimeError(**errorMessage**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### toBeDone -> unknown
:todo: desc
```js
//:todo: example
```

### Matchers
:todo: desc

---

#### new(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### NumMatchers
:todo: desc

---

#### new(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### toBeGreaterThan(**other**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### toBeLessThan(**other**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### toBeBetween(**min**: `Any`, **max**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### RangeMatchers
:todo: desc

---

#### new(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### toContain(**other**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### toBeContainedBy(**other**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Reporter
:todo: desc

---

#### epilogue() -> unknown
:todo: desc
```js
//:todo: example
```

#### runnableSkipped(**skippable**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### suiteStart(**title**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### suiteEnd(**title**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### testStart(**runnable**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### testPassed(**runnable**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### testFailed(**runnable**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### testError(**runnable**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### testEnd(**runnable**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Runnable
:todo: desc

---

#### new(**title**: `Any`, **beforeEaches**: `Any`, **afterEaches**: `Any`, **fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### duration -> unknown
:todo: desc
```js
//:todo: example
```

#### error -> unknown
:todo: desc
```js
//:todo: example
```

#### expectations -> unknown
:todo: desc
```js
//:todo: example
```

#### hasRun -> unknown
:todo: desc
```js
//:todo: example
```

#### run() -> unknown
:todo: desc
```js
//:todo: example
```

#### title -> unknown
:todo: desc
```js
//:todo: example
```

### Skippable
:todo: desc

---

#### new(**title**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### run -> unknown
:todo: desc
```js
//:todo: example
```

#### title -> unknown
:todo: desc
```js
//:todo: example
```

### Stub
:todo: desc

---

#### new(**name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### new(**name**: `Any`, **fakeFn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### andCallFake(**name**: `Any`, **fakeFn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### andReturnValue(**name**: `Any`, **returnValue**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### called -> unknown
:todo: desc
```js
//:todo: example
```

#### calls -> unknown
:todo: desc
```js
//:todo: example
```

#### firstCall -> unknown
:todo: desc
```js
//:todo: example
```

#### mostRecentCall -> unknown
:todo: desc
```js
//:todo: example
```

#### name -> unknown
:todo: desc
```js
//:todo: example
```

#### reset -> unknown
:todo: desc
```js
//:todo: example
```

#### call -> unknown
:todo: desc
```js
//:todo: example
```

#### call() -> unknown
:todo: desc
```js
//:todo: example
```

#### call(**a**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### call(**a**: `Any`, **b**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### call(**a**: `Any`, **b**: `Any`, **c**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`, **i**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`, **i**: `Any`, **j**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`, **i**: `Any`, **j**: `Any`, **k**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`, **i**: `Any`, **j**: `Any`, **k**: `Any`, **l**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`, **i**: `Any`, **j**: `Any`, **k**: `Any`, **l**: `Any`, **m**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`, **i**: `Any`, **j**: `Any`, **k**: `Any`, **l**: `Any`, **m**: `Any`, **n**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`, **i**: `Any`, **j**: `Any`, **k**: `Any`, **l**: `Any`, **m**: `Any`, **n**: `Any`, **o**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### call(**a**: `Any`, **b**: `Any`, **c**: `Any`, **d**: `Any`, **e**: `Any`, **f**: `Any`, **g**: `Any`, **h**: `Any`, **i**: `Any`, **j**: `Any`, **k**: `Any`, **l**: `Any`, **m**: `Any`, **n**: `Any`, **o**: `Any`, **p**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### StubMatchers
:todo: desc

---

#### new(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### toHaveBeenCalled -> unknown
:todo: desc
```js
//:todo: example
```

#### toHaveBeenCalled(**times**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### toHaveBeenCalledWith(**args**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Suite
:todo: desc

---

#### new(**name**: `Any`, **block**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### new(**name**: `Any`, **beforeEaches**: `Any`, **afterEaches**: `Any`, **block**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### afterEach -> unknown
:todo: desc
```js
//:todo: example
```

#### afterEach(**block**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### beforeEach -> unknown
:todo: desc
```js
//:todo: example
```

#### beforeEach(**block**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### run(**reporter**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### should(**name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### should(**name**: `Any`, **block**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### skip(**block**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### suite(**name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### suite(**name**: `Any`, **block**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### title -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: ui

## luxe: ui/button

### UIButton
:todo: desc

---

#### create(**ui_entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_text(**control**: `Any`, **text**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_text(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_font(**control**: `Any`, **font**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_font(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_color(**control**: `Any`, **color**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_color(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_text_size(**control**: `Any`, **size**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_text_size(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_align(**control**: `Any`, **align**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_align(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_align_vertical(**control**: `Any`, **align**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_align_vertical(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: ui/check

### UICheck
:todo: desc

---

#### create(**ui_entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_state(**control**: `Any`, **state**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_state(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: ui/control

### Control
:todo: desc

---

#### create(**ui_entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy_children(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### valid(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get(**id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### exists(**id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### clear(**control**: `Any`, **uiclear_action**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_type(**control**: `Any`, **type**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_type(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_id(**control**: `Any`, **id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_id(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_bounds_abs(**control**: `Any`, **into**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_bounds(**control**: `Any`, **into**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_bounds_abs(**control**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_bounds(**control**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_pos_abs(**control**: `Any`, **x**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_pos(**control**: `Any`, **x**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_size(**control**: `Any`, **w**: `Any`, **h**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_pos_x(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_pos_x_abs(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_pos_y(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_pos_y_abs(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_width(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_height(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### contains(**control**: `Any`, **x**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_entity(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_parent(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_allow_input(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_allow_input(**control**: `Any`, **allow**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_allow_keys(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_allow_keys(**control**: `Any`, **allow**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_visible(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_visible(**control**: `Any`, **visible**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_disabled(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_disabled(**control**: `Any`, **disabled**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_clip(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_clip(**control**: `Any`, **clip**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_nodes(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_depth(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_depth_offset(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_depth_offset(**control**: `Any`, **depth_offset**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_input_inside(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_input_pressed(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### child_at_point(**control**: `Any`, **x**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### child_count(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### child_index(**control**: `Any`, **child**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### child_get(**control**: `Any`, **index**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### child_add(**control**: `Any`, **child**: `Any`, **internal**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### child_add(**control**: `Any`, **child**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### child_remove(**control**: `Any`, **child**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### children_bounds(**control**: `Any`, **into**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_render(**control**: `Any`, **fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_events(**control**: `Any`, **fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### unset_events(**control**: `Any`, **id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_process(**control**: `Any`, **fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_state_data(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_state_data(**control**: `Any`, **data**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: ui/image

### UIImage
:todo: desc

---

#### create(**ui_entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_image(**control**: `Any`, **image**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_image(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_material(**control**: `Any`, **material**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_uv(**control**: `Any`, **left**: `Any`, **top**: `Any`, **right**: `Any`, **bottom**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_color(**control**: `Any`, **color**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_angle(**control**: `Any`, **degrees**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: ui/label

### UILabel
:todo: desc

---

#### create(**ui_entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_text(**label**: `Any`, **text**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_text(**label**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_render_text(**label**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_text_extents(**label**: `Any`, **offset**: `Any`, **count**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_text_extents(**label**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_font(**label**: `Any`, **font**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_font(**label**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_color(**label**: `Any`, **color**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_color(**label**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_color_hover(**label**: `Any`, **color**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_color_hover(**label**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_text_size(**label**: `Any`, **size**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_text_size(**label**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_align(**label**: `Any`, **align**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_align(**label**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_align_vertical(**label**: `Any`, **align**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_align_vertical(**label**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: ui/list

### UIList
:todo: desc

---

#### create(**ui_entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### add(**list**: `Any`, **control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### remove(**list**: `Any`, **control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### clear(**list**: `Any`, **uiclear_action**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### refresh(**list**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_percent(**list**: `Any`, **vertical**: `Any`, **horizontal**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_percent_v(**list**: `Any`, **vertical**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_percent_h(**list**: `Any`, **horizontal**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_percent_v(**list**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_percent_h(**list**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_scroll(**list**: `Any`, **vertical**: `Any`, **horizontal**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_scroll_v(**list**: `Any`, **vertical**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_scroll_h(**list**: `Any`, **horizontal**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_scroll_v(**list**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_scroll_h(**list**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### can_scroll_v(**list**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### can_scroll_h(**list**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### count(**list**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get(**list**: `Any`, **index**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### index(**list**: `Any`, **control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: ui/panel

### UIPanel
:todo: desc

---

#### create(**ui_entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_color(**control**: `Any`, **color**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_border(**control**: `Any`, **size**: `Any`, **color**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: ui/progress

### UIProgress
:todo: desc

---

#### create(**ui_entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_progress(**control**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_progress(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: ui/scroll

### UIScroll
:todo: desc

---

#### create(**ui_entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### add(**scroll**: `Any`, **control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### remove(**scroll**: `Any`, **control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### count(**scroll**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### clear(**scroll**: `Any`, **uiclear_action**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get(**scroll**: `Any`, **index**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### index(**scroll**: `Any`, **control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### refresh(**scroll**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_percent(**scroll**: `Any`, **vertical**: `Any`, **horizontal**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_scroll(**scroll**: `Any`, **vertical**: `Any`, **horizontal**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_percent_v(**scroll**: `Any`, **vertical**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_percent_h(**scroll**: `Any`, **horizontal**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_scroll_v(**scroll**: `Any`, **vertical**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_scroll_h(**scroll**: `Any`, **horizontal**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_percent_v(**scroll**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_percent_h(**scroll**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_scroll_v(**scroll**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_scroll_h(**scroll**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### can_scroll_v(**scroll**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### can_scroll_h(**scroll**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: ui/slider

### UISlider
:todo: desc

---

#### create(**ui_entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_value(**control**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_value(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_step(**control**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_step(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_min(**control**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_min(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_max(**control**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_max(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_inverted(**control**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_inverted(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: ui/text

### UIText
:todo: desc

---

#### create(**ui_entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_text(**control**: `Any`, **text**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_text(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_font(**control**: `Any`, **font**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_font(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_color(**control**: `Any`, **color**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_color(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_text_size(**control**: `Any`, **size**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_text_size(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_align(**control**: `Any`, **align**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_align(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_align_vertical(**control**: `Any`, **align**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_align_vertical(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### select_all(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: ui/window

### UIWindow
:todo: desc

---

#### create(**ui_entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### close(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_collapsed(**control**: `Any`, **state**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_collapsed(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_text(**control**: `Any`, **text**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_text_size(**control**: `Any`, **size**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_title_size(**control**: `Any`, **size**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_resizable(**control**: `Any`, **state**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_bring_to_front(**control**: `Any`, **state**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_closable(**control**: `Any`, **state**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_collapsible(**control**: `Any`, **state**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_draggable(**control**: `Any`, **state**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_resizable(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_bring_to_front(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_closable(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_collapsible(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_draggable(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### UIWindowChange
:todo: desc

---

#### close -> unknown
:todo: desc
```js
//:todo: example
```

#### open -> unknown
:todo: desc
```js
//:todo: example
```

#### collapse -> unknown
:todo: desc
```js
//:todo: example
```

#### uncollapse -> unknown
:todo: desc
```js
//:todo: example
```

#### move -> unknown
:todo: desc
```js
//:todo: example
```

#### name(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

## luxe: version

## luxe: world

### AnimEvent
:todo: desc

---

#### start -> unknown
:todo: desc
```js
//:todo: example
```

#### tick -> unknown
:todo: desc
```js
//:todo: example
```

#### complete -> unknown
:todo: desc
```js
//:todo: example
```

### AnimInterval
:todo: desc

---

#### create(**world**: `Any`, **duration**: `Any`, **rate**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create(**world**: `Any`, **duration**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### time(**world**: `Any`, **anim**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_time(**world**: `Any`, **anim**: `Any`, **time**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_now(**world**: `Any`, **anim**: `Any`, **offset**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_now(**world**: `Any`, **anim**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_play_count(**world**: `Any`, **anim**: `Any`, **count**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_clock(**world**: `Any`, **anim**: `Any`, **clock**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_rate(**world**: `Any`, **anim**: `Any`, **rate**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_duration(**world**: `Any`, **anim**: `Any`, **duration**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_start(**world**: `Any`, **anim**: `Any`, **start**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_end(**world**: `Any`, **anim**: `Any`, **end**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_now(**world**: `Any`, **anim**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_play_count(**world**: `Any`, **anim**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_clock(**world**: `Any`, **anim**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_rate(**world**: `Any`, **anim**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_duration(**world**: `Any`, **anim**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_start(**world**: `Any`, **anim**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_end(**world**: `Any`, **anim**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Body2D
:todo: desc

---

#### create(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### has(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create_collider_box(**entity**: `Any`, **center**: `Any`, **size**: `Any`, **angle**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create_collider_circle(**entity**: `Any`, **center**: `Any`, **radius**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_center(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_mass(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_inertia(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_type(**entity**: `Any`, **type**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_type(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_sleeping_allowed(**entity**: `Any`, **allowed**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_sleeping_allowed(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_sleeping(**entity**: `Any`, **sleep_state**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_sleeping(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_active(**entity**: `Any`, **active_state**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_active(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_velocity_linear(**entity**: `Any`, **x**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_velocity_linear(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_velocity_angular(**entity**: `Any`, **angle**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_velocity_angular(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_damping_linear(**entity**: `Any`, **linear_damping**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_damping_linear(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_damping_angular(**entity**: `Any`, **angular_damping**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_damping_angular(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### apply_force(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **x**: `Any`, **y**: `Any`, **force_awake**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### apply_force(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **x**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### apply_force(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_awake**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### apply_force(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### apply_torque(**entity**: `Any`, **torque**: `Any`, **force_awake**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### apply_torque(**entity**: `Any`, **torque**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### apply_impulse_linear(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **x**: `Any`, **y**: `Any`, **force_awake**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### apply_impulse_linear(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **x**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### apply_impulse_angular(**entity**: `Any`, **impulse**: `Any`, **force_awake**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### apply_impulse_angular(**entity**: `Any`, **impulse**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Body3D
:todo: desc

---

#### create(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### has(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create_heightfield(**entity**: `Any`, **image**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create_collider_box(**entity**: `Any`, **center**: `Any`, **size**: `Any`, **euler**: `Any`, **physics_asset**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create_collider_box(**entity**: `Any`, **center**: `Any`, **size**: `Any`, **euler**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create_collider_sphere(**entity**: `Any`, **center**: `Any`, **radius**: `Any`, **physics_asset**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create_collider_sphere(**entity**: `Any`, **center**: `Any`, **radius**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create_collider_cylinder(**entity**: `Any`, **center**: `Any`, **size**: `Any`, **physics_asset**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create_collider_cylinder(**entity**: `Any`, **center**: `Any`, **size**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create_collider_capsule(**entity**: `Any`, **center**: `Any`, **radius**: `Any`, **height**: `Any`, **physics_asset**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create_collider_capsule(**entity**: `Any`, **center**: `Any`, **radius**: `Any`, **height**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create_collider_mesh(**entity**: `Any`, **center**: `Any`, **euler**: `Any`, **collider_type**: `MeshColliderType`, **mesh_asset**: `Any`, **mesh_level**: `Any`, **physics_asset**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create_collider_mesh(**entity**: `Any`, **center**: `Any`, **euler**: `Any`, **collider_type**: `MeshColliderType`, **mesh_asset**: `Any`, **mesh_level**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_center(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_mass(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_inertia(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_physics_asset(**entity**: `Any`, **physics_asset**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### on(**entity**: `Any`, **type**: `BodyEvent`, **fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### off(**entity**: `Any`, **handle**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_channel(**entity**: `Any`, **channel**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_type(**entity**: `Any`, **type**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_type(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_sleeping_allowed(**entity**: `Any`, **allowed**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_sleeping_allowed(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_sleeping(**entity**: `Any`, **sleep_state**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_sleeping(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_active(**entity**: `Any`, **active_state**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_active(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_rotation_allowed(**entity**: `Any`, **axis**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_rotation_allowed(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_velocity_linear(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_velocity_linear(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_velocity_angular(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_velocity_angular(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_damping_linear(**entity**: `Any`, **linear_damping**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_damping_linear(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_damping_angular(**entity**: `Any`, **angular_damping**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_damping_angular(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### apply_force(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_z**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **force_awake**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### apply_force(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_z**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### apply_force(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_z**: `Any`, **force_awake**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### apply_force(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### apply_torque(**entity**: `Any`, **torque_x**: `Any`, **torque_y**: `Any`, **torque_z**: `Any`, **force_awake**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### apply_torque(**entity**: `Any`, **torque_x**: `Any`, **torque_y**: `Any`, **torque_z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### apply_impulse_linear(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **impulse_z**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **force_awake**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### apply_impulse_linear(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **impulse_z**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### apply_impulse_angular(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **impulse_z**: `Any`, **force_awake**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### apply_impulse_angular(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **impulse_z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### BodyEvent
:todo: desc

---

#### invalid -> unknown
:todo: desc
```js
//:todo: example
```

#### overlap -> unknown
:todo: desc
```js
//:todo: example
```

#### collide -> unknown
:todo: desc
```js
//:todo: example
```

#### name(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### BodyType
:todo: desc

---

#### static_body -> unknown
:todo: desc
```js
//:todo: example
```

#### dynamic_body -> unknown
:todo: desc
```js
//:todo: example
```

#### kinematic_body -> unknown
:todo: desc
```js
//:todo: example
```

#### name(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Camera
:todo: desc

---

#### create(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### has(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_default(**world**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_default(**world**: `Any`, **camera**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_fov_vertical(**entity**: `Any`, **fov_vertical**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_fov_vertical(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_projection(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_near(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_far(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_aspect(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### perspective(**entity**: `Any`, **fov_vertical**: `Any`, **aspect**: `Any`, **near**: `Any`, **far**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### ortho(**entity**: `Any`, **left**: `Any`, **top**: `Any`, **right**: `Any`, **bottom**: `Any`, **near**: `Any`, **far**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### look_at(**entity**: `Any`, **from**: `Any`, **to**: `Any`, **up**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set2D(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **width**: `Any`, **height**: `Any`, **near**: `Any`, **far**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set3D(**entity**: `Any`, **fov_vertical**: `Any`, **aspect**: `Any`, **near**: `Any`, **far**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### screen_point_to_world(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### world_point_to_screen(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### world_point_to_view(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`, **into**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### world_point_to_view(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### view_point_to_world(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### world_point_to_clip(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### clip_point_to_world(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_view_matrix(**entity**: `Any`, **into_matrix**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_projection_matrix(**entity**: `Any`, **into_matrix**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_view_projection_matrix(**entity**: `Any`, **into_matrix**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_view_matrix(**entity**: `Any`, **matrix**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_projection_matrix(**entity**: `Any`, **matrix**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### cull(**camera**: `Any`, **render_set**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### froxelize(**camera**: `Any`, **slices**: `Any`, **entity_info_list**: `Any`, **cluster_image**: `Any`, **items_image**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Clock
:todo: desc

---

#### create(**world**: `Any`, **rate**: `Any`, **paused**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create(**world**: `Any`, **rate**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### time(**world**: `Any`, **clock**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Entity
:todo: desc

---

#### create(**world**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create(**world**: `Any`, **name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### valid(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_world(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get(**uuid**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_named(**world**: `Any`, **name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_named_all(**world**: `Any`, **name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_name(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_name(**entity**: `Any`, **name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_uuid(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_uuid(**entity**: `Any`, **uuid_string**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Layer
:todo: desc

---

#### create(**world**: `Any`, **scene**: `Any`, **layer_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy(**world**: `Any`, **scene**: `Any`, **layer_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### exists(**world**: `Any`, **scene**: `Any`, **layer_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_list(**world**: `Any`, **scene**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_id(**world**: `Any`, **scene**: `Any`, **layer_id**: `Any`, **new_layer_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### entity_list(**world**: `Any`, **scene**: `Any`, **layer_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### entity_set(**world**: `Any`, **scene**: `Any`, **layer_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### entity_add(**world**: `Any`, **scene**: `Any`, **layer_id**: `Any`, **entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### entity_remove(**world**: `Any`, **scene**: `Any`, **layer_id**: `Any`, **entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Mesh
:todo: desc

---

#### create(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create(**entity**: `Any`, **material**: `Any`, **mesh_lx**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### has(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### clear(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### level_get_element_count(**entity**: `Any`, **level**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### level_get_count(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### level_set_active(**entity**: `Any`, **level**: `Any`, **disable_current**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### level_get_active(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### level_set_enabled(**entity**: `Any`, **level**: `Any`, **state**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### level_get_enabled(**entity**: `Any`, **level**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_asset(**entity**: `Any`, **asset_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_source_id(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_default_material(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_default_material(**entity**: `Any`, **material**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_geometry(**entity**: `Any`, **level**: `Any`, **element**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_geometry(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### obb_intersect_ray(**entity**: `Any`, **ray_x**: `Any`, **ray_y**: `Any`, **ray_z**: `Any`, **ray_dir_x**: `Any`, **ray_dir_y**: `Any`, **ray_dir_z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### MeshColliderType
:todo: desc

---

#### static_only -> unknown
:todo: desc
```js
//:todo: example
```

#### dynamic_convex -> unknown
:todo: desc
```js
//:todo: example
```

#### dynamic_concave -> unknown
:todo: desc
```js
//:todo: example
```

#### name(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### ModifierSystem
:todo: desc

---

#### priority -> unknown
:todo: desc
```js
//:todo: example
```

#### persist -> unknown
:todo: desc
```js
//:todo: example
```

#### count -> unknown
:todo: desc
```js
//:todo: example
```

#### field -> unknown
:todo: desc
```js
//:todo: example
```

#### items -> unknown
:todo: desc
```js
//:todo: example
```

#### world -> unknown
:todo: desc
```js
//:todo: example
```

#### each(**fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### each(**unique**: `Any`, **fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### find_entity(**relative_entity**: `Any`, **uuid**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get(**entity**: `Any`, **inst**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_slot_at(**index**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_slot(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_entity(**slot**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_id(**slot**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_id_hash(**slot**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_entity(**slot**: `Any`, **entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### editor(**editor**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### init(**world**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### tick(**delta**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy() -> unknown
:todo: desc
```js
//:todo: example
```

#### detached() -> unknown
:todo: desc
```js
//:todo: example
```

#### attached() -> unknown
:todo: desc
```js
//:todo: example
```

#### disable(**entity**: `Any`, **instance**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### attach(**entity**: `Any`, **instance**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### detach(**entity**: `Any`, **instance**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### data -> unknown
:todo: desc
```js
//:todo: example
```

#### id -> unknown
:todo: desc
```js
//:todo: example
```

#### id=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### on_init(**world**: `Any`, **data**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### on_attached() -> unknown
:todo: desc
```js
//:todo: example
```

#### on_detached() -> unknown
:todo: desc
```js
//:todo: example
```

#### on_disabled(**entities**: `Any`, **state**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### on_destroying(**entities**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### on_destroyed(**entities**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### on_destroy() -> unknown
:todo: desc
```js
//:todo: example
```

#### on_attach_block(**block**: `Any`, **block_start**: `Any`, **block_end**: `Any`, **into**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Modifiers
:todo: desc

---

#### get_or_create_block(**world**: `Any`, **module**: `Any`, **block_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### attach_uuid(**module**: `Any`, **entity**: `Any`, **uuid**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### detach_uuid(**module**: `Any`, **entity**: `Any`, **uuid**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### has(**module**: `Any`, **entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_uuid(**module**: `Any`, **entity**: `Any`, **uuid**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_uuid(**module**: `Any`, **entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_attached(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_attached_types(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_entities(**module**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_instances(**module**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_module(**uuid**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_entity(**uuid**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### has_system_in_world(**module**: `Any`, **world**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_system_in_world(**module**: `Any`, **world**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get(**module**: `Any`, **entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_system(**module**: `Any`, **entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create(**module**: `Any`, **entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy(**module**: `Any`, **entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### init(**world**: `Any`, **modifier**: `Any`, **block**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_asset_compiler(**type**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_compiler_for_input(**modifier_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_data_block_type(**modifier_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_input_block_type(**modifier_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Overlap
:todo: desc

---

#### none -> unknown
:todo: desc
```js
//:todo: example
```

#### begin -> unknown
:todo: desc
```js
//:todo: example
```

#### end -> unknown
:todo: desc
```js
//:todo: example
```

#### active -> unknown
:todo: desc
```js
//:todo: example
```

#### name(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### from_string(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Physics2D
:todo: desc

---

#### set_gravity(**world**: `Any`, **x**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Physics3D
:todo: desc

---

#### set_debug_draw(**world**: `Any`, **state**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_gravity(**world**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### cast_ray(**world**: `Any`, **from**: `Any`, **to**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### cast_shape(**entity**: `Any`, **from**: `Any`, **to**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### query_sphere(**world**: `Any`, **center**: `Any`, **radius**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### query_box(**world**: `Any`, **center**: `Any`, **size**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Prototype
:todo: desc

---

#### destroy(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### has(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_type(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_root(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_tree(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### has_tree(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_ref(**entity**: `Any`, **uuid**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_ref_of(**entity**: `Any`, **target_entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_named(**entity**: `Any`, **name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_named_all(**entity**: `Any`, **name**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### entity_list(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### refs_list(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create(**world**: `Any`, **prototype_id**: `Any`, **instance_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create(**world**: `Any`, **prototype_id**: `Any`, **instance_id**: `Any`, **position**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create(**world**: `Any`, **prototype_id**: `Any`, **instance_id**: `Any`, **position**: `Any`, **rotation**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create(**world**: `Any`, **prototype_id**: `Any`, **instance_id**: `Any`, **position**: `Any`, **rotation**: `Any`, **scale**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Scene
:todo: desc

---

#### create(**world**: `Any`, **id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy(**world**: `Any`, **id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_list(**world**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### exists(**world**: `Any`, **id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### entity_list(**world**: `Any`, **id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### entity_forget(**world**: `Any`, **id**: `Any`, **entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_id(**world**: `Any`, **id**: `Any`, **new_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### load(**world**: `Any`, **id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### load_as_clone(**world**: `Any`, **id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### unload(**world**: `Any`, **id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Tags
:todo: desc

---

#### create(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### has(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### add(**entity**: `Any`, **tag**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### remove(**entity**: `Any`, **tag**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### list(**world**: `Any`, **tag**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### list(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### has_tag(**entity**: `Any`, **tag**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Text
:todo: desc

---

#### create(**entity**: `Any`, **material**: `Any`, **default_size**: `Any`, **default_font**: `Any`, **default_color**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_size(**entity**: `Any`, **default_size**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_size(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_font(**entity**: `Any`, **default_font**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_font(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_color(**entity**: `Any`, **default_color**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_color(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_align(**entity**: `Any`, **align**: `Any`, **align_vertical**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_align(**entity**: `Any`, **align**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_align(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_align_vertical(**entity**: `Any`, **align_vertical**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_align_vertical(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_bounds(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_bounds(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_attr(**entity**: `Any`, **start**: `Any`, **length**: `Any`, **key**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### attr_clear(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### commit(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_render_text(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_geometry(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_extents(**entity**: `Any`, **offset**: `Any`, **count**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_extents(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### contains(**entity**: `Any`, **x**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### has(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_text(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_text_buffer(**entity**: `Any`, **string**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_text(**entity**: `Any`, **string**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Tile
:todo: desc

---

#### create(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **depth**: `Any`, **visual_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy(**entity**: `Any`, **tile**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy_at(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **depth**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### exists_at(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **depth**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_at(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **depth**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_all(**entity**: `Any`, **into**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_all_at(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **into**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_all_at_depth(**entity**: `Any`, **depth**: `Any`, **into**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_all_with_tag(**entity**: `Any`, **tag**: `Any`, **into**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_all_with_visual(**entity**: `Any`, **visual**: `Any`, **into**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### add_tag(**entity**: `Any`, **tile**: `Any`, **tag**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### remove_tag(**entity**: `Any`, **tile**: `Any`, **tag**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### has_tag(**entity**: `Any`, **tile**: `Any`, **tag**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_tags(**entity**: `Any`, **tile**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### clear_tags(**entity**: `Any`, **tile**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set(**entity**: `Any`, **tile**: `Any`, **key**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get(**entity**: `Any`, **tile**: `Any`, **key**: `Any`, **default**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_coord(**entity**: `Any`, **tile**: `Any`, **x**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_coord_x(**entity**: `Any`, **tile**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_coord_y(**entity**: `Any`, **tile**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_depth(**entity**: `Any`, **tile**: `Any`, **depth**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_depth(**entity**: `Any`, **tile**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_offset(**entity**: `Any`, **tile**: `Any`, **x**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_offset_x(**entity**: `Any`, **tile**: `Any`, **x**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_offset_y(**entity**: `Any`, **tile**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_offset_x(**entity**: `Any`, **tile**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_offset_y(**entity**: `Any`, **tile**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### reset_size(**entity**: `Any`, **tile**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_size(**entity**: `Any`, **tile**: `Any`, **x**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_size_x(**entity**: `Any`, **tile**: `Any`, **x**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_size_y(**entity**: `Any`, **tile**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_size_x(**entity**: `Any`, **tile**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_size_y(**entity**: `Any`, **tile**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_flip(**entity**: `Any`, **tile**: `Any`, **x**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_flip_x(**entity**: `Any`, **tile**: `Any`, **flip**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_flip_y(**entity**: `Any`, **tile**: `Any`, **flip**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_flip_x(**entity**: `Any`, **tile**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_flip_y(**entity**: `Any`, **tile**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_visual(**entity**: `Any`, **tile**: `Any`, **visual**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_visual(**entity**: `Any`, **tile**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_angle(**entity**: `Any`, **tile**: `Any`, **angle**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_angle(**entity**: `Any`, **tile**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_color(**entity**: `Any`, **tile**: `Any`, **color**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_color(**entity**: `Any`, **tile**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Tiles
:todo: desc

---

#### create(**entity**: `Any`, **grid_size_x**: `Any`, **grid_size_y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create(**entity**: `Any`, **asset_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### clear(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### has(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### commit(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_grid_size(**entity**: `Any`, **x**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_grid_size(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_asset(**entity**: `Any`, **asset_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_asset_id(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_asset_id(**entity**: `Any`, **asset_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### define_source(**entity**: `Any`, **source_id**: `Any`, **material**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### undefine_source(**entity**: `Any`, **source_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### has_source(**entity**: `Any`, **source_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### define_visual(**entity**: `Any`, **source_id**: `Any`, **visual_id**: `Any`, **options**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### undefine_visual(**entity**: `Any`, **source_id**: `Any`, **visual_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### has_visual(**entity**: `Any`, **visual_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_bounds_rects(**entity**: `Any`, **tiles**: `Any`, **into**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### Transform
:todo: desc

---

#### create(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### has(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_link(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_linked(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### link(**entity**: `Any`, **target_entity**: `Any`, **reset_local**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### link(**entity**: `Any`, **target_entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### unlink(**entity**: `Any`, **reset_local**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### unlink(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### look_at_and_move(**entity**: `Any`, **pos**: `Any`, **target**: `Any`, **up**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### look_at_and_move(**entity**: `Any`, **pos**: `Any`, **target**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### look_at(**entity**: `Any`, **target**: `Any`, **up**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### look_at(**entity**: `Any`, **target**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_snap(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_pos(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_pos(**entity**: `Any`, **x**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_pos_world(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_pos_world(**entity**: `Any`, **x**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_pos_x(**entity**: `Any`, **x**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_pos_y(**entity**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_pos_z(**entity**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_pos_x_world(**entity**: `Any`, **x**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_pos_y_world(**entity**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_pos_z_world(**entity**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_scale(**entity**: `Any`, **x**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_scale(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_rotation_slerp_angle_axis(**entity**: `Any`, **axis**: `Any`, **from**: `Any`, **to**: `Any`, **t**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_rotation_slerp_angle_axis_world(**entity**: `Any`, **axis**: `Any`, **from**: `Any`, **to**: `Any`, **t**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_rotation_slerp(**entity**: `Any`, **from**: `Any`, **to**: `Any`, **t**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_rotation_slerp_world(**entity**: `Any`, **from**: `Any`, **to**: `Any`, **t**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_rotation(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_rotation_world(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_angle_axis(**entity**: `Any`, **degrees**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_angle_axis_world(**entity**: `Any`, **degrees**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_euler(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_euler_world(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_euler_x(**entity**: `Any`, **x**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_euler_y(**entity**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_euler_z(**entity**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_euler_x_world(**entity**: `Any`, **x**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_euler_y_world(**entity**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_euler_z_world(**entity**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### rotate_angle_axis_slerp(**entity**: `Any`, **axis**: `Any`, **angle_amount**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### rotate_angle_axis_slerp_world(**entity**: `Any`, **axis**: `Any`, **angle_amount**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### rotate_around_world(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **axis_x**: `Any`, **axis_y**: `Any`, **axis_z**: `Any`, **degrees**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### rotate_around(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **axis_x**: `Any`, **axis_y**: `Any`, **axis_z**: `Any`, **degrees**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### rotate_angle_axis(**entity**: `Any`, **degrees**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### rotate_angle_axis_world(**entity**: `Any`, **degrees**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### rotate_euler(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### rotate_euler_world(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### translate(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### translate(**entity**: `Any`, **x**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_pos(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_pos_x(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_pos_y(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_pos_z(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_pos_world(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_pos_world_unsnapped(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_pos_x_world(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_pos_y_world(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_pos_z_world(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### rotate2D(**entity**: `Any`, **degrees**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_angle2D(**entity**: `Any`, **degrees**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_angle2D_world(**entity**: `Any`, **degrees**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_angle2D(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_angle2D_world(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_depth2D(**entity**: `Any`, **depth**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_depth2D(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_depth2D_world(**entity**: `Any`, **depth**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_depth2D_world(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_rotation(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_rotation_world(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_rotation_matrix(**entity**: `Any`, **into_matrix**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_euler(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_euler_x(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_euler_y(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_euler_z(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_euler_world(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_euler_x_world(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_euler_y_world(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_euler_z_world(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_scale(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_scale_x(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_scale_y(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_scale_z(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_right(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_forward(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_up(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### sync(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### sync_world(**world**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### local_vector_to_world(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### world_vector_to_local(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### local_dir_to_world(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### world_dir_to_local(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### world_point_to_local(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### local_point_to_world(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### listen_all(**world**: `Any`, **fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### unlisten_all(**world**: `Any`, **handle**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### listen(**entity**: `Any`, **fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### unlisten(**entity**: `Any`, **handle**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### UI
:todo: desc

---

#### create(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`, **z**: `Any`, **camera**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### commit(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### event_cancel(**entity**: `Any`, **event_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### event_cancelled(**entity**: `Any`, **event_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### event_make_id(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_camera(**entity**: `Any`, **camera**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_render_mode(**entity**: `Any`, **mode**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_material_basis(**entity**: `Any`, **solid**: `Any`, **text**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_bounds(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_input_node(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_input_node(**entity**: `Any`, **input_node_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_focused(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_captured(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_marked(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_control_count(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_control(**entity**: `Any`, **index**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### focus_invalidate(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### focus(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### unfocus(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### mark(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### unmark(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### capture(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### uncapture(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### bring_to_front(**control**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### control_at_point(**entity**: `Any`, **x**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### dump(**ui**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### spawn(**asset_id**: `Any`, **parent**: `Any`, **instance_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### make(**ui**: `Any`, **asset**: `Any`, **instance_id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### draw_depth_of(**control**: `Any`, **index**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### draw_text(**control**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **string**: `Any`, **size**: `Any`, **font**: `Any`, **color**: `Any`, **align**: `Any`, **align_vertical**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### draw_text(**control**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **string**: `Any`, **size**: `Any`, **font**: `Any`, **color**: `Any`, **align**: `Any`, **align_vertical**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### draw_image(**control**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **color**: `Any`, **uv**: `Any`, **image**: `Any`, **pixelated**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### draw_image(**control**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **color**: `Any`, **uv**: `Any`, **image**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### draw_quad(**control**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **color**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### draw_circle(**control**: `Any`, **ox**: `Any`, **oy**: `Any`, **oz**: `Any`, **rx**: `Any`, **ry**: `Any`, **start_angle**: `Any`, **end_angle**: `Any`, **smoothness**: `Any`, **color**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### draw_line(**control**: `Any`, **x1**: `Any`, **y1**: `Any`, **x2**: `Any`, **y2**: `Any`, **z**: `Any`, **style**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### draw_rect(**control**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **style**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### draw_rect_detailed(**control**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **radius**: `Any`, **smoothness**: `Any`, **style**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### draw_ring(**control**: `Any`, **ox**: `Any`, **oy**: `Any`, **oz**: `Any`, **rx**: `Any`, **ry**: `Any`, **start_angle**: `Any`, **end_angle**: `Any`, **smoothness**: `Any`, **style**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### draw_path(**control**: `Any`, **points**: `Any`, **style**: `Any`, **closed**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### events_emit(**control**: `Any`, **type**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### events_emit(**control**: `Any`, **type**: `Any`, **data**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### UIClear
:todo: desc

---

#### destroy -> unknown
:todo: desc
```js
//:todo: example
```

#### remove -> unknown
:todo: desc
```js
//:todo: example
```

#### set_invisible -> unknown
:todo: desc
```js
//:todo: example
```

#### remove_set_invisible -> unknown
:todo: desc
```js
//:todo: example
```

### UILayout
:todo: desc

---

#### create(**ui_entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy(**ui_entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### commit(**ui_entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_behave(**ui_entity**: `Any`, **control**: `Any`, **behave**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_contain(**ui_entity**: `Any`, **control**: `Any`, **contain**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_margin(**ui_entity**: `Any`, **control**: `Any`, **left**: `Any`, **top**: `Any`, **right**: `Any`, **bottom**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### UILayoutBehave
:todo: desc

---

#### left -> unknown
:todo: desc
```js
//:todo: example
```

#### top -> unknown
:todo: desc
```js
//:todo: example
```

#### right -> unknown
:todo: desc
```js
//:todo: example
```

#### bottom -> unknown
:todo: desc
```js
//:todo: example
```

#### hfill -> unknown
:todo: desc
```js
//:todo: example
```

#### vfill -> unknown
:todo: desc
```js
//:todo: example
```

#### hcenter -> unknown
:todo: desc
```js
//:todo: example
```

#### vcenter -> unknown
:todo: desc
```js
//:todo: example
```

#### center -> unknown
:todo: desc
```js
//:todo: example
```

#### fill -> unknown
:todo: desc
```js
//:todo: example
```

#### break_line -> unknown
:todo: desc
```js
//:todo: example
```

### UILayoutContain
:todo: desc

---

#### row -> unknown
:todo: desc
```js
//:todo: example
```

#### column -> unknown
:todo: desc
```js
//:todo: example
```

#### layout -> unknown
:todo: desc
```js
//:todo: example
```

#### flex -> unknown
:todo: desc
```js
//:todo: example
```

#### nowrap -> unknown
:todo: desc
```js
//:todo: example
```

#### wrap -> unknown
:todo: desc
```js
//:todo: example
```

#### start -> unknown
:todo: desc
```js
//:todo: example
```

#### middle -> unknown
:todo: desc
```js
//:todo: example
```

#### end -> unknown
:todo: desc
```js
//:todo: example
```

#### justify -> unknown
:todo: desc
```js
//:todo: example
```

### UIRenderMode
:todo: desc

---

#### unknown -> unknown
:todo: desc
```js
//:todo: example
```

#### image -> unknown
:todo: desc
```js
//:todo: example
```

#### world -> unknown
:todo: desc
```js
//:todo: example
```

### Values
:todo: desc

---

#### create(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### has(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### has_key(**entity**: `Any`, **key**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### remove_key(**entity**: `Any`, **key**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_keys(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get(**entity**: `Any`, **key**: `Any`, **default**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set(**entity**: `Any`, **key**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_string(**entity**: `Any`, **key**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_bool(**entity**: `Any`, **key**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_number(**entity**: `Any`, **key**: `Any`, **value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_string(**entity**: `Any`, **key**: `Any`, **value**: `Any`, **length**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_float2(**entity**: `Any`, **key**: `Any`, **x**: `Any`, **y**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_float3(**entity**: `Any`, **key**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_float4(**entity**: `Any`, **key**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_type(**entity**: `Any`, **key**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_bool(**entity**: `Any`, **key**: `Any`, **default**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_number(**entity**: `Any`, **key**: `Any`, **default**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_string(**entity**: `Any`, **key**: `Any`, **default**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_float2(**entity**: `Any`, **key**: `Any`, **default**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_float3(**entity**: `Any`, **key**: `Any`, **default**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_float4(**entity**: `Any`, **key**: `Any`, **default**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### ValuesType
:todo: desc

---

#### unknown -> unknown
:todo: desc
```js
//:todo: example
```

#### bool -> unknown
:todo: desc
```js
//:todo: example
```

#### number -> unknown
:todo: desc
```js
//:todo: example
```

#### string -> unknown
:todo: desc
```js
//:todo: example
```

#### float2 -> unknown
:todo: desc
```js
//:todo: example
```

#### float3 -> unknown
:todo: desc
```js
//:todo: example
```

#### float4 -> unknown
:todo: desc
```js
//:todo: example
```

#### name(**value**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### World
:todo: desc

---

#### exists(**id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### valid(**world**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get(**id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_id(**world**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_id(**world**: `Any`, **id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_default() -> unknown
:todo: desc
```js
//:todo: example
```

#### set_default(**world**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### list(**world**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### list_ids(**world**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### clear(**world**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### tag_add(**world**: `Any`, **tag**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### tag_remove(**world**: `Any`, **tag**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### tag_has(**world**: `Any`, **tag**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_delta(**world**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### tick_systems(**world**: `Any`, **delta**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### schedule(**world**: `Any`, **time**: `Any`, **count**: `Any`, **fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### schedule(**world**: `Any`, **time**: `Any`, **fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### unschedule(**world**: `Any`, **handle**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### render_with_set(**world**: `Any`, **camera**: `Any`, **set**: `Any`, **target_path**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### render_with_set(**world**: `Any`, **camera**: `Any`, **set**: `Any`, **target_path**: `Any`, **settings**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### render_with_set(**world**: `Any`, **camera**: `Any`, **set**: `Any`, **target_path**: `Any`, **target_resource**: `Any`, **target_region**: `Any`, **settings**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### render(**world**: `Any`, **camera**: `Any`, **target_path**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### render(**world**: `Any`, **camera**: `Any`, **target_path**: `Any`, **settings**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### render(**world**: `Any`, **camera**: `Any`, **target_path**: `Any`, **target_resource**: `Any`, **target_region**: `Any`, **settings**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### render(**world**: `Any`, **desc**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### render_fn(**world**: `Any`, **camera**: `Any`, **target_resource**: `Any`, **target_region**: `Any`, **settings**: `Any`, **fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### get_rate(**world**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_rate(**world**: `Any`, **rate**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### set_time(**world**: `Any`, **time**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### time(**world**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### render_set(**world**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### render_set_add(**world**: `Any`, **geometry**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### render_set_add(**world**: `Any`, **geometry**: `Any`, **entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### render_set_remove(**world**: `Any`, **geometry**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### render_set_remove(**world**: `Any`, **geometry**: `Any`, **entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### render_get_entity(**world**: `Any`, **geometry**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### render_get_entity_set(**entity**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### disable(**world**: `Any`, **state**: `Any`, **entities**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### disable(**world**: `Any`, **state**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### emit(**world**: `Any`, **tags**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### emit(**world**: `Any`, **tags**: `Any`, **data**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### listen(**world**: `Any`, **tags**: `Any`, **fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### unlisten(**world**: `Any`, **tags**: `Any`, **fn**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### create() -> unknown
:todo: desc
```js
//:todo: example
```

#### create(**id**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### destroy(**world**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### tick(**world**: `Any`, **delta**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

### WorldRenderDesc
:todo: desc

---

#### camera -> unknown
:todo: desc
```js
//:todo: example
```

#### camera=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### camera(**v**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### cull_camera -> unknown
:todo: desc
```js
//:todo: example
```

#### cull_camera=(v : Any) -> unknown
:todo: desc
```js
//:todo: example
```

#### cull_camera(**v**: `Any`) -> unknown
:todo: desc
```js
//:todo: example
```

#### new() -> unknown
:todo: desc
```js
//:todo: example
```

