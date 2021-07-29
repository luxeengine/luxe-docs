#![](../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2021.0.7`)  


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
- [hex](#Color.hex)(**value**: `Num`)
- [hex](#Color.hex+2)(**value**: `Num`, **alpha**: `Num`)
- [hex_set](#Color.hex_set+2)(**color**: `Color`, **hex**: `Num`)
- [lerp](#Color.lerp+3)(**from**: `Color`, **to**: `Color`, **t**: `Num`)
- [lerp](#Color.lerp+4)(**from**: `Color`, **to**: `Color`, **t**: `Num`, **into**: `Color`)
- [rgb2hsv](#Color.rgb2hsv)(**rgb**: `Color`)
- [hsv2rgb](#Color.hsv2rgb)(**hsv**: `Color`)
- [color_from_hue](#Color.color_from_hue)(**hue**: `Num`)

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

<endpoint module="luxe: color" class="Color" signature="hex(value : Num)"></endpoint>
<signature id="Color.hex">Color.hex(**value**: `Num`)
<a class="headerlink" href="#Color.hex" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns a new color from the specified hex color value.
> 
>   ```js
>   var color = Color.hex(0xFF00AA)
>   ```   

<endpoint module="luxe: color" class="Color" signature="hex(value : Num, alpha : Num)"></endpoint>
<signature id="Color.hex+2">Color.hex(**value**: `Num`, **alpha**: `Num`)
<a class="headerlink" href="#Color.hex+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
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

<endpoint module="luxe: color" class="Color" signature="lerp(from : Color, to : Color, t : Num)"></endpoint>
<signature id="Color.lerp+3">Color.lerp(**from**: `Color`, **to**: `Color`, **t**: `Num`)
<a class="headerlink" href="#Color.lerp+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
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

