# luxe editor release notes

#### 2021.0.8

- Open Prototype will switch to already open prototypes
- Fix anim crashes when creating anims in a prototype world
- Fix wacky enter/exit outline expansion behaviour
  - World; hold shift while hovered in outline to expand
- Fix crashes from changing values on spawned prototypes
- Fix crash when cancelling several actions in omni
- Fix ui focus not working when omni is closed
- Fix "add track" repeatedly adding options to omni
- Fix crash on clicking cancel on the asset import view
- World; camera; some fixes to capture behaviour

#### 2021.0.7

- Fix regression from imports added in 2021.0.6, paths should work as intended
- Fix duplicate options added when clicking import repeatedly #52
- Fix anim view stealing focus when switching contexts #48
- Fix path lowercase behaviour in more places e.g #53
- UI; double click setting added `engine.runtime.input.rapid_press_interval`
- UI; double click time default increased to 0.45s (was 0.2s)
- Anim; Sprite Value Track now exposes uv.horizontal/uv.vertical
- Anim; Sprite Value Track now exposes uv.left/uv.right/uv.top/uv.bottom
- Material previews for sprite based materials render as 2D images

#### 2021.0.6

- remove Str.lower on paths removing cross platform behaviour
- remove create asset options from asset lists (use import menu)
- fix tab behaviours for several things

#### 2021.0.5

- Values / Tags - fix enter key being stolen 
- Anim - fix loading creating duplicate tracks
- Anim - add transform track settings to editor
- Anim - add sprite value track settings
- World - fix assumptions of project-local paths in world editor, so scenes in modules can be edited

#### 2021.0.4

- luxe 2021.0.4 compatability
- rename default scene folder to `scene/` instead of `scenes/` for consistency
- bunches of work on the animation editor
- fix escape key taking action when text fields are focused
- fix omni key taking action when text fields are focused
- custom modifiers - show validation errors properly on vec fields
- scene outline - fix renaming scenes to be consistent with layers
- scene outline - add several tooltips to things

#### 2021.0.3

- luxe 2021.0.3 compatability
- Editor - Fix several places where Str.fixed is used to display nicer numbers
- Editor - Fix notifications blocking input to the top bar
- Editor - Added toggle grid via `ctrl-G`/`cmd-G`
- Editor - Show a message in asset lists when there are no assets of that type
- Editor - Add tooltip to asset lists so you can see long names
- Editor - Fixed material/image previews from sometimes not showing up
- World - Text - update material properly when changing it
- World - Text - fix crash when text is saved without a default, or by duplicate
- World - Transform - link disallows + shows "can't link to self" and "no transform attached"
- World - Anim - anim view is now per world
- World - Anim - Fix mouse issues with animation views
- World - Anim - used shared doc context with world, now undoable/redoable
- World - Anim - allowing editing properties without stealing focus
- World - fix a crash when an error happens and invalid code was called
- World - gizmo now remembers world/local toggle
- World - transform gizmo (T) now shows a snap toggle for translation on space as well
- World - guard accessing invalid entities in highlights + outline, to prevent crashes
- World - fix crash from deleting a prototype where it deselected after destroy
- World - fix spawn prototype button being sneaky and sometimes not showing up
- World - fix open/create scene options showing in prototype worlds
- World - prototype or preview worlds now respect the default 2d/3d setting
- Tiles - when refreshing, don't access invalid entities to prevent crashes
- Tiles - fix painting brushes without overlap while dragging
- Tiles - show image/atlas source add panels separately for clarity
- Tiles - add tooltips to visual source add panels
- Tiles - display notifications for key events

#### 2021.0.2

- luxe 2021.0.2 compatability
- fix some issues with luxe dev mode
- fix deploy only deploying host target
- world - anim preview exploration
- world - anim fix doc updates on track properties changing
- world - anim fix track open not updating settings
- world - fix mouse staying connected on world destroy
- fix crash when asset reloading fails to compile

#### 2021.0.1

