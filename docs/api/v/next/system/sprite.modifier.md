#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2024.12.4`)  


---

## `luxe: system/sprite.modifier` module

- [Advanced](#advanced)   
- [Data](#data)   
- [Dissolve](#dissolve)   
- [HSV](#hsv)   
- [Outline](#outline)   
- [Shadow](#shadow)   
- [Shine](#shine)   
- [Sprite](#sprite)   
- [SpriteBillboard](#spritebillboard)   
- [System](#system)   

---

### Advanced
`:::js import "luxe: system/sprite.modifier" for Advanced`
> no docs found

- `:::js var auto_size : Bool = true`
- `:::js var material_input : String = "sprite.image"`
- `:::js var HSV : HSV = Object`
- `:::js var outline : Outline = Object`
- `:::js var shadow : Shadow = Object`
- `:::js var dissolve : Dissolve = Object`
- `:::js var shine : Shine = Object`

<hr/>
### Data
`:::js import "luxe: system/sprite.modifier" for Data`
> no docs found

- `:::js var image : Asset = "luxe: image/logo"`
- `:::js var size : Float2 = [64, 64]`
- `:::js var origin : Float2 = [0.5, 0.5]`
- `:::js var skew : Float2 = [0, 0]`
- `:::js var color : Color = [1, 1, 1, 1]`
- `:::js var uv : Float4 = [0, 0, 1, 1]`
- `:::js var flip_x : Bool = false`
- `:::js var flip_y : Bool = false`
- `:::js var pixelated : Bool = false`
- `:::js var billboard : SpriteBillboard = SpriteBillboard.none`
- `:::js var billboard_lock : Float3 = [0, 0, 0]`
- `:::js var atlas : Asset = null`
- `:::js var atlas_image_id : String = null`
- `:::js var material : Asset = null`
- `:::js var advanced : Advanced = Object`

<hr/>
### Dissolve
`:::js import "luxe: system/sprite.modifier" for Dissolve`
> no docs found

- `:::js var enabled : Bool = false`
- `:::js var image : Asset = null`
- `:::js var uv : Float4 = [0, 0, 1, 1]`
- `:::js var value : Num = 1`

<hr/>
### HSV
`:::js import "luxe: system/sprite.modifier" for HSV`
> no docs found

- `:::js var enabled : Bool = false`
- `:::js var hue_change : Num = 0`
- `:::js var saturation : Num = 1`
- `:::js var value : Num = 1`

<hr/>
### Outline
`:::js import "luxe: system/sprite.modifier" for Outline`
> no docs found

- `:::js var enabled : Bool = false`
- `:::js var color : Color = [1, 1, 1, 1]`
- `:::js var thickness : Num = 0`

<hr/>
### Shadow
`:::js import "luxe: system/sprite.modifier" for Shadow`
> no docs found

- `:::js var enabled : Bool = false`
- `:::js var offset : Float2 = [0, 0]`
- `:::js var color : Color = [0, 0, 0, 1]`
- `:::js var softness : Num = 0`

<hr/>
### Shine
`:::js import "luxe: system/sprite.modifier" for Shine`
> no docs found

- `:::js var enabled : Bool = false`
- `:::js var color : Color = [1, 0.92, 0.16, 1]`
- `:::js var direction : Float2 = [0, 0]`
- `:::js var width : Num = 0`
- `:::js var speed : Num = 0`
- `:::js var spacing : Num = 0`

<hr/>
### Sprite
`:::js import "luxe: system/sprite.modifier" for Sprite`
> A sprite is an image attached to an entity.   
> The `Sprite` modifier provides flipping, sizing, sub images and more.
> To attach a sprite to an entity, call `Sprite.create`:
> 
>   ```js
>   var entity = Entity.create(world)
>   var material = Assets.material("luxe: material/logo")
>   Sprite.create(entity, material, 128, 128)
>   ```

- [create](#Sprite.create+4)(**entity**: `Entity`, **image**: `Image`, **width**: `Num`, **height**: `Num`)
- [create](#Sprite.create+2)(**entity**: `Entity`, **image**: `Image`)
- [create](#Sprite.create)(**entity**: `Entity`)
- [create_with](#Sprite.create_with+4)(**entity**: `Entity`, **material**: `Material`, **width**: `Num`, **height**: `Num`)
- [create_with](#Sprite.create_with+2)(**entity**: `Entity`, **material**: `Material`)
- [create](#Sprite.create+3)(**entity**: `Entity`, **atlas**: `Atlas`, **atlas_image**: `String`)
- [destroy](#Sprite.destroy)(**entity**: `Entity`)
- [has](#Sprite.has)(**entity**: `Entity`)
- [contains](#Sprite.contains+3)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
- [set_material](#Sprite.set_material+2)(**entity**: `Entity`, **material**: `Material`)
- [get_material](#Sprite.get_material)(**entity**: `Entity`)
- [set_image](#Sprite.set_image+2)(**entity**: `Entity`, **image**: `Image`)
- [get_image](#Sprite.get_image)(**entity**: `Entity`)
- [set_origin](#Sprite.set_origin+3)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
- [get_origin](#Sprite.get_origin)(**entity**: `Entity`)
- [set_flip_h](#Sprite.set_flip_h+2)(**entity**: `Entity`, **flipped**: `Bool`)
- [get_flip_h](#Sprite.get_flip_h)(**entity**: `Entity`)
- [set_flip_v](#Sprite.set_flip_v+2)(**entity**: `Entity`, **flipped**: `Bool`)
- [get_flip_v](#Sprite.get_flip_v)(**entity**: `Entity`)
- [set_billboard](#Sprite.set_billboard+3)(**entity**: `Entity`, **kind**: `SpriteBillboard`, **lock**: `Float3`)
- [get_billboard](#Sprite.get_billboard)(**entity**: `Entity`)
- [set_size](#Sprite.set_size+3)(**entity**: `Entity`, **width**: `Num`, **height**: `Num`)
- [set_width](#Sprite.set_width+2)(**entity**: `Entity`, **width**: `Num`)
- [get_width](#Sprite.get_width)(**entity**: `Entity`)
- [set_height](#Sprite.set_height+2)(**entity**: `Entity`, **height**: `Num`)
- [get_height](#Sprite.get_height)(**entity**: `Entity`)
- [set_alpha](#Sprite.set_alpha+2)(**entity**: `Entity`, **alpha**: `Num`)
- [get_alpha](#Sprite.get_alpha)(**entity**: `Entity`)
- [set_color](#Sprite.set_color+2)(**entity**: `Entity`, **color**: `Color`)
- [set_color](#Sprite.set_color+5)(**entity**: `Entity`, **r**: `Num`, **g**: `Num`, **b**: `Num`, **a**: `Num`)
- [get_color](#Sprite.get_color)(**entity**: `Entity`)
- [set_uv](#Sprite.set_uv+5)(**entity**: `Entity`, **x0**: `Num`, **y0**: `Num`, **x1**: `Num`, **y1**: `Num`)
- [get_uv](#Sprite.get_uv)(**entity**: `Entity`)
- [set_skew](#Sprite.set_skew+3)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
- [get_skew](#Sprite.get_skew)(**entity**: `Entity`)
- [get_geometry](#Sprite.get_geometry)(**entity**: `Entity`)
- [set_geometry](#Sprite.set_geometry+2)(**entity**: `Entity`, **geo**: `Geometry`)
- [get_auto_size](#Sprite.get_auto_size)(**entity**: `Entity`)
- [set_auto_size](#Sprite.set_auto_size+2)(**entity**: `Entity`, **value**: `Bool`)
- [get_material_input](#Sprite.get_material_input)(**entity**: `Entity`)
- [set_material_input](#Sprite.set_material_input+2)(**entity**: `Entity`, **value**: `Bool`)
- [get_hsv_adjust](#Sprite.get_hsv_adjust)(**entity**: `Entity`)
- [set_hsv_adjust](#Sprite.set_hsv_adjust+5)(**entity**: `Entity`, **enabled**: `Bool`, **hue_change**: `Num`, **saturation**: `Num`, **value**: `Num`)
- [set_effect_HSV_enabled](#Sprite.set_effect_HSV_enabled+2)(**entity**: `Entity`, **enabled**: `Bool`)
- [get_effect_HSV_enabled](#Sprite.get_effect_HSV_enabled+2)(**entity**: `Entity`, **enabled**: `Bool`)
- [set_effect_HSV_hue_change](#Sprite.set_effect_HSV_hue_change+2)(**entity**: `Entity`, **hue_change**: `Num`)
- [get_effect_HSV_hue_change](#Sprite.get_effect_HSV_hue_change+2)(**entity**: `Entity`, **hue_change**: `Num`)
- [set_effect_HSV_saturation](#Sprite.set_effect_HSV_saturation+2)(**entity**: `Entity`, **saturation**: `Num`)
- [get_effect_HSV_saturation](#Sprite.get_effect_HSV_saturation+2)(**entity**: `Entity`, **saturation**: `Num`)
- [set_effect_HSV_value](#Sprite.set_effect_HSV_value+2)(**entity**: `Entity`, **value**: `Num`)
- [get_effect_HSV_value](#Sprite.get_effect_HSV_value+2)(**entity**: `Entity`, **value**: `Num`)
- [get_outline](#Sprite.get_outline)(**entity**: `Entity`)
- [set_outline](#Sprite.set_outline+4)(**entity**: `Entity`, **enabled**: `Bool`, **color**: `Color`, **thickness**: `Num`)
- [set_effect_outline_enabled](#Sprite.set_effect_outline_enabled+2)(**entity**: `Entity`, **enabled**: `Bool`)
- [get_effect_outline_enabled](#Sprite.get_effect_outline_enabled+2)(**entity**: `Entity`, **enabled**: `Bool`)
- [set_effect_outline_color](#Sprite.set_effect_outline_color+2)(**entity**: `Entity`, **color**: `Color`)
- [get_effect_outline_color](#Sprite.get_effect_outline_color+2)(**entity**: `Entity`, **color**: `Color`)
- [set_effect_outline_thickness](#Sprite.set_effect_outline_thickness+2)(**entity**: `Entity`, **thickness**: `Num`)
- [get_effect_outline_thickness](#Sprite.get_effect_outline_thickness+2)(**entity**: `Entity`, **thickness**: `Num`)
- [get_shadow](#Sprite.get_shadow)(**entity**: `Entity`)
- [set_shadow](#Sprite.set_shadow+5)(**entity**: `Entity`, **enabled**: `Bool`, **offset**: `Num`, **color**: `Color`, **softness**: `Num`)
- [set_effect_shadow_enabled](#Sprite.set_effect_shadow_enabled+2)(**entity**: `Entity`, **enabled**: `Bool`)
- [get_effect_shadow_enabled](#Sprite.get_effect_shadow_enabled+2)(**entity**: `Entity`, **enabled**: `Bool`)
- [set_effect_shadow_offset](#Sprite.set_effect_shadow_offset+2)(**entity**: `Entity`, **offset**: `Vector2`)
- [get_effect_shadow_offset](#Sprite.get_effect_shadow_offset+2)(**entity**: `Entity`, **offset**: `Vector2`)
- [set_effect_shadow_color](#Sprite.set_effect_shadow_color+2)(**entity**: `Entity`, **color**: `Color`)
- [get_effect_shadow_color](#Sprite.get_effect_shadow_color+2)(**entity**: `Entity`, **color**: `Color`)
- [get_dissolve](#Sprite.get_dissolve)(**entity**: `Entity`)
- [set_dissolve](#Sprite.set_dissolve+5)(**entity**: `Entity`, **enabled**: `Bool`, **image**: `Image`, **uv**: `List`, **value**: `Num`)
- [set_effect_dissolve_enabled](#Sprite.set_effect_dissolve_enabled+2)(**entity**: `Entity`, **enabled**: `Bool`)
- [get_effect_dissolve_enabled](#Sprite.get_effect_dissolve_enabled+2)(**entity**: `Entity`, **enabled**: `Bool`)
- [set_effect_dissolve_image](#Sprite.set_effect_dissolve_image+2)(**entity**: `Entity`, **image**: `Image`)
- [get_effect_dissolve_image](#Sprite.get_effect_dissolve_image+2)(**entity**: `Entity`, **image**: `Image`)
- [set_effect_dissolve_uv](#Sprite.set_effect_dissolve_uv+2)(**entity**: `Entity`, **uv**: `Vector4`)
- [get_effect_dissolve_uv](#Sprite.get_effect_dissolve_uv+2)(**entity**: `Entity`, **uv**: `Vector4`)
- [set_effect_dissolve_value](#Sprite.set_effect_dissolve_value+2)(**entity**: `Entity`, **value**: `Num`)
- [get_effect_dissolve_value](#Sprite.get_effect_dissolve_value+2)(**entity**: `Entity`, **value**: `Num`)
- [get_shine](#Sprite.get_shine)(**entity**: `Entity`)
- [set_shine](#Sprite.set_shine+7)(**entity**: `Entity`, **enabled**: `Bool`, **color**: `Num`, **direction**: `Vector2`, **width**: `Num`, **speed**: `Num`, **spacing**: `Num`)
- [set_effect_shine_enabled](#Sprite.set_effect_shine_enabled+2)(**entity**: `Entity`, **enabled**: `Bool`)
- [get_effect_shine_enabled](#Sprite.get_effect_shine_enabled+2)(**entity**: `Entity`, **enabled**: `Bool`)
- [set_effect_shine_color](#Sprite.set_effect_shine_color+2)(**entity**: `Entity`, **color**: `Color`)
- [get_effect_shine_color](#Sprite.get_effect_shine_color+2)(**entity**: `Entity`, **color**: `Color`)
- [set_effect_shine_direction](#Sprite.set_effect_shine_direction+2)(**entity**: `Entity`, **direction**: `Vector2`)
- [get_effect_shine_direction](#Sprite.get_effect_shine_direction+2)(**entity**: `Entity`, **direction**: `Vector2`)
- [set_effect_shine_width](#Sprite.set_effect_shine_width+2)(**entity**: `Entity`, **width**: `Num`)
- [get_effect_shine_width](#Sprite.get_effect_shine_width+2)(**entity**: `Entity`, **width**: `Num`)
- [set_effect_shine_speed](#Sprite.set_effect_shine_speed+2)(**entity**: `Entity`, **speed**: `Num`)
- [get_effect_shine_speed](#Sprite.get_effect_shine_speed+2)(**entity**: `Entity`, **speed**: `Num`)
- [set_effect_shine_spacing](#Sprite.set_effect_shine_spacing+2)(**entity**: `Entity`, **spacing**: `Num`)
- [get_effect_shine_spacing](#Sprite.get_effect_shine_spacing+2)(**entity**: `Entity`, **spacing**: `Num`)

<hr/>
<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="create(entity : Entity, image : Image, width : Num, height : Num)"></endpoint>
<signature id="Sprite.create+4">Sprite.create(**entity**: `Entity`, **image**: `Image`, **width**: `Num`, **height**: `Num`)
<a class="headerlink" href="#Sprite.create+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Attach a `Sprite` modifier to `entity`, drawn using `image`,
> with a given size of `width`x`height`.
> 
>   ```js
>   var entity = Entity.create(world)
>   var image = Assets.image("luxe: image/logo")
>   Sprite.create(entity, material, 128, 128)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="create(entity : Entity, image : Image)"></endpoint>
<signature id="Sprite.create+2">Sprite.create(**entity**: `Entity`, **image**: `Image`)
<a class="headerlink" href="#Sprite.create+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Attach a `Sprite` modifier to `entity`, drawn using `image`.
> The size of the sprite will be determined by the size of the image.
> 
>   ```js
>   var entity = Entity.create(world)
>   var image = Assets.image("luxe: image/logo")
>   Sprite.create(entity, image)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="create(entity : Entity)"></endpoint>
<signature id="Sprite.create">Sprite.create(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Attach a `Sprite` modifier to `entity`, drawn using a default `image`.
> Use `Sprite.set_image` or `Sprite.set_material` to change it later.
> 
>   ```js
>   var entity = Entity.create(world)
>   Sprite.create(entity)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="create_with(entity : Entity, material : Material, width : Num, height : Num)"></endpoint>
<signature id="Sprite.create_with+4">Sprite.create_with(**entity**: `Entity`, **material**: `Material`, **width**: `Num`, **height**: `Num`)
<a class="headerlink" href="#Sprite.create_with+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Attach a `Sprite` modifier to `entity`, drawn using `material`,
> with a size of `width`x`height`.
> 
>   ```js
>   var entity = Entity.create(world)
>   var material = Assets.material("luxe: material/logo")
>   Sprite.create_with(entity, material, 128, 128)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="create_with(entity : Entity, material : Material)"></endpoint>
<signature id="Sprite.create_with+2">Sprite.create_with(**entity**: `Entity`, **material**: `Material`)
<a class="headerlink" href="#Sprite.create_with+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Attach a `Sprite` modifier to `entity`, drawn using `material`.
> The size of the sprite will be determined by the `sprite.image` slot in the material.
> 
>   ```js
>   var entity = Entity.create(world)
>   var material = Assets.material("luxe: material/logo")
>   Sprite.create(entity, material)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="create(entity : Entity, atlas : Atlas, atlas_image : String)"></endpoint>
<signature id="Sprite.create+3">Sprite.create(**entity**: `Entity`, **atlas**: `Atlas`, **atlas_image**: `String`)
<a class="headerlink" href="#Sprite.create+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Attach a `Sprite` modifier to `entity`, drawn using the `atlas`, 
> using the image name in the atlas as `atlas_image`,
> with a size defined by the image in the atlas.
> 
>   ```js
>   var entity = Entity.create(world)
>   var atlas = Assets.atlas("atlas/example")
>   var image_name = "images/atlas/example/tree"
>   Sprite.create(entity, atlas, image_name)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="destroy(entity : Entity)"></endpoint>
<signature id="Sprite.destroy">Sprite.destroy(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Detach and destroy the `Sprite` attached to `entity`
> 
>   ```js
>   Sprite.destroy(entity)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="has(entity : Entity)"></endpoint>
<signature id="Sprite.has">Sprite.has(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if `entity` has a `Sprite` modifier attached.
> 
>   ```js
>   if(Sprite.has(entity)) {
>     Log.print("found sprite")
>   }
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="contains(entity : Entity, x : Num, y : Num)"></endpoint>
<signature id="Sprite.contains+3">Sprite.contains(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
<a class="headerlink" href="#Sprite.contains+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if the `Sprite` attached to `entity` contains the point at `x`,`y` (in world units).
> Note that the function is based on the sprite `width` and `height`, it is not pixel perfect.
> 
>   ```js
>   //Convert mouse coords to world units
>   var pos = Camera.screen_point_to_world(
>       app.camera,
>       Input.mouse_x(),
>       Input.mouse_y())
>   //Check if point is inside the sprite
>   if(Sprite.contains(entity, pos.x, pos.y)) {
>     Log.print("mouse inside sprite!")
>   }
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_material(entity : Entity, material : Material)"></endpoint>
<signature id="Sprite.set_material+2">Sprite.set_material(**entity**: `Entity`, **material**: `Material`)
<a class="headerlink" href="#Sprite.set_material+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Change the material that the `Sprite` attached to `entity` is drawn with, so it will draw with `material` instead.
> 
>   ```js
>   var material = Assets.material("luxe: material/logo.sprite")
>   Sprite.set_material(entity, material)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_material(entity : Entity)"></endpoint>
<signature id="Sprite.get_material">Sprite.get_material(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_material" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Material`
> Returns the current material that the `Sprite` attached to `entity` is drawn with.
> 
>   ```js
>   var material = Sprite.get_material(entity)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_image(entity : Entity, image : Image)"></endpoint>
<signature id="Sprite.set_image+2">Sprite.set_image(**entity**: `Entity`, **image**: `Image`)
<a class="headerlink" href="#Sprite.set_image+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Change the image that the `Sprite` attached to `entity` is drawn with.
> 
>   ```js
>   var image = Assets.image("luxe: image/logo.sprite")
>   Sprite.set_image(entity, image)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_image(entity : Entity)"></endpoint>
<signature id="Sprite.get_image">Sprite.get_image(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_image" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Image`
> Returns the current image that the `Sprite` attached to `entity` is drawn with.
> 
>   ```js
>   var image = Sprite.get_image(entity)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_origin(entity : Entity, x : Num, y : Num)"></endpoint>
<signature id="Sprite.set_origin+3">Sprite.set_origin(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
<a class="headerlink" href="#Sprite.set_origin+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Sets the origin of the sprite in relation to the `Transform` on `entity`. The `x` and `y` values are `0...1` range, where `0, 0` is bottom left, and `1, 1` is top right. A centered sprite is `0.5, 0.5`. To set the origin to the center, bottom you'd use `0.5, 0`.
> 
>   ```js
>   //centered
>   Sprite.set_origin(entity, 0.5, 0.5)
>   //bottom left
>   Sprite.set_origin(entity, 0, 0)
>   //bottom center
>   Sprite.set_origin(entity, 0.5, 0)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_origin(entity : Entity)"></endpoint>
<signature id="Sprite.get_origin">Sprite.get_origin(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_origin" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Float2`
> Returns the current origin for the Sprite attached to `entity`.
>         
>   ```js
>   var origin = Sprite.get_origin(entity)
>   Log.print(origin) //[0.5, 0.5]
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_flip_h(entity : Entity, flipped : Bool)"></endpoint>
<signature id="Sprite.set_flip_h+2">Sprite.set_flip_h(**entity**: `Entity`, **flipped**: `Bool`)
<a class="headerlink" href="#Sprite.set_flip_h+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set whether the `Sprite` attached to `entity` is `flipped` horizontally.
> 
>   ```js
>   Sprite.set_flip_h(entity, true)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_flip_h(entity : Entity)"></endpoint>
<signature id="Sprite.get_flip_h">Sprite.get_flip_h(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_flip_h" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if the `Sprite` attached to `entity` is flipped horizontally.
> 
>   ```js
>   var flipped = Sprite.get_flip_h(entity)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_flip_v(entity : Entity, flipped : Bool)"></endpoint>
<signature id="Sprite.set_flip_v+2">Sprite.set_flip_v(**entity**: `Entity`, **flipped**: `Bool`)
<a class="headerlink" href="#Sprite.set_flip_v+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set whether the `Sprite` attached to `entity` is `flipped` vertically.
> 
>   ```js
>   Sprite.set_flip_v(entity, true)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_flip_v(entity : Entity)"></endpoint>
<signature id="Sprite.get_flip_v">Sprite.get_flip_v(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_flip_v" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if the `Sprite` attached to `entity` is flipped vertically.
> 
>   ```js
>   var flipped = Sprite.get_flip_v(entity)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_billboard(entity : Entity, kind : SpriteBillboard, lock : Float3)"></endpoint>
<signature id="Sprite.set_billboard+3">Sprite.set_billboard(**entity**: `Entity`, **kind**: `SpriteBillboard`, **lock**: `Float3`)
<a class="headerlink" href="#Sprite.set_billboard+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set how the `Sprite` attached to `entity` behaves as a `billboard` sprite.
> The lock field is 0 for unlocked rotation, 1 for locked rotation on that axis.
> 
>   ```js
>   Sprite.set_billboard(entity, SpriteBillboard.fixed_scale, [0,1,0])
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_billboard(entity : Entity)"></endpoint>
<signature id="Sprite.get_billboard">Sprite.get_billboard(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_billboard" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js SpriteBillboard`
> Get how the `Sprite` attached to `entity` behaves as a `billboard` sprite.
> 
>   ```js
>   var kind = Sprite.get_billboard(entity)
>   if(kind == SpriteBillboard.fixed_scale) { ... }
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_size(entity : Entity, width : Num, height : Num)"></endpoint>
<signature id="Sprite.set_size+3">Sprite.set_size(**entity**: `Entity`, **width**: `Num`, **height**: `Num`)
<a class="headerlink" href="#Sprite.set_size+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Resize the `Sprite` attached to `entity` to be `width`x`height`.
> 
>   ```js
>   Sprite.set_size(entity, 256, 256)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_width(entity : Entity, width : Num)"></endpoint>
<signature id="Sprite.set_width+2">Sprite.set_width(**entity**: `Entity`, **width**: `Num`)
<a class="headerlink" href="#Sprite.set_width+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Resize the `Sprite` attached to `entity` to have a new `width`.
> 
>   ```js
>   Sprite.set_width(entity, 64)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_width(entity : Entity)"></endpoint>
<signature id="Sprite.get_width">Sprite.get_width(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_width" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Returns the width of the `Sprite` attached to `entity`.
> 
>   ```js
>   var width = Sprite.get_width(entity)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_height(entity : Entity, height : Num)"></endpoint>
<signature id="Sprite.set_height+2">Sprite.set_height(**entity**: `Entity`, **height**: `Num`)
<a class="headerlink" href="#Sprite.set_height+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Resize the `Sprite` attached to `entity` to have a new `height`.
> 
>   ```js
>   Sprite.set_height(entity, 64)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_height(entity : Entity)"></endpoint>
<signature id="Sprite.get_height">Sprite.get_height(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_height" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Returns the height of the `Sprite` attached to `entity`.
> 
>   ```js
>   var height = Sprite.get_height(entity)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_alpha(entity : Entity, alpha : Num)"></endpoint>
<signature id="Sprite.set_alpha+2">Sprite.set_alpha(**entity**: `Entity`, **alpha**: `Num`)
<a class="headerlink" href="#Sprite.set_alpha+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Change the alpha (transparency) of the `Sprite` attached to `entity` to be `alpha`. Modifies the color.
> 
>   ```js
>   Sprite.set_alpha(entity, 0.5)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_alpha(entity : Entity)"></endpoint>
<signature id="Sprite.get_alpha">Sprite.get_alpha(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_alpha" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Returns the current alpha of the `Sprite` attached to `entity`.
> 
>   ```js
>   var a = Sprite.get_alpha(entity)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_color(entity : Entity, color : Color)"></endpoint>
<signature id="Sprite.set_color+2">Sprite.set_color(**entity**: `Entity`, **color**: `Color`)
<a class="headerlink" href="#Sprite.set_color+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the color of the `Sprite` attached to `entity` to be a color. 
> The default color is white, `[1, 1, 1, 1]`, so to undo a color change, set it to that.
> 
>   ```js
>   var color = Color.hex(0xf6007c)
>   Sprite.set_color(entity, color)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_color(entity : Entity, r : Num, g : Num, b : Num, a : Num)"></endpoint>
<signature id="Sprite.set_color+5">Sprite.set_color(**entity**: `Entity`, **r**: `Num`, **g**: `Num`, **b**: `Num`, **a**: `Num`)
<a class="headerlink" href="#Sprite.set_color+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the color of the `Sprite` attached to `entity` to be a color of `r`,`g`,`b`,`a`. 
> The default color is white, `[1, 1, 1, 1]`, so to undo a color change, set it to that.
> 
>   ```js
>   Sprite.set_color(entity, r, g, b, a)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_color(entity : Entity)"></endpoint>
<signature id="Sprite.get_color">Sprite.get_color(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Color`
> Returns the current color of the `Sprite` attached to `entity`.
> 
>   ```js
>   var color = Sprite.get_color(entity)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_uv(entity : Entity, x0 : Num, y0 : Num, x1 : Num, y1 : Num)"></endpoint>
<signature id="Sprite.set_uv+5">Sprite.set_uv(**entity**: `Entity`, **x0**: `Num`, **y0**: `Num`, **x1**: `Num`, **y1**: `Num`)
<a class="headerlink" href="#Sprite.set_uv+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the UV coordinates for the `Sprite` attached to `entity` with top left at `x0`,`y0` and bottom right `x1`,`y1`. The default is `0, 0, 1, 1`, a full rectangle in UV coordinate space. If you want to tile the image on a sprite, set it to values > 1.
> 
>   ```js
>   //tile 4 times on both x and y
>   Sprite.set_uv(entity, 0, 0, 4, 4)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_uv(entity : Entity)"></endpoint>
<signature id="Sprite.get_uv">Sprite.get_uv(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_uv" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Float4`
> Returns the current uv of the `Sprite` attached to `entity`.
> 
>   ```js
>   var uv = Sprite.get_uv(entity)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_skew(entity : Entity, x : Num, y : Num)"></endpoint>
<signature id="Sprite.set_skew+3">Sprite.set_skew(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
<a class="headerlink" href="#Sprite.set_skew+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the skew amounts for the `Sprite` attached to `entity`. The values of `x` and `y` are between `0 ... 1`, where 1 is the most skew and 0 is none.
> 
>   ```js
>   Sprite.set_skew(entity, 0, 0.25)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_skew(entity : Entity)"></endpoint>
<signature id="Sprite.get_skew">Sprite.get_skew(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_skew" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Float2`
> Return the skew for the `Sprite` attached to `entity`.
> 
>   ```js
>   var skew = Sprite.get_skew(entity)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_geometry(entity : Entity)"></endpoint>
<signature id="Sprite.get_geometry">Sprite.get_geometry(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_geometry" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Geometry`
> Returns the render [Geometry](#geometry) for the `Sprite` attached to `entity`. The geometry is owned by the sprite, so be aware when modifying it.
> 
>   ```js
>   var geometry = Sprite.get_geometry(entity)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_geometry(entity : Entity, geo : Geometry)"></endpoint>
<signature id="Sprite.set_geometry+2">Sprite.set_geometry(**entity**: `Entity`, **geo**: `Geometry`)
<a class="headerlink" href="#Sprite.set_geometry+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Sets the render [Geometry](#geometry) for the `Sprite` attached to `entity`.
> 
>   ```js
>   Sprite.set_geometry(entity, geo)
>   ```   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_auto_size(entity : Entity)"></endpoint>
<signature id="Sprite.get_auto_size">Sprite.get_auto_size(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_auto_size" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_auto_size(entity : Entity, value : Bool)"></endpoint>
<signature id="Sprite.set_auto_size+2">Sprite.set_auto_size(**entity**: `Entity`, **value**: `Bool`)
<a class="headerlink" href="#Sprite.set_auto_size+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> When setting an image or material, resize the sprite to the image size   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_material_input(entity : Entity)"></endpoint>
<signature id="Sprite.get_material_input">Sprite.get_material_input(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_material_input" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_material_input(entity : Entity, value : Bool)"></endpoint>
<signature id="Sprite.set_material_input+2">Sprite.set_material_input(**entity**: `Entity`, **value**: `Bool`)
<a class="headerlink" href="#Sprite.set_material_input+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> For custom materials, the material input ID for the image.   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_hsv_adjust(entity : Entity)"></endpoint>
<signature id="Sprite.get_hsv_adjust">Sprite.get_hsv_adjust(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_hsv_adjust" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js HSV`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_hsv_adjust(entity : Entity, enabled : Bool, hue_change : Num, saturation : Num, value : Num)"></endpoint>
<signature id="Sprite.set_hsv_adjust+5">Sprite.set_hsv_adjust(**entity**: `Entity`, **enabled**: `Bool`, **hue_change**: `Num`, **saturation**: `Num`, **value**: `Num`)
<a class="headerlink" href="#Sprite.set_hsv_adjust+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the values for the hsv adjustment effect.
> The effect applies several operations on the colors of the sprite in sRGB HSV space.
> Saturation and Value changes are applied with exponents as `value ^ adjustment`.   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_effect_HSV_enabled(entity : Entity, enabled : Bool)"></endpoint>
<signature id="Sprite.set_effect_HSV_enabled+2">Sprite.set_effect_HSV_enabled(**entity**: `Entity`, **enabled**: `Bool`)
<a class="headerlink" href="#Sprite.set_effect_HSV_enabled+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_effect_HSV_enabled(entity : Entity, enabled : Bool)"></endpoint>
<signature id="Sprite.get_effect_HSV_enabled+2">Sprite.get_effect_HSV_enabled(**entity**: `Entity`, **enabled**: `Bool`)
<a class="headerlink" href="#Sprite.get_effect_HSV_enabled+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_effect_HSV_hue_change(entity : Entity, hue_change : Num)"></endpoint>
<signature id="Sprite.set_effect_HSV_hue_change+2">Sprite.set_effect_HSV_hue_change(**entity**: `Entity`, **hue_change**: `Num`)
<a class="headerlink" href="#Sprite.set_effect_HSV_hue_change+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_effect_HSV_hue_change(entity : Entity, hue_change : Num)"></endpoint>
<signature id="Sprite.get_effect_HSV_hue_change+2">Sprite.get_effect_HSV_hue_change(**entity**: `Entity`, **hue_change**: `Num`)
<a class="headerlink" href="#Sprite.get_effect_HSV_hue_change+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_effect_HSV_saturation(entity : Entity, saturation : Num)"></endpoint>
<signature id="Sprite.set_effect_HSV_saturation+2">Sprite.set_effect_HSV_saturation(**entity**: `Entity`, **saturation**: `Num`)
<a class="headerlink" href="#Sprite.set_effect_HSV_saturation+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_effect_HSV_saturation(entity : Entity, saturation : Num)"></endpoint>
<signature id="Sprite.get_effect_HSV_saturation+2">Sprite.get_effect_HSV_saturation(**entity**: `Entity`, **saturation**: `Num`)
<a class="headerlink" href="#Sprite.get_effect_HSV_saturation+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_effect_HSV_value(entity : Entity, value : Num)"></endpoint>
<signature id="Sprite.set_effect_HSV_value+2">Sprite.set_effect_HSV_value(**entity**: `Entity`, **value**: `Num`)
<a class="headerlink" href="#Sprite.set_effect_HSV_value+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_effect_HSV_value(entity : Entity, value : Num)"></endpoint>
<signature id="Sprite.get_effect_HSV_value+2">Sprite.get_effect_HSV_value(**entity**: `Entity`, **value**: `Num`)
<a class="headerlink" href="#Sprite.get_effect_HSV_value+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_outline(entity : Entity)"></endpoint>
<signature id="Sprite.get_outline">Sprite.get_outline(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_outline" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Outline`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_outline(entity : Entity, enabled : Bool, color : Color, thickness : Num)"></endpoint>
<signature id="Sprite.set_outline+4">Sprite.set_outline(**entity**: `Entity`, **enabled**: `Bool`, **color**: `Color`, **thickness**: `Num`)
<a class="headerlink" href="#Sprite.set_outline+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the values of the outline effect.   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_effect_outline_enabled(entity : Entity, enabled : Bool)"></endpoint>
<signature id="Sprite.set_effect_outline_enabled+2">Sprite.set_effect_outline_enabled(**entity**: `Entity`, **enabled**: `Bool`)
<a class="headerlink" href="#Sprite.set_effect_outline_enabled+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_effect_outline_enabled(entity : Entity, enabled : Bool)"></endpoint>
<signature id="Sprite.get_effect_outline_enabled+2">Sprite.get_effect_outline_enabled(**entity**: `Entity`, **enabled**: `Bool`)
<a class="headerlink" href="#Sprite.get_effect_outline_enabled+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_effect_outline_color(entity : Entity, color : Color)"></endpoint>
<signature id="Sprite.set_effect_outline_color+2">Sprite.set_effect_outline_color(**entity**: `Entity`, **color**: `Color`)
<a class="headerlink" href="#Sprite.set_effect_outline_color+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_effect_outline_color(entity : Entity, color : Color)"></endpoint>
<signature id="Sprite.get_effect_outline_color+2">Sprite.get_effect_outline_color(**entity**: `Entity`, **color**: `Color`)
<a class="headerlink" href="#Sprite.get_effect_outline_color+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_effect_outline_thickness(entity : Entity, thickness : Num)"></endpoint>
<signature id="Sprite.set_effect_outline_thickness+2">Sprite.set_effect_outline_thickness(**entity**: `Entity`, **thickness**: `Num`)
<a class="headerlink" href="#Sprite.set_effect_outline_thickness+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_effect_outline_thickness(entity : Entity, thickness : Num)"></endpoint>
<signature id="Sprite.get_effect_outline_thickness+2">Sprite.get_effect_outline_thickness(**entity**: `Entity`, **thickness**: `Num`)
<a class="headerlink" href="#Sprite.get_effect_outline_thickness+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_shadow(entity : Entity)"></endpoint>
<signature id="Sprite.get_shadow">Sprite.get_shadow(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_shadow" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Shadow`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_shadow(entity : Entity, enabled : Bool, offset : Num, color : Color, softness : Num)"></endpoint>
<signature id="Sprite.set_shadow+5">Sprite.set_shadow(**entity**: `Entity`, **enabled**: `Bool`, **offset**: `Num`, **color**: `Color`, **softness**: `Num`)
<a class="headerlink" href="#Sprite.set_shadow+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the values for the shadow effect.
> Shadows are the same color as the base sprite image, but only have a single color.   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_effect_shadow_enabled(entity : Entity, enabled : Bool)"></endpoint>
<signature id="Sprite.set_effect_shadow_enabled+2">Sprite.set_effect_shadow_enabled(**entity**: `Entity`, **enabled**: `Bool`)
<a class="headerlink" href="#Sprite.set_effect_shadow_enabled+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_effect_shadow_enabled(entity : Entity, enabled : Bool)"></endpoint>
<signature id="Sprite.get_effect_shadow_enabled+2">Sprite.get_effect_shadow_enabled(**entity**: `Entity`, **enabled**: `Bool`)
<a class="headerlink" href="#Sprite.get_effect_shadow_enabled+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_effect_shadow_offset(entity : Entity, offset : Vector2)"></endpoint>
<signature id="Sprite.set_effect_shadow_offset+2">Sprite.set_effect_shadow_offset(**entity**: `Entity`, **offset**: `Vector2`)
<a class="headerlink" href="#Sprite.set_effect_shadow_offset+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_effect_shadow_offset(entity : Entity, offset : Vector2)"></endpoint>
<signature id="Sprite.get_effect_shadow_offset+2">Sprite.get_effect_shadow_offset(**entity**: `Entity`, **offset**: `Vector2`)
<a class="headerlink" href="#Sprite.get_effect_shadow_offset+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_effect_shadow_color(entity : Entity, color : Color)"></endpoint>
<signature id="Sprite.set_effect_shadow_color+2">Sprite.set_effect_shadow_color(**entity**: `Entity`, **color**: `Color`)
<a class="headerlink" href="#Sprite.set_effect_shadow_color+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_effect_shadow_color(entity : Entity, color : Color)"></endpoint>
<signature id="Sprite.get_effect_shadow_color+2">Sprite.get_effect_shadow_color(**entity**: `Entity`, **color**: `Color`)
<a class="headerlink" href="#Sprite.get_effect_shadow_color+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_dissolve(entity : Entity)"></endpoint>
<signature id="Sprite.get_dissolve">Sprite.get_dissolve(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_dissolve" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Dissolve`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_dissolve(entity : Entity, enabled : Bool, image : Image, uv : List, value : Num)"></endpoint>
<signature id="Sprite.set_dissolve+5">Sprite.set_dissolve(**entity**: `Entity`, **enabled**: `Bool`, **image**: `Image`, **uv**: `List`, **value**: `Num`)
<a class="headerlink" href="#Sprite.set_dissolve+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the values for the hsv adjustment effect.
> The effect applies several operations on the colors of the sprite in sRGB HSV space.
> Saturation and Value changes are applied with exponents as `value ^ adjustment`.   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_effect_dissolve_enabled(entity : Entity, enabled : Bool)"></endpoint>
<signature id="Sprite.set_effect_dissolve_enabled+2">Sprite.set_effect_dissolve_enabled(**entity**: `Entity`, **enabled**: `Bool`)
<a class="headerlink" href="#Sprite.set_effect_dissolve_enabled+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_effect_dissolve_enabled(entity : Entity, enabled : Bool)"></endpoint>
<signature id="Sprite.get_effect_dissolve_enabled+2">Sprite.get_effect_dissolve_enabled(**entity**: `Entity`, **enabled**: `Bool`)
<a class="headerlink" href="#Sprite.get_effect_dissolve_enabled+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_effect_dissolve_image(entity : Entity, image : Image)"></endpoint>
<signature id="Sprite.set_effect_dissolve_image+2">Sprite.set_effect_dissolve_image(**entity**: `Entity`, **image**: `Image`)
<a class="headerlink" href="#Sprite.set_effect_dissolve_image+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_effect_dissolve_image(entity : Entity, image : Image)"></endpoint>
<signature id="Sprite.get_effect_dissolve_image+2">Sprite.get_effect_dissolve_image(**entity**: `Entity`, **image**: `Image`)
<a class="headerlink" href="#Sprite.get_effect_dissolve_image+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_effect_dissolve_uv(entity : Entity, uv : Vector4)"></endpoint>
<signature id="Sprite.set_effect_dissolve_uv+2">Sprite.set_effect_dissolve_uv(**entity**: `Entity`, **uv**: `Vector4`)
<a class="headerlink" href="#Sprite.set_effect_dissolve_uv+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_effect_dissolve_uv(entity : Entity, uv : Vector4)"></endpoint>
<signature id="Sprite.get_effect_dissolve_uv+2">Sprite.get_effect_dissolve_uv(**entity**: `Entity`, **uv**: `Vector4`)
<a class="headerlink" href="#Sprite.get_effect_dissolve_uv+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_effect_dissolve_value(entity : Entity, value : Num)"></endpoint>
<signature id="Sprite.set_effect_dissolve_value+2">Sprite.set_effect_dissolve_value(**entity**: `Entity`, **value**: `Num`)
<a class="headerlink" href="#Sprite.set_effect_dissolve_value+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_effect_dissolve_value(entity : Entity, value : Num)"></endpoint>
<signature id="Sprite.get_effect_dissolve_value+2">Sprite.get_effect_dissolve_value(**entity**: `Entity`, **value**: `Num`)
<a class="headerlink" href="#Sprite.get_effect_dissolve_value+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_shine(entity : Entity)"></endpoint>
<signature id="Sprite.get_shine">Sprite.get_shine(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_shine" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Shine`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_shine(entity : Entity, enabled : Bool, color : Num, direction : Vector2, width : Num, speed : Num, spacing : Num)"></endpoint>
<signature id="Sprite.set_shine+7">Sprite.set_shine(**entity**: `Entity`, **enabled**: `Bool`, **color**: `Num`, **direction**: `Vector2`, **width**: `Num`, **speed**: `Num`, **spacing**: `Num`)
<a class="headerlink" href="#Sprite.set_shine+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the values for the hsv adjustment effect.
> The effect applies several operations on the colors of the sprite in sRGB HSV space.
> Saturation and Value changes are applied with exponents as `value ^ adjustment`.   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_effect_shine_enabled(entity : Entity, enabled : Bool)"></endpoint>
<signature id="Sprite.set_effect_shine_enabled+2">Sprite.set_effect_shine_enabled(**entity**: `Entity`, **enabled**: `Bool`)
<a class="headerlink" href="#Sprite.set_effect_shine_enabled+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_effect_shine_enabled(entity : Entity, enabled : Bool)"></endpoint>
<signature id="Sprite.get_effect_shine_enabled+2">Sprite.get_effect_shine_enabled(**entity**: `Entity`, **enabled**: `Bool`)
<a class="headerlink" href="#Sprite.get_effect_shine_enabled+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_effect_shine_color(entity : Entity, color : Color)"></endpoint>
<signature id="Sprite.set_effect_shine_color+2">Sprite.set_effect_shine_color(**entity**: `Entity`, **color**: `Color`)
<a class="headerlink" href="#Sprite.set_effect_shine_color+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_effect_shine_color(entity : Entity, color : Color)"></endpoint>
<signature id="Sprite.get_effect_shine_color+2">Sprite.get_effect_shine_color(**entity**: `Entity`, **color**: `Color`)
<a class="headerlink" href="#Sprite.get_effect_shine_color+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_effect_shine_direction(entity : Entity, direction : Vector2)"></endpoint>
<signature id="Sprite.set_effect_shine_direction+2">Sprite.set_effect_shine_direction(**entity**: `Entity`, **direction**: `Vector2`)
<a class="headerlink" href="#Sprite.set_effect_shine_direction+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_effect_shine_direction(entity : Entity, direction : Vector2)"></endpoint>
<signature id="Sprite.get_effect_shine_direction+2">Sprite.get_effect_shine_direction(**entity**: `Entity`, **direction**: `Vector2`)
<a class="headerlink" href="#Sprite.get_effect_shine_direction+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_effect_shine_width(entity : Entity, width : Num)"></endpoint>
<signature id="Sprite.set_effect_shine_width+2">Sprite.set_effect_shine_width(**entity**: `Entity`, **width**: `Num`)
<a class="headerlink" href="#Sprite.set_effect_shine_width+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_effect_shine_width(entity : Entity, width : Num)"></endpoint>
<signature id="Sprite.get_effect_shine_width+2">Sprite.get_effect_shine_width(**entity**: `Entity`, **width**: `Num`)
<a class="headerlink" href="#Sprite.get_effect_shine_width+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_effect_shine_speed(entity : Entity, speed : Num)"></endpoint>
<signature id="Sprite.set_effect_shine_speed+2">Sprite.set_effect_shine_speed(**entity**: `Entity`, **speed**: `Num`)
<a class="headerlink" href="#Sprite.set_effect_shine_speed+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_effect_shine_speed(entity : Entity, speed : Num)"></endpoint>
<signature id="Sprite.get_effect_shine_speed+2">Sprite.get_effect_shine_speed(**entity**: `Entity`, **speed**: `Num`)
<a class="headerlink" href="#Sprite.get_effect_shine_speed+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="set_effect_shine_spacing(entity : Entity, spacing : Num)"></endpoint>
<signature id="Sprite.set_effect_shine_spacing+2">Sprite.set_effect_shine_spacing(**entity**: `Entity`, **spacing**: `Num`)
<a class="headerlink" href="#Sprite.set_effect_shine_spacing+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="Sprite" signature="get_effect_shine_spacing(entity : Entity, spacing : Num)"></endpoint>
<signature id="Sprite.get_effect_shine_spacing+2">Sprite.get_effect_shine_spacing(**entity**: `Entity`, **spacing**: `Num`)
<a class="headerlink" href="#Sprite.get_effect_shine_spacing+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

### SpriteBillboard
`:::js import "luxe: system/sprite.modifier" for SpriteBillboard`
> no docs found

- [none](#SpriteBillboard.none)
- [billboard](#SpriteBillboard.billboard)
- [fixed_scale](#SpriteBillboard.fixed_scale)
- [fixed_screen_scale](#SpriteBillboard.fixed_screen_scale)

<hr/>
<endpoint module="luxe: system/sprite.modifier" class="SpriteBillboard" signature="none"></endpoint>
<signature id="SpriteBillboard.none">SpriteBillboard.none
<a class="headerlink" href="#SpriteBillboard.none" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="SpriteBillboard" signature="billboard"></endpoint>
<signature id="SpriteBillboard.billboard">SpriteBillboard.billboard
<a class="headerlink" href="#SpriteBillboard.billboard" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="SpriteBillboard" signature="fixed_scale"></endpoint>
<signature id="SpriteBillboard.fixed_scale">SpriteBillboard.fixed_scale
<a class="headerlink" href="#SpriteBillboard.fixed_scale" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/sprite.modifier" class="SpriteBillboard" signature="fixed_screen_scale"></endpoint>
<signature id="SpriteBillboard.fixed_screen_scale">SpriteBillboard.fixed_screen_scale
<a class="headerlink" href="#SpriteBillboard.fixed_screen_scale" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### System
`:::js import "luxe: system/sprite.modifier" for System`
> no docs found

- [new](#System.new)(**world**: `World`)

<hr/>
<endpoint module="luxe: system/sprite.modifier" class="System" signature="new(world : World)"></endpoint>
<signature id="System.new">System.new(**world**: `World`)
<a class="headerlink" href="#System.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js System`
> no docs found   

