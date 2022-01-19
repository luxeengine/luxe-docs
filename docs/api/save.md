#![](../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2022.0.3`)  


---

## `luxe: save` module

- [Save](#save)   
- [SaveContext](#savecontext)   

---

### Save
`:::js import "luxe: save" for Save`
> no docs found

- [create](#Save.create+2)(**org**: `String`, **app**: `String`)
- [create](#Save.create+3)(**org**: `String`, **app**: `String`, **slot**: `Num`)
- [create](#Save.create+4)(**org**: `String`, **app**: `String`, **slot**: `Num`, **user_id**: `String`)
- [save](#Save.save)(**save**: `Save`)
- [load](#Save.load)(**save**: `Save`)
- [file_exists](#Save.file_exists+2)(**save**: `Save`, **file_id**: `String`)
- [set_file](#Save.set_file+3)(**save**: `Save`, **file_id**: `String`, **file_contents**: `String`)
- [get_file](#Save.get_file+2)(**save**: `Save`, **file_id**: `String`)
- [set](#Save.set+3)(**save**: `Save`, **key**: `String`, **value**: `Any`)
- [get](#Save.get+3)(**save**: `Save`, **key**: `String`, **default**: `Any`)
- [has](#Save.has+2)(**save**: `Save`, **key**: `String`)
- [get_keys](#Save.get_keys)(**save**: `Save`)

<hr/>
<endpoint module="luxe: save" class="Save" signature="create(org : String, app : String)"></endpoint>
<signature id="Save.create+2">Save.create(**org**: `String`, **app**: `String`)
<a class="headerlink" href="#Save.create+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Save`
> Create a simple save profile for the given organization/app name pair. Defaults to 'user' and slot 0   

<endpoint module="luxe: save" class="Save" signature="create(org : String, app : String, slot : Num)"></endpoint>
<signature id="Save.create+3">Save.create(**org**: `String`, **app**: `String`, **slot**: `Num`)
<a class="headerlink" href="#Save.create+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Save`
> Create a save slot for the given organization/app name pair. Defaults to 'user' for user id   

<endpoint module="luxe: save" class="Save" signature="create(org : String, app : String, slot : Num, user_id : String)"></endpoint>
<signature id="Save.create+4">Save.create(**org**: `String`, **app**: `String`, **slot**: `Num`, **user_id**: `String`)
<a class="headerlink" href="#Save.create+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Save`
> Create a save slot for the given user and organization/app name pair. e.g If you have a steam user ID, you'd pass it in here as a string.   

<endpoint module="luxe: save" class="Save" signature="save(save : Save)"></endpoint>
<signature id="Save.save">Save.save(**save**: `Save`)
<a class="headerlink" href="#Save.save" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Save the data for this profile to storage   

<endpoint module="luxe: save" class="Save" signature="load(save : Save)"></endpoint>
<signature id="Save.load">Save.load(**save**: `Save`)
<a class="headerlink" href="#Save.load" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Load the data for this profile from storage   

<endpoint module="luxe: save" class="Save" signature="file_exists(save : Save, file_id : String)"></endpoint>
<signature id="Save.file_exists+2">Save.file_exists(**save**: `Save`, **file_id**: `String`)
<a class="headerlink" href="#Save.file_exists+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns true if the given file path can be found   

<endpoint module="luxe: save" class="Save" signature="set_file(save : Save, file_id : String, file_contents : String)"></endpoint>
<signature id="Save.set_file+3">Save.set_file(**save**: `Save`, **file_id**: `String`, **file_contents**: `String`)
<a class="headerlink" href="#Save.set_file+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Save the contents of a file at the given path. The path is a relative style path, like `some/file/here`   

<endpoint module="luxe: save" class="Save" signature="get_file(save : Save, file_id : String)"></endpoint>
<signature id="Save.get_file+2">Save.get_file(**save**: `Save`, **file_id**: `String`)
<a class="headerlink" href="#Save.get_file+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Return the contents of the file with the given path. If not found, returns null   

<endpoint module="luxe: save" class="Save" signature="set(save : Save, key : String, value : Any)"></endpoint>
<signature id="Save.set+3">Save.set(**save**: `Save`, **key**: `String`, **value**: `Any`)
<a class="headerlink" href="#Save.set+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Set the value for a key to the given value   

<endpoint module="luxe: save" class="Save" signature="get(save : Save, key : String, default : Any)"></endpoint>
<signature id="Save.get+3">Save.get(**save**: `Save`, **key**: `String`, **default**: `Any`)
<a class="headerlink" href="#Save.get+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns the value for the given key if found, otherwise returns the default provided   

<endpoint module="luxe: save" class="Save" signature="has(save : Save, key : String)"></endpoint>
<signature id="Save.has+2">Save.has(**save**: `Save`, **key**: `String`)
<a class="headerlink" href="#Save.has+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns true if the given key can be found   

<endpoint module="luxe: save" class="Save" signature="get_keys(save : Save)"></endpoint>
<signature id="Save.get_keys">Save.get_keys(**save**: `Save`)
<a class="headerlink" href="#Save.get_keys" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns a list of knowns keys   

### SaveContext
`:::js import "luxe: save" for SaveContext`
> no docs found

- [keys_path](#SaveContext.keys_path)
- [new](#SaveContext.new+4)(**org**: `String`, **app**: `String`, **slot**: `Num`, **user_id**: `String`)
- [set](#SaveContext.set+2)(**key**: `String`, **value**: `Any`)
- [get_keys](#SaveContext.get_keys)()
- [get](#SaveContext.get+2)(**key**: `String`, **default**: `Any`)
- [has](#SaveContext.has)(**key**: `String`)
- [save](#SaveContext.save)()
- [load](#SaveContext.load)()
- [ensure](#SaveContext.ensure)(**file_path**: `String`)
- [set_file](#SaveContext.set_file+2)(**id**: `String`, **contents**: `String`)
- [get_file](#SaveContext.get_file)(**id**: `String`)
- [file_exists](#SaveContext.file_exists)(**id**: `String`)

<hr/>
<endpoint module="luxe: save" class="SaveContext" signature="keys_path"></endpoint>
<signature id="SaveContext.keys_path">SaveContext.keys_path
<a class="headerlink" href="#SaveContext.keys_path" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: save" class="SaveContext" signature="new(org : String, app : String, slot : Num, user_id : String)"></endpoint>
<signature id="SaveContext.new+4">SaveContext.new(**org**: `String`, **app**: `String`, **slot**: `Num`, **user_id**: `String`)
<a class="headerlink" href="#SaveContext.new+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js SaveContext`
> no docs found   

<endpoint module="luxe: save" class="SaveContext" signature="set(key : String, value : Any)"></endpoint>
<signature id="SaveContext.set+2">SaveContext.set(**key**: `String`, **value**: `Any`)
<a class="headerlink" href="#SaveContext.set+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: save" class="SaveContext" signature="get_keys()"></endpoint>
<signature id="SaveContext.get_keys">SaveContext.get_keys()
<a class="headerlink" href="#SaveContext.get_keys" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: save" class="SaveContext" signature="get(key : String, default : Any)"></endpoint>
<signature id="SaveContext.get+2">SaveContext.get(**key**: `String`, **default**: `Any`)
<a class="headerlink" href="#SaveContext.get+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: save" class="SaveContext" signature="has(key : String)"></endpoint>
<signature id="SaveContext.has">SaveContext.has(**key**: `String`)
<a class="headerlink" href="#SaveContext.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: save" class="SaveContext" signature="save()"></endpoint>
<signature id="SaveContext.save">SaveContext.save()
<a class="headerlink" href="#SaveContext.save" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: save" class="SaveContext" signature="load()"></endpoint>
<signature id="SaveContext.load">SaveContext.load()
<a class="headerlink" href="#SaveContext.load" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: save" class="SaveContext" signature="ensure(file_path : String)"></endpoint>
<signature id="SaveContext.ensure">SaveContext.ensure(**file_path**: `String`)
<a class="headerlink" href="#SaveContext.ensure" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: save" class="SaveContext" signature="set_file(id : String, contents : String)"></endpoint>
<signature id="SaveContext.set_file+2">SaveContext.set_file(**id**: `String`, **contents**: `String`)
<a class="headerlink" href="#SaveContext.set_file+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: save" class="SaveContext" signature="get_file(id : String)"></endpoint>
<signature id="SaveContext.get_file">SaveContext.get_file(**id**: `String`)
<a class="headerlink" href="#SaveContext.get_file" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: save" class="SaveContext" signature="file_exists(id : String)"></endpoint>
<signature id="SaveContext.file_exists">SaveContext.file_exists(**id**: `String`)
<a class="headerlink" href="#SaveContext.file_exists" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

