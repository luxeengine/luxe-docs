#![](../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.10.1`)  


---

## `luxe: noise` module

- [Noise](#noise)   
- [NoiseCellularDistanceFunc](#noisecellulardistancefunc)   
- [NoiseCellularReturnType](#noisecellularreturntype)   
- [NoiseDomainWarpType](#noisedomainwarptype)   
- [NoiseFractalType](#noisefractaltype)   
- [NoiseRotationType3D](#noiserotationtype3d)   
- [NoiseType](#noisetype)   

---

### Noise
`:::js import "luxe: noise" for Noise`
> no docs found

- [create](#Noise.create)(**type**: `NoiseType`)
- [create](#Noise.create+2)(**type**: `NoiseType`, **seed**: `Num`)
- [destroy](#Noise.destroy)(**handle**: `Noise`)
- [valid](#Noise.valid)(**handle**: `Noise`)
- [get2D](#Noise.get2D+3)(**handle**: `Noise`, **x**: `Num`, **y**: `Num`)
- [get3D](#Noise.get3D+4)(**handle**: `Noise`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
- [set_seed](#Noise.set_seed+2)(**handle**: `Noise`, **seed**: `Num`)
- [domain_warp2D](#Noise.domain_warp2D+3)(**handle**: `Noise`, **x**: `Num`, **y**: `Num`)
- [domain_warp3D](#Noise.domain_warp3D+4)(**handle**: `Noise`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
- [set_rotation_type3D](#Noise.set_rotation_type3D+2)(**handle**: `Noise`, **type**: `NoiseRotationType3D`)
- [set_fractal_type](#Noise.set_fractal_type+2)(**handle**: `Noise`, **type**: `NoiseFractalType`)
- [set_fractal_octaves](#Noise.set_fractal_octaves+2)(**handle**: `Noise`, **octaves**: `Num`)
- [set_fractal_lacunarity](#Noise.set_fractal_lacunarity+2)(**handle**: `Noise`, **lacunarity**: `Num`)
- [set_fractal_gain](#Noise.set_fractal_gain+2)(**handle**: `Noise`, **gain**: `Num`)
- [set_fractal_weighted_strength](#Noise.set_fractal_weighted_strength+2)(**handle**: `Noise`, **weighted_strength**: `Num`)
- [set_fractal_ping_pong_strength](#Noise.set_fractal_ping_pong_strength+2)(**handle**: `Noise`, **ping_pong_strength**: `Num`)
- [set_cellular_distance_func](#Noise.set_cellular_distance_func+2)(**handle**: `Noise`, **distance_func**: `NoiseCellularDistanceFunc`)
- [set_cellular_return_type](#Noise.set_cellular_return_type+2)(**handle**: `Noise`, **type**: `NoiseCellularReturnType`)
- [set_cellular_jitter](#Noise.set_cellular_jitter+2)(**handle**: `Noise`, **jitter**: `Num`)
- [set_domain_warp_type](#Noise.set_domain_warp_type+2)(**handle**: `Noise`, **type**: `NoiseDomainWarpType`)
- [set_domain_warp_amp](#Noise.set_domain_warp_amp+2)(**handle**: `Noise`, **amp**: `Num`)

<hr/>
<endpoint module="luxe: noise" class="Noise" signature="create(type : NoiseType)"></endpoint>
<signature id="Noise.create">Noise.create(**type**: `NoiseType`)
<a class="headerlink" href="#Noise.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Noise`
> no docs found   

<endpoint module="luxe: noise" class="Noise" signature="create(type : NoiseType, seed : Num)"></endpoint>
<signature id="Noise.create+2">Noise.create(**type**: `NoiseType`, **seed**: `Num`)
<a class="headerlink" href="#Noise.create+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Noise`
> no docs found   

<endpoint module="luxe: noise" class="Noise" signature="destroy(handle : Noise)"></endpoint>
<signature id="Noise.destroy">Noise.destroy(**handle**: `Noise`)
<a class="headerlink" href="#Noise.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: noise" class="Noise" signature="valid(handle : Noise)"></endpoint>
<signature id="Noise.valid">Noise.valid(**handle**: `Noise`)
<a class="headerlink" href="#Noise.valid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: noise" class="Noise" signature="get2D(handle : Noise, x : Num, y : Num)"></endpoint>
<signature id="Noise.get2D+3">Noise.get2D(**handle**: `Noise`, **x**: `Num`, **y**: `Num`)
<a class="headerlink" href="#Noise.get2D+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: noise" class="Noise" signature="get3D(handle : Noise, x : Num, y : Num, z : Num)"></endpoint>
<signature id="Noise.get3D+4">Noise.get3D(**handle**: `Noise`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Noise.get3D+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: noise" class="Noise" signature="set_seed(handle : Noise, seed : Num)"></endpoint>
<signature id="Noise.set_seed+2">Noise.set_seed(**handle**: `Noise`, **seed**: `Num`)
<a class="headerlink" href="#Noise.set_seed+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: noise" class="Noise" signature="domain_warp2D(handle : Noise, x : Num, y : Num)"></endpoint>
<signature id="Noise.domain_warp2D+3">Noise.domain_warp2D(**handle**: `Noise`, **x**: `Num`, **y**: `Num`)
<a class="headerlink" href="#Noise.domain_warp2D+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec2`
> no docs found   

<endpoint module="luxe: noise" class="Noise" signature="domain_warp3D(handle : Noise, x : Num, y : Num, z : Num)"></endpoint>
<signature id="Noise.domain_warp3D+4">Noise.domain_warp3D(**handle**: `Noise`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Noise.domain_warp3D+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec3`
> no docs found   

<endpoint module="luxe: noise" class="Noise" signature="set_rotation_type3D(handle : Noise, type : NoiseRotationType3D)"></endpoint>
<signature id="Noise.set_rotation_type3D+2">Noise.set_rotation_type3D(**handle**: `Noise`, **type**: `NoiseRotationType3D`)
<a class="headerlink" href="#Noise.set_rotation_type3D+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: noise" class="Noise" signature="set_fractal_type(handle : Noise, type : NoiseFractalType)"></endpoint>
<signature id="Noise.set_fractal_type+2">Noise.set_fractal_type(**handle**: `Noise`, **type**: `NoiseFractalType`)
<a class="headerlink" href="#Noise.set_fractal_type+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: noise" class="Noise" signature="set_fractal_octaves(handle : Noise, octaves : Num)"></endpoint>
<signature id="Noise.set_fractal_octaves+2">Noise.set_fractal_octaves(**handle**: `Noise`, **octaves**: `Num`)
<a class="headerlink" href="#Noise.set_fractal_octaves+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: noise" class="Noise" signature="set_fractal_lacunarity(handle : Noise, lacunarity : Num)"></endpoint>
<signature id="Noise.set_fractal_lacunarity+2">Noise.set_fractal_lacunarity(**handle**: `Noise`, **lacunarity**: `Num`)
<a class="headerlink" href="#Noise.set_fractal_lacunarity+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: noise" class="Noise" signature="set_fractal_gain(handle : Noise, gain : Num)"></endpoint>
<signature id="Noise.set_fractal_gain+2">Noise.set_fractal_gain(**handle**: `Noise`, **gain**: `Num`)
<a class="headerlink" href="#Noise.set_fractal_gain+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: noise" class="Noise" signature="set_fractal_weighted_strength(handle : Noise, weighted_strength : Num)"></endpoint>
<signature id="Noise.set_fractal_weighted_strength+2">Noise.set_fractal_weighted_strength(**handle**: `Noise`, **weighted_strength**: `Num`)
<a class="headerlink" href="#Noise.set_fractal_weighted_strength+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: noise" class="Noise" signature="set_fractal_ping_pong_strength(handle : Noise, ping_pong_strength : Num)"></endpoint>
<signature id="Noise.set_fractal_ping_pong_strength+2">Noise.set_fractal_ping_pong_strength(**handle**: `Noise`, **ping_pong_strength**: `Num`)
<a class="headerlink" href="#Noise.set_fractal_ping_pong_strength+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: noise" class="Noise" signature="set_cellular_distance_func(handle : Noise, distance_func : NoiseCellularDistanceFunc)"></endpoint>
<signature id="Noise.set_cellular_distance_func+2">Noise.set_cellular_distance_func(**handle**: `Noise`, **distance_func**: `NoiseCellularDistanceFunc`)
<a class="headerlink" href="#Noise.set_cellular_distance_func+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: noise" class="Noise" signature="set_cellular_return_type(handle : Noise, type : NoiseCellularReturnType)"></endpoint>
<signature id="Noise.set_cellular_return_type+2">Noise.set_cellular_return_type(**handle**: `Noise`, **type**: `NoiseCellularReturnType`)
<a class="headerlink" href="#Noise.set_cellular_return_type+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: noise" class="Noise" signature="set_cellular_jitter(handle : Noise, jitter : Num)"></endpoint>
<signature id="Noise.set_cellular_jitter+2">Noise.set_cellular_jitter(**handle**: `Noise`, **jitter**: `Num`)
<a class="headerlink" href="#Noise.set_cellular_jitter+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: noise" class="Noise" signature="set_domain_warp_type(handle : Noise, type : NoiseDomainWarpType)"></endpoint>
<signature id="Noise.set_domain_warp_type+2">Noise.set_domain_warp_type(**handle**: `Noise`, **type**: `NoiseDomainWarpType`)
<a class="headerlink" href="#Noise.set_domain_warp_type+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: noise" class="Noise" signature="set_domain_warp_amp(handle : Noise, amp : Num)"></endpoint>
<signature id="Noise.set_domain_warp_amp+2">Noise.set_domain_warp_amp(**handle**: `Noise`, **amp**: `Num`)
<a class="headerlink" href="#Noise.set_domain_warp_amp+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

### NoiseCellularDistanceFunc
`:::js import "luxe: noise" for NoiseCellularDistanceFunc`
> no docs found

- [euclidean](#NoiseCellularDistanceFunc.euclidean)
- [euclidean_sq](#NoiseCellularDistanceFunc.euclidean_sq)
- [manhattan](#NoiseCellularDistanceFunc.manhattan)
- [hybrid](#NoiseCellularDistanceFunc.hybrid)

<hr/>
<endpoint module="luxe: noise" class="NoiseCellularDistanceFunc" signature="euclidean"></endpoint>
<signature id="NoiseCellularDistanceFunc.euclidean">NoiseCellularDistanceFunc.euclidean
<a class="headerlink" href="#NoiseCellularDistanceFunc.euclidean" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: noise" class="NoiseCellularDistanceFunc" signature="euclidean_sq"></endpoint>
<signature id="NoiseCellularDistanceFunc.euclidean_sq">NoiseCellularDistanceFunc.euclidean_sq
<a class="headerlink" href="#NoiseCellularDistanceFunc.euclidean_sq" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: noise" class="NoiseCellularDistanceFunc" signature="manhattan"></endpoint>
<signature id="NoiseCellularDistanceFunc.manhattan">NoiseCellularDistanceFunc.manhattan
<a class="headerlink" href="#NoiseCellularDistanceFunc.manhattan" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: noise" class="NoiseCellularDistanceFunc" signature="hybrid"></endpoint>
<signature id="NoiseCellularDistanceFunc.hybrid">NoiseCellularDistanceFunc.hybrid
<a class="headerlink" href="#NoiseCellularDistanceFunc.hybrid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### NoiseCellularReturnType
`:::js import "luxe: noise" for NoiseCellularReturnType`
> no docs found

- [cell_value](#NoiseCellularReturnType.cell_value)
- [distance](#NoiseCellularReturnType.distance)
- [distance2](#NoiseCellularReturnType.distance2)
- [distance2_add](#NoiseCellularReturnType.distance2_add)
- [distance2_sub](#NoiseCellularReturnType.distance2_sub)
- [distance2_mul](#NoiseCellularReturnType.distance2_mul)
- [distance2_div](#NoiseCellularReturnType.distance2_div)

<hr/>
<endpoint module="luxe: noise" class="NoiseCellularReturnType" signature="cell_value"></endpoint>
<signature id="NoiseCellularReturnType.cell_value">NoiseCellularReturnType.cell_value
<a class="headerlink" href="#NoiseCellularReturnType.cell_value" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: noise" class="NoiseCellularReturnType" signature="distance"></endpoint>
<signature id="NoiseCellularReturnType.distance">NoiseCellularReturnType.distance
<a class="headerlink" href="#NoiseCellularReturnType.distance" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: noise" class="NoiseCellularReturnType" signature="distance2"></endpoint>
<signature id="NoiseCellularReturnType.distance2">NoiseCellularReturnType.distance2
<a class="headerlink" href="#NoiseCellularReturnType.distance2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: noise" class="NoiseCellularReturnType" signature="distance2_add"></endpoint>
<signature id="NoiseCellularReturnType.distance2_add">NoiseCellularReturnType.distance2_add
<a class="headerlink" href="#NoiseCellularReturnType.distance2_add" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: noise" class="NoiseCellularReturnType" signature="distance2_sub"></endpoint>
<signature id="NoiseCellularReturnType.distance2_sub">NoiseCellularReturnType.distance2_sub
<a class="headerlink" href="#NoiseCellularReturnType.distance2_sub" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: noise" class="NoiseCellularReturnType" signature="distance2_mul"></endpoint>
<signature id="NoiseCellularReturnType.distance2_mul">NoiseCellularReturnType.distance2_mul
<a class="headerlink" href="#NoiseCellularReturnType.distance2_mul" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: noise" class="NoiseCellularReturnType" signature="distance2_div"></endpoint>
<signature id="NoiseCellularReturnType.distance2_div">NoiseCellularReturnType.distance2_div
<a class="headerlink" href="#NoiseCellularReturnType.distance2_div" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### NoiseDomainWarpType
`:::js import "luxe: noise" for NoiseDomainWarpType`
> no docs found

- [open_simplex2](#NoiseDomainWarpType.open_simplex2)
- [open_simplex2_reduced](#NoiseDomainWarpType.open_simplex2_reduced)
- [basic_grid](#NoiseDomainWarpType.basic_grid)

<hr/>
<endpoint module="luxe: noise" class="NoiseDomainWarpType" signature="open_simplex2"></endpoint>
<signature id="NoiseDomainWarpType.open_simplex2">NoiseDomainWarpType.open_simplex2
<a class="headerlink" href="#NoiseDomainWarpType.open_simplex2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: noise" class="NoiseDomainWarpType" signature="open_simplex2_reduced"></endpoint>
<signature id="NoiseDomainWarpType.open_simplex2_reduced">NoiseDomainWarpType.open_simplex2_reduced
<a class="headerlink" href="#NoiseDomainWarpType.open_simplex2_reduced" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: noise" class="NoiseDomainWarpType" signature="basic_grid"></endpoint>
<signature id="NoiseDomainWarpType.basic_grid">NoiseDomainWarpType.basic_grid
<a class="headerlink" href="#NoiseDomainWarpType.basic_grid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### NoiseFractalType
`:::js import "luxe: noise" for NoiseFractalType`
> no docs found

- [none](#NoiseFractalType.none)
- [fbm](#NoiseFractalType.fbm)
- [ridged](#NoiseFractalType.ridged)
- [pingpong](#NoiseFractalType.pingpong)
- [domain_warp_progressive](#NoiseFractalType.domain_warp_progressive)
- [domain_warp_independent](#NoiseFractalType.domain_warp_independent)

<hr/>
<endpoint module="luxe: noise" class="NoiseFractalType" signature="none"></endpoint>
<signature id="NoiseFractalType.none">NoiseFractalType.none
<a class="headerlink" href="#NoiseFractalType.none" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: noise" class="NoiseFractalType" signature="fbm"></endpoint>
<signature id="NoiseFractalType.fbm">NoiseFractalType.fbm
<a class="headerlink" href="#NoiseFractalType.fbm" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: noise" class="NoiseFractalType" signature="ridged"></endpoint>
<signature id="NoiseFractalType.ridged">NoiseFractalType.ridged
<a class="headerlink" href="#NoiseFractalType.ridged" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: noise" class="NoiseFractalType" signature="pingpong"></endpoint>
<signature id="NoiseFractalType.pingpong">NoiseFractalType.pingpong
<a class="headerlink" href="#NoiseFractalType.pingpong" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: noise" class="NoiseFractalType" signature="domain_warp_progressive"></endpoint>
<signature id="NoiseFractalType.domain_warp_progressive">NoiseFractalType.domain_warp_progressive
<a class="headerlink" href="#NoiseFractalType.domain_warp_progressive" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: noise" class="NoiseFractalType" signature="domain_warp_independent"></endpoint>
<signature id="NoiseFractalType.domain_warp_independent">NoiseFractalType.domain_warp_independent
<a class="headerlink" href="#NoiseFractalType.domain_warp_independent" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### NoiseRotationType3D
`:::js import "luxe: noise" for NoiseRotationType3D`
> no docs found

- [none](#NoiseRotationType3D.none)
- [improve_xy_planes](#NoiseRotationType3D.improve_xy_planes)
- [improve_xz_planes](#NoiseRotationType3D.improve_xz_planes)

<hr/>
<endpoint module="luxe: noise" class="NoiseRotationType3D" signature="none"></endpoint>
<signature id="NoiseRotationType3D.none">NoiseRotationType3D.none
<a class="headerlink" href="#NoiseRotationType3D.none" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: noise" class="NoiseRotationType3D" signature="improve_xy_planes"></endpoint>
<signature id="NoiseRotationType3D.improve_xy_planes">NoiseRotationType3D.improve_xy_planes
<a class="headerlink" href="#NoiseRotationType3D.improve_xy_planes" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: noise" class="NoiseRotationType3D" signature="improve_xz_planes"></endpoint>
<signature id="NoiseRotationType3D.improve_xz_planes">NoiseRotationType3D.improve_xz_planes
<a class="headerlink" href="#NoiseRotationType3D.improve_xz_planes" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### NoiseType
`:::js import "luxe: noise" for NoiseType`
> no docs found

- [open_simplex2](#NoiseType.open_simplex2)
- [open_simplex2s](#NoiseType.open_simplex2s)
- [cellular](#NoiseType.cellular)
- [perlin](#NoiseType.perlin)
- [value_cubic](#NoiseType.value_cubic)
- [value](#NoiseType.value)

<hr/>
<endpoint module="luxe: noise" class="NoiseType" signature="open_simplex2"></endpoint>
<signature id="NoiseType.open_simplex2">NoiseType.open_simplex2
<a class="headerlink" href="#NoiseType.open_simplex2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: noise" class="NoiseType" signature="open_simplex2s"></endpoint>
<signature id="NoiseType.open_simplex2s">NoiseType.open_simplex2s
<a class="headerlink" href="#NoiseType.open_simplex2s" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: noise" class="NoiseType" signature="cellular"></endpoint>
<signature id="NoiseType.cellular">NoiseType.cellular
<a class="headerlink" href="#NoiseType.cellular" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: noise" class="NoiseType" signature="perlin"></endpoint>
<signature id="NoiseType.perlin">NoiseType.perlin
<a class="headerlink" href="#NoiseType.perlin" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: noise" class="NoiseType" signature="value_cubic"></endpoint>
<signature id="NoiseType.value_cubic">NoiseType.value_cubic
<a class="headerlink" href="#NoiseType.value_cubic" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: noise" class="NoiseType" signature="value"></endpoint>
<signature id="NoiseType.value">NoiseType.value
<a class="headerlink" href="#NoiseType.value" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

