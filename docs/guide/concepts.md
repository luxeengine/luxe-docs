#![](../images/luxe-dark.svg){width="96em"}

# concepts

luxe is created with a design philosophy, having a better understanding of some of the choices, concepts and ideas should help you use it better.

## Commit 

Several APIs in luxe use a concept called `commit`, where changes are made in bulk first,
and then committed. [2D drawing](../../tutorial/older/drawing-2d) for example, you queue up
drawing by calling the API, and then commit the changes when done. [UI](../../tutorial/ui/intro) is also an example.

This makes bulk changes cheaper, and is a good way to make things more efficient.

## API concepts

### API patterns

All APIs in luxe aim to be consistent, and many concepts have a pattern behind them.   

API functions operate on instances, and all API functions that are related live on the same class. For example the `World` API deals with all the functions that operate on a world, `Entity` has functions that operate on entities.

Creating anything in luxe uses a function starting with `create`.   
Cleaning up always uses a function starting with `destroy`.   

### API design

In luxe, the API is not object oriented.   
In object oriented APIs, you create an _instance_ of something,    
and then call functions _on that instance_. For example,

```js
var world = World.new()
    world.set_time(0)
    world.destroy()
```

In luxe however, the API is not object oriented for various reasons (like performance, aesthetics and preference). The same code above in the luxe API looks like this, where the API is used consistently to operate on an instance:

```js
var world = World.create()
    World.set_time(world, 0)
    World.destroy(world)
```

!!! note ""
    Sometimes these instances are called a handle, so the terms will be used interchangeably.

This makes it easier to find all call sites of any particular API, and instead of treating objects as instances which have a cost to create and maintain, they are treated as a primitive value. They're just like a number, making them light weight. 

!!! summary ""
    This design makes instances very cheap to create and maintain, and makes them especially convenient for many use cases in games and game engine APIs. For example when dealing with networking, plugins and other programming languages a primitive value is significantly easier for everyone.

    They're also a little bit safer, because using an invalid handle doesn't necessarily generate crashes or null values. Finally, in larger projects, it is not possible to efficiently operate on many instances in memory, but handles are a lot more efficient.
