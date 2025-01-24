#![](../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2025.1.1`)  


---

## `luxe: events` module

- [Events](#events)   

---

### Events
`:::js import "luxe: events" for Events`
> A simple event system for listening to and emitting events.
> 
> Note: this API will likely change to ID based soon, where 
> on listening, an ID will be returned, and use that ID to unlisten 
> rather than needing the function object.

- [new](#Events.new)()
- [once](#Events.once+2)(**tags**: `List`, **fn**: `Fn`)
- [listen](#Events.listen+2)(**tags**: `List`, **fn**: `Fn`)
- [unlisten](#Events.unlisten+2)(**tags**: `List`, **fn**: `Fn`)
- [unlisten_id](#Events.unlisten_id+2)(**tags**: `List`, **id**: `String`)
- [unlisten](#Events.unlisten)(**tags**: `List`)
- [emit](#Events.emit)(**tags**: `List`)
- [emit](#Events.emit+2)(**tags**: `List`, **data**: `Any`)

<hr/>
<endpoint module="luxe: events" class="Events" signature="new()"></endpoint>
<signature id="Events.new">Events.new()
<a class="headerlink" href="#Events.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Events`
> Create a new `Events` instance to use.
> 
>   ```js
>   var events = Events.new()
>   ```   

<endpoint module="luxe: events" class="Events" signature="once(tags : List, fn : Fn)"></endpoint>
<signature id="Events.once+2">Events.once(**tags**: `List`, **fn**: `Fn`)
<a class="headerlink" href="#Events.once+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Connect a function to the given tags, that is automatically removed after the event is emitted.
> The function takes a single argument, `data`, which is sent from `emit`.
> 
>   ```js
>   events.once(["example"]) {|data|
>     Log.print("event received: data = `%(data)`")
>   }
> 
>   //make the event happen, will call the above function
>   //which prints  event received: data = `321`
>   events.emit(["example"], 321)
>   //fire the event again, but this one does NOT print,
>   //because the event was only listening once
>   events.emit(["example"], 654)
>   ```   

<endpoint module="luxe: events" class="Events" signature="listen(tags : List, fn : Fn)"></endpoint>
<signature id="Events.listen+2">Events.listen(**tags**: `List`, **fn**: `Fn`)
<a class="headerlink" href="#Events.listen+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Connect a function to the given tags. The function will be called each time the event is
> emitted, until `unlisten` is called. The function takes a single argument, `data`, which is sent through `emit`.
> Returns an id that you give to `unlisten`.
> 
>   ```js
>   var tags = ["example", "tags"]
>   var fn = Fn.new {|data|
>     Log.print("data = `%(data)`")
>   }
> 
>   var id = events.listen(tags, fn)
>   events.emit(tags, "hello")          //prints data = `hello`
>   events.emit(tags, { "map":"data" }) //prints data = `{map:data}`
>   events.emit(tags)                   //prints data = `null`
>   events.unlisten_id(tags, id)        //remove the function
>   events.emit(tags)                   //nothing printed
>   ```   

<endpoint module="luxe: events" class="Events" signature="unlisten(tags : List, fn : Fn)"></endpoint>
<signature id="Events.unlisten+2">Events.unlisten(**tags**: `List`, **fn**: `Fn`)
<a class="headerlink" href="#Events.unlisten+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Removes a connected function for the specified tags (if one exists), 
> by specifying the same function passed to `listen`. See `listen` for example.
> 
>   ```js
>   events.unlisten(["tag"], fn)
>   ```   

<endpoint module="luxe: events" class="Events" signature="unlisten_id(tags : List, id : String)"></endpoint>
<signature id="Events.unlisten_id+2">Events.unlisten_id(**tags**: `List`, **id**: `String`)
<a class="headerlink" href="#Events.unlisten_id+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Removes a connected function for the specified tags (if one exists).
> The id is the one returned from `listen`. See `listen` for example.
> 
>   ```js
>   events.unlisten_id(["tag"], id)
>   ```   

<endpoint module="luxe: events" class="Events" signature="unlisten(tags : List)"></endpoint>
<signature id="Events.unlisten">Events.unlisten(**tags**: `List`)
<a class="headerlink" href="#Events.unlisten" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Removes ALL functions from the specified tags, clearing them.
> 
>   ```js
>   events.unlisten(["tag"])
>   ```   

<endpoint module="luxe: events" class="Events" signature="emit(tags : List)"></endpoint>
<signature id="Events.emit">Events.emit(**tags**: `List`)
<a class="headerlink" href="#Events.emit" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Emit the event tags so that any connected functions will be called.
> Sends `null` for the data argument to the functions. See `listen` for an example.
> 
>   ```js
>   events.emit(["tag"])
>   ```   

<endpoint module="luxe: events" class="Events" signature="emit(tags : List, data : Any)"></endpoint>
<signature id="Events.emit+2">Events.emit(**tags**: `List`, **data**: `Any`)
<a class="headerlink" href="#Events.emit+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Emit the event tags so that any connected functions will be called.
> Sends `data` as is for the data argument to the functions. See `listen` for an example.
> 
>   ```js
>   events.emit(["tag"], ["hello"])
>   ```   

