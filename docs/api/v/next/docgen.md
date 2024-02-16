#![](../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.11.1`)  


---

## `luxe: docgen` module

- [DocGen](#docgen)   

---

### DocGen
`:::js import "luxe: docgen" for DocGen`
> no docs found

- [config](#DocGen.config)
- [new](#DocGen.new)(**in_config**: `Map`)
- [get_param_string](#DocGen.get_param_string)(**parameters**: `Any`)
- [get_param_string](#DocGen.get_param_string+2)(**parameters**: `Any`, **display**: `Any`)
- [generate_from_module](#DocGen.generate_from_module)(**module_path**: `String`)
- [generate_from_module](#DocGen.generate_from_module+2)(**config**: `Map`, **module_path**: `String`)
- [get_ast_for_path](#DocGen.get_ast_for_path+2)(**module_prefix**: `String`, **path**: `String`)
- [generate](#DocGen.generate)()
- [generate_from_project](#DocGen.generate_from_project)(**config**: `Any`)
- [generate_from_ast_nodes](#DocGen.generate_from_ast_nodes+2)(**config**: `Map`, **nodes**: `Map`)
- [format_docs](#DocGen.format_docs)(**meta_list**: `Any`)
- [get_alias](#DocGen.get_alias+2)(**meta**: `Any`, **name**: `Any`)
- [signature_url](#DocGen.signature_url+3)(**name**: `Any`, **args**: `Any`, **setter**: `Any`)
- [get_meta](#DocGen.get_meta)(**source_meta**: `Any`)
- [convert_meta](#DocGen.convert_meta)(**in_meta**: `Any`)

<hr/>
<endpoint module="luxe: docgen" class="DocGen" signature="config"></endpoint>
<signature id="DocGen.config">DocGen.config
<a class="headerlink" href="#DocGen.config" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Map`
> no docs found   

<endpoint module="luxe: docgen" class="DocGen" signature="new(in_config : Map)"></endpoint>
<signature id="DocGen.new">DocGen.new(**in_config**: `Map`)
<a class="headerlink" href="#DocGen.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js DocGen`
> no docs found   

<endpoint module="luxe: docgen" class="DocGen" signature="get_param_string(parameters : Any)"></endpoint>
<signature id="DocGen.get_param_string">DocGen.get_param_string(**parameters**: `Any`)
<a class="headerlink" href="#DocGen.get_param_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: docgen" class="DocGen" signature="get_param_string(parameters : Any, display : Any)"></endpoint>
<signature id="DocGen.get_param_string+2">DocGen.get_param_string(**parameters**: `Any`, **display**: `Any`)
<a class="headerlink" href="#DocGen.get_param_string+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: docgen" class="DocGen" signature="generate_from_module(module_path : String)"></endpoint>
<signature id="DocGen.generate_from_module">DocGen.generate_from_module(**module_path**: `String`)
<a class="headerlink" href="#DocGen.generate_from_module" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: docgen" class="DocGen" signature="generate_from_module(config : Map, module_path : String)"></endpoint>
<signature id="DocGen.generate_from_module+2">DocGen.generate_from_module(**config**: `Map`, **module_path**: `String`)
<a class="headerlink" href="#DocGen.generate_from_module+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> takes a raw path for a module and tries to generate documentation for it   

<endpoint module="luxe: docgen" class="DocGen" signature="get_ast_for_path(module_prefix : String, path : String)"></endpoint>
<signature id="DocGen.get_ast_for_path+2">DocGen.get_ast_for_path(**module_prefix**: `String`, **path**: `String`)
<a class="headerlink" href="#DocGen.get_ast_for_path+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: docgen" class="DocGen" signature="generate()"></endpoint>
<signature id="DocGen.generate">DocGen.generate()
<a class="headerlink" href="#DocGen.generate" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: docgen" class="DocGen" signature="generate_from_project(config : Any)"></endpoint>
<signature id="DocGen.generate_from_project">DocGen.generate_from_project(**config**: `Any`)
<a class="headerlink" href="#DocGen.generate_from_project" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: docgen" class="DocGen" signature="generate_from_ast_nodes(config : Map, nodes : Map)"></endpoint>
<signature id="DocGen.generate_from_ast_nodes+2">DocGen.generate_from_ast_nodes(**config**: `Map`, **nodes**: `Map`)
<a class="headerlink" href="#DocGen.generate_from_ast_nodes+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: docgen" class="DocGen" signature="format_docs(meta_list : Any)"></endpoint>
<signature id="DocGen.format_docs">DocGen.format_docs(**meta_list**: `Any`)
<a class="headerlink" href="#DocGen.format_docs" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: docgen" class="DocGen" signature="get_alias(meta : Any, name : Any)"></endpoint>
<signature id="DocGen.get_alias+2">DocGen.get_alias(**meta**: `Any`, **name**: `Any`)
<a class="headerlink" href="#DocGen.get_alias+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: docgen" class="DocGen" signature="signature_url(name : Any, args : Any, setter : Any)"></endpoint>
<signature id="DocGen.signature_url+3">DocGen.signature_url(**name**: `Any`, **args**: `Any`, **setter**: `Any`)
<a class="headerlink" href="#DocGen.signature_url+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: docgen" class="DocGen" signature="get_meta(source_meta : Any)"></endpoint>
<signature id="DocGen.get_meta">DocGen.get_meta(**source_meta**: `Any`)
<a class="headerlink" href="#DocGen.get_meta" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: docgen" class="DocGen" signature="convert_meta(in_meta : Any)"></endpoint>
<signature id="DocGen.convert_meta">DocGen.convert_meta(**in_meta**: `Any`)
<a class="headerlink" href="#DocGen.convert_meta" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

