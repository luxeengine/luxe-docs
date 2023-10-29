#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.10.1`)  


---

## `luxe: ui/list_filtered` module

- [State](#state)   
- [UIListFiltered](#uilistfiltered)   
- [UIListFilteredItem](#uilistfiltereditem)   

---

### State
`:::js import "luxe: ui/list_filtered" for State`
> no docs found

- [list](#State.list)
- [set_filter_sizes](#State.set_filter_sizes+2)(**height**: `Num`, **text_size**: `Num`)
- [set_filter_string](#State.set_filter_string)(**text**: `String`)
- [add](#State.add+2)(**control**: `Any`, **keywords**: `Any`)
- [remove](#State.remove)(**control**: `Any`)
- [clear](#State.clear)(**uiclear_action**: `Any`)
- [refresh](#State.refresh)()
- [focus](#State.focus)()
- [placeholder](#State.placeholder=)=(v : Any)
- [placeholder](#State.placeholder)
- [events](#State.events)
- [new](#State.new+2)(**ui**: `Any`, **control**: `Any`)
- [has_filter](#State.has_filter)
- [get_filter](#State.get_filter)()
- [force_filter](#State.force_filter+2)(**text**: `Any`, **focus**: `Any`)
- [cancel_filter](#State.cancel_filter)()
- [filter](#State.filter)(**filter**: `String`)
- [filter_and_sort](#State.filter_and_sort+2)(**items**: `List`, **filter**: `String`)

<hr/>
<endpoint module="luxe: ui/list_filtered" class="State" signature="list"></endpoint>
<signature id="State.list">State.list
<a class="headerlink" href="#State.list" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="State" signature="set_filter_sizes(height : Num, text_size : Num)"></endpoint>
<signature id="State.set_filter_sizes+2">State.set_filter_sizes(**height**: `Num`, **text_size**: `Num`)
<a class="headerlink" href="#State.set_filter_sizes+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="State" signature="set_filter_string(text : String)"></endpoint>
<signature id="State.set_filter_string">State.set_filter_string(**text**: `String`)
<a class="headerlink" href="#State.set_filter_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="State" signature="add(control : Any, keywords : Any)"></endpoint>
<signature id="State.add+2">State.add(**control**: `Any`, **keywords**: `Any`)
<a class="headerlink" href="#State.add+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="State" signature="remove(control : Any)"></endpoint>
<signature id="State.remove">State.remove(**control**: `Any`)
<a class="headerlink" href="#State.remove" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="State" signature="clear(uiclear_action : Any)"></endpoint>
<signature id="State.clear">State.clear(**uiclear_action**: `Any`)
<a class="headerlink" href="#State.clear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="State" signature="refresh()"></endpoint>
<signature id="State.refresh">State.refresh()
<a class="headerlink" href="#State.refresh" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="State" signature="focus()"></endpoint>
<signature id="State.focus">State.focus()
<a class="headerlink" href="#State.focus" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="State" signature="placeholder=(v : Any)"></endpoint>
<signature id="State.placeholder=">State.placeholder=(v : Any)
<a class="headerlink" href="#State.placeholder=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="State" signature="placeholder"></endpoint>
<signature id="State.placeholder">State.placeholder
<a class="headerlink" href="#State.placeholder" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="State" signature="events"></endpoint>
<signature id="State.events">State.events
<a class="headerlink" href="#State.events" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Events`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="State" signature="new(ui : Any, control : Any)"></endpoint>
<signature id="State.new+2">State.new(**ui**: `Any`, **control**: `Any`)
<a class="headerlink" href="#State.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js State`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="State" signature="has_filter"></endpoint>
<signature id="State.has_filter">State.has_filter
<a class="headerlink" href="#State.has_filter" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="State" signature="get_filter()"></endpoint>
<signature id="State.get_filter">State.get_filter()
<a class="headerlink" href="#State.get_filter" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="State" signature="force_filter(text : Any, focus : Any)"></endpoint>
<signature id="State.force_filter+2">State.force_filter(**text**: `Any`, **focus**: `Any`)
<a class="headerlink" href="#State.force_filter+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="State" signature="cancel_filter()"></endpoint>
<signature id="State.cancel_filter">State.cancel_filter()
<a class="headerlink" href="#State.cancel_filter" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="State" signature="filter(filter : String)"></endpoint>
<signature id="State.filter">State.filter(**filter**: `String`)
<a class="headerlink" href="#State.filter" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="State" signature="filter_and_sort(items : List, filter : String)"></endpoint>
<signature id="State.filter_and_sort+2">State.filter_and_sort(**items**: `List`, **filter**: `String`)
<a class="headerlink" href="#State.filter_and_sort+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### UIListFiltered
`:::js import "luxe: ui/list_filtered" for UIListFiltered`
> no docs found

- [MATCH](#UIListFiltered.MATCH)
- [create](#UIListFiltered.create)(**ui**: `Any`)
- [set_bounds](#UIListFiltered.set_bounds+5)(**list**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`)
- [set_size](#UIListFiltered.set_size+3)(**list**: `Any`, **w**: `Any`, **h**: `Any`)
- [set_filter_sizes](#UIListFiltered.set_filter_sizes+3)(**list**: `Any`, **height**: `Num`, **text_size**: `Num`)
- [on_filter](#UIListFiltered.on_filter+2)(**list**: `Control`, **fn**: `Fn`)
- [get_placeholder](#UIListFiltered.get_placeholder+2)(**list**: `Any`, **text**: `Any`)
- [set_placeholder](#UIListFiltered.set_placeholder+2)(**list**: `Any`, **text**: `Any`)
- [set_filter](#UIListFiltered.set_filter+2)(**list**: `Any`, **fn**: `Any`)
- [get_filter](#UIListFiltered.get_filter)(**list**: `Any`)
- [set_filter_string](#UIListFiltered.set_filter_string+2)(**list**: `Any`, **text**: `String`)
- [get_list_view](#UIListFiltered.get_list_view)(**list**: `Any`)
- [add](#UIListFiltered.add+3)(**list**: `Any`, **control**: `Any`, **keywords**: `Any`)
- [remove](#UIListFiltered.remove+2)(**list**: `Any`, **control**: `Any`)
- [clear](#UIListFiltered.clear+2)(**list**: `Any`, **uiclear_action**: `Any`)
- [refresh](#UIListFiltered.refresh)(**list**: `Any`)
- [focus](#UIListFiltered.focus)(**list**: `Any`)

<hr/>
<endpoint module="luxe: ui/list_filtered" class="UIListFiltered" signature="MATCH"></endpoint>
<signature id="UIListFiltered.MATCH">UIListFiltered.MATCH
<a class="headerlink" href="#UIListFiltered.MATCH" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="UIListFiltered" signature="create(ui : Any)"></endpoint>
<signature id="UIListFiltered.create">UIListFiltered.create(**ui**: `Any`)
<a class="headerlink" href="#UIListFiltered.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="UIListFiltered" signature="set_bounds(list : Any, x : Any, y : Any, w : Any, h : Any)"></endpoint>
<signature id="UIListFiltered.set_bounds+5">UIListFiltered.set_bounds(**list**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`)
<a class="headerlink" href="#UIListFiltered.set_bounds+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="UIListFiltered" signature="set_size(list : Any, w : Any, h : Any)"></endpoint>
<signature id="UIListFiltered.set_size+3">UIListFiltered.set_size(**list**: `Any`, **w**: `Any`, **h**: `Any`)
<a class="headerlink" href="#UIListFiltered.set_size+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="UIListFiltered" signature="set_filter_sizes(list : Any, height : Num, text_size : Num)"></endpoint>
<signature id="UIListFiltered.set_filter_sizes+3">UIListFiltered.set_filter_sizes(**list**: `Any`, **height**: `Num`, **text_size**: `Num`)
<a class="headerlink" href="#UIListFiltered.set_filter_sizes+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="UIListFiltered" signature="on_filter(list : Control, fn : Fn)"></endpoint>
<signature id="UIListFiltered.on_filter+2">UIListFiltered.on_filter(**list**: `Control`, **fn**: `Fn`)
<a class="headerlink" href="#UIListFiltered.on_filter+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="UIListFiltered" signature="get_placeholder(list : Any, text : Any)"></endpoint>
<signature id="UIListFiltered.get_placeholder+2">UIListFiltered.get_placeholder(**list**: `Any`, **text**: `Any`)
<a class="headerlink" href="#UIListFiltered.get_placeholder+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="UIListFiltered" signature="set_placeholder(list : Any, text : Any)"></endpoint>
<signature id="UIListFiltered.set_placeholder+2">UIListFiltered.set_placeholder(**list**: `Any`, **text**: `Any`)
<a class="headerlink" href="#UIListFiltered.set_placeholder+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="UIListFiltered" signature="set_filter(list : Any, fn : Any)"></endpoint>
<signature id="UIListFiltered.set_filter+2">UIListFiltered.set_filter(**list**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#UIListFiltered.set_filter+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="UIListFiltered" signature="get_filter(list : Any)"></endpoint>
<signature id="UIListFiltered.get_filter">UIListFiltered.get_filter(**list**: `Any`)
<a class="headerlink" href="#UIListFiltered.get_filter" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="UIListFiltered" signature="set_filter_string(list : Any, text : String)"></endpoint>
<signature id="UIListFiltered.set_filter_string+2">UIListFiltered.set_filter_string(**list**: `Any`, **text**: `String`)
<a class="headerlink" href="#UIListFiltered.set_filter_string+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="UIListFiltered" signature="get_list_view(list : Any)"></endpoint>
<signature id="UIListFiltered.get_list_view">UIListFiltered.get_list_view(**list**: `Any`)
<a class="headerlink" href="#UIListFiltered.get_list_view" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="UIListFiltered" signature="add(list : Any, control : Any, keywords : Any)"></endpoint>
<signature id="UIListFiltered.add+3">UIListFiltered.add(**list**: `Any`, **control**: `Any`, **keywords**: `Any`)
<a class="headerlink" href="#UIListFiltered.add+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="UIListFiltered" signature="remove(list : Any, control : Any)"></endpoint>
<signature id="UIListFiltered.remove+2">UIListFiltered.remove(**list**: `Any`, **control**: `Any`)
<a class="headerlink" href="#UIListFiltered.remove+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="UIListFiltered" signature="clear(list : Any, uiclear_action : Any)"></endpoint>
<signature id="UIListFiltered.clear+2">UIListFiltered.clear(**list**: `Any`, **uiclear_action**: `Any`)
<a class="headerlink" href="#UIListFiltered.clear+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="UIListFiltered" signature="refresh(list : Any)"></endpoint>
<signature id="UIListFiltered.refresh">UIListFiltered.refresh(**list**: `Any`)
<a class="headerlink" href="#UIListFiltered.refresh" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="UIListFiltered" signature="focus(list : Any)"></endpoint>
<signature id="UIListFiltered.focus">UIListFiltered.focus(**list**: `Any`)
<a class="headerlink" href="#UIListFiltered.focus" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### UIListFilteredItem
`:::js import "luxe: ui/list_filtered" for UIListFilteredItem`
> no docs found

- [control](#UIListFilteredItem.control)
- [keywords](#UIListFilteredItem.keywords)
- [result](#UIListFilteredItem.result)
- [result](#UIListFilteredItem.result=)=(v : FuzzyResult)
- [new](#UIListFilteredItem.new+2)(**control**: `Control`, **keywords**: `List`)

<hr/>
<endpoint module="luxe: ui/list_filtered" class="UIListFilteredItem" signature="control"></endpoint>
<signature id="UIListFilteredItem.control">UIListFilteredItem.control
<a class="headerlink" href="#UIListFilteredItem.control" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Control`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="UIListFilteredItem" signature="keywords"></endpoint>
<signature id="UIListFilteredItem.keywords">UIListFilteredItem.keywords
<a class="headerlink" href="#UIListFilteredItem.keywords" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="UIListFilteredItem" signature="result"></endpoint>
<signature id="UIListFilteredItem.result">UIListFilteredItem.result
<a class="headerlink" href="#UIListFilteredItem.result" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js FuzzyResult`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="UIListFilteredItem" signature="result=(v : FuzzyResult)"></endpoint>
<signature id="UIListFilteredItem.result=">UIListFilteredItem.result=(v : FuzzyResult)
<a class="headerlink" href="#UIListFilteredItem.result=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js FuzzyResult`
> no docs found   

<endpoint module="luxe: ui/list_filtered" class="UIListFilteredItem" signature="new(control : Control, keywords : List)"></endpoint>
<signature id="UIListFilteredItem.new+2">UIListFilteredItem.new(**control**: `Control`, **keywords**: `List`)
<a class="headerlink" href="#UIListFilteredItem.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js UIListFilteredItem`
> no docs found   

