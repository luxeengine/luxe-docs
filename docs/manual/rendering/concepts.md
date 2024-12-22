# Rendering concepts

The below is a list of key concepts the luxe renderer uses, based on this set of questions:

- What is rendered? (Geometry)
- What controls how that looks? (Materials)
- How is it decided what gets rendered? (Render Set)
- What happens during rendering? (Render Path)
- Where does the rendering end up? (Resources/Render Targets/Target Region)

Many of these concepts will be expanded in detail in the pipeline section, 
but are important to understand how rendering fits together.

## Geometry
_What is rendered?_

In luxe the basic unit of work for the renderer is called [Geometry](../../../api/render/#geometry).    
Geometry is a container for vertex buffers, a vertex count, and a material. 

A vertex buffer contains information for the geometry such as positions, colors or uvs, which get handed to the GPU, and the vert count controls how many vertices for this geometry will get drawn. 

## Materials
_What controls how that looks?_

A material controls what geometry will look like once rendered: which shaders are used, what material inputs are set, and what blend modes are active. 

A material **basis** defines a _type_ of material, and a material **instance** customizes the type with different material input values. 

A basis is typically defined in a `material.basis.lx` asset, and an instance inside a `material.lx` asset.

## Render Set
_How is it decided what gets rendered?_

A render set is **a list of `Geometry`**.    

In luxe, when submitting a render, a `set` is passed in to tell the renderer what geometry to draw.   
On the **high level**, each world has a render set, and when rendered, submits it.   

On the **low level** you can make your own render set via `var set = Render.create_set()`.   

- use `Render.set_add(set, geometry)` to add,
- or `Render.set_remove(set, geometry)` to remove

**A render set is how you control visibility of geometry.**   
To hide an object, remove it from the set.

## Render Graph
_What happens during rendering?_

Rendering in luxe is designed as a Render Graph, a scriptable one.

With a render graph, you describe what you want to happen,   
and the renderer will execute the set of steps when it is time.
The _path_ taken contains the steps to execute.

!!! note ""
    At the moment, the render graph is scripted only,   
    but in future will be a visual node based graph too.

## Render Path
_What happens during rendering?_

A render path is what contains the steps to execute.   
This is "the path that the renderer will take" when submitting.   

In the scripted render graph, you can add `layers` which are executed in order.

There's a `render layer` which renders geometry from a `set`.   
There's also a `pass layer` which renders a fullscreen pass (as a triangle). 

In each case, a layer contains configuration including a destination target.

## Render Targets (resources)
_Where does the rendering end up?_

Rendering ends up in a render target, which is an image that has been defined as a _resource_, and given a name. **An image must be defined as a resource first**, to be rendered to. The render graph speaks about these resources by name when deciding where to render. 

Using `Render.define_resource(name, image)` will define a resource pointing to the given image will be defined.

#### Special targets

**`screen`**   
Refers to the target window/primary backbuffer _(likely a better name will come later)_

**`target`**   
This refers to "the target resource on the submit". 

Both world and direct rendering can take a resource name to render to. 
Any graph nodes that specify `target` will draw into the resource from the submission, 
because often they won't know the name of the target resource directly. This also means you can share
render paths across multiple different renders into different targets because their name won't be hardcoded.

An example: you're rendering a world into a resource called `scene`. 
Inside the render graph, you have to render something into a lower res target called `scene_low_res` and blur it.
Then, you combine that with the other stuff into `scene`, by using `target` as the destination.


## Target Region

In luxe rendering, a target region is defined as `x, y, w, h`, but with values in the `0...1` range.

A full screen region would be `0 0 1 1`, where `1` is the full width and height.   
A region of `0.5 0 0.5 1` would be a split screen region (right hand side).

This is because in the majority of cases, you don't want to encode a resolution into the viewport. 
Doing so makes the viewport size stateful, and means that if the resolution changes, all values become wrong.

By making the values map automatically to the destination target size, you are more often expressing intent rather than state.
Some examples: split screen is always 0.5, regardless of resolution. A minimap might always be 10% of the screen size. 

This avoids a large class of bugs that are hard to debug, 
but does require some viewport calculations to happen on your end if doing subregions.