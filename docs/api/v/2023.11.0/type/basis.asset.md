#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.11.0`)  


---

## `luxe: type/basis.asset` module

- [Asset](#asset)   
- [Basis](#basis)   
- [BasisBlendFactor](#basisblendfactor)   
- [BasisBlendOperation](#basisblendoperation)   
- [BasisBlending](#basisblending)   
- [BasisCompareFunction](#basiscomparefunction)   
- [BasisCullMode](#basiscullmode)   
- [BasisDepth](#basisdepth)   
- [BasisInput](#basisinput)   
- [BasisInputField](#basisinputfield)   
- [BasisInputType](#basisinputtype)   
- [BasisReplace](#basisreplace)   
- [BasisShaderFunction](#basisshaderfunction)   
- [BasisShaders](#basisshaders)   
- [BasisStencil](#basisstencil)   
- [BasisStencilDesc](#basisstencildesc)   
- [BasisStencilOperation](#basisstenciloperation)   
- [BasisWinding](#basiswinding)   
- [BasisWriteMask](#basiswritemask)   

---

### Asset
`:::js import "luxe: type/basis.asset" for Asset`
> no docs found

- [subtype](#Asset.subtype)
- [new](#Asset.new+2)(**type_id**: `String`, **ctx**: `AssetContext`)
- [pre](#Asset.pre)(**assets**: `List`)
- [process](#Asset.process+2)(**assets**: `List`, **each**: `Fn`)

<hr/>
<endpoint module="luxe: type/basis.asset" class="Asset" signature="subtype"></endpoint>
<signature id="Asset.subtype">Asset.subtype
<a class="headerlink" href="#Asset.subtype" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="Asset" signature="new(type_id : String, ctx : AssetContext)"></endpoint>
<signature id="Asset.new+2">Asset.new(**type_id**: `String`, **ctx**: `AssetContext`)
<a class="headerlink" href="#Asset.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Asset`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="Asset" signature="pre(assets : List)"></endpoint>
<signature id="Asset.pre">Asset.pre(**assets**: `List`)
<a class="headerlink" href="#Asset.pre" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="Asset" signature="process(assets : List, each : Fn)"></endpoint>
<signature id="Asset.process+2">Asset.process(**assets**: `List`, **each**: `Fn`)
<a class="headerlink" href="#Asset.process+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Basis
`:::js import "luxe: type/basis.asset" for Basis`
> no docs found


<hr/>
### BasisBlendFactor
`:::js import "luxe: type/basis.asset" for BasisBlendFactor`
> no docs found

- [zero](#BasisBlendFactor.zero)
- [one](#BasisBlendFactor.one)
- [source_color](#BasisBlendFactor.source_color)
- [one_minus_source_color](#BasisBlendFactor.one_minus_source_color)
- [source_alpha](#BasisBlendFactor.source_alpha)
- [one_minus_source_alpha](#BasisBlendFactor.one_minus_source_alpha)
- [destination_color](#BasisBlendFactor.destination_color)
- [one_minus_destination_color](#BasisBlendFactor.one_minus_destination_color)
- [destination_alpha](#BasisBlendFactor.destination_alpha)
- [one_minus_destination_alpha](#BasisBlendFactor.one_minus_destination_alpha)
- [source_alpha_saturated](#BasisBlendFactor.source_alpha_saturated)
- [blend_color](#BasisBlendFactor.blend_color)
- [one_minus_blend_color](#BasisBlendFactor.one_minus_blend_color)
- [blend_alpha](#BasisBlendFactor.blend_alpha)
- [one_minus_blend_alpha](#BasisBlendFactor.one_minus_blend_alpha)
- [invalid](#BasisBlendFactor.invalid)

<hr/>
<endpoint module="luxe: type/basis.asset" class="BasisBlendFactor" signature="zero"></endpoint>
<signature id="BasisBlendFactor.zero">BasisBlendFactor.zero
<a class="headerlink" href="#BasisBlendFactor.zero" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisBlendFactor" signature="one"></endpoint>
<signature id="BasisBlendFactor.one">BasisBlendFactor.one
<a class="headerlink" href="#BasisBlendFactor.one" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisBlendFactor" signature="source_color"></endpoint>
<signature id="BasisBlendFactor.source_color">BasisBlendFactor.source_color
<a class="headerlink" href="#BasisBlendFactor.source_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisBlendFactor" signature="one_minus_source_color"></endpoint>
<signature id="BasisBlendFactor.one_minus_source_color">BasisBlendFactor.one_minus_source_color
<a class="headerlink" href="#BasisBlendFactor.one_minus_source_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisBlendFactor" signature="source_alpha"></endpoint>
<signature id="BasisBlendFactor.source_alpha">BasisBlendFactor.source_alpha
<a class="headerlink" href="#BasisBlendFactor.source_alpha" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisBlendFactor" signature="one_minus_source_alpha"></endpoint>
<signature id="BasisBlendFactor.one_minus_source_alpha">BasisBlendFactor.one_minus_source_alpha
<a class="headerlink" href="#BasisBlendFactor.one_minus_source_alpha" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisBlendFactor" signature="destination_color"></endpoint>
<signature id="BasisBlendFactor.destination_color">BasisBlendFactor.destination_color
<a class="headerlink" href="#BasisBlendFactor.destination_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisBlendFactor" signature="one_minus_destination_color"></endpoint>
<signature id="BasisBlendFactor.one_minus_destination_color">BasisBlendFactor.one_minus_destination_color
<a class="headerlink" href="#BasisBlendFactor.one_minus_destination_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisBlendFactor" signature="destination_alpha"></endpoint>
<signature id="BasisBlendFactor.destination_alpha">BasisBlendFactor.destination_alpha
<a class="headerlink" href="#BasisBlendFactor.destination_alpha" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisBlendFactor" signature="one_minus_destination_alpha"></endpoint>
<signature id="BasisBlendFactor.one_minus_destination_alpha">BasisBlendFactor.one_minus_destination_alpha
<a class="headerlink" href="#BasisBlendFactor.one_minus_destination_alpha" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisBlendFactor" signature="source_alpha_saturated"></endpoint>
<signature id="BasisBlendFactor.source_alpha_saturated">BasisBlendFactor.source_alpha_saturated
<a class="headerlink" href="#BasisBlendFactor.source_alpha_saturated" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisBlendFactor" signature="blend_color"></endpoint>
<signature id="BasisBlendFactor.blend_color">BasisBlendFactor.blend_color
<a class="headerlink" href="#BasisBlendFactor.blend_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisBlendFactor" signature="one_minus_blend_color"></endpoint>
<signature id="BasisBlendFactor.one_minus_blend_color">BasisBlendFactor.one_minus_blend_color
<a class="headerlink" href="#BasisBlendFactor.one_minus_blend_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisBlendFactor" signature="blend_alpha"></endpoint>
<signature id="BasisBlendFactor.blend_alpha">BasisBlendFactor.blend_alpha
<a class="headerlink" href="#BasisBlendFactor.blend_alpha" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisBlendFactor" signature="one_minus_blend_alpha"></endpoint>
<signature id="BasisBlendFactor.one_minus_blend_alpha">BasisBlendFactor.one_minus_blend_alpha
<a class="headerlink" href="#BasisBlendFactor.one_minus_blend_alpha" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisBlendFactor" signature="invalid"></endpoint>
<signature id="BasisBlendFactor.invalid">BasisBlendFactor.invalid
<a class="headerlink" href="#BasisBlendFactor.invalid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### BasisBlendOperation
`:::js import "luxe: type/basis.asset" for BasisBlendOperation`
> no docs found

- [add](#BasisBlendOperation.add)
- [subtract](#BasisBlendOperation.subtract)
- [reverse_subtract](#BasisBlendOperation.reverse_subtract)
- [min](#BasisBlendOperation.min)
- [max](#BasisBlendOperation.max)

<hr/>
<endpoint module="luxe: type/basis.asset" class="BasisBlendOperation" signature="add"></endpoint>
<signature id="BasisBlendOperation.add">BasisBlendOperation.add
<a class="headerlink" href="#BasisBlendOperation.add" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisBlendOperation" signature="subtract"></endpoint>
<signature id="BasisBlendOperation.subtract">BasisBlendOperation.subtract
<a class="headerlink" href="#BasisBlendOperation.subtract" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisBlendOperation" signature="reverse_subtract"></endpoint>
<signature id="BasisBlendOperation.reverse_subtract">BasisBlendOperation.reverse_subtract
<a class="headerlink" href="#BasisBlendOperation.reverse_subtract" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisBlendOperation" signature="min"></endpoint>
<signature id="BasisBlendOperation.min">BasisBlendOperation.min
<a class="headerlink" href="#BasisBlendOperation.min" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisBlendOperation" signature="max"></endpoint>
<signature id="BasisBlendOperation.max">BasisBlendOperation.max
<a class="headerlink" href="#BasisBlendOperation.max" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### BasisBlending
`:::js import "luxe: type/basis.asset" for BasisBlending`
> no docs found


<hr/>
### BasisCompareFunction
`:::js import "luxe: type/basis.asset" for BasisCompareFunction`
> no docs found

- [never](#BasisCompareFunction.never)
- [less](#BasisCompareFunction.less)
- [equal](#BasisCompareFunction.equal)
- [less_equal](#BasisCompareFunction.less_equal)
- [greater](#BasisCompareFunction.greater)
- [not_equal](#BasisCompareFunction.not_equal)
- [greater_equal](#BasisCompareFunction.greater_equal)
- [always](#BasisCompareFunction.always)

<hr/>
<endpoint module="luxe: type/basis.asset" class="BasisCompareFunction" signature="never"></endpoint>
<signature id="BasisCompareFunction.never">BasisCompareFunction.never
<a class="headerlink" href="#BasisCompareFunction.never" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisCompareFunction" signature="less"></endpoint>
<signature id="BasisCompareFunction.less">BasisCompareFunction.less
<a class="headerlink" href="#BasisCompareFunction.less" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisCompareFunction" signature="equal"></endpoint>
<signature id="BasisCompareFunction.equal">BasisCompareFunction.equal
<a class="headerlink" href="#BasisCompareFunction.equal" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisCompareFunction" signature="less_equal"></endpoint>
<signature id="BasisCompareFunction.less_equal">BasisCompareFunction.less_equal
<a class="headerlink" href="#BasisCompareFunction.less_equal" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisCompareFunction" signature="greater"></endpoint>
<signature id="BasisCompareFunction.greater">BasisCompareFunction.greater
<a class="headerlink" href="#BasisCompareFunction.greater" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisCompareFunction" signature="not_equal"></endpoint>
<signature id="BasisCompareFunction.not_equal">BasisCompareFunction.not_equal
<a class="headerlink" href="#BasisCompareFunction.not_equal" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisCompareFunction" signature="greater_equal"></endpoint>
<signature id="BasisCompareFunction.greater_equal">BasisCompareFunction.greater_equal
<a class="headerlink" href="#BasisCompareFunction.greater_equal" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisCompareFunction" signature="always"></endpoint>
<signature id="BasisCompareFunction.always">BasisCompareFunction.always
<a class="headerlink" href="#BasisCompareFunction.always" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### BasisCullMode
`:::js import "luxe: type/basis.asset" for BasisCullMode`
> no docs found

- [none](#BasisCullMode.none)
- [front](#BasisCullMode.front)
- [back](#BasisCullMode.back)

<hr/>
<endpoint module="luxe: type/basis.asset" class="BasisCullMode" signature="none"></endpoint>
<signature id="BasisCullMode.none">BasisCullMode.none
<a class="headerlink" href="#BasisCullMode.none" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisCullMode" signature="front"></endpoint>
<signature id="BasisCullMode.front">BasisCullMode.front
<a class="headerlink" href="#BasisCullMode.front" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisCullMode" signature="back"></endpoint>
<signature id="BasisCullMode.back">BasisCullMode.back
<a class="headerlink" href="#BasisCullMode.back" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### BasisDepth
`:::js import "luxe: type/basis.asset" for BasisDepth`
> no docs found


<hr/>
### BasisInput
`:::js import "luxe: type/basis.asset" for BasisInput`
> no docs found


<hr/>
### BasisInputField
`:::js import "luxe: type/basis.asset" for BasisInputField`
> no docs found


<hr/>
### BasisInputType
`:::js import "luxe: type/basis.asset" for BasisInputType`
> no docs found

- [image](#BasisInputType.image)
- [image_array](#BasisInputType.image_array)
- [float](#BasisInputType.float)
- [float_array](#BasisInputType.float_array)
- [float2](#BasisInputType.float2)
- [float2_array](#BasisInputType.float2_array)
- [float3](#BasisInputType.float3)
- [float3_array](#BasisInputType.float3_array)
- [float4](#BasisInputType.float4)
- [float4_array](#BasisInputType.float4_array)
- [mat4](#BasisInputType.mat4)
- [mat4_array](#BasisInputType.mat4_array)
- [int](#BasisInputType.int)
- [int_array](#BasisInputType.int_array)
- [int2](#BasisInputType.int2)
- [int2_array](#BasisInputType.int2_array)
- [int3](#BasisInputType.int3)
- [int3_array](#BasisInputType.int3_array)
- [int4](#BasisInputType.int4)
- [int4_array](#BasisInputType.int4_array)
- [uint](#BasisInputType.uint)
- [uint_array](#BasisInputType.uint_array)
- [uint2](#BasisInputType.uint2)
- [uint2_array](#BasisInputType.uint2_array)
- [uint3](#BasisInputType.uint3)
- [uint3_array](#BasisInputType.uint3_array)
- [uint4](#BasisInputType.uint4)
- [uint4_array](#BasisInputType.uint4_array)

<hr/>
<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="image"></endpoint>
<signature id="BasisInputType.image">BasisInputType.image
<a class="headerlink" href="#BasisInputType.image" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="image_array"></endpoint>
<signature id="BasisInputType.image_array">BasisInputType.image_array
<a class="headerlink" href="#BasisInputType.image_array" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="float"></endpoint>
<signature id="BasisInputType.float">BasisInputType.float
<a class="headerlink" href="#BasisInputType.float" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="float_array"></endpoint>
<signature id="BasisInputType.float_array">BasisInputType.float_array
<a class="headerlink" href="#BasisInputType.float_array" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="float2"></endpoint>
<signature id="BasisInputType.float2">BasisInputType.float2
<a class="headerlink" href="#BasisInputType.float2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="float2_array"></endpoint>
<signature id="BasisInputType.float2_array">BasisInputType.float2_array
<a class="headerlink" href="#BasisInputType.float2_array" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="float3"></endpoint>
<signature id="BasisInputType.float3">BasisInputType.float3
<a class="headerlink" href="#BasisInputType.float3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="float3_array"></endpoint>
<signature id="BasisInputType.float3_array">BasisInputType.float3_array
<a class="headerlink" href="#BasisInputType.float3_array" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="float4"></endpoint>
<signature id="BasisInputType.float4">BasisInputType.float4
<a class="headerlink" href="#BasisInputType.float4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="float4_array"></endpoint>
<signature id="BasisInputType.float4_array">BasisInputType.float4_array
<a class="headerlink" href="#BasisInputType.float4_array" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="mat4"></endpoint>
<signature id="BasisInputType.mat4">BasisInputType.mat4
<a class="headerlink" href="#BasisInputType.mat4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="mat4_array"></endpoint>
<signature id="BasisInputType.mat4_array">BasisInputType.mat4_array
<a class="headerlink" href="#BasisInputType.mat4_array" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="int"></endpoint>
<signature id="BasisInputType.int">BasisInputType.int
<a class="headerlink" href="#BasisInputType.int" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="int_array"></endpoint>
<signature id="BasisInputType.int_array">BasisInputType.int_array
<a class="headerlink" href="#BasisInputType.int_array" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="int2"></endpoint>
<signature id="BasisInputType.int2">BasisInputType.int2
<a class="headerlink" href="#BasisInputType.int2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="int2_array"></endpoint>
<signature id="BasisInputType.int2_array">BasisInputType.int2_array
<a class="headerlink" href="#BasisInputType.int2_array" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="int3"></endpoint>
<signature id="BasisInputType.int3">BasisInputType.int3
<a class="headerlink" href="#BasisInputType.int3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="int3_array"></endpoint>
<signature id="BasisInputType.int3_array">BasisInputType.int3_array
<a class="headerlink" href="#BasisInputType.int3_array" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="int4"></endpoint>
<signature id="BasisInputType.int4">BasisInputType.int4
<a class="headerlink" href="#BasisInputType.int4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="int4_array"></endpoint>
<signature id="BasisInputType.int4_array">BasisInputType.int4_array
<a class="headerlink" href="#BasisInputType.int4_array" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="uint"></endpoint>
<signature id="BasisInputType.uint">BasisInputType.uint
<a class="headerlink" href="#BasisInputType.uint" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="uint_array"></endpoint>
<signature id="BasisInputType.uint_array">BasisInputType.uint_array
<a class="headerlink" href="#BasisInputType.uint_array" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="uint2"></endpoint>
<signature id="BasisInputType.uint2">BasisInputType.uint2
<a class="headerlink" href="#BasisInputType.uint2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="uint2_array"></endpoint>
<signature id="BasisInputType.uint2_array">BasisInputType.uint2_array
<a class="headerlink" href="#BasisInputType.uint2_array" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="uint3"></endpoint>
<signature id="BasisInputType.uint3">BasisInputType.uint3
<a class="headerlink" href="#BasisInputType.uint3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="uint3_array"></endpoint>
<signature id="BasisInputType.uint3_array">BasisInputType.uint3_array
<a class="headerlink" href="#BasisInputType.uint3_array" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="uint4"></endpoint>
<signature id="BasisInputType.uint4">BasisInputType.uint4
<a class="headerlink" href="#BasisInputType.uint4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisInputType" signature="uint4_array"></endpoint>
<signature id="BasisInputType.uint4_array">BasisInputType.uint4_array
<a class="headerlink" href="#BasisInputType.uint4_array" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### BasisReplace
`:::js import "luxe: type/basis.asset" for BasisReplace`
> no docs found


<hr/>
### BasisShaderFunction
`:::js import "luxe: type/basis.asset" for BasisShaderFunction`
> no docs found


<hr/>
### BasisShaders
`:::js import "luxe: type/basis.asset" for BasisShaders`
> no docs found


<hr/>
### BasisStencil
`:::js import "luxe: type/basis.asset" for BasisStencil`
> no docs found


<hr/>
### BasisStencilDesc
`:::js import "luxe: type/basis.asset" for BasisStencilDesc`
> no docs found


<hr/>
### BasisStencilOperation
`:::js import "luxe: type/basis.asset" for BasisStencilOperation`
> no docs found

- [keep](#BasisStencilOperation.keep)
- [zero](#BasisStencilOperation.zero)
- [replace](#BasisStencilOperation.replace)
- [increment_clamp](#BasisStencilOperation.increment_clamp)
- [decrement_clamp](#BasisStencilOperation.decrement_clamp)
- [invert](#BasisStencilOperation.invert)
- [increment_wrap](#BasisStencilOperation.increment_wrap)
- [decrement_wrap](#BasisStencilOperation.decrement_wrap)
- [invalid](#BasisStencilOperation.invalid)

<hr/>
<endpoint module="luxe: type/basis.asset" class="BasisStencilOperation" signature="keep"></endpoint>
<signature id="BasisStencilOperation.keep">BasisStencilOperation.keep
<a class="headerlink" href="#BasisStencilOperation.keep" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisStencilOperation" signature="zero"></endpoint>
<signature id="BasisStencilOperation.zero">BasisStencilOperation.zero
<a class="headerlink" href="#BasisStencilOperation.zero" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisStencilOperation" signature="replace"></endpoint>
<signature id="BasisStencilOperation.replace">BasisStencilOperation.replace
<a class="headerlink" href="#BasisStencilOperation.replace" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisStencilOperation" signature="increment_clamp"></endpoint>
<signature id="BasisStencilOperation.increment_clamp">BasisStencilOperation.increment_clamp
<a class="headerlink" href="#BasisStencilOperation.increment_clamp" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisStencilOperation" signature="decrement_clamp"></endpoint>
<signature id="BasisStencilOperation.decrement_clamp">BasisStencilOperation.decrement_clamp
<a class="headerlink" href="#BasisStencilOperation.decrement_clamp" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisStencilOperation" signature="invert"></endpoint>
<signature id="BasisStencilOperation.invert">BasisStencilOperation.invert
<a class="headerlink" href="#BasisStencilOperation.invert" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisStencilOperation" signature="increment_wrap"></endpoint>
<signature id="BasisStencilOperation.increment_wrap">BasisStencilOperation.increment_wrap
<a class="headerlink" href="#BasisStencilOperation.increment_wrap" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisStencilOperation" signature="decrement_wrap"></endpoint>
<signature id="BasisStencilOperation.decrement_wrap">BasisStencilOperation.decrement_wrap
<a class="headerlink" href="#BasisStencilOperation.decrement_wrap" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisStencilOperation" signature="invalid"></endpoint>
<signature id="BasisStencilOperation.invalid">BasisStencilOperation.invalid
<a class="headerlink" href="#BasisStencilOperation.invalid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### BasisWinding
`:::js import "luxe: type/basis.asset" for BasisWinding`
> no docs found

- [clockwise](#BasisWinding.clockwise)
- [counter_clockwise](#BasisWinding.counter_clockwise)

<hr/>
<endpoint module="luxe: type/basis.asset" class="BasisWinding" signature="clockwise"></endpoint>
<signature id="BasisWinding.clockwise">BasisWinding.clockwise
<a class="headerlink" href="#BasisWinding.clockwise" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/basis.asset" class="BasisWinding" signature="counter_clockwise"></endpoint>
<signature id="BasisWinding.counter_clockwise">BasisWinding.counter_clockwise
<a class="headerlink" href="#BasisWinding.counter_clockwise" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### BasisWriteMask
`:::js import "luxe: type/basis.asset" for BasisWriteMask`
> no docs found


<hr/>
