#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2024.12.3`)  


---

## `luxe: system/tiles.modifier` module

- [Data](#data)   
- [System](#system)   
- [Tile](#tile)   
- [Tiles](#tiles)   

---

### Data
`:::js import "luxe: system/tiles.modifier" for Data`
> no docs found

- `:::js var tiles : Asset = null`

<hr/>
### System
`:::js import "luxe: system/tiles.modifier" for System`
> no docs found

- [new](#System.new)(**world**: `World`)

<hr/>
<endpoint module="luxe: system/tiles.modifier" class="System" signature="new(world : World)"></endpoint>
<signature id="System.new">System.new(**world**: `World`)
<a class="headerlink" href="#System.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js System`
> no docs found   

### Tile
`:::js import "luxe: system/tiles.modifier" for Tile`
> no docs found

- [create](#Tile.create+5)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **depth**: `Any`, **visual_id**: `Any`)
- [destroy](#Tile.destroy+2)(**entity**: `Any`, **tile**: `Any`)
- [destroy_at](#Tile.destroy_at+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **depth**: `Any`)
- [exists_at](#Tile.exists_at+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **depth**: `Any`)
- [get_at](#Tile.get_at+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **depth**: `Any`)
- [get_all](#Tile.get_all+2)(**entity**: `Any`, **into**: `Any`)
- [get_all_at](#Tile.get_all_at+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **into**: `Any`)
- [get_all_at_depth](#Tile.get_all_at_depth+3)(**entity**: `Any`, **depth**: `Any`, **into**: `Any`)
- [get_all_with_tag](#Tile.get_all_with_tag+3)(**entity**: `Any`, **tag**: `Any`, **into**: `Any`)
- [get_all_with_visual](#Tile.get_all_with_visual+3)(**entity**: `Any`, **visual**: `Any`, **into**: `Any`)
- [add_tag](#Tile.add_tag+3)(**entity**: `Any`, **tile**: `Any`, **tag**: `Any`)
- [remove_tag](#Tile.remove_tag+3)(**entity**: `Any`, **tile**: `Any`, **tag**: `Any`)
- [has_tag](#Tile.has_tag+3)(**entity**: `Any`, **tile**: `Any`, **tag**: `Any`)
- [get_tags](#Tile.get_tags+2)(**entity**: `Any`, **tile**: `Any`)
- [clear_tags](#Tile.clear_tags+2)(**entity**: `Any`, **tile**: `Any`)
- [set](#Tile.set+4)(**entity**: `Any`, **tile**: `Any`, **key**: `Any`, **value**: `Any`)
- [get](#Tile.get+4)(**entity**: `Any`, **tile**: `Any`, **key**: `Any`, **default**: `Any`)
- [set_coord](#Tile.set_coord+4)(**entity**: `Any`, **tile**: `Any`, **x**: `Any`, **y**: `Any`)
- [get_coord_x](#Tile.get_coord_x+2)(**entity**: `Any`, **tile**: `Any`)
- [get_coord_y](#Tile.get_coord_y+2)(**entity**: `Any`, **tile**: `Any`)
- [set_depth](#Tile.set_depth+3)(**entity**: `Any`, **tile**: `Any`, **depth**: `Any`)
- [get_depth](#Tile.get_depth+2)(**entity**: `Any`, **tile**: `Any`)
- [set_offset](#Tile.set_offset+4)(**entity**: `Any`, **tile**: `Any`, **x**: `Any`, **y**: `Any`)
- [set_offset_x](#Tile.set_offset_x+3)(**entity**: `Any`, **tile**: `Any`, **x**: `Any`)
- [set_offset_y](#Tile.set_offset_y+3)(**entity**: `Any`, **tile**: `Any`, **y**: `Any`)
- [get_offset_x](#Tile.get_offset_x+2)(**entity**: `Any`, **tile**: `Any`)
- [get_offset_y](#Tile.get_offset_y+2)(**entity**: `Any`, **tile**: `Any`)
- [reset_size](#Tile.reset_size+2)(**entity**: `Any`, **tile**: `Any`)
- [set_size](#Tile.set_size+4)(**entity**: `Any`, **tile**: `Any`, **x**: `Any`, **y**: `Any`)
- [set_size_x](#Tile.set_size_x+3)(**entity**: `Any`, **tile**: `Any`, **x**: `Any`)
- [set_size_y](#Tile.set_size_y+3)(**entity**: `Any`, **tile**: `Any`, **y**: `Any`)
- [get_size_x](#Tile.get_size_x+2)(**entity**: `Any`, **tile**: `Any`)
- [get_size_y](#Tile.get_size_y+2)(**entity**: `Any`, **tile**: `Any`)
- [set_flip](#Tile.set_flip+4)(**entity**: `Any`, **tile**: `Any`, **x**: `Any`, **y**: `Any`)
- [set_flip_x](#Tile.set_flip_x+3)(**entity**: `Any`, **tile**: `Any`, **flip**: `Any`)
- [set_flip_y](#Tile.set_flip_y+3)(**entity**: `Any`, **tile**: `Any`, **flip**: `Any`)
- [get_flip_x](#Tile.get_flip_x+2)(**entity**: `Any`, **tile**: `Any`)
- [get_flip_y](#Tile.get_flip_y+2)(**entity**: `Any`, **tile**: `Any`)
- [set_visual](#Tile.set_visual+3)(**entity**: `Any`, **tile**: `Any`, **visual**: `Any`)
- [get_visual](#Tile.get_visual+2)(**entity**: `Any`, **tile**: `Any`)
- [set_angle](#Tile.set_angle+3)(**entity**: `Any`, **tile**: `Any`, **angle**: `Any`)
- [get_angle](#Tile.get_angle+2)(**entity**: `Any`, **tile**: `Any`)
- [set_color](#Tile.set_color+3)(**entity**: `Any`, **tile**: `Any`, **color**: `Any`)
- [get_color](#Tile.get_color+2)(**entity**: `Any`, **tile**: `Any`)

<hr/>
<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="create(entity : Any, x : Any, y : Any, depth : Any, visual_id : Any)"></endpoint>
<signature id="Tile.create+5">Tile.create(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **depth**: `Any`, **visual_id**: `Any`)
<a class="headerlink" href="#Tile.create+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="destroy(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.destroy+2">Tile.destroy(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.destroy+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="destroy_at(entity : Any, x : Any, y : Any, depth : Any)"></endpoint>
<signature id="Tile.destroy_at+4">Tile.destroy_at(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **depth**: `Any`)
<a class="headerlink" href="#Tile.destroy_at+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="exists_at(entity : Any, x : Any, y : Any, depth : Any)"></endpoint>
<signature id="Tile.exists_at+4">Tile.exists_at(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **depth**: `Any`)
<a class="headerlink" href="#Tile.exists_at+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="get_at(entity : Any, x : Any, y : Any, depth : Any)"></endpoint>
<signature id="Tile.get_at+4">Tile.get_at(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **depth**: `Any`)
<a class="headerlink" href="#Tile.get_at+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="get_all(entity : Any, into : Any)"></endpoint>
<signature id="Tile.get_all+2">Tile.get_all(**entity**: `Any`, **into**: `Any`)
<a class="headerlink" href="#Tile.get_all+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="get_all_at(entity : Any, x : Any, y : Any, into : Any)"></endpoint>
<signature id="Tile.get_all_at+4">Tile.get_all_at(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **into**: `Any`)
<a class="headerlink" href="#Tile.get_all_at+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="get_all_at_depth(entity : Any, depth : Any, into : Any)"></endpoint>
<signature id="Tile.get_all_at_depth+3">Tile.get_all_at_depth(**entity**: `Any`, **depth**: `Any`, **into**: `Any`)
<a class="headerlink" href="#Tile.get_all_at_depth+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="get_all_with_tag(entity : Any, tag : Any, into : Any)"></endpoint>
<signature id="Tile.get_all_with_tag+3">Tile.get_all_with_tag(**entity**: `Any`, **tag**: `Any`, **into**: `Any`)
<a class="headerlink" href="#Tile.get_all_with_tag+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="get_all_with_visual(entity : Any, visual : Any, into : Any)"></endpoint>
<signature id="Tile.get_all_with_visual+3">Tile.get_all_with_visual(**entity**: `Any`, **visual**: `Any`, **into**: `Any`)
<a class="headerlink" href="#Tile.get_all_with_visual+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="add_tag(entity : Any, tile : Any, tag : Any)"></endpoint>
<signature id="Tile.add_tag+3">Tile.add_tag(**entity**: `Any`, **tile**: `Any`, **tag**: `Any`)
<a class="headerlink" href="#Tile.add_tag+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="remove_tag(entity : Any, tile : Any, tag : Any)"></endpoint>
<signature id="Tile.remove_tag+3">Tile.remove_tag(**entity**: `Any`, **tile**: `Any`, **tag**: `Any`)
<a class="headerlink" href="#Tile.remove_tag+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="has_tag(entity : Any, tile : Any, tag : Any)"></endpoint>
<signature id="Tile.has_tag+3">Tile.has_tag(**entity**: `Any`, **tile**: `Any`, **tag**: `Any`)
<a class="headerlink" href="#Tile.has_tag+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="get_tags(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_tags+2">Tile.get_tags(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_tags+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="clear_tags(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.clear_tags+2">Tile.clear_tags(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.clear_tags+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="set(entity : Any, tile : Any, key : Any, value : Any)"></endpoint>
<signature id="Tile.set+4">Tile.set(**entity**: `Any`, **tile**: `Any`, **key**: `Any`, **value**: `Any`)
<a class="headerlink" href="#Tile.set+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="get(entity : Any, tile : Any, key : Any, default : Any)"></endpoint>
<signature id="Tile.get+4">Tile.get(**entity**: `Any`, **tile**: `Any`, **key**: `Any`, **default**: `Any`)
<a class="headerlink" href="#Tile.get+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="set_coord(entity : Any, tile : Any, x : Any, y : Any)"></endpoint>
<signature id="Tile.set_coord+4">Tile.set_coord(**entity**: `Any`, **tile**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Tile.set_coord+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="get_coord_x(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_coord_x+2">Tile.get_coord_x(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_coord_x+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="get_coord_y(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_coord_y+2">Tile.get_coord_y(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_coord_y+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="set_depth(entity : Any, tile : Any, depth : Any)"></endpoint>
<signature id="Tile.set_depth+3">Tile.set_depth(**entity**: `Any`, **tile**: `Any`, **depth**: `Any`)
<a class="headerlink" href="#Tile.set_depth+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="get_depth(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_depth+2">Tile.get_depth(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_depth+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="set_offset(entity : Any, tile : Any, x : Any, y : Any)"></endpoint>
<signature id="Tile.set_offset+4">Tile.set_offset(**entity**: `Any`, **tile**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Tile.set_offset+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="set_offset_x(entity : Any, tile : Any, x : Any)"></endpoint>
<signature id="Tile.set_offset_x+3">Tile.set_offset_x(**entity**: `Any`, **tile**: `Any`, **x**: `Any`)
<a class="headerlink" href="#Tile.set_offset_x+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="set_offset_y(entity : Any, tile : Any, y : Any)"></endpoint>
<signature id="Tile.set_offset_y+3">Tile.set_offset_y(**entity**: `Any`, **tile**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Tile.set_offset_y+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="get_offset_x(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_offset_x+2">Tile.get_offset_x(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_offset_x+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="get_offset_y(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_offset_y+2">Tile.get_offset_y(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_offset_y+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="reset_size(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.reset_size+2">Tile.reset_size(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.reset_size+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="set_size(entity : Any, tile : Any, x : Any, y : Any)"></endpoint>
<signature id="Tile.set_size+4">Tile.set_size(**entity**: `Any`, **tile**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Tile.set_size+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="set_size_x(entity : Any, tile : Any, x : Any)"></endpoint>
<signature id="Tile.set_size_x+3">Tile.set_size_x(**entity**: `Any`, **tile**: `Any`, **x**: `Any`)
<a class="headerlink" href="#Tile.set_size_x+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="set_size_y(entity : Any, tile : Any, y : Any)"></endpoint>
<signature id="Tile.set_size_y+3">Tile.set_size_y(**entity**: `Any`, **tile**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Tile.set_size_y+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="get_size_x(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_size_x+2">Tile.get_size_x(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_size_x+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="get_size_y(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_size_y+2">Tile.get_size_y(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_size_y+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="set_flip(entity : Any, tile : Any, x : Any, y : Any)"></endpoint>
<signature id="Tile.set_flip+4">Tile.set_flip(**entity**: `Any`, **tile**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Tile.set_flip+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="set_flip_x(entity : Any, tile : Any, flip : Any)"></endpoint>
<signature id="Tile.set_flip_x+3">Tile.set_flip_x(**entity**: `Any`, **tile**: `Any`, **flip**: `Any`)
<a class="headerlink" href="#Tile.set_flip_x+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="set_flip_y(entity : Any, tile : Any, flip : Any)"></endpoint>
<signature id="Tile.set_flip_y+3">Tile.set_flip_y(**entity**: `Any`, **tile**: `Any`, **flip**: `Any`)
<a class="headerlink" href="#Tile.set_flip_y+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="get_flip_x(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_flip_x+2">Tile.get_flip_x(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_flip_x+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="get_flip_y(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_flip_y+2">Tile.get_flip_y(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_flip_y+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="set_visual(entity : Any, tile : Any, visual : Any)"></endpoint>
<signature id="Tile.set_visual+3">Tile.set_visual(**entity**: `Any`, **tile**: `Any`, **visual**: `Any`)
<a class="headerlink" href="#Tile.set_visual+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="get_visual(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_visual+2">Tile.get_visual(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_visual+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="set_angle(entity : Any, tile : Any, angle : Any)"></endpoint>
<signature id="Tile.set_angle+3">Tile.set_angle(**entity**: `Any`, **tile**: `Any`, **angle**: `Any`)
<a class="headerlink" href="#Tile.set_angle+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="get_angle(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_angle+2">Tile.get_angle(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_angle+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="set_color(entity : Any, tile : Any, color : Any)"></endpoint>
<signature id="Tile.set_color+3">Tile.set_color(**entity**: `Any`, **tile**: `Any`, **color**: `Any`)
<a class="headerlink" href="#Tile.set_color+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tile" signature="get_color(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_color+2">Tile.get_color(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_color+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Tiles
`:::js import "luxe: system/tiles.modifier" for Tiles`
> no docs found

- [create](#Tiles.create+3)(**entity**: `Any`, **grid_size_x**: `Any`, **grid_size_y**: `Any`)
- [create](#Tiles.create+2)(**entity**: `Any`, **asset**: `Any`)
- [destroy](#Tiles.destroy)(**entity**: `Any`)
- [clear](#Tiles.clear)(**entity**: `Any`)
- [has](#Tiles.has)(**entity**: `Any`)
- [commit](#Tiles.commit)(**entity**: `Any`)
- [set_grid_size](#Tiles.set_grid_size+3)(**entity**: `Any`, **x**: `Any`, **y**: `Any`)
- [get_grid_size](#Tiles.get_grid_size)(**entity**: `Any`)
- [set_asset](#Tiles.set_asset+2)(**entity**: `Any`, **asset_id**: `Any`)
- [get_asset_id](#Tiles.get_asset_id)(**entity**: `Any`)
- [set_asset_id](#Tiles.set_asset_id+2)(**entity**: `Any`, **asset_id**: `Any`)
- [define_source](#Tiles.define_source+3)(**entity**: `Any`, **source_id**: `Any`, **material**: `Any`)
- [undefine_source](#Tiles.undefine_source+2)(**entity**: `Any`, **source_id**: `Any`)
- [has_source](#Tiles.has_source+2)(**entity**: `Any`, **source_id**: `Any`)
- [define_visual](#Tiles.define_visual+4)(**entity**: `Any`, **source_id**: `Any`, **visual_id**: `Any`, **options**: `Any`)
- [undefine_visual](#Tiles.undefine_visual+3)(**entity**: `Any`, **source_id**: `Any`, **visual_id**: `Any`)
- [has_visual](#Tiles.has_visual+2)(**entity**: `Any`, **visual_id**: `Any`)
- [get_bounds_rects](#Tiles.get_bounds_rects+3)(**entity**: `Any`, **tiles**: `Any`, **into**: `Any`)

<hr/>
<endpoint module="luxe: system/tiles.modifier" class="Tiles" signature="create(entity : Any, grid_size_x : Any, grid_size_y : Any)"></endpoint>
<signature id="Tiles.create+3">Tiles.create(**entity**: `Any`, **grid_size_x**: `Any`, **grid_size_y**: `Any`)
<a class="headerlink" href="#Tiles.create+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tiles" signature="create(entity : Any, asset : Any)"></endpoint>
<signature id="Tiles.create+2">Tiles.create(**entity**: `Any`, **asset**: `Any`)
<a class="headerlink" href="#Tiles.create+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tiles" signature="destroy(entity : Any)"></endpoint>
<signature id="Tiles.destroy">Tiles.destroy(**entity**: `Any`)
<a class="headerlink" href="#Tiles.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tiles" signature="clear(entity : Any)"></endpoint>
<signature id="Tiles.clear">Tiles.clear(**entity**: `Any`)
<a class="headerlink" href="#Tiles.clear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tiles" signature="has(entity : Any)"></endpoint>
<signature id="Tiles.has">Tiles.has(**entity**: `Any`)
<a class="headerlink" href="#Tiles.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tiles" signature="commit(entity : Any)"></endpoint>
<signature id="Tiles.commit">Tiles.commit(**entity**: `Any`)
<a class="headerlink" href="#Tiles.commit" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tiles" signature="set_grid_size(entity : Any, x : Any, y : Any)"></endpoint>
<signature id="Tiles.set_grid_size+3">Tiles.set_grid_size(**entity**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Tiles.set_grid_size+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tiles" signature="get_grid_size(entity : Any)"></endpoint>
<signature id="Tiles.get_grid_size">Tiles.get_grid_size(**entity**: `Any`)
<a class="headerlink" href="#Tiles.get_grid_size" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tiles" signature="set_asset(entity : Any, asset_id : Any)"></endpoint>
<signature id="Tiles.set_asset+2">Tiles.set_asset(**entity**: `Any`, **asset_id**: `Any`)
<a class="headerlink" href="#Tiles.set_asset+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tiles" signature="get_asset_id(entity : Any)"></endpoint>
<signature id="Tiles.get_asset_id">Tiles.get_asset_id(**entity**: `Any`)
<a class="headerlink" href="#Tiles.get_asset_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tiles" signature="set_asset_id(entity : Any, asset_id : Any)"></endpoint>
<signature id="Tiles.set_asset_id+2">Tiles.set_asset_id(**entity**: `Any`, **asset_id**: `Any`)
<a class="headerlink" href="#Tiles.set_asset_id+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tiles" signature="define_source(entity : Any, source_id : Any, material : Any)"></endpoint>
<signature id="Tiles.define_source+3">Tiles.define_source(**entity**: `Any`, **source_id**: `Any`, **material**: `Any`)
<a class="headerlink" href="#Tiles.define_source+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tiles" signature="undefine_source(entity : Any, source_id : Any)"></endpoint>
<signature id="Tiles.undefine_source+2">Tiles.undefine_source(**entity**: `Any`, **source_id**: `Any`)
<a class="headerlink" href="#Tiles.undefine_source+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tiles" signature="has_source(entity : Any, source_id : Any)"></endpoint>
<signature id="Tiles.has_source+2">Tiles.has_source(**entity**: `Any`, **source_id**: `Any`)
<a class="headerlink" href="#Tiles.has_source+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tiles" signature="define_visual(entity : Any, source_id : Any, visual_id : Any, options : Any)"></endpoint>
<signature id="Tiles.define_visual+4">Tiles.define_visual(**entity**: `Any`, **source_id**: `Any`, **visual_id**: `Any`, **options**: `Any`)
<a class="headerlink" href="#Tiles.define_visual+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tiles" signature="undefine_visual(entity : Any, source_id : Any, visual_id : Any)"></endpoint>
<signature id="Tiles.undefine_visual+3">Tiles.undefine_visual(**entity**: `Any`, **source_id**: `Any`, **visual_id**: `Any`)
<a class="headerlink" href="#Tiles.undefine_visual+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tiles" signature="has_visual(entity : Any, visual_id : Any)"></endpoint>
<signature id="Tiles.has_visual+2">Tiles.has_visual(**entity**: `Any`, **visual_id**: `Any`)
<a class="headerlink" href="#Tiles.has_visual+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/tiles.modifier" class="Tiles" signature="get_bounds_rects(entity : Any, tiles : Any, into : Any)"></endpoint>
<signature id="Tiles.get_bounds_rects+3">Tiles.get_bounds_rects(**entity**: `Any`, **tiles**: `Any`, **into**: `Any`)
<a class="headerlink" href="#Tiles.get_bounds_rects+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

