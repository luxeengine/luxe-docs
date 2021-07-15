#![](../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2021.0.5`)  


---

## `luxe: shape2D` module

- [Ray2D](#ray2d)   
- [Ray2DType](#ray2dtype)   
- [Shape2D](#shape2d)   
- [Shape2DType](#shape2dtype)   

---

### Ray2D
`:::js import "luxe: shape2D" for Ray2D`
> no docs found

- [create](#Ray2D.create+3)(**start**: `Any`, **end**: `Any`, **type**: `Any`)
- [set](#Ray2D.set+4)(**ray**: `Any`, **start**: `Any`, **end**: `Any`, **type**: `Any`)
- [set_start](#Ray2D.set_start+2)(**ray**: `Any`, **start**: `Any`)
- [set_end](#Ray2D.set_end+2)(**ray**: `Any`, **end**: `Any`)
- [set_type](#Ray2D.set_type+2)(**ray**: `Any`, **type**: `Any`)
- [get_start](#Ray2D.get_start)(**ray**: `Any`)
- [get_end](#Ray2D.get_end)(**ray**: `Any`)
- [get_type](#Ray2D.get_type)(**ray**: `Any`)

<hr/>
<endpoint module="luxe: shape2D" class="Ray2D" signature="create(start : Any, end : Any, type : Any)"></endpoint>
<signature id="Ray2D.create+3">Ray2D.create(**start**: `Any`, **end**: `Any`, **type**: `Any`)
<a class="headerlink" href="#Ray2D.create+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Ray2D" signature="set(ray : Any, start : Any, end : Any, type : Any)"></endpoint>
<signature id="Ray2D.set+4">Ray2D.set(**ray**: `Any`, **start**: `Any`, **end**: `Any`, **type**: `Any`)
<a class="headerlink" href="#Ray2D.set+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Ray2D" signature="set_start(ray : Any, start : Any)"></endpoint>
<signature id="Ray2D.set_start+2">Ray2D.set_start(**ray**: `Any`, **start**: `Any`)
<a class="headerlink" href="#Ray2D.set_start+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Ray2D" signature="set_end(ray : Any, end : Any)"></endpoint>
<signature id="Ray2D.set_end+2">Ray2D.set_end(**ray**: `Any`, **end**: `Any`)
<a class="headerlink" href="#Ray2D.set_end+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Ray2D" signature="set_type(ray : Any, type : Any)"></endpoint>
<signature id="Ray2D.set_type+2">Ray2D.set_type(**ray**: `Any`, **type**: `Any`)
<a class="headerlink" href="#Ray2D.set_type+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Ray2D" signature="get_start(ray : Any)"></endpoint>
<signature id="Ray2D.get_start">Ray2D.get_start(**ray**: `Any`)
<a class="headerlink" href="#Ray2D.get_start" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Ray2D" signature="get_end(ray : Any)"></endpoint>
<signature id="Ray2D.get_end">Ray2D.get_end(**ray**: `Any`)
<a class="headerlink" href="#Ray2D.get_end" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Ray2D" signature="get_type(ray : Any)"></endpoint>
<signature id="Ray2D.get_type">Ray2D.get_type(**ray**: `Any`)
<a class="headerlink" href="#Ray2D.get_type" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Ray2DType
`:::js import "luxe: shape2D" for Ray2DType`
> no docs found

- [finite](#Ray2DType.finite)
- [infinite_end](#Ray2DType.infinite_end)
- [infinite](#Ray2DType.infinite)
- [from_string](#Ray2DType.from_string)(**value**: `Any`)
- [name](#Ray2DType.name)(**value**: `Any`)

<hr/>
<endpoint module="luxe: shape2D" class="Ray2DType" signature="finite"></endpoint>
<signature id="Ray2DType.finite">Ray2DType.finite
<a class="headerlink" href="#Ray2DType.finite" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Ray2DType" signature="infinite_end"></endpoint>
<signature id="Ray2DType.infinite_end">Ray2DType.infinite_end
<a class="headerlink" href="#Ray2DType.infinite_end" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Ray2DType" signature="infinite"></endpoint>
<signature id="Ray2DType.infinite">Ray2DType.infinite
<a class="headerlink" href="#Ray2DType.infinite" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Ray2DType" signature="from_string(value : Any)"></endpoint>
<signature id="Ray2DType.from_string">Ray2DType.from_string(**value**: `Any`)
<a class="headerlink" href="#Ray2DType.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Ray2DType" signature="name(value : Any)"></endpoint>
<signature id="Ray2DType.name">Ray2DType.name(**value**: `Any`)
<a class="headerlink" href="#Ray2DType.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Shape2D
`:::js import "luxe: shape2D" for Shape2D`
> no docs found

- [create_poly](#Shape2D.create_poly+4)(**pos**: `Any`, **angle**: `Any`, **scale**: `Any`, **verts**: `Any`)
- [create_ngon](#Shape2D.create_ngon+5)(**pos**: `Any`, **angle**: `Any`, **scale**: `Any`, **sides**: `Any`, **radius**: `Any`)
- [create_rect](#Shape2D.create_rect+5)(**pos**: `Any`, **angle**: `Any`, **scale**: `Any`, **size**: `Any`, **centered**: `Any`)
- [create_circle](#Shape2D.create_circle+4)(**pos**: `Any`, **angle**: `Any`, **scale**: `Any`, **radius**: `Any`)
- [destroy](#Shape2D.destroy)(**shape**: `Any`)
- [set_pos](#Shape2D.set_pos+2)(**shape**: `Any`, **pos**: `Any`)
- [set_rotation](#Shape2D.set_rotation+2)(**shape**: `Any`, **angle**: `Any`)
- [set_scale](#Shape2D.set_scale+2)(**shape**: `Any`, **scale**: `Any`)
- [get_type](#Shape2D.get_type)(**shape**: `Any`)
- [get_pos](#Shape2D.get_pos)(**shape**: `Any`)
- [get_bounds](#Shape2D.get_bounds+2)(**shape**: `Any`, **into**: `Any`)
- [get_rotation](#Shape2D.get_rotation)(**shape**: `Any`)
- [get_scale](#Shape2D.get_scale)(**shape**: `Any`)
- [get_verts](#Shape2D.get_verts)(**shape**: `Any`)
- [get_radius](#Shape2D.get_radius)(**shape**: `Any`)

<hr/>
<endpoint module="luxe: shape2D" class="Shape2D" signature="create_poly(pos : Any, angle : Any, scale : Any, verts : Any)"></endpoint>
<signature id="Shape2D.create_poly+4">Shape2D.create_poly(**pos**: `Any`, **angle**: `Any`, **scale**: `Any`, **verts**: `Any`)
<a class="headerlink" href="#Shape2D.create_poly+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Shape2D" signature="create_ngon(pos : Any, angle : Any, scale : Any, sides : Any, radius : Any)"></endpoint>
<signature id="Shape2D.create_ngon+5">Shape2D.create_ngon(**pos**: `Any`, **angle**: `Any`, **scale**: `Any`, **sides**: `Any`, **radius**: `Any`)
<a class="headerlink" href="#Shape2D.create_ngon+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Shape2D" signature="create_rect(pos : Any, angle : Any, scale : Any, size : Any, centered : Any)"></endpoint>
<signature id="Shape2D.create_rect+5">Shape2D.create_rect(**pos**: `Any`, **angle**: `Any`, **scale**: `Any`, **size**: `Any`, **centered**: `Any`)
<a class="headerlink" href="#Shape2D.create_rect+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Shape2D" signature="create_circle(pos : Any, angle : Any, scale : Any, radius : Any)"></endpoint>
<signature id="Shape2D.create_circle+4">Shape2D.create_circle(**pos**: `Any`, **angle**: `Any`, **scale**: `Any`, **radius**: `Any`)
<a class="headerlink" href="#Shape2D.create_circle+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Shape2D" signature="destroy(shape : Any)"></endpoint>
<signature id="Shape2D.destroy">Shape2D.destroy(**shape**: `Any`)
<a class="headerlink" href="#Shape2D.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Shape2D" signature="set_pos(shape : Any, pos : Any)"></endpoint>
<signature id="Shape2D.set_pos+2">Shape2D.set_pos(**shape**: `Any`, **pos**: `Any`)
<a class="headerlink" href="#Shape2D.set_pos+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Shape2D" signature="set_rotation(shape : Any, angle : Any)"></endpoint>
<signature id="Shape2D.set_rotation+2">Shape2D.set_rotation(**shape**: `Any`, **angle**: `Any`)
<a class="headerlink" href="#Shape2D.set_rotation+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Shape2D" signature="set_scale(shape : Any, scale : Any)"></endpoint>
<signature id="Shape2D.set_scale+2">Shape2D.set_scale(**shape**: `Any`, **scale**: `Any`)
<a class="headerlink" href="#Shape2D.set_scale+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Shape2D" signature="get_type(shape : Any)"></endpoint>
<signature id="Shape2D.get_type">Shape2D.get_type(**shape**: `Any`)
<a class="headerlink" href="#Shape2D.get_type" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Shape2D" signature="get_pos(shape : Any)"></endpoint>
<signature id="Shape2D.get_pos">Shape2D.get_pos(**shape**: `Any`)
<a class="headerlink" href="#Shape2D.get_pos" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Shape2D" signature="get_bounds(shape : Any, into : Any)"></endpoint>
<signature id="Shape2D.get_bounds+2">Shape2D.get_bounds(**shape**: `Any`, **into**: `Any`)
<a class="headerlink" href="#Shape2D.get_bounds+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Shape2D" signature="get_rotation(shape : Any)"></endpoint>
<signature id="Shape2D.get_rotation">Shape2D.get_rotation(**shape**: `Any`)
<a class="headerlink" href="#Shape2D.get_rotation" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Shape2D" signature="get_scale(shape : Any)"></endpoint>
<signature id="Shape2D.get_scale">Shape2D.get_scale(**shape**: `Any`)
<a class="headerlink" href="#Shape2D.get_scale" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Shape2D" signature="get_verts(shape : Any)"></endpoint>
<signature id="Shape2D.get_verts">Shape2D.get_verts(**shape**: `Any`)
<a class="headerlink" href="#Shape2D.get_verts" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Shape2D" signature="get_radius(shape : Any)"></endpoint>
<signature id="Shape2D.get_radius">Shape2D.get_radius(**shape**: `Any`)
<a class="headerlink" href="#Shape2D.get_radius" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Shape2DType
`:::js import "luxe: shape2D" for Shape2DType`
> no docs found

- [poly](#Shape2DType.poly)
- [circle](#Shape2DType.circle)
- [from_string](#Shape2DType.from_string)(**value**: `Any`)
- [name](#Shape2DType.name)(**value**: `Any`)

<hr/>
<endpoint module="luxe: shape2D" class="Shape2DType" signature="poly"></endpoint>
<signature id="Shape2DType.poly">Shape2DType.poly
<a class="headerlink" href="#Shape2DType.poly" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Shape2DType" signature="circle"></endpoint>
<signature id="Shape2DType.circle">Shape2DType.circle
<a class="headerlink" href="#Shape2DType.circle" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Shape2DType" signature="from_string(value : Any)"></endpoint>
<signature id="Shape2DType.from_string">Shape2DType.from_string(**value**: `Any`)
<a class="headerlink" href="#Shape2DType.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: shape2D" class="Shape2DType" signature="name(value : Any)"></endpoint>
<signature id="Shape2DType.name">Shape2DType.name(**value**: `Any`)
<a class="headerlink" href="#Shape2DType.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

