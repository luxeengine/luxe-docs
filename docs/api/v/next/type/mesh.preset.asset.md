#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.11.1`)  


---

## `luxe: type/mesh.preset.asset` module

- [Asset](#asset)   
- [MeshPreset](#meshpreset)   
- [MeshPresetContext](#meshpresetcontext)   
- [PresetInput](#presetinput)   
- [Presets](#presets)   

---

### Asset
`:::js import "luxe: type/mesh.preset.asset" for Asset`
> no docs found

- [subtype](#Asset.subtype)
- [ext](#Asset.ext)
- [after](#Asset.after)
- [before](#Asset.before)
- [new](#Asset.new+2)(**type_id**: `String`, **ctx**: `AssetContext`)
- [pre](#Asset.pre)(**assets**: `List`)

<hr/>
<endpoint module="luxe: type/mesh.preset.asset" class="Asset" signature="subtype"></endpoint>
<signature id="Asset.subtype">Asset.subtype
<a class="headerlink" href="#Asset.subtype" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/mesh.preset.asset" class="Asset" signature="ext"></endpoint>
<signature id="Asset.ext">Asset.ext
<a class="headerlink" href="#Asset.ext" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/mesh.preset.asset" class="Asset" signature="after"></endpoint>
<signature id="Asset.after">Asset.after
<a class="headerlink" href="#Asset.after" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/mesh.preset.asset" class="Asset" signature="before"></endpoint>
<signature id="Asset.before">Asset.before
<a class="headerlink" href="#Asset.before" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/mesh.preset.asset" class="Asset" signature="new(type_id : String, ctx : AssetContext)"></endpoint>
<signature id="Asset.new+2">Asset.new(**type_id**: `String`, **ctx**: `AssetContext`)
<a class="headerlink" href="#Asset.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Asset`
> no docs found   

<endpoint module="luxe: type/mesh.preset.asset" class="Asset" signature="pre(assets : List)"></endpoint>
<signature id="Asset.pre">Asset.pre(**assets**: `List`)
<a class="headerlink" href="#Asset.pre" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### MeshPreset
`:::js import "luxe: type/mesh.preset.asset" for MeshPreset`
> no docs found

- [order](#MeshPreset.order)
- [search_paths](#MeshPreset.search_paths)(**mesh**: `String`)
- [convert_material](#MeshPreset.convert_material)(**from**: `Map`)
- [convert_material](#MeshPreset.convert_material+2)(**asset**: `AssetID`, **from**: `Map`)
- [map_material](#MeshPreset.map_material+2)(**asset**: `AssetID`, **name**: `String`)

<hr/>
<endpoint module="luxe: type/mesh.preset.asset" class="MeshPreset" signature="order"></endpoint>
<signature id="MeshPreset.order">MeshPreset.order
<a class="headerlink" href="#MeshPreset.order" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/mesh.preset.asset" class="MeshPreset" signature="search_paths(mesh : String)"></endpoint>
<signature id="MeshPreset.search_paths">MeshPreset.search_paths(**mesh**: `String`)
<a class="headerlink" href="#MeshPreset.search_paths" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/mesh.preset.asset" class="MeshPreset" signature="convert_material(from : Map)"></endpoint>
<signature id="MeshPreset.convert_material">MeshPreset.convert_material(**from**: `Map`)
<a class="headerlink" href="#MeshPreset.convert_material" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Map`
> no docs found   

<endpoint module="luxe: type/mesh.preset.asset" class="MeshPreset" signature="convert_material(asset : AssetID, from : Map)"></endpoint>
<signature id="MeshPreset.convert_material+2">MeshPreset.convert_material(**asset**: `AssetID`, **from**: `Map`)
<a class="headerlink" href="#MeshPreset.convert_material+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Map`
> no docs found   

<endpoint module="luxe: type/mesh.preset.asset" class="MeshPreset" signature="map_material(asset : AssetID, name : String)"></endpoint>
<signature id="MeshPreset.map_material+2">MeshPreset.map_material(**asset**: `AssetID`, **name**: `String`)
<a class="headerlink" href="#MeshPreset.map_material+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

### MeshPresetContext
`:::js import "luxe: type/mesh.preset.asset" for MeshPresetContext`
> no docs found

- [new](#MeshPresetContext.new)()

<hr/>
<endpoint module="luxe: type/mesh.preset.asset" class="MeshPresetContext" signature="new()"></endpoint>
<signature id="MeshPresetContext.new">MeshPresetContext.new()
<a class="headerlink" href="#MeshPresetContext.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js MeshPresetContext`
> no docs found   

### PresetInput
`:::js import "luxe: type/mesh.preset.asset" for PresetInput`
> no docs found

- [unknown](#PresetInput.unknown)
- [name](#PresetInput.name)
- [has_images](#PresetInput.has_images)
- [base_color](#PresetInput.base_color)
- [base_color_factor](#PresetInput.base_color_factor)
- [base_color_image](#PresetInput.base_color_image)
- [metallic_factor](#PresetInput.metallic_factor)
- [roughness_factor](#PresetInput.roughness_factor)
- [normal_image](#PresetInput.normal_image)
- [occlusion_image](#PresetInput.occlusion_image)
- [roughness_image](#PresetInput.roughness_image)
- [metallic_image](#PresetInput.metallic_image)

<hr/>
<endpoint module="luxe: type/mesh.preset.asset" class="PresetInput" signature="unknown"></endpoint>
<signature id="PresetInput.unknown">PresetInput.unknown
<a class="headerlink" href="#PresetInput.unknown" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/mesh.preset.asset" class="PresetInput" signature="name"></endpoint>
<signature id="PresetInput.name">PresetInput.name
<a class="headerlink" href="#PresetInput.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/mesh.preset.asset" class="PresetInput" signature="has_images"></endpoint>
<signature id="PresetInput.has_images">PresetInput.has_images
<a class="headerlink" href="#PresetInput.has_images" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/mesh.preset.asset" class="PresetInput" signature="base_color"></endpoint>
<signature id="PresetInput.base_color">PresetInput.base_color
<a class="headerlink" href="#PresetInput.base_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/mesh.preset.asset" class="PresetInput" signature="base_color_factor"></endpoint>
<signature id="PresetInput.base_color_factor">PresetInput.base_color_factor
<a class="headerlink" href="#PresetInput.base_color_factor" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/mesh.preset.asset" class="PresetInput" signature="base_color_image"></endpoint>
<signature id="PresetInput.base_color_image">PresetInput.base_color_image
<a class="headerlink" href="#PresetInput.base_color_image" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/mesh.preset.asset" class="PresetInput" signature="metallic_factor"></endpoint>
<signature id="PresetInput.metallic_factor">PresetInput.metallic_factor
<a class="headerlink" href="#PresetInput.metallic_factor" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/mesh.preset.asset" class="PresetInput" signature="roughness_factor"></endpoint>
<signature id="PresetInput.roughness_factor">PresetInput.roughness_factor
<a class="headerlink" href="#PresetInput.roughness_factor" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/mesh.preset.asset" class="PresetInput" signature="normal_image"></endpoint>
<signature id="PresetInput.normal_image">PresetInput.normal_image
<a class="headerlink" href="#PresetInput.normal_image" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/mesh.preset.asset" class="PresetInput" signature="occlusion_image"></endpoint>
<signature id="PresetInput.occlusion_image">PresetInput.occlusion_image
<a class="headerlink" href="#PresetInput.occlusion_image" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/mesh.preset.asset" class="PresetInput" signature="roughness_image"></endpoint>
<signature id="PresetInput.roughness_image">PresetInput.roughness_image
<a class="headerlink" href="#PresetInput.roughness_image" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/mesh.preset.asset" class="PresetInput" signature="metallic_image"></endpoint>
<signature id="PresetInput.metallic_image">PresetInput.metallic_image
<a class="headerlink" href="#PresetInput.metallic_image" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Presets
`:::js import "luxe: type/mesh.preset.asset" for Presets`
> no docs found

- [get](#Presets.get)()
- [fix_path](#Presets.fix_path)(**path**: `String`)
- [post_fix](#Presets.post_fix)(**result**: `Map`)
- [generate](#Presets.generate+4)(**ctx**: `AssetContext`, **tag**: `String`, **asset**: `AssetID`, **converter**: `Fn`)

<hr/>
<endpoint module="luxe: type/mesh.preset.asset" class="Presets" signature="get()"></endpoint>
<signature id="Presets.get">Presets.get()
<a class="headerlink" href="#Presets.get" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: type/mesh.preset.asset" class="Presets" signature="fix_path(path : String)"></endpoint>
<signature id="Presets.fix_path">Presets.fix_path(**path**: `String`)
<a class="headerlink" href="#Presets.fix_path" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: type/mesh.preset.asset" class="Presets" signature="post_fix(result : Map)"></endpoint>
<signature id="Presets.post_fix">Presets.post_fix(**result**: `Map`)
<a class="headerlink" href="#Presets.post_fix" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/mesh.preset.asset" class="Presets" signature="generate(ctx : AssetContext, tag : String, asset : AssetID, converter : Fn)"></endpoint>
<signature id="Presets.generate+4">Presets.generate(**ctx**: `AssetContext`, **tag**: `String`, **asset**: `AssetID`, **converter**: `Fn`)
<a class="headerlink" href="#Presets.generate+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

