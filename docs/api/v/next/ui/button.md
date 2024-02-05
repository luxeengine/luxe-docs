#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2024.2.1`)  


---

## `luxe: ui/button` module

- [UIButton](#uibutton)   

---

### UIButton
`:::js import "luxe: ui/button" for UIButton`
> `UIButton` is a `Control` that represents a clickable button with optional text content.
> 
>   ```js
>   var btn = UIButton.create(ui)
>   UIButton.set_text(btn, "click me!")
>   Control.set_events(btn) {|event|
>     if(event.type == UIEvent.release) {
>       Log.print("clicked button")
>     }
>   }
>   ```

- [create](#UIButton.create)(**ui_entity**: `Entity`)
- [set_text](#UIButton.set_text+2)(**control**: `UIButton`, **text**: `String`)
- [get_text](#UIButton.get_text)(**control**: `UIButton`)
- [set_font](#UIButton.set_font+2)(**control**: `UIButton`, **font**: `String`)
- [get_font](#UIButton.get_font)(**control**: `UIButton`)
- [set_color](#UIButton.set_color+2)(**control**: `UIButton`, **color**: `Color`)
- [get_color](#UIButton.get_color)(**control**: `UIButton`)
- [set_text_size](#UIButton.set_text_size+2)(**control**: `UIButton`, **size**: `Num`)
- [get_text_size](#UIButton.get_text_size)(**control**: `UIButton`)
- [set_align](#UIButton.set_align+2)(**control**: `UIButton`, **align**: `TextAlign`)
- [get_align](#UIButton.get_align)(**control**: `UIButton`)
- [set_align_vertical](#UIButton.set_align_vertical+2)(**control**: `UIButton`, **align**: `TextAlign`)
- [get_align_vertical](#UIButton.get_align_vertical)(**control**: `UIButton`)
- [get_render_text](#UIButton.get_render_text)(**control**: `UIButton`)

<hr/>
<endpoint module="luxe: ui/button" class="UIButton" signature="create(ui_entity : Entity)"></endpoint>
<signature id="UIButton.create">UIButton.create(**ui_entity**: `Entity`)
<a class="headerlink" href="#UIButton.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js UIButton`
> Create a new button control.   

<endpoint module="luxe: ui/button" class="UIButton" signature="set_text(control : UIButton, text : String)"></endpoint>
<signature id="UIButton.set_text+2">UIButton.set_text(**control**: `UIButton`, **text**: `String`)
<a class="headerlink" href="#UIButton.set_text+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the text displayed on a button.   

<endpoint module="luxe: ui/button" class="UIButton" signature="get_text(control : UIButton)"></endpoint>
<signature id="UIButton.get_text">UIButton.get_text(**control**: `UIButton`)
<a class="headerlink" href="#UIButton.get_text" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Get the text displayed on a button.   

<endpoint module="luxe: ui/button" class="UIButton" signature="set_font(control : UIButton, font : String)"></endpoint>
<signature id="UIButton.set_font+2">UIButton.set_font(**control**: `UIButton`, **font**: `String`)
<a class="headerlink" href="#UIButton.set_font+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the font of the text on a button.   

<endpoint module="luxe: ui/button" class="UIButton" signature="get_font(control : UIButton)"></endpoint>
<signature id="UIButton.get_font">UIButton.get_font(**control**: `UIButton`)
<a class="headerlink" href="#UIButton.get_font" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Id32`
> Get the font asset id of the text on the button.
> The asset id is returned as the string hash, to get the string use `Strings.get`.   

<endpoint module="luxe: ui/button" class="UIButton" signature="set_color(control : UIButton, color : Color)"></endpoint>
<signature id="UIButton.set_color+2">UIButton.set_color(**control**: `UIButton`, **color**: `Color`)
<a class="headerlink" href="#UIButton.set_color+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the color of a button.   

<endpoint module="luxe: ui/button" class="UIButton" signature="get_color(control : UIButton)"></endpoint>
<signature id="UIButton.get_color">UIButton.get_color(**control**: `UIButton`)
<a class="headerlink" href="#UIButton.get_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Color`
> Get the color of a button.   

<endpoint module="luxe: ui/button" class="UIButton" signature="set_text_size(control : UIButton, size : Num)"></endpoint>
<signature id="UIButton.set_text_size+2">UIButton.set_text_size(**control**: `UIButton`, **size**: `Num`)
<a class="headerlink" href="#UIButton.set_text_size+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the size of the text on a button.   

<endpoint module="luxe: ui/button" class="UIButton" signature="get_text_size(control : UIButton)"></endpoint>
<signature id="UIButton.get_text_size">UIButton.get_text_size(**control**: `UIButton`)
<a class="headerlink" href="#UIButton.get_text_size" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get the size of the text on a button.   

<endpoint module="luxe: ui/button" class="UIButton" signature="set_align(control : UIButton, align : TextAlign)"></endpoint>
<signature id="UIButton.set_align+2">UIButton.set_align(**control**: `UIButton`, **align**: `TextAlign`)
<a class="headerlink" href="#UIButton.set_align+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the horizontal alignment of the text on a button.   

<endpoint module="luxe: ui/button" class="UIButton" signature="get_align(control : UIButton)"></endpoint>
<signature id="UIButton.get_align">UIButton.get_align(**control**: `UIButton`)
<a class="headerlink" href="#UIButton.get_align" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js TextAlign`
> Get the horizontal alignment of the text on a button.   

<endpoint module="luxe: ui/button" class="UIButton" signature="set_align_vertical(control : UIButton, align : TextAlign)"></endpoint>
<signature id="UIButton.set_align_vertical+2">UIButton.set_align_vertical(**control**: `UIButton`, **align**: `TextAlign`)
<a class="headerlink" href="#UIButton.set_align_vertical+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the vertical alignment of the text on a button.   

<endpoint module="luxe: ui/button" class="UIButton" signature="get_align_vertical(control : UIButton)"></endpoint>
<signature id="UIButton.get_align_vertical">UIButton.get_align_vertical(**control**: `UIButton`)
<a class="headerlink" href="#UIButton.get_align_vertical" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js TextAlign`
> Get the vertical alignment of the text on a button.   

<endpoint module="luxe: ui/button" class="UIButton" signature="get_render_text(control : UIButton)"></endpoint>
<signature id="UIButton.get_render_text">UIButton.get_render_text(**control**: `UIButton`)
<a class="headerlink" href="#UIButton.get_render_text" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js RenderText`
> Get the underlying lowlevel text render object.
> Usable with the `Render.text_*` API.   

