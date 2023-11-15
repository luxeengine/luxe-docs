#![](../images/luxe-dark.svg){width="96em"}

## Work In Progress!

Below are some details on what to expect immediate term, how we work, and why things like the world editor are in a bit of flux right now. 

!!! warning "2023.x transition period"
    There's a major shift happening in preparation for open beta, **please be patient**.   

    As we are converting systems and content to the new final form, there will be some growing pains and sometimes things won't be as stable as they usually are. **This period is typically short** and made shorter by people using and testing the engine, helping us flush them out quickly. We love it when you break stuff ✨
  
    We appreciate the understanding!

The docs too, are going to include outdated info briefly, but we're happy to guide via discord or the forums till they update (docs welcome contribution as well).

## Iterative design

The way luxe is made is iterative. Typically we know the rough direction but
not the exact shape until we prototype, experiment and explore. This allows us to find
the best workflows and also allows keeping the user projects functional and usable. 

_Projects from old versions remain compatible and we expect newer projects to be even more stable to change in that regard._

For a significant amount of the workflow, we've done the hard parts now, and are busy landing the final form of a lot of user facing things. This involves a lot of higher level, quick to do work (that is also really satisfying).

## Brief history

- The luxe closed beta started happening in small waves 
- In 2021 the closed beta became available more widely, named 'preview'
- Around 160 people participated, doing [game jams](https://luxeengine.com/luxe-jam-1/) and more
- The preview was stable enough and gave clarity to fundamental needs for wider use
    - e.g stable enough to make a whole [commercial game](https://store.steampowered.com/app/1836400/) with it
- During the rest of 2022, significant work happened to finalize the foundations 
- Work on the game drove development a lot as well, pushing forward on shipping essentials
- We are now in the transition period moving to the new systems!

## Major shifts

The transition period is where we have kinda both versions of the engine in flight for a short period.
_This speaks to the flexibility and design that we can replace entire systems while still keeping projects compatible, and still keep big projects running smoothly._

Below has some info on the moving parts, as well as some before/after for comparison on the improvements driven by these shifts, and how they'll be the last form for a long time.

### 'Blocks' - The data transport

There's a data transport concept in luxe called 'blocks', it's a schema based data definition and storage system that holds onto typed data for you. It can load and save this data to binary or lx format, it can copy and slice the data, it can take snapshots and more. This is a fundamental foundational part of the engine.

The block service (unsurprisingly) took a lot of iterating to find the right shape. Since it kind of fills a lot of needs, from custom user asset types all the way to runtime data for custom modifiers, there was a lot of exploring needed and a lot of real world data from making games needed. 

And, because a lot of things (like assets, and modifiers, the editors etc) rely on it, these things were waiting on the blocks to land before expanding their features. With the blocks in place now, a lot of stuff cascades out behind them quickly.

### The asset system 
The old asset system did just enough to make stuff with, but was a placeholder until blocks filled the gaps. The old system did the obvious thing of writing a compiler for every type, manually, and the reader for it on the other end. 

The new asset system makes assets automatic, where you define the asset schema, it handles all the details (thanks to blocks). Asset processing is now user space as well, and custom asset types are treated the same as built in, and come with all the same benefits. The new asset system is significantly nicer already, but still has a few key things being hooked up - notably the two way reference being finished and better hot reloading support.

### The modifiers
The old modifiers did actually use the early version of blocks (to figure out the shape), but it was limited to primitve values and defining the blocks in lx data (see the old custom modifier docs for now). 

This has been redone, and the new modifier data is defined in code, in place, and supports arrays and objects as well as more primitive types (thanks to the blocks). The modifier UI in the editor is now all automated instead of hand written (thanks to blocks). There's a dozen other things here that will become clear in the new modifier docs when they land.

Built in modifiers are in the process of being converted to the new format.

### The scenes and prototypes
Old prototypes (prefabs) had a fatal flaw in their data addressing which was tricky to realize cos of how things were set up. For example, in Mossfield Origins there's around 300 prototypes, all working perfectly, and not encountering the issue. The new prototypes solve all those issues and are more sturdy and ready for further improvement.

The old scene format was focused on putting multiple entities into a single file, but splitting those into layers so that teams could work on the same content without too much merge conflicts. The real issue came in the editing workflow, managing content inside of a container vs modifying the content directly led to a lot of complexity and code. 

The new scene format goes back to a much older iteration, where each entity in a scene is it's own file. This makes the content significantly clearer, simpler, and easier to edit manipulate. It also is much simpler mental model, as you can move around files on disk within the scene folder as regular files.

The old scene format compiler used to manually splice the content together if only a portion changed, now it's all automatic and simpler. The new compiler is now shared by prototypes and scenes, and internally the data representation is shared so that there's a single, well defined code path for everything. 

### The world editor

The world editor has been rewritten from scratch, to utilize the new blocks and to use the modifiers and scene formats. This alone cut down on thouands of lines of code, which is a strong signal we're on the right path.

There's still some minor QOL things and some major issues as this is very fresh code and we'll rapidly iterate on improving it.


## Conclusion

With so many moving parts being finalized, and them taking really great shape, it's still important to recognize the potential for code that hasn't been exercised as much as the old code, for things that aren't 100% yet, or are just plain broken. 

We're aware of those things, and they get fixed quickly. They get fixed even quicker by people using it and bumping into them, as it's difficult to test all of the corners ourselves. You are also welcome to contribute, the editor code is a regular luxe game written in wren, and a lot of the harder stuff is done.

We appreciate the patience and support in helping us test and solidify all this new stuff! And we can't wait for the dust to settle and this warning to not be necessary.