#![](../../../../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.10.1`)  


---

## `luxe: ui/field/path` module

- [UIPath](#uipath)   
- [UIPathState](#uipathstate)   
- [UIPathType](#uipathtype)   

---

### UIPath
`:::js import "luxe: ui/field/path" for UIPath`
> no docs found

- [create](#UIPath.create)(**ui**: `Entity`)
- [set_validation](#UIPath.set_validation+2)(**path**: `Control`, **fn**: `Fn`)
- [set_defaults](#UIPath.set_defaults+3)(**path**: `Control`, **default_path**: `String`, **filters**: `String`)
- [set_defaults](#UIPath.set_defaults+2)(**path**: `Control`, **default_path**: `String`)
- [set_type](#UIPath.set_type+2)(**path**: `Control`, **type**: `UIPathType`)
- [get_text_field](#UIPath.get_text_field)(**path**: `Control`)
- [get_path](#UIPath.get_path)(**path**: `Control`)
- [set_path](#UIPath.set_path+2)(**path**: `Control`, **path_value**: `String`)

<hr/>
<endpoint module="luxe: ui/field/path" class="UIPath" signature="create(ui : Entity)"></endpoint>
<signature id="UIPath.create">UIPath.create(**ui**: `Entity`)
<a class="headerlink" href="#UIPath.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/path" class="UIPath" signature="set_validation(path : Control, fn : Fn)"></endpoint>
<signature id="UIPath.set_validation+2">UIPath.set_validation(**path**: `Control`, **fn**: `Fn`)
<a class="headerlink" href="#UIPath.set_validation+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> set a validation function to be called which will ensure the path is validated before use   

<endpoint module="luxe: ui/field/path" class="UIPath" signature="set_defaults(path : Control, default_path : String, filters : String)"></endpoint>
<signature id="UIPath.set_defaults+3">UIPath.set_defaults(**path**: `Control`, **default_path**: `String`, **filters**: `String`)
<a class="headerlink" href="#UIPath.set_defaults+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> set the default file dialog path and file dialog filters   

<endpoint module="luxe: ui/field/path" class="UIPath" signature="set_defaults(path : Control, default_path : String)"></endpoint>
<signature id="UIPath.set_defaults+2">UIPath.set_defaults(**path**: `Control`, **default_path**: `String`)
<a class="headerlink" href="#UIPath.set_defaults+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> set the default file dialog path   

<endpoint module="luxe: ui/field/path" class="UIPath" signature="set_type(path : Control, type : UIPathType)"></endpoint>
<signature id="UIPath.set_type+2">UIPath.set_type(**path**: `Control`, **type**: `UIPathType`)
<a class="headerlink" href="#UIPath.set_type+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> set the path type, to open/save/folder   

<endpoint module="luxe: ui/field/path" class="UIPath" signature="get_text_field(path : Control)"></endpoint>
<signature id="UIPath.get_text_field">UIPath.get_text_field(**path**: `Control`)
<a class="headerlink" href="#UIPath.get_text_field" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> return the text field   

<endpoint module="luxe: ui/field/path" class="UIPath" signature="get_path(path : Control)"></endpoint>
<signature id="UIPath.get_path">UIPath.get_path(**path**: `Control`)
<a class="headerlink" href="#UIPath.get_path" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> return the path stored in the field   

<endpoint module="luxe: ui/field/path" class="UIPath" signature="set_path(path : Control, path_value : String)"></endpoint>
<signature id="UIPath.set_path+2">UIPath.set_path(**path**: `Control`, **path_value**: `String`)
<a class="headerlink" href="#UIPath.set_path+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> set the path stored in the field (will be validated)   

### UIPathState
`:::js import "luxe: ui/field/path" for UIPathState`
> no docs found

- [new](#UIPathState.new+2)(**ui**: `Entity`, **control**: `Control`)
- [get_text_field](#UIPathState.get_text_field)()
- [get_path](#UIPathState.get_path)()
- [set_path](#UIPathState.set_path)(**path**: `String`)
- [set_validation](#UIPathState.set_validation)(**fn**: `Fn`)
- [set_defaults](#UIPathState.set_defaults+2)(**default_path**: `String`, **filters**: `String`)
- [set_type](#UIPathState.set_type)(**type**: `UIPathType`)

<hr/>
<endpoint module="luxe: ui/field/path" class="UIPathState" signature="new(ui : Entity, control : Control)"></endpoint>
<signature id="UIPathState.new+2">UIPathState.new(**ui**: `Entity`, **control**: `Control`)
<a class="headerlink" href="#UIPathState.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js UIPathState`
> no docs found   

<endpoint module="luxe: ui/field/path" class="UIPathState" signature="get_text_field()"></endpoint>
<signature id="UIPathState.get_text_field">UIPathState.get_text_field()
<a class="headerlink" href="#UIPathState.get_text_field" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/path" class="UIPathState" signature="get_path()"></endpoint>
<signature id="UIPathState.get_path">UIPathState.get_path()
<a class="headerlink" href="#UIPathState.get_path" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/path" class="UIPathState" signature="set_path(path : String)"></endpoint>
<signature id="UIPathState.set_path">UIPathState.set_path(**path**: `String`)
<a class="headerlink" href="#UIPathState.set_path" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/path" class="UIPathState" signature="set_validation(fn : Fn)"></endpoint>
<signature id="UIPathState.set_validation">UIPathState.set_validation(**fn**: `Fn`)
<a class="headerlink" href="#UIPathState.set_validation" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/path" class="UIPathState" signature="set_defaults(default_path : String, filters : String)"></endpoint>
<signature id="UIPathState.set_defaults+2">UIPathState.set_defaults(**default_path**: `String`, **filters**: `String`)
<a class="headerlink" href="#UIPathState.set_defaults+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/path" class="UIPathState" signature="set_type(type : UIPathType)"></endpoint>
<signature id="UIPathState.set_type">UIPathState.set_type(**type**: `UIPathType`)
<a class="headerlink" href="#UIPathState.set_type" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### UIPathType
`:::js import "luxe: ui/field/path" for UIPathType`
> no docs found

- [open](#UIPathType.open)
- [save](#UIPathType.save)
- [folder](#UIPathType.folder)

<hr/>
<endpoint module="luxe: ui/field/path" class="UIPathType" signature="open"></endpoint>
<signature id="UIPathType.open">UIPathType.open
<a class="headerlink" href="#UIPathType.open" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/path" class="UIPathType" signature="save"></endpoint>
<signature id="UIPathType.save">UIPathType.save
<a class="headerlink" href="#UIPathType.save" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/field/path" class="UIPathType" signature="folder"></endpoint>
<signature id="UIPathType.folder">UIPathType.folder
<a class="headerlink" href="#UIPathType.folder" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

