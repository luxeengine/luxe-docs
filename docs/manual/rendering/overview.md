
# Rendering in luxe

!!! note ""
    Please note that rendering is a fairly wide and deep topic.

## Concepts

The [concepts](../concepts) page covers important concepts related to how things are rendered in luxe. 
This covers topics like targets and viewports, for deciding how and where things render.

## Tiers

In luxe, rendering occupies mutliple tiers of access/usage.   
On the user facing side, there is a high level and a low level.

Internally there are more layers, like mid level and lowest level (the backend, which abstracts away graphics APIs, making it portable).

#### High level

In a typical game, a lot of the time, you render *`Worlds`*, and not individual objects.
This includes _Modifier Systems_ that provide drawing, like `Sprite`, `Mesh` or `UI`, 
as well as _Service APIs_ like the `Draw` drawing API, which places its contents into the world.

The world will track which renderable items are in it, and when that world is rendered, the active ones will be submitted to be drawn.

#### Low level

Below that, you can access the `Render` API directly,
which offers access to `Geometry` and more, as well as a `Render.submit` call.

This allows manually controlling which geometry is submitted and when, as well as offers access to 
modifying geometry or images directly.

#### Differences

It's important to remember that the higher level tools will be doing work for you. 
If you bypass that work, you'll have to do more work yourself. 

---

More details on each:

- [High level](../high-level)
- [Low level](../low-level)