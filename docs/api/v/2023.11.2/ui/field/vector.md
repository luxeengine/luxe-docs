#![](../../../../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.11.2`)  


---

## `luxe: ui/field/vector` module

- [UIVector](#uivector)   
- [UIVectorState](#uivectorstate)   

---

### UIVector
`:::js import "luxe: ui/field/vector" for UIVector`
> no docs found

- [create](#UIVector.create)(**ui**: `Any`)
- [get_component_count](#UIVector.get_component_count)(**vec**: `Control`)
- [set_component_count](#UIVector.set_component_count+2)(**vec**: `Control`, **count**: `Num`)
- [get_value](#UIVector.get_value)(**vec**: `Control`)
- [set_value](#UIVector.set_value+2)(**vec**: `Control`, **value**: `Vec`)
- [get_text_field](#UIVector.get_text_field+2)(**vec**: `Control`, **index**: `Num`)

<hr/>
<endpoint module="luxe: ui/field/vector" class="UIVector" signature="create(ui : Any)"></endpoint>
<signature id="UIVector.create">UIVector.create(**ui**: `Any`)
<a class="headerlink" href="#UIVector.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/vector" class="UIVector" signature="get_component_count(vec : Control)"></endpoint>
<signature id="UIVector.get_component_count">UIVector.get_component_count(**vec**: `Control`)
<a class="headerlink" href="#UIVector.get_component_count" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/vector" class="UIVector" signature="set_component_count(vec : Control, count : Num)"></endpoint>
<signature id="UIVector.set_component_count+2">UIVector.set_component_count(**vec**: `Control`, **count**: `Num`)
<a class="headerlink" href="#UIVector.set_component_count+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/vector" class="UIVector" signature="get_value(vec : Control)"></endpoint>
<signature id="UIVector.get_value">UIVector.get_value(**vec**: `Control`)
<a class="headerlink" href="#UIVector.get_value" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> no docs found   

<endpoint module="luxe: ui/field/vector" class="UIVector" signature="set_value(vec : Control, value : Vec)"></endpoint>
<signature id="UIVector.set_value+2">UIVector.set_value(**vec**: `Control`, **value**: `Vec`)
<a class="headerlink" href="#UIVector.set_value+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/vector" class="UIVector" signature="get_text_field(vec : Control, index : Num)"></endpoint>
<signature id="UIVector.get_text_field+2">UIVector.get_text_field(**vec**: `Control`, **index**: `Num`)
<a class="headerlink" href="#UIVector.get_text_field+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Control`
> no docs found   

### UIVectorState
`:::js import "luxe: ui/field/vector" for UIVectorState`
> no docs found

- [components](#UIVectorState.components)
- [components](#UIVectorState.components=)=(v : Any)
- [value](#UIVectorState.value)
- [set_value](#UIVectorState.set_value)(**value**: `Vec`)
- [get_text_field](#UIVectorState.get_text_field)(**index**: `Num`)
- [make_field](#UIVectorState.make_field)(**index**: `Num`)
- [new](#UIVectorState.new+2)(**ui**: `Any`, **ctrl**: `Any`)
- [on_event](#UIVectorState.on_event+2)(**field**: `Any`, **event**: `Any`)

<hr/>
<endpoint module="luxe: ui/field/vector" class="UIVectorState" signature="components"></endpoint>
<signature id="UIVectorState.components">UIVectorState.components
<a class="headerlink" href="#UIVectorState.components" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/vector" class="UIVectorState" signature="components=(v : Any)"></endpoint>
<signature id="UIVectorState.components=">UIVectorState.components=(v : Any)
<a class="headerlink" href="#UIVectorState.components=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/vector" class="UIVectorState" signature="value"></endpoint>
<signature id="UIVectorState.value">UIVectorState.value
<a class="headerlink" href="#UIVectorState.value" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/vector" class="UIVectorState" signature="set_value(value : Vec)"></endpoint>
<signature id="UIVectorState.set_value">UIVectorState.set_value(**value**: `Vec`)
<a class="headerlink" href="#UIVectorState.set_value" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/vector" class="UIVectorState" signature="get_text_field(index : Num)"></endpoint>
<signature id="UIVectorState.get_text_field">UIVectorState.get_text_field(**index**: `Num`)
<a class="headerlink" href="#UIVectorState.get_text_field" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Control`
> no docs found   

<endpoint module="luxe: ui/field/vector" class="UIVectorState" signature="make_field(index : Num)"></endpoint>
<signature id="UIVectorState.make_field">UIVectorState.make_field(**index**: `Num`)
<a class="headerlink" href="#UIVectorState.make_field" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/vector" class="UIVectorState" signature="new(ui : Any, ctrl : Any)"></endpoint>
<signature id="UIVectorState.new+2">UIVectorState.new(**ui**: `Any`, **ctrl**: `Any`)
<a class="headerlink" href="#UIVectorState.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js UIVectorState`
> no docs found   

<endpoint module="luxe: ui/field/vector" class="UIVectorState" signature="on_event(field : Any, event : Any)"></endpoint>
<signature id="UIVectorState.on_event+2">UIVectorState.on_event(**field**: `Any`, **event**: `Any`)
<a class="headerlink" href="#UIVectorState.on_event+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

