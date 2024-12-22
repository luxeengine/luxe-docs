#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2024.12.4`)  


---

## `luxe: ui/image` module

- [UIImage](#uiimage)   

---

### UIImage
`:::js import "luxe: ui/image" for UIImage`
> `UIImage` is a type of `Control` made to display images.
> 
> ```js
>   var image = UIImage.create(ui)
>   UIImage.set_image(image, Assets.image("path/to/image"))
>   //setup positioning etc with `Control.___`
> ```

- [create](#UIImage.create)(**ui_entity**: `Entity`)
- [set_image](#UIImage.set_image+2)(**control**: `UIImage`, **image**: `Image`)
- [set_image](#UIImage.set_image+3)(**control**: `UIImage`, **image**: `Image`, **flags**: `UIImageFlags`)
- [get_image](#UIImage.get_image)(**control**: `UIImage`)
- [set_material](#UIImage.set_material+2)(**control**: `UIImage`, **material**: `Material`)
- [set_uv](#UIImage.set_uv+5)(**control**: `UIImage`, **left**: `Num`, **top**: `Num`, **right**: `Num`, **bottom**: `Num`)
- [set_color](#UIImage.set_color+2)(**control**: `UIImage`, **color**: `Color`)
- [get_color](#UIImage.get_color)(**control**: `UIImage`)
- [set_angle](#UIImage.set_angle+2)(**control**: `UIImage`, **degrees**: `Num`)

<hr/>
<endpoint module="luxe: ui/image" class="UIImage" signature="create(ui_entity : Entity)"></endpoint>
<signature id="UIImage.create">UIImage.create(**ui_entity**: `Entity`)
<a class="headerlink" href="#UIImage.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js UIImage`
> Create a new UIImage control.   

<endpoint module="luxe: ui/image" class="UIImage" signature="set_image(control : UIImage, image : Image)"></endpoint>
<signature id="UIImage.set_image+2">UIImage.set_image(**control**: `UIImage`, **image**: `Image`)
<a class="headerlink" href="#UIImage.set_image+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set image of `UIImage` control (uses `UIImageFlags.none` with linear interpolation).
> Setting an image will reset any set custom material and use an internal material created from the `luxe: material_basis/ui_solid` basis instead.   

<endpoint module="luxe: ui/image" class="UIImage" signature="set_image(control : UIImage, image : Image, flags : UIImageFlags)"></endpoint>
<signature id="UIImage.set_image+3">UIImage.set_image(**control**: `UIImage`, **image**: `Image`, **flags**: `UIImageFlags`)
<a class="headerlink" href="#UIImage.set_image+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set displayed image of `UIImage` control.
> The flags determine what sampler is used to read the image.
> Setting an image will reset any set custom material and use an internal material created from the `luxe: material_basis/ui_solid` basis instead.
> ```js
>   var image = UIImage.create(ui)
>   UIImage.set_image(image, Assets.image("path/to/image"), UIImageFlags.pixelated)
> ```   

<endpoint module="luxe: ui/image" class="UIImage" signature="get_image(control : UIImage)"></endpoint>
<signature id="UIImage.get_image">UIImage.get_image(**control**: `UIImage`)
<a class="headerlink" href="#UIImage.get_image" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Image`
> Get currently displayed image of `UIImage`.   

<endpoint module="luxe: ui/image" class="UIImage" signature="set_material(control : UIImage, material : Material)"></endpoint>
<signature id="UIImage.set_material+2">UIImage.set_material(**control**: `UIImage`, **material**: `Material`)
<a class="headerlink" href="#UIImage.set_material+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the material used to render the `UIImage`.
> Setting a custom material will reset the controls image, so you need to author that via the inputs on your material.   

<endpoint module="luxe: ui/image" class="UIImage" signature="set_uv(control : UIImage, left : Num, top : Num, right : Num, bottom : Num)"></endpoint>
<signature id="UIImage.set_uv+5">UIImage.set_uv(**control**: `UIImage`, **left**: `Num`, **top**: `Num`, **right**: `Num`, **bottom**: `Num`)
<a class="headerlink" href="#UIImage.set_uv+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the uv bounds, default is (0, 0, 1, 1). Drawing only top left of the image would be (0.5, 0.5, 1, 1).   

<endpoint module="luxe: ui/image" class="UIImage" signature="set_color(control : UIImage, color : Color)"></endpoint>
<signature id="UIImage.set_color+2">UIImage.set_color(**control**: `UIImage`, **color**: `Color`)
<a class="headerlink" href="#UIImage.set_color+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the tint color of the `UIImage`. Communicated to the shader via vertex colors.   

<endpoint module="luxe: ui/image" class="UIImage" signature="get_color(control : UIImage)"></endpoint>
<signature id="UIImage.get_color">UIImage.get_color(**control**: `UIImage`)
<a class="headerlink" href="#UIImage.get_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Color`
> Get the current tint color of the `UIImage`.   

<endpoint module="luxe: ui/image" class="UIImage" signature="set_angle(control : UIImage, degrees : Num)"></endpoint>
<signature id="UIImage.set_angle+2">UIImage.set_angle(**control**: `UIImage`, **degrees**: `Num`)
<a class="headerlink" href="#UIImage.set_angle+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Get the angle of the `UIImage` control. Note that this will not affect child controls.   

