#![](../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2024.2.1`)  


---

## `luxe: asset` module

- [Asset](#asset)   
- [AssetGetAPI](#assetgetapi)   
- [AssetType](#assettype)   

---

### Asset
`:::js import "luxe: asset" for Asset`
> no docs found

- [get](#Asset.get)
- [tiles_source](#Asset.tiles_source)(**asset_id**: `String`)
- [tiles_visual](#Asset.tiles_visual)(**asset_id**: `String`)
- [face](#Asset.face)(**asset_id**: `String`)
- [prototype](#Asset.prototype)(**asset_id**: `String`)
- [font](#Asset.font)(**asset_id**: `String`)
- [tiles](#Asset.tiles)(**asset_id**: `String`)
- [compute](#Asset.compute)(**asset_id**: `String`)
- [text_style](#Asset.text_style)(**asset_id**: `String`)
- [scene](#Asset.scene)(**asset_id**: `String`)

<hr/>
<endpoint module="luxe: asset" class="Asset" signature="get"></endpoint>
<signature id="Asset.get">Asset.get
<a class="headerlink" href="#Asset.get" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AssetGetAPI`
> no docs found   

<endpoint module="luxe: asset" class="Asset" signature="tiles_source(asset_id : String)"></endpoint>
<signature id="Asset.tiles_source">Asset.tiles_source(**asset_id**: `String`)
<a class="headerlink" href="#Asset.tiles_source" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: asset" class="Asset" signature="tiles_visual(asset_id : String)"></endpoint>
<signature id="Asset.tiles_visual">Asset.tiles_visual(**asset_id**: `String`)
<a class="headerlink" href="#Asset.tiles_visual" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: asset" class="Asset" signature="face(asset_id : String)"></endpoint>
<signature id="Asset.face">Asset.face(**asset_id**: `String`)
<a class="headerlink" href="#Asset.face" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: asset" class="Asset" signature="prototype(asset_id : String)"></endpoint>
<signature id="Asset.prototype">Asset.prototype(**asset_id**: `String`)
<a class="headerlink" href="#Asset.prototype" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: asset" class="Asset" signature="font(asset_id : String)"></endpoint>
<signature id="Asset.font">Asset.font(**asset_id**: `String`)
<a class="headerlink" href="#Asset.font" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: asset" class="Asset" signature="tiles(asset_id : String)"></endpoint>
<signature id="Asset.tiles">Asset.tiles(**asset_id**: `String`)
<a class="headerlink" href="#Asset.tiles" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: asset" class="Asset" signature="compute(asset_id : String)"></endpoint>
<signature id="Asset.compute">Asset.compute(**asset_id**: `String`)
<a class="headerlink" href="#Asset.compute" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: asset" class="Asset" signature="text_style(asset_id : String)"></endpoint>
<signature id="Asset.text_style">Asset.text_style(**asset_id**: `String`)
<a class="headerlink" href="#Asset.text_style" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: asset" class="Asset" signature="scene(asset_id : String)"></endpoint>
<signature id="Asset.scene">Asset.scene(**asset_id**: `String`)
<a class="headerlink" href="#Asset.scene" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

### AssetGetAPI
`:::js import "luxe: asset" for AssetGetAPI`
> no docs found

- [new](#AssetGetAPI.new)()
- [tiles_source](#AssetGetAPI.tiles_source)(**asset_id**: `String`)
- [tiles_visual](#AssetGetAPI.tiles_visual)(**asset_id**: `String`)
- [face](#AssetGetAPI.face)(**asset_id**: `String`)
- [font](#AssetGetAPI.font)(**asset_id**: `String`)
- [basis](#AssetGetAPI.basis)(**asset_id**: `String`)
- [tiles](#AssetGetAPI.tiles)(**asset_id**: `String`)
- [asset_meta](#AssetGetAPI.asset_meta)(**asset_id**: `String`)
- [compute](#AssetGetAPI.compute)(**asset_id**: `String`)
- [text_style](#AssetGetAPI.text_style)(**asset_id**: `String`)
- [scene](#AssetGetAPI.scene)(**asset_id**: `String`)

<hr/>
<endpoint module="luxe: asset" class="AssetGetAPI" signature="new()"></endpoint>
<signature id="AssetGetAPI.new">AssetGetAPI.new()
<a class="headerlink" href="#AssetGetAPI.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AssetGetAPI`
> no docs found   

<endpoint module="luxe: asset" class="AssetGetAPI" signature="tiles_source(asset_id : String)"></endpoint>
<signature id="AssetGetAPI.tiles_source">AssetGetAPI.tiles_source(**asset_id**: `String`)
<a class="headerlink" href="#AssetGetAPI.tiles_source" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js TilesSourceDesc`
> no docs found   

<endpoint module="luxe: asset" class="AssetGetAPI" signature="tiles_visual(asset_id : String)"></endpoint>
<signature id="AssetGetAPI.tiles_visual">AssetGetAPI.tiles_visual(**asset_id**: `String`)
<a class="headerlink" href="#AssetGetAPI.tiles_visual" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js TilesVisualDesc`
> no docs found   

<endpoint module="luxe: asset" class="AssetGetAPI" signature="face(asset_id : String)"></endpoint>
<signature id="AssetGetAPI.face">AssetGetAPI.face(**asset_id**: `String`)
<a class="headerlink" href="#AssetGetAPI.face" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js FaceDesc`
> no docs found   

<endpoint module="luxe: asset" class="AssetGetAPI" signature="font(asset_id : String)"></endpoint>
<signature id="AssetGetAPI.font">AssetGetAPI.font(**asset_id**: `String`)
<a class="headerlink" href="#AssetGetAPI.font" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js FontDesc`
> no docs found   

<endpoint module="luxe: asset" class="AssetGetAPI" signature="basis(asset_id : String)"></endpoint>
<signature id="AssetGetAPI.basis">AssetGetAPI.basis(**asset_id**: `String`)
<a class="headerlink" href="#AssetGetAPI.basis" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Basis`
> no docs found   

<endpoint module="luxe: asset" class="AssetGetAPI" signature="tiles(asset_id : String)"></endpoint>
<signature id="AssetGetAPI.tiles">AssetGetAPI.tiles(**asset_id**: `String`)
<a class="headerlink" href="#AssetGetAPI.tiles" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js TilesDesc`
> no docs found   

<endpoint module="luxe: asset" class="AssetGetAPI" signature="asset_meta(asset_id : String)"></endpoint>
<signature id="AssetGetAPI.asset_meta">AssetGetAPI.asset_meta(**asset_id**: `String`)
<a class="headerlink" href="#AssetGetAPI.asset_meta" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AssetMeta`
> no docs found   

<endpoint module="luxe: asset" class="AssetGetAPI" signature="compute(asset_id : String)"></endpoint>
<signature id="AssetGetAPI.compute">AssetGetAPI.compute(**asset_id**: `String`)
<a class="headerlink" href="#AssetGetAPI.compute" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Compute`
> no docs found   

<endpoint module="luxe: asset" class="AssetGetAPI" signature="text_style(asset_id : String)"></endpoint>
<signature id="AssetGetAPI.text_style">AssetGetAPI.text_style(**asset_id**: `String`)
<a class="headerlink" href="#AssetGetAPI.text_style" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js TextStyle`
> no docs found   

<endpoint module="luxe: asset" class="AssetGetAPI" signature="scene(asset_id : String)"></endpoint>
<signature id="AssetGetAPI.scene">AssetGetAPI.scene(**asset_id**: `String`)
<a class="headerlink" href="#AssetGetAPI.scene" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js SceneDesc`
> no docs found   

### AssetType
`:::js import "luxe: asset" for AssetType`
> no docs found

- [modifier](#AssetType.modifier)
- [mesh](#AssetType.mesh)
- [anim](#AssetType.anim)
- [tiles_source](#AssetType.tiles_source)
- [tiles_visual](#AssetType.tiles_visual)
- [face](#AssetType.face)
- [entity](#AssetType.entity)
- [prototype](#AssetType.prototype)
- [image](#AssetType.image)
- [font](#AssetType.font)
- [basis](#AssetType.basis)
- [tiles](#AssetType.tiles)
- [material](#AssetType.material)
- [block_def](#AssetType.block_def)
- [asset_meta](#AssetType.asset_meta)
- [compute](#AssetType.compute)
- [text_style](#AssetType.text_style)
- [scene](#AssetType.scene)

<hr/>
<endpoint module="luxe: asset" class="AssetType" signature="modifier"></endpoint>
<signature id="AssetType.modifier">AssetType.modifier
<a class="headerlink" href="#AssetType.modifier" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset" class="AssetType" signature="mesh"></endpoint>
<signature id="AssetType.mesh">AssetType.mesh
<a class="headerlink" href="#AssetType.mesh" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset" class="AssetType" signature="anim"></endpoint>
<signature id="AssetType.anim">AssetType.anim
<a class="headerlink" href="#AssetType.anim" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset" class="AssetType" signature="tiles_source"></endpoint>
<signature id="AssetType.tiles_source">AssetType.tiles_source
<a class="headerlink" href="#AssetType.tiles_source" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset" class="AssetType" signature="tiles_visual"></endpoint>
<signature id="AssetType.tiles_visual">AssetType.tiles_visual
<a class="headerlink" href="#AssetType.tiles_visual" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset" class="AssetType" signature="face"></endpoint>
<signature id="AssetType.face">AssetType.face
<a class="headerlink" href="#AssetType.face" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset" class="AssetType" signature="entity"></endpoint>
<signature id="AssetType.entity">AssetType.entity
<a class="headerlink" href="#AssetType.entity" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset" class="AssetType" signature="prototype"></endpoint>
<signature id="AssetType.prototype">AssetType.prototype
<a class="headerlink" href="#AssetType.prototype" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset" class="AssetType" signature="image"></endpoint>
<signature id="AssetType.image">AssetType.image
<a class="headerlink" href="#AssetType.image" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset" class="AssetType" signature="font"></endpoint>
<signature id="AssetType.font">AssetType.font
<a class="headerlink" href="#AssetType.font" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset" class="AssetType" signature="basis"></endpoint>
<signature id="AssetType.basis">AssetType.basis
<a class="headerlink" href="#AssetType.basis" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset" class="AssetType" signature="tiles"></endpoint>
<signature id="AssetType.tiles">AssetType.tiles
<a class="headerlink" href="#AssetType.tiles" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset" class="AssetType" signature="material"></endpoint>
<signature id="AssetType.material">AssetType.material
<a class="headerlink" href="#AssetType.material" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset" class="AssetType" signature="block_def"></endpoint>
<signature id="AssetType.block_def">AssetType.block_def
<a class="headerlink" href="#AssetType.block_def" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset" class="AssetType" signature="asset_meta"></endpoint>
<signature id="AssetType.asset_meta">AssetType.asset_meta
<a class="headerlink" href="#AssetType.asset_meta" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset" class="AssetType" signature="compute"></endpoint>
<signature id="AssetType.compute">AssetType.compute
<a class="headerlink" href="#AssetType.compute" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset" class="AssetType" signature="text_style"></endpoint>
<signature id="AssetType.text_style">AssetType.text_style
<a class="headerlink" href="#AssetType.text_style" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: asset" class="AssetType" signature="scene"></endpoint>
<signature id="AssetType.scene">AssetType.scene
<a class="headerlink" href="#AssetType.scene" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

