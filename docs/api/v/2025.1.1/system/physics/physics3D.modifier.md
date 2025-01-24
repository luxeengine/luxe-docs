#![](../../../../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2025.1.1`)  


---

## `luxe: system/physics/physics3D.modifier` module

- [Data](#data)   
- [Physics3D](#physics3d)   
- [System](#system)   

---

### Data
`:::js import "luxe: system/physics/physics3D.modifier" for Data`
> no docs found

- `:::js var gravity : Float3 = [0, -9.8, 0]`

<hr/>
### Physics3D
`:::js import "luxe: system/physics/physics3D.modifier" for Physics3D`
> no docs found

- [create_in](#Physics3D.create_in)(**world**: `World`)
- [cast_ray_closest](#Physics3D.cast_ray_closest+4)(**world**: `World`, **origin**: `Float3`, **dir**: `Float3`, **distance**: `Num`)
- [cast_ray](#Physics3D.cast_ray+4)(**world**: `World`, **origin**: `Float3`, **dir**: `Float3`, **distance**: `Num`)
- [set_debug_draw](#Physics3D.set_debug_draw+2)(**world**: `World`, **state**: `Bool`)
- [unlisten](#Physics3D.unlisten+2)(**world**: `World`, **handle**: `Handle`)
- [listen](#Physics3D.listen+2)(**world**: `World`, **fn**: `Fn`)

<hr/>
<endpoint module="luxe: system/physics/physics3D.modifier" class="Physics3D" signature="create_in(world : World)"></endpoint>
<signature id="Physics3D.create_in">Physics3D.create_in(**world**: `World`)
<a class="headerlink" href="#Physics3D.create_in" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/physics/physics3D.modifier" class="Physics3D" signature="cast_ray_closest(world : World, origin : Float3, dir : Float3, distance : Num)"></endpoint>
<signature id="Physics3D.cast_ray_closest+4">Physics3D.cast_ray_closest(**world**: `World`, **origin**: `Float3`, **dir**: `Float3`, **distance**: `Num`)
<a class="headerlink" href="#Physics3D.cast_ray_closest+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js CastRayResult`
> no docs found   

<endpoint module="luxe: system/physics/physics3D.modifier" class="Physics3D" signature="cast_ray(world : World, origin : Float3, dir : Float3, distance : Num)"></endpoint>
<signature id="Physics3D.cast_ray+4">Physics3D.cast_ray(**world**: `World`, **origin**: `Float3`, **dir**: `Float3`, **distance**: `Num`)
<a class="headerlink" href="#Physics3D.cast_ray+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Cast a ray into the world and return all hits, sorted by closest first   

<endpoint module="luxe: system/physics/physics3D.modifier" class="Physics3D" signature="set_debug_draw(world : World, state : Bool)"></endpoint>
<signature id="Physics3D.set_debug_draw+2">Physics3D.set_debug_draw(**world**: `World`, **state**: `Bool`)
<a class="headerlink" href="#Physics3D.set_debug_draw+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: system/physics/physics3D.modifier" class="Physics3D" signature="unlisten(world : World, handle : Handle)"></endpoint>
<signature id="Physics3D.unlisten+2">Physics3D.unlisten(**world**: `World`, **handle**: `Handle`)
<a class="headerlink" href="#Physics3D.unlisten+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: system/physics/physics3D.modifier" class="Physics3D" signature="listen(world : World, fn : Fn)"></endpoint>
<signature id="Physics3D.listen+2">Physics3D.listen(**world**: `World`, **fn**: `Fn`)
<a class="headerlink" href="#Physics3D.listen+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### System
`:::js import "luxe: system/physics/physics3D.modifier" for System`
> no docs found

- [new](#System.new)(**world**: `World`)
- [init](#System.init)(**world**: `World`)

<hr/>
<endpoint module="luxe: system/physics/physics3D.modifier" class="System" signature="new(world : World)"></endpoint>
<signature id="System.new">System.new(**world**: `World`)
<a class="headerlink" href="#System.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js System`
> no docs found   

<endpoint module="luxe: system/physics/physics3D.modifier" class="System" signature="init(world : World)"></endpoint>
<signature id="System.init">System.init(**world**: `World`)
<a class="headerlink" href="#System.init" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

