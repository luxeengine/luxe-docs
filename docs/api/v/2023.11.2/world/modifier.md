#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.11.2`)  


---

## `luxe: world/modifier` module

- [Modifier](#modifier)   

---

### Modifier
`:::js import "luxe: world/modifier" for Modifier`
> no docs found

- [create](#Modifier.create+2)(**modifier_id**: `String`, **entity**: `Entity`)
- [destroy](#Modifier.destroy+2)(**modifier_id**: `String`, **entity**: `Entity`)
- [has](#Modifier.has+2)(**modifier_id**: `String`, **entity**: `Entity`)
- [set_transient](#Modifier.set_transient+3)(**entity**: `Entity`, **modifier_id**: `String`, **state**: `Bool`)
- [get_transient](#Modifier.get_transient+2)(**entity**: `Entity`, **modifier_id**: `String`)
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

<endpoint module="luxe: world/modifier" class="Modifier" signature="has(modifier_id : String, entity : Entity)"></endpoint>
<signature id="Modifier.has+2">Modifier.has(**modifier_id**: `String`, **entity**: `Entity`)
<a class="headerlink" href="#Modifier.has+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: world/modifier" class="Modifier" signature="set_transient(entity : Entity, modifier_id : String, state : Bool)"></endpoint>
<signature id="Modifier.set_transient+3">Modifier.set_transient(**entity**: `Entity`, **modifier_id**: `String`, **state**: `Bool`)
<a class="headerlink" href="#Modifier.set_transient+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: world/modifier" class="Modifier" signature="get_transient(entity : Entity, modifier_id : String)"></endpoint>
<signature id="Modifier.get_transient+2">Modifier.get_transient(**entity**: `Entity`, **modifier_id**: `String`)
<a class="headerlink" href="#Modifier.get_transient+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
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