- luxe 2021.0.1 compatability
- UI - fix lists with filters, fixes annoying mouse snapping bug on click
- Animation editor continued work (sprites, etc)
- Remove old anim context, rename materials to reduce confusion
- block in assets context

#### 2021.0.0

- luxe 2021.0.0 compatability
- Project - add hot reload for meshes, images and shaders (only)
- Project - clean up landing page + recent projects and such
- UI - add notifier for important actions
- UI - add "open folder" when a project is open
- UI - added tooltips to a lot of things to test the tooltip stuff
- UI - visual polish for several things
- Noodles - fix for y+ up
- World - allow closing a prototype world
- World - add `editor="options"` so enums act like selectable lists in editor
- World - fix selection of prototype entities via the icon
- World - highlight all children of a prototype when selected
- World - wip - scene outline expands on mouse enter. if you see weirdness, move the mouse out of omni
- World - add link to `Transform` for connecting entities in editor
- World - add initial sort option for scene outline, default to alphabetical
- World - change how active layer works. clicking a layer now activates it. use edit to rename
- World - fix bug when saving would save invisible internal scenes into the project
- World - selecting a child of a prototype selects the root, hold alt to select child
- World - clicking multiple times to select things behind the first one
- World - Anim - clean up on closing a project
- World - Anim - lots of UI work and fixes toward a usable editor. It can load/save basics.

#### 2020.3.5

- luxe 2020.3.5 compatability
- world - gizmo adapts to the scale of the world (tilman)
- world - fix selection rendering in custom rendering
- world - fix axes and grid rendering in custom rendering
- world - gizmos persist snap settings when editing
- world - gizmo snap settings select all on focus

#### 2020.3.4

- luxe 2020.3.4 compatability
- load project strings up front
- fix loading prototypes (tilman) 
- fix preview in world editor using old data (tilman) 
- fix obscure case in scene outline displaying prototype entities loose
- when selecting part of a prototype in view, select the root instead (tilman)
- show errors when duplicating/deleting parts of a prototype
- redo duplicating, now anything i.e prototype instances can be duplicated
- initial support for deleting prototype roots (not undoable, but saveable)

#### 2020.3.3

- luxe 2020.3.3 compatability
- Fix some crashes in tiles and filtered lists
- Update create material tool to latest material format 
- Add tag to preview world so it can be identified (tilman)
- Swap Q/E controls on camera as they were inverted (tilman)

#### 2020.3.2

- luxe 2020.3.2 compatability
- Fix crash when closing a project and some other places
- World - prevent naming two entities the same thing to avoid bugs atm (eva)

#### 2020.3.1

- luxe 2020.3.1 compatability
- fix a crash when closing a scene sometimes
- set default world and camera for reaching
- use project compiler for project assets (not editor compiler)

#### 2020.3.0

- luxe 2020.3.0 compatability
- editor - load input entry setting so game input bindings exist
- editor - choosing file paths on windows was broken, all fixed now
- editor - make keymap UI slightly taller for legibility
- world - fix bug in scene preview where old scenes could linger (fixed by tilman)
- world - don't allow selecting prototype entities for entity reference atm
- world - add shift-B to display bounds of world contents
- world - fix crash with new modifier block format (ronja)
- tiles - add 45 degree snap when rotating (hold shift) (eduardo)
- tiles - add material input name to sources
- tiles - store a pixelated flag for sources
- tiles - can now set color on tiles via the editor
- tiles - fix gaps when painting fast (eduardo)


#### 2020.2.0

- luxe 2020.2.0 compatability

## 2020.1.2

- doc - context concept for plural doc editing + undo
- world - add `luxe.editor.world.camera.default` setting, "2D"/"3D"
- world - fix prototype scenes showing up in preview mode (tilman)
- world - hide ui for scenes inside prototype worlds
- world - more wip animation editing, not usable yet (though saving works)
- project - handle errors when loading projects gracefully, not aborts
- project - fix a few crashes when closing/opening projects in a row

## 2020.1.1

- latest luxe path support
- fix intro tooltip location
- fix text wrapping in various places
- more work on new animation views (not done)

## 2020.1.0

