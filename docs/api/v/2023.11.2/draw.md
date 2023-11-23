#![](../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.11.2`)  


---

## `luxe: draw` module

- [Draw](#draw)   
- [LineCap](#linecap)   
- [LineJoin](#linejoin)   
- [PathStyle](#pathstyle)   

---

### Draw
`:::js import "luxe: draw" for Draw`
> Draw is a service API that offers drawing to a context (canvas) in an efficient way.
> Things like lines, circles, paths and so on are what it provides. _The terms canvas and context
> will be used interchangeably._ 
> 
> It is important to note that
> `Draw` is a [commit](../../guide/concepts#commit) based API. A brief tutorial 
> on using it can be found here: [2D drawing tutorial](../../tutorial/basics/drawing-2d).
> 
> `Draw` can be used to draw game content with, but is also a great tool for debug visualization.
> Many problems are a lot clearer when their details are drawn in the world, which Draw is very useful for.
> 
> The context can be drawn to once or updated frequently. For example you might draw a grid to the context,
> and then leave it there which is a very efficient way to draw many lines.

- [create](#Draw.create)(**set**: `Any`)
- [create](#Draw.create+4)(**set**: `RenderSet`, **tri_basis**: `String`, **text_basis**: `String`, **line_basis**: `String`)
- [destroy](#Draw.destroy)(**context**: `Any`)
- [valid](#Draw.valid)(**context**: `Any`)
- [clear](#Draw.clear)(**context**: `Any`)
- [commit](#Draw.commit)(**context**: `Any`)
- [rect](#Draw.rect+8)(**context**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **style**: `Any`)
- [rect_detailed](#Draw.rect_detailed+10)(**context**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **radius**: `Any`, **smoothness**: `Any`, **style**: `Any`)
- [quad_detailed](#Draw.quad_detailed+10)(**context**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **radius**: `Any`, **smoothness**: `Any`, **color**: `Any`)
- [quad](#Draw.quad+8)(**context**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **color**: `Any`)
- [ngon](#Draw.ngon+9)(**context**: `Any`, **ox**: `Any`, **oy**: `Any`, **oz**: `Any`, **rx**: `Any`, **ry**: `Any`, **sides**: `Any`, **angle**: `Any`, **style**: `Any`)
- [ngon_solid](#Draw.ngon_solid+9)(**context**: `Any`, **ox**: `Any`, **oy**: `Any`, **oz**: `Any`, **rx**: `Any`, **ry**: `Any`, **sides**: `Any`, **angle**: `Any`, **color**: `Any`)
- [ring](#Draw.ring+10)(**context**: `Any`, **ox**: `Any`, **oy**: `Any`, **oz**: `Any`, **rx**: `Any`, **ry**: `Any`, **start_angle**: `Any`, **end_angle**: `Any`, **smoothness**: `Any`, **style**: `Any`)
- [ring](#Draw.ring+7)(**context**: `Any`, **ox**: `Any`, **oy**: `Any`, **oz**: `Any`, **radius**: `Any`, **smoothness**: `Any`, **style**: `Any`)
- [circle](#Draw.circle+7)(**context**: `Any`, **ox**: `Any`, **oy**: `Any`, **oz**: `Any`, **radius**: `Any`, **smoothness**: `Any`, **color**: `Any`)
- [circle](#Draw.circle+10)(**context**: `Any`, **ox**: `Any`, **oy**: `Any`, **oz**: `Any`, **rx**: `Any`, **ry**: `Any`, **start_angle**: `Any`, **end_angle**: `Any`, **smoothness**: `Any`, **color**: `Any`)
- [line](#Draw.line+7)(**context**: `Any`, **x1**: `Any`, **y1**: `Any`, **x2**: `Any`, **y2**: `Any`, **z**: `Any`, **style**: `Any`)
- [path](#Draw.path+4)(**context**: `Any`, **points**: `Any`, **style**: `Any`, **closed**: `Any`)
- [path3D](#Draw.path3D+4)(**context**: `Any`, **points**: `Any`, **style**: `Any`, **closed**: `Any`)
- [line3D](#Draw.line3D+4)(**context**: `Draw`, **start**: `Vec`, **end**: `Vec`, **style**: `PathStyle`)
- [bounds3D](#Draw.bounds3D+3)(**context**: `Any`, **geometry**: `Any`, **style**: `Any`)
- [aabb3D](#Draw.aabb3D+4)(**context**: `Any`, **center**: `Any`, **radius**: `Any`, **style**: `Any`)
- [plane3D](#Draw.plane3D+5)(**context**: `Draw`, **pos**: `Vec`, **normal**: `Vec`, **radius**: `Num`, **style**: `PathStyle`)
- [plus3D](#Draw.plus3D+4)(**context**: `Draw`, **pos**: `Vec`, **radius**: `Num`, **style**: `PathStyle`)
- [ring3D](#Draw.ring3D+7)(**context**: `Draw`, **pos**: `Vec3`, **radius**: `Vec2`, **start_angle**: `Num`, **end_angle**: `Num`, **smoothness**: `Num`, **style**: `PathStyle`)
- [plus](#Draw.plus+4)(**context**: `Draw`, **pos**: `Vec`, **radius**: `Num`, **style**: `PathStyle`)
- [camera](#Draw.camera+3)(**context**: `Draw`, **camera**: `Entity`, **style**: `PathStyle`)
- [frustum](#Draw.frustum+3)(**context**: `Draw`, **corners**: `List`, **style**: `PathStyle`)
- [text](#Draw.text+12)(**context**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **string**: `Any`, **size**: `Any`, **font**: `Any`, **color**: `Any`, **align**: `Any`, **align_vertical**: `Any`)
- [text](#Draw.text+10)(**context**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **string**: `Any`, **size**: `Any`, **font**: `Any`, **color**: `Any`, **align**: `Any`, **align_vertical**: `Any`)
- [image](#Draw.image+8)(**context**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **material**: `Any`)
- [image](#Draw.image+10)(**context**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **color**: `Any`, **uv**: `Any`, **material**: `Any`)
- [cross](#Draw.cross+7)(**context**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **radius**: `Any`, **angle**: `Any`, **style**: `Any`)

<hr/>
<endpoint module="luxe: draw" class="Draw" signature="create(set : Any)"></endpoint>
<signature id="Draw.create">Draw.create(**set**: `Any`)
<a class="headerlink" href="#Draw.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Creates a new drawing context to draw with.
> The `set` passed in is a `RenderSet`, which you normally get from a `World` via `World.render_set(world)`.
> This would place the canvas in the world to be rendered at the same time, as part of the world.
> 
>     var canvas = Draw.create(World.render_set(app.world))   

<endpoint module="luxe: draw" class="Draw" signature="create(set : RenderSet, tri_basis : String, text_basis : String, line_basis : String)"></endpoint>
<signature id="Draw.create+4">Draw.create(**set**: `RenderSet`, **tri_basis**: `String`, **text_basis**: `String`, **line_basis**: `String`)
<a class="headerlink" href="#Draw.create+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Creates a new drawing context to draw with.
> The `set` passed in is a `RenderSet`, which you normally get from a `World` via `World.render_set(world)`.
> This would place the canvas in the world to be rendered at the same time, as part of the world.
> 
> - `tri_basis`
>   - Triangle Material Basis for the geometry
>   - default `luxe: material_basis/solid`
> - `text_basis`
>   - Text Material Basis
>   - default `luxe: material_basis/font`
> - `line_basis`
>   - Line Material Basis for 3D line geometry
>   - default `luxe: material_basis/debug_line3d`
> 
>     var canvas = Draw.create(World.render_set(app.world), 
>                              "luxe: material_basis/solid", 
>                              "luxe: material_basis/font",
>                              "luxe: material_basis/debug_line3d")   

<endpoint module="luxe: draw" class="Draw" signature="destroy(context : Any)"></endpoint>
<signature id="Draw.destroy">Draw.destroy(**context**: `Any`)
<a class="headerlink" href="#Draw.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Destroy a previously created context.
> 
>   ```js
>   var canvas = Draw.create(World.render_set(app.world))
>   ...
>   Draw.destroy(canvas)
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="valid(context : Any)"></endpoint>
<signature id="Draw.valid">Draw.valid(**context**: `Any`)
<a class="headerlink" href="#Draw.valid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns true if the context is valid (and hasn't been destroyed).
> 
>   ```js
>   var canvas = Draw.create(World.render_set(app.world))
>   var canvas = Draw.create(World.render_set(app.world))
>   Log.print(Draw.valid(canvas)) //true
>   Draw.destroy(canvas)
>   Log.print(Draw.valid(canvas)) //false
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="clear(context : Any)"></endpoint>
<signature id="Draw.clear">Draw.clear(**context**: `Any`)
<a class="headerlink" href="#Draw.clear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Clears the context of any drawn content.
> This clears both committed and uncommitted data.
> 
>   ```js
>   Draw.clear(draw)
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="commit(context : Any)"></endpoint>
<signature id="Draw.commit">Draw.commit(**context**: `Any`)
<a class="headerlink" href="#Draw.commit" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Commit the content that has been drawn to the context.
> 
> When using the Draw API, you can submit a bunch of drawing to happen,
> but it won't show up until it is committed. 
> 
> You can think of the draw calls as a queue, commit will process 
> that queue, and the canvas contents will be updated. The content
> will stay there until commit is called again. 
> 
> Calling commit with nothing in the queue will clear the contents (see also `Draw.clear`).
> 
>   ```js
>   var canvas = Draw.create(World.render_set(app.world))
>   //draw a red box rotated 45 degrees
>   Draw.quad(canvas, 0, 0, 0, 100, 100, 45, [1, 0, 0, 1])
>   Draw.commit(canvas)
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="rect(context : Any, x : Any, y : Any, z : Any, w : Any, h : Any, angle : Any, style : Any)"></endpoint>
<signature id="Draw.rect+8">Draw.rect(**context**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **style**: `Any`)
<a class="headerlink" href="#Draw.rect+8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Draws a rectangle **outline** using `style` (`PathStyle`) at `x`,`y`, with depth `z`, with width of `w` and height of `h`.
> The rectangle will be rotated `angle` degrees.
> 
>   ```js
>   var depth = 0
>   var angle = 45
>   var style = PathStyle.new()
>       style.color = [1,0,0,1]
>       style.thickness = 2
>   Draw.rect(canvas, 0, 0, depth, 100, 100, angle, style)
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="rect_detailed(context : Any, x : Any, y : Any, z : Any, w : Any, h : Any, angle : Any, radius : Any, smoothness : Any, style : Any)"></endpoint>
<signature id="Draw.rect_detailed+10">Draw.rect_detailed(**context**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **radius**: `Any`, **smoothness**: `Any`, **style**: `Any`)
<a class="headerlink" href="#Draw.rect_detailed+10" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Draws a detailed rectangle **outline** using `style` (`PathStyle`) at `x`,`y`, with depth `z`, with width of `w` and height of `h`.
> The rectangle will be rotated `angle` degrees. 
> 
> "Detailed" means that the corners can be configured using the `radius` and `smoothness` values.
> This allows drawing rounded rectangles, rectangles with inverted rounded corners, and with flat corners.
> The radius controls the amount inset from the edges. With a smoothness of 0, the corners will be angled/flat.
> 
> The order is `[bottom left, bottom right, top right, top left]` for radius + smoothness.
> 
>   ```js
>   var depth = 0
>   var angle = 0
>   var style = PathStyle.new()
>   var radius = [16, 16, 16, 16]
>   var smoothness = [2, 2, 2, 2]
>   Draw.rect_detailed(_ctx, 64, 64, depth, 256, 128, angle, radius, smoothness, style)
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="quad_detailed(context : Any, x : Any, y : Any, z : Any, w : Any, h : Any, angle : Any, radius : Any, smoothness : Any, color : Any)"></endpoint>
<signature id="Draw.quad_detailed+10">Draw.quad_detailed(**context**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **radius**: `Any`, **smoothness**: `Any`, **color**: `Any`)
<a class="headerlink" href="#Draw.quad_detailed+10" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Draws a detailed rectangle using `color` at `x`,`y`, with depth `z`, with width of `w` and height of `h`.
> The rectangle will be rotated `angle` degrees. 
> 
> "Detailed" means that the corners can be configured using the `radius` and `smoothness` values.
> This allows drawing rounded rectangles, rectangles with inverted rounded corners, and with flat corners.
> The radius controls the amount inset from the edges. With a smoothness of 0, the corners will be angled/flat.
> 
> The order is `[bottom left, bottom right, top right, top left]` for radius + smoothness.
> 
>   ```js
>   var depth = 0
>   var angle = 0
>   var color = [0,0,0,1]
>   var radius = [16, 16, 16, 16]
>   var smoothness = [2, 2, 2, 2]
>   Draw.quad_detailed(_ctx, 64, 64, depth, 256, 128, angle, radius, smoothness, color)
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="quad(context : Any, x : Any, y : Any, z : Any, w : Any, h : Any, angle : Any, color : Any)"></endpoint>
<signature id="Draw.quad+8">Draw.quad(**context**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **color**: `Any`)
<a class="headerlink" href="#Draw.quad+8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Draws a **solid** rectangle using `color` at `x`,`y`, with depth `z`, with width of `w` and height of `h`.
> The rectangle will be rotated `angle` degrees.
> 
>   ```js
>   //draw a black solid rectangle
>   var depth = 0
>   var angle = 45
>   Draw.quad(canvas, 0, 0, depth, 100, 100, angle, [0,0,0,1])
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="ngon(context : Any, ox : Any, oy : Any, oz : Any, rx : Any, ry : Any, sides : Any, angle : Any, style : Any)"></endpoint>
<signature id="Draw.ngon+9">Draw.ngon(**context**: `Any`, **ox**: `Any`, **oy**: `Any`, **oz**: `Any`, **rx**: `Any`, **ry**: `Any`, **sides**: `Any`, **angle**: `Any`, **style**: `Any`)
<a class="headerlink" href="#Draw.ngon+9" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Draw an ngon (like a triangle, hexagon, pentagon etc) **outline** at `ox`,`oy` at depth `oz`. 
> The `rx` and `ry` radius values control the size of the shape around its origin.
> The number of `sides` controls how many sides the polygon will have (3 for a triangle, 6 for a hexagon).
> `sides` must be bigger than `3` to make sense for this function, it will be clamped to 3.
> 
>   ```js
>   var depth = 0
>   var sides = 3
>   var radius = 32
>   var angle = 45
>   var style = PathStyle.new()
>   Draw.ngon(canvas, 128, 128, depth, radius, radius, sides, angle, style)
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="ngon_solid(context : Any, ox : Any, oy : Any, oz : Any, rx : Any, ry : Any, sides : Any, angle : Any, color : Any)"></endpoint>
<signature id="Draw.ngon_solid+9">Draw.ngon_solid(**context**: `Any`, **ox**: `Any`, **oy**: `Any`, **oz**: `Any`, **rx**: `Any`, **ry**: `Any`, **sides**: `Any`, **angle**: `Any`, **color**: `Any`)
<a class="headerlink" href="#Draw.ngon_solid+9" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Draw a **solid** ngon (like a triangle, hexagon, pentagon etc)  at `ox`,`oy` at depth `oz`. 
> The `rx` and `ry` radius values control the size of the shape around its origin.
> The number of `sides` controls how many sides the polygon will have (3 for a triangle, 6 for a hexagon).
> `sides` must be bigger than `3` to make sense for this function.
> 
> :todo: this naming will change soon to be consistent across all draw APIs.
> 
>   ```js
>   var depth = 0
>   var sides = 3
>   var radius = 32
>   var angle = 45
>   Draw.ngon_solid(canvas, 128, 128, depth, radius, radius, sides, angle, Color.pink)
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="ring(context : Any, ox : Any, oy : Any, oz : Any, rx : Any, ry : Any, start_angle : Any, end_angle : Any, smoothness : Any, style : Any)"></endpoint>
<signature id="Draw.ring+10">Draw.ring(**context**: `Any`, **ox**: `Any`, **oy**: `Any`, **oz**: `Any`, **rx**: `Any`, **ry**: `Any`, **start_angle**: `Any`, **end_angle**: `Any`, **smoothness**: `Any`, **style**: `Any`)
<a class="headerlink" href="#Draw.ring+10" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Draw a circle **outline** at `ox`,`oy` at depth `oz`. `rx` and `ry` control separate radius values
> for x and y axis, to draw an ellipse.
> 
> `start_angle` and `end_angle` specify in degrees allow drawing
> an open arc, instead of a closed circle. A closed circle has `start_angle` as `0` and `end_angle` as `360`.
> These angles match "the unit circle" in mathematics, where 0 is to the right, and 90 is pointing up.
> 
> :todo: `smoothness` controls how smooth the circle will be.
> 
>   ```js
>   var depth = 0
>   var start_angle = 0
>   var end_angle = 270
>   var smoothness = 2
>   var style = PathStyle.new()
>   Draw.ring(canvas, 128, 128, depth, 32, 16, start_angle, end_angle, smoothness, style)
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="ring(context : Any, ox : Any, oy : Any, oz : Any, radius : Any, smoothness : Any, style : Any)"></endpoint>
<signature id="Draw.ring+7">Draw.ring(**context**: `Any`, **ox**: `Any`, **oy**: `Any`, **oz**: `Any`, **radius**: `Any`, **smoothness**: `Any`, **style**: `Any`)
<a class="headerlink" href="#Draw.ring+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Similar to `ring` with a single radius for both `x` and `y`.   

<endpoint module="luxe: draw" class="Draw" signature="circle(context : Any, ox : Any, oy : Any, oz : Any, radius : Any, smoothness : Any, color : Any)"></endpoint>
<signature id="Draw.circle+7">Draw.circle(**context**: `Any`, **ox**: `Any`, **oy**: `Any`, **oz**: `Any`, **radius**: `Any`, **smoothness**: `Any`, **color**: `Any`)
<a class="headerlink" href="#Draw.circle+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Draw a **solid** circle at `ox`,`oy` at depth `oz`, using `color` and `radius` in size.
> :todo: `smoothness` controls how smooth the circle will be.
> 
>   ```js
>   var depth = 0
>   var smoothness = 2
>   Draw.circle(canvas, 128, 128, depth, 32, smoothness, [1,0,0,1])
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="circle(context : Any, ox : Any, oy : Any, oz : Any, rx : Any, ry : Any, start_angle : Any, end_angle : Any, smoothness : Any, color : Any)"></endpoint>
<signature id="Draw.circle+10">Draw.circle(**context**: `Any`, **ox**: `Any`, **oy**: `Any`, **oz**: `Any`, **rx**: `Any`, **ry**: `Any`, **start_angle**: `Any`, **end_angle**: `Any`, **smoothness**: `Any`, **color**: `Any`)
<a class="headerlink" href="#Draw.circle+10" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Draw a **solid** circle at `ox`,`oy` at depth `oz`. `rx` and `ry` control separate radius values
> for x and y axis, to draw an ellipse.
> 
> `start_angle` and `end_angle` specify in degrees allow drawing
> an open area, like a pie chart (or pacman) instead of a closed circle. A closed circle has `start_angle` as `0` and `end_angle` as `360`.
> These angles match "the unit circle" in mathematics, where 0 is to the right, and 90 is pointing up.
> 
> :todo: `smoothness` controls how smooth the circle will be.
> 
>   ```js
>   var depth = 0
>   var start_angle = 0
>   var end_angle = 270
>   var smoothness = 2
>   Draw.circle(canvas, 128, 128, depth, 32, 16, start_angle, end_angle, smoothness, Color.black)
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="line(context : Any, x1 : Any, y1 : Any, x2 : Any, y2 : Any, z : Any, style : Any)"></endpoint>
<signature id="Draw.line+7">Draw.line(**context**: `Any`, **x1**: `Any`, **y1**: `Any`, **x2**: `Any`, **y2**: `Any`, **z**: `Any`, **style**: `Any`)
<a class="headerlink" href="#Draw.line+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Draw a line from `x1`,`y1` to `x2`,`y2` at depth `z` using `style` (`PathStyle`).
> 
>   ```js
>   var depth = 0
>   var style = PathStyle.new()
>   Draw.line(canvas, 0,0, 100,100, depth, style)
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="path(context : Any, points : Any, style : Any, closed : Any)"></endpoint>
<signature id="Draw.path+4">Draw.path(**context**: `Any`, **points**: `Any`, **style**: `Any`, **closed**: `Any`)
<a class="headerlink" href="#Draw.path+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Draw a path consisting of a list of points. 
> 
> If `closed` is true it is expected that the first and last point in `points`
> have the same positions. 
> 
> `points` is a `List` of `[x, y]` or `[x,y,z]` points. 
> If `z` is not specified for a point it will be 0. 
> Note that this is a 2D drawing function atm, so different z values may not be what you expect.
> 
>   ```js
>   var style = PathStyle.new()
>   var points = [
>     [0,0],
>     [100,100],
>     [120,50],
>     [0,0]
>   ]
>   Draw.path(canvas, points, style, true)
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="path3D(context : Any, points : Any, style : Any, closed : Any)"></endpoint>
<signature id="Draw.path3D+4">Draw.path3D(**context**: `Any`, **points**: `Any`, **style**: `Any`, **closed**: `Any`)
<a class="headerlink" href="#Draw.path3D+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Draw a 3D path consisting of a list of points. 
> 
> If `closed` is true it is expected that the first and last point in `points`
> have the same positions. 
> 
> `points` is a `List` of `[x,y,z]` points. 
> 
>   ```js
>   var style = PathStyle.new()
>   var points = [
>     [0,0,0],
>     [100,100,100],
>     [120,50,100],
>     [0,0,0]
>   ]
>   Draw.path3D(canvas, points, style, true)
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="line3D(context : Draw, start : Vec, end : Vec, style : PathStyle)"></endpoint>
<signature id="Draw.line3D+4">Draw.line3D(**context**: `Draw`, **start**: `Vec`, **end**: `Vec`, **style**: `PathStyle`)
<a class="headerlink" href="#Draw.line3D+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Draw a 3D line from `start` to `end` using `style`. 
> 
>   ```js
>   var style = PathStyle.new()
>   Draw.line3D(canvas, [100,100,100], [120,50,100], style)
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="bounds3D(context : Any, geometry : Any, style : Any)"></endpoint>
<signature id="Draw.bounds3D+3">Draw.bounds3D(**context**: `Any`, **geometry**: `Any`, **style**: `Any`)
<a class="headerlink" href="#Draw.bounds3D+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: draw" class="Draw" signature="aabb3D(context : Any, center : Any, radius : Any, style : Any)"></endpoint>
<signature id="Draw.aabb3D+4">Draw.aabb3D(**context**: `Any`, **center**: `Any`, **radius**: `Any`, **style**: `Any`)
<a class="headerlink" href="#Draw.aabb3D+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: draw" class="Draw" signature="plane3D(context : Draw, pos : Vec, normal : Vec, radius : Num, style : PathStyle)"></endpoint>
<signature id="Draw.plane3D+5">Draw.plane3D(**context**: `Draw`, **pos**: `Vec`, **normal**: `Vec`, **radius**: `Num`, **style**: `PathStyle`)
<a class="headerlink" href="#Draw.plane3D+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: draw" class="Draw" signature="plus3D(context : Draw, pos : Vec, radius : Num, style : PathStyle)"></endpoint>
<signature id="Draw.plus3D+4">Draw.plus3D(**context**: `Draw`, **pos**: `Vec`, **radius**: `Num`, **style**: `PathStyle`)
<a class="headerlink" href="#Draw.plus3D+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Draw a 3D plus at `pos` with size `radius` using `style`. 
> 
>   ```js
>   var style = PathStyle.new()
>   Draw.plus3D(canvas, [100,100,100], 4, style)
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="ring3D(context : Draw, pos : Vec3, radius : Vec2, start_angle : Num, end_angle : Num, smoothness : Num, style : PathStyle)"></endpoint>
<signature id="Draw.ring3D+7">Draw.ring3D(**context**: `Draw`, **pos**: `Vec3`, **radius**: `Vec2`, **start_angle**: `Num`, **end_angle**: `Num`, **smoothness**: `Num`, **style**: `PathStyle`)
<a class="headerlink" href="#Draw.ring3D+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Draw a 3D ring at `pos` with radius `[radius_x, radius_y]` using `style`. 
> 
>   ```js
>   var style = PathStyle.new()
>   Draw.ring3D(canvas, [100,100,100], [4, 4], 0, 360, smoothness, style)
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="plus(context : Draw, pos : Vec, radius : Num, style : PathStyle)"></endpoint>
<signature id="Draw.plus+4">Draw.plus(**context**: `Draw`, **pos**: `Vec`, **radius**: `Num`, **style**: `PathStyle`)
<a class="headerlink" href="#Draw.plus+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Draw a 2D plus at `pos` with size `radius` using `style`. 
> 
>   ```js
>   var style = PathStyle.new()
>   Draw.plus(canvas, [100,100], 20, style)
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="camera(context : Draw, camera : Entity, style : PathStyle)"></endpoint>
<signature id="Draw.camera+3">Draw.camera(**context**: `Draw`, **camera**: `Entity`, **style**: `PathStyle`)
<a class="headerlink" href="#Draw.camera+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Draw a 3D camera frustum for the given camera entity using `style`. 
> 
>   ```js
>   var style = PathStyle.new()
>   Draw.camera(canvas, camera, style)
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="frustum(context : Draw, corners : List, style : PathStyle)"></endpoint>
<signature id="Draw.frustum+3">Draw.frustum(**context**: `Draw`, **corners**: `List`, **style**: `PathStyle`)
<a class="headerlink" href="#Draw.frustum+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Draw a 3D camera frustum for the given 8 corner points using `style`.
> (You can get one from Camera.get_frustum(entity) for example, but can use Draw.camera as well).
> 
>   ```js
>   var style = PathStyle.new()
>   var corners = [
>     near_top_left, 
>     near_top_right, 
>     near_bottom_left, 
>     near_bottom_right,
>     far_top_left, 
>     far_top_right, 
>     far_bottom_left, 
>     far_bottom_right,
>   ]
>   Draw.frustum(canvas, corners, style)
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="text(context : Any, x : Any, y : Any, z : Any, w : Any, h : Any, string : Any, size : Any, font : Any, color : Any, align : Any, align_vertical : Any)"></endpoint>
<signature id="Draw.text+12">Draw.text(**context**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **string**: `Any`, **size**: `Any`, **font**: `Any`, **color**: `Any`, **align**: `Any`, **align_vertical**: `Any`)
<a class="headerlink" href="#Draw.text+12" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Draw the specified `string` at `x`,`y` and depth `z`. `w` and `h` specify the bounds for the text, bottom left origin, y going up. 
> The `size` specifies the text size, and `color` the color. `font` is a font asset, e.g Asset.font("luxe: font/lato"). 
> `align` and `align_vertical` control alignment within the bounds, 
> using the `TextAlign` enums such as `TextAlign.left`.
> 
>   ```js
>   var depth = 0
>   var size = 24
>   var red = [1,0,0,1]
>   Draw.text(canvas, 32, 32, depth, 100, 32, "hello", size, Asset.font("luxe: font/lato"), red, TextAlign.center, TextAlign.bottom)
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="text(context : Any, x : Any, y : Any, z : Any, string : Any, size : Any, font : Any, color : Any, align : Any, align_vertical : Any)"></endpoint>
<signature id="Draw.text+10">Draw.text(**context**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **string**: `Any`, **size**: `Any`, **font**: `Any`, **color**: `Any`, **align**: `Any`, **align_vertical**: `Any`)
<a class="headerlink" href="#Draw.text+10" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Draw the specified `string` at `x`,`y` and depth `z`. 
> The `size` specifies the text size, and `color` the color.  `font` is a font asset, e.g Asset.font("luxe: font/lato"). 
> `align` and `align_vertical` control alignment relative to the specified position, 
> using the `TextAlign` enums such as `TextAlign.left`.
> 
>   ```js
>   var depth = 0
>   var size = 24
>   var red = [1,0,0,1]
>   Draw.text(canvas, 32, 32, depth, "hello", size, Asset.font("luxe: font/lato"), red, TextAlign.center, TextAlign.bottom)
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="image(context : Any, x : Any, y : Any, z : Any, w : Any, h : Any, angle : Any, material : Any)"></endpoint>
<signature id="Draw.image+8">Draw.image(**context**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **material**: `Any`)
<a class="headerlink" href="#Draw.image+8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Draw an image with the specified `material` at `x`,`y` and depth `z`. 
> The image will be rotated by `angle` degrees.
> 
>   ```js
>   var depth = 0
>   var angle = 30
>   var material = Assets.material("luxe: material/logo.sprite")
>   Draw.image(canvas, 128, 128, depth, 64, 64, angle, material)
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="image(context : Any, x : Any, y : Any, z : Any, w : Any, h : Any, angle : Any, color : Any, uv : Any, material : Any)"></endpoint>
<signature id="Draw.image+10">Draw.image(**context**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **color**: `Any`, **uv**: `Any`, **material**: `Any`)
<a class="headerlink" href="#Draw.image+10" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Draw an image with the specified `material` at `x`,`y` and depth `z`. 
> The image will be rotated by `angle` degrees. 
> 
> The `uv` value specifies a fixed rectangle like `[left, top, right, bottom]` in the `0..1` range,
> where `[0,0,1,1]` is the default and displays the full image. 
> A `uv` value of `[0.5, 0, 1, 0.5]` would draw the top right corner of the image only.
> A `uv` value of `[0, 0, 4, 4]` would tile the image 4 times _(as long as the material has a repeat mode for the image)._
> 
>   ```js
>   var depth = 0
>   var angle = 30
>   var material = Assets.material("luxe: material/logo.sprite")
>   var uv = [0, 0.5, 0, 1] //bottom right
>   Draw.image(canvas, 128, 128, depth, 64, 64, angle, uv, material)
>   ```   

<endpoint module="luxe: draw" class="Draw" signature="cross(context : Any, x : Any, y : Any, z : Any, radius : Any, angle : Any, style : Any)"></endpoint>
<signature id="Draw.cross+7">Draw.cross(**context**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **radius**: `Any`, **angle**: `Any`, **style**: `Any`)
<a class="headerlink" href="#Draw.cross+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Draws a cross, an x shape   

### LineCap
`:::js import "luxe: draw" for LineCap`
> The end of a line is called a "cap", when drawing paths, this determines the type of cap that a line will have. :todo: images

- [butt](#LineCap.butt)
- [round](#LineCap.round)
- [square](#LineCap.square)
- [from_string](#LineCap.from_string)(**value**: `Any`)

<hr/>
<endpoint module="luxe: draw" class="LineCap" signature="butt"></endpoint>
<signature id="LineCap.butt">LineCap.butt
<a class="headerlink" href="#LineCap.butt" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> This cap is as if there was no cap, the line is just ended. The default.
> 
>   ```js
>   var style = PathStyle.new()
>       style.cap = LineCap.butt
>   ```   

<endpoint module="luxe: draw" class="LineCap" signature="round"></endpoint>
<signature id="LineCap.round">LineCap.round
<a class="headerlink" href="#LineCap.round" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> A round cap is a half circle at the end of the line.
> 
>   ```js
>   var style = PathStyle.new()
>       style.cap = LineCap.round
>   ```   

<endpoint module="luxe: draw" class="LineCap" signature="square"></endpoint>
<signature id="LineCap.square">LineCap.square
<a class="headerlink" href="#LineCap.square" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> A square cap is a square at the end of the line.
> 
>   ```js
>   var style = PathStyle.new()
>       style.cap = LineCap.square
>   ```   

<endpoint module="luxe: draw" class="LineCap" signature="from_string(value : Any)"></endpoint>
<signature id="LineCap.from_string">LineCap.from_string(**value**: `Any`)
<a class="headerlink" href="#LineCap.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Convert a string to a LineCap value.
> 
>   ```js
>   Log.print(LineCap.round == LineCap.from_string("round")) //true
>   ```   

### LineJoin
`:::js import "luxe: draw" for LineJoin`
> When drawing a path, a series of lines will be drawn and joined together.
> The join of each connection can be configured when drawing paths using `LineJoin`.
> :todo: images

- [bevel](#LineJoin.bevel)
- [round](#LineJoin.round)
- [miter](#LineJoin.miter)
- [from_string](#LineJoin.from_string)(**value**: `Any`)

<hr/>
<endpoint module="luxe: draw" class="LineJoin" signature="bevel"></endpoint>
<signature id="LineJoin.bevel">LineJoin.bevel
<a class="headerlink" href="#LineJoin.bevel" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> The default join is a bevel, which is a flat join.
> 
>   ```js
>   var style = PathStyle.new()
>       style.join = LineJoin.bevel
>   ```   

<endpoint module="luxe: draw" class="LineJoin" signature="round"></endpoint>
<signature id="LineJoin.round">LineJoin.round
<a class="headerlink" href="#LineJoin.round" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> A round join is a semi circle that makes the corner rounded.
> 
>   ```js
>   var style = PathStyle.new()
>       style.join = LineJoin.round
>   ```   

<endpoint module="luxe: draw" class="LineJoin" signature="miter"></endpoint>
<signature id="LineJoin.miter">LineJoin.miter
<a class="headerlink" href="#LineJoin.miter" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> A miter join is a sharp triangle join that has a limit value (which falls back to bevel).
> 
>   ```js
>   var style = PathStyle.new()
>       style.join = LineJoin.miter
>       style.miter_limit = 8
>   ```   

<endpoint module="luxe: draw" class="LineJoin" signature="from_string(value : Any)"></endpoint>
<signature id="LineJoin.from_string">LineJoin.from_string(**value**: `Any`)
<a class="headerlink" href="#LineJoin.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Convert a string to a LineJoin value.
> 
>   ```js
>   Log.print(LineJoin.round == LineJoin.from_string("round")) //true
>   ```   

### PathStyle
`:::js import "luxe: draw" for PathStyle`
> 

- [array](#PathStyle.array)
- [color](#PathStyle.color)
- [color](#PathStyle.color=)=(value : Any)
- [alpha](#PathStyle.alpha)
- [alpha](#PathStyle.alpha=)=(value : Any)
- [thickness](#PathStyle.thickness)
- [thickness](#PathStyle.thickness=)=(value : Any)
- [feather](#PathStyle.feather)
- [feather](#PathStyle.feather=)=(value : Any)
- [cap](#PathStyle.cap)
- [cap](#PathStyle.cap=)=(value : Any)
- [join](#PathStyle.join)
- [join](#PathStyle.join=)=(value : Any)
- [miter_limit](#PathStyle.miter_limit)
- [miter_limit](#PathStyle.miter_limit=)=(value : Any)
- [new](#PathStyle.new)()

<hr/>
<endpoint module="luxe: draw" class="PathStyle" signature="array"></endpoint>
<signature id="PathStyle.array">PathStyle.array
<a class="headerlink" href="#PathStyle.array" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: draw" class="PathStyle" signature="color"></endpoint>
<signature id="PathStyle.color">PathStyle.color
<a class="headerlink" href="#PathStyle.color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns the color of the path style.
> 
>   ```js
>   var style = PathStyle.new()
>   var color = style.color //the default color
>   ```   

<endpoint module="luxe: draw" class="PathStyle" signature="color=(value : Any)"></endpoint>
<signature id="PathStyle.color=">PathStyle.color=(value : Any)
<a class="headerlink" href="#PathStyle.color=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Set the color for the style.
> 
>   ```js
>   var style = PathStyle.new()
>   style.color = [0, 0, 0, 1] //black
>   ```   

<endpoint module="luxe: draw" class="PathStyle" signature="alpha"></endpoint>
<signature id="PathStyle.alpha">PathStyle.alpha
<a class="headerlink" href="#PathStyle.alpha" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns the alpha from the color of the path style.
> 
>   ```js
>   var style = PathStyle.new()
>   var color = style.alpha //the alpha value of the default color
>   ```   

<endpoint module="luxe: draw" class="PathStyle" signature="alpha=(value : Any)"></endpoint>
<signature id="PathStyle.alpha=">PathStyle.alpha=(value : Any)
<a class="headerlink" href="#PathStyle.alpha=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Set the alpha of the color for the style.
> 
>   ```js
>   var style = PathStyle.new()
>   style.alpha = 0.5 //half alpha
>   ```   

<endpoint module="luxe: draw" class="PathStyle" signature="thickness"></endpoint>
<signature id="PathStyle.thickness">PathStyle.thickness
<a class="headerlink" href="#PathStyle.thickness" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns the thickness of the path style.
> 
>   ```js
>   var style = PathStyle.new()
>   Log.print(style.thickness) //1
>   ```   

<endpoint module="luxe: draw" class="PathStyle" signature="thickness=(value : Any)"></endpoint>
<signature id="PathStyle.thickness=">PathStyle.thickness=(value : Any)
<a class="headerlink" href="#PathStyle.thickness=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Set the thickness of the path style.
> 
>   ```js
>   var style = PathStyle.new()
>   style.thickness = 4
>   ```   

<endpoint module="luxe: draw" class="PathStyle" signature="feather"></endpoint>
<signature id="PathStyle.feather">PathStyle.feather
<a class="headerlink" href="#PathStyle.feather" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns the feather value for the path style. 
> Note: not used much at the moment.
> 
>   ```js
>   var style = PathStyle.new()
>   var feather = style.feather
>   ```   

<endpoint module="luxe: draw" class="PathStyle" signature="feather=(value : Any)"></endpoint>
<signature id="PathStyle.feather=">PathStyle.feather=(value : Any)
<a class="headerlink" href="#PathStyle.feather=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Set the feather value for the path style. 
> Note: not used much at the moment.
> 
>   ```js
>   var style = PathStyle.new()
>   style.feather = 2
>   ```   

<endpoint module="luxe: draw" class="PathStyle" signature="cap"></endpoint>
<signature id="PathStyle.cap">PathStyle.cap
<a class="headerlink" href="#PathStyle.cap" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns the `LineCap` type for the path style.
> 
>   ```js
>   var style = PathStyle.new()
>   var cap = style.cap
>   ```   

<endpoint module="luxe: draw" class="PathStyle" signature="cap=(value : Any)"></endpoint>
<signature id="PathStyle.cap=">PathStyle.cap=(value : Any)
<a class="headerlink" href="#PathStyle.cap=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Set the `LineCap` type for the path style.
> 
>   ```js
>   var style = PathStyle.new()
>   style.cap = LineCap.round
>   ```   

<endpoint module="luxe: draw" class="PathStyle" signature="join"></endpoint>
<signature id="PathStyle.join">PathStyle.join
<a class="headerlink" href="#PathStyle.join" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns the `LineJoin` type for the path style.
> 
>   ```js
>   var style = PathStyle.new()
>   var join = style.join
>   ```   

<endpoint module="luxe: draw" class="PathStyle" signature="join=(value : Any)"></endpoint>
<signature id="PathStyle.join=">PathStyle.join=(value : Any)
<a class="headerlink" href="#PathStyle.join=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Set the `LineJoin` type for the path style.
> 
>   ```js
>   var style = PathStyle.new()
>   style.cap = LineJoin.round
>   ```   

<endpoint module="luxe: draw" class="PathStyle" signature="miter_limit"></endpoint>
<signature id="PathStyle.miter_limit">PathStyle.miter_limit
<a class="headerlink" href="#PathStyle.miter_limit" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns the miter limit for the path style.
> Only relevant if the `join` type is `LineJoin.miter`.
> 
>   ```js
>   var style = PathStyle.new()
>   var limit = style.miter_limit
>   ```   

<endpoint module="luxe: draw" class="PathStyle" signature="miter_limit=(value : Any)"></endpoint>
<signature id="PathStyle.miter_limit=">PathStyle.miter_limit=(value : Any)
<a class="headerlink" href="#PathStyle.miter_limit=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Set the miter limit for the path style.
> Only relevant if the `join` type is `LineJoin.miter`.
> 
>   ```js
>   var style = PathStyle.new()
>   style.miter_limit = 8
>   ```   

<endpoint module="luxe: draw" class="PathStyle" signature="new()"></endpoint>
<signature id="PathStyle.new">PathStyle.new()
<a class="headerlink" href="#PathStyle.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js PathStyle`
> Create a new `PathStyle` instance.
> 
>   ```js
>   var style = PathStyle.new()
>   style.color = [1,0,0,1]
>   style.thickness = 2
>   style.join = LineJoin.round
>   //use style
>   //...
>   style.thickness = 1
>   //use style again...
>   ```   

