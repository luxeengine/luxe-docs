#![](../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2025.1.1`)  


---

## `luxe: world` module

- [Body2D](#body2d)   
- [Body3D](#body3d)   
- [BodyEvent](#bodyevent)   
- [BodyType](#bodytype)   
- [Clock](#clock)   
- [Entity](#entity)   
- [EntityContextType](#entitycontexttype)   
- [EntityEventType](#entityeventtype)   
- [MeshColliderType](#meshcollidertype)   
- [ModifierEventType](#modifiereventtype)   
- [ModifierSystem](#modifiersystem)   
- [Modifiers](#modifiers)   
- [Overlap](#overlap)   
- [Physics2D](#physics2d)   
- [Physics3D](#physics3d)   
- [Prototype](#prototype)   
- [Scene](#scene)   
- [UI](#ui)   
- [UIBehave](#uibehave)   
- [UIClear](#uiclear)   
- [UIContain](#uicontain)   
- [UIDebugMode](#uidebugmode)   
- [UIDrop](#uidrop)   
- [UIEvent](#uievent)   
- [UIImageFit](#uiimagefit)   
- [UIImageFlags](#uiimageflags)   
- [UILayoutMode](#uilayoutmode)   
- [UIRenderMode](#uirendermode)   
- [WorldEventType](#worldeventtype)   
- [WorldRenderDesc](#worldrenderdesc)   

---

### Body2D
`:::js import "luxe: world" for Body2D`
> no docs found

- [create](#Body2D.create)(**entity**: `Any`)
- [has](#Body2D.has)(**entity**: `Any`)
- [create_collider_box](#Body2D.create_collider_box+4)(**entity**: `Any`, **center**: `Any`, **size**: `Any`, **angle**: `Any`)
- [create_collider_circle](#Body2D.create_collider_circle+3)(**entity**: `Any`, **center**: `Any`, **radius**: `Any`)
- [get_center](#Body2D.get_center)(**entity**: `Any`)
- [get_mass](#Body2D.get_mass)(**entity**: `Any`)
- [get_inertia](#Body2D.get_inertia)(**entity**: `Any`)
- [set_type](#Body2D.set_type+2)(**entity**: `Any`, **type**: `Any`)
- [get_type](#Body2D.get_type)(**entity**: `Any`)
- [set_sleeping_allowed](#Body2D.set_sleeping_allowed+2)(**entity**: `Any`, **allowed**: `Any`)
- [get_sleeping_allowed](#Body2D.get_sleeping_allowed)(**entity**: `Any`)
- [set_sleeping](#Body2D.set_sleeping+2)(**entity**: `Any`, **sleep_state**: `Any`)
- [get_sleeping](#Body2D.get_sleeping)(**entity**: `Any`)
- [set_active](#Body2D.set_active+2)(**entity**: `Any`, **active_state**: `Any`)
- [get_active](#Body2D.get_active)(**entity**: `Any`)
- [set_velocity_linear](#Body2D.set_velocity_linear+3)(**entity**: `Any`, **x**: `Any`, **y**: `Any`)
- [get_velocity_linear](#Body2D.get_velocity_linear)(**entity**: `Any`)
- [set_velocity_angular](#Body2D.set_velocity_angular+2)(**entity**: `Any`, **angle**: `Any`)
- [get_velocity_angular](#Body2D.get_velocity_angular)(**entity**: `Any`)
- [set_damping_linear](#Body2D.set_damping_linear+2)(**entity**: `Any`, **linear_damping**: `Any`)
- [get_damping_linear](#Body2D.get_damping_linear)(**entity**: `Any`)
- [set_damping_angular](#Body2D.set_damping_angular+2)(**entity**: `Any`, **angular_damping**: `Any`)
- [get_damping_angular](#Body2D.get_damping_angular)(**entity**: `Any`)
- [apply_force](#Body2D.apply_force+6)(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **x**: `Any`, **y**: `Any`, **force_awake**: `Any`)
- [apply_force](#Body2D.apply_force+5)(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **x**: `Any`, **y**: `Any`)
- [apply_force](#Body2D.apply_force+4)(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_awake**: `Any`)
- [apply_force](#Body2D.apply_force+3)(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`)
- [apply_torque](#Body2D.apply_torque+3)(**entity**: `Any`, **torque**: `Any`, **force_awake**: `Any`)
- [apply_torque](#Body2D.apply_torque+2)(**entity**: `Any`, **torque**: `Any`)
- [apply_impulse_linear](#Body2D.apply_impulse_linear+6)(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **x**: `Any`, **y**: `Any`, **force_awake**: `Any`)
- [apply_impulse_linear](#Body2D.apply_impulse_linear+5)(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **x**: `Any`, **y**: `Any`)
- [apply_impulse_angular](#Body2D.apply_impulse_angular+3)(**entity**: `Any`, **impulse**: `Any`, **force_awake**: `Any`)
- [apply_impulse_angular](#Body2D.apply_impulse_angular+2)(**entity**: `Any`, **impulse**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Body2D" signature="create(entity : Any)"></endpoint>
<signature id="Body2D.create">Body2D.create(**entity**: `Any`)
<a class="headerlink" href="#Body2D.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="has(entity : Any)"></endpoint>
<signature id="Body2D.has">Body2D.has(**entity**: `Any`)
<a class="headerlink" href="#Body2D.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="create_collider_box(entity : Any, center : Any, size : Any, angle : Any)"></endpoint>
<signature id="Body2D.create_collider_box+4">Body2D.create_collider_box(**entity**: `Any`, **center**: `Any`, **size**: `Any`, **angle**: `Any`)
<a class="headerlink" href="#Body2D.create_collider_box+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="create_collider_circle(entity : Any, center : Any, radius : Any)"></endpoint>
<signature id="Body2D.create_collider_circle+3">Body2D.create_collider_circle(**entity**: `Any`, **center**: `Any`, **radius**: `Any`)
<a class="headerlink" href="#Body2D.create_collider_circle+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="get_center(entity : Any)"></endpoint>
<signature id="Body2D.get_center">Body2D.get_center(**entity**: `Any`)
<a class="headerlink" href="#Body2D.get_center" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="get_mass(entity : Any)"></endpoint>
<signature id="Body2D.get_mass">Body2D.get_mass(**entity**: `Any`)
<a class="headerlink" href="#Body2D.get_mass" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="get_inertia(entity : Any)"></endpoint>
<signature id="Body2D.get_inertia">Body2D.get_inertia(**entity**: `Any`)
<a class="headerlink" href="#Body2D.get_inertia" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="set_type(entity : Any, type : Any)"></endpoint>
<signature id="Body2D.set_type+2">Body2D.set_type(**entity**: `Any`, **type**: `Any`)
<a class="headerlink" href="#Body2D.set_type+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="get_type(entity : Any)"></endpoint>
<signature id="Body2D.get_type">Body2D.get_type(**entity**: `Any`)
<a class="headerlink" href="#Body2D.get_type" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="set_sleeping_allowed(entity : Any, allowed : Any)"></endpoint>
<signature id="Body2D.set_sleeping_allowed+2">Body2D.set_sleeping_allowed(**entity**: `Any`, **allowed**: `Any`)
<a class="headerlink" href="#Body2D.set_sleeping_allowed+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="get_sleeping_allowed(entity : Any)"></endpoint>
<signature id="Body2D.get_sleeping_allowed">Body2D.get_sleeping_allowed(**entity**: `Any`)
<a class="headerlink" href="#Body2D.get_sleeping_allowed" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="set_sleeping(entity : Any, sleep_state : Any)"></endpoint>
<signature id="Body2D.set_sleeping+2">Body2D.set_sleeping(**entity**: `Any`, **sleep_state**: `Any`)
<a class="headerlink" href="#Body2D.set_sleeping+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="get_sleeping(entity : Any)"></endpoint>
<signature id="Body2D.get_sleeping">Body2D.get_sleeping(**entity**: `Any`)
<a class="headerlink" href="#Body2D.get_sleeping" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="set_active(entity : Any, active_state : Any)"></endpoint>
<signature id="Body2D.set_active+2">Body2D.set_active(**entity**: `Any`, **active_state**: `Any`)
<a class="headerlink" href="#Body2D.set_active+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="get_active(entity : Any)"></endpoint>
<signature id="Body2D.get_active">Body2D.get_active(**entity**: `Any`)
<a class="headerlink" href="#Body2D.get_active" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="set_velocity_linear(entity : Any, x : Any, y : Any)"></endpoint>
<signature id="Body2D.set_velocity_linear+3">Body2D.set_velocity_linear(**entity**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Body2D.set_velocity_linear+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="get_velocity_linear(entity : Any)"></endpoint>
<signature id="Body2D.get_velocity_linear">Body2D.get_velocity_linear(**entity**: `Any`)
<a class="headerlink" href="#Body2D.get_velocity_linear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="set_velocity_angular(entity : Any, angle : Any)"></endpoint>
<signature id="Body2D.set_velocity_angular+2">Body2D.set_velocity_angular(**entity**: `Any`, **angle**: `Any`)
<a class="headerlink" href="#Body2D.set_velocity_angular+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="get_velocity_angular(entity : Any)"></endpoint>
<signature id="Body2D.get_velocity_angular">Body2D.get_velocity_angular(**entity**: `Any`)
<a class="headerlink" href="#Body2D.get_velocity_angular" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="set_damping_linear(entity : Any, linear_damping : Any)"></endpoint>
<signature id="Body2D.set_damping_linear+2">Body2D.set_damping_linear(**entity**: `Any`, **linear_damping**: `Any`)
<a class="headerlink" href="#Body2D.set_damping_linear+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="get_damping_linear(entity : Any)"></endpoint>
<signature id="Body2D.get_damping_linear">Body2D.get_damping_linear(**entity**: `Any`)
<a class="headerlink" href="#Body2D.get_damping_linear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="set_damping_angular(entity : Any, angular_damping : Any)"></endpoint>
<signature id="Body2D.set_damping_angular+2">Body2D.set_damping_angular(**entity**: `Any`, **angular_damping**: `Any`)
<a class="headerlink" href="#Body2D.set_damping_angular+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="get_damping_angular(entity : Any)"></endpoint>
<signature id="Body2D.get_damping_angular">Body2D.get_damping_angular(**entity**: `Any`)
<a class="headerlink" href="#Body2D.get_damping_angular" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="apply_force(entity : Any, force_x : Any, force_y : Any, x : Any, y : Any, force_awake : Any)"></endpoint>
<signature id="Body2D.apply_force+6">Body2D.apply_force(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **x**: `Any`, **y**: `Any`, **force_awake**: `Any`)
<a class="headerlink" href="#Body2D.apply_force+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="apply_force(entity : Any, force_x : Any, force_y : Any, x : Any, y : Any)"></endpoint>
<signature id="Body2D.apply_force+5">Body2D.apply_force(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Body2D.apply_force+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="apply_force(entity : Any, force_x : Any, force_y : Any, force_awake : Any)"></endpoint>
<signature id="Body2D.apply_force+4">Body2D.apply_force(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_awake**: `Any`)
<a class="headerlink" href="#Body2D.apply_force+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="apply_force(entity : Any, force_x : Any, force_y : Any)"></endpoint>
<signature id="Body2D.apply_force+3">Body2D.apply_force(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`)
<a class="headerlink" href="#Body2D.apply_force+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="apply_torque(entity : Any, torque : Any, force_awake : Any)"></endpoint>
<signature id="Body2D.apply_torque+3">Body2D.apply_torque(**entity**: `Any`, **torque**: `Any`, **force_awake**: `Any`)
<a class="headerlink" href="#Body2D.apply_torque+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="apply_torque(entity : Any, torque : Any)"></endpoint>
<signature id="Body2D.apply_torque+2">Body2D.apply_torque(**entity**: `Any`, **torque**: `Any`)
<a class="headerlink" href="#Body2D.apply_torque+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="apply_impulse_linear(entity : Any, impulse_x : Any, impulse_y : Any, x : Any, y : Any, force_awake : Any)"></endpoint>
<signature id="Body2D.apply_impulse_linear+6">Body2D.apply_impulse_linear(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **x**: `Any`, **y**: `Any`, **force_awake**: `Any`)
<a class="headerlink" href="#Body2D.apply_impulse_linear+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="apply_impulse_linear(entity : Any, impulse_x : Any, impulse_y : Any, x : Any, y : Any)"></endpoint>
<signature id="Body2D.apply_impulse_linear+5">Body2D.apply_impulse_linear(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Body2D.apply_impulse_linear+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="apply_impulse_angular(entity : Any, impulse : Any, force_awake : Any)"></endpoint>
<signature id="Body2D.apply_impulse_angular+3">Body2D.apply_impulse_angular(**entity**: `Any`, **impulse**: `Any`, **force_awake**: `Any`)
<a class="headerlink" href="#Body2D.apply_impulse_angular+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="apply_impulse_angular(entity : Any, impulse : Any)"></endpoint>
<signature id="Body2D.apply_impulse_angular+2">Body2D.apply_impulse_angular(**entity**: `Any`, **impulse**: `Any`)
<a class="headerlink" href="#Body2D.apply_impulse_angular+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Body3D
`:::js import "luxe: world" for Body3D`
> no docs found

- [create](#Body3D.create)(**entity**: `Any`)
- [destroy](#Body3D.destroy)(**entity**: `Any`)
- [has](#Body3D.has)(**entity**: `Any`)
- [create_heightfield](#Body3D.create_heightfield+2)(**entity**: `Any`, **image**: `Any`)
- [create_collider_box](#Body3D.create_collider_box+5)(**entity**: `Any`, **center**: `Any`, **size**: `Any`, **euler**: `Any`, **physics_asset**: `Any`)
- [create_collider_box](#Body3D.create_collider_box+4)(**entity**: `Any`, **center**: `Any`, **size**: `Any`, **euler**: `Any`)
- [create_collider_sphere](#Body3D.create_collider_sphere+4)(**entity**: `Any`, **center**: `Any`, **radius**: `Any`, **physics_asset**: `Any`)
- [create_collider_sphere](#Body3D.create_collider_sphere+3)(**entity**: `Any`, **center**: `Any`, **radius**: `Any`)
- [create_collider_cylinder](#Body3D.create_collider_cylinder+4)(**entity**: `Any`, **center**: `Any`, **size**: `Any`, **physics_asset**: `Any`)
- [create_collider_cylinder](#Body3D.create_collider_cylinder+3)(**entity**: `Any`, **center**: `Any`, **size**: `Any`)
- [create_collider_capsule](#Body3D.create_collider_capsule+5)(**entity**: `Any`, **center**: `Any`, **radius**: `Any`, **height**: `Any`, **physics_asset**: `Any`)
- [create_collider_capsule](#Body3D.create_collider_capsule+4)(**entity**: `Any`, **center**: `Any`, **radius**: `Any`, **height**: `Any`)
- [create_collider_mesh](#Body3D.create_collider_mesh+7)(**entity**: `Any`, **center**: `Any`, **euler**: `Any`, **collider_type**: `MeshColliderType`, **mesh_asset**: `Any`, **mesh_level**: `Any`, **physics_asset**: `Any`)
- [create_collider_mesh](#Body3D.create_collider_mesh+6)(**entity**: `Any`, **center**: `Any`, **euler**: `Any`, **collider_type**: `MeshColliderType`, **mesh_asset**: `Any`, **mesh_level**: `Any`)
- [get_aabb](#Body3D.get_aabb)(**entity**: `Any`)
- [get_center](#Body3D.get_center)(**entity**: `Any`)
- [get_mass](#Body3D.get_mass)(**entity**: `Any`)
- [get_inertia](#Body3D.get_inertia)(**entity**: `Any`)
- [set_physics_asset](#Body3D.set_physics_asset+2)(**entity**: `Any`, **physics_asset**: `Any`)
- [on](#Body3D.on+3)(**entity**: `Any`, **type**: `BodyEvent`, **fn**: `Any`)
- [off](#Body3D.off+2)(**entity**: `Any`, **handle**: `Any`)
- [set_channel](#Body3D.set_channel+2)(**entity**: `Any`, **channel**: `Any`)
- [set_type](#Body3D.set_type+2)(**entity**: `Any`, **type**: `Any`)
- [get_type](#Body3D.get_type)(**entity**: `Any`)
- [set_sleeping_allowed](#Body3D.set_sleeping_allowed+2)(**entity**: `Any`, **allowed**: `Any`)
- [get_sleeping_allowed](#Body3D.get_sleeping_allowed)(**entity**: `Any`)
- [set_sleeping](#Body3D.set_sleeping+2)(**entity**: `Any`, **sleep_state**: `Any`)
- [get_sleeping](#Body3D.get_sleeping)(**entity**: `Any`)
- [set_active](#Body3D.set_active+2)(**entity**: `Any`, **active_state**: `Any`)
- [get_active](#Body3D.get_active)(**entity**: `Any`)
- [set_rotation_allowed](#Body3D.set_rotation_allowed+2)(**entity**: `Any`, **axis**: `Any`)
- [get_rotation_allowed](#Body3D.get_rotation_allowed)(**entity**: `Any`)
- [set_velocity_linear](#Body3D.set_velocity_linear+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [get_velocity_linear](#Body3D.get_velocity_linear)(**entity**: `Any`)
- [set_velocity_angular](#Body3D.set_velocity_angular+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [get_velocity_angular](#Body3D.get_velocity_angular)(**entity**: `Any`)
- [set_damping_linear](#Body3D.set_damping_linear+2)(**entity**: `Any`, **linear_damping**: `Any`)
- [get_damping_linear](#Body3D.get_damping_linear)(**entity**: `Any`)
- [set_damping_angular](#Body3D.set_damping_angular+2)(**entity**: `Any`, **angular_damping**: `Any`)
- [get_damping_angular](#Body3D.get_damping_angular)(**entity**: `Any`)
- [apply_force](#Body3D.apply_force+8)(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_z**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **force_awake**: `Any`)
- [apply_force](#Body3D.apply_force+7)(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_z**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [apply_force](#Body3D.apply_force+5)(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_z**: `Any`, **force_awake**: `Any`)
- [apply_force](#Body3D.apply_force+4)(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_z**: `Any`)
- [apply_torque](#Body3D.apply_torque+5)(**entity**: `Any`, **torque_x**: `Any`, **torque_y**: `Any`, **torque_z**: `Any`, **force_awake**: `Any`)
- [apply_torque](#Body3D.apply_torque+4)(**entity**: `Any`, **torque_x**: `Any`, **torque_y**: `Any`, **torque_z**: `Any`)
- [apply_impulse_linear](#Body3D.apply_impulse_linear+8)(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **impulse_z**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **force_awake**: `Any`)
- [apply_impulse_linear](#Body3D.apply_impulse_linear+7)(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **impulse_z**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [apply_impulse_angular](#Body3D.apply_impulse_angular+5)(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **impulse_z**: `Any`, **force_awake**: `Any`)
- [apply_impulse_angular](#Body3D.apply_impulse_angular+4)(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **impulse_z**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Body3D" signature="create(entity : Any)"></endpoint>
<signature id="Body3D.create">Body3D.create(**entity**: `Any`)
<a class="headerlink" href="#Body3D.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="destroy(entity : Any)"></endpoint>
<signature id="Body3D.destroy">Body3D.destroy(**entity**: `Any`)
<a class="headerlink" href="#Body3D.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="has(entity : Any)"></endpoint>
<signature id="Body3D.has">Body3D.has(**entity**: `Any`)
<a class="headerlink" href="#Body3D.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="create_heightfield(entity : Any, image : Any)"></endpoint>
<signature id="Body3D.create_heightfield+2">Body3D.create_heightfield(**entity**: `Any`, **image**: `Any`)
<a class="headerlink" href="#Body3D.create_heightfield+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="create_collider_box(entity : Any, center : Any, size : Any, euler : Any, physics_asset : Any)"></endpoint>
<signature id="Body3D.create_collider_box+5">Body3D.create_collider_box(**entity**: `Any`, **center**: `Any`, **size**: `Any`, **euler**: `Any`, **physics_asset**: `Any`)
<a class="headerlink" href="#Body3D.create_collider_box+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="create_collider_box(entity : Any, center : Any, size : Any, euler : Any)"></endpoint>
<signature id="Body3D.create_collider_box+4">Body3D.create_collider_box(**entity**: `Any`, **center**: `Any`, **size**: `Any`, **euler**: `Any`)
<a class="headerlink" href="#Body3D.create_collider_box+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="create_collider_sphere(entity : Any, center : Any, radius : Any, physics_asset : Any)"></endpoint>
<signature id="Body3D.create_collider_sphere+4">Body3D.create_collider_sphere(**entity**: `Any`, **center**: `Any`, **radius**: `Any`, **physics_asset**: `Any`)
<a class="headerlink" href="#Body3D.create_collider_sphere+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="create_collider_sphere(entity : Any, center : Any, radius : Any)"></endpoint>
<signature id="Body3D.create_collider_sphere+3">Body3D.create_collider_sphere(**entity**: `Any`, **center**: `Any`, **radius**: `Any`)
<a class="headerlink" href="#Body3D.create_collider_sphere+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="create_collider_cylinder(entity : Any, center : Any, size : Any, physics_asset : Any)"></endpoint>
<signature id="Body3D.create_collider_cylinder+4">Body3D.create_collider_cylinder(**entity**: `Any`, **center**: `Any`, **size**: `Any`, **physics_asset**: `Any`)
<a class="headerlink" href="#Body3D.create_collider_cylinder+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="create_collider_cylinder(entity : Any, center : Any, size : Any)"></endpoint>
<signature id="Body3D.create_collider_cylinder+3">Body3D.create_collider_cylinder(**entity**: `Any`, **center**: `Any`, **size**: `Any`)
<a class="headerlink" href="#Body3D.create_collider_cylinder+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="create_collider_capsule(entity : Any, center : Any, radius : Any, height : Any, physics_asset : Any)"></endpoint>
<signature id="Body3D.create_collider_capsule+5">Body3D.create_collider_capsule(**entity**: `Any`, **center**: `Any`, **radius**: `Any`, **height**: `Any`, **physics_asset**: `Any`)
<a class="headerlink" href="#Body3D.create_collider_capsule+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="create_collider_capsule(entity : Any, center : Any, radius : Any, height : Any)"></endpoint>
<signature id="Body3D.create_collider_capsule+4">Body3D.create_collider_capsule(**entity**: `Any`, **center**: `Any`, **radius**: `Any`, **height**: `Any`)
<a class="headerlink" href="#Body3D.create_collider_capsule+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="create_collider_mesh(entity : Any, center : Any, euler : Any, collider_type : MeshColliderType, mesh_asset : Any, mesh_level : Any, physics_asset : Any)"></endpoint>
<signature id="Body3D.create_collider_mesh+7">Body3D.create_collider_mesh(**entity**: `Any`, **center**: `Any`, **euler**: `Any`, **collider_type**: `MeshColliderType`, **mesh_asset**: `Any`, **mesh_level**: `Any`, **physics_asset**: `Any`)
<a class="headerlink" href="#Body3D.create_collider_mesh+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="create_collider_mesh(entity : Any, center : Any, euler : Any, collider_type : MeshColliderType, mesh_asset : Any, mesh_level : Any)"></endpoint>
<signature id="Body3D.create_collider_mesh+6">Body3D.create_collider_mesh(**entity**: `Any`, **center**: `Any`, **euler**: `Any`, **collider_type**: `MeshColliderType`, **mesh_asset**: `Any`, **mesh_level**: `Any`)
<a class="headerlink" href="#Body3D.create_collider_mesh+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_aabb(entity : Any)"></endpoint>
<signature id="Body3D.get_aabb">Body3D.get_aabb(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_aabb" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_center(entity : Any)"></endpoint>
<signature id="Body3D.get_center">Body3D.get_center(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_center" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_mass(entity : Any)"></endpoint>
<signature id="Body3D.get_mass">Body3D.get_mass(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_mass" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_inertia(entity : Any)"></endpoint>
<signature id="Body3D.get_inertia">Body3D.get_inertia(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_inertia" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="set_physics_asset(entity : Any, physics_asset : Any)"></endpoint>
<signature id="Body3D.set_physics_asset+2">Body3D.set_physics_asset(**entity**: `Any`, **physics_asset**: `Any`)
<a class="headerlink" href="#Body3D.set_physics_asset+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="on(entity : Any, type : BodyEvent, fn : Any)"></endpoint>
<signature id="Body3D.on+3">Body3D.on(**entity**: `Any`, **type**: `BodyEvent`, **fn**: `Any`)
<a class="headerlink" href="#Body3D.on+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="off(entity : Any, handle : Any)"></endpoint>
<signature id="Body3D.off+2">Body3D.off(**entity**: `Any`, **handle**: `Any`)
<a class="headerlink" href="#Body3D.off+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="set_channel(entity : Any, channel : Any)"></endpoint>
<signature id="Body3D.set_channel+2">Body3D.set_channel(**entity**: `Any`, **channel**: `Any`)
<a class="headerlink" href="#Body3D.set_channel+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="set_type(entity : Any, type : Any)"></endpoint>
<signature id="Body3D.set_type+2">Body3D.set_type(**entity**: `Any`, **type**: `Any`)
<a class="headerlink" href="#Body3D.set_type+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_type(entity : Any)"></endpoint>
<signature id="Body3D.get_type">Body3D.get_type(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_type" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="set_sleeping_allowed(entity : Any, allowed : Any)"></endpoint>
<signature id="Body3D.set_sleeping_allowed+2">Body3D.set_sleeping_allowed(**entity**: `Any`, **allowed**: `Any`)
<a class="headerlink" href="#Body3D.set_sleeping_allowed+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_sleeping_allowed(entity : Any)"></endpoint>
<signature id="Body3D.get_sleeping_allowed">Body3D.get_sleeping_allowed(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_sleeping_allowed" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="set_sleeping(entity : Any, sleep_state : Any)"></endpoint>
<signature id="Body3D.set_sleeping+2">Body3D.set_sleeping(**entity**: `Any`, **sleep_state**: `Any`)
<a class="headerlink" href="#Body3D.set_sleeping+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_sleeping(entity : Any)"></endpoint>
<signature id="Body3D.get_sleeping">Body3D.get_sleeping(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_sleeping" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="set_active(entity : Any, active_state : Any)"></endpoint>
<signature id="Body3D.set_active+2">Body3D.set_active(**entity**: `Any`, **active_state**: `Any`)
<a class="headerlink" href="#Body3D.set_active+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_active(entity : Any)"></endpoint>
<signature id="Body3D.get_active">Body3D.get_active(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_active" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="set_rotation_allowed(entity : Any, axis : Any)"></endpoint>
<signature id="Body3D.set_rotation_allowed+2">Body3D.set_rotation_allowed(**entity**: `Any`, **axis**: `Any`)
<a class="headerlink" href="#Body3D.set_rotation_allowed+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_rotation_allowed(entity : Any)"></endpoint>
<signature id="Body3D.get_rotation_allowed">Body3D.get_rotation_allowed(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_rotation_allowed" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="set_velocity_linear(entity : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Body3D.set_velocity_linear+4">Body3D.set_velocity_linear(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Body3D.set_velocity_linear+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_velocity_linear(entity : Any)"></endpoint>
<signature id="Body3D.get_velocity_linear">Body3D.get_velocity_linear(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_velocity_linear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="set_velocity_angular(entity : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Body3D.set_velocity_angular+4">Body3D.set_velocity_angular(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Body3D.set_velocity_angular+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_velocity_angular(entity : Any)"></endpoint>
<signature id="Body3D.get_velocity_angular">Body3D.get_velocity_angular(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_velocity_angular" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="set_damping_linear(entity : Any, linear_damping : Any)"></endpoint>
<signature id="Body3D.set_damping_linear+2">Body3D.set_damping_linear(**entity**: `Any`, **linear_damping**: `Any`)
<a class="headerlink" href="#Body3D.set_damping_linear+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_damping_linear(entity : Any)"></endpoint>
<signature id="Body3D.get_damping_linear">Body3D.get_damping_linear(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_damping_linear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="set_damping_angular(entity : Any, angular_damping : Any)"></endpoint>
<signature id="Body3D.set_damping_angular+2">Body3D.set_damping_angular(**entity**: `Any`, **angular_damping**: `Any`)
<a class="headerlink" href="#Body3D.set_damping_angular+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_damping_angular(entity : Any)"></endpoint>
<signature id="Body3D.get_damping_angular">Body3D.get_damping_angular(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_damping_angular" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="apply_force(entity : Any, force_x : Any, force_y : Any, force_z : Any, x : Any, y : Any, z : Any, force_awake : Any)"></endpoint>
<signature id="Body3D.apply_force+8">Body3D.apply_force(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_z**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **force_awake**: `Any`)
<a class="headerlink" href="#Body3D.apply_force+8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="apply_force(entity : Any, force_x : Any, force_y : Any, force_z : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Body3D.apply_force+7">Body3D.apply_force(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_z**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Body3D.apply_force+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="apply_force(entity : Any, force_x : Any, force_y : Any, force_z : Any, force_awake : Any)"></endpoint>
<signature id="Body3D.apply_force+5">Body3D.apply_force(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_z**: `Any`, **force_awake**: `Any`)
<a class="headerlink" href="#Body3D.apply_force+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="apply_force(entity : Any, force_x : Any, force_y : Any, force_z : Any)"></endpoint>
<signature id="Body3D.apply_force+4">Body3D.apply_force(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_z**: `Any`)
<a class="headerlink" href="#Body3D.apply_force+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="apply_torque(entity : Any, torque_x : Any, torque_y : Any, torque_z : Any, force_awake : Any)"></endpoint>
<signature id="Body3D.apply_torque+5">Body3D.apply_torque(**entity**: `Any`, **torque_x**: `Any`, **torque_y**: `Any`, **torque_z**: `Any`, **force_awake**: `Any`)
<a class="headerlink" href="#Body3D.apply_torque+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="apply_torque(entity : Any, torque_x : Any, torque_y : Any, torque_z : Any)"></endpoint>
<signature id="Body3D.apply_torque+4">Body3D.apply_torque(**entity**: `Any`, **torque_x**: `Any`, **torque_y**: `Any`, **torque_z**: `Any`)
<a class="headerlink" href="#Body3D.apply_torque+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="apply_impulse_linear(entity : Any, impulse_x : Any, impulse_y : Any, impulse_z : Any, x : Any, y : Any, z : Any, force_awake : Any)"></endpoint>
<signature id="Body3D.apply_impulse_linear+8">Body3D.apply_impulse_linear(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **impulse_z**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **force_awake**: `Any`)
<a class="headerlink" href="#Body3D.apply_impulse_linear+8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="apply_impulse_linear(entity : Any, impulse_x : Any, impulse_y : Any, impulse_z : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Body3D.apply_impulse_linear+7">Body3D.apply_impulse_linear(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **impulse_z**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Body3D.apply_impulse_linear+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="apply_impulse_angular(entity : Any, impulse_x : Any, impulse_y : Any, impulse_z : Any, force_awake : Any)"></endpoint>
<signature id="Body3D.apply_impulse_angular+5">Body3D.apply_impulse_angular(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **impulse_z**: `Any`, **force_awake**: `Any`)
<a class="headerlink" href="#Body3D.apply_impulse_angular+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="apply_impulse_angular(entity : Any, impulse_x : Any, impulse_y : Any, impulse_z : Any)"></endpoint>
<signature id="Body3D.apply_impulse_angular+4">Body3D.apply_impulse_angular(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **impulse_z**: `Any`)
<a class="headerlink" href="#Body3D.apply_impulse_angular+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### BodyEvent
`:::js import "luxe: world" for BodyEvent`
> no docs found

- [invalid](#BodyEvent.invalid)
- [overlap](#BodyEvent.overlap)
- [collide](#BodyEvent.collide)
- [name](#BodyEvent.name)(**value**: `Any`)
- [from_string](#BodyEvent.from_string)(**value**: `Any`)

<hr/>
<endpoint module="luxe: world" class="BodyEvent" signature="invalid"></endpoint>
<signature id="BodyEvent.invalid">BodyEvent.invalid
<a class="headerlink" href="#BodyEvent.invalid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="BodyEvent" signature="overlap"></endpoint>
<signature id="BodyEvent.overlap">BodyEvent.overlap
<a class="headerlink" href="#BodyEvent.overlap" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="BodyEvent" signature="collide"></endpoint>
<signature id="BodyEvent.collide">BodyEvent.collide
<a class="headerlink" href="#BodyEvent.collide" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="BodyEvent" signature="name(value : Any)"></endpoint>
<signature id="BodyEvent.name">BodyEvent.name(**value**: `Any`)
<a class="headerlink" href="#BodyEvent.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="BodyEvent" signature="from_string(value : Any)"></endpoint>
<signature id="BodyEvent.from_string">BodyEvent.from_string(**value**: `Any`)
<a class="headerlink" href="#BodyEvent.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### BodyType
`:::js import "luxe: world" for BodyType`
> no docs found

- [static_body](#BodyType.static_body)
- [dynamic_body](#BodyType.dynamic_body)
- [kinematic_body](#BodyType.kinematic_body)
- [name](#BodyType.name)(**value**: `Any`)
- [from_string](#BodyType.from_string)(**value**: `Any`)

<hr/>
<endpoint module="luxe: world" class="BodyType" signature="static_body"></endpoint>
<signature id="BodyType.static_body">BodyType.static_body
<a class="headerlink" href="#BodyType.static_body" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="BodyType" signature="dynamic_body"></endpoint>
<signature id="BodyType.dynamic_body">BodyType.dynamic_body
<a class="headerlink" href="#BodyType.dynamic_body" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="BodyType" signature="kinematic_body"></endpoint>
<signature id="BodyType.kinematic_body">BodyType.kinematic_body
<a class="headerlink" href="#BodyType.kinematic_body" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="BodyType" signature="name(value : Any)"></endpoint>
<signature id="BodyType.name">BodyType.name(**value**: `Any`)
<a class="headerlink" href="#BodyType.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="BodyType" signature="from_string(value : Any)"></endpoint>
<signature id="BodyType.from_string">BodyType.from_string(**value**: `Any`)
<a class="headerlink" href="#BodyType.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Clock
`:::js import "luxe: world" for Clock`
> no docs found

- [create](#Clock.create+3)(**world**: `Any`, **rate**: `Any`, **paused**: `Any`)
- [create](#Clock.create+2)(**world**: `Any`, **rate**: `Any`)
- [time](#Clock.time+2)(**world**: `Any`, **clock**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Clock" signature="create(world : Any, rate : Any, paused : Any)"></endpoint>
<signature id="Clock.create+3">Clock.create(**world**: `Any`, **rate**: `Any`, **paused**: `Any`)
<a class="headerlink" href="#Clock.create+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Clock" signature="create(world : Any, rate : Any)"></endpoint>
<signature id="Clock.create+2">Clock.create(**world**: `Any`, **rate**: `Any`)
<a class="headerlink" href="#Clock.create+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Clock" signature="time(world : Any, clock : Any)"></endpoint>
<signature id="Clock.time+2">Clock.time(**world**: `Any`, **clock**: `Any`)
<a class="headerlink" href="#Clock.time+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Entity
`:::js import "luxe: world" for Entity`
> Anything that exists in a world is a `entity`. The entity itself is just a handle (represented by a number) with which modifiers and a name can be associated. Entities are very lightweight, so creating and destroying many of them usually isnt a concern.
> 
> An entity in itself does not have a transform (you can attach the `transform` modifier to it to gain that) or any kind of hierarchy (different implicit hierarchies can result from modifiers).
> Entities can be created manually in code, or loaded as Scenes or Prototypes.

- [none](#Entity.none)
- [create](#Entity.create)(**world**: `World`)
- [create](#Entity.create+2)(**world**: `World`, **name**: `String`)
- [valid](#Entity.valid)(**entity**: `Entity`)
- [valid_handle](#Entity.valid_handle)(**entity**: `Entity`)
- [get_world](#Entity.get_world)(**entity**: `Entity`)
- [get](#Entity.get)(**uuid**: `String`)
- [get_addressed_in](#Entity.get_addressed_in+2)(**context_root**: `Entity`, **address**: `List`)
- [get_addressed](#Entity.get_addressed+2)(**relative_to**: `Entity`, **address**: `List`)
- [resolve](#Entity.resolve+2)(**relative_to**: `Entity`, **address**: `List`)
- [get_addressed_context](#Entity.get_addressed_context+2)(**relative_to**: `Entity`, **address**: `List`)
- [get_named](#Entity.get_named+2)(**world**: `World`, **name**: `String`)
- [get_named_all](#Entity.get_named_all+2)(**world**: `World`, **name**: `String`)
- [get_named_in](#Entity.get_named_in+2)(**context**: `Entity`, **name**: `String`)
- [get_named_all_in](#Entity.get_named_all_in+2)(**context**: `Entity`, **name**: `String`)
- [get_name](#Entity.get_name)(**entity**: `Entity`)
- [name](#Entity.name)(**entity**: `Entity`)
- [get_folder](#Entity.get_folder)(**entity**: `Entity`)
- [set_folder](#Entity.set_folder+2)(**entity**: `Entity`, **folder**: `String`)
- [get_asset_id](#Entity.get_asset_id)(**entity**: `Entity`)
- [set_asset_id](#Entity.set_asset_id+2)(**entity**: `Entity`, **asset_id**: `String`)
- [get_context_asset_id](#Entity.get_context_asset_id)(**entity**: `Entity`)
- [set_context_asset_id](#Entity.set_context_asset_id+2)(**entity**: `Entity`, **asset_id**: `String`)
- [get_context_type](#Entity.get_context_type)(**entity**: `Entity`)
- [get_context_instance_uuid](#Entity.get_context_instance_uuid)(**entity**: `Entity`)
- [get_context](#Entity.get_context)(**entity**: `Entity`)
- [get_context_origin](#Entity.get_context_origin)(**entity**: `Entity`)
- [get_context_address](#Entity.get_context_address+2)(**entity**: `Entity`, **context**: `Entity`)
- [list_context_all](#Entity.list_context_all)(**context**: `Entity`)
- [list_context_direct](#Entity.list_context_direct)(**context**: `Entity`)
- [get_context_id](#Entity.get_context_id)(**context**: `Entity`)
- [get_origin_address](#Entity.get_origin_address)(**entity**: `Entity`)
- [get_address](#Entity.get_address)(**entity**: `Entity`)
- [get_context_is_direct](#Entity.get_context_is_direct+2)(**context**: `Entity`, **entity**: `Entity`)
- [init_into_context](#Entity.init_into_context+2)(**entity**: `Entity`, **context**: `Entity`)
- [init_into_context](#Entity.init_into_context+3)(**entity**: `Entity`, **context**: `Entity`, **address_uuid**: `UUID`)
- [note_add](#Entity.note_add+2)(**entity**: `Entity`, **note**: `String`)
- [note_remove](#Entity.note_remove+2)(**entity**: `Entity`, **note**: `String`)
- [note_has](#Entity.note_has+2)(**entity**: `Entity`, **note**: `String`)
- [notes](#Entity.notes)(**entity**: `Entity`)
- [set_name](#Entity.set_name+2)(**entity**: `Entity`, **name**: `String`)
- [get_uuid](#Entity.get_uuid)(**entity**: `Entity`)
- [set_uuid](#Entity.set_uuid+2)(**entity**: `Entity`, **uuid_string**: `String`)
- [destroy](#Entity.destroy)(**entity**: `Entity`)
- [duplicate](#Entity.duplicate)(**entity**: `Entity`)
- [duplicate](#Entity.duplicate+2)(**entity**: `Entity`, **world**: `World`)

<hr/>
<endpoint module="luxe: world" class="Entity" signature="none"></endpoint>
<signature id="Entity.none">Entity.none
<a class="headerlink" href="#Entity.none" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> An entity representing no value. Note, not for comparisons! Use Entity.valid(entity) for that   

<endpoint module="luxe: world" class="Entity" signature="create(world : World)"></endpoint>
<signature id="Entity.create">Entity.create(**world**: `World`)
<a class="headerlink" href="#Entity.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> Creates a new `entity` in the given `world`.
> 
>   ```js
>   var player = Entity.create(app.world)
>   ```   

<endpoint module="luxe: world" class="Entity" signature="create(world : World, name : String)"></endpoint>
<signature id="Entity.create+2">Entity.create(**world**: `World`, **name**: `String`)
<a class="headerlink" href="#Entity.create+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> Creates a new `entity` in the given `world` with the specified `String` name.
> 
>   ```js
>   var player = Entity.create(app.world, "player")
>   ```   

<endpoint module="luxe: world" class="Entity" signature="valid(entity : Entity)"></endpoint>
<signature id="Entity.valid">Entity.valid(**entity**: `Entity`)
<a class="headerlink" href="#Entity.valid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Checks if the given variable references a valid `entity`.
> 
>   ```js
>   var player = Entity.get_named(app.world, "player")
>   if (Entity.valid(player)) {
>     Log.print("Got the player entity!")
>   }
>   ```   

<endpoint module="luxe: world" class="Entity" signature="valid_handle(entity : Entity)"></endpoint>
<signature id="Entity.valid_handle">Entity.valid_handle(**entity**: `Entity`)
<a class="headerlink" href="#Entity.valid_handle" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Checks if the given variable references a valid `entity` handle.
> Note that when an entity is destroyed, it marks the entity as invalid 
> for Entity.valid(), but the destroy happens at the end of the frame.
> This means during that frame the entity can still be "live", but not valid.
> 
> This is mostly useful in the detach handlers, where Entity.valid would return false.   

<endpoint module="luxe: world" class="Entity" signature="get_world(entity : Entity)"></endpoint>
<signature id="Entity.get_world">Entity.get_world(**entity**: `Entity`)
<a class="headerlink" href="#Entity.get_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js World`
> Get the `world` a given `entity` belongs to
> 
>   ```js
>   var world = Entity.get_world(entity)
>   ```   

<endpoint module="luxe: world" class="Entity" signature="get(uuid : String)"></endpoint>
<signature id="Entity.get">Entity.get(**uuid**: `String`)
<a class="headerlink" href="#Entity.get" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> Get the entity with a given UUID. Since an entity can have 
> a name that is shared by several entities in the same world, 
> the unique ID of an entity is used to locate exactly one entity.
> Generally, no two entities will have the same UUID.
> 
>   ```js
>   var entity = Entity.get("5b01869b-fd59-4f2c-892f-4c0b726c79a2")
> 
>   if (Entity.valid(entity)) {
>     Log.print("found entity")
>   }
>   ```   

<endpoint module="luxe: world" class="Entity" signature="get_addressed_in(context_root : Entity, address : List)"></endpoint>
<signature id="Entity.get_addressed_in+2">Entity.get_addressed_in(**context_root**: `Entity`, **address**: `List`)
<a class="headerlink" href="#Entity.get_addressed_in+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> Find an entity by `address` in the given context (only). 
> The address is a list of uuids, and the context is a scene root entity, 
> or prototype root entity.   

<endpoint module="luxe: world" class="Entity" signature="get_addressed(relative_to : Entity, address : List)"></endpoint>
<signature id="Entity.get_addressed+2">Entity.get_addressed(**relative_to**: `Entity`, **address**: `List`)
<a class="headerlink" href="#Entity.get_addressed+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> Find an entity by `address` relative to the given entity, and will search upward
> through all contexts in the tree to try and find the addressed entity.
> The address is a list of uuids.   

<endpoint module="luxe: world" class="Entity" signature="resolve(relative_to : Entity, address : List)"></endpoint>
<signature id="Entity.resolve+2">Entity.resolve(**relative_to**: `Entity`, **address**: `List`)
<a class="headerlink" href="#Entity.resolve+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> Find an entity by `address` relative to the given entity, and will search upward
> through all contexts in the tree to try and find the addressed entity.
> The address is a list of uuids called a `Link` typically.
> Alias for `Entity.get_addressed`.   

<endpoint module="luxe: world" class="Entity" signature="get_addressed_context(relative_to : Entity, address : List)"></endpoint>
<signature id="Entity.get_addressed_context+2">Entity.get_addressed_context(**relative_to**: `Entity`, **address**: `List`)
<a class="headerlink" href="#Entity.get_addressed_context+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> Find an entity by `address` relative to the given entity, and will search upward
> through all contexts in the tree to try and find the addressed entity - but this
> function will return the context it was found in (e.g the context the address is for).
> The address is a list of uuids.   

<endpoint module="luxe: world" class="Entity" signature="get_named(world : World, name : String)"></endpoint>
<signature id="Entity.get_named+2">Entity.get_named(**world**: `World`, **name**: `String`)
<a class="headerlink" href="#Entity.get_named+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> Get the first `entity` from the given `world` with the name `name`.
> Which entity is returned is unspecified if there are multiple with the same name.
> If you need to test further use `Entity.get_named_all`. Returns null if no
> entity is found by that name.
> 
>   ```js
>   var player = Entity.get_named(app.world, "player")
>   ```   

<endpoint module="luxe: world" class="Entity" signature="get_named_all(world : World, name : String)"></endpoint>
<signature id="Entity.get_named_all+2">Entity.get_named_all(**world**: `World`, **name**: `String`)
<a class="headerlink" href="#Entity.get_named_all+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> Get a list of all `entities` from the given `world` with the name `name`.
> Returns a list of entities with an unspecified order. Returns an empty list
> if no entities are found.
> 
>   ```js
>   var list = Entity.get_named_all(app.world, "fern")
>   Log.print("There are %(list.count) ferns in this forest!")
>   ```   

<endpoint module="luxe: world" class="Entity" signature="get_named_in(context : Entity, name : String)"></endpoint>
<signature id="Entity.get_named_in+2">Entity.get_named_in(**context**: `Entity`, **name**: `String`)
<a class="headerlink" href="#Entity.get_named_in+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> Get the first `entity` from the given `context` with the name `name`.
> The context is a scene root or a prototype root entity.
> Which entity is returned is unspecified if there are multiple with the same name.
> If you need to test further use `Entity.get_named_all`. Returns null if no
> entity is found by that name.
> 
>   ```js
>   var prototype = Prototype.create(world, Asset.prototype("proto/example"))
>   var item = Entity.get_named_in(prototype, "item")
>   ```   

<endpoint module="luxe: world" class="Entity" signature="get_named_all_in(context : Entity, name : String)"></endpoint>
<signature id="Entity.get_named_all_in+2">Entity.get_named_all_in(**context**: `Entity`, **name**: `String`)
<a class="headerlink" href="#Entity.get_named_all_in+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> Get a list of all `entities` from the given `context` with the name `name`.
> The context is a scene root or a prototype root entity.
> Returns a list of entities with an unspecified order. Returns an empty list
> if no entities are found.
> 
>   ```js
>     var scene = Scene.load(world, Asset.scene("scene/example")) {
>     var list = Entity.get_named_all_in(scene, "fern")
>     Log.print("There are %(list.count) ferns in this forest!")
>   }
>   ```   

<endpoint module="luxe: world" class="Entity" signature="get_name(entity : Entity)"></endpoint>
<signature id="Entity.get_name">Entity.get_name(**entity**: `Entity`)
<a class="headerlink" href="#Entity.get_name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js StringID`
> Get the name of a given `entity` as a hashed string ID.
> Use `import "luxe: assets" for Strings` with `Strings.get(name)`
> to convert to a string. :note: this ID nuance is wip.
> 
>   ```js
>   Entity.set_name(player, "player")
>   var name_id = Entity.get_name(player)
>   var name = Strings.get(name_id)
>   Log.print("Entity name is `%(name)`!")
>   // prints "Entity name is `player`"
>   ```   

<endpoint module="luxe: world" class="Entity" signature="name(entity : Entity)"></endpoint>
<signature id="Entity.name">Entity.name(**entity**: `Entity`)
<a class="headerlink" href="#Entity.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Get the name of a given `entity` as a string.
> Supports invalid entities (returns `<invalid>`).
> 
>   ```js
>   Entity.set_name(player, "player")
>   var name = Entity.name(player)
>   Log.print("Entity name is `%(name)`!")
>   // prints "Entity name is `player`"
>   ```   

<endpoint module="luxe: world" class="Entity" signature="get_folder(entity : Entity)"></endpoint>
<signature id="Entity.get_folder">Entity.get_folder(**entity**: `Entity`)
<a class="headerlink" href="#Entity.get_folder" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> get the folder of this entity (used for nested display in a world outliner)   

<endpoint module="luxe: world" class="Entity" signature="set_folder(entity : Entity, folder : String)"></endpoint>
<signature id="Entity.set_folder+2">Entity.set_folder(**entity**: `Entity`, **folder**: `String`)
<a class="headerlink" href="#Entity.set_folder+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> set the folder of this entity (used for nested display in a world outliner)   

<endpoint module="luxe: world" class="Entity" signature="get_asset_id(entity : Entity)"></endpoint>
<signature id="Entity.get_asset_id">Entity.get_asset_id(**entity**: `Entity`)
<a class="headerlink" href="#Entity.get_asset_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> get the asset ID of this entity (if it has one)   

<endpoint module="luxe: world" class="Entity" signature="set_asset_id(entity : Entity, asset_id : String)"></endpoint>
<signature id="Entity.set_asset_id+2">Entity.set_asset_id(**entity**: `Entity`, **asset_id**: `String`)
<a class="headerlink" href="#Entity.set_asset_id+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> set the asset ID of this entity (used for e.g editor)   

<endpoint module="luxe: world" class="Entity" signature="get_context_asset_id(entity : Entity)"></endpoint>
<signature id="Entity.get_context_asset_id">Entity.get_context_asset_id(**entity**: `Entity`)
<a class="headerlink" href="#Entity.get_context_asset_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> get the context asset ID of this entity (if it has one)   

<endpoint module="luxe: world" class="Entity" signature="set_context_asset_id(entity : Entity, asset_id : String)"></endpoint>
<signature id="Entity.set_context_asset_id+2">Entity.set_context_asset_id(**entity**: `Entity`, **asset_id**: `String`)
<a class="headerlink" href="#Entity.set_context_asset_id+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> set the context asset ID of this entity (used for e.g editor)   

<endpoint module="luxe: world" class="Entity" signature="get_context_type(entity : Entity)"></endpoint>
<signature id="Entity.get_context_type">Entity.get_context_type(**entity**: `Entity`)
<a class="headerlink" href="#Entity.get_context_type" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js EntityContextType`
> get the context type for an entity   

<endpoint module="luxe: world" class="Entity" signature="get_context_instance_uuid(entity : Entity)"></endpoint>
<signature id="Entity.get_context_instance_uuid">Entity.get_context_instance_uuid(**entity**: `Entity`)
<a class="headerlink" href="#Entity.get_context_instance_uuid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> get the context uuid for a given entity. Entity should be EntityContextType `scene` or `prototype` or null is returned   

<endpoint module="luxe: world" class="Entity" signature="get_context(entity : Entity)"></endpoint>
<signature id="Entity.get_context">Entity.get_context(**entity**: `Entity`)
<a class="headerlink" href="#Entity.get_context" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> get the context this entity belongs to if any   

<endpoint module="luxe: world" class="Entity" signature="get_context_origin(entity : Entity)"></endpoint>
<signature id="Entity.get_context_origin">Entity.get_context_origin(**entity**: `Entity`)
<a class="headerlink" href="#Entity.get_context_origin" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> get the context that this entity originated from. For example if a scene was loaded and inside it there was a prototype and so on, the scene is the origin.   

<endpoint module="luxe: world" class="Entity" signature="get_context_address(entity : Entity, context : Entity)"></endpoint>
<signature id="Entity.get_context_address+2">Entity.get_context_address(**entity**: `Entity`, **context**: `Entity`)
<a class="headerlink" href="#Entity.get_context_address+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> get the address of the entity within a given context.   

<endpoint module="luxe: world" class="Entity" signature="list_context_all(context : Entity)"></endpoint>
<signature id="Entity.list_context_all">Entity.list_context_all(**context**: `Entity`)
<a class="headerlink" href="#Entity.list_context_all" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Set`
> Get all the entities this context created as a Set of entities.   

<endpoint module="luxe: world" class="Entity" signature="list_context_direct(context : Entity)"></endpoint>
<signature id="Entity.list_context_direct">Entity.list_context_direct(**context**: `Entity`)
<a class="headerlink" href="#Entity.list_context_direct" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Set`
> Get all the entities this context created directly (rather than indirectly) as a Set of entities.   

<endpoint module="luxe: world" class="Entity" signature="get_context_id(context : Entity)"></endpoint>
<signature id="Entity.get_context_id">Entity.get_context_id(**context**: `Entity`)
<a class="headerlink" href="#Entity.get_context_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> get the id of the given context.   

<endpoint module="luxe: world" class="Entity" signature="get_origin_address(entity : Entity)"></endpoint>
<signature id="Entity.get_origin_address">Entity.get_origin_address(**entity**: `Entity`)
<a class="headerlink" href="#Entity.get_origin_address" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> get the address of the entity within it's origin context.   

<endpoint module="luxe: world" class="Entity" signature="get_address(entity : Entity)"></endpoint>
<signature id="Entity.get_address">Entity.get_address(**entity**: `Entity`)
<a class="headerlink" href="#Entity.get_address" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> get the address of the entity within it's origin context.   

<endpoint module="luxe: world" class="Entity" signature="get_context_is_direct(context : Entity, entity : Entity)"></endpoint>
<signature id="Entity.get_context_is_direct+2">Entity.get_context_is_direct(**context**: `Entity`, **entity**: `Entity`)
<a class="headerlink" href="#Entity.get_context_is_direct+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> returns true if the given entity is a direct entity in the context. This includes prototype roots spawned into the context (use context type to filter them out).   

<endpoint module="luxe: world" class="Entity" signature="init_into_context(entity : Entity, context : Entity)"></endpoint>
<signature id="Entity.init_into_context+2">Entity.init_into_context(**entity**: `Entity`, **context**: `Entity`)
<a class="headerlink" href="#Entity.init_into_context+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Initialize an entity into an existing context (typically editor related)   

<endpoint module="luxe: world" class="Entity" signature="init_into_context(entity : Entity, context : Entity, address_uuid : UUID)"></endpoint>
<signature id="Entity.init_into_context+3">Entity.init_into_context(**entity**: `Entity`, **context**: `Entity`, **address_uuid**: `UUID`)
<a class="headerlink" href="#Entity.init_into_context+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Initialize an entity into an existing context with an address uuid (typically editor related)   

<endpoint module="luxe: world" class="Entity" signature="note_add(entity : Entity, note : String)"></endpoint>
<signature id="Entity.note_add+2">Entity.note_add(**entity**: `Entity`, **note**: `String`)
<a class="headerlink" href="#Entity.note_add+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> add a note to this entity (like a lower level tag)   

<endpoint module="luxe: world" class="Entity" signature="note_remove(entity : Entity, note : String)"></endpoint>
<signature id="Entity.note_remove+2">Entity.note_remove(**entity**: `Entity`, **note**: `String`)
<a class="headerlink" href="#Entity.note_remove+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> remove a note to this entity   

<endpoint module="luxe: world" class="Entity" signature="note_has(entity : Entity, note : String)"></endpoint>
<signature id="Entity.note_has+2">Entity.note_has(**entity**: `Entity`, **note**: `String`)
<a class="headerlink" href="#Entity.note_has+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> returns true if this note exists, false otherwise   

<endpoint module="luxe: world" class="Entity" signature="notes(entity : Entity)"></endpoint>
<signature id="Entity.notes">Entity.notes(**entity**: `Entity`)
<a class="headerlink" href="#Entity.notes" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> get all the notes on the given entity   

<endpoint module="luxe: world" class="Entity" signature="set_name(entity : Entity, name : String)"></endpoint>
<signature id="Entity.set_name+2">Entity.set_name(**entity**: `Entity`, **name**: `String`)
<a class="headerlink" href="#Entity.set_name+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Set the name of a given `entity`.
> 
>   ```js
>   Entity.set_name(player, "player")
>   ```   

<endpoint module="luxe: world" class="Entity" signature="get_uuid(entity : Entity)"></endpoint>
<signature id="Entity.get_uuid">Entity.get_uuid(**entity**: `Entity`)
<a class="headerlink" href="#Entity.get_uuid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Get the unique ID as a string UUID for a given `entity`.   

<endpoint module="luxe: world" class="Entity" signature="set_uuid(entity : Entity, uuid_string : String)"></endpoint>
<signature id="Entity.set_uuid+2">Entity.set_uuid(**entity**: `Entity`, **uuid_string**: `String`)
<a class="headerlink" href="#Entity.set_uuid+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Set the unique ID of a given `entity`.
> Typically used in special cases, not commonly used on the high level.   

<endpoint module="luxe: world" class="Entity" signature="destroy(entity : Entity)"></endpoint>
<signature id="Entity.destroy">Entity.destroy(**entity**: `Entity`)
<a class="headerlink" href="#Entity.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Destroy the given `entity`, removing it from the world it's in.
>         
> At the moment destroy is immediate (potentially changing soon),
> so sometimes you might want `Frame.end { Entity.destroy(entity) }` 
> to push the destroy to the end of the frame, so it doesn't happen
> while iterating a list or when things are still processing it.   

<endpoint module="luxe: world" class="Entity" signature="duplicate(entity : Entity)"></endpoint>
<signature id="Entity.duplicate">Entity.duplicate(**entity**: `Entity`)
<a class="headerlink" href="#Entity.duplicate" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> Duplicate the given `entity`. 
> Returns a new entity with the same notes, folder, name and modifiers.   

<endpoint module="luxe: world" class="Entity" signature="duplicate(entity : Entity, world : World)"></endpoint>
<signature id="Entity.duplicate+2">Entity.duplicate(**entity**: `Entity`, **world**: `World`)
<a class="headerlink" href="#Entity.duplicate+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> Duplicate the given `entity` into another world.
> Returns a new entity with the same notes, folder, name and modifiers.
> Will not duplicate in same context as origin entity if the new world is different.   

### EntityContextType
`:::js import "luxe: world" for EntityContextType`
> no docs found

- [none](#EntityContextType.none)
- [scene](#EntityContextType.scene)
- [prototype](#EntityContextType.prototype)
- [name](#EntityContextType.name)(**value**: `EntityContextType`)

<hr/>
<endpoint module="luxe: world" class="EntityContextType" signature="none"></endpoint>
<signature id="EntityContextType.none">EntityContextType.none
<a class="headerlink" href="#EntityContextType.none" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="EntityContextType" signature="scene"></endpoint>
<signature id="EntityContextType.scene">EntityContextType.scene
<a class="headerlink" href="#EntityContextType.scene" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="EntityContextType" signature="prototype"></endpoint>
<signature id="EntityContextType.prototype">EntityContextType.prototype
<a class="headerlink" href="#EntityContextType.prototype" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="EntityContextType" signature="name(value : EntityContextType)"></endpoint>
<signature id="EntityContextType.name">EntityContextType.name(**value**: `EntityContextType`)
<a class="headerlink" href="#EntityContextType.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

### EntityEventType
`:::js import "luxe: world" for EntityEventType`
> no docs found

- [unknown](#EntityEventType.unknown)
- [create](#EntityEventType.create)
- [destroy](#EntityEventType.destroy)
- [load](#EntityEventType.load)
- [unload](#EntityEventType.unload)
- [modifier](#EntityEventType.modifier)
- [name](#EntityEventType.name)(**value**: `EntityEventType`)

<hr/>
<endpoint module="luxe: world" class="EntityEventType" signature="unknown"></endpoint>
<signature id="EntityEventType.unknown">EntityEventType.unknown
<a class="headerlink" href="#EntityEventType.unknown" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="EntityEventType" signature="create"></endpoint>
<signature id="EntityEventType.create">EntityEventType.create
<a class="headerlink" href="#EntityEventType.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="EntityEventType" signature="destroy"></endpoint>
<signature id="EntityEventType.destroy">EntityEventType.destroy
<a class="headerlink" href="#EntityEventType.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="EntityEventType" signature="load"></endpoint>
<signature id="EntityEventType.load">EntityEventType.load
<a class="headerlink" href="#EntityEventType.load" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="EntityEventType" signature="unload"></endpoint>
<signature id="EntityEventType.unload">EntityEventType.unload
<a class="headerlink" href="#EntityEventType.unload" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="EntityEventType" signature="modifier"></endpoint>
<signature id="EntityEventType.modifier">EntityEventType.modifier
<a class="headerlink" href="#EntityEventType.modifier" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="EntityEventType" signature="name(value : EntityEventType)"></endpoint>
<signature id="EntityEventType.name">EntityEventType.name(**value**: `EntityEventType`)
<a class="headerlink" href="#EntityEventType.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

### MeshColliderType
`:::js import "luxe: world" for MeshColliderType`
> no docs found

- [static_only](#MeshColliderType.static_only)
- [dynamic_convex](#MeshColliderType.dynamic_convex)
- [dynamic_concave](#MeshColliderType.dynamic_concave)
- [name](#MeshColliderType.name)(**value**: `Any`)
- [from_string](#MeshColliderType.from_string)(**value**: `Any`)

<hr/>
<endpoint module="luxe: world" class="MeshColliderType" signature="static_only"></endpoint>
<signature id="MeshColliderType.static_only">MeshColliderType.static_only
<a class="headerlink" href="#MeshColliderType.static_only" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="MeshColliderType" signature="dynamic_convex"></endpoint>
<signature id="MeshColliderType.dynamic_convex">MeshColliderType.dynamic_convex
<a class="headerlink" href="#MeshColliderType.dynamic_convex" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="MeshColliderType" signature="dynamic_concave"></endpoint>
<signature id="MeshColliderType.dynamic_concave">MeshColliderType.dynamic_concave
<a class="headerlink" href="#MeshColliderType.dynamic_concave" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="MeshColliderType" signature="name(value : Any)"></endpoint>
<signature id="MeshColliderType.name">MeshColliderType.name(**value**: `Any`)
<a class="headerlink" href="#MeshColliderType.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="MeshColliderType" signature="from_string(value : Any)"></endpoint>
<signature id="MeshColliderType.from_string">MeshColliderType.from_string(**value**: `Any`)
<a class="headerlink" href="#MeshColliderType.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### ModifierEventType
`:::js import "luxe: world" for ModifierEventType`
> no docs found

- [unknown](#ModifierEventType.unknown)
- [attach](#ModifierEventType.attach)
- [detach](#ModifierEventType.detach)
- [change](#ModifierEventType.change)
- [name](#ModifierEventType.name)(**value**: `ModifierEventType`)

<hr/>
<endpoint module="luxe: world" class="ModifierEventType" signature="unknown"></endpoint>
<signature id="ModifierEventType.unknown">ModifierEventType.unknown
<a class="headerlink" href="#ModifierEventType.unknown" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierEventType" signature="attach"></endpoint>
<signature id="ModifierEventType.attach">ModifierEventType.attach
<a class="headerlink" href="#ModifierEventType.attach" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierEventType" signature="detach"></endpoint>
<signature id="ModifierEventType.detach">ModifierEventType.detach
<a class="headerlink" href="#ModifierEventType.detach" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierEventType" signature="change"></endpoint>
<signature id="ModifierEventType.change">ModifierEventType.change
<a class="headerlink" href="#ModifierEventType.change" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierEventType" signature="name(value : ModifierEventType)"></endpoint>
<signature id="ModifierEventType.name">ModifierEventType.name(**value**: `ModifierEventType`)
<a class="headerlink" href="#ModifierEventType.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

### ModifierSystem
`:::js import "luxe: world" for ModifierSystem`
> no docs found

- [priority](#ModifierSystem.priority)
- [persist](#ModifierSystem.persist)
- [count](#ModifierSystem.count)
- [field](#ModifierSystem.field)
- [items](#ModifierSystem.items)
- [world](#ModifierSystem.world)
- [each](#ModifierSystem.each)(**fn**: `Any`)
- [each](#ModifierSystem.each+2)(**unique**: `Any`, **fn**: `Any`)
- [find_entity](#ModifierSystem.find_entity+2)(**relative_entity**: `Any`, **uuid**: `Any`)
- [create](#ModifierSystem.create)(**entity**: `Any`)
- [destroy](#ModifierSystem.destroy)(**entity**: `Any`)
- [get](#ModifierSystem.get)(**entity**: `Any`)
- [get](#ModifierSystem.get+2)(**entity**: `Any`, **inst**: `Any`)
- [get_slot_at](#ModifierSystem.get_slot_at)(**index**: `Any`)
- [get_slot](#ModifierSystem.get_slot)(**entity**: `Any`)
- [get_entity](#ModifierSystem.get_entity)(**slot**: `Any`)
- [get_id](#ModifierSystem.get_id)(**slot**: `Any`)
- [get_id_hash](#ModifierSystem.get_id_hash)(**slot**: `Any`)
- [set_entity](#ModifierSystem.set_entity+2)(**slot**: `Any`, **entity**: `Any`)
- [editor](#ModifierSystem.editor)(**editor**: `Any`)
- [init](#ModifierSystem.init)(**world**: `Any`)
- [tick](#ModifierSystem.tick)(**delta**: `Any`)
- [destroy](#ModifierSystem.destroy)()
- [detached](#ModifierSystem.detached)()
- [attached](#ModifierSystem.attached)()
- [disable](#ModifierSystem.disable+2)(**entity**: `Any`, **instance**: `Any`)
- [attach](#ModifierSystem.attach+2)(**entity**: `Any`, **instance**: `Any`)
- [detach](#ModifierSystem.detach+2)(**entity**: `Any`, **instance**: `Any`)
- [data](#ModifierSystem.data)
- [id](#ModifierSystem.id)
- [id](#ModifierSystem.id=)=(v : Any)
- [on_init](#ModifierSystem.on_init+2)(**world**: `Any`, **data**: `Any`)
- [on_attached](#ModifierSystem.on_attached)()
- [on_detached](#ModifierSystem.on_detached)()
- [on_disabled](#ModifierSystem.on_disabled+2)(**entities**: `Any`, **state**: `Any`)
- [on_destroying](#ModifierSystem.on_destroying)(**entities**: `Any`)
- [on_destroyed](#ModifierSystem.on_destroyed)(**entities**: `Any`)
- [on_destroy](#ModifierSystem.on_destroy)()
- [on_attach_block](#ModifierSystem.on_attach_block+4)(**block**: `Any`, **block_start**: `Any`, **block_end**: `Any`, **into**: `Any`)

<hr/>
<endpoint module="luxe: world" class="ModifierSystem" signature="priority"></endpoint>
<signature id="ModifierSystem.priority">ModifierSystem.priority
<a class="headerlink" href="#ModifierSystem.priority" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="persist"></endpoint>
<signature id="ModifierSystem.persist">ModifierSystem.persist
<a class="headerlink" href="#ModifierSystem.persist" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="count"></endpoint>
<signature id="ModifierSystem.count">ModifierSystem.count
<a class="headerlink" href="#ModifierSystem.count" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="field"></endpoint>
<signature id="ModifierSystem.field">ModifierSystem.field
<a class="headerlink" href="#ModifierSystem.field" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="items"></endpoint>
<signature id="ModifierSystem.items">ModifierSystem.items
<a class="headerlink" href="#ModifierSystem.items" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="world"></endpoint>
<signature id="ModifierSystem.world">ModifierSystem.world
<a class="headerlink" href="#ModifierSystem.world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="each(fn : Any)"></endpoint>
<signature id="ModifierSystem.each">ModifierSystem.each(**fn**: `Any`)
<a class="headerlink" href="#ModifierSystem.each" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="each(unique : Any, fn : Any)"></endpoint>
<signature id="ModifierSystem.each+2">ModifierSystem.each(**unique**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#ModifierSystem.each+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="find_entity(relative_entity : Any, uuid : Any)"></endpoint>
<signature id="ModifierSystem.find_entity+2">ModifierSystem.find_entity(**relative_entity**: `Any`, **uuid**: `Any`)
<a class="headerlink" href="#ModifierSystem.find_entity+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="create(entity : Any)"></endpoint>
<signature id="ModifierSystem.create">ModifierSystem.create(**entity**: `Any`)
<a class="headerlink" href="#ModifierSystem.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="destroy(entity : Any)"></endpoint>
<signature id="ModifierSystem.destroy">ModifierSystem.destroy(**entity**: `Any`)
<a class="headerlink" href="#ModifierSystem.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="get(entity : Any)"></endpoint>
<signature id="ModifierSystem.get">ModifierSystem.get(**entity**: `Any`)
<a class="headerlink" href="#ModifierSystem.get" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="get(entity : Any, inst : Any)"></endpoint>
<signature id="ModifierSystem.get+2">ModifierSystem.get(**entity**: `Any`, **inst**: `Any`)
<a class="headerlink" href="#ModifierSystem.get+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="get_slot_at(index : Any)"></endpoint>
<signature id="ModifierSystem.get_slot_at">ModifierSystem.get_slot_at(**index**: `Any`)
<a class="headerlink" href="#ModifierSystem.get_slot_at" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="get_slot(entity : Any)"></endpoint>
<signature id="ModifierSystem.get_slot">ModifierSystem.get_slot(**entity**: `Any`)
<a class="headerlink" href="#ModifierSystem.get_slot" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="get_entity(slot : Any)"></endpoint>
<signature id="ModifierSystem.get_entity">ModifierSystem.get_entity(**slot**: `Any`)
<a class="headerlink" href="#ModifierSystem.get_entity" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="get_id(slot : Any)"></endpoint>
<signature id="ModifierSystem.get_id">ModifierSystem.get_id(**slot**: `Any`)
<a class="headerlink" href="#ModifierSystem.get_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="get_id_hash(slot : Any)"></endpoint>
<signature id="ModifierSystem.get_id_hash">ModifierSystem.get_id_hash(**slot**: `Any`)
<a class="headerlink" href="#ModifierSystem.get_id_hash" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="set_entity(slot : Any, entity : Any)"></endpoint>
<signature id="ModifierSystem.set_entity+2">ModifierSystem.set_entity(**slot**: `Any`, **entity**: `Any`)
<a class="headerlink" href="#ModifierSystem.set_entity+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="editor(editor : Any)"></endpoint>
<signature id="ModifierSystem.editor">ModifierSystem.editor(**editor**: `Any`)
<a class="headerlink" href="#ModifierSystem.editor" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="init(world : Any)"></endpoint>
<signature id="ModifierSystem.init">ModifierSystem.init(**world**: `Any`)
<a class="headerlink" href="#ModifierSystem.init" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="tick(delta : Any)"></endpoint>
<signature id="ModifierSystem.tick">ModifierSystem.tick(**delta**: `Any`)
<a class="headerlink" href="#ModifierSystem.tick" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="destroy()"></endpoint>
<signature id="ModifierSystem.destroy">ModifierSystem.destroy()
<a class="headerlink" href="#ModifierSystem.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="detached()"></endpoint>
<signature id="ModifierSystem.detached">ModifierSystem.detached()
<a class="headerlink" href="#ModifierSystem.detached" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="attached()"></endpoint>
<signature id="ModifierSystem.attached">ModifierSystem.attached()
<a class="headerlink" href="#ModifierSystem.attached" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="disable(entity : Any, instance : Any)"></endpoint>
<signature id="ModifierSystem.disable+2">ModifierSystem.disable(**entity**: `Any`, **instance**: `Any`)
<a class="headerlink" href="#ModifierSystem.disable+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="attach(entity : Any, instance : Any)"></endpoint>
<signature id="ModifierSystem.attach+2">ModifierSystem.attach(**entity**: `Any`, **instance**: `Any`)
<a class="headerlink" href="#ModifierSystem.attach+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="detach(entity : Any, instance : Any)"></endpoint>
<signature id="ModifierSystem.detach+2">ModifierSystem.detach(**entity**: `Any`, **instance**: `Any`)
<a class="headerlink" href="#ModifierSystem.detach+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="data"></endpoint>
<signature id="ModifierSystem.data">ModifierSystem.data
<a class="headerlink" href="#ModifierSystem.data" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="id"></endpoint>
<signature id="ModifierSystem.id">ModifierSystem.id
<a class="headerlink" href="#ModifierSystem.id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="id=(v : Any)"></endpoint>
<signature id="ModifierSystem.id=">ModifierSystem.id=(v : Any)
<a class="headerlink" href="#ModifierSystem.id=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="on_init(world : Any, data : Any)"></endpoint>
<signature id="ModifierSystem.on_init+2">ModifierSystem.on_init(**world**: `Any`, **data**: `Any`)
<a class="headerlink" href="#ModifierSystem.on_init+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="on_attached()"></endpoint>
<signature id="ModifierSystem.on_attached">ModifierSystem.on_attached()
<a class="headerlink" href="#ModifierSystem.on_attached" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="on_detached()"></endpoint>
<signature id="ModifierSystem.on_detached">ModifierSystem.on_detached()
<a class="headerlink" href="#ModifierSystem.on_detached" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="on_disabled(entities : Any, state : Any)"></endpoint>
<signature id="ModifierSystem.on_disabled+2">ModifierSystem.on_disabled(**entities**: `Any`, **state**: `Any`)
<a class="headerlink" href="#ModifierSystem.on_disabled+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="on_destroying(entities : Any)"></endpoint>
<signature id="ModifierSystem.on_destroying">ModifierSystem.on_destroying(**entities**: `Any`)
<a class="headerlink" href="#ModifierSystem.on_destroying" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="on_destroyed(entities : Any)"></endpoint>
<signature id="ModifierSystem.on_destroyed">ModifierSystem.on_destroyed(**entities**: `Any`)
<a class="headerlink" href="#ModifierSystem.on_destroyed" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="on_destroy()"></endpoint>
<signature id="ModifierSystem.on_destroy">ModifierSystem.on_destroy()
<a class="headerlink" href="#ModifierSystem.on_destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="on_attach_block(block : Any, block_start : Any, block_end : Any, into : Any)"></endpoint>
<signature id="ModifierSystem.on_attach_block+4">ModifierSystem.on_attach_block(**block**: `Any`, **block_start**: `Any`, **block_end**: `Any`, **into**: `Any`)
<a class="headerlink" href="#ModifierSystem.on_attach_block+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Modifiers
`:::js import "luxe: world" for Modifiers`
> no docs found

- [get_or_create_block](#Modifiers.get_or_create_block+3)(**world**: `Any`, **module**: `Any`, **block_id**: `Any`)
- [attach_uuid](#Modifiers.attach_uuid+3)(**module**: `Any`, **entity**: `Any`, **uuid**: `Any`)
- [detach_uuid](#Modifiers.detach_uuid+3)(**module**: `Any`, **entity**: `Any`, **uuid**: `Any`)
- [has](#Modifiers.has+2)(**module**: `Any`, **entity**: `Any`)
- [set_uuid](#Modifiers.set_uuid+3)(**module**: `Any`, **entity**: `Any`, **uuid**: `Any`)
- [get_uuid](#Modifiers.get_uuid+2)(**module**: `Any`, **entity**: `Any`)
- [get_attached](#Modifiers.get_attached)(**entity**: `Any`)
- [get_attached_types](#Modifiers.get_attached_types)(**entity**: `Any`)
- [get_entities](#Modifiers.get_entities)(**module**: `Any`)
- [get_instances](#Modifiers.get_instances)(**module**: `Any`)
- [get_module](#Modifiers.get_module)(**uuid**: `Any`)
- [get_entity](#Modifiers.get_entity)(**uuid**: `Any`)
- [has_system_in_world](#Modifiers.has_system_in_world+2)(**module**: `Any`, **world**: `Any`)
- [get_system_in_world](#Modifiers.get_system_in_world+2)(**module**: `Any`, **world**: `Any`)
- [get](#Modifiers.get+2)(**module**: `Any`, **entity**: `Any`)
- [get_system](#Modifiers.get_system+2)(**module**: `Any`, **entity**: `Any`)
- [create](#Modifiers.create+2)(**module**: `Any`, **entity**: `Any`)
- [destroy](#Modifiers.destroy+2)(**module**: `Any`, **entity**: `Any`)
- [init](#Modifiers.init+3)(**world**: `Any`, **modifier**: `Any`, **block**: `Any`)
- [get_asset_compiler](#Modifiers.get_asset_compiler)(**type**: `Any`)
- [get_compiler_for_input](#Modifiers.get_compiler_for_input)(**modifier_id**: `Any`)
- [get_data_block_type](#Modifiers.get_data_block_type)(**modifier_id**: `Any`)
- [get_input_block_type](#Modifiers.get_input_block_type)(**modifier_id**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Modifiers" signature="get_or_create_block(world : Any, module : Any, block_id : Any)"></endpoint>
<signature id="Modifiers.get_or_create_block+3">Modifiers.get_or_create_block(**world**: `Any`, **module**: `Any`, **block_id**: `Any`)
<a class="headerlink" href="#Modifiers.get_or_create_block+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="attach_uuid(module : Any, entity : Any, uuid : Any)"></endpoint>
<signature id="Modifiers.attach_uuid+3">Modifiers.attach_uuid(**module**: `Any`, **entity**: `Any`, **uuid**: `Any`)
<a class="headerlink" href="#Modifiers.attach_uuid+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="detach_uuid(module : Any, entity : Any, uuid : Any)"></endpoint>
<signature id="Modifiers.detach_uuid+3">Modifiers.detach_uuid(**module**: `Any`, **entity**: `Any`, **uuid**: `Any`)
<a class="headerlink" href="#Modifiers.detach_uuid+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="has(module : Any, entity : Any)"></endpoint>
<signature id="Modifiers.has+2">Modifiers.has(**module**: `Any`, **entity**: `Any`)
<a class="headerlink" href="#Modifiers.has+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="set_uuid(module : Any, entity : Any, uuid : Any)"></endpoint>
<signature id="Modifiers.set_uuid+3">Modifiers.set_uuid(**module**: `Any`, **entity**: `Any`, **uuid**: `Any`)
<a class="headerlink" href="#Modifiers.set_uuid+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_uuid(module : Any, entity : Any)"></endpoint>
<signature id="Modifiers.get_uuid+2">Modifiers.get_uuid(**module**: `Any`, **entity**: `Any`)
<a class="headerlink" href="#Modifiers.get_uuid+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_attached(entity : Any)"></endpoint>
<signature id="Modifiers.get_attached">Modifiers.get_attached(**entity**: `Any`)
<a class="headerlink" href="#Modifiers.get_attached" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_attached_types(entity : Any)"></endpoint>
<signature id="Modifiers.get_attached_types">Modifiers.get_attached_types(**entity**: `Any`)
<a class="headerlink" href="#Modifiers.get_attached_types" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_entities(module : Any)"></endpoint>
<signature id="Modifiers.get_entities">Modifiers.get_entities(**module**: `Any`)
<a class="headerlink" href="#Modifiers.get_entities" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_instances(module : Any)"></endpoint>
<signature id="Modifiers.get_instances">Modifiers.get_instances(**module**: `Any`)
<a class="headerlink" href="#Modifiers.get_instances" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_module(uuid : Any)"></endpoint>
<signature id="Modifiers.get_module">Modifiers.get_module(**uuid**: `Any`)
<a class="headerlink" href="#Modifiers.get_module" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_entity(uuid : Any)"></endpoint>
<signature id="Modifiers.get_entity">Modifiers.get_entity(**uuid**: `Any`)
<a class="headerlink" href="#Modifiers.get_entity" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="has_system_in_world(module : Any, world : Any)"></endpoint>
<signature id="Modifiers.has_system_in_world+2">Modifiers.has_system_in_world(**module**: `Any`, **world**: `Any`)
<a class="headerlink" href="#Modifiers.has_system_in_world+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_system_in_world(module : Any, world : Any)"></endpoint>
<signature id="Modifiers.get_system_in_world+2">Modifiers.get_system_in_world(**module**: `Any`, **world**: `Any`)
<a class="headerlink" href="#Modifiers.get_system_in_world+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get(module : Any, entity : Any)"></endpoint>
<signature id="Modifiers.get+2">Modifiers.get(**module**: `Any`, **entity**: `Any`)
<a class="headerlink" href="#Modifiers.get+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_system(module : Any, entity : Any)"></endpoint>
<signature id="Modifiers.get_system+2">Modifiers.get_system(**module**: `Any`, **entity**: `Any`)
<a class="headerlink" href="#Modifiers.get_system+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="create(module : Any, entity : Any)"></endpoint>
<signature id="Modifiers.create+2">Modifiers.create(**module**: `Any`, **entity**: `Any`)
<a class="headerlink" href="#Modifiers.create+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="destroy(module : Any, entity : Any)"></endpoint>
<signature id="Modifiers.destroy+2">Modifiers.destroy(**module**: `Any`, **entity**: `Any`)
<a class="headerlink" href="#Modifiers.destroy+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="init(world : Any, modifier : Any, block : Any)"></endpoint>
<signature id="Modifiers.init+3">Modifiers.init(**world**: `Any`, **modifier**: `Any`, **block**: `Any`)
<a class="headerlink" href="#Modifiers.init+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_asset_compiler(type : Any)"></endpoint>
<signature id="Modifiers.get_asset_compiler">Modifiers.get_asset_compiler(**type**: `Any`)
<a class="headerlink" href="#Modifiers.get_asset_compiler" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_compiler_for_input(modifier_id : Any)"></endpoint>
<signature id="Modifiers.get_compiler_for_input">Modifiers.get_compiler_for_input(**modifier_id**: `Any`)
<a class="headerlink" href="#Modifiers.get_compiler_for_input" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_data_block_type(modifier_id : Any)"></endpoint>
<signature id="Modifiers.get_data_block_type">Modifiers.get_data_block_type(**modifier_id**: `Any`)
<a class="headerlink" href="#Modifiers.get_data_block_type" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_input_block_type(modifier_id : Any)"></endpoint>
<signature id="Modifiers.get_input_block_type">Modifiers.get_input_block_type(**modifier_id**: `Any`)
<a class="headerlink" href="#Modifiers.get_input_block_type" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Overlap
`:::js import "luxe: world" for Overlap`
> no docs found

- [none](#Overlap.none)
- [begin](#Overlap.begin)
- [end](#Overlap.end)
- [active](#Overlap.active)
- [name](#Overlap.name)(**value**: `Any`)
- [from_string](#Overlap.from_string)(**value**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Overlap" signature="none"></endpoint>
<signature id="Overlap.none">Overlap.none
<a class="headerlink" href="#Overlap.none" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Overlap" signature="begin"></endpoint>
<signature id="Overlap.begin">Overlap.begin
<a class="headerlink" href="#Overlap.begin" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Overlap" signature="end"></endpoint>
<signature id="Overlap.end">Overlap.end
<a class="headerlink" href="#Overlap.end" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Overlap" signature="active"></endpoint>
<signature id="Overlap.active">Overlap.active
<a class="headerlink" href="#Overlap.active" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Overlap" signature="name(value : Any)"></endpoint>
<signature id="Overlap.name">Overlap.name(**value**: `Any`)
<a class="headerlink" href="#Overlap.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Overlap" signature="from_string(value : Any)"></endpoint>
<signature id="Overlap.from_string">Overlap.from_string(**value**: `Any`)
<a class="headerlink" href="#Overlap.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Physics2D
`:::js import "luxe: world" for Physics2D`
> no docs found

- [set_gravity](#Physics2D.set_gravity+3)(**world**: `Any`, **x**: `Any`, **y**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Physics2D" signature="set_gravity(world : Any, x : Any, y : Any)"></endpoint>
<signature id="Physics2D.set_gravity+3">Physics2D.set_gravity(**world**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Physics2D.set_gravity+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Physics3D
`:::js import "luxe: world" for Physics3D`
> no docs found

- [set_debug_draw](#Physics3D.set_debug_draw+2)(**world**: `Any`, **state**: `Any`)
- [set_gravity](#Physics3D.set_gravity+4)(**world**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [cast_ray](#Physics3D.cast_ray+3)(**world**: `Any`, **from**: `Any`, **to**: `Any`)
- [cast_shape](#Physics3D.cast_shape+4)(**entity**: `Any`, **from**: `Any`, **to**: `Any`, **scale**: `Any`)
- [cast_shape](#Physics3D.cast_shape+3)(**entity**: `Any`, **from**: `Any`, **to**: `Any`)
- [query_sphere](#Physics3D.query_sphere+3)(**world**: `Any`, **center**: `Any`, **radius**: `Any`)
- [query_box](#Physics3D.query_box+3)(**world**: `Any`, **center**: `Any`, **size**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Physics3D" signature="set_debug_draw(world : Any, state : Any)"></endpoint>
<signature id="Physics3D.set_debug_draw+2">Physics3D.set_debug_draw(**world**: `Any`, **state**: `Any`)
<a class="headerlink" href="#Physics3D.set_debug_draw+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Physics3D" signature="set_gravity(world : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Physics3D.set_gravity+4">Physics3D.set_gravity(**world**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Physics3D.set_gravity+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Physics3D" signature="cast_ray(world : Any, from : Any, to : Any)"></endpoint>
<signature id="Physics3D.cast_ray+3">Physics3D.cast_ray(**world**: `Any`, **from**: `Any`, **to**: `Any`)
<a class="headerlink" href="#Physics3D.cast_ray+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Physics3D" signature="cast_shape(entity : Any, from : Any, to : Any, scale : Any)"></endpoint>
<signature id="Physics3D.cast_shape+4">Physics3D.cast_shape(**entity**: `Any`, **from**: `Any`, **to**: `Any`, **scale**: `Any`)
<a class="headerlink" href="#Physics3D.cast_shape+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Physics3D" signature="cast_shape(entity : Any, from : Any, to : Any)"></endpoint>
<signature id="Physics3D.cast_shape+3">Physics3D.cast_shape(**entity**: `Any`, **from**: `Any`, **to**: `Any`)
<a class="headerlink" href="#Physics3D.cast_shape+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Physics3D" signature="query_sphere(world : Any, center : Any, radius : Any)"></endpoint>
<signature id="Physics3D.query_sphere+3">Physics3D.query_sphere(**world**: `Any`, **center**: `Any`, **radius**: `Any`)
<a class="headerlink" href="#Physics3D.query_sphere+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Physics3D" signature="query_box(world : Any, center : Any, size : Any)"></endpoint>
<signature id="Physics3D.query_box+3">Physics3D.query_box(**world**: `Any`, **center**: `Any`, **size**: `Any`)
<a class="headerlink" href="#Physics3D.query_box+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Prototype
`:::js import "luxe: world" for Prototype`
> Prototypes are collections of entities that are stored together and can be instanced together. Protoype instances can be nested in other prototypes as well as in scenes. If entities in a prototype have a transform modifier without a transform parent, the prototype root will automatically be set as their parent.
> 
> Once a prototype is instanced in a world, all its entities behave just like other entities in the world and get assigned unique entity UUIDs. Relative prototype UUIDs, or named entities within a prototype can be accessed via the root entity of the prototype instance.

- [destroy](#Prototype.destroy)(**entity**: `Entity`)
- [has](#Prototype.has)(**entity**: `Entity`)
- [get_type](#Prototype.get_type)(**entity**: `Entity`)
- [get_root](#Prototype.get_root)(**entity**: `Entity`)
- [get_tree](#Prototype.get_tree)(**entity**: `Entity`)
- [has_tree](#Prototype.has_tree)(**entity**: `Entity`)
- [get_ref](#Prototype.get_ref+2)(**entity**: `Entity`, **uuid**: `String`)
- [get_ref_of](#Prototype.get_ref_of+2)(**entity**: `Entity`, **target_entity**: `Entity`)
- [get_named](#Prototype.get_named+2)(**entity**: `Entity`, **name**: `String`)
- [get_named_all](#Prototype.get_named_all+2)(**entity**: `Entity`, **name**: `String`)
- [entity_list](#Prototype.entity_list)(**entity**: `Entity`)
- [refs_list](#Prototype.refs_list)(**entity**: `Entity`)
- [create](#Prototype.create+3)(**world**: `World`, **prototype_id**: `String`, **instance_id**: `String`)
- [create](#Prototype.create+4)(**world**: `World`, **prototype_id**: `String`, **instance_id**: `String`, **position**: `Vec`)
- [create](#Prototype.create+5)(**world**: `World`, **prototype_id**: `String`, **instance_id**: `String`, **position**: `Vec`, **rotation**: `Vec`)
- [create](#Prototype.create+6)(**world**: `World`, **prototype_id**: `String`, **instance_id**: `String`, **position**: `Vec`, **rotation**: `Vec`, **scale**: `Vec`)

<hr/>
<endpoint module="luxe: world" class="Prototype" signature="destroy(entity : Entity)"></endpoint>
<signature id="Prototype.destroy">Prototype.destroy(**entity**: `Entity`)
<a class="headerlink" href="#Prototype.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Destroys the prototype instance. (called on the root entity and will also destroy member entities that were instanced with it)   

<endpoint module="luxe: world" class="Prototype" signature="has(entity : Entity)"></endpoint>
<signature id="Prototype.has">Prototype.has(**entity**: `Entity`)
<a class="headerlink" href="#Prototype.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Get whether a entity has a prototype modifier (is a prototype instance root).   

<endpoint module="luxe: world" class="Prototype" signature="get_type(entity : Entity)"></endpoint>
<signature id="Prototype.get_type">Prototype.get_type(**entity**: `Entity`)
<a class="headerlink" href="#Prototype.get_type" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js ID`
> Get the prototype id the prototype instance was spawned from.   

<endpoint module="luxe: world" class="Prototype" signature="get_root(entity : Entity)"></endpoint>
<signature id="Prototype.get_root">Prototype.get_root(**entity**: `Entity`)
<a class="headerlink" href="#Prototype.get_root" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> Get the \"innermost\" prototype root if entity is part of a prototype instance. Returns the entity itself if it is a prototype root. Returns null if entity is not part of a prototype instance.   

<endpoint module="luxe: world" class="Prototype" signature="get_tree(entity : Entity)"></endpoint>
<signature id="Prototype.get_tree">Prototype.get_tree(**entity**: `Entity`)
<a class="headerlink" href="#Prototype.get_tree" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> Get the list of prototype instances this entity is a part of. (List will have 1 elements for unnested prototypes and goes from innermost to outermost instance root for nested prototypes.). Null if entity is not part of prototype instance.   

<endpoint module="luxe: world" class="Prototype" signature="has_tree(entity : Entity)"></endpoint>
<signature id="Prototype.has_tree">Prototype.has_tree(**entity**: `Entity`)
<a class="headerlink" href="#Prototype.has_tree" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Get whether the entity is part of a prototype instance.   

<endpoint module="luxe: world" class="Prototype" signature="get_ref(entity : Entity, uuid : String)"></endpoint>
<signature id="Prototype.get_ref+2">Prototype.get_ref(**entity**: `Entity`, **uuid**: `String`)
<a class="headerlink" href="#Prototype.get_ref+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> Get an entity by its reference (prototype-relative UUID) from its prototype root. (the same prototype asset may be instanced multiple times, so it may be important to find a specific prototype root and ask it for its version of the entity)   

<endpoint module="luxe: world" class="Prototype" signature="get_ref_of(entity : Entity, target_entity : Entity)"></endpoint>
<signature id="Prototype.get_ref_of+2">Prototype.get_ref_of(**entity**: `Entity`, **target_entity**: `Entity`)
<a class="headerlink" href="#Prototype.get_ref_of+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Get the reference (prototype-relative UUID) of an entity within a prototype instance. One Entity can be part of multiple nested prototypes and have different references in each context.   

<endpoint module="luxe: world" class="Prototype" signature="get_named(entity : Entity, name : String)"></endpoint>
<signature id="Prototype.get_named+2">Prototype.get_named(**entity**: `Entity`, **name**: `String`)
<a class="headerlink" href="#Prototype.get_named+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> Get first entity in a prototype instance with a specific name.   

<endpoint module="luxe: world" class="Prototype" signature="get_named_all(entity : Entity, name : String)"></endpoint>
<signature id="Prototype.get_named_all+2">Prototype.get_named_all(**entity**: `Entity`, **name**: `String`)
<a class="headerlink" href="#Prototype.get_named_all+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> Get all entities in a prototype instance with a specific name.   

<endpoint module="luxe: world" class="Prototype" signature="entity_list(entity : Entity)"></endpoint>
<signature id="Prototype.entity_list">Prototype.entity_list(**entity**: `Entity`)
<a class="headerlink" href="#Prototype.entity_list" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> Get a list of all entities that are part of a prototype instance.   

<endpoint module="luxe: world" class="Prototype" signature="refs_list(entity : Entity)"></endpoint>
<signature id="Prototype.refs_list">Prototype.refs_list(**entity**: `Entity`)
<a class="headerlink" href="#Prototype.refs_list" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> Get a list of all references (prototype-relative UUIDs) to entities within one prototype instance.   

<endpoint module="luxe: world" class="Prototype" signature="create(world : World, prototype_id : String, instance_id : String)"></endpoint>
<signature id="Prototype.create+3">Prototype.create(**world**: `World`, **prototype_id**: `String`, **instance_id**: `String`)
<a class="headerlink" href="#Prototype.create+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Prototype" signature="create(world : World, prototype_id : String, instance_id : String, position : Vec)"></endpoint>
<signature id="Prototype.create+4">Prototype.create(**world**: `World`, **prototype_id**: `String`, **instance_id**: `String`, **position**: `Vec`)
<a class="headerlink" href="#Prototype.create+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Prototype" signature="create(world : World, prototype_id : String, instance_id : String, position : Vec, rotation : Vec)"></endpoint>
<signature id="Prototype.create+5">Prototype.create(**world**: `World`, **prototype_id**: `String`, **instance_id**: `String`, **position**: `Vec`, **rotation**: `Vec`)
<a class="headerlink" href="#Prototype.create+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Prototype" signature="create(world : World, prototype_id : String, instance_id : String, position : Vec, rotation : Vec, scale : Vec)"></endpoint>
<signature id="Prototype.create+6">Prototype.create(**world**: `World`, **prototype_id**: `String`, **instance_id**: `String`, **position**: `Vec`, **rotation**: `Vec`, **scale**: `Vec`)
<a class="headerlink" href="#Prototype.create+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Instantiate a new prototype into a world with a new name(instance id), position, rotation and scale.
> You may pass `null` into position rotation and scale (or call one of the functions that omit those arguments), to give them default values (0,0,0 for position/rotation, 1,1,1 for scale).
> This function returns the root entity of the newly created prototype instance.   

### Scene
`:::js import "luxe: world" for Scene`
> Scenes are collections of entities that are stored together and can be instanced together. If entities in a scene have a transform modifier without a transform parent, the scene root will automatically be set as their parent.
> 
> Once a scene is instanced in a world, all its entities behave just like other entities in the world and get assigned unique entity UUIDs. Relative scene UUIDs, or named entities within a scene can be accessed via the root entity of the scene instance.
> 
> Scenes are mostly referred to by their scene ID. By default for new scenes, this is their asset id, but it can be changed to allow loading multiple scenes from the same asset and have them exist in the same world.

- [create](#Scene.create+2)(**world**: `World`, **id**: `String`)
- [destroy](#Scene.destroy+2)(**world**: `World`, **id**: `String`)
- [get_list](#Scene.get_list)(**world**: `World`)
- [exists](#Scene.exists+2)(**world**: `World`, **id**: `String`)
- [entity_list](#Scene.entity_list+2)(**world**: `World`, **id**: `String`)
- [entity_forget](#Scene.entity_forget+3)(**world**: `World`, **id**: `String`, **entity**: `Entity`)
- [set_id](#Scene.set_id+3)(**world**: `World`, **id**: `String`, **new_id**: `String`)

<hr/>
<endpoint module="luxe: world" class="Scene" signature="create(world : World, id : String)"></endpoint>
<signature id="Scene.create+2">Scene.create(**world**: `World`, **id**: `String`)
<a class="headerlink" href="#Scene.create+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> Create a new scene into a world. Does *not* load a scene asset with the given id.
> This function returns the root entity of the newly created scene.   

<endpoint module="luxe: world" class="Scene" signature="destroy(world : World, id : String)"></endpoint>
<signature id="Scene.destroy+2">Scene.destroy(**world**: `World`, **id**: `String`)
<a class="headerlink" href="#Scene.destroy+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> Destroy a scene by its id.
> 
> ```js
>   Scene.create(app.world, "scenes/main")
>   Scene.destroy(app.world, "scenes/main")
> ```   

<endpoint module="luxe: world" class="Scene" signature="get_list(world : World)"></endpoint>
<signature id="Scene.get_list">Scene.get_list(**world**: `World`)
<a class="headerlink" href="#Scene.get_list" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> Get a list of scenes in a world. The list contains the IDs of the scenes (as string IDs).   

<endpoint module="luxe: world" class="Scene" signature="exists(world : World, id : String)"></endpoint>
<signature id="Scene.exists+2">Scene.exists(**world**: `World`, **id**: `String`)
<a class="headerlink" href="#Scene.exists+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Check if a scene is currently instanced in a world.   

<endpoint module="luxe: world" class="Scene" signature="entity_list(world : World, id : String)"></endpoint>
<signature id="Scene.entity_list+2">Scene.entity_list(**world**: `World`, **id**: `String`)
<a class="headerlink" href="#Scene.entity_list+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> Get all entities that are part of an instanced scene.   

<endpoint module="luxe: world" class="Scene" signature="entity_forget(world : World, id : String, entity : Entity)"></endpoint>
<signature id="Scene.entity_forget+3">Scene.entity_forget(**world**: `World`, **id**: `String`, **entity**: `Entity`)
<a class="headerlink" href="#Scene.entity_forget+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Stop associating an entity with a loaded scene.   

<endpoint module="luxe: world" class="Scene" signature="set_id(world : World, id : String, new_id : String)"></endpoint>
<signature id="Scene.set_id+3">Scene.set_id(**world**: `World`, **id**: `String`, **new_id**: `String`)
<a class="headerlink" href="#Scene.set_id+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Change the ID of a scene instance. 
>     
> By default this ID is the asset id, but with this function it can be changed and the original scene loaded again without causting conflicts.   

### UI
`:::js import "luxe: world" for UI`
> A `UI` modifier holds controls which define a 2d user interface with images, buttons, sliders, etc...
> 
> ```js
>   //create ui modifier in ui world
>   var ui = Entity.create(app.ui)
>   UI.create(ui, 0, 0, world.width, world.height, 0, app.ui_camera)
> 
>   //add controls
>   var control = Control.create(ui)
>   //more control stuff
> 
>   //then rebuild the UI
>   UI.commit(ui)
> ```

- [create](#UI.create+7)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **w**: `Num`, **h**: `Num`, **z**: `Num`, **camera**: `Entity`)
- [destroy](#UI.destroy)(**entity**: `Entity`)
- [has](#UI.has)(**entity**: `Entity`)
- [commit](#UI.commit)(**entity**: `Entity`)
- [commit_now](#UI.commit_now)(**entity**: `Entity`)
- [event_cancel](#UI.event_cancel+2)(**entity**: `Entity`, **event_id**: `ID`)
- [event_cancelled](#UI.event_cancelled+2)(**entity**: `Entity`, **event_id**: `ID`)
- [set_camera](#UI.set_camera+2)(**entity**: `Entity`, **camera**: `Entity`)
- [set_render_mode](#UI.set_render_mode+2)(**entity**: `Entity`, **mode**: `UIRenderMode`)
- [set_material_basis](#UI.set_material_basis+3)(**entity**: `Entity`, **solid**: `String`, **text**: `String`)
- [set_bounds](#UI.set_bounds+6)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **w**: `Num`, **h**: `Num`, **z**: `Num`)
- [get_pos](#UI.get_pos)(**entity**: `Entity`)
- [get_opacity](#UI.get_opacity)(**entity**: `Entity`)
- [set_opacity](#UI.set_opacity+2)(**entity**: `Entity`, **opacity**: `Num`)
- [get_size](#UI.get_size)(**entity**: `Entity`)
- [get_debug_control](#UI.get_debug_control)(**entity**: `Entity`)
- [get_debug_draw_depth](#UI.get_debug_draw_depth)(**entity**: `Entity`)
- [get_input_node](#UI.get_input_node)(**entity**: `Entity`)
- [set_input_node](#UI.set_input_node+2)(**entity**: `Entity`, **input_node_id**: `String`)
- [set_layout_mode](#UI.set_layout_mode+2)(**entity**: `Entity`, **mode**: `UILayoutMode`)
- [set_debug_mode](#UI.set_debug_mode+2)(**entity**: `Entity`, **mode**: `UIDebugMode`)
- [any_marked](#UI.any_marked)()
- [any_focused](#UI.any_focused)()
- [get_focused](#UI.get_focused)(**entity**: `Entity`)
- [get_captured](#UI.get_captured)(**entity**: `Entity`)
- [get_marked](#UI.get_marked)(**entity**: `Entity`)
- [get_control_count](#UI.get_control_count)(**entity**: `Entity`)
- [get_control](#UI.get_control+2)(**entity**: `Entity`, **index**: `Num`)
- [focus_invalidate](#UI.focus_invalidate)(**entity**: `Entity`)
- [focus](#UI.focus)(**control**: `Control`)
- [unfocus](#UI.unfocus)(**control**: `Control`)
- [mark](#UI.mark)(**control**: `Control`)
- [unmark](#UI.unmark)(**control**: `Control`)
- [capture](#UI.capture)(**control**: `Control`)
- [uncapture](#UI.uncapture)(**control**: `Control`)
- [bring_to_front](#UI.bring_to_front)(**control**: `Control`)
- [control_at_point](#UI.control_at_point+3)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
- [mouse_to_canvas](#UI.mouse_to_canvas+3)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
- [dump](#UI.dump)(**ui**: `Entity`)
- [spawn](#UI.spawn+3)(**asset_id**: `String`, **parent**: `Control`, **instance_id**: `String`)
- [make](#UI.make+3)(**ui**: `Entity`, **asset**: `String`, **instance_id**: `String`)
- [draw_depth_of](#UI.draw_depth_of+2)(**control**: `Control`, **index**: `Num`)
- [draw_text](#UI.draw_text+12)(**control**: `Control`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **w**: `Num`, **h**: `Num`, **string**: `String`, **size**: `Num`, **font**: `String`, **color**: `Color`, **align**: `TextAlign`, **align_vertical**: `TextAlign`)
- [draw_text](#UI.draw_text+10)(**control**: `Control`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **string**: `String`, **size**: `Num`, **font**: `String`, **color**: `Color`, **align**: `TextAlign`, **align_vertical**: `TextAlign`)
- [draw_image](#UI.draw_image+11)(**control**: `Control`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **w**: `Num`, **h**: `Num`, **angle**: `Num`, **color**: `Color`, **uv**: `Vec`, **image**: `Image`, **flags**: `UIImageFlags`)
- [draw_image](#UI.draw_image+10)(**control**: `Control`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **w**: `Num`, **h**: `Num`, **angle**: `Num`, **color**: `Color`, **uv**: `Vec`, **image**: `Image`)
- [draw_quad](#UI.draw_quad+8)(**control**: `Control`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **w**: `Num`, **h**: `Num`, **angle**: `Num`, **color**: `Color`)
- [draw_circle](#UI.draw_circle+10)(**control**: `Control`, **ox**: `Num`, **oy**: `Num`, **oz**: `Num`, **rx**: `Num`, **ry**: `Num`, **start_angle**: `Num`, **end_angle**: `Num`, **smoothness**: `Num`, **color**: `Color`)
- [draw_line](#UI.draw_line+7)(**control**: `Control`, **x1**: `Num`, **y1**: `Num`, **x2**: `Num`, **y2**: `Num`, **z**: `Num`, **style**: `PathStyle`)
- [draw_rect](#UI.draw_rect+8)(**control**: `Control`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **w**: `Num`, **h**: `Num`, **angle**: `Num`, **style**: `PathStyle`)
- [draw_rect_detailed](#UI.draw_rect_detailed+10)(**control**: `Control`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **w**: `Num`, **h**: `Num`, **angle**: `Num`, **radius**: `Num`, **smoothness**: `Num`, **style**: `PathStyle`)
- [draw_quad_detailed](#UI.draw_quad_detailed+10)(**control**: `Control`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **w**: `Num`, **h**: `Num`, **angle**: `Num`, **radius**: `Num`, **smoothness**: `Num`, **color**: `Color`)
- [draw_ring](#UI.draw_ring+10)(**control**: `Control`, **ox**: `Num`, **oy**: `Num`, **oz**: `Num`, **rx**: `Num`, **ry**: `Num`, **start_angle**: `Num`, **end_angle**: `Num`, **smoothness**: `Num`, **style**: `PathStyle`)
- [draw_path](#UI.draw_path+4)(**control**: `Control`, **points**: `List`, **style**: `PathStyle`, **closed**: `Bool`)
- [events_emit](#UI.events_emit+2)(**control**: `Control`, **type**: `UIEvent`)
- [events_emit](#UI.events_emit+3)(**control**: `Control`, **type**: `UIEvent`, **data**: `Any`)
- [events_emit](#UI.events_emit+4)(**control**: `Control`, **type**: `UIEvent`, **data**: `Any`, **data_before**: `Any`)

<hr/>
<endpoint module="luxe: world" class="UI" signature="create(entity : Entity, x : Num, y : Num, w : Num, h : Num, z : Num, camera : Entity)"></endpoint>
<signature id="UI.create+7">UI.create(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **w**: `Num`, **h**: `Num`, **z**: `Num`, **camera**: `Entity`)
<a class="headerlink" href="#UI.create+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Create a UI modifier on an Entity.
> The `x` `y` `z` arguments are the position relative to the world origin, or relative to the `Transform` on the same entity if one exists.
> `w` and `h` are the width and the height of the canvas, this is both used for the mask texture (and in `UIRenderMode.image` the ui rendertarget) as well as the (unscaled) size of the UI in worldspace.
> `camera` describes a camera that is used to resolve input, most of the time this is the camera rendering the world the UI is in, but it doesnt have to be.   

<endpoint module="luxe: world" class="UI" signature="destroy(entity : Entity)"></endpoint>
<signature id="UI.destroy">UI.destroy(**entity**: `Entity`)
<a class="headerlink" href="#UI.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Remove a `UI` modifier from an entity. This also destroys all controls on that `UI`.   

<endpoint module="luxe: world" class="UI" signature="has(entity : Entity)"></endpoint>
<signature id="UI.has">UI.has(**entity**: `Entity`)
<a class="headerlink" href="#UI.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Get whether an Entity has an `UI` modifier attached.   

<endpoint module="luxe: world" class="UI" signature="commit(entity : Entity)"></endpoint>
<signature id="UI.commit">UI.commit(**entity**: `Entity`)
<a class="headerlink" href="#UI.commit" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Request all changes to the UI are committed before rendering happens   

<endpoint module="luxe: world" class="UI" signature="commit_now(entity : Entity)"></endpoint>
<signature id="UI.commit_now">UI.commit_now(**entity**: `Entity`)
<a class="headerlink" href="#UI.commit_now" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Commit all changes to the UI immediately   

<endpoint module="luxe: world" class="UI" signature="event_cancel(entity : Entity, event_id : ID)"></endpoint>
<signature id="UI.event_cancel+2">UI.event_cancel(**entity**: `Entity`, **event_id**: `ID`)
<a class="headerlink" href="#UI.event_cancel+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Cancel an event.   

<endpoint module="luxe: world" class="UI" signature="event_cancelled(entity : Entity, event_id : ID)"></endpoint>
<signature id="UI.event_cancelled+2">UI.event_cancelled(**entity**: `Entity`, **event_id**: `ID`)
<a class="headerlink" href="#UI.event_cancelled+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Check whether an event was cancelled before.   

<endpoint module="luxe: world" class="UI" signature="set_camera(entity : Entity, camera : Entity)"></endpoint>
<signature id="UI.set_camera+2">UI.set_camera(**entity**: `Entity`, **camera**: `Entity`)
<a class="headerlink" href="#UI.set_camera+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the camera used for input calculations. Most of the time this is the camera rendering the world the UI is in, but it doesnt have to be.   

<endpoint module="luxe: world" class="UI" signature="set_render_mode(entity : Entity, mode : UIRenderMode)"></endpoint>
<signature id="UI.set_render_mode+2">UI.set_render_mode(**entity**: `Entity`, **mode**: `UIRenderMode`)
<a class="headerlink" href="#UI.set_render_mode+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the render mode of the UI canvas.
>           
> `UIRenderMode.world` renders the controls directly into the world, while `UIRenderMode.image` first renders them to an intermediate texture and then renders that.
> 
> `UIRenderMode.image` is the default as it can avoid artifacts and works in more circumstances, though `UIRenderMode.world` can lead to more sharp results and slightly better performance.   

<endpoint module="luxe: world" class="UI" signature="set_material_basis(entity : Entity, solid : String, text : String)"></endpoint>
<signature id="UI.set_material_basis+3">UI.set_material_basis(**entity**: `Entity`, **solid**: `String`, **text**: `String`)
<a class="headerlink" href="#UI.set_material_basis+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the material basis the controls (excluding `UIImage`) is drawn with. By default "luxe: material_basis/ui_solid" is the basis for solid controls and "luxe: material_basis/ui_font" the basis for text.   

<endpoint module="luxe: world" class="UI" signature="set_bounds(entity : Entity, x : Num, y : Num, w : Num, h : Num, z : Num)"></endpoint>
<signature id="UI.set_bounds+6">UI.set_bounds(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **w**: `Num`, **h**: `Num`, **z**: `Num`)
<a class="headerlink" href="#UI.set_bounds+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set size and position of an `UI` modifier.
> The `x` `y` `z` arguments are the position relative to the world origin, or relative to the `Transform` on the same entity if one exists.
> `w` and `h` are the width and the height of the canvas, this is both used for the mask texture (and in `UIRenderMode.image` the ui rendertarget) as well as the (unscaled) size of the UI in worldspace.   

<endpoint module="luxe: world" class="UI" signature="get_pos(entity : Entity)"></endpoint>
<signature id="UI.get_pos">UI.get_pos(**entity**: `Entity`)
<a class="headerlink" href="#UI.get_pos" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Get position of an `UI` modifier.   

<endpoint module="luxe: world" class="UI" signature="get_opacity(entity : Entity)"></endpoint>
<signature id="UI.get_opacity">UI.get_opacity(**entity**: `Entity`)
<a class="headerlink" href="#UI.get_opacity" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get overall UI opacity   

<endpoint module="luxe: world" class="UI" signature="set_opacity(entity : Entity, opacity : Num)"></endpoint>
<signature id="UI.set_opacity+2">UI.set_opacity(**entity**: `Entity`, **opacity**: `Num`)
<a class="headerlink" href="#UI.set_opacity+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Set overall UI opacity   

<endpoint module="luxe: world" class="UI" signature="get_size(entity : Entity)"></endpoint>
<signature id="UI.get_size">UI.get_size(**entity**: `Entity`)
<a class="headerlink" href="#UI.get_size" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Get size of an `UI` modifier.   

<endpoint module="luxe: world" class="UI" signature="get_debug_control(entity : Entity)"></endpoint>
<signature id="UI.get_debug_control">UI.get_debug_control(**entity**: `Entity`)
<a class="headerlink" href="#UI.get_debug_control" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Control`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="get_debug_draw_depth(entity : Entity)"></endpoint>
<signature id="UI.get_debug_draw_depth">UI.get_debug_draw_depth(**entity**: `Entity`)
<a class="headerlink" href="#UI.get_debug_draw_depth" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="get_input_node(entity : Entity)"></endpoint>
<signature id="UI.get_input_node">UI.get_input_node(**entity**: `Entity`)
<a class="headerlink" href="#UI.get_input_node" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="set_input_node(entity : Entity, input_node_id : String)"></endpoint>
<signature id="UI.set_input_node+2">UI.set_input_node(**entity**: `Entity`, **input_node_id**: `String`)
<a class="headerlink" href="#UI.set_input_node+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="set_layout_mode(entity : Entity, mode : UILayoutMode)"></endpoint>
<signature id="UI.set_layout_mode+2">UI.set_layout_mode(**entity**: `Entity`, **mode**: `UILayoutMode`)
<a class="headerlink" href="#UI.set_layout_mode+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the layout mode of the UI.
> 
> By default this is `UILayoutMode.none`, which will do no extra layouting and ignore `Control` margin, behave and contain.
> 
> `UILayoutMode.flex` is the default layout implementation which will follow the `Control` margin, behave and contain settings.
> 
> ```js
>   UI.set_layout_mode(ui, UILayoutMode.flex)
> 
>   var root = Control.create(ui)
>     Control.set_size(root, 300, 0)
>     Control.set_behave(root, UIBehave.left | UIBehave.top)
>     Control.set_margin(root, 100, 100, 0, 0)
>     Control.set_contain(root, UIContain.column | UIContain.start | UIContain.vfit)
> 
>   var text_input = UIText.create(ui)
>     Control.set_behave(text_input, UIBehave.left | UIBehave.top | UIBehave.hfill)
>   Control.child_add(root, text_input)
> 
>   var image = UIImage.create(ui)
>     UIImage.set_image(image, Assets.image("luxe: image/logo.sprite"))
>     Control.set_size(image, 300, 300)
>     Control.set_behave(image, UIBehave.left | UIBehave.top | UIBehave.hfill)
>   Control.child_add(root, image)
> ```   

<endpoint module="luxe: world" class="UI" signature="set_debug_mode(entity : Entity, mode : UIDebugMode)"></endpoint>
<signature id="UI.set_debug_mode+2">UI.set_debug_mode(**entity**: `Entity`, **mode**: `UIDebugMode`)
<a class="headerlink" href="#UI.set_debug_mode+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="any_marked()"></endpoint>
<signature id="UI.any_marked">UI.any_marked()
<a class="headerlink" href="#UI.any_marked" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if any UI has a marked control (any control with input under the mouse)   

<endpoint module="luxe: world" class="UI" signature="any_focused()"></endpoint>
<signature id="UI.any_focused">UI.any_focused()
<a class="headerlink" href="#UI.any_focused" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if any UI has a focused control   

<endpoint module="luxe: world" class="UI" signature="get_focused(entity : Entity)"></endpoint>
<signature id="UI.get_focused">UI.get_focused(**entity**: `Entity`)
<a class="headerlink" href="#UI.get_focused" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Control`
> Get currently focussed control. A control being focused means its been clicked on or otherwise focused and will recieve context inputs like keyboard presses on a text input field.   

<endpoint module="luxe: world" class="UI" signature="get_captured(entity : Entity)"></endpoint>
<signature id="UI.get_captured">UI.get_captured(**entity**: `Entity`)
<a class="headerlink" href="#UI.get_captured" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Control`
> Get captured control, `null` if none is captured. A control being captured means all inputs will only be sent to this control until it is uncaptured again.   

<endpoint module="luxe: world" class="UI" signature="get_marked(entity : Entity)"></endpoint>
<signature id="UI.get_marked">UI.get_marked(**entity**: `Entity`)
<a class="headerlink" href="#UI.get_marked" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Control`
> Get marked control, `null` if none is marked. A control being marked means it is hovered over and can be focused.   

<endpoint module="luxe: world" class="UI" signature="get_control_count(entity : Entity)"></endpoint>
<signature id="UI.get_control_count">UI.get_control_count(**entity**: `Entity`)
<a class="headerlink" href="#UI.get_control_count" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get amount of controls in a `UI`.   

<endpoint module="luxe: world" class="UI" signature="get_control(entity : Entity, index : Num)"></endpoint>
<signature id="UI.get_control+2">UI.get_control(**entity**: `Entity`, **index**: `Num`)
<a class="headerlink" href="#UI.get_control+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Control`
> Get a control in a `UI` by its index. Useful for iterating over all controls.   

<endpoint module="luxe: world" class="UI" signature="focus_invalidate(entity : Entity)"></endpoint>
<signature id="UI.focus_invalidate">UI.focus_invalidate(**entity**: `Entity`)
<a class="headerlink" href="#UI.focus_invalidate" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Unfocus whatever is focussed in a specific `UI`.   

<endpoint module="luxe: world" class="UI" signature="focus(control : Control)"></endpoint>
<signature id="UI.focus">UI.focus(**control**: `Control`)
<a class="headerlink" href="#UI.focus" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Focus a control. Will unfocus any previously focused controls on the `UI`. A control being focused means its been clicked on or otherwise focused and will recieve context inputs like keyboard presses on a text input field.   

<endpoint module="luxe: world" class="UI" signature="unfocus(control : Control)"></endpoint>
<signature id="UI.unfocus">UI.unfocus(**control**: `Control`)
<a class="headerlink" href="#UI.unfocus" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Unfocus a specific control. If the control is not the focused control in the UI, this does nothing.   

<endpoint module="luxe: world" class="UI" signature="mark(control : Control)"></endpoint>
<signature id="UI.mark">UI.mark(**control**: `Control`)
<a class="headerlink" href="#UI.mark" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Mark a control. Will unfocus any previously marked controls on the `UI`. A control being marked means it is hovered over and can be focused.   

<endpoint module="luxe: world" class="UI" signature="unmark(control : Control)"></endpoint>
<signature id="UI.unmark">UI.unmark(**control**: `Control`)
<a class="headerlink" href="#UI.unmark" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Unmark a specific control. If the control is not the marked control in the UI, this does nothing.   

<endpoint module="luxe: world" class="UI" signature="capture(control : Control)"></endpoint>
<signature id="UI.capture">UI.capture(**control**: `Control`)
<a class="headerlink" href="#UI.capture" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Capture a control. Until uncaptured all inputs will only go to this control.   

<endpoint module="luxe: world" class="UI" signature="uncapture(control : Control)"></endpoint>
<signature id="UI.uncapture">UI.uncapture(**control**: `Control`)
<a class="headerlink" href="#UI.uncapture" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Uncapture a control and have inputs be distributed regularly.   

<endpoint module="luxe: world" class="UI" signature="bring_to_front(control : Control)"></endpoint>
<signature id="UI.bring_to_front">UI.bring_to_front(**control**: `Control`)
<a class="headerlink" href="#UI.bring_to_front" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Bring the control to the front in its current context (globally in the `UI` or within its parent if its a child)   

<endpoint module="luxe: world" class="UI" signature="control_at_point(entity : Entity, x : Num, y : Num)"></endpoint>
<signature id="UI.control_at_point+3">UI.control_at_point(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
<a class="headerlink" href="#UI.control_at_point+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Control`
> Get the highest control at a position.   

<endpoint module="luxe: world" class="UI" signature="mouse_to_canvas(entity : Entity, x : Num, y : Num)"></endpoint>
<signature id="UI.mouse_to_canvas+3">UI.mouse_to_canvas(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
<a class="headerlink" href="#UI.mouse_to_canvas+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Float2`
> Translate from mouse position on screen to canvas coordinates. Uses the set canvas camera.   

<endpoint module="luxe: world" class="UI" signature="dump(ui : Entity)"></endpoint>
<signature id="UI.dump">UI.dump(**ui**: `Entity`)
<a class="headerlink" href="#UI.dump" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Write a bunch of information about the `UI` and its controls into the console.   

<endpoint module="luxe: world" class="UI" signature="spawn(asset_id : String, parent : Control, instance_id : String)"></endpoint>
<signature id="UI.spawn+3">UI.spawn(**asset_id**: `String`, **parent**: `Control`, **instance_id**: `String`)
<a class="headerlink" href="#UI.spawn+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Spawn controls from a ui asset.
> Puts newly spawned controls into a parent control.   

<endpoint module="luxe: world" class="UI" signature="make(ui : Entity, asset : String, instance_id : String)"></endpoint>
<signature id="UI.make+3">UI.make(**ui**: `Entity`, **asset**: `String`, **instance_id**: `String`)
<a class="headerlink" href="#UI.make+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Control`
> Spawn controls from a ui asset.
> Creates new root for newly spawned controls and returns that root control.   

<endpoint module="luxe: world" class="UI" signature="draw_depth_of(control : Control, index : Num)"></endpoint>
<signature id="UI.draw_depth_of+2">UI.draw_depth_of(**control**: `Control`, **index**: `Num`)
<a class="headerlink" href="#UI.draw_depth_of+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="draw_text(control : Control, x : Num, y : Num, z : Num, w : Num, h : Num, string : String, size : Num, font : String, color : Color, align : TextAlign, align_vertical : TextAlign)"></endpoint>
<signature id="UI.draw_text+12">UI.draw_text(**control**: `Control`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **w**: `Num`, **h**: `Num`, **string**: `String`, **size**: `Num`, **font**: `String`, **color**: `Color`, **align**: `TextAlign`, **align_vertical**: `TextAlign`)
<a class="headerlink" href="#UI.draw_text+12" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="draw_text(control : Control, x : Num, y : Num, z : Num, string : String, size : Num, font : String, color : Color, align : TextAlign, align_vertical : TextAlign)"></endpoint>
<signature id="UI.draw_text+10">UI.draw_text(**control**: `Control`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **string**: `String`, **size**: `Num`, **font**: `String`, **color**: `Color`, **align**: `TextAlign`, **align_vertical**: `TextAlign`)
<a class="headerlink" href="#UI.draw_text+10" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="draw_image(control : Control, x : Num, y : Num, z : Num, w : Num, h : Num, angle : Num, color : Color, uv : Vec, image : Image, flags : UIImageFlags)"></endpoint>
<signature id="UI.draw_image+11">UI.draw_image(**control**: `Control`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **w**: `Num`, **h**: `Num`, **angle**: `Num`, **color**: `Color`, **uv**: `Vec`, **image**: `Image`, **flags**: `UIImageFlags`)
<a class="headerlink" href="#UI.draw_image+11" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="draw_image(control : Control, x : Num, y : Num, z : Num, w : Num, h : Num, angle : Num, color : Color, uv : Vec, image : Image)"></endpoint>
<signature id="UI.draw_image+10">UI.draw_image(**control**: `Control`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **w**: `Num`, **h**: `Num`, **angle**: `Num`, **color**: `Color`, **uv**: `Vec`, **image**: `Image`)
<a class="headerlink" href="#UI.draw_image+10" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="draw_quad(control : Control, x : Num, y : Num, z : Num, w : Num, h : Num, angle : Num, color : Color)"></endpoint>
<signature id="UI.draw_quad+8">UI.draw_quad(**control**: `Control`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **w**: `Num`, **h**: `Num`, **angle**: `Num`, **color**: `Color`)
<a class="headerlink" href="#UI.draw_quad+8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="draw_circle(control : Control, ox : Num, oy : Num, oz : Num, rx : Num, ry : Num, start_angle : Num, end_angle : Num, smoothness : Num, color : Color)"></endpoint>
<signature id="UI.draw_circle+10">UI.draw_circle(**control**: `Control`, **ox**: `Num`, **oy**: `Num`, **oz**: `Num`, **rx**: `Num`, **ry**: `Num`, **start_angle**: `Num`, **end_angle**: `Num`, **smoothness**: `Num`, **color**: `Color`)
<a class="headerlink" href="#UI.draw_circle+10" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="draw_line(control : Control, x1 : Num, y1 : Num, x2 : Num, y2 : Num, z : Num, style : PathStyle)"></endpoint>
<signature id="UI.draw_line+7">UI.draw_line(**control**: `Control`, **x1**: `Num`, **y1**: `Num`, **x2**: `Num`, **y2**: `Num`, **z**: `Num`, **style**: `PathStyle`)
<a class="headerlink" href="#UI.draw_line+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="draw_rect(control : Control, x : Num, y : Num, z : Num, w : Num, h : Num, angle : Num, style : PathStyle)"></endpoint>
<signature id="UI.draw_rect+8">UI.draw_rect(**control**: `Control`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **w**: `Num`, **h**: `Num`, **angle**: `Num`, **style**: `PathStyle`)
<a class="headerlink" href="#UI.draw_rect+8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="draw_rect_detailed(control : Control, x : Num, y : Num, z : Num, w : Num, h : Num, angle : Num, radius : Num, smoothness : Num, style : PathStyle)"></endpoint>
<signature id="UI.draw_rect_detailed+10">UI.draw_rect_detailed(**control**: `Control`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **w**: `Num`, **h**: `Num`, **angle**: `Num`, **radius**: `Num`, **smoothness**: `Num`, **style**: `PathStyle`)
<a class="headerlink" href="#UI.draw_rect_detailed+10" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="draw_quad_detailed(control : Control, x : Num, y : Num, z : Num, w : Num, h : Num, angle : Num, radius : Num, smoothness : Num, color : Color)"></endpoint>
<signature id="UI.draw_quad_detailed+10">UI.draw_quad_detailed(**control**: `Control`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **w**: `Num`, **h**: `Num`, **angle**: `Num`, **radius**: `Num`, **smoothness**: `Num`, **color**: `Color`)
<a class="headerlink" href="#UI.draw_quad_detailed+10" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="draw_ring(control : Control, ox : Num, oy : Num, oz : Num, rx : Num, ry : Num, start_angle : Num, end_angle : Num, smoothness : Num, style : PathStyle)"></endpoint>
<signature id="UI.draw_ring+10">UI.draw_ring(**control**: `Control`, **ox**: `Num`, **oy**: `Num`, **oz**: `Num`, **rx**: `Num`, **ry**: `Num`, **start_angle**: `Num`, **end_angle**: `Num`, **smoothness**: `Num`, **style**: `PathStyle`)
<a class="headerlink" href="#UI.draw_ring+10" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="draw_path(control : Control, points : List, style : PathStyle, closed : Bool)"></endpoint>
<signature id="UI.draw_path+4">UI.draw_path(**control**: `Control`, **points**: `List`, **style**: `PathStyle`, **closed**: `Bool`)
<a class="headerlink" href="#UI.draw_path+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="events_emit(control : Control, type : UIEvent)"></endpoint>
<signature id="UI.events_emit+2">UI.events_emit(**control**: `Control`, **type**: `UIEvent`)
<a class="headerlink" href="#UI.events_emit+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="events_emit(control : Control, type : UIEvent, data : Any)"></endpoint>
<signature id="UI.events_emit+3">UI.events_emit(**control**: `Control`, **type**: `UIEvent`, **data**: `Any`)
<a class="headerlink" href="#UI.events_emit+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="events_emit(control : Control, type : UIEvent, data : Any, data_before : Any)"></endpoint>
<signature id="UI.events_emit+4">UI.events_emit(**control**: `Control`, **type**: `UIEvent`, **data**: `Any`, **data_before**: `Any`)
<a class="headerlink" href="#UI.events_emit+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

### UIBehave
`:::js import "luxe: world" for UIBehave`
> no docs found

- [left](#UIBehave.left)
- [top](#UIBehave.top)
- [right](#UIBehave.right)
- [bottom](#UIBehave.bottom)
- [hfill](#UIBehave.hfill)
- [vfill](#UIBehave.vfill)
- [hcenter](#UIBehave.hcenter)
- [vcenter](#UIBehave.vcenter)
- [center](#UIBehave.center)
- [fill](#UIBehave.fill)
- [break_line](#UIBehave.break_line)

<hr/>
<endpoint module="luxe: world" class="UIBehave" signature="left"></endpoint>
<signature id="UIBehave.left">UIBehave.left
<a class="headerlink" href="#UIBehave.left" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Item anchors to the item to its left or left side of parent   

<endpoint module="luxe: world" class="UIBehave" signature="top"></endpoint>
<signature id="UIBehave.top">UIBehave.top
<a class="headerlink" href="#UIBehave.top" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Item anchors to the item above it or top side of parent   

<endpoint module="luxe: world" class="UIBehave" signature="right"></endpoint>
<signature id="UIBehave.right">UIBehave.right
<a class="headerlink" href="#UIBehave.right" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Item anchors to the item to its right or right side of parent   

<endpoint module="luxe: world" class="UIBehave" signature="bottom"></endpoint>
<signature id="UIBehave.bottom">UIBehave.bottom
<a class="headerlink" href="#UIBehave.bottom" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Item anchors to the item below it or bottom side of parent   

<endpoint module="luxe: world" class="UIBehave" signature="hfill"></endpoint>
<signature id="UIBehave.hfill">UIBehave.hfill
<a class="headerlink" href="#UIBehave.hfill" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Item anchors to both left and right item or parent borders   

<endpoint module="luxe: world" class="UIBehave" signature="vfill"></endpoint>
<signature id="UIBehave.vfill">UIBehave.vfill
<a class="headerlink" href="#UIBehave.vfill" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Item anchors to both top and bottom item or parent borders   

<endpoint module="luxe: world" class="UIBehave" signature="hcenter"></endpoint>
<signature id="UIBehave.hcenter">UIBehave.hcenter
<a class="headerlink" href="#UIBehave.hcenter" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Center item horizontally, with left margin as offset   

<endpoint module="luxe: world" class="UIBehave" signature="vcenter"></endpoint>
<signature id="UIBehave.vcenter">UIBehave.vcenter
<a class="headerlink" href="#UIBehave.vcenter" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Center item vertically, with top margin as offset   

<endpoint module="luxe: world" class="UIBehave" signature="center"></endpoint>
<signature id="UIBehave.center">UIBehave.center
<a class="headerlink" href="#UIBehave.center" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Center item in both directions, with left/top margin as offset   

<endpoint module="luxe: world" class="UIBehave" signature="fill"></endpoint>
<signature id="UIBehave.fill">UIBehave.fill
<a class="headerlink" href="#UIBehave.fill" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Anchor item to all four directions   

<endpoint module="luxe: world" class="UIBehave" signature="break_line"></endpoint>
<signature id="UIBehave.break_line">UIBehave.break_line
<a class="headerlink" href="#UIBehave.break_line" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### UIClear
`:::js import "luxe: world" for UIClear`
> no docs found

- [destroy](#UIClear.destroy)
- [remove](#UIClear.remove)
- [set_invisible](#UIClear.set_invisible)
- [remove_set_invisible](#UIClear.remove_set_invisible)

<hr/>
<endpoint module="luxe: world" class="UIClear" signature="destroy"></endpoint>
<signature id="UIClear.destroy">UIClear.destroy
<a class="headerlink" href="#UIClear.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UIClear" signature="remove"></endpoint>
<signature id="UIClear.remove">UIClear.remove
<a class="headerlink" href="#UIClear.remove" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UIClear" signature="set_invisible"></endpoint>
<signature id="UIClear.set_invisible">UIClear.set_invisible
<a class="headerlink" href="#UIClear.set_invisible" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UIClear" signature="remove_set_invisible"></endpoint>
<signature id="UIClear.remove_set_invisible">UIClear.remove_set_invisible
<a class="headerlink" href="#UIClear.remove_set_invisible" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### UIContain
`:::js import "luxe: world" for UIContain`
> no docs found

- [row](#UIContain.row)
- [column](#UIContain.column)
- [layout](#UIContain.layout)
- [flex](#UIContain.flex)
- [nowrap](#UIContain.nowrap)
- [wrap](#UIContain.wrap)
- [start](#UIContain.start)
- [middle](#UIContain.middle)
- [end](#UIContain.end)
- [justify](#UIContain.justify)
- [vfit](#UIContain.vfit)
- [hfit](#UIContain.hfit)

<hr/>
<endpoint module="luxe: world" class="UIContain" signature="row"></endpoint>
<signature id="UIContain.row">UIContain.row
<a class="headerlink" href="#UIContain.row" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Items go from left to right   

<endpoint module="luxe: world" class="UIContain" signature="column"></endpoint>
<signature id="UIContain.column">UIContain.column
<a class="headerlink" href="#UIContain.column" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Items go from top to bottom   

<endpoint module="luxe: world" class="UIContain" signature="layout"></endpoint>
<signature id="UIContain.layout">UIContain.layout
<a class="headerlink" href="#UIContain.layout" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Use Free Layout model   

<endpoint module="luxe: world" class="UIContain" signature="flex"></endpoint>
<signature id="UIContain.flex">UIContain.flex
<a class="headerlink" href="#UIContain.flex" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Use Flex Layout model   

<endpoint module="luxe: world" class="UIContain" signature="nowrap"></endpoint>
<signature id="UIContain.nowrap">UIContain.nowrap
<a class="headerlink" href="#UIContain.nowrap" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Stays on a single line   

<endpoint module="luxe: world" class="UIContain" signature="wrap"></endpoint>
<signature id="UIContain.wrap">UIContain.wrap
<a class="headerlink" href="#UIContain.wrap" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Wraps to multiple lines, wrapping left to right   

<endpoint module="luxe: world" class="UIContain" signature="start"></endpoint>
<signature id="UIContain.start">UIContain.start
<a class="headerlink" href="#UIContain.start" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Items begin at start of row/column   

<endpoint module="luxe: world" class="UIContain" signature="middle"></endpoint>
<signature id="UIContain.middle">UIContain.middle
<a class="headerlink" href="#UIContain.middle" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Items begin at middle of row/column   

<endpoint module="luxe: world" class="UIContain" signature="end"></endpoint>
<signature id="UIContain.end">UIContain.end
<a class="headerlink" href="#UIContain.end" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Items begin at end of row/column   

<endpoint module="luxe: world" class="UIContain" signature="justify"></endpoint>
<signature id="UIContain.justify">UIContain.justify
<a class="headerlink" href="#UIContain.justify" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Insert spacing between items to stretch elements across whole row/column   

<endpoint module="luxe: world" class="UIContain" signature="vfit"></endpoint>
<signature id="UIContain.vfit">UIContain.vfit
<a class="headerlink" href="#UIContain.vfit" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Items stretch height to fill vertical space   

<endpoint module="luxe: world" class="UIContain" signature="hfit"></endpoint>
<signature id="UIContain.hfit">UIContain.hfit
<a class="headerlink" href="#UIContain.hfit" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Items stretch width to fill horizontal space   

### UIDebugMode
`:::js import "luxe: world" for UIDebugMode`
> no docs found

- [none](#UIDebugMode.none)
- [basic](#UIDebugMode.basic)

<hr/>
<endpoint module="luxe: world" class="UIDebugMode" signature="none"></endpoint>
<signature id="UIDebugMode.none">UIDebugMode.none
<a class="headerlink" href="#UIDebugMode.none" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UIDebugMode" signature="basic"></endpoint>
<signature id="UIDebugMode.basic">UIDebugMode.basic
<a class="headerlink" href="#UIDebugMode.basic" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### UIDrop
`:::js import "luxe: world" for UIDrop`
> no docs found

- [start](#UIDrop.start)
- [end](#UIDrop.end)
- [move](#UIDrop.move)
- [drop](#UIDrop.drop)

<hr/>
<endpoint module="luxe: world" class="UIDrop" signature="start"></endpoint>
<signature id="UIDrop.start">UIDrop.start
<a class="headerlink" href="#UIDrop.start" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UIDrop" signature="end"></endpoint>
<signature id="UIDrop.end">UIDrop.end
<a class="headerlink" href="#UIDrop.end" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UIDrop" signature="move"></endpoint>
<signature id="UIDrop.move">UIDrop.move
<a class="headerlink" href="#UIDrop.move" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UIDrop" signature="drop"></endpoint>
<signature id="UIDrop.drop">UIDrop.drop
<a class="headerlink" href="#UIDrop.drop" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### UIEvent
`:::js import "luxe: world" for UIEvent`
> The built in UI events that all controls can potentially use.

- [name](#UIEvent.name)(**value**: `Any`)
- [unknown](#UIEvent.unknown)
- [enter](#UIEvent.enter)
- [exit](#UIEvent.exit)
- [press](#UIEvent.press)
- [release](#UIEvent.release)
- [scroll](#UIEvent.scroll)
- [move](#UIEvent.move)
- [key](#UIEvent.key)
- [text](#UIEvent.text)
- [focus](#UIEvent.focus)
- [unfocus](#UIEvent.unfocus)
- [capture](#UIEvent.capture)
- [uncapture](#UIEvent.uncapture)
- [commit](#UIEvent.commit)
- [destroy](#UIEvent.destroy)
- [language](#UIEvent.language)
- [change](#UIEvent.change)
- [bounds](#UIEvent.bounds)
- [drag](#UIEvent.drag)

<hr/>
<endpoint module="luxe: world" class="UIEvent" signature="name(value : Any)"></endpoint>
<signature id="UIEvent.name">UIEvent.name(**value**: `Any`)
<a class="headerlink" href="#UIEvent.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Converts a UIEvent value to a readable name.
> 
>   ```js
>   Log.print(UIEvent.name(UIEvent.move)) //prints "move"
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="unknown"></endpoint>
<signature id="UIEvent.unknown">UIEvent.unknown
<a class="headerlink" href="#UIEvent.unknown" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> An event of unknown type, invalid. This is the default value.   

<endpoint module="luxe: world" class="UIEvent" signature="enter"></endpoint>
<signature id="UIEvent.enter">UIEvent.enter
<a class="headerlink" href="#UIEvent.enter" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> An input cursor has entered this control. (e.g on mouse enter).
> Sends no additional data in the event.
> 
>   ```js
>   if(event.type == UIEvent.enter) {
>     Log.print("entered control!")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="exit"></endpoint>
<signature id="UIEvent.exit">UIEvent.exit
<a class="headerlink" href="#UIEvent.exit" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> An input cursor has left this control. (e.g on mouse exit)
> Sends no additional data in the event.
> 
>   ```js
>   if(event.type == UIEvent.exit) {
>     Log.print("exited control!")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="press"></endpoint>
<signature id="UIEvent.press">UIEvent.press
<a class="headerlink" href="#UIEvent.press" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> An input press event (e.g mouse button was pressed down). a.k.a "down"
> Sends `event.x`, `event.y` and `event.button`.
> 
>   ```js
>   if(event.type == UIEvent.press) {
>     var button = MouseButton.name(event.button)
>     Log.print("pressed down on control at `%(event.x)`,`%(event.y)`")
>     Log.print("  button was `%(button)`")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="release"></endpoint>
<signature id="UIEvent.release">UIEvent.release
<a class="headerlink" href="#UIEvent.release" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> An input release event (e.g mouse button was released). a.k.a "up"
> Sends `event.x`, `event.y` and `event.button`.
> 
>   ```js
>   if(event.type == UIEvent.press) {
>     var button = MouseButton.name(event.button)
>     Log.print("released input on control at `%(event.x)`,`%(event.y)`")
>     Log.print("  button was `%(button)`")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="scroll"></endpoint>
<signature id="UIEvent.scroll">UIEvent.scroll
<a class="headerlink" href="#UIEvent.scroll" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> A scroll event (e.g mouse wheel).
> Sends `event.x`, `event.y` where `x` is the horizontal scroll amount, 
> and `y` is the vertical scroll amount.
> 
>   ```js
>   if(event.type == UIEvent.scroll) {
>     Log.print("scroll amount `%(event.x)`,`%(event.y)`")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="move"></endpoint>
<signature id="UIEvent.move">UIEvent.move
<a class="headerlink" href="#UIEvent.move" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> An input move event (e.g mouse movement).
> Sends `event.x`, `event.y` as the position of the input.
> 
>   ```js
>   if(event.type == UIEvent.press) {
>     Log.print("move on control at `%(event.x)`,`%(event.y)`")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="key"></endpoint>
<signature id="UIEvent.key">UIEvent.key
<a class="headerlink" href="#UIEvent.key" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> A key input event.
> Sends a few useful values:
> 
> - `event.key` - a [Key](../input/#key) value
> - `event.scan` - a [Scan](../input/#scan) value
> - `event.mod` - a [ModState](../input/#modstate) value
> - `event.down` - a `Bool` value, whether the key is down or not
> - `event.repeat` - a `Bool` value, whether the event is from a key repeat
> 
>   ```js
>   if(event.type == UIEvent.key) {
>     var down = event.down ? "pressed" : "released"
>     Log.print("key %(down), key was `%(Key.name(event.key))`")
>     Log.print("  scan `%(Scan.name(event.scan))`, repeat? %(event.repeat)")
>     if(event.mod.lshift || event.mod.rshift) {
>       Log.print("shift was also held down!")
>     }
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="text"></endpoint>
<signature id="UIEvent.text">UIEvent.text
<a class="headerlink" href="#UIEvent.text" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> A control has sent a text event, which originates from typing.
> 
> These events allow handling complex input that comes from the OS
> level IME input dialogs. On the simplest level, displaying `event.text`
> is enough to get started. 
> 
> Sends the following:
> 
> - `event.text` - the latest text displayed
> - `event.text_start` - the start of the modified text
> - `event.text_length` - the length of the modified text
> - `event.text_type` - a [TextEvent](../input/#textevent) type (`edit` or `input`)
> 
> The easiest way to understand might be to see.
> [This video](https://twitter.com/ruby0x1/status/928435874718679040) shows this at work.
> 
> As a user is typing, there may be candidates avaiable to select from, 
> when this is true, these are sent as `TextInput.edit` events, with a start and end.
> When a candidate is selected (or no choices), a `TextEvent.input` is sent with the `text`.   

<endpoint module="luxe: world" class="UIEvent" signature="focus"></endpoint>
<signature id="UIEvent.focus">UIEvent.focus
<a class="headerlink" href="#UIEvent.focus" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> A control has gained focus.
> Sends no additional data in the event.
> 
>   ```js
>   if(event.type == UIEvent.focus) {
>     Log.print("gained focus!")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="unfocus"></endpoint>
<signature id="UIEvent.unfocus">UIEvent.unfocus
<a class="headerlink" href="#UIEvent.unfocus" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> A control has lost focus.
> Sends no additional data in the event.
> 
>   ```js
>   if(event.type == UIEvent.unfocus) {
>     Log.print("lost focus!")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="capture"></endpoint>
<signature id="UIEvent.capture">UIEvent.capture
<a class="headerlink" href="#UIEvent.capture" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> A control has been captured.
> 
>   ```js
>   if(event.type == UIEvent.capture) {
>     Log.print("gained input capture!")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="uncapture"></endpoint>
<signature id="UIEvent.uncapture">UIEvent.uncapture
<a class="headerlink" href="#UIEvent.uncapture" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> A control has lost capture status.
> 
>   ```js
>   if(event.type == UIEvent.uncapture) {
>     Log.print("lost input capture!")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="commit"></endpoint>
<signature id="UIEvent.commit">UIEvent.commit
<a class="headerlink" href="#UIEvent.commit" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> When a control has changeable state (like an editable text control),
> it will send a `commit` event when the contents are being applied/committed.
> For example, if you are typing text and hit enter, or unfocus the control.
> 
>   ```js
>   if(event.type == UIEvent.uncapture) {
>     Log.print("lost input capture!")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="destroy"></endpoint>
<signature id="UIEvent.destroy">UIEvent.destroy
<a class="headerlink" href="#UIEvent.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> When a control is destroyed you'll get notified here.
> Keep in mind that it's destroyed.
> 
>   ```js
>   if(event.type == UIEvent.destroy) {
>     Log.print("destroyed!")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="language"></endpoint>
<signature id="UIEvent.language">UIEvent.language
<a class="headerlink" href="#UIEvent.language" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> When the UI lanuage changes, your control will receive this event.
> 
>   ```js
>   if(event.type == UIEvent.language) {
>     Log.print("language changed.. I should update my size..")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="change"></endpoint>
<signature id="UIEvent.change">UIEvent.change
<a class="headerlink" href="#UIEvent.change" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Change events are context specific, but notify you of a change in state.
> For example, [UIWindow](../ui/window) sends a change event with [UIWindowChange](../ui/window/#uiwindowchange) to notify when a window was closed, collapsed or uncollapsed. A [UIText](../ui/text) sends a change event
> when the text has been changed, via typing or otherwise.
> 
> In each case, `event.change` contains the relevant data.
> 
>   ```js
>   //UIText example
>   if(event.type == UIEvent.change) {
>     Log.print("text changed `%(event.change)`!")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="bounds"></endpoint>
<signature id="UIEvent.bounds">UIEvent.bounds
<a class="headerlink" href="#UIEvent.bounds" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> A control has changed bounds (note: this may not be working as intended right now).
> Sends `event.dx`, `event.dy` and `event.dw`, `event.dh` where `d` means `delta`.
> i.e the change in bounds as a difference between now and before.
> 
>   ```js
>   if(event.type == UIEvent.bounds) {
>     if(event.dx != 0) Log.print("moved on x by %(event.dx) amount!")
>     if(event.dy != 0) Log.print("moved on y by %(event.dy) amount!")
>     if(event.dw != 0) Log.print("width changed by %(event.dw) amount!")
>     if(event.dh != 0) Log.print("height changed by %(event.dh) amount!")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="drag"></endpoint>
<signature id="UIEvent.drag">UIEvent.drag
<a class="headerlink" href="#UIEvent.drag" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> When a control is dragged or dropped on the UI canvas.
> The data field contains the kind of event, e.g UIDrag.start or UIDrag.end.
> The x/y is the start, and end_x/end_y is the end (for a start they're the same)
> 
>   ```js
>   if(event.type == UIEvent.drag) {
>     Log.print("control drag changed.. %(event.data)")
>   }
>   ```   

### UIImageFit
`:::js import "luxe: world" for UIImageFit`
> no docs found

- [fill](#UIImageFit.fill)
- [contain](#UIImageFit.contain)
- [cover](#UIImageFit.cover)
- [keep_width](#UIImageFit.keep_width)
- [keep_height](#UIImageFit.keep_height)

<hr/>
<endpoint module="luxe: world" class="UIImageFit" signature="fill"></endpoint>
<signature id="UIImageFit.fill">UIImageFit.fill
<a class="headerlink" href="#UIImageFit.fill" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UIImageFit" signature="contain"></endpoint>
<signature id="UIImageFit.contain">UIImageFit.contain
<a class="headerlink" href="#UIImageFit.contain" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UIImageFit" signature="cover"></endpoint>
<signature id="UIImageFit.cover">UIImageFit.cover
<a class="headerlink" href="#UIImageFit.cover" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UIImageFit" signature="keep_width"></endpoint>
<signature id="UIImageFit.keep_width">UIImageFit.keep_width
<a class="headerlink" href="#UIImageFit.keep_width" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UIImageFit" signature="keep_height"></endpoint>
<signature id="UIImageFit.keep_height">UIImageFit.keep_height
<a class="headerlink" href="#UIImageFit.keep_height" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### UIImageFlags
`:::js import "luxe: world" for UIImageFlags`
> no docs found

- [none](#UIImageFlags.none)
- [pixelated](#UIImageFlags.pixelated)
- [use_mips](#UIImageFlags.use_mips)

<hr/>
<endpoint module="luxe: world" class="UIImageFlags" signature="none"></endpoint>
<signature id="UIImageFlags.none">UIImageFlags.none
<a class="headerlink" href="#UIImageFlags.none" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> uses linear interpolation samplers, interpolating smoothly between pixels.   

<endpoint module="luxe: world" class="UIImageFlags" signature="pixelated"></endpoint>
<signature id="UIImageFlags.pixelated">UIImageFlags.pixelated
<a class="headerlink" href="#UIImageFlags.pixelated" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> uses nearest neighbor samplers, leading to an interpolated look.   

<endpoint module="luxe: world" class="UIImageFlags" signature="use_mips"></endpoint>
<signature id="UIImageFlags.use_mips">UIImageFlags.use_mips
<a class="headerlink" href="#UIImageFlags.use_mips" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> uses trilinear interpolation samplers, interpolating smoothly between pixels and mip levels.   

### UILayoutMode
`:::js import "luxe: world" for UILayoutMode`
> no docs found

- [none](#UILayoutMode.none)
- [flex](#UILayoutMode.flex)

<hr/>
<endpoint module="luxe: world" class="UILayoutMode" signature="none"></endpoint>
<signature id="UILayoutMode.none">UILayoutMode.none
<a class="headerlink" href="#UILayoutMode.none" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayoutMode" signature="flex"></endpoint>
<signature id="UILayoutMode.flex">UILayoutMode.flex
<a class="headerlink" href="#UILayoutMode.flex" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### UIRenderMode
`:::js import "luxe: world" for UIRenderMode`
> no docs found

- [unknown](#UIRenderMode.unknown)
- [image](#UIRenderMode.image)
- [world](#UIRenderMode.world)

<hr/>
<endpoint module="luxe: world" class="UIRenderMode" signature="unknown"></endpoint>
<signature id="UIRenderMode.unknown">UIRenderMode.unknown
<a class="headerlink" href="#UIRenderMode.unknown" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UIRenderMode" signature="image"></endpoint>
<signature id="UIRenderMode.image">UIRenderMode.image
<a class="headerlink" href="#UIRenderMode.image" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UIRenderMode" signature="world"></endpoint>
<signature id="UIRenderMode.world">UIRenderMode.world
<a class="headerlink" href="#UIRenderMode.world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### WorldEventType
`:::js import "luxe: world" for WorldEventType`
> no docs found

- [unknown](#WorldEventType.unknown)
- [create](#WorldEventType.create)
- [destroy](#WorldEventType.destroy)
- [tick](#WorldEventType.tick)
- [modifier_tick](#WorldEventType.modifier_tick)
- [name](#WorldEventType.name)(**value**: `WorldEventType`)

<hr/>
<endpoint module="luxe: world" class="WorldEventType" signature="unknown"></endpoint>
<signature id="WorldEventType.unknown">WorldEventType.unknown
<a class="headerlink" href="#WorldEventType.unknown" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="WorldEventType" signature="create"></endpoint>
<signature id="WorldEventType.create">WorldEventType.create
<a class="headerlink" href="#WorldEventType.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="WorldEventType" signature="destroy"></endpoint>
<signature id="WorldEventType.destroy">WorldEventType.destroy
<a class="headerlink" href="#WorldEventType.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="WorldEventType" signature="tick"></endpoint>
<signature id="WorldEventType.tick">WorldEventType.tick
<a class="headerlink" href="#WorldEventType.tick" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="WorldEventType" signature="modifier_tick"></endpoint>
<signature id="WorldEventType.modifier_tick">WorldEventType.modifier_tick
<a class="headerlink" href="#WorldEventType.modifier_tick" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="WorldEventType" signature="name(value : WorldEventType)"></endpoint>
<signature id="WorldEventType.name">WorldEventType.name(**value**: `WorldEventType`)
<a class="headerlink" href="#WorldEventType.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

### WorldRenderDesc
`:::js import "luxe: world" for WorldRenderDesc`
> no docs found

- [camera](#WorldRenderDesc.camera)
- [camera](#WorldRenderDesc.camera=)=(v : Any)
- [camera](#WorldRenderDesc.camera)(**v**: `Any`)
- [cull_camera](#WorldRenderDesc.cull_camera)
- [cull_camera](#WorldRenderDesc.cull_camera=)=(v : Any)
- [cull_camera](#WorldRenderDesc.cull_camera)(**v**: `Any`)
- [new](#WorldRenderDesc.new)()

<hr/>
<endpoint module="luxe: world" class="WorldRenderDesc" signature="camera"></endpoint>
<signature id="WorldRenderDesc.camera">WorldRenderDesc.camera
<a class="headerlink" href="#WorldRenderDesc.camera" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="WorldRenderDesc" signature="camera=(v : Any)"></endpoint>
<signature id="WorldRenderDesc.camera=">WorldRenderDesc.camera=(v : Any)
<a class="headerlink" href="#WorldRenderDesc.camera=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="WorldRenderDesc" signature="camera(v : Any)"></endpoint>
<signature id="WorldRenderDesc.camera">WorldRenderDesc.camera(**v**: `Any`)
<a class="headerlink" href="#WorldRenderDesc.camera" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="WorldRenderDesc" signature="cull_camera"></endpoint>
<signature id="WorldRenderDesc.cull_camera">WorldRenderDesc.cull_camera
<a class="headerlink" href="#WorldRenderDesc.cull_camera" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="WorldRenderDesc" signature="cull_camera=(v : Any)"></endpoint>
<signature id="WorldRenderDesc.cull_camera=">WorldRenderDesc.cull_camera=(v : Any)
<a class="headerlink" href="#WorldRenderDesc.cull_camera=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="WorldRenderDesc" signature="cull_camera(v : Any)"></endpoint>
<signature id="WorldRenderDesc.cull_camera">WorldRenderDesc.cull_camera(**v**: `Any`)
<a class="headerlink" href="#WorldRenderDesc.cull_camera" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="WorldRenderDesc" signature="new()"></endpoint>
<signature id="WorldRenderDesc.new">WorldRenderDesc.new()
<a class="headerlink" href="#WorldRenderDesc.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js WorldRenderDesc`
> no docs found   