#### editor

- new versioning
- fix projects that use dev versions by version number
- make sure project settings are loaded for use
- make sure project dependencies are loaded as well
- lx parsing now labels all sources for better errors
- fix doc handling keys with dots inside. entities etc can be named whatever
- doc now has transient docs for handling behind the scenes change
- editor handles cancel (esc), commit (enter), and tab for custom modifiers
- recent projects shown by order of access, shared with launcher
- now handles project path from command line
- expose access to editor contexts for modifiers
- fix direction of zoom with mouse wheel in 3d spaces

#### world

- fix renaming layers being broken in some cases
- don't allow unselectable things to be selected from scene view
- active worlds concept for prototype + animation editing
- prototypes now openable, editable, creatable
- prototypes overrides can now be edited
- prototypes can now accept modifiers on their root entity
- fix active layer in various cases, like load/close/new/etc
- handle many errors more gracefully as messages, not aborts
- game rendering is now handled, so in editor looks like the game
- fix duplicating entities handling dependency ordering right
- fix custom modifiers vector fields using last selected values
- Shift P shows physics debug (if available)
- fix crash on entities without an ID
- gizmos now can snap (press space bar with gizmo active)

#### tiles

- flip keys will now flip selected tiles (if select tool is on)
- drawing ui in world space for consistency
- fix rotation in some cases
- fix clearing tags
- tags + offset are now painted correctly
- displays dimensions of select rect, useful for measuring
- highlight + select all with visuals (ctrl click, alt click)

## 0.0.31

#### editor

- fix same source/dest image import zeroing file (jonathan)
- fix context switcher ui location on resize
- fix loading projects with dependencies, again
- when deploying, the folder now opens on complete
- anim - don't show buttons with no project (that crash on click)

#### tiles

- fix crash sometimes on `viaul`
- try different logic for half texels
- fixed crash on removing tiles modifier

#### world

- modifiers now add their dependencies first if missing
- modifiers now get notified when in editor for events
- attach list for modifiers cleaned up and sorted nicely
- fix missing strings on modifier asset select
- log attach errors to log as well in case of crashes
- fix ui world camera on window resize 

## 0.0.30

#### omni

- fix fast switch not resetting on esc (tilman)
- fix context changes cancelling pages. fixes 'attach' (tilman)
- fixed scroll jumping to be more consistent again

#### editor

- cleaned up project intro flow
- omni now uses the luxe logo as intended (not a weird symbol)
- fixed material/image create outside `world` (jonathan)
- create material/images ensure path exists (jonathan)
- improved material/image create workflow (added file select)

#### project

- added deploy panel for making builds
- make it possible to load projects with dependencies!

#### world 

- fix state of collapsed scene view selected entities (tilman)
- fix missing strings on id32/id64 field types
- fixed ui for id32/id64 field types
- add entity select for custom modifiers
- tags - fixed crashes when adding sometimes

## 0.0.29

#### editor

- added keymaps to tiles, world
- added readme to tiles, world
- fixed omni snapping awkwardly in most cases
- fixed omni filtering being case sensitive
- bring back fast switcher UI immediate term
- context switcher closes when clicking outside of
- add 'create material...' in material select
- add 'create image...' in image select
- add hover previews for materials/images
- anim - removed crashing logic, can now play with it

#### world
- custom modifiers now display id32/id64 correctly
- clean up attach modifiers UI a bit

#### tiles

- added size operations to tiles
- properties panel can edit selected tiles
- "add visual source" now has an image source

## 0.0.28

- editor - fixed an issue with project upgrades

## 0.0.27

#### editor
- resizable window
- added several wip tooltips
- context switcher usability improved
- play button is now global (not world only)
- project - 'update bin' is now dev toggle
- modules - 'view update' link fixed on updates

#### tiles
- rectangle selection (cmd/ctrl drag with select tool)
- fixed rogue rendering with no project open

## 0.0.26

#### editor
- added log.txt so errors can be relayed
- more game level rendering integration
- omni now has placeholder text and cancel button (sg)
- omni has initial version of mini (tooltips), more in .27
- new project displays latest outlines better (Jonathan)

