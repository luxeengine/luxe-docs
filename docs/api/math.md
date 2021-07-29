#![](../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2021.0.7`)  


---

## `luxe: math` module

- [Math](#math)   

---

### Math
`:::js import "luxe: math" for Math`
> no docs found

- [length](#Math.length+2)(**x**: `Any`, **y**: `Any`)
- [length](#Math.length+3)(**x**: `Any`, **y**: `Any`, **z**: `Any`)
- [length](#Math.length)(**vec**: `Any`)
- [length2D](#Math.length2D)(**vec**: `Any`)
- [length_sq](#Math.length_sq+2)(**x**: `Any`, **y**: `Any`)
- [length_sq](#Math.length_sq+3)(**x**: `Any`, **y**: `Any`, **z**: `Any`)
- [length_sq](#Math.length_sq)(**vec**: `Any`)
- [length_sq2D](#Math.length_sq2D)(**vec**: `Any`)
- [dot](#Math.dot+6)(**x**: `Any`, **y**: `Any`, **z**: `Any`, **other_x**: `Any`, **other_y**: `Any`, **other_z**: `Any`)
- [dot](#Math.dot+4)(**x**: `Any`, **y**: `Any`, **other_x**: `Any`, **other_y**: `Any`)
- [dot](#Math.dot+2)(**vec**: `Any`, **other**: `Any`)
- [dot2D](#Math.dot2D+2)(**vec**: `Any`, **other**: `Any`)
- [cross](#Math.cross+2)(**a**: `Any`, **b**: `Any`)
- [angle](#Math.angle+2)(**from**: `Any`, **to**: `Any`)
- [angle](#Math.angle+3)(**v1**: `Any`, **v2**: `Any`, **up**: `Any`)
- [normalize2D](#Math.normalize2D)(**vec**: `Any`)
- [normalize](#Math.normalize)(**vec**: `Any`)
- [dist](#Math.dist+6)(**x**: `Any`, **y**: `Any`, **z**: `Any`, **other_x**: `Any`, **other_y**: `Any`, **other_z**: `Any`)
- [dist](#Math.dist+2)(**vec**: `Any`, **other**: `Any`)
- [dist2D](#Math.dist2D+2)(**vec**: `Any`, **other**: `Any`)
- [dist2D](#Math.dist2D+4)(**x**: `Any`, **y**: `Any`, **other_x**: `Any`, **other_y**: `Any`)
- [dir2D](#Math.dir2D+2)(**pos**: `Any`, **target**: `Any`)
- [rotate](#Math.rotate+4)(**vec**: `Any`, **ox**: `Any`, **oy**: `Any`, **angle**: `Any`)
- [ray_intersect_plane](#Math.ray_intersect_plane+12)(**plane_x**: `Any`, **plane_y**: `Any`, **plane_z**: `Any`, **normal_x**: `Any`, **normal_y**: `Any`, **normal_z**: `Any`, **ray_x**: `Any`, **ray_y**: `Any`, **ray_z**: `Any`, **ray_dir_x**: `Any`, **ray_dir_y**: `Any`, **ray_dir_z**: `Any`)
- [closest_point_on_plane](#Math.closest_point_on_plane+9)(**plane_x**: `Any`, **plane_y**: `Any`, **plane_z**: `Any`, **normal_x**: `Any`, **normal_y**: `Any`, **normal_z**: `Any`, **point_x**: `Any`, **point_y**: `Any`, **point_z**: `Any`)
- [closest_point_on_line](#Math.closest_point_on_line+9)(**line_x**: `Any`, **line_y**: `Any`, **line_z**: `Any`, **line_end_x**: `Any`, **line_end_y**: `Any`, **line_end_z**: `Any`, **point_x**: `Any`, **point_y**: `Any`, **point_z**: `Any`)
- [in_rect](#Math.in_rect+6)(**x**: `Any`, **y**: `Any`, **rx**: `Any`, **ry**: `Any`, **rw**: `Any`, **rh**: `Any`)
- [overlaps](#Math.overlaps+8)(**x0**: `Any`, **y0**: `Any`, **w0**: `Any`, **h0**: `Any`, **x1**: `Any`, **y1**: `Any`, **w1**: `Any`, **h1**: `Any`)
- [sign](#Math.sign)(**x**: `Any`)
- [sign0](#Math.sign0)(**x**: `Any`)
- [atan2](#Math.atan2+2)(**y**: `Any`, **x**: `Any`)
- [degrees](#Math.degrees)(**radians**: `Any`)
- [radians](#Math.radians)(**degrees**: `Any`)
- [clamp](#Math.clamp+3)(**value**: `Any`, **a**: `Any`, **b**: `Any`)
- [min](#Math.min+2)(**a**: `Any`, **b**: `Any`)
- [max](#Math.max+2)(**a**: `Any`, **b**: `Any`)
- [floor_around_zero](#Math.floor_around_zero)(**a**: `Any`)
- [ceil_around_zero](#Math.ceil_around_zero)(**a**: `Any`)
- [fixed](#Math.fixed)(**value**: `Any`)
- [fixed](#Math.fixed+2)(**value**: `Any`, **precision**: `Any`)
- [angle_delta](#Math.angle_delta+2)(**a**: `Any`, **b**: `Any`)
- [lerp](#Math.lerp+3)(**a**: `Any`, **b**: `Any`, **t**: `Any`)
- [lerp_angle](#Math.lerp_angle+3)(**a**: `Any`, **b**: `Any`, **t**: `Any`)
- [weighted_avg](#Math.weighted_avg+3)(**value**: `Any`, **target**: `Any`, **slowness**: `Any`)
- [within_range](#Math.within_range+3)(**value**: `Any`, **start_range**: `Any`, **end_range**: `Any`)
- [wrap_angle](#Math.wrap_angle)(**degrees**: `Any`)
- [wrap_angle](#Math.wrap_angle+3)(**degrees**: `Any`, **lower**: `Any`, **upper**: `Any`)
- [wrap_radians](#Math.wrap_radians+3)(**radians**: `Any`, **lower**: `Any`, **upper**: `Any`)
- [nearest_power_of_two](#Math.nearest_power_of_two)(**value**: `Any`)
- [map_linear](#Math.map_linear+5)(**value**: `Any`, **a1**: `Any`, **a2**: `Any`, **b1**: `Any`, **b2**: `Any`)
- [smoothstep](#Math.smoothstep+3)(**x**: `Any`, **min**: `Any`, **max**: `Any`)
- [smootherstep](#Math.smootherstep+3)(**x**: `Any`, **min**: `Any`, **max**: `Any`)
- [random_point_in_unit_circle](#Math.random_point_in_unit_circle)(**rng**: `Any`)

<hr/>
<endpoint module="luxe: math" class="Math" signature="length(x : Any, y : Any)"></endpoint>
<signature id="Math.length+2">Math.length(**x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Math.length+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="length(x : Any, y : Any, z : Any)"></endpoint>
<signature id="Math.length+3">Math.length(**x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Math.length+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="length(vec : Any)"></endpoint>
<signature id="Math.length">Math.length(**vec**: `Any`)
<a class="headerlink" href="#Math.length" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="length2D(vec : Any)"></endpoint>
<signature id="Math.length2D">Math.length2D(**vec**: `Any`)
<a class="headerlink" href="#Math.length2D" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="length_sq(x : Any, y : Any)"></endpoint>
<signature id="Math.length_sq+2">Math.length_sq(**x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Math.length_sq+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="length_sq(x : Any, y : Any, z : Any)"></endpoint>
<signature id="Math.length_sq+3">Math.length_sq(**x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Math.length_sq+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="length_sq(vec : Any)"></endpoint>
<signature id="Math.length_sq">Math.length_sq(**vec**: `Any`)
<a class="headerlink" href="#Math.length_sq" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="length_sq2D(vec : Any)"></endpoint>
<signature id="Math.length_sq2D">Math.length_sq2D(**vec**: `Any`)
<a class="headerlink" href="#Math.length_sq2D" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="dot(x : Any, y : Any, z : Any, other_x : Any, other_y : Any, other_z : Any)"></endpoint>
<signature id="Math.dot+6">Math.dot(**x**: `Any`, **y**: `Any`, **z**: `Any`, **other_x**: `Any`, **other_y**: `Any`, **other_z**: `Any`)
<a class="headerlink" href="#Math.dot+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="dot(x : Any, y : Any, other_x : Any, other_y : Any)"></endpoint>
<signature id="Math.dot+4">Math.dot(**x**: `Any`, **y**: `Any`, **other_x**: `Any`, **other_y**: `Any`)
<a class="headerlink" href="#Math.dot+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="dot(vec : Any, other : Any)"></endpoint>
<signature id="Math.dot+2">Math.dot(**vec**: `Any`, **other**: `Any`)
<a class="headerlink" href="#Math.dot+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="dot2D(vec : Any, other : Any)"></endpoint>
<signature id="Math.dot2D+2">Math.dot2D(**vec**: `Any`, **other**: `Any`)
<a class="headerlink" href="#Math.dot2D+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="cross(a : Any, b : Any)"></endpoint>
<signature id="Math.cross+2">Math.cross(**a**: `Any`, **b**: `Any`)
<a class="headerlink" href="#Math.cross+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="angle(from : Any, to : Any)"></endpoint>
<signature id="Math.angle+2">Math.angle(**from**: `Any`, **to**: `Any`)
<a class="headerlink" href="#Math.angle+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="angle(v1 : Any, v2 : Any, up : Any)"></endpoint>
<signature id="Math.angle+3">Math.angle(**v1**: `Any`, **v2**: `Any`, **up**: `Any`)
<a class="headerlink" href="#Math.angle+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="normalize2D(vec : Any)"></endpoint>
<signature id="Math.normalize2D">Math.normalize2D(**vec**: `Any`)
<a class="headerlink" href="#Math.normalize2D" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="normalize(vec : Any)"></endpoint>
<signature id="Math.normalize">Math.normalize(**vec**: `Any`)
<a class="headerlink" href="#Math.normalize" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="dist(x : Any, y : Any, z : Any, other_x : Any, other_y : Any, other_z : Any)"></endpoint>
<signature id="Math.dist+6">Math.dist(**x**: `Any`, **y**: `Any`, **z**: `Any`, **other_x**: `Any`, **other_y**: `Any`, **other_z**: `Any`)
<a class="headerlink" href="#Math.dist+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="dist(vec : Any, other : Any)"></endpoint>
<signature id="Math.dist+2">Math.dist(**vec**: `Any`, **other**: `Any`)
<a class="headerlink" href="#Math.dist+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="dist2D(vec : Any, other : Any)"></endpoint>
<signature id="Math.dist2D+2">Math.dist2D(**vec**: `Any`, **other**: `Any`)
<a class="headerlink" href="#Math.dist2D+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="dist2D(x : Any, y : Any, other_x : Any, other_y : Any)"></endpoint>
<signature id="Math.dist2D+4">Math.dist2D(**x**: `Any`, **y**: `Any`, **other_x**: `Any`, **other_y**: `Any`)
<a class="headerlink" href="#Math.dist2D+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="dir2D(pos : Any, target : Any)"></endpoint>
<signature id="Math.dir2D+2">Math.dir2D(**pos**: `Any`, **target**: `Any`)
<a class="headerlink" href="#Math.dir2D+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="rotate(vec : Any, ox : Any, oy : Any, angle : Any)"></endpoint>
<signature id="Math.rotate+4">Math.rotate(**vec**: `Any`, **ox**: `Any`, **oy**: `Any`, **angle**: `Any`)
<a class="headerlink" href="#Math.rotate+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="ray_intersect_plane(plane_x : Any, plane_y : Any, plane_z : Any, normal_x : Any, normal_y : Any, normal_z : Any, ray_x : Any, ray_y : Any, ray_z : Any, ray_dir_x : Any, ray_dir_y : Any, ray_dir_z : Any)"></endpoint>
<signature id="Math.ray_intersect_plane+12">Math.ray_intersect_plane(**plane_x**: `Any`, **plane_y**: `Any`, **plane_z**: `Any`, **normal_x**: `Any`, **normal_y**: `Any`, **normal_z**: `Any`, **ray_x**: `Any`, **ray_y**: `Any`, **ray_z**: `Any`, **ray_dir_x**: `Any`, **ray_dir_y**: `Any`, **ray_dir_z**: `Any`)
<a class="headerlink" href="#Math.ray_intersect_plane+12" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="closest_point_on_plane(plane_x : Any, plane_y : Any, plane_z : Any, normal_x : Any, normal_y : Any, normal_z : Any, point_x : Any, point_y : Any, point_z : Any)"></endpoint>
<signature id="Math.closest_point_on_plane+9">Math.closest_point_on_plane(**plane_x**: `Any`, **plane_y**: `Any`, **plane_z**: `Any`, **normal_x**: `Any`, **normal_y**: `Any`, **normal_z**: `Any`, **point_x**: `Any`, **point_y**: `Any`, **point_z**: `Any`)
<a class="headerlink" href="#Math.closest_point_on_plane+9" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="closest_point_on_line(line_x : Any, line_y : Any, line_z : Any, line_end_x : Any, line_end_y : Any, line_end_z : Any, point_x : Any, point_y : Any, point_z : Any)"></endpoint>
<signature id="Math.closest_point_on_line+9">Math.closest_point_on_line(**line_x**: `Any`, **line_y**: `Any`, **line_z**: `Any`, **line_end_x**: `Any`, **line_end_y**: `Any`, **line_end_z**: `Any`, **point_x**: `Any`, **point_y**: `Any`, **point_z**: `Any`)
<a class="headerlink" href="#Math.closest_point_on_line+9" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="in_rect(x : Any, y : Any, rx : Any, ry : Any, rw : Any, rh : Any)"></endpoint>
<signature id="Math.in_rect+6">Math.in_rect(**x**: `Any`, **y**: `Any`, **rx**: `Any`, **ry**: `Any`, **rw**: `Any`, **rh**: `Any`)
<a class="headerlink" href="#Math.in_rect+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="overlaps(x0 : Any, y0 : Any, w0 : Any, h0 : Any, x1 : Any, y1 : Any, w1 : Any, h1 : Any)"></endpoint>
<signature id="Math.overlaps+8">Math.overlaps(**x0**: `Any`, **y0**: `Any`, **w0**: `Any`, **h0**: `Any`, **x1**: `Any`, **y1**: `Any`, **w1**: `Any`, **h1**: `Any`)
<a class="headerlink" href="#Math.overlaps+8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="sign(x : Any)"></endpoint>
<signature id="Math.sign">Math.sign(**x**: `Any`)
<a class="headerlink" href="#Math.sign" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="sign0(x : Any)"></endpoint>
<signature id="Math.sign0">Math.sign0(**x**: `Any`)
<a class="headerlink" href="#Math.sign0" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="atan2(y : Any, x : Any)"></endpoint>
<signature id="Math.atan2+2">Math.atan2(**y**: `Any`, **x**: `Any`)
<a class="headerlink" href="#Math.atan2+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="degrees(radians : Any)"></endpoint>
<signature id="Math.degrees">Math.degrees(**radians**: `Any`)
<a class="headerlink" href="#Math.degrees" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="radians(degrees : Any)"></endpoint>
<signature id="Math.radians">Math.radians(**degrees**: `Any`)
<a class="headerlink" href="#Math.radians" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="clamp(value : Any, a : Any, b : Any)"></endpoint>
<signature id="Math.clamp+3">Math.clamp(**value**: `Any`, **a**: `Any`, **b**: `Any`)
<a class="headerlink" href="#Math.clamp+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="min(a : Any, b : Any)"></endpoint>
<signature id="Math.min+2">Math.min(**a**: `Any`, **b**: `Any`)
<a class="headerlink" href="#Math.min+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="max(a : Any, b : Any)"></endpoint>
<signature id="Math.max+2">Math.max(**a**: `Any`, **b**: `Any`)
<a class="headerlink" href="#Math.max+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="floor_around_zero(a : Any)"></endpoint>
<signature id="Math.floor_around_zero">Math.floor_around_zero(**a**: `Any`)
<a class="headerlink" href="#Math.floor_around_zero" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="ceil_around_zero(a : Any)"></endpoint>
<signature id="Math.ceil_around_zero">Math.ceil_around_zero(**a**: `Any`)
<a class="headerlink" href="#Math.ceil_around_zero" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="fixed(value : Any)"></endpoint>
<signature id="Math.fixed">Math.fixed(**value**: `Any`)
<a class="headerlink" href="#Math.fixed" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="fixed(value : Any, precision : Any)"></endpoint>
<signature id="Math.fixed+2">Math.fixed(**value**: `Any`, **precision**: `Any`)
<a class="headerlink" href="#Math.fixed+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="angle_delta(a : Any, b : Any)"></endpoint>
<signature id="Math.angle_delta+2">Math.angle_delta(**a**: `Any`, **b**: `Any`)
<a class="headerlink" href="#Math.angle_delta+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="lerp(a : Any, b : Any, t : Any)"></endpoint>
<signature id="Math.lerp+3">Math.lerp(**a**: `Any`, **b**: `Any`, **t**: `Any`)
<a class="headerlink" href="#Math.lerp+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="lerp_angle(a : Any, b : Any, t : Any)"></endpoint>
<signature id="Math.lerp_angle+3">Math.lerp_angle(**a**: `Any`, **b**: `Any`, **t**: `Any`)
<a class="headerlink" href="#Math.lerp_angle+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="weighted_avg(value : Any, target : Any, slowness : Any)"></endpoint>
<signature id="Math.weighted_avg+3">Math.weighted_avg(**value**: `Any`, **target**: `Any`, **slowness**: `Any`)
<a class="headerlink" href="#Math.weighted_avg+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="within_range(value : Any, start_range : Any, end_range : Any)"></endpoint>
<signature id="Math.within_range+3">Math.within_range(**value**: `Any`, **start_range**: `Any`, **end_range**: `Any`)
<a class="headerlink" href="#Math.within_range+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="wrap_angle(degrees : Any)"></endpoint>
<signature id="Math.wrap_angle">Math.wrap_angle(**degrees**: `Any`)
<a class="headerlink" href="#Math.wrap_angle" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="wrap_angle(degrees : Any, lower : Any, upper : Any)"></endpoint>
<signature id="Math.wrap_angle+3">Math.wrap_angle(**degrees**: `Any`, **lower**: `Any`, **upper**: `Any`)
<a class="headerlink" href="#Math.wrap_angle+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="wrap_radians(radians : Any, lower : Any, upper : Any)"></endpoint>
<signature id="Math.wrap_radians+3">Math.wrap_radians(**radians**: `Any`, **lower**: `Any`, **upper**: `Any`)
<a class="headerlink" href="#Math.wrap_radians+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="nearest_power_of_two(value : Any)"></endpoint>
<signature id="Math.nearest_power_of_two">Math.nearest_power_of_two(**value**: `Any`)
<a class="headerlink" href="#Math.nearest_power_of_two" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="map_linear(value : Any, a1 : Any, a2 : Any, b1 : Any, b2 : Any)"></endpoint>
<signature id="Math.map_linear+5">Math.map_linear(**value**: `Any`, **a1**: `Any`, **a2**: `Any`, **b1**: `Any`, **b2**: `Any`)
<a class="headerlink" href="#Math.map_linear+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="smoothstep(x : Any, min : Any, max : Any)"></endpoint>
<signature id="Math.smoothstep+3">Math.smoothstep(**x**: `Any`, **min**: `Any`, **max**: `Any`)
<a class="headerlink" href="#Math.smoothstep+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="smootherstep(x : Any, min : Any, max : Any)"></endpoint>
<signature id="Math.smootherstep+3">Math.smootherstep(**x**: `Any`, **min**: `Any`, **max**: `Any`)
<a class="headerlink" href="#Math.smootherstep+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="random_point_in_unit_circle(rng : Any)"></endpoint>
<signature id="Math.random_point_in_unit_circle">Math.random_point_in_unit_circle(**rng**: `Any`)
<a class="headerlink" href="#Math.random_point_in_unit_circle" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

