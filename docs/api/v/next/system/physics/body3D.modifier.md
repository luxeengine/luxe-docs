#![](../../../../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2025.1.2`)  


---

## `luxe: system/physics/body3D.modifier` module

- [Body3D](#body3d)   
- [Data](#data)   
- [MotionQuality](#motionquality)   
- [MotionType](#motiontype)   
- [System](#system)   

---

### Body3D
`:::js import "luxe: system/physics/body3D.modifier" for Body3D`
> no docs found

- [unlisten](#Body3D.unlisten+2)(**entity**: `Entity`, **handle**: `Handle`)
- [listen](#Body3D.listen+2)(**entity**: `Entity`, **fn**: `Fn`)

<hr/>
<endpoint module="luxe: system/physics/body3D.modifier" class="Body3D" signature="unlisten(entity : Entity, handle : Handle)"></endpoint>
<signature id="Body3D.unlisten+2">Body3D.unlisten(**entity**: `Entity`, **handle**: `Handle`)
<a class="headerlink" href="#Body3D.unlisten+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: system/physics/body3D.modifier" class="Body3D" signature="listen(entity : Entity, fn : Fn)"></endpoint>
<signature id="Body3D.listen+2">Body3D.listen(**entity**: `Entity`, **fn**: `Fn`)
<a class="headerlink" href="#Body3D.listen+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Data
`:::js import "luxe: system/physics/body3D.modifier" for Data`
> no docs found

- `:::js var motion_type : MotionType = MotionType.is_static`
- `:::js var motion_quality : MotionQuality = MotionQuality.discrete`
- `:::js var is_sensor : Bool = false`
- `:::js var allow_sleeping : Bool = true`
- `:::js var friction : Num = 0.2`
- `:::js var restitution : Num = 0.0`
- `:::js var linear_damping : Num = 0.05`
- `:::js var angular_damping : Num = 0.05`
- `:::js var max_linear_velocity : Num = 500.0`
- `:::js var max_angular_velocity : Num = 2700`
- `:::js var gravity_factor : Num = 1`
- `:::js var mass : Num = 1`
- `:::js var lock_movement : Float3 = [0, 0, 0]`
- `:::js var lock_rotation : Float3 = [0, 0, 0]`
- `:::js var use_manifold_reduction : Bool = true`
- `:::js var allow_dynamic_or_kinematic : Bool = false`
- `:::js var collide_kinematic_vs_non_dynamic : Bool = false`
- `:::js var apply_gyroscopic_force : Bool = false`
- `:::js var enhanced_internal_edge_removal : Bool = false`
- `:::js var velocity_steps_override : Num = 0`
- `:::js var position_steps_override : Num = 0`

<hr/>
### MotionQuality
`:::js import "luxe: system/physics/body3D.modifier" for MotionQuality`
> no docs found

- [discrete](#MotionQuality.discrete)
- [linear_cast](#MotionQuality.linear_cast)

<hr/>
<endpoint module="luxe: system/physics/body3D.modifier" class="MotionQuality" signature="discrete"></endpoint>
<signature id="MotionQuality.discrete">MotionQuality.discrete
<a class="headerlink" href="#MotionQuality.discrete" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/physics/body3D.modifier" class="MotionQuality" signature="linear_cast"></endpoint>
<signature id="MotionQuality.linear_cast">MotionQuality.linear_cast
<a class="headerlink" href="#MotionQuality.linear_cast" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### MotionType
`:::js import "luxe: system/physics/body3D.modifier" for MotionType`
> no docs found

- [is_static](#MotionType.is_static)
- [is_dynamic](#MotionType.is_dynamic)
- [is_kinematic](#MotionType.is_kinematic)

<hr/>
<endpoint module="luxe: system/physics/body3D.modifier" class="MotionType" signature="is_static"></endpoint>
<signature id="MotionType.is_static">MotionType.is_static
<a class="headerlink" href="#MotionType.is_static" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/physics/body3D.modifier" class="MotionType" signature="is_dynamic"></endpoint>
<signature id="MotionType.is_dynamic">MotionType.is_dynamic
<a class="headerlink" href="#MotionType.is_dynamic" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/physics/body3D.modifier" class="MotionType" signature="is_kinematic"></endpoint>
<signature id="MotionType.is_kinematic">MotionType.is_kinematic
<a class="headerlink" href="#MotionType.is_kinematic" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### System
`:::js import "luxe: system/physics/body3D.modifier" for System`
> no docs found

- [new](#System.new)(**world**: `World`)
- [init](#System.init)(**world**: `World`)

<hr/>
<endpoint module="luxe: system/physics/body3D.modifier" class="System" signature="new(world : World)"></endpoint>
<signature id="System.new">System.new(**world**: `World`)
<a class="headerlink" href="#System.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js System`
> no docs found   

<endpoint module="luxe: system/physics/body3D.modifier" class="System" signature="init(world : World)"></endpoint>
<signature id="System.init">System.init(**world**: `World`)
<a class="headerlink" href="#System.init" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

