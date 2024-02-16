#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.11.1`)  


---

## `luxe: ui/color_picker` module

- [ColorPicker](#colorpicker)   
- [ColorPickerData](#colorpickerdata)   

---

### ColorPicker
`:::js import "luxe: ui/color_picker" for ColorPicker`
> no docs found

- [create](#ColorPicker.create)(**ui**: `Entity`)
- [set_color](#ColorPicker.set_color+2)(**control**: `Control`, **color**: `Color`)
- [get_color](#ColorPicker.get_color)(**control**: `Control`)
- [set_allow_hdr](#ColorPicker.set_allow_hdr+2)(**control**: `Control`, **allow**: `Bool`)

<hr/>
<endpoint module="luxe: ui/color_picker" class="ColorPicker" signature="create(ui : Entity)"></endpoint>
<signature id="ColorPicker.create">ColorPicker.create(**ui**: `Entity`)
<a class="headerlink" href="#ColorPicker.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Control`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPicker" signature="set_color(control : Control, color : Color)"></endpoint>
<signature id="ColorPicker.set_color+2">ColorPicker.set_color(**control**: `Control`, **color**: `Color`)
<a class="headerlink" href="#ColorPicker.set_color+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPicker" signature="get_color(control : Control)"></endpoint>
<signature id="ColorPicker.get_color">ColorPicker.get_color(**control**: `Control`)
<a class="headerlink" href="#ColorPicker.get_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Color`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPicker" signature="set_allow_hdr(control : Control, allow : Bool)"></endpoint>
<signature id="ColorPicker.set_allow_hdr+2">ColorPicker.set_allow_hdr(**control**: `Control`, **allow**: `Bool`)
<a class="headerlink" href="#ColorPicker.set_allow_hdr+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### ColorPickerData
`:::js import "luxe: ui/color_picker" for ColorPickerData`
> no docs found

- [triangle_size](#ColorPickerData.triangle_size)
- [outer_ring_size](#ColorPickerData.outer_ring_size)
- [inner_ring_size](#ColorPickerData.inner_ring_size)
- [r](#ColorPickerData.r)
- [g](#ColorPickerData.g)
- [b](#ColorPickerData.b)
- [h](#ColorPickerData.h)
- [s](#ColorPickerData.s)
- [v](#ColorPickerData.v)
- [a](#ColorPickerData.a)
- [color_ldr](#ColorPickerData.color_ldr)
- [color_hdr](#ColorPickerData.color_hdr)
- [srgb](#ColorPickerData.srgb)
- [srgb](#ColorPickerData.srgb=)=(value : Bool)
- [hdr_multiplier](#ColorPickerData.hdr_multiplier)
- [hdr_multiplier](#ColorPickerData.hdr_multiplier=)=(value : Num)
- [allow_hdr](#ColorPickerData.allow_hdr)
- [allow_hdr](#ColorPickerData.allow_hdr=)=(v : Bool)
- [show_hdr](#ColorPickerData.show_hdr)
- [show_hdr](#ColorPickerData.show_hdr=)=(v : Bool)
- [show_components](#ColorPickerData.show_components)
- [show_components](#ColorPickerData.show_components)(**v**: `String`)
- [debug](#ColorPickerData.debug=)=(v : Any)
- [new](#ColorPickerData.new+2)(**ui**: `Control`, **root**: `Control`)
- [set_allow_hdr](#ColorPickerData.set_allow_hdr)(**allow**: `Bool`)
- [set_color](#ColorPickerData.set_color)(**color**: `Color`)
- [get_rgba](#ColorPickerData.get_rgba)()
- [get_rgba](#ColorPickerData.get_rgba+2)(**srgb**: `Bool`, **hdr**: `Bool`)
- [get_hsva_component](#ColorPickerData.get_hsva_component)()
- [get_hsva](#ColorPickerData.get_hsva)(**srgb**: `Bool`)
- [set_rgba](#ColorPickerData.set_rgba)(**col**: `Color`)
- [set_rgba](#ColorPickerData.set_rgba+2)(**col**: `Color`, **srgb**: `Bool`)
- [set_rgba](#ColorPickerData.set_rgba+3)(**col**: `Color`, **srgb**: `Bool`, **update_spaces**: `Bool`)
- [set_hsva](#ColorPickerData.set_hsva)(**col**: `Any`)
- [set_hsva](#ColorPickerData.set_hsva+2)(**col**: `Color`, **srgb**: `Bool`)
- [set_hsva](#ColorPickerData.set_hsva+3)(**col**: `Color`, **srgb**: `Bool`, **update_spaces**: `Bool`)
- [set_rgba_component](#ColorPickerData.set_rgba_component+2)(**index**: `Num`, **value**: `Num`)
- [set_rgba_component](#ColorPickerData.set_rgba_component+3)(**index**: `Num`, **value**: `Num`, **srgb**: `Bool`)
- [get_rgba_component](#ColorPickerData.get_rgba_component)(**index**: `Num`)
- [get_rgba_component](#ColorPickerData.get_rgba_component+2)(**index**: `Num`, **srgb**: `Bool`)
- [get_rgba_component](#ColorPickerData.get_rgba_component+3)(**index**: `Num`, **srgb**: `Bool`, **hdr**: `Bool`)
- [set_hsva_component](#ColorPickerData.set_hsva_component+2)(**index**: `Num`, **value**: `Num`)
- [set_hsva_component](#ColorPickerData.set_hsva_component+3)(**index**: `Num`, **value**: `Num`, **srgb**: `Bool`)
- [get_hsva_component](#ColorPickerData.get_hsva_component)(**index**: `Num`)
- [get_hsva_component](#ColorPickerData.get_hsva_component+2)(**index**: `Num`, **srgb**: `Bool`)
- [create_colorpicker](#ColorPickerData.create_colorpicker+2)(**ui**: `Entity`, **color_view**: `Control`)
- [hdr_settings](#ColorPickerData.hdr_settings+2)(**ui**: `UI`, **data_control**: `Control`)
- [color_display](#ColorPickerData.color_display+2)(**ui**: `UI`, **data_control**: `Control`)
- [colorspace_choice](#ColorPickerData.colorspace_choice+2)(**ui**: `Any`, **data_control**: `Any`)
- [hex_input](#ColorPickerData.hex_input+2)(**ui**: `UI`, **data_control**: `Control`)
- [rgba_values](#ColorPickerData.rgba_values+2)(**ui**: `UI`, **color_view**: `Control`)
- [hsva_values](#ColorPickerData.hsva_values+2)(**ui**: `UI`, **color_view**: `Control`)
- [color_component](#ColorPickerData.color_component+5)(**ui**: `Entity`, **name**: `String`, **index**: `Num`, **color_view**: `Control`, **space**: `String`)
- [create_hsv_wheel](#ColorPickerData.create_hsv_wheel+2)(**ui**: `Entity`, **data_root**: `Control`)

<hr/>
<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="triangle_size"></endpoint>
<signature id="ColorPickerData.triangle_size">ColorPickerData.triangle_size
<a class="headerlink" href="#ColorPickerData.triangle_size" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="outer_ring_size"></endpoint>
<signature id="ColorPickerData.outer_ring_size">ColorPickerData.outer_ring_size
<a class="headerlink" href="#ColorPickerData.outer_ring_size" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="inner_ring_size"></endpoint>
<signature id="ColorPickerData.inner_ring_size">ColorPickerData.inner_ring_size
<a class="headerlink" href="#ColorPickerData.inner_ring_size" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="r"></endpoint>
<signature id="ColorPickerData.r">ColorPickerData.r
<a class="headerlink" href="#ColorPickerData.r" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="g"></endpoint>
<signature id="ColorPickerData.g">ColorPickerData.g
<a class="headerlink" href="#ColorPickerData.g" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="b"></endpoint>
<signature id="ColorPickerData.b">ColorPickerData.b
<a class="headerlink" href="#ColorPickerData.b" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="h"></endpoint>
<signature id="ColorPickerData.h">ColorPickerData.h
<a class="headerlink" href="#ColorPickerData.h" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="s"></endpoint>
<signature id="ColorPickerData.s">ColorPickerData.s
<a class="headerlink" href="#ColorPickerData.s" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="v"></endpoint>
<signature id="ColorPickerData.v">ColorPickerData.v
<a class="headerlink" href="#ColorPickerData.v" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="a"></endpoint>
<signature id="ColorPickerData.a">ColorPickerData.a
<a class="headerlink" href="#ColorPickerData.a" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="color_ldr"></endpoint>
<signature id="ColorPickerData.color_ldr">ColorPickerData.color_ldr
<a class="headerlink" href="#ColorPickerData.color_ldr" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Color`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="color_hdr"></endpoint>
<signature id="ColorPickerData.color_hdr">ColorPickerData.color_hdr
<a class="headerlink" href="#ColorPickerData.color_hdr" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Color`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="srgb"></endpoint>
<signature id="ColorPickerData.srgb">ColorPickerData.srgb
<a class="headerlink" href="#ColorPickerData.srgb" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="srgb=(value : Bool)"></endpoint>
<signature id="ColorPickerData.srgb=">ColorPickerData.srgb=(value : Bool)
<a class="headerlink" href="#ColorPickerData.srgb=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="hdr_multiplier"></endpoint>
<signature id="ColorPickerData.hdr_multiplier">ColorPickerData.hdr_multiplier
<a class="headerlink" href="#ColorPickerData.hdr_multiplier" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="hdr_multiplier=(value : Num)"></endpoint>
<signature id="ColorPickerData.hdr_multiplier=">ColorPickerData.hdr_multiplier=(value : Num)
<a class="headerlink" href="#ColorPickerData.hdr_multiplier=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="allow_hdr"></endpoint>
<signature id="ColorPickerData.allow_hdr">ColorPickerData.allow_hdr
<a class="headerlink" href="#ColorPickerData.allow_hdr" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="allow_hdr=(v : Bool)"></endpoint>
<signature id="ColorPickerData.allow_hdr=">ColorPickerData.allow_hdr=(v : Bool)
<a class="headerlink" href="#ColorPickerData.allow_hdr=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="show_hdr"></endpoint>
<signature id="ColorPickerData.show_hdr">ColorPickerData.show_hdr
<a class="headerlink" href="#ColorPickerData.show_hdr" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="show_hdr=(v : Bool)"></endpoint>
<signature id="ColorPickerData.show_hdr=">ColorPickerData.show_hdr=(v : Bool)
<a class="headerlink" href="#ColorPickerData.show_hdr=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="show_components"></endpoint>
<signature id="ColorPickerData.show_components">ColorPickerData.show_components
<a class="headerlink" href="#ColorPickerData.show_components" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="show_components(v : String)"></endpoint>
<signature id="ColorPickerData.show_components">ColorPickerData.show_components(**v**: `String`)
<a class="headerlink" href="#ColorPickerData.show_components" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="debug=(v : Any)"></endpoint>
<signature id="ColorPickerData.debug=">ColorPickerData.debug=(v : Any)
<a class="headerlink" href="#ColorPickerData.debug=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="new(ui : Control, root : Control)"></endpoint>
<signature id="ColorPickerData.new+2">ColorPickerData.new(**ui**: `Control`, **root**: `Control`)
<a class="headerlink" href="#ColorPickerData.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js ColorPickerData`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="set_allow_hdr(allow : Bool)"></endpoint>
<signature id="ColorPickerData.set_allow_hdr">ColorPickerData.set_allow_hdr(**allow**: `Bool`)
<a class="headerlink" href="#ColorPickerData.set_allow_hdr" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="set_color(color : Color)"></endpoint>
<signature id="ColorPickerData.set_color">ColorPickerData.set_color(**color**: `Color`)
<a class="headerlink" href="#ColorPickerData.set_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="get_rgba()"></endpoint>
<signature id="ColorPickerData.get_rgba">ColorPickerData.get_rgba()
<a class="headerlink" href="#ColorPickerData.get_rgba" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Color`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="get_rgba(srgb : Bool, hdr : Bool)"></endpoint>
<signature id="ColorPickerData.get_rgba+2">ColorPickerData.get_rgba(**srgb**: `Bool`, **hdr**: `Bool`)
<a class="headerlink" href="#ColorPickerData.get_rgba+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Color`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="get_hsva_component()"></endpoint>
<signature id="ColorPickerData.get_hsva_component">ColorPickerData.get_hsva_component()
<a class="headerlink" href="#ColorPickerData.get_hsva_component" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Color`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="get_hsva(srgb : Bool)"></endpoint>
<signature id="ColorPickerData.get_hsva">ColorPickerData.get_hsva(**srgb**: `Bool`)
<a class="headerlink" href="#ColorPickerData.get_hsva" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Color`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="set_rgba(col : Color)"></endpoint>
<signature id="ColorPickerData.set_rgba">ColorPickerData.set_rgba(**col**: `Color`)
<a class="headerlink" href="#ColorPickerData.set_rgba" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="set_rgba(col : Color, srgb : Bool)"></endpoint>
<signature id="ColorPickerData.set_rgba+2">ColorPickerData.set_rgba(**col**: `Color`, **srgb**: `Bool`)
<a class="headerlink" href="#ColorPickerData.set_rgba+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="set_rgba(col : Color, srgb : Bool, update_spaces : Bool)"></endpoint>
<signature id="ColorPickerData.set_rgba+3">ColorPickerData.set_rgba(**col**: `Color`, **srgb**: `Bool`, **update_spaces**: `Bool`)
<a class="headerlink" href="#ColorPickerData.set_rgba+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="set_hsva(col : Any)"></endpoint>
<signature id="ColorPickerData.set_hsva">ColorPickerData.set_hsva(**col**: `Any`)
<a class="headerlink" href="#ColorPickerData.set_hsva" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="set_hsva(col : Color, srgb : Bool)"></endpoint>
<signature id="ColorPickerData.set_hsva+2">ColorPickerData.set_hsva(**col**: `Color`, **srgb**: `Bool`)
<a class="headerlink" href="#ColorPickerData.set_hsva+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="set_hsva(col : Color, srgb : Bool, update_spaces : Bool)"></endpoint>
<signature id="ColorPickerData.set_hsva+3">ColorPickerData.set_hsva(**col**: `Color`, **srgb**: `Bool`, **update_spaces**: `Bool`)
<a class="headerlink" href="#ColorPickerData.set_hsva+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="set_rgba_component(index : Num, value : Num)"></endpoint>
<signature id="ColorPickerData.set_rgba_component+2">ColorPickerData.set_rgba_component(**index**: `Num`, **value**: `Num`)
<a class="headerlink" href="#ColorPickerData.set_rgba_component+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="set_rgba_component(index : Num, value : Num, srgb : Bool)"></endpoint>
<signature id="ColorPickerData.set_rgba_component+3">ColorPickerData.set_rgba_component(**index**: `Num`, **value**: `Num`, **srgb**: `Bool`)
<a class="headerlink" href="#ColorPickerData.set_rgba_component+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="get_rgba_component(index : Num)"></endpoint>
<signature id="ColorPickerData.get_rgba_component">ColorPickerData.get_rgba_component(**index**: `Num`)
<a class="headerlink" href="#ColorPickerData.get_rgba_component" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="get_rgba_component(index : Num, srgb : Bool)"></endpoint>
<signature id="ColorPickerData.get_rgba_component+2">ColorPickerData.get_rgba_component(**index**: `Num`, **srgb**: `Bool`)
<a class="headerlink" href="#ColorPickerData.get_rgba_component+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="get_rgba_component(index : Num, srgb : Bool, hdr : Bool)"></endpoint>
<signature id="ColorPickerData.get_rgba_component+3">ColorPickerData.get_rgba_component(**index**: `Num`, **srgb**: `Bool`, **hdr**: `Bool`)
<a class="headerlink" href="#ColorPickerData.get_rgba_component+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="set_hsva_component(index : Num, value : Num)"></endpoint>
<signature id="ColorPickerData.set_hsva_component+2">ColorPickerData.set_hsva_component(**index**: `Num`, **value**: `Num`)
<a class="headerlink" href="#ColorPickerData.set_hsva_component+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="set_hsva_component(index : Num, value : Num, srgb : Bool)"></endpoint>
<signature id="ColorPickerData.set_hsva_component+3">ColorPickerData.set_hsva_component(**index**: `Num`, **value**: `Num`, **srgb**: `Bool`)
<a class="headerlink" href="#ColorPickerData.set_hsva_component+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="get_hsva_component(index : Num)"></endpoint>
<signature id="ColorPickerData.get_hsva_component">ColorPickerData.get_hsva_component(**index**: `Num`)
<a class="headerlink" href="#ColorPickerData.get_hsva_component" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="get_hsva_component(index : Num, srgb : Bool)"></endpoint>
<signature id="ColorPickerData.get_hsva_component+2">ColorPickerData.get_hsva_component(**index**: `Num`, **srgb**: `Bool`)
<a class="headerlink" href="#ColorPickerData.get_hsva_component+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="create_colorpicker(ui : Entity, color_view : Control)"></endpoint>
<signature id="ColorPickerData.create_colorpicker+2">ColorPickerData.create_colorpicker(**ui**: `Entity`, **color_view**: `Control`)
<a class="headerlink" href="#ColorPickerData.create_colorpicker+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="hdr_settings(ui : UI, data_control : Control)"></endpoint>
<signature id="ColorPickerData.hdr_settings+2">ColorPickerData.hdr_settings(**ui**: `UI`, **data_control**: `Control`)
<a class="headerlink" href="#ColorPickerData.hdr_settings+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="color_display(ui : UI, data_control : Control)"></endpoint>
<signature id="ColorPickerData.color_display+2">ColorPickerData.color_display(**ui**: `UI`, **data_control**: `Control`)
<a class="headerlink" href="#ColorPickerData.color_display+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="colorspace_choice(ui : Any, data_control : Any)"></endpoint>
<signature id="ColorPickerData.colorspace_choice+2">ColorPickerData.colorspace_choice(**ui**: `Any`, **data_control**: `Any`)
<a class="headerlink" href="#ColorPickerData.colorspace_choice+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="hex_input(ui : UI, data_control : Control)"></endpoint>
<signature id="ColorPickerData.hex_input+2">ColorPickerData.hex_input(**ui**: `UI`, **data_control**: `Control`)
<a class="headerlink" href="#ColorPickerData.hex_input+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="rgba_values(ui : UI, color_view : Control)"></endpoint>
<signature id="ColorPickerData.rgba_values+2">ColorPickerData.rgba_values(**ui**: `UI`, **color_view**: `Control`)
<a class="headerlink" href="#ColorPickerData.rgba_values+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="hsva_values(ui : UI, color_view : Control)"></endpoint>
<signature id="ColorPickerData.hsva_values+2">ColorPickerData.hsva_values(**ui**: `UI`, **color_view**: `Control`)
<a class="headerlink" href="#ColorPickerData.hsva_values+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="color_component(ui : Entity, name : String, index : Num, color_view : Control, space : String)"></endpoint>
<signature id="ColorPickerData.color_component+5">ColorPickerData.color_component(**ui**: `Entity`, **name**: `String`, **index**: `Num`, **color_view**: `Control`, **space**: `String`)
<a class="headerlink" href="#ColorPickerData.color_component+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/color_picker" class="ColorPickerData" signature="create_hsv_wheel(ui : Entity, data_root : Control)"></endpoint>
<signature id="ColorPickerData.create_hsv_wheel+2">ColorPickerData.create_hsv_wheel(**ui**: `Entity`, **data_root**: `Control`)
<a class="headerlink" href="#ColorPickerData.create_hsv_wheel+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Control`
> no docs found   

