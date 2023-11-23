#![](../../../../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.11.2`)  


---

## `luxe: ui/field/choice` module

- [State](#state)   
- [UIChoice](#uichoice)   

---

### State
`:::js import "luxe: ui/field/choice" for State`
> no docs found

- [list](#State.list)
- [new](#State.new+2)(**ui**: `Any`, **control**: `Any`)
- [resize](#State.resize)()
- [add](#State.add+2)(**control**: `Any`, **keywords**: `Any`)
- [remove](#State.remove)(**control**: `Any`)
- [clear](#State.clear)(**uiclear_action**: `Any`)
- [refresh](#State.refresh)()
- [focus](#State.focus)()
- [placeholder](#State.placeholder=)=(v : Any)
- [placeholder](#State.placeholder)
- [fn](#State.fn=)=(v : Any)
- [fn](#State.fn)
- [has_filter](#State.has_filter)
- [force_filter](#State.force_filter+2)(**text**: `Any`, **focus**: `Any`)
- [cancel_filter](#State.cancel_filter)()
- [filter](#State.filter)(**filter**: `Any`)

<hr/>
<endpoint module="luxe: ui/field/choice" class="State" signature="list"></endpoint>
<signature id="State.list">State.list
<a class="headerlink" href="#State.list" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/choice" class="State" signature="new(ui : Any, control : Any)"></endpoint>
<signature id="State.new+2">State.new(**ui**: `Any`, **control**: `Any`)
<a class="headerlink" href="#State.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js State`
> no docs found   

<endpoint module="luxe: ui/field/choice" class="State" signature="resize()"></endpoint>
<signature id="State.resize">State.resize()
<a class="headerlink" href="#State.resize" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/choice" class="State" signature="add(control : Any, keywords : Any)"></endpoint>
<signature id="State.add+2">State.add(**control**: `Any`, **keywords**: `Any`)
<a class="headerlink" href="#State.add+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/choice" class="State" signature="remove(control : Any)"></endpoint>
<signature id="State.remove">State.remove(**control**: `Any`)
<a class="headerlink" href="#State.remove" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/choice" class="State" signature="clear(uiclear_action : Any)"></endpoint>
<signature id="State.clear">State.clear(**uiclear_action**: `Any`)
<a class="headerlink" href="#State.clear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/choice" class="State" signature="refresh()"></endpoint>
<signature id="State.refresh">State.refresh()
<a class="headerlink" href="#State.refresh" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/choice" class="State" signature="focus()"></endpoint>
<signature id="State.focus">State.focus()
<a class="headerlink" href="#State.focus" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/choice" class="State" signature="placeholder=(v : Any)"></endpoint>
<signature id="State.placeholder=">State.placeholder=(v : Any)
<a class="headerlink" href="#State.placeholder=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/choice" class="State" signature="placeholder"></endpoint>
<signature id="State.placeholder">State.placeholder
<a class="headerlink" href="#State.placeholder" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/choice" class="State" signature="fn=(v : Any)"></endpoint>
<signature id="State.fn=">State.fn=(v : Any)
<a class="headerlink" href="#State.fn=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/choice" class="State" signature="fn"></endpoint>
<signature id="State.fn">State.fn
<a class="headerlink" href="#State.fn" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/choice" class="State" signature="has_filter"></endpoint>
<signature id="State.has_filter">State.has_filter
<a class="headerlink" href="#State.has_filter" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/choice" class="State" signature="force_filter(text : Any, focus : Any)"></endpoint>
<signature id="State.force_filter+2">State.force_filter(**text**: `Any`, **focus**: `Any`)
<a class="headerlink" href="#State.force_filter+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/choice" class="State" signature="cancel_filter()"></endpoint>
<signature id="State.cancel_filter">State.cancel_filter()
<a class="headerlink" href="#State.cancel_filter" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/choice" class="State" signature="filter(filter : Any)"></endpoint>
<signature id="State.filter">State.filter(**filter**: `Any`)
<a class="headerlink" href="#State.filter" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### UIChoice
`:::js import "luxe: ui/field/choice" for UIChoice`
> no docs found

- [create](#UIChoice.create)(**ui**: `UI`)
- [get_placeholder](#UIChoice.get_placeholder)(**choice**: `Control`)
- [set_placeholder](#UIChoice.set_placeholder+2)(**choice**: `Control`, **text**: `String`)
- [set_filter](#UIChoice.set_filter+2)(**choice**: `Control`, **fn**: `Fn`)
- [add](#UIChoice.add+3)(**choice**: `Control`, **control**: `Control`, **keywords**: `List`)
- [remove](#UIChoice.remove+2)(**choice**: `Control`, **control**: `Control`)
- [clear](#UIChoice.clear+2)(**choice**: `Control`, **uiclear_action**: `UIClear`)
- [refresh](#UIChoice.refresh)(**choice**: `Control`)
- [focus](#UIChoice.focus)(**choice**: `Control`)

<hr/>
<endpoint module="luxe: ui/field/choice" class="UIChoice" signature="create(ui : UI)"></endpoint>
<signature id="UIChoice.create">UIChoice.create(**ui**: `UI`)
<a class="headerlink" href="#UIChoice.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Control`
> no docs found   

<endpoint module="luxe: ui/field/choice" class="UIChoice" signature="get_placeholder(choice : Control)"></endpoint>
<signature id="UIChoice.get_placeholder">UIChoice.get_placeholder(**choice**: `Control`)
<a class="headerlink" href="#UIChoice.get_placeholder" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: ui/field/choice" class="UIChoice" signature="set_placeholder(choice : Control, text : String)"></endpoint>
<signature id="UIChoice.set_placeholder+2">UIChoice.set_placeholder(**choice**: `Control`, **text**: `String`)
<a class="headerlink" href="#UIChoice.set_placeholder+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/choice" class="UIChoice" signature="set_filter(choice : Control, fn : Fn)"></endpoint>
<signature id="UIChoice.set_filter+2">UIChoice.set_filter(**choice**: `Control`, **fn**: `Fn`)
<a class="headerlink" href="#UIChoice.set_filter+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/choice" class="UIChoice" signature="add(choice : Control, control : Control, keywords : List)"></endpoint>
<signature id="UIChoice.add+3">UIChoice.add(**choice**: `Control`, **control**: `Control`, **keywords**: `List`)
<a class="headerlink" href="#UIChoice.add+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/choice" class="UIChoice" signature="remove(choice : Control, control : Control)"></endpoint>
<signature id="UIChoice.remove+2">UIChoice.remove(**choice**: `Control`, **control**: `Control`)
<a class="headerlink" href="#UIChoice.remove+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/choice" class="UIChoice" signature="clear(choice : Control, uiclear_action : UIClear)"></endpoint>
<signature id="UIChoice.clear+2">UIChoice.clear(**choice**: `Control`, **uiclear_action**: `UIClear`)
<a class="headerlink" href="#UIChoice.clear+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/choice" class="UIChoice" signature="refresh(choice : Control)"></endpoint>
<signature id="UIChoice.refresh">UIChoice.refresh(**choice**: `Control`)
<a class="headerlink" href="#UIChoice.refresh" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/choice" class="UIChoice" signature="focus(choice : Control)"></endpoint>
<signature id="UIChoice.focus">UIChoice.focus(**choice**: `Control`)
<a class="headerlink" href="#UIChoice.focus" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

