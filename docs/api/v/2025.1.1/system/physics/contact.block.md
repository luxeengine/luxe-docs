#![](../../../../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2025.1.1`)  


---

## `luxe: system/physics/contact.block` module

- [Contact](#contact)   
- [ContactHelper](#contacthelper)   
- [ContactKind](#contactkind)   

---

### Contact
`:::js import "luxe: system/physics/contact.block" for Contact`
> no docs found

- `:::js var kind : ContactKind = ContactKind.none`
- `:::js var body : Num = 0`
- `:::js var collider : Num = 0`
- `:::js var contacts : List = []`
- `:::js var other_body : Num = 0`
- `:::js var other_collider : Num = 0`
- `:::js var other_contacts : List = []`
- `:::js var normal : Float3 = [0, 0, 0]`
- `:::js var overlap : Num = 0`

<hr/>
### ContactHelper
`:::js import "luxe: system/physics/contact.block" for ContactHelper`
> no docs found

- [get_other](#ContactHelper.get_other+2)(**body**: `Entity`, **contact**: `Contact`)
- [get_other_collider](#ContactHelper.get_other_collider+2)(**collider**: `Entity`, **contact**: `Contact`)

<hr/>
<endpoint module="luxe: system/physics/contact.block" class="ContactHelper" signature="get_other(body : Entity, contact : Contact)"></endpoint>
<signature id="ContactHelper.get_other+2">ContactHelper.get_other(**body**: `Entity`, **contact**: `Contact`)
<a class="headerlink" href="#ContactHelper.get_other+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/physics/contact.block" class="ContactHelper" signature="get_other_collider(collider : Entity, contact : Contact)"></endpoint>
<signature id="ContactHelper.get_other_collider+2">ContactHelper.get_other_collider(**collider**: `Entity`, **contact**: `Contact`)
<a class="headerlink" href="#ContactHelper.get_other_collider+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### ContactKind
`:::js import "luxe: system/physics/contact.block" for ContactKind`
> no docs found

- [none](#ContactKind.none)
- [begin](#ContactKind.begin)
- [end](#ContactKind.end)
- [active](#ContactKind.active)

<hr/>
<endpoint module="luxe: system/physics/contact.block" class="ContactKind" signature="none"></endpoint>
<signature id="ContactKind.none">ContactKind.none
<a class="headerlink" href="#ContactKind.none" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/physics/contact.block" class="ContactKind" signature="begin"></endpoint>
<signature id="ContactKind.begin">ContactKind.begin
<a class="headerlink" href="#ContactKind.begin" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/physics/contact.block" class="ContactKind" signature="end"></endpoint>
<signature id="ContactKind.end">ContactKind.end
<a class="headerlink" href="#ContactKind.end" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/physics/contact.block" class="ContactKind" signature="active"></endpoint>
<signature id="ContactKind.active">ContactKind.active
<a class="headerlink" href="#ContactKind.active" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

