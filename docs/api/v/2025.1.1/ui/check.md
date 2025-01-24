#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2025.1.1`)  


---

## `luxe: ui/check` module

- [UICheck](#uicheck)   

---

### UICheck
`:::js import "luxe: ui/check" for UICheck`
> `UICheck` is a `Control` that represents a boolean toggle.
> 
>   ```js
>   var check = UICheck.create(ui)
>   UICheck.set_state(check, true)
>   Control.set_events(check) {|event|
>     if(event.type == UIEvent.change) {
>       Log.print("Check is toggled %(event.change ? "on" : "off")")
>     }
>   }
>   ```

- [create](#UICheck.create)(**ui_entity**: `Entity`)
- [set_state](#UICheck.set_state+2)(**control**: `UICheck`, **state**: `Bool`)
- [get_state](#UICheck.get_state)(**control**: `UICheck`)

<hr/>
<endpoint module="luxe: ui/check" class="UICheck" signature="create(ui_entity : Entity)"></endpoint>
<signature id="UICheck.create">UICheck.create(**ui_entity**: `Entity`)
<a class="headerlink" href="#UICheck.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js UICheck`
> Create a new check control.   

<endpoint module="luxe: ui/check" class="UICheck" signature="set_state(control : UICheck, state : Bool)"></endpoint>
<signature id="UICheck.set_state+2">UICheck.set_state(**control**: `UICheck`, **state**: `Bool`)
<a class="headerlink" href="#UICheck.set_state+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the current state of a check.   

<endpoint module="luxe: ui/check" class="UICheck" signature="get_state(control : UICheck)"></endpoint>
<signature id="UICheck.get_state">UICheck.get_state(**control**: `UICheck`)
<a class="headerlink" href="#UICheck.get_state" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Get whether a check is toggled on or off.   

