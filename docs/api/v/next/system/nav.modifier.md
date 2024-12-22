#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2024.12.4`)  


---

## `luxe: system/nav.modifier` module

- [Data](#data)   
- [Nav](#nav)   
- [Partition](#partition)   
- [System](#system)   

---

### Data
`:::js import "luxe: system/nav.modifier" for Data`
> no docs found

- `:::js var rebuild : Num = 1`
- `:::js var mesh : Asset = null`
- `:::js var tile_size : Num = 32`
- `:::js var cell_size : Num = 0.3`
- `:::js var cell_height : Num = 0.2`
- `:::js var height : Num = 2`
- `:::js var radius : Num = 0.6`
- `:::js var max_climb : Num = 0.9`
- `:::js var max_slope : Num = 45`
- `:::js var min_region_size : Num = 8`
- `:::js var merged_region_size : Num = 20`
- `:::js var max_edge_length : Num = 12`
- `:::js var max_edge_error : Num = 1.3`
- `:::js var verts_per_poly : Num = 6`
- `:::js var detail_sample_distance : Num = 6`
- `:::js var detail_sample_max_error : Num = 1`
- `:::js var partition : Partition = Partition.watershed`
- `:::js var no_low_hanging : Bool = true`
- `:::js var no_ledge_spans : Bool = true`
- `:::js var no_walkable_low_spans : Bool = true`
- `:::js var debug_draw : Bool = false`
- `:::js var keep_debug_data : Bool = false`

<hr/>
### Nav
`:::js import "luxe: system/nav.modifier" for Nav`
> no docs found

- [raycast](#Nav.raycast+4)(**entity**: `Entity`, **start**: `Float3`, **end**: `Float3`, **extents**: `Float3`)
- [nearest_point](#Nav.nearest_point+3)(**entity**: `Entity`, **start**: `Float3`, **extents**: `Float3`)
- [get_path](#Nav.get_path+4)(**entity**: `Entity`, **start**: `Float3`, **end**: `Float3`, **extents**: `Float3`)

<hr/>
<endpoint module="luxe: system/nav.modifier" class="Nav" signature="raycast(entity : Entity, start : Float3, end : Float3, extents : Float3)"></endpoint>
<signature id="Nav.raycast+4">Nav.raycast(**entity**: `Entity`, **start**: `Float3`, **end**: `Float3`, **extents**: `Float3`)
<a class="headerlink" href="#Nav.raycast+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Float3`
> no docs found   

<endpoint module="luxe: system/nav.modifier" class="Nav" signature="nearest_point(entity : Entity, start : Float3, extents : Float3)"></endpoint>
<signature id="Nav.nearest_point+3">Nav.nearest_point(**entity**: `Entity`, **start**: `Float3`, **extents**: `Float3`)
<a class="headerlink" href="#Nav.nearest_point+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Float3`
> no docs found   

<endpoint module="luxe: system/nav.modifier" class="Nav" signature="get_path(entity : Entity, start : Float3, end : Float3, extents : Float3)"></endpoint>
<signature id="Nav.get_path+4">Nav.get_path(**entity**: `Entity`, **start**: `Float3`, **end**: `Float3`, **extents**: `Float3`)
<a class="headerlink" href="#Nav.get_path+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

### Partition
`:::js import "luxe: system/nav.modifier" for Partition`
> no docs found

- [watershed](#Partition.watershed)
- [monotone](#Partition.monotone)
- [layers](#Partition.layers)

<hr/>
<endpoint module="luxe: system/nav.modifier" class="Partition" signature="watershed"></endpoint>
<signature id="Partition.watershed">Partition.watershed
<a class="headerlink" href="#Partition.watershed" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/nav.modifier" class="Partition" signature="monotone"></endpoint>
<signature id="Partition.monotone">Partition.monotone
<a class="headerlink" href="#Partition.monotone" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/nav.modifier" class="Partition" signature="layers"></endpoint>
<signature id="Partition.layers">Partition.layers
<a class="headerlink" href="#Partition.layers" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### System
`:::js import "luxe: system/nav.modifier" for System`
> no docs found

- [new](#System.new)(**world**: `World`)

<hr/>
<endpoint module="luxe: system/nav.modifier" class="System" signature="new(world : World)"></endpoint>
<signature id="System.new">System.new(**world**: `World`)
<a class="headerlink" href="#System.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js System`
> no docs found   

