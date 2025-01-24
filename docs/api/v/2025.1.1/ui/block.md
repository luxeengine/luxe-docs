#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2025.1.1`)  


---

## `luxe: ui/block` module

- [BlockListener](#blocklistener)   
- [ModifiedPip](#modifiedpip)   
- [UIBlock](#uiblock)   
- [UIBlockAssetEvent](#uiblockassetevent)   
- [UIBlockChange](#uiblockchange)   
- [UIBlockChangeType](#uiblockchangetype)   
- [UIBlockEventType](#uiblockeventtype)   
- [UIBlockLinkEvent](#uiblocklinkevent)   
- [UIBlockState](#uiblockstate)   

---

### BlockListener
`:::js import "luxe: ui/block" for BlockListener`
> no docs found

- [block](#BlockListener.block)
- [handle](#BlockListener.handle)
- [new](#BlockListener.new+2)(**block**: `Block`, **handle**: `Handle`)

<hr/>
<endpoint module="luxe: ui/block" class="BlockListener" signature="block"></endpoint>
<signature id="BlockListener.block">BlockListener.block
<a class="headerlink" href="#BlockListener.block" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Block`
> no docs found   

<endpoint module="luxe: ui/block" class="BlockListener" signature="handle"></endpoint>
<signature id="BlockListener.handle">BlockListener.handle
<a class="headerlink" href="#BlockListener.handle" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Handle`
> no docs found   

<endpoint module="luxe: ui/block" class="BlockListener" signature="new(block : Block, handle : Handle)"></endpoint>
<signature id="BlockListener.new+2">BlockListener.new(**block**: `Block`, **handle**: `Handle`)
<a class="headerlink" href="#BlockListener.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js BlockListener`
> no docs found   

### ModifiedPip
`:::js import "luxe: ui/block" for ModifiedPip`
> no docs found

- [control](#ModifiedPip.control)
- [kind](#ModifiedPip.kind)
- [kind](#ModifiedPip.kind=)=(value : BlockFieldModified)
- [color](#ModifiedPip.color)
- [new](#ModifiedPip.new+2)(**ui**: `UI`, **kind**: `BlockFieldModified`)

<hr/>
<endpoint module="luxe: ui/block" class="ModifiedPip" signature="control"></endpoint>
<signature id="ModifiedPip.control">ModifiedPip.control
<a class="headerlink" href="#ModifiedPip.control" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Control`
> no docs found   

<endpoint module="luxe: ui/block" class="ModifiedPip" signature="kind"></endpoint>
<signature id="ModifiedPip.kind">ModifiedPip.kind
<a class="headerlink" href="#ModifiedPip.kind" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js BlockFieldModified`
> no docs found   

<endpoint module="luxe: ui/block" class="ModifiedPip" signature="kind=(value : BlockFieldModified)"></endpoint>
<signature id="ModifiedPip.kind=">ModifiedPip.kind=(value : BlockFieldModified)
<a class="headerlink" href="#ModifiedPip.kind=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="ModifiedPip" signature="color"></endpoint>
<signature id="ModifiedPip.color">ModifiedPip.color
<a class="headerlink" href="#ModifiedPip.color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="ModifiedPip" signature="new(ui : UI, kind : BlockFieldModified)"></endpoint>
<signature id="ModifiedPip.new+2">ModifiedPip.new(**ui**: `UI`, **kind**: `BlockFieldModified`)
<a class="headerlink" href="#ModifiedPip.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js ModifiedPip`
> no docs found   

### UIBlock
`:::js import "luxe: ui/block" for UIBlock`
> no docs found

- [create](#UIBlock.create)(**ui**: `Entity`)
- [set_block_instance](#UIBlock.set_block_instance+3)(**control**: `Control`, **block**: `Block`, **instance**: `BlockInstance`)
- [set_block_instances](#UIBlock.set_block_instances+3)(**control**: `Control`, **block**: `Block`, **instances**: `List`)
- [set_blocks_instances](#UIBlock.set_blocks_instances+3)(**control**: `Control`, **blocks**: `List`, **instances**: `List`)
- [set_sizes](#UIBlock.set_sizes+4)(**control**: `Control`, **label_width**: `Num`, **label_size**: `Num`, **field_height**: `Num`)
- [refresh](#UIBlock.refresh)(**control**: `Control`)
- [get_handle_assets](#UIBlock.get_handle_assets)(**control**: `Control`)
- [set_handle_assets](#UIBlock.set_handle_assets+2)(**control**: `Control`, **yes**: `Bool`)
- [set_show_defaults](#UIBlock.set_show_defaults+2)(**control**: `Control`, **yes**: `Bool`)
- [get_block_fields](#UIBlock.get_block_fields)(**control**: `Any`)

<hr/>
<endpoint module="luxe: ui/block" class="UIBlock" signature="create(ui : Entity)"></endpoint>
<signature id="UIBlock.create">UIBlock.create(**ui**: `Entity`)
<a class="headerlink" href="#UIBlock.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlock" signature="set_block_instance(control : Control, block : Block, instance : BlockInstance)"></endpoint>
<signature id="UIBlock.set_block_instance+3">UIBlock.set_block_instance(**control**: `Control`, **block**: `Block`, **instance**: `BlockInstance`)
<a class="headerlink" href="#UIBlock.set_block_instance+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlock" signature="set_block_instances(control : Control, block : Block, instances : List)"></endpoint>
<signature id="UIBlock.set_block_instances+3">UIBlock.set_block_instances(**control**: `Control`, **block**: `Block`, **instances**: `List`)
<a class="headerlink" href="#UIBlock.set_block_instances+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlock" signature="set_blocks_instances(control : Control, blocks : List, instances : List)"></endpoint>
<signature id="UIBlock.set_blocks_instances+3">UIBlock.set_blocks_instances(**control**: `Control`, **blocks**: `List`, **instances**: `List`)
<a class="headerlink" href="#UIBlock.set_blocks_instances+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlock" signature="set_sizes(control : Control, label_width : Num, label_size : Num, field_height : Num)"></endpoint>
<signature id="UIBlock.set_sizes+4">UIBlock.set_sizes(**control**: `Control`, **label_width**: `Num`, **label_size**: `Num`, **field_height**: `Num`)
<a class="headerlink" href="#UIBlock.set_sizes+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlock" signature="refresh(control : Control)"></endpoint>
<signature id="UIBlock.refresh">UIBlock.refresh(**control**: `Control`)
<a class="headerlink" href="#UIBlock.refresh" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlock" signature="get_handle_assets(control : Control)"></endpoint>
<signature id="UIBlock.get_handle_assets">UIBlock.get_handle_assets(**control**: `Control`)
<a class="headerlink" href="#UIBlock.get_handle_assets" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlock" signature="set_handle_assets(control : Control, yes : Bool)"></endpoint>
<signature id="UIBlock.set_handle_assets+2">UIBlock.set_handle_assets(**control**: `Control`, **yes**: `Bool`)
<a class="headerlink" href="#UIBlock.set_handle_assets+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlock" signature="set_show_defaults(control : Control, yes : Bool)"></endpoint>
<signature id="UIBlock.set_show_defaults+2">UIBlock.set_show_defaults(**control**: `Control`, **yes**: `Bool`)
<a class="headerlink" href="#UIBlock.set_show_defaults+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlock" signature="get_block_fields(control : Any)"></endpoint>
<signature id="UIBlock.get_block_fields">UIBlock.get_block_fields(**control**: `Any`)
<a class="headerlink" href="#UIBlock.get_block_fields" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Map`
> no docs found   

### UIBlockAssetEvent
`:::js import "luxe: ui/block" for UIBlockAssetEvent`
> no docs found

- [tags](#UIBlockAssetEvent.tags)
- [original](#UIBlockAssetEvent.original)
- [new](#UIBlockAssetEvent.new+3)(**tags_in**: `List`, **original_in**: `String`, **fn**: `Fn`)
- [done](#UIBlockAssetEvent.done)(**value**: `String`)

<hr/>
<endpoint module="luxe: ui/block" class="UIBlockAssetEvent" signature="tags"></endpoint>
<signature id="UIBlockAssetEvent.tags">UIBlockAssetEvent.tags
<a class="headerlink" href="#UIBlockAssetEvent.tags" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockAssetEvent" signature="original"></endpoint>
<signature id="UIBlockAssetEvent.original">UIBlockAssetEvent.original
<a class="headerlink" href="#UIBlockAssetEvent.original" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockAssetEvent" signature="new(tags_in : List, original_in : String, fn : Fn)"></endpoint>
<signature id="UIBlockAssetEvent.new+3">UIBlockAssetEvent.new(**tags_in**: `List`, **original_in**: `String`, **fn**: `Fn`)
<a class="headerlink" href="#UIBlockAssetEvent.new+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js UIBlockAssetEvent`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockAssetEvent" signature="done(value : String)"></endpoint>
<signature id="UIBlockAssetEvent.done">UIBlockAssetEvent.done(**value**: `String`)
<a class="headerlink" href="#UIBlockAssetEvent.done" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### UIBlockChange
`:::js import "luxe: ui/block" for UIBlockChange`
> A change in the block ui can inside a nested block, each
> with it's own individual instance, list of nested fields, and list of 
> nested array index values each step down. This tracks that for changes.

- `:::js var change_id : Any = null`
- [new](#UIBlockChange.new+8)(**kind**: `UIBlockChangeType`, **root**: `Block`, **root_instance**: `BlockInstance`, **blocks**: `List`, **instances**: `List`, **fields**: `List`, **indices**: `List`, **edit_value**: `Any`)
- [refresh](#UIBlockChange.refresh)()
- [handle](#UIBlockChange.handle)()
- [set_refresh](#UIBlockChange.set_refresh)(**fn**: `Fn`)
- [set_handler](#UIBlockChange.set_handler)(**fn**: `Fn`)
- [kind](#UIBlockChange.kind)
- [block](#UIBlockChange.block)
- [instance](#UIBlockChange.instance)
- [blocks](#UIBlockChange.blocks)
- [instances](#UIBlockChange.instances)
- [field](#UIBlockChange.field)
- [array_indices](#UIBlockChange.array_indices)
- [field_index](#UIBlockChange.field_index)(**idx**: `Num`)
- [default](#UIBlockChange.default)
- [get_field_value](#UIBlockChange.get_field_value)()
- [get_leaf_value](#UIBlockChange.get_leaf_value)()
- [leaf_block](#UIBlockChange.leaf_block)
- [leaf_instance](#UIBlockChange.leaf_instance)
- [leaf_field_index](#UIBlockChange.leaf_field_index)
- [leaf_array_index](#UIBlockChange.leaf_array_index)
- [get_change_value](#UIBlockChange.get_change_value)()
- [field_is_array](#UIBlockChange.field_is_array)()
- [field_is_object](#UIBlockChange.field_is_object)()
- [value](#UIBlockChange.value)
- [edit_value](#UIBlockChange.edit_value)

<hr/>
<endpoint module="luxe: ui/block" class="UIBlockChange" signature="new(kind : UIBlockChangeType, root : Block, root_instance : BlockInstance, blocks : List, instances : List, fields : List, indices : List, edit_value : Any)"></endpoint>
<signature id="UIBlockChange.new+8">UIBlockChange.new(**kind**: `UIBlockChangeType`, **root**: `Block`, **root_instance**: `BlockInstance`, **blocks**: `List`, **instances**: `List`, **fields**: `List`, **indices**: `List`, **edit_value**: `Any`)
<a class="headerlink" href="#UIBlockChange.new+8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js UIBlockChange`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockChange" signature="refresh()"></endpoint>
<signature id="UIBlockChange.refresh">UIBlockChange.refresh()
<a class="headerlink" href="#UIBlockChange.refresh" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockChange" signature="handle()"></endpoint>
<signature id="UIBlockChange.handle">UIBlockChange.handle()
<a class="headerlink" href="#UIBlockChange.handle" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockChange" signature="set_refresh(fn : Fn)"></endpoint>
<signature id="UIBlockChange.set_refresh">UIBlockChange.set_refresh(**fn**: `Fn`)
<a class="headerlink" href="#UIBlockChange.set_refresh" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockChange" signature="set_handler(fn : Fn)"></endpoint>
<signature id="UIBlockChange.set_handler">UIBlockChange.set_handler(**fn**: `Fn`)
<a class="headerlink" href="#UIBlockChange.set_handler" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockChange" signature="kind"></endpoint>
<signature id="UIBlockChange.kind">UIBlockChange.kind
<a class="headerlink" href="#UIBlockChange.kind" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js UIBlockChangeType`
> The type of change event   

<endpoint module="luxe: ui/block" class="UIBlockChange" signature="block"></endpoint>
<signature id="UIBlockChange.block">UIBlockChange.block
<a class="headerlink" href="#UIBlockChange.block" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Block`
> The root block in which the change occurred   

<endpoint module="luxe: ui/block" class="UIBlockChange" signature="instance"></endpoint>
<signature id="UIBlockChange.instance">UIBlockChange.instance
<a class="headerlink" href="#UIBlockChange.instance" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> The instance of the root block   

<endpoint module="luxe: ui/block" class="UIBlockChange" signature="blocks"></endpoint>
<signature id="UIBlockChange.blocks">UIBlockChange.blocks
<a class="headerlink" href="#UIBlockChange.blocks" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> The list of blocks down the chain e.g some.nested.field   

<endpoint module="luxe: ui/block" class="UIBlockChange" signature="instances"></endpoint>
<signature id="UIBlockChange.instances">UIBlockChange.instances
<a class="headerlink" href="#UIBlockChange.instances" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> The list of instances for each block down the chain e.g some.nested.field   

<endpoint module="luxe: ui/block" class="UIBlockChange" signature="field"></endpoint>
<signature id="UIBlockChange.field">UIBlockChange.field
<a class="headerlink" href="#UIBlockChange.field" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> The list of nested fields for each block, e.g some.nested.field -> ["some", "nested", "field"]   

<endpoint module="luxe: ui/block" class="UIBlockChange" signature="array_indices"></endpoint>
<signature id="UIBlockChange.array_indices">UIBlockChange.array_indices
<a class="headerlink" href="#UIBlockChange.array_indices" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> The array index for each nested block. e.g some.nested[2].block[3] is [0, 2, 3]   

<endpoint module="luxe: ui/block" class="UIBlockChange" signature="field_index(idx : Num)"></endpoint>
<signature id="UIBlockChange.field_index">UIBlockChange.field_index(**idx**: `Num`)
<a class="headerlink" href="#UIBlockChange.field_index" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> The field index for the field in the fields list. 
>   e.g ["some", "nested", "field"] -> field_index[1] returns the field index of nested in the second block down   

<endpoint module="luxe: ui/block" class="UIBlockChange" signature="default"></endpoint>
<signature id="UIBlockChange.default">UIBlockChange.default
<a class="headerlink" href="#UIBlockChange.default" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Any`
> The default value in the leaf block for this field   

<endpoint module="luxe: ui/block" class="UIBlockChange" signature="get_field_value()"></endpoint>
<signature id="UIBlockChange.get_field_value">UIBlockChange.get_field_value()
<a class="headerlink" href="#UIBlockChange.get_field_value" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Any`
> The current value in the leaf block for this field (e.g for an array, returns the contents of the array)   

<endpoint module="luxe: ui/block" class="UIBlockChange" signature="get_leaf_value()"></endpoint>
<signature id="UIBlockChange.get_leaf_value">UIBlockChange.get_leaf_value()
<a class="headerlink" href="#UIBlockChange.get_leaf_value" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Any`
> The current value in the leaf for this block/field/array?   

<endpoint module="luxe: ui/block" class="UIBlockChange" signature="leaf_block"></endpoint>
<signature id="UIBlockChange.leaf_block">UIBlockChange.leaf_block
<a class="headerlink" href="#UIBlockChange.leaf_block" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Block`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockChange" signature="leaf_instance"></endpoint>
<signature id="UIBlockChange.leaf_instance">UIBlockChange.leaf_instance
<a class="headerlink" href="#UIBlockChange.leaf_instance" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js BlockInstance`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockChange" signature="leaf_field_index"></endpoint>
<signature id="UIBlockChange.leaf_field_index">UIBlockChange.leaf_field_index
<a class="headerlink" href="#UIBlockChange.leaf_field_index" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockChange" signature="leaf_array_index"></endpoint>
<signature id="UIBlockChange.leaf_array_index">UIBlockChange.leaf_array_index
<a class="headerlink" href="#UIBlockChange.leaf_array_index" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockChange" signature="get_change_value()"></endpoint>
<signature id="UIBlockChange.get_change_value">UIBlockChange.get_change_value()
<a class="headerlink" href="#UIBlockChange.get_change_value" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Any`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockChange" signature="field_is_array()"></endpoint>
<signature id="UIBlockChange.field_is_array">UIBlockChange.field_is_array()
<a class="headerlink" href="#UIBlockChange.field_is_array" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockChange" signature="field_is_object()"></endpoint>
<signature id="UIBlockChange.field_is_object">UIBlockChange.field_is_object()
<a class="headerlink" href="#UIBlockChange.field_is_object" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockChange" signature="value"></endpoint>
<signature id="UIBlockChange.value">UIBlockChange.value
<a class="headerlink" href="#UIBlockChange.value" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Any`
> The intended change value based on type   

<endpoint module="luxe: ui/block" class="UIBlockChange" signature="edit_value"></endpoint>
<signature id="UIBlockChange.edit_value">UIBlockChange.edit_value
<a class="headerlink" href="#UIBlockChange.edit_value" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Any`
> The value from the ui at the time of the change   

### UIBlockChangeType
`:::js import "luxe: ui/block" for UIBlockChangeType`
> no docs found

- [NORMAL](#UIBlockChangeType.NORMAL)
- [RESET](#UIBlockChangeType.RESET)
- [ARRAY_ADD](#UIBlockChangeType.ARRAY_ADD)
- [ARRAY_REMOVE](#UIBlockChangeType.ARRAY_REMOVE)
- [ARRAY_CLEAR](#UIBlockChangeType.ARRAY_CLEAR)
- [ARRAY_RESET](#UIBlockChangeType.ARRAY_RESET)
- [ARRAY_ELEMENT_RESET](#UIBlockChangeType.ARRAY_ELEMENT_RESET)
- [ARRAY_REORDER](#UIBlockChangeType.ARRAY_REORDER)
- [BLOCK](#UIBlockChangeType.BLOCK)

<hr/>
<endpoint module="luxe: ui/block" class="UIBlockChangeType" signature="NORMAL"></endpoint>
<signature id="UIBlockChangeType.NORMAL">UIBlockChangeType.NORMAL
<a class="headerlink" href="#UIBlockChangeType.NORMAL" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockChangeType" signature="RESET"></endpoint>
<signature id="UIBlockChangeType.RESET">UIBlockChangeType.RESET
<a class="headerlink" href="#UIBlockChangeType.RESET" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockChangeType" signature="ARRAY_ADD"></endpoint>
<signature id="UIBlockChangeType.ARRAY_ADD">UIBlockChangeType.ARRAY_ADD
<a class="headerlink" href="#UIBlockChangeType.ARRAY_ADD" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockChangeType" signature="ARRAY_REMOVE"></endpoint>
<signature id="UIBlockChangeType.ARRAY_REMOVE">UIBlockChangeType.ARRAY_REMOVE
<a class="headerlink" href="#UIBlockChangeType.ARRAY_REMOVE" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockChangeType" signature="ARRAY_CLEAR"></endpoint>
<signature id="UIBlockChangeType.ARRAY_CLEAR">UIBlockChangeType.ARRAY_CLEAR
<a class="headerlink" href="#UIBlockChangeType.ARRAY_CLEAR" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockChangeType" signature="ARRAY_RESET"></endpoint>
<signature id="UIBlockChangeType.ARRAY_RESET">UIBlockChangeType.ARRAY_RESET
<a class="headerlink" href="#UIBlockChangeType.ARRAY_RESET" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockChangeType" signature="ARRAY_ELEMENT_RESET"></endpoint>
<signature id="UIBlockChangeType.ARRAY_ELEMENT_RESET">UIBlockChangeType.ARRAY_ELEMENT_RESET
<a class="headerlink" href="#UIBlockChangeType.ARRAY_ELEMENT_RESET" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockChangeType" signature="ARRAY_REORDER"></endpoint>
<signature id="UIBlockChangeType.ARRAY_REORDER">UIBlockChangeType.ARRAY_REORDER
<a class="headerlink" href="#UIBlockChangeType.ARRAY_REORDER" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockChangeType" signature="BLOCK"></endpoint>
<signature id="UIBlockChangeType.BLOCK">UIBlockChangeType.BLOCK
<a class="headerlink" href="#UIBlockChangeType.BLOCK" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### UIBlockEventType
`:::js import "luxe: ui/block" for UIBlockEventType`
> no docs found

- [asset](#UIBlockEventType.asset)
- [link](#UIBlockEventType.link)

<hr/>
<endpoint module="luxe: ui/block" class="UIBlockEventType" signature="asset"></endpoint>
<signature id="UIBlockEventType.asset">UIBlockEventType.asset
<a class="headerlink" href="#UIBlockEventType.asset" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockEventType" signature="link"></endpoint>
<signature id="UIBlockEventType.link">UIBlockEventType.link
<a class="headerlink" href="#UIBlockEventType.link" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### UIBlockLinkEvent
`:::js import "luxe: ui/block" for UIBlockLinkEvent`
> no docs found

- [original](#UIBlockLinkEvent.original)
- [tag](#UIBlockLinkEvent.tag)
- [from_drop](#UIBlockLinkEvent.from_drop)
- [drop_payload](#UIBlockLinkEvent.drop_payload)
- [new](#UIBlockLinkEvent.new+3)(**original_in**: `List`, **tag**: `ID32`, **fn**: `Fn`)
- [new](#UIBlockLinkEvent.new+4)(**original_in**: `List`, **tag**: `ID32`, **drop_payload**: `Handle`, **fn**: `Fn`)
- [done](#UIBlockLinkEvent.done)(**value**: `List`)

<hr/>
<endpoint module="luxe: ui/block" class="UIBlockLinkEvent" signature="original"></endpoint>
<signature id="UIBlockLinkEvent.original">UIBlockLinkEvent.original
<a class="headerlink" href="#UIBlockLinkEvent.original" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockLinkEvent" signature="tag"></endpoint>
<signature id="UIBlockLinkEvent.tag">UIBlockLinkEvent.tag
<a class="headerlink" href="#UIBlockLinkEvent.tag" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockLinkEvent" signature="from_drop"></endpoint>
<signature id="UIBlockLinkEvent.from_drop">UIBlockLinkEvent.from_drop
<a class="headerlink" href="#UIBlockLinkEvent.from_drop" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockLinkEvent" signature="drop_payload"></endpoint>
<signature id="UIBlockLinkEvent.drop_payload">UIBlockLinkEvent.drop_payload
<a class="headerlink" href="#UIBlockLinkEvent.drop_payload" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockLinkEvent" signature="new(original_in : List, tag : ID32, fn : Fn)"></endpoint>
<signature id="UIBlockLinkEvent.new+3">UIBlockLinkEvent.new(**original_in**: `List`, **tag**: `ID32`, **fn**: `Fn`)
<a class="headerlink" href="#UIBlockLinkEvent.new+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js UIBlockLinkEvent`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockLinkEvent" signature="new(original_in : List, tag : ID32, drop_payload : Handle, fn : Fn)"></endpoint>
<signature id="UIBlockLinkEvent.new+4">UIBlockLinkEvent.new(**original_in**: `List`, **tag**: `ID32`, **drop_payload**: `Handle`, **fn**: `Fn`)
<a class="headerlink" href="#UIBlockLinkEvent.new+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js UIBlockLinkEvent`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockLinkEvent" signature="done(value : List)"></endpoint>
<signature id="UIBlockLinkEvent.done">UIBlockLinkEvent.done(**value**: `List`)
<a class="headerlink" href="#UIBlockLinkEvent.done" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### UIBlockState
`:::js import "luxe: ui/block" for UIBlockState`
> no docs found

- [new](#UIBlockState.new+2)(**ui**: `Entity`, **control**: `Control`)
- [get_block_fields](#UIBlockState.get_block_fields)()
- [set_show_defaults](#UIBlockState.set_show_defaults)(**show_defaults**: `Any`)
- [clear_listeners](#UIBlockState.clear_listeners)()
- [handle_assets](#UIBlockState.handle_assets)
- [handle_assets](#UIBlockState.handle_assets=)=(v : Bool)
- [field_h](#UIBlockState.field_h)
- [label_w](#UIBlockState.label_w)
- [set_sizes](#UIBlockState.set_sizes+3)(**label_width**: `Num`, **label_size**: `Num`, **field_height**: `Num`)
- [set_instance](#UIBlockState.set_instance+2)(**block**: `Block`, **instance**: `BlockInstance`)
- [set_instances](#UIBlockState.set_instances+2)(**block**: `Block`, **instances**: `List`)
- [set_blocks_instances](#UIBlockState.set_blocks_instances+2)(**blocks**: `List`, **instances**: `List`)
- [do_refresh](#UIBlockState.do_refresh)()
- [refresh](#UIBlockState.refresh)()
- [make_vec](#UIBlockState.make_vec)(**view**: `ValueView`)
- [make_color](#UIBlockState.make_color)(**view**: `ValueView`)
- [make_num](#UIBlockState.make_num)(**view**: `ValueView`)
- [make_text](#UIBlockState.make_text)(**view**: `ValueView`)
- [get_asset_picks](#UIBlockState.get_asset_picks)(**types**: `Any`)
- [make_asset](#UIBlockState.make_asset)(**view**: `ValueView`)
- [make_link](#UIBlockState.make_link)(**view**: `ValueView`)
- [make_path](#UIBlockState.make_path+2)(**view**: `ValueView`, **tag**: `Num`)
- [make_empty_object](#UIBlockState.make_empty_object)(**name**: `String`)
- [make_empty_object](#UIBlockState.make_empty_object+2)(**name**: `String`, **display**: `String`)
- [make_multiple_message](#UIBlockState.make_multiple_message)()
- [make_message](#UIBlockState.make_message)(**display**: `String`)
- [make_bool](#UIBlockState.make_bool)(**default**: `Bool`)
- [make_options](#UIBlockState.make_options+2)(**options**: `List`, **default**: `String`)
- [make_object_field](#UIBlockState.make_object_field+2)(**name**: `String`, **view**: `ValueView`)
- [make_options_field](#UIBlockState.make_options_field)(**view**: `ValueView`)
- [make_field](#UIBlockState.make_field+3)(**name**: `String`, **type**: `BlockFieldType`, **view**: `ValueView`)
- [make_object](#UIBlockState.make_object)(**name**: `String`)
- [make_object](#UIBlockState.make_object+2)(**name**: `String`, **title_color**: `Color`)
- [make_object](#UIBlockState.make_object+3)(**name**: `String`, **details**: `String`, **title_color**: `Color`)
- [make_label](#UIBlockState.make_label+2)(**name**: `String`, **width**: `Num`)
- [p](#UIBlockState.p+2)(**depth**: `Any`, **value**: `Any`)
- [dump_info](#UIBlockState.dump_info+2)(**control**: `Control`, **d**: `Num`)
- [make_mod_pip](#UIBlockState.make_mod_pip)(**kind**: `BlockFieldModified`)
- [get_changes](#UIBlockState.get_changes+3)(**kind**: `UIBlockChange`, **value**: `ValueView`, **edit_value**: `Any`)
- [get_changes](#UIBlockState.get_changes+4)(**kind**: `UIBlockChange`, **value**: `ValueView`, **edit_value**: `Any`, **edit_value_fn**: `Fn`)
- [get_changes](#UIBlockState.get_changes+5)(**kind**: `UIBlockChange`, **value**: `ValueView`, **change_id**: `String`, **edit_value**: `Any`, **edit_value_fn**: `Fn`)
- [make_block](#UIBlockState.make_block+2)(**instance_view**: `InstanceView`, **into**: `Control`)
- [make_block](#UIBlockState.make_block+3)(**instance_view**: `InstanceView`, **into**: `Control`, **indent**: `Num`)
- [hide_tip](#UIBlockState.hide_tip)(**from**: `Control`)
- [show_tip](#UIBlockState.show_tip+2)(**tooltip**: `String`, **control**: `Control`)
- [make_group](#UIBlockState.make_group)(**name**: `Any`)

<hr/>
<endpoint module="luxe: ui/block" class="UIBlockState" signature="new(ui : Entity, control : Control)"></endpoint>
<signature id="UIBlockState.new+2">UIBlockState.new(**ui**: `Entity`, **control**: `Control`)
<a class="headerlink" href="#UIBlockState.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js UIBlockState`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="get_block_fields()"></endpoint>
<signature id="UIBlockState.get_block_fields">UIBlockState.get_block_fields()
<a class="headerlink" href="#UIBlockState.get_block_fields" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="set_show_defaults(show_defaults : Any)"></endpoint>
<signature id="UIBlockState.set_show_defaults">UIBlockState.set_show_defaults(**show_defaults**: `Any`)
<a class="headerlink" href="#UIBlockState.set_show_defaults" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="clear_listeners()"></endpoint>
<signature id="UIBlockState.clear_listeners">UIBlockState.clear_listeners()
<a class="headerlink" href="#UIBlockState.clear_listeners" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="handle_assets"></endpoint>
<signature id="UIBlockState.handle_assets">UIBlockState.handle_assets
<a class="headerlink" href="#UIBlockState.handle_assets" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="handle_assets=(v : Bool)"></endpoint>
<signature id="UIBlockState.handle_assets=">UIBlockState.handle_assets=(v : Bool)
<a class="headerlink" href="#UIBlockState.handle_assets=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="field_h"></endpoint>
<signature id="UIBlockState.field_h">UIBlockState.field_h
<a class="headerlink" href="#UIBlockState.field_h" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="label_w"></endpoint>
<signature id="UIBlockState.label_w">UIBlockState.label_w
<a class="headerlink" href="#UIBlockState.label_w" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="set_sizes(label_width : Num, label_size : Num, field_height : Num)"></endpoint>
<signature id="UIBlockState.set_sizes+3">UIBlockState.set_sizes(**label_width**: `Num`, **label_size**: `Num`, **field_height**: `Num`)
<a class="headerlink" href="#UIBlockState.set_sizes+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="set_instance(block : Block, instance : BlockInstance)"></endpoint>
<signature id="UIBlockState.set_instance+2">UIBlockState.set_instance(**block**: `Block`, **instance**: `BlockInstance`)
<a class="headerlink" href="#UIBlockState.set_instance+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="set_instances(block : Block, instances : List)"></endpoint>
<signature id="UIBlockState.set_instances+2">UIBlockState.set_instances(**block**: `Block`, **instances**: `List`)
<a class="headerlink" href="#UIBlockState.set_instances+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="set_blocks_instances(blocks : List, instances : List)"></endpoint>
<signature id="UIBlockState.set_blocks_instances+2">UIBlockState.set_blocks_instances(**blocks**: `List`, **instances**: `List`)
<a class="headerlink" href="#UIBlockState.set_blocks_instances+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="do_refresh()"></endpoint>
<signature id="UIBlockState.do_refresh">UIBlockState.do_refresh()
<a class="headerlink" href="#UIBlockState.do_refresh" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="refresh()"></endpoint>
<signature id="UIBlockState.refresh">UIBlockState.refresh()
<a class="headerlink" href="#UIBlockState.refresh" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_vec(view : ValueView)"></endpoint>
<signature id="UIBlockState.make_vec">UIBlockState.make_vec(**view**: `ValueView`)
<a class="headerlink" href="#UIBlockState.make_vec" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Field`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_color(view : ValueView)"></endpoint>
<signature id="UIBlockState.make_color">UIBlockState.make_color(**view**: `ValueView`)
<a class="headerlink" href="#UIBlockState.make_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Field`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_num(view : ValueView)"></endpoint>
<signature id="UIBlockState.make_num">UIBlockState.make_num(**view**: `ValueView`)
<a class="headerlink" href="#UIBlockState.make_num" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Field`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_text(view : ValueView)"></endpoint>
<signature id="UIBlockState.make_text">UIBlockState.make_text(**view**: `ValueView`)
<a class="headerlink" href="#UIBlockState.make_text" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Field`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="get_asset_picks(types : Any)"></endpoint>
<signature id="UIBlockState.get_asset_picks">UIBlockState.get_asset_picks(**types**: `Any`)
<a class="headerlink" href="#UIBlockState.get_asset_picks" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_asset(view : ValueView)"></endpoint>
<signature id="UIBlockState.make_asset">UIBlockState.make_asset(**view**: `ValueView`)
<a class="headerlink" href="#UIBlockState.make_asset" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Field`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_link(view : ValueView)"></endpoint>
<signature id="UIBlockState.make_link">UIBlockState.make_link(**view**: `ValueView`)
<a class="headerlink" href="#UIBlockState.make_link" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Field`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_path(view : ValueView, tag : Num)"></endpoint>
<signature id="UIBlockState.make_path+2">UIBlockState.make_path(**view**: `ValueView`, **tag**: `Num`)
<a class="headerlink" href="#UIBlockState.make_path+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Field`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_empty_object(name : String)"></endpoint>
<signature id="UIBlockState.make_empty_object">UIBlockState.make_empty_object(**name**: `String`)
<a class="headerlink" href="#UIBlockState.make_empty_object" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Field`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_empty_object(name : String, display : String)"></endpoint>
<signature id="UIBlockState.make_empty_object+2">UIBlockState.make_empty_object(**name**: `String`, **display**: `String`)
<a class="headerlink" href="#UIBlockState.make_empty_object+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Field`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_multiple_message()"></endpoint>
<signature id="UIBlockState.make_multiple_message">UIBlockState.make_multiple_message()
<a class="headerlink" href="#UIBlockState.make_multiple_message" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_message(display : String)"></endpoint>
<signature id="UIBlockState.make_message">UIBlockState.make_message(**display**: `String`)
<a class="headerlink" href="#UIBlockState.make_message" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_bool(default : Bool)"></endpoint>
<signature id="UIBlockState.make_bool">UIBlockState.make_bool(**default**: `Bool`)
<a class="headerlink" href="#UIBlockState.make_bool" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Field`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_options(options : List, default : String)"></endpoint>
<signature id="UIBlockState.make_options+2">UIBlockState.make_options(**options**: `List`, **default**: `String`)
<a class="headerlink" href="#UIBlockState.make_options+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Field`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_object_field(name : String, view : ValueView)"></endpoint>
<signature id="UIBlockState.make_object_field+2">UIBlockState.make_object_field(**name**: `String`, **view**: `ValueView`)
<a class="headerlink" href="#UIBlockState.make_object_field+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_options_field(view : ValueView)"></endpoint>
<signature id="UIBlockState.make_options_field">UIBlockState.make_options_field(**view**: `ValueView`)
<a class="headerlink" href="#UIBlockState.make_options_field" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Field`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_field(name : String, type : BlockFieldType, view : ValueView)"></endpoint>
<signature id="UIBlockState.make_field+3">UIBlockState.make_field(**name**: `String`, **type**: `BlockFieldType`, **view**: `ValueView`)
<a class="headerlink" href="#UIBlockState.make_field+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Field`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_object(name : String)"></endpoint>
<signature id="UIBlockState.make_object">UIBlockState.make_object(**name**: `String`)
<a class="headerlink" href="#UIBlockState.make_object" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_object(name : String, title_color : Color)"></endpoint>
<signature id="UIBlockState.make_object+2">UIBlockState.make_object(**name**: `String`, **title_color**: `Color`)
<a class="headerlink" href="#UIBlockState.make_object+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_object(name : String, details : String, title_color : Color)"></endpoint>
<signature id="UIBlockState.make_object+3">UIBlockState.make_object(**name**: `String`, **details**: `String`, **title_color**: `Color`)
<a class="headerlink" href="#UIBlockState.make_object+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_label(name : String, width : Num)"></endpoint>
<signature id="UIBlockState.make_label+2">UIBlockState.make_label(**name**: `String`, **width**: `Num`)
<a class="headerlink" href="#UIBlockState.make_label+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="p(depth : Any, value : Any)"></endpoint>
<signature id="UIBlockState.p+2">UIBlockState.p(**depth**: `Any`, **value**: `Any`)
<a class="headerlink" href="#UIBlockState.p+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="dump_info(control : Control, d : Num)"></endpoint>
<signature id="UIBlockState.dump_info+2">UIBlockState.dump_info(**control**: `Control`, **d**: `Num`)
<a class="headerlink" href="#UIBlockState.dump_info+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_mod_pip(kind : BlockFieldModified)"></endpoint>
<signature id="UIBlockState.make_mod_pip">UIBlockState.make_mod_pip(**kind**: `BlockFieldModified`)
<a class="headerlink" href="#UIBlockState.make_mod_pip" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js ModifiedPip`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="get_changes(kind : UIBlockChange, value : ValueView, edit_value : Any)"></endpoint>
<signature id="UIBlockState.get_changes+3">UIBlockState.get_changes(**kind**: `UIBlockChange`, **value**: `ValueView`, **edit_value**: `Any`)
<a class="headerlink" href="#UIBlockState.get_changes+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="get_changes(kind : UIBlockChange, value : ValueView, edit_value : Any, edit_value_fn : Fn)"></endpoint>
<signature id="UIBlockState.get_changes+4">UIBlockState.get_changes(**kind**: `UIBlockChange`, **value**: `ValueView`, **edit_value**: `Any`, **edit_value_fn**: `Fn`)
<a class="headerlink" href="#UIBlockState.get_changes+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="get_changes(kind : UIBlockChange, value : ValueView, change_id : String, edit_value : Any, edit_value_fn : Fn)"></endpoint>
<signature id="UIBlockState.get_changes+5">UIBlockState.get_changes(**kind**: `UIBlockChange`, **value**: `ValueView`, **change_id**: `String`, **edit_value**: `Any`, **edit_value_fn**: `Fn`)
<a class="headerlink" href="#UIBlockState.get_changes+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_block(instance_view : InstanceView, into : Control)"></endpoint>
<signature id="UIBlockState.make_block+2">UIBlockState.make_block(**instance_view**: `InstanceView`, **into**: `Control`)
<a class="headerlink" href="#UIBlockState.make_block+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_block(instance_view : InstanceView, into : Control, indent : Num)"></endpoint>
<signature id="UIBlockState.make_block+3">UIBlockState.make_block(**instance_view**: `InstanceView`, **into**: `Control`, **indent**: `Num`)
<a class="headerlink" href="#UIBlockState.make_block+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="hide_tip(from : Control)"></endpoint>
<signature id="UIBlockState.hide_tip">UIBlockState.hide_tip(**from**: `Control`)
<a class="headerlink" href="#UIBlockState.hide_tip" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="show_tip(tooltip : String, control : Control)"></endpoint>
<signature id="UIBlockState.show_tip+2">UIBlockState.show_tip(**tooltip**: `String`, **control**: `Control`)
<a class="headerlink" href="#UIBlockState.show_tip+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: ui/block" class="UIBlockState" signature="make_group(name : Any)"></endpoint>
<signature id="UIBlockState.make_group">UIBlockState.make_group(**name**: `Any`)
<a class="headerlink" href="#UIBlockState.make_group" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

