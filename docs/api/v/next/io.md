#![](../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2024.12.4`)  


---

## `luxe: io` module

- [DirNode](#dirnode)   
- [Flags](#flags)   
- [PlotType](#plottype)   
- [ProcFlags](#procflags)   

---

### DirNode
`:::js import "luxe: io" for DirNode`
> no docs found

- [path](#DirNode.path)
- [name](#DirNode.name)
- [ext](#DirNode.ext)
- [is_regular](#DirNode.is_regular)
- [is_directory](#DirNode.is_directory)
- [new](#DirNode.new+5)(**in_path**: `Any`, **in_name**: `Any`, **in_ext**: `Any`, **in_is_regular**: `Any`, **in_is_directory**: `Any`)

<hr/>
<endpoint module="luxe: io" class="DirNode" signature="path"></endpoint>
<signature id="DirNode.path">DirNode.path
<a class="headerlink" href="#DirNode.path" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: io" class="DirNode" signature="name"></endpoint>
<signature id="DirNode.name">DirNode.name
<a class="headerlink" href="#DirNode.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: io" class="DirNode" signature="ext"></endpoint>
<signature id="DirNode.ext">DirNode.ext
<a class="headerlink" href="#DirNode.ext" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: io" class="DirNode" signature="is_regular"></endpoint>
<signature id="DirNode.is_regular">DirNode.is_regular
<a class="headerlink" href="#DirNode.is_regular" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: io" class="DirNode" signature="is_directory"></endpoint>
<signature id="DirNode.is_directory">DirNode.is_directory
<a class="headerlink" href="#DirNode.is_directory" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: io" class="DirNode" signature="new(in_path : Any, in_name : Any, in_ext : Any, in_is_regular : Any, in_is_directory : Any)"></endpoint>
<signature id="DirNode.new+5">DirNode.new(**in_path**: `Any`, **in_name**: `Any`, **in_ext**: `Any`, **in_is_regular**: `Any`, **in_is_directory**: `Any`)
<a class="headerlink" href="#DirNode.new+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js DirNode`
> no docs found   

### Flags
`:::js import "luxe: io" for Flags`
> no docs found

- [new](#Flags.new)(**args**: `Any`)
- [all](#Flags.all)()
- [has](#Flags.has)(**flag**: `Any`)
- [value](#Flags.value)(**flag**: `Any`)
- [value](#Flags.value+2)(**flag**: `Any`, **require**: `Any`)
- [values](#Flags.values)(**flag**: `Any`)
- [values](#Flags.values+2)(**flag**: `Any`, **require**: `Any`)

<hr/>
<endpoint module="luxe: io" class="Flags" signature="new(args : Any)"></endpoint>
<signature id="Flags.new">Flags.new(**args**: `Any`)
<a class="headerlink" href="#Flags.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Flags`
> no docs found   

<endpoint module="luxe: io" class="Flags" signature="all()"></endpoint>
<signature id="Flags.all">Flags.all()
<a class="headerlink" href="#Flags.all" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: io" class="Flags" signature="has(flag : Any)"></endpoint>
<signature id="Flags.has">Flags.has(**flag**: `Any`)
<a class="headerlink" href="#Flags.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: io" class="Flags" signature="value(flag : Any)"></endpoint>
<signature id="Flags.value">Flags.value(**flag**: `Any`)
<a class="headerlink" href="#Flags.value" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: io" class="Flags" signature="value(flag : Any, require : Any)"></endpoint>
<signature id="Flags.value+2">Flags.value(**flag**: `Any`, **require**: `Any`)
<a class="headerlink" href="#Flags.value+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: io" class="Flags" signature="values(flag : Any)"></endpoint>
<signature id="Flags.values">Flags.values(**flag**: `Any`)
<a class="headerlink" href="#Flags.values" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: io" class="Flags" signature="values(flag : Any, require : Any)"></endpoint>
<signature id="Flags.values+2">Flags.values(**flag**: `Any`, **require**: `Any`)
<a class="headerlink" href="#Flags.values+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### PlotType
`:::js import "luxe: io" for PlotType`
> no docs found

- [normal](#PlotType.normal)
- [counter](#PlotType.counter)

<hr/>
<endpoint module="luxe: io" class="PlotType" signature="normal"></endpoint>
<signature id="PlotType.normal">PlotType.normal
<a class="headerlink" href="#PlotType.normal" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: io" class="PlotType" signature="counter"></endpoint>
<signature id="PlotType.counter">PlotType.counter
<a class="headerlink" href="#PlotType.counter" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### ProcFlags
`:::js import "luxe: io" for ProcFlags`
> no docs found

- [none](#ProcFlags.none)
- [setuid](#ProcFlags.setuid)
- [setgid](#ProcFlags.setgid)
- [windows_verbatim_arguments](#ProcFlags.windows_verbatim_arguments)
- [detached](#ProcFlags.detached)
- [windows_hide](#ProcFlags.windows_hide)
- [windows_hide_console](#ProcFlags.windows_hide_console)
- [windows_hide_gui](#ProcFlags.windows_hide_gui)

<hr/>
<endpoint module="luxe: io" class="ProcFlags" signature="none"></endpoint>
<signature id="ProcFlags.none">ProcFlags.none
<a class="headerlink" href="#ProcFlags.none" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: io" class="ProcFlags" signature="setuid"></endpoint>
<signature id="ProcFlags.setuid">ProcFlags.setuid
<a class="headerlink" href="#ProcFlags.setuid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: io" class="ProcFlags" signature="setgid"></endpoint>
<signature id="ProcFlags.setgid">ProcFlags.setgid
<a class="headerlink" href="#ProcFlags.setgid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: io" class="ProcFlags" signature="windows_verbatim_arguments"></endpoint>
<signature id="ProcFlags.windows_verbatim_arguments">ProcFlags.windows_verbatim_arguments
<a class="headerlink" href="#ProcFlags.windows_verbatim_arguments" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: io" class="ProcFlags" signature="detached"></endpoint>
<signature id="ProcFlags.detached">ProcFlags.detached
<a class="headerlink" href="#ProcFlags.detached" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: io" class="ProcFlags" signature="windows_hide"></endpoint>
<signature id="ProcFlags.windows_hide">ProcFlags.windows_hide
<a class="headerlink" href="#ProcFlags.windows_hide" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: io" class="ProcFlags" signature="windows_hide_console"></endpoint>
<signature id="ProcFlags.windows_hide_console">ProcFlags.windows_hide_console
<a class="headerlink" href="#ProcFlags.windows_hide_console" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: io" class="ProcFlags" signature="windows_hide_gui"></endpoint>
<signature id="ProcFlags.windows_hide_gui">ProcFlags.windows_hide_gui
<a class="headerlink" href="#ProcFlags.windows_hide_gui" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

