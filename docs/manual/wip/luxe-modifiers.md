# luxe modifiers

As we found out in the [guide](../../../guide), luxe often works based on modifiers attached to an entity to give it the ability to do things.
Below, we'll do a real brief tour of the base modifiers luxe provides, before looking at how to make our own systems.

## Transform

Position, rotation and scale for an entity. 
When present, any other modifiers that deal with transform typically reference this one.
For example, to move/teleport a physics Body2D, you'd set the transform normally. 
To move an entity with `Text` attached around, set the transform position.

## Anim 

The animation modifier is an animation player that can play several animations at once. 
The animations themselves can affect any entity, not just the one the animation player is attached to.

[Basic Animation Tutorial](../wip/animate-a-sprite.md)

## Body2D

A 2D physics body. The API offers forces, impulses etc as you'd expect from a physics engine. 
Uses the more full featured physics engine internally, rather than simpler arcade style physics you might find in a module.

## Camera

A 2D or 3D camera for rendering with. Also provides important tools for 
converting between coordinate spaces, like taking a world space point and finding the screen space 2D value for it.
To move a camera, give it a Transform if it doesn't have one, and use `Transform.set_pos` as normal.

## Clock 

A simple clock to measure in-world time with, that can have a rate different to the world clock rate. 
When the world time is paused or slowed down, the clock is affected by it.
This is useful for game items that want to track their own time.

## Mesh

A mesh modifier displays geometry from mesh assets (3D or 2D), and provides mesh levels (for e.g LOD). 
Can be used for simple 2D geometry from external apps, 3D sprites or complex 3D games.

## Sprite 

A simple 2D image. Provides tools like color tint, flipping, tiling or sub UV display, skew, size and so on.

## Tags

Gives an entity the ability to have one or more tags associated with. Tags are a powerful way to interact with and filter the world.

## Text

Displays text attached to an entity. 

## Tiles

Displays a `tiles` asset attached to an entity. This is what you'd use to bring a tilemap into the world.

## UI

A UI canvas attached to an entity. A canvas is a self contained UI with optional auto layout, where
controls are created inside the canvas, and it has it's own coordinate space. 

[UI Tutorials](../../ui/intro)

## Values

A simple key/value storage attached to an entity. 
In a lot of cases when you just need a few simple values, it can be much simpler to use this
than to make your own modifier each time. 
Some examples: can store age of a building, what dialog to play on a trigger, what area to load on a door etc.

---

Now that we've learned about what exists, let's look at making our own.
