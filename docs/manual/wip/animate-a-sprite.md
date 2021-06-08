
# Animating a sprite

!!! warning ""
    Animation is a work in progress but still usable.   
    See `samples/systems/anim` and `samples/wip/sprite_anim` for more examples.

## Frame by frame animation

luxe provides an easy way to animate a sprite via atlas (packed image, sometimes called a spritesheet). This is done via the `Anim` modifier, which handles animating for us. 

We'll use a `sprite` animation track to achieve this.

## Create an animation asset

An animation is specified inside an `.anim.lx` file as an asset. 
We'll make one called `anim/idle.anim.lx` for our example. 

!!! note ""
    Soon, the [animation editor](https://i.imgur.com/dvQWXoE.mp4) will handle this for you. 

Inside an animation asset is some basic properties like the base animation rate (`fps_base`, default of `30`fps), how fast it should play (`rate`), whether it loops or not (`loop = true`), and the most important: a list of animation tracks. 

**Animation tracks allow us to specify something specific to animate**. These tracks are provided by various systems in the engine and your game. For example, a sprite animation track is provided by the `Sprite` modifier! 

We'll need to give the sprite animation track some specific options. 
One of those is the `grid` property, which tells it how to find the frames within our sprite image, and the other is the `material` which tells the sprite how to draw and which image to use.

We also specify keyframes. These keyframes are "image frames", and are specified in the `keys` list. The list of keys are items with a `time` and a `value`, which you'll find common in most animation tracks. 

!!! note ""
    Currently sprite animation is done via keys for consistency.
    You may find that you need frames+1 to get a full animation.

## A sprite animation asset

```js
animation = {
  rate = 1
  loop = true
  tracks = [
    {
       //this id is not important yet, 
       //it is not related to the anim asset id,
       //but must be unique to this animation asset
      id = "idle"
      type = "luxe: anim/sprite"
      options = {
        grid = [8,8]
      } //options
      keys = [
        { time=0 value=0 }
        { time=2 value=8 }
      ]
    }
  ]
}
```

## Playing the animation

To play the animation you need an `Anim` modifier attached to your entity. We reference the animation asset we just created.

```js
    //create an animation modifier on the entity
Anim.create(sprite)

    //play the animation that contains our sprite track.
    //this gives us an animation instance we can control
var current_anim = Anim.play(sprite, "anim/idle")
```

## Changing the animation

You can play multiple animations on an entity at any time, but for sprite animation tracks it won't really make sense to do that. Instead what we want to do is stop the one that was looping, and play a new one. To do that, we use the `Anim.play_only(entity, anim)` function. Or we can use the animation instance we got from `Anim.play` and give it to `Anim.stop`.

```js
  //create some animations
Anim.create(sprite)
var current_anim = Anim.play(sprite, "anim/idle")

  //now we want to change to run
current_anim = Anim.play_only(sprite, "anim/run")

  //now we want to change to jump
  //we stop only the run animation, 
  //so we can stack other animations if we want.

  //for example: a flashing animation to show
  //that the player is gaining experience.
  //we want that animation to keep playing,
  //but we want to replace the sprite animation.
Anim.stop(sprite, current_anim)
current_anim = Anim.play(sprite, "anim/jump")
```

!!! note "Future"
    An animation can have multiple tracks, making it easy to sync details in an animation. 

    For example, when animating a player jump animation, you might have: an audio track which plays a sound, right when the character leaves the ground. A particle effect spawned via an event track, a sprite track, and an event for when they're at the peak of the jump. On the game side, you'd use `Anim.play(player, "anim/jump")` to make it play all of that together.
    Currently there are `material` tracks, `transform` tracks, and `sprite` tracks only.