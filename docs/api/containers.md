#![](../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2021.0.3`)  


---

## `luxe: containers` module

- [Lists](#lists)   
- [MapOrdered](#mapordered)   

---

### Lists
`:::js import "luxe: containers" for Lists`
> The `Lists` API operates on the built in Wren `List` type,
offering more tools to operate on them.

- [binary_search](#Lists.binary_search+2)(**list**: `Any`, **value**: `Any`)
- [binary_search_first](#Lists.binary_search_first+3)(**list**: `Any`, **value**: `Any`, **fn**: `Any`)
- [equal](#Lists.equal+2)(**a**: `Any`, **b**: `Any`)
- [equalish](#Lists.equalish+2)(**a**: `Any`, **b**: `Any`)
- [flatten](#Lists.flatten)(**list**: `Any`)
- [add_unique](#Lists.add_unique+2)(**list**: `Any`, **value**: `Any`)
- [append](#Lists.append+2)(**into**: `Any`, **list**: `Any`)
- [prepend](#Lists.prepend+2)(**into**: `Any`, **list**: `Any`)
- [remove](#Lists.remove+2)(**list**: `Any`, **to_remove**: `Any`)
- [remove_where](#Lists.remove_where+3)(**list**: `Any`, **value**: `Any`, **fn**: `Any`)
- [contains](#Lists.contains+2)(**list**: `Any`, **item**: `Any`)
- [index_of](#Lists.index_of+2)(**list**: `Any`, **item**: `Any`)
- [index_of_where](#Lists.index_of_where+3)(**list**: `Any`, **value**: `Any`, **fn**: `Any`)
- [bubble_sort](#Lists.bubble_sort+2)(**list**: `Any`, **compare**: `Any`)
- [quicksort](#Lists.quicksort+2)(**list**: `Any`, **compare**: `Any`)
- [quicksort](#Lists.quicksort+4)(**list**: `Any`, **low**: `Any`, **high**: `Any`, **compare**: `Any`)

<hr/>
<endpoint module="luxe: containers" class="Lists" signature="binary_search(list : Any, value : Any)"></endpoint>
<signature id="Lists.binary_search+2">Lists.binary_search(**list**: `Any`, **value**: `Any`)
<a class="headerlink" href="#Lists.binary_search+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Searches for `value` in `list` using a binary search. 
> Binary searches can be more efficient for finding items when there are many.
> This requires the list to be sorted, and values in the list to be comparable with `>`/`<`.
> 
> Returns the index in the list, or `-1` if not found.   
```js
var to_find = 9
var list = [1,3,7,9,23,54]
var index = Lists.binary_search(list, to_find) //index is 3
```

<endpoint module="luxe: containers" class="Lists" signature="binary_search_first(list : Any, value : Any, fn : Any)"></endpoint>
<signature id="Lists.binary_search_first+3">Lists.binary_search_first(**list**: `Any`, **value**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#Lists.binary_search_first+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Similar to `binary_search` but handles comparison via a callback.
> The callback should return 0 for equal, -1 for lower and 1 for higher.
> The callback puts the input value in the first argument.
> 
> Returns the index in the list, or `-1` if not found.   
```js
var list = [1,3,7,9,23,54]
var index = Lists.binary_search_first(list, 9) {|value, other|
  if(value == to_find) return 0
  if(value < to_find)  return -1
  return 1
}
```

<endpoint module="luxe: containers" class="Lists" signature="equal(a : Any, b : Any)"></endpoint>
<signature id="Lists.equal+2">Lists.equal(**a**: `Any`, **b**: `Any`)
<a class="headerlink" href="#Lists.equal+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Compares two flat lists, returning true if the contents are the same and in the same order.
> Does not recurse nested lists. Uses `a[i] != b[i]` to compare.   
```js
var listA = [1,9,7]
var listB = [1,7,9]
var equalA = Lists.equal(listA, [1,7,9]) //false
var equalB = Lists.equal(listB, [1,7,9]) //true
```

<endpoint module="luxe: containers" class="Lists" signature="equalish(a : Any, b : Any)"></endpoint>
<signature id="Lists.equalish+2">Lists.equalish(**a**: `Any`, **b**: `Any`)
<a class="headerlink" href="#Lists.equalish+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Similar to `equal` but values don't need to be in the same order.   
```js
var listA = [1,9,7]
var listB = [1,7,9]
var equalA = Lists.equal(listA, [1,7,9]) //true
var equalB = Lists.equal(listB, [1,7,9]) //true
```

<endpoint module="luxe: containers" class="Lists" signature="flatten(list : Any)"></endpoint>
<signature id="Lists.flatten">Lists.flatten(**list**: `Any`)
<a class="headerlink" href="#Lists.flatten" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> Converts a nested list of lists to a single flat list of values.   
```js
var list = [1,[2,3,[4,[5]]]]
var flat = Lists.flatten(list) //[1,2,3,4,5]
```

<endpoint module="luxe: containers" class="Lists" signature="add_unique(list : Any, value : Any)"></endpoint>
<signature id="Lists.add_unique+2">Lists.add_unique(**list**: `Any`, **value**: `Any`)
<a class="headerlink" href="#Lists.add_unique+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Add an item to a list if the value doesn't already exist in the list.
> Uses `Lists.index_of` to check. 
> 
> Returns true if the value was unique and added to the list.   
```js
var list = [1,2,3]
Lists.add_unique(list, 0) //true
Lists.add_unique(list, 1) //false, already found
```

<endpoint module="luxe: containers" class="Lists" signature="append(into : Any, list : Any)"></endpoint>
<signature id="Lists.append+2">Lists.append(**into**: `Any`, **list**: `Any`)
<a class="headerlink" href="#Lists.append+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Append `list` at the end of `into` without allocating a new list.
> This function modifies `into`, and both `into` and `list` are a Wren `List`.
> 
> Note that in Wren, `List` implements `+`, which is append too, 
> but that makes a new list with the two combined. `[1] + [2] = [1, 2]`   
```js
var list = [1,2]
Lists.append(list, [3,4,5])
System.print(list) //[1,2,3,4,5]
```

<endpoint module="luxe: containers" class="Lists" signature="prepend(into : Any, list : Any)"></endpoint>
<signature id="Lists.prepend+2">Lists.prepend(**into**: `Any`, **list**: `Any`)
<a class="headerlink" href="#Lists.prepend+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Similar to `append`, but adds the items from `list` to the front of `into`.
> This function modifies `into`, and both `into` and `list` are a Wren `List`.   
```js
var list = [1,2]
Lists.prepend(list, [3,4,5])
System.print(list) //[3,4,5,1,2]
```

<endpoint module="luxe: containers" class="Lists" signature="remove(list : Any, to_remove : Any)"></endpoint>
<signature id="Lists.remove+2">Lists.remove(**list**: `Any`, **to_remove**: `Any`)
<a class="headerlink" href="#Lists.remove+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Removes the `to_remove` value from `list`.
> Uses `Lists.index_of` to find the index (standard equality is used).
> 
> Returns true if the value was removed, false if it wasn't found.   
```js
var list = [1,2,3]
Lists.remove(list, 3) //true
Lists.remove(list, 5) //false
System.print(list)    //[1,2]
```

<endpoint module="luxe: containers" class="Lists" signature="remove_where(list : Any, value : Any, fn : Any)"></endpoint>
<signature id="Lists.remove_where+3">Lists.remove_where(**list**: `Any`, **value**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#Lists.remove_where+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Similar to `remove` but uses a function for the find/equality check.
> Uses `Lists.index_of_where` to find the index, so the callback 
> msut return true if the values are equal or false if not.
> 
> Returns true if the value was removed, false if it wasn't found.   
```js
var list = [1,2,3]
var fn = Fn.new {|value, other| value == other }
Lists.remove_where(list, 3, fn)  //true
Lists.remove_where(list, 6, fn)  //false
System.print(list)               //[1,2]
```

<endpoint module="luxe: containers" class="Lists" signature="contains(list : Any, item : Any)"></endpoint>
<signature id="Lists.contains+2">Lists.contains(**list**: `Any`, **item**: `Any`)
<a class="headerlink" href="#Lists.contains+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if the `list` contains `item`.
> You can use `list.contains(item)` too, this was added before this was available.
> Uses `index_of`.   
```js
//:todo: example
```

<endpoint module="luxe: containers" class="Lists" signature="index_of(list : Any, item : Any)"></endpoint>
<signature id="Lists.index_of+2">Lists.index_of(**list**: `Any`, **item**: `Any`)
<a class="headerlink" href="#Lists.index_of+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Returns the index of `item` in `list` or `-1` if not found.   
```js
var list = [1,2,3]
System.print( Lists.index_of(list, 2) ) //1
System.print( Lists.index_of(list, 5) ) //-1
```

<endpoint module="luxe: containers" class="Lists" signature="index_of_where(list : Any, value : Any, fn : Any)"></endpoint>
<signature id="Lists.index_of_where+3">Lists.index_of_where(**list**: `Any`, **value**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#Lists.index_of_where+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Returns the index of `item` in `list` or `-1` if not found,
> but comparison is handled by a callback function.   
```js
var list = [1,2,3]
Lists.index_of_where(list, 3) {|value, other| value == other } //2
```

<endpoint module="luxe: containers" class="Lists" signature="bubble_sort(list : Any, compare : Any)"></endpoint>
<signature id="Lists.bubble_sort+2">Lists.bubble_sort(**list**: `Any`, **compare**: `Any`)
<a class="headerlink" href="#Lists.bubble_sort+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> In-place sorting of `list` using the `compare` function. Modifies `list`. Uses bubble sort.
> The compare function should return `0` for equal, `-1` for lower values and `1` for higher values.   
```js
var list = [5,2,67,23]
Lists.bubble_sort(list) {|a, b| b - a }
System.print(list) // [67, 23, 5, 2]

Lists.bubble_sort(list) {|a, b| a - b }
System.print(list) // [2, 5, 23, 67]
```

<endpoint module="luxe: containers" class="Lists" signature="quicksort(list : Any, compare : Any)"></endpoint>
<signature id="Lists.quicksort+2">Lists.quicksort(**list**: `Any`, **compare**: `Any`)
<a class="headerlink" href="#Lists.quicksort+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> In-place sorting of `list` using the `compare` function. Modifies `list`. Uses quick sort.
> The compare function should return `0` for equal, `-1` for lower values and `1` for higher values.   
```js
var list = [5,2,67,23]
Lists.quicksort(list) {|a, b| b - a }
System.print(list) // [67, 23, 5, 2]

Lists.quicksort(list) {|a, b| a - b }
System.print(list) // [2, 5, 23, 67]
```

<endpoint module="luxe: containers" class="Lists" signature="quicksort(list : Any, low : Any, high : Any, compare : Any)"></endpoint>
<signature id="Lists.quicksort+4">Lists.quicksort(**list**: `Any`, **low**: `Any`, **high**: `Any`, **compare**: `Any`)
<a class="headerlink" href="#Lists.quicksort+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Same as `quicksort` but a low and high index can be specified to sort just a portion of a list.
> The default for `quicksort(list, compare)` is `low = 0`, `high = list.count-1`.   
```js
var list = [5,2,34,89,11,60,45]
Lists.quicksort(list, 2, 5) {|a, b| a - b }
System.print(list) // [5, 2, |11, 34, 60, 89|, 45]
//note only the range between | was sorted
```

### MapOrdered
`:::js import "luxe: containers" for MapOrdered`
> A `Map` wrapper that keeps the order of the keys the same in which they're added.
Note: The Wren `Map` class doesn't guarantee order of keys.

- [keys](#MapOrdered.keys)
- [map](#MapOrdered.map)
- [new](#MapOrdered.new)()
- [get](#MapOrdered.get)(**key**: `Any`)
- [set](#MapOrdered.set+2)(**key**: `Any`, **value**: `Any`)
- [containsKey](#MapOrdered.containsKey)(**key**: `Any`)
- [[key : Any]](#MapOrdered.[key : Any])
- [[key : Any]](#MapOrdered.[key : Any]=)=(value : Any)

<hr/>
<endpoint module="luxe: containers" class="MapOrdered" signature="keys"></endpoint>
<signature id="MapOrdered.keys">MapOrdered.keys
<a class="headerlink" href="#MapOrdered.keys" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> Returns the list of `keys` in the Map.   
```js
var map = MapOrdered.new()
map["one"] = 1
map["two"] = 2
System.print(map.keys) //["one", "two"]
```

<endpoint module="luxe: containers" class="MapOrdered" signature="map"></endpoint>
<signature id="MapOrdered.map">MapOrdered.map
<a class="headerlink" href="#MapOrdered.map" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Map`
> Access to the underlying `Map` data.   
```js
var map = MapOrdered.new()
map["one"] = 1
map["two"] = 2
System.print(map.map) //{two: 2, one: 1}
```

<endpoint module="luxe: containers" class="MapOrdered" signature="new()"></endpoint>
<signature id="MapOrdered.new">MapOrdered.new()
<a class="headerlink" href="#MapOrdered.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js MapOrdered`
> Create a new ordered map.   
```js
var map = MapOrdered.new()
```

<endpoint module="luxe: containers" class="MapOrdered" signature="get(key : Any)"></endpoint>
<signature id="MapOrdered.get">MapOrdered.get(**key**: `Any`)
<a class="headerlink" href="#MapOrdered.get" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Any`
> Return the value associated with `key`, or `null` if not found.
> You can also use `map[key]` as an alternative.   
```js
var map = MapOrdered.new()
map["one"] = 1
System.print(map.get("one"))  //1
System.print(map.get("two"))  //null
```

<endpoint module="luxe: containers" class="MapOrdered" signature="set(key : Any, value : Any)"></endpoint>
<signature id="MapOrdered.set+2">MapOrdered.set(**key**: `Any`, **value**: `Any`)
<a class="headerlink" href="#MapOrdered.set+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set a `value` for a given `key`.
> You can also use `map[key] = value` as an alternative.   
```js
var map = MapOrdered.new()
map.set("one", 1)
```

<endpoint module="luxe: containers" class="MapOrdered" signature="containsKey(key : Any)"></endpoint>
<signature id="MapOrdered.containsKey">MapOrdered.containsKey(**key**: `Any`)
<a class="headerlink" href="#MapOrdered.containsKey" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if `key` is found in the map.   
```js
var map = MapOrdered.new()
map["one"] = 1
System.print(map.containsKey("one"))  //true
System.print(map.containsKey("two"))  //false
```

<endpoint module="luxe: containers" class="MapOrdered" signature="[key : Any]"></endpoint>
<signature id="MapOrdered.[key : Any]">MapOrdered [key : Any]
<a class="headerlink" href="#MapOrdered.[key : Any]" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> :todo: desc   
```js
//:todo: example
```

<endpoint module="luxe: containers" class="MapOrdered" signature="[key : Any]=(value : Any)"></endpoint>
<signature id="MapOrdered.[key : Any]=">MapOrdered [key : Any]=(value : Any)
<a class="headerlink" href="#MapOrdered.[key : Any]=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> :todo: desc   
```js
//:todo: example
```

