#![](../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.11.1`)  


---

## `luxe: color` module

- [Color](#color)   

---

### Color
`:::js import "luxe: color" for Color`
> Access to color APIs. Note that this is not done at all.

- [white](#Color.white)
- [black](#Color.black)
- [clear](#Color.clear)
- [pink](#Color.pink)
- [hex](#Color.hex)(**value**: `Num`)
- [clone](#Color.clone+2)(**other**: `Color`, **alpha**: `Num`)
- [hex](#Color.hex+2)(**value**: `Num`, **alpha**: `Num`)
- [hex_set](#Color.hex_set+2)(**color**: `Color`, **hex**: `Num`)
- [hex_color](#Color.hex_color)(**color**: `Color`)
- [hex_color](#Color.hex_color+2)(**color**: `Color`, **include_alpha**: `Bool`)
- [lerp](#Color.lerp+3)(**from**: `Color`, **to**: `Color`, **t**: `Num`)
- [lerp](#Color.lerp+4)(**from**: `Color`, **to**: `Color`, **t**: `Num`, **into**: `Color`)
- [rgb2hsv](#Color.rgb2hsv)(**rgb**: `Color`)
- [hsv2rgb](#Color.hsv2rgb)(**hsv**: `Color`)
- [color_from_hue](#Color.color_from_hue)(**hue**: `Num`)
- [linear_srgb_to_oklab](#Color.linear_srgb_to_oklab+3)(**r**: `Num`, **g**: `Num`, **b**: `Num`)
- [oklab_to_linear_srgb](#Color.oklab_to_linear_srgb+3)(**L**: `Num`, **a**: `Num`, **b**: `Num`)
- [okhsl_to_srgb](#Color.okhsl_to_srgb+3)(**h**: `Num`, **s**: `Num`, **l**: `Num`)
- [srgb_to_okhsl](#Color.srgb_to_okhsl+3)(**r**: `Num`, **g**: `Num`, **b**: `Num`)
- [okhsv_to_srgb](#Color.okhsv_to_srgb+3)(**h**: `Num`, **s**: `Num`, **v**: `Num`)
- [srgb_to_okhsv](#Color.srgb_to_okhsv+3)(**r**: `Num`, **g**: `Num`, **b**: `Num`)
- [find_cusp](#Color.find_cusp+2)(**a**: `Any`, **b**: `Any`)
- [compute_max_saturation](#Color.compute_max_saturation+2)(**a**: `Num`, **b**: `Num`)
- [find_gamut_intersection](#Color.find_gamut_intersection+6)(**a**: `Any`, **b**: `Any`, **L1**: `Any`, **C1**: `Any`, **L0**: `Any`, **cusp**: `Any`)

<hr/>
<endpoint module="luxe: color" class="Color" signature="white"></endpoint>
<signature id="Color.white">Color.white
<a class="headerlink" href="#Color.white" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Color`
> A constant for [1,1,1,1]. Note: don't modify the return value.   

<endpoint module="luxe: color" class="Color" signature="black"></endpoint>
<signature id="Color.black">Color.black
<a class="headerlink" href="#Color.black" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Color`
> A constant for [0,0,0,1]. Note: don't modify the return value.   

<endpoint module="luxe: color" class="Color" signature="clear"></endpoint>
<signature id="Color.clear">Color.clear
<a class="headerlink" href="#Color.clear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Color`
> A constant for [0,0,0,0]. Note: don't modify the return value.   

<endpoint module="luxe: color" class="Color" signature="pink"></endpoint>
<signature id="Color.pink">Color.pink
<a class="headerlink" href="#Color.pink" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Color`
> The luxe pink color used everywhere. Note: don't modify the return value.   

<endpoint module="luxe: color" class="Color" signature="hex(value : Num)"></endpoint>
<signature id="Color.hex">Color.hex(**value**: `Num`)
<a class="headerlink" href="#Color.hex" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Color`
> Returns a new color from the specified hex color value.
> 
>   ```js
>   var color = Color.hex(0xFF00AA)
>   ```   

<endpoint module="luxe: color" class="Color" signature="clone(other : Color, alpha : Num)"></endpoint>
<signature id="Color.clone+2">Color.clone(**other**: `Color`, **alpha**: `Num`)
<a class="headerlink" href="#Color.clone+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns a new color from the specified color with a different alpha.
> 
>   ```js
>   var other = Color.hex(0xFF00AA)
>   var color = Color.clone(other, 0.5)
>   ```   

<endpoint module="luxe: color" class="Color" signature="hex(value : Num, alpha : Num)"></endpoint>
<signature id="Color.hex+2">Color.hex(**value**: `Num`, **alpha**: `Num`)
<a class="headerlink" href="#Color.hex+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Color`
> Returns a new color from the specified hex color value, with the specified alpha value.
> 
>     var color = Color.hex(0xFF00AA, 0.5)   

<endpoint module="luxe: color" class="Color" signature="hex_set(color : Color, hex : Num)"></endpoint>
<signature id="Color.hex_set+2">Color.hex_set(**color**: `Color`, **hex**: `Num`)
<a class="headerlink" href="#Color.hex_set+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Set an existing color to the specified hex color value.
> 
>   ```js
>   var color = Color.hex_set(0xFF00AA)
>   ```   

<endpoint module="luxe: color" class="Color" signature="hex_color(color : Color)"></endpoint>
<signature id="Color.hex_color">Color.hex_color(**color**: `Color`)
<a class="headerlink" href="#Color.hex_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get the hex color value of a color   

<endpoint module="luxe: color" class="Color" signature="hex_color(color : Color, include_alpha : Bool)"></endpoint>
<signature id="Color.hex_color+2">Color.hex_color(**color**: `Color`, **include_alpha**: `Bool`)
<a class="headerlink" href="#Color.hex_color+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get the hex color value of a color, either 3 byte or 4 byte with alpha   

<endpoint module="luxe: color" class="Color" signature="lerp(from : Color, to : Color, t : Num)"></endpoint>
<signature id="Color.lerp+3">Color.lerp(**from**: `Color`, **to**: `Color`, **t**: `Num`)
<a class="headerlink" href="#Color.lerp+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Color`
> Linearly interpolate between two colors, using `t` as the distance between the two in 0...1 range.
> To blend two colors half and half, you'd use `lerp(from, to, 0.5)`. If `t` is `0`, `from` is returned
> and if `t` is `1`, `to` is returned.   

<endpoint module="luxe: color" class="Color" signature="lerp(from : Color, to : Color, t : Num, into : Color)"></endpoint>
<signature id="Color.lerp+4">Color.lerp(**from**: `Color`, **to**: `Color`, **t**: `Num`, **into**: `Color`)
<a class="headerlink" href="#Color.lerp+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Linearly interpolate between two colors, storing the result in the existing color `into`. 
> `t` is the distance between the two in 0...1 range. To blend two colors half and half, 
> you'd use `lerp(from, to, 0.5)`. If `t` is `0`, `from` is returned and if `t` is `1`, `to` is returned.   

<endpoint module="luxe: color" class="Color" signature="rgb2hsv(rgb : Color)"></endpoint>
<signature id="Color.rgb2hsv">Color.rgb2hsv(**rgb**: `Color`)
<a class="headerlink" href="#Color.rgb2hsv" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Color`
> Convert from an RGB format color to an HSV format.   

<endpoint module="luxe: color" class="Color" signature="hsv2rgb(hsv : Color)"></endpoint>
<signature id="Color.hsv2rgb">Color.hsv2rgb(**hsv**: `Color`)
<a class="headerlink" href="#Color.hsv2rgb" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Color`
> Convert an HSV format color to an RGB format.   

<endpoint module="luxe: color" class="Color" signature="color_from_hue(hue : Num)"></endpoint>
<signature id="Color.color_from_hue">Color.color_from_hue(**hue**: `Num`)
<a class="headerlink" href="#Color.color_from_hue" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Color`
> Create a color from the given hue, in a 0...1 range. 
> Values outside 0...1 are wrapped into 0...1 range.   

<endpoint module="luxe: color" class="Color" signature="linear_srgb_to_oklab(r : Num, g : Num, b : Num)"></endpoint>
<signature id="Color.linear_srgb_to_oklab+3">Color.linear_srgb_to_oklab(**r**: `Num`, **g**: `Num`, **b**: `Num`)
<a class="headerlink" href="#Color.linear_srgb_to_oklab+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: color" class="Color" signature="oklab_to_linear_srgb(L : Num, a : Num, b : Num)"></endpoint>
<signature id="Color.oklab_to_linear_srgb+3">Color.oklab_to_linear_srgb(**L**: `Num`, **a**: `Num`, **b**: `Num`)
<a class="headerlink" href="#Color.oklab_to_linear_srgb+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: color" class="Color" signature="okhsl_to_srgb(h : Num, s : Num, l : Num)"></endpoint>
<signature id="Color.okhsl_to_srgb+3">Color.okhsl_to_srgb(**h**: `Num`, **s**: `Num`, **l**: `Num`)
<a class="headerlink" href="#Color.okhsl_to_srgb+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: color" class="Color" signature="srgb_to_okhsl(r : Num, g : Num, b : Num)"></endpoint>
<signature id="Color.srgb_to_okhsl+3">Color.srgb_to_okhsl(**r**: `Num`, **g**: `Num`, **b**: `Num`)
<a class="headerlink" href="#Color.srgb_to_okhsl+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: color" class="Color" signature="okhsv_to_srgb(h : Num, s : Num, v : Num)"></endpoint>
<signature id="Color.okhsv_to_srgb+3">Color.okhsv_to_srgb(**h**: `Num`, **s**: `Num`, **v**: `Num`)
<a class="headerlink" href="#Color.okhsv_to_srgb+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: color" class="Color" signature="srgb_to_okhsv(r : Num, g : Num, b : Num)"></endpoint>
<signature id="Color.srgb_to_okhsv+3">Color.srgb_to_okhsv(**r**: `Num`, **g**: `Num`, **b**: `Num`)
<a class="headerlink" href="#Color.srgb_to_okhsv+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: color" class="Color" signature="find_cusp(a : Any, b : Any)"></endpoint>
<signature id="Color.find_cusp+2">Color.find_cusp(**a**: `Any`, **b**: `Any`)
<a class="headerlink" href="#Color.find_cusp+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: color" class="Color" signature="compute_max_saturation(a : Num, b : Num)"></endpoint>
<signature id="Color.compute_max_saturation+2">Color.compute_max_saturation(**a**: `Num`, **b**: `Num`)
<a class="headerlink" href="#Color.compute_max_saturation+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: color" class="Color" signature="find_gamut_intersection(a : Any, b : Any, L1 : Any, C1 : Any, L0 : Any, cusp : Any)"></endpoint>
<signature id="Color.find_gamut_intersection+6">Color.find_gamut_intersection(**a**: `Any`, **b**: `Any`, **L1**: `Any`, **C1**: `Any`, **L0**: `Any`, **cusp**: `Any`)
<a class="headerlink" href="#Color.find_gamut_intersection+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

