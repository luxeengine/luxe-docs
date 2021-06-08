#![](../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2021.0.3`)  


---

## `luxe: events` module

- [Events](#events)   

---

### Events
`:::js import "luxe: events" for Events`
> A simple event system for listening to and emitting events.

Note: this API will likely change to ID based soon, where 
on listening, an ID will be returned, and use that ID to unlisten 
rather than needing the function object.

- [new](#Events.new)()
- [once](#Events.once+2)(**tags**: `Any`, **fn**: `Any`)
- [listen](#Events.listen+2)(**tags**: `Any`, **fn**: `Any`)
- [unlisten](#Events.unlisten+2)(**tags**: `Any`, **fn**: `Any`)
- [unlisten](#Events.unlisten)(**tags**: `Any`)
- [emit](#Events.emit)(**tags**: `Any`)
- [emit](#Events.emit+2)(**tags**: `Any`, **data**: `Any`)

<hr/>
<endpoint module="luxe: events" class="Events" signature="new()"></endpoint>
<signature id="Events.new">Events.new()
<a class="headerlink" href="#Events.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Events`
> Create a new `Events` instance to use.   
```js
var events = Events.new()
```

<endpoint module="luxe: events" class="Events" signature="once(tags : Any, fn : Any)"></endpoint>
<signature id="Events.once+2">Events.once(**tags**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#Events.once+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Connect a function to the given tags, that is automatically removed after the event is emitted.
> The function takes a single argument, `data`, which is sent from `emit`.   
```js
events.once(["example"]) {|data|
  System.print("event received: data = `%(data)`")
}

//make the event happen, will call the above function
//which prints  event received: data = `321`
events.emit(["example"], 321)
//fire the event again, but this one does NOT print,
//because the event was only listening once
events.emit(["example"], 654)
```

<endpoint module="luxe: events" class="Events" signature="listen(tags : Any, fn : Any)"></endpoint>
<signature id="Events.listen+2">Events.listen(**tags**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#Events.listen+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Connect a function to the given tags. The function will be called each time the event is
> emitted, until `unlisten` is called. The function takes a single argument, `data`, which is sent from `emit`.   
```js
var tags = ["example", "tags"]
var fn = Fn.new {|data|
  System.print("data = `%(data)`")
}

events.listen(tags, fn)
events.emit(tags, "hello")          //prints data = `hello`
events.emit(tags, { "map":"data" }) //prints data = `{map:data}`
events.emit(tags)                   //prints data = `null`
events.unlisten(tags, fn)           //remove the function
events.emit(tags)                   //nothing printed
```

<endpoint module="luxe: events" class="Events" signature="unlisten(tags : Any, fn : Any)"></endpoint>
<signature id="Events.unlisten+2">Events.unlisten(**tags**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#Events.unlisten+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Removes a connected function for the specified tags (if one exists).
> See `listen` for example.   
```js
events.unlisten(["tag"], fn)
```

<endpoint module="luxe: events" class="Events" signature="unlisten(tags : Any)"></endpoint>
<signature id="Events.unlisten">Events.unlisten(**tags**: `Any`)
<a class="headerlink" href="#Events.unlisten" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Removes ALL functions from the specified tags, clearing it.   
```js
events.unlisten(["tag"])
```

<endpoint module="luxe: events" class="Events" signature="emit(tags : Any)"></endpoint>
<signature id="Events.emit">Events.emit(**tags**: `Any`)
<a class="headerlink" href="#Events.emit" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Emit the event tags so that any connected functions will be called.
> Sends `null` for the data argument to the functions. See `listen` for an example.   
```js
events.emit(["tag"])
```

<endpoint module="luxe: events" class="Events" signature="emit(tags : Any, data : Any)"></endpoint>
<signature id="Events.emit+2">Events.emit(**tags**: `Any`, **data**: `Any`)
<a class="headerlink" href="#Events.emit+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Emit the event tags so that any connected functions will be called.
> Sends `data` as is for the data argument to the functions. See `listen` for an example.   
```js
events.emit(["tag"], ["hello"])
```

