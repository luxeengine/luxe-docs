#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2025.1.1`)  


---

## `luxe: system/sound.modifier` module

- [Data](#data)   
- [Sound](#sound)   
- [SoundAttenuation](#soundattenuation)   
- [System](#system)   

---

### Data
`:::js import "luxe: system/sound.modifier" for Data`
> no docs found

- `:::js var source : Asset = null`
- `:::js var bus : Asset = null`
- `:::js var volume : Num = -1`
- `:::js var pan : Num = 0`
- `:::js var pitch : Num = 1`
- `:::js var looping : Bool = false`
- `:::js var world_space : Bool = false`
- `:::js var debug_draw : Bool = true`
- `:::js var attenuation : SoundAttenuation = SoundAttenuation.none`
- `:::js var range : Float2 = [1, 10]`
- `:::js var rolloff : Num = 1`
- `:::js var simulate_doppler : Bool = false`
- `:::js var doppler_factor : Num = 1`

<hr/>
### Sound
`:::js import "luxe: system/sound.modifier" for Sound`
> no docs found


<hr/>
### SoundAttenuation
`:::js import "luxe: system/sound.modifier" for SoundAttenuation`
> no docs found

- [none](#SoundAttenuation.none)
- [inverse_distance](#SoundAttenuation.inverse_distance)
- [linear_distance](#SoundAttenuation.linear_distance)
- [exponential_distance](#SoundAttenuation.exponential_distance)

<hr/>
<endpoint module="luxe: system/sound.modifier" class="SoundAttenuation" signature="none"></endpoint>
<signature id="SoundAttenuation.none">SoundAttenuation.none
<a class="headerlink" href="#SoundAttenuation.none" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/sound.modifier" class="SoundAttenuation" signature="inverse_distance"></endpoint>
<signature id="SoundAttenuation.inverse_distance">SoundAttenuation.inverse_distance
<a class="headerlink" href="#SoundAttenuation.inverse_distance" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/sound.modifier" class="SoundAttenuation" signature="linear_distance"></endpoint>
<signature id="SoundAttenuation.linear_distance">SoundAttenuation.linear_distance
<a class="headerlink" href="#SoundAttenuation.linear_distance" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/sound.modifier" class="SoundAttenuation" signature="exponential_distance"></endpoint>
<signature id="SoundAttenuation.exponential_distance">SoundAttenuation.exponential_distance
<a class="headerlink" href="#SoundAttenuation.exponential_distance" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### System
`:::js import "luxe: system/sound.modifier" for System`
> no docs found

- `:::js var draw : Draw = null`
- `:::js var style : null = PathStyle.new`
- `:::js var last_pos : Map = {}`
- [new](#System.new)(**world**: `World`)
- [init](#System.init)(**world**: `World`)
- [editor_init](#System.editor_init)(**world**: `World`)
- [attach](#System.attach+2)(**entity**: `Entity`, **data**: `Data`)
- [detach](#System.detach+2)(**entity**: `Entity`, **data**: `Data`)
- [get_attenuation](#System.get_attenuation)(**attn**: `SoundAttenuation`)
- [tick](#System.tick)(**delta**: `Num`)
- [draw](#System.draw+2)(**entity**: `Entity`, **data**: `Data`)
- [editor_change](#System.editor_change+2)(**entity**: `Entity`, **change**: `ModifierChange`)
- [editor_tick](#System.editor_tick)(**delta**: `Num`)

<hr/>
<endpoint module="luxe: system/sound.modifier" class="System" signature="new(world : World)"></endpoint>
<signature id="System.new">System.new(**world**: `World`)
<a class="headerlink" href="#System.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js System`
> no docs found   

<endpoint module="luxe: system/sound.modifier" class="System" signature="init(world : World)"></endpoint>
<signature id="System.init">System.init(**world**: `World`)
<a class="headerlink" href="#System.init" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/sound.modifier" class="System" signature="editor_init(world : World)"></endpoint>
<signature id="System.editor_init">System.editor_init(**world**: `World`)
<a class="headerlink" href="#System.editor_init" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/sound.modifier" class="System" signature="attach(entity : Entity, data : Data)"></endpoint>
<signature id="System.attach+2">System.attach(**entity**: `Entity`, **data**: `Data`)
<a class="headerlink" href="#System.attach+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/sound.modifier" class="System" signature="detach(entity : Entity, data : Data)"></endpoint>
<signature id="System.detach+2">System.detach(**entity**: `Entity`, **data**: `Data`)
<a class="headerlink" href="#System.detach+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/sound.modifier" class="System" signature="get_attenuation(attn : SoundAttenuation)"></endpoint>
<signature id="System.get_attenuation">System.get_attenuation(**attn**: `SoundAttenuation`)
<a class="headerlink" href="#System.get_attenuation" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AudioAttenuation`
> no docs found   

<endpoint module="luxe: system/sound.modifier" class="System" signature="tick(delta : Num)"></endpoint>
<signature id="System.tick">System.tick(**delta**: `Num`)
<a class="headerlink" href="#System.tick" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/sound.modifier" class="System" signature="draw(entity : Entity, data : Data)"></endpoint>
<signature id="System.draw+2">System.draw(**entity**: `Entity`, **data**: `Data`)
<a class="headerlink" href="#System.draw+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/sound.modifier" class="System" signature="editor_change(entity : Entity, change : ModifierChange)"></endpoint>
<signature id="System.editor_change+2">System.editor_change(**entity**: `Entity`, **change**: `ModifierChange`)
<a class="headerlink" href="#System.editor_change+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/sound.modifier" class="System" signature="editor_tick(delta : Num)"></endpoint>
<signature id="System.editor_tick">System.editor_tick(**delta**: `Num`)
<a class="headerlink" href="#System.editor_tick" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

