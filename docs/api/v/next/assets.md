#![](../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.10.1`)  


---

## `luxe: assets` module

- [Assets](#assets)   
- [Strings](#strings)   

---

### Assets
`:::js import "luxe: assets" for Assets`
> The `Assets` services is how you access loaded assets, and query if an asset is loaded.
> The primary use for this at the moment is the accessors like `Assets.image`, and finding out 
> if an asset is loaded via `Assets.has_image`. 
> 
> Note that the asset system is a work in progress and is not final. 
> There are several accessors missing, for example, fonts are often referenced 
> as a string, not via `Assets.font("fonts/name")`. Later, all assets will be unified into this form as intended.
> 
> Also, they're supposed to be able to reload dynamically, many can't currently. And remember the input
> to the asset system is compiled assets, not the assets themselves. 
> 
> Finally, there are functions in the API that shouldn't be used directly (they aren't listed here.)

- [image](#Assets.image)(**id**: `String`)
- [bytes](#Assets.bytes)(**id**: `String`)
- [material](#Assets.material)(**id**: `String`)
- [atlas](#Assets.atlas)(**id**: `String`)
- [lx](#Assets.lx)(**id**: `String`)
- [has_shader_library](#Assets.has_shader_library)(**id**: `String`)
- [has_image](#Assets.has_image)(**id**: `String`)
- [has_material_basis](#Assets.has_material_basis)(**id**: `String`)
- [has_material](#Assets.has_material)(**id**: `String`)
- [has_bytes](#Assets.has_bytes)(**id**: `String`)
- [has_settings](#Assets.has_settings)(**id**: `String`)
- [has_atlas](#Assets.has_atlas)(**id**: `String`)
- [has_physics](#Assets.has_physics)(**id**: `String`)
- [has_prototype](#Assets.has_prototype)(**id**: `String`)
- [has_scene](#Assets.has_scene)(**id**: `String`)
- [has_input](#Assets.has_input)(**id**: `String`)
- [has_anim](#Assets.has_anim)(**id**: `String`)
- [has_mesh](#Assets.has_mesh)(**id**: `String`)
- [has_tiles](#Assets.has_tiles)(**id**: `String`)
- [has_ui](#Assets.has_ui)(**id**: `String`)
- [unload_input](#Assets.unload_input)(**id**: `String`)
- [load_input](#Assets.load_input)(**id**: `String`)

<hr/>
<endpoint module="luxe: assets" class="Assets" signature="image(id : String)"></endpoint>
<signature id="Assets.image">Assets.image(**id**: `String`)
<a class="headerlink" href="#Assets.image" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Image`
> Return a loaded image by id.
> 
>   ```js
>   var image = Assets.image("image/player")
>   Log.print("width: %(Image.get_width(image))")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="bytes(id : String)"></endpoint>
<signature id="Assets.bytes">Assets.bytes(**id**: `String`)
<a class="headerlink" href="#Assets.bytes" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Returns the data stored as bytes. 
> A Wren `String` is also a byte sequence, used via `string.bytes`.
> 
> **Note** That unlike other assets, bytes are stored by name _with_ extension.
> For example if you put a file called `data/hello.txt` in your project,
> you would access it via `var data = Assets.bytes("data/hello.txt")`.
> 
> This is because the extension might be meaningful to the user of the bytes,
> for example loading an image based on png vs jpg extension would be impossible
> if we don't know the extension of the data. Because bytes are "opaque", as in, 
> we don't care what they store, we just store them for you to access, we keep the extension.
> 
>   ```js
>   var text = Assets.bytes("data/hello.txt")
>   Log.print(text) //prints the contents of the file (the contents at compile time).
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="material(id : String)"></endpoint>
<signature id="Assets.material">Assets.material(**id**: `String`)
<a class="headerlink" href="#Assets.material" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Material`
> Returns a loaded material by id.
> 
>   ```js
>   var material = Assets.material("material/player")
>   Sprite.set_material(player, material)
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="atlas(id : String)"></endpoint>
<signature id="Assets.atlas">Assets.atlas(**id**: `String`)
<a class="headerlink" href="#Assets.atlas" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Atlas`
> Returns a loaded atlas by id.
> 
>   ```js
>   var atlas = Assets.atlas("atlas/example")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="lx(id : String)"></endpoint>
<signature id="Assets.lx">Assets.lx(**id**: `String`)
<a class="headerlink" href="#Assets.lx" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Any`
> Returns the LX parsed representation of a `bytes` asset.
> This is convenience for `Assets.bytes` followed by `LX.parse`.
> Returns null if the asset isn't found, or if parsing failed.
> 
> See `Assets.bytes`, as bytes require an extension.
> 
>   ```js
>   //assuming our data contains { speaker="sara" message="follow me." }
>   var dialog = Assets.lx("dialog/hello.lx")
>   var speaker = dialog["speaker"]
>   var message = dialog["message"]
>   Log.print("%(speaker): %(message)")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_shader_library(id : String)"></endpoint>
<signature id="Assets.has_shader_library">Assets.has_shader_library(**id**: `String`)
<a class="headerlink" href="#Assets.has_shader_library" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if a shader library with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_shader_library("assets/shaders")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_image(id : String)"></endpoint>
<signature id="Assets.has_image">Assets.has_image(**id**: `String`)
<a class="headerlink" href="#Assets.has_image" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if an image with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_image("image/player")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_material_basis(id : String)"></endpoint>
<signature id="Assets.has_material_basis">Assets.has_material_basis(**id**: `String`)
<a class="headerlink" href="#Assets.has_material_basis" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if a material basis with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_material_basis("basis/example")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_material(id : String)"></endpoint>
<signature id="Assets.has_material">Assets.has_material(**id**: `String`)
<a class="headerlink" href="#Assets.has_material" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if a material with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_material("material/player")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_bytes(id : String)"></endpoint>
<signature id="Assets.has_bytes">Assets.has_bytes(**id**: `String`)
<a class="headerlink" href="#Assets.has_bytes" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if a bytes asset with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_bytes("data/hello.txt")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_settings(id : String)"></endpoint>
<signature id="Assets.has_settings">Assets.has_settings(**id**: `String`)
<a class="headerlink" href="#Assets.has_settings" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if a settings asset with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_settings("settings/area1")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_atlas(id : String)"></endpoint>
<signature id="Assets.has_atlas">Assets.has_atlas(**id**: `String`)
<a class="headerlink" href="#Assets.has_atlas" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if an atlas asset with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_atlas("atlas/example")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_physics(id : String)"></endpoint>
<signature id="Assets.has_physics">Assets.has_physics(**id**: `String`)
<a class="headerlink" href="#Assets.has_physics" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if a physics asset with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_physics("physics/ice")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_prototype(id : String)"></endpoint>
<signature id="Assets.has_prototype">Assets.has_prototype(**id**: `String`)
<a class="headerlink" href="#Assets.has_prototype" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if a prototype with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_prototype("proto/tree")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_scene(id : String)"></endpoint>
<signature id="Assets.has_scene">Assets.has_scene(**id**: `String`)
<a class="headerlink" href="#Assets.has_scene" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if a scene with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_scene("scene/area1")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_input(id : String)"></endpoint>
<signature id="Assets.has_input">Assets.has_input(**id**: `String`)
<a class="headerlink" href="#Assets.has_input" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if an input asset with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_input("input/player")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_anim(id : String)"></endpoint>
<signature id="Assets.has_anim">Assets.has_anim(**id**: `String`)
<a class="headerlink" href="#Assets.has_anim" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if an animation with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_anim("anim/jump")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_mesh(id : String)"></endpoint>
<signature id="Assets.has_mesh">Assets.has_mesh(**id**: `String`)
<a class="headerlink" href="#Assets.has_mesh" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if a mesh with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_mesh("mesh/cube")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_tiles(id : String)"></endpoint>
<signature id="Assets.has_tiles">Assets.has_tiles(**id**: `String`)
<a class="headerlink" href="#Assets.has_tiles" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if a tilemap with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_tiles("tiles/caves")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_ui(id : String)"></endpoint>
<signature id="Assets.has_ui">Assets.has_ui(**id**: `String`)
<a class="headerlink" href="#Assets.has_ui" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if a ui asset with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_ui("ui/menu")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="unload_input(id : String)"></endpoint>
<signature id="Assets.unload_input">Assets.unload_input(**id**: `String`)
<a class="headerlink" href="#Assets.unload_input" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Unload the input asset, which undefines any nodes or events   

<endpoint module="luxe: assets" class="Assets" signature="load_input(id : String)"></endpoint>
<signature id="Assets.load_input">Assets.load_input(**id**: `String`)
<a class="headerlink" href="#Assets.load_input" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Load an input asset, which defines any nodes or events within it   

### Strings
`:::js import "luxe: assets" for Strings`
> When dealing with data like assets, storing a string directly can take up a lot of space.
> Instead, what we can do is store the strings once, in a shared place, and then reference that string later.
> 
> At runtime, strings can also be more expensive than is ideal (like needing to iterate the characters individually, or taking up more memory).
> 
> In both cases, what we store instead of a string is a _string id_, which is just a number.
> 
> Comparing two numbers, looking up numbers in an array or map and so on, it's _much_ faster with a number than using
> the string itself. Operating on numbers is both faster and simpler, and has a fixed size in memory.
> This is commonly called "string interning".
> 
> In luxe, the `Strings` class is how you interact with the strings available to your game.
> For example, `var name_id = Entity.get_name(entity)` will return a _string id_, not a string.
> To get the string, you can use `var name = Strings.get(name_id)`.
> Note that if the name is unknown to `Strings`, it will return null, so handle that appropriately.
> 
> To add a string, use `Strings.add("string")`.
> 
> For debugging strings, if you look inside `.luxe/luxe.strings.lx`, 
> this lists all the strings your assets reference, and what their key is.
> 
>   ```js
>   //Assuming this string hasn't been added before:
>   Log.print( Strings.get("hello") ) //prints null
>   var key = Strings.add("hello") //key is 1335831723
>   Log.print( Strings.get("hello") ) //prints 'hello'
>   ```

- [add](#Strings.add)(**value**: `String`)
- [get](#Strings.get)(**key**: `Num`)

<hr/>
<endpoint module="luxe: assets" class="Strings" signature="add(value : String)"></endpoint>
<signature id="Strings.add">Strings.add(**value**: `String`)
<a class="headerlink" href="#Strings.add" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Adds a string to the `Strings` service and returns the key.
> 
>   ```js
>   Log.print(Strings.add("hello")) //prints 1335831723
>   ```   

<endpoint module="luxe: assets" class="Strings" signature="get(key : Num)"></endpoint>
<signature id="Strings.get">Strings.get(**key**: `Num`)
<a class="headerlink" href="#Strings.get" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Return the value associated with the given key.
> This will return null if the string is not found.
> 
>   ```js
>   var name_id = Entity.get_name(entity)
>   var name = Strings.get(name_id)
>   if(name) {
>     Log.print("entity name is %(name)")
>   } else {
>     Log.print("entity name is not known (or it has no name)")
>   }
>   ```   

