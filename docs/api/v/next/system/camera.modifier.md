#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.11.1`)  


---

## `luxe: system/camera.modifier` module

- [Camera](#camera)   
- [CameraProjection](#cameraprojection)   
- [CameraViewType](#cameraviewtype)   
- [Data](#data)   
- [System](#system)   

---

### Camera
`:::js import "luxe: system/camera.modifier" for Camera`
> no docs found

- [create](#Camera.create)(**entity**: `Any`)
- [destroy](#Camera.destroy)(**entity**: `Any`)
- [has](#Camera.has)(**entity**: `Any`)
- [get_default](#Camera.get_default)(**world**: `Any`)
- [set_default](#Camera.set_default+2)(**world**: `Any`, **camera**: `Any`)
- [set_fov_vertical](#Camera.set_fov_vertical+2)(**entity**: `Any`, **fov_vertical**: `Any`)
- [get_fov_vertical](#Camera.get_fov_vertical)(**entity**: `Any`)
- [get_projection](#Camera.get_projection)(**entity**: `Any`)
- [set_zoom2D](#Camera.set_zoom2D+2)(**entity**: `Entity`, **zoom**: `Num`)
- [get_zoom2D](#Camera.get_zoom2D)(**entity**: `Any`)
- [get_near](#Camera.get_near)(**entity**: `Any`)
- [get_far](#Camera.get_far)(**entity**: `Any`)
- [get_aspect](#Camera.get_aspect)(**entity**: `Any`)
- [get_frustum](#Camera.get_frustum)(**entity**: `Any`)
- [perspective](#Camera.perspective+5)(**entity**: `Any`, **fov_vertical**: `Any`, **aspect**: `Any`, **near**: `Any`, **far**: `Any`)
- [ortho](#Camera.ortho+7)(**entity**: `Any`, **left**: `Any`, **top**: `Any`, **right**: `Any`, **bottom**: `Any`, **near**: `Any`, **far**: `Any`)
- [look_at](#Camera.look_at+4)(**entity**: `Any`, **from**: `Any`, **to**: `Any`, **up**: `Any`)
- [set2D](#Camera.set2D+7)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **width**: `Any`, **height**: `Any`, **near**: `Any`, **far**: `Any`)
- [set3D](#Camera.set3D+5)(**entity**: `Any`, **fov_vertical**: `Any`, **aspect**: `Any`, **near**: `Any`, **far**: `Any`)
- [screen_point_to_world](#Camera.screen_point_to_world+3)(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`)
- [world_point_to_screen](#Camera.world_point_to_screen+4)(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`)
- [world_point_to_view](#Camera.world_point_to_view+5)(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`, **into**: `Any`)
- [world_point_to_view](#Camera.world_point_to_view+4)(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`)
- [view_point_to_world](#Camera.view_point_to_world+4)(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`)
- [world_point_to_clip](#Camera.world_point_to_clip+4)(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`)
- [clip_point_to_world](#Camera.clip_point_to_world+4)(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`)
- [get_view_matrix](#Camera.get_view_matrix+2)(**entity**: `Any`, **into_matrix**: `Any`)
- [get_projection_matrix](#Camera.get_projection_matrix+2)(**entity**: `Any`, **into_matrix**: `Any`)
- [get_view_projection_matrix](#Camera.get_view_projection_matrix+2)(**entity**: `Any`, **into_matrix**: `Any`)
- [set_view_matrix](#Camera.set_view_matrix+2)(**entity**: `Any`, **matrix**: `Any`)
- [set_projection_matrix](#Camera.set_projection_matrix+2)(**entity**: `Any`, **matrix**: `Any`)
- [cull](#Camera.cull+2)(**camera**: `Any`, **render_set**: `Any`)
- [froxelize](#Camera.froxelize+5)(**camera**: `Any`, **slices**: `Any`, **entity_info_list**: `Any`, **cluster_image**: `Any`, **items_image**: `Any`)

<hr/>
<endpoint module="luxe: system/camera.modifier" class="Camera" signature="create(entity : Any)"></endpoint>
<signature id="Camera.create">Camera.create(**entity**: `Any`)
<a class="headerlink" href="#Camera.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="destroy(entity : Any)"></endpoint>
<signature id="Camera.destroy">Camera.destroy(**entity**: `Any`)
<a class="headerlink" href="#Camera.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="has(entity : Any)"></endpoint>
<signature id="Camera.has">Camera.has(**entity**: `Any`)
<a class="headerlink" href="#Camera.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="get_default(world : Any)"></endpoint>
<signature id="Camera.get_default">Camera.get_default(**world**: `Any`)
<a class="headerlink" href="#Camera.get_default" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="set_default(world : Any, camera : Any)"></endpoint>
<signature id="Camera.set_default+2">Camera.set_default(**world**: `Any`, **camera**: `Any`)
<a class="headerlink" href="#Camera.set_default+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="set_fov_vertical(entity : Any, fov_vertical : Any)"></endpoint>
<signature id="Camera.set_fov_vertical+2">Camera.set_fov_vertical(**entity**: `Any`, **fov_vertical**: `Any`)
<a class="headerlink" href="#Camera.set_fov_vertical+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="get_fov_vertical(entity : Any)"></endpoint>
<signature id="Camera.get_fov_vertical">Camera.get_fov_vertical(**entity**: `Any`)
<a class="headerlink" href="#Camera.get_fov_vertical" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="get_projection(entity : Any)"></endpoint>
<signature id="Camera.get_projection">Camera.get_projection(**entity**: `Any`)
<a class="headerlink" href="#Camera.get_projection" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js CameraProjection`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="set_zoom2D(entity : Entity, zoom : Num)"></endpoint>
<signature id="Camera.set_zoom2D+2">Camera.set_zoom2D(**entity**: `Entity`, **zoom**: `Num`)
<a class="headerlink" href="#Camera.set_zoom2D+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="get_zoom2D(entity : Any)"></endpoint>
<signature id="Camera.get_zoom2D">Camera.get_zoom2D(**entity**: `Any`)
<a class="headerlink" href="#Camera.get_zoom2D" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="get_near(entity : Any)"></endpoint>
<signature id="Camera.get_near">Camera.get_near(**entity**: `Any`)
<a class="headerlink" href="#Camera.get_near" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="get_far(entity : Any)"></endpoint>
<signature id="Camera.get_far">Camera.get_far(**entity**: `Any`)
<a class="headerlink" href="#Camera.get_far" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="get_aspect(entity : Any)"></endpoint>
<signature id="Camera.get_aspect">Camera.get_aspect(**entity**: `Any`)
<a class="headerlink" href="#Camera.get_aspect" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="get_frustum(entity : Any)"></endpoint>
<signature id="Camera.get_frustum">Camera.get_frustum(**entity**: `Any`)
<a class="headerlink" href="#Camera.get_frustum" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="perspective(entity : Any, fov_vertical : Any, aspect : Any, near : Any, far : Any)"></endpoint>
<signature id="Camera.perspective+5">Camera.perspective(**entity**: `Any`, **fov_vertical**: `Any`, **aspect**: `Any`, **near**: `Any`, **far**: `Any`)
<a class="headerlink" href="#Camera.perspective+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="ortho(entity : Any, left : Any, top : Any, right : Any, bottom : Any, near : Any, far : Any)"></endpoint>
<signature id="Camera.ortho+7">Camera.ortho(**entity**: `Any`, **left**: `Any`, **top**: `Any`, **right**: `Any`, **bottom**: `Any`, **near**: `Any`, **far**: `Any`)
<a class="headerlink" href="#Camera.ortho+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="look_at(entity : Any, from : Any, to : Any, up : Any)"></endpoint>
<signature id="Camera.look_at+4">Camera.look_at(**entity**: `Any`, **from**: `Any`, **to**: `Any`, **up**: `Any`)
<a class="headerlink" href="#Camera.look_at+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="set2D(entity : Any, x : Any, y : Any, width : Any, height : Any, near : Any, far : Any)"></endpoint>
<signature id="Camera.set2D+7">Camera.set2D(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **width**: `Any`, **height**: `Any`, **near**: `Any`, **far**: `Any`)
<a class="headerlink" href="#Camera.set2D+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="set3D(entity : Any, fov_vertical : Any, aspect : Any, near : Any, far : Any)"></endpoint>
<signature id="Camera.set3D+5">Camera.set3D(**entity**: `Any`, **fov_vertical**: `Any`, **aspect**: `Any`, **near**: `Any`, **far**: `Any`)
<a class="headerlink" href="#Camera.set3D+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="screen_point_to_world(entity : Any, pos_x : Any, pos_y : Any)"></endpoint>
<signature id="Camera.screen_point_to_world+3">Camera.screen_point_to_world(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`)
<a class="headerlink" href="#Camera.screen_point_to_world+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="world_point_to_screen(entity : Any, pos_x : Any, pos_y : Any, pos_z : Any)"></endpoint>
<signature id="Camera.world_point_to_screen+4">Camera.world_point_to_screen(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`)
<a class="headerlink" href="#Camera.world_point_to_screen+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="world_point_to_view(entity : Any, pos_x : Any, pos_y : Any, pos_z : Any, into : Any)"></endpoint>
<signature id="Camera.world_point_to_view+5">Camera.world_point_to_view(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`, **into**: `Any`)
<a class="headerlink" href="#Camera.world_point_to_view+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="world_point_to_view(entity : Any, pos_x : Any, pos_y : Any, pos_z : Any)"></endpoint>
<signature id="Camera.world_point_to_view+4">Camera.world_point_to_view(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`)
<a class="headerlink" href="#Camera.world_point_to_view+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="view_point_to_world(entity : Any, pos_x : Any, pos_y : Any, pos_z : Any)"></endpoint>
<signature id="Camera.view_point_to_world+4">Camera.view_point_to_world(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`)
<a class="headerlink" href="#Camera.view_point_to_world+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="world_point_to_clip(entity : Any, pos_x : Any, pos_y : Any, pos_z : Any)"></endpoint>
<signature id="Camera.world_point_to_clip+4">Camera.world_point_to_clip(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`)
<a class="headerlink" href="#Camera.world_point_to_clip+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="clip_point_to_world(entity : Any, pos_x : Any, pos_y : Any, pos_z : Any)"></endpoint>
<signature id="Camera.clip_point_to_world+4">Camera.clip_point_to_world(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`)
<a class="headerlink" href="#Camera.clip_point_to_world+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="get_view_matrix(entity : Any, into_matrix : Any)"></endpoint>
<signature id="Camera.get_view_matrix+2">Camera.get_view_matrix(**entity**: `Any`, **into_matrix**: `Any`)
<a class="headerlink" href="#Camera.get_view_matrix+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="get_projection_matrix(entity : Any, into_matrix : Any)"></endpoint>
<signature id="Camera.get_projection_matrix+2">Camera.get_projection_matrix(**entity**: `Any`, **into_matrix**: `Any`)
<a class="headerlink" href="#Camera.get_projection_matrix+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="get_view_projection_matrix(entity : Any, into_matrix : Any)"></endpoint>
<signature id="Camera.get_view_projection_matrix+2">Camera.get_view_projection_matrix(**entity**: `Any`, **into_matrix**: `Any`)
<a class="headerlink" href="#Camera.get_view_projection_matrix+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="set_view_matrix(entity : Any, matrix : Any)"></endpoint>
<signature id="Camera.set_view_matrix+2">Camera.set_view_matrix(**entity**: `Any`, **matrix**: `Any`)
<a class="headerlink" href="#Camera.set_view_matrix+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="set_projection_matrix(entity : Any, matrix : Any)"></endpoint>
<signature id="Camera.set_projection_matrix+2">Camera.set_projection_matrix(**entity**: `Any`, **matrix**: `Any`)
<a class="headerlink" href="#Camera.set_projection_matrix+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="cull(camera : Any, render_set : Any)"></endpoint>
<signature id="Camera.cull+2">Camera.cull(**camera**: `Any`, **render_set**: `Any`)
<a class="headerlink" href="#Camera.cull+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="Camera" signature="froxelize(camera : Any, slices : Any, entity_info_list : Any, cluster_image : Any, items_image : Any)"></endpoint>
<signature id="Camera.froxelize+5">Camera.froxelize(**camera**: `Any`, **slices**: `Any`, **entity_info_list**: `Any`, **cluster_image**: `Any`, **items_image**: `Any`)
<a class="headerlink" href="#Camera.froxelize+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### CameraProjection
`:::js import "luxe: system/camera.modifier" for CameraProjection`
> no docs found

- [ortho](#CameraProjection.ortho)
- [perspective](#CameraProjection.perspective)
- [custom](#CameraProjection.custom)

<hr/>
<endpoint module="luxe: system/camera.modifier" class="CameraProjection" signature="ortho"></endpoint>
<signature id="CameraProjection.ortho">CameraProjection.ortho
<a class="headerlink" href="#CameraProjection.ortho" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="CameraProjection" signature="perspective"></endpoint>
<signature id="CameraProjection.perspective">CameraProjection.perspective
<a class="headerlink" href="#CameraProjection.perspective" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="CameraProjection" signature="custom"></endpoint>
<signature id="CameraProjection.custom">CameraProjection.custom
<a class="headerlink" href="#CameraProjection.custom" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### CameraViewType
`:::js import "luxe: system/camera.modifier" for CameraViewType`
> no docs found

- [view_2D](#CameraViewType.view_2D)
- [view_3D](#CameraViewType.view_3D)
- [custom](#CameraViewType.custom)

<hr/>
<endpoint module="luxe: system/camera.modifier" class="CameraViewType" signature="view_2D"></endpoint>
<signature id="CameraViewType.view_2D">CameraViewType.view_2D
<a class="headerlink" href="#CameraViewType.view_2D" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="CameraViewType" signature="view_3D"></endpoint>
<signature id="CameraViewType.view_3D">CameraViewType.view_3D
<a class="headerlink" href="#CameraViewType.view_3D" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/camera.modifier" class="CameraViewType" signature="custom"></endpoint>
<signature id="CameraViewType.custom">CameraViewType.custom
<a class="headerlink" href="#CameraViewType.custom" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Data
`:::js import "luxe: system/camera.modifier" for Data`
> no docs found


<hr/>
### System
`:::js import "luxe: system/camera.modifier" for System`
> no docs found

- [new](#System.new)(**world**: `World`)

<hr/>
<endpoint module="luxe: system/camera.modifier" class="System" signature="new(world : World)"></endpoint>
<signature id="System.new">System.new(**world**: `World`)
<a class="headerlink" href="#System.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js System`
> no docs found   

