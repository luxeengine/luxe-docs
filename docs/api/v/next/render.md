#![](../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2024.12.4`)  


---

## `luxe: render` module

- [Atlas](#atlas)   
- [BlendFactor](#blendfactor)   
- [BlendOperation](#blendoperation)   
- [Clip](#clip)   
- [ColorWriteMask](#colorwritemask)   
- [CompareFunction](#comparefunction)   
- [ComputeLayerDesc](#computelayerdesc)   
- [ComputeLayerInput](#computelayerinput)   
- [CullMode](#cullmode)   
- [Geometry](#geometry)   
- [Image](#image)   
- [ImageDesc](#imagedesc)   
- [ImageType](#imagetype)   
- [ImageUsage](#imageusage)   
- [IndexType](#indextype)   
- [InputBuffer](#inputbuffer)   
- [LayerCompute](#layercompute)   
- [LayerPass](#layerpass)   
- [LoadAction](#loadaction)   
- [Material](#material)   
- [MaterialDesc](#materialdesc)   
- [MaterialFunction](#materialfunction)   
- [MaterialInput](#materialinput)   
- [MaterialInputBlock](#materialinputblock)   
- [MaterialInputImage](#materialinputimage)   
- [MaterialInputType](#materialinputtype)   
- [MaterialReplace](#materialreplace)   
- [PassLayerDesc](#passlayerdesc)   
- [PixelFormat](#pixelformat)   
- [Pose](#pose)   
- [PoseGraph](#posegraph)   
- [PoseNode](#posenode)   
- [Primitive](#primitive)   
- [Render](#render)   
- [RenderDest](#renderdest)   
- [RenderDestColor](#renderdestcolor)   
- [RenderDestDepth](#renderdestdepth)   
- [RenderDestStencil](#renderdeststencil)   
- [RenderLayerDesc](#renderlayerdesc)   
- [RenderPathContext](#renderpathcontext)   
- [RenderViewDesc](#renderviewdesc)   
- [SamplerAddressMode](#sampleraddressmode)   
- [SamplerMinMagFilter](#samplerminmagfilter)   
- [SamplerMipFilter](#samplermipfilter)   
- [SamplerState](#samplerstate)   
- [SortType](#sorttype)   
- [StencilOperation](#stenciloperation)   
- [StoreAction](#storeaction)   
- [TextAlign](#textalign)   
- [TextAttrType](#textattrtype)   
- [TextWrapMode](#textwrapmode)   
- [VertexAttr](#vertexattr)   
- [VertexAttrFormat](#vertexattrformat)   
- [VertexFormat](#vertexformat)   
- [VertexInputRate](#vertexinputrate)   
- [VertexLayout](#vertexlayout)   
- [Winding](#winding)   

---

### Atlas
`:::js import "luxe: render" for Atlas`
> no docs found

- [create](#Atlas.create+2)(**size**: `Any`, **material**: `Any`)
- [destroy](#Atlas.destroy)(**atlas**: `Any`)
- [valid](#Atlas.valid)(**atlas**: `Any`)
- [get_size](#Atlas.get_size)(**atlas**: `Any`)
- [get_material](#Atlas.get_material)(**atlas**: `Any`)
- [rect_add](#Atlas.rect_add+5)(**atlas**: `Any`, **atlas_image_id**: `Any`, **frame**: `Any`, **rect**: `Any`, **rotated**: `Any`)
- [rect_remove](#Atlas.rect_remove+2)(**atlas**: `Any`, **atlas_image_id**: `Any`)
- [rect_get_frame](#Atlas.rect_get_frame+2)(**atlas**: `Any`, **atlas_image**: `Any`)
- [rect_get_rect](#Atlas.rect_get_rect+2)(**atlas**: `Any`, **atlas_image**: `Any`)
- [rect_get_rotated](#Atlas.rect_get_rotated+2)(**atlas**: `Any`, **atlas_image**: `Any`)
- [rect_exists](#Atlas.rect_exists+2)(**atlas**: `Any`, **atlas_image**: `Any`)

<hr/>
<endpoint module="luxe: render" class="Atlas" signature="create(size : Any, material : Any)"></endpoint>
<signature id="Atlas.create+2">Atlas.create(**size**: `Any`, **material**: `Any`)
<a class="headerlink" href="#Atlas.create+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Atlas" signature="destroy(atlas : Any)"></endpoint>
<signature id="Atlas.destroy">Atlas.destroy(**atlas**: `Any`)
<a class="headerlink" href="#Atlas.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Atlas" signature="valid(atlas : Any)"></endpoint>
<signature id="Atlas.valid">Atlas.valid(**atlas**: `Any`)
<a class="headerlink" href="#Atlas.valid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Atlas" signature="get_size(atlas : Any)"></endpoint>
<signature id="Atlas.get_size">Atlas.get_size(**atlas**: `Any`)
<a class="headerlink" href="#Atlas.get_size" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Atlas" signature="get_material(atlas : Any)"></endpoint>
<signature id="Atlas.get_material">Atlas.get_material(**atlas**: `Any`)
<a class="headerlink" href="#Atlas.get_material" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Atlas" signature="rect_add(atlas : Any, atlas_image_id : Any, frame : Any, rect : Any, rotated : Any)"></endpoint>
<signature id="Atlas.rect_add+5">Atlas.rect_add(**atlas**: `Any`, **atlas_image_id**: `Any`, **frame**: `Any`, **rect**: `Any`, **rotated**: `Any`)
<a class="headerlink" href="#Atlas.rect_add+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Atlas" signature="rect_remove(atlas : Any, atlas_image_id : Any)"></endpoint>
<signature id="Atlas.rect_remove+2">Atlas.rect_remove(**atlas**: `Any`, **atlas_image_id**: `Any`)
<a class="headerlink" href="#Atlas.rect_remove+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Atlas" signature="rect_get_frame(atlas : Any, atlas_image : Any)"></endpoint>
<signature id="Atlas.rect_get_frame+2">Atlas.rect_get_frame(**atlas**: `Any`, **atlas_image**: `Any`)
<a class="headerlink" href="#Atlas.rect_get_frame+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Atlas" signature="rect_get_rect(atlas : Any, atlas_image : Any)"></endpoint>
<signature id="Atlas.rect_get_rect+2">Atlas.rect_get_rect(**atlas**: `Any`, **atlas_image**: `Any`)
<a class="headerlink" href="#Atlas.rect_get_rect+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Atlas" signature="rect_get_rotated(atlas : Any, atlas_image : Any)"></endpoint>
<signature id="Atlas.rect_get_rotated+2">Atlas.rect_get_rotated(**atlas**: `Any`, **atlas_image**: `Any`)
<a class="headerlink" href="#Atlas.rect_get_rotated+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Atlas" signature="rect_exists(atlas : Any, atlas_image : Any)"></endpoint>
<signature id="Atlas.rect_exists+2">Atlas.rect_exists(**atlas**: `Any`, **atlas_image**: `Any`)
<a class="headerlink" href="#Atlas.rect_exists+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### BlendFactor
`:::js import "luxe: render" for BlendFactor`
> no docs found

- [zero](#BlendFactor.zero)
- [one](#BlendFactor.one)
- [source_color](#BlendFactor.source_color)
- [one_minus_source_color](#BlendFactor.one_minus_source_color)
- [source_alpha](#BlendFactor.source_alpha)
- [one_minus_source_alpha](#BlendFactor.one_minus_source_alpha)
- [destination_color](#BlendFactor.destination_color)
- [one_minus_destination_color](#BlendFactor.one_minus_destination_color)
- [destination_alpha](#BlendFactor.destination_alpha)
- [one_minus_destination_alpha](#BlendFactor.one_minus_destination_alpha)
- [source_alpha_saturated](#BlendFactor.source_alpha_saturated)
- [blend_color](#BlendFactor.blend_color)
- [one_minus_blend_color](#BlendFactor.one_minus_blend_color)
- [blend_alpha](#BlendFactor.blend_alpha)
- [one_minus_blend_alpha](#BlendFactor.one_minus_blend_alpha)
- [invalid](#BlendFactor.invalid)
- [from_string](#BlendFactor.from_string)(**value**: `Any`)

<hr/>
<endpoint module="luxe: render" class="BlendFactor" signature="zero"></endpoint>
<signature id="BlendFactor.zero">BlendFactor.zero
<a class="headerlink" href="#BlendFactor.zero" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="BlendFactor" signature="one"></endpoint>
<signature id="BlendFactor.one">BlendFactor.one
<a class="headerlink" href="#BlendFactor.one" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="BlendFactor" signature="source_color"></endpoint>
<signature id="BlendFactor.source_color">BlendFactor.source_color
<a class="headerlink" href="#BlendFactor.source_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="BlendFactor" signature="one_minus_source_color"></endpoint>
<signature id="BlendFactor.one_minus_source_color">BlendFactor.one_minus_source_color
<a class="headerlink" href="#BlendFactor.one_minus_source_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="BlendFactor" signature="source_alpha"></endpoint>
<signature id="BlendFactor.source_alpha">BlendFactor.source_alpha
<a class="headerlink" href="#BlendFactor.source_alpha" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="BlendFactor" signature="one_minus_source_alpha"></endpoint>
<signature id="BlendFactor.one_minus_source_alpha">BlendFactor.one_minus_source_alpha
<a class="headerlink" href="#BlendFactor.one_minus_source_alpha" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="BlendFactor" signature="destination_color"></endpoint>
<signature id="BlendFactor.destination_color">BlendFactor.destination_color
<a class="headerlink" href="#BlendFactor.destination_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="BlendFactor" signature="one_minus_destination_color"></endpoint>
<signature id="BlendFactor.one_minus_destination_color">BlendFactor.one_minus_destination_color
<a class="headerlink" href="#BlendFactor.one_minus_destination_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="BlendFactor" signature="destination_alpha"></endpoint>
<signature id="BlendFactor.destination_alpha">BlendFactor.destination_alpha
<a class="headerlink" href="#BlendFactor.destination_alpha" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="BlendFactor" signature="one_minus_destination_alpha"></endpoint>
<signature id="BlendFactor.one_minus_destination_alpha">BlendFactor.one_minus_destination_alpha
<a class="headerlink" href="#BlendFactor.one_minus_destination_alpha" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="BlendFactor" signature="source_alpha_saturated"></endpoint>
<signature id="BlendFactor.source_alpha_saturated">BlendFactor.source_alpha_saturated
<a class="headerlink" href="#BlendFactor.source_alpha_saturated" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="BlendFactor" signature="blend_color"></endpoint>
<signature id="BlendFactor.blend_color">BlendFactor.blend_color
<a class="headerlink" href="#BlendFactor.blend_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="BlendFactor" signature="one_minus_blend_color"></endpoint>
<signature id="BlendFactor.one_minus_blend_color">BlendFactor.one_minus_blend_color
<a class="headerlink" href="#BlendFactor.one_minus_blend_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="BlendFactor" signature="blend_alpha"></endpoint>
<signature id="BlendFactor.blend_alpha">BlendFactor.blend_alpha
<a class="headerlink" href="#BlendFactor.blend_alpha" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="BlendFactor" signature="one_minus_blend_alpha"></endpoint>
<signature id="BlendFactor.one_minus_blend_alpha">BlendFactor.one_minus_blend_alpha
<a class="headerlink" href="#BlendFactor.one_minus_blend_alpha" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="BlendFactor" signature="invalid"></endpoint>
<signature id="BlendFactor.invalid">BlendFactor.invalid
<a class="headerlink" href="#BlendFactor.invalid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="BlendFactor" signature="from_string(value : Any)"></endpoint>
<signature id="BlendFactor.from_string">BlendFactor.from_string(**value**: `Any`)
<a class="headerlink" href="#BlendFactor.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### BlendOperation
`:::js import "luxe: render" for BlendOperation`
> no docs found

- [add](#BlendOperation.add)
- [subtract](#BlendOperation.subtract)
- [reverse_subtract](#BlendOperation.reverse_subtract)
- [min](#BlendOperation.min)
- [max](#BlendOperation.max)
- [from_string](#BlendOperation.from_string)(**value**: `Any`)

<hr/>
<endpoint module="luxe: render" class="BlendOperation" signature="add"></endpoint>
<signature id="BlendOperation.add">BlendOperation.add
<a class="headerlink" href="#BlendOperation.add" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="BlendOperation" signature="subtract"></endpoint>
<signature id="BlendOperation.subtract">BlendOperation.subtract
<a class="headerlink" href="#BlendOperation.subtract" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="BlendOperation" signature="reverse_subtract"></endpoint>
<signature id="BlendOperation.reverse_subtract">BlendOperation.reverse_subtract
<a class="headerlink" href="#BlendOperation.reverse_subtract" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="BlendOperation" signature="min"></endpoint>
<signature id="BlendOperation.min">BlendOperation.min
<a class="headerlink" href="#BlendOperation.min" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="BlendOperation" signature="max"></endpoint>
<signature id="BlendOperation.max">BlendOperation.max
<a class="headerlink" href="#BlendOperation.max" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="BlendOperation" signature="from_string(value : Any)"></endpoint>
<signature id="BlendOperation.from_string">BlendOperation.from_string(**value**: `Any`)
<a class="headerlink" href="#BlendOperation.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Clip
`:::js import "luxe: render" for Clip`
> no docs found

- [get_duration](#Clip.get_duration)(**clip**: `Clip`)

<hr/>
<endpoint module="luxe: render" class="Clip" signature="get_duration(clip : Clip)"></endpoint>
<signature id="Clip.get_duration">Clip.get_duration(**clip**: `Clip`)
<a class="headerlink" href="#Clip.get_duration" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

### ColorWriteMask
`:::js import "luxe: render" for ColorWriteMask`
> no docs found

- [none](#ColorWriteMask.none)
- [red](#ColorWriteMask.red)
- [green](#ColorWriteMask.green)
- [blue](#ColorWriteMask.blue)
- [alpha](#ColorWriteMask.alpha)
- [all](#ColorWriteMask.all)
- [invalid](#ColorWriteMask.invalid)
- [from_map](#ColorWriteMask.from_map)(**value**: `Any`)
- [from_string](#ColorWriteMask.from_string)(**value**: `Any`)

<hr/>
<endpoint module="luxe: render" class="ColorWriteMask" signature="none"></endpoint>
<signature id="ColorWriteMask.none">ColorWriteMask.none
<a class="headerlink" href="#ColorWriteMask.none" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ColorWriteMask" signature="red"></endpoint>
<signature id="ColorWriteMask.red">ColorWriteMask.red
<a class="headerlink" href="#ColorWriteMask.red" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ColorWriteMask" signature="green"></endpoint>
<signature id="ColorWriteMask.green">ColorWriteMask.green
<a class="headerlink" href="#ColorWriteMask.green" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ColorWriteMask" signature="blue"></endpoint>
<signature id="ColorWriteMask.blue">ColorWriteMask.blue
<a class="headerlink" href="#ColorWriteMask.blue" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ColorWriteMask" signature="alpha"></endpoint>
<signature id="ColorWriteMask.alpha">ColorWriteMask.alpha
<a class="headerlink" href="#ColorWriteMask.alpha" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ColorWriteMask" signature="all"></endpoint>
<signature id="ColorWriteMask.all">ColorWriteMask.all
<a class="headerlink" href="#ColorWriteMask.all" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ColorWriteMask" signature="invalid"></endpoint>
<signature id="ColorWriteMask.invalid">ColorWriteMask.invalid
<a class="headerlink" href="#ColorWriteMask.invalid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ColorWriteMask" signature="from_map(value : Any)"></endpoint>
<signature id="ColorWriteMask.from_map">ColorWriteMask.from_map(**value**: `Any`)
<a class="headerlink" href="#ColorWriteMask.from_map" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ColorWriteMask" signature="from_string(value : Any)"></endpoint>
<signature id="ColorWriteMask.from_string">ColorWriteMask.from_string(**value**: `Any`)
<a class="headerlink" href="#ColorWriteMask.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### CompareFunction
`:::js import "luxe: render" for CompareFunction`
> no docs found

- [never](#CompareFunction.never)
- [less](#CompareFunction.less)
- [equal](#CompareFunction.equal)
- [less_equal](#CompareFunction.less_equal)
- [greater](#CompareFunction.greater)
- [not_equal](#CompareFunction.not_equal)
- [greater_equal](#CompareFunction.greater_equal)
- [always](#CompareFunction.always)
- [from_string](#CompareFunction.from_string)(**value**: `Any`)

<hr/>
<endpoint module="luxe: render" class="CompareFunction" signature="never"></endpoint>
<signature id="CompareFunction.never">CompareFunction.never
<a class="headerlink" href="#CompareFunction.never" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="CompareFunction" signature="less"></endpoint>
<signature id="CompareFunction.less">CompareFunction.less
<a class="headerlink" href="#CompareFunction.less" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="CompareFunction" signature="equal"></endpoint>
<signature id="CompareFunction.equal">CompareFunction.equal
<a class="headerlink" href="#CompareFunction.equal" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="CompareFunction" signature="less_equal"></endpoint>
<signature id="CompareFunction.less_equal">CompareFunction.less_equal
<a class="headerlink" href="#CompareFunction.less_equal" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="CompareFunction" signature="greater"></endpoint>
<signature id="CompareFunction.greater">CompareFunction.greater
<a class="headerlink" href="#CompareFunction.greater" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="CompareFunction" signature="not_equal"></endpoint>
<signature id="CompareFunction.not_equal">CompareFunction.not_equal
<a class="headerlink" href="#CompareFunction.not_equal" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="CompareFunction" signature="greater_equal"></endpoint>
<signature id="CompareFunction.greater_equal">CompareFunction.greater_equal
<a class="headerlink" href="#CompareFunction.greater_equal" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="CompareFunction" signature="always"></endpoint>
<signature id="CompareFunction.always">CompareFunction.always
<a class="headerlink" href="#CompareFunction.always" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="CompareFunction" signature="from_string(value : Any)"></endpoint>
<signature id="CompareFunction.from_string">CompareFunction.from_string(**value**: `Any`)
<a class="headerlink" href="#CompareFunction.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### ComputeLayerDesc
`:::js import "luxe: render" for ComputeLayerDesc`
> no docs found

- [new](#ComputeLayerDesc.new)()
- [display_id](#ComputeLayerDesc.display_id)
- [display_id](#ComputeLayerDesc.display_id=)=(v : String)
- [compute_id](#ComputeLayerDesc.compute_id)
- [compute_id](#ComputeLayerDesc.compute_id=)=(v : String)
- [dimensions](#ComputeLayerDesc.dimensions)
- [inputs](#ComputeLayerDesc.inputs)
- [inputs](#ComputeLayerDesc.inputs=)=(v : List)
- [x](#ComputeLayerDesc.x)
- [x](#ComputeLayerDesc.x=)=(v : Num)
- [y](#ComputeLayerDesc.y)
- [y](#ComputeLayerDesc.y=)=(v : Num)
- [z](#ComputeLayerDesc.z)
- [z](#ComputeLayerDesc.z=)=(v : Num)

<hr/>
<endpoint module="luxe: render" class="ComputeLayerDesc" signature="new()"></endpoint>
<signature id="ComputeLayerDesc.new">ComputeLayerDesc.new()
<a class="headerlink" href="#ComputeLayerDesc.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js ComputeLayerDesc`
> no docs found   

<endpoint module="luxe: render" class="ComputeLayerDesc" signature="display_id"></endpoint>
<signature id="ComputeLayerDesc.display_id">ComputeLayerDesc.display_id
<a class="headerlink" href="#ComputeLayerDesc.display_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: render" class="ComputeLayerDesc" signature="display_id=(v : String)"></endpoint>
<signature id="ComputeLayerDesc.display_id=">ComputeLayerDesc.display_id=(v : String)
<a class="headerlink" href="#ComputeLayerDesc.display_id=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ComputeLayerDesc" signature="compute_id"></endpoint>
<signature id="ComputeLayerDesc.compute_id">ComputeLayerDesc.compute_id
<a class="headerlink" href="#ComputeLayerDesc.compute_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: render" class="ComputeLayerDesc" signature="compute_id=(v : String)"></endpoint>
<signature id="ComputeLayerDesc.compute_id=">ComputeLayerDesc.compute_id=(v : String)
<a class="headerlink" href="#ComputeLayerDesc.compute_id=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ComputeLayerDesc" signature="dimensions"></endpoint>
<signature id="ComputeLayerDesc.dimensions">ComputeLayerDesc.dimensions
<a class="headerlink" href="#ComputeLayerDesc.dimensions" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Float3`
> no docs found   

<endpoint module="luxe: render" class="ComputeLayerDesc" signature="inputs"></endpoint>
<signature id="ComputeLayerDesc.inputs">ComputeLayerDesc.inputs
<a class="headerlink" href="#ComputeLayerDesc.inputs" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: render" class="ComputeLayerDesc" signature="inputs=(v : List)"></endpoint>
<signature id="ComputeLayerDesc.inputs=">ComputeLayerDesc.inputs=(v : List)
<a class="headerlink" href="#ComputeLayerDesc.inputs=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ComputeLayerDesc" signature="x"></endpoint>
<signature id="ComputeLayerDesc.x">ComputeLayerDesc.x
<a class="headerlink" href="#ComputeLayerDesc.x" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: render" class="ComputeLayerDesc" signature="x=(v : Num)"></endpoint>
<signature id="ComputeLayerDesc.x=">ComputeLayerDesc.x=(v : Num)
<a class="headerlink" href="#ComputeLayerDesc.x=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ComputeLayerDesc" signature="y"></endpoint>
<signature id="ComputeLayerDesc.y">ComputeLayerDesc.y
<a class="headerlink" href="#ComputeLayerDesc.y" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: render" class="ComputeLayerDesc" signature="y=(v : Num)"></endpoint>
<signature id="ComputeLayerDesc.y=">ComputeLayerDesc.y=(v : Num)
<a class="headerlink" href="#ComputeLayerDesc.y=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ComputeLayerDesc" signature="z"></endpoint>
<signature id="ComputeLayerDesc.z">ComputeLayerDesc.z
<a class="headerlink" href="#ComputeLayerDesc.z" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: render" class="ComputeLayerDesc" signature="z=(v : Num)"></endpoint>
<signature id="ComputeLayerDesc.z=">ComputeLayerDesc.z=(v : Num)
<a class="headerlink" href="#ComputeLayerDesc.z=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### ComputeLayerInput
`:::js import "luxe: render" for ComputeLayerInput`
> no docs found

- [library](#ComputeLayerInput.library)
- [type](#ComputeLayerInput.type)
- [input](#ComputeLayerInput.input)
- [buffer](#ComputeLayerInput.buffer)
- [new](#ComputeLayerInput.new+4)(**library**: `Any`, **type**: `String`, **input**: `String`, **buffer**: `InputBuffer`)

<hr/>
<endpoint module="luxe: render" class="ComputeLayerInput" signature="library"></endpoint>
<signature id="ComputeLayerInput.library">ComputeLayerInput.library
<a class="headerlink" href="#ComputeLayerInput.library" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: render" class="ComputeLayerInput" signature="type"></endpoint>
<signature id="ComputeLayerInput.type">ComputeLayerInput.type
<a class="headerlink" href="#ComputeLayerInput.type" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: render" class="ComputeLayerInput" signature="input"></endpoint>
<signature id="ComputeLayerInput.input">ComputeLayerInput.input
<a class="headerlink" href="#ComputeLayerInput.input" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: render" class="ComputeLayerInput" signature="buffer"></endpoint>
<signature id="ComputeLayerInput.buffer">ComputeLayerInput.buffer
<a class="headerlink" href="#ComputeLayerInput.buffer" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js InputBuffer`
> no docs found   

<endpoint module="luxe: render" class="ComputeLayerInput" signature="new(library : Any, type : String, input : String, buffer : InputBuffer)"></endpoint>
<signature id="ComputeLayerInput.new+4">ComputeLayerInput.new(**library**: `Any`, **type**: `String`, **input**: `String`, **buffer**: `InputBuffer`)
<a class="headerlink" href="#ComputeLayerInput.new+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js ComputeLayerInput`
> no docs found   

### CullMode
`:::js import "luxe: render" for CullMode`
> no docs found

- [none](#CullMode.none)
- [front](#CullMode.front)
- [back](#CullMode.back)
- [from_string](#CullMode.from_string)(**value**: `Any`)

<hr/>
<endpoint module="luxe: render" class="CullMode" signature="none"></endpoint>
<signature id="CullMode.none">CullMode.none
<a class="headerlink" href="#CullMode.none" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="CullMode" signature="front"></endpoint>
<signature id="CullMode.front">CullMode.front
<a class="headerlink" href="#CullMode.front" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="CullMode" signature="back"></endpoint>
<signature id="CullMode.back">CullMode.back
<a class="headerlink" href="#CullMode.back" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="CullMode" signature="from_string(value : Any)"></endpoint>
<signature id="CullMode.from_string">CullMode.from_string(**value**: `Any`)
<a class="headerlink" href="#CullMode.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Geometry
`:::js import "luxe: render" for Geometry`
> no docs found

- [create](#Geometry.create+5)(**primitive**: `Any`, **material**: `Any`, **index_count**: `Any`, **index_type**: `Any`, **index_buffer**: `Any`)
- [create](#Geometry.create+3)(**primitive**: `Any`, **material**: `Any`, **vert_count**: `Any`)
- [destroy](#Geometry.destroy)(**geo**: `Any`)
- [valid](#Geometry.valid)(**geo**: `Any`)
- [set_world_matrix](#Geometry.set_world_matrix+2)(**geo**: `Any`, **world**: `Any`)
- [set_vertex_buffer](#Geometry.set_vertex_buffer+3)(**geo**: `Any`, **index**: `Any`, **vertex_buffer**: `Any`)
- [get_vertex_buffer](#Geometry.get_vertex_buffer+2)(**geo**: `Any`, **index**: `Any`)
- [get_index_buffer](#Geometry.get_index_buffer)(**geo**: `Any`)
- [set_instance_count](#Geometry.set_instance_count+2)(**geo**: `Any`, **count**: `Any`)
- [get_instance_count](#Geometry.get_instance_count)(**geo**: `Any`)
- [set_vert_count](#Geometry.set_vert_count+2)(**geo**: `Any`, **count**: `Any`)
- [set_material](#Geometry.set_material+2)(**geo**: `Any`, **material**: `Any`)
- [set_stencil_references](#Geometry.set_stencil_references+3)(**geo**: `Any`, **back**: `Any`, **front**: `Any`)
- [set_stencil_reference](#Geometry.set_stencil_reference+2)(**geo**: `Any`, **value**: `Any`)
- [set_aabb](#Geometry.set_aabb+7)(**geo**: `Any`, **center_x**: `Any`, **center_y**: `Any`, **center_z**: `Any`, **radius_x**: `Any`, **radius_y**: `Any`, **radius_z**: `Any`)
- [get_aabb](#Geometry.get_aabb)(**geo**: `Any`)
- [get_world_obb](#Geometry.get_world_obb)(**geo**: `Any`)
- [get_vert_count](#Geometry.get_vert_count)(**geo**: `Any`)
- [get_material](#Geometry.get_material)(**geo**: `Any`)
- [obb_intersect_ray](#Geometry.obb_intersect_ray+7)(**geo**: `Any`, **ray_x**: `Any`, **ray_y**: `Any`, **ray_z**: `Any`, **ray_dir_x**: `Any`, **ray_dir_y**: `Any`, **ray_dir_z**: `Any`)
- [layer_include_add](#Geometry.layer_include_add+2)(**geo**: `Any`, **layer_id**: `Any`)
- [layer_include_remove](#Geometry.layer_include_remove+2)(**geo**: `Any`, **layer_id**: `Any`)
- [layer_exclude_add](#Geometry.layer_exclude_add+2)(**geo**: `Any`, **layer_id**: `Any`)
- [layer_exclude_remove](#Geometry.layer_exclude_remove+2)(**geo**: `Any`, **layer_id**: `Any`)

<hr/>
<endpoint module="luxe: render" class="Geometry" signature="create(primitive : Any, material : Any, index_count : Any, index_type : Any, index_buffer : Any)"></endpoint>
<signature id="Geometry.create+5">Geometry.create(**primitive**: `Any`, **material**: `Any`, **index_count**: `Any`, **index_type**: `Any`, **index_buffer**: `Any`)
<a class="headerlink" href="#Geometry.create+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Geometry" signature="create(primitive : Any, material : Any, vert_count : Any)"></endpoint>
<signature id="Geometry.create+3">Geometry.create(**primitive**: `Any`, **material**: `Any`, **vert_count**: `Any`)
<a class="headerlink" href="#Geometry.create+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Geometry" signature="destroy(geo : Any)"></endpoint>
<signature id="Geometry.destroy">Geometry.destroy(**geo**: `Any`)
<a class="headerlink" href="#Geometry.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Geometry" signature="valid(geo : Any)"></endpoint>
<signature id="Geometry.valid">Geometry.valid(**geo**: `Any`)
<a class="headerlink" href="#Geometry.valid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Geometry" signature="set_world_matrix(geo : Any, world : Any)"></endpoint>
<signature id="Geometry.set_world_matrix+2">Geometry.set_world_matrix(**geo**: `Any`, **world**: `Any`)
<a class="headerlink" href="#Geometry.set_world_matrix+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Geometry" signature="set_vertex_buffer(geo : Any, index : Any, vertex_buffer : Any)"></endpoint>
<signature id="Geometry.set_vertex_buffer+3">Geometry.set_vertex_buffer(**geo**: `Any`, **index**: `Any`, **vertex_buffer**: `Any`)
<a class="headerlink" href="#Geometry.set_vertex_buffer+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Geometry" signature="get_vertex_buffer(geo : Any, index : Any)"></endpoint>
<signature id="Geometry.get_vertex_buffer+2">Geometry.get_vertex_buffer(**geo**: `Any`, **index**: `Any`)
<a class="headerlink" href="#Geometry.get_vertex_buffer+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Geometry" signature="get_index_buffer(geo : Any)"></endpoint>
<signature id="Geometry.get_index_buffer">Geometry.get_index_buffer(**geo**: `Any`)
<a class="headerlink" href="#Geometry.get_index_buffer" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Geometry" signature="set_instance_count(geo : Any, count : Any)"></endpoint>
<signature id="Geometry.set_instance_count+2">Geometry.set_instance_count(**geo**: `Any`, **count**: `Any`)
<a class="headerlink" href="#Geometry.set_instance_count+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Geometry" signature="get_instance_count(geo : Any)"></endpoint>
<signature id="Geometry.get_instance_count">Geometry.get_instance_count(**geo**: `Any`)
<a class="headerlink" href="#Geometry.get_instance_count" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Geometry" signature="set_vert_count(geo : Any, count : Any)"></endpoint>
<signature id="Geometry.set_vert_count+2">Geometry.set_vert_count(**geo**: `Any`, **count**: `Any`)
<a class="headerlink" href="#Geometry.set_vert_count+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Geometry" signature="set_material(geo : Any, material : Any)"></endpoint>
<signature id="Geometry.set_material+2">Geometry.set_material(**geo**: `Any`, **material**: `Any`)
<a class="headerlink" href="#Geometry.set_material+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Geometry" signature="set_stencil_references(geo : Any, back : Any, front : Any)"></endpoint>
<signature id="Geometry.set_stencil_references+3">Geometry.set_stencil_references(**geo**: `Any`, **back**: `Any`, **front**: `Any`)
<a class="headerlink" href="#Geometry.set_stencil_references+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Geometry" signature="set_stencil_reference(geo : Any, value : Any)"></endpoint>
<signature id="Geometry.set_stencil_reference+2">Geometry.set_stencil_reference(**geo**: `Any`, **value**: `Any`)
<a class="headerlink" href="#Geometry.set_stencil_reference+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Geometry" signature="set_aabb(geo : Any, center_x : Any, center_y : Any, center_z : Any, radius_x : Any, radius_y : Any, radius_z : Any)"></endpoint>
<signature id="Geometry.set_aabb+7">Geometry.set_aabb(**geo**: `Any`, **center_x**: `Any`, **center_y**: `Any`, **center_z**: `Any`, **radius_x**: `Any`, **radius_y**: `Any`, **radius_z**: `Any`)
<a class="headerlink" href="#Geometry.set_aabb+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Geometry" signature="get_aabb(geo : Any)"></endpoint>
<signature id="Geometry.get_aabb">Geometry.get_aabb(**geo**: `Any`)
<a class="headerlink" href="#Geometry.get_aabb" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Geometry" signature="get_world_obb(geo : Any)"></endpoint>
<signature id="Geometry.get_world_obb">Geometry.get_world_obb(**geo**: `Any`)
<a class="headerlink" href="#Geometry.get_world_obb" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Geometry" signature="get_vert_count(geo : Any)"></endpoint>
<signature id="Geometry.get_vert_count">Geometry.get_vert_count(**geo**: `Any`)
<a class="headerlink" href="#Geometry.get_vert_count" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Geometry" signature="get_material(geo : Any)"></endpoint>
<signature id="Geometry.get_material">Geometry.get_material(**geo**: `Any`)
<a class="headerlink" href="#Geometry.get_material" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Geometry" signature="obb_intersect_ray(geo : Any, ray_x : Any, ray_y : Any, ray_z : Any, ray_dir_x : Any, ray_dir_y : Any, ray_dir_z : Any)"></endpoint>
<signature id="Geometry.obb_intersect_ray+7">Geometry.obb_intersect_ray(**geo**: `Any`, **ray_x**: `Any`, **ray_y**: `Any`, **ray_z**: `Any`, **ray_dir_x**: `Any`, **ray_dir_y**: `Any`, **ray_dir_z**: `Any`)
<a class="headerlink" href="#Geometry.obb_intersect_ray+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Geometry" signature="layer_include_add(geo : Any, layer_id : Any)"></endpoint>
<signature id="Geometry.layer_include_add+2">Geometry.layer_include_add(**geo**: `Any`, **layer_id**: `Any`)
<a class="headerlink" href="#Geometry.layer_include_add+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Geometry" signature="layer_include_remove(geo : Any, layer_id : Any)"></endpoint>
<signature id="Geometry.layer_include_remove+2">Geometry.layer_include_remove(**geo**: `Any`, **layer_id**: `Any`)
<a class="headerlink" href="#Geometry.layer_include_remove+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Geometry" signature="layer_exclude_add(geo : Any, layer_id : Any)"></endpoint>
<signature id="Geometry.layer_exclude_add+2">Geometry.layer_exclude_add(**geo**: `Any`, **layer_id**: `Any`)
<a class="headerlink" href="#Geometry.layer_exclude_add+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Geometry" signature="layer_exclude_remove(geo : Any, layer_id : Any)"></endpoint>
<signature id="Geometry.layer_exclude_remove+2">Geometry.layer_exclude_remove(**geo**: `Any`, **layer_id**: `Any`)
<a class="headerlink" href="#Geometry.layer_exclude_remove+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Image
`:::js import "luxe: render" for Image`
> no docs found

- [create](#Image.create)(**desc**: `Any`)
- [redefine](#Image.redefine+2)(**image**: `Any`, **desc**: `Any`)
- [destroy](#Image.destroy)(**name**: `Any`)
- [valid](#Image.valid)(**name**: `Any`)
- [get_resource](#Image.get_resource)(**name**: `Any`)
- [generate_mipmaps](#Image.generate_mipmaps)(**image**: `Any`)
- [update](#Image.update+8)(**image**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`, **level**: `Any`, **slice**: `Any`, **bytes**: `Any`)
- [get_type](#Image.get_type)(**image**: `Any`)
- [get_width](#Image.get_width)(**image**: `Any`)
- [get_height](#Image.get_height)(**image**: `Any`)
- [get_depth](#Image.get_depth)(**image**: `Any`)
- [get_pixel_format](#Image.get_pixel_format)(**image**: `Any`)
- [get_mipmap_levels](#Image.get_mipmap_levels)(**image**: `Any`)
- [get_array_length](#Image.get_array_length)(**image**: `Any`)
- [get_sample_count](#Image.get_sample_count)(**image**: `Any`)
- [get_bytes](#Image.get_bytes+2)(**image**: `Any`, **into_bytes**: `Any`)

<hr/>
<endpoint module="luxe: render" class="Image" signature="create(desc : Any)"></endpoint>
<signature id="Image.create">Image.create(**desc**: `Any`)
<a class="headerlink" href="#Image.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Image" signature="redefine(image : Any, desc : Any)"></endpoint>
<signature id="Image.redefine+2">Image.redefine(**image**: `Any`, **desc**: `Any`)
<a class="headerlink" href="#Image.redefine+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Image" signature="destroy(name : Any)"></endpoint>
<signature id="Image.destroy">Image.destroy(**name**: `Any`)
<a class="headerlink" href="#Image.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Image" signature="valid(name : Any)"></endpoint>
<signature id="Image.valid">Image.valid(**name**: `Any`)
<a class="headerlink" href="#Image.valid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Image" signature="get_resource(name : Any)"></endpoint>
<signature id="Image.get_resource">Image.get_resource(**name**: `Any`)
<a class="headerlink" href="#Image.get_resource" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Image" signature="generate_mipmaps(image : Any)"></endpoint>
<signature id="Image.generate_mipmaps">Image.generate_mipmaps(**image**: `Any`)
<a class="headerlink" href="#Image.generate_mipmaps" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Image" signature="update(image : Any, x : Any, y : Any, w : Any, h : Any, level : Any, slice : Any, bytes : Any)"></endpoint>
<signature id="Image.update+8">Image.update(**image**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`, **level**: `Any`, **slice**: `Any`, **bytes**: `Any`)
<a class="headerlink" href="#Image.update+8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Image" signature="get_type(image : Any)"></endpoint>
<signature id="Image.get_type">Image.get_type(**image**: `Any`)
<a class="headerlink" href="#Image.get_type" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Image" signature="get_width(image : Any)"></endpoint>
<signature id="Image.get_width">Image.get_width(**image**: `Any`)
<a class="headerlink" href="#Image.get_width" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Image" signature="get_height(image : Any)"></endpoint>
<signature id="Image.get_height">Image.get_height(**image**: `Any`)
<a class="headerlink" href="#Image.get_height" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Image" signature="get_depth(image : Any)"></endpoint>
<signature id="Image.get_depth">Image.get_depth(**image**: `Any`)
<a class="headerlink" href="#Image.get_depth" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Image" signature="get_pixel_format(image : Any)"></endpoint>
<signature id="Image.get_pixel_format">Image.get_pixel_format(**image**: `Any`)
<a class="headerlink" href="#Image.get_pixel_format" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Image" signature="get_mipmap_levels(image : Any)"></endpoint>
<signature id="Image.get_mipmap_levels">Image.get_mipmap_levels(**image**: `Any`)
<a class="headerlink" href="#Image.get_mipmap_levels" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Image" signature="get_array_length(image : Any)"></endpoint>
<signature id="Image.get_array_length">Image.get_array_length(**image**: `Any`)
<a class="headerlink" href="#Image.get_array_length" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Image" signature="get_sample_count(image : Any)"></endpoint>
<signature id="Image.get_sample_count">Image.get_sample_count(**image**: `Any`)
<a class="headerlink" href="#Image.get_sample_count" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Image" signature="get_bytes(image : Any, into_bytes : Any)"></endpoint>
<signature id="Image.get_bytes+2">Image.get_bytes(**image**: `Any`, **into_bytes**: `Any`)
<a class="headerlink" href="#Image.get_bytes+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### ImageDesc
`:::js import "luxe: render" for ImageDesc`
> no docs found

- [display_id](#ImageDesc.display_id)
- [display_id](#ImageDesc.display_id=)=(v : Any)
- [type](#ImageDesc.type)
- [type](#ImageDesc.type=)=(v : Any)
- [pixel_format](#ImageDesc.pixel_format)
- [pixel_format](#ImageDesc.pixel_format=)=(v : Any)
- [width](#ImageDesc.width)
- [width](#ImageDesc.width=)=(v : Any)
- [height](#ImageDesc.height)
- [height](#ImageDesc.height=)=(v : Any)
- [depth](#ImageDesc.depth)
- [depth](#ImageDesc.depth=)=(v : Any)
- [mipmap_levels](#ImageDesc.mipmap_levels)
- [mipmap_levels](#ImageDesc.mipmap_levels=)=(v : Any)
- [array_length](#ImageDesc.array_length)
- [array_length](#ImageDesc.array_length=)=(v : Any)
- [sample_count](#ImageDesc.sample_count)
- [sample_count](#ImageDesc.sample_count=)=(v : Any)
- [usage](#ImageDesc.usage)
- [usage](#ImageDesc.usage=)=(v : Any)
- [new](#ImageDesc.new)()

<hr/>
<endpoint module="luxe: render" class="ImageDesc" signature="display_id"></endpoint>
<signature id="ImageDesc.display_id">ImageDesc.display_id
<a class="headerlink" href="#ImageDesc.display_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageDesc" signature="display_id=(v : Any)"></endpoint>
<signature id="ImageDesc.display_id=">ImageDesc.display_id=(v : Any)
<a class="headerlink" href="#ImageDesc.display_id=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageDesc" signature="type"></endpoint>
<signature id="ImageDesc.type">ImageDesc.type
<a class="headerlink" href="#ImageDesc.type" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageDesc" signature="type=(v : Any)"></endpoint>
<signature id="ImageDesc.type=">ImageDesc.type=(v : Any)
<a class="headerlink" href="#ImageDesc.type=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageDesc" signature="pixel_format"></endpoint>
<signature id="ImageDesc.pixel_format">ImageDesc.pixel_format
<a class="headerlink" href="#ImageDesc.pixel_format" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageDesc" signature="pixel_format=(v : Any)"></endpoint>
<signature id="ImageDesc.pixel_format=">ImageDesc.pixel_format=(v : Any)
<a class="headerlink" href="#ImageDesc.pixel_format=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageDesc" signature="width"></endpoint>
<signature id="ImageDesc.width">ImageDesc.width
<a class="headerlink" href="#ImageDesc.width" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageDesc" signature="width=(v : Any)"></endpoint>
<signature id="ImageDesc.width=">ImageDesc.width=(v : Any)
<a class="headerlink" href="#ImageDesc.width=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageDesc" signature="height"></endpoint>
<signature id="ImageDesc.height">ImageDesc.height
<a class="headerlink" href="#ImageDesc.height" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageDesc" signature="height=(v : Any)"></endpoint>
<signature id="ImageDesc.height=">ImageDesc.height=(v : Any)
<a class="headerlink" href="#ImageDesc.height=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageDesc" signature="depth"></endpoint>
<signature id="ImageDesc.depth">ImageDesc.depth
<a class="headerlink" href="#ImageDesc.depth" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageDesc" signature="depth=(v : Any)"></endpoint>
<signature id="ImageDesc.depth=">ImageDesc.depth=(v : Any)
<a class="headerlink" href="#ImageDesc.depth=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageDesc" signature="mipmap_levels"></endpoint>
<signature id="ImageDesc.mipmap_levels">ImageDesc.mipmap_levels
<a class="headerlink" href="#ImageDesc.mipmap_levels" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageDesc" signature="mipmap_levels=(v : Any)"></endpoint>
<signature id="ImageDesc.mipmap_levels=">ImageDesc.mipmap_levels=(v : Any)
<a class="headerlink" href="#ImageDesc.mipmap_levels=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageDesc" signature="array_length"></endpoint>
<signature id="ImageDesc.array_length">ImageDesc.array_length
<a class="headerlink" href="#ImageDesc.array_length" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageDesc" signature="array_length=(v : Any)"></endpoint>
<signature id="ImageDesc.array_length=">ImageDesc.array_length=(v : Any)
<a class="headerlink" href="#ImageDesc.array_length=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageDesc" signature="sample_count"></endpoint>
<signature id="ImageDesc.sample_count">ImageDesc.sample_count
<a class="headerlink" href="#ImageDesc.sample_count" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageDesc" signature="sample_count=(v : Any)"></endpoint>
<signature id="ImageDesc.sample_count=">ImageDesc.sample_count=(v : Any)
<a class="headerlink" href="#ImageDesc.sample_count=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageDesc" signature="usage"></endpoint>
<signature id="ImageDesc.usage">ImageDesc.usage
<a class="headerlink" href="#ImageDesc.usage" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageDesc" signature="usage=(v : Any)"></endpoint>
<signature id="ImageDesc.usage=">ImageDesc.usage=(v : Any)
<a class="headerlink" href="#ImageDesc.usage=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageDesc" signature="new()"></endpoint>
<signature id="ImageDesc.new">ImageDesc.new()
<a class="headerlink" href="#ImageDesc.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js ImageDesc`
> no docs found   

### ImageType
`:::js import "luxe: render" for ImageType`
> no docs found

- [invalid](#ImageType.invalid)
- [image1D](#ImageType.image1D)
- [image1DArray](#ImageType.image1DArray)
- [image2D](#ImageType.image2D)
- [image2DArray](#ImageType.image2DArray)
- [image2DMultisample](#ImageType.image2DMultisample)
- [imageCube](#ImageType.imageCube)
- [imageCubeArray](#ImageType.imageCubeArray)
- [image3D](#ImageType.image3D)
- [from_string](#ImageType.from_string)(**value**: `Any`)
- [name](#ImageType.name)(**value**: `Any`)

<hr/>
<endpoint module="luxe: render" class="ImageType" signature="invalid"></endpoint>
<signature id="ImageType.invalid">ImageType.invalid
<a class="headerlink" href="#ImageType.invalid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageType" signature="image1D"></endpoint>
<signature id="ImageType.image1D">ImageType.image1D
<a class="headerlink" href="#ImageType.image1D" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageType" signature="image1DArray"></endpoint>
<signature id="ImageType.image1DArray">ImageType.image1DArray
<a class="headerlink" href="#ImageType.image1DArray" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageType" signature="image2D"></endpoint>
<signature id="ImageType.image2D">ImageType.image2D
<a class="headerlink" href="#ImageType.image2D" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageType" signature="image2DArray"></endpoint>
<signature id="ImageType.image2DArray">ImageType.image2DArray
<a class="headerlink" href="#ImageType.image2DArray" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageType" signature="image2DMultisample"></endpoint>
<signature id="ImageType.image2DMultisample">ImageType.image2DMultisample
<a class="headerlink" href="#ImageType.image2DMultisample" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageType" signature="imageCube"></endpoint>
<signature id="ImageType.imageCube">ImageType.imageCube
<a class="headerlink" href="#ImageType.imageCube" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageType" signature="imageCubeArray"></endpoint>
<signature id="ImageType.imageCubeArray">ImageType.imageCubeArray
<a class="headerlink" href="#ImageType.imageCubeArray" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageType" signature="image3D"></endpoint>
<signature id="ImageType.image3D">ImageType.image3D
<a class="headerlink" href="#ImageType.image3D" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageType" signature="from_string(value : Any)"></endpoint>
<signature id="ImageType.from_string">ImageType.from_string(**value**: `Any`)
<a class="headerlink" href="#ImageType.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageType" signature="name(value : Any)"></endpoint>
<signature id="ImageType.name">ImageType.name(**value**: `Any`)
<a class="headerlink" href="#ImageType.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### ImageUsage
`:::js import "luxe: render" for ImageUsage`
> no docs found

- [unknown](#ImageUsage.unknown)
- [shader_read](#ImageUsage.shader_read)
- [shader_write](#ImageUsage.shader_write)
- [shader_read_write](#ImageUsage.shader_read_write)
- [render_target](#ImageUsage.render_target)
- [pixel_format_view](#ImageUsage.pixel_format_view)
- [stream](#ImageUsage.stream)

<hr/>
<endpoint module="luxe: render" class="ImageUsage" signature="unknown"></endpoint>
<signature id="ImageUsage.unknown">ImageUsage.unknown
<a class="headerlink" href="#ImageUsage.unknown" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageUsage" signature="shader_read"></endpoint>
<signature id="ImageUsage.shader_read">ImageUsage.shader_read
<a class="headerlink" href="#ImageUsage.shader_read" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageUsage" signature="shader_write"></endpoint>
<signature id="ImageUsage.shader_write">ImageUsage.shader_write
<a class="headerlink" href="#ImageUsage.shader_write" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageUsage" signature="shader_read_write"></endpoint>
<signature id="ImageUsage.shader_read_write">ImageUsage.shader_read_write
<a class="headerlink" href="#ImageUsage.shader_read_write" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageUsage" signature="render_target"></endpoint>
<signature id="ImageUsage.render_target">ImageUsage.render_target
<a class="headerlink" href="#ImageUsage.render_target" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageUsage" signature="pixel_format_view"></endpoint>
<signature id="ImageUsage.pixel_format_view">ImageUsage.pixel_format_view
<a class="headerlink" href="#ImageUsage.pixel_format_view" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="ImageUsage" signature="stream"></endpoint>
<signature id="ImageUsage.stream">ImageUsage.stream
<a class="headerlink" href="#ImageUsage.stream" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### IndexType
`:::js import "luxe: render" for IndexType`
> no docs found

- [none](#IndexType.none)
- [u16](#IndexType.u16)
- [u32](#IndexType.u32)
- [size_of](#IndexType.size_of)(**value**: `Any`)

<hr/>
<endpoint module="luxe: render" class="IndexType" signature="none"></endpoint>
<signature id="IndexType.none">IndexType.none
<a class="headerlink" href="#IndexType.none" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="IndexType" signature="u16"></endpoint>
<signature id="IndexType.u16">IndexType.u16
<a class="headerlink" href="#IndexType.u16" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="IndexType" signature="u32"></endpoint>
<signature id="IndexType.u32">IndexType.u32
<a class="headerlink" href="#IndexType.u32" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="IndexType" signature="size_of(value : Any)"></endpoint>
<signature id="IndexType.size_of">IndexType.size_of(**value**: `Any`)
<a class="headerlink" href="#IndexType.size_of" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### InputBuffer
`:::js import "luxe: render" for InputBuffer`
> no docs found

- [create](#InputBuffer.create+4)(**library**: `String`, **type**: `String`, **input**: `String`, **N**: `Num`)
- [set](#InputBuffer.set+2)(**buffer**: `InputBuffer`, **data**: `String`)

<hr/>
<endpoint module="luxe: render" class="InputBuffer" signature="create(library : String, type : String, input : String, N : Num)"></endpoint>
<signature id="InputBuffer.create+4">InputBuffer.create(**library**: `String`, **type**: `String`, **input**: `String`, **N**: `Num`)
<a class="headerlink" href="#InputBuffer.create+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js InputBuffer`
> no docs found   

<endpoint module="luxe: render" class="InputBuffer" signature="set(buffer : InputBuffer, data : String)"></endpoint>
<signature id="InputBuffer.set+2">InputBuffer.set(**buffer**: `InputBuffer`, **data**: `String`)
<a class="headerlink" href="#InputBuffer.set+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### LayerCompute
`:::js import "luxe: render" for LayerCompute`
> no docs found

- [id](#LayerCompute.id)
- [id](#LayerCompute.id=)=(v : Any)
- [new](#LayerCompute.new)(**desc**: `ComputeLayerDesc`)
- [update](#LayerCompute.update)(**desc**: `ComputeLayerDesc`)
- [queue](#LayerCompute.queue)(**path**: `RenderPath`)

<hr/>
<endpoint module="luxe: render" class="LayerCompute" signature="id"></endpoint>
<signature id="LayerCompute.id">LayerCompute.id
<a class="headerlink" href="#LayerCompute.id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="LayerCompute" signature="id=(v : Any)"></endpoint>
<signature id="LayerCompute.id=">LayerCompute.id=(v : Any)
<a class="headerlink" href="#LayerCompute.id=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="LayerCompute" signature="new(desc : ComputeLayerDesc)"></endpoint>
<signature id="LayerCompute.new">LayerCompute.new(**desc**: `ComputeLayerDesc`)
<a class="headerlink" href="#LayerCompute.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js LayerCompute`
> no docs found   

<endpoint module="luxe: render" class="LayerCompute" signature="update(desc : ComputeLayerDesc)"></endpoint>
<signature id="LayerCompute.update">LayerCompute.update(**desc**: `ComputeLayerDesc`)
<a class="headerlink" href="#LayerCompute.update" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="LayerCompute" signature="queue(path : RenderPath)"></endpoint>
<signature id="LayerCompute.queue">LayerCompute.queue(**path**: `RenderPath`)
<a class="headerlink" href="#LayerCompute.queue" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### LayerPass
`:::js import "luxe: render" for LayerPass`
> no docs found

- [id](#LayerPass.id)
- [id](#LayerPass.id=)=(v : Any)
- [new](#LayerPass.new)(**pass**: `Any`)
- [queue](#LayerPass.queue)(**path**: `Any`)
- [new](#LayerPass.new+2)(**path**: `Any`, **pass**: `Any`)
- [create_dest](#LayerPass.create_dest)(**pass**: `Any`)
- [update_material](#LayerPass.update_material)(**desc**: `Any`)
- [create_material](#LayerPass.create_material)(**pass**: `PassLayerDesc`)

<hr/>
<endpoint module="luxe: render" class="LayerPass" signature="id"></endpoint>
<signature id="LayerPass.id">LayerPass.id
<a class="headerlink" href="#LayerPass.id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="LayerPass" signature="id=(v : Any)"></endpoint>
<signature id="LayerPass.id=">LayerPass.id=(v : Any)
<a class="headerlink" href="#LayerPass.id=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="LayerPass" signature="new(pass : Any)"></endpoint>
<signature id="LayerPass.new">LayerPass.new(**pass**: `Any`)
<a class="headerlink" href="#LayerPass.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js LayerPass`
> no docs found   

<endpoint module="luxe: render" class="LayerPass" signature="queue(path : Any)"></endpoint>
<signature id="LayerPass.queue">LayerPass.queue(**path**: `Any`)
<a class="headerlink" href="#LayerPass.queue" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="LayerPass" signature="new(path : Any, pass : Any)"></endpoint>
<signature id="LayerPass.new+2">LayerPass.new(**path**: `Any`, **pass**: `Any`)
<a class="headerlink" href="#LayerPass.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js LayerPass`
> no docs found   

<endpoint module="luxe: render" class="LayerPass" signature="create_dest(pass : Any)"></endpoint>
<signature id="LayerPass.create_dest">LayerPass.create_dest(**pass**: `Any`)
<a class="headerlink" href="#LayerPass.create_dest" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="LayerPass" signature="update_material(desc : Any)"></endpoint>
<signature id="LayerPass.update_material">LayerPass.update_material(**desc**: `Any`)
<a class="headerlink" href="#LayerPass.update_material" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="LayerPass" signature="create_material(pass : PassLayerDesc)"></endpoint>
<signature id="LayerPass.create_material">LayerPass.create_material(**pass**: `PassLayerDesc`)
<a class="headerlink" href="#LayerPass.create_material" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### LoadAction
`:::js import "luxe: render" for LoadAction`
> no docs found

- [dont_care](#LoadAction.dont_care)
- [load](#LoadAction.load)
- [clear](#LoadAction.clear)

<hr/>
<endpoint module="luxe: render" class="LoadAction" signature="dont_care"></endpoint>
<signature id="LoadAction.dont_care">LoadAction.dont_care
<a class="headerlink" href="#LoadAction.dont_care" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="LoadAction" signature="load"></endpoint>
<signature id="LoadAction.load">LoadAction.load
<a class="headerlink" href="#LoadAction.load" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="LoadAction" signature="clear"></endpoint>
<signature id="LoadAction.clear">LoadAction.clear
<a class="headerlink" href="#LoadAction.clear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Material
`:::js import "luxe: render" for Material`
> no docs found

- [create](#Material.create)(**basis_type**: `Any`)
- [clone](#Material.clone)(**material**: `Any`)
- [destroy](#Material.destroy)(**material**: `Any`)
- [valid](#Material.valid)(**material**: `Any`)
- [undefine](#Material.undefine)(**name**: `Any`)
- [get_source_id](#Material.get_source_id)(**material**: `Any`)
- [set_source_id](#Material.set_source_id+2)(**material**: `Any`, **source_id**: `Any`)
- [set_stencil_references](#Material.set_stencil_references+3)(**material**: `Any`, **back**: `Any`, **front**: `Any`)
- [set_stencil_reference](#Material.set_stencil_reference+2)(**material**: `Any`, **value**: `Any`)
- [get_input_image](#Material.get_input_image+2)(**material**: `Any`, **name**: `Any`)
- [has_input](#Material.has_input+2)(**material**: `Any`, **name**: `Any`)
- [is_input_array](#Material.is_input_array+2)(**material**: `Any`, **name**: `Any`)
- [set_input](#Material.set_input+3)(**material**: `Any`, **name**: `Any`, **value**: `Any`)
- [define](#Material.define+2)(**name**: `Any`, **desc**: `Any`)

<hr/>
<endpoint module="luxe: render" class="Material" signature="create(basis_type : Any)"></endpoint>
<signature id="Material.create">Material.create(**basis_type**: `Any`)
<a class="headerlink" href="#Material.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Material" signature="clone(material : Any)"></endpoint>
<signature id="Material.clone">Material.clone(**material**: `Any`)
<a class="headerlink" href="#Material.clone" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Material" signature="destroy(material : Any)"></endpoint>
<signature id="Material.destroy">Material.destroy(**material**: `Any`)
<a class="headerlink" href="#Material.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Material" signature="valid(material : Any)"></endpoint>
<signature id="Material.valid">Material.valid(**material**: `Any`)
<a class="headerlink" href="#Material.valid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Material" signature="undefine(name : Any)"></endpoint>
<signature id="Material.undefine">Material.undefine(**name**: `Any`)
<a class="headerlink" href="#Material.undefine" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Material" signature="get_source_id(material : Any)"></endpoint>
<signature id="Material.get_source_id">Material.get_source_id(**material**: `Any`)
<a class="headerlink" href="#Material.get_source_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Material" signature="set_source_id(material : Any, source_id : Any)"></endpoint>
<signature id="Material.set_source_id+2">Material.set_source_id(**material**: `Any`, **source_id**: `Any`)
<a class="headerlink" href="#Material.set_source_id+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Material" signature="set_stencil_references(material : Any, back : Any, front : Any)"></endpoint>
<signature id="Material.set_stencil_references+3">Material.set_stencil_references(**material**: `Any`, **back**: `Any`, **front**: `Any`)
<a class="headerlink" href="#Material.set_stencil_references+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Material" signature="set_stencil_reference(material : Any, value : Any)"></endpoint>
<signature id="Material.set_stencil_reference+2">Material.set_stencil_reference(**material**: `Any`, **value**: `Any`)
<a class="headerlink" href="#Material.set_stencil_reference+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Material" signature="get_input_image(material : Any, name : Any)"></endpoint>
<signature id="Material.get_input_image+2">Material.get_input_image(**material**: `Any`, **name**: `Any`)
<a class="headerlink" href="#Material.get_input_image+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Material" signature="has_input(material : Any, name : Any)"></endpoint>
<signature id="Material.has_input+2">Material.has_input(**material**: `Any`, **name**: `Any`)
<a class="headerlink" href="#Material.has_input+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Material" signature="is_input_array(material : Any, name : Any)"></endpoint>
<signature id="Material.is_input_array+2">Material.is_input_array(**material**: `Any`, **name**: `Any`)
<a class="headerlink" href="#Material.is_input_array+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Material" signature="set_input(material : Any, name : Any, value : Any)"></endpoint>
<signature id="Material.set_input+3">Material.set_input(**material**: `Any`, **name**: `Any`, **value**: `Any`)
<a class="headerlink" href="#Material.set_input+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Material" signature="define(name : Any, desc : Any)"></endpoint>
<signature id="Material.define+2">Material.define(**name**: `Any`, **desc**: `Any`)
<a class="headerlink" href="#Material.define+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### MaterialDesc
`:::js import "luxe: render" for MaterialDesc`
> no docs found

- [new](#MaterialDesc.new)()
- [vertex_format](#MaterialDesc.vertex_format)
- [vertex_format](#MaterialDesc.vertex_format=)=(v : Any)
- [vertex](#MaterialDesc.vertex)
- [vertex](#MaterialDesc.vertex=)=(v : Any)
- [fragment](#MaterialDesc.fragment)
- [fragment](#MaterialDesc.fragment=)=(v : Any)
- [geometry](#MaterialDesc.geometry)
- [geometry](#MaterialDesc.geometry=)=(v : Any)
- [depth_bias_enabled](#MaterialDesc.depth_bias_enabled)
- [depth_bias_enabled](#MaterialDesc.depth_bias_enabled=)=(v : Any)
- [depth_bias](#MaterialDesc.depth_bias)
- [depth_bias](#MaterialDesc.depth_bias=)=(v : Any)
- [depth_bias_slope_scale](#MaterialDesc.depth_bias_slope_scale)
- [depth_bias_slope_scale](#MaterialDesc.depth_bias_slope_scale=)=(v : Any)
- [depth_test](#MaterialDesc.depth_test)
- [depth_test](#MaterialDesc.depth_test=)=(v : Any)
- [depth_write](#MaterialDesc.depth_write)
- [depth_write](#MaterialDesc.depth_write=)=(v : Any)
- [depth_compare](#MaterialDesc.depth_compare)
- [depth_compare](#MaterialDesc.depth_compare=)=(v : Any)
- [stencil_test](#MaterialDesc.stencil_test)
- [stencil_test](#MaterialDesc.stencil_test=)=(v : Any)
- [write_mask](#MaterialDesc.write_mask)
- [write_mask](#MaterialDesc.write_mask=)=(v : Any)
- [blending](#MaterialDesc.blending)
- [blending](#MaterialDesc.blending=)=(v : Any)
- [alpha_blend](#MaterialDesc.alpha_blend)
- [alpha_blend](#MaterialDesc.alpha_blend=)=(v : Any)
- [rgb_blend](#MaterialDesc.rgb_blend)
- [rgb_blend](#MaterialDesc.rgb_blend=)=(v : Any)
- [src_alpha](#MaterialDesc.src_alpha)
- [src_alpha](#MaterialDesc.src_alpha=)=(v : Any)
- [src_rgb](#MaterialDesc.src_rgb)
- [src_rgb](#MaterialDesc.src_rgb=)=(v : Any)
- [dest_alpha](#MaterialDesc.dest_alpha)
- [dest_alpha](#MaterialDesc.dest_alpha=)=(v : Any)
- [dest_rgb](#MaterialDesc.dest_rgb)
- [dest_rgb](#MaterialDesc.dest_rgb=)=(v : Any)
- [blend_color](#MaterialDesc.blend_color)
- [blend_color](#MaterialDesc.blend_color=)=(v : Any)
- [cull](#MaterialDesc.cull)
- [cull](#MaterialDesc.cull=)=(v : Any)
- [winding](#MaterialDesc.winding)
- [winding](#MaterialDesc.winding=)=(v : Any)
- [layers](#MaterialDesc.layers)
- [layers](#MaterialDesc.layers=)=(v : Any)
- [inputs](#MaterialDesc.inputs)
- [inputs](#MaterialDesc.inputs=)=(v : Any)
- [blocks](#MaterialDesc.blocks)
- [blocks](#MaterialDesc.blocks=)=(v : Any)
- [replace](#MaterialDesc.replace)
- [replace](#MaterialDesc.replace=)=(v : Any)
- [stencil_back_failure_stencil](#MaterialDesc.stencil_back_failure_stencil)
- [stencil_back_failure_stencil](#MaterialDesc.stencil_back_failure_stencil=)=(v : Any)
- [stencil_back_failure_depth](#MaterialDesc.stencil_back_failure_depth)
- [stencil_back_failure_depth](#MaterialDesc.stencil_back_failure_depth=)=(v : Any)
- [stencil_back_pass_depth_stencil](#MaterialDesc.stencil_back_pass_depth_stencil)
- [stencil_back_pass_depth_stencil](#MaterialDesc.stencil_back_pass_depth_stencil=)=(v : Any)
- [stencil_back_compare](#MaterialDesc.stencil_back_compare)
- [stencil_back_compare](#MaterialDesc.stencil_back_compare=)=(v : Any)
- [stencil_back_mask_read](#MaterialDesc.stencil_back_mask_read)
- [stencil_back_mask_read](#MaterialDesc.stencil_back_mask_read=)=(v : Any)
- [stencil_back_mask_write](#MaterialDesc.stencil_back_mask_write)
- [stencil_back_mask_write](#MaterialDesc.stencil_back_mask_write=)=(v : Any)
- [stencil_back_reference](#MaterialDesc.stencil_back_reference)
- [stencil_back_reference](#MaterialDesc.stencil_back_reference=)=(v : Any)
- [stencil_front_failure_stencil](#MaterialDesc.stencil_front_failure_stencil)
- [stencil_front_failure_stencil](#MaterialDesc.stencil_front_failure_stencil=)=(v : Any)
- [stencil_front_failure_depth](#MaterialDesc.stencil_front_failure_depth)
- [stencil_front_failure_depth](#MaterialDesc.stencil_front_failure_depth=)=(v : Any)
- [stencil_front_pass_depth_stencil](#MaterialDesc.stencil_front_pass_depth_stencil)
- [stencil_front_pass_depth_stencil](#MaterialDesc.stencil_front_pass_depth_stencil=)=(v : Any)
- [stencil_front_compare](#MaterialDesc.stencil_front_compare)
- [stencil_front_compare](#MaterialDesc.stencil_front_compare=)=(v : Any)
- [stencil_front_mask_read](#MaterialDesc.stencil_front_mask_read)
- [stencil_front_mask_read](#MaterialDesc.stencil_front_mask_read=)=(v : Any)
- [stencil_front_mask_write](#MaterialDesc.stencil_front_mask_write)
- [stencil_front_mask_write](#MaterialDesc.stencil_front_mask_write=)=(v : Any)
- [stencil_front_reference](#MaterialDesc.stencil_front_reference)
- [stencil_front_reference](#MaterialDesc.stencil_front_reference=)=(v : Any)

<hr/>
<endpoint module="luxe: render" class="MaterialDesc" signature="new()"></endpoint>
<signature id="MaterialDesc.new">MaterialDesc.new()
<a class="headerlink" href="#MaterialDesc.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js MaterialDesc`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="vertex_format"></endpoint>
<signature id="MaterialDesc.vertex_format">MaterialDesc.vertex_format
<a class="headerlink" href="#MaterialDesc.vertex_format" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="vertex_format=(v : Any)"></endpoint>
<signature id="MaterialDesc.vertex_format=">MaterialDesc.vertex_format=(v : Any)
<a class="headerlink" href="#MaterialDesc.vertex_format=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="vertex"></endpoint>
<signature id="MaterialDesc.vertex">MaterialDesc.vertex
<a class="headerlink" href="#MaterialDesc.vertex" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="vertex=(v : Any)"></endpoint>
<signature id="MaterialDesc.vertex=">MaterialDesc.vertex=(v : Any)
<a class="headerlink" href="#MaterialDesc.vertex=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="fragment"></endpoint>
<signature id="MaterialDesc.fragment">MaterialDesc.fragment
<a class="headerlink" href="#MaterialDesc.fragment" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="fragment=(v : Any)"></endpoint>
<signature id="MaterialDesc.fragment=">MaterialDesc.fragment=(v : Any)
<a class="headerlink" href="#MaterialDesc.fragment=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="geometry"></endpoint>
<signature id="MaterialDesc.geometry">MaterialDesc.geometry
<a class="headerlink" href="#MaterialDesc.geometry" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="geometry=(v : Any)"></endpoint>
<signature id="MaterialDesc.geometry=">MaterialDesc.geometry=(v : Any)
<a class="headerlink" href="#MaterialDesc.geometry=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="depth_bias_enabled"></endpoint>
<signature id="MaterialDesc.depth_bias_enabled">MaterialDesc.depth_bias_enabled
<a class="headerlink" href="#MaterialDesc.depth_bias_enabled" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="depth_bias_enabled=(v : Any)"></endpoint>
<signature id="MaterialDesc.depth_bias_enabled=">MaterialDesc.depth_bias_enabled=(v : Any)
<a class="headerlink" href="#MaterialDesc.depth_bias_enabled=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="depth_bias"></endpoint>
<signature id="MaterialDesc.depth_bias">MaterialDesc.depth_bias
<a class="headerlink" href="#MaterialDesc.depth_bias" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="depth_bias=(v : Any)"></endpoint>
<signature id="MaterialDesc.depth_bias=">MaterialDesc.depth_bias=(v : Any)
<a class="headerlink" href="#MaterialDesc.depth_bias=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="depth_bias_slope_scale"></endpoint>
<signature id="MaterialDesc.depth_bias_slope_scale">MaterialDesc.depth_bias_slope_scale
<a class="headerlink" href="#MaterialDesc.depth_bias_slope_scale" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="depth_bias_slope_scale=(v : Any)"></endpoint>
<signature id="MaterialDesc.depth_bias_slope_scale=">MaterialDesc.depth_bias_slope_scale=(v : Any)
<a class="headerlink" href="#MaterialDesc.depth_bias_slope_scale=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="depth_test"></endpoint>
<signature id="MaterialDesc.depth_test">MaterialDesc.depth_test
<a class="headerlink" href="#MaterialDesc.depth_test" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="depth_test=(v : Any)"></endpoint>
<signature id="MaterialDesc.depth_test=">MaterialDesc.depth_test=(v : Any)
<a class="headerlink" href="#MaterialDesc.depth_test=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="depth_write"></endpoint>
<signature id="MaterialDesc.depth_write">MaterialDesc.depth_write
<a class="headerlink" href="#MaterialDesc.depth_write" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="depth_write=(v : Any)"></endpoint>
<signature id="MaterialDesc.depth_write=">MaterialDesc.depth_write=(v : Any)
<a class="headerlink" href="#MaterialDesc.depth_write=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="depth_compare"></endpoint>
<signature id="MaterialDesc.depth_compare">MaterialDesc.depth_compare
<a class="headerlink" href="#MaterialDesc.depth_compare" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="depth_compare=(v : Any)"></endpoint>
<signature id="MaterialDesc.depth_compare=">MaterialDesc.depth_compare=(v : Any)
<a class="headerlink" href="#MaterialDesc.depth_compare=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_test"></endpoint>
<signature id="MaterialDesc.stencil_test">MaterialDesc.stencil_test
<a class="headerlink" href="#MaterialDesc.stencil_test" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_test=(v : Any)"></endpoint>
<signature id="MaterialDesc.stencil_test=">MaterialDesc.stencil_test=(v : Any)
<a class="headerlink" href="#MaterialDesc.stencil_test=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="write_mask"></endpoint>
<signature id="MaterialDesc.write_mask">MaterialDesc.write_mask
<a class="headerlink" href="#MaterialDesc.write_mask" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="write_mask=(v : Any)"></endpoint>
<signature id="MaterialDesc.write_mask=">MaterialDesc.write_mask=(v : Any)
<a class="headerlink" href="#MaterialDesc.write_mask=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="blending"></endpoint>
<signature id="MaterialDesc.blending">MaterialDesc.blending
<a class="headerlink" href="#MaterialDesc.blending" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="blending=(v : Any)"></endpoint>
<signature id="MaterialDesc.blending=">MaterialDesc.blending=(v : Any)
<a class="headerlink" href="#MaterialDesc.blending=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="alpha_blend"></endpoint>
<signature id="MaterialDesc.alpha_blend">MaterialDesc.alpha_blend
<a class="headerlink" href="#MaterialDesc.alpha_blend" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="alpha_blend=(v : Any)"></endpoint>
<signature id="MaterialDesc.alpha_blend=">MaterialDesc.alpha_blend=(v : Any)
<a class="headerlink" href="#MaterialDesc.alpha_blend=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="rgb_blend"></endpoint>
<signature id="MaterialDesc.rgb_blend">MaterialDesc.rgb_blend
<a class="headerlink" href="#MaterialDesc.rgb_blend" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="rgb_blend=(v : Any)"></endpoint>
<signature id="MaterialDesc.rgb_blend=">MaterialDesc.rgb_blend=(v : Any)
<a class="headerlink" href="#MaterialDesc.rgb_blend=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="src_alpha"></endpoint>
<signature id="MaterialDesc.src_alpha">MaterialDesc.src_alpha
<a class="headerlink" href="#MaterialDesc.src_alpha" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="src_alpha=(v : Any)"></endpoint>
<signature id="MaterialDesc.src_alpha=">MaterialDesc.src_alpha=(v : Any)
<a class="headerlink" href="#MaterialDesc.src_alpha=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="src_rgb"></endpoint>
<signature id="MaterialDesc.src_rgb">MaterialDesc.src_rgb
<a class="headerlink" href="#MaterialDesc.src_rgb" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="src_rgb=(v : Any)"></endpoint>
<signature id="MaterialDesc.src_rgb=">MaterialDesc.src_rgb=(v : Any)
<a class="headerlink" href="#MaterialDesc.src_rgb=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="dest_alpha"></endpoint>
<signature id="MaterialDesc.dest_alpha">MaterialDesc.dest_alpha
<a class="headerlink" href="#MaterialDesc.dest_alpha" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="dest_alpha=(v : Any)"></endpoint>
<signature id="MaterialDesc.dest_alpha=">MaterialDesc.dest_alpha=(v : Any)
<a class="headerlink" href="#MaterialDesc.dest_alpha=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="dest_rgb"></endpoint>
<signature id="MaterialDesc.dest_rgb">MaterialDesc.dest_rgb
<a class="headerlink" href="#MaterialDesc.dest_rgb" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="dest_rgb=(v : Any)"></endpoint>
<signature id="MaterialDesc.dest_rgb=">MaterialDesc.dest_rgb=(v : Any)
<a class="headerlink" href="#MaterialDesc.dest_rgb=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="blend_color"></endpoint>
<signature id="MaterialDesc.blend_color">MaterialDesc.blend_color
<a class="headerlink" href="#MaterialDesc.blend_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="blend_color=(v : Any)"></endpoint>
<signature id="MaterialDesc.blend_color=">MaterialDesc.blend_color=(v : Any)
<a class="headerlink" href="#MaterialDesc.blend_color=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="cull"></endpoint>
<signature id="MaterialDesc.cull">MaterialDesc.cull
<a class="headerlink" href="#MaterialDesc.cull" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="cull=(v : Any)"></endpoint>
<signature id="MaterialDesc.cull=">MaterialDesc.cull=(v : Any)
<a class="headerlink" href="#MaterialDesc.cull=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="winding"></endpoint>
<signature id="MaterialDesc.winding">MaterialDesc.winding
<a class="headerlink" href="#MaterialDesc.winding" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="winding=(v : Any)"></endpoint>
<signature id="MaterialDesc.winding=">MaterialDesc.winding=(v : Any)
<a class="headerlink" href="#MaterialDesc.winding=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="layers"></endpoint>
<signature id="MaterialDesc.layers">MaterialDesc.layers
<a class="headerlink" href="#MaterialDesc.layers" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="layers=(v : Any)"></endpoint>
<signature id="MaterialDesc.layers=">MaterialDesc.layers=(v : Any)
<a class="headerlink" href="#MaterialDesc.layers=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="inputs"></endpoint>
<signature id="MaterialDesc.inputs">MaterialDesc.inputs
<a class="headerlink" href="#MaterialDesc.inputs" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="inputs=(v : Any)"></endpoint>
<signature id="MaterialDesc.inputs=">MaterialDesc.inputs=(v : Any)
<a class="headerlink" href="#MaterialDesc.inputs=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="blocks"></endpoint>
<signature id="MaterialDesc.blocks">MaterialDesc.blocks
<a class="headerlink" href="#MaterialDesc.blocks" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="blocks=(v : Any)"></endpoint>
<signature id="MaterialDesc.blocks=">MaterialDesc.blocks=(v : Any)
<a class="headerlink" href="#MaterialDesc.blocks=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="replace"></endpoint>
<signature id="MaterialDesc.replace">MaterialDesc.replace
<a class="headerlink" href="#MaterialDesc.replace" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="replace=(v : Any)"></endpoint>
<signature id="MaterialDesc.replace=">MaterialDesc.replace=(v : Any)
<a class="headerlink" href="#MaterialDesc.replace=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_back_failure_stencil"></endpoint>
<signature id="MaterialDesc.stencil_back_failure_stencil">MaterialDesc.stencil_back_failure_stencil
<a class="headerlink" href="#MaterialDesc.stencil_back_failure_stencil" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_back_failure_stencil=(v : Any)"></endpoint>
<signature id="MaterialDesc.stencil_back_failure_stencil=">MaterialDesc.stencil_back_failure_stencil=(v : Any)
<a class="headerlink" href="#MaterialDesc.stencil_back_failure_stencil=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_back_failure_depth"></endpoint>
<signature id="MaterialDesc.stencil_back_failure_depth">MaterialDesc.stencil_back_failure_depth
<a class="headerlink" href="#MaterialDesc.stencil_back_failure_depth" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_back_failure_depth=(v : Any)"></endpoint>
<signature id="MaterialDesc.stencil_back_failure_depth=">MaterialDesc.stencil_back_failure_depth=(v : Any)
<a class="headerlink" href="#MaterialDesc.stencil_back_failure_depth=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_back_pass_depth_stencil"></endpoint>
<signature id="MaterialDesc.stencil_back_pass_depth_stencil">MaterialDesc.stencil_back_pass_depth_stencil
<a class="headerlink" href="#MaterialDesc.stencil_back_pass_depth_stencil" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_back_pass_depth_stencil=(v : Any)"></endpoint>
<signature id="MaterialDesc.stencil_back_pass_depth_stencil=">MaterialDesc.stencil_back_pass_depth_stencil=(v : Any)
<a class="headerlink" href="#MaterialDesc.stencil_back_pass_depth_stencil=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_back_compare"></endpoint>
<signature id="MaterialDesc.stencil_back_compare">MaterialDesc.stencil_back_compare
<a class="headerlink" href="#MaterialDesc.stencil_back_compare" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_back_compare=(v : Any)"></endpoint>
<signature id="MaterialDesc.stencil_back_compare=">MaterialDesc.stencil_back_compare=(v : Any)
<a class="headerlink" href="#MaterialDesc.stencil_back_compare=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_back_mask_read"></endpoint>
<signature id="MaterialDesc.stencil_back_mask_read">MaterialDesc.stencil_back_mask_read
<a class="headerlink" href="#MaterialDesc.stencil_back_mask_read" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_back_mask_read=(v : Any)"></endpoint>
<signature id="MaterialDesc.stencil_back_mask_read=">MaterialDesc.stencil_back_mask_read=(v : Any)
<a class="headerlink" href="#MaterialDesc.stencil_back_mask_read=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_back_mask_write"></endpoint>
<signature id="MaterialDesc.stencil_back_mask_write">MaterialDesc.stencil_back_mask_write
<a class="headerlink" href="#MaterialDesc.stencil_back_mask_write" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_back_mask_write=(v : Any)"></endpoint>
<signature id="MaterialDesc.stencil_back_mask_write=">MaterialDesc.stencil_back_mask_write=(v : Any)
<a class="headerlink" href="#MaterialDesc.stencil_back_mask_write=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_back_reference"></endpoint>
<signature id="MaterialDesc.stencil_back_reference">MaterialDesc.stencil_back_reference
<a class="headerlink" href="#MaterialDesc.stencil_back_reference" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_back_reference=(v : Any)"></endpoint>
<signature id="MaterialDesc.stencil_back_reference=">MaterialDesc.stencil_back_reference=(v : Any)
<a class="headerlink" href="#MaterialDesc.stencil_back_reference=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_front_failure_stencil"></endpoint>
<signature id="MaterialDesc.stencil_front_failure_stencil">MaterialDesc.stencil_front_failure_stencil
<a class="headerlink" href="#MaterialDesc.stencil_front_failure_stencil" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_front_failure_stencil=(v : Any)"></endpoint>
<signature id="MaterialDesc.stencil_front_failure_stencil=">MaterialDesc.stencil_front_failure_stencil=(v : Any)
<a class="headerlink" href="#MaterialDesc.stencil_front_failure_stencil=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_front_failure_depth"></endpoint>
<signature id="MaterialDesc.stencil_front_failure_depth">MaterialDesc.stencil_front_failure_depth
<a class="headerlink" href="#MaterialDesc.stencil_front_failure_depth" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_front_failure_depth=(v : Any)"></endpoint>
<signature id="MaterialDesc.stencil_front_failure_depth=">MaterialDesc.stencil_front_failure_depth=(v : Any)
<a class="headerlink" href="#MaterialDesc.stencil_front_failure_depth=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_front_pass_depth_stencil"></endpoint>
<signature id="MaterialDesc.stencil_front_pass_depth_stencil">MaterialDesc.stencil_front_pass_depth_stencil
<a class="headerlink" href="#MaterialDesc.stencil_front_pass_depth_stencil" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_front_pass_depth_stencil=(v : Any)"></endpoint>
<signature id="MaterialDesc.stencil_front_pass_depth_stencil=">MaterialDesc.stencil_front_pass_depth_stencil=(v : Any)
<a class="headerlink" href="#MaterialDesc.stencil_front_pass_depth_stencil=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_front_compare"></endpoint>
<signature id="MaterialDesc.stencil_front_compare">MaterialDesc.stencil_front_compare
<a class="headerlink" href="#MaterialDesc.stencil_front_compare" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_front_compare=(v : Any)"></endpoint>
<signature id="MaterialDesc.stencil_front_compare=">MaterialDesc.stencil_front_compare=(v : Any)
<a class="headerlink" href="#MaterialDesc.stencil_front_compare=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_front_mask_read"></endpoint>
<signature id="MaterialDesc.stencil_front_mask_read">MaterialDesc.stencil_front_mask_read
<a class="headerlink" href="#MaterialDesc.stencil_front_mask_read" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_front_mask_read=(v : Any)"></endpoint>
<signature id="MaterialDesc.stencil_front_mask_read=">MaterialDesc.stencil_front_mask_read=(v : Any)
<a class="headerlink" href="#MaterialDesc.stencil_front_mask_read=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_front_mask_write"></endpoint>
<signature id="MaterialDesc.stencil_front_mask_write">MaterialDesc.stencil_front_mask_write
<a class="headerlink" href="#MaterialDesc.stencil_front_mask_write" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_front_mask_write=(v : Any)"></endpoint>
<signature id="MaterialDesc.stencil_front_mask_write=">MaterialDesc.stencil_front_mask_write=(v : Any)
<a class="headerlink" href="#MaterialDesc.stencil_front_mask_write=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_front_reference"></endpoint>
<signature id="MaterialDesc.stencil_front_reference">MaterialDesc.stencil_front_reference
<a class="headerlink" href="#MaterialDesc.stencil_front_reference" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialDesc" signature="stencil_front_reference=(v : Any)"></endpoint>
<signature id="MaterialDesc.stencil_front_reference=">MaterialDesc.stencil_front_reference=(v : Any)
<a class="headerlink" href="#MaterialDesc.stencil_front_reference=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### MaterialFunction
`:::js import "luxe: render" for MaterialFunction`
> no docs found

- [library](#MaterialFunction.library)
- [library](#MaterialFunction.library=)=(v : Any)
- [function](#MaterialFunction.function)
- [function](#MaterialFunction.function=)=(v : Any)
- [new](#MaterialFunction.new)()

<hr/>
<endpoint module="luxe: render" class="MaterialFunction" signature="library"></endpoint>
<signature id="MaterialFunction.library">MaterialFunction.library
<a class="headerlink" href="#MaterialFunction.library" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialFunction" signature="library=(v : Any)"></endpoint>
<signature id="MaterialFunction.library=">MaterialFunction.library=(v : Any)
<a class="headerlink" href="#MaterialFunction.library=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialFunction" signature="function"></endpoint>
<signature id="MaterialFunction.function">MaterialFunction.function
<a class="headerlink" href="#MaterialFunction.function" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialFunction" signature="function=(v : Any)"></endpoint>
<signature id="MaterialFunction.function=">MaterialFunction.function=(v : Any)
<a class="headerlink" href="#MaterialFunction.function=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialFunction" signature="new()"></endpoint>
<signature id="MaterialFunction.new">MaterialFunction.new()
<a class="headerlink" href="#MaterialFunction.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js MaterialFunction`
> no docs found   

### MaterialInput
`:::js import "luxe: render" for MaterialInput`
> no docs found

- [name](#MaterialInput.name)
- [name](#MaterialInput.name=)=(name : Any)
- [type](#MaterialInput.type)
- [type](#MaterialInput.type=)=(type : Any)
- [value](#MaterialInput.value)
- [value](#MaterialInput.value=)=(value : Any)
- [count](#MaterialInput.count)
- [count](#MaterialInput.count=)=(count : Any)
- [new](#MaterialInput.new)()
- [new](#MaterialInput.new+4)(**name**: `Any`, **type**: `Any`, **value**: `Any`, **count**: `Any`)
- [new](#MaterialInput.new+3)(**name**: `Any`, **type**: `Any`, **value**: `Any`)
- [init](#MaterialInput.init+4)(**name**: `Any`, **type**: `Any`, **value**: `Any`, **count**: `Any`)

<hr/>
<endpoint module="luxe: render" class="MaterialInput" signature="name"></endpoint>
<signature id="MaterialInput.name">MaterialInput.name
<a class="headerlink" href="#MaterialInput.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInput" signature="name=(name : Any)"></endpoint>
<signature id="MaterialInput.name=">MaterialInput.name=(name : Any)
<a class="headerlink" href="#MaterialInput.name=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInput" signature="type"></endpoint>
<signature id="MaterialInput.type">MaterialInput.type
<a class="headerlink" href="#MaterialInput.type" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInput" signature="type=(type : Any)"></endpoint>
<signature id="MaterialInput.type=">MaterialInput.type=(type : Any)
<a class="headerlink" href="#MaterialInput.type=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInput" signature="value"></endpoint>
<signature id="MaterialInput.value">MaterialInput.value
<a class="headerlink" href="#MaterialInput.value" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInput" signature="value=(value : Any)"></endpoint>
<signature id="MaterialInput.value=">MaterialInput.value=(value : Any)
<a class="headerlink" href="#MaterialInput.value=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInput" signature="count"></endpoint>
<signature id="MaterialInput.count">MaterialInput.count
<a class="headerlink" href="#MaterialInput.count" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInput" signature="count=(count : Any)"></endpoint>
<signature id="MaterialInput.count=">MaterialInput.count=(count : Any)
<a class="headerlink" href="#MaterialInput.count=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInput" signature="new()"></endpoint>
<signature id="MaterialInput.new">MaterialInput.new()
<a class="headerlink" href="#MaterialInput.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js MaterialInput`
> no docs found   

<endpoint module="luxe: render" class="MaterialInput" signature="new(name : Any, type : Any, value : Any, count : Any)"></endpoint>
<signature id="MaterialInput.new+4">MaterialInput.new(**name**: `Any`, **type**: `Any`, **value**: `Any`, **count**: `Any`)
<a class="headerlink" href="#MaterialInput.new+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js MaterialInput`
> no docs found   

<endpoint module="luxe: render" class="MaterialInput" signature="new(name : Any, type : Any, value : Any)"></endpoint>
<signature id="MaterialInput.new+3">MaterialInput.new(**name**: `Any`, **type**: `Any`, **value**: `Any`)
<a class="headerlink" href="#MaterialInput.new+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js MaterialInput`
> no docs found   

<endpoint module="luxe: render" class="MaterialInput" signature="init(name : Any, type : Any, value : Any, count : Any)"></endpoint>
<signature id="MaterialInput.init+4">MaterialInput.init(**name**: `Any`, **type**: `Any`, **value**: `Any`, **count**: `Any`)
<a class="headerlink" href="#MaterialInput.init+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### MaterialInputBlock
`:::js import "luxe: render" for MaterialInputBlock`
> no docs found

- [get_defined](#MaterialInputBlock.get_defined)(**name**: `Any`)
- [has_input](#MaterialInputBlock.has_input+2)(**block**: `Any`, **name**: `Any`)
- [is_input_array](#MaterialInputBlock.is_input_array+2)(**block**: `Any`, **name**: `Any`)
- [set_floats](#MaterialInputBlock.set_floats+3)(**block**: `MaterialInputBlock`, **name**: `String`, **value**: `Floats`)
- [set_bytes](#MaterialInputBlock.set_bytes+3)(**block**: `MaterialInputBlock`, **name**: `String`, **value**: `Bytes`)
- [set](#MaterialInputBlock.set+3)(**block**: `Any`, **name**: `Any`, **value**: `Any`)

<hr/>
<endpoint module="luxe: render" class="MaterialInputBlock" signature="get_defined(name : Any)"></endpoint>
<signature id="MaterialInputBlock.get_defined">MaterialInputBlock.get_defined(**name**: `Any`)
<a class="headerlink" href="#MaterialInputBlock.get_defined" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputBlock" signature="has_input(block : Any, name : Any)"></endpoint>
<signature id="MaterialInputBlock.has_input+2">MaterialInputBlock.has_input(**block**: `Any`, **name**: `Any`)
<a class="headerlink" href="#MaterialInputBlock.has_input+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputBlock" signature="is_input_array(block : Any, name : Any)"></endpoint>
<signature id="MaterialInputBlock.is_input_array+2">MaterialInputBlock.is_input_array(**block**: `Any`, **name**: `Any`)
<a class="headerlink" href="#MaterialInputBlock.is_input_array+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputBlock" signature="set_floats(block : MaterialInputBlock, name : String, value : Floats)"></endpoint>
<signature id="MaterialInputBlock.set_floats+3">MaterialInputBlock.set_floats(**block**: `MaterialInputBlock`, **name**: `String`, **value**: `Floats`)
<a class="headerlink" href="#MaterialInputBlock.set_floats+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputBlock" signature="set_bytes(block : MaterialInputBlock, name : String, value : Bytes)"></endpoint>
<signature id="MaterialInputBlock.set_bytes+3">MaterialInputBlock.set_bytes(**block**: `MaterialInputBlock`, **name**: `String`, **value**: `Bytes`)
<a class="headerlink" href="#MaterialInputBlock.set_bytes+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputBlock" signature="set(block : Any, name : Any, value : Any)"></endpoint>
<signature id="MaterialInputBlock.set+3">MaterialInputBlock.set(**block**: `Any`, **name**: `Any`, **value**: `Any`)
<a class="headerlink" href="#MaterialInputBlock.set+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### MaterialInputImage
`:::js import "luxe: render" for MaterialInputImage`
> no docs found

- [image](#MaterialInputImage.image)
- [image](#MaterialInputImage.image=)=(image : Any)
- [type](#MaterialInputImage.type)
- [type](#MaterialInputImage.type=)=(type : Any)
- [sampler](#MaterialInputImage.sampler)
- [sampler](#MaterialInputImage.sampler=)=(value : Any)
- [new](#MaterialInputImage.new)()
- [new](#MaterialInputImage.new+2)(**in_image**: `Any`, **in_sampler**: `Any`)
- [new](#MaterialInputImage.new+3)(**in_image**: `Any`, **in_sampler**: `Any`, **in_type**: `Any`)

<hr/>
<endpoint module="luxe: render" class="MaterialInputImage" signature="image"></endpoint>
<signature id="MaterialInputImage.image">MaterialInputImage.image
<a class="headerlink" href="#MaterialInputImage.image" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputImage" signature="image=(image : Any)"></endpoint>
<signature id="MaterialInputImage.image=">MaterialInputImage.image=(image : Any)
<a class="headerlink" href="#MaterialInputImage.image=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputImage" signature="type"></endpoint>
<signature id="MaterialInputImage.type">MaterialInputImage.type
<a class="headerlink" href="#MaterialInputImage.type" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputImage" signature="type=(type : Any)"></endpoint>
<signature id="MaterialInputImage.type=">MaterialInputImage.type=(type : Any)
<a class="headerlink" href="#MaterialInputImage.type=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputImage" signature="sampler"></endpoint>
<signature id="MaterialInputImage.sampler">MaterialInputImage.sampler
<a class="headerlink" href="#MaterialInputImage.sampler" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputImage" signature="sampler=(value : Any)"></endpoint>
<signature id="MaterialInputImage.sampler=">MaterialInputImage.sampler=(value : Any)
<a class="headerlink" href="#MaterialInputImage.sampler=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputImage" signature="new()"></endpoint>
<signature id="MaterialInputImage.new">MaterialInputImage.new()
<a class="headerlink" href="#MaterialInputImage.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js MaterialInputImage`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputImage" signature="new(in_image : Any, in_sampler : Any)"></endpoint>
<signature id="MaterialInputImage.new+2">MaterialInputImage.new(**in_image**: `Any`, **in_sampler**: `Any`)
<a class="headerlink" href="#MaterialInputImage.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js MaterialInputImage`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputImage" signature="new(in_image : Any, in_sampler : Any, in_type : Any)"></endpoint>
<signature id="MaterialInputImage.new+3">MaterialInputImage.new(**in_image**: `Any`, **in_sampler**: `Any`, **in_type**: `Any`)
<a class="headerlink" href="#MaterialInputImage.new+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js MaterialInputImage`
> no docs found   

### MaterialInputType
`:::js import "luxe: render" for MaterialInputType`
> no docs found

- [invalid](#MaterialInputType.invalid)
- [bool](#MaterialInputType.bool)
- [bool2](#MaterialInputType.bool2)
- [bool4](#MaterialInputType.bool4)
- [int](#MaterialInputType.int)
- [int2](#MaterialInputType.int2)
- [int4](#MaterialInputType.int4)
- [uint](#MaterialInputType.uint)
- [uint2](#MaterialInputType.uint2)
- [uint4](#MaterialInputType.uint4)
- [float](#MaterialInputType.float)
- [float2](#MaterialInputType.float2)
- [float4](#MaterialInputType.float4)
- [mat4](#MaterialInputType.mat4)
- [image](#MaterialInputType.image)
- [from_string](#MaterialInputType.from_string)(**value**: `Any`)
- [name](#MaterialInputType.name)(**value**: `Any`)
- [size_of](#MaterialInputType.size_of)(**value**: `Any`)
- [default_of](#MaterialInputType.default_of)(**value**: `Any`)

<hr/>
<endpoint module="luxe: render" class="MaterialInputType" signature="invalid"></endpoint>
<signature id="MaterialInputType.invalid">MaterialInputType.invalid
<a class="headerlink" href="#MaterialInputType.invalid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputType" signature="bool"></endpoint>
<signature id="MaterialInputType.bool">MaterialInputType.bool
<a class="headerlink" href="#MaterialInputType.bool" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputType" signature="bool2"></endpoint>
<signature id="MaterialInputType.bool2">MaterialInputType.bool2
<a class="headerlink" href="#MaterialInputType.bool2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputType" signature="bool4"></endpoint>
<signature id="MaterialInputType.bool4">MaterialInputType.bool4
<a class="headerlink" href="#MaterialInputType.bool4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputType" signature="int"></endpoint>
<signature id="MaterialInputType.int">MaterialInputType.int
<a class="headerlink" href="#MaterialInputType.int" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputType" signature="int2"></endpoint>
<signature id="MaterialInputType.int2">MaterialInputType.int2
<a class="headerlink" href="#MaterialInputType.int2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputType" signature="int4"></endpoint>
<signature id="MaterialInputType.int4">MaterialInputType.int4
<a class="headerlink" href="#MaterialInputType.int4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputType" signature="uint"></endpoint>
<signature id="MaterialInputType.uint">MaterialInputType.uint
<a class="headerlink" href="#MaterialInputType.uint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputType" signature="uint2"></endpoint>
<signature id="MaterialInputType.uint2">MaterialInputType.uint2
<a class="headerlink" href="#MaterialInputType.uint2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputType" signature="uint4"></endpoint>
<signature id="MaterialInputType.uint4">MaterialInputType.uint4
<a class="headerlink" href="#MaterialInputType.uint4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputType" signature="float"></endpoint>
<signature id="MaterialInputType.float">MaterialInputType.float
<a class="headerlink" href="#MaterialInputType.float" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputType" signature="float2"></endpoint>
<signature id="MaterialInputType.float2">MaterialInputType.float2
<a class="headerlink" href="#MaterialInputType.float2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputType" signature="float4"></endpoint>
<signature id="MaterialInputType.float4">MaterialInputType.float4
<a class="headerlink" href="#MaterialInputType.float4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputType" signature="mat4"></endpoint>
<signature id="MaterialInputType.mat4">MaterialInputType.mat4
<a class="headerlink" href="#MaterialInputType.mat4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputType" signature="image"></endpoint>
<signature id="MaterialInputType.image">MaterialInputType.image
<a class="headerlink" href="#MaterialInputType.image" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputType" signature="from_string(value : Any)"></endpoint>
<signature id="MaterialInputType.from_string">MaterialInputType.from_string(**value**: `Any`)
<a class="headerlink" href="#MaterialInputType.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputType" signature="name(value : Any)"></endpoint>
<signature id="MaterialInputType.name">MaterialInputType.name(**value**: `Any`)
<a class="headerlink" href="#MaterialInputType.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputType" signature="size_of(value : Any)"></endpoint>
<signature id="MaterialInputType.size_of">MaterialInputType.size_of(**value**: `Any`)
<a class="headerlink" href="#MaterialInputType.size_of" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialInputType" signature="default_of(value : Any)"></endpoint>
<signature id="MaterialInputType.default_of">MaterialInputType.default_of(**value**: `Any`)
<a class="headerlink" href="#MaterialInputType.default_of" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### MaterialReplace
`:::js import "luxe: render" for MaterialReplace`
> no docs found

- [tag](#MaterialReplace.tag)
- [tag](#MaterialReplace.tag=)=(v : Any)
- [basis](#MaterialReplace.basis)
- [basis](#MaterialReplace.basis=)=(v : Any)
- [new](#MaterialReplace.new)()

<hr/>
<endpoint module="luxe: render" class="MaterialReplace" signature="tag"></endpoint>
<signature id="MaterialReplace.tag">MaterialReplace.tag
<a class="headerlink" href="#MaterialReplace.tag" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialReplace" signature="tag=(v : Any)"></endpoint>
<signature id="MaterialReplace.tag=">MaterialReplace.tag=(v : Any)
<a class="headerlink" href="#MaterialReplace.tag=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialReplace" signature="basis"></endpoint>
<signature id="MaterialReplace.basis">MaterialReplace.basis
<a class="headerlink" href="#MaterialReplace.basis" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialReplace" signature="basis=(v : Any)"></endpoint>
<signature id="MaterialReplace.basis=">MaterialReplace.basis=(v : Any)
<a class="headerlink" href="#MaterialReplace.basis=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="MaterialReplace" signature="new()"></endpoint>
<signature id="MaterialReplace.new">MaterialReplace.new()
<a class="headerlink" href="#MaterialReplace.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js MaterialReplace`
> no docs found   

### PassLayerDesc
`:::js import "luxe: render" for PassLayerDesc`
> no docs found

- [new](#PassLayerDesc.new)()
- [display_id](#PassLayerDesc.display_id)
- [display_id](#PassLayerDesc.display_id=)=(v : Any)
- [dest](#PassLayerDesc.dest)
- [dest](#PassLayerDesc.dest=)=(v : Any)
- [basis](#PassLayerDesc.basis)
- [basis](#PassLayerDesc.basis=)=(v : Any)
- [inputs](#PassLayerDesc.inputs)
- [inputs](#PassLayerDesc.inputs=)=(v : Any)
- [targets](#PassLayerDesc.targets)
- [targets](#PassLayerDesc.targets=)=(v : Any)
- [vertex](#PassLayerDesc.vertex=)=(v : Any)
- [vertex](#PassLayerDesc.vertex)
- [fragment](#PassLayerDesc.fragment=)=(v : Any)
- [fragment](#PassLayerDesc.fragment)
- [clear_color](#PassLayerDesc.clear_color)
- [clear_color](#PassLayerDesc.clear_color=)=(v : Any)
- [clear_depth](#PassLayerDesc.clear_depth)
- [clear_depth](#PassLayerDesc.clear_depth=)=(v : Any)
- [blending](#PassLayerDesc.blending)
- [blending](#PassLayerDesc.blending=)=(v : Any)
- [write_mask](#PassLayerDesc.write_mask)
- [write_mask](#PassLayerDesc.write_mask=)=(v : Any)
- [depth_test](#PassLayerDesc.depth_test)
- [depth_test](#PassLayerDesc.depth_test=)=(v : Any)
- [depth_write](#PassLayerDesc.depth_write)
- [depth_write](#PassLayerDesc.depth_write=)=(v : Any)
- [depth_compare](#PassLayerDesc.depth_compare)
- [depth_compare](#PassLayerDesc.depth_compare=)=(v : Any)

<hr/>
<endpoint module="luxe: render" class="PassLayerDesc" signature="new()"></endpoint>
<signature id="PassLayerDesc.new">PassLayerDesc.new()
<a class="headerlink" href="#PassLayerDesc.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js PassLayerDesc`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="display_id"></endpoint>
<signature id="PassLayerDesc.display_id">PassLayerDesc.display_id
<a class="headerlink" href="#PassLayerDesc.display_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="display_id=(v : Any)"></endpoint>
<signature id="PassLayerDesc.display_id=">PassLayerDesc.display_id=(v : Any)
<a class="headerlink" href="#PassLayerDesc.display_id=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="dest"></endpoint>
<signature id="PassLayerDesc.dest">PassLayerDesc.dest
<a class="headerlink" href="#PassLayerDesc.dest" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="dest=(v : Any)"></endpoint>
<signature id="PassLayerDesc.dest=">PassLayerDesc.dest=(v : Any)
<a class="headerlink" href="#PassLayerDesc.dest=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="basis"></endpoint>
<signature id="PassLayerDesc.basis">PassLayerDesc.basis
<a class="headerlink" href="#PassLayerDesc.basis" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="basis=(v : Any)"></endpoint>
<signature id="PassLayerDesc.basis=">PassLayerDesc.basis=(v : Any)
<a class="headerlink" href="#PassLayerDesc.basis=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="inputs"></endpoint>
<signature id="PassLayerDesc.inputs">PassLayerDesc.inputs
<a class="headerlink" href="#PassLayerDesc.inputs" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="inputs=(v : Any)"></endpoint>
<signature id="PassLayerDesc.inputs=">PassLayerDesc.inputs=(v : Any)
<a class="headerlink" href="#PassLayerDesc.inputs=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="targets"></endpoint>
<signature id="PassLayerDesc.targets">PassLayerDesc.targets
<a class="headerlink" href="#PassLayerDesc.targets" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="targets=(v : Any)"></endpoint>
<signature id="PassLayerDesc.targets=">PassLayerDesc.targets=(v : Any)
<a class="headerlink" href="#PassLayerDesc.targets=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="vertex=(v : Any)"></endpoint>
<signature id="PassLayerDesc.vertex=">PassLayerDesc.vertex=(v : Any)
<a class="headerlink" href="#PassLayerDesc.vertex=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="vertex"></endpoint>
<signature id="PassLayerDesc.vertex">PassLayerDesc.vertex
<a class="headerlink" href="#PassLayerDesc.vertex" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="fragment=(v : Any)"></endpoint>
<signature id="PassLayerDesc.fragment=">PassLayerDesc.fragment=(v : Any)
<a class="headerlink" href="#PassLayerDesc.fragment=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="fragment"></endpoint>
<signature id="PassLayerDesc.fragment">PassLayerDesc.fragment
<a class="headerlink" href="#PassLayerDesc.fragment" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="clear_color"></endpoint>
<signature id="PassLayerDesc.clear_color">PassLayerDesc.clear_color
<a class="headerlink" href="#PassLayerDesc.clear_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="clear_color=(v : Any)"></endpoint>
<signature id="PassLayerDesc.clear_color=">PassLayerDesc.clear_color=(v : Any)
<a class="headerlink" href="#PassLayerDesc.clear_color=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="clear_depth"></endpoint>
<signature id="PassLayerDesc.clear_depth">PassLayerDesc.clear_depth
<a class="headerlink" href="#PassLayerDesc.clear_depth" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="clear_depth=(v : Any)"></endpoint>
<signature id="PassLayerDesc.clear_depth=">PassLayerDesc.clear_depth=(v : Any)
<a class="headerlink" href="#PassLayerDesc.clear_depth=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="blending"></endpoint>
<signature id="PassLayerDesc.blending">PassLayerDesc.blending
<a class="headerlink" href="#PassLayerDesc.blending" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="blending=(v : Any)"></endpoint>
<signature id="PassLayerDesc.blending=">PassLayerDesc.blending=(v : Any)
<a class="headerlink" href="#PassLayerDesc.blending=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="write_mask"></endpoint>
<signature id="PassLayerDesc.write_mask">PassLayerDesc.write_mask
<a class="headerlink" href="#PassLayerDesc.write_mask" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="write_mask=(v : Any)"></endpoint>
<signature id="PassLayerDesc.write_mask=">PassLayerDesc.write_mask=(v : Any)
<a class="headerlink" href="#PassLayerDesc.write_mask=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="depth_test"></endpoint>
<signature id="PassLayerDesc.depth_test">PassLayerDesc.depth_test
<a class="headerlink" href="#PassLayerDesc.depth_test" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="depth_test=(v : Any)"></endpoint>
<signature id="PassLayerDesc.depth_test=">PassLayerDesc.depth_test=(v : Any)
<a class="headerlink" href="#PassLayerDesc.depth_test=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="depth_write"></endpoint>
<signature id="PassLayerDesc.depth_write">PassLayerDesc.depth_write
<a class="headerlink" href="#PassLayerDesc.depth_write" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="depth_write=(v : Any)"></endpoint>
<signature id="PassLayerDesc.depth_write=">PassLayerDesc.depth_write=(v : Any)
<a class="headerlink" href="#PassLayerDesc.depth_write=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="depth_compare"></endpoint>
<signature id="PassLayerDesc.depth_compare">PassLayerDesc.depth_compare
<a class="headerlink" href="#PassLayerDesc.depth_compare" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PassLayerDesc" signature="depth_compare=(v : Any)"></endpoint>
<signature id="PassLayerDesc.depth_compare=">PassLayerDesc.depth_compare=(v : Any)
<a class="headerlink" href="#PassLayerDesc.depth_compare=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### PixelFormat
`:::js import "luxe: render" for PixelFormat`
> no docs found

- [invalid](#PixelFormat.invalid)
- [rgb8Unorm](#PixelFormat.rgb8Unorm)
- [rgb8Unorm_srgb](#PixelFormat.rgb8Unorm_srgb)
- [rgb8Snorm](#PixelFormat.rgb8Snorm)
- [rgb8Uint](#PixelFormat.rgb8Uint)
- [rgb8Sint](#PixelFormat.rgb8Sint)
- [rgb16Unorm](#PixelFormat.rgb16Unorm)
- [rgb16Snorm](#PixelFormat.rgb16Snorm)
- [rgb16Uint](#PixelFormat.rgb16Uint)
- [rgb16Sint](#PixelFormat.rgb16Sint)
- [rgb16Float](#PixelFormat.rgb16Float)
- [rgb32Uint](#PixelFormat.rgb32Uint)
- [rgb32Sint](#PixelFormat.rgb32Sint)
- [rgb32Float](#PixelFormat.rgb32Float)
- [rgba8Unorm](#PixelFormat.rgba8Unorm)
- [rgba8Unorm_srgb](#PixelFormat.rgba8Unorm_srgb)
- [rgba8Snorm](#PixelFormat.rgba8Snorm)
- [rgba8Uint](#PixelFormat.rgba8Uint)
- [rgba8Sint](#PixelFormat.rgba8Sint)
- [rgba16Unorm](#PixelFormat.rgba16Unorm)
- [rgba16Snorm](#PixelFormat.rgba16Snorm)
- [rgba16Uint](#PixelFormat.rgba16Uint)
- [rgba16Sint](#PixelFormat.rgba16Sint)
- [rgba16Float](#PixelFormat.rgba16Float)
- [rgba32Uint](#PixelFormat.rgba32Uint)
- [rgba32Sint](#PixelFormat.rgba32Sint)
- [rgba32Float](#PixelFormat.rgba32Float)
- [r11g11b10Float](#PixelFormat.r11g11b10Float)
- [bgra8Unorm](#PixelFormat.bgra8Unorm)
- [bgra8Unorm_srgb](#PixelFormat.bgra8Unorm_srgb)
- [depth16Unorm](#PixelFormat.depth16Unorm)
- [depth32Float](#PixelFormat.depth32Float)
- [stencil8](#PixelFormat.stencil8)
- [depth24Unorm_stencil8](#PixelFormat.depth24Unorm_stencil8)
- [depth32Float_stencil8](#PixelFormat.depth32Float_stencil8)
- [bc1_rgba](#PixelFormat.bc1_rgba)
- [bc3_rgba](#PixelFormat.bc3_rgba)
- [r8Unorm](#PixelFormat.r8Unorm)
- [r8Snorm](#PixelFormat.r8Snorm)
- [r8Uint](#PixelFormat.r8Uint)
- [r8Sint](#PixelFormat.r8Sint)
- [rg8Unorm](#PixelFormat.rg8Unorm)
- [rg8Snorm](#PixelFormat.rg8Snorm)
- [rg8Uint](#PixelFormat.rg8Uint)
- [rg8Sint](#PixelFormat.rg8Sint)
- [r16Uint](#PixelFormat.r16Uint)
- [r16Sint](#PixelFormat.r16Sint)
- [r16Float](#PixelFormat.r16Float)
- [rg16Uint](#PixelFormat.rg16Uint)
- [rg16Sint](#PixelFormat.rg16Sint)
- [rg16Float](#PixelFormat.rg16Float)
- [r32Uint](#PixelFormat.r32Uint)
- [r32Sint](#PixelFormat.r32Sint)
- [r32Float](#PixelFormat.r32Float)
- [rg32Uint](#PixelFormat.rg32Uint)
- [rg32Sint](#PixelFormat.rg32Sint)
- [rg32Float](#PixelFormat.rg32Float)
- [from_string](#PixelFormat.from_string)(**value**: `Any`)
- [name](#PixelFormat.name)(**value**: `Any`)

<hr/>
<endpoint module="luxe: render" class="PixelFormat" signature="invalid"></endpoint>
<signature id="PixelFormat.invalid">PixelFormat.invalid
<a class="headerlink" href="#PixelFormat.invalid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgb8Unorm"></endpoint>
<signature id="PixelFormat.rgb8Unorm">PixelFormat.rgb8Unorm
<a class="headerlink" href="#PixelFormat.rgb8Unorm" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgb8Unorm_srgb"></endpoint>
<signature id="PixelFormat.rgb8Unorm_srgb">PixelFormat.rgb8Unorm_srgb
<a class="headerlink" href="#PixelFormat.rgb8Unorm_srgb" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgb8Snorm"></endpoint>
<signature id="PixelFormat.rgb8Snorm">PixelFormat.rgb8Snorm
<a class="headerlink" href="#PixelFormat.rgb8Snorm" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgb8Uint"></endpoint>
<signature id="PixelFormat.rgb8Uint">PixelFormat.rgb8Uint
<a class="headerlink" href="#PixelFormat.rgb8Uint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgb8Sint"></endpoint>
<signature id="PixelFormat.rgb8Sint">PixelFormat.rgb8Sint
<a class="headerlink" href="#PixelFormat.rgb8Sint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgb16Unorm"></endpoint>
<signature id="PixelFormat.rgb16Unorm">PixelFormat.rgb16Unorm
<a class="headerlink" href="#PixelFormat.rgb16Unorm" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgb16Snorm"></endpoint>
<signature id="PixelFormat.rgb16Snorm">PixelFormat.rgb16Snorm
<a class="headerlink" href="#PixelFormat.rgb16Snorm" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgb16Uint"></endpoint>
<signature id="PixelFormat.rgb16Uint">PixelFormat.rgb16Uint
<a class="headerlink" href="#PixelFormat.rgb16Uint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgb16Sint"></endpoint>
<signature id="PixelFormat.rgb16Sint">PixelFormat.rgb16Sint
<a class="headerlink" href="#PixelFormat.rgb16Sint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgb16Float"></endpoint>
<signature id="PixelFormat.rgb16Float">PixelFormat.rgb16Float
<a class="headerlink" href="#PixelFormat.rgb16Float" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgb32Uint"></endpoint>
<signature id="PixelFormat.rgb32Uint">PixelFormat.rgb32Uint
<a class="headerlink" href="#PixelFormat.rgb32Uint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgb32Sint"></endpoint>
<signature id="PixelFormat.rgb32Sint">PixelFormat.rgb32Sint
<a class="headerlink" href="#PixelFormat.rgb32Sint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgb32Float"></endpoint>
<signature id="PixelFormat.rgb32Float">PixelFormat.rgb32Float
<a class="headerlink" href="#PixelFormat.rgb32Float" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgba8Unorm"></endpoint>
<signature id="PixelFormat.rgba8Unorm">PixelFormat.rgba8Unorm
<a class="headerlink" href="#PixelFormat.rgba8Unorm" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgba8Unorm_srgb"></endpoint>
<signature id="PixelFormat.rgba8Unorm_srgb">PixelFormat.rgba8Unorm_srgb
<a class="headerlink" href="#PixelFormat.rgba8Unorm_srgb" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgba8Snorm"></endpoint>
<signature id="PixelFormat.rgba8Snorm">PixelFormat.rgba8Snorm
<a class="headerlink" href="#PixelFormat.rgba8Snorm" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgba8Uint"></endpoint>
<signature id="PixelFormat.rgba8Uint">PixelFormat.rgba8Uint
<a class="headerlink" href="#PixelFormat.rgba8Uint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgba8Sint"></endpoint>
<signature id="PixelFormat.rgba8Sint">PixelFormat.rgba8Sint
<a class="headerlink" href="#PixelFormat.rgba8Sint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgba16Unorm"></endpoint>
<signature id="PixelFormat.rgba16Unorm">PixelFormat.rgba16Unorm
<a class="headerlink" href="#PixelFormat.rgba16Unorm" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgba16Snorm"></endpoint>
<signature id="PixelFormat.rgba16Snorm">PixelFormat.rgba16Snorm
<a class="headerlink" href="#PixelFormat.rgba16Snorm" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgba16Uint"></endpoint>
<signature id="PixelFormat.rgba16Uint">PixelFormat.rgba16Uint
<a class="headerlink" href="#PixelFormat.rgba16Uint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgba16Sint"></endpoint>
<signature id="PixelFormat.rgba16Sint">PixelFormat.rgba16Sint
<a class="headerlink" href="#PixelFormat.rgba16Sint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgba16Float"></endpoint>
<signature id="PixelFormat.rgba16Float">PixelFormat.rgba16Float
<a class="headerlink" href="#PixelFormat.rgba16Float" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgba32Uint"></endpoint>
<signature id="PixelFormat.rgba32Uint">PixelFormat.rgba32Uint
<a class="headerlink" href="#PixelFormat.rgba32Uint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgba32Sint"></endpoint>
<signature id="PixelFormat.rgba32Sint">PixelFormat.rgba32Sint
<a class="headerlink" href="#PixelFormat.rgba32Sint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rgba32Float"></endpoint>
<signature id="PixelFormat.rgba32Float">PixelFormat.rgba32Float
<a class="headerlink" href="#PixelFormat.rgba32Float" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="r11g11b10Float"></endpoint>
<signature id="PixelFormat.r11g11b10Float">PixelFormat.r11g11b10Float
<a class="headerlink" href="#PixelFormat.r11g11b10Float" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="bgra8Unorm"></endpoint>
<signature id="PixelFormat.bgra8Unorm">PixelFormat.bgra8Unorm
<a class="headerlink" href="#PixelFormat.bgra8Unorm" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="bgra8Unorm_srgb"></endpoint>
<signature id="PixelFormat.bgra8Unorm_srgb">PixelFormat.bgra8Unorm_srgb
<a class="headerlink" href="#PixelFormat.bgra8Unorm_srgb" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="depth16Unorm"></endpoint>
<signature id="PixelFormat.depth16Unorm">PixelFormat.depth16Unorm
<a class="headerlink" href="#PixelFormat.depth16Unorm" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="depth32Float"></endpoint>
<signature id="PixelFormat.depth32Float">PixelFormat.depth32Float
<a class="headerlink" href="#PixelFormat.depth32Float" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="stencil8"></endpoint>
<signature id="PixelFormat.stencil8">PixelFormat.stencil8
<a class="headerlink" href="#PixelFormat.stencil8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="depth24Unorm_stencil8"></endpoint>
<signature id="PixelFormat.depth24Unorm_stencil8">PixelFormat.depth24Unorm_stencil8
<a class="headerlink" href="#PixelFormat.depth24Unorm_stencil8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="depth32Float_stencil8"></endpoint>
<signature id="PixelFormat.depth32Float_stencil8">PixelFormat.depth32Float_stencil8
<a class="headerlink" href="#PixelFormat.depth32Float_stencil8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="bc1_rgba"></endpoint>
<signature id="PixelFormat.bc1_rgba">PixelFormat.bc1_rgba
<a class="headerlink" href="#PixelFormat.bc1_rgba" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="bc3_rgba"></endpoint>
<signature id="PixelFormat.bc3_rgba">PixelFormat.bc3_rgba
<a class="headerlink" href="#PixelFormat.bc3_rgba" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="r8Unorm"></endpoint>
<signature id="PixelFormat.r8Unorm">PixelFormat.r8Unorm
<a class="headerlink" href="#PixelFormat.r8Unorm" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="r8Snorm"></endpoint>
<signature id="PixelFormat.r8Snorm">PixelFormat.r8Snorm
<a class="headerlink" href="#PixelFormat.r8Snorm" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="r8Uint"></endpoint>
<signature id="PixelFormat.r8Uint">PixelFormat.r8Uint
<a class="headerlink" href="#PixelFormat.r8Uint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="r8Sint"></endpoint>
<signature id="PixelFormat.r8Sint">PixelFormat.r8Sint
<a class="headerlink" href="#PixelFormat.r8Sint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rg8Unorm"></endpoint>
<signature id="PixelFormat.rg8Unorm">PixelFormat.rg8Unorm
<a class="headerlink" href="#PixelFormat.rg8Unorm" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rg8Snorm"></endpoint>
<signature id="PixelFormat.rg8Snorm">PixelFormat.rg8Snorm
<a class="headerlink" href="#PixelFormat.rg8Snorm" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rg8Uint"></endpoint>
<signature id="PixelFormat.rg8Uint">PixelFormat.rg8Uint
<a class="headerlink" href="#PixelFormat.rg8Uint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rg8Sint"></endpoint>
<signature id="PixelFormat.rg8Sint">PixelFormat.rg8Sint
<a class="headerlink" href="#PixelFormat.rg8Sint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="r16Uint"></endpoint>
<signature id="PixelFormat.r16Uint">PixelFormat.r16Uint
<a class="headerlink" href="#PixelFormat.r16Uint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="r16Sint"></endpoint>
<signature id="PixelFormat.r16Sint">PixelFormat.r16Sint
<a class="headerlink" href="#PixelFormat.r16Sint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="r16Float"></endpoint>
<signature id="PixelFormat.r16Float">PixelFormat.r16Float
<a class="headerlink" href="#PixelFormat.r16Float" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rg16Uint"></endpoint>
<signature id="PixelFormat.rg16Uint">PixelFormat.rg16Uint
<a class="headerlink" href="#PixelFormat.rg16Uint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rg16Sint"></endpoint>
<signature id="PixelFormat.rg16Sint">PixelFormat.rg16Sint
<a class="headerlink" href="#PixelFormat.rg16Sint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rg16Float"></endpoint>
<signature id="PixelFormat.rg16Float">PixelFormat.rg16Float
<a class="headerlink" href="#PixelFormat.rg16Float" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="r32Uint"></endpoint>
<signature id="PixelFormat.r32Uint">PixelFormat.r32Uint
<a class="headerlink" href="#PixelFormat.r32Uint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="r32Sint"></endpoint>
<signature id="PixelFormat.r32Sint">PixelFormat.r32Sint
<a class="headerlink" href="#PixelFormat.r32Sint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="r32Float"></endpoint>
<signature id="PixelFormat.r32Float">PixelFormat.r32Float
<a class="headerlink" href="#PixelFormat.r32Float" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rg32Uint"></endpoint>
<signature id="PixelFormat.rg32Uint">PixelFormat.rg32Uint
<a class="headerlink" href="#PixelFormat.rg32Uint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rg32Sint"></endpoint>
<signature id="PixelFormat.rg32Sint">PixelFormat.rg32Sint
<a class="headerlink" href="#PixelFormat.rg32Sint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="rg32Float"></endpoint>
<signature id="PixelFormat.rg32Float">PixelFormat.rg32Float
<a class="headerlink" href="#PixelFormat.rg32Float" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="from_string(value : Any)"></endpoint>
<signature id="PixelFormat.from_string">PixelFormat.from_string(**value**: `Any`)
<a class="headerlink" href="#PixelFormat.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PixelFormat" signature="name(value : Any)"></endpoint>
<signature id="PixelFormat.name">PixelFormat.name(**value**: `Any`)
<a class="headerlink" href="#PixelFormat.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Pose
`:::js import "luxe: render" for Pose`
> no docs found

- [create](#Pose.create)(**skeleton**: `Skeleton`)
- [destroy](#Pose.destroy)(**pose**: `Pose`)
- [reset](#Pose.reset)(**pose**: `Pose`)
- [copy](#Pose.copy+2)(**from**: `Pose`, **to**: `Pose`)
- [get_bone_pos_joint](#Pose.get_bone_pos_joint+2)(**pose**: `Pose`, **bone_id**: `String`)
- [get_bone_pos](#Pose.get_bone_pos+2)(**pose**: `Pose`, **bone_id**: `String`)
- [get_bone_up](#Pose.get_bone_up+2)(**pose**: `Pose`, **bone_id**: `String`)
- [get_bone_forward](#Pose.get_bone_forward+2)(**pose**: `Pose`, **bone_id**: `String`)
- [get_bone_right](#Pose.get_bone_right+2)(**pose**: `Pose`, **bone_id**: `String`)

<hr/>
<endpoint module="luxe: render" class="Pose" signature="create(skeleton : Skeleton)"></endpoint>
<signature id="Pose.create">Pose.create(**skeleton**: `Skeleton`)
<a class="headerlink" href="#Pose.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Pose`
> no docs found   

<endpoint module="luxe: render" class="Pose" signature="destroy(pose : Pose)"></endpoint>
<signature id="Pose.destroy">Pose.destroy(**pose**: `Pose`)
<a class="headerlink" href="#Pose.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: render" class="Pose" signature="reset(pose : Pose)"></endpoint>
<signature id="Pose.reset">Pose.reset(**pose**: `Pose`)
<a class="headerlink" href="#Pose.reset" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: render" class="Pose" signature="copy(from : Pose, to : Pose)"></endpoint>
<signature id="Pose.copy+2">Pose.copy(**from**: `Pose`, **to**: `Pose`)
<a class="headerlink" href="#Pose.copy+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: render" class="Pose" signature="get_bone_pos_joint(pose : Pose, bone_id : String)"></endpoint>
<signature id="Pose.get_bone_pos_joint+2">Pose.get_bone_pos_joint(**pose**: `Pose`, **bone_id**: `String`)
<a class="headerlink" href="#Pose.get_bone_pos_joint+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Float3`
> no docs found   

<endpoint module="luxe: render" class="Pose" signature="get_bone_pos(pose : Pose, bone_id : String)"></endpoint>
<signature id="Pose.get_bone_pos+2">Pose.get_bone_pos(**pose**: `Pose`, **bone_id**: `String`)
<a class="headerlink" href="#Pose.get_bone_pos+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Float3`
> no docs found   

<endpoint module="luxe: render" class="Pose" signature="get_bone_up(pose : Pose, bone_id : String)"></endpoint>
<signature id="Pose.get_bone_up+2">Pose.get_bone_up(**pose**: `Pose`, **bone_id**: `String`)
<a class="headerlink" href="#Pose.get_bone_up+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Float3`
> no docs found   

<endpoint module="luxe: render" class="Pose" signature="get_bone_forward(pose : Pose, bone_id : String)"></endpoint>
<signature id="Pose.get_bone_forward+2">Pose.get_bone_forward(**pose**: `Pose`, **bone_id**: `String`)
<a class="headerlink" href="#Pose.get_bone_forward+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Float3`
> no docs found   

<endpoint module="luxe: render" class="Pose" signature="get_bone_right(pose : Pose, bone_id : String)"></endpoint>
<signature id="Pose.get_bone_right+2">Pose.get_bone_right(**pose**: `Pose`, **bone_id**: `String`)
<a class="headerlink" href="#Pose.get_bone_right+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Float3`
> no docs found   

### PoseGraph
`:::js import "luxe: render" for PoseGraph`
> no docs found

- [create](#PoseGraph.create)(**skeleton**: `Skeleton`)
- [destroy](#PoseGraph.destroy)(**graph**: `PoseGraph`)
- [valid](#PoseGraph.valid)(**graph**: `PoseGraph`)
- [tick](#PoseGraph.tick+2)(**graph**: `PoseGraph`, **delta**: `Num`)
- [pose](#PoseGraph.pose)(**graph**: `PoseGraph`)
- [set_time](#PoseGraph.set_time+2)(**graph**: `PoseGraph`, **time**: `Num`)
- [get_time](#PoseGraph.get_time)(**graph**: `PoseGraph`)
- [node_add](#PoseGraph.node_add+2)(**graph**: `PoseGraph`, **node**: `PoseNode`)
- [node_remove](#PoseGraph.node_remove+2)(**graph**: `PoseGraph`, **index**: `Num`)
- [node_at](#PoseGraph.node_at+2)(**graph**: `PoseGraph`, **index**: `Num`)
- [node_index](#PoseGraph.node_index+2)(**graph**: `PoseGraph`, **node**: `PoseNode`)
- [node_count](#PoseGraph.node_count)(**graph**: `PoseGraph`)

<hr/>
<endpoint module="luxe: render" class="PoseGraph" signature="create(skeleton : Skeleton)"></endpoint>
<signature id="PoseGraph.create">PoseGraph.create(**skeleton**: `Skeleton`)
<a class="headerlink" href="#PoseGraph.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PoseGraph" signature="destroy(graph : PoseGraph)"></endpoint>
<signature id="PoseGraph.destroy">PoseGraph.destroy(**graph**: `PoseGraph`)
<a class="headerlink" href="#PoseGraph.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PoseGraph" signature="valid(graph : PoseGraph)"></endpoint>
<signature id="PoseGraph.valid">PoseGraph.valid(**graph**: `PoseGraph`)
<a class="headerlink" href="#PoseGraph.valid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: render" class="PoseGraph" signature="tick(graph : PoseGraph, delta : Num)"></endpoint>
<signature id="PoseGraph.tick+2">PoseGraph.tick(**graph**: `PoseGraph`, **delta**: `Num`)
<a class="headerlink" href="#PoseGraph.tick+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PoseGraph" signature="pose(graph : PoseGraph)"></endpoint>
<signature id="PoseGraph.pose">PoseGraph.pose(**graph**: `PoseGraph`)
<a class="headerlink" href="#PoseGraph.pose" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Pose`
> no docs found   

<endpoint module="luxe: render" class="PoseGraph" signature="set_time(graph : PoseGraph, time : Num)"></endpoint>
<signature id="PoseGraph.set_time+2">PoseGraph.set_time(**graph**: `PoseGraph`, **time**: `Num`)
<a class="headerlink" href="#PoseGraph.set_time+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PoseGraph" signature="get_time(graph : PoseGraph)"></endpoint>
<signature id="PoseGraph.get_time">PoseGraph.get_time(**graph**: `PoseGraph`)
<a class="headerlink" href="#PoseGraph.get_time" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: render" class="PoseGraph" signature="node_add(graph : PoseGraph, node : PoseNode)"></endpoint>
<signature id="PoseGraph.node_add+2">PoseGraph.node_add(**graph**: `PoseGraph`, **node**: `PoseNode`)
<a class="headerlink" href="#PoseGraph.node_add+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PoseGraph" signature="node_remove(graph : PoseGraph, index : Num)"></endpoint>
<signature id="PoseGraph.node_remove+2">PoseGraph.node_remove(**graph**: `PoseGraph`, **index**: `Num`)
<a class="headerlink" href="#PoseGraph.node_remove+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PoseGraph" signature="node_at(graph : PoseGraph, index : Num)"></endpoint>
<signature id="PoseGraph.node_at+2">PoseGraph.node_at(**graph**: `PoseGraph`, **index**: `Num`)
<a class="headerlink" href="#PoseGraph.node_at+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js PoseNode`
> no docs found   

<endpoint module="luxe: render" class="PoseGraph" signature="node_index(graph : PoseGraph, node : PoseNode)"></endpoint>
<signature id="PoseGraph.node_index+2">PoseGraph.node_index(**graph**: `PoseGraph`, **node**: `PoseNode`)
<a class="headerlink" href="#PoseGraph.node_index+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: render" class="PoseGraph" signature="node_count(graph : PoseGraph)"></endpoint>
<signature id="PoseGraph.node_count">PoseGraph.node_count(**graph**: `PoseGraph`)
<a class="headerlink" href="#PoseGraph.node_count" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

### PoseNode
`:::js import "luxe: render" for PoseNode`
> no docs found

- [create](#PoseNode.create)(**node_type_id**: `String`)
- [destroy](#PoseNode.destroy)(**node**: `PoseNode`)
- [valid](#PoseNode.valid)(**node**: `PoseNode`)
- [pose](#PoseNode.pose)(**node**: `PoseNode`)
- [block](#PoseNode.block)(**node**: `PoseNode`)
- [input](#PoseNode.input)(**node**: `PoseNode`)

<hr/>
<endpoint module="luxe: render" class="PoseNode" signature="create(node_type_id : String)"></endpoint>
<signature id="PoseNode.create">PoseNode.create(**node_type_id**: `String`)
<a class="headerlink" href="#PoseNode.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PoseNode" signature="destroy(node : PoseNode)"></endpoint>
<signature id="PoseNode.destroy">PoseNode.destroy(**node**: `PoseNode`)
<a class="headerlink" href="#PoseNode.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="PoseNode" signature="valid(node : PoseNode)"></endpoint>
<signature id="PoseNode.valid">PoseNode.valid(**node**: `PoseNode`)
<a class="headerlink" href="#PoseNode.valid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: render" class="PoseNode" signature="pose(node : PoseNode)"></endpoint>
<signature id="PoseNode.pose">PoseNode.pose(**node**: `PoseNode`)
<a class="headerlink" href="#PoseNode.pose" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Pose`
> no docs found   

<endpoint module="luxe: render" class="PoseNode" signature="block(node : PoseNode)"></endpoint>
<signature id="PoseNode.block">PoseNode.block(**node**: `PoseNode`)
<a class="headerlink" href="#PoseNode.block" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Block`
> no docs found   

<endpoint module="luxe: render" class="PoseNode" signature="input(node : PoseNode)"></endpoint>
<signature id="PoseNode.input">PoseNode.input(**node**: `PoseNode`)
<a class="headerlink" href="#PoseNode.input" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Any`
> no docs found   

### Primitive
`:::js import "luxe: render" for Primitive`
> no docs found

- [point](#Primitive.point)
- [line](#Primitive.line)
- [line_strip](#Primitive.line_strip)
- [triangle](#Primitive.triangle)
- [triangle_strip](#Primitive.triangle_strip)
- [from_string](#Primitive.from_string)(**value**: `Any`)

<hr/>
<endpoint module="luxe: render" class="Primitive" signature="point"></endpoint>
<signature id="Primitive.point">Primitive.point
<a class="headerlink" href="#Primitive.point" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Primitive" signature="line"></endpoint>
<signature id="Primitive.line">Primitive.line
<a class="headerlink" href="#Primitive.line" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Primitive" signature="line_strip"></endpoint>
<signature id="Primitive.line_strip">Primitive.line_strip
<a class="headerlink" href="#Primitive.line_strip" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Primitive" signature="triangle"></endpoint>
<signature id="Primitive.triangle">Primitive.triangle
<a class="headerlink" href="#Primitive.triangle" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Primitive" signature="triangle_strip"></endpoint>
<signature id="Primitive.triangle_strip">Primitive.triangle_strip
<a class="headerlink" href="#Primitive.triangle_strip" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Primitive" signature="from_string(value : Any)"></endpoint>
<signature id="Primitive.from_string">Primitive.from_string(**value**: `Any`)
<a class="headerlink" href="#Primitive.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Render
`:::js import "luxe: render" for Render`
> no docs found

- [dispatch](#Render.dispatch+5)(**library**: `String`, **function**: `String`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
- [submit](#Render.submit+6)(**set**: `RenderSet`, **target_path**: `RenderPath`, **target_resource**: `String`, **target_region**: `Float4`, **mat_proj**: `Floats`, **mat_view**: `Floats`)
- [submit_now](#Render.submit_now+6)(**set**: `RenderSet`, **target_path**: `RenderPath`, **target_resource**: `String`, **target_region**: `Float4`, **mat_proj**: `Floats`, **mat_view**: `Floats`)
- [submit_fn](#Render.submit_fn+8)(**set**: `RenderSet`, **target_path**: `String`, **target_resource**: `String`, **target_region**: `Float4`, **mat_proj**: `Floats`, **mat_view**: `Floats`, **settings**: `Maps`, **fn**: `Fn`)
- [create_set](#Render.create_set)()
- [destroy_set](#Render.destroy_set)(**set**: `RenderSet`)
- [valid_set](#Render.valid_set)(**set**: `RenderSet`)
- [set_add](#Render.set_add+2)(**set**: `RenderSet`, **geo**: `Geometry`)
- [set_remove](#Render.set_remove+2)(**set**: `RenderSet`, **geo**: `Geometry`)
- [set_get_geometry](#Render.set_get_geometry+2)(**set**: `RenderSet`, **into**: `List`)
- [set_get_count](#Render.set_get_count)(**set**: `RenderSet`)
- [create_path](#Render.create_path)()
- [destroy_path](#Render.destroy_path)(**path**: `RenderPath`)
- [valid_path](#Render.valid_path)(**path**: `RenderPath`)
- [window_w](#Render.window_w)()
- [window_h](#Render.window_h)()
- [window_state](#Render.window_state)()
- [window_focus](#Render.window_focus)()
- [window_hide](#Render.window_hide)(**state**: `Any`)
- [drawable_w](#Render.drawable_w)()
- [drawable_h](#Render.drawable_h)()
- [drawable_ratio](#Render.drawable_ratio)()
- [window_set_title](#Render.window_set_title)(**title**: `String`)
- [get_path_vertices](#Render.get_path_vertices+13)(**into_pos**: `Any`, **offset_pos**: `Any`, **stride_pos**: `Any`, **into_color**: `Any`, **offset_color**: `Any`, **stride_color**: `Any`, **points**: `Any`, **color**: `Any`, **thickness**: `Any`, **cap**: `Any`, **join**: `Any`, **closed**: `Any`, **miter_limit**: `Any`)
- [get_path_vertex_count](#Render.get_path_vertex_count+6)(**points**: `Any`, **thickness**: `Any`, **cap**: `Any`, **join**: `Any`, **closed**: `Any`, **miter_limit**: `Any`)
- [push_render_dest](#Render.push_render_dest+2)(**dest**: `Any`, **into**: `Any`)
- [path_add_render_layers](#Render.path_add_render_layers+4)(**path**: `Any`, **name**: `Any`, **layers_add**: `Any`, **layer**: `Any`)
- [path_add_render_layers](#Render.path_add_render_layers+5)(**path**: `Any`, **name**: `Any`, **layers_add**: `Any`, **layers_exclude**: `Any`, **layer**: `RenderLayerDesc`)
- [path_add_render_layer](#Render.path_add_render_layer+3)(**path**: `Any`, **name**: `Any`, **layer**: `RenderLayerDesc`)
- [path_add_compute_layer](#Render.path_add_compute_layer+5)(**path**: `Any`, **compute_id**: `Any`, **display**: `Any`, **dimensions**: `Any`, **inputs**: `Any`)
- [path_add_pass_layer](#Render.path_add_pass_layer+4)(**path**: `Any`, **name**: `Any`, **dest**: `Any`, **material**: `Any`)
- [path_remove](#Render.path_remove+2)(**path**: `Any`, **name**: `Any`)
- [path_update](#Render.path_update+3)(**path**: `Any`, **name**: `Any`, **layer**: `RenderLayerDesc`)
- [define_compute](#Render.define_compute+4)(**name**: `String`, **library**: `String`, **function**: `String`, **blocks**: `List`)
- [undefine_compute](#Render.undefine_compute)(**name**: `Any`)
- [undefine_sampler_state](#Render.undefine_sampler_state)(**name**: `Any`)
- [define_sampler_state](#Render.define_sampler_state+2)(**name**: `Any`, **desc**: `Any`)
- [define_vertex_format](#Render.define_vertex_format+2)(**name**: `Any`, **desc**: `Any`)
- [undefine_vertex_format](#Render.undefine_vertex_format)(**name**: `Any`)
- [define_resource](#Render.define_resource+2)(**name**: `Any`, **image**: `Any`)
- [resource_get_image](#Render.resource_get_image)(**name**: `Any`)
- [undefine_resource](#Render.undefine_resource)(**name**: `Any`)
- [create_vertex_buffer](#Render.create_vertex_buffer+2)(**data**: `Any`, **length**: `Any`)
- [vertex_buffer_get_size](#Render.vertex_buffer_get_size)(**vertex_buffer**: `Any`)
- [vertex_buffer_get_data](#Render.vertex_buffer_get_data+4)(**vertex_buffer**: `Any`, **into**: `Any`, **length**: `Any`, **offset**: `Any`)
- [vertex_buffer_replace](#Render.vertex_buffer_replace+3)(**vertex_buffer**: `Any`, **data**: `Any`, **length**: `Any`)
- [vertex_buffer_update](#Render.vertex_buffer_update+5)(**vertex_buffer**: `Any`, **data**: `Any`, **length**: `Any`, **data_src_offset**: `Any`, **dest_offset**: `Any`)
- [destroy_vertex_buffer](#Render.destroy_vertex_buffer)(**vertex_buffer**: `Any`)
- [create_index_buffer](#Render.create_index_buffer+2)(**data**: `Any`, **length**: `Any`)
- [create_index_buffer32](#Render.create_index_buffer32+2)(**data**: `Any`, **length**: `Any`)
- [index_buffer_get_size](#Render.index_buffer_get_size)(**index_buffer**: `Any`)
- [index_buffer_get_data](#Render.index_buffer_get_data+4)(**index_buffer**: `Any`, **into**: `Any`, **length**: `Any`, **offset**: `Any`)
- [index_buffer_replace](#Render.index_buffer_replace+3)(**index_buffer**: `Any`, **data**: `Any`, **length**: `Any`)
- [index_buffer_update](#Render.index_buffer_update+5)(**index_buffer**: `Any`, **data**: `Any`, **length**: `Any`, **data_src_offset**: `Any`, **dest_offset**: `Any`)
- [destroy_index_buffer](#Render.destroy_index_buffer)(**index_buffer**: `Any`)
- [create_text](#Render.create_text+5)(**material**: `Any`, **default_size**: `Any`, **default_font**: `Any`, **default_color**: `Any`, **render_set**: `Any`)
- [destroy_text](#Render.destroy_text)(**text**: `Any`)
- [valid_text](#Render.valid_text)(**text**: `Any`)
- [text_attr_clear](#Render.text_attr_clear)(**text**: `Any`)
- [text_set_text_buffer](#Render.text_set_text_buffer+2)(**text**: `Any`, **string**: `Any`)
- [text_set_attr](#Render.text_set_attr+6)(**text**: `Text`, **start**: `Num`, **length**: `Num`, **type**: `TextAttrType`, **key**: `String`, **value**: `Any`)
- [text_set_outline](#Render.text_set_outline+5)(**text**: `Text`, **radius**: `Num`, **softness**: `Num`, **color**: `Color`, **offset**: `Float2`)
- [text_set_shadow](#Render.text_set_shadow+5)(**text**: `Text`, **radius**: `Num`, **softness**: `Num`, **color**: `Color`, **offset**: `Float2`)
- [text_set_pos](#Render.text_set_pos+4)(**text**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [text_set_align](#Render.text_set_align+3)(**text**: `Any`, **align**: `Any`, **align_vertical**: `Any`)
- [text_set_bounds](#Render.text_set_bounds+5)(**text**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`)
- [text_commit](#Render.text_commit)(**text**: `Any`)
- [text_get_geometry](#Render.text_get_geometry)(**text**: `Any`)
- [text_get_extents](#Render.text_get_extents+3)(**text**: `Any`, **offset**: `Any`, **count**: `Any`)
- [text_get_extents](#Render.text_get_extents)(**text**: `Any`)
- [text_get_character_bounds](#Render.text_get_character_bounds+2)(**text**: `Any`, **index**: `Any`)
- [text_set_text](#Render.text_set_text+2)(**text**: `Any`, **string**: `Any`)
- [kVertexAttributes](#Render.kVertexAttributes)
- [kColorTargets](#Render.kColorTargets)
- [kMaterialLayerTargets](#Render.kMaterialLayerTargets)
- [kMaterialInputs](#Render.kMaterialInputs)
- [kMaterialReplace](#Render.kMaterialReplace)
- [kMaterialPassUsage](#Render.kMaterialPassUsage)
- [kStencilUnset](#Render.kStencilUnset)

<hr/>
<endpoint module="luxe: render" class="Render" signature="dispatch(library : String, function : String, x : Num, y : Num, z : Num)"></endpoint>
<signature id="Render.dispatch+5">Render.dispatch(**library**: `String`, **function**: `String`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Render.dispatch+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Dispatch a compute function directly (todo: doesn't have a way to get inputs atm)   

<endpoint module="luxe: render" class="Render" signature="submit(set : RenderSet, target_path : RenderPath, target_resource : String, target_region : Float4, mat_proj : Floats, mat_view : Floats)"></endpoint>
<signature id="Render.submit+6">Render.submit(**set**: `RenderSet`, **target_path**: `RenderPath`, **target_resource**: `String`, **target_region**: `Float4`, **mat_proj**: `Floats`, **mat_view**: `Floats`)
<a class="headerlink" href="#Render.submit+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="submit_now(set : RenderSet, target_path : RenderPath, target_resource : String, target_region : Float4, mat_proj : Floats, mat_view : Floats)"></endpoint>
<signature id="Render.submit_now+6">Render.submit_now(**set**: `RenderSet`, **target_path**: `RenderPath`, **target_resource**: `String`, **target_region**: `Float4`, **mat_proj**: `Floats`, **mat_view**: `Floats`)
<a class="headerlink" href="#Render.submit_now+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="submit_fn(set : RenderSet, target_path : String, target_resource : String, target_region : Float4, mat_proj : Floats, mat_view : Floats, settings : Maps, fn : Fn)"></endpoint>
<signature id="Render.submit_fn+8">Render.submit_fn(**set**: `RenderSet`, **target_path**: `String`, **target_resource**: `String`, **target_region**: `Float4`, **mat_proj**: `Floats`, **mat_view**: `Floats`, **settings**: `Maps`, **fn**: `Fn`)
<a class="headerlink" href="#Render.submit_fn+8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="create_set()"></endpoint>
<signature id="Render.create_set">Render.create_set()
<a class="headerlink" href="#Render.create_set" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js RenderSet`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="destroy_set(set : RenderSet)"></endpoint>
<signature id="Render.destroy_set">Render.destroy_set(**set**: `RenderSet`)
<a class="headerlink" href="#Render.destroy_set" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="valid_set(set : RenderSet)"></endpoint>
<signature id="Render.valid_set">Render.valid_set(**set**: `RenderSet`)
<a class="headerlink" href="#Render.valid_set" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="set_add(set : RenderSet, geo : Geometry)"></endpoint>
<signature id="Render.set_add+2">Render.set_add(**set**: `RenderSet`, **geo**: `Geometry`)
<a class="headerlink" href="#Render.set_add+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="set_remove(set : RenderSet, geo : Geometry)"></endpoint>
<signature id="Render.set_remove+2">Render.set_remove(**set**: `RenderSet`, **geo**: `Geometry`)
<a class="headerlink" href="#Render.set_remove+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="set_get_geometry(set : RenderSet, into : List)"></endpoint>
<signature id="Render.set_get_geometry+2">Render.set_get_geometry(**set**: `RenderSet`, **into**: `List`)
<a class="headerlink" href="#Render.set_get_geometry+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="set_get_count(set : RenderSet)"></endpoint>
<signature id="Render.set_get_count">Render.set_get_count(**set**: `RenderSet`)
<a class="headerlink" href="#Render.set_get_count" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="create_path()"></endpoint>
<signature id="Render.create_path">Render.create_path()
<a class="headerlink" href="#Render.create_path" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js RenderPath`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="destroy_path(path : RenderPath)"></endpoint>
<signature id="Render.destroy_path">Render.destroy_path(**path**: `RenderPath`)
<a class="headerlink" href="#Render.destroy_path" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="valid_path(path : RenderPath)"></endpoint>
<signature id="Render.valid_path">Render.valid_path(**path**: `RenderPath`)
<a class="headerlink" href="#Render.valid_path" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="window_w()"></endpoint>
<signature id="Render.window_w">Render.window_w()
<a class="headerlink" href="#Render.window_w" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="window_h()"></endpoint>
<signature id="Render.window_h">Render.window_h()
<a class="headerlink" href="#Render.window_h" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="window_state()"></endpoint>
<signature id="Render.window_state">Render.window_state()
<a class="headerlink" href="#Render.window_state" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="window_focus()"></endpoint>
<signature id="Render.window_focus">Render.window_focus()
<a class="headerlink" href="#Render.window_focus" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="window_hide(state : Any)"></endpoint>
<signature id="Render.window_hide">Render.window_hide(**state**: `Any`)
<a class="headerlink" href="#Render.window_hide" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="drawable_w()"></endpoint>
<signature id="Render.drawable_w">Render.drawable_w()
<a class="headerlink" href="#Render.drawable_w" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="drawable_h()"></endpoint>
<signature id="Render.drawable_h">Render.drawable_h()
<a class="headerlink" href="#Render.drawable_h" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="drawable_ratio()"></endpoint>
<signature id="Render.drawable_ratio">Render.drawable_ratio()
<a class="headerlink" href="#Render.drawable_ratio" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="window_set_title(title : String)"></endpoint>
<signature id="Render.window_set_title">Render.window_set_title(**title**: `String`)
<a class="headerlink" href="#Render.window_set_title" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="get_path_vertices(into_pos : Any, offset_pos : Any, stride_pos : Any, into_color : Any, offset_color : Any, stride_color : Any, points : Any, color : Any, thickness : Any, cap : Any, join : Any, closed : Any, miter_limit : Any)"></endpoint>
<signature id="Render.get_path_vertices+13">Render.get_path_vertices(**into_pos**: `Any`, **offset_pos**: `Any`, **stride_pos**: `Any`, **into_color**: `Any`, **offset_color**: `Any`, **stride_color**: `Any`, **points**: `Any`, **color**: `Any`, **thickness**: `Any`, **cap**: `Any`, **join**: `Any`, **closed**: `Any`, **miter_limit**: `Any`)
<a class="headerlink" href="#Render.get_path_vertices+13" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="get_path_vertex_count(points : Any, thickness : Any, cap : Any, join : Any, closed : Any, miter_limit : Any)"></endpoint>
<signature id="Render.get_path_vertex_count+6">Render.get_path_vertex_count(**points**: `Any`, **thickness**: `Any`, **cap**: `Any`, **join**: `Any`, **closed**: `Any`, **miter_limit**: `Any`)
<a class="headerlink" href="#Render.get_path_vertex_count+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="push_render_dest(dest : Any, into : Any)"></endpoint>
<signature id="Render.push_render_dest+2">Render.push_render_dest(**dest**: `Any`, **into**: `Any`)
<a class="headerlink" href="#Render.push_render_dest+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="path_add_render_layers(path : Any, name : Any, layers_add : Any, layer : Any)"></endpoint>
<signature id="Render.path_add_render_layers+4">Render.path_add_render_layers(**path**: `Any`, **name**: `Any`, **layers_add**: `Any`, **layer**: `Any`)
<a class="headerlink" href="#Render.path_add_render_layers+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="path_add_render_layers(path : Any, name : Any, layers_add : Any, layers_exclude : Any, layer : RenderLayerDesc)"></endpoint>
<signature id="Render.path_add_render_layers+5">Render.path_add_render_layers(**path**: `Any`, **name**: `Any`, **layers_add**: `Any`, **layers_exclude**: `Any`, **layer**: `RenderLayerDesc`)
<a class="headerlink" href="#Render.path_add_render_layers+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="path_add_render_layer(path : Any, name : Any, layer : RenderLayerDesc)"></endpoint>
<signature id="Render.path_add_render_layer+3">Render.path_add_render_layer(**path**: `Any`, **name**: `Any`, **layer**: `RenderLayerDesc`)
<a class="headerlink" href="#Render.path_add_render_layer+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="path_add_compute_layer(path : Any, compute_id : Any, display : Any, dimensions : Any, inputs : Any)"></endpoint>
<signature id="Render.path_add_compute_layer+5">Render.path_add_compute_layer(**path**: `Any`, **compute_id**: `Any`, **display**: `Any`, **dimensions**: `Any`, **inputs**: `Any`)
<a class="headerlink" href="#Render.path_add_compute_layer+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="path_add_pass_layer(path : Any, name : Any, dest : Any, material : Any)"></endpoint>
<signature id="Render.path_add_pass_layer+4">Render.path_add_pass_layer(**path**: `Any`, **name**: `Any`, **dest**: `Any`, **material**: `Any`)
<a class="headerlink" href="#Render.path_add_pass_layer+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="path_remove(path : Any, name : Any)"></endpoint>
<signature id="Render.path_remove+2">Render.path_remove(**path**: `Any`, **name**: `Any`)
<a class="headerlink" href="#Render.path_remove+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="path_update(path : Any, name : Any, layer : RenderLayerDesc)"></endpoint>
<signature id="Render.path_update+3">Render.path_update(**path**: `Any`, **name**: `Any`, **layer**: `RenderLayerDesc`)
<a class="headerlink" href="#Render.path_update+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="define_compute(name : String, library : String, function : String, blocks : List)"></endpoint>
<signature id="Render.define_compute+4">Render.define_compute(**name**: `String`, **library**: `String`, **function**: `String`, **blocks**: `List`)
<a class="headerlink" href="#Render.define_compute+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="undefine_compute(name : Any)"></endpoint>
<signature id="Render.undefine_compute">Render.undefine_compute(**name**: `Any`)
<a class="headerlink" href="#Render.undefine_compute" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="undefine_sampler_state(name : Any)"></endpoint>
<signature id="Render.undefine_sampler_state">Render.undefine_sampler_state(**name**: `Any`)
<a class="headerlink" href="#Render.undefine_sampler_state" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="define_sampler_state(name : Any, desc : Any)"></endpoint>
<signature id="Render.define_sampler_state+2">Render.define_sampler_state(**name**: `Any`, **desc**: `Any`)
<a class="headerlink" href="#Render.define_sampler_state+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="define_vertex_format(name : Any, desc : Any)"></endpoint>
<signature id="Render.define_vertex_format+2">Render.define_vertex_format(**name**: `Any`, **desc**: `Any`)
<a class="headerlink" href="#Render.define_vertex_format+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="undefine_vertex_format(name : Any)"></endpoint>
<signature id="Render.undefine_vertex_format">Render.undefine_vertex_format(**name**: `Any`)
<a class="headerlink" href="#Render.undefine_vertex_format" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="define_resource(name : Any, image : Any)"></endpoint>
<signature id="Render.define_resource+2">Render.define_resource(**name**: `Any`, **image**: `Any`)
<a class="headerlink" href="#Render.define_resource+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="resource_get_image(name : Any)"></endpoint>
<signature id="Render.resource_get_image">Render.resource_get_image(**name**: `Any`)
<a class="headerlink" href="#Render.resource_get_image" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="undefine_resource(name : Any)"></endpoint>
<signature id="Render.undefine_resource">Render.undefine_resource(**name**: `Any`)
<a class="headerlink" href="#Render.undefine_resource" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="create_vertex_buffer(data : Any, length : Any)"></endpoint>
<signature id="Render.create_vertex_buffer+2">Render.create_vertex_buffer(**data**: `Any`, **length**: `Any`)
<a class="headerlink" href="#Render.create_vertex_buffer+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="vertex_buffer_get_size(vertex_buffer : Any)"></endpoint>
<signature id="Render.vertex_buffer_get_size">Render.vertex_buffer_get_size(**vertex_buffer**: `Any`)
<a class="headerlink" href="#Render.vertex_buffer_get_size" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="vertex_buffer_get_data(vertex_buffer : Any, into : Any, length : Any, offset : Any)"></endpoint>
<signature id="Render.vertex_buffer_get_data+4">Render.vertex_buffer_get_data(**vertex_buffer**: `Any`, **into**: `Any`, **length**: `Any`, **offset**: `Any`)
<a class="headerlink" href="#Render.vertex_buffer_get_data+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="vertex_buffer_replace(vertex_buffer : Any, data : Any, length : Any)"></endpoint>
<signature id="Render.vertex_buffer_replace+3">Render.vertex_buffer_replace(**vertex_buffer**: `Any`, **data**: `Any`, **length**: `Any`)
<a class="headerlink" href="#Render.vertex_buffer_replace+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="vertex_buffer_update(vertex_buffer : Any, data : Any, length : Any, data_src_offset : Any, dest_offset : Any)"></endpoint>
<signature id="Render.vertex_buffer_update+5">Render.vertex_buffer_update(**vertex_buffer**: `Any`, **data**: `Any`, **length**: `Any`, **data_src_offset**: `Any`, **dest_offset**: `Any`)
<a class="headerlink" href="#Render.vertex_buffer_update+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="destroy_vertex_buffer(vertex_buffer : Any)"></endpoint>
<signature id="Render.destroy_vertex_buffer">Render.destroy_vertex_buffer(**vertex_buffer**: `Any`)
<a class="headerlink" href="#Render.destroy_vertex_buffer" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="create_index_buffer(data : Any, length : Any)"></endpoint>
<signature id="Render.create_index_buffer+2">Render.create_index_buffer(**data**: `Any`, **length**: `Any`)
<a class="headerlink" href="#Render.create_index_buffer+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="create_index_buffer32(data : Any, length : Any)"></endpoint>
<signature id="Render.create_index_buffer32+2">Render.create_index_buffer32(**data**: `Any`, **length**: `Any`)
<a class="headerlink" href="#Render.create_index_buffer32+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="index_buffer_get_size(index_buffer : Any)"></endpoint>
<signature id="Render.index_buffer_get_size">Render.index_buffer_get_size(**index_buffer**: `Any`)
<a class="headerlink" href="#Render.index_buffer_get_size" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="index_buffer_get_data(index_buffer : Any, into : Any, length : Any, offset : Any)"></endpoint>
<signature id="Render.index_buffer_get_data+4">Render.index_buffer_get_data(**index_buffer**: `Any`, **into**: `Any`, **length**: `Any`, **offset**: `Any`)
<a class="headerlink" href="#Render.index_buffer_get_data+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="index_buffer_replace(index_buffer : Any, data : Any, length : Any)"></endpoint>
<signature id="Render.index_buffer_replace+3">Render.index_buffer_replace(**index_buffer**: `Any`, **data**: `Any`, **length**: `Any`)
<a class="headerlink" href="#Render.index_buffer_replace+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="index_buffer_update(index_buffer : Any, data : Any, length : Any, data_src_offset : Any, dest_offset : Any)"></endpoint>
<signature id="Render.index_buffer_update+5">Render.index_buffer_update(**index_buffer**: `Any`, **data**: `Any`, **length**: `Any`, **data_src_offset**: `Any`, **dest_offset**: `Any`)
<a class="headerlink" href="#Render.index_buffer_update+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="destroy_index_buffer(index_buffer : Any)"></endpoint>
<signature id="Render.destroy_index_buffer">Render.destroy_index_buffer(**index_buffer**: `Any`)
<a class="headerlink" href="#Render.destroy_index_buffer" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="create_text(material : Any, default_size : Any, default_font : Any, default_color : Any, render_set : Any)"></endpoint>
<signature id="Render.create_text+5">Render.create_text(**material**: `Any`, **default_size**: `Any`, **default_font**: `Any`, **default_color**: `Any`, **render_set**: `Any`)
<a class="headerlink" href="#Render.create_text+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="destroy_text(text : Any)"></endpoint>
<signature id="Render.destroy_text">Render.destroy_text(**text**: `Any`)
<a class="headerlink" href="#Render.destroy_text" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="valid_text(text : Any)"></endpoint>
<signature id="Render.valid_text">Render.valid_text(**text**: `Any`)
<a class="headerlink" href="#Render.valid_text" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="text_attr_clear(text : Any)"></endpoint>
<signature id="Render.text_attr_clear">Render.text_attr_clear(**text**: `Any`)
<a class="headerlink" href="#Render.text_attr_clear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="text_set_text_buffer(text : Any, string : Any)"></endpoint>
<signature id="Render.text_set_text_buffer+2">Render.text_set_text_buffer(**text**: `Any`, **string**: `Any`)
<a class="headerlink" href="#Render.text_set_text_buffer+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="text_set_attr(text : Text, start : Num, length : Num, type : TextAttrType, key : String, value : Any)"></endpoint>
<signature id="Render.text_set_attr+6">Render.text_set_attr(**text**: `Text`, **start**: `Num`, **length**: `Num`, **type**: `TextAttrType`, **key**: `String`, **value**: `Any`)
<a class="headerlink" href="#Render.text_set_attr+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="text_set_outline(text : Text, radius : Num, softness : Num, color : Color, offset : Float2)"></endpoint>
<signature id="Render.text_set_outline+5">Render.text_set_outline(**text**: `Text`, **radius**: `Num`, **softness**: `Num`, **color**: `Color`, **offset**: `Float2`)
<a class="headerlink" href="#Render.text_set_outline+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="text_set_shadow(text : Text, radius : Num, softness : Num, color : Color, offset : Float2)"></endpoint>
<signature id="Render.text_set_shadow+5">Render.text_set_shadow(**text**: `Text`, **radius**: `Num`, **softness**: `Num`, **color**: `Color`, **offset**: `Float2`)
<a class="headerlink" href="#Render.text_set_shadow+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="text_set_pos(text : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Render.text_set_pos+4">Render.text_set_pos(**text**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Render.text_set_pos+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="text_set_align(text : Any, align : Any, align_vertical : Any)"></endpoint>
<signature id="Render.text_set_align+3">Render.text_set_align(**text**: `Any`, **align**: `Any`, **align_vertical**: `Any`)
<a class="headerlink" href="#Render.text_set_align+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="text_set_bounds(text : Any, x : Any, y : Any, w : Any, h : Any)"></endpoint>
<signature id="Render.text_set_bounds+5">Render.text_set_bounds(**text**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`)
<a class="headerlink" href="#Render.text_set_bounds+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="text_commit(text : Any)"></endpoint>
<signature id="Render.text_commit">Render.text_commit(**text**: `Any`)
<a class="headerlink" href="#Render.text_commit" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="text_get_geometry(text : Any)"></endpoint>
<signature id="Render.text_get_geometry">Render.text_get_geometry(**text**: `Any`)
<a class="headerlink" href="#Render.text_get_geometry" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="text_get_extents(text : Any, offset : Any, count : Any)"></endpoint>
<signature id="Render.text_get_extents+3">Render.text_get_extents(**text**: `Any`, **offset**: `Any`, **count**: `Any`)
<a class="headerlink" href="#Render.text_get_extents+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="text_get_extents(text : Any)"></endpoint>
<signature id="Render.text_get_extents">Render.text_get_extents(**text**: `Any`)
<a class="headerlink" href="#Render.text_get_extents" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="text_get_character_bounds(text : Any, index : Any)"></endpoint>
<signature id="Render.text_get_character_bounds+2">Render.text_get_character_bounds(**text**: `Any`, **index**: `Any`)
<a class="headerlink" href="#Render.text_get_character_bounds+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="text_set_text(text : Any, string : Any)"></endpoint>
<signature id="Render.text_set_text+2">Render.text_set_text(**text**: `Any`, **string**: `Any`)
<a class="headerlink" href="#Render.text_set_text+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="kVertexAttributes"></endpoint>
<signature id="Render.kVertexAttributes">Render.kVertexAttributes
<a class="headerlink" href="#Render.kVertexAttributes" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="kColorTargets"></endpoint>
<signature id="Render.kColorTargets">Render.kColorTargets
<a class="headerlink" href="#Render.kColorTargets" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="kMaterialLayerTargets"></endpoint>
<signature id="Render.kMaterialLayerTargets">Render.kMaterialLayerTargets
<a class="headerlink" href="#Render.kMaterialLayerTargets" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="kMaterialInputs"></endpoint>
<signature id="Render.kMaterialInputs">Render.kMaterialInputs
<a class="headerlink" href="#Render.kMaterialInputs" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="kMaterialReplace"></endpoint>
<signature id="Render.kMaterialReplace">Render.kMaterialReplace
<a class="headerlink" href="#Render.kMaterialReplace" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="kMaterialPassUsage"></endpoint>
<signature id="Render.kMaterialPassUsage">Render.kMaterialPassUsage
<a class="headerlink" href="#Render.kMaterialPassUsage" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Render" signature="kStencilUnset"></endpoint>
<signature id="Render.kStencilUnset">Render.kStencilUnset
<a class="headerlink" href="#Render.kStencilUnset" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### RenderDest
`:::js import "luxe: render" for RenderDest`
> no docs found

- [target_region](#RenderDest.target_region)
- [color](#RenderDest.color)
- [depth](#RenderDest.depth)
- [stencil](#RenderDest.stencil)
- [color](#RenderDest.color=)=(color : Any)
- [depth](#RenderDest.depth=)=(depth : Any)
- [stencil](#RenderDest.stencil=)=(stencil : Any)
- [new](#RenderDest.new)()

<hr/>
<endpoint module="luxe: render" class="RenderDest" signature="target_region"></endpoint>
<signature id="RenderDest.target_region">RenderDest.target_region
<a class="headerlink" href="#RenderDest.target_region" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDest" signature="color"></endpoint>
<signature id="RenderDest.color">RenderDest.color
<a class="headerlink" href="#RenderDest.color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDest" signature="depth"></endpoint>
<signature id="RenderDest.depth">RenderDest.depth
<a class="headerlink" href="#RenderDest.depth" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDest" signature="stencil"></endpoint>
<signature id="RenderDest.stencil">RenderDest.stencil
<a class="headerlink" href="#RenderDest.stencil" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDest" signature="color=(color : Any)"></endpoint>
<signature id="RenderDest.color=">RenderDest.color=(color : Any)
<a class="headerlink" href="#RenderDest.color=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDest" signature="depth=(depth : Any)"></endpoint>
<signature id="RenderDest.depth=">RenderDest.depth=(depth : Any)
<a class="headerlink" href="#RenderDest.depth=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDest" signature="stencil=(stencil : Any)"></endpoint>
<signature id="RenderDest.stencil=">RenderDest.stencil=(stencil : Any)
<a class="headerlink" href="#RenderDest.stencil=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDest" signature="new()"></endpoint>
<signature id="RenderDest.new">RenderDest.new()
<a class="headerlink" href="#RenderDest.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js RenderDest`
> no docs found   

### RenderDestColor
`:::js import "luxe: render" for RenderDestColor`
> no docs found

- [render_target](#RenderDestColor.render_target)
- [render_target](#RenderDestColor.render_target=)=(render_target : Any)
- [clear_color](#RenderDestColor.clear_color)
- [clear_color](#RenderDestColor.clear_color=)=(clear_color : Any)
- [load_action](#RenderDestColor.load_action)
- [load_action](#RenderDestColor.load_action=)=(load_action : Any)
- [store_action](#RenderDestColor.store_action)
- [store_action](#RenderDestColor.store_action=)=(store_action : Any)
- [level](#RenderDestColor.level)
- [level](#RenderDestColor.level=)=(level : Any)
- [slice](#RenderDestColor.slice)
- [slice](#RenderDestColor.slice=)=(slice : Any)
- [depth](#RenderDestColor.depth)
- [depth](#RenderDestColor.depth=)=(depth : Any)
- [new](#RenderDestColor.new)()

<hr/>
<endpoint module="luxe: render" class="RenderDestColor" signature="render_target"></endpoint>
<signature id="RenderDestColor.render_target">RenderDestColor.render_target
<a class="headerlink" href="#RenderDestColor.render_target" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestColor" signature="render_target=(render_target : Any)"></endpoint>
<signature id="RenderDestColor.render_target=">RenderDestColor.render_target=(render_target : Any)
<a class="headerlink" href="#RenderDestColor.render_target=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestColor" signature="clear_color"></endpoint>
<signature id="RenderDestColor.clear_color">RenderDestColor.clear_color
<a class="headerlink" href="#RenderDestColor.clear_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestColor" signature="clear_color=(clear_color : Any)"></endpoint>
<signature id="RenderDestColor.clear_color=">RenderDestColor.clear_color=(clear_color : Any)
<a class="headerlink" href="#RenderDestColor.clear_color=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestColor" signature="load_action"></endpoint>
<signature id="RenderDestColor.load_action">RenderDestColor.load_action
<a class="headerlink" href="#RenderDestColor.load_action" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestColor" signature="load_action=(load_action : Any)"></endpoint>
<signature id="RenderDestColor.load_action=">RenderDestColor.load_action=(load_action : Any)
<a class="headerlink" href="#RenderDestColor.load_action=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestColor" signature="store_action"></endpoint>
<signature id="RenderDestColor.store_action">RenderDestColor.store_action
<a class="headerlink" href="#RenderDestColor.store_action" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestColor" signature="store_action=(store_action : Any)"></endpoint>
<signature id="RenderDestColor.store_action=">RenderDestColor.store_action=(store_action : Any)
<a class="headerlink" href="#RenderDestColor.store_action=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestColor" signature="level"></endpoint>
<signature id="RenderDestColor.level">RenderDestColor.level
<a class="headerlink" href="#RenderDestColor.level" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestColor" signature="level=(level : Any)"></endpoint>
<signature id="RenderDestColor.level=">RenderDestColor.level=(level : Any)
<a class="headerlink" href="#RenderDestColor.level=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestColor" signature="slice"></endpoint>
<signature id="RenderDestColor.slice">RenderDestColor.slice
<a class="headerlink" href="#RenderDestColor.slice" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestColor" signature="slice=(slice : Any)"></endpoint>
<signature id="RenderDestColor.slice=">RenderDestColor.slice=(slice : Any)
<a class="headerlink" href="#RenderDestColor.slice=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestColor" signature="depth"></endpoint>
<signature id="RenderDestColor.depth">RenderDestColor.depth
<a class="headerlink" href="#RenderDestColor.depth" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestColor" signature="depth=(depth : Any)"></endpoint>
<signature id="RenderDestColor.depth=">RenderDestColor.depth=(depth : Any)
<a class="headerlink" href="#RenderDestColor.depth=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestColor" signature="new()"></endpoint>
<signature id="RenderDestColor.new">RenderDestColor.new()
<a class="headerlink" href="#RenderDestColor.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js RenderDestColor`
> no docs found   

### RenderDestDepth
`:::js import "luxe: render" for RenderDestDepth`
> no docs found

- [render_target](#RenderDestDepth.render_target)
- [render_target](#RenderDestDepth.render_target=)=(render_target : Any)
- [clear_depth](#RenderDestDepth.clear_depth)
- [clear_depth](#RenderDestDepth.clear_depth=)=(clear_depth : Any)
- [load_action](#RenderDestDepth.load_action)
- [load_action](#RenderDestDepth.load_action=)=(load_action : Any)
- [store_action](#RenderDestDepth.store_action)
- [store_action](#RenderDestDepth.store_action=)=(store_action : Any)
- [level](#RenderDestDepth.level)
- [level](#RenderDestDepth.level=)=(level : Any)
- [slice](#RenderDestDepth.slice)
- [slice](#RenderDestDepth.slice=)=(slice : Any)
- [depth](#RenderDestDepth.depth)
- [depth](#RenderDestDepth.depth=)=(depth : Any)
- [new](#RenderDestDepth.new)()

<hr/>
<endpoint module="luxe: render" class="RenderDestDepth" signature="render_target"></endpoint>
<signature id="RenderDestDepth.render_target">RenderDestDepth.render_target
<a class="headerlink" href="#RenderDestDepth.render_target" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestDepth" signature="render_target=(render_target : Any)"></endpoint>
<signature id="RenderDestDepth.render_target=">RenderDestDepth.render_target=(render_target : Any)
<a class="headerlink" href="#RenderDestDepth.render_target=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestDepth" signature="clear_depth"></endpoint>
<signature id="RenderDestDepth.clear_depth">RenderDestDepth.clear_depth
<a class="headerlink" href="#RenderDestDepth.clear_depth" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestDepth" signature="clear_depth=(clear_depth : Any)"></endpoint>
<signature id="RenderDestDepth.clear_depth=">RenderDestDepth.clear_depth=(clear_depth : Any)
<a class="headerlink" href="#RenderDestDepth.clear_depth=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestDepth" signature="load_action"></endpoint>
<signature id="RenderDestDepth.load_action">RenderDestDepth.load_action
<a class="headerlink" href="#RenderDestDepth.load_action" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestDepth" signature="load_action=(load_action : Any)"></endpoint>
<signature id="RenderDestDepth.load_action=">RenderDestDepth.load_action=(load_action : Any)
<a class="headerlink" href="#RenderDestDepth.load_action=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestDepth" signature="store_action"></endpoint>
<signature id="RenderDestDepth.store_action">RenderDestDepth.store_action
<a class="headerlink" href="#RenderDestDepth.store_action" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestDepth" signature="store_action=(store_action : Any)"></endpoint>
<signature id="RenderDestDepth.store_action=">RenderDestDepth.store_action=(store_action : Any)
<a class="headerlink" href="#RenderDestDepth.store_action=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestDepth" signature="level"></endpoint>
<signature id="RenderDestDepth.level">RenderDestDepth.level
<a class="headerlink" href="#RenderDestDepth.level" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestDepth" signature="level=(level : Any)"></endpoint>
<signature id="RenderDestDepth.level=">RenderDestDepth.level=(level : Any)
<a class="headerlink" href="#RenderDestDepth.level=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestDepth" signature="slice"></endpoint>
<signature id="RenderDestDepth.slice">RenderDestDepth.slice
<a class="headerlink" href="#RenderDestDepth.slice" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestDepth" signature="slice=(slice : Any)"></endpoint>
<signature id="RenderDestDepth.slice=">RenderDestDepth.slice=(slice : Any)
<a class="headerlink" href="#RenderDestDepth.slice=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestDepth" signature="depth"></endpoint>
<signature id="RenderDestDepth.depth">RenderDestDepth.depth
<a class="headerlink" href="#RenderDestDepth.depth" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestDepth" signature="depth=(depth : Any)"></endpoint>
<signature id="RenderDestDepth.depth=">RenderDestDepth.depth=(depth : Any)
<a class="headerlink" href="#RenderDestDepth.depth=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestDepth" signature="new()"></endpoint>
<signature id="RenderDestDepth.new">RenderDestDepth.new()
<a class="headerlink" href="#RenderDestDepth.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js RenderDestDepth`
> no docs found   

### RenderDestStencil
`:::js import "luxe: render" for RenderDestStencil`
> no docs found

- [render_target](#RenderDestStencil.render_target)
- [render_target](#RenderDestStencil.render_target=)=(render_target : Any)
- [clear_stencil](#RenderDestStencil.clear_stencil)
- [clear_stencil](#RenderDestStencil.clear_stencil=)=(clear_stencil : Any)
- [load_action](#RenderDestStencil.load_action)
- [load_action](#RenderDestStencil.load_action=)=(load_action : Any)
- [store_action](#RenderDestStencil.store_action)
- [store_action](#RenderDestStencil.store_action=)=(store_action : Any)
- [level](#RenderDestStencil.level)
- [level](#RenderDestStencil.level=)=(level : Any)
- [slice](#RenderDestStencil.slice)
- [slice](#RenderDestStencil.slice=)=(slice : Any)
- [depth](#RenderDestStencil.depth)
- [depth](#RenderDestStencil.depth=)=(depth : Any)
- [new](#RenderDestStencil.new)()

<hr/>
<endpoint module="luxe: render" class="RenderDestStencil" signature="render_target"></endpoint>
<signature id="RenderDestStencil.render_target">RenderDestStencil.render_target
<a class="headerlink" href="#RenderDestStencil.render_target" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestStencil" signature="render_target=(render_target : Any)"></endpoint>
<signature id="RenderDestStencil.render_target=">RenderDestStencil.render_target=(render_target : Any)
<a class="headerlink" href="#RenderDestStencil.render_target=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestStencil" signature="clear_stencil"></endpoint>
<signature id="RenderDestStencil.clear_stencil">RenderDestStencil.clear_stencil
<a class="headerlink" href="#RenderDestStencil.clear_stencil" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestStencil" signature="clear_stencil=(clear_stencil : Any)"></endpoint>
<signature id="RenderDestStencil.clear_stencil=">RenderDestStencil.clear_stencil=(clear_stencil : Any)
<a class="headerlink" href="#RenderDestStencil.clear_stencil=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestStencil" signature="load_action"></endpoint>
<signature id="RenderDestStencil.load_action">RenderDestStencil.load_action
<a class="headerlink" href="#RenderDestStencil.load_action" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestStencil" signature="load_action=(load_action : Any)"></endpoint>
<signature id="RenderDestStencil.load_action=">RenderDestStencil.load_action=(load_action : Any)
<a class="headerlink" href="#RenderDestStencil.load_action=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestStencil" signature="store_action"></endpoint>
<signature id="RenderDestStencil.store_action">RenderDestStencil.store_action
<a class="headerlink" href="#RenderDestStencil.store_action" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestStencil" signature="store_action=(store_action : Any)"></endpoint>
<signature id="RenderDestStencil.store_action=">RenderDestStencil.store_action=(store_action : Any)
<a class="headerlink" href="#RenderDestStencil.store_action=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestStencil" signature="level"></endpoint>
<signature id="RenderDestStencil.level">RenderDestStencil.level
<a class="headerlink" href="#RenderDestStencil.level" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestStencil" signature="level=(level : Any)"></endpoint>
<signature id="RenderDestStencil.level=">RenderDestStencil.level=(level : Any)
<a class="headerlink" href="#RenderDestStencil.level=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestStencil" signature="slice"></endpoint>
<signature id="RenderDestStencil.slice">RenderDestStencil.slice
<a class="headerlink" href="#RenderDestStencil.slice" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestStencil" signature="slice=(slice : Any)"></endpoint>
<signature id="RenderDestStencil.slice=">RenderDestStencil.slice=(slice : Any)
<a class="headerlink" href="#RenderDestStencil.slice=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestStencil" signature="depth"></endpoint>
<signature id="RenderDestStencil.depth">RenderDestStencil.depth
<a class="headerlink" href="#RenderDestStencil.depth" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestStencil" signature="depth=(depth : Any)"></endpoint>
<signature id="RenderDestStencil.depth=">RenderDestStencil.depth=(depth : Any)
<a class="headerlink" href="#RenderDestStencil.depth=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderDestStencil" signature="new()"></endpoint>
<signature id="RenderDestStencil.new">RenderDestStencil.new()
<a class="headerlink" href="#RenderDestStencil.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js RenderDestStencil`
> no docs found   

### RenderLayerDesc
`:::js import "luxe: render" for RenderLayerDesc`
> no docs found

- [display_id](#RenderLayerDesc.display_id)
- [display_id](#RenderLayerDesc.display_id=)=(display_id : Any)
- [sort](#RenderLayerDesc.sort)
- [sort](#RenderLayerDesc.sort=)=(sort : Any)
- [material_override](#RenderLayerDesc.material_override)
- [material_override](#RenderLayerDesc.material_override=)=(material_override : Any)
- [replace_tag](#RenderLayerDesc.replace_tag)
- [replace_tag](#RenderLayerDesc.replace_tag=)=(replace_tag : Any)
- [dest](#RenderLayerDesc.dest)
- [dest](#RenderLayerDesc.dest=)=(dest : Any)
- [new](#RenderLayerDesc.new)()

<hr/>
<endpoint module="luxe: render" class="RenderLayerDesc" signature="display_id"></endpoint>
<signature id="RenderLayerDesc.display_id">RenderLayerDesc.display_id
<a class="headerlink" href="#RenderLayerDesc.display_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderLayerDesc" signature="display_id=(display_id : Any)"></endpoint>
<signature id="RenderLayerDesc.display_id=">RenderLayerDesc.display_id=(display_id : Any)
<a class="headerlink" href="#RenderLayerDesc.display_id=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderLayerDesc" signature="sort"></endpoint>
<signature id="RenderLayerDesc.sort">RenderLayerDesc.sort
<a class="headerlink" href="#RenderLayerDesc.sort" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderLayerDesc" signature="sort=(sort : Any)"></endpoint>
<signature id="RenderLayerDesc.sort=">RenderLayerDesc.sort=(sort : Any)
<a class="headerlink" href="#RenderLayerDesc.sort=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderLayerDesc" signature="material_override"></endpoint>
<signature id="RenderLayerDesc.material_override">RenderLayerDesc.material_override
<a class="headerlink" href="#RenderLayerDesc.material_override" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderLayerDesc" signature="material_override=(material_override : Any)"></endpoint>
<signature id="RenderLayerDesc.material_override=">RenderLayerDesc.material_override=(material_override : Any)
<a class="headerlink" href="#RenderLayerDesc.material_override=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderLayerDesc" signature="replace_tag"></endpoint>
<signature id="RenderLayerDesc.replace_tag">RenderLayerDesc.replace_tag
<a class="headerlink" href="#RenderLayerDesc.replace_tag" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderLayerDesc" signature="replace_tag=(replace_tag : Any)"></endpoint>
<signature id="RenderLayerDesc.replace_tag=">RenderLayerDesc.replace_tag=(replace_tag : Any)
<a class="headerlink" href="#RenderLayerDesc.replace_tag=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderLayerDesc" signature="dest"></endpoint>
<signature id="RenderLayerDesc.dest">RenderLayerDesc.dest
<a class="headerlink" href="#RenderLayerDesc.dest" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderLayerDesc" signature="dest=(dest : Any)"></endpoint>
<signature id="RenderLayerDesc.dest=">RenderLayerDesc.dest=(dest : Any)
<a class="headerlink" href="#RenderLayerDesc.dest=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderLayerDesc" signature="new()"></endpoint>
<signature id="RenderLayerDesc.new">RenderLayerDesc.new()
<a class="headerlink" href="#RenderLayerDesc.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js RenderLayerDesc`
> no docs found   

### RenderPathContext
`:::js import "luxe: render" for RenderPathContext`
> no docs found

- [settings](#RenderPathContext.settings)
- [new](#RenderPathContext.new+2)(**path**: `String`, **settings**: `Map`)
- [path](#RenderPathContext.path)
- [change_path](#RenderPathContext.change_path)(**path**: `String`)
- [layer_render](#RenderPathContext.layer_render+2)(**name**: `String`, **render_layer_desc**: `RenderLayerDesc`)
- [layers_render](#RenderPathContext.layers_render+3)(**name**: `Any`, **layers_add**: `Any`, **render_layer_desc**: `Any`)
- [layers_render](#RenderPathContext.layers_render+4)(**name**: `Any`, **layers_add**: `Any`, **layers_exclude**: `Any`, **render_layer_desc**: `Any`)
- [layer_pass](#RenderPathContext.layer_pass)(**pass_layer_desc**: `Any`)
- [layer_compute](#RenderPathContext.layer_compute)(**compute_layer_desc**: `ComputeLayerDesc`)
- [get](#RenderPathContext.get+2)(**key**: `Any`, **default**: `Any`)
- [set](#RenderPathContext.set+2)(**key**: `Any`, **value**: `Any`)

<hr/>
<endpoint module="luxe: render" class="RenderPathContext" signature="settings"></endpoint>
<signature id="RenderPathContext.settings">RenderPathContext.settings
<a class="headerlink" href="#RenderPathContext.settings" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Map`
> no docs found   

<endpoint module="luxe: render" class="RenderPathContext" signature="new(path : String, settings : Map)"></endpoint>
<signature id="RenderPathContext.new+2">RenderPathContext.new(**path**: `String`, **settings**: `Map`)
<a class="headerlink" href="#RenderPathContext.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js RenderPathContext`
> no docs found   

<endpoint module="luxe: render" class="RenderPathContext" signature="path"></endpoint>
<signature id="RenderPathContext.path">RenderPathContext.path
<a class="headerlink" href="#RenderPathContext.path" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: render" class="RenderPathContext" signature="change_path(path : String)"></endpoint>
<signature id="RenderPathContext.change_path">RenderPathContext.change_path(**path**: `String`)
<a class="headerlink" href="#RenderPathContext.change_path" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderPathContext" signature="layer_render(name : String, render_layer_desc : RenderLayerDesc)"></endpoint>
<signature id="RenderPathContext.layer_render+2">RenderPathContext.layer_render(**name**: `String`, **render_layer_desc**: `RenderLayerDesc`)
<a class="headerlink" href="#RenderPathContext.layer_render+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderPathContext" signature="layers_render(name : Any, layers_add : Any, render_layer_desc : Any)"></endpoint>
<signature id="RenderPathContext.layers_render+3">RenderPathContext.layers_render(**name**: `Any`, **layers_add**: `Any`, **render_layer_desc**: `Any`)
<a class="headerlink" href="#RenderPathContext.layers_render+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderPathContext" signature="layers_render(name : Any, layers_add : Any, layers_exclude : Any, render_layer_desc : Any)"></endpoint>
<signature id="RenderPathContext.layers_render+4">RenderPathContext.layers_render(**name**: `Any`, **layers_add**: `Any`, **layers_exclude**: `Any`, **render_layer_desc**: `Any`)
<a class="headerlink" href="#RenderPathContext.layers_render+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderPathContext" signature="layer_pass(pass_layer_desc : Any)"></endpoint>
<signature id="RenderPathContext.layer_pass">RenderPathContext.layer_pass(**pass_layer_desc**: `Any`)
<a class="headerlink" href="#RenderPathContext.layer_pass" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderPathContext" signature="layer_compute(compute_layer_desc : ComputeLayerDesc)"></endpoint>
<signature id="RenderPathContext.layer_compute">RenderPathContext.layer_compute(**compute_layer_desc**: `ComputeLayerDesc`)
<a class="headerlink" href="#RenderPathContext.layer_compute" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderPathContext" signature="get(key : Any, default : Any)"></endpoint>
<signature id="RenderPathContext.get+2">RenderPathContext.get(**key**: `Any`, **default**: `Any`)
<a class="headerlink" href="#RenderPathContext.get+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderPathContext" signature="set(key : Any, value : Any)"></endpoint>
<signature id="RenderPathContext.set+2">RenderPathContext.set(**key**: `Any`, **value**: `Any`)
<a class="headerlink" href="#RenderPathContext.set+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### RenderViewDesc
`:::js import "luxe: render" for RenderViewDesc`
> no docs found

- [target](#RenderViewDesc.target)
- [target](#RenderViewDesc.target=)=(v : Any)
- [target](#RenderViewDesc.target)(**v**: `Any`)
- [path](#RenderViewDesc.path)
- [path](#RenderViewDesc.path=)=(v : Any)
- [path](#RenderViewDesc.path)(**v**: `Any`)
- [region](#RenderViewDesc.region)
- [region](#RenderViewDesc.region=)=(v : Any)
- [region](#RenderViewDesc.region)(**v**: `Any`)
- [settings](#RenderViewDesc.settings)
- [settings](#RenderViewDesc.settings=)=(v : Any)
- [settings](#RenderViewDesc.settings)(**v**: `Any`)
- [new](#RenderViewDesc.new+4)(**target_resource**: `Any`, **target_path**: `Any`, **target_region**: `Any`, **target_settings**: `Any`)
- [new](#RenderViewDesc.new)()

<hr/>
<endpoint module="luxe: render" class="RenderViewDesc" signature="target"></endpoint>
<signature id="RenderViewDesc.target">RenderViewDesc.target
<a class="headerlink" href="#RenderViewDesc.target" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderViewDesc" signature="target=(v : Any)"></endpoint>
<signature id="RenderViewDesc.target=">RenderViewDesc.target=(v : Any)
<a class="headerlink" href="#RenderViewDesc.target=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderViewDesc" signature="target(v : Any)"></endpoint>
<signature id="RenderViewDesc.target">RenderViewDesc.target(**v**: `Any`)
<a class="headerlink" href="#RenderViewDesc.target" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderViewDesc" signature="path"></endpoint>
<signature id="RenderViewDesc.path">RenderViewDesc.path
<a class="headerlink" href="#RenderViewDesc.path" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderViewDesc" signature="path=(v : Any)"></endpoint>
<signature id="RenderViewDesc.path=">RenderViewDesc.path=(v : Any)
<a class="headerlink" href="#RenderViewDesc.path=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderViewDesc" signature="path(v : Any)"></endpoint>
<signature id="RenderViewDesc.path">RenderViewDesc.path(**v**: `Any`)
<a class="headerlink" href="#RenderViewDesc.path" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderViewDesc" signature="region"></endpoint>
<signature id="RenderViewDesc.region">RenderViewDesc.region
<a class="headerlink" href="#RenderViewDesc.region" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderViewDesc" signature="region=(v : Any)"></endpoint>
<signature id="RenderViewDesc.region=">RenderViewDesc.region=(v : Any)
<a class="headerlink" href="#RenderViewDesc.region=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderViewDesc" signature="region(v : Any)"></endpoint>
<signature id="RenderViewDesc.region">RenderViewDesc.region(**v**: `Any`)
<a class="headerlink" href="#RenderViewDesc.region" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderViewDesc" signature="settings"></endpoint>
<signature id="RenderViewDesc.settings">RenderViewDesc.settings
<a class="headerlink" href="#RenderViewDesc.settings" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderViewDesc" signature="settings=(v : Any)"></endpoint>
<signature id="RenderViewDesc.settings=">RenderViewDesc.settings=(v : Any)
<a class="headerlink" href="#RenderViewDesc.settings=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderViewDesc" signature="settings(v : Any)"></endpoint>
<signature id="RenderViewDesc.settings">RenderViewDesc.settings(**v**: `Any`)
<a class="headerlink" href="#RenderViewDesc.settings" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="RenderViewDesc" signature="new(target_resource : Any, target_path : Any, target_region : Any, target_settings : Any)"></endpoint>
<signature id="RenderViewDesc.new+4">RenderViewDesc.new(**target_resource**: `Any`, **target_path**: `Any`, **target_region**: `Any`, **target_settings**: `Any`)
<a class="headerlink" href="#RenderViewDesc.new+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js RenderViewDesc`
> no docs found   

<endpoint module="luxe: render" class="RenderViewDesc" signature="new()"></endpoint>
<signature id="RenderViewDesc.new">RenderViewDesc.new()
<a class="headerlink" href="#RenderViewDesc.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js RenderViewDesc`
> no docs found   

### SamplerAddressMode
`:::js import "luxe: render" for SamplerAddressMode`
> no docs found

- [clamp_to_edge](#SamplerAddressMode.clamp_to_edge)
- [repeat](#SamplerAddressMode.repeat)
- [mirror_repeat](#SamplerAddressMode.mirror_repeat)
- [from_string](#SamplerAddressMode.from_string)(**value**: `Any`)

<hr/>
<endpoint module="luxe: render" class="SamplerAddressMode" signature="clamp_to_edge"></endpoint>
<signature id="SamplerAddressMode.clamp_to_edge">SamplerAddressMode.clamp_to_edge
<a class="headerlink" href="#SamplerAddressMode.clamp_to_edge" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="SamplerAddressMode" signature="repeat"></endpoint>
<signature id="SamplerAddressMode.repeat">SamplerAddressMode.repeat
<a class="headerlink" href="#SamplerAddressMode.repeat" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="SamplerAddressMode" signature="mirror_repeat"></endpoint>
<signature id="SamplerAddressMode.mirror_repeat">SamplerAddressMode.mirror_repeat
<a class="headerlink" href="#SamplerAddressMode.mirror_repeat" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="SamplerAddressMode" signature="from_string(value : Any)"></endpoint>
<signature id="SamplerAddressMode.from_string">SamplerAddressMode.from_string(**value**: `Any`)
<a class="headerlink" href="#SamplerAddressMode.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### SamplerMinMagFilter
`:::js import "luxe: render" for SamplerMinMagFilter`
> no docs found

- [nearest](#SamplerMinMagFilter.nearest)
- [linear](#SamplerMinMagFilter.linear)
- [from_string](#SamplerMinMagFilter.from_string)(**value**: `Any`)

<hr/>
<endpoint module="luxe: render" class="SamplerMinMagFilter" signature="nearest"></endpoint>
<signature id="SamplerMinMagFilter.nearest">SamplerMinMagFilter.nearest
<a class="headerlink" href="#SamplerMinMagFilter.nearest" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="SamplerMinMagFilter" signature="linear"></endpoint>
<signature id="SamplerMinMagFilter.linear">SamplerMinMagFilter.linear
<a class="headerlink" href="#SamplerMinMagFilter.linear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="SamplerMinMagFilter" signature="from_string(value : Any)"></endpoint>
<signature id="SamplerMinMagFilter.from_string">SamplerMinMagFilter.from_string(**value**: `Any`)
<a class="headerlink" href="#SamplerMinMagFilter.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### SamplerMipFilter
`:::js import "luxe: render" for SamplerMipFilter`
> no docs found

- [none](#SamplerMipFilter.none)
- [nearest](#SamplerMipFilter.nearest)
- [linear](#SamplerMipFilter.linear)
- [from_string](#SamplerMipFilter.from_string)(**value**: `Any`)

<hr/>
<endpoint module="luxe: render" class="SamplerMipFilter" signature="none"></endpoint>
<signature id="SamplerMipFilter.none">SamplerMipFilter.none
<a class="headerlink" href="#SamplerMipFilter.none" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="SamplerMipFilter" signature="nearest"></endpoint>
<signature id="SamplerMipFilter.nearest">SamplerMipFilter.nearest
<a class="headerlink" href="#SamplerMipFilter.nearest" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="SamplerMipFilter" signature="linear"></endpoint>
<signature id="SamplerMipFilter.linear">SamplerMipFilter.linear
<a class="headerlink" href="#SamplerMipFilter.linear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="SamplerMipFilter" signature="from_string(value : Any)"></endpoint>
<signature id="SamplerMipFilter.from_string">SamplerMipFilter.from_string(**value**: `Any`)
<a class="headerlink" href="#SamplerMipFilter.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### SamplerState
`:::js import "luxe: render" for SamplerState`
> no docs found

- [new](#SamplerState.new)()
- [address_r](#SamplerState.address_r)
- [address_r](#SamplerState.address_r=)=(v : Any)
- [address_s](#SamplerState.address_s)
- [address_s](#SamplerState.address_s=)=(v : Any)
- [address_t](#SamplerState.address_t)
- [address_t](#SamplerState.address_t=)=(v : Any)
- [filter_min](#SamplerState.filter_min)
- [filter_min](#SamplerState.filter_min=)=(v : Any)
- [filter_mag](#SamplerState.filter_mag)
- [filter_mag](#SamplerState.filter_mag=)=(v : Any)
- [filter_mip](#SamplerState.filter_mip)
- [filter_mip](#SamplerState.filter_mip=)=(v : Any)

<hr/>
<endpoint module="luxe: render" class="SamplerState" signature="new()"></endpoint>
<signature id="SamplerState.new">SamplerState.new()
<a class="headerlink" href="#SamplerState.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js SamplerState`
> no docs found   

<endpoint module="luxe: render" class="SamplerState" signature="address_r"></endpoint>
<signature id="SamplerState.address_r">SamplerState.address_r
<a class="headerlink" href="#SamplerState.address_r" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="SamplerState" signature="address_r=(v : Any)"></endpoint>
<signature id="SamplerState.address_r=">SamplerState.address_r=(v : Any)
<a class="headerlink" href="#SamplerState.address_r=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="SamplerState" signature="address_s"></endpoint>
<signature id="SamplerState.address_s">SamplerState.address_s
<a class="headerlink" href="#SamplerState.address_s" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="SamplerState" signature="address_s=(v : Any)"></endpoint>
<signature id="SamplerState.address_s=">SamplerState.address_s=(v : Any)
<a class="headerlink" href="#SamplerState.address_s=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="SamplerState" signature="address_t"></endpoint>
<signature id="SamplerState.address_t">SamplerState.address_t
<a class="headerlink" href="#SamplerState.address_t" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="SamplerState" signature="address_t=(v : Any)"></endpoint>
<signature id="SamplerState.address_t=">SamplerState.address_t=(v : Any)
<a class="headerlink" href="#SamplerState.address_t=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="SamplerState" signature="filter_min"></endpoint>
<signature id="SamplerState.filter_min">SamplerState.filter_min
<a class="headerlink" href="#SamplerState.filter_min" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="SamplerState" signature="filter_min=(v : Any)"></endpoint>
<signature id="SamplerState.filter_min=">SamplerState.filter_min=(v : Any)
<a class="headerlink" href="#SamplerState.filter_min=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="SamplerState" signature="filter_mag"></endpoint>
<signature id="SamplerState.filter_mag">SamplerState.filter_mag
<a class="headerlink" href="#SamplerState.filter_mag" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="SamplerState" signature="filter_mag=(v : Any)"></endpoint>
<signature id="SamplerState.filter_mag=">SamplerState.filter_mag=(v : Any)
<a class="headerlink" href="#SamplerState.filter_mag=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="SamplerState" signature="filter_mip"></endpoint>
<signature id="SamplerState.filter_mip">SamplerState.filter_mip
<a class="headerlink" href="#SamplerState.filter_mip" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="SamplerState" signature="filter_mip=(v : Any)"></endpoint>
<signature id="SamplerState.filter_mip=">SamplerState.filter_mip=(v : Any)
<a class="headerlink" href="#SamplerState.filter_mip=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### SortType
`:::js import "luxe: render" for SortType`
> no docs found

- [front_to_back](#SortType.front_to_back)
- [back_to_front](#SortType.back_to_front)
- [sort_by_z](#SortType.sort_by_z)
- [sort_by_z_reverse](#SortType.sort_by_z_reverse)
- [none](#SortType.none)

<hr/>
<endpoint module="luxe: render" class="SortType" signature="front_to_back"></endpoint>
<signature id="SortType.front_to_back">SortType.front_to_back
<a class="headerlink" href="#SortType.front_to_back" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="SortType" signature="back_to_front"></endpoint>
<signature id="SortType.back_to_front">SortType.back_to_front
<a class="headerlink" href="#SortType.back_to_front" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="SortType" signature="sort_by_z"></endpoint>
<signature id="SortType.sort_by_z">SortType.sort_by_z
<a class="headerlink" href="#SortType.sort_by_z" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="SortType" signature="sort_by_z_reverse"></endpoint>
<signature id="SortType.sort_by_z_reverse">SortType.sort_by_z_reverse
<a class="headerlink" href="#SortType.sort_by_z_reverse" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="SortType" signature="none"></endpoint>
<signature id="SortType.none">SortType.none
<a class="headerlink" href="#SortType.none" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### StencilOperation
`:::js import "luxe: render" for StencilOperation`
> no docs found

- [keep](#StencilOperation.keep)
- [zero](#StencilOperation.zero)
- [replace](#StencilOperation.replace)
- [increment_clamp](#StencilOperation.increment_clamp)
- [decrement_clamp](#StencilOperation.decrement_clamp)
- [invert](#StencilOperation.invert)
- [increment_wrap](#StencilOperation.increment_wrap)
- [decrement_wrap](#StencilOperation.decrement_wrap)
- [invalid](#StencilOperation.invalid)
- [from_string](#StencilOperation.from_string)(**value**: `Any`)

<hr/>
<endpoint module="luxe: render" class="StencilOperation" signature="keep"></endpoint>
<signature id="StencilOperation.keep">StencilOperation.keep
<a class="headerlink" href="#StencilOperation.keep" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="StencilOperation" signature="zero"></endpoint>
<signature id="StencilOperation.zero">StencilOperation.zero
<a class="headerlink" href="#StencilOperation.zero" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="StencilOperation" signature="replace"></endpoint>
<signature id="StencilOperation.replace">StencilOperation.replace
<a class="headerlink" href="#StencilOperation.replace" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="StencilOperation" signature="increment_clamp"></endpoint>
<signature id="StencilOperation.increment_clamp">StencilOperation.increment_clamp
<a class="headerlink" href="#StencilOperation.increment_clamp" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="StencilOperation" signature="decrement_clamp"></endpoint>
<signature id="StencilOperation.decrement_clamp">StencilOperation.decrement_clamp
<a class="headerlink" href="#StencilOperation.decrement_clamp" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="StencilOperation" signature="invert"></endpoint>
<signature id="StencilOperation.invert">StencilOperation.invert
<a class="headerlink" href="#StencilOperation.invert" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="StencilOperation" signature="increment_wrap"></endpoint>
<signature id="StencilOperation.increment_wrap">StencilOperation.increment_wrap
<a class="headerlink" href="#StencilOperation.increment_wrap" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="StencilOperation" signature="decrement_wrap"></endpoint>
<signature id="StencilOperation.decrement_wrap">StencilOperation.decrement_wrap
<a class="headerlink" href="#StencilOperation.decrement_wrap" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="StencilOperation" signature="invalid"></endpoint>
<signature id="StencilOperation.invalid">StencilOperation.invalid
<a class="headerlink" href="#StencilOperation.invalid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="StencilOperation" signature="from_string(value : Any)"></endpoint>
<signature id="StencilOperation.from_string">StencilOperation.from_string(**value**: `Any`)
<a class="headerlink" href="#StencilOperation.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### StoreAction
`:::js import "luxe: render" for StoreAction`
> no docs found

- [dont_care](#StoreAction.dont_care)
- [store](#StoreAction.store)

<hr/>
<endpoint module="luxe: render" class="StoreAction" signature="dont_care"></endpoint>
<signature id="StoreAction.dont_care">StoreAction.dont_care
<a class="headerlink" href="#StoreAction.dont_care" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="StoreAction" signature="store"></endpoint>
<signature id="StoreAction.store">StoreAction.store
<a class="headerlink" href="#StoreAction.store" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### TextAlign
`:::js import "luxe: render" for TextAlign`
> no docs found

- [left](#TextAlign.left)
- [center](#TextAlign.center)
- [right](#TextAlign.right)
- [top](#TextAlign.top)
- [bottom](#TextAlign.bottom)
- [from_string](#TextAlign.from_string)(**value**: `Any`)
- [name](#TextAlign.name)(**value**: `Any`)

<hr/>
<endpoint module="luxe: render" class="TextAlign" signature="left"></endpoint>
<signature id="TextAlign.left">TextAlign.left
<a class="headerlink" href="#TextAlign.left" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="TextAlign" signature="center"></endpoint>
<signature id="TextAlign.center">TextAlign.center
<a class="headerlink" href="#TextAlign.center" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="TextAlign" signature="right"></endpoint>
<signature id="TextAlign.right">TextAlign.right
<a class="headerlink" href="#TextAlign.right" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="TextAlign" signature="top"></endpoint>
<signature id="TextAlign.top">TextAlign.top
<a class="headerlink" href="#TextAlign.top" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="TextAlign" signature="bottom"></endpoint>
<signature id="TextAlign.bottom">TextAlign.bottom
<a class="headerlink" href="#TextAlign.bottom" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="TextAlign" signature="from_string(value : Any)"></endpoint>
<signature id="TextAlign.from_string">TextAlign.from_string(**value**: `Any`)
<a class="headerlink" href="#TextAlign.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="TextAlign" signature="name(value : Any)"></endpoint>
<signature id="TextAlign.name">TextAlign.name(**value**: `Any`)
<a class="headerlink" href="#TextAlign.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### TextAttrType
`:::js import "luxe: render" for TextAttrType`
> no docs found

- [unknown](#TextAttrType.unknown)
- [handle32](#TextAttrType.handle32)
- [handle64](#TextAttrType.handle64)
- [number](#TextAttrType.number)
- [string](#TextAttrType.string)
- [color](#TextAttrType.color)
- [float2](#TextAttrType.float2)
- [name](#TextAttrType.name)(**value**: `Any`)

<hr/>
<endpoint module="luxe: render" class="TextAttrType" signature="unknown"></endpoint>
<signature id="TextAttrType.unknown">TextAttrType.unknown
<a class="headerlink" href="#TextAttrType.unknown" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="TextAttrType" signature="handle32"></endpoint>
<signature id="TextAttrType.handle32">TextAttrType.handle32
<a class="headerlink" href="#TextAttrType.handle32" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="TextAttrType" signature="handle64"></endpoint>
<signature id="TextAttrType.handle64">TextAttrType.handle64
<a class="headerlink" href="#TextAttrType.handle64" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="TextAttrType" signature="number"></endpoint>
<signature id="TextAttrType.number">TextAttrType.number
<a class="headerlink" href="#TextAttrType.number" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="TextAttrType" signature="string"></endpoint>
<signature id="TextAttrType.string">TextAttrType.string
<a class="headerlink" href="#TextAttrType.string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="TextAttrType" signature="color"></endpoint>
<signature id="TextAttrType.color">TextAttrType.color
<a class="headerlink" href="#TextAttrType.color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="TextAttrType" signature="float2"></endpoint>
<signature id="TextAttrType.float2">TextAttrType.float2
<a class="headerlink" href="#TextAttrType.float2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="TextAttrType" signature="name(value : Any)"></endpoint>
<signature id="TextAttrType.name">TextAttrType.name(**value**: `Any`)
<a class="headerlink" href="#TextAttrType.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### TextWrapMode
`:::js import "luxe: render" for TextWrapMode`
> no docs found

- [unknown](#TextWrapMode.unknown)
- [none](#TextWrapMode.none)
- [word](#TextWrapMode.word)
- [from_string](#TextWrapMode.from_string)(**value**: `Any`)
- [name](#TextWrapMode.name)(**value**: `Any`)

<hr/>
<endpoint module="luxe: render" class="TextWrapMode" signature="unknown"></endpoint>
<signature id="TextWrapMode.unknown">TextWrapMode.unknown
<a class="headerlink" href="#TextWrapMode.unknown" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="TextWrapMode" signature="none"></endpoint>
<signature id="TextWrapMode.none">TextWrapMode.none
<a class="headerlink" href="#TextWrapMode.none" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="TextWrapMode" signature="word"></endpoint>
<signature id="TextWrapMode.word">TextWrapMode.word
<a class="headerlink" href="#TextWrapMode.word" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="TextWrapMode" signature="from_string(value : Any)"></endpoint>
<signature id="TextWrapMode.from_string">TextWrapMode.from_string(**value**: `Any`)
<a class="headerlink" href="#TextWrapMode.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="TextWrapMode" signature="name(value : Any)"></endpoint>
<signature id="TextWrapMode.name">TextWrapMode.name(**value**: `Any`)
<a class="headerlink" href="#TextWrapMode.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### VertexAttr
`:::js import "luxe: render" for VertexAttr`
> no docs found

- [new](#VertexAttr.new)(**name**: `Any`)
- [name](#VertexAttr.name)
- [name](#VertexAttr.name=)=(v : Any)
- [format](#VertexAttr.format)
- [format](#VertexAttr.format=)=(v : Any)
- [offset](#VertexAttr.offset)
- [offset](#VertexAttr.offset=)=(v : Any)
- [buffer_index](#VertexAttr.buffer_index)
- [buffer_index](#VertexAttr.buffer_index=)=(v : Any)

<hr/>
<endpoint module="luxe: render" class="VertexAttr" signature="new(name : Any)"></endpoint>
<signature id="VertexAttr.new">VertexAttr.new(**name**: `Any`)
<a class="headerlink" href="#VertexAttr.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js VertexAttr`
> no docs found   

<endpoint module="luxe: render" class="VertexAttr" signature="name"></endpoint>
<signature id="VertexAttr.name">VertexAttr.name
<a class="headerlink" href="#VertexAttr.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttr" signature="name=(v : Any)"></endpoint>
<signature id="VertexAttr.name=">VertexAttr.name=(v : Any)
<a class="headerlink" href="#VertexAttr.name=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttr" signature="format"></endpoint>
<signature id="VertexAttr.format">VertexAttr.format
<a class="headerlink" href="#VertexAttr.format" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttr" signature="format=(v : Any)"></endpoint>
<signature id="VertexAttr.format=">VertexAttr.format=(v : Any)
<a class="headerlink" href="#VertexAttr.format=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttr" signature="offset"></endpoint>
<signature id="VertexAttr.offset">VertexAttr.offset
<a class="headerlink" href="#VertexAttr.offset" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttr" signature="offset=(v : Any)"></endpoint>
<signature id="VertexAttr.offset=">VertexAttr.offset=(v : Any)
<a class="headerlink" href="#VertexAttr.offset=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttr" signature="buffer_index"></endpoint>
<signature id="VertexAttr.buffer_index">VertexAttr.buffer_index
<a class="headerlink" href="#VertexAttr.buffer_index" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttr" signature="buffer_index=(v : Any)"></endpoint>
<signature id="VertexAttr.buffer_index=">VertexAttr.buffer_index=(v : Any)
<a class="headerlink" href="#VertexAttr.buffer_index=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### VertexAttrFormat
`:::js import "luxe: render" for VertexAttrFormat`
> no docs found

- [invalid](#VertexAttrFormat.invalid)
- [bool](#VertexAttrFormat.bool)
- [bool2](#VertexAttrFormat.bool2)
- [bool3](#VertexAttrFormat.bool3)
- [bool4](#VertexAttrFormat.bool4)
- [int](#VertexAttrFormat.int)
- [int2](#VertexAttrFormat.int2)
- [int3](#VertexAttrFormat.int3)
- [int4](#VertexAttrFormat.int4)
- [uint](#VertexAttrFormat.uint)
- [uint2](#VertexAttrFormat.uint2)
- [uint3](#VertexAttrFormat.uint3)
- [uint4](#VertexAttrFormat.uint4)
- [float](#VertexAttrFormat.float)
- [float2](#VertexAttrFormat.float2)
- [float3](#VertexAttrFormat.float3)
- [float4](#VertexAttrFormat.float4)
- [double](#VertexAttrFormat.double)
- [double2](#VertexAttrFormat.double2)
- [double3](#VertexAttrFormat.double3)
- [double4](#VertexAttrFormat.double4)
- [mat4](#VertexAttrFormat.mat4)
- [from_string](#VertexAttrFormat.from_string)(**value**: `Any`)
- [size_of](#VertexAttrFormat.size_of)(**value**: `Any`)

<hr/>
<endpoint module="luxe: render" class="VertexAttrFormat" signature="invalid"></endpoint>
<signature id="VertexAttrFormat.invalid">VertexAttrFormat.invalid
<a class="headerlink" href="#VertexAttrFormat.invalid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttrFormat" signature="bool"></endpoint>
<signature id="VertexAttrFormat.bool">VertexAttrFormat.bool
<a class="headerlink" href="#VertexAttrFormat.bool" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttrFormat" signature="bool2"></endpoint>
<signature id="VertexAttrFormat.bool2">VertexAttrFormat.bool2
<a class="headerlink" href="#VertexAttrFormat.bool2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttrFormat" signature="bool3"></endpoint>
<signature id="VertexAttrFormat.bool3">VertexAttrFormat.bool3
<a class="headerlink" href="#VertexAttrFormat.bool3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttrFormat" signature="bool4"></endpoint>
<signature id="VertexAttrFormat.bool4">VertexAttrFormat.bool4
<a class="headerlink" href="#VertexAttrFormat.bool4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttrFormat" signature="int"></endpoint>
<signature id="VertexAttrFormat.int">VertexAttrFormat.int
<a class="headerlink" href="#VertexAttrFormat.int" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttrFormat" signature="int2"></endpoint>
<signature id="VertexAttrFormat.int2">VertexAttrFormat.int2
<a class="headerlink" href="#VertexAttrFormat.int2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttrFormat" signature="int3"></endpoint>
<signature id="VertexAttrFormat.int3">VertexAttrFormat.int3
<a class="headerlink" href="#VertexAttrFormat.int3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttrFormat" signature="int4"></endpoint>
<signature id="VertexAttrFormat.int4">VertexAttrFormat.int4
<a class="headerlink" href="#VertexAttrFormat.int4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttrFormat" signature="uint"></endpoint>
<signature id="VertexAttrFormat.uint">VertexAttrFormat.uint
<a class="headerlink" href="#VertexAttrFormat.uint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttrFormat" signature="uint2"></endpoint>
<signature id="VertexAttrFormat.uint2">VertexAttrFormat.uint2
<a class="headerlink" href="#VertexAttrFormat.uint2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttrFormat" signature="uint3"></endpoint>
<signature id="VertexAttrFormat.uint3">VertexAttrFormat.uint3
<a class="headerlink" href="#VertexAttrFormat.uint3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttrFormat" signature="uint4"></endpoint>
<signature id="VertexAttrFormat.uint4">VertexAttrFormat.uint4
<a class="headerlink" href="#VertexAttrFormat.uint4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttrFormat" signature="float"></endpoint>
<signature id="VertexAttrFormat.float">VertexAttrFormat.float
<a class="headerlink" href="#VertexAttrFormat.float" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttrFormat" signature="float2"></endpoint>
<signature id="VertexAttrFormat.float2">VertexAttrFormat.float2
<a class="headerlink" href="#VertexAttrFormat.float2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttrFormat" signature="float3"></endpoint>
<signature id="VertexAttrFormat.float3">VertexAttrFormat.float3
<a class="headerlink" href="#VertexAttrFormat.float3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttrFormat" signature="float4"></endpoint>
<signature id="VertexAttrFormat.float4">VertexAttrFormat.float4
<a class="headerlink" href="#VertexAttrFormat.float4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttrFormat" signature="double"></endpoint>
<signature id="VertexAttrFormat.double">VertexAttrFormat.double
<a class="headerlink" href="#VertexAttrFormat.double" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttrFormat" signature="double2"></endpoint>
<signature id="VertexAttrFormat.double2">VertexAttrFormat.double2
<a class="headerlink" href="#VertexAttrFormat.double2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttrFormat" signature="double3"></endpoint>
<signature id="VertexAttrFormat.double3">VertexAttrFormat.double3
<a class="headerlink" href="#VertexAttrFormat.double3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttrFormat" signature="double4"></endpoint>
<signature id="VertexAttrFormat.double4">VertexAttrFormat.double4
<a class="headerlink" href="#VertexAttrFormat.double4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttrFormat" signature="mat4"></endpoint>
<signature id="VertexAttrFormat.mat4">VertexAttrFormat.mat4
<a class="headerlink" href="#VertexAttrFormat.mat4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttrFormat" signature="from_string(value : Any)"></endpoint>
<signature id="VertexAttrFormat.from_string">VertexAttrFormat.from_string(**value**: `Any`)
<a class="headerlink" href="#VertexAttrFormat.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexAttrFormat" signature="size_of(value : Any)"></endpoint>
<signature id="VertexAttrFormat.size_of">VertexAttrFormat.size_of(**value**: `Any`)
<a class="headerlink" href="#VertexAttrFormat.size_of" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### VertexFormat
`:::js import "luxe: render" for VertexFormat`
> no docs found

- [new](#VertexFormat.new)()
- [attributes](#VertexFormat.attributes)
- [attributes](#VertexFormat.attributes=)=(v : Any)
- [layouts](#VertexFormat.layouts)
- [layouts](#VertexFormat.layouts=)=(v : Any)

<hr/>
<endpoint module="luxe: render" class="VertexFormat" signature="new()"></endpoint>
<signature id="VertexFormat.new">VertexFormat.new()
<a class="headerlink" href="#VertexFormat.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js VertexFormat`
> no docs found   

<endpoint module="luxe: render" class="VertexFormat" signature="attributes"></endpoint>
<signature id="VertexFormat.attributes">VertexFormat.attributes
<a class="headerlink" href="#VertexFormat.attributes" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexFormat" signature="attributes=(v : Any)"></endpoint>
<signature id="VertexFormat.attributes=">VertexFormat.attributes=(v : Any)
<a class="headerlink" href="#VertexFormat.attributes=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexFormat" signature="layouts"></endpoint>
<signature id="VertexFormat.layouts">VertexFormat.layouts
<a class="headerlink" href="#VertexFormat.layouts" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexFormat" signature="layouts=(v : Any)"></endpoint>
<signature id="VertexFormat.layouts=">VertexFormat.layouts=(v : Any)
<a class="headerlink" href="#VertexFormat.layouts=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### VertexInputRate
`:::js import "luxe: render" for VertexInputRate`
> no docs found

- [vertex](#VertexInputRate.vertex)
- [instance](#VertexInputRate.instance)
- [from_string](#VertexInputRate.from_string)(**value**: `Any`)

<hr/>
<endpoint module="luxe: render" class="VertexInputRate" signature="vertex"></endpoint>
<signature id="VertexInputRate.vertex">VertexInputRate.vertex
<a class="headerlink" href="#VertexInputRate.vertex" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexInputRate" signature="instance"></endpoint>
<signature id="VertexInputRate.instance">VertexInputRate.instance
<a class="headerlink" href="#VertexInputRate.instance" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexInputRate" signature="from_string(value : Any)"></endpoint>
<signature id="VertexInputRate.from_string">VertexInputRate.from_string(**value**: `Any`)
<a class="headerlink" href="#VertexInputRate.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### VertexLayout
`:::js import "luxe: render" for VertexLayout`
> no docs found

- [new](#VertexLayout.new)()
- [stride](#VertexLayout.stride)
- [stride](#VertexLayout.stride=)=(v : Any)

<hr/>
<endpoint module="luxe: render" class="VertexLayout" signature="new()"></endpoint>
<signature id="VertexLayout.new">VertexLayout.new()
<a class="headerlink" href="#VertexLayout.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js VertexLayout`
> no docs found   

<endpoint module="luxe: render" class="VertexLayout" signature="stride"></endpoint>
<signature id="VertexLayout.stride">VertexLayout.stride
<a class="headerlink" href="#VertexLayout.stride" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="VertexLayout" signature="stride=(v : Any)"></endpoint>
<signature id="VertexLayout.stride=">VertexLayout.stride=(v : Any)
<a class="headerlink" href="#VertexLayout.stride=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Winding
`:::js import "luxe: render" for Winding`
> no docs found

- [clockwise](#Winding.clockwise)
- [counter_clockwise](#Winding.counter_clockwise)
- [from_string](#Winding.from_string)(**value**: `Any`)

<hr/>
<endpoint module="luxe: render" class="Winding" signature="clockwise"></endpoint>
<signature id="Winding.clockwise">Winding.clockwise
<a class="headerlink" href="#Winding.clockwise" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Winding" signature="counter_clockwise"></endpoint>
<signature id="Winding.counter_clockwise">Winding.counter_clockwise
<a class="headerlink" href="#Winding.counter_clockwise" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: render" class="Winding" signature="from_string(value : Any)"></endpoint>
<signature id="Winding.from_string">Winding.from_string(**value**: `Any`)
<a class="headerlink" href="#Winding.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

