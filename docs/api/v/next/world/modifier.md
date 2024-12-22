#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2024.12.4`)  


---

## `luxe: world/modifier` module

- [Modifier](#modifier)   
- [ModifierChange](#modifierchange)   

---

### Modifier
`:::js import "luxe: world/modifier" for Modifier`
> no docs found

- [create](#Modifier.create+2)(**modifier_id**: `String`, **entity**: `Entity`)
- [destroy](#Modifier.destroy+2)(**modifier_id**: `String`, **entity**: `Entity`)
- [has](#Modifier.has+3)(**modifier_id**: `String`, **entity**: `Entity`, **ignore_removed_flag**: `Bool`)
- [has](#Modifier.has+2)(**modifier_id**: `String`, **entity**: `Entity`)
- [get_missing_expected](#Modifier.get_missing_expected+2)(**modifier_meta**: `ModifierMeta`, **entity**: `Entity`)
- [has_expected](#Modifier.has_expected+2)(**modifier_meta**: `ModifierMeta`, **entity**: `Entity`)
- [set_transient](#Modifier.set_transient+3)(**entity**: `Entity`, **modifier_id**: `String`, **state**: `Bool`)
- [set_transient](#Modifier.set_transient+4)(**entity**: `Entity`, **modifier_id**: `String`, **state**: `Bool`, **commit**: `Bool`)
- [get_transient](#Modifier.get_transient+2)(**entity**: `Entity`, **modifier_id**: `String`)
- [get](#Modifier.get+2)(**entity**: `String`, **modifier_id**: `String`)
- [get_attached_to](#Modifier.get_attached_to+2)(**world**: `World`, **modifier_id**: `String`)
- [get_meta](#Modifier.get_meta)(**modifier_id**: `String`)
- [connect](#Modifier.connect+4)(**world**: `World`, **modifier_id**: `String`, **wire**: `Num`, **fn**: `Fn`)
- [send](#Modifier.send+4)(**modifier_id**: `String`, **wire**: `Num`, **entity**: `Entity`, **data**: `Any`)
- [get_attached](#Modifier.get_attached)(**entity**: `Entity`)
- [get_modifier_id](#Modifier.get_modifier_id+2)(**world**: `World`, **block**: `Block`)

<hr/>
<endpoint module="luxe: world/modifier" class="Modifier" signature="create(modifier_id : String, entity : Entity)"></endpoint>
<signature id="Modifier.create+2">Modifier.create(**modifier_id**: `String`, **entity**: `Entity`)
<a class="headerlink" href="#Modifier.create+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: world/modifier" class="Modifier" signature="destroy(modifier_id : String, entity : Entity)"></endpoint>
<signature id="Modifier.destroy+2">Modifier.destroy(**modifier_id**: `String`, **entity**: `Entity`)
<a class="headerlink" href="#Modifier.destroy+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: world/modifier" class="Modifier" signature="has(modifier_id : String, entity : Entity, ignore_removed_flag : Bool)"></endpoint>
<signature id="Modifier.has+3">Modifier.has(**modifier_id**: `String`, **entity**: `Entity`, **ignore_removed_flag**: `Bool`)
<a class="headerlink" href="#Modifier.has+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: world/modifier" class="Modifier" signature="has(modifier_id : String, entity : Entity)"></endpoint>
<signature id="Modifier.has+2">Modifier.has(**modifier_id**: `String`, **entity**: `Entity`)
<a class="headerlink" href="#Modifier.has+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: world/modifier" class="Modifier" signature="get_missing_expected(modifier_meta : ModifierMeta, entity : Entity)"></endpoint>
<signature id="Modifier.get_missing_expected+2">Modifier.get_missing_expected(**modifier_meta**: `ModifierMeta`, **entity**: `Entity`)
<a class="headerlink" href="#Modifier.get_missing_expected+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/modifier" class="Modifier" signature="has_expected(modifier_meta : ModifierMeta, entity : Entity)"></endpoint>
<signature id="Modifier.has_expected+2">Modifier.has_expected(**modifier_meta**: `ModifierMeta`, **entity**: `Entity`)
<a class="headerlink" href="#Modifier.has_expected+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/modifier" class="Modifier" signature="set_transient(entity : Entity, modifier_id : String, state : Bool)"></endpoint>
<signature id="Modifier.set_transient+3">Modifier.set_transient(**entity**: `Entity`, **modifier_id**: `String`, **state**: `Bool`)
<a class="headerlink" href="#Modifier.set_transient+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: world/modifier" class="Modifier" signature="set_transient(entity : Entity, modifier_id : String, state : Bool, commit : Bool)"></endpoint>
<signature id="Modifier.set_transient+4">Modifier.set_transient(**entity**: `Entity`, **modifier_id**: `String`, **state**: `Bool`, **commit**: `Bool`)
<a class="headerlink" href="#Modifier.set_transient+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: world/modifier" class="Modifier" signature="get_transient(entity : Entity, modifier_id : String)"></endpoint>
<signature id="Modifier.get_transient+2">Modifier.get_transient(**entity**: `Entity`, **modifier_id**: `String`)
<a class="headerlink" href="#Modifier.get_transient+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: world/modifier" class="Modifier" signature="get(entity : String, modifier_id : String)"></endpoint>
<signature id="Modifier.get+2">Modifier.get(**entity**: `String`, **modifier_id**: `String`)
<a class="headerlink" href="#Modifier.get+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/modifier" class="Modifier" signature="get_attached_to(world : World, modifier_id : String)"></endpoint>
<signature id="Modifier.get_attached_to+2">Modifier.get_attached_to(**world**: `World`, **modifier_id**: `String`)
<a class="headerlink" href="#Modifier.get_attached_to+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/modifier" class="Modifier" signature="get_meta(modifier_id : String)"></endpoint>
<signature id="Modifier.get_meta">Modifier.get_meta(**modifier_id**: `String`)
<a class="headerlink" href="#Modifier.get_meta" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js ModifierMeta`
> no docs found   

<endpoint module="luxe: world/modifier" class="Modifier" signature="connect(world : World, modifier_id : String, wire : Num, fn : Fn)"></endpoint>
<signature id="Modifier.connect+4">Modifier.connect(**world**: `World`, **modifier_id**: `String`, **wire**: `Num`, **fn**: `Fn`)
<a class="headerlink" href="#Modifier.connect+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/modifier" class="Modifier" signature="send(modifier_id : String, wire : Num, entity : Entity, data : Any)"></endpoint>
<signature id="Modifier.send+4">Modifier.send(**modifier_id**: `String`, **wire**: `Num`, **entity**: `Entity`, **data**: `Any`)
<a class="headerlink" href="#Modifier.send+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/modifier" class="Modifier" signature="get_attached(entity : Entity)"></endpoint>
<signature id="Modifier.get_attached">Modifier.get_attached(**entity**: `Entity`)
<a class="headerlink" href="#Modifier.get_attached" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Set`
> Returns a set of attached modifier IDs for the given entity   

<endpoint module="luxe: world/modifier" class="Modifier" signature="get_modifier_id(world : World, block : Block)"></endpoint>
<signature id="Modifier.get_modifier_id+2">Modifier.get_modifier_id(**world**: `World`, **block**: `Block`)
<a class="headerlink" href="#Modifier.get_modifier_id+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Returns a modifier id (or null if not found) for the given data block   

### ModifierChange
`:::js import "luxe: world/modifier" for ModifierChange`
> no docs found

- `:::js var world : World = 0`
- `:::js var block : Block = 0`
- `:::js var instance : BlockInstance = 0`
- `:::js var field_path : String = null`
- `:::js var field_id : String = null`
- [new](#ModifierChange.new)()
- [update](#ModifierChange.update+4)(**in_world**: `World`, **in_block**: `Block`, **in_instance**: `BlockInstance`, **in_field_path**: `String`)
- [array_count](#ModifierChange.array_count)(**field**: `String`)
- [value](#ModifierChange.value)
- [value_for](#ModifierChange.value_for)(**field**: `String`)
- [value_for](#ModifierChange.value_for+2)(**field**: `String`, **array_index**: `Num`)

<hr/>
<endpoint module="luxe: world/modifier" class="ModifierChange" signature="new()"></endpoint>
<signature id="ModifierChange.new">ModifierChange.new()
<a class="headerlink" href="#ModifierChange.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js ModifierChange`
> no docs found   

<endpoint module="luxe: world/modifier" class="ModifierChange" signature="update(in_world : World, in_block : Block, in_instance : BlockInstance, in_field_path : String)"></endpoint>
<signature id="ModifierChange.update+4">ModifierChange.update(**in_world**: `World`, **in_block**: `Block`, **in_instance**: `BlockInstance`, **in_field_path**: `String`)
<a class="headerlink" href="#ModifierChange.update+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/modifier" class="ModifierChange" signature="array_count(field : String)"></endpoint>
<signature id="ModifierChange.array_count">ModifierChange.array_count(**field**: `String`)
<a class="headerlink" href="#ModifierChange.array_count" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/modifier" class="ModifierChange" signature="value"></endpoint>
<signature id="ModifierChange.value">ModifierChange.value
<a class="headerlink" href="#ModifierChange.value" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/modifier" class="ModifierChange" signature="value_for(field : String)"></endpoint>
<signature id="ModifierChange.value_for">ModifierChange.value_for(**field**: `String`)
<a class="headerlink" href="#ModifierChange.value_for" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/modifier" class="ModifierChange" signature="value_for(field : String, array_index : Num)"></endpoint>
<signature id="ModifierChange.value_for+2">ModifierChange.value_for(**field**: `String`, **array_index**: `Num`)
<a class="headerlink" href="#ModifierChange.value_for+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

