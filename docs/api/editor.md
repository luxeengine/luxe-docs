#![](../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2021.0.8`)  


---

## `luxe: editor` module

- [Editor](#editor)   

---

### Editor
`:::js import "luxe: editor" for Editor`
> Access to information about the editor, _if the game is currently running in the editor_.
> Please note this API is new and heavily work in progress.

- [get](#Editor.get)(**context_id**: `Any`)

<hr/>
<endpoint module="luxe: editor" class="Editor" signature="get(context_id : Any)"></endpoint>
<signature id="Editor.get">Editor.get(**context_id**: `Any`)
<a class="headerlink" href="#Editor.get" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Returns the editor context with the given ID.
> Examples include `luxe.editor.world` for the world editor, or `luxe.editor.tiles`.
> 
>   ```js
>   //We can check if a world is in edit mode via the `edit` tag.
>   //For example, a scene being previewed in editor is still running in 
>   //the editor, but we don't want to act as if it's being edited.
>   var is_world_editable = World.tag_has(world, "edit")
>   if(!is_world_editable) return
> 
>   //if we're in the editor, we can access the world editor and do some things
>   var world_editor = Editor.get("luxe.editor.world")
>   if(world_editor) {
>     //simple example, make sure the gizmo matches the transform
>     //if there's no gizmo, the function returns null
>     var gizmo = world_editor.gizmo
>     if(gizmo) gizmo.refresh()
>   }
>   ```   

