#![](../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.10.1`)  


---

## `luxe: lx` module

- [LX](#lx)   
- [LXMerge](#lxmerge)   

---

### LX
`:::js import "luxe: lx" for LX`
> no docs found

- [parse_bytes](#LX.parse_bytes+2)(**source_name**: `Any`, **bytes**: `Any`)
- [read](#LX.read)(**path**: `Any`)
- [read](#LX.read+2)(**source_id**: `Any`, **path**: `Any`)
- [parse](#LX.parse)(**data**: `Any`)
- [parse](#LX.parse+2)(**source_path**: `Any`, **data**: `Any`)
- [apply](#LX.apply+2)(**from**: `Any`, **to**: `Any`)
- [clone](#LX.clone)(**lx**: `Any`)
- [equal](#LX.equal+2)(**lxA**: `Any`, **lxB**: `Any`)
- [delta](#LX.delta+2)(**lxA**: `Any`, **lxB**: `Any`)
- [delta_apply](#LX.delta_apply+2)(**lx**: `Any`, **delta**: `Any`)
- [delta_unapply](#LX.delta_unapply+2)(**lx**: `Any`, **delta**: `Any`)
- [key_get](#LX.key_get+2)(**lx**: `Any`, **key**: `Any`)
- [key_get_via_list](#LX.key_get_via_list+2)(**lx**: `Any`, **key**: `Any`)
- [key_remove](#LX.key_remove+2)(**lx**: `Any`, **key**: `Any`)
- [key_remove_via_list](#LX.key_remove_via_list+2)(**lx**: `Any`, **key**: `Any`)
- [key_set](#LX.key_set+3)(**lx**: `Any`, **key**: `Any`, **value**: `Any`)
- [key_set_via_list](#LX.key_set_via_list+3)(**lx**: `Any`, **key**: `Any`, **value**: `Any`)
- [stringify](#LX.stringify)(**root**: `Any`)
- [stringify](#LX.stringify+2)(**root**: `Any`, **spaces**: `Any`)
- [stringify](#LX.stringify+3)(**root**: `Any`, **spaces**: `Any`, **with_root**: `Any`)
- [stringify_to_bytes](#LX.stringify_to_bytes+4)(**root**: `Any`, **max_size**: `Any`, **spaces**: `Any`, **with_root**: `Any`)
- [write](#LX.write+2)(**contents**: `Any`, **path**: `Any`)
- [write](#LX.write+3)(**contents**: `Any`, **path**: `Any`, **spaces**: `Any`)
- [write](#LX.write+4)(**contents**: `Any`, **path**: `Any`, **spaces**: `Any`, **with_root**: `Any`)
- [stringify_to_file](#LX.stringify_to_file+2)(**root**: `Any`, **path**: `Any`)
- [stringify_to_file](#LX.stringify_to_file+4)(**root**: `Any`, **path**: `Any`, **spaces**: `Any`, **with_root**: `Any`)
- [flatten](#LX.flatten)(**lx**: `Any`)
- [flatten](#LX.flatten+2)(**lx**: `Any`, **delimiter**: `Any`)

<hr/>
<endpoint module="luxe: lx" class="LX" signature="parse_bytes(source_name : Any, bytes : Any)"></endpoint>
<signature id="LX.parse_bytes+2">LX.parse_bytes(**source_name**: `Any`, **bytes**: `Any`)
<a class="headerlink" href="#LX.parse_bytes+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Result`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="read(path : Any)"></endpoint>
<signature id="LX.read">LX.read(**path**: `Any`)
<a class="headerlink" href="#LX.read" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="read(source_id : Any, path : Any)"></endpoint>
<signature id="LX.read+2">LX.read(**source_id**: `Any`, **path**: `Any`)
<a class="headerlink" href="#LX.read+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="parse(data : Any)"></endpoint>
<signature id="LX.parse">LX.parse(**data**: `Any`)
<a class="headerlink" href="#LX.parse" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="parse(source_path : Any, data : Any)"></endpoint>
<signature id="LX.parse+2">LX.parse(**source_path**: `Any`, **data**: `Any`)
<a class="headerlink" href="#LX.parse+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="apply(from : Any, to : Any)"></endpoint>
<signature id="LX.apply+2">LX.apply(**from**: `Any`, **to**: `Any`)
<a class="headerlink" href="#LX.apply+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="clone(lx : Any)"></endpoint>
<signature id="LX.clone">LX.clone(**lx**: `Any`)
<a class="headerlink" href="#LX.clone" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="equal(lxA : Any, lxB : Any)"></endpoint>
<signature id="LX.equal+2">LX.equal(**lxA**: `Any`, **lxB**: `Any`)
<a class="headerlink" href="#LX.equal+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="delta(lxA : Any, lxB : Any)"></endpoint>
<signature id="LX.delta+2">LX.delta(**lxA**: `Any`, **lxB**: `Any`)
<a class="headerlink" href="#LX.delta+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="delta_apply(lx : Any, delta : Any)"></endpoint>
<signature id="LX.delta_apply+2">LX.delta_apply(**lx**: `Any`, **delta**: `Any`)
<a class="headerlink" href="#LX.delta_apply+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="delta_unapply(lx : Any, delta : Any)"></endpoint>
<signature id="LX.delta_unapply+2">LX.delta_unapply(**lx**: `Any`, **delta**: `Any`)
<a class="headerlink" href="#LX.delta_unapply+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="key_get(lx : Any, key : Any)"></endpoint>
<signature id="LX.key_get+2">LX.key_get(**lx**: `Any`, **key**: `Any`)
<a class="headerlink" href="#LX.key_get+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="key_get_via_list(lx : Any, key : Any)"></endpoint>
<signature id="LX.key_get_via_list+2">LX.key_get_via_list(**lx**: `Any`, **key**: `Any`)
<a class="headerlink" href="#LX.key_get_via_list+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="key_remove(lx : Any, key : Any)"></endpoint>
<signature id="LX.key_remove+2">LX.key_remove(**lx**: `Any`, **key**: `Any`)
<a class="headerlink" href="#LX.key_remove+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="key_remove_via_list(lx : Any, key : Any)"></endpoint>
<signature id="LX.key_remove_via_list+2">LX.key_remove_via_list(**lx**: `Any`, **key**: `Any`)
<a class="headerlink" href="#LX.key_remove_via_list+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="key_set(lx : Any, key : Any, value : Any)"></endpoint>
<signature id="LX.key_set+3">LX.key_set(**lx**: `Any`, **key**: `Any`, **value**: `Any`)
<a class="headerlink" href="#LX.key_set+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="key_set_via_list(lx : Any, key : Any, value : Any)"></endpoint>
<signature id="LX.key_set_via_list+3">LX.key_set_via_list(**lx**: `Any`, **key**: `Any`, **value**: `Any`)
<a class="headerlink" href="#LX.key_set_via_list+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="stringify(root : Any)"></endpoint>
<signature id="LX.stringify">LX.stringify(**root**: `Any`)
<a class="headerlink" href="#LX.stringify" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="stringify(root : Any, spaces : Any)"></endpoint>
<signature id="LX.stringify+2">LX.stringify(**root**: `Any`, **spaces**: `Any`)
<a class="headerlink" href="#LX.stringify+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="stringify(root : Any, spaces : Any, with_root : Any)"></endpoint>
<signature id="LX.stringify+3">LX.stringify(**root**: `Any`, **spaces**: `Any`, **with_root**: `Any`)
<a class="headerlink" href="#LX.stringify+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="stringify_to_bytes(root : Any, max_size : Any, spaces : Any, with_root : Any)"></endpoint>
<signature id="LX.stringify_to_bytes+4">LX.stringify_to_bytes(**root**: `Any`, **max_size**: `Any`, **spaces**: `Any`, **with_root**: `Any`)
<a class="headerlink" href="#LX.stringify_to_bytes+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="write(contents : Any, path : Any)"></endpoint>
<signature id="LX.write+2">LX.write(**contents**: `Any`, **path**: `Any`)
<a class="headerlink" href="#LX.write+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="write(contents : Any, path : Any, spaces : Any)"></endpoint>
<signature id="LX.write+3">LX.write(**contents**: `Any`, **path**: `Any`, **spaces**: `Any`)
<a class="headerlink" href="#LX.write+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="write(contents : Any, path : Any, spaces : Any, with_root : Any)"></endpoint>
<signature id="LX.write+4">LX.write(**contents**: `Any`, **path**: `Any`, **spaces**: `Any`, **with_root**: `Any`)
<a class="headerlink" href="#LX.write+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="stringify_to_file(root : Any, path : Any)"></endpoint>
<signature id="LX.stringify_to_file+2">LX.stringify_to_file(**root**: `Any`, **path**: `Any`)
<a class="headerlink" href="#LX.stringify_to_file+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="stringify_to_file(root : Any, path : Any, spaces : Any, with_root : Any)"></endpoint>
<signature id="LX.stringify_to_file+4">LX.stringify_to_file(**root**: `Any`, **path**: `Any`, **spaces**: `Any`, **with_root**: `Any`)
<a class="headerlink" href="#LX.stringify_to_file+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="flatten(lx : Any)"></endpoint>
<signature id="LX.flatten">LX.flatten(**lx**: `Any`)
<a class="headerlink" href="#LX.flatten" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LX" signature="flatten(lx : Any, delimiter : Any)"></endpoint>
<signature id="LX.flatten+2">LX.flatten(**lx**: `Any`, **delimiter**: `Any`)
<a class="headerlink" href="#LX.flatten+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### LXMerge
`:::js import "luxe: lx" for LXMerge`
> no docs found

- [merge_map](#LXMerge.merge_map+2)(**from_map**: `Map`, **to_map**: `Map`)
- [merge_list](#LXMerge.merge_list+2)(**from_list**: `List`, **to_list**: `List`)
- [merge](#LXMerge.merge+2)(**from**: `Any`, **to**: `Any`)

<hr/>
<endpoint module="luxe: lx" class="LXMerge" signature="merge_map(from_map : Map, to_map : Map)"></endpoint>
<signature id="LXMerge.merge_map+2">LXMerge.merge_map(**from_map**: `Map`, **to_map**: `Map`)
<a class="headerlink" href="#LXMerge.merge_map+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LXMerge" signature="merge_list(from_list : List, to_list : List)"></endpoint>
<signature id="LXMerge.merge_list+2">LXMerge.merge_list(**from_list**: `List`, **to_list**: `List`)
<a class="headerlink" href="#LXMerge.merge_list+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: lx" class="LXMerge" signature="merge(from : Any, to : Any)"></endpoint>
<signature id="LXMerge.merge+2">LXMerge.merge(**from**: `Any`, **to**: `Any`)
<a class="headerlink" href="#LXMerge.merge+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

