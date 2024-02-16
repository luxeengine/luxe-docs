#![](../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.11.1`)  


---

## `luxe: settings` module

- [Settings](#settings)   
- [SettingsType](#settingstype)   

---

### Settings
`:::js import "luxe: settings" for Settings`
> no docs found

- [apply](#Settings.apply)(**settings_id**: `String`)
- [apply](#Settings.apply+2)(**settings_id**: `String`, **settings_lx_data**: `String`)
- [unapply](#Settings.unapply)(**settings_id**: `String`)
- [forget](#Settings.forget)(**key**: `String`)
- [has](#Settings.has)(**key**: `String`)
- [get](#Settings.get+2)(**key**: `String`, **default**: `Any`)
- [set_string](#Settings.set_string+3)(**key**: `String`, **value**: `String`, **length**: `Num`)
- [set_number](#Settings.set_number+2)(**key**: `String`, **value**: `Num`)
- [set_bool](#Settings.set_bool+2)(**key**: `String`, **value**: `Bool`)
- [set_float2](#Settings.set_float2+3)(**key**: `String`, **x**: `Num`, **y**: `Num`)
- [set_float3](#Settings.set_float3+4)(**key**: `String`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
- [set_float4](#Settings.set_float4+5)(**key**: `String`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **w**: `Num`)
- [set](#Settings.set+2)(**key**: `String`, **value**: `Any`)

<hr/>
<endpoint module="luxe: settings" class="Settings" signature="apply(settings_id : String)"></endpoint>
<signature id="Settings.apply">Settings.apply(**settings_id**: `String`)
<a class="headerlink" href="#Settings.apply" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: settings" class="Settings" signature="apply(settings_id : String, settings_lx_data : String)"></endpoint>
<signature id="Settings.apply+2">Settings.apply(**settings_id**: `String`, **settings_lx_data**: `String`)
<a class="headerlink" href="#Settings.apply+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: settings" class="Settings" signature="unapply(settings_id : String)"></endpoint>
<signature id="Settings.unapply">Settings.unapply(**settings_id**: `String`)
<a class="headerlink" href="#Settings.unapply" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: settings" class="Settings" signature="forget(key : String)"></endpoint>
<signature id="Settings.forget">Settings.forget(**key**: `String`)
<a class="headerlink" href="#Settings.forget" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: settings" class="Settings" signature="has(key : String)"></endpoint>
<signature id="Settings.has">Settings.has(**key**: `String`)
<a class="headerlink" href="#Settings.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: settings" class="Settings" signature="get(key : String, default : Any)"></endpoint>
<signature id="Settings.get+2">Settings.get(**key**: `String`, **default**: `Any`)
<a class="headerlink" href="#Settings.get+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Any`
> no docs found   

<endpoint module="luxe: settings" class="Settings" signature="set_string(key : String, value : String, length : Num)"></endpoint>
<signature id="Settings.set_string+3">Settings.set_string(**key**: `String`, **value**: `String`, **length**: `Num`)
<a class="headerlink" href="#Settings.set_string+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: settings" class="Settings" signature="set_number(key : String, value : Num)"></endpoint>
<signature id="Settings.set_number+2">Settings.set_number(**key**: `String`, **value**: `Num`)
<a class="headerlink" href="#Settings.set_number+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: settings" class="Settings" signature="set_bool(key : String, value : Bool)"></endpoint>
<signature id="Settings.set_bool+2">Settings.set_bool(**key**: `String`, **value**: `Bool`)
<a class="headerlink" href="#Settings.set_bool+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: settings" class="Settings" signature="set_float2(key : String, x : Num, y : Num)"></endpoint>
<signature id="Settings.set_float2+3">Settings.set_float2(**key**: `String`, **x**: `Num`, **y**: `Num`)
<a class="headerlink" href="#Settings.set_float2+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: settings" class="Settings" signature="set_float3(key : String, x : Num, y : Num, z : Num)"></endpoint>
<signature id="Settings.set_float3+4">Settings.set_float3(**key**: `String`, **x**: `Num`, **y**: `Num`, **z**: `Num`)
<a class="headerlink" href="#Settings.set_float3+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: settings" class="Settings" signature="set_float4(key : String, x : Num, y : Num, z : Num, w : Num)"></endpoint>
<signature id="Settings.set_float4+5">Settings.set_float4(**key**: `String`, **x**: `Num`, **y**: `Num`, **z**: `Num`, **w**: `Num`)
<a class="headerlink" href="#Settings.set_float4+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: settings" class="Settings" signature="set(key : String, value : Any)"></endpoint>
<signature id="Settings.set+2">Settings.set(**key**: `String`, **value**: `Any`)
<a class="headerlink" href="#Settings.set+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

### SettingsType
`:::js import "luxe: settings" for SettingsType`
> no docs found

- [unknown](#SettingsType.unknown)
- [boolean](#SettingsType.boolean)
- [number](#SettingsType.number)
- [string](#SettingsType.string)
- [float2](#SettingsType.float2)
- [float3](#SettingsType.float3)
- [float4](#SettingsType.float4)
- [name](#SettingsType.name)(**value**: `Any`)

<hr/>
<endpoint module="luxe: settings" class="SettingsType" signature="unknown"></endpoint>
<signature id="SettingsType.unknown">SettingsType.unknown
<a class="headerlink" href="#SettingsType.unknown" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: settings" class="SettingsType" signature="boolean"></endpoint>
<signature id="SettingsType.boolean">SettingsType.boolean
<a class="headerlink" href="#SettingsType.boolean" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: settings" class="SettingsType" signature="number"></endpoint>
<signature id="SettingsType.number">SettingsType.number
<a class="headerlink" href="#SettingsType.number" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: settings" class="SettingsType" signature="string"></endpoint>
<signature id="SettingsType.string">SettingsType.string
<a class="headerlink" href="#SettingsType.string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: settings" class="SettingsType" signature="float2"></endpoint>
<signature id="SettingsType.float2">SettingsType.float2
<a class="headerlink" href="#SettingsType.float2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: settings" class="SettingsType" signature="float3"></endpoint>
<signature id="SettingsType.float3">SettingsType.float3
<a class="headerlink" href="#SettingsType.float3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: settings" class="SettingsType" signature="float4"></endpoint>
<signature id="SettingsType.float4">SettingsType.float4
<a class="headerlink" href="#SettingsType.float4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: settings" class="SettingsType" signature="name(value : Any)"></endpoint>
<signature id="SettingsType.name">SettingsType.name(**value**: `Any`)
<a class="headerlink" href="#SettingsType.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

