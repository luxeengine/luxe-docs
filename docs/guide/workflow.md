#![](../images/luxe-dark.svg){width="96em"}

# luxe workflow

This guide will briefly cover the workflow involved in a typical luxe project. For example, where to put things and how a project functions.

This will help you when you want to script something in your game.

## Scripting

When making a game in luxe, you'll be writing your game in a programming language called Wren.
Wren is very easy to learn, but is familiar if you're used to C#, lua or js.

<h4><a target="_blank" href="http://wren.io">Read the Wren documentation</a></h4>

This [Wren primer](../wren-primer) is a quick introduction if you're familiar with other languages.

### code completion

luxe supports code completion and other IDE features through vs code ([get vscode here](../../get#installing-ide-support)).

!!! tip ""
    The implementation is a work in progress. Some APIs don't complete (`Input` + `IO`).
    Not all classes have documentation yet. As time goes on more and more stuff will have docs
    and type annotations.

<video preload="auto" autoplay controls="" loop="loop" style="max-width:100%; width:auto; margin:auto; display:block;">  
  <source src="../../images/guide/completion.mp4" type="video/mp4"></source>
</video>

The completion works when the **luxe agent** is installed and running. 

**To install the agent**, open the luxe launcher:

  - on the **modules** page
  - find and install the **luxe-agent** module

!!! note ""
    The version of the luxe agent is less important. Just use the latest one.

**VS Code automatically runs the agent**, if it can, and as long as a version is installed.

!!! note ""    
    The agent is a regular applicaton, it's written in luxe itself.
    You can run it manually, make it run automatically on system start and so on.
    You can also run it via the launcher:
        - on the **tools + settings** page
        - wait a bit, and click **run agent**

Once running, you can test it by typing `Sprite.` in vscode in a project.

![](../images/guide/completion.png){: loading=lazy }

---

## game lifecycle

When you run your project, there are a few quick steps that prepare the game to run, and then control is handed over to you. Before the game runs, any outdated assets are _compiled_ and then when the game starts, the project settings are applied, then it's your turn.

### `game.wren`
Control is handed over to you inside your `game.wren` file. This is your **entry script**, and inside it you will have a `ready`, `tick` and `destroy` function. 

Your `ready` function is where you start making your game. From here you can load some levels, create some entities, and populate a world. 

When that's done, your `tick` function is called once every frame as the game runs. Inside this function things can be updated (for example, things are moved around, or the HUD is updated). 

And for `destroy`, this is called for you when the user quits (or the game is shutdown). In here, you can clean up anything you want to, and have an opportunity to perform any last minute tasks.

**outline and `app`**   
Since it is likely you created a project from an outline, you should see the `app` details in the `game.wren` file. This is initialized by your game code so that it can provide convenience for you.

## asset workflow

### an asset is...

In luxe an asset refers to content files in your project folder. 

There are many different types of assets in luxe that you use to create your game, like animations, materials, fonts, meshes and more.

### source assets
Your project will likely have a number of _source assets_ like images, fonts and audio files, **these can all go in your project folder**. 

Source assets are _referenced_ by luxe _assets_, in order to tell luxe what you want from them, and are only used when your project data is compiled. 

### luxe assets
Then there are the assets themselves, which can refer to source assets and other luxe asset files. These often have settings and information about the source asset, but most of them will actually be the content for your game.

**luxe assets are named `example.type.lx`**. For instance, an image would be `images/player.image.lx`. Both the type and the lx extension are needed.

If you were making a level for example, you would have an asset to describe it. You would also probably have assets describing all the types of pre-composed entities for your game with all their modifiers set up, all the materials describing how things should be drawn, what input mappings you have, animation curves and more.

While these files are easy to create, read and edit by hand, most of these will be created and edited using the editor tools instead.

!!! note "" 
    In luxe, you can do basically everything via assets. You can also do the same via code - which means assets compliment a code based workflow, they do not replace it.

### data compiling

Now that we have all our source assets, and all the assets describing them and describing our game content, it gets converted into a format luxe can efficiently use when the game runs. This makes it possible to load everything quickly when the game is running.

The compilation step is quick and keeps track of things that have changed, so that iterating on your game is fast and easy.

### asset parcels

The final piece of the asset puzzle is how assets actually get loaded in luxe.

With luxe, you typically don't load assets one at a time. Instead they are grouped together into what we call a **parcel**. A parcel is an asset that lists a bunch of other assets that are related, and should be loaded together.

When a parcel is loaded all of it's assets become available to the game. When the parcel is unloaded, they are cleaned up and removed (unless multiple parcels list the same asset, in which case it stays until it's not needed).

Using parcels gives you a lot of control but with a very simple workflow, and serves many important purposes in luxe. Some examples of using parcels include a level specific parcel, an area specific parcel (like streaming in and out sections of a world), they're useful for for modding and even for add-on/DLC.

!!! quote ""
    Parcels are compiled into a single data file, making it easier to distribute your game content with the game.

### The entry parcel
The default behaviour in luxe is that **the entry parcel is automatic**. You don't have to do anything for it to work, it will load all of the assets inside of your project folder for you. This allows you to focus on making your game without worrying about it.

**For most smaller games all of your content and assets can be loaded here without any trouble**.

!!! summary "Manually controlled parcels"
    At the moment, you can't load parcels manually.

    For bigger games, the entry parcel is typically where you'd store a splash screen and any essentials before the game loads the rest itself. Your project has a `parcel` setting, which is specifically for when the game starts up. This parcel is loaded first, before you get control, and means that any assets in this parcel are ready when your game starts. 

    From there, the game can load other parcels and assets as it needs.

### Ignoring assets
If your project has a file called `.luxeignore` in it, you can ignore folders and files inside your project for the automatic entry parcel. Just put one path per line inside the luxe ignore file, an example is given below. This will not allow any markdown files, or `some_folder` to be added to the automatic parcel or any other asset processing.

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

### The `empty/` outline

This outline is for a basic 2D game and is a good starting point!

**worlds**   
It creates two worlds for you, one called `app.ui` and `app.game`.   
You can put UI entities in the `UI` world, game entities in the `game` world.   
The worlds are automatically updated and drawn when `app.tick` is called.

**cameras**   
The UI is drawn after the game, and each world also has it's own camera, so moving the game camera won't affect the UI. A camera simply has a `Transform` and a `Camera` attached. To talk about the game camera use `app.camera` and for the UI camera use `app.ui_camera`.

Both cameras are set up as the size of the window, which makes 1 _window pixel_ = 1 world unit. This handles high DPI screens automatically, keeping your world units the same so don't worry about that. It does mean that changing the window size changes how much of your world you can see, which you may want to configure yourself. <small>_todo: link to guide on how_</small>

For convenience you can get the window size from `app.width` and `app.height` and if needed the device pixel ratio as `app.scale`.

!!! tip ":todo: dev specifics"

!!! warning
    This outline is currently a work in progress, so try to avoid changing it much unless you have to, for now.

---