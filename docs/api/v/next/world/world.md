#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2025.1.2`)  


---

## `luxe: world/world` module

- [OldEvent](#oldevent)   
- [Wire](#wire)   
- [World](#world)   

---

### OldEvent
`:::js import "luxe: world/world" for OldEvent`
> no docs found

- [destroy](#OldEvent.destroy)
- [tick](#OldEvent.tick)

<hr/>
<endpoint module="luxe: world/world" class="OldEvent" signature="destroy"></endpoint>
<signature id="OldEvent.destroy">OldEvent.destroy
<a class="headerlink" href="#OldEvent.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="OldEvent" signature="tick"></endpoint>
<signature id="OldEvent.tick">OldEvent.tick
<a class="headerlink" href="#OldEvent.tick" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Wire
`:::js import "luxe: world/world" for Wire`
> no docs found

- `:::js var id : Num = null`
- `:::js var uuid : String = null`
- `:::js var type : String = null`
- `:::js var target : String = null`
- [create](#Wire.create)()
- [send](#Wire.send)(**entity**: `Entity`)
- [send](#Wire.send+2)(**entity**: `Entity`, **data**: `Any`)
- [prepare](#Wire.prepare)()
- [connect](#Wire.connect+3)(**world**: `World`, **uuid**: `String`, **fn**: `Fn`)
- [send](#Wire.send+3)(**world**: `World`, **uuid**: `String`, **entity**: `Entity`)
- [send](#Wire.send+4)(**world**: `World`, **uuid**: `String`, **entity**: `Entity`, **args**: `Any`)

<hr/>
<endpoint module="luxe: world/world" class="Wire" signature="create()"></endpoint>
<signature id="Wire.create">Wire.create()
<a class="headerlink" href="#Wire.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Wire`
> no docs found   

<endpoint module="luxe: world/world" class="Wire" signature="send(entity : Entity)"></endpoint>
<signature id="Wire.send">Wire.send(**entity**: `Entity`)
<a class="headerlink" href="#Wire.send" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="Wire" signature="send(entity : Entity, data : Any)"></endpoint>
<signature id="Wire.send+2">Wire.send(**entity**: `Entity`, **data**: `Any`)
<a class="headerlink" href="#Wire.send+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="Wire" signature="prepare()"></endpoint>
<signature id="Wire.prepare">Wire.prepare()
<a class="headerlink" href="#Wire.prepare" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Any`
> no docs found   

<endpoint module="luxe: world/world" class="Wire" signature="connect(world : World, uuid : String, fn : Fn)"></endpoint>
<signature id="Wire.connect+3">Wire.connect(**world**: `World`, **uuid**: `String`, **fn**: `Fn`)
<a class="headerlink" href="#Wire.connect+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="Wire" signature="send(world : World, uuid : String, entity : Entity)"></endpoint>
<signature id="Wire.send+3">Wire.send(**world**: `World`, **uuid**: `String`, **entity**: `Entity`)
<a class="headerlink" href="#Wire.send+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="Wire" signature="send(world : World, uuid : String, entity : Entity, args : Any)"></endpoint>
<signature id="Wire.send+4">Wire.send(**world**: `World`, **uuid**: `String`, **entity**: `Entity`, **args**: `Any`)
<a class="headerlink" href="#Wire.send+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### World
`:::js import "luxe: world/world" for World`
> no docs found

- [get_system](#World.get_system+2)(**world**: `World`, **modifier_id**: `String`)
- [get_scene](#World.get_scene+2)(**world**: `World`, **scene_id**: `String`)
- [get_scene_for](#World.get_scene_for+2)(**world**: `World`, **scene**: `Entity`)
- [exists](#World.exists)(**id**: `String`)
- [valid](#World.valid)(**world**: `World`)
- [get](#World.get)(**id**: `String`)
- [get_id](#World.get_id)(**world**: `World`)
- [set_id](#World.set_id+2)(**world**: `World`, **id**: `String`)
- [get_default](#World.get_default)()
- [set_default](#World.set_default)(**world**: `World`)
- [list](#World.list)(**world**: `World`)
- [list_ids](#World.list_ids)(**world**: `World`)
- [clear](#World.clear)(**world**: `World`)
- [duplicate](#World.duplicate)(**world**: `World`)
- [tag_add](#World.tag_add+2)(**world**: `Any`, **tag**: `Any`)
- [tag_remove](#World.tag_remove+2)(**world**: `Any`, **tag**: `Any`)
- [tag_has](#World.tag_has+2)(**world**: `Any`, **tag**: `Any`)
- [get_scene_roots](#World.get_scene_roots)(**world**: `World`)
- [get_delta](#World.get_delta)(**world**: `Any`)
- [tick](#World.tick+4)(**world**: `World`, **when**: `FrameWhen`, **section**: `FrameSection`, **priority**: `Num`)
- [tick](#World.tick)(**world**: `World`)
- [tick](#World.tick+2)(**world**: `World`, **delta**: `Num`)
- [schedule](#World.schedule+4)(**world**: `Any`, **time**: `Any`, **count**: `Any`, **fn**: `Any`)
- [schedule](#World.schedule+3)(**world**: `Any`, **time**: `Any`, **fn**: `Any`)
- [unschedule](#World.unschedule+2)(**world**: `Any`, **handle**: `Any`)
- [render_with_set](#World.render_with_set+4)(**world**: `Any`, **camera**: `Any`, **set**: `Any`, **target_path**: `Any`)
- [render_with_set](#World.render_with_set+5)(**world**: `Any`, **camera**: `Any`, **set**: `Any`, **target_path**: `Any`, **settings**: `Any`)
- [render_with_set](#World.render_with_set+7)(**world**: `Any`, **camera**: `Any`, **set**: `Any`, **target_path**: `Any`, **target_resource**: `Any`, **target_region**: `Any`, **settings**: `Any`)
- [render](#World.render+3)(**world**: `Any`, **camera**: `Any`, **target_path**: `Any`)
- [render](#World.render+4)(**world**: `Any`, **camera**: `Any`, **target_path**: `Any`, **settings**: `Any`)
- [render](#World.render+6)(**world**: `Any`, **camera**: `Any`, **target_path**: `Any`, **target_resource**: `Any`, **target_region**: `Any`, **settings**: `Any`)
- [render](#World.render+2)(**world**: `Any`, **desc**: `Any`)
- [render_fn](#World.render_fn+6)(**world**: `Any`, **camera**: `Any`, **target_resource**: `Any`, **target_region**: `Any`, **settings**: `Any`, **fn**: `Any`)
- [get_phases](#World.get_phases)(**world**: `World`)
- [get_phase_modifiers](#World.get_phase_modifiers+3)(**world**: `World`, **phase**: `Num`, **stage**: `Num`)
- [get_modifier_block](#World.get_modifier_block+2)(**world**: `World`, **modifier_id**: `String`)
- [get_sorted_modifiers](#World.get_sorted_modifiers)(**world**: `World`)
- [get_rate](#World.get_rate)(**world**: `Any`)
- [set_rate](#World.set_rate+2)(**world**: `Any`, **rate**: `Any`)
- [set_time](#World.set_time+2)(**world**: `Any`, **time**: `Any`)
- [time](#World.time)(**world**: `Any`)
- [render_set](#World.render_set)(**world**: `Any`)
- [render_set_add](#World.render_set_add+2)(**world**: `Any`, **geometry**: `Any`)
- [render_set_add](#World.render_set_add+3)(**world**: `Any`, **geometry**: `Any`, **entity**: `Any`)
- [render_set_remove](#World.render_set_remove+2)(**world**: `Any`, **geometry**: `Any`)
- [render_set_remove](#World.render_set_remove+3)(**world**: `Any`, **geometry**: `Any`, **entity**: `Any`)
- [render_get_entity](#World.render_get_entity+2)(**world**: `Any`, **geometry**: `Any`)
- [render_get_entity_set](#World.render_get_entity_set)(**entity**: `Any`)
- [disable](#World.disable+3)(**world**: `Any`, **state**: `Any`, **entities**: `Any`)
- [disable](#World.disable+2)(**world**: `Any`, **state**: `Any`)
- [emit](#World.emit+2)(**world**: `Any`, **tags**: `Any`)
- [emit](#World.emit+3)(**world**: `Any`, **tags**: `Any`, **data**: `Any`)
- [listen](#World.listen+3)(**world**: `Any`, **tags**: `Any`, **fn**: `Any`)
- [unlisten](#World.unlisten+3)(**world**: `Any`, **tags**: `Any`, **fn**: `Any`)
- [create](#World.create)()
- [create](#World.create)(**id**: `Any`)
- [destroy](#World.destroy)(**world**: `Any`)
- [on_register_system](#World.on_register_system+2)(**world**: `World`, **fn**: `Fn`)
- [off_register_system](#World.off_register_system+2)(**world**: `World`, **listener**: `Handle`)
- [tick_now](#World.tick_now+2)(**world**: `Any`, **delta**: `Any`)
- [live_worlds](#World.live_worlds)

<hr/>
<endpoint module="luxe: world/world" class="World" signature="get_system(world : World, modifier_id : String)"></endpoint>
<signature id="World.get_system+2">World.get_system(**world**: `World`, **modifier_id**: `String`)
<a class="headerlink" href="#World.get_system+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="get_scene(world : World, scene_id : String)"></endpoint>
<signature id="World.get_scene+2">World.get_scene(**world**: `World`, **scene_id**: `String`)
<a class="headerlink" href="#World.get_scene+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="get_scene_for(world : World, scene : Entity)"></endpoint>
<signature id="World.get_scene_for+2">World.get_scene_for(**world**: `World`, **scene**: `Entity`)
<a class="headerlink" href="#World.get_scene_for+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="exists(id : String)"></endpoint>
<signature id="World.exists">World.exists(**id**: `String`)
<a class="headerlink" href="#World.exists" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="valid(world : World)"></endpoint>
<signature id="World.valid">World.valid(**world**: `World`)
<a class="headerlink" href="#World.valid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="get(id : String)"></endpoint>
<signature id="World.get">World.get(**id**: `String`)
<a class="headerlink" href="#World.get" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js World`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="get_id(world : World)"></endpoint>
<signature id="World.get_id">World.get_id(**world**: `World`)
<a class="headerlink" href="#World.get_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="set_id(world : World, id : String)"></endpoint>
<signature id="World.set_id+2">World.set_id(**world**: `World`, **id**: `String`)
<a class="headerlink" href="#World.set_id+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="get_default()"></endpoint>
<signature id="World.get_default">World.get_default()
<a class="headerlink" href="#World.get_default" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js World`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="set_default(world : World)"></endpoint>
<signature id="World.set_default">World.set_default(**world**: `World`)
<a class="headerlink" href="#World.set_default" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="list(world : World)"></endpoint>
<signature id="World.list">World.list(**world**: `World`)
<a class="headerlink" href="#World.list" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="list_ids(world : World)"></endpoint>
<signature id="World.list_ids">World.list_ids(**world**: `World`)
<a class="headerlink" href="#World.list_ids" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="clear(world : World)"></endpoint>
<signature id="World.clear">World.clear(**world**: `World`)
<a class="headerlink" href="#World.clear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="duplicate(world : World)"></endpoint>
<signature id="World.duplicate">World.duplicate(**world**: `World`)
<a class="headerlink" href="#World.duplicate" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js World`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="tag_add(world : Any, tag : Any)"></endpoint>
<signature id="World.tag_add+2">World.tag_add(**world**: `Any`, **tag**: `Any`)
<a class="headerlink" href="#World.tag_add+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="tag_remove(world : Any, tag : Any)"></endpoint>
<signature id="World.tag_remove+2">World.tag_remove(**world**: `Any`, **tag**: `Any`)
<a class="headerlink" href="#World.tag_remove+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="tag_has(world : Any, tag : Any)"></endpoint>
<signature id="World.tag_has+2">World.tag_has(**world**: `Any`, **tag**: `Any`)
<a class="headerlink" href="#World.tag_has+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="get_scene_roots(world : World)"></endpoint>
<signature id="World.get_scene_roots">World.get_scene_roots(**world**: `World`)
<a class="headerlink" href="#World.get_scene_roots" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns a Set of scene root entities in the given world   

<endpoint module="luxe: world/world" class="World" signature="get_delta(world : Any)"></endpoint>
<signature id="World.get_delta">World.get_delta(**world**: `Any`)
<a class="headerlink" href="#World.get_delta" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="tick(world : World, when : FrameWhen, section : FrameSection, priority : Num)"></endpoint>
<signature id="World.tick+4">World.tick(**world**: `World`, **when**: `FrameWhen`, **section**: `FrameSection`, **priority**: `Num`)
<a class="headerlink" href="#World.tick+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="tick(world : World)"></endpoint>
<signature id="World.tick">World.tick(**world**: `World`)
<a class="headerlink" href="#World.tick" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="tick(world : World, delta : Num)"></endpoint>
<signature id="World.tick+2">World.tick(**world**: `World`, **delta**: `Num`)
<a class="headerlink" href="#World.tick+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="schedule(world : Any, time : Any, count : Any, fn : Any)"></endpoint>
<signature id="World.schedule+4">World.schedule(**world**: `Any`, **time**: `Any`, **count**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#World.schedule+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="schedule(world : Any, time : Any, fn : Any)"></endpoint>
<signature id="World.schedule+3">World.schedule(**world**: `Any`, **time**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#World.schedule+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="unschedule(world : Any, handle : Any)"></endpoint>
<signature id="World.unschedule+2">World.unschedule(**world**: `Any`, **handle**: `Any`)
<a class="headerlink" href="#World.unschedule+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="render_with_set(world : Any, camera : Any, set : Any, target_path : Any)"></endpoint>
<signature id="World.render_with_set+4">World.render_with_set(**world**: `Any`, **camera**: `Any`, **set**: `Any`, **target_path**: `Any`)
<a class="headerlink" href="#World.render_with_set+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="render_with_set(world : Any, camera : Any, set : Any, target_path : Any, settings : Any)"></endpoint>
<signature id="World.render_with_set+5">World.render_with_set(**world**: `Any`, **camera**: `Any`, **set**: `Any`, **target_path**: `Any`, **settings**: `Any`)
<a class="headerlink" href="#World.render_with_set+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="render_with_set(world : Any, camera : Any, set : Any, target_path : Any, target_resource : Any, target_region : Any, settings : Any)"></endpoint>
<signature id="World.render_with_set+7">World.render_with_set(**world**: `Any`, **camera**: `Any`, **set**: `Any`, **target_path**: `Any`, **target_resource**: `Any`, **target_region**: `Any`, **settings**: `Any`)
<a class="headerlink" href="#World.render_with_set+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="render(world : Any, camera : Any, target_path : Any)"></endpoint>
<signature id="World.render+3">World.render(**world**: `Any`, **camera**: `Any`, **target_path**: `Any`)
<a class="headerlink" href="#World.render+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="render(world : Any, camera : Any, target_path : Any, settings : Any)"></endpoint>
<signature id="World.render+4">World.render(**world**: `Any`, **camera**: `Any`, **target_path**: `Any`, **settings**: `Any`)
<a class="headerlink" href="#World.render+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="render(world : Any, camera : Any, target_path : Any, target_resource : Any, target_region : Any, settings : Any)"></endpoint>
<signature id="World.render+6">World.render(**world**: `Any`, **camera**: `Any`, **target_path**: `Any`, **target_resource**: `Any`, **target_region**: `Any`, **settings**: `Any`)
<a class="headerlink" href="#World.render+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="render(world : Any, desc : Any)"></endpoint>
<signature id="World.render+2">World.render(**world**: `Any`, **desc**: `Any`)
<a class="headerlink" href="#World.render+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="render_fn(world : Any, camera : Any, target_resource : Any, target_region : Any, settings : Any, fn : Any)"></endpoint>
<signature id="World.render_fn+6">World.render_fn(**world**: `Any`, **camera**: `Any`, **target_resource**: `Any`, **target_region**: `Any`, **settings**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#World.render_fn+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="get_phases(world : World)"></endpoint>
<signature id="World.get_phases">World.get_phases(**world**: `World`)
<a class="headerlink" href="#World.get_phases" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Set`
> Return the set of phases in the world, in order   

<endpoint module="luxe: world/world" class="World" signature="get_phase_modifiers(world : World, phase : Num, stage : Num)"></endpoint>
<signature id="World.get_phase_modifiers+3">World.get_phase_modifiers(**world**: `World`, **phase**: `Num`, **stage**: `Num`)
<a class="headerlink" href="#World.get_phase_modifiers+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Set`
> Return a set of modifier ids in the phase/stage   

<endpoint module="luxe: world/world" class="World" signature="get_modifier_block(world : World, modifier_id : String)"></endpoint>
<signature id="World.get_modifier_block+2">World.get_modifier_block(**world**: `World`, **modifier_id**: `String`)
<a class="headerlink" href="#World.get_modifier_block+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Block`
> Get the block for the given modifier `modifier_id` in `world`   

<endpoint module="luxe: world/world" class="World" signature="get_sorted_modifiers(world : World)"></endpoint>
<signature id="World.get_sorted_modifiers">World.get_sorted_modifiers(**world**: `World`)
<a class="headerlink" href="#World.get_sorted_modifiers" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Set`
> Get the list of modifiers in `world` (sorted by their order)   

<endpoint module="luxe: world/world" class="World" signature="get_rate(world : Any)"></endpoint>
<signature id="World.get_rate">World.get_rate(**world**: `Any`)
<a class="headerlink" href="#World.get_rate" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="set_rate(world : Any, rate : Any)"></endpoint>
<signature id="World.set_rate+2">World.set_rate(**world**: `Any`, **rate**: `Any`)
<a class="headerlink" href="#World.set_rate+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="set_time(world : Any, time : Any)"></endpoint>
<signature id="World.set_time+2">World.set_time(**world**: `Any`, **time**: `Any`)
<a class="headerlink" href="#World.set_time+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="time(world : Any)"></endpoint>
<signature id="World.time">World.time(**world**: `Any`)
<a class="headerlink" href="#World.time" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="render_set(world : Any)"></endpoint>
<signature id="World.render_set">World.render_set(**world**: `Any`)
<a class="headerlink" href="#World.render_set" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="render_set_add(world : Any, geometry : Any)"></endpoint>
<signature id="World.render_set_add+2">World.render_set_add(**world**: `Any`, **geometry**: `Any`)
<a class="headerlink" href="#World.render_set_add+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="render_set_add(world : Any, geometry : Any, entity : Any)"></endpoint>
<signature id="World.render_set_add+3">World.render_set_add(**world**: `Any`, **geometry**: `Any`, **entity**: `Any`)
<a class="headerlink" href="#World.render_set_add+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="render_set_remove(world : Any, geometry : Any)"></endpoint>
<signature id="World.render_set_remove+2">World.render_set_remove(**world**: `Any`, **geometry**: `Any`)
<a class="headerlink" href="#World.render_set_remove+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="render_set_remove(world : Any, geometry : Any, entity : Any)"></endpoint>
<signature id="World.render_set_remove+3">World.render_set_remove(**world**: `Any`, **geometry**: `Any`, **entity**: `Any`)
<a class="headerlink" href="#World.render_set_remove+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="render_get_entity(world : Any, geometry : Any)"></endpoint>
<signature id="World.render_get_entity+2">World.render_get_entity(**world**: `Any`, **geometry**: `Any`)
<a class="headerlink" href="#World.render_get_entity+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="render_get_entity_set(entity : Any)"></endpoint>
<signature id="World.render_get_entity_set">World.render_get_entity_set(**entity**: `Any`)
<a class="headerlink" href="#World.render_get_entity_set" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="disable(world : Any, state : Any, entities : Any)"></endpoint>
<signature id="World.disable+3">World.disable(**world**: `Any`, **state**: `Any`, **entities**: `Any`)
<a class="headerlink" href="#World.disable+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="disable(world : Any, state : Any)"></endpoint>
<signature id="World.disable+2">World.disable(**world**: `Any`, **state**: `Any`)
<a class="headerlink" href="#World.disable+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="emit(world : Any, tags : Any)"></endpoint>
<signature id="World.emit+2">World.emit(**world**: `Any`, **tags**: `Any`)
<a class="headerlink" href="#World.emit+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="emit(world : Any, tags : Any, data : Any)"></endpoint>
<signature id="World.emit+3">World.emit(**world**: `Any`, **tags**: `Any`, **data**: `Any`)
<a class="headerlink" href="#World.emit+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="listen(world : Any, tags : Any, fn : Any)"></endpoint>
<signature id="World.listen+3">World.listen(**world**: `Any`, **tags**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#World.listen+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="unlisten(world : Any, tags : Any, fn : Any)"></endpoint>
<signature id="World.unlisten+3">World.unlisten(**world**: `Any`, **tags**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#World.unlisten+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="create()"></endpoint>
<signature id="World.create">World.create()
<a class="headerlink" href="#World.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="create(id : Any)"></endpoint>
<signature id="World.create">World.create(**id**: `Any`)
<a class="headerlink" href="#World.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="destroy(world : Any)"></endpoint>
<signature id="World.destroy">World.destroy(**world**: `Any`)
<a class="headerlink" href="#World.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="on_register_system(world : World, fn : Fn)"></endpoint>
<signature id="World.on_register_system+2">World.on_register_system(**world**: `World`, **fn**: `Fn`)
<a class="headerlink" href="#World.on_register_system+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Handle`
> Add a function to be called when a new modifier system is added to a world.   

<endpoint module="luxe: world/world" class="World" signature="off_register_system(world : World, listener : Handle)"></endpoint>
<signature id="World.off_register_system+2">World.off_register_system(**world**: `World`, **listener**: `Handle`)
<a class="headerlink" href="#World.off_register_system+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Unsubscribe a listener from the creation of new modifier systems.   

<endpoint module="luxe: world/world" class="World" signature="tick_now(world : Any, delta : Any)"></endpoint>
<signature id="World.tick_now+2">World.tick_now(**world**: `Any`, **delta**: `Any`)
<a class="headerlink" href="#World.tick_now+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/world" class="World" signature="live_worlds"></endpoint>
<signature id="World.live_worlds">World.live_worlds
<a class="headerlink" href="#World.live_worlds" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

