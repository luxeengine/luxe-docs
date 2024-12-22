#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2024.12.3`)  


---

## `luxe: system/mesh.modifier` module

- [Data](#data)   
- [InstancedMode](#instancedmode)   
- [Mesh](#mesh)   
- [System](#system)   

---

### Data
`:::js import "luxe: system/mesh.modifier" for Data`
> no docs found

- `:::js var mesh : Asset = null`
- `:::js var material : Asset = null`
- `:::js var instanced : InstancedMode = InstancedMode.none`
- `:::js var own_materials : Bool = false`

<hr/>
### InstancedMode
`:::js import "luxe: system/mesh.modifier" for InstancedMode`
> no docs found

- [none](#InstancedMode.none)
- [group_auto](#InstancedMode.group_auto)
- [group_custom](#InstancedMode.group_custom)

<hr/>
<endpoint module="luxe: system/mesh.modifier" class="InstancedMode" signature="none"></endpoint>
<signature id="InstancedMode.none">InstancedMode.none
<a class="headerlink" href="#InstancedMode.none" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="InstancedMode" signature="group_auto"></endpoint>
<signature id="InstancedMode.group_auto">InstancedMode.group_auto
<a class="headerlink" href="#InstancedMode.group_auto" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="InstancedMode" signature="group_custom"></endpoint>
<signature id="InstancedMode.group_custom">InstancedMode.group_custom
<a class="headerlink" href="#InstancedMode.group_custom" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Mesh
`:::js import "luxe: system/mesh.modifier" for Mesh`
> no docs found

- [create](#Mesh.create)(**entity**: `Entity`)
- [create](#Mesh.create+3)(**entity**: `Entity`, **material**: `Material`, **mesh_lx**: `String`)
- [destroy](#Mesh.destroy)(**entity**: `Entity`)
- [set_instanced_auto_units](#Mesh.set_instanced_auto_units+2)(**world**: `World`, **grid_units_cell_size**: `Num`)
- [get_instanced_auto_units](#Mesh.get_instanced_auto_units)(**world**: `World`)
- [has](#Mesh.has)(**entity**: `Entity`)
- [clear](#Mesh.clear)(**entity**: `Entity`)
- [level_get_element_count](#Mesh.level_get_element_count+2)(**entity**: `Entity`, **level**: `Num`)
- [level_get_count](#Mesh.level_get_count)(**entity**: `Entity`)
- [level_set_active](#Mesh.level_set_active+3)(**entity**: `Entity`, **level**: `Num`, **disable_current**: `Bool`)
- [level_get_active](#Mesh.level_get_active)(**entity**: `Entity`)
- [level_set_enabled](#Mesh.level_set_enabled+3)(**entity**: `Entity`, **level**: `Num`, **state**: `Bool`)
- [level_get_enabled](#Mesh.level_get_enabled+2)(**entity**: `Entity`, **level**: `Num`)
- [set_asset](#Mesh.set_asset+2)(**entity**: `Entity`, **asset_id**: `String`)
- [set_instanced_group](#Mesh.set_instanced_group+2)(**entity**: `Entity`, **group_id**: `String`)
- [get_instanced_group](#Mesh.get_instanced_group)(**entity**: `Entity`)
- [set_instanced](#Mesh.set_instanced+2)(**entity**: `Entity`, **state**: `Bool`)
- [get_instanced](#Mesh.get_instanced)(**entity**: `Entity`)
- [get_source_id](#Mesh.get_source_id)(**entity**: `Entity`)
- [get_default_material](#Mesh.get_default_material)(**entity**: `Entity`)
- [set_default_material](#Mesh.set_default_material+2)(**entity**: `Entity`, **material**: `Material`)
- [get_geometry](#Mesh.get_geometry+3)(**entity**: `Entity`, **level**: `Num`, **element**: `Num`)
- [get_geometry](#Mesh.get_geometry)(**entity**: `Entity`)
- [obb_intersect_ray](#Mesh.obb_intersect_ray+7)(**entity**: `Entity`, **ray_x**: `Num`, **ray_y**: `Num`, **ray_z**: `Num`, **ray_dir_x**: `Num`, **ray_dir_y**: `Num`, **ray_dir_z**: `Num`)

<hr/>
<endpoint module="luxe: system/mesh.modifier" class="Mesh" signature="create(entity : Entity)"></endpoint>
<signature id="Mesh.create">Mesh.create(**entity**: `Entity`)
<a class="headerlink" href="#Mesh.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="Mesh" signature="create(entity : Entity, material : Material, mesh_lx : String)"></endpoint>
<signature id="Mesh.create+3">Mesh.create(**entity**: `Entity`, **material**: `Material`, **mesh_lx**: `String`)
<a class="headerlink" href="#Mesh.create+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="Mesh" signature="destroy(entity : Entity)"></endpoint>
<signature id="Mesh.destroy">Mesh.destroy(**entity**: `Entity`)
<a class="headerlink" href="#Mesh.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="Mesh" signature="set_instanced_auto_units(world : World, grid_units_cell_size : Num)"></endpoint>
<signature id="Mesh.set_instanced_auto_units+2">Mesh.set_instanced_auto_units(**world**: `World`, **grid_units_cell_size**: `Num`)
<a class="headerlink" href="#Mesh.set_instanced_auto_units+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="Mesh" signature="get_instanced_auto_units(world : World)"></endpoint>
<signature id="Mesh.get_instanced_auto_units">Mesh.get_instanced_auto_units(**world**: `World`)
<a class="headerlink" href="#Mesh.get_instanced_auto_units" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="Mesh" signature="has(entity : Entity)"></endpoint>
<signature id="Mesh.has">Mesh.has(**entity**: `Entity`)
<a class="headerlink" href="#Mesh.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="Mesh" signature="clear(entity : Entity)"></endpoint>
<signature id="Mesh.clear">Mesh.clear(**entity**: `Entity`)
<a class="headerlink" href="#Mesh.clear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="Mesh" signature="level_get_element_count(entity : Entity, level : Num)"></endpoint>
<signature id="Mesh.level_get_element_count+2">Mesh.level_get_element_count(**entity**: `Entity`, **level**: `Num`)
<a class="headerlink" href="#Mesh.level_get_element_count+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="Mesh" signature="level_get_count(entity : Entity)"></endpoint>
<signature id="Mesh.level_get_count">Mesh.level_get_count(**entity**: `Entity`)
<a class="headerlink" href="#Mesh.level_get_count" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="Mesh" signature="level_set_active(entity : Entity, level : Num, disable_current : Bool)"></endpoint>
<signature id="Mesh.level_set_active+3">Mesh.level_set_active(**entity**: `Entity`, **level**: `Num`, **disable_current**: `Bool`)
<a class="headerlink" href="#Mesh.level_set_active+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="Mesh" signature="level_get_active(entity : Entity)"></endpoint>
<signature id="Mesh.level_get_active">Mesh.level_get_active(**entity**: `Entity`)
<a class="headerlink" href="#Mesh.level_get_active" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="Mesh" signature="level_set_enabled(entity : Entity, level : Num, state : Bool)"></endpoint>
<signature id="Mesh.level_set_enabled+3">Mesh.level_set_enabled(**entity**: `Entity`, **level**: `Num`, **state**: `Bool`)
<a class="headerlink" href="#Mesh.level_set_enabled+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="Mesh" signature="level_get_enabled(entity : Entity, level : Num)"></endpoint>
<signature id="Mesh.level_get_enabled+2">Mesh.level_get_enabled(**entity**: `Entity`, **level**: `Num`)
<a class="headerlink" href="#Mesh.level_get_enabled+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="Mesh" signature="set_asset(entity : Entity, asset_id : String)"></endpoint>
<signature id="Mesh.set_asset+2">Mesh.set_asset(**entity**: `Entity`, **asset_id**: `String`)
<a class="headerlink" href="#Mesh.set_asset+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="Mesh" signature="set_instanced_group(entity : Entity, group_id : String)"></endpoint>
<signature id="Mesh.set_instanced_group+2">Mesh.set_instanced_group(**entity**: `Entity`, **group_id**: `String`)
<a class="headerlink" href="#Mesh.set_instanced_group+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="Mesh" signature="get_instanced_group(entity : Entity)"></endpoint>
<signature id="Mesh.get_instanced_group">Mesh.get_instanced_group(**entity**: `Entity`)
<a class="headerlink" href="#Mesh.get_instanced_group" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="Mesh" signature="set_instanced(entity : Entity, state : Bool)"></endpoint>
<signature id="Mesh.set_instanced+2">Mesh.set_instanced(**entity**: `Entity`, **state**: `Bool`)
<a class="headerlink" href="#Mesh.set_instanced+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="Mesh" signature="get_instanced(entity : Entity)"></endpoint>
<signature id="Mesh.get_instanced">Mesh.get_instanced(**entity**: `Entity`)
<a class="headerlink" href="#Mesh.get_instanced" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="Mesh" signature="get_source_id(entity : Entity)"></endpoint>
<signature id="Mesh.get_source_id">Mesh.get_source_id(**entity**: `Entity`)
<a class="headerlink" href="#Mesh.get_source_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="Mesh" signature="get_default_material(entity : Entity)"></endpoint>
<signature id="Mesh.get_default_material">Mesh.get_default_material(**entity**: `Entity`)
<a class="headerlink" href="#Mesh.get_default_material" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="Mesh" signature="set_default_material(entity : Entity, material : Material)"></endpoint>
<signature id="Mesh.set_default_material+2">Mesh.set_default_material(**entity**: `Entity`, **material**: `Material`)
<a class="headerlink" href="#Mesh.set_default_material+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="Mesh" signature="get_geometry(entity : Entity, level : Num, element : Num)"></endpoint>
<signature id="Mesh.get_geometry+3">Mesh.get_geometry(**entity**: `Entity`, **level**: `Num`, **element**: `Num`)
<a class="headerlink" href="#Mesh.get_geometry+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="Mesh" signature="get_geometry(entity : Entity)"></endpoint>
<signature id="Mesh.get_geometry">Mesh.get_geometry(**entity**: `Entity`)
<a class="headerlink" href="#Mesh.get_geometry" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/mesh.modifier" class="Mesh" signature="obb_intersect_ray(entity : Entity, ray_x : Num, ray_y : Num, ray_z : Num, ray_dir_x : Num, ray_dir_y : Num, ray_dir_z : Num)"></endpoint>
<signature id="Mesh.obb_intersect_ray+7">Mesh.obb_intersect_ray(**entity**: `Entity`, **ray_x**: `Num`, **ray_y**: `Num`, **ray_z**: `Num`, **ray_dir_x**: `Num`, **ray_dir_y**: `Num`, **ray_dir_z**: `Num`)
<a class="headerlink" href="#Mesh.obb_intersect_ray+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### System
`:::js import "luxe: system/mesh.modifier" for System`
> no docs found

- [new](#System.new)(**world**: `World`)

<hr/>
<endpoint module="luxe: system/mesh.modifier" class="System" signature="new(world : World)"></endpoint>
<signature id="System.new">System.new(**world**: `World`)
<a class="headerlink" href="#System.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js System`
> no docs found   

