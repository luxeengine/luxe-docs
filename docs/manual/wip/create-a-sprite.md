
# Sprites

## What is a sprite?

A sprite is another name for an image, drawn to represent something in your game like the player or a tree.

## A sprite in luxe

In luxe, we read in the intro that things are represented in a world [as entities](/guide/), and they have modifiers attached to them to make them do things. A sprite is also done this way, we create an entity if we don't have one, and then attach a `Sprite` modifier. 

To use the sprite system, import them from the world module at the top of your code:
```js
import "luxe: world" for Entity, Sprite
```

## Creating a sprite

To create a sprite we first need an entity, we ask the `Entity` system to create one for us to use. The `Entity.create` function asks us for an optional name (an identifier, or `id`), and a world in which to create the sprite.

```js
Entity.create(world, id)
```

We'll call our entity `player`, and we'll use the `app.world` game world from our template.

```js
var player = Entity.create(app.world, "player")
```

We'll probably want our sprite to exist some _where_ in the world, so we'll want to create a `Transform` modifier as well. The `Transform` modifier handles all the things related to position, rotation and scale. 

```js
Transform.create(player)
```

Now we're ready to add a `Sprite`! Let's see what `Sprite.create` wants from us...

```js
Sprite.create(entity, material, width, height)
```

We can see that we need a `material` and a size, and to tell it which entity we want to attach the sprite to. 

## What is a material?

**A material tells luxe how a sprite is drawn.** For example, whether or not our sprite is pixelated, or which `image` will be drawn. Materials are a big topic, but creating one for our sprite is simple. 

```js
var material = Material.create("luxe: material_basis/sprite")
```

This creates a material _instance_ that uses a _basis_ to define how it draws. 

This basis - `luxe: material_basis/sprite` - is a default one that comes with luxe as a convenience. There is also `luxe: material_basis/sprite_pixelated` **if you are using pixel art**. 

## Specifying an image

We'll now need to specify an image for our material to use.

Let's place an image file in our project to use, we'll use `image/player.png` as an example. The image will be referred to in your material as `image/player` (assets are used without the file extension).

If you place a _source image asset_ in your project (like a png or jpg file), an _image asset_ will be automatically generated for you (if one doesn't exist for that image).

??? note "how it works"
    If you place a png in your project at **`image/player.png`**, the `image/player.image.lx` file is automatically generated. We can then refer to the image as `image/player` later.

    The `.image.lx` asset is a convenience, but make sure to understand that luxe refers to the `image` asset, not the source image. [read more](/guide/workflow/#source-assets)


Once we have an `image`, we just need to tell the material to use it.

```js
var image = Assets.image("image/player")
Material.set_input(material, "sprite.image", image)
```

!!! note ""
    Make sure you import `Assets` and `Material` at the top of your file.
    ```js
    import "luxe: assets" for Assets
    import "luxe: render" for Material
    ```

## The whole example

```js
  //we need an entity to represent our player
var player = Entity.create(app.world, "player")
  //let's create our material instance
var material = Material.create("luxe: material_basis/sprite")
  //ask the assets for our image
var image = Assets.image("image/player")
  //and tell the material to use it 
Material.set_input(material, "sprite.image", image)
  //now, we can attach a Sprite modifier
Sprite.create(player, material, 64, 64)
  //and we want to give our sprite a position
Transform.create(player)
```

## Moving your sprite

```js
  //move to an absolute position
Transform.set_pos(player, x, y)
  //rotate to a specific angle
Transform.rotate_2D(player, 45)
  //move to a relative position
Transform.translate(player, -1, -1)
  //flip the sprite horizontally
Sprite.set_flip_h(player, true)
```

## Conclusion

The sprite modifier offers several conveniences, like flipping or tinting the sprite, amongst other things. The [Sprite API documentation](/api/#sprite) has all the details.

--- 

# Extra details 

## Creating a material asset

A `material` asset is a simple file in our project. Let's create one called `material/player.material.lx` in our project. Materials will be discussed in detail later, but inside that file we want it to look something like this:

```js
material = {
  basis = "luxe: material_basis/sprite"
  inputs = { "sprite.image" = "image/player" }
}
```

That's it!    
We now have a material we can talk about as `material/player`.

## Using the material asset

Now that we have a material, we have to ask the `Assets` api to give us a handle for it. We'll pass that handle to the `Sprite.create` function.

```js
  //we need an entity to represent our player
var player = Entity.create(app.world, "player")
  //let's get our material
var material = Assets.material("material/player")
  //now we can attach a Sprite modifier
Sprite.create(player, material, 64, 64)
```

---