#![](../../../../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.10.1`)  


---

## `luxe: ui/field/number` module

- [UINumber](#uinumber)   
- [UINumberState](#uinumberstate)   

---

### UINumber
`:::js import "luxe: ui/field/number" for UINumber`
> no docs found

- [create](#UINumber.create)(**ui**: `Any`)
- [get_text_field](#UINumber.get_text_field)(**num**: `Control`)
- [get_value](#UINumber.get_value)(**num**: `Control`)
- [get_valid](#UINumber.get_valid)(**num**: `Control`)
- [set_value](#UINumber.set_value+2)(**num**: `Control`, **value**: `Num`)
- [set_precision](#UINumber.set_precision+2)(**num**: `Control`, **value**: `Num`)
- [get_precision](#UINumber.get_precision+2)(**num**: `Control`, **value**: `Num`)
- [set_validation](#UINumber.set_validation+2)(**num**: `Control`, **fn**: `Fn`)

<hr/>
<endpoint module="luxe: ui/field/number" class="UINumber" signature="create(ui : Any)"></endpoint>
<signature id="UINumber.create">UINumber.create(**ui**: `Any`)
<a class="headerlink" href="#UINumber.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumber" signature="get_text_field(num : Control)"></endpoint>
<signature id="UINumber.get_text_field">UINumber.get_text_field(**num**: `Control`)
<a class="headerlink" href="#UINumber.get_text_field" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Control`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumber" signature="get_value(num : Control)"></endpoint>
<signature id="UINumber.get_value">UINumber.get_value(**num**: `Control`)
<a class="headerlink" href="#UINumber.get_value" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumber" signature="get_valid(num : Control)"></endpoint>
<signature id="UINumber.get_valid">UINumber.get_valid(**num**: `Control`)
<a class="headerlink" href="#UINumber.get_valid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumber" signature="set_value(num : Control, value : Num)"></endpoint>
<signature id="UINumber.set_value+2">UINumber.set_value(**num**: `Control`, **value**: `Num`)
<a class="headerlink" href="#UINumber.set_value+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumber" signature="set_precision(num : Control, value : Num)"></endpoint>
<signature id="UINumber.set_precision+2">UINumber.set_precision(**num**: `Control`, **value**: `Num`)
<a class="headerlink" href="#UINumber.set_precision+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumber" signature="get_precision(num : Control, value : Num)"></endpoint>
<signature id="UINumber.get_precision+2">UINumber.get_precision(**num**: `Control`, **value**: `Num`)
<a class="headerlink" href="#UINumber.get_precision+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumber" signature="set_validation(num : Control, fn : Fn)"></endpoint>
<signature id="UINumber.set_validation+2">UINumber.set_validation(**num**: `Control`, **fn**: `Fn`)
<a class="headerlink" href="#UINumber.set_validation+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### UINumberState
`:::js import "luxe: ui/field/number" for UINumberState`
> no docs found

- [validation](#UINumberState.validation)
- [validation](#UINumberState.validation=)=(v : Any)
- [text_control](#UINumberState.text_control)
- [text_value](#UINumberState.text_value)
- [precision](#UINumberState.precision)
- [precision](#UINumberState.precision=)=(v : Any)
- [value](#UINumberState.value)
- [valid](#UINumberState.valid)
- [new](#UINumberState.new+2)(**ui**: `Any`, **ctrl**: `Any`)
- [set_value](#UINumberState.set_value)(**value**: `Any`)
- [resize](#UINumberState.resize+4)(**x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`)
- [refresh_radial](#UINumberState.refresh_radial)()
- [expand_radial](#UINumberState.expand_radial)(**state**: `Any`)
- [fix](#UINumberState.fix)(**value**: `Num`)
- [on_radial_event](#UINumberState.on_radial_event)(**event**: `Any`)
- [cancel_radial_capture](#UINumberState.cancel_radial_capture)()
- [render_radial](#UINumberState.render_radial+6)(**control**: `Any`, **state**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`)
- [validate](#UINumberState.validate)(**num**: `Num`)
- [try_expression](#UINumberState.try_expression)(**string**: `String`)
- [on_text_event](#UINumberState.on_text_event)(**event**: `Any`)

<hr/>
<endpoint module="luxe: ui/field/number" class="UINumberState" signature="validation"></endpoint>
<signature id="UINumberState.validation">UINumberState.validation
<a class="headerlink" href="#UINumberState.validation" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumberState" signature="validation=(v : Any)"></endpoint>
<signature id="UINumberState.validation=">UINumberState.validation=(v : Any)
<a class="headerlink" href="#UINumberState.validation=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumberState" signature="text_control"></endpoint>
<signature id="UINumberState.text_control">UINumberState.text_control
<a class="headerlink" href="#UINumberState.text_control" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumberState" signature="text_value"></endpoint>
<signature id="UINumberState.text_value">UINumberState.text_value
<a class="headerlink" href="#UINumberState.text_value" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumberState" signature="precision"></endpoint>
<signature id="UINumberState.precision">UINumberState.precision
<a class="headerlink" href="#UINumberState.precision" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumberState" signature="precision=(v : Any)"></endpoint>
<signature id="UINumberState.precision=">UINumberState.precision=(v : Any)
<a class="headerlink" href="#UINumberState.precision=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumberState" signature="value"></endpoint>
<signature id="UINumberState.value">UINumberState.value
<a class="headerlink" href="#UINumberState.value" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumberState" signature="valid"></endpoint>
<signature id="UINumberState.valid">UINumberState.valid
<a class="headerlink" href="#UINumberState.valid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumberState" signature="new(ui : Any, ctrl : Any)"></endpoint>
<signature id="UINumberState.new+2">UINumberState.new(**ui**: `Any`, **ctrl**: `Any`)
<a class="headerlink" href="#UINumberState.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js UINumberState`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumberState" signature="set_value(value : Any)"></endpoint>
<signature id="UINumberState.set_value">UINumberState.set_value(**value**: `Any`)
<a class="headerlink" href="#UINumberState.set_value" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumberState" signature="resize(x : Any, y : Any, w : Any, h : Any)"></endpoint>
<signature id="UINumberState.resize+4">UINumberState.resize(**x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`)
<a class="headerlink" href="#UINumberState.resize+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumberState" signature="refresh_radial()"></endpoint>
<signature id="UINumberState.refresh_radial">UINumberState.refresh_radial()
<a class="headerlink" href="#UINumberState.refresh_radial" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumberState" signature="expand_radial(state : Any)"></endpoint>
<signature id="UINumberState.expand_radial">UINumberState.expand_radial(**state**: `Any`)
<a class="headerlink" href="#UINumberState.expand_radial" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumberState" signature="fix(value : Num)"></endpoint>
<signature id="UINumberState.fix">UINumberState.fix(**value**: `Num`)
<a class="headerlink" href="#UINumberState.fix" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumberState" signature="on_radial_event(event : Any)"></endpoint>
<signature id="UINumberState.on_radial_event">UINumberState.on_radial_event(**event**: `Any`)
<a class="headerlink" href="#UINumberState.on_radial_event" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumberState" signature="cancel_radial_capture()"></endpoint>
<signature id="UINumberState.cancel_radial_capture">UINumberState.cancel_radial_capture()
<a class="headerlink" href="#UINumberState.cancel_radial_capture" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumberState" signature="render_radial(control : Any, state : Any, x : Any, y : Any, w : Any, h : Any)"></endpoint>
<signature id="UINumberState.render_radial+6">UINumberState.render_radial(**control**: `Any`, **state**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`)
<a class="headerlink" href="#UINumberState.render_radial+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumberState" signature="validate(num : Num)"></endpoint>
<signature id="UINumberState.validate">UINumberState.validate(**num**: `Num`)
<a class="headerlink" href="#UINumberState.validate" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumberState" signature="try_expression(string : String)"></endpoint>
<signature id="UINumberState.try_expression">UINumberState.try_expression(**string**: `String`)
<a class="headerlink" href="#UINumberState.try_expression" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/number" class="UINumberState" signature="on_text_event(event : Any)"></endpoint>
<signature id="UINumberState.on_text_event">UINumberState.on_text_event(**event**: `Any`)
<a class="headerlink" href="#UINumberState.on_text_event" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

