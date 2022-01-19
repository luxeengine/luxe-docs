#![](../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2022.0.3`)  


---

## `luxe: sat2D` module

- [SAT2D](#sat2d)   

---

### SAT2D
`:::js import "luxe: sat2D" for SAT2D`
> The SAT2D API is a collision and query API for the [luxe: shape2D](../shape2D) shapes and types.
> It implements the "separating axis theorom" for collision.   
> **Note** The return values in the API are not user friendly atm, this will improve.
> They return lists with various values packed inside.

- [collide_shape](#SAT2D.collide_shape+2)(**shape1**: `Any`, **shape2**: `Any`)
- [collide_shapes](#SAT2D.collide_shapes+2)(**shape**: `Any`, **list**: `Any`)
- [contains](#SAT2D.contains+2)(**shape**: `Any`, **point**: `Any`)
- [sweep_shape](#SAT2D.sweep_shape+3)(**shape1**: `Any`, **shape2**: `Any`, **vel**: `Any`)
- [raycast_ray](#SAT2D.raycast_ray+2)(**ray1**: `Any`, **ray2**: `Any`)
- [raycast_rays](#SAT2D.raycast_rays+2)(**ray**: `Any`, **rays**: `Any`)
- [raycast_shape](#SAT2D.raycast_shape+2)(**ray**: `Any`, **shape**: `Any`)
- [raycast_shapes](#SAT2D.raycast_shapes+2)(**ray**: `Any`, **shapes**: `Any`)

<hr/>
<endpoint module="luxe: sat2D" class="SAT2D" signature="collide_shape(shape1 : Any, shape2 : Any)"></endpoint>
<signature id="SAT2D.collide_shape+2">SAT2D.collide_shape(**shape1**: `Any`, **shape2**: `Any`)
<a class="headerlink" href="#SAT2D.collide_shape+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Check if two `Shape2D` instances are colliding. Returns a result with several values in a `List`.
> 
> The results include a `separation` value for x and y axis, which is how much to move `shape1` to cancel
> out the overlap. An example of using this: move a player `shape2D` collider, check for collision,
> and then move them back by `separation` so that they do not collide anymore.
> 
>   ```js
>   [
>     shape1,       //the original shapes
>     shape2,
>     overlap,      //amount the shapes overlap
>     separation_x, //the amount to separate on the x axis
>     separation_y, //the amount to separate on the y axis
>     normal_x,     //the normal of the collision
>     normal_y      //the amount to separate on the y axis
>   ]
>   ```   

<endpoint module="luxe: sat2D" class="SAT2D" signature="collide_shapes(shape : Any, list : Any)"></endpoint>
<signature id="SAT2D.collide_shapes+2">SAT2D.collide_shapes(**shape**: `Any`, **list**: `Any`)
<a class="headerlink" href="#SAT2D.collide_shapes+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Like `collide_shape` for details on the results, but checks multiple shapes against a single one. 
> For example `SAT2D.collide_shapes(player, walls)`, where walls is a list of `Shape2D` to collide against.
> 
> Note this returns a list of results, and each result is a list described by `collide_shape`.
> 
>   ```js
>   //:todo: example. see samples/wip/shape2D
>   ```   

<endpoint module="luxe: sat2D" class="SAT2D" signature="contains(shape : Any, point : Any)"></endpoint>
<signature id="SAT2D.contains+2">SAT2D.contains(**shape**: `Any`, **point**: `Any`)
<a class="headerlink" href="#SAT2D.contains+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns true if the given `Shape2D` contains `point`.   

<endpoint module="luxe: sat2D" class="SAT2D" signature="sweep_shape(shape1 : Any, shape2 : Any, vel : Any)"></endpoint>
<signature id="SAT2D.sweep_shape+3">SAT2D.sweep_shape(**shape1**: `Any`, **shape2**: `Any`, **vel**: `Any`)
<a class="headerlink" href="#SAT2D.sweep_shape+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
>    

<endpoint module="luxe: sat2D" class="SAT2D" signature="raycast_ray(ray1 : Any, ray2 : Any)"></endpoint>
<signature id="SAT2D.raycast_ray+2">SAT2D.raycast_ray(**ray1**: `Any`, **ray2**: `Any`)
<a class="headerlink" href="#SAT2D.raycast_ray+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
>    

<endpoint module="luxe: sat2D" class="SAT2D" signature="raycast_rays(ray : Any, rays : Any)"></endpoint>
<signature id="SAT2D.raycast_rays+2">SAT2D.raycast_rays(**ray**: `Any`, **rays**: `Any`)
<a class="headerlink" href="#SAT2D.raycast_rays+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
>    

<endpoint module="luxe: sat2D" class="SAT2D" signature="raycast_shape(ray : Any, shape : Any)"></endpoint>
<signature id="SAT2D.raycast_shape+2">SAT2D.raycast_shape(**ray**: `Any`, **shape**: `Any`)
<a class="headerlink" href="#SAT2D.raycast_shape+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
>    

<endpoint module="luxe: sat2D" class="SAT2D" signature="raycast_shapes(ray : Any, shapes : Any)"></endpoint>
<signature id="SAT2D.raycast_shapes+2">SAT2D.raycast_shapes(**ray**: `Any`, **shapes**: `Any`)
<a class="headerlink" href="#SAT2D.raycast_shapes+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
>    

