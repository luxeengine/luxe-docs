#![](../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.11.1`)  


---

## `luxe: assets` module

- [Assets](#assets)   
- [Strings](#strings)   

---

### Assets
`:::js import "luxe: assets" for Assets`
> The `Assets` services is how you access loaded assets, and query if an asset is loaded.
> The primary use for this at the moment is the accessors like `Assets.image`, and finding out 
> if an asset is loaded via `Assets.has_image`. 
> 
> Note that the asset system is a work in progress and is not final. 
> There are several accessors missing, for example, fonts are often referenced 
> as a string, not via `Assets.font("fonts/name")`. Later, all assets will be unified into this form as intended.
> 
> Also, they're supposed to be able to reload dynamically, many can't currently. And remember the input
> to the asset system is compiled assets, not the assets themselves. 
> 
> Finally, there are functions in the API that shouldn't be used directly (they aren't listed here.)

- [db_init](#Assets.db_init)()
- [db_commit](#Assets.db_commit)(**db**: `AssetDB`)
- [db_default](#Assets.db_default)()
- [db_default_set](#Assets.db_default_set)(**db**: `AssetDB`)
- [db_commit_post](#Assets.db_commit_post)(**db**: `AssetDB`)
- [db_commit_refs](#Assets.db_commit_refs)(**db**: `AssetDB`)
- [db_add_root_path](#Assets.db_add_root_path+4)(**db**: `AssetDB`, **path**: `String`, **subfolder**: `String`, **prefix**: `String`)
- [db_add_item](#Assets.db_add_item+4)(**db**: `AssetDB`, **root**: `String`, **path**: `String`, **is_directory**: `Bool`)
- [db_make_item](#Assets.db_make_item+4)(**db**: `AssetDB`, **root**: `String`, **path**: `String`, **is_directory**: `Bool`)
- [db_make_item](#Assets.db_make_item+3)(**db**: `AssetDB`, **root**: `String`, **path**: `String`)
- [db_remove_item](#Assets.db_remove_item+2)(**db**: `AssetDB`, **asset_id**: `String`)
- [db_add_item](#Assets.db_add_item+3)(**db**: `AssetDB`, **root**: `String`, **path**: `String`)
- [db_add_ignore](#Assets.db_add_ignore+2)(**db**: `AssetDB`, **globs**: `List`)
- [db_asset_from_path](#Assets.db_asset_from_path+2)(**db**: `AssetDB`, **path**: `String`)
- [db_asset_from_id](#Assets.db_asset_from_id+2)(**db**: `AssetDB`, **asset_id**: `String`)
- [db_asset_from_uuid](#Assets.db_asset_from_uuid+2)(**db**: `AssetDB`, **meta_uuid**: `String`)
- [db_asset_get_root](#Assets.db_asset_get_root+2)(**db**: `AssetDB`, **asset_id**: `String`)
- [db_compile](#Assets.db_compile)(**db**: `AssetDB`)
- [db_parse](#Assets.db_parse)(**bytes**: `String`)
- [db_has](#Assets.db_has+2)(**db**: `AssetDB`, **asset_id**: `String`)
- [db_add_reference](#Assets.db_add_reference+3)(**db**: `AssetDB`, **from_asset_id**: `String`, **to_asset_id**: `String`)
- [db_reset_references](#Assets.db_reset_references+2)(**db**: `AssetDB`, **asset_id**: `String`)
- [db_get_references](#Assets.db_get_references+2)(**db**: `AssetDB`, **asset_id**: `String`)
- [db_get_referenced_by](#Assets.db_get_referenced_by+2)(**db**: `AssetDB`, **asset_id**: `String`)
- [list](#Assets.list)(**db**: `AssetDB`)
- [list](#Assets.list+3)(**db**: `AssetDB`, **ext**: `String`, **subtype**: `String`)
- [list](#Assets.list+4)(**db**: `AssetDB`, **ext**: `String`, **subtype**: `String`, **root**: `String`)
- [list](#Assets.list+2)(**db**: `AssetDB`, **ext**: `String`)
- [list_folders](#Assets.list_folders+3)(**db**: `AssetDB`, **root**: `String`, **use_path**: `Bool`)
- [db_get_tags](#Assets.db_get_tags+2)(**db**: `AssetDB`, **asset_id**: `String`)
- [db_get_tagged](#Assets.db_get_tagged+2)(**db**: `AssetDB`, **tag**: `String`)
- [db_get_tagged_from_list](#Assets.db_get_tagged_from_list+2)(**db**: `AssetDB`, **tags**: `List`)
- [db_add_tags](#Assets.db_add_tags+3)(**db**: `AssetDB`, **asset_id**: `String`, **tags**: `List`)
- [db_remove_tags](#Assets.db_remove_tags+3)(**db**: `AssetDB`, **asset_id**: `String`, **tags**: `List`)
- [modified](#Assets.modified+2)(**db**: `AssetDB`, **query_id**: `String`)
- [modified](#Assets.modified+4)(**db**: `AssetDB`, **query_id**: `String`, **ext**: `String`, **subtype**: `String`)
- [modified](#Assets.modified+5)(**db**: `AssetDB`, **query_id**: `String`, **ext**: `String`, **subtype**: `String`, **root**: `String`)
- [modified](#Assets.modified+3)(**db**: `AssetDB`, **query_id**: `String`, **ext**: `String`)
- [unmodified](#Assets.unmodified+3)(**db**: `AssetDB`, **query_id**: `String`, **asset_id**: `String`)
- [modify](#Assets.modify+3)(**db**: `AssetDB`, **query_id**: `String`, **asset_id**: `String`)
- [is_modified](#Assets.is_modified+3)(**db**: `AssetDB`, **query_id**: `String`, **asset_id**: `String`)
- [get_data](#Assets.get_data+2)(**type_id**: `String`, **id**: `String`)
- [get_block](#Assets.get_block)(**type_id**: `String`)
- [get_handle](#Assets.get_handle+2)(**type_id**: `String`, **id**: `String`)
- [set_handle](#Assets.set_handle+3)(**type_id**: `String`, **id**: `String`, **handle**: `Num`)
- [get_dev_version_path](#Assets.get_dev_version_path+2)(**db**: `AssetDB`, **asset_id**: `String`)
- [get_dev_version_data](#Assets.get_dev_version_data+2)(**db**: `AssetDB`, **asset_id**: `String`)
- [save_dev_version_data](#Assets.save_dev_version_data+3)(**db**: `AssetDB`, **asset_id**: `String`, **version_data**: `Map`)
- [image](#Assets.image)(**id**: `String`)
- [bytes](#Assets.bytes)(**id**: `String`)
- [material](#Assets.material)(**id**: `String`)
- [atlas](#Assets.atlas)(**id**: `String`)
- [lx](#Assets.lx)(**id**: `String`)
- [has_shader_library](#Assets.has_shader_library)(**id**: `String`)
- [has_image](#Assets.has_image)(**id**: `String`)
- [has_material_basis](#Assets.has_material_basis)(**id**: `String`)
- [has_material](#Assets.has_material)(**id**: `String`)
- [has_bytes](#Assets.has_bytes)(**id**: `String`)
- [has_settings](#Assets.has_settings)(**id**: `String`)
- [has_atlas](#Assets.has_atlas)(**id**: `String`)
- [has_physics](#Assets.has_physics)(**id**: `String`)
- [has_prototype](#Assets.has_prototype)(**id**: `String`)
- [has_scene](#Assets.has_scene)(**id**: `String`)
- [has_input](#Assets.has_input)(**id**: `String`)
- [has_anim](#Assets.has_anim)(**id**: `String`)
- [has_mesh](#Assets.has_mesh)(**id**: `String`)
- [has_tiles](#Assets.has_tiles)(**id**: `String`)
- [has_ui](#Assets.has_ui)(**id**: `String`)
- [unload_input](#Assets.unload_input)(**id**: `String`)
- [load_input](#Assets.load_input)(**id**: `String`)

<hr/>
<endpoint module="luxe: assets" class="Assets" signature="db_init()"></endpoint>
<signature id="Assets.db_init">Assets.db_init()
<a class="headerlink" href="#Assets.db_init" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AssetDB`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_commit(db : AssetDB)"></endpoint>
<signature id="Assets.db_commit">Assets.db_commit(**db**: `AssetDB`)
<a class="headerlink" href="#Assets.db_commit" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_default()"></endpoint>
<signature id="Assets.db_default">Assets.db_default()
<a class="headerlink" href="#Assets.db_default" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AssetDB`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_default_set(db : AssetDB)"></endpoint>
<signature id="Assets.db_default_set">Assets.db_default_set(**db**: `AssetDB`)
<a class="headerlink" href="#Assets.db_default_set" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_commit_post(db : AssetDB)"></endpoint>
<signature id="Assets.db_commit_post">Assets.db_commit_post(**db**: `AssetDB`)
<a class="headerlink" href="#Assets.db_commit_post" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_commit_refs(db : AssetDB)"></endpoint>
<signature id="Assets.db_commit_refs">Assets.db_commit_refs(**db**: `AssetDB`)
<a class="headerlink" href="#Assets.db_commit_refs" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_add_root_path(db : AssetDB, path : String, subfolder : String, prefix : String)"></endpoint>
<signature id="Assets.db_add_root_path+4">Assets.db_add_root_path(**db**: `AssetDB`, **path**: `String`, **subfolder**: `String`, **prefix**: `String`)
<a class="headerlink" href="#Assets.db_add_root_path+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_add_item(db : AssetDB, root : String, path : String, is_directory : Bool)"></endpoint>
<signature id="Assets.db_add_item+4">Assets.db_add_item(**db**: `AssetDB`, **root**: `String`, **path**: `String`, **is_directory**: `Bool`)
<a class="headerlink" href="#Assets.db_add_item+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_make_item(db : AssetDB, root : String, path : String, is_directory : Bool)"></endpoint>
<signature id="Assets.db_make_item+4">Assets.db_make_item(**db**: `AssetDB`, **root**: `String`, **path**: `String`, **is_directory**: `Bool`)
<a class="headerlink" href="#Assets.db_make_item+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Map`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_make_item(db : AssetDB, root : String, path : String)"></endpoint>
<signature id="Assets.db_make_item+3">Assets.db_make_item(**db**: `AssetDB`, **root**: `String`, **path**: `String`)
<a class="headerlink" href="#Assets.db_make_item+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_remove_item(db : AssetDB, asset_id : String)"></endpoint>
<signature id="Assets.db_remove_item+2">Assets.db_remove_item(**db**: `AssetDB`, **asset_id**: `String`)
<a class="headerlink" href="#Assets.db_remove_item+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_add_item(db : AssetDB, root : String, path : String)"></endpoint>
<signature id="Assets.db_add_item+3">Assets.db_add_item(**db**: `AssetDB`, **root**: `String`, **path**: `String`)
<a class="headerlink" href="#Assets.db_add_item+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_add_ignore(db : AssetDB, globs : List)"></endpoint>
<signature id="Assets.db_add_ignore+2">Assets.db_add_ignore(**db**: `AssetDB`, **globs**: `List`)
<a class="headerlink" href="#Assets.db_add_ignore+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_asset_from_path(db : AssetDB, path : String)"></endpoint>
<signature id="Assets.db_asset_from_path+2">Assets.db_asset_from_path(**db**: `AssetDB`, **path**: `String`)
<a class="headerlink" href="#Assets.db_asset_from_path+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Map`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_asset_from_id(db : AssetDB, asset_id : String)"></endpoint>
<signature id="Assets.db_asset_from_id+2">Assets.db_asset_from_id(**db**: `AssetDB`, **asset_id**: `String`)
<a class="headerlink" href="#Assets.db_asset_from_id+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Map`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_asset_from_uuid(db : AssetDB, meta_uuid : String)"></endpoint>
<signature id="Assets.db_asset_from_uuid+2">Assets.db_asset_from_uuid(**db**: `AssetDB`, **meta_uuid**: `String`)
<a class="headerlink" href="#Assets.db_asset_from_uuid+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Map`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_asset_get_root(db : AssetDB, asset_id : String)"></endpoint>
<signature id="Assets.db_asset_get_root+2">Assets.db_asset_get_root(**db**: `AssetDB`, **asset_id**: `String`)
<a class="headerlink" href="#Assets.db_asset_get_root+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_compile(db : AssetDB)"></endpoint>
<signature id="Assets.db_compile">Assets.db_compile(**db**: `AssetDB`)
<a class="headerlink" href="#Assets.db_compile" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_parse(bytes : String)"></endpoint>
<signature id="Assets.db_parse">Assets.db_parse(**bytes**: `String`)
<a class="headerlink" href="#Assets.db_parse" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AssetDB`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_has(db : AssetDB, asset_id : String)"></endpoint>
<signature id="Assets.db_has+2">Assets.db_has(**db**: `AssetDB`, **asset_id**: `String`)
<a class="headerlink" href="#Assets.db_has+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_add_reference(db : AssetDB, from_asset_id : String, to_asset_id : String)"></endpoint>
<signature id="Assets.db_add_reference+3">Assets.db_add_reference(**db**: `AssetDB`, **from_asset_id**: `String`, **to_asset_id**: `String`)
<a class="headerlink" href="#Assets.db_add_reference+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_reset_references(db : AssetDB, asset_id : String)"></endpoint>
<signature id="Assets.db_reset_references+2">Assets.db_reset_references(**db**: `AssetDB`, **asset_id**: `String`)
<a class="headerlink" href="#Assets.db_reset_references+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_get_references(db : AssetDB, asset_id : String)"></endpoint>
<signature id="Assets.db_get_references+2">Assets.db_get_references(**db**: `AssetDB`, **asset_id**: `String`)
<a class="headerlink" href="#Assets.db_get_references+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_get_referenced_by(db : AssetDB, asset_id : String)"></endpoint>
<signature id="Assets.db_get_referenced_by+2">Assets.db_get_referenced_by(**db**: `AssetDB`, **asset_id**: `String`)
<a class="headerlink" href="#Assets.db_get_referenced_by+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="list(db : AssetDB)"></endpoint>
<signature id="Assets.list">Assets.list(**db**: `AssetDB`)
<a class="headerlink" href="#Assets.list" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="list(db : AssetDB, ext : String, subtype : String)"></endpoint>
<signature id="Assets.list+3">Assets.list(**db**: `AssetDB`, **ext**: `String`, **subtype**: `String`)
<a class="headerlink" href="#Assets.list+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="list(db : AssetDB, ext : String, subtype : String, root : String)"></endpoint>
<signature id="Assets.list+4">Assets.list(**db**: `AssetDB`, **ext**: `String`, **subtype**: `String`, **root**: `String`)
<a class="headerlink" href="#Assets.list+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="list(db : AssetDB, ext : String)"></endpoint>
<signature id="Assets.list+2">Assets.list(**db**: `AssetDB`, **ext**: `String`)
<a class="headerlink" href="#Assets.list+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="list_folders(db : AssetDB, root : String, use_path : Bool)"></endpoint>
<signature id="Assets.list_folders+3">Assets.list_folders(**db**: `AssetDB`, **root**: `String`, **use_path**: `Bool`)
<a class="headerlink" href="#Assets.list_folders+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_get_tags(db : AssetDB, asset_id : String)"></endpoint>
<signature id="Assets.db_get_tags+2">Assets.db_get_tags(**db**: `AssetDB`, **asset_id**: `String`)
<a class="headerlink" href="#Assets.db_get_tags+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_get_tagged(db : AssetDB, tag : String)"></endpoint>
<signature id="Assets.db_get_tagged+2">Assets.db_get_tagged(**db**: `AssetDB`, **tag**: `String`)
<a class="headerlink" href="#Assets.db_get_tagged+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_get_tagged_from_list(db : AssetDB, tags : List)"></endpoint>
<signature id="Assets.db_get_tagged_from_list+2">Assets.db_get_tagged_from_list(**db**: `AssetDB`, **tags**: `List`)
<a class="headerlink" href="#Assets.db_get_tagged_from_list+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_add_tags(db : AssetDB, asset_id : String, tags : List)"></endpoint>
<signature id="Assets.db_add_tags+3">Assets.db_add_tags(**db**: `AssetDB`, **asset_id**: `String`, **tags**: `List`)
<a class="headerlink" href="#Assets.db_add_tags+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="db_remove_tags(db : AssetDB, asset_id : String, tags : List)"></endpoint>
<signature id="Assets.db_remove_tags+3">Assets.db_remove_tags(**db**: `AssetDB`, **asset_id**: `String`, **tags**: `List`)
<a class="headerlink" href="#Assets.db_remove_tags+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="modified(db : AssetDB, query_id : String)"></endpoint>
<signature id="Assets.modified+2">Assets.modified(**db**: `AssetDB`, **query_id**: `String`)
<a class="headerlink" href="#Assets.modified+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="modified(db : AssetDB, query_id : String, ext : String, subtype : String)"></endpoint>
<signature id="Assets.modified+4">Assets.modified(**db**: `AssetDB`, **query_id**: `String`, **ext**: `String`, **subtype**: `String`)
<a class="headerlink" href="#Assets.modified+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="modified(db : AssetDB, query_id : String, ext : String, subtype : String, root : String)"></endpoint>
<signature id="Assets.modified+5">Assets.modified(**db**: `AssetDB`, **query_id**: `String`, **ext**: `String`, **subtype**: `String`, **root**: `String`)
<a class="headerlink" href="#Assets.modified+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="modified(db : AssetDB, query_id : String, ext : String)"></endpoint>
<signature id="Assets.modified+3">Assets.modified(**db**: `AssetDB`, **query_id**: `String`, **ext**: `String`)
<a class="headerlink" href="#Assets.modified+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="unmodified(db : AssetDB, query_id : String, asset_id : String)"></endpoint>
<signature id="Assets.unmodified+3">Assets.unmodified(**db**: `AssetDB`, **query_id**: `String`, **asset_id**: `String`)
<a class="headerlink" href="#Assets.unmodified+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="modify(db : AssetDB, query_id : String, asset_id : String)"></endpoint>
<signature id="Assets.modify+3">Assets.modify(**db**: `AssetDB`, **query_id**: `String`, **asset_id**: `String`)
<a class="headerlink" href="#Assets.modify+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="is_modified(db : AssetDB, query_id : String, asset_id : String)"></endpoint>
<signature id="Assets.is_modified+3">Assets.is_modified(**db**: `AssetDB`, **query_id**: `String`, **asset_id**: `String`)
<a class="headerlink" href="#Assets.is_modified+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="get_data(type_id : String, id : String)"></endpoint>
<signature id="Assets.get_data+2">Assets.get_data(**type_id**: `String`, **id**: `String`)
<a class="headerlink" href="#Assets.get_data+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="get_block(type_id : String)"></endpoint>
<signature id="Assets.get_block">Assets.get_block(**type_id**: `String`)
<a class="headerlink" href="#Assets.get_block" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Block`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="get_handle(type_id : String, id : String)"></endpoint>
<signature id="Assets.get_handle+2">Assets.get_handle(**type_id**: `String`, **id**: `String`)
<a class="headerlink" href="#Assets.get_handle+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="set_handle(type_id : String, id : String, handle : Num)"></endpoint>
<signature id="Assets.set_handle+3">Assets.set_handle(**type_id**: `String`, **id**: `String`, **handle**: `Num`)
<a class="headerlink" href="#Assets.set_handle+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="get_dev_version_path(db : AssetDB, asset_id : String)"></endpoint>
<signature id="Assets.get_dev_version_path+2">Assets.get_dev_version_path(**db**: `AssetDB`, **asset_id**: `String`)
<a class="headerlink" href="#Assets.get_dev_version_path+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="get_dev_version_data(db : AssetDB, asset_id : String)"></endpoint>
<signature id="Assets.get_dev_version_data+2">Assets.get_dev_version_data(**db**: `AssetDB`, **asset_id**: `String`)
<a class="headerlink" href="#Assets.get_dev_version_data+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Map`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="save_dev_version_data(db : AssetDB, asset_id : String, version_data : Map)"></endpoint>
<signature id="Assets.save_dev_version_data+3">Assets.save_dev_version_data(**db**: `AssetDB`, **asset_id**: `String`, **version_data**: `Map`)
<a class="headerlink" href="#Assets.save_dev_version_data+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

<endpoint module="luxe: assets" class="Assets" signature="image(id : String)"></endpoint>
<signature id="Assets.image">Assets.image(**id**: `String`)
<a class="headerlink" href="#Assets.image" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Image`
> Return a loaded image by id.
> 
>   ```js
>   var image = Assets.image("image/player")
>   Log.print("width: %(Image.get_width(image))")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="bytes(id : String)"></endpoint>
<signature id="Assets.bytes">Assets.bytes(**id**: `String`)
<a class="headerlink" href="#Assets.bytes" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Returns the data stored as bytes. 
> A Wren `String` is also a byte sequence, used via `string.bytes`.
> 
> **Note** That unlike other assets, bytes are stored by name _with_ extension.
> For example if you put a file called `data/hello.txt` in your project,
> you would access it via `var data = Assets.bytes("data/hello.txt")`.
> 
> This is because the extension might be meaningful to the user of the bytes,
> for example loading an image based on png vs jpg extension would be impossible
> if we don't know the extension of the data. Because bytes are "opaque", as in, 
> we don't care what they store, we just store them for you to access, we keep the extension.
> 
>   ```js
>   var text = Assets.bytes("data/hello.txt")
>   Log.print(text) //prints the contents of the file (the contents at compile time).
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="material(id : String)"></endpoint>
<signature id="Assets.material">Assets.material(**id**: `String`)
<a class="headerlink" href="#Assets.material" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Material`
> Returns a loaded material by id.
> 
>   ```js
>   var material = Assets.material("material/player")
>   Sprite.set_material(player, material)
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="atlas(id : String)"></endpoint>
<signature id="Assets.atlas">Assets.atlas(**id**: `String`)
<a class="headerlink" href="#Assets.atlas" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Atlas`
> Returns a loaded atlas by id.
> 
>   ```js
>   var atlas = Assets.atlas("atlas/example")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="lx(id : String)"></endpoint>
<signature id="Assets.lx">Assets.lx(**id**: `String`)
<a class="headerlink" href="#Assets.lx" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Any`
> Returns the LX parsed representation of a `bytes` asset.
> This is convenience for `Assets.bytes` followed by `LX.parse`.
> Returns null if the asset isn't found, or if parsing failed.
> 
> See `Assets.bytes`, as bytes require an extension.
> 
>   ```js
>   //assuming our data contains { speaker="sara" message="follow me." }
>   var dialog = Assets.lx("dialog/hello.lx")
>   var speaker = dialog["speaker"]
>   var message = dialog["message"]
>   Log.print("%(speaker): %(message)")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_shader_library(id : String)"></endpoint>
<signature id="Assets.has_shader_library">Assets.has_shader_library(**id**: `String`)
<a class="headerlink" href="#Assets.has_shader_library" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if a shader library with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_shader_library("assets/shaders")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_image(id : String)"></endpoint>
<signature id="Assets.has_image">Assets.has_image(**id**: `String`)
<a class="headerlink" href="#Assets.has_image" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if an image with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_image("image/player")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_material_basis(id : String)"></endpoint>
<signature id="Assets.has_material_basis">Assets.has_material_basis(**id**: `String`)
<a class="headerlink" href="#Assets.has_material_basis" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if a material basis with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_material_basis("basis/example")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_material(id : String)"></endpoint>
<signature id="Assets.has_material">Assets.has_material(**id**: `String`)
<a class="headerlink" href="#Assets.has_material" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if a material with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_material("material/player")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_bytes(id : String)"></endpoint>
<signature id="Assets.has_bytes">Assets.has_bytes(**id**: `String`)
<a class="headerlink" href="#Assets.has_bytes" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if a bytes asset with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_bytes("data/hello.txt")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_settings(id : String)"></endpoint>
<signature id="Assets.has_settings">Assets.has_settings(**id**: `String`)
<a class="headerlink" href="#Assets.has_settings" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if a settings asset with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_settings("settings/area1")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_atlas(id : String)"></endpoint>
<signature id="Assets.has_atlas">Assets.has_atlas(**id**: `String`)
<a class="headerlink" href="#Assets.has_atlas" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if an atlas asset with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_atlas("atlas/example")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_physics(id : String)"></endpoint>
<signature id="Assets.has_physics">Assets.has_physics(**id**: `String`)
<a class="headerlink" href="#Assets.has_physics" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if a physics asset with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_physics("physics/ice")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_prototype(id : String)"></endpoint>
<signature id="Assets.has_prototype">Assets.has_prototype(**id**: `String`)
<a class="headerlink" href="#Assets.has_prototype" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if a prototype with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_prototype("proto/tree")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_scene(id : String)"></endpoint>
<signature id="Assets.has_scene">Assets.has_scene(**id**: `String`)
<a class="headerlink" href="#Assets.has_scene" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if a scene with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_scene("scene/area1")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_input(id : String)"></endpoint>
<signature id="Assets.has_input">Assets.has_input(**id**: `String`)
<a class="headerlink" href="#Assets.has_input" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if an input asset with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_input("input/player")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_anim(id : String)"></endpoint>
<signature id="Assets.has_anim">Assets.has_anim(**id**: `String`)
<a class="headerlink" href="#Assets.has_anim" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if an animation with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_anim("anim/jump")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_mesh(id : String)"></endpoint>
<signature id="Assets.has_mesh">Assets.has_mesh(**id**: `String`)
<a class="headerlink" href="#Assets.has_mesh" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if a mesh with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_mesh("mesh/cube")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_tiles(id : String)"></endpoint>
<signature id="Assets.has_tiles">Assets.has_tiles(**id**: `String`)
<a class="headerlink" href="#Assets.has_tiles" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if a tilemap with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_tiles("tiles/caves")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="has_ui(id : String)"></endpoint>
<signature id="Assets.has_ui">Assets.has_ui(**id**: `String`)
<a class="headerlink" href="#Assets.has_ui" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if a ui asset with this id is loaded, or false otherwise.
> 
>   ```js
>   var exists = Assets.has_ui("ui/menu")
>   ```   

<endpoint module="luxe: assets" class="Assets" signature="unload_input(id : String)"></endpoint>
<signature id="Assets.unload_input">Assets.unload_input(**id**: `String`)
<a class="headerlink" href="#Assets.unload_input" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Unload the input asset, which undefines any nodes or events   

<endpoint module="luxe: assets" class="Assets" signature="load_input(id : String)"></endpoint>
<signature id="Assets.load_input">Assets.load_input(**id**: `String`)
<a class="headerlink" href="#Assets.load_input" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Load an input asset, which defines any nodes or events within it   

### Strings
`:::js import "luxe: assets" for Strings`
> When dealing with data like assets, storing a string directly can take up a lot of space.
> Instead, what we can do is store the strings once, in a shared place, and then reference that string later.
> 
> At runtime, strings can also be more expensive than is ideal (like needing to iterate the characters individually, or taking up more memory).
> 
> In both cases, what we store instead of a string is a _string id_, which is just a number.
> 
> Comparing two numbers, looking up numbers in an array or map and so on, it's _much_ faster with a number than using
> the string itself. Operating on numbers is both faster and simpler, and has a fixed size in memory.
> This is commonly called "string interning".
> 
> In luxe, the `Strings` class is how you interact with the strings available to your game.
> For example, `var name_id = Entity.get_name(entity)` will return a _string id_, not a string.
> To get the string, you can use `var name = Strings.get(name_id)`.
> Note that if the name is unknown to `Strings`, it will return null, so handle that appropriately.
> 
> To add a string, use `Strings.add("string")`.
> 
> For debugging strings, if you look inside `.luxe/luxe.strings.lx`, 
> this lists all the strings your assets reference, and what their key is.
> 
>   ```js
>   //Assuming this string hasn't been added before:
>   Log.print( Strings.get("hello") ) //prints null
>   var key = Strings.add("hello") //key is 1335831723
>   Log.print( Strings.get("hello") ) //prints 'hello'
>   ```

- [add](#Strings.add)(**value**: `String`)
- [get](#Strings.get)(**key**: `Num`)

<hr/>
<endpoint module="luxe: assets" class="Strings" signature="add(value : String)"></endpoint>
<signature id="Strings.add">Strings.add(**value**: `String`)
<a class="headerlink" href="#Strings.add" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Adds a string to the `Strings` service and returns the key.
> 
>   ```js
>   Log.print(Strings.add("hello")) //prints 1335831723
>   ```   

<endpoint module="luxe: assets" class="Strings" signature="get(key : Num)"></endpoint>
<signature id="Strings.get">Strings.get(**key**: `Num`)
<a class="headerlink" href="#Strings.get" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Return the value associated with the given key.
> This will return null if the string is not found.
> 
>   ```js
>   var name_id = Entity.get_name(entity)
>   var name = Strings.get(name_id)
>   if(name) {
>     Log.print("entity name is %(name)")
>   } else {
>     Log.print("entity name is not known (or it has no name)")
>   }
>   ```   

