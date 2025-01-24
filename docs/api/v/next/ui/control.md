#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2025.1.2`)  


---

## `luxe: ui/control` module

- [Control](#control)   

---

### Control
`:::js import "luxe: ui/control" for Control`
> Class for managing controls on UI modifiers.
> Note that all UI elements are controls, including UIImage, UILabel, UIButton, etc...
> 
> ```js
>   _ui = Entity.create(app.ui)
>   UI.create(_ui, 0, 0, app.width, app.height, 0, app.ui_camera)
> 
>   var control = Control.create(_ui)
> ```

- [create](#Control.create)(**ui_entity**: `Entity`)
- [destroy](#Control.destroy)(**control**: `Control`)
- [destroy_children](#Control.destroy_children)(**control**: `Control`)
- [valid](#Control.valid)(**control**: `Control`)
- [get_ui](#Control.get_ui)(**control**: `Control`)
- [get](#Control.get)(**id**: `String`)
- [exists](#Control.exists)(**id**: `String`)
- [clear](#Control.clear+2)(**control**: `Control`, **uiclear_action**: `UIClear`)
- [press](#Control.press+2)(**control**: `Control`, **state**: `Bool`)
- [enter](#Control.enter+2)(**control**: `Control`, **state**: `Bool`)
- [can_see](#Control.can_see)(**control**: `Control`)
- [can_see_area](#Control.can_see_area+2)(**control**: `Control`, **area**: `Rect`)
- [can_see_point](#Control.can_see_point+2)(**control**: `Control`, **point**: `Vec`)
- [set_type](#Control.set_type+2)(**control**: `Control`, **type**: `String`)
- [get_type](#Control.get_type)(**control**: `Control`)
- [set_id](#Control.set_id+2)(**control**: `Control`, **id**: `String`)
- [get_id](#Control.get_id)(**control**: `Control`)
- [get_bounds_abs](#Control.get_bounds_abs+2)(**control**: `Control`, **into**: `List`)
- [get_bounds](#Control.get_bounds+2)(**control**: `Control`, **into**: `List`)
- [set_allow_bounds_event](#Control.set_allow_bounds_event+2)(**control**: `Control`, **state**: `Bool`)
- [get_allow_bounds_event](#Control.get_allow_bounds_event)(**control**: `Control`)
- [set_bounds_abs](#Control.set_bounds_abs+5)(**control**: `Control`, **x**: `Num`, **y**: `Num`, **w**: `Num`, **h**: `Num`)
- [set_bounds](#Control.set_bounds+5)(**control**: `Control`, **x**: `Num`, **y**: `Num`, **w**: `Num`, **h**: `Num`)
- [set_pos_abs](#Control.set_pos_abs+3)(**control**: `Control`, **x**: `Num`, **y**: `Num`)
- [set_pos](#Control.set_pos+3)(**control**: `Control`, **x**: `Num`, **y**: `Num`)
- [set_system_cursor](#Control.set_system_cursor+2)(**control**: `Control`, **cursor**: `SystemCursor`)
- [set_size](#Control.set_size+3)(**control**: `Control`, **w**: `Num`, **h**: `Num`)
- [get_pos_x](#Control.get_pos_x)(**control**: `Control`)
- [get_pos_x_abs](#Control.get_pos_x_abs)(**control**: `Control`)
- [get_pos_y](#Control.get_pos_y)(**control**: `Control`)
- [get_pos_y_abs](#Control.get_pos_y_abs)(**control**: `Control`)
- [get_width](#Control.get_width)(**control**: `Control`)
- [get_height](#Control.get_height)(**control**: `Control`)
- [contains](#Control.contains+3)(**control**: `Control`, **x**: `Num`, **y**: `Num`)
- [get_entity](#Control.get_entity)(**control**: `Control`)
- [get_parent](#Control.get_parent)(**control**: `Control`)
- [get_allow_input](#Control.get_allow_input)(**control**: `Control`)
- [set_allow_input](#Control.set_allow_input+2)(**control**: `Control`, **allow**: `Bool`)
- [set_allow_drag](#Control.set_allow_drag+3)(**control**: `Control`, **allow**: `Bool`, **tag**: `String`)
- [set_droppable_payload](#Control.set_droppable_payload+2)(**control**: `Control`, **value**: `Handle`)
- [get_droppable_payload](#Control.get_droppable_payload)(**control**: `Control`)
- [set_droppable_tags](#Control.set_droppable_tags+2)(**control**: `Control`, **tags**: `List`)
- [get_droppable_tags](#Control.get_droppable_tags)(**control**: `Control`)
- [get_allow_keys](#Control.get_allow_keys)(**control**: `Control`)
- [set_allow_keys](#Control.set_allow_keys+2)(**control**: `Control`, **allow**: `Bool`)
- [get_allow_tab](#Control.get_allow_tab)(**control**: `Control`)
- [set_allow_tab](#Control.set_allow_tab+2)(**control**: `Control`, **allow**: `Bool`)
- [get_visible](#Control.get_visible)(**control**: `Control`)
- [set_visible](#Control.set_visible+2)(**control**: `Control`, **visible**: `Bool`)
- [get_opacity](#Control.get_opacity)(**control**: `Control`)
- [set_opacity](#Control.set_opacity+2)(**control**: `Control`, **opacity**: `Num`)
- [get_disabled](#Control.get_disabled)(**control**: `Control`)
- [set_disabled](#Control.set_disabled+2)(**control**: `Control`, **disabled**: `Bool`)
- [get_enabled](#Control.get_enabled)(**control**: `Control`)
- [set_enabled](#Control.set_enabled+2)(**control**: `Control`, **enabled**: `Bool`)
- [get_clip](#Control.get_clip)(**control**: `Control`)
- [set_clip](#Control.set_clip+2)(**control**: `Control`, **clip**: `Bool`)
- [get_nodes](#Control.get_nodes)(**control**: `Control`)
- [get_depth](#Control.get_depth)(**control**: `Control`)
- [get_depth_offset](#Control.get_depth_offset)(**control**: `Control`)
- [set_depth_offset](#Control.set_depth_offset+2)(**control**: `Control`, **depth_offset**: `Num`)
- [get_input_inside](#Control.get_input_inside)(**control**: `Control`)
- [get_input_pressed](#Control.get_input_pressed)(**control**: `Control`)
- [child_at_point](#Control.child_at_point+3)(**control**: `Control`, **x**: `Num`, **y**: `Num`)
- [child_count](#Control.child_count)(**control**: `Control`)
- [child_index](#Control.child_index+2)(**control**: `Control`, **child**: `Control`)
- [child_get](#Control.child_get+2)(**control**: `Control`, **index**: `Num`)
- [child_add](#Control.child_add+3)(**control**: `Control`, **child**: `Control`, **internal**: `Bool`)
- [child_add](#Control.child_add+2)(**control**: `Control`, **child**: `Control`)
- [child_remove](#Control.child_remove+2)(**control**: `Control`, **child**: `Control`)
- [children_bounds](#Control.children_bounds+2)(**control**: `Control`, **into**: `List`)
- [set_behave](#Control.set_behave+2)(**control**: `Control`, **behave**: `UIBehave`)
- [get_behave](#Control.get_behave)(**control**: `Control`)
- [set_contain](#Control.set_contain+2)(**control**: `Control`, **contain**: `UIContain`)
- [get_contain](#Control.get_contain)(**control**: `Control`)
- [set_margin](#Control.set_margin+5)(**control**: `Control`, **left**: `Num`, **top**: `Num`, **right**: `Num`, **bottom**: `Num`)
- [set_limits](#Control.set_limits+5)(**control**: `Control`, **min_x**: `Num`, **min_y**: `Num`, **max_x**: `Num`, **max_y**: `Num`)
- [get_margin](#Control.get_margin)(**control**: `Control`)
- [set_render](#Control.set_render+2)(**control**: `Control`, **fn**: `Fn`)
- [set_events](#Control.set_events+2)(**control**: `Control`, **fn**: `Fn`)
- [unset_events](#Control.unset_events+2)(**control**: `Control`, **id**: `String`)
- [set_process](#Control.set_process+2)(**control**: `Control`, **fn**: `Fn`)
- [get_state_data](#Control.get_state_data)(**control**: `Control`)
- [set_state_data](#Control.set_state_data+2)(**control**: `Control`, **data**: `Any`)

<hr/>
<endpoint module="luxe: ui/control" class="Control" signature="create(ui_entity : Entity)"></endpoint>
<signature id="Control.create">Control.create(**ui_entity**: `Entity`)
<a class="headerlink" href="#Control.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Control`
> Create a "blank" control for layout or custom input/drawing.
> Returns the new Control.   

<endpoint module="luxe: ui/control" class="Control" signature="destroy(control : Control)"></endpoint>
<signature id="Control.destroy">Control.destroy(**control**: `Control`)
<a class="headerlink" href="#Control.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Destroy an existing control.
> 
> ```js
>   var control = Control.create(_ui)
>   //do stuff and then later...
>   Control.destroy(control)
> ```   

<endpoint module="luxe: ui/control" class="Control" signature="destroy_children(control : Control)"></endpoint>
<signature id="Control.destroy_children">Control.destroy_children(**control**: `Control`)
<a class="headerlink" href="#Control.destroy_children" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Destroy the children of a control.   

<endpoint module="luxe: ui/control" class="Control" signature="valid(control : Control)"></endpoint>
<signature id="Control.valid">Control.valid(**control**: `Control`)
<a class="headerlink" href="#Control.valid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Check if a control exists and has not been destroyed.
>     
> ```js
>   var control = Control.create(_ui)
>   Log.print(Control.valid(control)) //true
>   Control.destroy(control)
>   Log.print(Control.valid(control)) //false
> ```   

<endpoint module="luxe: ui/control" class="Control" signature="get_ui(control : Control)"></endpoint>
<signature id="Control.get_ui">Control.get_ui(**control**: `Control`)
<a class="headerlink" href="#Control.get_ui" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> Get UI entity a control is part of.
> 
> ```js
>   var control = Control.create(_ui)
>   var control_ui = Control.get_ui(control)
>   Log.print(control_ui == _ui) //true
> ```   

<endpoint module="luxe: ui/control" class="Control" signature="get(id : String)"></endpoint>
<signature id="Control.get">Control.get(**id**: `String`)
<a class="headerlink" href="#Control.get" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Control`
> Get a control by its id.
>     
> ```js
>   var control = Control.create(_ui)
>   Control.set_id(control, "test_id")
>   var control_by_id = Control.get("test_id")
>   Log.print(control == control_by_id) //true
> ```   

<endpoint module="luxe: ui/control" class="Control" signature="exists(id : String)"></endpoint>
<signature id="Control.exists">Control.exists(**id**: `String`)
<a class="headerlink" href="#Control.exists" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Check if a control with a specific id exists.   

<endpoint module="luxe: ui/control" class="Control" signature="clear(control : Control, uiclear_action : UIClear)"></endpoint>
<signature id="Control.clear+2">Control.clear(**control**: `Control`, **uiclear_action**: `UIClear`)
<a class="headerlink" href="#Control.clear+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Clear the children of a control in a specific manner.   

<endpoint module="luxe: ui/control" class="Control" signature="press(control : Control, state : Bool)"></endpoint>
<signature id="Control.press+2">Control.press(**control**: `Control`, **state**: `Bool`)
<a class="headerlink" href="#Control.press+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Send a press or release event to the control (in the center of the control)   

<endpoint module="luxe: ui/control" class="Control" signature="enter(control : Control, state : Bool)"></endpoint>
<signature id="Control.enter+2">Control.enter(**control**: `Control`, **state**: `Bool`)
<a class="headerlink" href="#Control.enter+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Send a enter or exit event to the control   

<endpoint module="luxe: ui/control" class="Control" signature="can_see(control : Control)"></endpoint>
<signature id="Control.can_see">Control.can_see(**control**: `Control`)
<a class="headerlink" href="#Control.can_see" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if this control can be seen, or false if clipped.   

<endpoint module="luxe: ui/control" class="Control" signature="can_see_area(control : Control, area : Rect)"></endpoint>
<signature id="Control.can_see_area+2">Control.can_see_area(**control**: `Control`, **area**: `Rect`)
<a class="headerlink" href="#Control.can_see_area+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if the area at this control can be seen or false if clipped.   

<endpoint module="luxe: ui/control" class="Control" signature="can_see_point(control : Control, point : Vec)"></endpoint>
<signature id="Control.can_see_point+2">Control.can_see_point(**control**: `Control`, **point**: `Vec`)
<a class="headerlink" href="#Control.can_see_point+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if the point at this control can be seen or false if clipped.   

<endpoint module="luxe: ui/control" class="Control" signature="set_type(control : Control, type : String)"></endpoint>
<signature id="Control.set_type+2">Control.set_type(**control**: `Control`, **type**: `String`)
<a class="headerlink" href="#Control.set_type+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get_type(control : Control)"></endpoint>
<signature id="Control.get_type">Control.get_type(**control**: `Control`)
<a class="headerlink" href="#Control.get_type" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="set_id(control : Control, id : String)"></endpoint>
<signature id="Control.set_id+2">Control.set_id(**control**: `Control`, **id**: `String`)
<a class="headerlink" href="#Control.set_id+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Set the id of a control. Good for debugging and retrieving controls by their id.
> Must be unique, so adding `ID.unique()` to the id can be useful.
> 
> ```js
>   var control = Control.create(_ui)
>   Control.set_id(control, "good_recognizable_control_name_%(ID.unique())")
> ```   

<endpoint module="luxe: ui/control" class="Control" signature="get_id(control : Control)"></endpoint>
<signature id="Control.get_id">Control.get_id(**control**: `Control`)
<a class="headerlink" href="#Control.get_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Retrieve the id of a control.   

<endpoint module="luxe: ui/control" class="Control" signature="get_bounds_abs(control : Control, into : List)"></endpoint>
<signature id="Control.get_bounds_abs+2">Control.get_bounds_abs(**control**: `Control`, **into**: `List`)
<a class="headerlink" href="#Control.get_bounds_abs+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Retrieve the bounds(position and size) of a control (relative to the UI modifier) into a list `[x, y, width, height]`.
> The passed list must have at least 4 elements and the function will write into the first 4.
> Passing a list into the function instead of returning a value is to avoid allocating memory where not needed.
> 
> ```js
>   var parent = Control.create(_ui)
>   Control.set_pos(parent, 50, 50)
>   var child = Control.create(_ui)
>   Control.child_add(parent, child)
>   Control.set_pos(child, 100, 100)
>   Control.set_size(child, 20, 20)
>   var bounds = [0,0,0,0]
>   Control.get_bounds_abs(child, bounds)
>   Log.print(bounds) // [150, 150, 20, 20]
> ```   

<endpoint module="luxe: ui/control" class="Control" signature="get_bounds(control : Control, into : List)"></endpoint>
<signature id="Control.get_bounds+2">Control.get_bounds(**control**: `Control`, **into**: `List`)
<a class="headerlink" href="#Control.get_bounds+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Retrieve the bounds(position and size) of a control (relative to their parent control or ui modifier if there is none) into a list `[x, y, width, height]`.
> The passed list must have at least 4 elements and the function will write into the first 4.
> Passing a list into the function instead of returning a value is to avoid allocating memory where not needed.
> 
> ```js
>   var parent = Control.create(_ui)
>   Control.set_pos(parent, 50, 50)
>   var child = Control.create(_ui)
>   Control.child_add(parent, child)
>   Control.set_pos(child, 100, 100)
>   Control.set_size(child, 20, 20)
>   var bounds = [0,0,0,0]
>   Control.get_bounds(child, bounds)
>   Log.print(bounds) // [100, 100, 20, 20]
> ```   

<endpoint module="luxe: ui/control" class="Control" signature="set_allow_bounds_event(control : Control, state : Bool)"></endpoint>
<signature id="Control.set_allow_bounds_event+2">Control.set_allow_bounds_event(**control**: `Control`, **state**: `Bool`)
<a class="headerlink" href="#Control.set_allow_bounds_event+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Enables bounds events for the control. Since there are many controls
> that may be resized during layout events, only ones that ask for the event 
> will receive it to save time.   

<endpoint module="luxe: ui/control" class="Control" signature="get_allow_bounds_event(control : Control)"></endpoint>
<signature id="Control.get_allow_bounds_event">Control.get_allow_bounds_event(**control**: `Control`)
<a class="headerlink" href="#Control.get_allow_bounds_event" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if this control sends bounds events.   

<endpoint module="luxe: ui/control" class="Control" signature="set_bounds_abs(control : Control, x : Num, y : Num, w : Num, h : Num)"></endpoint>
<signature id="Control.set_bounds_abs+5">Control.set_bounds_abs(**control**: `Control`, **x**: `Num`, **y**: `Num`, **w**: `Num`, **h**: `Num`)
<a class="headerlink" href="#Control.set_bounds_abs+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the control bounds(position and size) relative to the UI modifier.   

<endpoint module="luxe: ui/control" class="Control" signature="set_bounds(control : Control, x : Num, y : Num, w : Num, h : Num)"></endpoint>
<signature id="Control.set_bounds+5">Control.set_bounds(**control**: `Control`, **x**: `Num`, **y**: `Num`, **w**: `Num`, **h**: `Num`)
<a class="headerlink" href="#Control.set_bounds+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the control bounds(position and size) relative to the parent control.   

<endpoint module="luxe: ui/control" class="Control" signature="set_pos_abs(control : Control, x : Num, y : Num)"></endpoint>
<signature id="Control.set_pos_abs+3">Control.set_pos_abs(**control**: `Control`, **x**: `Num`, **y**: `Num`)
<a class="headerlink" href="#Control.set_pos_abs+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the control position relative to the UI modifier.   

<endpoint module="luxe: ui/control" class="Control" signature="set_pos(control : Control, x : Num, y : Num)"></endpoint>
<signature id="Control.set_pos+3">Control.set_pos(**control**: `Control`, **x**: `Num`, **y**: `Num`)
<a class="headerlink" href="#Control.set_pos+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the control position relative to the parent control, or UI modifier if no parent exists.   

<endpoint module="luxe: ui/control" class="Control" signature="set_system_cursor(control : Control, cursor : SystemCursor)"></endpoint>
<signature id="Control.set_system_cursor+2">Control.set_system_cursor(**control**: `Control`, **cursor**: `SystemCursor`)
<a class="headerlink" href="#Control.set_system_cursor+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> If the control has input enabled, when entered it will set the system cursor to the given type.   

<endpoint module="luxe: ui/control" class="Control" signature="set_size(control : Control, w : Num, h : Num)"></endpoint>
<signature id="Control.set_size+3">Control.set_size(**control**: `Control`, **w**: `Num`, **h**: `Num`)
<a class="headerlink" href="#Control.set_size+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the control size.   

<endpoint module="luxe: ui/control" class="Control" signature="get_pos_x(control : Control)"></endpoint>
<signature id="Control.get_pos_x">Control.get_pos_x(**control**: `Control`)
<a class="headerlink" href="#Control.get_pos_x" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get the control position x component relative to its parent control.   

<endpoint module="luxe: ui/control" class="Control" signature="get_pos_x_abs(control : Control)"></endpoint>
<signature id="Control.get_pos_x_abs">Control.get_pos_x_abs(**control**: `Control`)
<a class="headerlink" href="#Control.get_pos_x_abs" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get the control position x component.   

<endpoint module="luxe: ui/control" class="Control" signature="get_pos_y(control : Control)"></endpoint>
<signature id="Control.get_pos_y">Control.get_pos_y(**control**: `Control`)
<a class="headerlink" href="#Control.get_pos_y" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get the control position y component relative to its parent control.   

<endpoint module="luxe: ui/control" class="Control" signature="get_pos_y_abs(control : Control)"></endpoint>
<signature id="Control.get_pos_y_abs">Control.get_pos_y_abs(**control**: `Control`)
<a class="headerlink" href="#Control.get_pos_y_abs" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get the control position y component.   

<endpoint module="luxe: ui/control" class="Control" signature="get_width(control : Control)"></endpoint>
<signature id="Control.get_width">Control.get_width(**control**: `Control`)
<a class="headerlink" href="#Control.get_width" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get the control width.   

<endpoint module="luxe: ui/control" class="Control" signature="get_height(control : Control)"></endpoint>
<signature id="Control.get_height">Control.get_height(**control**: `Control`)
<a class="headerlink" href="#Control.get_height" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get the control height.   

<endpoint module="luxe: ui/control" class="Control" signature="contains(control : Control, x : Num, y : Num)"></endpoint>
<signature id="Control.contains+3">Control.contains(**control**: `Control`, **x**: `Num`, **y**: `Num`)
<a class="headerlink" href="#Control.contains+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Check whether the a point is within the control bounds   

<endpoint module="luxe: ui/control" class="Control" signature="get_entity(control : Control)"></endpoint>
<signature id="Control.get_entity">Control.get_entity(**control**: `Control`)
<a class="headerlink" href="#Control.get_entity" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> Get the entity that has the UI modifier the control in.   

<endpoint module="luxe: ui/control" class="Control" signature="get_parent(control : Control)"></endpoint>
<signature id="Control.get_parent">Control.get_parent(**control**: `Control`)
<a class="headerlink" href="#Control.get_parent" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Control`
> Get the entity this entity is a child of or `null` if there isnt any.   

<endpoint module="luxe: ui/control" class="Control" signature="get_allow_input(control : Control)"></endpoint>
<signature id="Control.get_allow_input">Control.get_allow_input(**control**: `Control`)
<a class="headerlink" href="#Control.get_allow_input" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Get whether the control recieves input events in its `set_process` function.   

<endpoint module="luxe: ui/control" class="Control" signature="set_allow_input(control : Control, allow : Bool)"></endpoint>
<signature id="Control.set_allow_input+2">Control.set_allow_input(**control**: `Control`, **allow**: `Bool`)
<a class="headerlink" href="#Control.set_allow_input+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set whether the control recieves input events in its `set_process` function.   

<endpoint module="luxe: ui/control" class="Control" signature="set_allow_drag(control : Control, allow : Bool, tag : String)"></endpoint>
<signature id="Control.set_allow_drag+3">Control.set_allow_drag(**control**: `Control`, **allow**: `Bool`, **tag**: `String`)
<a class="headerlink" href="#Control.set_allow_drag+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set whether the control recieves drag events   

<endpoint module="luxe: ui/control" class="Control" signature="set_droppable_payload(control : Control, value : Handle)"></endpoint>
<signature id="Control.set_droppable_payload+2">Control.set_droppable_payload(**control**: `Control`, **value**: `Handle`)
<a class="headerlink" href="#Control.set_droppable_payload+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set a value that will be passed through the drag event to the drop event on the other side. 
>           This value is a handle/number, so you can pass api handles, a number, a hashed string, or a block instance   

<endpoint module="luxe: ui/control" class="Control" signature="get_droppable_payload(control : Control)"></endpoint>
<signature id="Control.get_droppable_payload">Control.get_droppable_payload(**control**: `Control`)
<a class="headerlink" href="#Control.get_droppable_payload" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Handle`
> Get the drop payload for this control   

<endpoint module="luxe: ui/control" class="Control" signature="set_droppable_tags(control : Control, tags : List)"></endpoint>
<signature id="Control.set_droppable_tags+2">Control.set_droppable_tags(**control**: `Control`, **tags**: `List`)
<a class="headerlink" href="#Control.set_droppable_tags+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the droppable tags that are allowed for this control, as an array of strings   

<endpoint module="luxe: ui/control" class="Control" signature="get_droppable_tags(control : Control)"></endpoint>
<signature id="Control.get_droppable_tags">Control.get_droppable_tags(**control**: `Control`)
<a class="headerlink" href="#Control.get_droppable_tags" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> Get the droppable tags that are allowed for this control, as an array of strings   

<endpoint module="luxe: ui/control" class="Control" signature="get_allow_keys(control : Control)"></endpoint>
<signature id="Control.get_allow_keys">Control.get_allow_keys(**control**: `Control`)
<a class="headerlink" href="#Control.get_allow_keys" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Get whether the control recieves key events in its `set_process` function.   

<endpoint module="luxe: ui/control" class="Control" signature="set_allow_keys(control : Control, allow : Bool)"></endpoint>
<signature id="Control.set_allow_keys+2">Control.set_allow_keys(**control**: `Control`, **allow**: `Bool`)
<a class="headerlink" href="#Control.set_allow_keys+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set whether the control recieves key events in its `set_process` function.   

<endpoint module="luxe: ui/control" class="Control" signature="get_allow_tab(control : Control)"></endpoint>
<signature id="Control.get_allow_tab">Control.get_allow_tab(**control**: `Control`)
<a class="headerlink" href="#Control.get_allow_tab" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Get whether the control can be "tabbed" to.   

<endpoint module="luxe: ui/control" class="Control" signature="set_allow_tab(control : Control, allow : Bool)"></endpoint>
<signature id="Control.set_allow_tab+2">Control.set_allow_tab(**control**: `Control`, **allow**: `Bool`)
<a class="headerlink" href="#Control.set_allow_tab+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set whether the control can be "tabbed" to.   

<endpoint module="luxe: ui/control" class="Control" signature="get_visible(control : Control)"></endpoint>
<signature id="Control.get_visible">Control.get_visible(**control**: `Control`)
<a class="headerlink" href="#Control.get_visible" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Get whether a control is visible.   

<endpoint module="luxe: ui/control" class="Control" signature="set_visible(control : Control, visible : Bool)"></endpoint>
<signature id="Control.set_visible+2">Control.set_visible(**control**: `Control`, **visible**: `Bool`)
<a class="headerlink" href="#Control.set_visible+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set whether a control (or its children) is visible.
> Note that when a control is not visible, it also doesnt contribute to the layout.   

<endpoint module="luxe: ui/control" class="Control" signature="get_opacity(control : Control)"></endpoint>
<signature id="Control.get_opacity">Control.get_opacity(**control**: `Control`)
<a class="headerlink" href="#Control.get_opacity" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get a control opacity value.   

<endpoint module="luxe: ui/control" class="Control" signature="set_opacity(control : Control, opacity : Num)"></endpoint>
<signature id="Control.set_opacity+2">Control.set_opacity(**control**: `Control`, **opacity**: `Num`)
<a class="headerlink" href="#Control.set_opacity+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set a control opacity value. Affects children opacity as well.   

<endpoint module="luxe: ui/control" class="Control" signature="get_disabled(control : Control)"></endpoint>
<signature id="Control.get_disabled">Control.get_disabled(**control**: `Control`)
<a class="headerlink" href="#Control.get_disabled" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Get whether a control is disabled. This refers to the "inputable" state of inputs like buttons or text fields.   

<endpoint module="luxe: ui/control" class="Control" signature="set_disabled(control : Control, disabled : Bool)"></endpoint>
<signature id="Control.set_disabled+2">Control.set_disabled(**control**: `Control`, **disabled**: `Bool`)
<a class="headerlink" href="#Control.set_disabled+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set whether a control is disabled. This refers to the "inputable" state of inputs like buttons or text fields.   

<endpoint module="luxe: ui/control" class="Control" signature="get_enabled(control : Control)"></endpoint>
<signature id="Control.get_enabled">Control.get_enabled(**control**: `Control`)
<a class="headerlink" href="#Control.get_enabled" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Get whether a control is enabled. This refers to the "inputable" state of inputs like buttons or text fields.   

<endpoint module="luxe: ui/control" class="Control" signature="set_enabled(control : Control, enabled : Bool)"></endpoint>
<signature id="Control.set_enabled+2">Control.set_enabled(**control**: `Control`, **enabled**: `Bool`)
<a class="headerlink" href="#Control.set_enabled+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set whether a control is enabled. This refers to the "inputable" state of inputs like buttons or text fields.   

<endpoint module="luxe: ui/control" class="Control" signature="get_clip(control : Control)"></endpoint>
<signature id="Control.get_clip">Control.get_clip(**control**: `Control`)
<a class="headerlink" href="#Control.get_clip" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Get whether a control should clip its contents.   

<endpoint module="luxe: ui/control" class="Control" signature="set_clip(control : Control, clip : Bool)"></endpoint>
<signature id="Control.set_clip+2">Control.set_clip(**control**: `Control`, **clip**: `Bool`)
<a class="headerlink" href="#Control.set_clip+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set whether a control should clip its contents.   

<endpoint module="luxe: ui/control" class="Control" signature="get_nodes(control : Control)"></endpoint>
<signature id="Control.get_nodes">Control.get_nodes(**control**: `Control`)
<a class="headerlink" href="#Control.get_nodes" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get how many child controls this control has recursively.
> So 1 if it doesnt have any children, 2 if it has 1 child, 3 if it has 2 children or if it has 1 child which itself has a child, etc...
> Only valid after `UI.commit`.   

<endpoint module="luxe: ui/control" class="Control" signature="get_depth(control : Control)"></endpoint>
<signature id="Control.get_depth">Control.get_depth(**control**: `Control`)
<a class="headerlink" href="#Control.get_depth" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get the depth generated for a control, not including the depth offset.   

<endpoint module="luxe: ui/control" class="Control" signature="get_depth_offset(control : Control)"></endpoint>
<signature id="Control.get_depth_offset">Control.get_depth_offset(**control**: `Control`)
<a class="headerlink" href="#Control.get_depth_offset" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get the depth offset of a control.   

<endpoint module="luxe: ui/control" class="Control" signature="set_depth_offset(control : Control, depth_offset : Num)"></endpoint>
<signature id="Control.set_depth_offset+2">Control.set_depth_offset(**control**: `Control`, **depth_offset**: `Num`)
<a class="headerlink" href="#Control.set_depth_offset+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the depth offset for a control, allowing you to move it in front or behind other controls if the generated depth doesnt work for you   

<endpoint module="luxe: ui/control" class="Control" signature="get_input_inside(control : Control)"></endpoint>
<signature id="Control.get_input_inside">Control.get_input_inside(**control**: `Control`)
<a class="headerlink" href="#Control.get_input_inside" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Check whether the input (usually mouse cursor) is currently in a control. (In sync with `UIEvent.enter` and `UIEvent.exit`)   

<endpoint module="luxe: ui/control" class="Control" signature="get_input_pressed(control : Control)"></endpoint>
<signature id="Control.get_input_pressed">Control.get_input_pressed(**control**: `Control`)
<a class="headerlink" href="#Control.get_input_pressed" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Check whether the input (usually mouse cursor) is currently in a control and any of its buttons are pressed.   

<endpoint module="luxe: ui/control" class="Control" signature="child_at_point(control : Control, x : Num, y : Num)"></endpoint>
<signature id="Control.child_at_point+3">Control.child_at_point(**control**: `Control`, **x**: `Num`, **y**: `Num`)
<a class="headerlink" href="#Control.child_at_point+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Control`
> Get the top child control at a specific (absolute) point.   

<endpoint module="luxe: ui/control" class="Control" signature="child_count(control : Control)"></endpoint>
<signature id="Control.child_count">Control.child_count(**control**: `Control`)
<a class="headerlink" href="#Control.child_count" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get the amount of children a control has.   

<endpoint module="luxe: ui/control" class="Control" signature="child_index(control : Control, child : Control)"></endpoint>
<signature id="Control.child_index+2">Control.child_index(**control**: `Control`, **child**: `Control`)
<a class="headerlink" href="#Control.child_index+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get the index of a child control.   

<endpoint module="luxe: ui/control" class="Control" signature="child_get(control : Control, index : Num)"></endpoint>
<signature id="Control.child_get+2">Control.child_get(**control**: `Control`, **index**: `Num`)
<a class="headerlink" href="#Control.child_get+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Child`
> Get a child control by its index.   

<endpoint module="luxe: ui/control" class="Control" signature="child_add(control : Control, child : Control, internal : Bool)"></endpoint>
<signature id="Control.child_add+3">Control.child_add(**control**: `Control`, **child**: `Control`, **internal**: `Bool`)
<a class="headerlink" href="#Control.child_add+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Make a control the child control of another control.
> If you mark the child as internal, it wont be queried by other methods affecting children.   

<endpoint module="luxe: ui/control" class="Control" signature="child_add(control : Control, child : Control)"></endpoint>
<signature id="Control.child_add+2">Control.child_add(**control**: `Control`, **child**: `Control`)
<a class="headerlink" href="#Control.child_add+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Make a control the child control of another control.
> This means the childs position will be relative to its parent, layout depends a lot on those relationships and its used by functions like destroy_children.
> 
> ```js
>   //create parent
>   var parent = Control.create(_ui)
>   Control.set_bounds(parent, 200, 200, 100, 100)
>   //create child
>   var child = Control.create(_ui)
>   Control.set_bounds(child, 25, 25, 50, 50)
> 
>   //parent child to parent
>   Control.child_add(parent, child)
> 
>   var bounds = [0,0,0,0]
>   Control.get_bounds_abs(child, bounds)
>   Log.print(bounds) //[225, 225, 50, 50]
> 
>   Control.clear(parent, UIClear.destroy)
>   Log.print(Control.child_count(parent)) //0
>   Log.print(Control.valid(child)) //false
> 
>   UI.commit(_ui)
> ```   

<endpoint module="luxe: ui/control" class="Control" signature="child_remove(control : Control, child : Control)"></endpoint>
<signature id="Control.child_remove+2">Control.child_remove(**control**: `Control`, **child**: `Control`)
<a class="headerlink" href="#Control.child_remove+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Remove a child from a control, unparenting it.   

<endpoint module="luxe: ui/control" class="Control" signature="children_bounds(control : Control, into : List)"></endpoint>
<signature id="Control.children_bounds+2">Control.children_bounds(**control**: `Control`, **into**: `List`)
<a class="headerlink" href="#Control.children_bounds+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Get the combined bounds of all children of a control into a list `[x, y, width, height]`.
> The passed list must have at least 4 elements and the function will write into the first 4.
> Passing a list into the function instead of returning a value is to avoid allocating memory where not needed.   

<endpoint module="luxe: ui/control" class="Control" signature="set_behave(control : Control, behave : UIBehave)"></endpoint>
<signature id="Control.set_behave+2">Control.set_behave(**control**: `Control`, **behave**: `UIBehave`)
<a class="headerlink" href="#Control.set_behave+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set how the control behaves in the layout as a child of its container.
> You can combine characteristics with a bit or operator (`|`).   

<endpoint module="luxe: ui/control" class="Control" signature="get_behave(control : Control)"></endpoint>
<signature id="Control.get_behave">Control.get_behave(**control**: `Control`)
<a class="headerlink" href="#Control.get_behave" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js UIBehave`
> Returns the behave bitflags for the control   

<endpoint module="luxe: ui/control" class="Control" signature="set_contain(control : Control, contain : UIContain)"></endpoint>
<signature id="Control.set_contain+2">Control.set_contain(**control**: `Control`, **contain**: `UIContain`)
<a class="headerlink" href="#Control.set_contain+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set how the control behaves in the layout as a container of its children.
> You can combine characteristics with a bit or operator (`|`).   

<endpoint module="luxe: ui/control" class="Control" signature="get_contain(control : Control)"></endpoint>
<signature id="Control.get_contain">Control.get_contain(**control**: `Control`)
<a class="headerlink" href="#Control.get_contain" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js UIContain`
> Returns the contain bitflags for the control   

<endpoint module="luxe: ui/control" class="Control" signature="set_margin(control : Control, left : Num, top : Num, right : Num, bottom : Num)"></endpoint>
<signature id="Control.set_margin+5">Control.set_margin(**control**: `Control`, **left**: `Num`, **top**: `Num`, **right**: `Num`, **bottom**: `Num`)
<a class="headerlink" href="#Control.set_margin+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the margins of a control. Only the margins set in `set_behave` are actually observed.   

<endpoint module="luxe: ui/control" class="Control" signature="set_limits(control : Control, min_x : Num, min_y : Num, max_x : Num, max_y : Num)"></endpoint>
<signature id="Control.set_limits+5">Control.set_limits(**control**: `Control`, **min_x**: `Num`, **min_y**: `Num`, **max_x**: `Num`, **max_y**: `Num`)
<a class="headerlink" href="#Control.set_limits+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the min and max size of a control when using layout.   

<endpoint module="luxe: ui/control" class="Control" signature="get_margin(control : Control)"></endpoint>
<signature id="Control.get_margin">Control.get_margin(**control**: `Control`)
<a class="headerlink" href="#Control.get_margin" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> Get the margins of a control.   

<endpoint module="luxe: ui/control" class="Control" signature="set_render(control : Control, fn : Fn)"></endpoint>
<signature id="Control.set_render+2">Control.set_render(**control**: `Control`, **fn**: `Fn`)
<a class="headerlink" href="#Control.set_render+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set a custom render function with the arguments `|control, state, x, y, w, h|`. 
> Useful for making your own controls.   

<endpoint module="luxe: ui/control" class="Control" signature="set_events(control : Control, fn : Fn)"></endpoint>
<signature id="Control.set_events+2">Control.set_events(**control**: `Control`, **fn**: `Fn`)
<a class="headerlink" href="#Control.set_events+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Add a function to handle events on a control.
> Returns an `id` for the newly added event that can be used to remove it.
> 
> ```js
>   var btn = UIButton.create(ui)
>   UIButton.set_text(btn, "click me!")
>   Control.set_events(btn) {|event|
>     if(event.type == UIEvent.release) {
>       Log.print("clicked button")
>     }
>   }
> ```   

<endpoint module="luxe: ui/control" class="Control" signature="unset_events(control : Control, id : String)"></endpoint>
<signature id="Control.unset_events+2">Control.unset_events(**control**: `Control`, **id**: `String`)
<a class="headerlink" href="#Control.unset_events+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Remove an event handling function from a control.
> Takes in the id that was returned upon registering the function.   

<endpoint module="luxe: ui/control" class="Control" signature="set_process(control : Control, fn : Fn)"></endpoint>
<signature id="Control.set_process+2">Control.set_process(**control**: `Control`, **fn**: `Fn`)
<a class="headerlink" href="#Control.set_process+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set a custom process function with the arguments `|control, state, event, x, y, w, h|`. 
> Useful for making your own controls.   

<endpoint module="luxe: ui/control" class="Control" signature="get_state_data(control : Control)"></endpoint>
<signature id="Control.get_state_data">Control.get_state_data(**control**: `Control`)
<a class="headerlink" href="#Control.get_state_data" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Any`
> Get the state data associated with this control.   

<endpoint module="luxe: ui/control" class="Control" signature="set_state_data(control : Control, data : Any)"></endpoint>
<signature id="Control.set_state_data+2">Control.set_state_data(**control**: `Control`, **data**: `Any`)
<a class="headerlink" href="#Control.set_state_data+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set state data associated with this control.
> Can be any wren object.   

