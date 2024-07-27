#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.11.1`)  


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
- [System](#system)   

---

### Advanced
`:::js import "luxe: system/sprite.modifier" for Advanced`
> no docs found


<hr/>
### Data
`:::js import "luxe: system/sprite.modifier" for Data`
> no docs found


<hr/>
### Dissolve
`:::js import "luxe: system/sprite.modifier" for Dissolve`
> no docs found


<hr/>
### HSV
`:::js import "luxe: system/sprite.modifier" for HSV`
> no docs found


<hr/>
### Outline
`:::js import "luxe: system/sprite.modifier" for Outline`
> no docs found


<hr/>
### Shadow
`:::js import "luxe: system/sprite.modifier" for Shadow`
> no docs found


<hr/>
### Shine
`:::js import "luxe: system/sprite.modifier" for Shine`
> no docs found


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
- [create_with](#Sprite.create_with+4)(**entity**: `Entity`, **material**: `Material`, **width**: `Num`, **height**: `Num`)
- [create_with](#Sprite.create_with+2)(**entity**: `Entity`, **material**: `Material`)
- [create](#Sprite.create+3)(**entity**: `Entity`, **atlas**: `Atlas`, **atlas_image**: `String`)
- [destroy](#Sprite.destroy)(**entity**: `Entity`)
- [has](#Sprite.has)(**entity**: `Entity`)
- [contains](#Sprite.contains+3)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
- [set_material](#Sprite.set_material+2)(**entity**: `Entity`, **material**: `Material`)
- [get_material](#Sprite.get_material)(**entity**: `Entity`)
- [set_origin](#Sprite.set_origin+3)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
- [get_origin](#Sprite.get_origin)(**entity**: `Entity`)
- [set_flip_h](#Sprite.set_flip_h+2)(**entity**: `Entity`, **flipped**: `Bool`)
- [get_flip_h](#Sprite.get_flip_h)(**entity**: `Entity`)
- [set_flip_v](#Sprite.set_flip_v+2)(**entity**: `Entity`, **flipped**: `Bool`)
- [get_flip_v](#Sprite.get_flip_v)(**entity**: `Entity`)
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

