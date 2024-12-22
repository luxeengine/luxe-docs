#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2024.12.4`)  


---

## `luxe: system/transform.modifier` module

- [Data](#data)   
- [System](#system)   
- [Transform](#transform)   
- [TransformApplyMask](#transformapplymask)   

---

### Data
`:::js import "luxe: system/transform.modifier" for Data`
> no docs found

- `:::js var pos : Double3 = [0, 0, 0]`
- `:::js var rotation : Float3 = [0, 0, 0]`
- `:::js var scale : Float3 = [1, 1, 1]`
- `:::js var link : Link = null`

<hr/>
### System
`:::js import "luxe: system/transform.modifier" for System`
> no docs found

- [new](#System.new)(**world**: `World`)

<hr/>
<endpoint module="luxe: system/transform.modifier" class="System" signature="new(world : World)"></endpoint>
<signature id="System.new">System.new(**world**: `World`)
<a class="headerlink" href="#System.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js System`
> no docs found   

### Transform
`:::js import "luxe: system/transform.modifier" for Transform`
> A transform modifier defines where a entity is.
> That includes position, rotation and scale.
> A `Transform` can also be linked to another `Transform`, in which case its values are relative to their link target.
>   
> While not all entities need to be "somewhere" locally, a lot of them do, which is when this modifier is used.
> Other modifiers on the same entity aren't required to read and react to the `Transform`, but most do, allowing you to use this to move things (like Sprites, Meshes, Physics shapes, etc...).

- [id](#Transform.id)
- [create](#Transform.create+3)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
- [create](#Transform.create+4)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
- [create](#Transform.create)(**entity**: `Entity`)
- [destroy](#Transform.destroy)(**entity**: `Entity`)
- [has](#Transform.has)(**entity**: `Entity`)
- [get_link](#Transform.get_link)(**entity**: `Entity`)
- [get_linked](#Transform.get_linked)(**entity**: `Entity`)
- [link](#Transform.link+3)(**entity**: `Entity`, **target_entity**: `Entity`, **reset_local**: `Bool`)
- [link](#Transform.link+2)(**entity**: `Entity`, **target_entity**: `Entity`)
- [unlink](#Transform.unlink+2)(**entity**: `Entity`, **reset_local**: `Bool`)
- [unlink](#Transform.unlink)(**entity**: `Entity`)
- [look_at_and_move](#Transform.look_at_and_move+5)(**entity**: `Entity`, **pos**: `Vec`, **target**: `Vec`, **up**: `Vec`, **invert**: `Bool`)
- [look_at_and_move](#Transform.look_at_and_move+4)(**entity**: `Entity`, **pos**: `Vec`, **target**: `Vec`, **up**: `Vec`)
- [look_at_and_move](#Transform.look_at_and_move+3)(**entity**: `Entity`, **pos**: `Vec`, **target**: `Vec`)
- [look_at](#Transform.look_at+4)(**entity**: `Entity`, **target**: `Vec`, **up**: `Vec`, **invert**: `Bool`)
- [look_at](#Transform.look_at+3)(**entity**: `Entity`, **target**: `Vec`, **up**: `Vec`)
- [look_at](#Transform.look_at+2)(**entity**: `Entity`, **target**: `Vec`)
- [set_snap](#Transform.set_snap+4)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
- [set_snap](#Transform.set_snap+3)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
- [set_pos](#Transform.set_pos+4)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
- [set_pos](#Transform.set_pos+3)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
- [set_pos_world](#Transform.set_pos_world+4)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
- [set_pos_world](#Transform.set_pos_world+3)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
- [set_pos_x](#Transform.set_pos_x+2)(**entity**: `Entity`, **x**: `Num`)
- [set_pos_y](#Transform.set_pos_y+2)(**entity**: `Entity`, **y**: `Num`)
- [set_pos_z](#Transform.set_pos_z+2)(**entity**: `Entity`, **z**: `Num`)
- [set_pos_x_world](#Transform.set_pos_x_world+2)(**entity**: `Entity`, **x**: `Num`)
- [set_pos_y_world](#Transform.set_pos_y_world+2)(**entity**: `Entity`, **y**: `Num`)
- [set_pos_z_world](#Transform.set_pos_z_world+2)(**entity**: `Entity`, **z**: `Num`)
- [set_scale](#Transform.set_scale+3)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
- [set_scale](#Transform.set_scale+4)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
- [set_rotation_slerp_angle_axis](#Transform.set_rotation_slerp_angle_axis+5)(**entity**: `Entity`, **axis**: `Vec`, **from**: `Num`, **to**: `Num`, **t**: `Num`)
- [set_rotation_slerp_angle_axis_world](#Transform.set_rotation_slerp_angle_axis_world+5)(**entity**: `Entity`, **axis**: `Vec`, **from**: `Num`, **to**: `Num`, **t**: `Num`)
- [set_rotation_slerp](#Transform.set_rotation_slerp+4)(**entity**: `Entity`, **from**: `Vec`, **to**: `Vec`, **t**: `Num`)
- [set_rotation_slerp_world](#Transform.set_rotation_slerp_world+4)(**entity**: `Entity`, **from**: `Vec`, **to**: `Vec`, **t**: `Num`)
- [set_rotation](#Transform.set_rotation+5)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **w**: `Num`)
- [set_rotation_world](#Transform.set_rotation_world+5)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **w**: `Num`)
- [set_angle_axis](#Transform.set_angle_axis+5)(**entity**: `Entity`, **degrees**: `Any`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
- [set_angle_axis_world](#Transform.set_angle_axis_world+5)(**entity**: `Entity`, **degrees**: `Any`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
- [set_euler](#Transform.set_euler+4)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
- [set_euler_world](#Transform.set_euler_world+4)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
- [set_euler_x](#Transform.set_euler_x+2)(**entity**: `Entity`, **x**: `Num`)
- [set_euler_y](#Transform.set_euler_y+2)(**entity**: `Entity`, **y**: `Num`)
- [set_euler_z](#Transform.set_euler_z+2)(**entity**: `Entity`, **z**: `Num`)
- [set_euler_x_world](#Transform.set_euler_x_world+2)(**entity**: `Entity`, **x**: `Num`)
- [set_euler_y_world](#Transform.set_euler_y_world+2)(**entity**: `Entity`, **y**: `Num`)
- [set_euler_z_world](#Transform.set_euler_z_world+2)(**entity**: `Entity`, **z**: `Num`)
- [rotate_angle_axis_slerp](#Transform.rotate_angle_axis_slerp+3)(**entity**: `Entity`, **axis**: `Vec`, **angle_amount**: `Num`)
- [rotate_angle_axis_slerp_world](#Transform.rotate_angle_axis_slerp_world+3)(**entity**: `Entity`, **axis**: `Vec`, **angle_amount**: `Num`)
- [rotate_around_world](#Transform.rotate_around_world+8)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **axis_x**: `Num`, **axis_y**: `Num`, **axis_z**: `Num`, **degrees**: `Num`)
- [rotate_around](#Transform.rotate_around+8)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **axis_x**: `Num`, **axis_y**: `Num`, **axis_z**: `Num`, **degrees**: `Num`)
- [rotate_angle_axis](#Transform.rotate_angle_axis+5)(**entity**: `Entity`, **degrees**: `Any`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
- [rotate_angle_axis_world](#Transform.rotate_angle_axis_world+5)(**entity**: `Entity`, **degrees**: `Any`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
- [rotate_euler](#Transform.rotate_euler+4)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
- [rotate_euler_world](#Transform.rotate_euler_world+4)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
- [translate](#Transform.translate+4)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
- [translate](#Transform.translate+3)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
- [get_pos](#Transform.get_pos)(**entity**: `Entity`)
- [get_pos_x](#Transform.get_pos_x)(**entity**: `Entity`)
- [get_pos_y](#Transform.get_pos_y)(**entity**: `Entity`)
- [get_pos_z](#Transform.get_pos_z)(**entity**: `Entity`)
- [get_pos_world](#Transform.get_pos_world)(**entity**: `Entity`)
- [get_pos_world_unsnapped](#Transform.get_pos_world_unsnapped)(**entity**: `Entity`)
- [get_pos_x_world](#Transform.get_pos_x_world)(**entity**: `Entity`)
- [get_pos_y_world](#Transform.get_pos_y_world)(**entity**: `Entity`)
- [get_pos_z_world](#Transform.get_pos_z_world)(**entity**: `Entity`)
- [rotate2D](#Transform.rotate2D+2)(**entity**: `Entity`, **degrees**: `Num`)
- [set_angle2D](#Transform.set_angle2D+2)(**entity**: `Entity`, **degrees**: `Num`)
- [set_angle2D_world](#Transform.set_angle2D_world+2)(**entity**: `Entity`, **degrees**: `Num`)
- [get_angle2D](#Transform.get_angle2D)(**entity**: `Entity`)
- [get_angle2D_world](#Transform.get_angle2D_world)(**entity**: `Entity`)
- [set_depth2D](#Transform.set_depth2D+2)(**entity**: `Entity`, **depth**: `Num`)
- [get_depth2D](#Transform.get_depth2D)(**entity**: `Entity`)
- [set_depth2D_world](#Transform.set_depth2D_world+2)(**entity**: `Entity`, **depth**: `Num`)
- [get_depth2D_world](#Transform.get_depth2D_world)(**entity**: `Entity`)
- [get_world_matrix](#Transform.get_world_matrix+2)(**entity**: `Entity`, **into_matrix**: `Floats`)
- [get_rotation](#Transform.get_rotation)(**entity**: `Entity`)
- [get_rotation_world](#Transform.get_rotation_world)(**entity**: `Entity`)
- [get_rotation_matrix](#Transform.get_rotation_matrix+2)(**entity**: `Entity`, **into_matrix**: `Floats`)
- [get_euler](#Transform.get_euler)(**entity**: `Entity`)
- [get_euler_x](#Transform.get_euler_x)(**entity**: `Entity`)
- [get_euler_y](#Transform.get_euler_y)(**entity**: `Entity`)
- [get_euler_z](#Transform.get_euler_z)(**entity**: `Entity`)
- [get_euler_world](#Transform.get_euler_world)(**entity**: `Entity`)
- [get_euler_x_world](#Transform.get_euler_x_world)(**entity**: `Entity`)
- [get_euler_y_world](#Transform.get_euler_y_world)(**entity**: `Entity`)
- [get_euler_z_world](#Transform.get_euler_z_world)(**entity**: `Entity`)
- [get_scale](#Transform.get_scale)(**entity**: `Entity`)
- [get_scale_x](#Transform.get_scale_x)(**entity**: `Entity`)
- [get_scale_y](#Transform.get_scale_y)(**entity**: `Entity`)
- [get_scale_z](#Transform.get_scale_z)(**entity**: `Entity`)
- [get_scale_world](#Transform.get_scale_world)(**entity**: `Entity`)
- [get_scale_x_world](#Transform.get_scale_x_world)(**entity**: `Entity`)
- [get_scale_y_world](#Transform.get_scale_y_world)(**entity**: `Entity`)
- [get_scale_z_world](#Transform.get_scale_z_world)(**entity**: `Entity`)
- [get_right](#Transform.get_right)(**entity**: `Entity`)
- [get_forward](#Transform.get_forward)(**entity**: `Entity`)
- [get_up](#Transform.get_up)(**entity**: `Entity`)
- [sync](#Transform.sync)(**entity**: `Entity`)
- [sync_block](#Transform.sync_block+2)(**entity**: `Entity`, **mask**: `TransformApplyMask`)
- [sync_world](#Transform.sync_world)(**world**: `World`)
- [transform_by](#Transform.transform_by+2)(**entity**: `Entity`, **other**: `Entity`)
- [scale_by](#Transform.scale_by+3)(**entity**: `Entity`, **scale**: `Float3`, **origin**: `Float3`)
- [rotate_euler_by](#Transform.rotate_euler_by+3)(**entity**: `Entity`, **euler**: `Float3`, **origin**: `Float3`)
- [local_vector_to_world](#Transform.local_vector_to_world+4)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
- [world_vector_to_local](#Transform.world_vector_to_local+4)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
- [local_dir_to_world](#Transform.local_dir_to_world+4)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
- [world_dir_to_local](#Transform.world_dir_to_local+4)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
- [local_point_to_world](#Transform.local_point_to_world+4)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
- [local_point_to_world](#Transform.local_point_to_world+5)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **scaled**: `Bool`)
- [world_point_to_local](#Transform.world_point_to_local+4)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
- [world_point_to_local](#Transform.world_point_to_local+5)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **scaled**: `Bool`)
- [listen_all](#Transform.listen_all+2)(**world**: `World`, **fn**: `Fn`)
- [unlisten_all](#Transform.unlisten_all+2)(**world**: `World`, **handle**: `Handle`)
- [listen](#Transform.listen+2)(**entity**: `Entity`, **fn**: `Fn`)
- [unlisten](#Transform.unlisten+2)(**entity**: `Entity`, **handle**: `Handle`)

<hr/>
<endpoint module="luxe: system/transform.modifier" class="Transform" signature="id"></endpoint>
<signature id="Transform.id">Transform.id
<a class="headerlink" href="#Transform.id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="create(entity : Entity, x : Num, y : Num)"></endpoint>
<signature id="Transform.create+3">Transform.create(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
<a class="headerlink" href="#Transform.create+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Attach a `Transform` modifier to an entity with the given `x` and `y` position (with a z of 0)   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="create(entity : Entity, x : Num, y : Num, z : Num)"></endpoint>
<signature id="Transform.create+4">Transform.create(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Transform.create+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Attach a `Transform` modifier to an entity with the given `x`, `y` and `z` position   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="create(entity : Entity)"></endpoint>
<signature id="Transform.create">Transform.create(**entity**: `Entity`)
<a class="headerlink" href="#Transform.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Attach a `Transform` modifier to an entity.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="destroy(entity : Entity)"></endpoint>
<signature id="Transform.destroy">Transform.destroy(**entity**: `Entity`)
<a class="headerlink" href="#Transform.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Detatch a `Transform` modifier from an entity.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="has(entity : Entity)"></endpoint>
<signature id="Transform.has">Transform.has(**entity**: `Entity`)
<a class="headerlink" href="#Transform.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> get whether an entity has an attached `Transform`.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_link(entity : Entity)"></endpoint>
<signature id="Transform.get_link">Transform.get_link(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_link" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> Get what entity this entity is linked to. So what entity the position/rotation/scale of this transform are relative to.
> Linked to entity always has a `Transform` of its own.
> In case `Transform` isn't linked to anything, returns `null` and transformations are global.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_linked(entity : Entity)"></endpoint>
<signature id="Transform.get_linked">Transform.get_linked(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_linked" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> Get what entities are linked to this entity (opposite relationship as `get_link`).
> Transformation values of linked entities are relative to this entity.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="link(entity : Entity, target_entity : Entity, reset_local : Bool)"></endpoint>
<signature id="Transform.link+3">Transform.link(**entity**: `Entity`, **target_entity**: `Entity`, **reset_local**: `Bool`)
<a class="headerlink" href="#Transform.link+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Link one `Transform` to another.
> The `Transform` values will now be be relative to the link target, meaning the link target `Transform` position, rotation and scale all apply to the local position, rotation, scale of this `Transform`.
> When using non-uniform scales somewhere in your transform link hierarchy you can get transform deformations that would not be possible with just a single transform.
> 
> In other environments, this transform link is often part of the object hierarchy, but here it's specific to transforms and other hierarchies aren't bound to follow the same links.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="link(entity : Entity, target_entity : Entity)"></endpoint>
<signature id="Transform.link+2">Transform.link(**entity**: `Entity`, **target_entity**: `Entity`)
<a class="headerlink" href="#Transform.link+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Link one `Transform` to another.
> The `Transform` values will now be be relative to the link target, meaning the link target `Transform` position, rotation and scale all apply to the local position, rotation, scale of this `Transform`.
> When using non-uniform scales somewhere in your transform link hierarchy you can get transform deformations that would not be possible with just a single transform.
> 
> In other environments, this transform link is often part of the object hierarchy, but here it's specific to transforms and other hierarchies aren't bound to follow the same links.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="unlink(entity : Entity, reset_local : Bool)"></endpoint>
<signature id="Transform.unlink+2">Transform.unlink(**entity**: `Entity`, **reset_local**: `Bool`)
<a class="headerlink" href="#Transform.unlink+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Unlink a `Transform`. Local position will be kept (unless reset), so if your parent isnt at the origin, expect the transform to move, or save and reapply the world position.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="unlink(entity : Entity)"></endpoint>
<signature id="Transform.unlink">Transform.unlink(**entity**: `Entity`)
<a class="headerlink" href="#Transform.unlink" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Unlink a `Transform`. Local position will be kept, so if your parent isnt at the origin, expect the transform to move, or save and reapply the world position.
> 
> ```js
>   //get the current jar position
>   var pos = Transform.get_pos_world(_jar)
>   //unlink the jar from the player first
>   Transform.unlink(_jar)
>   //set the position for the jar, which now refers 
>   //to world space since the jar has no parent
>   //this makes the jar stay in the same place
>   Transform.set_pos(_jar, pos.x, pos.y, pos.z)
> ```   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="look_at_and_move(entity : Entity, pos : Vec, target : Vec, up : Vec, invert : Bool)"></endpoint>
<signature id="Transform.look_at_and_move+5">Transform.look_at_and_move(**entity**: `Entity`, **pos**: `Vec`, **target**: `Vec`, **up**: `Vec`, **invert**: `Bool`)
<a class="headerlink" href="#Transform.look_at_and_move+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Move `Transform` somewhere else, then look towards target position.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="look_at_and_move(entity : Entity, pos : Vec, target : Vec, up : Vec)"></endpoint>
<signature id="Transform.look_at_and_move+4">Transform.look_at_and_move(**entity**: `Entity`, **pos**: `Vec`, **target**: `Vec`, **up**: `Vec`)
<a class="headerlink" href="#Transform.look_at_and_move+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Move `Transform` somewhere else, then look towards target position.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="look_at_and_move(entity : Entity, pos : Vec, target : Vec)"></endpoint>
<signature id="Transform.look_at_and_move+3">Transform.look_at_and_move(**entity**: `Entity`, **pos**: `Vec`, **target**: `Vec`)
<a class="headerlink" href="#Transform.look_at_and_move+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Move `Transform` somewhere else, then look towards target position.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="look_at(entity : Entity, target : Vec, up : Vec, invert : Bool)"></endpoint>
<signature id="Transform.look_at+4">Transform.look_at(**entity**: `Entity`, **target**: `Vec`, **up**: `Vec`, **invert**: `Bool`)
<a class="headerlink" href="#Transform.look_at+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Rotate `Transform` to look at a position in worldspace, 
>       rotated around that new view axis so the `Transform` 'up' aligns with the `up` input as closely as possible.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="look_at(entity : Entity, target : Vec, up : Vec)"></endpoint>
<signature id="Transform.look_at+3">Transform.look_at(**entity**: `Entity`, **target**: `Vec`, **up**: `Vec`)
<a class="headerlink" href="#Transform.look_at+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Rotate `Transform` to look at a position in worldspace, 
>       rotated around that new view axis so the `Transform` 'up' aligns with the `up` input as closely as possible.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="look_at(entity : Entity, target : Vec)"></endpoint>
<signature id="Transform.look_at+2">Transform.look_at(**entity**: `Entity`, **target**: `Vec`)
<a class="headerlink" href="#Transform.look_at+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Rotate `Transform` to look at a position in worldspace.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_snap(entity : Entity, x : Num, y : Num, z : Num)"></endpoint>
<signature id="Transform.set_snap+4">Transform.set_snap(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Transform.set_snap+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set `Transform` position to snap at specific intervals. (midpoints round away from 0)
> 
> ```js
>   var entity = Entity.create(world)
>   Transform.create(entity)
>   Transform.set_snap(entity, 2, 2, 2)
>   Transform.set_pos(entity, 0.5, 1.5, -3)
>   Log.print(Transform.get_pos(entity)) //[0, 2, -4]
> ```   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_snap(entity : Entity, x : Num, y : Num)"></endpoint>
<signature id="Transform.set_snap+3">Transform.set_snap(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
<a class="headerlink" href="#Transform.set_snap+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set `Transform` position to snap at specific intervals.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_pos(entity : Entity, x : Num, y : Num, z : Num)"></endpoint>
<signature id="Transform.set_pos+4">Transform.set_pos(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Transform.set_pos+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set local position of a `Transform`.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_pos(entity : Entity, x : Num, y : Num)"></endpoint>
<signature id="Transform.set_pos+3">Transform.set_pos(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
<a class="headerlink" href="#Transform.set_pos+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set local position of a `Transform`.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_pos_world(entity : Entity, x : Num, y : Num, z : Num)"></endpoint>
<signature id="Transform.set_pos_world+4">Transform.set_pos_world(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Transform.set_pos_world+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set global position of a `Transform`.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_pos_world(entity : Entity, x : Num, y : Num)"></endpoint>
<signature id="Transform.set_pos_world+3">Transform.set_pos_world(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
<a class="headerlink" href="#Transform.set_pos_world+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set global position of a `Transform`.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_pos_x(entity : Entity, x : Num)"></endpoint>
<signature id="Transform.set_pos_x+2">Transform.set_pos_x(**entity**: `Entity`, **x**: `Num`)
<a class="headerlink" href="#Transform.set_pos_x+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set `x` component of local `Transform` pos.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_pos_y(entity : Entity, y : Num)"></endpoint>
<signature id="Transform.set_pos_y+2">Transform.set_pos_y(**entity**: `Entity`, **y**: `Num`)
<a class="headerlink" href="#Transform.set_pos_y+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set `y` component of local `Transform` pos.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_pos_z(entity : Entity, z : Num)"></endpoint>
<signature id="Transform.set_pos_z+2">Transform.set_pos_z(**entity**: `Entity`, **z**: `Num`)
<a class="headerlink" href="#Transform.set_pos_z+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set `z` component of local `Transform` pos.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_pos_x_world(entity : Entity, x : Num)"></endpoint>
<signature id="Transform.set_pos_x_world+2">Transform.set_pos_x_world(**entity**: `Entity`, **x**: `Num`)
<a class="headerlink" href="#Transform.set_pos_x_world+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set `x` component of global `Transform` pos.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_pos_y_world(entity : Entity, y : Num)"></endpoint>
<signature id="Transform.set_pos_y_world+2">Transform.set_pos_y_world(**entity**: `Entity`, **y**: `Num`)
<a class="headerlink" href="#Transform.set_pos_y_world+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set `y` component of global `Transform` pos.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_pos_z_world(entity : Entity, z : Num)"></endpoint>
<signature id="Transform.set_pos_z_world+2">Transform.set_pos_z_world(**entity**: `Entity`, **z**: `Num`)
<a class="headerlink" href="#Transform.set_pos_z_world+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set `z` component of global `Transform` pos.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_scale(entity : Entity, x : Num, y : Num)"></endpoint>
<signature id="Transform.set_scale+3">Transform.set_scale(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
<a class="headerlink" href="#Transform.set_scale+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set x and y scale of a `Transform`, keeping z scale unchanged.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_scale(entity : Entity, x : Num, y : Num, z : Num)"></endpoint>
<signature id="Transform.set_scale+4">Transform.set_scale(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Transform.set_scale+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set local scale of a `Transform`.
> Setting the scale in a global context isnt available, as link hierarchies with rotations and nonuniform scalings can lead to weird and hard to predict states for that.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_rotation_slerp_angle_axis(entity : Entity, axis : Vec, from : Num, to : Num, t : Num)"></endpoint>
<signature id="Transform.set_rotation_slerp_angle_axis+5">Transform.set_rotation_slerp_angle_axis(**entity**: `Entity`, **axis**: `Vec`, **from**: `Num`, **to**: `Num`, **t**: `Num`)
<a class="headerlink" href="#Transform.set_rotation_slerp_angle_axis+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_rotation_slerp_angle_axis_world(entity : Entity, axis : Vec, from : Num, to : Num, t : Num)"></endpoint>
<signature id="Transform.set_rotation_slerp_angle_axis_world+5">Transform.set_rotation_slerp_angle_axis_world(**entity**: `Entity`, **axis**: `Vec`, **from**: `Num`, **to**: `Num`, **t**: `Num`)
<a class="headerlink" href="#Transform.set_rotation_slerp_angle_axis_world+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_rotation_slerp(entity : Entity, from : Vec, to : Vec, t : Num)"></endpoint>
<signature id="Transform.set_rotation_slerp+4">Transform.set_rotation_slerp(**entity**: `Entity`, **from**: `Vec`, **to**: `Vec`, **t**: `Num`)
<a class="headerlink" href="#Transform.set_rotation_slerp+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_rotation_slerp_world(entity : Entity, from : Vec, to : Vec, t : Num)"></endpoint>
<signature id="Transform.set_rotation_slerp_world+4">Transform.set_rotation_slerp_world(**entity**: `Entity`, **from**: `Vec`, **to**: `Vec`, **t**: `Num`)
<a class="headerlink" href="#Transform.set_rotation_slerp_world+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_rotation(entity : Entity, x : Num, y : Num, z : Num, w : Num)"></endpoint>
<signature id="Transform.set_rotation+5">Transform.set_rotation(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **w**: `Num`)
<a class="headerlink" href="#Transform.set_rotation+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set local rotation in quaternions.
>   
> (Quaternions are how rotations are handled by the engine internally, though it can be hard to understand how to manipulate them, so feel free to stick to euler angles using `set_euler(entity, x, y, z)`.)   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_rotation_world(entity : Entity, x : Num, y : Num, z : Num, w : Num)"></endpoint>
<signature id="Transform.set_rotation_world+5">Transform.set_rotation_world(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **w**: `Num`)
<a class="headerlink" href="#Transform.set_rotation_world+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set global rotation in quaternions.
>   
> (Quaternions are how rotations are handled by the engine internally, though it can be hard to understand how to manipulate them, so feel free to stick to euler angles using `set_euler_world(entity, x, y, z)`.)   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_angle_axis(entity : Entity, degrees : Any, x : Num, y : Num, z : Num)"></endpoint>
<signature id="Transform.set_angle_axis+5">Transform.set_angle_axis(**entity**: `Entity`, **degrees**: `Any`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Transform.set_angle_axis+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set local rotation as a rotation around an axis.
> 
> Rotation direction is left-handed (counter-clockwise when looking in the direction of the axis.)   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_angle_axis_world(entity : Entity, degrees : Any, x : Num, y : Num, z : Num)"></endpoint>
<signature id="Transform.set_angle_axis_world+5">Transform.set_angle_axis_world(**entity**: `Entity`, **degrees**: `Any`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Transform.set_angle_axis_world+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set global rotation as a rotation around an axis.
> 
> Rotation direction is left-handed (counter-clockwise when looking in the direction of the axis.)   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_euler(entity : Entity, x : Num, y : Num, z : Num)"></endpoint>
<signature id="Transform.set_euler+4">Transform.set_euler(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Transform.set_euler+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set local rotation as xyz euler angles.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_euler_world(entity : Entity, x : Num, y : Num, z : Num)"></endpoint>
<signature id="Transform.set_euler_world+4">Transform.set_euler_world(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Transform.set_euler_world+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set global rotation as xyz euler angles.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_euler_x(entity : Entity, x : Num)"></endpoint>
<signature id="Transform.set_euler_x+2">Transform.set_euler_x(**entity**: `Entity`, **x**: `Num`)
<a class="headerlink" href="#Transform.set_euler_x+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_euler_y(entity : Entity, y : Num)"></endpoint>
<signature id="Transform.set_euler_y+2">Transform.set_euler_y(**entity**: `Entity`, **y**: `Num`)
<a class="headerlink" href="#Transform.set_euler_y+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_euler_z(entity : Entity, z : Num)"></endpoint>
<signature id="Transform.set_euler_z+2">Transform.set_euler_z(**entity**: `Entity`, **z**: `Num`)
<a class="headerlink" href="#Transform.set_euler_z+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_euler_x_world(entity : Entity, x : Num)"></endpoint>
<signature id="Transform.set_euler_x_world+2">Transform.set_euler_x_world(**entity**: `Entity`, **x**: `Num`)
<a class="headerlink" href="#Transform.set_euler_x_world+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_euler_y_world(entity : Entity, y : Num)"></endpoint>
<signature id="Transform.set_euler_y_world+2">Transform.set_euler_y_world(**entity**: `Entity`, **y**: `Num`)
<a class="headerlink" href="#Transform.set_euler_y_world+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_euler_z_world(entity : Entity, z : Num)"></endpoint>
<signature id="Transform.set_euler_z_world+2">Transform.set_euler_z_world(**entity**: `Entity`, **z**: `Num`)
<a class="headerlink" href="#Transform.set_euler_z_world+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="rotate_angle_axis_slerp(entity : Entity, axis : Vec, angle_amount : Num)"></endpoint>
<signature id="Transform.rotate_angle_axis_slerp+3">Transform.rotate_angle_axis_slerp(**entity**: `Entity`, **axis**: `Vec`, **angle_amount**: `Num`)
<a class="headerlink" href="#Transform.rotate_angle_axis_slerp+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="rotate_angle_axis_slerp_world(entity : Entity, axis : Vec, angle_amount : Num)"></endpoint>
<signature id="Transform.rotate_angle_axis_slerp_world+3">Transform.rotate_angle_axis_slerp_world(**entity**: `Entity`, **axis**: `Vec`, **angle_amount**: `Num`)
<a class="headerlink" href="#Transform.rotate_angle_axis_slerp_world+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="rotate_around_world(entity : Entity, x : Num, y : Num, z : Num, axis_x : Num, axis_y : Num, axis_z : Num, degrees : Num)"></endpoint>
<signature id="Transform.rotate_around_world+8">Transform.rotate_around_world(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **axis_x**: `Num`, **axis_y**: `Num`, **axis_z**: `Num`, **degrees**: `Num`)
<a class="headerlink" href="#Transform.rotate_around_world+8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Rotate around an axis in world space.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="rotate_around(entity : Entity, x : Num, y : Num, z : Num, axis_x : Num, axis_y : Num, axis_z : Num, degrees : Num)"></endpoint>
<signature id="Transform.rotate_around+8">Transform.rotate_around(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **axis_x**: `Num`, **axis_y**: `Num`, **axis_z**: `Num`, **degrees**: `Num`)
<a class="headerlink" href="#Transform.rotate_around+8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Rotate around an axis in local space.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="rotate_angle_axis(entity : Entity, degrees : Any, x : Num, y : Num, z : Num)"></endpoint>
<signature id="Transform.rotate_angle_axis+5">Transform.rotate_angle_axis(**entity**: `Entity`, **degrees**: `Any`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Transform.rotate_angle_axis+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Rotate on the spot around an axis in local coordinates.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="rotate_angle_axis_world(entity : Entity, degrees : Any, x : Num, y : Num, z : Num)"></endpoint>
<signature id="Transform.rotate_angle_axis_world+5">Transform.rotate_angle_axis_world(**entity**: `Entity`, **degrees**: `Any`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Transform.rotate_angle_axis_world+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Rotate on the spot around an axis in global coordinates.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="rotate_euler(entity : Entity, x : Num, y : Num, z : Num)"></endpoint>
<signature id="Transform.rotate_euler+4">Transform.rotate_euler(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Transform.rotate_euler+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Rotate by euler angles in local space.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="rotate_euler_world(entity : Entity, x : Num, y : Num, z : Num)"></endpoint>
<signature id="Transform.rotate_euler_world+4">Transform.rotate_euler_world(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Transform.rotate_euler_world+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Rotate by euler angles in global space.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="translate(entity : Entity, x : Num, y : Num, z : Num)"></endpoint>
<signature id="Transform.translate+4">Transform.translate(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Transform.translate+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Move `Transform` in local space.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="translate(entity : Entity, x : Num, y : Num)"></endpoint>
<signature id="Transform.translate+3">Transform.translate(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
<a class="headerlink" href="#Transform.translate+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Move `Transform` in local space.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_pos(entity : Entity)"></endpoint>
<signature id="Transform.get_pos">Transform.get_pos(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_pos" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Get position local space (relative to link `Transform`).   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_pos_x(entity : Entity)"></endpoint>
<signature id="Transform.get_pos_x">Transform.get_pos_x(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_pos_x" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_pos_y(entity : Entity)"></endpoint>
<signature id="Transform.get_pos_y">Transform.get_pos_y(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_pos_y" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_pos_z(entity : Entity)"></endpoint>
<signature id="Transform.get_pos_z">Transform.get_pos_z(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_pos_z" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_pos_world(entity : Entity)"></endpoint>
<signature id="Transform.get_pos_world">Transform.get_pos_world(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_pos_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Get position global space.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_pos_world_unsnapped(entity : Entity)"></endpoint>
<signature id="Transform.get_pos_world_unsnapped">Transform.get_pos_world_unsnapped(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_pos_world_unsnapped" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Get position global space independently of `set_snap` settings.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_pos_x_world(entity : Entity)"></endpoint>
<signature id="Transform.get_pos_x_world">Transform.get_pos_x_world(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_pos_x_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_pos_y_world(entity : Entity)"></endpoint>
<signature id="Transform.get_pos_y_world">Transform.get_pos_y_world(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_pos_y_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_pos_z_world(entity : Entity)"></endpoint>
<signature id="Transform.get_pos_z_world">Transform.get_pos_z_world(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_pos_z_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="rotate2D(entity : Entity, degrees : Num)"></endpoint>
<signature id="Transform.rotate2D+2">Transform.rotate2D(**entity**: `Entity`, **degrees**: `Num`)
<a class="headerlink" href="#Transform.rotate2D+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Rotate the `Transform` in local space.
>     
> This technically rotates around the z axis, since thats the only axis we care about in 2d contexts.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_angle2D(entity : Entity, degrees : Num)"></endpoint>
<signature id="Transform.set_angle2D+2">Transform.set_angle2D(**entity**: `Entity`, **degrees**: `Num`)
<a class="headerlink" href="#Transform.set_angle2D+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the 2d angle in local space.
>     
> This is technically the same as `set_euler_z`(doesnt touch x or y), since thats the only axis we care about in 2d contexts.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_angle2D_world(entity : Entity, degrees : Num)"></endpoint>
<signature id="Transform.set_angle2D_world+2">Transform.set_angle2D_world(**entity**: `Entity`, **degrees**: `Num`)
<a class="headerlink" href="#Transform.set_angle2D_world+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the 2d angle in global space.
>     
> This is technically the same as `set_euler_z`(doesnt touch x or y), since thats the only axis we care about in 2d contexts.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_angle2D(entity : Entity)"></endpoint>
<signature id="Transform.get_angle2D">Transform.get_angle2D(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_angle2D" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get the 2d angle in local space.
>     
> This is technically the same as `get_euler_z`, since thats the only axis we care about in 2d contexts.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_angle2D_world(entity : Entity)"></endpoint>
<signature id="Transform.get_angle2D_world">Transform.get_angle2D_world(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_angle2D_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get the 2d angle in global space.
>     
> This is technically the same as `get_euler_z_world`, since thats the only axis we care about in 2d contexts.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_depth2D(entity : Entity, depth : Num)"></endpoint>
<signature id="Transform.set_depth2D+2">Transform.set_depth2D(**entity**: `Entity`, **depth**: `Num`)
<a class="headerlink" href="#Transform.set_depth2D+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the local depth (relative to link `Transform`).
>     
> This is technically the same as `set_pos_z`.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_depth2D(entity : Entity)"></endpoint>
<signature id="Transform.get_depth2D">Transform.get_depth2D(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_depth2D" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get the local depth (relative to link `Transform`).
>     
> This is technically the same as `get_pos_z`.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="set_depth2D_world(entity : Entity, depth : Num)"></endpoint>
<signature id="Transform.set_depth2D_world+2">Transform.set_depth2D_world(**entity**: `Entity`, **depth**: `Num`)
<a class="headerlink" href="#Transform.set_depth2D_world+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the global depth.
>     
> This is technically the same as `set_pos_z_world`.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_depth2D_world(entity : Entity)"></endpoint>
<signature id="Transform.get_depth2D_world">Transform.get_depth2D_world(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_depth2D_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get the global depth.
>     
> This is technically the same as `get_pos_z_world`.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_world_matrix(entity : Entity, into_matrix : Floats)"></endpoint>
<signature id="Transform.get_world_matrix+2">Transform.get_world_matrix(**entity**: `Entity`, **into_matrix**: `Floats`)
<a class="headerlink" href="#Transform.get_world_matrix+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Get 4x4 world transform matrix (column major array).
> 
> ```js
>   var ent = Entity.create(app.world)
>   Transform.create(ent)
>   Transform.set_pos(ent, 2, 3, 4)
>   var matrix = Floats.new(16)
>   Transform.get_world_matrix(ent, matrix)
>   //matrix is now [1,0,0,0, 0,1,0,0, 0,0,1,0, 2,3,4,1]
> ```   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_rotation(entity : Entity)"></endpoint>
<signature id="Transform.get_rotation">Transform.get_rotation(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_rotation" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Quat`
> Get local quaternion rotation.
>     
> (Note that quaternions can be unfamiliar and hard to manipulate, so if you're not familiar with them you might want to use `get_euler` instead)   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_rotation_world(entity : Entity)"></endpoint>
<signature id="Transform.get_rotation_world">Transform.get_rotation_world(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_rotation_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Quat`
> Get global quaternion rotation.
>     
> (Note that quaternions can be unfamiliar and hard to manipulate, so if you're not familiar with them you might want to use `get_euler_world` instead)   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_rotation_matrix(entity : Entity, into_matrix : Floats)"></endpoint>
<signature id="Transform.get_rotation_matrix+2">Transform.get_rotation_matrix(**entity**: `Entity`, **into_matrix**: `Floats`)
<a class="headerlink" href="#Transform.get_rotation_matrix+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Get 4x4 world rotation matrix (column major array).   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_euler(entity : Entity)"></endpoint>
<signature id="Transform.get_euler">Transform.get_euler(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_euler" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Get local euler angles.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_euler_x(entity : Entity)"></endpoint>
<signature id="Transform.get_euler_x">Transform.get_euler_x(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_euler_x" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_euler_y(entity : Entity)"></endpoint>
<signature id="Transform.get_euler_y">Transform.get_euler_y(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_euler_y" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_euler_z(entity : Entity)"></endpoint>
<signature id="Transform.get_euler_z">Transform.get_euler_z(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_euler_z" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_euler_world(entity : Entity)"></endpoint>
<signature id="Transform.get_euler_world">Transform.get_euler_world(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_euler_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Get global euler angles.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_euler_x_world(entity : Entity)"></endpoint>
<signature id="Transform.get_euler_x_world">Transform.get_euler_x_world(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_euler_x_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_euler_y_world(entity : Entity)"></endpoint>
<signature id="Transform.get_euler_y_world">Transform.get_euler_y_world(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_euler_y_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_euler_z_world(entity : Entity)"></endpoint>
<signature id="Transform.get_euler_z_world">Transform.get_euler_z_world(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_euler_z_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_scale(entity : Entity)"></endpoint>
<signature id="Transform.get_scale">Transform.get_scale(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_scale" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Get local scale.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_scale_x(entity : Entity)"></endpoint>
<signature id="Transform.get_scale_x">Transform.get_scale_x(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_scale_x" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_scale_y(entity : Entity)"></endpoint>
<signature id="Transform.get_scale_y">Transform.get_scale_y(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_scale_y" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_scale_z(entity : Entity)"></endpoint>
<signature id="Transform.get_scale_z">Transform.get_scale_z(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_scale_z" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_scale_world(entity : Entity)"></endpoint>
<signature id="Transform.get_scale_world">Transform.get_scale_world(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_scale_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Get global scale.
> Note that through rotations and non-uniform scale in the transform link hierarchy, getting an accurate world scale might be impossible, making this lossy.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_scale_x_world(entity : Entity)"></endpoint>
<signature id="Transform.get_scale_x_world">Transform.get_scale_x_world(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_scale_x_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_scale_y_world(entity : Entity)"></endpoint>
<signature id="Transform.get_scale_y_world">Transform.get_scale_y_world(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_scale_y_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_scale_z_world(entity : Entity)"></endpoint>
<signature id="Transform.get_scale_z_world">Transform.get_scale_z_world(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_scale_z_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_right(entity : Entity)"></endpoint>
<signature id="Transform.get_right">Transform.get_right(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_right" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Get the "right" direction of the `Transform`.
> Same direction as the red arrow in the translation gizmo in the editor.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_forward(entity : Entity)"></endpoint>
<signature id="Transform.get_forward">Transform.get_forward(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_forward" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Get the "forward" direction of the `Transform`.
> Same direction as the green arrow in the translation gizmo in the editor.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="get_up(entity : Entity)"></endpoint>
<signature id="Transform.get_up">Transform.get_up(**entity**: `Entity`)
<a class="headerlink" href="#Transform.get_up" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Get the "up" direction of the `Transform`.
> Same direction as the blue arrow in the translation gizmo in the editor.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="sync(entity : Entity)"></endpoint>
<signature id="Transform.sync">Transform.sync(**entity**: `Entity`)
<a class="headerlink" href="#Transform.sync" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Forces a sync of the `Transform`. Will trigger listen functions.
> This usually shouldn't be needed as `Transform` sync automatically when updated.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="sync_block(entity : Entity, mask : TransformApplyMask)"></endpoint>
<signature id="Transform.sync_block+2">Transform.sync_block(**entity**: `Entity`, **mask**: `TransformApplyMask`)
<a class="headerlink" href="#Transform.sync_block+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Forces a sync of the `Transform` block data. Will trigger block listener functions.
> This usually shouldn't be needed as `Transform` sync automatically when updated.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="sync_world(world : World)"></endpoint>
<signature id="Transform.sync_world">Transform.sync_world(**world**: `World`)
<a class="headerlink" href="#Transform.sync_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Forces a sync of all `Transform` in a world. Will trigger listen functions.
> This usually shouldn't be needed as `Transform` sync automatically when updated.   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="transform_by(entity : Entity, other : Entity)"></endpoint>
<signature id="Transform.transform_by+2">Transform.transform_by(**entity**: `Entity`, **other**: `Entity`)
<a class="headerlink" href="#Transform.transform_by+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Transform the given entity by another entities transform. e.g set world using the other as a parent   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="scale_by(entity : Entity, scale : Float3, origin : Float3)"></endpoint>
<signature id="Transform.scale_by+3">Transform.scale_by(**entity**: `Entity`, **scale**: `Float3`, **origin**: `Float3`)
<a class="headerlink" href="#Transform.scale_by+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Transform the given entity scale by the value around the given origin   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="rotate_euler_by(entity : Entity, euler : Float3, origin : Float3)"></endpoint>
<signature id="Transform.rotate_euler_by+3">Transform.rotate_euler_by(**entity**: `Entity`, **euler**: `Float3`, **origin**: `Float3`)
<a class="headerlink" href="#Transform.rotate_euler_by+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Transform the given entity rotation around the origin, by euler amount (radians)   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="local_vector_to_world(entity : Entity, x : Num, y : Num, z : Num)"></endpoint>
<signature id="Transform.local_vector_to_world+4">Transform.local_vector_to_world(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Transform.local_vector_to_world+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Convert a vector from local space to world space. (applies scale and rotation, but not translation)   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="world_vector_to_local(entity : Entity, x : Num, y : Num, z : Num)"></endpoint>
<signature id="Transform.world_vector_to_local+4">Transform.world_vector_to_local(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Transform.world_vector_to_local+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Convert a vector from world space to local space. (applies scale and rotation, but not translation)   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="local_dir_to_world(entity : Entity, x : Num, y : Num, z : Num)"></endpoint>
<signature id="Transform.local_dir_to_world+4">Transform.local_dir_to_world(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Transform.local_dir_to_world+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Convert a direction from local space to world space. (applies only rotation, not rotation or translation)   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="world_dir_to_local(entity : Entity, x : Num, y : Num, z : Num)"></endpoint>
<signature id="Transform.world_dir_to_local+4">Transform.world_dir_to_local(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Transform.world_dir_to_local+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Convert a direction from world space to local space. (applies only rotation, not rotation or translation)   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="local_point_to_world(entity : Entity, x : Num, y : Num, z : Num)"></endpoint>
<signature id="Transform.local_point_to_world+4">Transform.local_point_to_world(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Transform.local_point_to_world+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Convert a point from local space to world space. (applies translation, rotation and scale)   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="local_point_to_world(entity : Entity, x : Num, y : Num, z : Num, scaled : Bool)"></endpoint>
<signature id="Transform.local_point_to_world+5">Transform.local_point_to_world(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **scaled**: `Bool`)
<a class="headerlink" href="#Transform.local_point_to_world+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Convert a point from local space to world space. (applies translation, rotation and optionally, scale)   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="world_point_to_local(entity : Entity, x : Num, y : Num, z : Num)"></endpoint>
<signature id="Transform.world_point_to_local+4">Transform.world_point_to_local(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Transform.world_point_to_local+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Convert a point from world space to local space. (applies translation, rotation and scale)   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="world_point_to_local(entity : Entity, x : Num, y : Num, z : Num, scaled : Bool)"></endpoint>
<signature id="Transform.world_point_to_local+5">Transform.world_point_to_local(**entity**: `Entity`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **scaled**: `Bool`)
<a class="headerlink" href="#Transform.world_point_to_local+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Convert a point from world space to local space. (applies translation, rotation and optionally, scale)   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="listen_all(world : World, fn : Fn)"></endpoint>
<signature id="Transform.listen_all+2">Transform.listen_all(**world**: `World`, **fn**: `Fn`)
<a class="headerlink" href="#Transform.listen_all+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Handle`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="unlisten_all(world : World, handle : Handle)"></endpoint>
<signature id="Transform.unlisten_all+2">Transform.unlisten_all(**world**: `World`, **handle**: `Handle`)
<a class="headerlink" href="#Transform.unlisten_all+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="listen(entity : Entity, fn : Fn)"></endpoint>
<signature id="Transform.listen+2">Transform.listen(**entity**: `Entity`, **fn**: `Fn`)
<a class="headerlink" href="#Transform.listen+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Handle`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="Transform" signature="unlisten(entity : Entity, handle : Handle)"></endpoint>
<signature id="Transform.unlisten+2">Transform.unlisten(**entity**: `Entity`, **handle**: `Handle`)
<a class="headerlink" href="#Transform.unlisten+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

### TransformApplyMask
`:::js import "luxe: system/transform.modifier" for TransformApplyMask`
> no docs found

- [pos](#TransformApplyMask.pos)
- [scale](#TransformApplyMask.scale)
- [rotation](#TransformApplyMask.rotation)
- [modified](#TransformApplyMask.modified)
- [all_modified](#TransformApplyMask.all_modified)

<hr/>
<endpoint module="luxe: system/transform.modifier" class="TransformApplyMask" signature="pos"></endpoint>
<signature id="TransformApplyMask.pos">TransformApplyMask.pos
<a class="headerlink" href="#TransformApplyMask.pos" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="TransformApplyMask" signature="scale"></endpoint>
<signature id="TransformApplyMask.scale">TransformApplyMask.scale
<a class="headerlink" href="#TransformApplyMask.scale" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="TransformApplyMask" signature="rotation"></endpoint>
<signature id="TransformApplyMask.rotation">TransformApplyMask.rotation
<a class="headerlink" href="#TransformApplyMask.rotation" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="TransformApplyMask" signature="modified"></endpoint>
<signature id="TransformApplyMask.modified">TransformApplyMask.modified
<a class="headerlink" href="#TransformApplyMask.modified" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/transform.modifier" class="TransformApplyMask" signature="all_modified"></endpoint>
<signature id="TransformApplyMask.all_modified">TransformApplyMask.all_modified
<a class="headerlink" href="#TransformApplyMask.all_modified" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

