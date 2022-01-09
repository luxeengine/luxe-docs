#![](../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2022.0.1`)  


---

## `luxe: id` module

- [ID](#id)   

---

### ID
`:::js import "luxe: id" for ID`
> IDs are useful in many cases, this API provides them in various forms like UUID or unique short strings.

- [unique](#ID.unique)()
- [uuid](#ID.uuid)()
- [uuid_base62](#ID.uuid_base62)()

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
> (Don't make assumptions about the length of the ID).
> 
>   ```js
>   System.print(ID.unique()) //UuIyH
>   System.print(ID.unique()) //39sjDw
>   System.print(ID.unique()) //28zASZ
>   ```   

<endpoint module="luxe: id" class="ID" signature="uuid()"></endpoint>
<signature id="ID.uuid">ID.uuid()
<a class="headerlink" href="#ID.uuid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Returns a UUID v4 ID.
> These are unique enough to not worry about collisions (not for cryptography).
> 
>   ```js
>   System.print(ID.uuid()) //5606ba0f-968a-4ab7-8230-ba46cdb345da
>   System.print(ID.uuid()) //48e3d469-e9fa-4a24-aa22-d653de9af5b2
>   System.print(ID.uuid()) //a4861cc5-c2e4-4656-a3a4-176bc63e5d05
>   ```   

<endpoint module="luxe: id" class="ID" signature="uuid_base62()"></endpoint>
<signature id="ID.uuid_base62">ID.uuid_base62()
<a class="headerlink" href="#ID.uuid_base62" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Returns a UUID represented as a base62 string.
> 
>   ```js
>   System.print(ID.uuid_base62()) //AXiFxIVixJM-EDCrnEHVkWJ
>   ```   

