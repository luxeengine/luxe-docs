#![](../../../../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2025.1.2`)  


---

## `luxe: system/physics/character3D.modifier` module

- [BackFaceMode](#backfacemode)   
- [Character3D](#character3d)   
- [Data](#data)   
- [System](#system)   

---

### BackFaceMode
`:::js import "luxe: system/physics/character3D.modifier" for BackFaceMode`
> no docs found

- [ignore](#BackFaceMode.ignore)
- [collide](#BackFaceMode.collide)

<hr/>
<endpoint module="luxe: system/physics/character3D.modifier" class="BackFaceMode" signature="ignore"></endpoint>
<signature id="BackFaceMode.ignore">BackFaceMode.ignore
<a class="headerlink" href="#BackFaceMode.ignore" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/physics/character3D.modifier" class="BackFaceMode" signature="collide"></endpoint>
<signature id="BackFaceMode.collide">BackFaceMode.collide
<a class="headerlink" href="#BackFaceMode.collide" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Character3D
`:::js import "luxe: system/physics/character3D.modifier" for Character3D`
> no docs found


<hr/>
### Data
`:::js import "luxe: system/physics/character3D.modifier" for Data`
> no docs found

- `:::js var target : Link = null`
- `:::js var height : Num = 2`
- `:::js var width : Num = 1`
- `:::js var input : Float3 = [0, 0, 0]`
- `:::js var speed : Num = 1`
- `:::js var velocity : Float3 = [0, 0, 0]`
- `:::js var mass : Num = 70`
- `:::js var max_strength : Num = 100`
- `:::js var shape_offset : Float3 = [0, 0, 0]`
- `:::js var backface_mode : BackFaceMode = BackFaceMode.collide`
- `:::js var predictive_contact_distance : Num = 0.1`
- `:::js var max_collision_iterations : Num = 5`
- `:::js var max_constraint_iterations : Num = 5`
- `:::js var min_time_remaining : Num = 0.0001`
- `:::js var collision_tolerance : Num = 0.001`
- `:::js var character_padding : Num = 0.02`
- `:::js var max_hits : Num = 256`
- `:::js var hit_reduction_cos_max_angle : Num = 0.999`
- `:::js var penetration_recovery_speed : Num = 1`

<hr/>
### System
`:::js import "luxe: system/physics/character3D.modifier" for System`
> no docs found

- [new](#System.new)(**world**: `World`)
- [init](#System.init)(**world**: `World`)

<hr/>
<endpoint module="luxe: system/physics/character3D.modifier" class="System" signature="new(world : World)"></endpoint>
<signature id="System.new">System.new(**world**: `World`)
<a class="headerlink" href="#System.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js System`
> no docs found   

<endpoint module="luxe: system/physics/character3D.modifier" class="System" signature="init(world : World)"></endpoint>
<signature id="System.init">System.init(**world**: `World`)
<a class="headerlink" href="#System.init" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

