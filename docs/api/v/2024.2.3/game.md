#![](../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2024.2.3`)  


---

## `luxe: game` module

- [Frame](#frame)   
- [FrameSection](#framesection)   
- [FrameWhen](#framewhen)   
- [Ready](#ready)   

---

### Frame
`:::js import "luxe: game" for Frame`
> Access to the frame and game loop. 
> At the moment, the loop contains fixed sections,
> `begin` -> `init` -> `sim` -> `visual` -> `debug` -> `end`.
> 
> Functions can be hooked into sections of the frame using `before`,
> `after` or `on` ordering.
> 
> Note: This API is a work in progress.

- [begin](#Frame.begin)
- [init](#Frame.init)
- [sim](#Frame.sim)
- [visual](#Frame.visual)
- [debug](#Frame.debug)
- [end](#Frame.end)
- [queue](#Frame.queue)(**fn**: `Fn`)
- [next](#Frame.next)(**fn**: `Fn`)
- [end](#Frame.end)(**fn**: `Fn`)
- [schedule](#Frame.schedule+2)(**time**: `Num`, **fn**: `Fn`)
- [schedule](#Frame.schedule+3)(**time**: `Num`, **count**: `Num`, **fn**: `Fn`)
- [unschedule](#Frame.unschedule)(**handle**: `Handle`)
- [off](#Frame.off)(**handle**: `Handle`)
- [once](#Frame.once+3)(**section**: `String`, **priority**: `Num`, **fn**: `Fn`)
- [on](#Frame.on+3)(**section**: `String`, **priority**: `Num`, **fn**: `Fn`)
- [before](#Frame.before+3)(**section**: `String`, **priority**: `Num`, **fn**: `Fn`)
- [after](#Frame.after+3)(**section**: `String`, **priority**: `Num`, **fn**: `Fn`)
- [on](#Frame.on+2)(**section**: `String`, **fn**: `Fn`)
- [once](#Frame.once+2)(**section**: `String`, **fn**: `Fn`)
- [before](#Frame.before+2)(**section**: `String`, **fn**: `Fn`)
- [after](#Frame.after+2)(**section**: `String`, **fn**: `Fn`)
- [skip](#Frame.skip+2)(**count_frames**: `Num`, **fn**: `Fn`)
- [mark](#Frame.mark+2)(**id**: `String`, **display**: `String`)
- [get_marks](#Frame.get_marks)(**frame_index**: `Num`)
- [index](#Frame.index)
- [delta](#Frame.delta)

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

<endpoint module="luxe: game" class="Frame" signature="debug"></endpoint>
<signature id="Frame.debug">Frame.debug
<a class="headerlink" href="#Frame.debug" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> An enum value for the `debug` section in the loop.
> The `debug` part of the loop can perform debug related tasks before the end of the frame and rendering is submitted.
> 
>   ```js
>   Frame.on(Frame.debug) {|delta| ... }
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

<endpoint module="luxe: game" class="Frame" signature="queue(fn : Fn)"></endpoint>
<signature id="Frame.queue">Frame.queue(**fn**: `Fn`)
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
>     Log.print("happens at the end of the current section")
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

<endpoint module="luxe: game" class="Frame" signature="next(fn : Fn)"></endpoint>
<signature id="Frame.next">Frame.next(**fn**: `Fn`)
<a class="headerlink" href="#Frame.next" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> **Once off**. Queue a function to be called at the beginning of the next frame, 
> before any sections.
> 
>   ```js
>   Frame.next {
>     Log.print("next frame!")
>   }
> 
>   //common example, destroying something when it might
>   //not be safe to. Instead, just destroy it later
>   for(thing in list) {
>     Frame.next { Thing.destroy(thing) }
>   }
>   ```   

<endpoint module="luxe: game" class="Frame" signature="end(fn : Fn)"></endpoint>
<signature id="Frame.end">Frame.end(**fn**: `Fn`)
<a class="headerlink" href="#Frame.end" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> **Once off**. Queue a function to be called at the end of the current frame,
> after all sections.
> 
>   ```js
>   Frame.end {
>     Log.print("end frame!")
>   }
>   ```   

<endpoint module="luxe: game" class="Frame" signature="schedule(time : Num, fn : Fn)"></endpoint>
<signature id="Frame.schedule+2">Frame.schedule(**time**: `Num`, **fn**: `Fn`)
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
<span class='api_ret'>returns</span> `:::js None`
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
>   var tick = Frame.on(Frame.sim) {|delta| Log.print("delta:%(delta)") }
>   //...
>   Frame.off(tick)
>   ```   

<endpoint module="luxe: game" class="Frame" signature="once(section : String, priority : Num, fn : Fn)"></endpoint>
<signature id="Frame.once+3">Frame.once(**section**: `String`, **priority**: `Num`, **fn**: `Fn`)
<a class="headerlink" href="#Frame.once+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Handle`
> **Once off**. Queues a function to the specified section, with a given priority which will be executed _during_ the section.
> Priority is based on "highest priority first". So priority 1 executes before 0.
> 
> Returns a handle that can be used to remove the function via `off`.
> 
>   ```js
>   Frame.once(Frame.sim, 3) {|delta| Log.print("prints first") }
>   Frame.once(Frame.sim, 1) {|delta| Log.print("prints second") }
>   ```   

<endpoint module="luxe: game" class="Frame" signature="on(section : String, priority : Num, fn : Fn)"></endpoint>
<signature id="Frame.on+3">Frame.on(**section**: `String`, **priority**: `Num`, **fn**: `Fn`)
<a class="headerlink" href="#Frame.on+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Handle`
> Connect a function to the specified section, with a given priority which will be executed _during_ the section.
> Priority is based on "highest priority first". So priority 1 executes before 0.
> 
> Returns a handle that can be used to remove the function via `off`.
> 
>   ```js
>   Frame.on(Frame.sim, 3) {|delta| Log.print("prints first") }
>   Frame.on(Frame.sim, 1) {|delta| Log.print("prints second") }
>   ```   

<endpoint module="luxe: game" class="Frame" signature="before(section : String, priority : Num, fn : Fn)"></endpoint>
<signature id="Frame.before+3">Frame.before(**section**: `String`, **priority**: `Num`, **fn**: `Fn`)
<a class="headerlink" href="#Frame.before+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Handle`
> Connect a function to the specified section, with a given priority which will be executed _before_ the section.
> Priority is based on "highest priority first". So priority 1 executes before 0.
> 
> Returns a handle that can be used to remove the function via `off`.
> 
>   ```js
>   Frame.before(Frame.sim, 0) {|delta| Log.print("prints second") }
>   Frame.before(Frame.sim, 1) {|delta| Log.print("prints first") }
>   ```   

<endpoint module="luxe: game" class="Frame" signature="after(section : String, priority : Num, fn : Fn)"></endpoint>
<signature id="Frame.after+3">Frame.after(**section**: `String`, **priority**: `Num`, **fn**: `Fn`)
<a class="headerlink" href="#Frame.after+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Handle`
> Connect a function to the specified section, with a given priority which will be executed _after_ the section.
> Priority is based on "highest priority first". So priority 1 executes before 0.
> 
> Returns a handle that can be used to remove the function via `off`.
> 
>   ```js
>   Frame.after(Frame.sim, 2) {|delta| Log.print("prints first") }
>   Frame.after(Frame.sim, 1) {|delta| Log.print("prints second") }
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
>   Frame.on(Frame.sim) {|delta| Log.print("delta:%(delta)") }
>   ```   

<endpoint module="luxe: game" class="Frame" signature="once(section : String, fn : Fn)"></endpoint>
<signature id="Frame.once+2">Frame.once(**section**: `String`, **fn**: `Fn`)
<a class="headerlink" href="#Frame.once+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Handle`
> **Once off**. Queue a function to the specified section (with priority 0) which will be executed _during_ the section.
> Returns a handle that can be used to remove the function via `off`.
> 
>   ```js
>   Frame.once(Frame.sim) { Log.print("happens during 'sim'") }
>   ```   

<endpoint module="luxe: game" class="Frame" signature="before(section : String, fn : Fn)"></endpoint>
<signature id="Frame.before+2">Frame.before(**section**: `String`, **fn**: `Fn`)
<a class="headerlink" href="#Frame.before+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Handle`
> Connect a function to the specified section (with priority 0) which will be executed _before_ the section.
> 
> Returns a handle that can be used to remove the function via `off`.
> 
>   ```js
>   Frame.before(Frame.sim) {|delta| Log.print("delta:%(delta)") }
>   ```   

<endpoint module="luxe: game" class="Frame" signature="after(section : String, fn : Fn)"></endpoint>
<signature id="Frame.after+2">Frame.after(**section**: `String`, **fn**: `Fn`)
<a class="headerlink" href="#Frame.after+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Handle`
> Connect a function to the specified section (with priority 0) which will be executed _after_ the section.
> 
> Returns a handle that can be used to remove the function via `off`.
> 
>   ```js
>   Frame.after(Frame.sim) {|delta| Log.print("delta:%(delta)") }
>   ```   

<endpoint module="luxe: game" class="Frame" signature="skip(count_frames : Num, fn : Fn)"></endpoint>
<signature id="Frame.skip+2">Frame.skip(**count_frames**: `Num`, **fn**: `Fn`)
<a class="headerlink" href="#Frame.skip+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> **Once off**. Queue a function to be called at the beginning of the frame `count_frames` from now, 
> before any sections. This is `Frame.next` but can push actions forward by frame count instead of time.
> 
>   ```js
>   Frame.skip(3) {
>     Log.print("three frames from now!")
>   }
>   ```   

<endpoint module="luxe: game" class="Frame" signature="mark(id : String, display : String)"></endpoint>
<signature id="Frame.mark+2">Frame.mark(**id**: `String`, **display**: `String`)
<a class="headerlink" href="#Frame.mark+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: game" class="Frame" signature="get_marks(frame_index : Num)"></endpoint>
<signature id="Frame.get_marks">Frame.get_marks(**frame_index**: `Num`)
<a class="headerlink" href="#Frame.get_marks" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: game" class="Frame" signature="index"></endpoint>
<signature id="Frame.index">Frame.index
<a class="headerlink" href="#Frame.index" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: game" class="Frame" signature="delta"></endpoint>
<signature id="Frame.delta">Frame.delta
<a class="headerlink" href="#Frame.delta" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

### FrameSection
`:::js import "luxe: game" for FrameSection`
> no docs found

- [begin](#FrameSection.begin)
- [init](#FrameSection.init)
- [sim](#FrameSection.sim)
- [visual](#FrameSection.visual)
- [debug](#FrameSection.debug)
- [end](#FrameSection.end)
- [name](#FrameSection.name)(**value**: `Any`)

<hr/>
<endpoint module="luxe: game" class="FrameSection" signature="begin"></endpoint>
<signature id="FrameSection.begin">FrameSection.begin
<a class="headerlink" href="#FrameSection.begin" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> An enum value for the `begin` section in the loop.
> The `begin section is the start of the frame from the game's perspective.
> 
>   ```js
>   Frame.on(Frame.begin) {|delta| ... }
>   ```   

<endpoint module="luxe: game" class="FrameSection" signature="init"></endpoint>
<signature id="FrameSection.init">FrameSection.init
<a class="headerlink" href="#FrameSection.init" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> An enum value for the `init` section in the loop.
> The `init` section is used for initialization tasks that happen before
> updates, like when a new entity is created, it can be added to a queue and
> processed in init to set some default values before it arrives in `sim` or `visual`.
>     
>   ```js
>   Frame.on(Frame.init) {|delta| ... }
>   ```   

<endpoint module="luxe: game" class="FrameSection" signature="sim"></endpoint>
<signature id="FrameSection.sim">FrameSection.sim
<a class="headerlink" href="#FrameSection.sim" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> An enum value for the `sim` section in the loop.
> The `sim` section is for simulation, also known as `update`. 
> In this section you would update game logic and modify things that the `visual` section would reference.
> 
>   ```js
>   Frame.on(Frame.sim) {|delta| ... }
>   ```   

<endpoint module="luxe: game" class="FrameSection" signature="visual"></endpoint>
<signature id="FrameSection.visual">FrameSection.visual
<a class="headerlink" href="#FrameSection.visual" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> An enum value for the `visual` section in the loop.
> The `visual` section is for rendering, also known as `render`.
> Updating visual state from the sim states happens here.
> 
>   ```js
>   Frame.on(Frame.visual) {|delta| ... }
>   ```   

<endpoint module="luxe: game" class="FrameSection" signature="debug"></endpoint>
<signature id="FrameSection.debug">FrameSection.debug
<a class="headerlink" href="#FrameSection.debug" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> An enum value for the `debug` section in the loop.
> The `debug` part of the loop can perform debug related tasks before the end of the frame and rendering is submitted.
> 
>   ```js
>   Frame.on(Frame.debug) {|delta| ... }
>   ```   

<endpoint module="luxe: game" class="FrameSection" signature="end"></endpoint>
<signature id="FrameSection.end">FrameSection.end
<a class="headerlink" href="#FrameSection.end" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> An enum value for the `end` section in the loop.
> The `end` of the loop can perform tasks after rendering and simulation.
> 
>   ```js
>   Frame.on(Frame.end) {|delta| ... }
>   ```   

<endpoint module="luxe: game" class="FrameSection" signature="name(value : Any)"></endpoint>
<signature id="FrameSection.name">FrameSection.name(**value**: `Any`)
<a class="headerlink" href="#FrameSection.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### FrameWhen
`:::js import "luxe: game" for FrameWhen`
> no docs found

- [unknown](#FrameWhen.unknown)
- [before](#FrameWhen.before)
- [on](#FrameWhen.on)
- [after](#FrameWhen.after)
- [name](#FrameWhen.name)(**value**: `Any`)

<hr/>
<endpoint module="luxe: game" class="FrameWhen" signature="unknown"></endpoint>
<signature id="FrameWhen.unknown">FrameWhen.unknown
<a class="headerlink" href="#FrameWhen.unknown" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: game" class="FrameWhen" signature="before"></endpoint>
<signature id="FrameWhen.before">FrameWhen.before
<a class="headerlink" href="#FrameWhen.before" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: game" class="FrameWhen" signature="on"></endpoint>
<signature id="FrameWhen.on">FrameWhen.on
<a class="headerlink" href="#FrameWhen.on" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: game" class="FrameWhen" signature="after"></endpoint>
<signature id="FrameWhen.after">FrameWhen.after
<a class="headerlink" href="#FrameWhen.after" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: game" class="FrameWhen" signature="name(value : Any)"></endpoint>
<signature id="FrameWhen.name">FrameWhen.name(**value**: `Any`)
<a class="headerlink" href="#FrameWhen.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Ready
`:::js import "luxe: game" for Ready`
> The base class for a luxe game.

- [ready](#Ready.ready)()
- [ready](#Ready.ready)(**message**: `String`)
- [tick](#Ready.tick)(**delta**: `Num`)
- [destroy](#Ready.destroy)()

<hr/>
<endpoint module="luxe: game" class="Ready" signature="ready()"></endpoint>
<signature id="Ready.ready">Ready.ready()
<a class="headerlink" href="#Ready.ready" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Called via `super()` inside your `ready` function. Must be called.   

<endpoint module="luxe: game" class="Ready" signature="ready(message : String)"></endpoint>
<signature id="Ready.ready">Ready.ready(**message**: `String`)
<a class="headerlink" href="#Ready.ready" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Called via `super(message)` inside your `ready` function. Must be called.   

<endpoint module="luxe: game" class="Ready" signature="tick(delta : Num)"></endpoint>
<signature id="Ready.tick">Ready.tick(**delta**: `Num`)
<a class="headerlink" href="#Ready.tick" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> A default implementation for tick.   

<endpoint module="luxe: game" class="Ready" signature="destroy()"></endpoint>
<signature id="Ready.destroy">Ready.destroy()
<a class="headerlink" href="#Ready.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> A default implementation for destroy.   

