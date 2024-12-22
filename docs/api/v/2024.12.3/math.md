#![](../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2024.12.3`)  


---

## `luxe: math` module

- [Math](#math)   

---

### Math
`:::js import "luxe: math" for Math`
> Utility class with static math functions.

- [add](#Math.add+2)(**a**: `Vec`, **b**: `Vec`)
- [add2D](#Math.add2D+2)(**a**: `Vec`, **b**: `Vec`)
- [add_to](#Math.add_to+2)(**a**: `Vec`, **b**: `Vec`)
- [add2D_to](#Math.add2D_to+2)(**a**: `Vec`, **b**: `Vec`)
- [sub](#Math.sub+2)(**a**: `Vec`, **b**: `Vec`)
- [sub2D](#Math.sub2D+2)(**a**: `Vec`, **b**: `Vec`)
- [sub_to](#Math.sub_to+2)(**a**: `Vec`, **b**: `Vec`)
- [sub2D_to](#Math.sub2D_to+2)(**a**: `Vec`, **b**: `Vec`)
- [mults](#Math.mults+2)(**a**: `Vec`, **b**: `Num`)
- [mult](#Math.mult+2)(**a**: `Vec`, **b**: `Vec`)
- [mult2D](#Math.mult2D+2)(**a**: `Vec`, **b**: `Vec`)
- [mult_to](#Math.mult_to+2)(**a**: `Vec`, **b**: `Vec`)
- [mults_to](#Math.mults_to+2)(**a**: `Vec`, **b**: `Num`)
- [mult2D_to](#Math.mult2D_to+2)(**a**: `Vec`, **b**: `Vec`)
- [scale](#Math.scale+2)(**a**: `Vec`, **s**: `Num`)
- [scale2D](#Math.scale2D+2)(**a**: `Vec`, **s**: `Num`)
- [scale_to](#Math.scale_to+2)(**a**: `Vec`, **s**: `Num`)
- [scale2D_to](#Math.scale2D_to+2)(**a**: `Vec`, **s**: `Num`)
- [divide](#Math.divide+2)(**a**: `Vec`, **b**: `Vec`)
- [divide_to](#Math.divide_to+2)(**vec**: `Vec`, **other**: `Vec`)
- [div](#Math.div+2)(**a**: `Vec`, **s**: `Num`)
- [div2D](#Math.div2D+2)(**a**: `Vec`, **s**: `Num`)
- [div_to](#Math.div_to+2)(**a**: `Vec`, **s**: `Num`)
- [div2D_to](#Math.div2D_to+2)(**a**: `Vec`, **s**: `Num`)
- [equal](#Math.equal+2)(**a**: `Vec`, **b**: `Vec`)
- [length](#Math.length+2)(**x**: `Num`, **y**: `Num`)
- [length](#Math.length+3)(**x**: `Num`, **y**: `Num`, **z**: `Num`)
- [length](#Math.length)(**vec**: `Vec`)
- [length2D](#Math.length2D)(**vec**: `Vec`)
- [length_sq](#Math.length_sq+2)(**x**: `Num`, **y**: `Num`)
- [length_sq](#Math.length_sq+3)(**x**: `Num`, **y**: `Num`, **z**: `Num`)
- [length_sq](#Math.length_sq)(**vec**: `Vec`)
- [length_sq2D](#Math.length_sq2D)(**vec**: `Vec`)
- [dot](#Math.dot+6)(**x**: `Num`, **y**: `Num`, **z**: `Num`, **other_x**: `Num`, **other_y**: `Num`, **other_z**: `Num`)
- [dot](#Math.dot+4)(**x**: `Num`, **y**: `Num`, **other_x**: `Num`, **other_y**: `Num`)
- [dot](#Math.dot+2)(**vec**: `Vec`, **other**: `Vec`)
- [dot2D](#Math.dot2D+2)(**vec**: `Vec`, **other**: `Vec`)
- [cross](#Math.cross+2)(**a**: `Vec`, **b**: `Vec`)
- [angle](#Math.angle+2)(**from**: `Vec`, **to**: `Vec`)
- [angle](#Math.angle+3)(**v1**: `Vec`, **v2**: `Vec`, **up**: `Vec`)
- [angle2D](#Math.angle2D+2)(**from**: `Vec`, **to**: `Vec`)
- [angle2D](#Math.angle2D+4)(**from_x**: `Num`, **from_y**: `Num`, **to_x**: `Num`, **to_y**: `Num`)
- [normalize2D](#Math.normalize2D)(**vec**: `Vec`)
- [normalized](#Math.normalized)(**vec**: `Vec`)
- [normalized2D](#Math.normalized2D)(**vec**: `Vec`)
- [normalize](#Math.normalize)(**vec**: `Vec`)
- [dist](#Math.dist+6)(**x**: `Num`, **y**: `Num`, **z**: `Num`, **other_x**: `Num`, **other_y**: `Num`, **other_z**: `Num`)
- [dist](#Math.dist+2)(**vec**: `Vec`, **other**: `Vec`)
- [dist2D](#Math.dist2D+2)(**vec**: `Vec`, **other**: `Vec`)
- [dist2D](#Math.dist2D+4)(**x**: `Num`, **y**: `Num`, **other_x**: `Num`, **other_y**: `Num`)
- [dir2D](#Math.dir2D+2)(**pos**: `Vec`, **target**: `Vec`)
- [dir](#Math.dir+2)(**pos**: `Vec`, **target**: `Vec`)
- [rotate](#Math.rotate+3)(**vec**: `Vec`, **axis**: `Vec`, **angle**: `Num`)
- [rotate_by_quat](#Math.rotate_by_quat+2)(**vec**: `Vec`, **quat**: `Float4`)
- [quat_from_euler](#Math.quat_from_euler)(**vec**: `Vec`)
- [rotate](#Math.rotate+4)(**vec**: `Vec`, **ox**: `Num`, **oy**: `Num`, **angle**: `Num`)
- [ray_intersect_plane](#Math.ray_intersect_plane+12)(**plane_x**: `Num`, **plane_y**: `Num`, **plane_z**: `Num`, **normal_x**: `Num`, **normal_y**: `Num`, **normal_z**: `Num`, **ray_x**: `Num`, **ray_y**: `Num`, **ray_z**: `Num`, **ray_dir_x**: `Num`, **ray_dir_y**: `Num`, **ray_dir_z**: `Num`)
- [closest_point_on_plane](#Math.closest_point_on_plane+9)(**plane_x**: `Num`, **plane_y**: `Num`, **plane_z**: `Num`, **normal_x**: `Num`, **normal_y**: `Num`, **normal_z**: `Num`, **point_x**: `Num`, **point_y**: `Num`, **point_z**: `Num`)
- [closest_point_on_line](#Math.closest_point_on_line+9)(**line_x**: `Num`, **line_y**: `Num`, **line_z**: `Num`, **line_end_x**: `Num`, **line_end_y**: `Num`, **line_end_z**: `Num`, **point_x**: `Num`, **point_y**: `Num`, **point_z**: `Num`)
- [closest_point_on_line](#Math.closest_point_on_line+3)(**line**: `Vec`, **line_end**: `Vec`, **point**: `Vec`)
- [in_rect](#Math.in_rect+6)(**x**: `Num`, **y**: `Num`, **rx**: `Num`, **ry**: `Num`, **rw**: `Num`, **rh**: `Num`)
- [wrap](#Math.wrap+2)(**value**: `Num`, **modulus**: `Num`)
- [overlaps](#Math.overlaps+8)(**x0**: `Num`, **y0**: `Num`, **w0**: `Num`, **h0**: `Num`, **x1**: `Num`, **y1**: `Num`, **w1**: `Num`, **h1**: `Num`)
- [sign](#Math.sign)(**x**: `Num`)
- [sign0](#Math.sign0)(**x**: `Num`)
- [atan2](#Math.atan2+2)(**y**: `Num`, **x**: `Num`)
- [degrees](#Math.degrees)(**radians**: `Num`)
- [radians](#Math.radians)(**degrees**: `Num`)
- [clamp](#Math.clamp+3)(**value**: `Num`, **a**: `Num`, **b**: `Num`)
- [min](#Math.min+2)(**a**: `Num`, **b**: `Num`)
- [max](#Math.max+2)(**a**: `Num`, **b**: `Num`)
- [floor_around_zero](#Math.floor_around_zero)(**a**: `Num`)
- [ceil_around_zero](#Math.ceil_around_zero)(**a**: `Num`)
- [fixed](#Math.fixed)(**value**: `Num`)
- [fixed](#Math.fixed+2)(**value**: `Num`, **precision**: `Num`)
- [angle_delta](#Math.angle_delta+2)(**from**: `Num`, **to**: `Num`)
- [lerp2D](#Math.lerp2D+3)(**a**: `Vec`, **b**: `Vec`, **t**: `Num`)
- [lerp3D](#Math.lerp3D+3)(**a**: `Vec`, **b**: `Vec`, **t**: `Num`)
- [smooth_t](#Math.smooth_t+2)(**t**: `Num`, **smoothness**: `Num`)
- [smoother_t](#Math.smoother_t+2)(**t**: `Num`, **smoothness**: `Num`)
- [lerp](#Math.lerp+3)(**a**: `Num`, **b**: `Num`, **t**: `Num`)
- [lerp_angle](#Math.lerp_angle+3)(**a**: `Num`, **b**: `Num`, **t**: `Num`)
- [weighted_avg](#Math.weighted_avg+3)(**value**: `Num`, **target**: `Num`, **slowness**: `Num`)
- [within_range](#Math.within_range+3)(**value**: `Num`, **start_range**: `Num`, **end_range**: `Num`)
- [approx](#Math.approx+2)(**one**: `Num`, **other**: `Num`)
- [approx](#Math.approx+3)(**one**: `Num`, **other**: `Num`, **epsilon**: `Num`)
- [wrap_angle](#Math.wrap_angle)(**degrees**: `Num`)
- [wrap_angle](#Math.wrap_angle+3)(**degrees**: `Num`, **lower**: `Num`, **upper**: `Num`)
- [wrap_radians](#Math.wrap_radians+3)(**radians**: `Num`, **lower**: `Num`, **upper**: `Num`)
- [nearest_power_of_two](#Math.nearest_power_of_two)(**value**: `Num`)
- [map_linear](#Math.map_linear+5)(**value**: `Num`, **a1**: `Num`, **a2**: `Num`, **b1**: `Num`, **b2**: `Num`)
- [smoothstep](#Math.smoothstep+3)(**x**: `Num`, **min**: `Num`, **max**: `Num`)
- [smootherstep](#Math.smootherstep+3)(**x**: `Num`, **min**: `Num`, **max**: `Num`)
- [smoothstepx](#Math.smoothstepx+3)(**x**: `Num`, **round**: `Num`, **steep**: `Num`)
- [random_point_in_unit_circle](#Math.random_point_in_unit_circle)(**rng**: `Random`)
- [slerp](#Math.slerp+3)(**a**: `Quat`, **b**: `Quat`, **t**: `Num`)

<hr/>
<endpoint module="luxe: math" class="Math" signature="add(a : Vec, b : Vec)"></endpoint>
<signature id="Math.add+2">Math.add(**a**: `Vec`, **b**: `Vec`)
<a class="headerlink" href="#Math.add+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Add two 3D vectors together componentwise, returning the result   

<endpoint module="luxe: math" class="Math" signature="add2D(a : Vec, b : Vec)"></endpoint>
<signature id="Math.add2D+2">Math.add2D(**a**: `Vec`, **b**: `Vec`)
<a class="headerlink" href="#Math.add2D+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Add two vector2s together componentwise, returning the result   

<endpoint module="luxe: math" class="Math" signature="add_to(a : Vec, b : Vec)"></endpoint>
<signature id="Math.add_to+2">Math.add_to(**a**: `Vec`, **b**: `Vec`)
<a class="headerlink" href="#Math.add_to+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Add two 3D vectors together componentwise, updating the first vector   

<endpoint module="luxe: math" class="Math" signature="add2D_to(a : Vec, b : Vec)"></endpoint>
<signature id="Math.add2D_to+2">Math.add2D_to(**a**: `Vec`, **b**: `Vec`)
<a class="headerlink" href="#Math.add2D_to+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Add two 2D vectors together componentwise, updating the first vector   

<endpoint module="luxe: math" class="Math" signature="sub(a : Vec, b : Vec)"></endpoint>
<signature id="Math.sub+2">Math.sub(**a**: `Vec`, **b**: `Vec`)
<a class="headerlink" href="#Math.sub+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Subtract two 3D vectors together componentwise, returning the result   

<endpoint module="luxe: math" class="Math" signature="sub2D(a : Vec, b : Vec)"></endpoint>
<signature id="Math.sub2D+2">Math.sub2D(**a**: `Vec`, **b**: `Vec`)
<a class="headerlink" href="#Math.sub2D+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Subtract two 2D vectors together componentwise, returning the result   

<endpoint module="luxe: math" class="Math" signature="sub_to(a : Vec, b : Vec)"></endpoint>
<signature id="Math.sub_to+2">Math.sub_to(**a**: `Vec`, **b**: `Vec`)
<a class="headerlink" href="#Math.sub_to+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Subtract two 3D vectors together componentwise, updating the first vector   

<endpoint module="luxe: math" class="Math" signature="sub2D_to(a : Vec, b : Vec)"></endpoint>
<signature id="Math.sub2D_to+2">Math.sub2D_to(**a**: `Vec`, **b**: `Vec`)
<a class="headerlink" href="#Math.sub2D_to+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Subtract two 2D vectors together componentwise, updating the first vector   

<endpoint module="luxe: math" class="Math" signature="mults(a : Vec, b : Num)"></endpoint>
<signature id="Math.mults+2">Math.mults(**a**: `Vec`, **b**: `Num`)
<a class="headerlink" href="#Math.mults+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Multiply a 3D vector by a scalar, returning the result   

<endpoint module="luxe: math" class="Math" signature="mult(a : Vec, b : Vec)"></endpoint>
<signature id="Math.mult+2">Math.mult(**a**: `Vec`, **b**: `Vec`)
<a class="headerlink" href="#Math.mult+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Multiply two 3D vectors together componentwise, returning the result   

<endpoint module="luxe: math" class="Math" signature="mult2D(a : Vec, b : Vec)"></endpoint>
<signature id="Math.mult2D+2">Math.mult2D(**a**: `Vec`, **b**: `Vec`)
<a class="headerlink" href="#Math.mult2D+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Multiply two 2D vectors together componentwise, returning the result   

<endpoint module="luxe: math" class="Math" signature="mult_to(a : Vec, b : Vec)"></endpoint>
<signature id="Math.mult_to+2">Math.mult_to(**a**: `Vec`, **b**: `Vec`)
<a class="headerlink" href="#Math.mult_to+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Multiply two 3D vectors together componentwise, updating the first vector   

<endpoint module="luxe: math" class="Math" signature="mults_to(a : Vec, b : Num)"></endpoint>
<signature id="Math.mults_to+2">Math.mults_to(**a**: `Vec`, **b**: `Num`)
<a class="headerlink" href="#Math.mults_to+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Multiply a 3D vector by a scalar, updating the vector   

<endpoint module="luxe: math" class="Math" signature="mult2D_to(a : Vec, b : Vec)"></endpoint>
<signature id="Math.mult2D_to+2">Math.mult2D_to(**a**: `Vec`, **b**: `Vec`)
<a class="headerlink" href="#Math.mult2D_to+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Multiply two 2D vectors together componentwise, updating the first vector   

<endpoint module="luxe: math" class="Math" signature="scale(a : Vec, s : Num)"></endpoint>
<signature id="Math.scale+2">Math.scale(**a**: `Vec`, **s**: `Num`)
<a class="headerlink" href="#Math.scale+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Multiply a 3D vector by a scalar, returning the result   

<endpoint module="luxe: math" class="Math" signature="scale2D(a : Vec, s : Num)"></endpoint>
<signature id="Math.scale2D+2">Math.scale2D(**a**: `Vec`, **s**: `Num`)
<a class="headerlink" href="#Math.scale2D+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Multiply a 2D vector by a scalar, returning the result   

<endpoint module="luxe: math" class="Math" signature="scale_to(a : Vec, s : Num)"></endpoint>
<signature id="Math.scale_to+2">Math.scale_to(**a**: `Vec`, **s**: `Num`)
<a class="headerlink" href="#Math.scale_to+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Multiply a 3D vector by a scalar, updating the vector   

<endpoint module="luxe: math" class="Math" signature="scale2D_to(a : Vec, s : Num)"></endpoint>
<signature id="Math.scale2D_to+2">Math.scale2D_to(**a**: `Vec`, **s**: `Num`)
<a class="headerlink" href="#Math.scale2D_to+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Multiply a 2D vector by a scalar, updating the vector   

<endpoint module="luxe: math" class="Math" signature="divide(a : Vec, b : Vec)"></endpoint>
<signature id="Math.divide+2">Math.divide(**a**: `Vec`, **b**: `Vec`)
<a class="headerlink" href="#Math.divide+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Divide a 3D vector by another, returning the result   

<endpoint module="luxe: math" class="Math" signature="divide_to(vec : Vec, other : Vec)"></endpoint>
<signature id="Math.divide_to+2">Math.divide_to(**vec**: `Vec`, **other**: `Vec`)
<a class="headerlink" href="#Math.divide_to+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Divide a 3D vector by another, updating the vector   

<endpoint module="luxe: math" class="Math" signature="div(a : Vec, s : Num)"></endpoint>
<signature id="Math.div+2">Math.div(**a**: `Vec`, **s**: `Num`)
<a class="headerlink" href="#Math.div+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Divide a 3D vector by a scalar, returning the result   

<endpoint module="luxe: math" class="Math" signature="div2D(a : Vec, s : Num)"></endpoint>
<signature id="Math.div2D+2">Math.div2D(**a**: `Vec`, **s**: `Num`)
<a class="headerlink" href="#Math.div2D+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Divide a 2D vector by a scalar, returning the result   

<endpoint module="luxe: math" class="Math" signature="div_to(a : Vec, s : Num)"></endpoint>
<signature id="Math.div_to+2">Math.div_to(**a**: `Vec`, **s**: `Num`)
<a class="headerlink" href="#Math.div_to+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Divide a 3D vector by a scalar, updating the vector   

<endpoint module="luxe: math" class="Math" signature="div2D_to(a : Vec, s : Num)"></endpoint>
<signature id="Math.div2D_to+2">Math.div2D_to(**a**: `Vec`, **s**: `Num`)
<a class="headerlink" href="#Math.div2D_to+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Divide a 2D vector by a scalar, updating the vector   

<endpoint module="luxe: math" class="Math" signature="equal(a : Vec, b : Vec)"></endpoint>
<signature id="Math.equal+2">Math.equal(**a**: `Vec`, **b**: `Vec`)
<a class="headerlink" href="#Math.equal+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Checks if two vectors are equal. Vectors of different dimensions (e.g. 2D and 3D) are considered unequal   

<endpoint module="luxe: math" class="Math" signature="length(x : Num, y : Num)"></endpoint>
<signature id="Math.length+2">Math.length(**x**: `Num`, **y**: `Num`)
<a class="headerlink" href="#Math.length+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Length of a 2d vector.   

<endpoint module="luxe: math" class="Math" signature="length(x : Num, y : Num, z : Num)"></endpoint>
<signature id="Math.length+3">Math.length(**x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Math.length+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Length of a 3d vector.   

<endpoint module="luxe: math" class="Math" signature="length(vec : Vec)"></endpoint>
<signature id="Math.length">Math.length(**vec**: `Vec`)
<a class="headerlink" href="#Math.length" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Length of a 3d vector.   

<endpoint module="luxe: math" class="Math" signature="length2D(vec : Vec)"></endpoint>
<signature id="Math.length2D">Math.length2D(**vec**: `Vec`)
<a class="headerlink" href="#Math.length2D" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Length of a 2d vector.   

<endpoint module="luxe: math" class="Math" signature="length_sq(x : Num, y : Num)"></endpoint>
<signature id="Math.length_sq+2">Math.length_sq(**x**: `Num`, **y**: `Num`)
<a class="headerlink" href="#Math.length_sq+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Squared length of a 2d vector (slightly cheaper than length).   

<endpoint module="luxe: math" class="Math" signature="length_sq(x : Num, y : Num, z : Num)"></endpoint>
<signature id="Math.length_sq+3">Math.length_sq(**x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Math.length_sq+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Squared length of a 3d vector (slightly cheaper than length).   

<endpoint module="luxe: math" class="Math" signature="length_sq(vec : Vec)"></endpoint>
<signature id="Math.length_sq">Math.length_sq(**vec**: `Vec`)
<a class="headerlink" href="#Math.length_sq" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Squared length of a 3d vector.   

<endpoint module="luxe: math" class="Math" signature="length_sq2D(vec : Vec)"></endpoint>
<signature id="Math.length_sq2D">Math.length_sq2D(**vec**: `Vec`)
<a class="headerlink" href="#Math.length_sq2D" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Squared length of a 2d vector.   

<endpoint module="luxe: math" class="Math" signature="dot(x : Num, y : Num, z : Num, other_x : Num, other_y : Num, other_z : Num)"></endpoint>
<signature id="Math.dot+6">Math.dot(**x**: `Num`, **y**: `Num`, **z**: `Num`, **other_x**: `Num`, **other_y**: `Num`, **other_z**: `Num`)
<a class="headerlink" href="#Math.dot+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Dot product (or scalar product) of two 3d vectors.   

<endpoint module="luxe: math" class="Math" signature="dot(x : Num, y : Num, other_x : Num, other_y : Num)"></endpoint>
<signature id="Math.dot+4">Math.dot(**x**: `Num`, **y**: `Num`, **other_x**: `Num`, **other_y**: `Num`)
<a class="headerlink" href="#Math.dot+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Dot product (or scalar product) of two 2d vectors.   

<endpoint module="luxe: math" class="Math" signature="dot(vec : Vec, other : Vec)"></endpoint>
<signature id="Math.dot+2">Math.dot(**vec**: `Vec`, **other**: `Vec`)
<a class="headerlink" href="#Math.dot+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Dot product (or scalar product) of two 3d vectors.   

<endpoint module="luxe: math" class="Math" signature="dot2D(vec : Vec, other : Vec)"></endpoint>
<signature id="Math.dot2D+2">Math.dot2D(**vec**: `Vec`, **other**: `Vec`)
<a class="headerlink" href="#Math.dot2D+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Dot product (or scalar product) of two 2d vectors.   

<endpoint module="luxe: math" class="Math" signature="cross(a : Vec, b : Vec)"></endpoint>
<signature id="Math.cross+2">Math.cross(**a**: `Vec`, **b**: `Vec`)
<a class="headerlink" href="#Math.cross+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Cross product of two 3d vectors. 
> Result will always be orthogonal to both input vectors (and [0, 0, 0] if the arguments are parallel)   

<endpoint module="luxe: math" class="Math" signature="angle(from : Vec, to : Vec)"></endpoint>
<signature id="Math.angle+2">Math.angle(**from**: `Vec`, **to**: `Vec`)
<a class="headerlink" href="#Math.angle+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Unsigned angle between two 3d vectors.   

<endpoint module="luxe: math" class="Math" signature="angle(v1 : Vec, v2 : Vec, up : Vec)"></endpoint>
<signature id="Math.angle+3">Math.angle(**v1**: `Vec`, **v2**: `Vec`, **up**: `Vec`)
<a class="headerlink" href="#Math.angle+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Signed angle between two 3d vectors.   

<endpoint module="luxe: math" class="Math" signature="angle2D(from : Vec, to : Vec)"></endpoint>
<signature id="Math.angle2D+2">Math.angle2D(**from**: `Vec`, **to**: `Vec`)
<a class="headerlink" href="#Math.angle2D+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Signed angle between two 2d vectors.   

<endpoint module="luxe: math" class="Math" signature="angle2D(from_x : Num, from_y : Num, to_x : Num, to_y : Num)"></endpoint>
<signature id="Math.angle2D+4">Math.angle2D(**from_x**: `Num`, **from_y**: `Num`, **to_x**: `Num`, **to_y**: `Num`)
<a class="headerlink" href="#Math.angle2D+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Signed angle between two 2d vectors.   

<endpoint module="luxe: math" class="Math" signature="normalize2D(vec : Vec)"></endpoint>
<signature id="Math.normalize2D">Math.normalize2D(**vec**: `Vec`)
<a class="headerlink" href="#Math.normalize2D" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Normalize 2d vector. Changes input vector and doesnt return anything. 0 length vectors remain untouched.   

<endpoint module="luxe: math" class="Math" signature="normalized(vec : Vec)"></endpoint>
<signature id="Math.normalized">Math.normalized(**vec**: `Vec`)
<a class="headerlink" href="#Math.normalized" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Normalize 3d vector. Returns the result.   

<endpoint module="luxe: math" class="Math" signature="normalized2D(vec : Vec)"></endpoint>
<signature id="Math.normalized2D">Math.normalized2D(**vec**: `Vec`)
<a class="headerlink" href="#Math.normalized2D" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Normalize 2d vector. Returns the result.   

<endpoint module="luxe: math" class="Math" signature="normalize(vec : Vec)"></endpoint>
<signature id="Math.normalize">Math.normalize(**vec**: `Vec`)
<a class="headerlink" href="#Math.normalize" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Normalize 3d vector. Changes input vector and doesnt return anything. 0 length vectors remain untouched.   

<endpoint module="luxe: math" class="Math" signature="dist(x : Num, y : Num, z : Num, other_x : Num, other_y : Num, other_z : Num)"></endpoint>
<signature id="Math.dist+6">Math.dist(**x**: `Num`, **y**: `Num`, **z**: `Num`, **other_x**: `Num`, **other_y**: `Num`, **other_z**: `Num`)
<a class="headerlink" href="#Math.dist+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Distance between two 3d vectors.   

<endpoint module="luxe: math" class="Math" signature="dist(vec : Vec, other : Vec)"></endpoint>
<signature id="Math.dist+2">Math.dist(**vec**: `Vec`, **other**: `Vec`)
<a class="headerlink" href="#Math.dist+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Distance between two 3d vectors.   

<endpoint module="luxe: math" class="Math" signature="dist2D(vec : Vec, other : Vec)"></endpoint>
<signature id="Math.dist2D+2">Math.dist2D(**vec**: `Vec`, **other**: `Vec`)
<a class="headerlink" href="#Math.dist2D+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Distance between two 2d vectors.   

<endpoint module="luxe: math" class="Math" signature="dist2D(x : Num, y : Num, other_x : Num, other_y : Num)"></endpoint>
<signature id="Math.dist2D+4">Math.dist2D(**x**: `Num`, **y**: `Num`, **other_x**: `Num`, **other_y**: `Num`)
<a class="headerlink" href="#Math.dist2D+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Distance between two 2d vectors.   

<endpoint module="luxe: math" class="Math" signature="dir2D(pos : Vec, target : Vec)"></endpoint>
<signature id="Math.dir2D+2">Math.dir2D(**pos**: `Vec`, **target**: `Vec`)
<a class="headerlink" href="#Math.dir2D+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Directional vector (length 1 unless the arguments are the same) between two 2d vectors.   

<endpoint module="luxe: math" class="Math" signature="dir(pos : Vec, target : Vec)"></endpoint>
<signature id="Math.dir+2">Math.dir(**pos**: `Vec`, **target**: `Vec`)
<a class="headerlink" href="#Math.dir+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Directional vector (length 1 unless the arguments are the same) between two 3d vectors.   

<endpoint module="luxe: math" class="Math" signature="rotate(vec : Vec, axis : Vec, angle : Num)"></endpoint>
<signature id="Math.rotate+3">Math.rotate(**vec**: `Vec`, **axis**: `Vec`, **angle**: `Num`)
<a class="headerlink" href="#Math.rotate+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Rotate a 3d vector around the given axis by angle degrees   

<endpoint module="luxe: math" class="Math" signature="rotate_by_quat(vec : Vec, quat : Float4)"></endpoint>
<signature id="Math.rotate_by_quat+2">Math.rotate_by_quat(**vec**: `Vec`, **quat**: `Float4`)
<a class="headerlink" href="#Math.rotate_by_quat+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Rotate a 3d vector using the given quaternion   

<endpoint module="luxe: math" class="Math" signature="quat_from_euler(vec : Vec)"></endpoint>
<signature id="Math.quat_from_euler">Math.quat_from_euler(**vec**: `Vec`)
<a class="headerlink" href="#Math.quat_from_euler" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Float4`
> Create a quaternion from float3 euler (radians)   

<endpoint module="luxe: math" class="Math" signature="rotate(vec : Vec, ox : Num, oy : Num, angle : Num)"></endpoint>
<signature id="Math.rotate+4">Math.rotate(**vec**: `Vec`, **ox**: `Num`, **oy**: `Num`, **angle**: `Num`)
<a class="headerlink" href="#Math.rotate+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Rotate 2d vector around another 2d vector. This rotates the input vector and doesnt return anything.   

<endpoint module="luxe: math" class="Math" signature="ray_intersect_plane(plane_x : Num, plane_y : Num, plane_z : Num, normal_x : Num, normal_y : Num, normal_z : Num, ray_x : Num, ray_y : Num, ray_z : Num, ray_dir_x : Num, ray_dir_y : Num, ray_dir_z : Num)"></endpoint>
<signature id="Math.ray_intersect_plane+12">Math.ray_intersect_plane(**plane_x**: `Num`, **plane_y**: `Num`, **plane_z**: `Num`, **normal_x**: `Num`, **normal_y**: `Num`, **normal_z**: `Num`, **ray_x**: `Num`, **ray_y**: `Num`, **ray_z**: `Num`, **ray_dir_x**: `Num`, **ray_dir_y**: `Num`, **ray_dir_z**: `Num`)
<a class="headerlink" href="#Math.ray_intersect_plane+12" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Intersection point between an infinitely long ray and a infinitely big plane.
> Returns `null` if parallel.   

<endpoint module="luxe: math" class="Math" signature="closest_point_on_plane(plane_x : Num, plane_y : Num, plane_z : Num, normal_x : Num, normal_y : Num, normal_z : Num, point_x : Num, point_y : Num, point_z : Num)"></endpoint>
<signature id="Math.closest_point_on_plane+9">Math.closest_point_on_plane(**plane_x**: `Num`, **plane_y**: `Num`, **plane_z**: `Num`, **normal_x**: `Num`, **normal_y**: `Num`, **normal_z**: `Num`, **point_x**: `Num`, **point_y**: `Num`, **point_z**: `Num`)
<a class="headerlink" href="#Math.closest_point_on_plane+9" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Closest point on an infinite plane to a point.   

<endpoint module="luxe: math" class="Math" signature="closest_point_on_line(line_x : Num, line_y : Num, line_z : Num, line_end_x : Num, line_end_y : Num, line_end_z : Num, point_x : Num, point_y : Num, point_z : Num)"></endpoint>
<signature id="Math.closest_point_on_line+9">Math.closest_point_on_line(**line_x**: `Num`, **line_y**: `Num`, **line_z**: `Num`, **line_end_x**: `Num`, **line_end_y**: `Num`, **line_end_z**: `Num`, **point_x**: `Num`, **point_y**: `Num`, **point_z**: `Num`)
<a class="headerlink" href="#Math.closest_point_on_line+9" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Closest point on an infinite line to a point.
> The progress from line start to line end in 4th component of return value.
> Line is constructed by 2 points on the line, 
> but the closest point can also be before the start of after the end 
> (in that case the 4th component of the return value wont be in the 0-1 range).   

<endpoint module="luxe: math" class="Math" signature="closest_point_on_line(line : Vec, line_end : Vec, point : Vec)"></endpoint>
<signature id="Math.closest_point_on_line+3">Math.closest_point_on_line(**line**: `Vec`, **line_end**: `Vec`, **point**: `Vec`)
<a class="headerlink" href="#Math.closest_point_on_line+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Closest point on an infinite line to a point.
> The progress from line start to line end in 4th component of return value.
> Line is constructed by 2 points on the line, 
> but the closest point can also be before the start of after the end 
> (in that case the 4th component of the return value wont be in the 0-1 range).   

<endpoint module="luxe: math" class="Math" signature="in_rect(x : Num, y : Num, rx : Num, ry : Num, rw : Num, rh : Num)"></endpoint>
<signature id="Math.in_rect+6">Math.in_rect(**x**: `Num`, **y**: `Num`, **rx**: `Num`, **ry**: `Num`, **rw**: `Num`, **rh**: `Num`)
<a class="headerlink" href="#Math.in_rect+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Checks if a 2d point is inside a rectangle.
> Only works for positive rectangle sizes.   

<endpoint module="luxe: math" class="Math" signature="wrap(value : Num, modulus : Num)"></endpoint>
<signature id="Math.wrap+2">Math.wrap(**value**: `Num`, **modulus**: `Num`)
<a class="headerlink" href="#Math.wrap+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="overlaps(x0 : Num, y0 : Num, w0 : Num, h0 : Num, x1 : Num, y1 : Num, w1 : Num, h1 : Num)"></endpoint>
<signature id="Math.overlaps+8">Math.overlaps(**x0**: `Num`, **y0**: `Num`, **w0**: `Num`, **h0**: `Num`, **x1**: `Num`, **y1**: `Num`, **w1**: `Num`, **h1**: `Num`)
<a class="headerlink" href="#Math.overlaps+8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Checks if two rectangles overlap.
> Only works for positive rectangle sizes.   

<endpoint module="luxe: math" class="Math" signature="sign(x : Num)"></endpoint>
<signature id="Math.sign">Math.sign(**x**: `Num`)
<a class="headerlink" href="#Math.sign" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> The sign of the number, expressed as a -1, 1 or 0, for negative and positive numbers, and zero.   

<endpoint module="luxe: math" class="Math" signature="sign0(x : Num)"></endpoint>
<signature id="Math.sign0">Math.sign0(**x**: `Num`)
<a class="headerlink" href="#Math.sign0" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> The sign of the number, expressed as a -1 0r 1, for negative and positive numbers, zero is positive.   

<endpoint module="luxe: math" class="Math" signature="atan2(y : Num, x : Num)"></endpoint>
<signature id="Math.atan2+2">Math.atan2(**y**: `Num`, **x**: `Num`)
<a class="headerlink" href="#Math.atan2+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> The arc tangent of `y` when divided by `x`, 
>     using the signs of the two numbers to determine the quadrant of the result. 
>     (equivalient to `y.atan(x)`)   

<endpoint module="luxe: math" class="Math" signature="degrees(radians : Num)"></endpoint>
<signature id="Math.degrees">Math.degrees(**radians**: `Num`)
<a class="headerlink" href="#Math.degrees" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Convert radians (0...2*PI) to degree (0...360).   

<endpoint module="luxe: math" class="Math" signature="radians(degrees : Num)"></endpoint>
<signature id="Math.radians">Math.radians(**degrees**: `Num`)
<a class="headerlink" href="#Math.radians" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Convert degree (0...360) to radians (0...2*PI).   

<endpoint module="luxe: math" class="Math" signature="clamp(value : Num, a : Num, b : Num)"></endpoint>
<signature id="Math.clamp+3">Math.clamp(**value**: `Num`, **a**: `Num`, **b**: `Num`)
<a class="headerlink" href="#Math.clamp+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Clamp `value` between `a` and `b` (result will never be smaller than a or bigger than b). 
>     Equivalent to `value.clamp(a, b)`.   

<endpoint module="luxe: math" class="Math" signature="min(a : Num, b : Num)"></endpoint>
<signature id="Math.min+2">Math.min(**a**: `Num`, **b**: `Num`)
<a class="headerlink" href="#Math.min+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> The smaller of two numbers. Eqivalent to `a.min(b)`.   

<endpoint module="luxe: math" class="Math" signature="max(a : Num, b : Num)"></endpoint>
<signature id="Math.max+2">Math.max(**a**: `Num`, **b**: `Num`)
<a class="headerlink" href="#Math.max+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> The larger of two numbers. Eqivalent to `a.max(b)`.   

<endpoint module="luxe: math" class="Math" signature="floor_around_zero(a : Num)"></endpoint>
<signature id="Math.floor_around_zero">Math.floor_around_zero(**a**: `Num`)
<a class="headerlink" href="#Math.floor_around_zero" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Round towards zero. (floor when positive, ceil when negative)   

<endpoint module="luxe: math" class="Math" signature="ceil_around_zero(a : Num)"></endpoint>
<signature id="Math.ceil_around_zero">Math.ceil_around_zero(**a**: `Num`)
<a class="headerlink" href="#Math.ceil_around_zero" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Round away from zero. (ceil when positive, floor when negative)   

<endpoint module="luxe: math" class="Math" signature="fixed(value : Num)"></endpoint>
<signature id="Math.fixed">Math.fixed(**value**: `Num`)
<a class="headerlink" href="#Math.fixed" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Round number to 3 digits after comma precision.   

<endpoint module="luxe: math" class="Math" signature="fixed(value : Num, precision : Num)"></endpoint>
<signature id="Math.fixed+2">Math.fixed(**value**: `Num`, **precision**: `Num`)
<a class="headerlink" href="#Math.fixed+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Round number to `precision` digits after comma precision.   

<endpoint module="luxe: math" class="Math" signature="angle_delta(from : Num, to : Num)"></endpoint>
<signature id="Math.angle_delta+2">Math.angle_delta(**from**: `Num`, **to**: `Num`)
<a class="headerlink" href="#Math.angle_delta+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Signed difference between two (degree) angles. Always in -180...180 range.   

<endpoint module="luxe: math" class="Math" signature="lerp2D(a : Vec, b : Vec, t : Num)"></endpoint>
<signature id="Math.lerp2D+3">Math.lerp2D(**a**: `Vec`, **b**: `Vec`, **t**: `Num`)
<a class="headerlink" href="#Math.lerp2D+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Linearly interpolate between two vectors.
> Returns `a` when `t` is `0` and `b` when `t` is `1`, with values inbetween interpolating inbetween.
> If `t` is outside 0-1 range, the output will be extrapolated.   

<endpoint module="luxe: math" class="Math" signature="lerp3D(a : Vec, b : Vec, t : Num)"></endpoint>
<signature id="Math.lerp3D+3">Math.lerp3D(**a**: `Vec`, **b**: `Vec`, **t**: `Num`)
<a class="headerlink" href="#Math.lerp3D+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Vec`
> Linearly interpolate between two vectors.
> Returns `a` when `t` is `0` and `b` when `t` is `1`, with values inbetween interpolating inbetween.
> If `t` is outside 0-1 range, the output will be extrapolated.   

<endpoint module="luxe: math" class="Math" signature="smooth_t(t : Num, smoothness : Num)"></endpoint>
<signature id="Math.smooth_t+2">Math.smooth_t(**t**: `Num`, **smoothness**: `Num`)
<a class="headerlink" href="#Math.smooth_t+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get a smooth time t for lerping, based on a smoothness value. e.g t = smooth_t(delta, 1.25). exponential decay   

<endpoint module="luxe: math" class="Math" signature="smoother_t(t : Num, smoothness : Num)"></endpoint>
<signature id="Math.smoother_t+2">Math.smoother_t(**t**: `Num`, **smoothness**: `Num`)
<a class="headerlink" href="#Math.smoother_t+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get a smooth time t for lerping, based on a smoothness value. e.g t = smoother_t(delta, 1.25). s curve like shape   

<endpoint module="luxe: math" class="Math" signature="lerp(a : Num, b : Num, t : Num)"></endpoint>
<signature id="Math.lerp+3">Math.lerp(**a**: `Num`, **b**: `Num`, **t**: `Num`)
<a class="headerlink" href="#Math.lerp+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Linearly interpolate between two numbers.
> Returns `a` when `t` is `0` and `b` when `t` is `1`, with values inbetween interpolating inbetween.
> If `t` is outside 0-1 range, the output will be extrapolated.   

<endpoint module="luxe: math" class="Math" signature="lerp_angle(a : Num, b : Num, t : Num)"></endpoint>
<signature id="Math.lerp_angle+3">Math.lerp_angle(**a**: `Num`, **b**: `Num`, **t**: `Num`)
<a class="headerlink" href="#Math.lerp_angle+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Interpolates between angles. Always in 0...360 range.   

<endpoint module="luxe: math" class="Math" signature="weighted_avg(value : Num, target : Num, slowness : Num)"></endpoint>
<signature id="Math.weighted_avg+3">Math.weighted_avg(**value**: `Num`, **target**: `Num`, **slowness**: `Num`)
<a class="headerlink" href="#Math.weighted_avg+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="within_range(value : Num, start_range : Num, end_range : Num)"></endpoint>
<signature id="Math.within_range+3">Math.within_range(**value**: `Num`, **start_range**: `Num`, **end_range**: `Num`)
<a class="headerlink" href="#Math.within_range+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Checks whether `value` is inbetween `start_range` and `end_range` (inclusive).   

<endpoint module="luxe: math" class="Math" signature="approx(one : Num, other : Num)"></endpoint>
<signature id="Math.approx+2">Math.approx(**one**: `Num`, **other**: `Num`)
<a class="headerlink" href="#Math.approx+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Checks whether two values are approximately the same (with a max difference of 0.001).   

<endpoint module="luxe: math" class="Math" signature="approx(one : Num, other : Num, epsilon : Num)"></endpoint>
<signature id="Math.approx+3">Math.approx(**one**: `Num`, **other**: `Num`, **epsilon**: `Num`)
<a class="headerlink" href="#Math.approx+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Checks whether two values are approximately the same (with a max difference of `epsilon`).   

<endpoint module="luxe: math" class="Math" signature="wrap_angle(degrees : Num)"></endpoint>
<signature id="Math.wrap_angle">Math.wrap_angle(**degrees**: `Num`)
<a class="headerlink" href="#Math.wrap_angle" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Bring angle into 0...360 degree space.   

<endpoint module="luxe: math" class="Math" signature="wrap_angle(degrees : Num, lower : Num, upper : Num)"></endpoint>
<signature id="Math.wrap_angle+3">Math.wrap_angle(**degrees**: `Num`, **lower**: `Num`, **upper**: `Num`)
<a class="headerlink" href="#Math.wrap_angle+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Bring angle into lower...upper degree space.   

<endpoint module="luxe: math" class="Math" signature="wrap_radians(radians : Num, lower : Num, upper : Num)"></endpoint>
<signature id="Math.wrap_radians+3">Math.wrap_radians(**radians**: `Num`, **lower**: `Num`, **upper**: `Num`)
<a class="headerlink" href="#Math.wrap_radians+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="nearest_power_of_two(value : Num)"></endpoint>
<signature id="Math.nearest_power_of_two">Math.nearest_power_of_two(**value**: `Num`)
<a class="headerlink" href="#Math.nearest_power_of_two" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="map_linear(value : Num, a1 : Num, a2 : Num, b1 : Num, b2 : Num)"></endpoint>
<signature id="Math.map_linear+5">Math.map_linear(**value**: `Num`, **a1**: `Num`, **a2**: `Num`, **b1**: `Num`, **b2**: `Num`)
<a class="headerlink" href="#Math.map_linear+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Remap value from `a1...a2` space to `b1...b2` space (unclamped).   

<endpoint module="luxe: math" class="Math" signature="smoothstep(x : Num, min : Num, max : Num)"></endpoint>
<signature id="Math.smoothstep+3">Math.smoothstep(**x**: `Num`, **min**: `Num`, **max**: `Num`)
<a class="headerlink" href="#Math.smoothstep+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Smoothed inverse lerp using cubic hermite interpolation. Output is clamped between 0 and 1.   

<endpoint module="luxe: math" class="Math" signature="smootherstep(x : Num, min : Num, max : Num)"></endpoint>
<signature id="Math.smootherstep+3">Math.smootherstep(**x**: `Num`, **min**: `Num`, **max**: `Num`)
<a class="headerlink" href="#Math.smootherstep+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Alternate smooth inverse interpolation with derivative of 0 at min and max points. Output is clamped between 0 and 1.   

<endpoint module="luxe: math" class="Math" signature="smoothstepx(x : Num, round : Num, steep : Num)"></endpoint>
<signature id="Math.smoothstepx+3">Math.smoothstepx(**x**: `Num`, **round**: `Num`, **steep**: `Num`)
<a class="headerlink" href="#Math.smoothstepx+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: math" class="Math" signature="random_point_in_unit_circle(rng : Random)"></endpoint>
<signature id="Math.random_point_in_unit_circle">Math.random_point_in_unit_circle(**rng**: `Random`)
<a class="headerlink" href="#Math.random_point_in_unit_circle" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Random 2d point in circle of radius 1. Has uniform distribution.   

<endpoint module="luxe: math" class="Math" signature="slerp(a : Quat, b : Quat, t : Num)"></endpoint>
<signature id="Math.slerp+3">Math.slerp(**a**: `Quat`, **b**: `Quat`, **t**: `Num`)
<a class="headerlink" href="#Math.slerp+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

