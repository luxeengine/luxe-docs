#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2024.12.3`)  


---

## `luxe: system/values.modifier` module

- [Data](#data)   
- [Value](#value)   
- [Values](#values)   
- [ValuesKind](#valueskind)   
- [ValuesType](#valuestype)   

---

### Data
`:::js import "luxe: system/values.modifier" for Data`
> no docs found

- `:::js var values : List = []`

<hr/>
### Value
`:::js import "luxe: system/values.modifier" for Value`
> no docs found

- `:::js var kind : ValuesKind = ValuesKind.number`
- `:::js var name : String = "value"`
- `:::js var number : Num = 0`
- `:::js var string : String = ""`
- `:::js var boolean : Bool = false`
- `:::js var float2 : Float2 = [0, 0]`
- `:::js var float3 : Float3 = [0, 0, 0]`
- `:::js var float4 : Float4 = [0, 0, 0, 0]`
- `:::js var color : Color = [1, 1, 1, 1]`

<hr/>
### Values
`:::js import "luxe: system/values.modifier" for Values`
> Values is a modifier that lets you store Key -> Value pairs. Store values like numbers, 
> strings, and colors on an entity, which can then be accessed by name (a Key).
> 
>   ```js
>   //we can use an enum for keys
>   class Keys {
>     static watered { "watered" }
>     static apples { "apples" }
>   }
>   var tree = Entity.create(world)
>   Values.create(tree)
>   Values.set(tree, Keys.watered, true)
>   Values.set(tree, Keys.apples, 10)
>   Values.set(tree, "keys are strings", true)
> 
>   var watered = Values.get(tree, Keys.watered, false)
>   var apples = Values.get(tree, Keys.apples, -1)
>   Log.print("The tree is %(watered ? "watered" : "thirsty") and has %(apples) apples!")
>   ```

- [create](#Values.create)(**entity**: `Entity`)
- [destroy](#Values.destroy)(**entity**: `Entity`)
- [has](#Values.has)(**entity**: `Entity`)
- [has_key](#Values.has_key+2)(**entity**: `Entity`, **key**: `String`)
- [remove_key](#Values.remove_key+2)(**entity**: `Entity`, **key**: `String`)
- [get_keys](#Values.get_keys)(**entity**: `Entity`)
- [get](#Values.get+3)(**entity**: `Entity`, **key**: `String`, **default**: `Any`)
- [set](#Values.set+3)(**entity**: `Entity`, **key**: `String`, **value**: `Any`)

<hr/>
<endpoint module="luxe: system/values.modifier" class="Values" signature="create(entity : Entity)"></endpoint>
<signature id="Values.create">Values.create(**entity**: `Entity`)
<a class="headerlink" href="#Values.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Attach a `Values` modifier to `entity`.
> 
>   ```js
>   var entity = Entity.create(world)
>   Values.create(entity)
>   ```   

<endpoint module="luxe: system/values.modifier" class="Values" signature="destroy(entity : Entity)"></endpoint>
<signature id="Values.destroy">Values.destroy(**entity**: `Entity`)
<a class="headerlink" href="#Values.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Detach and destroy the `Values` attached to `entity`
> 
>   ```js
>   Values.destroy(entity)
>   ```   

<endpoint module="luxe: system/values.modifier" class="Values" signature="has(entity : Entity)"></endpoint>
<signature id="Values.has">Values.has(**entity**: `Entity`)
<a class="headerlink" href="#Values.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if `entity` has a `Values` modifier attached.
> 
>   ```js
>   if(Values.has(entity)) {
>     Log.print("Has a Values modifier!")
>   }
>   ```   

<endpoint module="luxe: system/values.modifier" class="Values" signature="has_key(entity : Entity, key : String)"></endpoint>
<signature id="Values.has_key+2">Values.has_key(**entity**: `Entity`, **key**: `String`)
<a class="headerlink" href="#Values.has_key+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true the entity's Values modifier has a value with the given 'key'
> 
>   ```js
>   if(Values.has_key(entity, "apples")) {
>     Log.print("The tree has some apples!")
>   }
>   ```   

<endpoint module="luxe: system/values.modifier" class="Values" signature="remove_key(entity : Entity, key : String)"></endpoint>
<signature id="Values.remove_key+2">Values.remove_key(**entity**: `Entity`, **key**: `String`)
<a class="headerlink" href="#Values.remove_key+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Removes a value by key from 'entity's Values modifier, if it exists
> 
>   ```js
>   Values.remove_key(tree, "apples")
>   ```   

<endpoint module="luxe: system/values.modifier" class="Values" signature="get_keys(entity : Entity)"></endpoint>
<signature id="Values.get_keys">Values.get_keys(**entity**: `Entity`)
<a class="headerlink" href="#Values.get_keys" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> Get a List of all the String keys for values on 'entity's Values modifier
> 
>   ```js
>   var keys = Values.get_keys(grass)
>   for (key in keys) {
>     Log.print("Has Value Key: %(key)")
>   }
>   ```   

<endpoint module="luxe: system/values.modifier" class="Values" signature="get(entity : Entity, key : String, default : Any)"></endpoint>
<signature id="Values.get+3">Values.get(**entity**: `Entity`, **key**: `String`, **default**: `Any`)
<a class="headerlink" href="#Values.get+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Any`
> Get the current value stored with `key` on the Values modifier on `entity`,
> with a default value which is returned if the key isn't found.
> 
>   ```js
>   var seeds = Values.get(watermelon, "seeds", 0)
>   Log.print("The watermelon has %(seeds) seeds!")
>   ```   

<endpoint module="luxe: system/values.modifier" class="Values" signature="set(entity : Entity, key : String, value : Any)"></endpoint>
<signature id="Values.set+3">Values.set(**entity**: `Entity`, **key**: `String`, **value**: `Any`)
<a class="headerlink" href="#Values.set+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the value stored at the 'key' on the Values modifier on 'entity'.
> 
>   ```js
>   if(Values.has(seed)) {
>     Values.set(seed, "planted", true)
>   }
>   ```   

### ValuesKind
`:::js import "luxe: system/values.modifier" for ValuesKind`
> no docs found

- [number](#ValuesKind.number)
- [string](#ValuesKind.string)
- [boolean](#ValuesKind.boolean)
- [float2](#ValuesKind.float2)
- [float3](#ValuesKind.float3)
- [float4](#ValuesKind.float4)
- [color](#ValuesKind.color)

<hr/>
<endpoint module="luxe: system/values.modifier" class="ValuesKind" signature="number"></endpoint>
<signature id="ValuesKind.number">ValuesKind.number
<a class="headerlink" href="#ValuesKind.number" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/values.modifier" class="ValuesKind" signature="string"></endpoint>
<signature id="ValuesKind.string">ValuesKind.string
<a class="headerlink" href="#ValuesKind.string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/values.modifier" class="ValuesKind" signature="boolean"></endpoint>
<signature id="ValuesKind.boolean">ValuesKind.boolean
<a class="headerlink" href="#ValuesKind.boolean" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/values.modifier" class="ValuesKind" signature="float2"></endpoint>
<signature id="ValuesKind.float2">ValuesKind.float2
<a class="headerlink" href="#ValuesKind.float2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/values.modifier" class="ValuesKind" signature="float3"></endpoint>
<signature id="ValuesKind.float3">ValuesKind.float3
<a class="headerlink" href="#ValuesKind.float3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/values.modifier" class="ValuesKind" signature="float4"></endpoint>
<signature id="ValuesKind.float4">ValuesKind.float4
<a class="headerlink" href="#ValuesKind.float4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/values.modifier" class="ValuesKind" signature="color"></endpoint>
<signature id="ValuesKind.color">ValuesKind.color
<a class="headerlink" href="#ValuesKind.color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### ValuesType
`:::js import "luxe: system/values.modifier" for ValuesType`
> no docs found

- [unknown](#ValuesType.unknown)
- [bool](#ValuesType.bool)
- [number](#ValuesType.number)
- [string](#ValuesType.string)
- [float2](#ValuesType.float2)
- [float3](#ValuesType.float3)
- [float4](#ValuesType.float4)
- [name](#ValuesType.name)(**value**: `Any`)

<hr/>
<endpoint module="luxe: system/values.modifier" class="ValuesType" signature="unknown"></endpoint>
<signature id="ValuesType.unknown">ValuesType.unknown
<a class="headerlink" href="#ValuesType.unknown" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/values.modifier" class="ValuesType" signature="bool"></endpoint>
<signature id="ValuesType.bool">ValuesType.bool
<a class="headerlink" href="#ValuesType.bool" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/values.modifier" class="ValuesType" signature="number"></endpoint>
<signature id="ValuesType.number">ValuesType.number
<a class="headerlink" href="#ValuesType.number" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/values.modifier" class="ValuesType" signature="string"></endpoint>
<signature id="ValuesType.string">ValuesType.string
<a class="headerlink" href="#ValuesType.string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/values.modifier" class="ValuesType" signature="float2"></endpoint>
<signature id="ValuesType.float2">ValuesType.float2
<a class="headerlink" href="#ValuesType.float2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/values.modifier" class="ValuesType" signature="float3"></endpoint>
<signature id="ValuesType.float3">ValuesType.float3
<a class="headerlink" href="#ValuesType.float3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/values.modifier" class="ValuesType" signature="float4"></endpoint>
<signature id="ValuesType.float4">ValuesType.float4
<a class="headerlink" href="#ValuesType.float4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/values.modifier" class="ValuesType" signature="name(value : Any)"></endpoint>
<signature id="ValuesType.name">ValuesType.name(**value**: `Any`)
<a class="headerlink" href="#ValuesType.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

