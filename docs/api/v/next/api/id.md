#![](../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.10.1`)  


---

## `luxe: id` module

- [ID](#id)   

---

### ID
`:::js import "luxe: id" for ID`
> IDs are useful in many cases, this API provides them in various forms like UUID or unique short strings.

- [unique](#ID.unique)()
- [unique](#ID.unique)(**length**: `Num`)
- [index](#ID.index)(**index**: `Num`)
- [uuid](#ID.uuid)()
- [uuid_validate](#ID.uuid_validate)(**uuid**: `String`)
- [uuid_base62](#ID.uuid_base62)()
- [uuid_combine](#ID.uuid_combine+2)(**uuid_a**: `String`, **uuid_b**: `String`)

<hr/>
<endpoint module="luxe: id" class="ID" signature="unique()"></endpoint>
<signature id="ID.unique">ID.unique()
<a class="headerlink" href="#ID.unique" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Returns a unique short string ID for use.
> These are useful for default generated names, random urls, etc.
> 
> Note that these are "unique enough" but has higher risk of collision than a UUID.
> If you want _universally unique_ IDs that's what UUID is for.
> (Don't make assumptions about the length of the ID, for fixed length use `ID.unique(length: Num)`).
> 
>   ```js
>   Log.print(ID.unique()) //UuIyH
>   Log.print(ID.unique()) //39sjDw
>   Log.print(ID.unique()) //28zASZ
>   ```   

<endpoint module="luxe: id" class="ID" signature="unique(length : Num)"></endpoint>
<signature id="ID.unique">ID.unique(**length**: `Num`)
<a class="headerlink" href="#ID.unique" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Returns a unique short string ID for use.
> These are useful for default generated names, random urls, etc.
> 
> Note that these are "unique enough" but has higher risk of collision than a UUID.
> If you want _universally unique_ IDs that's what UUID is for.
> 
>   ```js
>   Log.print(ID.unique(6)) //Uu2IyH
>   Log.print(ID.unique(8)) //39sjDwl4
>   ```   

<endpoint module="luxe: id" class="ID" signature="index(index : Num)"></endpoint>
<signature id="ID.index">ID.index(**index**: `Num`)
<a class="headerlink" href="#ID.index" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: id" class="ID" signature="uuid()"></endpoint>
<signature id="ID.uuid">ID.uuid()
<a class="headerlink" href="#ID.uuid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Returns a UUID v4 ID.
> These are unique enough to not worry about collisions (not for cryptography).
> 
>   ```js
>   Log.print(ID.uuid()) //5606ba0f-968a-4ab7-8230-ba46cdb345da
>   Log.print(ID.uuid()) //48e3d469-e9fa-4a24-aa22-d653de9af5b2
>   Log.print(ID.uuid()) //a4861cc5-c2e4-4656-a3a4-176bc63e5d05
>   ```   

<endpoint module="luxe: id" class="ID" signature="uuid_validate(uuid : String)"></endpoint>
<signature id="ID.uuid_validate">ID.uuid_validate(**uuid**: `String`)
<a class="headerlink" href="#ID.uuid_validate" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns true if the given UUID is valid (using regex matching).
> 
>   ```js
>   Log.print(ID.validate_uuid(ID.uuid())) //true
>   Log.print(ID.validate_uuid("hello"))   //false
>   ```   

<endpoint module="luxe: id" class="ID" signature="uuid_base62()"></endpoint>
<signature id="ID.uuid_base62">ID.uuid_base62()
<a class="headerlink" href="#ID.uuid_base62" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Returns a UUID represented as a base62 string.
> 
>   ```js
>   Log.print(ID.uuid_base62()) //AXiFxIVixJM-EDCrnEHVkWJ
>   ```   

<endpoint module="luxe: id" class="ID" signature="uuid_combine(uuid_a : String, uuid_b : String)"></endpoint>
<signature id="ID.uuid_combine+2">ID.uuid_combine(**uuid_a**: `String`, **uuid_b**: `String`)
<a class="headerlink" href="#ID.uuid_combine+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Returns a new UUID by combining the two UUIDs given.
> 
>   ```js
>   Log.print(ID.uuid_combine(ID.uuid(), ID.uuid())) //5f558462-7525-48c0-812d-a65df074ce42
>   ```   

