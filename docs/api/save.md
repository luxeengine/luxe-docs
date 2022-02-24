#![](../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2022.0.3`)  


---

## `luxe: save` module

- [Save](#save)   

---

### Save
`:::js import "luxe: save" for Save`
> A cross platform save system with a Key/Value store and file storage.
> 
>   ```js
>     //create a save profile
>     var save = Save.create("organization", "game")
>     //load the profile
>     Save.load(save)
>     
>     //Set some values
>     Save.set(save, "key", "value")
>     //Get some values
>     var name = Save.get(save, "name", "default_name")
>   ```

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

