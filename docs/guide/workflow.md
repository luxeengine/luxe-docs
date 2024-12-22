#![](../images/luxe-dark.svg){width="96em"}

## luxe workflow

This guide will briefly cover the workflow involved in a typical luxe project, 
like where to put things and how a project functions.

## Scripting

When making a game in luxe, you'll typically be writing your game in a programming language called Wren.
Wren is very easy to learn, and is familiar if you're used to C#, lua or js.

#### This [Wren primer](wren-primer.md) is a quick introduction if you're familiar with other languages.

<h4>You can <a target="_blank" href="http://wren.io">Read the Wren documentation</a> for more details.</h4>

!!! note ""
    We'll have our own version of the Wren docs soon as luxe has customized Wren

### code completion

luxe supports code completion and other IDE features through Visual Studio Code ([instructions here](../get.md#installing-ide-support)).

!!! tip ""
    The implementation is a work in progress. Some APIs don't complete (`Input` + `IO`).
    Not all classes have documentation yet. As time goes on more and more stuff will have docs
    and type annotations.

The completion works when the **luxe agent** module is installed and running. 
**The agent is automatically installed and Visual Studio Code automatically runs the agent**.
Below you can see it in action (exact specifics might have changed over time, it is frequently improving).

<video preload="auto" autoplay controls="" loop="loop" style="max-width:100%; width:auto; margin:auto; display:block;">  
  <source src="../../images/guide/completion.mp4" type="video/mp4"></source>
</video>

---

## Game lifecycle

When you run your project, there are a few quick steps that prepare the game to run, and then control is handed over to you. Before the game runs, any outdated assets are _compiled_ and then when the game starts, the project settings are applied, then it's your turn.

### `game.wren`
Control is handed over to you inside your `game.wren` file. This is your **entry script**, and inside it you will typically have a `ready`, `tick`  function. 

Your `ready` function is where you start making your game. From here you can load some levels, create some entities, and populate a world. 

When that's done, your `tick` function is called once every frame as the game runs. Inside this function things can be updated (for example, things are moved around, or the HUD is updated). 

**outline data**   
Since it is likely you created a project from an outline, 
your game code is often adjusted to include helper methods and to set up the project for you.
For example the empty template creates a world, which is accessible via the `world` getter e.g 
```wren
var player = Entity.create(world)
```

## Asset workflow

### an asset is...

In luxe an asset refers to content files in your project folder. 

There are many different types of assets in luxe that you use to create your game, like animations, materials, fonts, meshes and more.

### source assets
Your project will likely have a number of _source assets_ like images, fonts and audio files, **these can all go in your project folder**. 

Source assets are _referenced_ by luxe _assets_, in order to tell luxe what you want from them, and are only used when your project data is compiled. 

### luxe assets
Then there are the assets themselves, which can refer to source assets and other luxe asset files. These often have settings and information about the source asset, but most of them will actually be the content for your game.

**luxe assets are named `example.type.lx`**. For instance, an image would be `image/player.image.lx`. Both the type and the lx extension are needed.

If you were making a level for example, you would have an asset to describe it. You would also probably have assets describing all the types of pre-composed entities for your game with all their modifiers set up, all the materials describing how things should be drawn, what input mappings you have, animation curves and more.

While these files are easy to create, read and edit by hand, most of these will be created and edited using the editor tools instead.

!!! note "" 
    In luxe, you can do basically everything via assets. You can also do the same via code - which means assets complement a code based workflow, they don't often replace it.

### data compiling

Now that we have all our source assets, and all the assets describing them and describing our game content, it gets converted into a format luxe can efficiently use when the game runs. This makes it possible to load everything quickly when the game is running.

The compilation step is quick and keeps track of things that have changed, so that iterating on your game is fast and easy.

!!! note "" 
    There is a new asset system since 2023.11.0 that co-exists with the old asset system.
    Note that there's a transition period where both are active but soon only the new one will be.
    This can add a little extra time on the compiling step but usually not noticeably slower.

### asset parcels

The final piece of the asset puzzle is how assets actually get loaded in luxe.

With luxe, you typically don't load assets one at a time. Instead they are grouped together into what we call a **parcel**. A parcel is an asset that lists a bunch of other assets that are related, and should be loaded together.

When a parcel is loaded all of it's assets become available to the game. When the parcel is unloaded, they are cleaned up and removed (unless multiple parcels list the same asset, in which case it stays until it's not needed).

Using parcels gives you a lot of control but with a very simple workflow, and serves many important purposes in luxe. Some examples of using parcels include a level specific parcel, an area specific parcel (like streaming in and out sections of a world), and they're useful for modding and add-on/DLC content.

!!! quote ""
    A parcels is usually compiled into a single data file, making it easier to distribute your game content with the game.

### The entry parcel
The default behaviour in luxe is that **the entry parcel is automatic**. You don't have to do anything for it to work, it will load all of the assets inside of your project folder for you. This allows you to focus on making your game without worrying about it.

**For most small to medium games all of your content can be loaded this even when shipped**.
For larger projects, you'll probably end up with several parcels, but this is in progress, see below.

!!! summary "Manually controlled parcels"
    At the moment, you can't load parcels manually.

    For bigger games, the entry parcel is typically where you'd store a splash screen and any essentials before the game loads the rest itself. Your project has a `parcel` setting, which is specifically for when the game starts up. This parcel is loaded first, before you get control, and means that any assets in this parcel are ready when your game starts. 

    From there, the game can load other parcels and assets as it needs.

### Ignoring assets
Your project config folder can have a file named `ignore` in it, so that you can ignore folders and files inside your project. This will also control what ends up in the automatic entry parcel. Put one path per line inside the luxe ignore file. An example is given below where no markdown files and `some_folder/` won't end up in loaded in game.

```
*.md
some_folder/
```

---

## project workflow 

### project outlines

Most projects are created from an outline, which is responsible for making it easier to get started making a game. As there are many types of projects that you can make with luxe, each of these have specific needs and defaults. As an example, a 3D project and a 2D only project may have very different defaults.

With luxe this happens in the project outline, which is set up based on the type of project. The outline configures the basic skeleton, making your project ready to use. For example, in a pixel art outline, the worlds, cameras and settings would be configured for what pixel art needs.

You can freely modify your outline as it belongs to your project.

!!! warning 
    Changing the template may require manually updating it,   
    if the base template changes and you want those changes in your project.

### The `empty` outline

This outline is for a basic 2D game and is a good starting point to tinker with luxe!

**worlds**   
It creates two worlds for you, one called `world` and `ui`.   
You can put UI entities in the `ui` world, and game entities in the `game` world.   
The worlds are automatically updated and drawn when the game updates.

**cameras**   
The UI is drawn after the game, and each world also has it's own camera, so moving the game camera won't affect the UI. A camera is an entity with a `Transform` and a `Camera` attached. To control the game camera use `camera` and for the UI camera use `ui_camera`. e.g `Transform.set_pos(camera, 10, 10)`

Both cameras are set up as the size of the window, which makes 1 _window pixel_ = 1 world unit. This handles high DPI screens automatically, keeping your world units the same. It does however mean that changing the window size changes how much of your world you can see, which you may want to configure yourself. <small>_todo: link to guide on how_</small>

For convenience you can get the window size from `width` and `height` and if needed the device pixel ratio as `scale`. You can also access the mouse position in world space using `mouse`, e.g `mouse.x` or `mouse.y`.

### The `tutorial` outline

Immediate term this template matches the old workflows and is being updated. It has some useful info but a lot of stuff has changed since and it is being updated. 

### The `pixel art` outline

This outline includes automatic pixel art scaling and a fixed world size, and handles converting the mouse coordinates for you via `mouse.x`/`mouse.y`.  It includes a UI world and game world as well.

---