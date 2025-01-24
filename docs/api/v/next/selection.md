#![](../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2025.1.2`)  


---

## `luxe: selection` module

- [Selection](#selection)   

---

### Selection
`:::js import "luxe: selection" for Selection`
> no docs found

- [CHANGE](#Selection.CHANGE)
- [DESELECT](#Selection.DESELECT)
- [SELECT](#Selection.SELECT)
- [INVALID](#Selection.INVALID)
- [PRE_CHANGE](#Selection.PRE_CHANGE)
- [id](#Selection.id)
- [events](#Selection.events)
- [selected](#Selection.selected)
- [any](#Selection.any)()
- [is_selected](#Selection.is_selected)(**value**: `Any`)
- [is_selected](#Selection.is_selected+2)(**value**: `Any`, **non_transient_only**: `Bool`)
- [is_invalid_selection](#Selection.is_invalid_selection)(**value**: `Any`)
- [count](#Selection.count)
- [first](#Selection.first)
- [last](#Selection.last)
- [transient](#Selection.transient)
- [new](#Selection.new)(**context**: `String`)
- [destroy](#Selection.destroy)()
- [emit](#Selection.emit+2)(**kind**: `Any`, **items**: `List`)
- [start_transient](#Selection.start_transient)(**change**: `Fn`)
- [end_transient](#Selection.end_transient)()
- [sync](#Selection.sync)(**other**: `Selection`)
- [unsync](#Selection.unsync)(**other**: `Selection`)
- [deselect](#Selection.deselect)()
- [deselect](#Selection.deselect)(**item**: `Any`)
- [deselect_items](#Selection.deselect_items)(**items**: `List`)
- [select](#Selection.select)(**item**: `Any`)
- [select](#Selection.select+2)(**item**: `Any`, **plural**: `Bool`)
- [select_items](#Selection.select_items)(**items**: `List`)
- [select_items](#Selection.select_items+2)(**items**: `List`, **plural**: `Bool`)
- [toggle](#Selection.toggle)(**item**: `Any`)
- [notify](#Selection.notify)()
- [set_invalid_handler](#Selection.set_invalid_handler)(**fn**: `Fn`)

<hr/>
<endpoint module="luxe: selection" class="Selection" signature="CHANGE"></endpoint>
<signature id="Selection.CHANGE">Selection.CHANGE
<a class="headerlink" href="#Selection.CHANGE" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: selection" class="Selection" signature="DESELECT"></endpoint>
<signature id="Selection.DESELECT">Selection.DESELECT
<a class="headerlink" href="#Selection.DESELECT" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: selection" class="Selection" signature="SELECT"></endpoint>
<signature id="Selection.SELECT">Selection.SELECT
<a class="headerlink" href="#Selection.SELECT" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: selection" class="Selection" signature="INVALID"></endpoint>
<signature id="Selection.INVALID">Selection.INVALID
<a class="headerlink" href="#Selection.INVALID" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: selection" class="Selection" signature="PRE_CHANGE"></endpoint>
<signature id="Selection.PRE_CHANGE">Selection.PRE_CHANGE
<a class="headerlink" href="#Selection.PRE_CHANGE" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: selection" class="Selection" signature="id"></endpoint>
<signature id="Selection.id">Selection.id
<a class="headerlink" href="#Selection.id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: selection" class="Selection" signature="events"></endpoint>
<signature id="Selection.events">Selection.events
<a class="headerlink" href="#Selection.events" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Events`
> no docs found   

<endpoint module="luxe: selection" class="Selection" signature="selected"></endpoint>
<signature id="Selection.selected">Selection.selected
<a class="headerlink" href="#Selection.selected" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: selection" class="Selection" signature="any()"></endpoint>
<signature id="Selection.any">Selection.any()
<a class="headerlink" href="#Selection.any" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: selection" class="Selection" signature="is_selected(value : Any)"></endpoint>
<signature id="Selection.is_selected">Selection.is_selected(**value**: `Any`)
<a class="headerlink" href="#Selection.is_selected" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: selection" class="Selection" signature="is_selected(value : Any, non_transient_only : Bool)"></endpoint>
<signature id="Selection.is_selected+2">Selection.is_selected(**value**: `Any`, **non_transient_only**: `Bool`)
<a class="headerlink" href="#Selection.is_selected+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: selection" class="Selection" signature="is_invalid_selection(value : Any)"></endpoint>
<signature id="Selection.is_invalid_selection">Selection.is_invalid_selection(**value**: `Any`)
<a class="headerlink" href="#Selection.is_invalid_selection" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> returns a string as a reason if not able to select, otherwise returns null   

<endpoint module="luxe: selection" class="Selection" signature="count"></endpoint>
<signature id="Selection.count">Selection.count
<a class="headerlink" href="#Selection.count" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: selection" class="Selection" signature="first"></endpoint>
<signature id="Selection.first">Selection.first
<a class="headerlink" href="#Selection.first" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Any`
> no docs found   

<endpoint module="luxe: selection" class="Selection" signature="last"></endpoint>
<signature id="Selection.last">Selection.last
<a class="headerlink" href="#Selection.last" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Any`
> no docs found   

<endpoint module="luxe: selection" class="Selection" signature="transient"></endpoint>
<signature id="Selection.transient">Selection.transient
<a class="headerlink" href="#Selection.transient" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: selection" class="Selection" signature="new(context : String)"></endpoint>
<signature id="Selection.new">Selection.new(**context**: `String`)
<a class="headerlink" href="#Selection.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Selection`
> no docs found   

<endpoint module="luxe: selection" class="Selection" signature="destroy()"></endpoint>
<signature id="Selection.destroy">Selection.destroy()
<a class="headerlink" href="#Selection.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: selection" class="Selection" signature="emit(kind : Any, items : List)"></endpoint>
<signature id="Selection.emit+2">Selection.emit(**kind**: `Any`, **items**: `List`)
<a class="headerlink" href="#Selection.emit+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: selection" class="Selection" signature="start_transient(change : Fn)"></endpoint>
<signature id="Selection.start_transient">Selection.start_transient(**change**: `Fn`)
<a class="headerlink" href="#Selection.start_transient" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Start a transient selection where changes will be stored separately and notifed of a change directly   

<endpoint module="luxe: selection" class="Selection" signature="end_transient()"></endpoint>
<signature id="Selection.end_transient">Selection.end_transient()
<a class="headerlink" href="#Selection.end_transient" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> End a transient selection, read .selected before calling to capture the transient selection   

<endpoint module="luxe: selection" class="Selection" signature="sync(other : Selection)"></endpoint>
<signature id="Selection.sync">Selection.sync(**other**: `Selection`)
<a class="headerlink" href="#Selection.sync" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Sync selection with another instance.   

<endpoint module="luxe: selection" class="Selection" signature="unsync(other : Selection)"></endpoint>
<signature id="Selection.unsync">Selection.unsync(**other**: `Selection`)
<a class="headerlink" href="#Selection.unsync" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Stop syncing selection.   

<endpoint module="luxe: selection" class="Selection" signature="deselect()"></endpoint>
<signature id="Selection.deselect">Selection.deselect()
<a class="headerlink" href="#Selection.deselect" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Clear the selection. emits `DESELECT` with a list of items deselected   

<endpoint module="luxe: selection" class="Selection" signature="deselect(item : Any)"></endpoint>
<signature id="Selection.deselect">Selection.deselect(**item**: `Any`)
<a class="headerlink" href="#Selection.deselect" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Deselect the given item. emits `DESELECT` with a list containing the item   

<endpoint module="luxe: selection" class="Selection" signature="deselect_items(items : List)"></endpoint>
<signature id="Selection.deselect_items">Selection.deselect_items(**items**: `List`)
<a class="headerlink" href="#Selection.deselect_items" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Deselect the given items. emits `DESELECT` with a list containing the items (ones that were actually selected)   

<endpoint module="luxe: selection" class="Selection" signature="select(item : Any)"></endpoint>
<signature id="Selection.select">Selection.select(**item**: `Any`)
<a class="headerlink" href="#Selection.select" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> select the given item. emits `SELECT` with a list containing the item   

<endpoint module="luxe: selection" class="Selection" signature="select(item : Any, plural : Bool)"></endpoint>
<signature id="Selection.select+2">Selection.select(**item**: `Any`, **plural**: `Bool`)
<a class="headerlink" href="#Selection.select+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Select the given item, and if plural is true, the item 
>             is added to the existing selection. If not, the selection
>             is cleared and only this item is selected afterward. 
>             Emits `SELECT` with a list containing the item   

<endpoint module="luxe: selection" class="Selection" signature="select_items(items : List)"></endpoint>
<signature id="Selection.select_items">Selection.select_items(**items**: `List`)
<a class="headerlink" href="#Selection.select_items" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Select multiple items. Replaces the current selection. Emits `SELECT` with a list containing the items   

<endpoint module="luxe: selection" class="Selection" signature="select_items(items : List, plural : Bool)"></endpoint>
<signature id="Selection.select_items+2">Selection.select_items(**items**: `List`, **plural**: `Bool`)
<a class="headerlink" href="#Selection.select_items+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Select the given items, and if plural is true, the items 
>             are added to the existing selection. If not, the selection
>             is cleared and only the items are selected afterward. 
>             Emits `SELECT` with a list containing the items   

<endpoint module="luxe: selection" class="Selection" signature="toggle(item : Any)"></endpoint>
<signature id="Selection.toggle">Selection.toggle(**item**: `Any`)
<a class="headerlink" href="#Selection.toggle" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: selection" class="Selection" signature="notify()"></endpoint>
<signature id="Selection.notify">Selection.notify()
<a class="headerlink" href="#Selection.notify" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> send a change event for the selection   

<endpoint module="luxe: selection" class="Selection" signature="set_invalid_handler(fn : Fn)"></endpoint>
<signature id="Selection.set_invalid_handler">Selection.set_invalid_handler(**fn**: `Fn`)
<a class="headerlink" href="#Selection.set_invalid_handler" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

