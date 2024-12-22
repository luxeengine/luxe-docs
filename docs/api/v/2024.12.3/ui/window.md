#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2024.12.3`)  


---

## `luxe: ui/window` module

- [UIWindow](#uiwindow)   
- [UIWindowChange](#uiwindowchange)   

---

### UIWindow
`:::js import "luxe: ui/window" for UIWindow`
> `UIWindow` is a `Control` with a title bar, close button, and can be moved around 
> and resized like a windowed application on a desktop operating system. As you'd expect,
> you can attach other `Controls` to it that stay attached as you move it around.
> 
> ```js
>   var window = UIWindow.create(ui)
>   UIWindow.set_text(window, "I'm a window!")
>   UIWindow.set_title_size(window, 24)
>   UIWindow.set_text_size(window, 14)
>   UIWindow.set_resizable(window, true)
>   Control.set_bounds(window, 64, 64, 680, 360)
> ```

- [create](#UIWindow.create)(**ui_entity**: `Entity`)
- [close](#UIWindow.close)(**control**: `UIWindow`)
- [set_collapsed](#UIWindow.set_collapsed+2)(**control**: `UIWindow`, **state**: `Bool`)
- [get_collapsed](#UIWindow.get_collapsed)(**control**: `UIWindow`)
- [set_text](#UIWindow.set_text+2)(**control**: `UIWindow`, **text**: `String`)
- [set_text_size](#UIWindow.set_text_size+2)(**control**: `UIWindow`, **size**: `Num`)
- [set_text_color](#UIWindow.set_text_color+2)(**control**: `UIWindow`, **color**: `Color`)
- [set_text_font](#UIWindow.set_text_font+2)(**control**: `UIWindow`, **font**: `Font`)
- [set_title_size](#UIWindow.set_title_size+2)(**control**: `UIWindow`, **size**: `Num`)
- [set_resizable](#UIWindow.set_resizable+2)(**control**: `UIWindow`, **state**: `Bool`)
- [set_bring_to_front](#UIWindow.set_bring_to_front+2)(**control**: `UIWindow`, **state**: `Bool`)
- [set_closable](#UIWindow.set_closable+2)(**control**: `UIWindow`, **state**: `Bool`)
- [set_collapsible](#UIWindow.set_collapsible+2)(**control**: `UIWindow`, **state**: `Bool`)
- [set_draggable](#UIWindow.set_draggable+2)(**control**: `UIWindow`, **state**: `Bool`)
- [get_resizable](#UIWindow.get_resizable)(**control**: `UIWindow`)
- [get_bring_to_front](#UIWindow.get_bring_to_front)(**control**: `UIWindow`)
- [get_closable](#UIWindow.get_closable)(**control**: `UIWindow`)
- [get_collapsible](#UIWindow.get_collapsible)(**control**: `UIWindow`)
- [get_draggable](#UIWindow.get_draggable)(**control**: `UIWindow`)
- [set_outline](#UIWindow.set_outline+5)(**control**: `UIWindow`, **radius**: `Num`, **softness**: `Num`, **color**: `Color`, **offset**: `Float2`)
- [set_shadow](#UIWindow.set_shadow+5)(**control**: `UIWindow`, **radius**: `Num`, **softness**: `Num`, **color**: `Color`, **offset**: `Float2`)

<hr/>
<endpoint module="luxe: ui/window" class="UIWindow" signature="create(ui_entity : Entity)"></endpoint>
<signature id="UIWindow.create">UIWindow.create(**ui_entity**: `Entity`)
<a class="headerlink" href="#UIWindow.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js UIWindow`
> Create a new `UIWindow` control for the given UI.   

<endpoint module="luxe: ui/window" class="UIWindow" signature="close(control : UIWindow)"></endpoint>
<signature id="UIWindow.close">UIWindow.close(**control**: `UIWindow`)
<a class="headerlink" href="#UIWindow.close" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Make the given window disappear.   

<endpoint module="luxe: ui/window" class="UIWindow" signature="set_collapsed(control : UIWindow, state : Bool)"></endpoint>
<signature id="UIWindow.set_collapsed+2">UIWindow.set_collapsed(**control**: `UIWindow`, **state**: `Bool`)
<a class="headerlink" href="#UIWindow.set_collapsed+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set whether the given window's body is drawn (false, uncollapsed) or only the titlebar (true, collapsed).   

<endpoint module="luxe: ui/window" class="UIWindow" signature="get_collapsed(control : UIWindow)"></endpoint>
<signature id="UIWindow.get_collapsed">UIWindow.get_collapsed(**control**: `UIWindow`)
<a class="headerlink" href="#UIWindow.get_collapsed" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Get if the given window is collapsed.   

<endpoint module="luxe: ui/window" class="UIWindow" signature="set_text(control : UIWindow, text : String)"></endpoint>
<signature id="UIWindow.set_text+2">UIWindow.set_text(**control**: `UIWindow`, **text**: `String`)
<a class="headerlink" href="#UIWindow.set_text+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the titlebar text of the given window.   

<endpoint module="luxe: ui/window" class="UIWindow" signature="set_text_size(control : UIWindow, size : Num)"></endpoint>
<signature id="UIWindow.set_text_size+2">UIWindow.set_text_size(**control**: `UIWindow`, **size**: `Num`)
<a class="headerlink" href="#UIWindow.set_text_size+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the size of the titlebar text of the given window.   

<endpoint module="luxe: ui/window" class="UIWindow" signature="set_text_color(control : UIWindow, color : Color)"></endpoint>
<signature id="UIWindow.set_text_color+2">UIWindow.set_text_color(**control**: `UIWindow`, **color**: `Color`)
<a class="headerlink" href="#UIWindow.set_text_color+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the color of the titlebar text of the given window.   

<endpoint module="luxe: ui/window" class="UIWindow" signature="set_text_font(control : UIWindow, font : Font)"></endpoint>
<signature id="UIWindow.set_text_font+2">UIWindow.set_text_font(**control**: `UIWindow`, **font**: `Font`)
<a class="headerlink" href="#UIWindow.set_text_font+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the font of the titlebar text of the given window.   

<endpoint module="luxe: ui/window" class="UIWindow" signature="set_title_size(control : UIWindow, size : Num)"></endpoint>
<signature id="UIWindow.set_title_size+2">UIWindow.set_title_size(**control**: `UIWindow`, **size**: `Num`)
<a class="headerlink" href="#UIWindow.set_title_size+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the height of the titlebar of the given window.   

<endpoint module="luxe: ui/window" class="UIWindow" signature="set_resizable(control : UIWindow, state : Bool)"></endpoint>
<signature id="UIWindow.set_resizable+2">UIWindow.set_resizable(**control**: `UIWindow`, **state**: `Bool`)
<a class="headerlink" href="#UIWindow.set_resizable+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set if a window can be resized by dragging its bottom right corner.   

<endpoint module="luxe: ui/window" class="UIWindow" signature="set_bring_to_front(control : UIWindow, state : Bool)"></endpoint>
<signature id="UIWindow.set_bring_to_front+2">UIWindow.set_bring_to_front(**control**: `UIWindow`, **state**: `Bool`)
<a class="headerlink" href="#UIWindow.set_bring_to_front+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set if a window will bring itself to the front of the UI when interacted with.   

<endpoint module="luxe: ui/window" class="UIWindow" signature="set_closable(control : UIWindow, state : Bool)"></endpoint>
<signature id="UIWindow.set_closable+2">UIWindow.set_closable(**control**: `UIWindow`, **state**: `Bool`)
<a class="headerlink" href="#UIWindow.set_closable+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set if a window has a Close button the user can press.   

<endpoint module="luxe: ui/window" class="UIWindow" signature="set_collapsible(control : UIWindow, state : Bool)"></endpoint>
<signature id="UIWindow.set_collapsible+2">UIWindow.set_collapsible(**control**: `UIWindow`, **state**: `Bool`)
<a class="headerlink" href="#UIWindow.set_collapsible+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set if a window has a Collapse button the user can press.   

<endpoint module="luxe: ui/window" class="UIWindow" signature="set_draggable(control : UIWindow, state : Bool)"></endpoint>
<signature id="UIWindow.set_draggable+2">UIWindow.set_draggable(**control**: `UIWindow`, **state**: `Bool`)
<a class="headerlink" href="#UIWindow.set_draggable+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set if a window can be dragged around with the mouse.   

<endpoint module="luxe: ui/window" class="UIWindow" signature="get_resizable(control : UIWindow)"></endpoint>
<signature id="UIWindow.get_resizable">UIWindow.get_resizable(**control**: `UIWindow`)
<a class="headerlink" href="#UIWindow.get_resizable" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Get if a window can be resized by the user.   

<endpoint module="luxe: ui/window" class="UIWindow" signature="get_bring_to_front(control : UIWindow)"></endpoint>
<signature id="UIWindow.get_bring_to_front">UIWindow.get_bring_to_front(**control**: `UIWindow`)
<a class="headerlink" href="#UIWindow.get_bring_to_front" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Get if a window will bring itself to the front of the UI when interacted with.   

<endpoint module="luxe: ui/window" class="UIWindow" signature="get_closable(control : UIWindow)"></endpoint>
<signature id="UIWindow.get_closable">UIWindow.get_closable(**control**: `UIWindow`)
<a class="headerlink" href="#UIWindow.get_closable" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Get if a window has its Close button visible.   

<endpoint module="luxe: ui/window" class="UIWindow" signature="get_collapsible(control : UIWindow)"></endpoint>
<signature id="UIWindow.get_collapsible">UIWindow.get_collapsible(**control**: `UIWindow`)
<a class="headerlink" href="#UIWindow.get_collapsible" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Get if a window has its Collapse button visible.   

<endpoint module="luxe: ui/window" class="UIWindow" signature="get_draggable(control : UIWindow)"></endpoint>
<signature id="UIWindow.get_draggable">UIWindow.get_draggable(**control**: `UIWindow`)
<a class="headerlink" href="#UIWindow.get_draggable" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Get if a window can be dragged around with the mouse.   

<endpoint module="luxe: ui/window" class="UIWindow" signature="set_outline(control : UIWindow, radius : Num, softness : Num, color : Color, offset : Float2)"></endpoint>
<signature id="UIWindow.set_outline+5">UIWindow.set_outline(**control**: `UIWindow`, **radius**: `Num`, **softness**: `Num`, **color**: `Color`, **offset**: `Float2`)
<a class="headerlink" href="#UIWindow.set_outline+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the text outline parameters.   

<endpoint module="luxe: ui/window" class="UIWindow" signature="set_shadow(control : UIWindow, radius : Num, softness : Num, color : Color, offset : Float2)"></endpoint>
<signature id="UIWindow.set_shadow+5">UIWindow.set_shadow(**control**: `UIWindow`, **radius**: `Num`, **softness**: `Num`, **color**: `Color`, **offset**: `Float2`)
<a class="headerlink" href="#UIWindow.set_shadow+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the text shadow parameters.   

### UIWindowChange
`:::js import "luxe: ui/window" for UIWindowChange`
> no docs found

- [close](#UIWindowChange.close)
- [open](#UIWindowChange.open)
- [collapse](#UIWindowChange.collapse)
- [uncollapse](#UIWindowChange.uncollapse)
- [move](#UIWindowChange.move)
- [name](#UIWindowChange.name)(**value**: `Any`)

<hr/>
<endpoint module="luxe: ui/window" class="UIWindowChange" signature="close"></endpoint>
<signature id="UIWindowChange.close">UIWindowChange.close
<a class="headerlink" href="#UIWindowChange.close" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/window" class="UIWindowChange" signature="open"></endpoint>
<signature id="UIWindowChange.open">UIWindowChange.open
<a class="headerlink" href="#UIWindowChange.open" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/window" class="UIWindowChange" signature="collapse"></endpoint>
<signature id="UIWindowChange.collapse">UIWindowChange.collapse
<a class="headerlink" href="#UIWindowChange.collapse" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/window" class="UIWindowChange" signature="uncollapse"></endpoint>
<signature id="UIWindowChange.uncollapse">UIWindowChange.uncollapse
<a class="headerlink" href="#UIWindowChange.uncollapse" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/window" class="UIWindowChange" signature="move"></endpoint>
<signature id="UIWindowChange.move">UIWindowChange.move
<a class="headerlink" href="#UIWindowChange.move" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/window" class="UIWindowChange" signature="name(value : Any)"></endpoint>
<signature id="UIWindowChange.name">UIWindowChange.name(**value**: `Any`)
<a class="headerlink" href="#UIWindowChange.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

