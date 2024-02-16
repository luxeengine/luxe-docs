#![](../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.11.1`)  


---

## `luxe: save` module

- [Save](#save)   
- [SaveScope](#savescope)   

---

### Save
`:::js import "luxe: save" for Save`
> A cross platform save system with a Key/Value store and file storage for a user, and save slots.
> 
>   ```js
>     //create a new save profile. loads the default save slot for single save use
>     var save = Save.create("organization", "game")
>     
>     //OR
> 
>     //create a new slot and set it as the active save slot 
>     Save.new_slot(save)
>     
>     //OR
> 
>     //Load a save slot from e.g Save.list()
>     var list = Save.list(save)
>     //activate the first slot
>     Save.set_slot(save, list[0])
> 
>     
>     //Set some slot specific values
>     Save.set(save, "key", "value")
>     //Set some user specific values
>     Save.set(save, "key", "value", SaveScope.user)
> 
>     //Get some values from the slot
>     var name = Save.get(save, "name", "default_name")
>     //get user values, like settings
>     var setting = Save.get(save, "setting", false, SaveScope.user)
>   ```

- [create](#Save.create+2)(**org**: `String`, **app**: `String`)
- [create](#Save.create+3)(**org**: `String`, **app**: `String`, **user_id**: `String`)
- [save](#Save.save)(**save**: `Save`)
- [new_slot](#Save.new_slot)(**save**: `Save`)
- [set_slot](#Save.set_slot+2)(**save**: `Save`, **slot**: `String`)
- [list](#Save.list)(**save**: `Save`)
- [file_exists](#Save.file_exists+2)(**save**: `Save`, **file_id**: `String`)
- [file_exists](#Save.file_exists+3)(**save**: `Save`, **file_id**: `String`, **kind**: `SaveScope`)
- [set_file](#Save.set_file+3)(**save**: `Save`, **file_id**: `String`, **file_contents**: `String`)
- [set_file](#Save.set_file+4)(**save**: `Save`, **file_id**: `String`, **file_contents**: `String`, **kind**: `SaveScope`)
- [get_file](#Save.get_file+2)(**save**: `Save`, **file_id**: `String`)
- [get_file](#Save.get_file+3)(**save**: `Save`, **file_id**: `String`, **kind**: `SaveScope`)
- [set](#Save.set+3)(**save**: `Save`, **key**: `String`, **value**: `Any`)
- [set](#Save.set+4)(**save**: `Save`, **key**: `String`, **value**: `Any`, **kind**: `SaveScope`)
- [get](#Save.get+3)(**save**: `Save`, **key**: `String`, **default**: `Any`)
- [get](#Save.get+4)(**save**: `Save`, **key**: `String`, **default**: `Any`, **kind**: `SaveScope`)
- [has](#Save.has+2)(**save**: `Save`, **key**: `String`)
- [has](#Save.has+3)(**save**: `Save`, **key**: `String`, **kind**: `SaveScope`)
- [get_keys](#Save.get_keys)(**save**: `Save`)
- [get_keys](#Save.get_keys+2)(**save**: `Save`, **kind**: `SaveScope`)
- [slot_clear](#Save.slot_clear+2)(**save**: `Save`, **slot**: `String`)
- [slot_backup](#Save.slot_backup+2)(**save**: `Save`, **slot**: `String`)
- [slot_modified_time](#Save.slot_modified_time+2)(**save**: `Save`, **slot**: `String`)
- [slot_file_exists](#Save.slot_file_exists+3)(**save**: `Save`, **slot**: `String`, **file_id**: `String`)
- [slot_set_file](#Save.slot_set_file+4)(**save**: `Save`, **slot**: `String`, **file_id**: `String`, **file_contents**: `String`)
- [slot_get_file](#Save.slot_get_file+3)(**save**: `Save`, **slot**: `String`, **file_id**: `String`)

<hr/>
<endpoint module="luxe: save" class="Save" signature="create(org : String, app : String)"></endpoint>
<signature id="Save.create+2">Save.create(**org**: `String`, **app**: `String`)
<a class="headerlink" href="#Save.create+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Save`
> Create a save slot for the given organization/app name pair. Defaults to 'user' for user id   

<endpoint module="luxe: save" class="Save" signature="create(org : String, app : String, user_id : String)"></endpoint>
<signature id="Save.create+3">Save.create(**org**: `String`, **app**: `String`, **user_id**: `String`)
<a class="headerlink" href="#Save.create+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Save`
> Create a save slot for the given user and organization/app name pair. e.g If you have a steam user ID, you'd pass it in here as a string.   

<endpoint module="luxe: save" class="Save" signature="save(save : Save)"></endpoint>
<signature id="Save.save">Save.save(**save**: `Save`)
<a class="headerlink" href="#Save.save" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Flush the data for this profile to storage. Unless auto save on key change is off, unnecessary   

<endpoint module="luxe: save" class="Save" signature="new_slot(save : Save)"></endpoint>
<signature id="Save.new_slot">Save.new_slot(**save**: `Save`)
<a class="headerlink" href="#Save.new_slot" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the current active save slot to a new slot ID.   

<endpoint module="luxe: save" class="Save" signature="set_slot(save : Save, slot : String)"></endpoint>
<signature id="Save.set_slot+2">Save.set_slot(**save**: `Save`, **slot**: `String`)
<a class="headerlink" href="#Save.set_slot+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Set the current active save slot to a Slot ID (from Save.list or otherwise).   

<endpoint module="luxe: save" class="Save" signature="list(save : Save)"></endpoint>
<signature id="Save.list">Save.list(**save**: `Save`)
<a class="headerlink" href="#Save.list" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Return a list of save slot uuids for use with the slot query apis, sorted by modified time (latest first)   

<endpoint module="luxe: save" class="Save" signature="file_exists(save : Save, file_id : String)"></endpoint>
<signature id="Save.file_exists+2">Save.file_exists(**save**: `Save`, **file_id**: `String`)
<a class="headerlink" href="#Save.file_exists+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns true if the given file path can be found for the active save slot   

<endpoint module="luxe: save" class="Save" signature="file_exists(save : Save, file_id : String, kind : SaveScope)"></endpoint>
<signature id="Save.file_exists+3">Save.file_exists(**save**: `Save`, **file_id**: `String`, **kind**: `SaveScope`)
<a class="headerlink" href="#Save.file_exists+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns true if the given file path can be found   

<endpoint module="luxe: save" class="Save" signature="set_file(save : Save, file_id : String, file_contents : String)"></endpoint>
<signature id="Save.set_file+3">Save.set_file(**save**: `Save`, **file_id**: `String`, **file_contents**: `String`)
<a class="headerlink" href="#Save.set_file+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Save the contents of a file at the given path for the active save slot. The path is a relative style path, like `some/file/here`   

<endpoint module="luxe: save" class="Save" signature="set_file(save : Save, file_id : String, file_contents : String, kind : SaveScope)"></endpoint>
<signature id="Save.set_file+4">Save.set_file(**save**: `Save`, **file_id**: `String`, **file_contents**: `String`, **kind**: `SaveScope`)
<a class="headerlink" href="#Save.set_file+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Save the contents of a file at the given path. The path is a relative style path, like `some/file/here`   

<endpoint module="luxe: save" class="Save" signature="get_file(save : Save, file_id : String)"></endpoint>
<signature id="Save.get_file+2">Save.get_file(**save**: `Save`, **file_id**: `String`)
<a class="headerlink" href="#Save.get_file+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Return the contents of the file with the given path for the active save slot. If not found, returns null   

<endpoint module="luxe: save" class="Save" signature="get_file(save : Save, file_id : String, kind : SaveScope)"></endpoint>
<signature id="Save.get_file+3">Save.get_file(**save**: `Save`, **file_id**: `String`, **kind**: `SaveScope`)
<a class="headerlink" href="#Save.get_file+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Return the contents of the file with the given path. If not found, returns null   

<endpoint module="luxe: save" class="Save" signature="set(save : Save, key : String, value : Any)"></endpoint>
<signature id="Save.set+3">Save.set(**save**: `Save`, **key**: `String`, **value**: `Any`)
<a class="headerlink" href="#Save.set+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Set the value for a key to the given value, for the active save slot   

<endpoint module="luxe: save" class="Save" signature="set(save : Save, key : String, value : Any, kind : SaveScope)"></endpoint>
<signature id="Save.set+4">Save.set(**save**: `Save`, **key**: `String`, **value**: `Any`, **kind**: `SaveScope`)
<a class="headerlink" href="#Save.set+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Set the value for a key to the given value   

<endpoint module="luxe: save" class="Save" signature="get(save : Save, key : String, default : Any)"></endpoint>
<signature id="Save.get+3">Save.get(**save**: `Save`, **key**: `String`, **default**: `Any`)
<a class="headerlink" href="#Save.get+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns the value for the given key if found, otherwise returns the default provided, for the active save slot   

<endpoint module="luxe: save" class="Save" signature="get(save : Save, key : String, default : Any, kind : SaveScope)"></endpoint>
<signature id="Save.get+4">Save.get(**save**: `Save`, **key**: `String`, **default**: `Any`, **kind**: `SaveScope`)
<a class="headerlink" href="#Save.get+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns the value for the given key if found, otherwise returns the default provided   

<endpoint module="luxe: save" class="Save" signature="has(save : Save, key : String)"></endpoint>
<signature id="Save.has+2">Save.has(**save**: `Save`, **key**: `String`)
<a class="headerlink" href="#Save.has+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns true if the given key can be found, for the active save slot   

<endpoint module="luxe: save" class="Save" signature="has(save : Save, key : String, kind : SaveScope)"></endpoint>
<signature id="Save.has+3">Save.has(**save**: `Save`, **key**: `String`, **kind**: `SaveScope`)
<a class="headerlink" href="#Save.has+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns true if the given key can be found   

<endpoint module="luxe: save" class="Save" signature="get_keys(save : Save)"></endpoint>
<signature id="Save.get_keys">Save.get_keys(**save**: `Save`)
<a class="headerlink" href="#Save.get_keys" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns a list of knowns keys, for the active save slot   

<endpoint module="luxe: save" class="Save" signature="get_keys(save : Save, kind : SaveScope)"></endpoint>
<signature id="Save.get_keys+2">Save.get_keys(**save**: `Save`, **kind**: `SaveScope`)
<a class="headerlink" href="#Save.get_keys+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns a list of knowns keys   

<endpoint module="luxe: save" class="Save" signature="slot_clear(save : Save, slot : String)"></endpoint>
<signature id="Save.slot_clear+2">Save.slot_clear(**save**: `Save`, **slot**: `String`)
<a class="headerlink" href="#Save.slot_clear+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Slot query. Delete a save slot, return true or false for success   

<endpoint module="luxe: save" class="Save" signature="slot_backup(save : Save, slot : String)"></endpoint>
<signature id="Save.slot_backup+2">Save.slot_backup(**save**: `Save`, **slot**: `String`)
<a class="headerlink" href="#Save.slot_backup+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Slot query. Makes a backup of the slot, returns a slot ID of the backup if successful, null if false   

<endpoint module="luxe: save" class="Save" signature="slot_modified_time(save : Save, slot : String)"></endpoint>
<signature id="Save.slot_modified_time+2">Save.slot_modified_time(**save**: `Save`, **slot**: `String`)
<a class="headerlink" href="#Save.slot_modified_time+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Slot query. Returns the modified time for the given save slot ID   

<endpoint module="luxe: save" class="Save" signature="slot_file_exists(save : Save, slot : String, file_id : String)"></endpoint>
<signature id="Save.slot_file_exists+3">Save.slot_file_exists(**save**: `Save`, **slot**: `String`, **file_id**: `String`)
<a class="headerlink" href="#Save.slot_file_exists+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Slot query. Returns true if the given file path can be found for the given save slot ID   

<endpoint module="luxe: save" class="Save" signature="slot_set_file(save : Save, slot : String, file_id : String, file_contents : String)"></endpoint>
<signature id="Save.slot_set_file+4">Save.slot_set_file(**save**: `Save`, **slot**: `String`, **file_id**: `String`, **file_contents**: `String`)
<a class="headerlink" href="#Save.slot_set_file+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Slot query. Save the contents of a file at the given path for the given slot ID. The path is a relative style path, like `some/file/here`   

<endpoint module="luxe: save" class="Save" signature="slot_get_file(save : Save, slot : String, file_id : String)"></endpoint>
<signature id="Save.slot_get_file+3">Save.slot_get_file(**save**: `Save`, **slot**: `String`, **file_id**: `String`)
<a class="headerlink" href="#Save.slot_get_file+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Slot query. Return the contents of the file with the given path for the given slot ID. If not found, returns null   

### SaveScope
`:::js import "luxe: save" for SaveScope`
> no docs found

- [slot](#SaveScope.slot)
- [user](#SaveScope.user)

<hr/>
<endpoint module="luxe: save" class="SaveScope" signature="slot"></endpoint>
<signature id="SaveScope.slot">SaveScope.slot
<a class="headerlink" href="#SaveScope.slot" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: save" class="SaveScope" signature="user"></endpoint>
<signature id="SaveScope.user">SaveScope.user
<a class="headerlink" href="#SaveScope.user" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

