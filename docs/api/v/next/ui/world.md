#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2024.12.4`)  


---

## `luxe: ui/world` module

- [BucketKind](#bucketkind)   
- [TreeNodeIter](#treenodeiter)   
- [UIWorld](#uiworld)   
- [UIWorldEvent](#uiworldevent)   
- [UIWorldIcon](#uiworldicon)   

---

### BucketKind
`:::js import "luxe: ui/world" for BucketKind`
> no docs found

- [folders](#BucketKind.folders)
- [contexts](#BucketKind.contexts)
- [entities](#BucketKind.entities)
- [name](#BucketKind.name)(**value**: `Any`)

<hr/>
<endpoint module="luxe: ui/world" class="BucketKind" signature="folders"></endpoint>
<signature id="BucketKind.folders">BucketKind.folders
<a class="headerlink" href="#BucketKind.folders" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="BucketKind" signature="contexts"></endpoint>
<signature id="BucketKind.contexts">BucketKind.contexts
<a class="headerlink" href="#BucketKind.contexts" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="BucketKind" signature="entities"></endpoint>
<signature id="BucketKind.entities">BucketKind.entities
<a class="headerlink" href="#BucketKind.entities" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="BucketKind" signature="name(value : Any)"></endpoint>
<signature id="BucketKind.name">BucketKind.name(**value**: `Any`)
<a class="headerlink" href="#BucketKind.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### TreeNodeIter
`:::js import "luxe: ui/world" for TreeNodeIter`
> no docs found

- [node](#TreeNodeIter.node)
- [new](#TreeNodeIter.new+2)(**node**: `TreeNode`, **depth**: `Num`)
- [iteratorValue](#TreeNodeIter.iteratorValue)(**index**: `Num`)
- [next_bucket](#TreeNodeIter.next_bucket)(**from_start**: `Bool`)
- [iterate](#TreeNodeIter.iterate)(**index**: `Num`)

<hr/>
<endpoint module="luxe: ui/world" class="TreeNodeIter" signature="node"></endpoint>
<signature id="TreeNodeIter.node">TreeNodeIter.node
<a class="headerlink" href="#TreeNodeIter.node" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js TreeNode`
> no docs found   

<endpoint module="luxe: ui/world" class="TreeNodeIter" signature="new(node : TreeNode, depth : Num)"></endpoint>
<signature id="TreeNodeIter.new+2">TreeNodeIter.new(**node**: `TreeNode`, **depth**: `Num`)
<a class="headerlink" href="#TreeNodeIter.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js TreeNodeIter`
> no docs found   

<endpoint module="luxe: ui/world" class="TreeNodeIter" signature="iteratorValue(index : Num)"></endpoint>
<signature id="TreeNodeIter.iteratorValue">TreeNodeIter.iteratorValue(**index**: `Num`)
<a class="headerlink" href="#TreeNodeIter.iteratorValue" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="TreeNodeIter" signature="next_bucket(from_start : Bool)"></endpoint>
<signature id="TreeNodeIter.next_bucket">TreeNodeIter.next_bucket(**from_start**: `Bool`)
<a class="headerlink" href="#TreeNodeIter.next_bucket" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: ui/world" class="TreeNodeIter" signature="iterate(index : Num)"></endpoint>
<signature id="TreeNodeIter.iterate">TreeNodeIter.iterate(**index**: `Num`)
<a class="headerlink" href="#TreeNodeIter.iterate" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### UIWorld
`:::js import "luxe: ui/world" for UIWorld`
> no docs found

- [create](#UIWorld.create)(**ui**: `UI`)
- [set_world](#UIWorld.set_world+2)(**control**: `Control`, **world**: `World`)
- [set_handle_default_icons](#UIWorld.set_handle_default_icons+2)(**control**: `Control`, **enable**: `Bool`)
- [refresh](#UIWorld.refresh)(**control**: `Control`)
- [get_view](#UIWorld.get_view)(**control**: `Control`)
- [scroll_to](#UIWorld.scroll_to+2)(**control**: `Control`, **entity**: `Entity`)
- [set_selection](#UIWorld.set_selection+2)(**control**: `Control`, **selection**: `Selection`)
- [get_selection](#UIWorld.get_selection)(**control**: `Control`)
- [enter_select_mode](#UIWorld.enter_select_mode+3)(**control**: `Control`, **enter_state**: `Bool`, **display**: `String`)
- [show_rename](#UIWorld.show_rename)(**control**: `Control`)

<hr/>
<endpoint module="luxe: ui/world" class="UIWorld" signature="create(ui : UI)"></endpoint>
<signature id="UIWorld.create">UIWorld.create(**ui**: `UI`)
<a class="headerlink" href="#UIWorld.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Control`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorld" signature="set_world(control : Control, world : World)"></endpoint>
<signature id="UIWorld.set_world+2">UIWorld.set_world(**control**: `Control`, **world**: `World`)
<a class="headerlink" href="#UIWorld.set_world+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorld" signature="set_handle_default_icons(control : Control, enable : Bool)"></endpoint>
<signature id="UIWorld.set_handle_default_icons+2">UIWorld.set_handle_default_icons(**control**: `Control`, **enable**: `Bool`)
<a class="headerlink" href="#UIWorld.set_handle_default_icons+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorld" signature="refresh(control : Control)"></endpoint>
<signature id="UIWorld.refresh">UIWorld.refresh(**control**: `Control`)
<a class="headerlink" href="#UIWorld.refresh" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorld" signature="get_view(control : Control)"></endpoint>
<signature id="UIWorld.get_view">UIWorld.get_view(**control**: `Control`)
<a class="headerlink" href="#UIWorld.get_view" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorld" signature="scroll_to(control : Control, entity : Entity)"></endpoint>
<signature id="UIWorld.scroll_to+2">UIWorld.scroll_to(**control**: `Control`, **entity**: `Entity`)
<a class="headerlink" href="#UIWorld.scroll_to+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorld" signature="set_selection(control : Control, selection : Selection)"></endpoint>
<signature id="UIWorld.set_selection+2">UIWorld.set_selection(**control**: `Control`, **selection**: `Selection`)
<a class="headerlink" href="#UIWorld.set_selection+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorld" signature="get_selection(control : Control)"></endpoint>
<signature id="UIWorld.get_selection">UIWorld.get_selection(**control**: `Control`)
<a class="headerlink" href="#UIWorld.get_selection" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Selection`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorld" signature="enter_select_mode(control : Control, enter_state : Bool, display : String)"></endpoint>
<signature id="UIWorld.enter_select_mode+3">UIWorld.enter_select_mode(**control**: `Control`, **enter_state**: `Bool`, **display**: `String`)
<a class="headerlink" href="#UIWorld.enter_select_mode+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorld" signature="show_rename(control : Control)"></endpoint>
<signature id="UIWorld.show_rename">UIWorld.show_rename(**control**: `Control`)
<a class="headerlink" href="#UIWorld.show_rename" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### UIWorldEvent
`:::js import "luxe: ui/world" for UIWorldEvent`
> no docs found

- [filter](#UIWorldEvent.filter)
- [save](#UIWorldEvent.save)
- [save_all](#UIWorldEvent.save_all)
- [delete](#UIWorldEvent.delete)
- [duplicate](#UIWorldEvent.duplicate)
- [rename](#UIWorldEvent.rename)
- [active_context](#UIWorldEvent.active_context)
- [focus](#UIWorldEvent.focus)
- [close](#UIWorldEvent.close)
- [kind](#UIWorldEvent.kind)
- [items](#UIWorldEvent.items)
- [data](#UIWorldEvent.data)
- [new](#UIWorldEvent.new+3)(**kind**: `UIWorldEvent`, **items**: `List`, **data**: `Any`)

<hr/>
<endpoint module="luxe: ui/world" class="UIWorldEvent" signature="filter"></endpoint>
<signature id="UIWorldEvent.filter">UIWorldEvent.filter
<a class="headerlink" href="#UIWorldEvent.filter" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldEvent" signature="save"></endpoint>
<signature id="UIWorldEvent.save">UIWorldEvent.save
<a class="headerlink" href="#UIWorldEvent.save" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldEvent" signature="save_all"></endpoint>
<signature id="UIWorldEvent.save_all">UIWorldEvent.save_all
<a class="headerlink" href="#UIWorldEvent.save_all" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldEvent" signature="delete"></endpoint>
<signature id="UIWorldEvent.delete">UIWorldEvent.delete
<a class="headerlink" href="#UIWorldEvent.delete" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldEvent" signature="duplicate"></endpoint>
<signature id="UIWorldEvent.duplicate">UIWorldEvent.duplicate
<a class="headerlink" href="#UIWorldEvent.duplicate" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldEvent" signature="rename"></endpoint>
<signature id="UIWorldEvent.rename">UIWorldEvent.rename
<a class="headerlink" href="#UIWorldEvent.rename" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldEvent" signature="active_context"></endpoint>
<signature id="UIWorldEvent.active_context">UIWorldEvent.active_context
<a class="headerlink" href="#UIWorldEvent.active_context" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldEvent" signature="focus"></endpoint>
<signature id="UIWorldEvent.focus">UIWorldEvent.focus
<a class="headerlink" href="#UIWorldEvent.focus" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldEvent" signature="close"></endpoint>
<signature id="UIWorldEvent.close">UIWorldEvent.close
<a class="headerlink" href="#UIWorldEvent.close" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldEvent" signature="kind"></endpoint>
<signature id="UIWorldEvent.kind">UIWorldEvent.kind
<a class="headerlink" href="#UIWorldEvent.kind" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Any`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldEvent" signature="items"></endpoint>
<signature id="UIWorldEvent.items">UIWorldEvent.items
<a class="headerlink" href="#UIWorldEvent.items" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Any`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldEvent" signature="data"></endpoint>
<signature id="UIWorldEvent.data">UIWorldEvent.data
<a class="headerlink" href="#UIWorldEvent.data" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Any`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldEvent" signature="new(kind : UIWorldEvent, items : List, data : Any)"></endpoint>
<signature id="UIWorldEvent.new+3">UIWorldEvent.new(**kind**: `UIWorldEvent`, **items**: `List`, **data**: `Any`)
<a class="headerlink" href="#UIWorldEvent.new+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js UIWorldEvent`
> no docs found   

### UIWorldIcon
`:::js import "luxe: ui/world" for UIWorldIcon`
> no docs found

- [icon](#UIWorldIcon.icon)
- [enabled](#UIWorldIcon.enabled)
- [enabled](#UIWorldIcon.enabled)(**handle**: `Num`)
- [tooltip](#UIWorldIcon.tooltip)
- [tooltip](#UIWorldIcon.tooltip=)=(v : String)
- [selection_based](#UIWorldIcon.selection_based)
- [selection_based](#UIWorldIcon.selection_based=)=(v : String)
- [allow_indirect](#UIWorldIcon.allow_indirect)
- [allow_indirect](#UIWorldIcon.allow_indirect=)=(v : String)
- [svg](#UIWorldIcon.svg)
- [svg](#UIWorldIcon.svg=)=(v : Any)
- [new](#UIWorldIcon.new)(**world_view**: `UIWorld`)
- [enable](#UIWorldIcon.enable)()
- [enable](#UIWorldIcon.enable)(**handle**: `Num`)
- [disable](#UIWorldIcon.disable)()
- [disable](#UIWorldIcon.disable)(**handle**: `Num`)
- [can_do_direct_only_action](#UIWorldIcon.can_do_direct_only_action)(**list**: `List`)
- [on_selection](#UIWorldIcon.on_selection)(**fn**: `Fn`)
- [on_release](#UIWorldIcon.on_release)(**fn**: `Fn`)
- [on_enter](#UIWorldIcon.on_enter)(**fn**: `Fn`)
- [on_exit](#UIWorldIcon.on_exit)(**fn**: `Fn`)

<hr/>
<endpoint module="luxe: ui/world" class="UIWorldIcon" signature="icon"></endpoint>
<signature id="UIWorldIcon.icon">UIWorldIcon.icon
<a class="headerlink" href="#UIWorldIcon.icon" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Control`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldIcon" signature="enabled"></endpoint>
<signature id="UIWorldIcon.enabled">UIWorldIcon.enabled
<a class="headerlink" href="#UIWorldIcon.enabled" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldIcon" signature="enabled(handle : Num)"></endpoint>
<signature id="UIWorldIcon.enabled">UIWorldIcon.enabled(**handle**: `Num`)
<a class="headerlink" href="#UIWorldIcon.enabled" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldIcon" signature="tooltip"></endpoint>
<signature id="UIWorldIcon.tooltip">UIWorldIcon.tooltip
<a class="headerlink" href="#UIWorldIcon.tooltip" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldIcon" signature="tooltip=(v : String)"></endpoint>
<signature id="UIWorldIcon.tooltip=">UIWorldIcon.tooltip=(v : String)
<a class="headerlink" href="#UIWorldIcon.tooltip=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldIcon" signature="selection_based"></endpoint>
<signature id="UIWorldIcon.selection_based">UIWorldIcon.selection_based
<a class="headerlink" href="#UIWorldIcon.selection_based" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldIcon" signature="selection_based=(v : String)"></endpoint>
<signature id="UIWorldIcon.selection_based=">UIWorldIcon.selection_based=(v : String)
<a class="headerlink" href="#UIWorldIcon.selection_based=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldIcon" signature="allow_indirect"></endpoint>
<signature id="UIWorldIcon.allow_indirect">UIWorldIcon.allow_indirect
<a class="headerlink" href="#UIWorldIcon.allow_indirect" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldIcon" signature="allow_indirect=(v : String)"></endpoint>
<signature id="UIWorldIcon.allow_indirect=">UIWorldIcon.allow_indirect=(v : String)
<a class="headerlink" href="#UIWorldIcon.allow_indirect=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldIcon" signature="svg"></endpoint>
<signature id="UIWorldIcon.svg">UIWorldIcon.svg
<a class="headerlink" href="#UIWorldIcon.svg" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldIcon" signature="svg=(v : Any)"></endpoint>
<signature id="UIWorldIcon.svg=">UIWorldIcon.svg=(v : Any)
<a class="headerlink" href="#UIWorldIcon.svg=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldIcon" signature="new(world_view : UIWorld)"></endpoint>
<signature id="UIWorldIcon.new">UIWorldIcon.new(**world_view**: `UIWorld`)
<a class="headerlink" href="#UIWorldIcon.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js UIWorldIcon`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldIcon" signature="enable()"></endpoint>
<signature id="UIWorldIcon.enable">UIWorldIcon.enable()
<a class="headerlink" href="#UIWorldIcon.enable" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldIcon" signature="enable(handle : Num)"></endpoint>
<signature id="UIWorldIcon.enable">UIWorldIcon.enable(**handle**: `Num`)
<a class="headerlink" href="#UIWorldIcon.enable" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldIcon" signature="disable()"></endpoint>
<signature id="UIWorldIcon.disable">UIWorldIcon.disable()
<a class="headerlink" href="#UIWorldIcon.disable" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldIcon" signature="disable(handle : Num)"></endpoint>
<signature id="UIWorldIcon.disable">UIWorldIcon.disable(**handle**: `Num`)
<a class="headerlink" href="#UIWorldIcon.disable" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldIcon" signature="can_do_direct_only_action(list : List)"></endpoint>
<signature id="UIWorldIcon.can_do_direct_only_action">UIWorldIcon.can_do_direct_only_action(**list**: `List`)
<a class="headerlink" href="#UIWorldIcon.can_do_direct_only_action" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldIcon" signature="on_selection(fn : Fn)"></endpoint>
<signature id="UIWorldIcon.on_selection">UIWorldIcon.on_selection(**fn**: `Fn`)
<a class="headerlink" href="#UIWorldIcon.on_selection" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldIcon" signature="on_release(fn : Fn)"></endpoint>
<signature id="UIWorldIcon.on_release">UIWorldIcon.on_release(**fn**: `Fn`)
<a class="headerlink" href="#UIWorldIcon.on_release" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldIcon" signature="on_enter(fn : Fn)"></endpoint>
<signature id="UIWorldIcon.on_enter">UIWorldIcon.on_enter(**fn**: `Fn`)
<a class="headerlink" href="#UIWorldIcon.on_enter" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/world" class="UIWorldIcon" signature="on_exit(fn : Fn)"></endpoint>
<signature id="UIWorldIcon.on_exit">UIWorldIcon.on_exit(**fn**: `Fn`)
<a class="headerlink" href="#UIWorldIcon.on_exit" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

