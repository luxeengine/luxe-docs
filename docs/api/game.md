#![](../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2021.0.9`)  


---

## `luxe: game` module

- [Frame](#frame)   
- [Ready](#ready)   

---

### Frame
`:::js import "luxe: game" for Frame`
> Access to the frame and game loop. 
> At the moment, the loop contains fixed sections,
> `begin` -> `init` -> `sim` -> `visual` -> `end`.
> 
> Functions can be hooked into sections of the frame using `before`,
> `after` or `on` ordering.
> 
> Note: This API is a work in progress.

- [begin](#Frame.begin)
- [init](#Frame.init)
- [sim](#Frame.sim)
- [visual](#Frame.visual)
- [end](#Frame.end)
- [queue](#Frame.queue)(**fn**: `Any`)
- [next](#Frame.next)(**fn**: `Any`)
- [end](#Frame.end)(**fn**: `Any`)
- [schedule](#Frame.schedule+2)(**time**: `Num`, **fn**: `Num`)
- [schedule](#Frame.schedule+3)(**time**: `Num`, **count**: `Num`, **fn**: `Fn`)
- [unschedule](#Frame.unschedule)(**handle**: `Handle`)
- [off](#Frame.off)(**handle**: `Handle`)
- [on](#Frame.on+3)(**section**: `Any`, **priority**: `Any`, **fn**: `Fn`)
- [before](#Frame.before+3)(**section**: `Any`, **priority**: `Any`, **fn**: `Fn`)
- [after](#Frame.after+3)(**section**: `Any`, **priority**: `Any`, **fn**: `Fn`)
- [on](#Frame.on+2)(**section**: `String`, **fn**: `Fn`)
- [before](#Frame.before+2)(**section**: `Any`, **fn**: `Fn`)
- [after](#Frame.after+2)(**section**: `Any`, **fn**: `Any`)

<hr/>
<endpoint module="luxe: game" class="Frame" signature="begin"></endpoint>
<signature id="Frame.begin">Frame.begin
<a class="headerlink" href="#Frame.begin" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> An enum value for the `begin` section in the loop.
> The `begin section is the start of the frame from the game's perspective.
> 
>   ```js
>   Frame.on(Frame.begin) {|delta| ... }
>   ```   

<endpoint module="luxe: game" class="Frame" signature="init"></endpoint>
<signature id="Frame.init">Frame.init
<a class="headerlink" href="#Frame.init" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> An enum value for the `init` section in the loop.
> The `init` section is used for initialization tasks that happen before
> updates, like when a new entity is created, it can be added to a queue and
> processed in init to set some default values before it arrives in `sim` or `visual`.
>     
>   ```js
>   Frame.on(Frame.init) {|delta| ... }
>   ```   

<endpoint module="luxe: game" class="Frame" signature="sim"></endpoint>
<signature id="Frame.sim">Frame.sim
<a class="headerlink" href="#Frame.sim" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> An enum value for the `sim` section in the loop.
> The `sim` section is for simulation, also known as `update`. 
> In this section you would update game logic and modify things that the `visual` section would reference.
> 
>   ```js
>   Frame.on(Frame.sim) {|delta| ... }
>   ```   

<endpoint module="luxe: game" class="Frame" signature="visual"></endpoint>
<signature id="Frame.visual">Frame.visual
<a class="headerlink" href="#Frame.visual" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> An enum value for the `visual` section in the loop.
> The `visual` section is for rendering, also known as `render`.
> Updating visual state from the sim states happens here.
> 
>   ```js
>   Frame.on(Frame.visual) {|delta| ... }
>   ```   

<endpoint module="luxe: game" class="Frame" signature="end"></endpoint>
<signature id="Frame.end">Frame.end
<a class="headerlink" href="#Frame.end" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> An enum value for the `end` section in the loop.
> The `end` of the loop can perform tasks after rendering and simulation.
> 
>   ```js
>   Frame.on(Frame.end) {|delta| ... }
>   ```   

<endpoint module="luxe: game" class="Frame" signature="queue(fn : Any)"></endpoint>
<signature id="Frame.queue">Frame.queue(**fn**: `Any`)
<a class="headerlink" href="#Frame.queue" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> **Once off**. Queue a function to be called after the current section has completed fully.
> That is, if we were inside of `sim` and we queued a function, it would happen after `before` `on` and `after`.
> 
> This is used for systems that fire callbacks, you normally don't want to fire callbacks during processing,
> so you can queue them to happen "as soon as possible" but in a well defined place and time.
> 
>   ```js
>   Frame.queue {
>     System.print("happens at the end of the current section")
>   }
> 
>   //fake example: collision callbacks
>   for(entity in collidable) {
>     if(collides(entity)) {
>       var fn = callbacks[entity]
>       Frame.queue { fn.call() }
>     }
>   }
>   ```   

<endpoint module="luxe: game" class="Frame" signature="next(fn : Any)"></endpoint>
<signature id="Frame.next">Frame.next(**fn**: `Any`)
<a class="headerlink" href="#Frame.next" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> **Once off**. Queue a function to be called at the beginning of the next frame, 
> before any sections.
> 
>   ```js
>   Frame.next {
>     System.print("next frame!")
>   }
> 
>   //common example, destroying an entity when it might
>   //not be safe to. Instead, just destroy it later
>   for(entity in list ) {
>     Frame.next { Entity.destroy(entity) }
>   }
>   ```   

<endpoint module="luxe: game" class="Frame" signature="end(fn : Any)"></endpoint>
<signature id="Frame.end">Frame.end(**fn**: `Any`)
<a class="headerlink" href="#Frame.end" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> **Once off**. Queue a function to be called at the end of the current frame,
> after all sections.
> 
>   ```js
>   Frame.end {
>     System.print("end frame!")
>   }
>   ```   

<endpoint module="luxe: game" class="Frame" signature="schedule(time : Num, fn : Num)"></endpoint>
<signature id="Frame.schedule+2">Frame.schedule(**time**: `Num`, **fn**: `Num`)
<a class="headerlink" href="#Frame.schedule+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Handle`
> Schedule a function to be called in future. 
> The `time` value is in seconds, and is not affected by any time scaling.
> The function is only called once. To repeat, see the other `schedule` method.   

<endpoint module="luxe: game" class="Frame" signature="schedule(time : Num, count : Num, fn : Fn)"></endpoint>
<signature id="Frame.schedule+3">Frame.schedule(**time**: `Num`, **count**: `Num`, **fn**: `Fn`)
<a class="headerlink" href="#Frame.schedule+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Handle`
> Schedule a function to be called in future. 
> The `time` value is in seconds, and is not affected by any time scaling.
> If `count` is 0, the function will be called repeatedly until `unschedule` is called.   

<endpoint module="luxe: game" class="Frame" signature="unschedule(handle : Handle)"></endpoint>
<signature id="Frame.unschedule">Frame.unschedule(**handle**: `Handle`)
<a class="headerlink" href="#Frame.unschedule" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Unschedule a function scheduled previously, using the handle returned from `schedule`.   

<endpoint module="luxe: game" class="Frame" signature="off(handle : Handle)"></endpoint>
<signature id="Frame.off">Frame.off(**handle**: `Handle`)
<a class="headerlink" href="#Frame.off" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Disconnect a function using the handle returned from one of the recurring functions.
> This will remove the function from the loop and it will no longer be called.
> 
> Returns true if the function was valid and removed.
> 
>   ```js
>   var tick = Frame.on(Frame.sim) {|delta| System.print("delta:%(delta)") }
>   //...
>   Frame.off(tick)
>   ```   

<endpoint module="luxe: game" class="Frame" signature="on(section : Any, priority : Any, fn : Fn)"></endpoint>
<signature id="Frame.on+3">Frame.on(**section**: `Any`, **priority**: `Any`, **fn**: `Fn`)
<a class="headerlink" href="#Frame.on+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Handle`
> Connect a function to the specified section, with a given priority which will be executed _during_ the section.
> Priority is based on "highest priority first". So priority 1 executes before 0.
> 
> Returns a handle that can be used to remove the function via `off`.
> 
>   ```js
>   Frame.on(Frame.sim, 3) {|delta| System.print("prints first") }
>   Frame.on(Frame.sim, 1) {|delta| System.print("prints second") }
>   ```   

<endpoint module="luxe: game" class="Frame" signature="before(section : Any, priority : Any, fn : Fn)"></endpoint>
<signature id="Frame.before+3">Frame.before(**section**: `Any`, **priority**: `Any`, **fn**: `Fn`)
<a class="headerlink" href="#Frame.before+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Handle`
> Connect a function to the specified section, with a given priority which will be executed _before_ the section.
> Priority is based on "highest priority first". So priority 1 executes before 0.
> 
> Returns a handle that can be used to remove the function via `off`.
> 
>   ```js
>   Frame.before(Frame.sim, 0) {|delta| System.print("prints second") }
>   Frame.before(Frame.sim, 1) {|delta| System.print("prints first") }
>   ```   

<endpoint module="luxe: game" class="Frame" signature="after(section : Any, priority : Any, fn : Fn)"></endpoint>
<signature id="Frame.after+3">Frame.after(**section**: `Any`, **priority**: `Any`, **fn**: `Fn`)
<a class="headerlink" href="#Frame.after+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Handle`
> Connect a function to the specified section, with a given priority which will be executed _after_ the section.
> Priority is based on "highest priority first". So priority 1 executes before 0.
> 
> Returns a handle that can be used to remove the function via `off`.
> 
>   ```js
>   Frame.after(Frame.sim, 2) {|delta| System.print("prints first") }
>   Frame.after(Frame.sim, 1) {|delta| System.print("prints second") }
>   ```   

<endpoint module="luxe: game" class="Frame" signature="on(section : String, fn : Fn)"></endpoint>
<signature id="Frame.on+2">Frame.on(**section**: `String`, **fn**: `Fn`)
<a class="headerlink" href="#Frame.on+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Handle`
> Connect a function to the specified section (with priority 0) which will be executed _during_ the section.
> 
> Returns a handle that can be used to remove the function via `off`.
> 
>   ```js
>   Frame.on(Frame.sim) {|delta| System.print("delta:%(delta)") }
>   ```   

<endpoint module="luxe: game" class="Frame" signature="before(section : Any, fn : Fn)"></endpoint>
<signature id="Frame.before+2">Frame.before(**section**: `Any`, **fn**: `Fn`)
<a class="headerlink" href="#Frame.before+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Handle`
> Connect a function to the specified section (with priority 0) which will be executed _before_ the section.
> 
> Returns a handle that can be used to remove the function via `off`.
> 
>   ```js
>   Frame.before(Frame.sim) {|delta| System.print("delta:%(delta)") }
>   ```   

<endpoint module="luxe: game" class="Frame" signature="after(section : Any, fn : Any)"></endpoint>
<signature id="Frame.after+2">Frame.after(**section**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#Frame.after+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Connect a function to the specified section (with priority 0) which will be executed _after_ the section.
> 
> Returns a handle that can be used to remove the function via `off`.
> 
>   ```js
>   Frame.after(Frame.sim) {|delta| System.print("delta:%(delta)") }
>   ```   

### Ready
`:::js import "luxe: game" for Ready`
> The base class for a luxe game.

- [ready](#Ready.ready)()
- [ready](#Ready.ready)(**message**: `Any`)
- [tick](#Ready.tick)(**delta**: `Any`)
- [destroy](#Ready.destroy)()

<hr/>
<endpoint module="luxe: game" class="Ready" signature="ready()"></endpoint>
<signature id="Ready.ready">Ready.ready()
<a class="headerlink" href="#Ready.ready" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Called via `super()` inside your `ready` function. Must be called.   

<endpoint module="luxe: game" class="Ready" signature="ready(message : Any)"></endpoint>
<signature id="Ready.ready">Ready.ready(**message**: `Any`)
<a class="headerlink" href="#Ready.ready" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Called via `super(message)` inside your `ready` function. Must be called.   

<endpoint module="luxe: game" class="Ready" signature="tick(delta : Any)"></endpoint>
<signature id="Ready.tick">Ready.tick(**delta**: `Any`)
<a class="headerlink" href="#Ready.tick" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> A default implementation for tick.   

<endpoint module="luxe: game" class="Ready" signature="destroy()"></endpoint>
<signature id="Ready.destroy">Ready.destroy()
<a class="headerlink" href="#Ready.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> A default implementation for destroy.   

