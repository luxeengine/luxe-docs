#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2025.1.1`)  


---

## `luxe: system/wires.modifier` module

- [Connection](#connection)   
- [Data](#data)   
- [System](#system)   
- [WireNode](#wirenode)   
- [WireTarget](#wiretarget)   
- [Wires](#wires)   

---

### Connection
`:::js import "luxe: system/wires.modifier" for Connection`
> no docs found

- `:::js var from : WireTarget = Object`
- `:::js var to : WireTarget = Object`

<hr/>
### Data
`:::js import "luxe: system/wires.modifier" for Data`
> no docs found

- `:::js var connections : List = []`

<hr/>
### System
`:::js import "luxe: system/wires.modifier" for System`
> no docs found

- `:::js var nodes : Map = {}`
- `:::js var nodes_from_panel : Map = {}`
- `:::js var right_panel : Control = 0`
- `:::js var left_panel : Control = 0`
- `:::js var world_editor : Any = null`
- [new](#System.new)(**world**: `World`)
- [init](#System.init)(**world**: `World`)
- [copy_target](#System.copy_target+2)(**src**: `WireTarget`, **to**: `WireTarget`)
- [refresh_entity](#System.refresh_entity)(**node**: `WireNode`)
- [get_drop_node](#System.get_drop_node+2)(**x**: `Num`, **y**: `Num`)
- [remove_block_connection](#System.remove_block_connection+2)(**entity**: `Entity`, **target**: `WireTarget`)
- [find_connection_index](#System.find_connection_index+2)(**entity**: `Entity`, **target**: `WireTarget`)
- [find_wire_in_list](#System.find_wire_in_list+2)(**wires**: `List`, **wire_id**: `Num`)
- [find_wire](#System.find_wire)(**target**: `WireTarget`)
- [make_placeholder_wire](#System.make_placeholder_wire+2)(**entity**: `Entity`, **do_doc**: `Bool`)
- [make_node](#System.make_node+4)(**out**: `Bool`, **entity**: `Entity`, **from**: `WireTarget`, **to**: `WireTarget`)
- [refresh_wires](#System.refresh_wires+3)(**window**: `UIPanel`, **window_w**: `Num`, **but**: `UIButton`)
- [editor_init](#System.editor_init)(**world**: `World`)
- [editor_attach](#System.editor_attach+2)(**entity**: `Entity`, **wires**: `Data`)

<hr/>
<endpoint module="luxe: system/wires.modifier" class="System" signature="new(world : World)"></endpoint>
<signature id="System.new">System.new(**world**: `World`)
<a class="headerlink" href="#System.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js System`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="System" signature="init(world : World)"></endpoint>
<signature id="System.init">System.init(**world**: `World`)
<a class="headerlink" href="#System.init" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="System" signature="copy_target(src : WireTarget, to : WireTarget)"></endpoint>
<signature id="System.copy_target+2">System.copy_target(**src**: `WireTarget`, **to**: `WireTarget`)
<a class="headerlink" href="#System.copy_target+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="System" signature="refresh_entity(node : WireNode)"></endpoint>
<signature id="System.refresh_entity">System.refresh_entity(**node**: `WireNode`)
<a class="headerlink" href="#System.refresh_entity" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="System" signature="get_drop_node(x : Num, y : Num)"></endpoint>
<signature id="System.get_drop_node+2">System.get_drop_node(**x**: `Num`, **y**: `Num`)
<a class="headerlink" href="#System.get_drop_node+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js WireNode`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="System" signature="remove_block_connection(entity : Entity, target : WireTarget)"></endpoint>
<signature id="System.remove_block_connection+2">System.remove_block_connection(**entity**: `Entity`, **target**: `WireTarget`)
<a class="headerlink" href="#System.remove_block_connection+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="System" signature="find_connection_index(entity : Entity, target : WireTarget)"></endpoint>
<signature id="System.find_connection_index+2">System.find_connection_index(**entity**: `Entity`, **target**: `WireTarget`)
<a class="headerlink" href="#System.find_connection_index+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="System" signature="find_wire_in_list(wires : List, wire_id : Num)"></endpoint>
<signature id="System.find_wire_in_list+2">System.find_wire_in_list(**wires**: `List`, **wire_id**: `Num`)
<a class="headerlink" href="#System.find_wire_in_list+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="System" signature="find_wire(target : WireTarget)"></endpoint>
<signature id="System.find_wire">System.find_wire(**target**: `WireTarget`)
<a class="headerlink" href="#System.find_wire" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="System" signature="make_placeholder_wire(entity : Entity, do_doc : Bool)"></endpoint>
<signature id="System.make_placeholder_wire+2">System.make_placeholder_wire(**entity**: `Entity`, **do_doc**: `Bool`)
<a class="headerlink" href="#System.make_placeholder_wire+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Connection`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="System" signature="make_node(out : Bool, entity : Entity, from : WireTarget, to : WireTarget)"></endpoint>
<signature id="System.make_node+4">System.make_node(**out**: `Bool`, **entity**: `Entity`, **from**: `WireTarget`, **to**: `WireTarget`)
<a class="headerlink" href="#System.make_node+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="System" signature="refresh_wires(window : UIPanel, window_w : Num, but : UIButton)"></endpoint>
<signature id="System.refresh_wires+3">System.refresh_wires(**window**: `UIPanel`, **window_w**: `Num`, **but**: `UIButton`)
<a class="headerlink" href="#System.refresh_wires+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="System" signature="editor_init(world : World)"></endpoint>
<signature id="System.editor_init">System.editor_init(**world**: `World`)
<a class="headerlink" href="#System.editor_init" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="System" signature="editor_attach(entity : Entity, wires : Data)"></endpoint>
<signature id="System.editor_attach+2">System.editor_attach(**entity**: `Entity`, **wires**: `Data`)
<a class="headerlink" href="#System.editor_attach+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### WireNode
`:::js import "luxe: system/wires.modifier" for WireNode`
> no docs found

- `:::js var uuid : String = ID.uuid`
- `:::js var panel : UIPanel = null`
- `:::js var entity : Entity = Entity.none`
- `:::js var out : Bool = true`
- `:::js var from : WireTarget = null`
- `:::js var to : WireTarget = null`
- `:::js var other_uuid : String = null`
- `:::js var label : UILabel = null`
- `:::js var change : UILabel = null`
- `:::js var icon : UIImage = null`
- `:::js var endpoint : Control = null`
- `:::js var cable_control : Control = null`
- `:::js var draw_control : Control = null`
- `:::js var resolve_node : Fn = null`
- `:::js var resolve_wire : Fn = null`
- `:::js var cable : Cable = Cable.new`
- `:::js var style : PathStyle = PathStyle.new`
- `:::js var cable_phase : Num = 0`
- `:::js var cable_drag : Bool = false`
- [valid_wire](#WireNode.valid_wire)
- [wire](#WireNode.wire)
- [draw_depth](#WireNode.draw_depth)
- [order](#WireNode.order)
- [disconnect](#WireNode.disconnect)()
- [new](#WireNode.new)()
- [destroy](#WireNode.destroy)()
- [highlight](#WireNode.highlight)(**state**: `Bool`)
- [from_entity](#WireNode.from_entity)
- [to_entity](#WireNode.to_entity)
- [from_node](#WireNode.from_node)
- [to_node](#WireNode.to_node)
- [make_cable](#WireNode.make_cable)()

<hr/>
<endpoint module="luxe: system/wires.modifier" class="WireNode" signature="valid_wire"></endpoint>
<signature id="WireNode.valid_wire">WireNode.valid_wire
<a class="headerlink" href="#WireNode.valid_wire" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="WireNode" signature="wire"></endpoint>
<signature id="WireNode.wire">WireNode.wire
<a class="headerlink" href="#WireNode.wire" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js WireData`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="WireNode" signature="draw_depth"></endpoint>
<signature id="WireNode.draw_depth">WireNode.draw_depth
<a class="headerlink" href="#WireNode.draw_depth" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="WireNode" signature="order"></endpoint>
<signature id="WireNode.order">WireNode.order
<a class="headerlink" href="#WireNode.order" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="WireNode" signature="disconnect()"></endpoint>
<signature id="WireNode.disconnect">WireNode.disconnect()
<a class="headerlink" href="#WireNode.disconnect" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="WireNode" signature="new()"></endpoint>
<signature id="WireNode.new">WireNode.new()
<a class="headerlink" href="#WireNode.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js WireNode`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="WireNode" signature="destroy()"></endpoint>
<signature id="WireNode.destroy">WireNode.destroy()
<a class="headerlink" href="#WireNode.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="WireNode" signature="highlight(state : Bool)"></endpoint>
<signature id="WireNode.highlight">WireNode.highlight(**state**: `Bool`)
<a class="headerlink" href="#WireNode.highlight" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="WireNode" signature="from_entity"></endpoint>
<signature id="WireNode.from_entity">WireNode.from_entity
<a class="headerlink" href="#WireNode.from_entity" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="WireNode" signature="to_entity"></endpoint>
<signature id="WireNode.to_entity">WireNode.to_entity
<a class="headerlink" href="#WireNode.to_entity" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="WireNode" signature="from_node"></endpoint>
<signature id="WireNode.from_node">WireNode.from_node
<a class="headerlink" href="#WireNode.from_node" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js WireNode`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="WireNode" signature="to_node"></endpoint>
<signature id="WireNode.to_node">WireNode.to_node
<a class="headerlink" href="#WireNode.to_node" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js WireNode`
> no docs found   

<endpoint module="luxe: system/wires.modifier" class="WireNode" signature="make_cable()"></endpoint>
<signature id="WireNode.make_cable">WireNode.make_cable()
<a class="headerlink" href="#WireNode.make_cable" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### WireTarget
`:::js import "luxe: system/wires.modifier" for WireTarget`
> no docs found

- `:::js var wire : Num = 0`
- `:::js var link : Link = null`
- `:::js var context : Asset = null`
- `:::js var order : Num = 0`
- `:::js var split : Bool = false`

<hr/>
### Wires
`:::js import "luxe: system/wires.modifier" for Wires`
> no docs found


<hr/>
