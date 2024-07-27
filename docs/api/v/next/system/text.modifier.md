#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.11.1`)  


---

## `luxe: system/text.modifier` module

- [Data](#data)   
- [System](#system)   
- [Text](#text)   
- [TextAlignH](#textalignh)   
- [TextAlignV](#textalignv)   

---

### Data
`:::js import "luxe: system/text.modifier" for Data`
> no docs found


<hr/>
### System
`:::js import "luxe: system/text.modifier" for System`
> no docs found

- [new](#System.new)(**world**: `World`)

<hr/>
<endpoint module="luxe: system/text.modifier" class="System" signature="new(world : World)"></endpoint>
<signature id="System.new">System.new(**world**: `World`)
<a class="headerlink" href="#System.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js System`
> no docs found   

### Text
`:::js import "luxe: system/text.modifier" for Text`
> no docs found

- [create](#Text.create+5)(**entity**: `Any`, **material**: `Any`, **default_size**: `Any`, **default_font**: `Any`, **default_color**: `Any`)
- [destroy](#Text.destroy)(**entity**: `Any`)
- [set_size](#Text.set_size+2)(**entity**: `Any`, **default_size**: `Any`)
- [get_size](#Text.get_size)(**entity**: `Any`)
- [set_font](#Text.set_font+2)(**entity**: `Any`, **default_font**: `Any`)
- [get_font](#Text.get_font)(**entity**: `Any`)
- [set_style](#Text.set_style+2)(**entity**: `Entity`, **style**: `TextStyle`)
- [get_style](#Text.get_style)(**entity**: `Entity`)
- [set_outline](#Text.set_outline+5)(**entity**: `Entity`, **radius**: `Num`, **softness**: `Num`, **color**: `Color`, **offset**: `Float2`)
- [set_shadow](#Text.set_shadow+5)(**entity**: `Entity`, **radius**: `Num`, **softness**: `Num`, **color**: `Color`, **offset**: `Float2`)
- [set_max_visible](#Text.set_max_visible+2)(**entity**: `Entity`, **max_visible**: `Num`)
- [get_max_visible](#Text.get_max_visible)(**entity**: `Entity`)
- [set_color](#Text.set_color+2)(**entity**: `Any`, **default_color**: `Any`)
- [get_color](#Text.get_color)(**entity**: `Any`)
- [set_align](#Text.set_align+3)(**entity**: `Any`, **align**: `Any`, **align_vertical**: `Any`)
- [set_align](#Text.set_align+2)(**entity**: `Any`, **align**: `Any`)
- [get_align](#Text.get_align)(**entity**: `Any`)
- [set_align_vertical](#Text.set_align_vertical+2)(**entity**: `Any`, **align_vertical**: `Any`)
- [get_align_vertical](#Text.get_align_vertical)(**entity**: `Any`)
- [set_bounds](#Text.set_bounds+5)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`)
- [get_bounds](#Text.get_bounds)(**entity**: `Any`)
- [set_attr](#Text.set_attr+6)(**entity**: `Entity`, **start**: `Num`, **length**: `Num`, **type**: `TextAttrType`, **key**: `String`, **value**: `Any`)
- [attr_clear](#Text.attr_clear)(**entity**: `Any`)
- [commit](#Text.commit)(**entity**: `Any`)
- [get_render_text](#Text.get_render_text)(**entity**: `Any`)
- [get_geometry](#Text.get_geometry)(**entity**: `Any`)
- [get_extents](#Text.get_extents+3)(**entity**: `Any`, **offset**: `Any`, **count**: `Any`)
- [get_extents](#Text.get_extents)(**entity**: `Any`)
- [contains](#Text.contains+3)(**entity**: `Any`, **x**: `Any`, **y**: `Any`)
- [has](#Text.has)(**entity**: `Any`)
- [set_loc](#Text.set_loc+3)(**entity**: `Entity`, **space**: `String`, **key**: `String`)
- [set_loc](#Text.set_loc+2)(**entity**: `Entity`, **key**: `String`)
- [set_loc_with_args](#Text.set_loc_with_args+4)(**entity**: `Entity`, **space**: `String`, **key**: `String`, **args**: `List`)
- [set_loc_with_args](#Text.set_loc_with_args+3)(**entity**: `Entity`, **key**: `String`, **args**: `List`)
- [get_text](#Text.get_text)(**entity**: `Any`)
- [set_text_buffer](#Text.set_text_buffer+2)(**entity**: `Any`, **string**: `Any`)
- [set_text](#Text.set_text+2)(**entity**: `Any`, **string**: `Any`)

<hr/>
<endpoint module="luxe: system/text.modifier" class="Text" signature="create(entity : Any, material : Any, default_size : Any, default_font : Any, default_color : Any)"></endpoint>
<signature id="Text.create+5">Text.create(**entity**: `Any`, **material**: `Any`, **default_size**: `Any`, **default_font**: `Any`, **default_color**: `Any`)
<a class="headerlink" href="#Text.create+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="destroy(entity : Any)"></endpoint>
<signature id="Text.destroy">Text.destroy(**entity**: `Any`)
<a class="headerlink" href="#Text.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="set_size(entity : Any, default_size : Any)"></endpoint>
<signature id="Text.set_size+2">Text.set_size(**entity**: `Any`, **default_size**: `Any`)
<a class="headerlink" href="#Text.set_size+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="get_size(entity : Any)"></endpoint>
<signature id="Text.get_size">Text.get_size(**entity**: `Any`)
<a class="headerlink" href="#Text.get_size" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="set_font(entity : Any, default_font : Any)"></endpoint>
<signature id="Text.set_font+2">Text.set_font(**entity**: `Any`, **default_font**: `Any`)
<a class="headerlink" href="#Text.set_font+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="get_font(entity : Any)"></endpoint>
<signature id="Text.get_font">Text.get_font(**entity**: `Any`)
<a class="headerlink" href="#Text.get_font" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="set_style(entity : Entity, style : TextStyle)"></endpoint>
<signature id="Text.set_style+2">Text.set_style(**entity**: `Entity`, **style**: `TextStyle`)
<a class="headerlink" href="#Text.set_style+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="get_style(entity : Entity)"></endpoint>
<signature id="Text.get_style">Text.get_style(**entity**: `Entity`)
<a class="headerlink" href="#Text.get_style" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js TextStyle`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="set_outline(entity : Entity, radius : Num, softness : Num, color : Color, offset : Float2)"></endpoint>
<signature id="Text.set_outline+5">Text.set_outline(**entity**: `Entity`, **radius**: `Num`, **softness**: `Num`, **color**: `Color`, **offset**: `Float2`)
<a class="headerlink" href="#Text.set_outline+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="set_shadow(entity : Entity, radius : Num, softness : Num, color : Color, offset : Float2)"></endpoint>
<signature id="Text.set_shadow+5">Text.set_shadow(**entity**: `Entity`, **radius**: `Num`, **softness**: `Num`, **color**: `Color`, **offset**: `Float2`)
<a class="headerlink" href="#Text.set_shadow+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="set_max_visible(entity : Entity, max_visible : Num)"></endpoint>
<signature id="Text.set_max_visible+2">Text.set_max_visible(**entity**: `Entity`, **max_visible**: `Num`)
<a class="headerlink" href="#Text.set_max_visible+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="get_max_visible(entity : Entity)"></endpoint>
<signature id="Text.get_max_visible">Text.get_max_visible(**entity**: `Entity`)
<a class="headerlink" href="#Text.get_max_visible" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="set_color(entity : Any, default_color : Any)"></endpoint>
<signature id="Text.set_color+2">Text.set_color(**entity**: `Any`, **default_color**: `Any`)
<a class="headerlink" href="#Text.set_color+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="get_color(entity : Any)"></endpoint>
<signature id="Text.get_color">Text.get_color(**entity**: `Any`)
<a class="headerlink" href="#Text.get_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="set_align(entity : Any, align : Any, align_vertical : Any)"></endpoint>
<signature id="Text.set_align+3">Text.set_align(**entity**: `Any`, **align**: `Any`, **align_vertical**: `Any`)
<a class="headerlink" href="#Text.set_align+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="set_align(entity : Any, align : Any)"></endpoint>
<signature id="Text.set_align+2">Text.set_align(**entity**: `Any`, **align**: `Any`)
<a class="headerlink" href="#Text.set_align+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="get_align(entity : Any)"></endpoint>
<signature id="Text.get_align">Text.get_align(**entity**: `Any`)
<a class="headerlink" href="#Text.get_align" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="set_align_vertical(entity : Any, align_vertical : Any)"></endpoint>
<signature id="Text.set_align_vertical+2">Text.set_align_vertical(**entity**: `Any`, **align_vertical**: `Any`)
<a class="headerlink" href="#Text.set_align_vertical+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="get_align_vertical(entity : Any)"></endpoint>
<signature id="Text.get_align_vertical">Text.get_align_vertical(**entity**: `Any`)
<a class="headerlink" href="#Text.get_align_vertical" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="set_bounds(entity : Any, x : Any, y : Any, w : Any, h : Any)"></endpoint>
<signature id="Text.set_bounds+5">Text.set_bounds(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`)
<a class="headerlink" href="#Text.set_bounds+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="get_bounds(entity : Any)"></endpoint>
<signature id="Text.get_bounds">Text.get_bounds(**entity**: `Any`)
<a class="headerlink" href="#Text.get_bounds" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="set_attr(entity : Entity, start : Num, length : Num, type : TextAttrType, key : String, value : Any)"></endpoint>
<signature id="Text.set_attr+6">Text.set_attr(**entity**: `Entity`, **start**: `Num`, **length**: `Num`, **type**: `TextAttrType`, **key**: `String`, **value**: `Any`)
<a class="headerlink" href="#Text.set_attr+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="attr_clear(entity : Any)"></endpoint>
<signature id="Text.attr_clear">Text.attr_clear(**entity**: `Any`)
<a class="headerlink" href="#Text.attr_clear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="commit(entity : Any)"></endpoint>
<signature id="Text.commit">Text.commit(**entity**: `Any`)
<a class="headerlink" href="#Text.commit" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="get_render_text(entity : Any)"></endpoint>
<signature id="Text.get_render_text">Text.get_render_text(**entity**: `Any`)
<a class="headerlink" href="#Text.get_render_text" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="get_geometry(entity : Any)"></endpoint>
<signature id="Text.get_geometry">Text.get_geometry(**entity**: `Any`)
<a class="headerlink" href="#Text.get_geometry" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="get_extents(entity : Any, offset : Any, count : Any)"></endpoint>
<signature id="Text.get_extents+3">Text.get_extents(**entity**: `Any`, **offset**: `Any`, **count**: `Any`)
<a class="headerlink" href="#Text.get_extents+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="get_extents(entity : Any)"></endpoint>
<signature id="Text.get_extents">Text.get_extents(**entity**: `Any`)
<a class="headerlink" href="#Text.get_extents" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="contains(entity : Any, x : Any, y : Any)"></endpoint>
<signature id="Text.contains+3">Text.contains(**entity**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Text.contains+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="has(entity : Any)"></endpoint>
<signature id="Text.has">Text.has(**entity**: `Any`)
<a class="headerlink" href="#Text.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="set_loc(entity : Entity, space : String, key : String)"></endpoint>
<signature id="Text.set_loc+3">Text.set_loc(**entity**: `Entity`, **space**: `String`, **key**: `String`)
<a class="headerlink" href="#Text.set_loc+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="set_loc(entity : Entity, key : String)"></endpoint>
<signature id="Text.set_loc+2">Text.set_loc(**entity**: `Entity`, **key**: `String`)
<a class="headerlink" href="#Text.set_loc+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="set_loc_with_args(entity : Entity, space : String, key : String, args : List)"></endpoint>
<signature id="Text.set_loc_with_args+4">Text.set_loc_with_args(**entity**: `Entity`, **space**: `String`, **key**: `String`, **args**: `List`)
<a class="headerlink" href="#Text.set_loc_with_args+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="set_loc_with_args(entity : Entity, key : String, args : List)"></endpoint>
<signature id="Text.set_loc_with_args+3">Text.set_loc_with_args(**entity**: `Entity`, **key**: `String`, **args**: `List`)
<a class="headerlink" href="#Text.set_loc_with_args+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="get_text(entity : Any)"></endpoint>
<signature id="Text.get_text">Text.get_text(**entity**: `Any`)
<a class="headerlink" href="#Text.get_text" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="set_text_buffer(entity : Any, string : Any)"></endpoint>
<signature id="Text.set_text_buffer+2">Text.set_text_buffer(**entity**: `Any`, **string**: `Any`)
<a class="headerlink" href="#Text.set_text_buffer+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="Text" signature="set_text(entity : Any, string : Any)"></endpoint>
<signature id="Text.set_text+2">Text.set_text(**entity**: `Any`, **string**: `Any`)
<a class="headerlink" href="#Text.set_text+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### TextAlignH
`:::js import "luxe: system/text.modifier" for TextAlignH`
> no docs found

- [left](#TextAlignH.left)
- [center](#TextAlignH.center)
- [right](#TextAlignH.right)

<hr/>
<endpoint module="luxe: system/text.modifier" class="TextAlignH" signature="left"></endpoint>
<signature id="TextAlignH.left">TextAlignH.left
<a class="headerlink" href="#TextAlignH.left" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="TextAlignH" signature="center"></endpoint>
<signature id="TextAlignH.center">TextAlignH.center
<a class="headerlink" href="#TextAlignH.center" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="TextAlignH" signature="right"></endpoint>
<signature id="TextAlignH.right">TextAlignH.right
<a class="headerlink" href="#TextAlignH.right" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### TextAlignV
`:::js import "luxe: system/text.modifier" for TextAlignV`
> no docs found

- [top](#TextAlignV.top)
- [center](#TextAlignV.center)
- [bottom](#TextAlignV.bottom)

<hr/>
<endpoint module="luxe: system/text.modifier" class="TextAlignV" signature="top"></endpoint>
<signature id="TextAlignV.top">TextAlignV.top
<a class="headerlink" href="#TextAlignV.top" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="TextAlignV" signature="center"></endpoint>
<signature id="TextAlignV.center">TextAlignV.center
<a class="headerlink" href="#TextAlignV.center" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/text.modifier" class="TextAlignV" signature="bottom"></endpoint>
<signature id="TextAlignV.bottom">TextAlignV.bottom
<a class="headerlink" href="#TextAlignV.bottom" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