#### tiles
- fixed bugs in painting not applying (by Tilman)
- fixed stack view getting clipped text (by Tilman)
- brushes with rotation paste incorrectly (by Tilman)
- fixed file name issues on saving tiles (Tilman)
- visuals now use texel center, fixes bleeding (Tilman)

#### camera
- fixed zoom speed, adding setting (everyone)
- add space key to drag as alternate (01010111/Eduardo)
- mouse wheel changes speed in free fly mode

#### anim
- initial work in progress anim editor. not usable yet.

#### world
- fixed play in editor, works well now
- fix crash on renaming a layer (everyone)
- custom modifiers can be removed now (Noel)
- added animation modifier, to attach anims
- blank scenes default to scenes/ folder

## 0.0.25

- select drag while holding alt now works 
- tiles - add basic tagging support
- tiles - display tile stack better
- world - add duplicate (cmd/ctrl D)
- omni - don't take focus on context switching
- project - add modules button for consistency
- update sublime/vscode support with new errors

## 0.0.24

- fix settings.lx not loading correctly (Tilman/sponge)

## 0.0.23

- added settings.lx for tweaking window size
- added tiles reset rotation key (Eduardo)
- fixed world selection state on switching back (Tilman)
- fixed world uuid bugs causing delete to crash
- fixed world bug in not removing entities from list
- fixed horizontal scroll inverted (Tilman)
- fixed escape = quit, use cmd+Q/alt+F4/close window (La)
- fixed tiles context clean up on closing project (Tilman)
- fixed tiles bug on certain actions (cut/palette)
- fixed tiles aspect visual bug (fixed source previously)
- fixed windows install not creating the link (sponge/torcado)

## 0.0.22

- added tiles background color setting
- added tiles toggle grid key (`G`)

## 0.0.21

- fixed readme from project displaying everywhere (Jonathan)

## 0.0.20

- added **uninstall** module version button
- added **getting started** to view readme in project view
- added **sample browser** in modules/installed/module/version
- added **update project** prompt for convenience
- added resilience when attaching modifiers (Jonathan)
- fixed modifiers list mismatch on project change (Jonathan)
- fixed tiles sources with wider ratio display bug (Jonathan)

## 0.0.19

- fixed play standalone not working via assumptions

## 0.0.18

- fixed custom modifiers in world/runtime (dev.78)
- world - added play standalone (cmd/ctrl P or Play icon)
- world - added single click to rename (torcado)
- world - fixed enter key commits name (Brody)
- tiles - added tool display hints/icons
- tiles - display open asset name
- tiles - added save as...
- fixed input bindings in world feeling off (Jonathan)
- fixed cancel save crashing
- fixed saving invalid tiles from clear/paint (Brody)
- fixed crash placing tile after clearing map (torcado)
- various minor bugs and improvements!

## 0.0.17

- fixed tiles refresh on save also when loaded via scene (Jonathan)

## 0.0.16

- tiles automatically refresh in world on save (Jonathan)
- added header in subsection of attach for clarity (torcado)
- fixed crash: adding visual modifers when gizmo shown
- fixed camera input being linked in diff contexts (Jonathan)
- fixed T (transform gizmo) crash in world editor (torcado)
- display modules in sorted order for consistency (Jonathan)

## 0.0.15

- include windows build

## 0.0.14

- display readme clearer, and scrolling
- when not focused, make app use much less cpu/energy

## 0.0.13

- fixed tiles being available when no project is open
- fixed tiles grid setting being stored wrong (Jonathan)
- fixed newly created tiles breaking in world (Jonathan)

## 0.0.12

- added version display to status bar
- fixed `remove missing project` lingering (Jonathan)
- fixed `transform` crashing on selection (Jonathan)
- added better error messages on `transform` misuse (Jonathan)

## 0.0.11

- fixed entities not getting their uuid saved (Jonathan)
- fixed scrollwheel direction again (Jim/Jonathan)
- fixed ID panel floating around when it shouldn't
