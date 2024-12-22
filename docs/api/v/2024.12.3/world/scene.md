#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2024.12.3`)  


---

## `luxe: world/scene` module

- [Scene](#scene)   
- [SceneReady](#sceneready)   
- [Stage](#stage)   

---

### Scene
`:::js import "luxe: world/scene" for Scene`
> no docs found

- [create](#Scene.create+2)(**world**: `World`, **scene**: `Scene`)
- [create](#Scene.create+3)(**world**: `World`, **scene**: `Scene`, **on_ready**: `Fn`)
- [has](#Scene.has)(**entity**: `Entity`)

<hr/>
<endpoint module="luxe: world/scene" class="Scene" signature="create(world : World, scene : Scene)"></endpoint>
<signature id="Scene.create+2">Scene.create(**world**: `World`, **scene**: `Scene`)
<a class="headerlink" href="#Scene.create+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/scene" class="Scene" signature="create(world : World, scene : Scene, on_ready : Fn)"></endpoint>
<signature id="Scene.create+3">Scene.create(**world**: `World`, **scene**: `Scene`, **on_ready**: `Fn`)
<a class="headerlink" href="#Scene.create+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/scene" class="Scene" signature="has(entity : Entity)"></endpoint>
<signature id="Scene.has">Scene.has(**entity**: `Entity`)
<a class="headerlink" href="#Scene.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### SceneReady
`:::js import "luxe: world/scene" for SceneReady`
> no docs found

- `:::js var world : World = 0`
- `:::js var scene : Entity = Entity.none`
- [new](#SceneReady.new+2)(**world**: `World`, **scene**: `Entity`)
- [editor_new](#SceneReady.editor_new+2)(**world**: `World`, **scene**: `Entity`)
- [ready](#SceneReady.ready+2)(**world**: `World`, **scene**: `Entity`)
- [ready](#SceneReady.ready)()
- [editor_ready](#SceneReady.editor_ready+2)(**world**: `World`, **scene**: `Entity`)
- [editor_ready](#SceneReady.editor_ready)()
- [tick](#SceneReady.tick)(**delta**: `Num`)
- [editor_tick](#SceneReady.editor_tick)(**delta**: `Num`)
- [destroy](#SceneReady.destroy+2)(**world**: `World`, **scene**: `Entity`)
- [destroy](#SceneReady.destroy)()
- [editor_destroy](#SceneReady.editor_destroy+2)(**world**: `World`, **scene**: `Entity`)
- [editor_destroy](#SceneReady.editor_destroy)()

<hr/>
<endpoint module="luxe: world/scene" class="SceneReady" signature="new(world : World, scene : Entity)"></endpoint>
<signature id="SceneReady.new+2">SceneReady.new(**world**: `World`, **scene**: `Entity`)
<a class="headerlink" href="#SceneReady.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js SceneReady`
> no docs found   

<endpoint module="luxe: world/scene" class="SceneReady" signature="editor_new(world : World, scene : Entity)"></endpoint>
<signature id="SceneReady.editor_new+2">SceneReady.editor_new(**world**: `World`, **scene**: `Entity`)
<a class="headerlink" href="#SceneReady.editor_new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js SceneReady`
> no docs found   

<endpoint module="luxe: world/scene" class="SceneReady" signature="ready(world : World, scene : Entity)"></endpoint>
<signature id="SceneReady.ready+2">SceneReady.ready(**world**: `World`, **scene**: `Entity`)
<a class="headerlink" href="#SceneReady.ready+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/scene" class="SceneReady" signature="ready()"></endpoint>
<signature id="SceneReady.ready">SceneReady.ready()
<a class="headerlink" href="#SceneReady.ready" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/scene" class="SceneReady" signature="editor_ready(world : World, scene : Entity)"></endpoint>
<signature id="SceneReady.editor_ready+2">SceneReady.editor_ready(**world**: `World`, **scene**: `Entity`)
<a class="headerlink" href="#SceneReady.editor_ready+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/scene" class="SceneReady" signature="editor_ready()"></endpoint>
<signature id="SceneReady.editor_ready">SceneReady.editor_ready()
<a class="headerlink" href="#SceneReady.editor_ready" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/scene" class="SceneReady" signature="tick(delta : Num)"></endpoint>
<signature id="SceneReady.tick">SceneReady.tick(**delta**: `Num`)
<a class="headerlink" href="#SceneReady.tick" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/scene" class="SceneReady" signature="editor_tick(delta : Num)"></endpoint>
<signature id="SceneReady.editor_tick">SceneReady.editor_tick(**delta**: `Num`)
<a class="headerlink" href="#SceneReady.editor_tick" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/scene" class="SceneReady" signature="destroy(world : World, scene : Entity)"></endpoint>
<signature id="SceneReady.destroy+2">SceneReady.destroy(**world**: `World`, **scene**: `Entity`)
<a class="headerlink" href="#SceneReady.destroy+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/scene" class="SceneReady" signature="destroy()"></endpoint>
<signature id="SceneReady.destroy">SceneReady.destroy()
<a class="headerlink" href="#SceneReady.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/scene" class="SceneReady" signature="editor_destroy(world : World, scene : Entity)"></endpoint>
<signature id="SceneReady.editor_destroy+2">SceneReady.editor_destroy(**world**: `World`, **scene**: `Entity`)
<a class="headerlink" href="#SceneReady.editor_destroy+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world/scene" class="SceneReady" signature="editor_destroy()"></endpoint>
<signature id="SceneReady.editor_destroy">SceneReady.editor_destroy()
<a class="headerlink" href="#SceneReady.editor_destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Stage
`:::js import "luxe: world/scene" for Stage`
> no docs found

- [create](#Stage.create+2)(**world**: `World`, **stage**: `Stage`)

<hr/>
<endpoint module="luxe: world/scene" class="Stage" signature="create(world : World, stage : Stage)"></endpoint>
<signature id="Stage.create+2">Stage.create(**world**: `World`, **stage**: `Stage`)
<a class="headerlink" href="#Stage.create+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

