#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.10.1`)  


---

## `luxe: type/entity.asset` module

- [Asset](#asset)   
- [CompiledModifier](#compiledmodifier)   
- [ContextContents](#contextcontents)   
- [EntityContext](#entitycontext)   
- [EntityInfo](#entityinfo)   
- [ModifierInfo](#modifierinfo)   
- [OverrideInfo](#overrideinfo)   
- [PrototypeInfo](#prototypeinfo)   

---

### Asset
`:::js import "luxe: type/entity.asset" for Asset`
> no docs found

- [subtype](#Asset.subtype)
- [after](#Asset.after)
- [before](#Asset.before)
- [new](#Asset.new+2)(**type_id**: `String`, **ctx**: `AssetContext`)
- [add_info](#Asset.add_info+4)(**into**: `Map`, **asset**: `AssetID`, **start**: `Num`, **range**: `Num`)
- [pre](#Asset.pre)(**assets**: `List`)

<hr/>
<endpoint module="luxe: type/entity.asset" class="Asset" signature="subtype"></endpoint>
<signature id="Asset.subtype">Asset.subtype
<a class="headerlink" href="#Asset.subtype" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="Asset" signature="after"></endpoint>
<signature id="Asset.after">Asset.after
<a class="headerlink" href="#Asset.after" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="Asset" signature="before"></endpoint>
<signature id="Asset.before">Asset.before
<a class="headerlink" href="#Asset.before" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="Asset" signature="new(type_id : String, ctx : AssetContext)"></endpoint>
<signature id="Asset.new+2">Asset.new(**type_id**: `String`, **ctx**: `AssetContext`)
<a class="headerlink" href="#Asset.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Asset`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="Asset" signature="add_info(into : Map, asset : AssetID, start : Num, range : Num)"></endpoint>
<signature id="Asset.add_info+4">Asset.add_info(**into**: `Map`, **asset**: `AssetID`, **start**: `Num`, **range**: `Num`)
<a class="headerlink" href="#Asset.add_info+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="Asset" signature="pre(assets : List)"></endpoint>
<signature id="Asset.pre">Asset.pre(**assets**: `List`)
<a class="headerlink" href="#Asset.pre" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### CompiledModifier
`:::js import "luxe: type/entity.asset" for CompiledModifier`
> no docs found

- [id](#CompiledModifier.id)
- [block](#CompiledModifier.block)
- [block](#CompiledModifier.block=)=(v : Any)
- [new](#CompiledModifier.new+2)(**id**: `String`, **block**: `Block`)

<hr/>
<endpoint module="luxe: type/entity.asset" class="CompiledModifier" signature="id"></endpoint>
<signature id="CompiledModifier.id">CompiledModifier.id
<a class="headerlink" href="#CompiledModifier.id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="CompiledModifier" signature="block"></endpoint>
<signature id="CompiledModifier.block">CompiledModifier.block
<a class="headerlink" href="#CompiledModifier.block" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Block`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="CompiledModifier" signature="block=(v : Any)"></endpoint>
<signature id="CompiledModifier.block=">CompiledModifier.block=(v : Any)
<a class="headerlink" href="#CompiledModifier.block=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="CompiledModifier" signature="new(id : String, block : Block)"></endpoint>
<signature id="CompiledModifier.new+2">CompiledModifier.new(**id**: `String`, **block**: `Block`)
<a class="headerlink" href="#CompiledModifier.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js CompiledModifier`
> no docs found   

### ContextContents
`:::js import "luxe: type/entity.asset" for ContextContents`
> no docs found

- [entities](#ContextContents.entities)
- [by_modifier](#ContextContents.by_modifier)
- [compiled_modifiers](#ContextContents.compiled_modifiers)
- [prototypes](#ContextContents.prototypes)
- [overrides](#ContextContents.overrides)
- [by_modifier_overrides](#ContextContents.by_modifier_overrides)
- [compiled_overrides](#ContextContents.compiled_overrides)
- [asset](#ContextContents.asset)
- [subtype](#ContextContents.subtype)
- [context_uuid](#ContextContents.context_uuid)
- [new](#ContextContents.new+4)(**ctx**: `AssetContext`, **asset**: `AssetID`, **subtype**: `String`, **context_uuid**: `String`)

<hr/>
<endpoint module="luxe: type/entity.asset" class="ContextContents" signature="entities"></endpoint>
<signature id="ContextContents.entities">ContextContents.entities
<a class="headerlink" href="#ContextContents.entities" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="ContextContents" signature="by_modifier"></endpoint>
<signature id="ContextContents.by_modifier">ContextContents.by_modifier
<a class="headerlink" href="#ContextContents.by_modifier" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="ContextContents" signature="compiled_modifiers"></endpoint>
<signature id="ContextContents.compiled_modifiers">ContextContents.compiled_modifiers
<a class="headerlink" href="#ContextContents.compiled_modifiers" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="ContextContents" signature="prototypes"></endpoint>
<signature id="ContextContents.prototypes">ContextContents.prototypes
<a class="headerlink" href="#ContextContents.prototypes" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="ContextContents" signature="overrides"></endpoint>
<signature id="ContextContents.overrides">ContextContents.overrides
<a class="headerlink" href="#ContextContents.overrides" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="ContextContents" signature="by_modifier_overrides"></endpoint>
<signature id="ContextContents.by_modifier_overrides">ContextContents.by_modifier_overrides
<a class="headerlink" href="#ContextContents.by_modifier_overrides" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="ContextContents" signature="compiled_overrides"></endpoint>
<signature id="ContextContents.compiled_overrides">ContextContents.compiled_overrides
<a class="headerlink" href="#ContextContents.compiled_overrides" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="ContextContents" signature="asset"></endpoint>
<signature id="ContextContents.asset">ContextContents.asset
<a class="headerlink" href="#ContextContents.asset" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="ContextContents" signature="subtype"></endpoint>
<signature id="ContextContents.subtype">ContextContents.subtype
<a class="headerlink" href="#ContextContents.subtype" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="ContextContents" signature="context_uuid"></endpoint>
<signature id="ContextContents.context_uuid">ContextContents.context_uuid
<a class="headerlink" href="#ContextContents.context_uuid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="ContextContents" signature="new(ctx : AssetContext, asset : AssetID, subtype : String, context_uuid : String)"></endpoint>
<signature id="ContextContents.new+4">ContextContents.new(**ctx**: `AssetContext`, **asset**: `AssetID`, **subtype**: `String`, **context_uuid**: `String`)
<a class="headerlink" href="#ContextContents.new+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js ContextContents`
> no docs found   

### EntityContext
`:::js import "luxe: type/entity.asset" for EntityContext`
> no docs found

- [compile](#EntityContext.compile+5)(**ctx**: `AssetContext`, **asset**: `AssetID`, **to_path**: `String`, **subtype**: `String`, **tag**: `String`)
- [process_modifiers](#EntityContext.process_modifiers)(**contents**: `ContextContents`)
- [compile_modifiers](#EntityContext.compile_modifiers+4)(**subtype**: `String`, **context**: `AssetID`, **by_modifier**: `Map`, **into**: `List`)
- [write](#EntityContext.write+3)(**contents**: `ContextContents`, **to_path**: `String`, **tag**: `String`)
- [get_modifiers](#EntityContext.get_modifiers+4)(**subtype**: `String`, **entity**: `EntityInfo`, **entity_lx**: `Map`, **into**: `Map`)
- [get_contents](#EntityContext.get_contents+3)(**ctx**: `AssetContext`, **asset**: `AssetID`, **subtype**: `String`)

<hr/>
<endpoint module="luxe: type/entity.asset" class="EntityContext" signature="compile(ctx : AssetContext, asset : AssetID, to_path : String, subtype : String, tag : String)"></endpoint>
<signature id="EntityContext.compile+5">EntityContext.compile(**ctx**: `AssetContext`, **asset**: `AssetID`, **to_path**: `String`, **subtype**: `String`, **tag**: `String`)
<a class="headerlink" href="#EntityContext.compile+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="EntityContext" signature="process_modifiers(contents : ContextContents)"></endpoint>
<signature id="EntityContext.process_modifiers">EntityContext.process_modifiers(**contents**: `ContextContents`)
<a class="headerlink" href="#EntityContext.process_modifiers" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="EntityContext" signature="compile_modifiers(subtype : String, context : AssetID, by_modifier : Map, into : List)"></endpoint>
<signature id="EntityContext.compile_modifiers+4">EntityContext.compile_modifiers(**subtype**: `String`, **context**: `AssetID`, **by_modifier**: `Map`, **into**: `List`)
<a class="headerlink" href="#EntityContext.compile_modifiers+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="EntityContext" signature="write(contents : ContextContents, to_path : String, tag : String)"></endpoint>
<signature id="EntityContext.write+3">EntityContext.write(**contents**: `ContextContents`, **to_path**: `String`, **tag**: `String`)
<a class="headerlink" href="#EntityContext.write+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="EntityContext" signature="get_modifiers(subtype : String, entity : EntityInfo, entity_lx : Map, into : Map)"></endpoint>
<signature id="EntityContext.get_modifiers+4">EntityContext.get_modifiers(**subtype**: `String`, **entity**: `EntityInfo`, **entity_lx**: `Map`, **into**: `Map`)
<a class="headerlink" href="#EntityContext.get_modifiers+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="EntityContext" signature="get_contents(ctx : AssetContext, asset : AssetID, subtype : String)"></endpoint>
<signature id="EntityContext.get_contents+3">EntityContext.get_contents(**ctx**: `AssetContext`, **asset**: `AssetID`, **subtype**: `String`)
<a class="headerlink" href="#EntityContext.get_contents+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js ContextContents`
> no docs found   

### EntityInfo
`:::js import "luxe: type/entity.asset" for EntityInfo`
> no docs found

- [context](#EntityInfo.context)
- [asset](#EntityInfo.asset)
- [uuid](#EntityInfo.uuid)
- [uuid](#EntityInfo.uuid=)=(v : Any)
- [relative](#EntityInfo.relative)
- [relative](#EntityInfo.relative=)=(v : Any)
- [name](#EntityInfo.name)
- [name](#EntityInfo.name=)=(v : Any)
- [index](#EntityInfo.index)
- [index](#EntityInfo.index=)=(v : Any)
- [new](#EntityInfo.new+2)(**asset**: `AssetID`, **context**: `AssetID`)

<hr/>
<endpoint module="luxe: type/entity.asset" class="EntityInfo" signature="context"></endpoint>
<signature id="EntityInfo.context">EntityInfo.context
<a class="headerlink" href="#EntityInfo.context" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AssetID`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="EntityInfo" signature="asset"></endpoint>
<signature id="EntityInfo.asset">EntityInfo.asset
<a class="headerlink" href="#EntityInfo.asset" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AssetID`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="EntityInfo" signature="uuid"></endpoint>
<signature id="EntityInfo.uuid">EntityInfo.uuid
<a class="headerlink" href="#EntityInfo.uuid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="EntityInfo" signature="uuid=(v : Any)"></endpoint>
<signature id="EntityInfo.uuid=">EntityInfo.uuid=(v : Any)
<a class="headerlink" href="#EntityInfo.uuid=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="EntityInfo" signature="relative"></endpoint>
<signature id="EntityInfo.relative">EntityInfo.relative
<a class="headerlink" href="#EntityInfo.relative" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="EntityInfo" signature="relative=(v : Any)"></endpoint>
<signature id="EntityInfo.relative=">EntityInfo.relative=(v : Any)
<a class="headerlink" href="#EntityInfo.relative=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="EntityInfo" signature="name"></endpoint>
<signature id="EntityInfo.name">EntityInfo.name
<a class="headerlink" href="#EntityInfo.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="EntityInfo" signature="name=(v : Any)"></endpoint>
<signature id="EntityInfo.name=">EntityInfo.name=(v : Any)
<a class="headerlink" href="#EntityInfo.name=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="EntityInfo" signature="index"></endpoint>
<signature id="EntityInfo.index">EntityInfo.index
<a class="headerlink" href="#EntityInfo.index" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="EntityInfo" signature="index=(v : Any)"></endpoint>
<signature id="EntityInfo.index=">EntityInfo.index=(v : Any)
<a class="headerlink" href="#EntityInfo.index=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="EntityInfo" signature="new(asset : AssetID, context : AssetID)"></endpoint>
<signature id="EntityInfo.new+2">EntityInfo.new(**asset**: `AssetID`, **context**: `AssetID`)
<a class="headerlink" href="#EntityInfo.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js EntityInfo`
> no docs found   

### ModifierInfo
`:::js import "luxe: type/entity.asset" for ModifierInfo`
> no docs found

- [type_id](#ModifierInfo.type_id)
- [entity](#ModifierInfo.entity)
- [data](#ModifierInfo.data)
- [new](#ModifierInfo.new+3)(**type_id**: `String`, **entity**: `EntityInfo`, **data**: `Map`)

<hr/>
<endpoint module="luxe: type/entity.asset" class="ModifierInfo" signature="type_id"></endpoint>
<signature id="ModifierInfo.type_id">ModifierInfo.type_id
<a class="headerlink" href="#ModifierInfo.type_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="ModifierInfo" signature="entity"></endpoint>
<signature id="ModifierInfo.entity">ModifierInfo.entity
<a class="headerlink" href="#ModifierInfo.entity" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js EntityInfo`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="ModifierInfo" signature="data"></endpoint>
<signature id="ModifierInfo.data">ModifierInfo.data
<a class="headerlink" href="#ModifierInfo.data" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Map`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="ModifierInfo" signature="new(type_id : String, entity : EntityInfo, data : Map)"></endpoint>
<signature id="ModifierInfo.new+3">ModifierInfo.new(**type_id**: `String`, **entity**: `EntityInfo`, **data**: `Map`)
<a class="headerlink" href="#ModifierInfo.new+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js ModifierInfo`
> no docs found   

### OverrideInfo
`:::js import "luxe: type/entity.asset" for OverrideInfo`
> no docs found

- [address](#OverrideInfo.address)
- [address](#OverrideInfo.address=)=(v : Num)
- [new](#OverrideInfo.new+2)(**asset**: `AssetID`, **context**: `AssetID`)

<hr/>
<endpoint module="luxe: type/entity.asset" class="OverrideInfo" signature="address"></endpoint>
<signature id="OverrideInfo.address">OverrideInfo.address
<a class="headerlink" href="#OverrideInfo.address" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="OverrideInfo" signature="address=(v : Num)"></endpoint>
<signature id="OverrideInfo.address=">OverrideInfo.address=(v : Num)
<a class="headerlink" href="#OverrideInfo.address=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="OverrideInfo" signature="new(asset : AssetID, context : AssetID)"></endpoint>
<signature id="OverrideInfo.new+2">OverrideInfo.new(**asset**: `AssetID`, **context**: `AssetID`)
<a class="headerlink" href="#OverrideInfo.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js OverrideInfo`
> no docs found   

### PrototypeInfo
`:::js import "luxe: type/entity.asset" for PrototypeInfo`
> no docs found

- [root](#PrototypeInfo.root)
- [source](#PrototypeInfo.source)
- [source_id](#PrototypeInfo.source_id)
- [new](#PrototypeInfo.new+2)(**entity**: `EntityInfo`, **source**: `AssetID`)

<hr/>
<endpoint module="luxe: type/entity.asset" class="PrototypeInfo" signature="root"></endpoint>
<signature id="PrototypeInfo.root">PrototypeInfo.root
<a class="headerlink" href="#PrototypeInfo.root" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js EntityInfo`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="PrototypeInfo" signature="source"></endpoint>
<signature id="PrototypeInfo.source">PrototypeInfo.source
<a class="headerlink" href="#PrototypeInfo.source" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AssetID`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="PrototypeInfo" signature="source_id"></endpoint>
<signature id="PrototypeInfo.source_id">PrototypeInfo.source_id
<a class="headerlink" href="#PrototypeInfo.source_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: type/entity.asset" class="PrototypeInfo" signature="new(entity : EntityInfo, source : AssetID)"></endpoint>
<signature id="PrototypeInfo.new+2">PrototypeInfo.new(**entity**: `EntityInfo`, **source**: `AssetID`)
<a class="headerlink" href="#PrototypeInfo.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js PrototypeInfo`
> no docs found   

