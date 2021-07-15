#![](../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2021.0.5`)  


---

## `luxe: ui/control` module

- [Control](#control)   

---

### Control
`:::js import "luxe: ui/control" for Control`
> no docs found

- [create](#Control.create)(**ui_entity**: `Any`)
- [destroy](#Control.destroy)(**control**: `Any`)
- [destroy_children](#Control.destroy_children)(**control**: `Any`)
- [valid](#Control.valid)(**control**: `Any`)
- [get](#Control.get)(**id**: `Any`)
- [exists](#Control.exists)(**id**: `Any`)
- [clear](#Control.clear+2)(**control**: `Any`, **uiclear_action**: `Any`)
- [set_type](#Control.set_type+2)(**control**: `Any`, **type**: `Any`)
- [get_type](#Control.get_type)(**control**: `Any`)
- [set_id](#Control.set_id+2)(**control**: `Any`, **id**: `Any`)
- [get_id](#Control.get_id)(**control**: `Any`)
- [get_bounds_abs](#Control.get_bounds_abs+2)(**control**: `Any`, **into**: `Any`)
- [get_bounds](#Control.get_bounds+2)(**control**: `Any`, **into**: `Any`)
- [set_bounds_abs](#Control.set_bounds_abs+5)(**control**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`)
- [set_bounds](#Control.set_bounds+5)(**control**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`)
- [set_pos_abs](#Control.set_pos_abs+3)(**control**: `Any`, **x**: `Any`, **y**: `Any`)
- [set_pos](#Control.set_pos+3)(**control**: `Any`, **x**: `Any`, **y**: `Any`)
- [set_size](#Control.set_size+3)(**control**: `Any`, **w**: `Any`, **h**: `Any`)
- [get_pos_x](#Control.get_pos_x)(**control**: `Any`)
- [get_pos_x_abs](#Control.get_pos_x_abs)(**control**: `Any`)
- [get_pos_y](#Control.get_pos_y)(**control**: `Any`)
- [get_pos_y_abs](#Control.get_pos_y_abs)(**control**: `Any`)
- [get_width](#Control.get_width)(**control**: `Any`)
- [get_height](#Control.get_height)(**control**: `Any`)
- [contains](#Control.contains+3)(**control**: `Any`, **x**: `Any`, **y**: `Any`)
- [get_entity](#Control.get_entity)(**control**: `Any`)
- [get_parent](#Control.get_parent)(**control**: `Any`)
- [get_allow_input](#Control.get_allow_input)(**control**: `Any`)
- [set_allow_input](#Control.set_allow_input+2)(**control**: `Any`, **allow**: `Any`)
- [get_allow_keys](#Control.get_allow_keys)(**control**: `Any`)
- [set_allow_keys](#Control.set_allow_keys+2)(**control**: `Any`, **allow**: `Any`)
- [get_visible](#Control.get_visible)(**control**: `Any`)
- [set_visible](#Control.set_visible+2)(**control**: `Any`, **visible**: `Any`)
- [get_disabled](#Control.get_disabled)(**control**: `Any`)
- [set_disabled](#Control.set_disabled+2)(**control**: `Any`, **disabled**: `Any`)
- [get_clip](#Control.get_clip)(**control**: `Any`)
- [set_clip](#Control.set_clip+2)(**control**: `Any`, **clip**: `Any`)
- [get_nodes](#Control.get_nodes)(**control**: `Any`)
- [get_depth](#Control.get_depth)(**control**: `Any`)
- [get_depth_offset](#Control.get_depth_offset)(**control**: `Any`)
- [set_depth_offset](#Control.set_depth_offset+2)(**control**: `Any`, **depth_offset**: `Any`)
- [get_input_inside](#Control.get_input_inside)(**control**: `Any`)
- [get_input_pressed](#Control.get_input_pressed)(**control**: `Any`)
- [child_at_point](#Control.child_at_point+3)(**control**: `Any`, **x**: `Any`, **y**: `Any`)
- [child_count](#Control.child_count)(**control**: `Any`)
- [child_index](#Control.child_index+2)(**control**: `Any`, **child**: `Any`)
- [child_get](#Control.child_get+2)(**control**: `Any`, **index**: `Any`)
- [child_add](#Control.child_add+3)(**control**: `Any`, **child**: `Any`, **internal**: `Any`)
- [child_add](#Control.child_add+2)(**control**: `Any`, **child**: `Any`)
- [child_remove](#Control.child_remove+2)(**control**: `Any`, **child**: `Any`)
- [children_bounds](#Control.children_bounds+2)(**control**: `Any`, **into**: `Any`)
- [set_render](#Control.set_render+2)(**control**: `Any`, **fn**: `Any`)
- [set_events](#Control.set_events+2)(**control**: `Any`, **fn**: `Any`)
- [unset_events](#Control.unset_events+2)(**control**: `Any`, **id**: `Any`)
- [set_process](#Control.set_process+2)(**control**: `Any`, **fn**: `Any`)
- [get_state_data](#Control.get_state_data)(**control**: `Any`)
- [set_state_data](#Control.set_state_data+2)(**control**: `Any`, **data**: `Any`)

<hr/>
<endpoint module="luxe: ui/control" class="Control" signature="create(ui_entity : Any)"></endpoint>
<signature id="Control.create">Control.create(**ui_entity**: `Any`)
<a class="headerlink" href="#Control.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="destroy(control : Any)"></endpoint>
<signature id="Control.destroy">Control.destroy(**control**: `Any`)
<a class="headerlink" href="#Control.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="destroy_children(control : Any)"></endpoint>
<signature id="Control.destroy_children">Control.destroy_children(**control**: `Any`)
<a class="headerlink" href="#Control.destroy_children" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="valid(control : Any)"></endpoint>
<signature id="Control.valid">Control.valid(**control**: `Any`)
<a class="headerlink" href="#Control.valid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get(id : Any)"></endpoint>
<signature id="Control.get">Control.get(**id**: `Any`)
<a class="headerlink" href="#Control.get" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="exists(id : Any)"></endpoint>
<signature id="Control.exists">Control.exists(**id**: `Any`)
<a class="headerlink" href="#Control.exists" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="clear(control : Any, uiclear_action : Any)"></endpoint>
<signature id="Control.clear+2">Control.clear(**control**: `Any`, **uiclear_action**: `Any`)
<a class="headerlink" href="#Control.clear+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="set_type(control : Any, type : Any)"></endpoint>
<signature id="Control.set_type+2">Control.set_type(**control**: `Any`, **type**: `Any`)
<a class="headerlink" href="#Control.set_type+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get_type(control : Any)"></endpoint>
<signature id="Control.get_type">Control.get_type(**control**: `Any`)
<a class="headerlink" href="#Control.get_type" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="set_id(control : Any, id : Any)"></endpoint>
<signature id="Control.set_id+2">Control.set_id(**control**: `Any`, **id**: `Any`)
<a class="headerlink" href="#Control.set_id+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get_id(control : Any)"></endpoint>
<signature id="Control.get_id">Control.get_id(**control**: `Any`)
<a class="headerlink" href="#Control.get_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get_bounds_abs(control : Any, into : Any)"></endpoint>
<signature id="Control.get_bounds_abs+2">Control.get_bounds_abs(**control**: `Any`, **into**: `Any`)
<a class="headerlink" href="#Control.get_bounds_abs+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get_bounds(control : Any, into : Any)"></endpoint>
<signature id="Control.get_bounds+2">Control.get_bounds(**control**: `Any`, **into**: `Any`)
<a class="headerlink" href="#Control.get_bounds+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="set_bounds_abs(control : Any, x : Any, y : Any, w : Any, h : Any)"></endpoint>
<signature id="Control.set_bounds_abs+5">Control.set_bounds_abs(**control**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`)
<a class="headerlink" href="#Control.set_bounds_abs+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="set_bounds(control : Any, x : Any, y : Any, w : Any, h : Any)"></endpoint>
<signature id="Control.set_bounds+5">Control.set_bounds(**control**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`)
<a class="headerlink" href="#Control.set_bounds+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="set_pos_abs(control : Any, x : Any, y : Any)"></endpoint>
<signature id="Control.set_pos_abs+3">Control.set_pos_abs(**control**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Control.set_pos_abs+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="set_pos(control : Any, x : Any, y : Any)"></endpoint>
<signature id="Control.set_pos+3">Control.set_pos(**control**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Control.set_pos+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="set_size(control : Any, w : Any, h : Any)"></endpoint>
<signature id="Control.set_size+3">Control.set_size(**control**: `Any`, **w**: `Any`, **h**: `Any`)
<a class="headerlink" href="#Control.set_size+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get_pos_x(control : Any)"></endpoint>
<signature id="Control.get_pos_x">Control.get_pos_x(**control**: `Any`)
<a class="headerlink" href="#Control.get_pos_x" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get_pos_x_abs(control : Any)"></endpoint>
<signature id="Control.get_pos_x_abs">Control.get_pos_x_abs(**control**: `Any`)
<a class="headerlink" href="#Control.get_pos_x_abs" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get_pos_y(control : Any)"></endpoint>
<signature id="Control.get_pos_y">Control.get_pos_y(**control**: `Any`)
<a class="headerlink" href="#Control.get_pos_y" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get_pos_y_abs(control : Any)"></endpoint>
<signature id="Control.get_pos_y_abs">Control.get_pos_y_abs(**control**: `Any`)
<a class="headerlink" href="#Control.get_pos_y_abs" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get_width(control : Any)"></endpoint>
<signature id="Control.get_width">Control.get_width(**control**: `Any`)
<a class="headerlink" href="#Control.get_width" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get_height(control : Any)"></endpoint>
<signature id="Control.get_height">Control.get_height(**control**: `Any`)
<a class="headerlink" href="#Control.get_height" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="contains(control : Any, x : Any, y : Any)"></endpoint>
<signature id="Control.contains+3">Control.contains(**control**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Control.contains+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get_entity(control : Any)"></endpoint>
<signature id="Control.get_entity">Control.get_entity(**control**: `Any`)
<a class="headerlink" href="#Control.get_entity" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get_parent(control : Any)"></endpoint>
<signature id="Control.get_parent">Control.get_parent(**control**: `Any`)
<a class="headerlink" href="#Control.get_parent" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get_allow_input(control : Any)"></endpoint>
<signature id="Control.get_allow_input">Control.get_allow_input(**control**: `Any`)
<a class="headerlink" href="#Control.get_allow_input" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="set_allow_input(control : Any, allow : Any)"></endpoint>
<signature id="Control.set_allow_input+2">Control.set_allow_input(**control**: `Any`, **allow**: `Any`)
<a class="headerlink" href="#Control.set_allow_input+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get_allow_keys(control : Any)"></endpoint>
<signature id="Control.get_allow_keys">Control.get_allow_keys(**control**: `Any`)
<a class="headerlink" href="#Control.get_allow_keys" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="set_allow_keys(control : Any, allow : Any)"></endpoint>
<signature id="Control.set_allow_keys+2">Control.set_allow_keys(**control**: `Any`, **allow**: `Any`)
<a class="headerlink" href="#Control.set_allow_keys+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get_visible(control : Any)"></endpoint>
<signature id="Control.get_visible">Control.get_visible(**control**: `Any`)
<a class="headerlink" href="#Control.get_visible" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="set_visible(control : Any, visible : Any)"></endpoint>
<signature id="Control.set_visible+2">Control.set_visible(**control**: `Any`, **visible**: `Any`)
<a class="headerlink" href="#Control.set_visible+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get_disabled(control : Any)"></endpoint>
<signature id="Control.get_disabled">Control.get_disabled(**control**: `Any`)
<a class="headerlink" href="#Control.get_disabled" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="set_disabled(control : Any, disabled : Any)"></endpoint>
<signature id="Control.set_disabled+2">Control.set_disabled(**control**: `Any`, **disabled**: `Any`)
<a class="headerlink" href="#Control.set_disabled+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get_clip(control : Any)"></endpoint>
<signature id="Control.get_clip">Control.get_clip(**control**: `Any`)
<a class="headerlink" href="#Control.get_clip" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="set_clip(control : Any, clip : Any)"></endpoint>
<signature id="Control.set_clip+2">Control.set_clip(**control**: `Any`, **clip**: `Any`)
<a class="headerlink" href="#Control.set_clip+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get_nodes(control : Any)"></endpoint>
<signature id="Control.get_nodes">Control.get_nodes(**control**: `Any`)
<a class="headerlink" href="#Control.get_nodes" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get_depth(control : Any)"></endpoint>
<signature id="Control.get_depth">Control.get_depth(**control**: `Any`)
<a class="headerlink" href="#Control.get_depth" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get_depth_offset(control : Any)"></endpoint>
<signature id="Control.get_depth_offset">Control.get_depth_offset(**control**: `Any`)
<a class="headerlink" href="#Control.get_depth_offset" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="set_depth_offset(control : Any, depth_offset : Any)"></endpoint>
<signature id="Control.set_depth_offset+2">Control.set_depth_offset(**control**: `Any`, **depth_offset**: `Any`)
<a class="headerlink" href="#Control.set_depth_offset+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get_input_inside(control : Any)"></endpoint>
<signature id="Control.get_input_inside">Control.get_input_inside(**control**: `Any`)
<a class="headerlink" href="#Control.get_input_inside" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get_input_pressed(control : Any)"></endpoint>
<signature id="Control.get_input_pressed">Control.get_input_pressed(**control**: `Any`)
<a class="headerlink" href="#Control.get_input_pressed" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="child_at_point(control : Any, x : Any, y : Any)"></endpoint>
<signature id="Control.child_at_point+3">Control.child_at_point(**control**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Control.child_at_point+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="child_count(control : Any)"></endpoint>
<signature id="Control.child_count">Control.child_count(**control**: `Any`)
<a class="headerlink" href="#Control.child_count" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="child_index(control : Any, child : Any)"></endpoint>
<signature id="Control.child_index+2">Control.child_index(**control**: `Any`, **child**: `Any`)
<a class="headerlink" href="#Control.child_index+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="child_get(control : Any, index : Any)"></endpoint>
<signature id="Control.child_get+2">Control.child_get(**control**: `Any`, **index**: `Any`)
<a class="headerlink" href="#Control.child_get+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="child_add(control : Any, child : Any, internal : Any)"></endpoint>
<signature id="Control.child_add+3">Control.child_add(**control**: `Any`, **child**: `Any`, **internal**: `Any`)
<a class="headerlink" href="#Control.child_add+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="child_add(control : Any, child : Any)"></endpoint>
<signature id="Control.child_add+2">Control.child_add(**control**: `Any`, **child**: `Any`)
<a class="headerlink" href="#Control.child_add+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="child_remove(control : Any, child : Any)"></endpoint>
<signature id="Control.child_remove+2">Control.child_remove(**control**: `Any`, **child**: `Any`)
<a class="headerlink" href="#Control.child_remove+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="children_bounds(control : Any, into : Any)"></endpoint>
<signature id="Control.children_bounds+2">Control.children_bounds(**control**: `Any`, **into**: `Any`)
<a class="headerlink" href="#Control.children_bounds+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="set_render(control : Any, fn : Any)"></endpoint>
<signature id="Control.set_render+2">Control.set_render(**control**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#Control.set_render+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="set_events(control : Any, fn : Any)"></endpoint>
<signature id="Control.set_events+2">Control.set_events(**control**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#Control.set_events+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="unset_events(control : Any, id : Any)"></endpoint>
<signature id="Control.unset_events+2">Control.unset_events(**control**: `Any`, **id**: `Any`)
<a class="headerlink" href="#Control.unset_events+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="set_process(control : Any, fn : Any)"></endpoint>
<signature id="Control.set_process+2">Control.set_process(**control**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#Control.set_process+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="get_state_data(control : Any)"></endpoint>
<signature id="Control.get_state_data">Control.get_state_data(**control**: `Any`)
<a class="headerlink" href="#Control.get_state_data" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/control" class="Control" signature="set_state_data(control : Any, data : Any)"></endpoint>
<signature id="Control.set_state_data+2">Control.set_state_data(**control**: `Any`, **data**: `Any`)
<a class="headerlink" href="#Control.set_state_data+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

