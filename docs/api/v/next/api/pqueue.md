#![](../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.10.1`)  


---

## `luxe: pqueue` module

- [MaxPQ](#maxpq)   
- [MinPQ](#minpq)   

---

### MaxPQ
`:::js import "luxe: pqueue" for MaxPQ`
> A priority queue that returns larger values first.
> 
> A priority queue holds various values and will sort
> them into an ordered list by priority. When queried
> via `peek` or values removed via `pop` the values are sorted.

- [value](#MaxPQ.value)
- [count](#MaxPQ.count)
- [new](#MaxPQ.new)()
- [new](#MaxPQ.new)(**get_priority_fn**: `Any`)
- [add](#MaxPQ.add)(**value**: `Any`)
- [pop](#MaxPQ.pop)()
- [peek](#MaxPQ.peek)()

<hr/>
<endpoint module="luxe: pqueue" class="MaxPQ" signature="value"></endpoint>
<signature id="MaxPQ.value">MaxPQ.value
<a class="headerlink" href="#MaxPQ.value" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns the internal array. Read only, modify the queue via `add` and `pop`.   

<endpoint module="luxe: pqueue" class="MaxPQ" signature="count"></endpoint>
<signature id="MaxPQ.count">MaxPQ.count
<a class="headerlink" href="#MaxPQ.count" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns the number of items in the priority queue.   

<endpoint module="luxe: pqueue" class="MaxPQ" signature="new()"></endpoint>
<signature id="MaxPQ.new">MaxPQ.new()
<a class="headerlink" href="#MaxPQ.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js MaxPQ`
> Create a new priority queue.   

<endpoint module="luxe: pqueue" class="MaxPQ" signature="new(get_priority_fn : Any)"></endpoint>
<signature id="MaxPQ.new">MaxPQ.new(**get_priority_fn**: `Any`)
<a class="headerlink" href="#MaxPQ.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js MaxPQ`
> Create a new priority queue with a callback for the priority of a value.
> The callback takes one parameter, the value, and should return a priority number 
> for that value.   

<endpoint module="luxe: pqueue" class="MaxPQ" signature="add(value : Any)"></endpoint>
<signature id="MaxPQ.add">MaxPQ.add(**value**: `Any`)
<a class="headerlink" href="#MaxPQ.add" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Add a value to the queue.   

<endpoint module="luxe: pqueue" class="MaxPQ" signature="pop()"></endpoint>
<signature id="MaxPQ.pop">MaxPQ.pop()
<a class="headerlink" href="#MaxPQ.pop" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Return the next value, removing it from the queue.   

<endpoint module="luxe: pqueue" class="MaxPQ" signature="peek()"></endpoint>
<signature id="MaxPQ.peek">MaxPQ.peek()
<a class="headerlink" href="#MaxPQ.peek" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Return the next value without removing it from the queue.   

### MinPQ
`:::js import "luxe: pqueue" for MinPQ`
> A priority queue that returns smaller values first.
> 
> A priority queue holds various values and will sort
> them into an ordered list by priority. When queried
> via `peek` or values removed via `pop` the values are sorted.

- [value](#MinPQ.value)
- [count](#MinPQ.count)
- [new](#MinPQ.new)()
- [new](#MinPQ.new)(**get_priority_fn**: `Any`)
- [add](#MinPQ.add)(**value**: `Any`)
- [pop](#MinPQ.pop)()
- [peek](#MinPQ.peek)()

<hr/>
<endpoint module="luxe: pqueue" class="MinPQ" signature="value"></endpoint>
<signature id="MinPQ.value">MinPQ.value
<a class="headerlink" href="#MinPQ.value" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns the internal array. Read only, modify the queue via `add` and `pop`.   

<endpoint module="luxe: pqueue" class="MinPQ" signature="count"></endpoint>
<signature id="MinPQ.count">MinPQ.count
<a class="headerlink" href="#MinPQ.count" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns the number of items in the priority queue.   

<endpoint module="luxe: pqueue" class="MinPQ" signature="new()"></endpoint>
<signature id="MinPQ.new">MinPQ.new()
<a class="headerlink" href="#MinPQ.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js MinPQ`
> Create a new priority queue.   

<endpoint module="luxe: pqueue" class="MinPQ" signature="new(get_priority_fn : Any)"></endpoint>
<signature id="MinPQ.new">MinPQ.new(**get_priority_fn**: `Any`)
<a class="headerlink" href="#MinPQ.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js MinPQ`
> Create a new priority queue with a callback for the priority of a value.
> The callback takes one parameter, the value, and should return a priority number 
> for that value.   

<endpoint module="luxe: pqueue" class="MinPQ" signature="add(value : Any)"></endpoint>
<signature id="MinPQ.add">MinPQ.add(**value**: `Any`)
<a class="headerlink" href="#MinPQ.add" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Add a value to the queue.   

<endpoint module="luxe: pqueue" class="MinPQ" signature="pop()"></endpoint>
<signature id="MinPQ.pop">MinPQ.pop()
<a class="headerlink" href="#MinPQ.pop" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Return the next value, removing it from the queue.   

<endpoint module="luxe: pqueue" class="MinPQ" signature="peek()"></endpoint>
<signature id="MinPQ.peek">MinPQ.peek()
<a class="headerlink" href="#MinPQ.peek" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Return the next value without removing it from the queue.   

