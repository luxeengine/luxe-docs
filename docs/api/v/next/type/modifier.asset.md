#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.11.1`)  


---

## `luxe: type/modifier.asset` module

- [Asset](#asset)   
- [ModifierMeta](#modifiermeta)   
- [ModifierPhase](#modifierphase)   
- [ModifierStage](#modifierstage)   

---

### Asset
`:::js import "luxe: type/modifier.asset" for Asset`
> no docs found

- [ext](#Asset.ext)
- [subtype](#Asset.subtype)
- [is_data](#Asset.is_data)
- [before](#Asset.before)
- [new](#Asset.new+2)(**type_id**: `String`, **ctx**: `AssetContext`)
- [should_skip](#Asset.should_skip)(**asset**: `AssetID`)
- [pre](#Asset.pre)(**assets**: `List`)
- [write_api](#Asset.write_api+2)(**asset**: `AssetID`, **block**: `Map`)
- [find_class_with_meta](#Asset.find_class_with_meta+2)(**ast**: `Module`, **tag**: `String`)
- [is_foreign](#Asset.is_foreign)(**asset**: `AssetID`)
- [is_hidden](#Asset.is_hidden)(**asset**: `AssetID`)
- [get_expects](#Asset.get_expects)(**asset**: `AssetID`)
- [write_modifier_meta](#Asset.write_modifier_meta)(**asset**: `AssetID`)
- [process_meta](#Asset.process_meta)()
- [process](#Asset.process+2)(**assets**: `List`, **each**: `Fn`)

<hr/>
<endpoint module="luxe: type/modifier.asset" class="Asset" signature="ext"></endpoint>
<signature id="Asset.ext">Asset.ext
<a class="headerlink" href="#Asset.ext" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/modifier.asset" class="Asset" signature="subtype"></endpoint>
<signature id="Asset.subtype">Asset.subtype
<a class="headerlink" href="#Asset.subtype" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/modifier.asset" class="Asset" signature="is_data"></endpoint>
<signature id="Asset.is_data">Asset.is_data
<a class="headerlink" href="#Asset.is_data" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/modifier.asset" class="Asset" signature="before"></endpoint>
<signature id="Asset.before">Asset.before
<a class="headerlink" href="#Asset.before" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/modifier.asset" class="Asset" signature="new(type_id : String, ctx : AssetContext)"></endpoint>
<signature id="Asset.new+2">Asset.new(**type_id**: `String`, **ctx**: `AssetContext`)
<a class="headerlink" href="#Asset.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Asset`
> no docs found   

<endpoint module="luxe: type/modifier.asset" class="Asset" signature="should_skip(asset : AssetID)"></endpoint>
<signature id="Asset.should_skip">Asset.should_skip(**asset**: `AssetID`)
<a class="headerlink" href="#Asset.should_skip" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/modifier.asset" class="Asset" signature="pre(assets : List)"></endpoint>
<signature id="Asset.pre">Asset.pre(**assets**: `List`)
<a class="headerlink" href="#Asset.pre" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/modifier.asset" class="Asset" signature="write_api(asset : AssetID, block : Map)"></endpoint>
<signature id="Asset.write_api+2">Asset.write_api(**asset**: `AssetID`, **block**: `Map`)
<a class="headerlink" href="#Asset.write_api+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/modifier.asset" class="Asset" signature="find_class_with_meta(ast : Module, tag : String)"></endpoint>
<signature id="Asset.find_class_with_meta+2">Asset.find_class_with_meta(**ast**: `Module`, **tag**: `String`)
<a class="headerlink" href="#Asset.find_class_with_meta+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js ClassStmt`
> no docs found   

<endpoint module="luxe: type/modifier.asset" class="Asset" signature="is_foreign(asset : AssetID)"></endpoint>
<signature id="Asset.is_foreign">Asset.is_foreign(**asset**: `AssetID`)
<a class="headerlink" href="#Asset.is_foreign" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: type/modifier.asset" class="Asset" signature="is_hidden(asset : AssetID)"></endpoint>
<signature id="Asset.is_hidden">Asset.is_hidden(**asset**: `AssetID`)
<a class="headerlink" href="#Asset.is_hidden" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: type/modifier.asset" class="Asset" signature="get_expects(asset : AssetID)"></endpoint>
<signature id="Asset.get_expects">Asset.get_expects(**asset**: `AssetID`)
<a class="headerlink" href="#Asset.get_expects" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: type/modifier.asset" class="Asset" signature="write_modifier_meta(asset : AssetID)"></endpoint>
<signature id="Asset.write_modifier_meta">Asset.write_modifier_meta(**asset**: `AssetID`)
<a class="headerlink" href="#Asset.write_modifier_meta" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/modifier.asset" class="Asset" signature="process_meta()"></endpoint>
<signature id="Asset.process_meta">Asset.process_meta()
<a class="headerlink" href="#Asset.process_meta" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/modifier.asset" class="Asset" signature="process(assets : List, each : Fn)"></endpoint>
<signature id="Asset.process+2">Asset.process(**assets**: `List`, **each**: `Fn`)
<a class="headerlink" href="#Asset.process+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### ModifierMeta
`:::js import "luxe: type/modifier.asset" for ModifierMeta`
> no docs found


<hr/>
### ModifierPhase
`:::js import "luxe: type/modifier.asset" for ModifierPhase`
> no docs found


<hr/>
### ModifierStage
`:::js import "luxe: type/modifier.asset" for ModifierStage`
> no docs found

- [before](#ModifierStage.before)
- [on](#ModifierStage.on)
- [after](#ModifierStage.after)

<hr/>
<endpoint module="luxe: type/modifier.asset" class="ModifierStage" signature="before"></endpoint>
<signature id="ModifierStage.before">ModifierStage.before
<a class="headerlink" href="#ModifierStage.before" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/modifier.asset" class="ModifierStage" signature="on"></endpoint>
<signature id="ModifierStage.on">ModifierStage.on
<a class="headerlink" href="#ModifierStage.on" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/modifier.asset" class="ModifierStage" signature="after"></endpoint>
<signature id="ModifierStage.after">ModifierStage.after
<a class="headerlink" href="#ModifierStage.after" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

