#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.11.0`)  


---

## `luxe: asset/type` module

- [AssetArtifact](#assetartifact)   
- [AssetContext](#assetcontext)   
- [AssetID](#assetid)   
- [AssetType](#assettype)   
- [AssetTypeID](#assettypeid)   

---

### AssetArtifact
`:::js import "luxe: asset/type" for AssetArtifact`
> no docs found

- [id](#AssetArtifact.id)
- [type](#AssetArtifact.type)
- [path](#AssetArtifact.path)
- [new](#AssetArtifact.new+3)(**type**: `String`, **id**: `String`, **path**: `String`)

<hr/>
<endpoint module="luxe: asset/type" class="AssetArtifact" signature="id"></endpoint>
<signature id="AssetArtifact.id">AssetArtifact.id
<a class="headerlink" href="#AssetArtifact.id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetArtifact" signature="type"></endpoint>
<signature id="AssetArtifact.type">AssetArtifact.type
<a class="headerlink" href="#AssetArtifact.type" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetArtifact" signature="path"></endpoint>
<signature id="AssetArtifact.path">AssetArtifact.path
<a class="headerlink" href="#AssetArtifact.path" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetArtifact" signature="new(type : String, id : String, path : String)"></endpoint>
<signature id="AssetArtifact.new+3">AssetArtifact.new(**type**: `String`, **id**: `String`, **path**: `String`)
<a class="headerlink" href="#AssetArtifact.new+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AssetArtifact`
> no docs found   

### AssetContext
`:::js import "luxe: asset/type" for AssetContext`
> no docs found

- [id](#AssetContext.id)
- [db](#AssetContext.db)
- [artifacts](#AssetContext.artifacts)
- [artifacts_for](#AssetContext.artifacts_for)(**type_id**: `String`)
- [tagged](#AssetContext.tagged)(**tag**: `String`)
- [tag](#AssetContext.tag+2)(**tag**: `String`, **value**: `Any`)
- [TYPE](#AssetContext.TYPE)
- [DEV](#AssetContext.DEV)
- [RELEASE](#AssetContext.RELEASE)
- [new](#AssetContext.new+3)(**id**: `String`, **db**: `Any`, **artifact_root**: `String`)
- [set_modified](#AssetContext.set_modified+2)(**type**: `String`, **modified**: `List`)
- [get_modified](#AssetContext.get_modified)(**type**: `String`)
- [get_modified](#AssetContext.get_modified)()
- [skip](#AssetContext.skip)(**id**: `String`)
- [skipped](#AssetContext.skipped)(**id**: `String`)
- [emit_path](#AssetContext.emit_path)(**id**: `String`)
- [emit_path](#AssetContext.emit_path+2)(**id**: `String`, **extra**: `String`)
- [emit](#AssetContext.emit+3)(**type_id**: `String`, **artifact_id**: `String`, **artifact_path**: `String`)

<hr/>
<endpoint module="luxe: asset/type" class="AssetContext" signature="id"></endpoint>
<signature id="AssetContext.id">AssetContext.id
<a class="headerlink" href="#AssetContext.id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetContext" signature="db"></endpoint>
<signature id="AssetContext.db">AssetContext.db
<a class="headerlink" href="#AssetContext.db" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetContext" signature="artifacts"></endpoint>
<signature id="AssetContext.artifacts">AssetContext.artifacts
<a class="headerlink" href="#AssetContext.artifacts" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Map`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetContext" signature="artifacts_for(type_id : String)"></endpoint>
<signature id="AssetContext.artifacts_for">AssetContext.artifacts_for(**type_id**: `String`)
<a class="headerlink" href="#AssetContext.artifacts_for" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetContext" signature="tagged(tag : String)"></endpoint>
<signature id="AssetContext.tagged">AssetContext.tagged(**tag**: `String`)
<a class="headerlink" href="#AssetContext.tagged" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Any`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetContext" signature="tag(tag : String, value : Any)"></endpoint>
<signature id="AssetContext.tag+2">AssetContext.tag(**tag**: `String`, **value**: `Any`)
<a class="headerlink" href="#AssetContext.tag+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetContext" signature="TYPE"></endpoint>
<signature id="AssetContext.TYPE">AssetContext.TYPE
<a class="headerlink" href="#AssetContext.TYPE" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetContext" signature="DEV"></endpoint>
<signature id="AssetContext.DEV">AssetContext.DEV
<a class="headerlink" href="#AssetContext.DEV" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetContext" signature="RELEASE"></endpoint>
<signature id="AssetContext.RELEASE">AssetContext.RELEASE
<a class="headerlink" href="#AssetContext.RELEASE" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetContext" signature="new(id : String, db : Any, artifact_root : String)"></endpoint>
<signature id="AssetContext.new+3">AssetContext.new(**id**: `String`, **db**: `Any`, **artifact_root**: `String`)
<a class="headerlink" href="#AssetContext.new+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AssetContext`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetContext" signature="set_modified(type : String, modified : List)"></endpoint>
<signature id="AssetContext.set_modified+2">AssetContext.set_modified(**type**: `String`, **modified**: `List`)
<a class="headerlink" href="#AssetContext.set_modified+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetContext" signature="get_modified(type : String)"></endpoint>
<signature id="AssetContext.get_modified">AssetContext.get_modified(**type**: `String`)
<a class="headerlink" href="#AssetContext.get_modified" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetContext" signature="get_modified()"></endpoint>
<signature id="AssetContext.get_modified">AssetContext.get_modified()
<a class="headerlink" href="#AssetContext.get_modified" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Map`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetContext" signature="skip(id : String)"></endpoint>
<signature id="AssetContext.skip">AssetContext.skip(**id**: `String`)
<a class="headerlink" href="#AssetContext.skip" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetContext" signature="skipped(id : String)"></endpoint>
<signature id="AssetContext.skipped">AssetContext.skipped(**id**: `String`)
<a class="headerlink" href="#AssetContext.skipped" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetContext" signature="emit_path(id : String)"></endpoint>
<signature id="AssetContext.emit_path">AssetContext.emit_path(**id**: `String`)
<a class="headerlink" href="#AssetContext.emit_path" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetContext" signature="emit_path(id : String, extra : String)"></endpoint>
<signature id="AssetContext.emit_path+2">AssetContext.emit_path(**id**: `String`, **extra**: `String`)
<a class="headerlink" href="#AssetContext.emit_path+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetContext" signature="emit(type_id : String, artifact_id : String, artifact_path : String)"></endpoint>
<signature id="AssetContext.emit+3">AssetContext.emit(**type_id**: `String`, **artifact_id**: `String`, **artifact_path**: `String`)
<a class="headerlink" href="#AssetContext.emit+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### AssetID
`:::js import "luxe: asset/type" for AssetID`
> no docs found

- [type_id](#AssetID.type_id)
- [id](#AssetID.id)
- [asset](#AssetID.asset)
- [path](#AssetID.path)
- [ext](#AssetID.ext)
- [subtype](#AssetID.subtype)
- [prefix](#AssetID.prefix)
- [meta_uuid](#AssetID.meta_uuid)
- [new](#AssetID.new+2)(**type_id**: `String`, **map**: `Map`)
- [refresh](#AssetID.refresh)()

<hr/>
<endpoint module="luxe: asset/type" class="AssetID" signature="type_id"></endpoint>
<signature id="AssetID.type_id">AssetID.type_id
<a class="headerlink" href="#AssetID.type_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetID" signature="id"></endpoint>
<signature id="AssetID.id">AssetID.id
<a class="headerlink" href="#AssetID.id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetID" signature="asset"></endpoint>
<signature id="AssetID.asset">AssetID.asset
<a class="headerlink" href="#AssetID.asset" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetID" signature="path"></endpoint>
<signature id="AssetID.path">AssetID.path
<a class="headerlink" href="#AssetID.path" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetID" signature="ext"></endpoint>
<signature id="AssetID.ext">AssetID.ext
<a class="headerlink" href="#AssetID.ext" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetID" signature="subtype"></endpoint>
<signature id="AssetID.subtype">AssetID.subtype
<a class="headerlink" href="#AssetID.subtype" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetID" signature="prefix"></endpoint>
<signature id="AssetID.prefix">AssetID.prefix
<a class="headerlink" href="#AssetID.prefix" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetID" signature="meta_uuid"></endpoint>
<signature id="AssetID.meta_uuid">AssetID.meta_uuid
<a class="headerlink" href="#AssetID.meta_uuid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetID" signature="new(type_id : String, map : Map)"></endpoint>
<signature id="AssetID.new+2">AssetID.new(**type_id**: `String`, **map**: `Map`)
<a class="headerlink" href="#AssetID.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AssetID`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetID" signature="refresh()"></endpoint>
<signature id="AssetID.refresh">AssetID.refresh()
<a class="headerlink" href="#AssetID.refresh" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### AssetType
`:::js import "luxe: asset/type" for AssetType`
> no docs found

- [type_id](#AssetType.type_id)
- [version_id](#AssetType.version_id)
- [ext](#AssetType.ext)
- [subtype](#AssetType.subtype)
- [ctx](#AssetType.ctx)
- [is_loader](#AssetType.is_loader)
- [is_data](#AssetType.is_data)
- [is_handle](#AssetType.is_handle)
- [version](#AssetType.version)
- [load_before](#AssetType.load_before)
- [load_after](#AssetType.load_after)
- [before](#AssetType.before)
- [after](#AssetType.after)
- [pre_early](#AssetType.pre_early)
- [pre_late](#AssetType.pre_late)
- [new](#AssetType.new+2)(**type_id**: `String`, **ctx**: `AssetContext`)
- [remap](#AssetType.remap+2)(**asset**: `AssetID`, **new_id**: `String`)
- [get_remap](#AssetType.get_remap)(**map**: `Map`)
- [modify](#AssetType.modify)(**asset**: `AssetID`)
- [unmodify](#AssetType.unmodify)(**asset**: `AssetID`)
- [emit_path](#AssetType.emit_path)(**asset**: `AssetID`)
- [skip](#AssetType.skip)(**asset**: `AssetID`)
- [get_data](#AssetType.get_data)(**id**: `String`)
- [set_handle](#AssetType.set_handle+2)(**id**: `String`, **handle**: `Num`)
- [pre](#AssetType.pre)(**assets**: `List`)
- [process](#AssetType.process+2)(**assets**: `List`, **each**: `Fn`)
- [loader](#AssetType.loader)(**assets**: `List`)

<hr/>
<endpoint module="luxe: asset/type" class="AssetType" signature="type_id"></endpoint>
<signature id="AssetType.type_id">AssetType.type_id
<a class="headerlink" href="#AssetType.type_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="version_id"></endpoint>
<signature id="AssetType.version_id">AssetType.version_id
<a class="headerlink" href="#AssetType.version_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="ext"></endpoint>
<signature id="AssetType.ext">AssetType.ext
<a class="headerlink" href="#AssetType.ext" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="subtype"></endpoint>
<signature id="AssetType.subtype">AssetType.subtype
<a class="headerlink" href="#AssetType.subtype" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="ctx"></endpoint>
<signature id="AssetType.ctx">AssetType.ctx
<a class="headerlink" href="#AssetType.ctx" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AssetContext`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="is_loader"></endpoint>
<signature id="AssetType.is_loader">AssetType.is_loader
<a class="headerlink" href="#AssetType.is_loader" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="is_data"></endpoint>
<signature id="AssetType.is_data">AssetType.is_data
<a class="headerlink" href="#AssetType.is_data" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="is_handle"></endpoint>
<signature id="AssetType.is_handle">AssetType.is_handle
<a class="headerlink" href="#AssetType.is_handle" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="version"></endpoint>
<signature id="AssetType.version">AssetType.version
<a class="headerlink" href="#AssetType.version" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="load_before"></endpoint>
<signature id="AssetType.load_before">AssetType.load_before
<a class="headerlink" href="#AssetType.load_before" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="load_after"></endpoint>
<signature id="AssetType.load_after">AssetType.load_after
<a class="headerlink" href="#AssetType.load_after" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="before"></endpoint>
<signature id="AssetType.before">AssetType.before
<a class="headerlink" href="#AssetType.before" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="after"></endpoint>
<signature id="AssetType.after">AssetType.after
<a class="headerlink" href="#AssetType.after" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="pre_early"></endpoint>
<signature id="AssetType.pre_early">AssetType.pre_early
<a class="headerlink" href="#AssetType.pre_early" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="pre_late"></endpoint>
<signature id="AssetType.pre_late">AssetType.pre_late
<a class="headerlink" href="#AssetType.pre_late" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="new(type_id : String, ctx : AssetContext)"></endpoint>
<signature id="AssetType.new+2">AssetType.new(**type_id**: `String`, **ctx**: `AssetContext`)
<a class="headerlink" href="#AssetType.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AssetType`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="remap(asset : AssetID, new_id : String)"></endpoint>
<signature id="AssetType.remap+2">AssetType.remap(**asset**: `AssetID`, **new_id**: `String`)
<a class="headerlink" href="#AssetType.remap+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="get_remap(map : Map)"></endpoint>
<signature id="AssetType.get_remap">AssetType.get_remap(**map**: `Map`)
<a class="headerlink" href="#AssetType.get_remap" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Map`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="modify(asset : AssetID)"></endpoint>
<signature id="AssetType.modify">AssetType.modify(**asset**: `AssetID`)
<a class="headerlink" href="#AssetType.modify" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="unmodify(asset : AssetID)"></endpoint>
<signature id="AssetType.unmodify">AssetType.unmodify(**asset**: `AssetID`)
<a class="headerlink" href="#AssetType.unmodify" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="emit_path(asset : AssetID)"></endpoint>
<signature id="AssetType.emit_path">AssetType.emit_path(**asset**: `AssetID`)
<a class="headerlink" href="#AssetType.emit_path" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="skip(asset : AssetID)"></endpoint>
<signature id="AssetType.skip">AssetType.skip(**asset**: `AssetID`)
<a class="headerlink" href="#AssetType.skip" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="get_data(id : String)"></endpoint>
<signature id="AssetType.get_data">AssetType.get_data(**id**: `String`)
<a class="headerlink" href="#AssetType.get_data" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="set_handle(id : String, handle : Num)"></endpoint>
<signature id="AssetType.set_handle+2">AssetType.set_handle(**id**: `String`, **handle**: `Num`)
<a class="headerlink" href="#AssetType.set_handle+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="pre(assets : List)"></endpoint>
<signature id="AssetType.pre">AssetType.pre(**assets**: `List`)
<a class="headerlink" href="#AssetType.pre" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="process(assets : List, each : Fn)"></endpoint>
<signature id="AssetType.process+2">AssetType.process(**assets**: `List`, **each**: `Fn`)
<a class="headerlink" href="#AssetType.process+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetType" signature="loader(assets : List)"></endpoint>
<signature id="AssetType.loader">AssetType.loader(**assets**: `List`)
<a class="headerlink" href="#AssetType.loader" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

### AssetTypeID
`:::js import "luxe: asset/type" for AssetTypeID`
> no docs found

- [block](#AssetTypeID.block)
- [block](#AssetTypeID.block=)=(v : Any)
- [block_class](#AssetTypeID.block_class)
- [block_class](#AssetTypeID.block_class=)=(v : Any)
- [loader](#AssetTypeID.loader)
- [loader](#AssetTypeID.loader=)=(v : Any)
- [handler](#AssetTypeID.handler)
- [handler](#AssetTypeID.handler=)=(v : Any)
- [new](#AssetTypeID.new)(**map**: `Map`)

<hr/>
<endpoint module="luxe: asset/type" class="AssetTypeID" signature="block"></endpoint>
<signature id="AssetTypeID.block">AssetTypeID.block
<a class="headerlink" href="#AssetTypeID.block" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetTypeID" signature="block=(v : Any)"></endpoint>
<signature id="AssetTypeID.block=">AssetTypeID.block=(v : Any)
<a class="headerlink" href="#AssetTypeID.block=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetTypeID" signature="block_class"></endpoint>
<signature id="AssetTypeID.block_class">AssetTypeID.block_class
<a class="headerlink" href="#AssetTypeID.block_class" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetTypeID" signature="block_class=(v : Any)"></endpoint>
<signature id="AssetTypeID.block_class=">AssetTypeID.block_class=(v : Any)
<a class="headerlink" href="#AssetTypeID.block_class=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetTypeID" signature="loader"></endpoint>
<signature id="AssetTypeID.loader">AssetTypeID.loader
<a class="headerlink" href="#AssetTypeID.loader" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetTypeID" signature="loader=(v : Any)"></endpoint>
<signature id="AssetTypeID.loader=">AssetTypeID.loader=(v : Any)
<a class="headerlink" href="#AssetTypeID.loader=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetTypeID" signature="handler"></endpoint>
<signature id="AssetTypeID.handler">AssetTypeID.handler
<a class="headerlink" href="#AssetTypeID.handler" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AssetType`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetTypeID" signature="handler=(v : Any)"></endpoint>
<signature id="AssetTypeID.handler=">AssetTypeID.handler=(v : Any)
<a class="headerlink" href="#AssetTypeID.handler=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AssetType`
> no docs found   

<endpoint module="luxe: asset/type" class="AssetTypeID" signature="new(map : Map)"></endpoint>
<signature id="AssetTypeID.new">AssetTypeID.new(**map**: `Map`)
<a class="headerlink" href="#AssetTypeID.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AssetTypeID`
> no docs found   

