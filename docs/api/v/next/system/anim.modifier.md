#![](../../../../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2024.12.4`)  


---

## `luxe: system/anim.modifier` module

- [Anim](#anim)   
- [AnimEvent](#animevent)   
- [AnimInterpolation](#animinterpolation)   
- [AnimInterval](#animinterval)   
- [AnimState](#animstate)   
- [Data](#data)   
- [System](#system)   

---

### Anim
`:::js import "luxe: system/anim.modifier" for Anim`
> `Anim` is an animation player attached to an entity.
> 
> It plays animations from animation assets or ones created from code. 
> Animations can target the entity `Anim` is attached to, 
> but can target any entity. 
> For example, a level cutscene could be played back from one entity, 
> but it drives several other entities. From assets like scenes and prototypes, 
> `Anim` provides an autoplay list, for playing when loaded. 
> 
> You can play multiple animations at the same time, 
> for example, the player might have a _walk_ animation playing 
> and you play a _glowing_ animation on top. 
> 
> `Anim` supports curve, linear and discrete driven animations 
> and is expanded on by World Systems that provide animation tracks.

- [create](#Anim.create)(**entity**: `Entity`)
- [destroy](#Anim.destroy)(**entity**: `Entity`)
- [has](#Anim.has)(**entity**: `Entity`)
- [valid](#Anim.valid+2)(**entity**: `Entity`, **anim**: `Anim`)
- [get_source_id](#Anim.get_source_id+2)(**entity**: `Entity`, **anim**: `Anim`)
- [get_state](#Anim.get_state+2)(**entity**: `Entity`, **anim**: `Anim`)
- [get_active_anims](#Anim.get_active_anims)(**entity**: `Entity`)
- [play](#Anim.play+3)(**entity**: `Entity`, **anim_lx**: `ID`, **time_offset**: `Num`)
- [blend](#Anim.blend+4)(**entity**: `Entity`, **anim_lx**: `ID`, **blend_time**: `Num`, **time_offset**: `Num`)
- [play](#Anim.play+2)(**entity**: `Entity`, **anim_lx**: `ID`)
- [blend](#Anim.blend+3)(**entity**: `Entity`, **anim_lx**: `ID`, **blend_time**: `Num`)
- [play_only](#Anim.play_only+3)(**entity**: `Entity`, **anim_lx**: `ID`, **time_offset**: `Num`)
- [play_only](#Anim.play_only+2)(**entity**: `Entity`, **anim_lx**: `ID`)
- [stop](#Anim.stop+3)(**entity**: `Entity`, **anim**: `Anim`, **reset**: `Bool`)
- [stop](#Anim.stop+2)(**entity**: `Entity`, **anim**: `Anim`)
- [stop_all](#Anim.stop_all+2)(**entity**: `Entity`, **reset**: `Bool`)
- [stop_all](#Anim.stop_all)(**entity**: `Entity`)
- [create_track](#Anim.create_track+4)(**entity**: `Entity`, **anim**: `Anim`, **track_id**: `Any`, **track_type**: `Any`)
- [has_track](#Anim.has_track+3)(**entity**: `Entity`, **anim**: `Anim`, **track_id**: `Any`)
- [track_set_range](#Anim.track_set_range+5)(**entity**: `Entity`, **anim**: `Anim`, **track_id**: `Any`, **min**: `Any`, **max**: `Any`)
- [track_get_range](#Anim.track_get_range+3)(**entity**: `Entity`, **anim**: `Anim`, **track_id**: `Any`)
- [track_set](#Anim.track_set+5)(**entity**: `Entity`, **anim**: `Anim`, **track_id**: `Any`, **property**: `Any`, **value**: `Any`)
- [track_set_channel](#Anim.track_set_channel+7)(**entity**: `Entity`, **anim**: `Anim`, **track_id**: `Any`, **channel_id**: `Any`, **channel_idx**: `Any`, **interp**: `Any`, **keys**: `Any`)
- [set_play_count](#Anim.set_play_count+3)(**entity**: `Entity`, **anim**: `Anim`, **play_count**: `Num`)
- [set_rate](#Anim.set_rate+3)(**entity**: `Entity`, **anim**: `Anim`, **rate**: `Num`)
- [set_start](#Anim.set_start+3)(**entity**: `Entity`, **anim**: `Anim`, **start**: `Num`)
- [set_end](#Anim.set_end+3)(**entity**: `Entity`, **anim**: `Anim`, **end**: `Num`)
- [set_interval_time](#Anim.set_interval_time+3)(**entity**: `Entity`, **anim**: `Anim`, **time**: `Num`)
- [get_play_count](#Anim.get_play_count+2)(**entity**: `Entity`, **anim**: `Anim`)
- [get_rate](#Anim.get_rate+2)(**entity**: `Entity`, **anim**: `Anim`)
- [get_duration](#Anim.get_duration+2)(**entity**: `Entity`, **anim**: `Anim`)
- [get_start](#Anim.get_start+2)(**entity**: `Entity`, **anim**: `Anim`)
- [get_end](#Anim.get_end+2)(**entity**: `Entity`, **anim**: `Anim`)
- [get_interval_time](#Anim.get_interval_time+2)(**entity**: `Entity`, **anim**: `Anim`)
- [on_event](#Anim.on_event+3)(**entity**: `Entity`, **anim**: `Anim`, **fn**: `Fn`)

<hr/>
<endpoint module="luxe: system/anim.modifier" class="Anim" signature="create(entity : Entity)"></endpoint>
<signature id="Anim.create">Anim.create(**entity**: `Entity`)
<a class="headerlink" href="#Anim.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Attach an `Anim` modifier to `entity`.
> 
>   ```js
>   var entity = Entity.create(world)
>   Anim.create(entity)
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="destroy(entity : Entity)"></endpoint>
<signature id="Anim.destroy">Anim.destroy(**entity**: `Entity`)
<a class="headerlink" href="#Anim.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Detach and destroy the `Anim` attached to `entity`.
> 
>   ```js
>   Anim.destroy(entity)
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="has(entity : Entity)"></endpoint>
<signature id="Anim.has">Anim.has(**entity**: `Entity`)
<a class="headerlink" href="#Anim.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns whether `entity` has an `Anim` modifier attached. 
> 
>   ```js
>   if(Anim.has(entity)) {
>     Log.print("found anim")
>   }
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="valid(entity : Entity, anim : Anim)"></endpoint>
<signature id="Anim.valid+2">Anim.valid(**entity**: `Entity`, **anim**: `Anim`)
<a class="headerlink" href="#Anim.valid+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns whether the `Anim` instance is valid for the `Anim` attached to `entity`. 
> 
>   ```js
>   var anim = Anim.play(entity, "player/idle")
>   if(!Anim.valid(entity, anim)) {
>     Log.print("oh no!")
>   }
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="get_source_id(entity : Entity, anim : Anim)"></endpoint>
<signature id="Anim.get_source_id+2">Anim.get_source_id(**entity**: `Entity`, **anim**: `Anim`)
<a class="headerlink" href="#Anim.get_source_id+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js ID`
> Returns the `ID` of the animation asset that the `Anim` instance was played from, 
> if known, by asking the `Anim` attached to `entity`. Returns `null` if not. 
> 
>   ```js
>   var anim = Anim.play(entity, "player/idle")
>   var source_id = Anim.get_source_id(entity, anim)
>   Log.print(Strings.get(source_id)) //expect: "player/idle"
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="get_state(entity : Entity, anim : Anim)"></endpoint>
<signature id="Anim.get_state+2">Anim.get_state(**entity**: `Entity`, **anim**: `Anim`)
<a class="headerlink" href="#Anim.get_state+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AnimState`
> Return the animation state of the `Anim` instance, by asking the `Anim` attached to `entity`. 
> 
>   ```js
>   var anim = Anim.play(entity, "player/idle")
>   var state = Anim.get_state(entity, anim)
>   if(state == AnimState.playing) {
>     Anim.stop(entity, anim)
>   }
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="get_active_anims(entity : Entity)"></endpoint>
<signature id="Anim.get_active_anims">Anim.get_active_anims(**entity**: `Entity`)
<a class="headerlink" href="#Anim.get_active_anims" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> Returns a list of `Anim` instances that are active on the `Anim` attached to `entity`. 
> 
>   ```js
>   var active = Anim.get_active_anims(entity)
>   for(anim in active) {
>     var state = Anim.get_state(entity, anim)
>     Log.print(AnimState.name(state));
>   }
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="play(entity : Entity, anim_lx : ID, time_offset : Num)"></endpoint>
<signature id="Anim.play+3">Anim.play(**entity**: `Entity`, **anim_lx**: `ID`, **time_offset**: `Num`)
<a class="headerlink" href="#Anim.play+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Anim`
> Play the animation asset `anim_lx` on the Anim attached to `entity`. 
> The `time_offset` is a time in seconds to begin playback from. 
> For example, you might pause an animation and hold onto the animation time when it was paused. 
> Then when resuming, you can play from the new time.
> Returns the newly started `Anim` instance.
> 
>   ```js
>   var anim = Anim.play(entity, "player/idle", 0.5)
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="blend(entity : Entity, anim_lx : ID, blend_time : Num, time_offset : Num)"></endpoint>
<signature id="Anim.blend+4">Anim.blend(**entity**: `Entity`, **anim_lx**: `ID`, **blend_time**: `Num`, **time_offset**: `Num`)
<a class="headerlink" href="#Anim.blend+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Anim`
> Play the animation asset `anim_lx` on the `Anim` attached to `entity` with a blend fade time. 
> The `time_offset` is a time in seconds to begin playback from. 
> The `blend_time` is handled by some tracks, not all.
> Returns the newly started `Anim` instance.
> 
>   ```js
>   //fade in the animation over 0.6 seconds
>   var anim = Anim.blend(entity, "player/idle", 0.6)
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="play(entity : Entity, anim_lx : ID)"></endpoint>
<signature id="Anim.play+2">Anim.play(**entity**: `Entity`, **anim_lx**: `ID`)
<a class="headerlink" href="#Anim.play+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Anim`
> Play the animation asset `anim_lx` on the `Anim` attached to `entity`. 
> Plays from the beginning.
> Returns the newly started `Anim` instance.
> 
>   ```js
>   var anim = Anim.play(entity, "player/idle")
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="blend(entity : Entity, anim_lx : ID, blend_time : Num)"></endpoint>
<signature id="Anim.blend+3">Anim.blend(**entity**: `Entity`, **anim_lx**: `ID`, **blend_time**: `Num`)
<a class="headerlink" href="#Anim.blend+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Anim`
> Play the animation asset `anim_lx` on the `Anim` attached to `entity` with a blend fade time. 
> Plays from the beginning. Blend time is handled by some tracks, not all.
> Returns the newly started `Anim` instance.
> 
>   ```js
>   //fade in the animation over 0.6 seconds
>   var anim = Anim.blend(entity, "player/idle", 0.6)
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="play_only(entity : Entity, anim_lx : ID, time_offset : Num)"></endpoint>
<signature id="Anim.play_only+3">Anim.play_only(**entity**: `Entity`, **anim_lx**: `ID`, **time_offset**: `Num`)
<a class="headerlink" href="#Anim.play_only+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Anim`
> Play the animation asset `anim_lx` on the `Anim` attached to `entity`, stopping all other active anims, 
> and only playing this one. The `time_offset` is a time in seconds to begin playback from. 
> Returns the newly started `Anim` instance.
> 
>   ```js
>   var anim = Anim.play_only(entity, "player/idle", 0.5)
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="play_only(entity : Entity, anim_lx : ID)"></endpoint>
<signature id="Anim.play_only+2">Anim.play_only(**entity**: `Entity`, **anim_lx**: `ID`)
<a class="headerlink" href="#Anim.play_only+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Anim`
> Play the animation asset `anim_lx` on the `Anim` attached to `entity`, stopping all other active anims, 
> and only playing this one.
> Returns the newly started `Anim` instance.
> 
>   ```js
>   var anim = Anim.play_only(entity, "player/idle")
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="stop(entity : Entity, anim : Anim, reset : Bool)"></endpoint>
<signature id="Anim.stop+3">Anim.stop(**entity**: `Entity`, **anim**: `Anim`, **reset**: `Bool`)
<a class="headerlink" href="#Anim.stop+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Stop the `Anim` instance if playing on the `Anim` attached to `entity`.
> 
> If `reset` is `true`, the state of anything that was being animated by this `Anim` instance, 
> will be reset to what it was before it was played. For example, if your animation is changing the transform position, 
> it will revert back to the position at the time the animation was played. 
> 
>   ```js
>   var anim = Anim.play(entity, "player/idle")
>   Anim.stop(entity, anim, true)
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="stop(entity : Entity, anim : Anim)"></endpoint>
<signature id="Anim.stop+2">Anim.stop(**entity**: `Entity`, **anim**: `Anim`)
<a class="headerlink" href="#Anim.stop+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Stop the `Anim` instance if playing on the `Anim` attached to `entity`. 
> State is not reset (see `Anim.stop(entity, anim, reset)`). 
> 
>   ```js
>   var anim = Anim.play(entity, "player/idle")
>   Anim.stop(entity, anim)
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="stop_all(entity : Entity, reset : Bool)"></endpoint>
<signature id="Anim.stop_all+2">Anim.stop_all(**entity**: `Entity`, **reset**: `Bool`)
<a class="headerlink" href="#Anim.stop_all+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Stop all active `Anim` instances playing on the `Anim` attached to `entity`. 
> If `reset` is `true`, state will be reset to the state before the animation started (see `Anim.stop(entity, anim, reset)`). 
> 
>   ```js
>   var anim = Anim.play(entity, "player/idle")
>   Anim.stop_all(entity, true)
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="stop_all(entity : Entity)"></endpoint>
<signature id="Anim.stop_all">Anim.stop_all(**entity**: `Entity`)
<a class="headerlink" href="#Anim.stop_all" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Stop all active `Anim` instances playing on the `Anim` attached to `entity`. 
> State is not reset (see `Anim.stop(entity, anim, reset)`). 
> 
>   ```js
>   var anim = Anim.play(entity, "player/idle")
>   Anim.stop_all(entity)
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="create_track(entity : Entity, anim : Anim, track_id : Any, track_type : Any)"></endpoint>
<signature id="Anim.create_track+4">Anim.create_track(**entity**: `Entity`, **anim**: `Anim`, **track_id**: `Any`, **track_type**: `Any`)
<a class="headerlink" href="#Anim.create_track+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="has_track(entity : Entity, anim : Anim, track_id : Any)"></endpoint>
<signature id="Anim.has_track+3">Anim.has_track(**entity**: `Entity`, **anim**: `Anim`, **track_id**: `Any`)
<a class="headerlink" href="#Anim.has_track+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="track_set_range(entity : Entity, anim : Anim, track_id : Any, min : Any, max : Any)"></endpoint>
<signature id="Anim.track_set_range+5">Anim.track_set_range(**entity**: `Entity`, **anim**: `Anim`, **track_id**: `Any`, **min**: `Any`, **max**: `Any`)
<a class="headerlink" href="#Anim.track_set_range+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="track_get_range(entity : Entity, anim : Anim, track_id : Any)"></endpoint>
<signature id="Anim.track_get_range+3">Anim.track_get_range(**entity**: `Entity`, **anim**: `Anim`, **track_id**: `Any`)
<a class="headerlink" href="#Anim.track_get_range+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="track_set(entity : Entity, anim : Anim, track_id : Any, property : Any, value : Any)"></endpoint>
<signature id="Anim.track_set+5">Anim.track_set(**entity**: `Entity`, **anim**: `Anim`, **track_id**: `Any`, **property**: `Any`, **value**: `Any`)
<a class="headerlink" href="#Anim.track_set+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="track_set_channel(entity : Entity, anim : Anim, track_id : Any, channel_id : Any, channel_idx : Any, interp : Any, keys : Any)"></endpoint>
<signature id="Anim.track_set_channel+7">Anim.track_set_channel(**entity**: `Entity`, **anim**: `Anim`, **track_id**: `Any`, **channel_id**: `Any`, **channel_idx**: `Any`, **interp**: `Any`, **keys**: `Any`)
<a class="headerlink" href="#Anim.track_set_channel+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="set_play_count(entity : Entity, anim : Anim, play_count : Num)"></endpoint>
<signature id="Anim.set_play_count+3">Anim.set_play_count(**entity**: `Entity`, **anim**: `Anim`, **play_count**: `Num`)
<a class="headerlink" href="#Anim.set_play_count+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the amount of times to play the `Anim` instance on the `Anim` attached to `entity`. 
> The `play_count` value can be `0`, which will loop forever.
> 
>   ```js
>   //play 3 times and then end
>   var anim = Anim.play(entity, "player/idle")
>   Anim.set_play_count(entity, anim, 3)
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="set_rate(entity : Entity, anim : Anim, rate : Num)"></endpoint>
<signature id="Anim.set_rate+3">Anim.set_rate(**entity**: `Entity`, **anim**: `Anim`, **rate**: `Num`)
<a class="headerlink" href="#Anim.set_rate+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the playback rate of the `Anim` instance on the `Anim` attached to `entity`. 
> The rate of `1` is the default speed. `0.5` is half speed, and `2` is twice as fast. 
> 
>   ```js
>   var anim = Anim.play(entity, "player/idle")
>   Anim.set_rate(entity, anim, 0.5)
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="set_start(entity : Entity, anim : Anim, start : Num)"></endpoint>
<signature id="Anim.set_start+3">Anim.set_start(**entity**: `Entity`, **anim**: `Anim`, **start**: `Num`)
<a class="headerlink" href="#Anim.set_start+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the start marker of the `Anim` instance on the `Anim` attached to `entity`. *note* This API is WIP. 
> 
>   ```js
>   Anim.set_start(entity, anim, 0)
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="set_end(entity : Entity, anim : Anim, end : Num)"></endpoint>
<signature id="Anim.set_end+3">Anim.set_end(**entity**: `Entity`, **anim**: `Anim`, **end**: `Num`)
<a class="headerlink" href="#Anim.set_end+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the end marker of the `Anim` instance on the `Anim` attached to `entity`. *note* This API is WIP. 
> 
>   ```js
>   Anim.set_end(entity, anim, 1)
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="set_interval_time(entity : Entity, anim : Anim, time : Num)"></endpoint>
<signature id="Anim.set_interval_time+3">Anim.set_interval_time(**entity**: `Entity`, **anim**: `Anim`, **time**: `Num`)
<a class="headerlink" href="#Anim.set_interval_time+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the current playback time of the `Anim` instance on the `Anim` attached to `entity`. *note* This API is WIP. 
> 
>   ```js
>   Anim.set_interval_time(entity, anim, 0.5)
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="get_play_count(entity : Entity, anim : Anim)"></endpoint>
<signature id="Anim.get_play_count+2">Anim.get_play_count(**entity**: `Entity`, **anim**: `Anim`)
<a class="headerlink" href="#Anim.get_play_count+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Return the play count of the `Anim` instance on the `Anim` attached to `entity`. 
> 
>   ```js
>   var play_count = Anim.get_play_count(entity, anim)
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="get_rate(entity : Entity, anim : Anim)"></endpoint>
<signature id="Anim.get_rate+2">Anim.get_rate(**entity**: `Entity`, **anim**: `Anim`)
<a class="headerlink" href="#Anim.get_rate+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Return the rate of playback of the `Anim` instance on the `Anim` attached to `entity`. 
> 
>   ```js
>   var play_count = Anim.get_play_count(entity, anim)
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="get_duration(entity : Entity, anim : Anim)"></endpoint>
<signature id="Anim.get_duration+2">Anim.get_duration(**entity**: `Entity`, **anim**: `Anim`)
<a class="headerlink" href="#Anim.get_duration+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Return the duration of the `Anim` instance on the `Anim` attached to `entity`. 
> 
>   ```js
>   var play_count = Anim.get_play_count(entity, anim)
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="get_start(entity : Entity, anim : Anim)"></endpoint>
<signature id="Anim.get_start+2">Anim.get_start(**entity**: `Entity`, **anim**: `Anim`)
<a class="headerlink" href="#Anim.get_start+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Return the start marker of the `Anim` instance on the `Anim` attached to `entity`. 
> 
>   ```js
>   var play_count = Anim.get_play_count(entity, anim)
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="get_end(entity : Entity, anim : Anim)"></endpoint>
<signature id="Anim.get_end+2">Anim.get_end(**entity**: `Entity`, **anim**: `Anim`)
<a class="headerlink" href="#Anim.get_end+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Return the end marker of the `Anim` instance on the `Anim` attached to `entity`. 
> 
>   ```js
>   var play_count = Anim.get_play_count(entity, anim)
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="get_interval_time(entity : Entity, anim : Anim)"></endpoint>
<signature id="Anim.get_interval_time+2">Anim.get_interval_time(**entity**: `Entity`, **anim**: `Anim`)
<a class="headerlink" href="#Anim.get_interval_time+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Return the current playback time of the `Anim` instance on the `Anim` attached to entity. *note* This API is WIP. 
> 
>   ```js
>   var play_count = Anim.get_play_count(entity, anim)
>   ```   

<endpoint module="luxe: system/anim.modifier" class="Anim" signature="on_event(entity : Entity, anim : Anim, fn : Fn)"></endpoint>
<signature id="Anim.on_event+3">Anim.on_event(**entity**: `Entity`, **anim**: `Anim`, **fn**: `Fn`)
<a class="headerlink" href="#Anim.on_event+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

### AnimEvent
`:::js import "luxe: system/anim.modifier" for AnimEvent`
> no docs found

- [start](#AnimEvent.start)
- [tick](#AnimEvent.tick)
- [complete](#AnimEvent.complete)

<hr/>
<endpoint module="luxe: system/anim.modifier" class="AnimEvent" signature="start"></endpoint>
<signature id="AnimEvent.start">AnimEvent.start
<a class="headerlink" href="#AnimEvent.start" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> An event fired when an animation started playing.   

<endpoint module="luxe: system/anim.modifier" class="AnimEvent" signature="tick"></endpoint>
<signature id="AnimEvent.tick">AnimEvent.tick
<a class="headerlink" href="#AnimEvent.tick" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> An event fired when an animation is updated, but only if the track is set to emit the event.   

<endpoint module="luxe: system/anim.modifier" class="AnimEvent" signature="complete"></endpoint>
<signature id="AnimEvent.complete">AnimEvent.complete
<a class="headerlink" href="#AnimEvent.complete" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> An event fired when an animation is stopped or done playing.   

### AnimInterpolation
`:::js import "luxe: system/anim.modifier" for AnimInterpolation`
> An enum for types of interpolation in animation tracks.

- [unknown](#AnimInterpolation.unknown)
- [curve](#AnimInterpolation.curve)
- [linear](#AnimInterpolation.linear)
- [discrete](#AnimInterpolation.discrete)
- [name](#AnimInterpolation.name)(**value**: `AnimInterpolation`)
- [from_string](#AnimInterpolation.from_string)(**value**: `String`)

<hr/>
<endpoint module="luxe: system/anim.modifier" class="AnimInterpolation" signature="unknown"></endpoint>
<signature id="AnimInterpolation.unknown">AnimInterpolation.unknown
<a class="headerlink" href="#AnimInterpolation.unknown" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> An invalid or unknown value.
> 
>   ```js
>   if(value == AnimInterpolation.unknown) {
>     Log.print("unknown interpolation type!")
>   }
>   ```   

<endpoint module="luxe: system/anim.modifier" class="AnimInterpolation" signature="curve"></endpoint>
<signature id="AnimInterpolation.curve">AnimInterpolation.curve
<a class="headerlink" href="#AnimInterpolation.curve" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> The animation values between keys will be interpolated 
> according to the curve defined by the keys themselves. 
> 
>   ```js
>   if(value == AnimInterpolation.curve) {
>     Log.print("curve")
>   }
>   ```   

<endpoint module="luxe: system/anim.modifier" class="AnimInterpolation" signature="linear"></endpoint>
<signature id="AnimInterpolation.linear">AnimInterpolation.linear
<a class="headerlink" href="#AnimInterpolation.linear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> The animation values between keys will be interpolated linearly. 
> For example if your keys were `{ time=0 value=0 }` and `{ time=1 value=4 }`, 
> at the time of `0.5` the value would be `2`, half of the next key. 
> 
>   ```js
>   if(value == AnimInterpolation.linear) {
>     Log.print("linear")
>   }
>   ```   

<endpoint module="luxe: system/anim.modifier" class="AnimInterpolation" signature="discrete"></endpoint>
<signature id="AnimInterpolation.discrete">AnimInterpolation.discrete
<a class="headerlink" href="#AnimInterpolation.discrete" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> The animation values between keys would not be interpolated, 
> they would jump from one value to the next. 
> For example if your keys were `{ time=0 value=0 }` and `{ time=1 value=3 }`, 
> with discrete the value at time `0.5` is still `0` 
> (instead of `1.5` with linear). 
> It will only change to `3` when the next key is reached. 
> 
>   ```js
>   if(value == AnimInterpolation.discrete) {
>     Log.print("discrete")
>   }
>   ```   

<endpoint module="luxe: system/anim.modifier" class="AnimInterpolation" signature="name(value : AnimInterpolation)"></endpoint>
<signature id="AnimInterpolation.name">AnimInterpolation.name(**value**: `AnimInterpolation`)
<a class="headerlink" href="#AnimInterpolation.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Convert an `AnimInterpolation` value to a string. 
> 
>   ```js
>   var type = AnimInterpolation.linear
>   var name = AnimInterpolation.name(type)
>   Log.print("type is %(name)") //expect: "linear"
>   ```   

<endpoint module="luxe: system/anim.modifier" class="AnimInterpolation" signature="from_string(value : String)"></endpoint>
<signature id="AnimInterpolation.from_string">AnimInterpolation.from_string(**value**: `String`)
<a class="headerlink" href="#AnimInterpolation.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AnimInterpolation`
> Get the `AnimInterpolation` value to a name.
> 
>   ```js
>   var type = AnimInterpolation.from_string("discrete")
>   Log.print("discrete is value %(type)") //expect: "3", the internal value
>   ```   

### AnimInterval
`:::js import "luxe: system/anim.modifier" for AnimInterval`
> no docs found

- [create](#AnimInterval.create+3)(**world**: `Any`, **duration**: `Any`, **rate**: `Any`)
- [create](#AnimInterval.create+2)(**world**: `Any`, **duration**: `Any`)
- [time](#AnimInterval.time+2)(**world**: `Any`, **anim**: `Any`)
- [set_time](#AnimInterval.set_time+3)(**world**: `Any`, **anim**: `Any`, **time**: `Any`)
- [set_now](#AnimInterval.set_now+3)(**world**: `Any`, **anim**: `Any`, **offset**: `Any`)
- [set_now](#AnimInterval.set_now+2)(**world**: `Any`, **anim**: `Any`)
- [set_play_count](#AnimInterval.set_play_count+3)(**world**: `Any`, **anim**: `Any`, **count**: `Any`)
- [set_clock](#AnimInterval.set_clock+3)(**world**: `Any`, **anim**: `Any`, **clock**: `Any`)
- [set_rate](#AnimInterval.set_rate+3)(**world**: `Any`, **anim**: `Any`, **rate**: `Any`)
- [set_duration](#AnimInterval.set_duration+3)(**world**: `Any`, **anim**: `Any`, **duration**: `Any`)
- [set_start](#AnimInterval.set_start+3)(**world**: `Any`, **anim**: `Any`, **start**: `Any`)
- [set_end](#AnimInterval.set_end+3)(**world**: `Any`, **anim**: `Any`, **end**: `Any`)
- [get_now](#AnimInterval.get_now+2)(**world**: `Any`, **anim**: `Any`)
- [get_play_count](#AnimInterval.get_play_count+2)(**world**: `Any`, **anim**: `Any`)
- [get_clock](#AnimInterval.get_clock+2)(**world**: `Any`, **anim**: `Any`)
- [get_rate](#AnimInterval.get_rate+2)(**world**: `Any`, **anim**: `Any`)
- [get_duration](#AnimInterval.get_duration+2)(**world**: `Any`, **anim**: `Any`)
- [get_start](#AnimInterval.get_start+2)(**world**: `Any`, **anim**: `Any`)
- [get_end](#AnimInterval.get_end+2)(**world**: `Any`, **anim**: `Any`)

<hr/>
<endpoint module="luxe: system/anim.modifier" class="AnimInterval" signature="create(world : Any, duration : Any, rate : Any)"></endpoint>
<signature id="AnimInterval.create+3">AnimInterval.create(**world**: `Any`, **duration**: `Any`, **rate**: `Any`)
<a class="headerlink" href="#AnimInterval.create+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/anim.modifier" class="AnimInterval" signature="create(world : Any, duration : Any)"></endpoint>
<signature id="AnimInterval.create+2">AnimInterval.create(**world**: `Any`, **duration**: `Any`)
<a class="headerlink" href="#AnimInterval.create+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/anim.modifier" class="AnimInterval" signature="time(world : Any, anim : Any)"></endpoint>
<signature id="AnimInterval.time+2">AnimInterval.time(**world**: `Any`, **anim**: `Any`)
<a class="headerlink" href="#AnimInterval.time+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/anim.modifier" class="AnimInterval" signature="set_time(world : Any, anim : Any, time : Any)"></endpoint>
<signature id="AnimInterval.set_time+3">AnimInterval.set_time(**world**: `Any`, **anim**: `Any`, **time**: `Any`)
<a class="headerlink" href="#AnimInterval.set_time+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/anim.modifier" class="AnimInterval" signature="set_now(world : Any, anim : Any, offset : Any)"></endpoint>
<signature id="AnimInterval.set_now+3">AnimInterval.set_now(**world**: `Any`, **anim**: `Any`, **offset**: `Any`)
<a class="headerlink" href="#AnimInterval.set_now+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/anim.modifier" class="AnimInterval" signature="set_now(world : Any, anim : Any)"></endpoint>
<signature id="AnimInterval.set_now+2">AnimInterval.set_now(**world**: `Any`, **anim**: `Any`)
<a class="headerlink" href="#AnimInterval.set_now+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/anim.modifier" class="AnimInterval" signature="set_play_count(world : Any, anim : Any, count : Any)"></endpoint>
<signature id="AnimInterval.set_play_count+3">AnimInterval.set_play_count(**world**: `Any`, **anim**: `Any`, **count**: `Any`)
<a class="headerlink" href="#AnimInterval.set_play_count+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/anim.modifier" class="AnimInterval" signature="set_clock(world : Any, anim : Any, clock : Any)"></endpoint>
<signature id="AnimInterval.set_clock+3">AnimInterval.set_clock(**world**: `Any`, **anim**: `Any`, **clock**: `Any`)
<a class="headerlink" href="#AnimInterval.set_clock+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/anim.modifier" class="AnimInterval" signature="set_rate(world : Any, anim : Any, rate : Any)"></endpoint>
<signature id="AnimInterval.set_rate+3">AnimInterval.set_rate(**world**: `Any`, **anim**: `Any`, **rate**: `Any`)
<a class="headerlink" href="#AnimInterval.set_rate+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/anim.modifier" class="AnimInterval" signature="set_duration(world : Any, anim : Any, duration : Any)"></endpoint>
<signature id="AnimInterval.set_duration+3">AnimInterval.set_duration(**world**: `Any`, **anim**: `Any`, **duration**: `Any`)
<a class="headerlink" href="#AnimInterval.set_duration+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/anim.modifier" class="AnimInterval" signature="set_start(world : Any, anim : Any, start : Any)"></endpoint>
<signature id="AnimInterval.set_start+3">AnimInterval.set_start(**world**: `Any`, **anim**: `Any`, **start**: `Any`)
<a class="headerlink" href="#AnimInterval.set_start+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/anim.modifier" class="AnimInterval" signature="set_end(world : Any, anim : Any, end : Any)"></endpoint>
<signature id="AnimInterval.set_end+3">AnimInterval.set_end(**world**: `Any`, **anim**: `Any`, **end**: `Any`)
<a class="headerlink" href="#AnimInterval.set_end+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/anim.modifier" class="AnimInterval" signature="get_now(world : Any, anim : Any)"></endpoint>
<signature id="AnimInterval.get_now+2">AnimInterval.get_now(**world**: `Any`, **anim**: `Any`)
<a class="headerlink" href="#AnimInterval.get_now+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/anim.modifier" class="AnimInterval" signature="get_play_count(world : Any, anim : Any)"></endpoint>
<signature id="AnimInterval.get_play_count+2">AnimInterval.get_play_count(**world**: `Any`, **anim**: `Any`)
<a class="headerlink" href="#AnimInterval.get_play_count+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/anim.modifier" class="AnimInterval" signature="get_clock(world : Any, anim : Any)"></endpoint>
<signature id="AnimInterval.get_clock+2">AnimInterval.get_clock(**world**: `Any`, **anim**: `Any`)
<a class="headerlink" href="#AnimInterval.get_clock+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/anim.modifier" class="AnimInterval" signature="get_rate(world : Any, anim : Any)"></endpoint>
<signature id="AnimInterval.get_rate+2">AnimInterval.get_rate(**world**: `Any`, **anim**: `Any`)
<a class="headerlink" href="#AnimInterval.get_rate+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/anim.modifier" class="AnimInterval" signature="get_duration(world : Any, anim : Any)"></endpoint>
<signature id="AnimInterval.get_duration+2">AnimInterval.get_duration(**world**: `Any`, **anim**: `Any`)
<a class="headerlink" href="#AnimInterval.get_duration+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/anim.modifier" class="AnimInterval" signature="get_start(world : Any, anim : Any)"></endpoint>
<signature id="AnimInterval.get_start+2">AnimInterval.get_start(**world**: `Any`, **anim**: `Any`)
<a class="headerlink" href="#AnimInterval.get_start+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: system/anim.modifier" class="AnimInterval" signature="get_end(world : Any, anim : Any)"></endpoint>
<signature id="AnimInterval.get_end+2">AnimInterval.get_end(**world**: `Any`, **anim**: `Any`)
<a class="headerlink" href="#AnimInterval.get_end+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### AnimState
`:::js import "luxe: system/anim.modifier" for AnimState`
> An enum for the state of an `Anim` instance.

- [inactive](#AnimState.inactive)
- [playing](#AnimState.playing)
- [ending](#AnimState.ending)
- [complete](#AnimState.complete)
- [name](#AnimState.name)(**value**: `Num`)
- [from_string](#AnimState.from_string)(**value**: `String`)

<hr/>
<endpoint module="luxe: system/anim.modifier" class="AnimState" signature="inactive"></endpoint>
<signature id="AnimState.inactive">AnimState.inactive
<a class="headerlink" href="#AnimState.inactive" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> The animation is inactive. _:todo: This may be obsolete_.
> 
>   ```js
>   var state = Anim.get_state(entity, anim)
>   if(state == AnimState.inactive) {
>     Log.print("anim is inactive")
>   }
>   ```   

<endpoint module="luxe: system/anim.modifier" class="AnimState" signature="playing"></endpoint>
<signature id="AnimState.playing">AnimState.playing
<a class="headerlink" href="#AnimState.playing" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> The animation is active and is playing.
> 
>   ```js
>   var state = Anim.get_state(entity, anim)
>   if(state == AnimState.playing) {
>     Log.print("anim is playing")
>   }
>   ```   

<endpoint module="luxe: system/anim.modifier" class="AnimState" signature="ending"></endpoint>
<signature id="AnimState.ending">AnimState.ending
<a class="headerlink" href="#AnimState.ending" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> The animation is ending, and will be marked complete next update.
> 
>   ```js
>   var state = Anim.get_state(entity, anim)
>   if(state == AnimState.ending) {
>     Log.print("anim is ending")
>   }
>   ```   

<endpoint module="luxe: system/anim.modifier" class="AnimState" signature="complete"></endpoint>
<signature id="AnimState.complete">AnimState.complete
<a class="headerlink" href="#AnimState.complete" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> The animation has ended and is complete.
> 
>   ```js
>   var state = Anim.get_state(entity, anim)
>   if(state == AnimState.complete) {
>     Log.print("anim is complete")
>   }
>   ```   

<endpoint module="luxe: system/anim.modifier" class="AnimState" signature="name(value : Num)"></endpoint>
<signature id="AnimState.name">AnimState.name(**value**: `Num`)
<a class="headerlink" href="#AnimState.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Convert an `AnimState` value to a string.
> 
>   ```js
>   var type = AnimState.ending
>   var name = AnimState.name(type)
>   Log.print("type is %(name)") //expect: "ending"
>   ```   

<endpoint module="luxe: system/anim.modifier" class="AnimState" signature="from_string(value : String)"></endpoint>
<signature id="AnimState.from_string">AnimState.from_string(**value**: `String`)
<a class="headerlink" href="#AnimState.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Convert a string to an enum value.
>         
>   ```js
>   var state = AnimState.from_string("ending")
>   var same = state == AnimState.ending //true
>   ```   

### Data
`:::js import "luxe: system/anim.modifier" for Data`
> no docs found

- `:::js var play : List = []`

<hr/>
### System
`:::js import "luxe: system/anim.modifier" for System`
> no docs found

- [new](#System.new)(**world**: `World`)

<hr/>
<endpoint module="luxe: system/anim.modifier" class="System" signature="new(world : World)"></endpoint>
<signature id="System.new">System.new(**world**: `World`)
<a class="headerlink" href="#System.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js System`
> no docs found   

