#![](../../images/luxe-dark.svg){width="96em"}

# `arcade` API (`0.0.15`)  


---

## `arcade: modifier/arcade` module

- [Arcade](#arcade)   
- [CollisionEvent](#collisionevent)   
- [ContactCache](#contactcache)   
- [ContactState](#contactstate)   
- [Shape2DDraw](#shape2ddraw)   
- [ShapeType](#shapetype)   
- [SimpleSpatialHash](#simplespatialhash)   

---

### Arcade
`:::js import "arcade: modifier/arcade" for Arcade`
> no docs found

- [create](#Arcade.create)(**entity**: `Any`)
- [destroy](#Arcade.destroy)(**entity**: `Any`)
- [has](#Arcade.has)(**entity**: `Any`)
- [get_vel](#Arcade.get_vel)(**entity**: `Any`)
- [set_vel](#Arcade.set_vel+2)(**entity**: `Any`, **vel**: `Any`)
- [get_vel_min](#Arcade.get_vel_min)(**entity**: `Any`)
- [set_vel_min](#Arcade.set_vel_min+2)(**entity**: `Any`, **min**: `Any`)
- [get_acc](#Arcade.get_acc)(**entity**: `Any`)
- [set_acc](#Arcade.set_acc+2)(**entity**: `Any`, **acc**: `Any`)
- [get_max_speed](#Arcade.get_max_speed)(**entity**: `Any`)
- [set_max_speed](#Arcade.set_max_speed+2)(**entity**: `Any`, **max_speed**: `Any`)
- [get_solid](#Arcade.get_solid)(**entity**: `Any`)
- [set_solid](#Arcade.set_solid+2)(**entity**: `Any`, **solid**: `Any`)
- [get_dynamic](#Arcade.get_dynamic)(**entity**: `Any`)
- [set_dynamic](#Arcade.set_dynamic+2)(**entity**: `Any`, **dynamic**: `Any`)
- [get_restitution](#Arcade.get_restitution)(**entity**: `Any`)
- [set_restitution](#Arcade.set_restitution+2)(**entity**: `Any`, **restitution**: `Any`)
- [get_drag](#Arcade.get_drag)(**entity**: `Any`)
- [set_drag](#Arcade.set_drag+2)(**entity**: `Any`, **drag**: `Any`)
- [set_drag_x](#Arcade.set_drag_x+2)(**entity**: `Any`, **drag_x**: `Any`)
- [set_drag_y](#Arcade.set_drag_y+2)(**entity**: `Any`, **drag_y**: `Any`)
- [add_collision_callback](#Arcade.add_collision_callback+2)(**entity**: `Any`, **fn**: `Any`)
- [remove_collision_callback](#Arcade.remove_collision_callback+2)(**entity**: `Any`, **fn**: `Any`)
- [get_frame_collision_normals](#Arcade.get_frame_collision_normals)(**entity**: `Any`)
- [collided_with_normal_angle](#Arcade.collided_with_normal_angle+3)(**entity**: `Any`, **angle_center**: `Any`, **angle_spread**: `Any`)
- [set_shape_type](#Arcade.set_shape_type+2)(**entity**: `Any`, **shape_type**: `Any`)
- [get_shape_type](#Arcade.get_shape_type)(**entity**: `Any`)
- [get_width](#Arcade.get_width)(**entity**: `Any`)
- [get_height](#Arcade.get_height)(**entity**: `Any`)
- [set_width](#Arcade.set_width+2)(**entity**: `Any`, **width**: `Any`)
- [set_height](#Arcade.set_height+2)(**entity**: `Any`, **height**: `Any`)
- [set_centered](#Arcade.set_centered+2)(**entity**: `Any`, **centered**: `Any`)
- [set_radius](#Arcade.set_radius+2)(**entity**: `Any`, **radius**: `Any`)
- [set_broadphase_cell_size](#Arcade.set_broadphase_cell_size+2)(**world**: `Any`, **size**: `Any`)
- [set_debug_draw_enabled](#Arcade.set_debug_draw_enabled+2)(**world**: `Any`, **enabled**: `Any`)
- [get_debug_draw_enabled](#Arcade.get_debug_draw_enabled)(**world**: `Any`)
- [toggle_debug_draw_enabled](#Arcade.toggle_debug_draw_enabled)(**world**: `Any`)
- [set_ignored](#Arcade.set_ignored+3)(**entity**: `Any`, **other**: `Any`, **state**: `Any`)
- [refresh](#Arcade.refresh)(**entity**: `Any`)

<hr/>
<endpoint module="arcade: modifier/arcade" class="Arcade" signature="create(entity : Any)"></endpoint>
<signature id="Arcade.create">Arcade.create(**entity**: `Any`)
<a class="headerlink" href="#Arcade.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="destroy(entity : Any)"></endpoint>
<signature id="Arcade.destroy">Arcade.destroy(**entity**: `Any`)
<a class="headerlink" href="#Arcade.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="has(entity : Any)"></endpoint>
<signature id="Arcade.has">Arcade.has(**entity**: `Any`)
<a class="headerlink" href="#Arcade.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="get_vel(entity : Any)"></endpoint>
<signature id="Arcade.get_vel">Arcade.get_vel(**entity**: `Any`)
<a class="headerlink" href="#Arcade.get_vel" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="set_vel(entity : Any, vel : Any)"></endpoint>
<signature id="Arcade.set_vel+2">Arcade.set_vel(**entity**: `Any`, **vel**: `Any`)
<a class="headerlink" href="#Arcade.set_vel+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="get_vel_min(entity : Any)"></endpoint>
<signature id="Arcade.get_vel_min">Arcade.get_vel_min(**entity**: `Any`)
<a class="headerlink" href="#Arcade.get_vel_min" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="set_vel_min(entity : Any, min : Any)"></endpoint>
<signature id="Arcade.set_vel_min+2">Arcade.set_vel_min(**entity**: `Any`, **min**: `Any`)
<a class="headerlink" href="#Arcade.set_vel_min+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="get_acc(entity : Any)"></endpoint>
<signature id="Arcade.get_acc">Arcade.get_acc(**entity**: `Any`)
<a class="headerlink" href="#Arcade.get_acc" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="set_acc(entity : Any, acc : Any)"></endpoint>
<signature id="Arcade.set_acc+2">Arcade.set_acc(**entity**: `Any`, **acc**: `Any`)
<a class="headerlink" href="#Arcade.set_acc+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="get_max_speed(entity : Any)"></endpoint>
<signature id="Arcade.get_max_speed">Arcade.get_max_speed(**entity**: `Any`)
<a class="headerlink" href="#Arcade.get_max_speed" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="set_max_speed(entity : Any, max_speed : Any)"></endpoint>
<signature id="Arcade.set_max_speed+2">Arcade.set_max_speed(**entity**: `Any`, **max_speed**: `Any`)
<a class="headerlink" href="#Arcade.set_max_speed+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="get_solid(entity : Any)"></endpoint>
<signature id="Arcade.get_solid">Arcade.get_solid(**entity**: `Any`)
<a class="headerlink" href="#Arcade.get_solid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="set_solid(entity : Any, solid : Any)"></endpoint>
<signature id="Arcade.set_solid+2">Arcade.set_solid(**entity**: `Any`, **solid**: `Any`)
<a class="headerlink" href="#Arcade.set_solid+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="get_dynamic(entity : Any)"></endpoint>
<signature id="Arcade.get_dynamic">Arcade.get_dynamic(**entity**: `Any`)
<a class="headerlink" href="#Arcade.get_dynamic" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="set_dynamic(entity : Any, dynamic : Any)"></endpoint>
<signature id="Arcade.set_dynamic+2">Arcade.set_dynamic(**entity**: `Any`, **dynamic**: `Any`)
<a class="headerlink" href="#Arcade.set_dynamic+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="get_restitution(entity : Any)"></endpoint>
<signature id="Arcade.get_restitution">Arcade.get_restitution(**entity**: `Any`)
<a class="headerlink" href="#Arcade.get_restitution" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="set_restitution(entity : Any, restitution : Any)"></endpoint>
<signature id="Arcade.set_restitution+2">Arcade.set_restitution(**entity**: `Any`, **restitution**: `Any`)
<a class="headerlink" href="#Arcade.set_restitution+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="get_drag(entity : Any)"></endpoint>
<signature id="Arcade.get_drag">Arcade.get_drag(**entity**: `Any`)
<a class="headerlink" href="#Arcade.get_drag" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="set_drag(entity : Any, drag : Any)"></endpoint>
<signature id="Arcade.set_drag+2">Arcade.set_drag(**entity**: `Any`, **drag**: `Any`)
<a class="headerlink" href="#Arcade.set_drag+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="set_drag_x(entity : Any, drag_x : Any)"></endpoint>
<signature id="Arcade.set_drag_x+2">Arcade.set_drag_x(**entity**: `Any`, **drag_x**: `Any`)
<a class="headerlink" href="#Arcade.set_drag_x+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="set_drag_y(entity : Any, drag_y : Any)"></endpoint>
<signature id="Arcade.set_drag_y+2">Arcade.set_drag_y(**entity**: `Any`, **drag_y**: `Any`)
<a class="headerlink" href="#Arcade.set_drag_y+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="add_collision_callback(entity : Any, fn : Any)"></endpoint>
<signature id="Arcade.add_collision_callback+2">Arcade.add_collision_callback(**entity**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#Arcade.add_collision_callback+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="remove_collision_callback(entity : Any, fn : Any)"></endpoint>
<signature id="Arcade.remove_collision_callback+2">Arcade.remove_collision_callback(**entity**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#Arcade.remove_collision_callback+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="get_frame_collision_normals(entity : Any)"></endpoint>
<signature id="Arcade.get_frame_collision_normals">Arcade.get_frame_collision_normals(**entity**: `Any`)
<a class="headerlink" href="#Arcade.get_frame_collision_normals" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="collided_with_normal_angle(entity : Any, angle_center : Any, angle_spread : Any)"></endpoint>
<signature id="Arcade.collided_with_normal_angle+3">Arcade.collided_with_normal_angle(**entity**: `Any`, **angle_center**: `Any`, **angle_spread**: `Any`)
<a class="headerlink" href="#Arcade.collided_with_normal_angle+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="set_shape_type(entity : Any, shape_type : Any)"></endpoint>
<signature id="Arcade.set_shape_type+2">Arcade.set_shape_type(**entity**: `Any`, **shape_type**: `Any`)
<a class="headerlink" href="#Arcade.set_shape_type+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="get_shape_type(entity : Any)"></endpoint>
<signature id="Arcade.get_shape_type">Arcade.get_shape_type(**entity**: `Any`)
<a class="headerlink" href="#Arcade.get_shape_type" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="get_width(entity : Any)"></endpoint>
<signature id="Arcade.get_width">Arcade.get_width(**entity**: `Any`)
<a class="headerlink" href="#Arcade.get_width" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="get_height(entity : Any)"></endpoint>
<signature id="Arcade.get_height">Arcade.get_height(**entity**: `Any`)
<a class="headerlink" href="#Arcade.get_height" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="set_width(entity : Any, width : Any)"></endpoint>
<signature id="Arcade.set_width+2">Arcade.set_width(**entity**: `Any`, **width**: `Any`)
<a class="headerlink" href="#Arcade.set_width+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="set_height(entity : Any, height : Any)"></endpoint>
<signature id="Arcade.set_height+2">Arcade.set_height(**entity**: `Any`, **height**: `Any`)
<a class="headerlink" href="#Arcade.set_height+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="set_centered(entity : Any, centered : Any)"></endpoint>
<signature id="Arcade.set_centered+2">Arcade.set_centered(**entity**: `Any`, **centered**: `Any`)
<a class="headerlink" href="#Arcade.set_centered+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="set_radius(entity : Any, radius : Any)"></endpoint>
<signature id="Arcade.set_radius+2">Arcade.set_radius(**entity**: `Any`, **radius**: `Any`)
<a class="headerlink" href="#Arcade.set_radius+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="set_broadphase_cell_size(world : Any, size : Any)"></endpoint>
<signature id="Arcade.set_broadphase_cell_size+2">Arcade.set_broadphase_cell_size(**world**: `Any`, **size**: `Any`)
<a class="headerlink" href="#Arcade.set_broadphase_cell_size+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="set_debug_draw_enabled(world : Any, enabled : Any)"></endpoint>
<signature id="Arcade.set_debug_draw_enabled+2">Arcade.set_debug_draw_enabled(**world**: `Any`, **enabled**: `Any`)
<a class="headerlink" href="#Arcade.set_debug_draw_enabled+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="get_debug_draw_enabled(world : Any)"></endpoint>
<signature id="Arcade.get_debug_draw_enabled">Arcade.get_debug_draw_enabled(**world**: `Any`)
<a class="headerlink" href="#Arcade.get_debug_draw_enabled" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="toggle_debug_draw_enabled(world : Any)"></endpoint>
<signature id="Arcade.toggle_debug_draw_enabled">Arcade.toggle_debug_draw_enabled(**world**: `Any`)
<a class="headerlink" href="#Arcade.toggle_debug_draw_enabled" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="set_ignored(entity : Any, other : Any, state : Any)"></endpoint>
<signature id="Arcade.set_ignored+3">Arcade.set_ignored(**entity**: `Any`, **other**: `Any`, **state**: `Any`)
<a class="headerlink" href="#Arcade.set_ignored+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Arcade" signature="refresh(entity : Any)"></endpoint>
<signature id="Arcade.refresh">Arcade.refresh(**entity**: `Any`)
<a class="headerlink" href="#Arcade.refresh" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### CollisionEvent
`:::js import "arcade: modifier/arcade" for CollisionEvent`
> no docs found

- [begin](#CollisionEvent.begin)
- [overlap](#CollisionEvent.overlap)
- [end](#CollisionEvent.end)
- [name](#CollisionEvent.name)(**value**: `Any`)

<hr/>
<endpoint module="arcade: modifier/arcade" class="CollisionEvent" signature="begin"></endpoint>
<signature id="CollisionEvent.begin">CollisionEvent.begin
<a class="headerlink" href="#CollisionEvent.begin" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="CollisionEvent" signature="overlap"></endpoint>
<signature id="CollisionEvent.overlap">CollisionEvent.overlap
<a class="headerlink" href="#CollisionEvent.overlap" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="CollisionEvent" signature="end"></endpoint>
<signature id="CollisionEvent.end">CollisionEvent.end
<a class="headerlink" href="#CollisionEvent.end" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="CollisionEvent" signature="name(value : Any)"></endpoint>
<signature id="CollisionEvent.name">CollisionEvent.name(**value**: `Any`)
<a class="headerlink" href="#CollisionEvent.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### ContactCache
`:::js import "arcade: modifier/arcade" for ContactCache`
> no docs found

- [new](#ContactCache.new)()
- [listen](#ContactCache.listen+2)(**entity**: `Any`, **fn**: `Any`)
- [unlisten](#ContactCache.unlisten+2)(**entity**: `Any`, **fn**: `Any`)
- [track](#ContactCache.track)(**entity**: `Any`)
- [untrack](#ContactCache.untrack)(**entity**: `Any`)
- [overlapped](#ContactCache.overlapped+4)(**entity_a**: `Any`, **entity_b**: `Any`, **normal**: `Any`, **overlap_dist**: `Any`)
- [send_event](#ContactCache.send_event+6)(**entity_a**: `Any`, **entity_b**: `Any`, **state**: `Any`, **normal**: `Any`, **overlap_dist**: `Any`, **flip**: `Any`)
- [set_ignored](#ContactCache.set_ignored+3)(**entity_a**: `Any`, **entity_b**: `Any`, **ignored**: `Any`)
- [is_ignored](#ContactCache.is_ignored+2)(**entity_a**: `Any`, **entity_b**: `Any`)
- [post_collision](#ContactCache.post_collision)()

<hr/>
<endpoint module="arcade: modifier/arcade" class="ContactCache" signature="new()"></endpoint>
<signature id="ContactCache.new">ContactCache.new()
<a class="headerlink" href="#ContactCache.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js ContactCache`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="ContactCache" signature="listen(entity : Any, fn : Any)"></endpoint>
<signature id="ContactCache.listen+2">ContactCache.listen(**entity**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#ContactCache.listen+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="ContactCache" signature="unlisten(entity : Any, fn : Any)"></endpoint>
<signature id="ContactCache.unlisten+2">ContactCache.unlisten(**entity**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#ContactCache.unlisten+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="ContactCache" signature="track(entity : Any)"></endpoint>
<signature id="ContactCache.track">ContactCache.track(**entity**: `Any`)
<a class="headerlink" href="#ContactCache.track" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="ContactCache" signature="untrack(entity : Any)"></endpoint>
<signature id="ContactCache.untrack">ContactCache.untrack(**entity**: `Any`)
<a class="headerlink" href="#ContactCache.untrack" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="ContactCache" signature="overlapped(entity_a : Any, entity_b : Any, normal : Any, overlap_dist : Any)"></endpoint>
<signature id="ContactCache.overlapped+4">ContactCache.overlapped(**entity_a**: `Any`, **entity_b**: `Any`, **normal**: `Any`, **overlap_dist**: `Any`)
<a class="headerlink" href="#ContactCache.overlapped+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="ContactCache" signature="send_event(entity_a : Any, entity_b : Any, state : Any, normal : Any, overlap_dist : Any, flip : Any)"></endpoint>
<signature id="ContactCache.send_event+6">ContactCache.send_event(**entity_a**: `Any`, **entity_b**: `Any`, **state**: `Any`, **normal**: `Any`, **overlap_dist**: `Any`, **flip**: `Any`)
<a class="headerlink" href="#ContactCache.send_event+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="ContactCache" signature="set_ignored(entity_a : Any, entity_b : Any, ignored : Any)"></endpoint>
<signature id="ContactCache.set_ignored+3">ContactCache.set_ignored(**entity_a**: `Any`, **entity_b**: `Any`, **ignored**: `Any`)
<a class="headerlink" href="#ContactCache.set_ignored+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="ContactCache" signature="is_ignored(entity_a : Any, entity_b : Any)"></endpoint>
<signature id="ContactCache.is_ignored+2">ContactCache.is_ignored(**entity_a**: `Any`, **entity_b**: `Any`)
<a class="headerlink" href="#ContactCache.is_ignored+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="ContactCache" signature="post_collision()"></endpoint>
<signature id="ContactCache.post_collision">ContactCache.post_collision()
<a class="headerlink" href="#ContactCache.post_collision" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### ContactState
`:::js import "arcade: modifier/arcade" for ContactState`
> no docs found

- [not_seen](#ContactState.not_seen)
- [seen_last_frame](#ContactState.seen_last_frame)
- [seen_this_frame](#ContactState.seen_this_frame)

<hr/>
<endpoint module="arcade: modifier/arcade" class="ContactState" signature="not_seen"></endpoint>
<signature id="ContactState.not_seen">ContactState.not_seen
<a class="headerlink" href="#ContactState.not_seen" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="ContactState" signature="seen_last_frame"></endpoint>
<signature id="ContactState.seen_last_frame">ContactState.seen_last_frame
<a class="headerlink" href="#ContactState.seen_last_frame" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="ContactState" signature="seen_this_frame"></endpoint>
<signature id="ContactState.seen_this_frame">ContactState.seen_this_frame
<a class="headerlink" href="#ContactState.seen_this_frame" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Shape2DDraw
`:::js import "arcade: modifier/arcade" for Shape2DDraw`
> no docs found

- [draw_shape](#Shape2DDraw.draw_shape+4)(**shape**: `Any`, **ctx**: `Any`, **style**: `Any`, **depth**: `Any`)
- [draw_poly](#Shape2DDraw.draw_poly+4)(**verts**: `Any`, **ctx**: `Any`, **style**: `Any`, **depth**: `Any`)

<hr/>
<endpoint module="arcade: modifier/arcade" class="Shape2DDraw" signature="draw_shape(shape : Any, ctx : Any, style : Any, depth : Any)"></endpoint>
<signature id="Shape2DDraw.draw_shape+4">Shape2DDraw.draw_shape(**shape**: `Any`, **ctx**: `Any`, **style**: `Any`, **depth**: `Any`)
<a class="headerlink" href="#Shape2DDraw.draw_shape+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="Shape2DDraw" signature="draw_poly(verts : Any, ctx : Any, style : Any, depth : Any)"></endpoint>
<signature id="Shape2DDraw.draw_poly+4">Shape2DDraw.draw_poly(**verts**: `Any`, **ctx**: `Any`, **style**: `Any`, **depth**: `Any`)
<a class="headerlink" href="#Shape2DDraw.draw_poly+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### ShapeType
`:::js import "arcade: modifier/arcade" for ShapeType`
> no docs found

- [rect](#ShapeType.rect)
- [circle](#ShapeType.circle)

<hr/>
<endpoint module="arcade: modifier/arcade" class="ShapeType" signature="rect"></endpoint>
<signature id="ShapeType.rect">ShapeType.rect
<a class="headerlink" href="#ShapeType.rect" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="ShapeType" signature="circle"></endpoint>
<signature id="ShapeType.circle">ShapeType.circle
<a class="headerlink" href="#ShapeType.circle" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### SimpleSpatialHash
`:::js import "arcade: modifier/arcade" for SimpleSpatialHash`
> no docs found

- [new](#SimpleSpatialHash.new)(**world**: `Any`)
- [set_cell_size](#SimpleSpatialHash.set_cell_size)(**size**: `Any`)
- [bounds_to_grid](#SimpleSpatialHash.bounds_to_grid)(**bounds**: `Any`)
- [bounds](#SimpleSpatialHash.bounds+5)(**x**: `Any`, **y**: `Any`, **aabb_w**: `Any`, **aabb_h**: `Any`, **into**: `Any`)
- [bounds_uncentered](#SimpleSpatialHash.bounds_uncentered+5)(**x**: `Any`, **y**: `Any`, **aabb_w**: `Any`, **aabb_h**: `Any`, **into**: `Any`)
- [has_changed](#SimpleSpatialHash.has_changed+6)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`, **centered**: `Any`)
- [query_area](#SimpleSpatialHash.query_area+5)(**x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`, **fn**: `Any`)
- [update](#SimpleSpatialHash.update+6)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **aabb_w**: `Any`, **aabb_h**: `Any`, **centered**: `Any`)
- [refresh](#SimpleSpatialHash.refresh+6)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **aabb_w**: `Any`, **aabb_h**: `Any`, **centered**: `Any`)
- [remove](#SimpleSpatialHash.remove)(**entity**: `Any`)
- [remove](#SimpleSpatialHash.remove+2)(**entity**: `Any`, **completely**: `Any`)
- [draw](#SimpleSpatialHash.draw+3)(**ctx**: `Any`, **ctx_ui**: `Any`, **style**: `Any`)
- [text](#SimpleSpatialHash.text+6)(**draw**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **size**: `Any`, **text**: `Any`)
- [get_depth](#SimpleSpatialHash.get_depth+4)(**count**: `Any`, **min**: `Any`, **max**: `Any`, **value**: `Any`)
- [get_color](#SimpleSpatialHash.get_color+5)(**colors**: `Any`, **min**: `Any`, **max**: `Any`, **value**: `Any`, **into**: `Any`)

<hr/>
<endpoint module="arcade: modifier/arcade" class="SimpleSpatialHash" signature="new(world : Any)"></endpoint>
<signature id="SimpleSpatialHash.new">SimpleSpatialHash.new(**world**: `Any`)
<a class="headerlink" href="#SimpleSpatialHash.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js SimpleSpatialHash`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="SimpleSpatialHash" signature="set_cell_size(size : Any)"></endpoint>
<signature id="SimpleSpatialHash.set_cell_size">SimpleSpatialHash.set_cell_size(**size**: `Any`)
<a class="headerlink" href="#SimpleSpatialHash.set_cell_size" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="SimpleSpatialHash" signature="bounds_to_grid(bounds : Any)"></endpoint>
<signature id="SimpleSpatialHash.bounds_to_grid">SimpleSpatialHash.bounds_to_grid(**bounds**: `Any`)
<a class="headerlink" href="#SimpleSpatialHash.bounds_to_grid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="SimpleSpatialHash" signature="bounds(x : Any, y : Any, aabb_w : Any, aabb_h : Any, into : Any)"></endpoint>
<signature id="SimpleSpatialHash.bounds+5">SimpleSpatialHash.bounds(**x**: `Any`, **y**: `Any`, **aabb_w**: `Any`, **aabb_h**: `Any`, **into**: `Any`)
<a class="headerlink" href="#SimpleSpatialHash.bounds+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="SimpleSpatialHash" signature="bounds_uncentered(x : Any, y : Any, aabb_w : Any, aabb_h : Any, into : Any)"></endpoint>
<signature id="SimpleSpatialHash.bounds_uncentered+5">SimpleSpatialHash.bounds_uncentered(**x**: `Any`, **y**: `Any`, **aabb_w**: `Any`, **aabb_h**: `Any`, **into**: `Any`)
<a class="headerlink" href="#SimpleSpatialHash.bounds_uncentered+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="SimpleSpatialHash" signature="has_changed(entity : Any, x : Any, y : Any, w : Any, h : Any, centered : Any)"></endpoint>
<signature id="SimpleSpatialHash.has_changed+6">SimpleSpatialHash.has_changed(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`, **centered**: `Any`)
<a class="headerlink" href="#SimpleSpatialHash.has_changed+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="SimpleSpatialHash" signature="query_area(x : Any, y : Any, w : Any, h : Any, fn : Any)"></endpoint>
<signature id="SimpleSpatialHash.query_area+5">SimpleSpatialHash.query_area(**x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#SimpleSpatialHash.query_area+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="SimpleSpatialHash" signature="update(entity : Any, x : Any, y : Any, aabb_w : Any, aabb_h : Any, centered : Any)"></endpoint>
<signature id="SimpleSpatialHash.update+6">SimpleSpatialHash.update(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **aabb_w**: `Any`, **aabb_h**: `Any`, **centered**: `Any`)
<a class="headerlink" href="#SimpleSpatialHash.update+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="SimpleSpatialHash" signature="refresh(entity : Any, x : Any, y : Any, aabb_w : Any, aabb_h : Any, centered : Any)"></endpoint>
<signature id="SimpleSpatialHash.refresh+6">SimpleSpatialHash.refresh(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **aabb_w**: `Any`, **aabb_h**: `Any`, **centered**: `Any`)
<a class="headerlink" href="#SimpleSpatialHash.refresh+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="SimpleSpatialHash" signature="remove(entity : Any)"></endpoint>
<signature id="SimpleSpatialHash.remove">SimpleSpatialHash.remove(**entity**: `Any`)
<a class="headerlink" href="#SimpleSpatialHash.remove" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="SimpleSpatialHash" signature="remove(entity : Any, completely : Any)"></endpoint>
<signature id="SimpleSpatialHash.remove+2">SimpleSpatialHash.remove(**entity**: `Any`, **completely**: `Any`)
<a class="headerlink" href="#SimpleSpatialHash.remove+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="SimpleSpatialHash" signature="draw(ctx : Any, ctx_ui : Any, style : Any)"></endpoint>
<signature id="SimpleSpatialHash.draw+3">SimpleSpatialHash.draw(**ctx**: `Any`, **ctx_ui**: `Any`, **style**: `Any`)
<a class="headerlink" href="#SimpleSpatialHash.draw+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="SimpleSpatialHash" signature="text(draw : Any, x : Any, y : Any, z : Any, size : Any, text : Any)"></endpoint>
<signature id="SimpleSpatialHash.text+6">SimpleSpatialHash.text(**draw**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **size**: `Any`, **text**: `Any`)
<a class="headerlink" href="#SimpleSpatialHash.text+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="SimpleSpatialHash" signature="get_depth(count : Any, min : Any, max : Any, value : Any)"></endpoint>
<signature id="SimpleSpatialHash.get_depth+4">SimpleSpatialHash.get_depth(**count**: `Any`, **min**: `Any`, **max**: `Any`, **value**: `Any`)
<a class="headerlink" href="#SimpleSpatialHash.get_depth+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="arcade: modifier/arcade" class="SimpleSpatialHash" signature="get_color(colors : Any, min : Any, max : Any, value : Any, into : Any)"></endpoint>
<signature id="SimpleSpatialHash.get_color+5">SimpleSpatialHash.get_color(**colors**: `Any`, **min**: `Any`, **max**: `Any`, **value**: `Any`, **into**: `Any`)
<a class="headerlink" href="#SimpleSpatialHash.get_color+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

