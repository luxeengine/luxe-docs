![](../../images/luxe-dark.svg){width="96em"}

# luxe modifiers

As we found out in the [guide](../../guide.md), luxe often works based on modifiers attached to an entity to give it the ability to do things.
Below, we'll do a real brief tour of the base modifiers luxe provides, before looking at how to make our own systems.

## Anim 

The animation modifier is an animation player that can play several animations at once. 
The animations themselves can affect any entity, not just the one the animation player is attached to.

## Camera

A 2D or 3D camera for rendering with. Also provides important tools for 
converting between coordinate spaces, like taking a world space point and finding the screen space 2D value for it.
To move a camera, give it a Transform if it doesn't have one, and use `Transform.set_pos` as normal.

## Mesh

A mesh modifier displays geometry from mesh assets (3D or 2D), and provides mesh levels (for e.g LOD). 
Can be used for simple 2D geometry from external apps, 3D sprites or complex 3D games.

## Skeleton

Typically for animation or IK. Can be driven by Anim or manually.

## Skin

A skin for a mesh, which binds the mesh to a Skeleton modifier.

## Sprite 

A simple 2D image. Provides tools like color tint, flipping, tiling or sub UV display, skew, size and so on.

## Tags

Gives an entity the ability to have one or more tags associated with. Tags are a powerful way to interact with and filter the world.

## Text

Displays text attached to an entity. 

## Transform

Position, rotation and scale for an entity. 
When present, any other modifiers that deal with transform typically reference this one.
To move an entity with `Text` attached around, set the transform position.

## Tiles

Displays a `tiles` asset attached to an entity. This is what you'd use to bring a [tilemap](../tilemaps.md) into the world.

---

Now that we've learned about what exists, let's look at making our own.
