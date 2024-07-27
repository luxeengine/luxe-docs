#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.11.1`)  


---

## `luxe: type/script.asset` module

- [Asset](#asset)   
- [Parsed](#parsed)   
- [ResolveContext](#resolvecontext)   

---

### Asset
`:::js import "luxe: type/script.asset" for Asset`
> no docs found

- [ext](#Asset.ext)
- [subtype](#Asset.subtype)
- [new](#Asset.new+2)(**type_id**: `String`, **ctx**: `AssetContext`)
- [process](#Asset.process+2)(**assets**: `List`, **each**: `Fn`)
- [is_special](#Asset.is_special)(**module_id**: `String`)
- [resolve_import](#Asset.resolve_import)(**import_id**: `String`)
- [resolve_parse](#Asset.resolve_parse+2)(**ctx**: `ResolveContext`, **module_id**: `String`)
- [do_parse](#Asset.do_parse+3)(**ctx**: `ResolveContext`, **module_id**: `String`, **module_path**: `String`)
- [ms](#Asset.ms+2)(**string**: `String`, **start**: `Num`)
- [resolve_methods](#Asset.resolve_methods+3)(**ctx**: `ResolveContext`, **module**: `String`, **type**: `String`)

<hr/>
<endpoint module="luxe: type/script.asset" class="Asset" signature="ext"></endpoint>
<signature id="Asset.ext">Asset.ext
<a class="headerlink" href="#Asset.ext" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/script.asset" class="Asset" signature="subtype"></endpoint>
<signature id="Asset.subtype">Asset.subtype
<a class="headerlink" href="#Asset.subtype" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/script.asset" class="Asset" signature="new(type_id : String, ctx : AssetContext)"></endpoint>
<signature id="Asset.new+2">Asset.new(**type_id**: `String`, **ctx**: `AssetContext`)
<a class="headerlink" href="#Asset.new+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Asset`
> no docs found   

<endpoint module="luxe: type/script.asset" class="Asset" signature="process(assets : List, each : Fn)"></endpoint>
<signature id="Asset.process+2">Asset.process(**assets**: `List`, **each**: `Fn`)
<a class="headerlink" href="#Asset.process+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/script.asset" class="Asset" signature="is_special(module_id : String)"></endpoint>
<signature id="Asset.is_special">Asset.is_special(**module_id**: `String`)
<a class="headerlink" href="#Asset.is_special" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: type/script.asset" class="Asset" signature="resolve_import(import_id : String)"></endpoint>
<signature id="Asset.resolve_import">Asset.resolve_import(**import_id**: `String`)
<a class="headerlink" href="#Asset.resolve_import" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/script.asset" class="Asset" signature="resolve_parse(ctx : ResolveContext, module_id : String)"></endpoint>
<signature id="Asset.resolve_parse+2">Asset.resolve_parse(**ctx**: `ResolveContext`, **module_id**: `String`)
<a class="headerlink" href="#Asset.resolve_parse+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Result`
> no docs found   

<endpoint module="luxe: type/script.asset" class="Asset" signature="do_parse(ctx : ResolveContext, module_id : String, module_path : String)"></endpoint>
<signature id="Asset.do_parse+3">Asset.do_parse(**ctx**: `ResolveContext`, **module_id**: `String`, **module_path**: `String`)
<a class="headerlink" href="#Asset.do_parse+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Module`
> no docs found   

<endpoint module="luxe: type/script.asset" class="Asset" signature="ms(string : String, start : Num)"></endpoint>
<signature id="Asset.ms+2">Asset.ms(**string**: `String`, **start**: `Num`)
<a class="headerlink" href="#Asset.ms+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/script.asset" class="Asset" signature="resolve_methods(ctx : ResolveContext, module : String, type : String)"></endpoint>
<signature id="Asset.resolve_methods+3">Asset.resolve_methods(**ctx**: `ResolveContext`, **module**: `String`, **type**: `String`)
<a class="headerlink" href="#Asset.resolve_methods+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Parsed
`:::js import "luxe: type/script.asset" for Parsed`
> no docs found

- [new](#Parsed.new+3)(**in_db**: `AssetDB`, **in_asset**: `AssetID`, **in_ast**: `Module`)
- [convert_meta](#Parsed.convert_meta)(**in_meta**: `Map`)
- [parse_methods](#Parsed.parse_methods)()

<hr/>
<endpoint module="luxe: type/script.asset" class="Parsed" signature="new(in_db : AssetDB, in_asset : AssetID, in_ast : Module)"></endpoint>
<signature id="Parsed.new+3">Parsed.new(**in_db**: `AssetDB`, **in_asset**: `AssetID`, **in_ast**: `Module`)
<a class="headerlink" href="#Parsed.new+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Parsed`
> no docs found   

<endpoint module="luxe: type/script.asset" class="Parsed" signature="convert_meta(in_meta : Map)"></endpoint>
<signature id="Parsed.convert_meta">Parsed.convert_meta(**in_meta**: `Map`)
<a class="headerlink" href="#Parsed.convert_meta" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: type/script.asset" class="Parsed" signature="parse_methods()"></endpoint>
<signature id="Parsed.parse_methods">Parsed.parse_methods()
<a class="headerlink" href="#Parsed.parse_methods" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### ResolveContext
`:::js import "luxe: type/script.asset" for ResolveContext`
> no docs found

- [new](#ResolveContext.new)()
- [limit](#ResolveContext.limit)()

<hr/>
<endpoint module="luxe: type/script.asset" class="ResolveContext" signature="new()"></endpoint>
<signature id="ResolveContext.new">ResolveContext.new()
<a class="headerlink" href="#ResolveContext.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js ResolveContext`
> no docs found   

<endpoint module="luxe: type/script.asset" class="ResolveContext" signature="limit()"></endpoint>
<signature id="ResolveContext.limit">ResolveContext.limit()
<a class="headerlink" href="#ResolveContext.limit" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

