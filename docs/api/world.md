#![](../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2021.0.9`)  


---

## `luxe: world` module

- [Anim](#anim)   
- [AnimEvent](#animevent)   
- [AnimInterpolation](#animinterpolation)   
- [AnimInterval](#animinterval)   
- [AnimState](#animstate)   
- [Body2D](#body2d)   
- [Body3D](#body3d)   
- [BodyEvent](#bodyevent)   
- [BodyType](#bodytype)   
- [Camera](#camera)   
- [Clock](#clock)   
- [Entity](#entity)   
- [Layer](#layer)   
- [Mesh](#mesh)   
- [MeshColliderType](#meshcollidertype)   
- [ModifierSystem](#modifiersystem)   
- [Modifiers](#modifiers)   
- [Overlap](#overlap)   
- [Physics2D](#physics2d)   
- [Physics3D](#physics3d)   
- [Prototype](#prototype)   
- [Scene](#scene)   
- [Sprite](#sprite)   
- [Tags](#tags)   
- [Text](#text)   
- [Tile](#tile)   
- [Tiles](#tiles)   
- [Transform](#transform)   
- [UI](#ui)   
- [UIClear](#uiclear)   
- [UIEvent](#uievent)   
- [UILayout](#uilayout)   
- [UILayoutBehave](#uilayoutbehave)   
- [UILayoutContain](#uilayoutcontain)   
- [UIRenderMode](#uirendermode)   
- [Values](#values)   
- [ValuesType](#valuestype)   
- [World](#world)   
- [WorldRenderDesc](#worldrenderdesc)   

---

### Anim
`:::js import "luxe: world" for Anim`
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
- [play](#Anim.play+2)(**entity**: `Entity`, **anim_lx**: `ID`)
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
<endpoint module="luxe: world" class="Anim" signature="create(entity : Entity)"></endpoint>
<signature id="Anim.create">Anim.create(**entity**: `Entity`)
<a class="headerlink" href="#Anim.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Attach an `Anim` modifier to `entity`.
> 
>   ```js
>   var entity = Entity.create(world)
>   Anim.create(entity)
>   ```   

<endpoint module="luxe: world" class="Anim" signature="destroy(entity : Entity)"></endpoint>
<signature id="Anim.destroy">Anim.destroy(**entity**: `Entity`)
<a class="headerlink" href="#Anim.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Detach and destroy the `Anim` attached to `entity`.
> 
>   ```js
>   Anim.destroy(entity)
>   ```   

<endpoint module="luxe: world" class="Anim" signature="has(entity : Entity)"></endpoint>
<signature id="Anim.has">Anim.has(**entity**: `Entity`)
<a class="headerlink" href="#Anim.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns whether `entity` has an `Anim` modifier attached. 
> 
>   ```js
>   if(Anim.has(entity)) {
>     System.print("found anim")
>   }
>   ```   

<endpoint module="luxe: world" class="Anim" signature="valid(entity : Entity, anim : Anim)"></endpoint>
<signature id="Anim.valid+2">Anim.valid(**entity**: `Entity`, **anim**: `Anim`)
<a class="headerlink" href="#Anim.valid+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns whether the `Anim` instance is valid for the `Anim` attached to `entity`. 
> 
>   ```js
>   var anim = Anim.play(entity, "player/idle")
>   if(!Anim.valid(entity, anim)) {
>     System.print("oh no!")
>   }
>   ```   

<endpoint module="luxe: world" class="Anim" signature="get_source_id(entity : Entity, anim : Anim)"></endpoint>
<signature id="Anim.get_source_id+2">Anim.get_source_id(**entity**: `Entity`, **anim**: `Anim`)
<a class="headerlink" href="#Anim.get_source_id+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js ID`
> Returns the `ID` of the animation asset that the `Anim` instance was played from, 
> if known, by asking the `Anim` attached to `entity`. Returns `null` if not. 
> 
>   ```js
>   var anim = Anim.play(entity, "player/idle")
>   var source_id = Anim.get_source_id(entity, anim)
>   System.print(Strings.get(source_id)) //expect: "player/idle"
>   ```   

<endpoint module="luxe: world" class="Anim" signature="get_state(entity : Entity, anim : Anim)"></endpoint>
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

<endpoint module="luxe: world" class="Anim" signature="get_active_anims(entity : Entity)"></endpoint>
<signature id="Anim.get_active_anims">Anim.get_active_anims(**entity**: `Entity`)
<a class="headerlink" href="#Anim.get_active_anims" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> Returns a list of `Anim` instances that are active on the `Anim` attached to `entity`. 
> 
>   ```js
>   var active = Anim.get_active_anims(entity)
>   for(anim in active) {
>     var state = Anim.get_state(entity, anim)
>     System.print(AnimState.name(state));
>   }
>   ```   

<endpoint module="luxe: world" class="Anim" signature="play(entity : Entity, anim_lx : ID, time_offset : Num)"></endpoint>
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

<endpoint module="luxe: world" class="Anim" signature="play(entity : Entity, anim_lx : ID)"></endpoint>
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

<endpoint module="luxe: world" class="Anim" signature="play_only(entity : Entity, anim_lx : ID, time_offset : Num)"></endpoint>
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

<endpoint module="luxe: world" class="Anim" signature="play_only(entity : Entity, anim_lx : ID)"></endpoint>
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

<endpoint module="luxe: world" class="Anim" signature="stop(entity : Entity, anim : Anim, reset : Bool)"></endpoint>
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

<endpoint module="luxe: world" class="Anim" signature="stop(entity : Entity, anim : Anim)"></endpoint>
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

<endpoint module="luxe: world" class="Anim" signature="stop_all(entity : Entity, reset : Bool)"></endpoint>
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

<endpoint module="luxe: world" class="Anim" signature="stop_all(entity : Entity)"></endpoint>
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

<endpoint module="luxe: world" class="Anim" signature="create_track(entity : Entity, anim : Anim, track_id : Any, track_type : Any)"></endpoint>
<signature id="Anim.create_track+4">Anim.create_track(**entity**: `Entity`, **anim**: `Anim`, **track_id**: `Any`, **track_type**: `Any`)
<a class="headerlink" href="#Anim.create_track+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Anim" signature="has_track(entity : Entity, anim : Anim, track_id : Any)"></endpoint>
<signature id="Anim.has_track+3">Anim.has_track(**entity**: `Entity`, **anim**: `Anim`, **track_id**: `Any`)
<a class="headerlink" href="#Anim.has_track+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Anim" signature="track_set_range(entity : Entity, anim : Anim, track_id : Any, min : Any, max : Any)"></endpoint>
<signature id="Anim.track_set_range+5">Anim.track_set_range(**entity**: `Entity`, **anim**: `Anim`, **track_id**: `Any`, **min**: `Any`, **max**: `Any`)
<a class="headerlink" href="#Anim.track_set_range+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Anim" signature="track_get_range(entity : Entity, anim : Anim, track_id : Any)"></endpoint>
<signature id="Anim.track_get_range+3">Anim.track_get_range(**entity**: `Entity`, **anim**: `Anim`, **track_id**: `Any`)
<a class="headerlink" href="#Anim.track_get_range+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Anim" signature="track_set(entity : Entity, anim : Anim, track_id : Any, property : Any, value : Any)"></endpoint>
<signature id="Anim.track_set+5">Anim.track_set(**entity**: `Entity`, **anim**: `Anim`, **track_id**: `Any`, **property**: `Any`, **value**: `Any`)
<a class="headerlink" href="#Anim.track_set+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Anim" signature="track_set_channel(entity : Entity, anim : Anim, track_id : Any, channel_id : Any, channel_idx : Any, interp : Any, keys : Any)"></endpoint>
<signature id="Anim.track_set_channel+7">Anim.track_set_channel(**entity**: `Entity`, **anim**: `Anim`, **track_id**: `Any`, **channel_id**: `Any`, **channel_idx**: `Any`, **interp**: `Any`, **keys**: `Any`)
<a class="headerlink" href="#Anim.track_set_channel+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Anim" signature="set_play_count(entity : Entity, anim : Anim, play_count : Num)"></endpoint>
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

<endpoint module="luxe: world" class="Anim" signature="set_rate(entity : Entity, anim : Anim, rate : Num)"></endpoint>
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

<endpoint module="luxe: world" class="Anim" signature="set_start(entity : Entity, anim : Anim, start : Num)"></endpoint>
<signature id="Anim.set_start+3">Anim.set_start(**entity**: `Entity`, **anim**: `Anim`, **start**: `Num`)
<a class="headerlink" href="#Anim.set_start+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the start marker of the `Anim` instance on the `Anim` attached to `entity`. *note* This API is WIP. 
> 
>   ```js
>   Anim.set_start(entity, anim, 0)
>   ```   

<endpoint module="luxe: world" class="Anim" signature="set_end(entity : Entity, anim : Anim, end : Num)"></endpoint>
<signature id="Anim.set_end+3">Anim.set_end(**entity**: `Entity`, **anim**: `Anim`, **end**: `Num`)
<a class="headerlink" href="#Anim.set_end+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the end marker of the `Anim` instance on the `Anim` attached to `entity`. *note* This API is WIP. 
> 
>   ```js
>   Anim.set_end(entity, anim, 1)
>   ```   

<endpoint module="luxe: world" class="Anim" signature="set_interval_time(entity : Entity, anim : Anim, time : Num)"></endpoint>
<signature id="Anim.set_interval_time+3">Anim.set_interval_time(**entity**: `Entity`, **anim**: `Anim`, **time**: `Num`)
<a class="headerlink" href="#Anim.set_interval_time+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the current playback time of the `Anim` instance on the `Anim` attached to `entity`. *note* This API is WIP. 
> 
>   ```js
>   Anim.set_interval_time(entity, anim, 0.5)
>   ```   

<endpoint module="luxe: world" class="Anim" signature="get_play_count(entity : Entity, anim : Anim)"></endpoint>
<signature id="Anim.get_play_count+2">Anim.get_play_count(**entity**: `Entity`, **anim**: `Anim`)
<a class="headerlink" href="#Anim.get_play_count+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Return the play count of the `Anim` instance on the `Anim` attached to `entity`. 
> 
>   ```js
>   var play_count = Anim.get_play_count(entity, anim)
>   ```   

<endpoint module="luxe: world" class="Anim" signature="get_rate(entity : Entity, anim : Anim)"></endpoint>
<signature id="Anim.get_rate+2">Anim.get_rate(**entity**: `Entity`, **anim**: `Anim`)
<a class="headerlink" href="#Anim.get_rate+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Return the rate of playback of the `Anim` instance on the `Anim` attached to `entity`. 
> 
>   ```js
>   var play_count = Anim.get_play_count(entity, anim)
>   ```   

<endpoint module="luxe: world" class="Anim" signature="get_duration(entity : Entity, anim : Anim)"></endpoint>
<signature id="Anim.get_duration+2">Anim.get_duration(**entity**: `Entity`, **anim**: `Anim`)
<a class="headerlink" href="#Anim.get_duration+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Return the duration of the `Anim` instance on the `Anim` attached to `entity`. 
> 
>   ```js
>   var play_count = Anim.get_play_count(entity, anim)
>   ```   

<endpoint module="luxe: world" class="Anim" signature="get_start(entity : Entity, anim : Anim)"></endpoint>
<signature id="Anim.get_start+2">Anim.get_start(**entity**: `Entity`, **anim**: `Anim`)
<a class="headerlink" href="#Anim.get_start+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Return the start marker of the `Anim` instance on the `Anim` attached to `entity`. 
> 
>   ```js
>   var play_count = Anim.get_play_count(entity, anim)
>   ```   

<endpoint module="luxe: world" class="Anim" signature="get_end(entity : Entity, anim : Anim)"></endpoint>
<signature id="Anim.get_end+2">Anim.get_end(**entity**: `Entity`, **anim**: `Anim`)
<a class="headerlink" href="#Anim.get_end+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Return the end marker of the `Anim` instance on the `Anim` attached to `entity`. 
> 
>   ```js
>   var play_count = Anim.get_play_count(entity, anim)
>   ```   

<endpoint module="luxe: world" class="Anim" signature="get_interval_time(entity : Entity, anim : Anim)"></endpoint>
<signature id="Anim.get_interval_time+2">Anim.get_interval_time(**entity**: `Entity`, **anim**: `Anim`)
<a class="headerlink" href="#Anim.get_interval_time+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Return the current playback time of the `Anim` instance on the `Anim` attached to entity. *note* This API is WIP. 
> 
>   ```js
>   var play_count = Anim.get_play_count(entity, anim)
>   ```   

<endpoint module="luxe: world" class="Anim" signature="on_event(entity : Entity, anim : Anim, fn : Fn)"></endpoint>
<signature id="Anim.on_event+3">Anim.on_event(**entity**: `Entity`, **anim**: `Anim`, **fn**: `Fn`)
<a class="headerlink" href="#Anim.on_event+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> no docs found   

### AnimEvent
`:::js import "luxe: world" for AnimEvent`
> no docs found

- [start](#AnimEvent.start)
- [tick](#AnimEvent.tick)
- [complete](#AnimEvent.complete)

<hr/>
<endpoint module="luxe: world" class="AnimEvent" signature="start"></endpoint>
<signature id="AnimEvent.start">AnimEvent.start
<a class="headerlink" href="#AnimEvent.start" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="AnimEvent" signature="tick"></endpoint>
<signature id="AnimEvent.tick">AnimEvent.tick
<a class="headerlink" href="#AnimEvent.tick" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="AnimEvent" signature="complete"></endpoint>
<signature id="AnimEvent.complete">AnimEvent.complete
<a class="headerlink" href="#AnimEvent.complete" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### AnimInterpolation
`:::js import "luxe: world" for AnimInterpolation`
> An enum for types of interpolation in animation tracks.

- [unknown](#AnimInterpolation.unknown)
- [curve](#AnimInterpolation.curve)
- [linear](#AnimInterpolation.linear)
- [discrete](#AnimInterpolation.discrete)
- [name](#AnimInterpolation.name)(**value**: `AnimInterpolation`)
- [from_string](#AnimInterpolation.from_string)(**value**: `String`)

<hr/>
<endpoint module="luxe: world" class="AnimInterpolation" signature="unknown"></endpoint>
<signature id="AnimInterpolation.unknown">AnimInterpolation.unknown
<a class="headerlink" href="#AnimInterpolation.unknown" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> An invalid or unknown value.
> 
>   ```js
>   if(value == AnimInterpolation.unknown) {
>     System.print("unknown interpolation type!")
>   }
>   ```   

<endpoint module="luxe: world" class="AnimInterpolation" signature="curve"></endpoint>
<signature id="AnimInterpolation.curve">AnimInterpolation.curve
<a class="headerlink" href="#AnimInterpolation.curve" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> The animation values between keys will be interpolated 
> according to the curve defined by the keys themselves. 
> 
>   ```js
>   if(value == AnimInterpolation.curve) {
>     System.print("curve")
>   }
>   ```   

<endpoint module="luxe: world" class="AnimInterpolation" signature="linear"></endpoint>
<signature id="AnimInterpolation.linear">AnimInterpolation.linear
<a class="headerlink" href="#AnimInterpolation.linear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> The animation values between keys will be interpolated linearly. 
> For example if your keys were `{ time=0 value=0 }` and `{ time=1 value=4 }`, 
> at the time of `0.5` the value would be `2`, half of the next key. 
> 
>   ```js
>   if(value == AnimInterpolation.linear) {
>     System.print("linear")
>   }
>   ```   

<endpoint module="luxe: world" class="AnimInterpolation" signature="discrete"></endpoint>
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
>     System.print("discrete")
>   }
>   ```   

<endpoint module="luxe: world" class="AnimInterpolation" signature="name(value : AnimInterpolation)"></endpoint>
<signature id="AnimInterpolation.name">AnimInterpolation.name(**value**: `AnimInterpolation`)
<a class="headerlink" href="#AnimInterpolation.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Convert an `AnimInterpolation` value to a string. 
> 
>   ```js
>   var type = AnimInterpolation.linear
>   var name = AnimInterpolation.name(type)
>   System.print("type is %(name)") //expect: "linear"
>   ```   

<endpoint module="luxe: world" class="AnimInterpolation" signature="from_string(value : String)"></endpoint>
<signature id="AnimInterpolation.from_string">AnimInterpolation.from_string(**value**: `String`)
<a class="headerlink" href="#AnimInterpolation.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AnimInterpolation`
> Get the `AnimInterpolation` value to a name.
> 
>   ```js
>   var type = AnimInterpolation.from_string("discrete")
>   System.print("discrete is value %(type)") //expect: "3", the internal value
>   ```   

### AnimInterval
`:::js import "luxe: world" for AnimInterval`
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
<endpoint module="luxe: world" class="AnimInterval" signature="create(world : Any, duration : Any, rate : Any)"></endpoint>
<signature id="AnimInterval.create+3">AnimInterval.create(**world**: `Any`, **duration**: `Any`, **rate**: `Any`)
<a class="headerlink" href="#AnimInterval.create+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="AnimInterval" signature="create(world : Any, duration : Any)"></endpoint>
<signature id="AnimInterval.create+2">AnimInterval.create(**world**: `Any`, **duration**: `Any`)
<a class="headerlink" href="#AnimInterval.create+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="AnimInterval" signature="time(world : Any, anim : Any)"></endpoint>
<signature id="AnimInterval.time+2">AnimInterval.time(**world**: `Any`, **anim**: `Any`)
<a class="headerlink" href="#AnimInterval.time+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="AnimInterval" signature="set_time(world : Any, anim : Any, time : Any)"></endpoint>
<signature id="AnimInterval.set_time+3">AnimInterval.set_time(**world**: `Any`, **anim**: `Any`, **time**: `Any`)
<a class="headerlink" href="#AnimInterval.set_time+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="AnimInterval" signature="set_now(world : Any, anim : Any, offset : Any)"></endpoint>
<signature id="AnimInterval.set_now+3">AnimInterval.set_now(**world**: `Any`, **anim**: `Any`, **offset**: `Any`)
<a class="headerlink" href="#AnimInterval.set_now+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="AnimInterval" signature="set_now(world : Any, anim : Any)"></endpoint>
<signature id="AnimInterval.set_now+2">AnimInterval.set_now(**world**: `Any`, **anim**: `Any`)
<a class="headerlink" href="#AnimInterval.set_now+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="AnimInterval" signature="set_play_count(world : Any, anim : Any, count : Any)"></endpoint>
<signature id="AnimInterval.set_play_count+3">AnimInterval.set_play_count(**world**: `Any`, **anim**: `Any`, **count**: `Any`)
<a class="headerlink" href="#AnimInterval.set_play_count+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="AnimInterval" signature="set_clock(world : Any, anim : Any, clock : Any)"></endpoint>
<signature id="AnimInterval.set_clock+3">AnimInterval.set_clock(**world**: `Any`, **anim**: `Any`, **clock**: `Any`)
<a class="headerlink" href="#AnimInterval.set_clock+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="AnimInterval" signature="set_rate(world : Any, anim : Any, rate : Any)"></endpoint>
<signature id="AnimInterval.set_rate+3">AnimInterval.set_rate(**world**: `Any`, **anim**: `Any`, **rate**: `Any`)
<a class="headerlink" href="#AnimInterval.set_rate+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="AnimInterval" signature="set_duration(world : Any, anim : Any, duration : Any)"></endpoint>
<signature id="AnimInterval.set_duration+3">AnimInterval.set_duration(**world**: `Any`, **anim**: `Any`, **duration**: `Any`)
<a class="headerlink" href="#AnimInterval.set_duration+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="AnimInterval" signature="set_start(world : Any, anim : Any, start : Any)"></endpoint>
<signature id="AnimInterval.set_start+3">AnimInterval.set_start(**world**: `Any`, **anim**: `Any`, **start**: `Any`)
<a class="headerlink" href="#AnimInterval.set_start+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="AnimInterval" signature="set_end(world : Any, anim : Any, end : Any)"></endpoint>
<signature id="AnimInterval.set_end+3">AnimInterval.set_end(**world**: `Any`, **anim**: `Any`, **end**: `Any`)
<a class="headerlink" href="#AnimInterval.set_end+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="AnimInterval" signature="get_now(world : Any, anim : Any)"></endpoint>
<signature id="AnimInterval.get_now+2">AnimInterval.get_now(**world**: `Any`, **anim**: `Any`)
<a class="headerlink" href="#AnimInterval.get_now+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="AnimInterval" signature="get_play_count(world : Any, anim : Any)"></endpoint>
<signature id="AnimInterval.get_play_count+2">AnimInterval.get_play_count(**world**: `Any`, **anim**: `Any`)
<a class="headerlink" href="#AnimInterval.get_play_count+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="AnimInterval" signature="get_clock(world : Any, anim : Any)"></endpoint>
<signature id="AnimInterval.get_clock+2">AnimInterval.get_clock(**world**: `Any`, **anim**: `Any`)
<a class="headerlink" href="#AnimInterval.get_clock+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="AnimInterval" signature="get_rate(world : Any, anim : Any)"></endpoint>
<signature id="AnimInterval.get_rate+2">AnimInterval.get_rate(**world**: `Any`, **anim**: `Any`)
<a class="headerlink" href="#AnimInterval.get_rate+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="AnimInterval" signature="get_duration(world : Any, anim : Any)"></endpoint>
<signature id="AnimInterval.get_duration+2">AnimInterval.get_duration(**world**: `Any`, **anim**: `Any`)
<a class="headerlink" href="#AnimInterval.get_duration+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="AnimInterval" signature="get_start(world : Any, anim : Any)"></endpoint>
<signature id="AnimInterval.get_start+2">AnimInterval.get_start(**world**: `Any`, **anim**: `Any`)
<a class="headerlink" href="#AnimInterval.get_start+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="AnimInterval" signature="get_end(world : Any, anim : Any)"></endpoint>
<signature id="AnimInterval.get_end+2">AnimInterval.get_end(**world**: `Any`, **anim**: `Any`)
<a class="headerlink" href="#AnimInterval.get_end+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### AnimState
`:::js import "luxe: world" for AnimState`
> An enum for the state of an `Anim` instance.

- [inactive](#AnimState.inactive)
- [playing](#AnimState.playing)
- [ending](#AnimState.ending)
- [complete](#AnimState.complete)
- [name](#AnimState.name)(**value**: `Num`)
- [from_string](#AnimState.from_string)(**value**: `String`)

<hr/>
<endpoint module="luxe: world" class="AnimState" signature="inactive"></endpoint>
<signature id="AnimState.inactive">AnimState.inactive
<a class="headerlink" href="#AnimState.inactive" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> The animation is inactive. _:todo: This may be obsolete_.
> 
>   ```js
>   var state = Anim.get_state(entity, anim)
>   if(state == AnimState.inactive) {
>     System.print("anim is inactive")
>   }
>   ```   

<endpoint module="luxe: world" class="AnimState" signature="playing"></endpoint>
<signature id="AnimState.playing">AnimState.playing
<a class="headerlink" href="#AnimState.playing" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> The animation is active and is playing.
> 
>   ```js
>   var state = Anim.get_state(entity, anim)
>   if(state == AnimState.playing) {
>     System.print("anim is playing")
>   }
>   ```   

<endpoint module="luxe: world" class="AnimState" signature="ending"></endpoint>
<signature id="AnimState.ending">AnimState.ending
<a class="headerlink" href="#AnimState.ending" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> The animation is ending, and will be marked complete next update.
> 
>   ```js
>   var state = Anim.get_state(entity, anim)
>   if(state == AnimState.ending) {
>     System.print("anim is ending")
>   }
>   ```   

<endpoint module="luxe: world" class="AnimState" signature="complete"></endpoint>
<signature id="AnimState.complete">AnimState.complete
<a class="headerlink" href="#AnimState.complete" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> The animation has ended and is complete.
> 
>   ```js
>   var state = Anim.get_state(entity, anim)
>   if(state == AnimState.complete) {
>     System.print("anim is complete")
>   }
>   ```   

<endpoint module="luxe: world" class="AnimState" signature="name(value : Num)"></endpoint>
<signature id="AnimState.name">AnimState.name(**value**: `Num`)
<a class="headerlink" href="#AnimState.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Convert an `AnimState` value to a string.
> 
>   ```js
>   var type = AnimState.ending
>   var name = AnimState.name(type)
>   System.print("type is %(name)") //expect: "ending"
>   ```   

<endpoint module="luxe: world" class="AnimState" signature="from_string(value : String)"></endpoint>
<signature id="AnimState.from_string">AnimState.from_string(**value**: `String`)
<a class="headerlink" href="#AnimState.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Convert a string to an enum value.
>             
>   ```js
>   var state = AnimState.from_string("ending")
>   var same = state == AnimState.ending //true
>   ```   

### Body2D
`:::js import "luxe: world" for Body2D`
> no docs found

- [create](#Body2D.create)(**entity**: `Any`)
- [has](#Body2D.has)(**entity**: `Any`)
- [create_collider_box](#Body2D.create_collider_box+4)(**entity**: `Any`, **center**: `Any`, **size**: `Any`, **angle**: `Any`)
- [create_collider_circle](#Body2D.create_collider_circle+3)(**entity**: `Any`, **center**: `Any`, **radius**: `Any`)
- [get_center](#Body2D.get_center)(**entity**: `Any`)
- [get_mass](#Body2D.get_mass)(**entity**: `Any`)
- [get_inertia](#Body2D.get_inertia)(**entity**: `Any`)
- [set_type](#Body2D.set_type+2)(**entity**: `Any`, **type**: `Any`)
- [get_type](#Body2D.get_type)(**entity**: `Any`)
- [set_sleeping_allowed](#Body2D.set_sleeping_allowed+2)(**entity**: `Any`, **allowed**: `Any`)
- [get_sleeping_allowed](#Body2D.get_sleeping_allowed)(**entity**: `Any`)
- [set_sleeping](#Body2D.set_sleeping+2)(**entity**: `Any`, **sleep_state**: `Any`)
- [get_sleeping](#Body2D.get_sleeping)(**entity**: `Any`)
- [set_active](#Body2D.set_active+2)(**entity**: `Any`, **active_state**: `Any`)
- [get_active](#Body2D.get_active)(**entity**: `Any`)
- [set_velocity_linear](#Body2D.set_velocity_linear+3)(**entity**: `Any`, **x**: `Any`, **y**: `Any`)
- [get_velocity_linear](#Body2D.get_velocity_linear)(**entity**: `Any`)
- [set_velocity_angular](#Body2D.set_velocity_angular+2)(**entity**: `Any`, **angle**: `Any`)
- [get_velocity_angular](#Body2D.get_velocity_angular)(**entity**: `Any`)
- [set_damping_linear](#Body2D.set_damping_linear+2)(**entity**: `Any`, **linear_damping**: `Any`)
- [get_damping_linear](#Body2D.get_damping_linear)(**entity**: `Any`)
- [set_damping_angular](#Body2D.set_damping_angular+2)(**entity**: `Any`, **angular_damping**: `Any`)
- [get_damping_angular](#Body2D.get_damping_angular)(**entity**: `Any`)
- [apply_force](#Body2D.apply_force+6)(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **x**: `Any`, **y**: `Any`, **force_awake**: `Any`)
- [apply_force](#Body2D.apply_force+5)(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **x**: `Any`, **y**: `Any`)
- [apply_force](#Body2D.apply_force+4)(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_awake**: `Any`)
- [apply_force](#Body2D.apply_force+3)(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`)
- [apply_torque](#Body2D.apply_torque+3)(**entity**: `Any`, **torque**: `Any`, **force_awake**: `Any`)
- [apply_torque](#Body2D.apply_torque+2)(**entity**: `Any`, **torque**: `Any`)
- [apply_impulse_linear](#Body2D.apply_impulse_linear+6)(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **x**: `Any`, **y**: `Any`, **force_awake**: `Any`)
- [apply_impulse_linear](#Body2D.apply_impulse_linear+5)(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **x**: `Any`, **y**: `Any`)
- [apply_impulse_angular](#Body2D.apply_impulse_angular+3)(**entity**: `Any`, **impulse**: `Any`, **force_awake**: `Any`)
- [apply_impulse_angular](#Body2D.apply_impulse_angular+2)(**entity**: `Any`, **impulse**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Body2D" signature="create(entity : Any)"></endpoint>
<signature id="Body2D.create">Body2D.create(**entity**: `Any`)
<a class="headerlink" href="#Body2D.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="has(entity : Any)"></endpoint>
<signature id="Body2D.has">Body2D.has(**entity**: `Any`)
<a class="headerlink" href="#Body2D.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="create_collider_box(entity : Any, center : Any, size : Any, angle : Any)"></endpoint>
<signature id="Body2D.create_collider_box+4">Body2D.create_collider_box(**entity**: `Any`, **center**: `Any`, **size**: `Any`, **angle**: `Any`)
<a class="headerlink" href="#Body2D.create_collider_box+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="create_collider_circle(entity : Any, center : Any, radius : Any)"></endpoint>
<signature id="Body2D.create_collider_circle+3">Body2D.create_collider_circle(**entity**: `Any`, **center**: `Any`, **radius**: `Any`)
<a class="headerlink" href="#Body2D.create_collider_circle+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="get_center(entity : Any)"></endpoint>
<signature id="Body2D.get_center">Body2D.get_center(**entity**: `Any`)
<a class="headerlink" href="#Body2D.get_center" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="get_mass(entity : Any)"></endpoint>
<signature id="Body2D.get_mass">Body2D.get_mass(**entity**: `Any`)
<a class="headerlink" href="#Body2D.get_mass" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="get_inertia(entity : Any)"></endpoint>
<signature id="Body2D.get_inertia">Body2D.get_inertia(**entity**: `Any`)
<a class="headerlink" href="#Body2D.get_inertia" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="set_type(entity : Any, type : Any)"></endpoint>
<signature id="Body2D.set_type+2">Body2D.set_type(**entity**: `Any`, **type**: `Any`)
<a class="headerlink" href="#Body2D.set_type+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="get_type(entity : Any)"></endpoint>
<signature id="Body2D.get_type">Body2D.get_type(**entity**: `Any`)
<a class="headerlink" href="#Body2D.get_type" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="set_sleeping_allowed(entity : Any, allowed : Any)"></endpoint>
<signature id="Body2D.set_sleeping_allowed+2">Body2D.set_sleeping_allowed(**entity**: `Any`, **allowed**: `Any`)
<a class="headerlink" href="#Body2D.set_sleeping_allowed+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="get_sleeping_allowed(entity : Any)"></endpoint>
<signature id="Body2D.get_sleeping_allowed">Body2D.get_sleeping_allowed(**entity**: `Any`)
<a class="headerlink" href="#Body2D.get_sleeping_allowed" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="set_sleeping(entity : Any, sleep_state : Any)"></endpoint>
<signature id="Body2D.set_sleeping+2">Body2D.set_sleeping(**entity**: `Any`, **sleep_state**: `Any`)
<a class="headerlink" href="#Body2D.set_sleeping+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="get_sleeping(entity : Any)"></endpoint>
<signature id="Body2D.get_sleeping">Body2D.get_sleeping(**entity**: `Any`)
<a class="headerlink" href="#Body2D.get_sleeping" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="set_active(entity : Any, active_state : Any)"></endpoint>
<signature id="Body2D.set_active+2">Body2D.set_active(**entity**: `Any`, **active_state**: `Any`)
<a class="headerlink" href="#Body2D.set_active+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="get_active(entity : Any)"></endpoint>
<signature id="Body2D.get_active">Body2D.get_active(**entity**: `Any`)
<a class="headerlink" href="#Body2D.get_active" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="set_velocity_linear(entity : Any, x : Any, y : Any)"></endpoint>
<signature id="Body2D.set_velocity_linear+3">Body2D.set_velocity_linear(**entity**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Body2D.set_velocity_linear+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="get_velocity_linear(entity : Any)"></endpoint>
<signature id="Body2D.get_velocity_linear">Body2D.get_velocity_linear(**entity**: `Any`)
<a class="headerlink" href="#Body2D.get_velocity_linear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="set_velocity_angular(entity : Any, angle : Any)"></endpoint>
<signature id="Body2D.set_velocity_angular+2">Body2D.set_velocity_angular(**entity**: `Any`, **angle**: `Any`)
<a class="headerlink" href="#Body2D.set_velocity_angular+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="get_velocity_angular(entity : Any)"></endpoint>
<signature id="Body2D.get_velocity_angular">Body2D.get_velocity_angular(**entity**: `Any`)
<a class="headerlink" href="#Body2D.get_velocity_angular" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="set_damping_linear(entity : Any, linear_damping : Any)"></endpoint>
<signature id="Body2D.set_damping_linear+2">Body2D.set_damping_linear(**entity**: `Any`, **linear_damping**: `Any`)
<a class="headerlink" href="#Body2D.set_damping_linear+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="get_damping_linear(entity : Any)"></endpoint>
<signature id="Body2D.get_damping_linear">Body2D.get_damping_linear(**entity**: `Any`)
<a class="headerlink" href="#Body2D.get_damping_linear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="set_damping_angular(entity : Any, angular_damping : Any)"></endpoint>
<signature id="Body2D.set_damping_angular+2">Body2D.set_damping_angular(**entity**: `Any`, **angular_damping**: `Any`)
<a class="headerlink" href="#Body2D.set_damping_angular+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="get_damping_angular(entity : Any)"></endpoint>
<signature id="Body2D.get_damping_angular">Body2D.get_damping_angular(**entity**: `Any`)
<a class="headerlink" href="#Body2D.get_damping_angular" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="apply_force(entity : Any, force_x : Any, force_y : Any, x : Any, y : Any, force_awake : Any)"></endpoint>
<signature id="Body2D.apply_force+6">Body2D.apply_force(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **x**: `Any`, **y**: `Any`, **force_awake**: `Any`)
<a class="headerlink" href="#Body2D.apply_force+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="apply_force(entity : Any, force_x : Any, force_y : Any, x : Any, y : Any)"></endpoint>
<signature id="Body2D.apply_force+5">Body2D.apply_force(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Body2D.apply_force+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="apply_force(entity : Any, force_x : Any, force_y : Any, force_awake : Any)"></endpoint>
<signature id="Body2D.apply_force+4">Body2D.apply_force(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_awake**: `Any`)
<a class="headerlink" href="#Body2D.apply_force+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="apply_force(entity : Any, force_x : Any, force_y : Any)"></endpoint>
<signature id="Body2D.apply_force+3">Body2D.apply_force(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`)
<a class="headerlink" href="#Body2D.apply_force+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="apply_torque(entity : Any, torque : Any, force_awake : Any)"></endpoint>
<signature id="Body2D.apply_torque+3">Body2D.apply_torque(**entity**: `Any`, **torque**: `Any`, **force_awake**: `Any`)
<a class="headerlink" href="#Body2D.apply_torque+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="apply_torque(entity : Any, torque : Any)"></endpoint>
<signature id="Body2D.apply_torque+2">Body2D.apply_torque(**entity**: `Any`, **torque**: `Any`)
<a class="headerlink" href="#Body2D.apply_torque+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="apply_impulse_linear(entity : Any, impulse_x : Any, impulse_y : Any, x : Any, y : Any, force_awake : Any)"></endpoint>
<signature id="Body2D.apply_impulse_linear+6">Body2D.apply_impulse_linear(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **x**: `Any`, **y**: `Any`, **force_awake**: `Any`)
<a class="headerlink" href="#Body2D.apply_impulse_linear+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="apply_impulse_linear(entity : Any, impulse_x : Any, impulse_y : Any, x : Any, y : Any)"></endpoint>
<signature id="Body2D.apply_impulse_linear+5">Body2D.apply_impulse_linear(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Body2D.apply_impulse_linear+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="apply_impulse_angular(entity : Any, impulse : Any, force_awake : Any)"></endpoint>
<signature id="Body2D.apply_impulse_angular+3">Body2D.apply_impulse_angular(**entity**: `Any`, **impulse**: `Any`, **force_awake**: `Any`)
<a class="headerlink" href="#Body2D.apply_impulse_angular+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body2D" signature="apply_impulse_angular(entity : Any, impulse : Any)"></endpoint>
<signature id="Body2D.apply_impulse_angular+2">Body2D.apply_impulse_angular(**entity**: `Any`, **impulse**: `Any`)
<a class="headerlink" href="#Body2D.apply_impulse_angular+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Body3D
`:::js import "luxe: world" for Body3D`
> no docs found

- [create](#Body3D.create)(**entity**: `Any`)
- [destroy](#Body3D.destroy)(**entity**: `Any`)
- [has](#Body3D.has)(**entity**: `Any`)
- [create_heightfield](#Body3D.create_heightfield+2)(**entity**: `Any`, **image**: `Any`)
- [create_collider_box](#Body3D.create_collider_box+5)(**entity**: `Any`, **center**: `Any`, **size**: `Any`, **euler**: `Any`, **physics_asset**: `Any`)
- [create_collider_box](#Body3D.create_collider_box+4)(**entity**: `Any`, **center**: `Any`, **size**: `Any`, **euler**: `Any`)
- [create_collider_sphere](#Body3D.create_collider_sphere+4)(**entity**: `Any`, **center**: `Any`, **radius**: `Any`, **physics_asset**: `Any`)
- [create_collider_sphere](#Body3D.create_collider_sphere+3)(**entity**: `Any`, **center**: `Any`, **radius**: `Any`)
- [create_collider_cylinder](#Body3D.create_collider_cylinder+4)(**entity**: `Any`, **center**: `Any`, **size**: `Any`, **physics_asset**: `Any`)
- [create_collider_cylinder](#Body3D.create_collider_cylinder+3)(**entity**: `Any`, **center**: `Any`, **size**: `Any`)
- [create_collider_capsule](#Body3D.create_collider_capsule+5)(**entity**: `Any`, **center**: `Any`, **radius**: `Any`, **height**: `Any`, **physics_asset**: `Any`)
- [create_collider_capsule](#Body3D.create_collider_capsule+4)(**entity**: `Any`, **center**: `Any`, **radius**: `Any`, **height**: `Any`)
- [create_collider_mesh](#Body3D.create_collider_mesh+7)(**entity**: `Any`, **center**: `Any`, **euler**: `Any`, **collider_type**: `MeshColliderType`, **mesh_asset**: `Any`, **mesh_level**: `Any`, **physics_asset**: `Any`)
- [create_collider_mesh](#Body3D.create_collider_mesh+6)(**entity**: `Any`, **center**: `Any`, **euler**: `Any`, **collider_type**: `MeshColliderType`, **mesh_asset**: `Any`, **mesh_level**: `Any`)
- [get_center](#Body3D.get_center)(**entity**: `Any`)
- [get_mass](#Body3D.get_mass)(**entity**: `Any`)
- [get_inertia](#Body3D.get_inertia)(**entity**: `Any`)
- [set_physics_asset](#Body3D.set_physics_asset+2)(**entity**: `Any`, **physics_asset**: `Any`)
- [on](#Body3D.on+3)(**entity**: `Any`, **type**: `BodyEvent`, **fn**: `Any`)
- [off](#Body3D.off+2)(**entity**: `Any`, **handle**: `Any`)
- [set_channel](#Body3D.set_channel+2)(**entity**: `Any`, **channel**: `Any`)
- [set_type](#Body3D.set_type+2)(**entity**: `Any`, **type**: `Any`)
- [get_type](#Body3D.get_type)(**entity**: `Any`)
- [set_sleeping_allowed](#Body3D.set_sleeping_allowed+2)(**entity**: `Any`, **allowed**: `Any`)
- [get_sleeping_allowed](#Body3D.get_sleeping_allowed)(**entity**: `Any`)
- [set_sleeping](#Body3D.set_sleeping+2)(**entity**: `Any`, **sleep_state**: `Any`)
- [get_sleeping](#Body3D.get_sleeping)(**entity**: `Any`)
- [set_active](#Body3D.set_active+2)(**entity**: `Any`, **active_state**: `Any`)
- [get_active](#Body3D.get_active)(**entity**: `Any`)
- [set_rotation_allowed](#Body3D.set_rotation_allowed+2)(**entity**: `Any`, **axis**: `Any`)
- [get_rotation_allowed](#Body3D.get_rotation_allowed)(**entity**: `Any`)
- [set_velocity_linear](#Body3D.set_velocity_linear+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [get_velocity_linear](#Body3D.get_velocity_linear)(**entity**: `Any`)
- [set_velocity_angular](#Body3D.set_velocity_angular+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [get_velocity_angular](#Body3D.get_velocity_angular)(**entity**: `Any`)
- [set_damping_linear](#Body3D.set_damping_linear+2)(**entity**: `Any`, **linear_damping**: `Any`)
- [get_damping_linear](#Body3D.get_damping_linear)(**entity**: `Any`)
- [set_damping_angular](#Body3D.set_damping_angular+2)(**entity**: `Any`, **angular_damping**: `Any`)
- [get_damping_angular](#Body3D.get_damping_angular)(**entity**: `Any`)
- [apply_force](#Body3D.apply_force+8)(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_z**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **force_awake**: `Any`)
- [apply_force](#Body3D.apply_force+7)(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_z**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [apply_force](#Body3D.apply_force+5)(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_z**: `Any`, **force_awake**: `Any`)
- [apply_force](#Body3D.apply_force+4)(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_z**: `Any`)
- [apply_torque](#Body3D.apply_torque+5)(**entity**: `Any`, **torque_x**: `Any`, **torque_y**: `Any`, **torque_z**: `Any`, **force_awake**: `Any`)
- [apply_torque](#Body3D.apply_torque+4)(**entity**: `Any`, **torque_x**: `Any`, **torque_y**: `Any`, **torque_z**: `Any`)
- [apply_impulse_linear](#Body3D.apply_impulse_linear+8)(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **impulse_z**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **force_awake**: `Any`)
- [apply_impulse_linear](#Body3D.apply_impulse_linear+7)(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **impulse_z**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [apply_impulse_angular](#Body3D.apply_impulse_angular+5)(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **impulse_z**: `Any`, **force_awake**: `Any`)
- [apply_impulse_angular](#Body3D.apply_impulse_angular+4)(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **impulse_z**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Body3D" signature="create(entity : Any)"></endpoint>
<signature id="Body3D.create">Body3D.create(**entity**: `Any`)
<a class="headerlink" href="#Body3D.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="destroy(entity : Any)"></endpoint>
<signature id="Body3D.destroy">Body3D.destroy(**entity**: `Any`)
<a class="headerlink" href="#Body3D.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="has(entity : Any)"></endpoint>
<signature id="Body3D.has">Body3D.has(**entity**: `Any`)
<a class="headerlink" href="#Body3D.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="create_heightfield(entity : Any, image : Any)"></endpoint>
<signature id="Body3D.create_heightfield+2">Body3D.create_heightfield(**entity**: `Any`, **image**: `Any`)
<a class="headerlink" href="#Body3D.create_heightfield+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="create_collider_box(entity : Any, center : Any, size : Any, euler : Any, physics_asset : Any)"></endpoint>
<signature id="Body3D.create_collider_box+5">Body3D.create_collider_box(**entity**: `Any`, **center**: `Any`, **size**: `Any`, **euler**: `Any`, **physics_asset**: `Any`)
<a class="headerlink" href="#Body3D.create_collider_box+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="create_collider_box(entity : Any, center : Any, size : Any, euler : Any)"></endpoint>
<signature id="Body3D.create_collider_box+4">Body3D.create_collider_box(**entity**: `Any`, **center**: `Any`, **size**: `Any`, **euler**: `Any`)
<a class="headerlink" href="#Body3D.create_collider_box+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="create_collider_sphere(entity : Any, center : Any, radius : Any, physics_asset : Any)"></endpoint>
<signature id="Body3D.create_collider_sphere+4">Body3D.create_collider_sphere(**entity**: `Any`, **center**: `Any`, **radius**: `Any`, **physics_asset**: `Any`)
<a class="headerlink" href="#Body3D.create_collider_sphere+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="create_collider_sphere(entity : Any, center : Any, radius : Any)"></endpoint>
<signature id="Body3D.create_collider_sphere+3">Body3D.create_collider_sphere(**entity**: `Any`, **center**: `Any`, **radius**: `Any`)
<a class="headerlink" href="#Body3D.create_collider_sphere+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="create_collider_cylinder(entity : Any, center : Any, size : Any, physics_asset : Any)"></endpoint>
<signature id="Body3D.create_collider_cylinder+4">Body3D.create_collider_cylinder(**entity**: `Any`, **center**: `Any`, **size**: `Any`, **physics_asset**: `Any`)
<a class="headerlink" href="#Body3D.create_collider_cylinder+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="create_collider_cylinder(entity : Any, center : Any, size : Any)"></endpoint>
<signature id="Body3D.create_collider_cylinder+3">Body3D.create_collider_cylinder(**entity**: `Any`, **center**: `Any`, **size**: `Any`)
<a class="headerlink" href="#Body3D.create_collider_cylinder+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="create_collider_capsule(entity : Any, center : Any, radius : Any, height : Any, physics_asset : Any)"></endpoint>
<signature id="Body3D.create_collider_capsule+5">Body3D.create_collider_capsule(**entity**: `Any`, **center**: `Any`, **radius**: `Any`, **height**: `Any`, **physics_asset**: `Any`)
<a class="headerlink" href="#Body3D.create_collider_capsule+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="create_collider_capsule(entity : Any, center : Any, radius : Any, height : Any)"></endpoint>
<signature id="Body3D.create_collider_capsule+4">Body3D.create_collider_capsule(**entity**: `Any`, **center**: `Any`, **radius**: `Any`, **height**: `Any`)
<a class="headerlink" href="#Body3D.create_collider_capsule+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="create_collider_mesh(entity : Any, center : Any, euler : Any, collider_type : MeshColliderType, mesh_asset : Any, mesh_level : Any, physics_asset : Any)"></endpoint>
<signature id="Body3D.create_collider_mesh+7">Body3D.create_collider_mesh(**entity**: `Any`, **center**: `Any`, **euler**: `Any`, **collider_type**: `MeshColliderType`, **mesh_asset**: `Any`, **mesh_level**: `Any`, **physics_asset**: `Any`)
<a class="headerlink" href="#Body3D.create_collider_mesh+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="create_collider_mesh(entity : Any, center : Any, euler : Any, collider_type : MeshColliderType, mesh_asset : Any, mesh_level : Any)"></endpoint>
<signature id="Body3D.create_collider_mesh+6">Body3D.create_collider_mesh(**entity**: `Any`, **center**: `Any`, **euler**: `Any`, **collider_type**: `MeshColliderType`, **mesh_asset**: `Any`, **mesh_level**: `Any`)
<a class="headerlink" href="#Body3D.create_collider_mesh+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_center(entity : Any)"></endpoint>
<signature id="Body3D.get_center">Body3D.get_center(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_center" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_mass(entity : Any)"></endpoint>
<signature id="Body3D.get_mass">Body3D.get_mass(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_mass" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_inertia(entity : Any)"></endpoint>
<signature id="Body3D.get_inertia">Body3D.get_inertia(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_inertia" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="set_physics_asset(entity : Any, physics_asset : Any)"></endpoint>
<signature id="Body3D.set_physics_asset+2">Body3D.set_physics_asset(**entity**: `Any`, **physics_asset**: `Any`)
<a class="headerlink" href="#Body3D.set_physics_asset+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="on(entity : Any, type : BodyEvent, fn : Any)"></endpoint>
<signature id="Body3D.on+3">Body3D.on(**entity**: `Any`, **type**: `BodyEvent`, **fn**: `Any`)
<a class="headerlink" href="#Body3D.on+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="off(entity : Any, handle : Any)"></endpoint>
<signature id="Body3D.off+2">Body3D.off(**entity**: `Any`, **handle**: `Any`)
<a class="headerlink" href="#Body3D.off+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="set_channel(entity : Any, channel : Any)"></endpoint>
<signature id="Body3D.set_channel+2">Body3D.set_channel(**entity**: `Any`, **channel**: `Any`)
<a class="headerlink" href="#Body3D.set_channel+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="set_type(entity : Any, type : Any)"></endpoint>
<signature id="Body3D.set_type+2">Body3D.set_type(**entity**: `Any`, **type**: `Any`)
<a class="headerlink" href="#Body3D.set_type+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_type(entity : Any)"></endpoint>
<signature id="Body3D.get_type">Body3D.get_type(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_type" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="set_sleeping_allowed(entity : Any, allowed : Any)"></endpoint>
<signature id="Body3D.set_sleeping_allowed+2">Body3D.set_sleeping_allowed(**entity**: `Any`, **allowed**: `Any`)
<a class="headerlink" href="#Body3D.set_sleeping_allowed+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_sleeping_allowed(entity : Any)"></endpoint>
<signature id="Body3D.get_sleeping_allowed">Body3D.get_sleeping_allowed(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_sleeping_allowed" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="set_sleeping(entity : Any, sleep_state : Any)"></endpoint>
<signature id="Body3D.set_sleeping+2">Body3D.set_sleeping(**entity**: `Any`, **sleep_state**: `Any`)
<a class="headerlink" href="#Body3D.set_sleeping+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_sleeping(entity : Any)"></endpoint>
<signature id="Body3D.get_sleeping">Body3D.get_sleeping(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_sleeping" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="set_active(entity : Any, active_state : Any)"></endpoint>
<signature id="Body3D.set_active+2">Body3D.set_active(**entity**: `Any`, **active_state**: `Any`)
<a class="headerlink" href="#Body3D.set_active+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_active(entity : Any)"></endpoint>
<signature id="Body3D.get_active">Body3D.get_active(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_active" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="set_rotation_allowed(entity : Any, axis : Any)"></endpoint>
<signature id="Body3D.set_rotation_allowed+2">Body3D.set_rotation_allowed(**entity**: `Any`, **axis**: `Any`)
<a class="headerlink" href="#Body3D.set_rotation_allowed+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_rotation_allowed(entity : Any)"></endpoint>
<signature id="Body3D.get_rotation_allowed">Body3D.get_rotation_allowed(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_rotation_allowed" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="set_velocity_linear(entity : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Body3D.set_velocity_linear+4">Body3D.set_velocity_linear(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Body3D.set_velocity_linear+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_velocity_linear(entity : Any)"></endpoint>
<signature id="Body3D.get_velocity_linear">Body3D.get_velocity_linear(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_velocity_linear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="set_velocity_angular(entity : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Body3D.set_velocity_angular+4">Body3D.set_velocity_angular(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Body3D.set_velocity_angular+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_velocity_angular(entity : Any)"></endpoint>
<signature id="Body3D.get_velocity_angular">Body3D.get_velocity_angular(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_velocity_angular" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="set_damping_linear(entity : Any, linear_damping : Any)"></endpoint>
<signature id="Body3D.set_damping_linear+2">Body3D.set_damping_linear(**entity**: `Any`, **linear_damping**: `Any`)
<a class="headerlink" href="#Body3D.set_damping_linear+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_damping_linear(entity : Any)"></endpoint>
<signature id="Body3D.get_damping_linear">Body3D.get_damping_linear(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_damping_linear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="set_damping_angular(entity : Any, angular_damping : Any)"></endpoint>
<signature id="Body3D.set_damping_angular+2">Body3D.set_damping_angular(**entity**: `Any`, **angular_damping**: `Any`)
<a class="headerlink" href="#Body3D.set_damping_angular+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="get_damping_angular(entity : Any)"></endpoint>
<signature id="Body3D.get_damping_angular">Body3D.get_damping_angular(**entity**: `Any`)
<a class="headerlink" href="#Body3D.get_damping_angular" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="apply_force(entity : Any, force_x : Any, force_y : Any, force_z : Any, x : Any, y : Any, z : Any, force_awake : Any)"></endpoint>
<signature id="Body3D.apply_force+8">Body3D.apply_force(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_z**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **force_awake**: `Any`)
<a class="headerlink" href="#Body3D.apply_force+8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="apply_force(entity : Any, force_x : Any, force_y : Any, force_z : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Body3D.apply_force+7">Body3D.apply_force(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_z**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Body3D.apply_force+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="apply_force(entity : Any, force_x : Any, force_y : Any, force_z : Any, force_awake : Any)"></endpoint>
<signature id="Body3D.apply_force+5">Body3D.apply_force(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_z**: `Any`, **force_awake**: `Any`)
<a class="headerlink" href="#Body3D.apply_force+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="apply_force(entity : Any, force_x : Any, force_y : Any, force_z : Any)"></endpoint>
<signature id="Body3D.apply_force+4">Body3D.apply_force(**entity**: `Any`, **force_x**: `Any`, **force_y**: `Any`, **force_z**: `Any`)
<a class="headerlink" href="#Body3D.apply_force+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="apply_torque(entity : Any, torque_x : Any, torque_y : Any, torque_z : Any, force_awake : Any)"></endpoint>
<signature id="Body3D.apply_torque+5">Body3D.apply_torque(**entity**: `Any`, **torque_x**: `Any`, **torque_y**: `Any`, **torque_z**: `Any`, **force_awake**: `Any`)
<a class="headerlink" href="#Body3D.apply_torque+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="apply_torque(entity : Any, torque_x : Any, torque_y : Any, torque_z : Any)"></endpoint>
<signature id="Body3D.apply_torque+4">Body3D.apply_torque(**entity**: `Any`, **torque_x**: `Any`, **torque_y**: `Any`, **torque_z**: `Any`)
<a class="headerlink" href="#Body3D.apply_torque+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="apply_impulse_linear(entity : Any, impulse_x : Any, impulse_y : Any, impulse_z : Any, x : Any, y : Any, z : Any, force_awake : Any)"></endpoint>
<signature id="Body3D.apply_impulse_linear+8">Body3D.apply_impulse_linear(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **impulse_z**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **force_awake**: `Any`)
<a class="headerlink" href="#Body3D.apply_impulse_linear+8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="apply_impulse_linear(entity : Any, impulse_x : Any, impulse_y : Any, impulse_z : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Body3D.apply_impulse_linear+7">Body3D.apply_impulse_linear(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **impulse_z**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Body3D.apply_impulse_linear+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="apply_impulse_angular(entity : Any, impulse_x : Any, impulse_y : Any, impulse_z : Any, force_awake : Any)"></endpoint>
<signature id="Body3D.apply_impulse_angular+5">Body3D.apply_impulse_angular(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **impulse_z**: `Any`, **force_awake**: `Any`)
<a class="headerlink" href="#Body3D.apply_impulse_angular+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Body3D" signature="apply_impulse_angular(entity : Any, impulse_x : Any, impulse_y : Any, impulse_z : Any)"></endpoint>
<signature id="Body3D.apply_impulse_angular+4">Body3D.apply_impulse_angular(**entity**: `Any`, **impulse_x**: `Any`, **impulse_y**: `Any`, **impulse_z**: `Any`)
<a class="headerlink" href="#Body3D.apply_impulse_angular+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### BodyEvent
`:::js import "luxe: world" for BodyEvent`
> no docs found

- [invalid](#BodyEvent.invalid)
- [overlap](#BodyEvent.overlap)
- [collide](#BodyEvent.collide)
- [name](#BodyEvent.name)(**value**: `Any`)
- [from_string](#BodyEvent.from_string)(**value**: `Any`)

<hr/>
<endpoint module="luxe: world" class="BodyEvent" signature="invalid"></endpoint>
<signature id="BodyEvent.invalid">BodyEvent.invalid
<a class="headerlink" href="#BodyEvent.invalid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="BodyEvent" signature="overlap"></endpoint>
<signature id="BodyEvent.overlap">BodyEvent.overlap
<a class="headerlink" href="#BodyEvent.overlap" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="BodyEvent" signature="collide"></endpoint>
<signature id="BodyEvent.collide">BodyEvent.collide
<a class="headerlink" href="#BodyEvent.collide" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="BodyEvent" signature="name(value : Any)"></endpoint>
<signature id="BodyEvent.name">BodyEvent.name(**value**: `Any`)
<a class="headerlink" href="#BodyEvent.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="BodyEvent" signature="from_string(value : Any)"></endpoint>
<signature id="BodyEvent.from_string">BodyEvent.from_string(**value**: `Any`)
<a class="headerlink" href="#BodyEvent.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### BodyType
`:::js import "luxe: world" for BodyType`
> no docs found

- [static_body](#BodyType.static_body)
- [dynamic_body](#BodyType.dynamic_body)
- [kinematic_body](#BodyType.kinematic_body)
- [name](#BodyType.name)(**value**: `Any`)
- [from_string](#BodyType.from_string)(**value**: `Any`)

<hr/>
<endpoint module="luxe: world" class="BodyType" signature="static_body"></endpoint>
<signature id="BodyType.static_body">BodyType.static_body
<a class="headerlink" href="#BodyType.static_body" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="BodyType" signature="dynamic_body"></endpoint>
<signature id="BodyType.dynamic_body">BodyType.dynamic_body
<a class="headerlink" href="#BodyType.dynamic_body" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="BodyType" signature="kinematic_body"></endpoint>
<signature id="BodyType.kinematic_body">BodyType.kinematic_body
<a class="headerlink" href="#BodyType.kinematic_body" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="BodyType" signature="name(value : Any)"></endpoint>
<signature id="BodyType.name">BodyType.name(**value**: `Any`)
<a class="headerlink" href="#BodyType.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="BodyType" signature="from_string(value : Any)"></endpoint>
<signature id="BodyType.from_string">BodyType.from_string(**value**: `Any`)
<a class="headerlink" href="#BodyType.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Camera
`:::js import "luxe: world" for Camera`
> no docs found

- [create](#Camera.create)(**entity**: `Any`)
- [destroy](#Camera.destroy)(**entity**: `Any`)
- [has](#Camera.has)(**entity**: `Any`)
- [get_default](#Camera.get_default)(**world**: `Any`)
- [set_default](#Camera.set_default+2)(**world**: `Any`, **camera**: `Any`)
- [set_fov_vertical](#Camera.set_fov_vertical+2)(**entity**: `Any`, **fov_vertical**: `Any`)
- [get_fov_vertical](#Camera.get_fov_vertical)(**entity**: `Any`)
- [get_projection](#Camera.get_projection)(**entity**: `Any`)
- [get_near](#Camera.get_near)(**entity**: `Any`)
- [get_far](#Camera.get_far)(**entity**: `Any`)
- [get_aspect](#Camera.get_aspect)(**entity**: `Any`)
- [perspective](#Camera.perspective+5)(**entity**: `Any`, **fov_vertical**: `Any`, **aspect**: `Any`, **near**: `Any`, **far**: `Any`)
- [ortho](#Camera.ortho+7)(**entity**: `Any`, **left**: `Any`, **top**: `Any`, **right**: `Any`, **bottom**: `Any`, **near**: `Any`, **far**: `Any`)
- [look_at](#Camera.look_at+4)(**entity**: `Any`, **from**: `Any`, **to**: `Any`, **up**: `Any`)
- [set2D](#Camera.set2D+7)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **width**: `Any`, **height**: `Any`, **near**: `Any`, **far**: `Any`)
- [set3D](#Camera.set3D+5)(**entity**: `Any`, **fov_vertical**: `Any`, **aspect**: `Any`, **near**: `Any`, **far**: `Any`)
- [screen_point_to_world](#Camera.screen_point_to_world+3)(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`)
- [world_point_to_screen](#Camera.world_point_to_screen+4)(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`)
- [world_point_to_view](#Camera.world_point_to_view+5)(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`, **into**: `Any`)
- [world_point_to_view](#Camera.world_point_to_view+4)(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`)
- [view_point_to_world](#Camera.view_point_to_world+4)(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`)
- [world_point_to_clip](#Camera.world_point_to_clip+4)(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`)
- [clip_point_to_world](#Camera.clip_point_to_world+4)(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`)
- [get_view_matrix](#Camera.get_view_matrix+2)(**entity**: `Any`, **into_matrix**: `Any`)
- [get_projection_matrix](#Camera.get_projection_matrix+2)(**entity**: `Any`, **into_matrix**: `Any`)
- [get_view_projection_matrix](#Camera.get_view_projection_matrix+2)(**entity**: `Any`, **into_matrix**: `Any`)
- [set_view_matrix](#Camera.set_view_matrix+2)(**entity**: `Any`, **matrix**: `Any`)
- [set_projection_matrix](#Camera.set_projection_matrix+2)(**entity**: `Any`, **matrix**: `Any`)
- [cull](#Camera.cull+2)(**camera**: `Any`, **render_set**: `Any`)
- [froxelize](#Camera.froxelize+5)(**camera**: `Any`, **slices**: `Any`, **entity_info_list**: `Any`, **cluster_image**: `Any`, **items_image**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Camera" signature="create(entity : Any)"></endpoint>
<signature id="Camera.create">Camera.create(**entity**: `Any`)
<a class="headerlink" href="#Camera.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="destroy(entity : Any)"></endpoint>
<signature id="Camera.destroy">Camera.destroy(**entity**: `Any`)
<a class="headerlink" href="#Camera.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="has(entity : Any)"></endpoint>
<signature id="Camera.has">Camera.has(**entity**: `Any`)
<a class="headerlink" href="#Camera.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="get_default(world : Any)"></endpoint>
<signature id="Camera.get_default">Camera.get_default(**world**: `Any`)
<a class="headerlink" href="#Camera.get_default" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="set_default(world : Any, camera : Any)"></endpoint>
<signature id="Camera.set_default+2">Camera.set_default(**world**: `Any`, **camera**: `Any`)
<a class="headerlink" href="#Camera.set_default+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="set_fov_vertical(entity : Any, fov_vertical : Any)"></endpoint>
<signature id="Camera.set_fov_vertical+2">Camera.set_fov_vertical(**entity**: `Any`, **fov_vertical**: `Any`)
<a class="headerlink" href="#Camera.set_fov_vertical+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="get_fov_vertical(entity : Any)"></endpoint>
<signature id="Camera.get_fov_vertical">Camera.get_fov_vertical(**entity**: `Any`)
<a class="headerlink" href="#Camera.get_fov_vertical" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="get_projection(entity : Any)"></endpoint>
<signature id="Camera.get_projection">Camera.get_projection(**entity**: `Any`)
<a class="headerlink" href="#Camera.get_projection" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="get_near(entity : Any)"></endpoint>
<signature id="Camera.get_near">Camera.get_near(**entity**: `Any`)
<a class="headerlink" href="#Camera.get_near" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="get_far(entity : Any)"></endpoint>
<signature id="Camera.get_far">Camera.get_far(**entity**: `Any`)
<a class="headerlink" href="#Camera.get_far" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="get_aspect(entity : Any)"></endpoint>
<signature id="Camera.get_aspect">Camera.get_aspect(**entity**: `Any`)
<a class="headerlink" href="#Camera.get_aspect" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="perspective(entity : Any, fov_vertical : Any, aspect : Any, near : Any, far : Any)"></endpoint>
<signature id="Camera.perspective+5">Camera.perspective(**entity**: `Any`, **fov_vertical**: `Any`, **aspect**: `Any`, **near**: `Any`, **far**: `Any`)
<a class="headerlink" href="#Camera.perspective+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="ortho(entity : Any, left : Any, top : Any, right : Any, bottom : Any, near : Any, far : Any)"></endpoint>
<signature id="Camera.ortho+7">Camera.ortho(**entity**: `Any`, **left**: `Any`, **top**: `Any`, **right**: `Any`, **bottom**: `Any`, **near**: `Any`, **far**: `Any`)
<a class="headerlink" href="#Camera.ortho+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="look_at(entity : Any, from : Any, to : Any, up : Any)"></endpoint>
<signature id="Camera.look_at+4">Camera.look_at(**entity**: `Any`, **from**: `Any`, **to**: `Any`, **up**: `Any`)
<a class="headerlink" href="#Camera.look_at+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="set2D(entity : Any, x : Any, y : Any, width : Any, height : Any, near : Any, far : Any)"></endpoint>
<signature id="Camera.set2D+7">Camera.set2D(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **width**: `Any`, **height**: `Any`, **near**: `Any`, **far**: `Any`)
<a class="headerlink" href="#Camera.set2D+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="set3D(entity : Any, fov_vertical : Any, aspect : Any, near : Any, far : Any)"></endpoint>
<signature id="Camera.set3D+5">Camera.set3D(**entity**: `Any`, **fov_vertical**: `Any`, **aspect**: `Any`, **near**: `Any`, **far**: `Any`)
<a class="headerlink" href="#Camera.set3D+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="screen_point_to_world(entity : Any, pos_x : Any, pos_y : Any)"></endpoint>
<signature id="Camera.screen_point_to_world+3">Camera.screen_point_to_world(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`)
<a class="headerlink" href="#Camera.screen_point_to_world+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="world_point_to_screen(entity : Any, pos_x : Any, pos_y : Any, pos_z : Any)"></endpoint>
<signature id="Camera.world_point_to_screen+4">Camera.world_point_to_screen(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`)
<a class="headerlink" href="#Camera.world_point_to_screen+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="world_point_to_view(entity : Any, pos_x : Any, pos_y : Any, pos_z : Any, into : Any)"></endpoint>
<signature id="Camera.world_point_to_view+5">Camera.world_point_to_view(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`, **into**: `Any`)
<a class="headerlink" href="#Camera.world_point_to_view+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="world_point_to_view(entity : Any, pos_x : Any, pos_y : Any, pos_z : Any)"></endpoint>
<signature id="Camera.world_point_to_view+4">Camera.world_point_to_view(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`)
<a class="headerlink" href="#Camera.world_point_to_view+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="view_point_to_world(entity : Any, pos_x : Any, pos_y : Any, pos_z : Any)"></endpoint>
<signature id="Camera.view_point_to_world+4">Camera.view_point_to_world(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`)
<a class="headerlink" href="#Camera.view_point_to_world+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="world_point_to_clip(entity : Any, pos_x : Any, pos_y : Any, pos_z : Any)"></endpoint>
<signature id="Camera.world_point_to_clip+4">Camera.world_point_to_clip(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`)
<a class="headerlink" href="#Camera.world_point_to_clip+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="clip_point_to_world(entity : Any, pos_x : Any, pos_y : Any, pos_z : Any)"></endpoint>
<signature id="Camera.clip_point_to_world+4">Camera.clip_point_to_world(**entity**: `Any`, **pos_x**: `Any`, **pos_y**: `Any`, **pos_z**: `Any`)
<a class="headerlink" href="#Camera.clip_point_to_world+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="get_view_matrix(entity : Any, into_matrix : Any)"></endpoint>
<signature id="Camera.get_view_matrix+2">Camera.get_view_matrix(**entity**: `Any`, **into_matrix**: `Any`)
<a class="headerlink" href="#Camera.get_view_matrix+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="get_projection_matrix(entity : Any, into_matrix : Any)"></endpoint>
<signature id="Camera.get_projection_matrix+2">Camera.get_projection_matrix(**entity**: `Any`, **into_matrix**: `Any`)
<a class="headerlink" href="#Camera.get_projection_matrix+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="get_view_projection_matrix(entity : Any, into_matrix : Any)"></endpoint>
<signature id="Camera.get_view_projection_matrix+2">Camera.get_view_projection_matrix(**entity**: `Any`, **into_matrix**: `Any`)
<a class="headerlink" href="#Camera.get_view_projection_matrix+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="set_view_matrix(entity : Any, matrix : Any)"></endpoint>
<signature id="Camera.set_view_matrix+2">Camera.set_view_matrix(**entity**: `Any`, **matrix**: `Any`)
<a class="headerlink" href="#Camera.set_view_matrix+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="set_projection_matrix(entity : Any, matrix : Any)"></endpoint>
<signature id="Camera.set_projection_matrix+2">Camera.set_projection_matrix(**entity**: `Any`, **matrix**: `Any`)
<a class="headerlink" href="#Camera.set_projection_matrix+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="cull(camera : Any, render_set : Any)"></endpoint>
<signature id="Camera.cull+2">Camera.cull(**camera**: `Any`, **render_set**: `Any`)
<a class="headerlink" href="#Camera.cull+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Camera" signature="froxelize(camera : Any, slices : Any, entity_info_list : Any, cluster_image : Any, items_image : Any)"></endpoint>
<signature id="Camera.froxelize+5">Camera.froxelize(**camera**: `Any`, **slices**: `Any`, **entity_info_list**: `Any`, **cluster_image**: `Any`, **items_image**: `Any`)
<a class="headerlink" href="#Camera.froxelize+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Clock
`:::js import "luxe: world" for Clock`
> no docs found

- [create](#Clock.create+3)(**world**: `Any`, **rate**: `Any`, **paused**: `Any`)
- [create](#Clock.create+2)(**world**: `Any`, **rate**: `Any`)
- [time](#Clock.time+2)(**world**: `Any`, **clock**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Clock" signature="create(world : Any, rate : Any, paused : Any)"></endpoint>
<signature id="Clock.create+3">Clock.create(**world**: `Any`, **rate**: `Any`, **paused**: `Any`)
<a class="headerlink" href="#Clock.create+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Clock" signature="create(world : Any, rate : Any)"></endpoint>
<signature id="Clock.create+2">Clock.create(**world**: `Any`, **rate**: `Any`)
<a class="headerlink" href="#Clock.create+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Clock" signature="time(world : Any, clock : Any)"></endpoint>
<signature id="Clock.time+2">Clock.time(**world**: `Any`, **clock**: `Any`)
<a class="headerlink" href="#Clock.time+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Entity
`:::js import "luxe: world" for Entity`
> no docs found

- [create](#Entity.create)(**world**: `World`)
- [create](#Entity.create+2)(**world**: `World`, **name**: `String`)
- [valid](#Entity.valid)(**entity**: `Entity`)
- [get_world](#Entity.get_world)(**entity**: `Any`)
- [get](#Entity.get)(**uuid**: `Any`)
- [get_named](#Entity.get_named+2)(**world**: `World`, **name**: `String`)
- [get_named_all](#Entity.get_named_all+2)(**world**: `World`, **name**: `String`)
- [get_name](#Entity.get_name)(**entity**: `Entity`)
- [set_name](#Entity.set_name+2)(**entity**: `Entity`, **name**: `String`)
- [get_uuid](#Entity.get_uuid)(**entity**: `Any`)
- [set_uuid](#Entity.set_uuid+2)(**entity**: `Any`, **uuid_string**: `Any`)
- [destroy](#Entity.destroy)(**entity**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Entity" signature="create(world : World)"></endpoint>
<signature id="Entity.create">Entity.create(**world**: `World`)
<a class="headerlink" href="#Entity.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> Creates a new `entity` in the given `world`.
> 
>   ```js
>   var player = Entity.create(app.world)
>   ```   

<endpoint module="luxe: world" class="Entity" signature="create(world : World, name : String)"></endpoint>
<signature id="Entity.create+2">Entity.create(**world**: `World`, **name**: `String`)
<a class="headerlink" href="#Entity.create+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> Creates a new `entity` in the given `world` with the specified `String` name.
> 
>   ```js
>   var player = Entity.create(app.world, "player")
>   ```   

<endpoint module="luxe: world" class="Entity" signature="valid(entity : Entity)"></endpoint>
<signature id="Entity.valid">Entity.valid(**entity**: `Entity`)
<a class="headerlink" href="#Entity.valid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Checks if the given variable references a valid `entity`.
> 
>   ```js
>   var player = Entity.get_named(app.world, "player")
>   if (Entity.valid(player)) {
>     System.print("Got the player entity!")
>   }
>   ```   

<endpoint module="luxe: world" class="Entity" signature="get_world(entity : Any)"></endpoint>
<signature id="Entity.get_world">Entity.get_world(**entity**: `Any`)
<a class="headerlink" href="#Entity.get_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Entity" signature="get(uuid : Any)"></endpoint>
<signature id="Entity.get">Entity.get(**uuid**: `Any`)
<a class="headerlink" href="#Entity.get" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Entity" signature="get_named(world : World, name : String)"></endpoint>
<signature id="Entity.get_named+2">Entity.get_named(**world**: `World`, **name**: `String`)
<a class="headerlink" href="#Entity.get_named+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Entity`
> Get the first `entity` from the given `world` with the name `name`.
> 
>   ```js
>   var player = Entity.get_named(app.world, "player")
>   ```   

<endpoint module="luxe: world" class="Entity" signature="get_named_all(world : World, name : String)"></endpoint>
<signature id="Entity.get_named_all+2">Entity.get_named_all(**world**: `World`, **name**: `String`)
<a class="headerlink" href="#Entity.get_named_all+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> Get a list of all `entities` from the given `world` with the name `name`.
> 
>   ```js
>   var ferns = Entity.get_named_all(app.world, "fern")
>   System.print("There are %(ferns.count) ferns in this forest!")
>   ```   

<endpoint module="luxe: world" class="Entity" signature="get_name(entity : Entity)"></endpoint>
<signature id="Entity.get_name">Entity.get_name(**entity**: `Entity`)
<a class="headerlink" href="#Entity.get_name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Get the name of a given `entity`
> 
>   ```js
>   System.print("Hello, my name is %(Entity.get_name(traveler))!")
>   // prints "Hello, my name is Frances!"
>   ```   

<endpoint module="luxe: world" class="Entity" signature="set_name(entity : Entity, name : String)"></endpoint>
<signature id="Entity.set_name+2">Entity.set_name(**entity**: `Entity`, **name**: `String`)
<a class="headerlink" href="#Entity.set_name+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Set the name of a given `entity`
> 
>   ```js
>   Entity.set_name(traveler, "Franny")
>   System.print("But you can just call me %(Entity.get_name(traveler))!")
>   // prints "But you can just call me Franny!"
>   ```   

<endpoint module="luxe: world" class="Entity" signature="get_uuid(entity : Any)"></endpoint>
<signature id="Entity.get_uuid">Entity.get_uuid(**entity**: `Any`)
<a class="headerlink" href="#Entity.get_uuid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Entity" signature="set_uuid(entity : Any, uuid_string : Any)"></endpoint>
<signature id="Entity.set_uuid+2">Entity.set_uuid(**entity**: `Any`, **uuid_string**: `Any`)
<a class="headerlink" href="#Entity.set_uuid+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Entity" signature="destroy(entity : Any)"></endpoint>
<signature id="Entity.destroy">Entity.destroy(**entity**: `Any`)
<a class="headerlink" href="#Entity.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Layer
`:::js import "luxe: world" for Layer`
> no docs found

- [create](#Layer.create+3)(**world**: `Any`, **scene**: `Any`, **layer_id**: `Any`)
- [destroy](#Layer.destroy+3)(**world**: `Any`, **scene**: `Any`, **layer_id**: `Any`)
- [exists](#Layer.exists+3)(**world**: `Any`, **scene**: `Any`, **layer_id**: `Any`)
- [get_list](#Layer.get_list+2)(**world**: `Any`, **scene**: `Any`)
- [set_id](#Layer.set_id+4)(**world**: `Any`, **scene**: `Any`, **layer_id**: `Any`, **new_layer_id**: `Any`)
- [entity_list](#Layer.entity_list+3)(**world**: `Any`, **scene**: `Any`, **layer_id**: `Any`)
- [entity_set](#Layer.entity_set+3)(**world**: `Any`, **scene**: `Any`, **layer_id**: `Any`)
- [entity_add](#Layer.entity_add+4)(**world**: `Any`, **scene**: `Any`, **layer_id**: `Any`, **entity**: `Any`)
- [entity_remove](#Layer.entity_remove+4)(**world**: `Any`, **scene**: `Any`, **layer_id**: `Any`, **entity**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Layer" signature="create(world : Any, scene : Any, layer_id : Any)"></endpoint>
<signature id="Layer.create+3">Layer.create(**world**: `Any`, **scene**: `Any`, **layer_id**: `Any`)
<a class="headerlink" href="#Layer.create+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Layer" signature="destroy(world : Any, scene : Any, layer_id : Any)"></endpoint>
<signature id="Layer.destroy+3">Layer.destroy(**world**: `Any`, **scene**: `Any`, **layer_id**: `Any`)
<a class="headerlink" href="#Layer.destroy+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Layer" signature="exists(world : Any, scene : Any, layer_id : Any)"></endpoint>
<signature id="Layer.exists+3">Layer.exists(**world**: `Any`, **scene**: `Any`, **layer_id**: `Any`)
<a class="headerlink" href="#Layer.exists+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Layer" signature="get_list(world : Any, scene : Any)"></endpoint>
<signature id="Layer.get_list+2">Layer.get_list(**world**: `Any`, **scene**: `Any`)
<a class="headerlink" href="#Layer.get_list+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Layer" signature="set_id(world : Any, scene : Any, layer_id : Any, new_layer_id : Any)"></endpoint>
<signature id="Layer.set_id+4">Layer.set_id(**world**: `Any`, **scene**: `Any`, **layer_id**: `Any`, **new_layer_id**: `Any`)
<a class="headerlink" href="#Layer.set_id+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Layer" signature="entity_list(world : Any, scene : Any, layer_id : Any)"></endpoint>
<signature id="Layer.entity_list+3">Layer.entity_list(**world**: `Any`, **scene**: `Any`, **layer_id**: `Any`)
<a class="headerlink" href="#Layer.entity_list+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Layer" signature="entity_set(world : Any, scene : Any, layer_id : Any)"></endpoint>
<signature id="Layer.entity_set+3">Layer.entity_set(**world**: `Any`, **scene**: `Any`, **layer_id**: `Any`)
<a class="headerlink" href="#Layer.entity_set+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Layer" signature="entity_add(world : Any, scene : Any, layer_id : Any, entity : Any)"></endpoint>
<signature id="Layer.entity_add+4">Layer.entity_add(**world**: `Any`, **scene**: `Any`, **layer_id**: `Any`, **entity**: `Any`)
<a class="headerlink" href="#Layer.entity_add+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Layer" signature="entity_remove(world : Any, scene : Any, layer_id : Any, entity : Any)"></endpoint>
<signature id="Layer.entity_remove+4">Layer.entity_remove(**world**: `Any`, **scene**: `Any`, **layer_id**: `Any`, **entity**: `Any`)
<a class="headerlink" href="#Layer.entity_remove+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Mesh
`:::js import "luxe: world" for Mesh`
> no docs found

- [create](#Mesh.create)(**entity**: `Any`)
- [create](#Mesh.create+3)(**entity**: `Any`, **material**: `Any`, **mesh_lx**: `Any`)
- [destroy](#Mesh.destroy)(**entity**: `Any`)
- [has](#Mesh.has)(**entity**: `Any`)
- [clear](#Mesh.clear)(**entity**: `Any`)
- [level_get_element_count](#Mesh.level_get_element_count+2)(**entity**: `Any`, **level**: `Any`)
- [level_get_count](#Mesh.level_get_count)(**entity**: `Any`)
- [level_set_active](#Mesh.level_set_active+3)(**entity**: `Any`, **level**: `Any`, **disable_current**: `Any`)
- [level_get_active](#Mesh.level_get_active)(**entity**: `Any`)
- [level_set_enabled](#Mesh.level_set_enabled+3)(**entity**: `Any`, **level**: `Any`, **state**: `Any`)
- [level_get_enabled](#Mesh.level_get_enabled+2)(**entity**: `Any`, **level**: `Any`)
- [set_asset](#Mesh.set_asset+2)(**entity**: `Any`, **asset_id**: `Any`)
- [get_source_id](#Mesh.get_source_id)(**entity**: `Any`)
- [get_default_material](#Mesh.get_default_material)(**entity**: `Any`)
- [set_default_material](#Mesh.set_default_material+2)(**entity**: `Any`, **material**: `Any`)
- [get_geometry](#Mesh.get_geometry+3)(**entity**: `Any`, **level**: `Any`, **element**: `Any`)
- [get_geometry](#Mesh.get_geometry)(**entity**: `Any`)
- [obb_intersect_ray](#Mesh.obb_intersect_ray+7)(**entity**: `Any`, **ray_x**: `Any`, **ray_y**: `Any`, **ray_z**: `Any`, **ray_dir_x**: `Any`, **ray_dir_y**: `Any`, **ray_dir_z**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Mesh" signature="create(entity : Any)"></endpoint>
<signature id="Mesh.create">Mesh.create(**entity**: `Any`)
<a class="headerlink" href="#Mesh.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Mesh" signature="create(entity : Any, material : Any, mesh_lx : Any)"></endpoint>
<signature id="Mesh.create+3">Mesh.create(**entity**: `Any`, **material**: `Any`, **mesh_lx**: `Any`)
<a class="headerlink" href="#Mesh.create+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Mesh" signature="destroy(entity : Any)"></endpoint>
<signature id="Mesh.destroy">Mesh.destroy(**entity**: `Any`)
<a class="headerlink" href="#Mesh.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Mesh" signature="has(entity : Any)"></endpoint>
<signature id="Mesh.has">Mesh.has(**entity**: `Any`)
<a class="headerlink" href="#Mesh.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Mesh" signature="clear(entity : Any)"></endpoint>
<signature id="Mesh.clear">Mesh.clear(**entity**: `Any`)
<a class="headerlink" href="#Mesh.clear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Mesh" signature="level_get_element_count(entity : Any, level : Any)"></endpoint>
<signature id="Mesh.level_get_element_count+2">Mesh.level_get_element_count(**entity**: `Any`, **level**: `Any`)
<a class="headerlink" href="#Mesh.level_get_element_count+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Mesh" signature="level_get_count(entity : Any)"></endpoint>
<signature id="Mesh.level_get_count">Mesh.level_get_count(**entity**: `Any`)
<a class="headerlink" href="#Mesh.level_get_count" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Mesh" signature="level_set_active(entity : Any, level : Any, disable_current : Any)"></endpoint>
<signature id="Mesh.level_set_active+3">Mesh.level_set_active(**entity**: `Any`, **level**: `Any`, **disable_current**: `Any`)
<a class="headerlink" href="#Mesh.level_set_active+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Mesh" signature="level_get_active(entity : Any)"></endpoint>
<signature id="Mesh.level_get_active">Mesh.level_get_active(**entity**: `Any`)
<a class="headerlink" href="#Mesh.level_get_active" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Mesh" signature="level_set_enabled(entity : Any, level : Any, state : Any)"></endpoint>
<signature id="Mesh.level_set_enabled+3">Mesh.level_set_enabled(**entity**: `Any`, **level**: `Any`, **state**: `Any`)
<a class="headerlink" href="#Mesh.level_set_enabled+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Mesh" signature="level_get_enabled(entity : Any, level : Any)"></endpoint>
<signature id="Mesh.level_get_enabled+2">Mesh.level_get_enabled(**entity**: `Any`, **level**: `Any`)
<a class="headerlink" href="#Mesh.level_get_enabled+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Mesh" signature="set_asset(entity : Any, asset_id : Any)"></endpoint>
<signature id="Mesh.set_asset+2">Mesh.set_asset(**entity**: `Any`, **asset_id**: `Any`)
<a class="headerlink" href="#Mesh.set_asset+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Mesh" signature="get_source_id(entity : Any)"></endpoint>
<signature id="Mesh.get_source_id">Mesh.get_source_id(**entity**: `Any`)
<a class="headerlink" href="#Mesh.get_source_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Mesh" signature="get_default_material(entity : Any)"></endpoint>
<signature id="Mesh.get_default_material">Mesh.get_default_material(**entity**: `Any`)
<a class="headerlink" href="#Mesh.get_default_material" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Mesh" signature="set_default_material(entity : Any, material : Any)"></endpoint>
<signature id="Mesh.set_default_material+2">Mesh.set_default_material(**entity**: `Any`, **material**: `Any`)
<a class="headerlink" href="#Mesh.set_default_material+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Mesh" signature="get_geometry(entity : Any, level : Any, element : Any)"></endpoint>
<signature id="Mesh.get_geometry+3">Mesh.get_geometry(**entity**: `Any`, **level**: `Any`, **element**: `Any`)
<a class="headerlink" href="#Mesh.get_geometry+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Mesh" signature="get_geometry(entity : Any)"></endpoint>
<signature id="Mesh.get_geometry">Mesh.get_geometry(**entity**: `Any`)
<a class="headerlink" href="#Mesh.get_geometry" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Mesh" signature="obb_intersect_ray(entity : Any, ray_x : Any, ray_y : Any, ray_z : Any, ray_dir_x : Any, ray_dir_y : Any, ray_dir_z : Any)"></endpoint>
<signature id="Mesh.obb_intersect_ray+7">Mesh.obb_intersect_ray(**entity**: `Any`, **ray_x**: `Any`, **ray_y**: `Any`, **ray_z**: `Any`, **ray_dir_x**: `Any`, **ray_dir_y**: `Any`, **ray_dir_z**: `Any`)
<a class="headerlink" href="#Mesh.obb_intersect_ray+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### MeshColliderType
`:::js import "luxe: world" for MeshColliderType`
> no docs found

- [static_only](#MeshColliderType.static_only)
- [dynamic_convex](#MeshColliderType.dynamic_convex)
- [dynamic_concave](#MeshColliderType.dynamic_concave)
- [name](#MeshColliderType.name)(**value**: `Any`)
- [from_string](#MeshColliderType.from_string)(**value**: `Any`)

<hr/>
<endpoint module="luxe: world" class="MeshColliderType" signature="static_only"></endpoint>
<signature id="MeshColliderType.static_only">MeshColliderType.static_only
<a class="headerlink" href="#MeshColliderType.static_only" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="MeshColliderType" signature="dynamic_convex"></endpoint>
<signature id="MeshColliderType.dynamic_convex">MeshColliderType.dynamic_convex
<a class="headerlink" href="#MeshColliderType.dynamic_convex" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="MeshColliderType" signature="dynamic_concave"></endpoint>
<signature id="MeshColliderType.dynamic_concave">MeshColliderType.dynamic_concave
<a class="headerlink" href="#MeshColliderType.dynamic_concave" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="MeshColliderType" signature="name(value : Any)"></endpoint>
<signature id="MeshColliderType.name">MeshColliderType.name(**value**: `Any`)
<a class="headerlink" href="#MeshColliderType.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="MeshColliderType" signature="from_string(value : Any)"></endpoint>
<signature id="MeshColliderType.from_string">MeshColliderType.from_string(**value**: `Any`)
<a class="headerlink" href="#MeshColliderType.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### ModifierSystem
`:::js import "luxe: world" for ModifierSystem`
> no docs found

- [priority](#ModifierSystem.priority)
- [persist](#ModifierSystem.persist)
- [count](#ModifierSystem.count)
- [field](#ModifierSystem.field)
- [items](#ModifierSystem.items)
- [world](#ModifierSystem.world)
- [each](#ModifierSystem.each)(**fn**: `Any`)
- [each](#ModifierSystem.each+2)(**unique**: `Any`, **fn**: `Any`)
- [find_entity](#ModifierSystem.find_entity+2)(**relative_entity**: `Any`, **uuid**: `Any`)
- [create](#ModifierSystem.create)(**entity**: `Any`)
- [destroy](#ModifierSystem.destroy)(**entity**: `Any`)
- [get](#ModifierSystem.get)(**entity**: `Any`)
- [get](#ModifierSystem.get+2)(**entity**: `Any`, **inst**: `Any`)
- [get_slot_at](#ModifierSystem.get_slot_at)(**index**: `Any`)
- [get_slot](#ModifierSystem.get_slot)(**entity**: `Any`)
- [get_entity](#ModifierSystem.get_entity)(**slot**: `Any`)
- [get_id](#ModifierSystem.get_id)(**slot**: `Any`)
- [get_id_hash](#ModifierSystem.get_id_hash)(**slot**: `Any`)
- [set_entity](#ModifierSystem.set_entity+2)(**slot**: `Any`, **entity**: `Any`)
- [editor](#ModifierSystem.editor)(**editor**: `Any`)
- [init](#ModifierSystem.init)(**world**: `Any`)
- [tick](#ModifierSystem.tick)(**delta**: `Any`)
- [destroy](#ModifierSystem.destroy)()
- [detached](#ModifierSystem.detached)()
- [attached](#ModifierSystem.attached)()
- [disable](#ModifierSystem.disable+2)(**entity**: `Any`, **instance**: `Any`)
- [attach](#ModifierSystem.attach+2)(**entity**: `Any`, **instance**: `Any`)
- [detach](#ModifierSystem.detach+2)(**entity**: `Any`, **instance**: `Any`)
- [data](#ModifierSystem.data)
- [id](#ModifierSystem.id)
- [id](#ModifierSystem.id=)=(v : Any)
- [on_init](#ModifierSystem.on_init+2)(**world**: `Any`, **data**: `Any`)
- [on_attached](#ModifierSystem.on_attached)()
- [on_detached](#ModifierSystem.on_detached)()
- [on_disabled](#ModifierSystem.on_disabled+2)(**entities**: `Any`, **state**: `Any`)
- [on_destroying](#ModifierSystem.on_destroying)(**entities**: `Any`)
- [on_destroyed](#ModifierSystem.on_destroyed)(**entities**: `Any`)
- [on_destroy](#ModifierSystem.on_destroy)()
- [on_attach_block](#ModifierSystem.on_attach_block+4)(**block**: `Any`, **block_start**: `Any`, **block_end**: `Any`, **into**: `Any`)

<hr/>
<endpoint module="luxe: world" class="ModifierSystem" signature="priority"></endpoint>
<signature id="ModifierSystem.priority">ModifierSystem.priority
<a class="headerlink" href="#ModifierSystem.priority" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="persist"></endpoint>
<signature id="ModifierSystem.persist">ModifierSystem.persist
<a class="headerlink" href="#ModifierSystem.persist" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="count"></endpoint>
<signature id="ModifierSystem.count">ModifierSystem.count
<a class="headerlink" href="#ModifierSystem.count" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="field"></endpoint>
<signature id="ModifierSystem.field">ModifierSystem.field
<a class="headerlink" href="#ModifierSystem.field" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="items"></endpoint>
<signature id="ModifierSystem.items">ModifierSystem.items
<a class="headerlink" href="#ModifierSystem.items" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="world"></endpoint>
<signature id="ModifierSystem.world">ModifierSystem.world
<a class="headerlink" href="#ModifierSystem.world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="each(fn : Any)"></endpoint>
<signature id="ModifierSystem.each">ModifierSystem.each(**fn**: `Any`)
<a class="headerlink" href="#ModifierSystem.each" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="each(unique : Any, fn : Any)"></endpoint>
<signature id="ModifierSystem.each+2">ModifierSystem.each(**unique**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#ModifierSystem.each+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="find_entity(relative_entity : Any, uuid : Any)"></endpoint>
<signature id="ModifierSystem.find_entity+2">ModifierSystem.find_entity(**relative_entity**: `Any`, **uuid**: `Any`)
<a class="headerlink" href="#ModifierSystem.find_entity+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="create(entity : Any)"></endpoint>
<signature id="ModifierSystem.create">ModifierSystem.create(**entity**: `Any`)
<a class="headerlink" href="#ModifierSystem.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="destroy(entity : Any)"></endpoint>
<signature id="ModifierSystem.destroy">ModifierSystem.destroy(**entity**: `Any`)
<a class="headerlink" href="#ModifierSystem.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="get(entity : Any)"></endpoint>
<signature id="ModifierSystem.get">ModifierSystem.get(**entity**: `Any`)
<a class="headerlink" href="#ModifierSystem.get" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="get(entity : Any, inst : Any)"></endpoint>
<signature id="ModifierSystem.get+2">ModifierSystem.get(**entity**: `Any`, **inst**: `Any`)
<a class="headerlink" href="#ModifierSystem.get+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="get_slot_at(index : Any)"></endpoint>
<signature id="ModifierSystem.get_slot_at">ModifierSystem.get_slot_at(**index**: `Any`)
<a class="headerlink" href="#ModifierSystem.get_slot_at" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="get_slot(entity : Any)"></endpoint>
<signature id="ModifierSystem.get_slot">ModifierSystem.get_slot(**entity**: `Any`)
<a class="headerlink" href="#ModifierSystem.get_slot" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="get_entity(slot : Any)"></endpoint>
<signature id="ModifierSystem.get_entity">ModifierSystem.get_entity(**slot**: `Any`)
<a class="headerlink" href="#ModifierSystem.get_entity" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="get_id(slot : Any)"></endpoint>
<signature id="ModifierSystem.get_id">ModifierSystem.get_id(**slot**: `Any`)
<a class="headerlink" href="#ModifierSystem.get_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="get_id_hash(slot : Any)"></endpoint>
<signature id="ModifierSystem.get_id_hash">ModifierSystem.get_id_hash(**slot**: `Any`)
<a class="headerlink" href="#ModifierSystem.get_id_hash" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="set_entity(slot : Any, entity : Any)"></endpoint>
<signature id="ModifierSystem.set_entity+2">ModifierSystem.set_entity(**slot**: `Any`, **entity**: `Any`)
<a class="headerlink" href="#ModifierSystem.set_entity+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="editor(editor : Any)"></endpoint>
<signature id="ModifierSystem.editor">ModifierSystem.editor(**editor**: `Any`)
<a class="headerlink" href="#ModifierSystem.editor" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="init(world : Any)"></endpoint>
<signature id="ModifierSystem.init">ModifierSystem.init(**world**: `Any`)
<a class="headerlink" href="#ModifierSystem.init" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="tick(delta : Any)"></endpoint>
<signature id="ModifierSystem.tick">ModifierSystem.tick(**delta**: `Any`)
<a class="headerlink" href="#ModifierSystem.tick" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="destroy()"></endpoint>
<signature id="ModifierSystem.destroy">ModifierSystem.destroy()
<a class="headerlink" href="#ModifierSystem.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="detached()"></endpoint>
<signature id="ModifierSystem.detached">ModifierSystem.detached()
<a class="headerlink" href="#ModifierSystem.detached" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="attached()"></endpoint>
<signature id="ModifierSystem.attached">ModifierSystem.attached()
<a class="headerlink" href="#ModifierSystem.attached" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="disable(entity : Any, instance : Any)"></endpoint>
<signature id="ModifierSystem.disable+2">ModifierSystem.disable(**entity**: `Any`, **instance**: `Any`)
<a class="headerlink" href="#ModifierSystem.disable+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="attach(entity : Any, instance : Any)"></endpoint>
<signature id="ModifierSystem.attach+2">ModifierSystem.attach(**entity**: `Any`, **instance**: `Any`)
<a class="headerlink" href="#ModifierSystem.attach+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="detach(entity : Any, instance : Any)"></endpoint>
<signature id="ModifierSystem.detach+2">ModifierSystem.detach(**entity**: `Any`, **instance**: `Any`)
<a class="headerlink" href="#ModifierSystem.detach+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="data"></endpoint>
<signature id="ModifierSystem.data">ModifierSystem.data
<a class="headerlink" href="#ModifierSystem.data" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="id"></endpoint>
<signature id="ModifierSystem.id">ModifierSystem.id
<a class="headerlink" href="#ModifierSystem.id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="id=(v : Any)"></endpoint>
<signature id="ModifierSystem.id=">ModifierSystem.id=(v : Any)
<a class="headerlink" href="#ModifierSystem.id=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="on_init(world : Any, data : Any)"></endpoint>
<signature id="ModifierSystem.on_init+2">ModifierSystem.on_init(**world**: `Any`, **data**: `Any`)
<a class="headerlink" href="#ModifierSystem.on_init+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="on_attached()"></endpoint>
<signature id="ModifierSystem.on_attached">ModifierSystem.on_attached()
<a class="headerlink" href="#ModifierSystem.on_attached" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="on_detached()"></endpoint>
<signature id="ModifierSystem.on_detached">ModifierSystem.on_detached()
<a class="headerlink" href="#ModifierSystem.on_detached" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="on_disabled(entities : Any, state : Any)"></endpoint>
<signature id="ModifierSystem.on_disabled+2">ModifierSystem.on_disabled(**entities**: `Any`, **state**: `Any`)
<a class="headerlink" href="#ModifierSystem.on_disabled+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="on_destroying(entities : Any)"></endpoint>
<signature id="ModifierSystem.on_destroying">ModifierSystem.on_destroying(**entities**: `Any`)
<a class="headerlink" href="#ModifierSystem.on_destroying" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="on_destroyed(entities : Any)"></endpoint>
<signature id="ModifierSystem.on_destroyed">ModifierSystem.on_destroyed(**entities**: `Any`)
<a class="headerlink" href="#ModifierSystem.on_destroyed" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="on_destroy()"></endpoint>
<signature id="ModifierSystem.on_destroy">ModifierSystem.on_destroy()
<a class="headerlink" href="#ModifierSystem.on_destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ModifierSystem" signature="on_attach_block(block : Any, block_start : Any, block_end : Any, into : Any)"></endpoint>
<signature id="ModifierSystem.on_attach_block+4">ModifierSystem.on_attach_block(**block**: `Any`, **block_start**: `Any`, **block_end**: `Any`, **into**: `Any`)
<a class="headerlink" href="#ModifierSystem.on_attach_block+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Modifiers
`:::js import "luxe: world" for Modifiers`
> no docs found

- [get_or_create_block](#Modifiers.get_or_create_block+3)(**world**: `Any`, **module**: `Any`, **block_id**: `Any`)
- [attach_uuid](#Modifiers.attach_uuid+3)(**module**: `Any`, **entity**: `Any`, **uuid**: `Any`)
- [detach_uuid](#Modifiers.detach_uuid+3)(**module**: `Any`, **entity**: `Any`, **uuid**: `Any`)
- [has](#Modifiers.has+2)(**module**: `Any`, **entity**: `Any`)
- [set_uuid](#Modifiers.set_uuid+3)(**module**: `Any`, **entity**: `Any`, **uuid**: `Any`)
- [get_uuid](#Modifiers.get_uuid+2)(**module**: `Any`, **entity**: `Any`)
- [get_attached](#Modifiers.get_attached)(**entity**: `Any`)
- [get_attached_types](#Modifiers.get_attached_types)(**entity**: `Any`)
- [get_entities](#Modifiers.get_entities)(**module**: `Any`)
- [get_instances](#Modifiers.get_instances)(**module**: `Any`)
- [get_module](#Modifiers.get_module)(**uuid**: `Any`)
- [get_entity](#Modifiers.get_entity)(**uuid**: `Any`)
- [has_system_in_world](#Modifiers.has_system_in_world+2)(**module**: `Any`, **world**: `Any`)
- [get_system_in_world](#Modifiers.get_system_in_world+2)(**module**: `Any`, **world**: `Any`)
- [get](#Modifiers.get+2)(**module**: `Any`, **entity**: `Any`)
- [get_system](#Modifiers.get_system+2)(**module**: `Any`, **entity**: `Any`)
- [create](#Modifiers.create+2)(**module**: `Any`, **entity**: `Any`)
- [destroy](#Modifiers.destroy+2)(**module**: `Any`, **entity**: `Any`)
- [init](#Modifiers.init+3)(**world**: `Any`, **modifier**: `Any`, **block**: `Any`)
- [get_asset_compiler](#Modifiers.get_asset_compiler)(**type**: `Any`)
- [get_compiler_for_input](#Modifiers.get_compiler_for_input)(**modifier_id**: `Any`)
- [get_data_block_type](#Modifiers.get_data_block_type)(**modifier_id**: `Any`)
- [get_input_block_type](#Modifiers.get_input_block_type)(**modifier_id**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Modifiers" signature="get_or_create_block(world : Any, module : Any, block_id : Any)"></endpoint>
<signature id="Modifiers.get_or_create_block+3">Modifiers.get_or_create_block(**world**: `Any`, **module**: `Any`, **block_id**: `Any`)
<a class="headerlink" href="#Modifiers.get_or_create_block+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="attach_uuid(module : Any, entity : Any, uuid : Any)"></endpoint>
<signature id="Modifiers.attach_uuid+3">Modifiers.attach_uuid(**module**: `Any`, **entity**: `Any`, **uuid**: `Any`)
<a class="headerlink" href="#Modifiers.attach_uuid+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="detach_uuid(module : Any, entity : Any, uuid : Any)"></endpoint>
<signature id="Modifiers.detach_uuid+3">Modifiers.detach_uuid(**module**: `Any`, **entity**: `Any`, **uuid**: `Any`)
<a class="headerlink" href="#Modifiers.detach_uuid+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="has(module : Any, entity : Any)"></endpoint>
<signature id="Modifiers.has+2">Modifiers.has(**module**: `Any`, **entity**: `Any`)
<a class="headerlink" href="#Modifiers.has+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="set_uuid(module : Any, entity : Any, uuid : Any)"></endpoint>
<signature id="Modifiers.set_uuid+3">Modifiers.set_uuid(**module**: `Any`, **entity**: `Any`, **uuid**: `Any`)
<a class="headerlink" href="#Modifiers.set_uuid+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_uuid(module : Any, entity : Any)"></endpoint>
<signature id="Modifiers.get_uuid+2">Modifiers.get_uuid(**module**: `Any`, **entity**: `Any`)
<a class="headerlink" href="#Modifiers.get_uuid+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_attached(entity : Any)"></endpoint>
<signature id="Modifiers.get_attached">Modifiers.get_attached(**entity**: `Any`)
<a class="headerlink" href="#Modifiers.get_attached" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_attached_types(entity : Any)"></endpoint>
<signature id="Modifiers.get_attached_types">Modifiers.get_attached_types(**entity**: `Any`)
<a class="headerlink" href="#Modifiers.get_attached_types" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_entities(module : Any)"></endpoint>
<signature id="Modifiers.get_entities">Modifiers.get_entities(**module**: `Any`)
<a class="headerlink" href="#Modifiers.get_entities" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_instances(module : Any)"></endpoint>
<signature id="Modifiers.get_instances">Modifiers.get_instances(**module**: `Any`)
<a class="headerlink" href="#Modifiers.get_instances" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_module(uuid : Any)"></endpoint>
<signature id="Modifiers.get_module">Modifiers.get_module(**uuid**: `Any`)
<a class="headerlink" href="#Modifiers.get_module" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_entity(uuid : Any)"></endpoint>
<signature id="Modifiers.get_entity">Modifiers.get_entity(**uuid**: `Any`)
<a class="headerlink" href="#Modifiers.get_entity" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="has_system_in_world(module : Any, world : Any)"></endpoint>
<signature id="Modifiers.has_system_in_world+2">Modifiers.has_system_in_world(**module**: `Any`, **world**: `Any`)
<a class="headerlink" href="#Modifiers.has_system_in_world+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_system_in_world(module : Any, world : Any)"></endpoint>
<signature id="Modifiers.get_system_in_world+2">Modifiers.get_system_in_world(**module**: `Any`, **world**: `Any`)
<a class="headerlink" href="#Modifiers.get_system_in_world+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get(module : Any, entity : Any)"></endpoint>
<signature id="Modifiers.get+2">Modifiers.get(**module**: `Any`, **entity**: `Any`)
<a class="headerlink" href="#Modifiers.get+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_system(module : Any, entity : Any)"></endpoint>
<signature id="Modifiers.get_system+2">Modifiers.get_system(**module**: `Any`, **entity**: `Any`)
<a class="headerlink" href="#Modifiers.get_system+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="create(module : Any, entity : Any)"></endpoint>
<signature id="Modifiers.create+2">Modifiers.create(**module**: `Any`, **entity**: `Any`)
<a class="headerlink" href="#Modifiers.create+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="destroy(module : Any, entity : Any)"></endpoint>
<signature id="Modifiers.destroy+2">Modifiers.destroy(**module**: `Any`, **entity**: `Any`)
<a class="headerlink" href="#Modifiers.destroy+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="init(world : Any, modifier : Any, block : Any)"></endpoint>
<signature id="Modifiers.init+3">Modifiers.init(**world**: `Any`, **modifier**: `Any`, **block**: `Any`)
<a class="headerlink" href="#Modifiers.init+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_asset_compiler(type : Any)"></endpoint>
<signature id="Modifiers.get_asset_compiler">Modifiers.get_asset_compiler(**type**: `Any`)
<a class="headerlink" href="#Modifiers.get_asset_compiler" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_compiler_for_input(modifier_id : Any)"></endpoint>
<signature id="Modifiers.get_compiler_for_input">Modifiers.get_compiler_for_input(**modifier_id**: `Any`)
<a class="headerlink" href="#Modifiers.get_compiler_for_input" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_data_block_type(modifier_id : Any)"></endpoint>
<signature id="Modifiers.get_data_block_type">Modifiers.get_data_block_type(**modifier_id**: `Any`)
<a class="headerlink" href="#Modifiers.get_data_block_type" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Modifiers" signature="get_input_block_type(modifier_id : Any)"></endpoint>
<signature id="Modifiers.get_input_block_type">Modifiers.get_input_block_type(**modifier_id**: `Any`)
<a class="headerlink" href="#Modifiers.get_input_block_type" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Overlap
`:::js import "luxe: world" for Overlap`
> no docs found

- [none](#Overlap.none)
- [begin](#Overlap.begin)
- [end](#Overlap.end)
- [active](#Overlap.active)
- [name](#Overlap.name)(**value**: `Any`)
- [from_string](#Overlap.from_string)(**value**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Overlap" signature="none"></endpoint>
<signature id="Overlap.none">Overlap.none
<a class="headerlink" href="#Overlap.none" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Overlap" signature="begin"></endpoint>
<signature id="Overlap.begin">Overlap.begin
<a class="headerlink" href="#Overlap.begin" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Overlap" signature="end"></endpoint>
<signature id="Overlap.end">Overlap.end
<a class="headerlink" href="#Overlap.end" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Overlap" signature="active"></endpoint>
<signature id="Overlap.active">Overlap.active
<a class="headerlink" href="#Overlap.active" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Overlap" signature="name(value : Any)"></endpoint>
<signature id="Overlap.name">Overlap.name(**value**: `Any`)
<a class="headerlink" href="#Overlap.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Overlap" signature="from_string(value : Any)"></endpoint>
<signature id="Overlap.from_string">Overlap.from_string(**value**: `Any`)
<a class="headerlink" href="#Overlap.from_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Physics2D
`:::js import "luxe: world" for Physics2D`
> no docs found

- [set_gravity](#Physics2D.set_gravity+3)(**world**: `Any`, **x**: `Any`, **y**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Physics2D" signature="set_gravity(world : Any, x : Any, y : Any)"></endpoint>
<signature id="Physics2D.set_gravity+3">Physics2D.set_gravity(**world**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Physics2D.set_gravity+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Physics3D
`:::js import "luxe: world" for Physics3D`
> no docs found

- [set_debug_draw](#Physics3D.set_debug_draw+2)(**world**: `Any`, **state**: `Any`)
- [set_gravity](#Physics3D.set_gravity+4)(**world**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [cast_ray](#Physics3D.cast_ray+3)(**world**: `Any`, **from**: `Any`, **to**: `Any`)
- [cast_shape](#Physics3D.cast_shape+3)(**entity**: `Any`, **from**: `Any`, **to**: `Any`)
- [query_sphere](#Physics3D.query_sphere+3)(**world**: `Any`, **center**: `Any`, **radius**: `Any`)
- [query_box](#Physics3D.query_box+3)(**world**: `Any`, **center**: `Any`, **size**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Physics3D" signature="set_debug_draw(world : Any, state : Any)"></endpoint>
<signature id="Physics3D.set_debug_draw+2">Physics3D.set_debug_draw(**world**: `Any`, **state**: `Any`)
<a class="headerlink" href="#Physics3D.set_debug_draw+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Physics3D" signature="set_gravity(world : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Physics3D.set_gravity+4">Physics3D.set_gravity(**world**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Physics3D.set_gravity+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Physics3D" signature="cast_ray(world : Any, from : Any, to : Any)"></endpoint>
<signature id="Physics3D.cast_ray+3">Physics3D.cast_ray(**world**: `Any`, **from**: `Any`, **to**: `Any`)
<a class="headerlink" href="#Physics3D.cast_ray+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Physics3D" signature="cast_shape(entity : Any, from : Any, to : Any)"></endpoint>
<signature id="Physics3D.cast_shape+3">Physics3D.cast_shape(**entity**: `Any`, **from**: `Any`, **to**: `Any`)
<a class="headerlink" href="#Physics3D.cast_shape+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Physics3D" signature="query_sphere(world : Any, center : Any, radius : Any)"></endpoint>
<signature id="Physics3D.query_sphere+3">Physics3D.query_sphere(**world**: `Any`, **center**: `Any`, **radius**: `Any`)
<a class="headerlink" href="#Physics3D.query_sphere+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Physics3D" signature="query_box(world : Any, center : Any, size : Any)"></endpoint>
<signature id="Physics3D.query_box+3">Physics3D.query_box(**world**: `Any`, **center**: `Any`, **size**: `Any`)
<a class="headerlink" href="#Physics3D.query_box+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Prototype
`:::js import "luxe: world" for Prototype`
> no docs found

- [destroy](#Prototype.destroy)(**entity**: `Any`)
- [has](#Prototype.has)(**entity**: `Any`)
- [get_type](#Prototype.get_type)(**entity**: `Any`)
- [get_root](#Prototype.get_root)(**entity**: `Any`)
- [get_tree](#Prototype.get_tree)(**entity**: `Any`)
- [has_tree](#Prototype.has_tree)(**entity**: `Any`)
- [get_ref](#Prototype.get_ref+2)(**entity**: `Any`, **uuid**: `Any`)
- [get_ref_of](#Prototype.get_ref_of+2)(**entity**: `Any`, **target_entity**: `Any`)
- [get_named](#Prototype.get_named+2)(**entity**: `Any`, **name**: `Any`)
- [get_named_all](#Prototype.get_named_all+2)(**entity**: `Any`, **name**: `Any`)
- [entity_list](#Prototype.entity_list)(**entity**: `Any`)
- [refs_list](#Prototype.refs_list)(**entity**: `Any`)
- [create](#Prototype.create+3)(**world**: `Any`, **prototype_id**: `Any`, **instance_id**: `Any`)
- [create](#Prototype.create+4)(**world**: `Any`, **prototype_id**: `Any`, **instance_id**: `Any`, **position**: `Any`)
- [create](#Prototype.create+5)(**world**: `Any`, **prototype_id**: `Any`, **instance_id**: `Any`, **position**: `Any`, **rotation**: `Any`)
- [create](#Prototype.create+6)(**world**: `Any`, **prototype_id**: `Any`, **instance_id**: `Any`, **position**: `Any`, **rotation**: `Any`, **scale**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Prototype" signature="destroy(entity : Any)"></endpoint>
<signature id="Prototype.destroy">Prototype.destroy(**entity**: `Any`)
<a class="headerlink" href="#Prototype.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Prototype" signature="has(entity : Any)"></endpoint>
<signature id="Prototype.has">Prototype.has(**entity**: `Any`)
<a class="headerlink" href="#Prototype.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Prototype" signature="get_type(entity : Any)"></endpoint>
<signature id="Prototype.get_type">Prototype.get_type(**entity**: `Any`)
<a class="headerlink" href="#Prototype.get_type" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Prototype" signature="get_root(entity : Any)"></endpoint>
<signature id="Prototype.get_root">Prototype.get_root(**entity**: `Any`)
<a class="headerlink" href="#Prototype.get_root" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Prototype" signature="get_tree(entity : Any)"></endpoint>
<signature id="Prototype.get_tree">Prototype.get_tree(**entity**: `Any`)
<a class="headerlink" href="#Prototype.get_tree" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Prototype" signature="has_tree(entity : Any)"></endpoint>
<signature id="Prototype.has_tree">Prototype.has_tree(**entity**: `Any`)
<a class="headerlink" href="#Prototype.has_tree" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Prototype" signature="get_ref(entity : Any, uuid : Any)"></endpoint>
<signature id="Prototype.get_ref+2">Prototype.get_ref(**entity**: `Any`, **uuid**: `Any`)
<a class="headerlink" href="#Prototype.get_ref+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Prototype" signature="get_ref_of(entity : Any, target_entity : Any)"></endpoint>
<signature id="Prototype.get_ref_of+2">Prototype.get_ref_of(**entity**: `Any`, **target_entity**: `Any`)
<a class="headerlink" href="#Prototype.get_ref_of+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Prototype" signature="get_named(entity : Any, name : Any)"></endpoint>
<signature id="Prototype.get_named+2">Prototype.get_named(**entity**: `Any`, **name**: `Any`)
<a class="headerlink" href="#Prototype.get_named+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Prototype" signature="get_named_all(entity : Any, name : Any)"></endpoint>
<signature id="Prototype.get_named_all+2">Prototype.get_named_all(**entity**: `Any`, **name**: `Any`)
<a class="headerlink" href="#Prototype.get_named_all+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Prototype" signature="entity_list(entity : Any)"></endpoint>
<signature id="Prototype.entity_list">Prototype.entity_list(**entity**: `Any`)
<a class="headerlink" href="#Prototype.entity_list" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Prototype" signature="refs_list(entity : Any)"></endpoint>
<signature id="Prototype.refs_list">Prototype.refs_list(**entity**: `Any`)
<a class="headerlink" href="#Prototype.refs_list" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Prototype" signature="create(world : Any, prototype_id : Any, instance_id : Any)"></endpoint>
<signature id="Prototype.create+3">Prototype.create(**world**: `Any`, **prototype_id**: `Any`, **instance_id**: `Any`)
<a class="headerlink" href="#Prototype.create+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Prototype" signature="create(world : Any, prototype_id : Any, instance_id : Any, position : Any)"></endpoint>
<signature id="Prototype.create+4">Prototype.create(**world**: `Any`, **prototype_id**: `Any`, **instance_id**: `Any`, **position**: `Any`)
<a class="headerlink" href="#Prototype.create+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Prototype" signature="create(world : Any, prototype_id : Any, instance_id : Any, position : Any, rotation : Any)"></endpoint>
<signature id="Prototype.create+5">Prototype.create(**world**: `Any`, **prototype_id**: `Any`, **instance_id**: `Any`, **position**: `Any`, **rotation**: `Any`)
<a class="headerlink" href="#Prototype.create+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Prototype" signature="create(world : Any, prototype_id : Any, instance_id : Any, position : Any, rotation : Any, scale : Any)"></endpoint>
<signature id="Prototype.create+6">Prototype.create(**world**: `Any`, **prototype_id**: `Any`, **instance_id**: `Any`, **position**: `Any`, **rotation**: `Any`, **scale**: `Any`)
<a class="headerlink" href="#Prototype.create+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Scene
`:::js import "luxe: world" for Scene`
> no docs found

- [create](#Scene.create+2)(**world**: `Any`, **id**: `Any`)
- [destroy](#Scene.destroy+2)(**world**: `Any`, **id**: `Any`)
- [get_list](#Scene.get_list)(**world**: `Any`)
- [exists](#Scene.exists+2)(**world**: `Any`, **id**: `Any`)
- [entity_list](#Scene.entity_list+2)(**world**: `Any`, **id**: `Any`)
- [entity_forget](#Scene.entity_forget+3)(**world**: `Any`, **id**: `Any`, **entity**: `Any`)
- [set_id](#Scene.set_id+3)(**world**: `Any`, **id**: `Any`, **new_id**: `Any`)
- [load](#Scene.load+2)(**world**: `Any`, **id**: `Any`)
- [load_as_clone](#Scene.load_as_clone+2)(**world**: `Any`, **id**: `Any`)
- [unload](#Scene.unload+2)(**world**: `Any`, **id**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Scene" signature="create(world : Any, id : Any)"></endpoint>
<signature id="Scene.create+2">Scene.create(**world**: `Any`, **id**: `Any`)
<a class="headerlink" href="#Scene.create+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Scene" signature="destroy(world : Any, id : Any)"></endpoint>
<signature id="Scene.destroy+2">Scene.destroy(**world**: `Any`, **id**: `Any`)
<a class="headerlink" href="#Scene.destroy+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Scene" signature="get_list(world : Any)"></endpoint>
<signature id="Scene.get_list">Scene.get_list(**world**: `Any`)
<a class="headerlink" href="#Scene.get_list" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Scene" signature="exists(world : Any, id : Any)"></endpoint>
<signature id="Scene.exists+2">Scene.exists(**world**: `Any`, **id**: `Any`)
<a class="headerlink" href="#Scene.exists+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Scene" signature="entity_list(world : Any, id : Any)"></endpoint>
<signature id="Scene.entity_list+2">Scene.entity_list(**world**: `Any`, **id**: `Any`)
<a class="headerlink" href="#Scene.entity_list+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Scene" signature="entity_forget(world : Any, id : Any, entity : Any)"></endpoint>
<signature id="Scene.entity_forget+3">Scene.entity_forget(**world**: `Any`, **id**: `Any`, **entity**: `Any`)
<a class="headerlink" href="#Scene.entity_forget+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Scene" signature="set_id(world : Any, id : Any, new_id : Any)"></endpoint>
<signature id="Scene.set_id+3">Scene.set_id(**world**: `Any`, **id**: `Any`, **new_id**: `Any`)
<a class="headerlink" href="#Scene.set_id+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Scene" signature="load(world : Any, id : Any)"></endpoint>
<signature id="Scene.load+2">Scene.load(**world**: `Any`, **id**: `Any`)
<a class="headerlink" href="#Scene.load+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Scene" signature="load_as_clone(world : Any, id : Any)"></endpoint>
<signature id="Scene.load_as_clone+2">Scene.load_as_clone(**world**: `Any`, **id**: `Any`)
<a class="headerlink" href="#Scene.load_as_clone+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Scene" signature="unload(world : Any, id : Any)"></endpoint>
<signature id="Scene.unload+2">Scene.unload(**world**: `Any`, **id**: `Any`)
<a class="headerlink" href="#Scene.unload+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Sprite
`:::js import "luxe: world" for Sprite`
> A sprite is an image attached to an entity.   
> The `Sprite` modifier provides flipping, sizing, sub images and more.
> To attach a sprite to an entity, call `Sprite.create`:
> 
>   ```js
>   var entity = Entity.create(world)
>   var material = Assets.material("luxe: material/logo")
>   Sprite.create(entity, material, 128, 128)
>   ```

- [create](#Sprite.create+4)(**entity**: `Entity`, **material**: `Material`, **width**: `Num`, **height**: `Num`)
- [create](#Sprite.create+3)(**entity**: `Entity`, **atlas**: `Atlas`, **atlas_image**: `String`)
- [destroy](#Sprite.destroy)(**entity**: `Entity`)
- [has](#Sprite.has)(**entity**: `Entity`)
- [contains](#Sprite.contains+3)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
- [set_material](#Sprite.set_material+2)(**entity**: `Entity`, **material**: `Material`)
- [get_material](#Sprite.get_material)(**entity**: `Entity`)
- [set_origin](#Sprite.set_origin+3)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
- [get_origin](#Sprite.get_origin)(**entity**: `Entity`)
- [set_flip_h](#Sprite.set_flip_h+2)(**entity**: `Entity`, **flipped**: `Bool`)
- [get_flip_h](#Sprite.get_flip_h)(**entity**: `Entity`)
- [set_flip_v](#Sprite.set_flip_v+2)(**entity**: `Entity`, **flipped**: `Bool`)
- [get_flip_v](#Sprite.get_flip_v)(**entity**: `Entity`)
- [set_size](#Sprite.set_size+3)(**entity**: `Entity`, **width**: `Num`, **height**: `Num`)
- [set_width](#Sprite.set_width+2)(**entity**: `Entity`, **width**: `Num`)
- [get_width](#Sprite.get_width)(**entity**: `Entity`)
- [set_height](#Sprite.set_height+2)(**entity**: `Entity`, **height**: `Num`)
- [get_height](#Sprite.get_height)(**entity**: `Entity`)
- [set_alpha](#Sprite.set_alpha+2)(**entity**: `Entity`, **alpha**: `Num`)
- [get_alpha](#Sprite.get_alpha)(**entity**: `Entity`)
- [set_color](#Sprite.set_color+5)(**entity**: `Entity`, **r**: `Num`, **g**: `Num`, **b**: `Num`, **a**: `Num`)
- [get_color](#Sprite.get_color)(**entity**: `Entity`)
- [set_uv](#Sprite.set_uv+5)(**entity**: `Entity`, **x0**: `Num`, **y0**: `Num`, **x1**: `Num`, **y1**: `Num`)
- [get_uv](#Sprite.get_uv)(**entity**: `Entity`)
- [set_skew](#Sprite.set_skew+3)(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
- [get_skew](#Sprite.get_skew)(**entity**: `Entity`)
- [get_geometry](#Sprite.get_geometry)(**entity**: `Entity`)

<hr/>
<endpoint module="luxe: world" class="Sprite" signature="create(entity : Entity, material : Material, width : Num, height : Num)"></endpoint>
<signature id="Sprite.create+4">Sprite.create(**entity**: `Entity`, **material**: `Material`, **width**: `Num`, **height**: `Num`)
<a class="headerlink" href="#Sprite.create+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Attach a `Sprite` modifier to `entity`, drawn using `material`,
> with a size of `width`x`height`.
> 
>   ```js
>   var entity = Entity.create(world)
>   var material = Assets.material("luxe: material/logo")
>   Sprite.create(entity, material, 128, 128)
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="create(entity : Entity, atlas : Atlas, atlas_image : String)"></endpoint>
<signature id="Sprite.create+3">Sprite.create(**entity**: `Entity`, **atlas**: `Atlas`, **atlas_image**: `String`)
<a class="headerlink" href="#Sprite.create+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Attach a `Sprite` modifier to `entity`, drawn using the `atlas`, 
> using the image name in the atlas as `atlas_image`,
> with a size defined by the image in the atlas.
> 
>   ```js
>   var entity = Entity.create(world)
>   var atlas = Assets.atlas("atlas/example")
>   var image_name = "images/atlas/example/tree"
>   Sprite.create(entity, atlas, image_name)
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="destroy(entity : Entity)"></endpoint>
<signature id="Sprite.destroy">Sprite.destroy(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Detach and destroy the `Sprite` attached to `entity`
> 
>   ```js
>   Sprite.destroy(entity)
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="has(entity : Entity)"></endpoint>
<signature id="Sprite.has">Sprite.has(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if `entity` has a `Sprite` modifier attached.
> 
>   ```js
>   if(Sprite.has(entity)) {
>     System.print("found sprite")
>   }
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="contains(entity : Entity, x : Num, y : Num)"></endpoint>
<signature id="Sprite.contains+3">Sprite.contains(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
<a class="headerlink" href="#Sprite.contains+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if the `Sprite` attached to `entity` contains the point at `x`,`y` (in world units).
> Note that the function is based on the sprite `width` and `height`, it is not pixel perfect.
> 
>   ```js
>   //Convert mouse coords to world units
>   var pos = Camera.screen_point_to_world(
>       app.camera,
>       Input.mouse_x(),
>       Input.mouse_y())
>   //Check if point is inside the sprite
>   if(Sprite.contains(entity, pos.x, pos.y)) {
>     System.print("mouse inside sprite!")
>   }
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="set_material(entity : Entity, material : Material)"></endpoint>
<signature id="Sprite.set_material+2">Sprite.set_material(**entity**: `Entity`, **material**: `Material`)
<a class="headerlink" href="#Sprite.set_material+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Change the material that the `Sprite` attached to `entity` is drawn with, so it will draw with `material` instead.
> 
>   ```js
>   var material = Assets.material("luxe: material/logo.sprite")
>   Sprite.set_material(entity, material)
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="get_material(entity : Entity)"></endpoint>
<signature id="Sprite.get_material">Sprite.get_material(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_material" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Material`
> Returns the current material that the `Sprite` attached to `entity` is drawn with.
> 
>   ```js
>   var material = Sprite.get_material(entity)
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="set_origin(entity : Entity, x : Num, y : Num)"></endpoint>
<signature id="Sprite.set_origin+3">Sprite.set_origin(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
<a class="headerlink" href="#Sprite.set_origin+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Sets the origin of the sprite in relation to the `Transform` on `entity`. The `x` and `y` values are `0...1` range, where `0, 0` is bottom left, and `1, 1` is top right. A centered sprite is `0.5, 0.5`. To set the origin to the center, bottom you'd use `0.5, 0`.
> 
>   ```js
>   //centered
>   Sprite.set_origin(entity, 0.5, 0.5)
>   //bottom left
>   Sprite.set_origin(entity, 0, 0)
>   //bottom center
>   Sprite.set_origin(entity, 0.5, 0)
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="get_origin(entity : Entity)"></endpoint>
<signature id="Sprite.get_origin">Sprite.get_origin(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_origin" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Float2`
> Returns the current origin for the Sprite attached to `entity`.
>               
>   ```js
>   var origin = Sprite.get_origin(entity)
>   System.print(origin) //[0.5, 0.5]
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="set_flip_h(entity : Entity, flipped : Bool)"></endpoint>
<signature id="Sprite.set_flip_h+2">Sprite.set_flip_h(**entity**: `Entity`, **flipped**: `Bool`)
<a class="headerlink" href="#Sprite.set_flip_h+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set whether the `Sprite` attached to `entity` is `flipped` horizontally.
> 
>   ```js
>   Sprite.set_flip_h(entity, true)
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="get_flip_h(entity : Entity)"></endpoint>
<signature id="Sprite.get_flip_h">Sprite.get_flip_h(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_flip_h" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if the `Sprite` attached to `entity` is flipped horizontally.
> 
>   ```js
>   var flipped = Sprite.get_flip_h(entity)
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="set_flip_v(entity : Entity, flipped : Bool)"></endpoint>
<signature id="Sprite.set_flip_v+2">Sprite.set_flip_v(**entity**: `Entity`, **flipped**: `Bool`)
<a class="headerlink" href="#Sprite.set_flip_v+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set whether the `Sprite` attached to `entity` is `flipped` vertically.
> 
>   ```js
>   Sprite.set_flip_v(entity, true)
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="get_flip_v(entity : Entity)"></endpoint>
<signature id="Sprite.get_flip_v">Sprite.get_flip_v(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_flip_v" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if the `Sprite` attached to `entity` is flipped vertically.
> 
>   ```js
>   var flipped = Sprite.get_flip_v(entity)
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="set_size(entity : Entity, width : Num, height : Num)"></endpoint>
<signature id="Sprite.set_size+3">Sprite.set_size(**entity**: `Entity`, **width**: `Num`, **height**: `Num`)
<a class="headerlink" href="#Sprite.set_size+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Resize the `Sprite` attached to `entity` to be `width`x`height`.
> 
>   ```js
>   Sprite.set_size(entity, 256, 256)
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="set_width(entity : Entity, width : Num)"></endpoint>
<signature id="Sprite.set_width+2">Sprite.set_width(**entity**: `Entity`, **width**: `Num`)
<a class="headerlink" href="#Sprite.set_width+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Resize the `Sprite` attached to `entity` to have a new `width`.
> 
>   ```js
>   Sprite.set_width(entity, 64)
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="get_width(entity : Entity)"></endpoint>
<signature id="Sprite.get_width">Sprite.get_width(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_width" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Returns the width of the `Sprite` attached to `entity`.
> 
>   ```js
>   var width = Sprite.get_width(entity)
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="set_height(entity : Entity, height : Num)"></endpoint>
<signature id="Sprite.set_height+2">Sprite.set_height(**entity**: `Entity`, **height**: `Num`)
<a class="headerlink" href="#Sprite.set_height+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Resize the `Sprite` attached to `entity` to have a new `height`.
> 
>   ```js
>   Sprite.set_height(entity, 64)
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="get_height(entity : Entity)"></endpoint>
<signature id="Sprite.get_height">Sprite.get_height(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_height" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Returns the height of the `Sprite` attached to `entity`.
> 
>   ```js
>   var height = Sprite.get_height(entity)
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="set_alpha(entity : Entity, alpha : Num)"></endpoint>
<signature id="Sprite.set_alpha+2">Sprite.set_alpha(**entity**: `Entity`, **alpha**: `Num`)
<a class="headerlink" href="#Sprite.set_alpha+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Change the alpha (transparency) of the `Sprite` attached to `entity` to be `alpha`. Modifies the color.
> 
>   ```js
>   Sprite.set_alpha(entity, 0.5)
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="get_alpha(entity : Entity)"></endpoint>
<signature id="Sprite.get_alpha">Sprite.get_alpha(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_alpha" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Returns the current alpha of the `Sprite` attached to `entity`.
> 
>   ```js
>   var a = Sprite.get_alpha(entity)
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="set_color(entity : Entity, r : Num, g : Num, b : Num, a : Num)"></endpoint>
<signature id="Sprite.set_color+5">Sprite.set_color(**entity**: `Entity`, **r**: `Num`, **g**: `Num`, **b**: `Num`, **a**: `Num`)
<a class="headerlink" href="#Sprite.set_color+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the color of the `Sprite` attached to `entity` to be a color of `r`,`g`,`b`,`a`. :todo: Add `Sprite.set_color(entity, color)` to API. The default color is white, `[1, 1, 1, 1]`, so to undo a color change, set it to that.
> 
>   ```js
>   Sprite.set_color(entity, r, g, b, a)
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="get_color(entity : Entity)"></endpoint>
<signature id="Sprite.get_color">Sprite.get_color(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Color`
> Returns the current color of the `Sprite` attached to `entity`.
> 
>   ```js
>   var color = Sprite.get_color(entity)
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="set_uv(entity : Entity, x0 : Num, y0 : Num, x1 : Num, y1 : Num)"></endpoint>
<signature id="Sprite.set_uv+5">Sprite.set_uv(**entity**: `Entity`, **x0**: `Num`, **y0**: `Num`, **x1**: `Num`, **y1**: `Num`)
<a class="headerlink" href="#Sprite.set_uv+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the UV coordinates for the `Sprite` attached to `entity` with top left at `x0`,`y0` and bottom right `x1`,`y1`. The default is `0, 0, 1, 1`, a full rectangle in UV coordinate space. If you want to tile the image on a sprite, set it to values > 1.
> 
>   ```js
>   //tile 4 times on both x and y
>   Sprite.set_uv(entity, 0, 0, 4, 4)
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="get_uv(entity : Entity)"></endpoint>
<signature id="Sprite.get_uv">Sprite.get_uv(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_uv" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Float4`
> Returns the current uv of the `Sprite` attached to `entity`.
> 
>   ```js
>   var uv = Sprite.get_uv(entity)
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="set_skew(entity : Entity, x : Num, y : Num)"></endpoint>
<signature id="Sprite.set_skew+3">Sprite.set_skew(**entity**: `Entity`, **x**: `Num`, **y**: `Num`)
<a class="headerlink" href="#Sprite.set_skew+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the skew amounts for the `Sprite` attached to `entity`. The values of `x` and `y` are between `0 ... 1`, where 1 is the most skew and 0 is none.
> 
>   ```js
>   Sprite.set_skew(entity, 0, 0.25)
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="get_skew(entity : Entity)"></endpoint>
<signature id="Sprite.get_skew">Sprite.get_skew(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_skew" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Float2`
> Return the skew for the `Sprite` attached to `entity`.
> 
>   ```js
>   var skew = Sprite.get_skew(entity)
>   ```   

<endpoint module="luxe: world" class="Sprite" signature="get_geometry(entity : Entity)"></endpoint>
<signature id="Sprite.get_geometry">Sprite.get_geometry(**entity**: `Entity`)
<a class="headerlink" href="#Sprite.get_geometry" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Geometry`
> Returns the render [Geometry](#geometry) for the `Sprite` attached to `entity`. The geometry is owned by the sprite, so be aware when modifying it.
> 
>   ```js
>   var geometry = Sprite.get_geometry(entity)
>   ```   

### Tags
`:::js import "luxe: world" for Tags`
> no docs found

- [create](#Tags.create)(**entity**: `Any`)
- [destroy](#Tags.destroy)(**entity**: `Any`)
- [has](#Tags.has)(**entity**: `Any`)
- [add](#Tags.add+2)(**entity**: `Any`, **tag**: `Any`)
- [remove](#Tags.remove+2)(**entity**: `Any`, **tag**: `Any`)
- [list](#Tags.list+2)(**world**: `Any`, **tag**: `Any`)
- [list](#Tags.list)(**entity**: `Any`)
- [has_tag](#Tags.has_tag+2)(**entity**: `Any`, **tag**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Tags" signature="create(entity : Any)"></endpoint>
<signature id="Tags.create">Tags.create(**entity**: `Any`)
<a class="headerlink" href="#Tags.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tags" signature="destroy(entity : Any)"></endpoint>
<signature id="Tags.destroy">Tags.destroy(**entity**: `Any`)
<a class="headerlink" href="#Tags.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tags" signature="has(entity : Any)"></endpoint>
<signature id="Tags.has">Tags.has(**entity**: `Any`)
<a class="headerlink" href="#Tags.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tags" signature="add(entity : Any, tag : Any)"></endpoint>
<signature id="Tags.add+2">Tags.add(**entity**: `Any`, **tag**: `Any`)
<a class="headerlink" href="#Tags.add+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tags" signature="remove(entity : Any, tag : Any)"></endpoint>
<signature id="Tags.remove+2">Tags.remove(**entity**: `Any`, **tag**: `Any`)
<a class="headerlink" href="#Tags.remove+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tags" signature="list(world : Any, tag : Any)"></endpoint>
<signature id="Tags.list+2">Tags.list(**world**: `Any`, **tag**: `Any`)
<a class="headerlink" href="#Tags.list+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tags" signature="list(entity : Any)"></endpoint>
<signature id="Tags.list">Tags.list(**entity**: `Any`)
<a class="headerlink" href="#Tags.list" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tags" signature="has_tag(entity : Any, tag : Any)"></endpoint>
<signature id="Tags.has_tag+2">Tags.has_tag(**entity**: `Any`, **tag**: `Any`)
<a class="headerlink" href="#Tags.has_tag+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Text
`:::js import "luxe: world" for Text`
> no docs found

- [create](#Text.create+5)(**entity**: `Any`, **material**: `Any`, **default_size**: `Any`, **default_font**: `Any`, **default_color**: `Any`)
- [destroy](#Text.destroy)(**entity**: `Any`)
- [set_size](#Text.set_size+2)(**entity**: `Any`, **default_size**: `Any`)
- [get_size](#Text.get_size)(**entity**: `Any`)
- [set_font](#Text.set_font+2)(**entity**: `Any`, **default_font**: `Any`)
- [get_font](#Text.get_font)(**entity**: `Any`)
- [set_color](#Text.set_color+2)(**entity**: `Any`, **default_color**: `Any`)
- [get_color](#Text.get_color)(**entity**: `Any`)
- [set_align](#Text.set_align+3)(**entity**: `Any`, **align**: `Any`, **align_vertical**: `Any`)
- [set_align](#Text.set_align+2)(**entity**: `Any`, **align**: `Any`)
- [get_align](#Text.get_align)(**entity**: `Any`)
- [set_align_vertical](#Text.set_align_vertical+2)(**entity**: `Any`, **align_vertical**: `Any`)
- [get_align_vertical](#Text.get_align_vertical)(**entity**: `Any`)
- [set_bounds](#Text.set_bounds+5)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`)
- [get_bounds](#Text.get_bounds)(**entity**: `Any`)
- [set_attr](#Text.set_attr+5)(**entity**: `Any`, **start**: `Any`, **length**: `Any`, **key**: `Any`, **value**: `Any`)
- [attr_clear](#Text.attr_clear)(**entity**: `Any`)
- [commit](#Text.commit)(**entity**: `Any`)
- [get_render_text](#Text.get_render_text)(**entity**: `Any`)
- [get_geometry](#Text.get_geometry)(**entity**: `Any`)
- [get_extents](#Text.get_extents+3)(**entity**: `Any`, **offset**: `Any`, **count**: `Any`)
- [get_extents](#Text.get_extents)(**entity**: `Any`)
- [contains](#Text.contains+3)(**entity**: `Any`, **x**: `Any`, **y**: `Any`)
- [has](#Text.has)(**entity**: `Any`)
- [get_text](#Text.get_text)(**entity**: `Any`)
- [set_text_buffer](#Text.set_text_buffer+2)(**entity**: `Any`, **string**: `Any`)
- [set_text](#Text.set_text+2)(**entity**: `Any`, **string**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Text" signature="create(entity : Any, material : Any, default_size : Any, default_font : Any, default_color : Any)"></endpoint>
<signature id="Text.create+5">Text.create(**entity**: `Any`, **material**: `Any`, **default_size**: `Any`, **default_font**: `Any`, **default_color**: `Any`)
<a class="headerlink" href="#Text.create+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="destroy(entity : Any)"></endpoint>
<signature id="Text.destroy">Text.destroy(**entity**: `Any`)
<a class="headerlink" href="#Text.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="set_size(entity : Any, default_size : Any)"></endpoint>
<signature id="Text.set_size+2">Text.set_size(**entity**: `Any`, **default_size**: `Any`)
<a class="headerlink" href="#Text.set_size+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="get_size(entity : Any)"></endpoint>
<signature id="Text.get_size">Text.get_size(**entity**: `Any`)
<a class="headerlink" href="#Text.get_size" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="set_font(entity : Any, default_font : Any)"></endpoint>
<signature id="Text.set_font+2">Text.set_font(**entity**: `Any`, **default_font**: `Any`)
<a class="headerlink" href="#Text.set_font+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="get_font(entity : Any)"></endpoint>
<signature id="Text.get_font">Text.get_font(**entity**: `Any`)
<a class="headerlink" href="#Text.get_font" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="set_color(entity : Any, default_color : Any)"></endpoint>
<signature id="Text.set_color+2">Text.set_color(**entity**: `Any`, **default_color**: `Any`)
<a class="headerlink" href="#Text.set_color+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="get_color(entity : Any)"></endpoint>
<signature id="Text.get_color">Text.get_color(**entity**: `Any`)
<a class="headerlink" href="#Text.get_color" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="set_align(entity : Any, align : Any, align_vertical : Any)"></endpoint>
<signature id="Text.set_align+3">Text.set_align(**entity**: `Any`, **align**: `Any`, **align_vertical**: `Any`)
<a class="headerlink" href="#Text.set_align+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="set_align(entity : Any, align : Any)"></endpoint>
<signature id="Text.set_align+2">Text.set_align(**entity**: `Any`, **align**: `Any`)
<a class="headerlink" href="#Text.set_align+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="get_align(entity : Any)"></endpoint>
<signature id="Text.get_align">Text.get_align(**entity**: `Any`)
<a class="headerlink" href="#Text.get_align" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="set_align_vertical(entity : Any, align_vertical : Any)"></endpoint>
<signature id="Text.set_align_vertical+2">Text.set_align_vertical(**entity**: `Any`, **align_vertical**: `Any`)
<a class="headerlink" href="#Text.set_align_vertical+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="get_align_vertical(entity : Any)"></endpoint>
<signature id="Text.get_align_vertical">Text.get_align_vertical(**entity**: `Any`)
<a class="headerlink" href="#Text.get_align_vertical" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="set_bounds(entity : Any, x : Any, y : Any, w : Any, h : Any)"></endpoint>
<signature id="Text.set_bounds+5">Text.set_bounds(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`)
<a class="headerlink" href="#Text.set_bounds+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="get_bounds(entity : Any)"></endpoint>
<signature id="Text.get_bounds">Text.get_bounds(**entity**: `Any`)
<a class="headerlink" href="#Text.get_bounds" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="set_attr(entity : Any, start : Any, length : Any, key : Any, value : Any)"></endpoint>
<signature id="Text.set_attr+5">Text.set_attr(**entity**: `Any`, **start**: `Any`, **length**: `Any`, **key**: `Any`, **value**: `Any`)
<a class="headerlink" href="#Text.set_attr+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="attr_clear(entity : Any)"></endpoint>
<signature id="Text.attr_clear">Text.attr_clear(**entity**: `Any`)
<a class="headerlink" href="#Text.attr_clear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="commit(entity : Any)"></endpoint>
<signature id="Text.commit">Text.commit(**entity**: `Any`)
<a class="headerlink" href="#Text.commit" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="get_render_text(entity : Any)"></endpoint>
<signature id="Text.get_render_text">Text.get_render_text(**entity**: `Any`)
<a class="headerlink" href="#Text.get_render_text" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="get_geometry(entity : Any)"></endpoint>
<signature id="Text.get_geometry">Text.get_geometry(**entity**: `Any`)
<a class="headerlink" href="#Text.get_geometry" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="get_extents(entity : Any, offset : Any, count : Any)"></endpoint>
<signature id="Text.get_extents+3">Text.get_extents(**entity**: `Any`, **offset**: `Any`, **count**: `Any`)
<a class="headerlink" href="#Text.get_extents+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="get_extents(entity : Any)"></endpoint>
<signature id="Text.get_extents">Text.get_extents(**entity**: `Any`)
<a class="headerlink" href="#Text.get_extents" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="contains(entity : Any, x : Any, y : Any)"></endpoint>
<signature id="Text.contains+3">Text.contains(**entity**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Text.contains+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="has(entity : Any)"></endpoint>
<signature id="Text.has">Text.has(**entity**: `Any`)
<a class="headerlink" href="#Text.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="get_text(entity : Any)"></endpoint>
<signature id="Text.get_text">Text.get_text(**entity**: `Any`)
<a class="headerlink" href="#Text.get_text" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="set_text_buffer(entity : Any, string : Any)"></endpoint>
<signature id="Text.set_text_buffer+2">Text.set_text_buffer(**entity**: `Any`, **string**: `Any`)
<a class="headerlink" href="#Text.set_text_buffer+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Text" signature="set_text(entity : Any, string : Any)"></endpoint>
<signature id="Text.set_text+2">Text.set_text(**entity**: `Any`, **string**: `Any`)
<a class="headerlink" href="#Text.set_text+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Tile
`:::js import "luxe: world" for Tile`
> no docs found

- [create](#Tile.create+5)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **depth**: `Any`, **visual_id**: `Any`)
- [destroy](#Tile.destroy+2)(**entity**: `Any`, **tile**: `Any`)
- [destroy_at](#Tile.destroy_at+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **depth**: `Any`)
- [exists_at](#Tile.exists_at+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **depth**: `Any`)
- [get_at](#Tile.get_at+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **depth**: `Any`)
- [get_all](#Tile.get_all+2)(**entity**: `Any`, **into**: `Any`)
- [get_all_at](#Tile.get_all_at+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **into**: `Any`)
- [get_all_at_depth](#Tile.get_all_at_depth+3)(**entity**: `Any`, **depth**: `Any`, **into**: `Any`)
- [get_all_with_tag](#Tile.get_all_with_tag+3)(**entity**: `Any`, **tag**: `Any`, **into**: `Any`)
- [get_all_with_visual](#Tile.get_all_with_visual+3)(**entity**: `Any`, **visual**: `Any`, **into**: `Any`)
- [add_tag](#Tile.add_tag+3)(**entity**: `Any`, **tile**: `Any`, **tag**: `Any`)
- [remove_tag](#Tile.remove_tag+3)(**entity**: `Any`, **tile**: `Any`, **tag**: `Any`)
- [has_tag](#Tile.has_tag+3)(**entity**: `Any`, **tile**: `Any`, **tag**: `Any`)
- [get_tags](#Tile.get_tags+2)(**entity**: `Any`, **tile**: `Any`)
- [clear_tags](#Tile.clear_tags+2)(**entity**: `Any`, **tile**: `Any`)
- [set](#Tile.set+4)(**entity**: `Any`, **tile**: `Any`, **key**: `Any`, **value**: `Any`)
- [get](#Tile.get+4)(**entity**: `Any`, **tile**: `Any`, **key**: `Any`, **default**: `Any`)
- [set_coord](#Tile.set_coord+4)(**entity**: `Any`, **tile**: `Any`, **x**: `Any`, **y**: `Any`)
- [get_coord_x](#Tile.get_coord_x+2)(**entity**: `Any`, **tile**: `Any`)
- [get_coord_y](#Tile.get_coord_y+2)(**entity**: `Any`, **tile**: `Any`)
- [set_depth](#Tile.set_depth+3)(**entity**: `Any`, **tile**: `Any`, **depth**: `Any`)
- [get_depth](#Tile.get_depth+2)(**entity**: `Any`, **tile**: `Any`)
- [set_offset](#Tile.set_offset+4)(**entity**: `Any`, **tile**: `Any`, **x**: `Any`, **y**: `Any`)
- [set_offset_x](#Tile.set_offset_x+3)(**entity**: `Any`, **tile**: `Any`, **x**: `Any`)
- [set_offset_y](#Tile.set_offset_y+3)(**entity**: `Any`, **tile**: `Any`, **y**: `Any`)
- [get_offset_x](#Tile.get_offset_x+2)(**entity**: `Any`, **tile**: `Any`)
- [get_offset_y](#Tile.get_offset_y+2)(**entity**: `Any`, **tile**: `Any`)
- [reset_size](#Tile.reset_size+2)(**entity**: `Any`, **tile**: `Any`)
- [set_size](#Tile.set_size+4)(**entity**: `Any`, **tile**: `Any`, **x**: `Any`, **y**: `Any`)
- [set_size_x](#Tile.set_size_x+3)(**entity**: `Any`, **tile**: `Any`, **x**: `Any`)
- [set_size_y](#Tile.set_size_y+3)(**entity**: `Any`, **tile**: `Any`, **y**: `Any`)
- [get_size_x](#Tile.get_size_x+2)(**entity**: `Any`, **tile**: `Any`)
- [get_size_y](#Tile.get_size_y+2)(**entity**: `Any`, **tile**: `Any`)
- [set_flip](#Tile.set_flip+4)(**entity**: `Any`, **tile**: `Any`, **x**: `Any`, **y**: `Any`)
- [set_flip_x](#Tile.set_flip_x+3)(**entity**: `Any`, **tile**: `Any`, **flip**: `Any`)
- [set_flip_y](#Tile.set_flip_y+3)(**entity**: `Any`, **tile**: `Any`, **flip**: `Any`)
- [get_flip_x](#Tile.get_flip_x+2)(**entity**: `Any`, **tile**: `Any`)
- [get_flip_y](#Tile.get_flip_y+2)(**entity**: `Any`, **tile**: `Any`)
- [set_visual](#Tile.set_visual+3)(**entity**: `Any`, **tile**: `Any`, **visual**: `Any`)
- [get_visual](#Tile.get_visual+2)(**entity**: `Any`, **tile**: `Any`)
- [set_angle](#Tile.set_angle+3)(**entity**: `Any`, **tile**: `Any`, **angle**: `Any`)
- [get_angle](#Tile.get_angle+2)(**entity**: `Any`, **tile**: `Any`)
- [set_color](#Tile.set_color+3)(**entity**: `Any`, **tile**: `Any`, **color**: `Any`)
- [get_color](#Tile.get_color+2)(**entity**: `Any`, **tile**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Tile" signature="create(entity : Any, x : Any, y : Any, depth : Any, visual_id : Any)"></endpoint>
<signature id="Tile.create+5">Tile.create(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **depth**: `Any`, **visual_id**: `Any`)
<a class="headerlink" href="#Tile.create+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="destroy(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.destroy+2">Tile.destroy(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.destroy+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="destroy_at(entity : Any, x : Any, y : Any, depth : Any)"></endpoint>
<signature id="Tile.destroy_at+4">Tile.destroy_at(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **depth**: `Any`)
<a class="headerlink" href="#Tile.destroy_at+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="exists_at(entity : Any, x : Any, y : Any, depth : Any)"></endpoint>
<signature id="Tile.exists_at+4">Tile.exists_at(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **depth**: `Any`)
<a class="headerlink" href="#Tile.exists_at+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="get_at(entity : Any, x : Any, y : Any, depth : Any)"></endpoint>
<signature id="Tile.get_at+4">Tile.get_at(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **depth**: `Any`)
<a class="headerlink" href="#Tile.get_at+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="get_all(entity : Any, into : Any)"></endpoint>
<signature id="Tile.get_all+2">Tile.get_all(**entity**: `Any`, **into**: `Any`)
<a class="headerlink" href="#Tile.get_all+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="get_all_at(entity : Any, x : Any, y : Any, into : Any)"></endpoint>
<signature id="Tile.get_all_at+4">Tile.get_all_at(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **into**: `Any`)
<a class="headerlink" href="#Tile.get_all_at+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="get_all_at_depth(entity : Any, depth : Any, into : Any)"></endpoint>
<signature id="Tile.get_all_at_depth+3">Tile.get_all_at_depth(**entity**: `Any`, **depth**: `Any`, **into**: `Any`)
<a class="headerlink" href="#Tile.get_all_at_depth+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="get_all_with_tag(entity : Any, tag : Any, into : Any)"></endpoint>
<signature id="Tile.get_all_with_tag+3">Tile.get_all_with_tag(**entity**: `Any`, **tag**: `Any`, **into**: `Any`)
<a class="headerlink" href="#Tile.get_all_with_tag+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="get_all_with_visual(entity : Any, visual : Any, into : Any)"></endpoint>
<signature id="Tile.get_all_with_visual+3">Tile.get_all_with_visual(**entity**: `Any`, **visual**: `Any`, **into**: `Any`)
<a class="headerlink" href="#Tile.get_all_with_visual+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="add_tag(entity : Any, tile : Any, tag : Any)"></endpoint>
<signature id="Tile.add_tag+3">Tile.add_tag(**entity**: `Any`, **tile**: `Any`, **tag**: `Any`)
<a class="headerlink" href="#Tile.add_tag+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="remove_tag(entity : Any, tile : Any, tag : Any)"></endpoint>
<signature id="Tile.remove_tag+3">Tile.remove_tag(**entity**: `Any`, **tile**: `Any`, **tag**: `Any`)
<a class="headerlink" href="#Tile.remove_tag+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="has_tag(entity : Any, tile : Any, tag : Any)"></endpoint>
<signature id="Tile.has_tag+3">Tile.has_tag(**entity**: `Any`, **tile**: `Any`, **tag**: `Any`)
<a class="headerlink" href="#Tile.has_tag+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="get_tags(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_tags+2">Tile.get_tags(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_tags+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="clear_tags(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.clear_tags+2">Tile.clear_tags(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.clear_tags+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="set(entity : Any, tile : Any, key : Any, value : Any)"></endpoint>
<signature id="Tile.set+4">Tile.set(**entity**: `Any`, **tile**: `Any`, **key**: `Any`, **value**: `Any`)
<a class="headerlink" href="#Tile.set+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="get(entity : Any, tile : Any, key : Any, default : Any)"></endpoint>
<signature id="Tile.get+4">Tile.get(**entity**: `Any`, **tile**: `Any`, **key**: `Any`, **default**: `Any`)
<a class="headerlink" href="#Tile.get+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="set_coord(entity : Any, tile : Any, x : Any, y : Any)"></endpoint>
<signature id="Tile.set_coord+4">Tile.set_coord(**entity**: `Any`, **tile**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Tile.set_coord+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="get_coord_x(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_coord_x+2">Tile.get_coord_x(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_coord_x+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="get_coord_y(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_coord_y+2">Tile.get_coord_y(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_coord_y+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="set_depth(entity : Any, tile : Any, depth : Any)"></endpoint>
<signature id="Tile.set_depth+3">Tile.set_depth(**entity**: `Any`, **tile**: `Any`, **depth**: `Any`)
<a class="headerlink" href="#Tile.set_depth+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="get_depth(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_depth+2">Tile.get_depth(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_depth+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="set_offset(entity : Any, tile : Any, x : Any, y : Any)"></endpoint>
<signature id="Tile.set_offset+4">Tile.set_offset(**entity**: `Any`, **tile**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Tile.set_offset+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="set_offset_x(entity : Any, tile : Any, x : Any)"></endpoint>
<signature id="Tile.set_offset_x+3">Tile.set_offset_x(**entity**: `Any`, **tile**: `Any`, **x**: `Any`)
<a class="headerlink" href="#Tile.set_offset_x+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="set_offset_y(entity : Any, tile : Any, y : Any)"></endpoint>
<signature id="Tile.set_offset_y+3">Tile.set_offset_y(**entity**: `Any`, **tile**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Tile.set_offset_y+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="get_offset_x(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_offset_x+2">Tile.get_offset_x(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_offset_x+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="get_offset_y(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_offset_y+2">Tile.get_offset_y(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_offset_y+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="reset_size(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.reset_size+2">Tile.reset_size(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.reset_size+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="set_size(entity : Any, tile : Any, x : Any, y : Any)"></endpoint>
<signature id="Tile.set_size+4">Tile.set_size(**entity**: `Any`, **tile**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Tile.set_size+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="set_size_x(entity : Any, tile : Any, x : Any)"></endpoint>
<signature id="Tile.set_size_x+3">Tile.set_size_x(**entity**: `Any`, **tile**: `Any`, **x**: `Any`)
<a class="headerlink" href="#Tile.set_size_x+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="set_size_y(entity : Any, tile : Any, y : Any)"></endpoint>
<signature id="Tile.set_size_y+3">Tile.set_size_y(**entity**: `Any`, **tile**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Tile.set_size_y+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="get_size_x(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_size_x+2">Tile.get_size_x(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_size_x+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="get_size_y(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_size_y+2">Tile.get_size_y(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_size_y+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="set_flip(entity : Any, tile : Any, x : Any, y : Any)"></endpoint>
<signature id="Tile.set_flip+4">Tile.set_flip(**entity**: `Any`, **tile**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Tile.set_flip+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="set_flip_x(entity : Any, tile : Any, flip : Any)"></endpoint>
<signature id="Tile.set_flip_x+3">Tile.set_flip_x(**entity**: `Any`, **tile**: `Any`, **flip**: `Any`)
<a class="headerlink" href="#Tile.set_flip_x+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="set_flip_y(entity : Any, tile : Any, flip : Any)"></endpoint>
<signature id="Tile.set_flip_y+3">Tile.set_flip_y(**entity**: `Any`, **tile**: `Any`, **flip**: `Any`)
<a class="headerlink" href="#Tile.set_flip_y+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="get_flip_x(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_flip_x+2">Tile.get_flip_x(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_flip_x+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="get_flip_y(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_flip_y+2">Tile.get_flip_y(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_flip_y+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="set_visual(entity : Any, tile : Any, visual : Any)"></endpoint>
<signature id="Tile.set_visual+3">Tile.set_visual(**entity**: `Any`, **tile**: `Any`, **visual**: `Any`)
<a class="headerlink" href="#Tile.set_visual+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="get_visual(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_visual+2">Tile.get_visual(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_visual+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="set_angle(entity : Any, tile : Any, angle : Any)"></endpoint>
<signature id="Tile.set_angle+3">Tile.set_angle(**entity**: `Any`, **tile**: `Any`, **angle**: `Any`)
<a class="headerlink" href="#Tile.set_angle+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="get_angle(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_angle+2">Tile.get_angle(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_angle+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="set_color(entity : Any, tile : Any, color : Any)"></endpoint>
<signature id="Tile.set_color+3">Tile.set_color(**entity**: `Any`, **tile**: `Any`, **color**: `Any`)
<a class="headerlink" href="#Tile.set_color+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tile" signature="get_color(entity : Any, tile : Any)"></endpoint>
<signature id="Tile.get_color+2">Tile.get_color(**entity**: `Any`, **tile**: `Any`)
<a class="headerlink" href="#Tile.get_color+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Tiles
`:::js import "luxe: world" for Tiles`
> no docs found

- [create](#Tiles.create+3)(**entity**: `Any`, **grid_size_x**: `Any`, **grid_size_y**: `Any`)
- [create](#Tiles.create+2)(**entity**: `Any`, **asset_id**: `Any`)
- [destroy](#Tiles.destroy)(**entity**: `Any`)
- [clear](#Tiles.clear)(**entity**: `Any`)
- [has](#Tiles.has)(**entity**: `Any`)
- [commit](#Tiles.commit)(**entity**: `Any`)
- [set_grid_size](#Tiles.set_grid_size+3)(**entity**: `Any`, **x**: `Any`, **y**: `Any`)
- [get_grid_size](#Tiles.get_grid_size)(**entity**: `Any`)
- [set_asset](#Tiles.set_asset+2)(**entity**: `Any`, **asset_id**: `Any`)
- [get_asset_id](#Tiles.get_asset_id)(**entity**: `Any`)
- [set_asset_id](#Tiles.set_asset_id+2)(**entity**: `Any`, **asset_id**: `Any`)
- [define_source](#Tiles.define_source+3)(**entity**: `Any`, **source_id**: `Any`, **material**: `Any`)
- [undefine_source](#Tiles.undefine_source+2)(**entity**: `Any`, **source_id**: `Any`)
- [has_source](#Tiles.has_source+2)(**entity**: `Any`, **source_id**: `Any`)
- [define_visual](#Tiles.define_visual+4)(**entity**: `Any`, **source_id**: `Any`, **visual_id**: `Any`, **options**: `Any`)
- [undefine_visual](#Tiles.undefine_visual+3)(**entity**: `Any`, **source_id**: `Any`, **visual_id**: `Any`)
- [has_visual](#Tiles.has_visual+2)(**entity**: `Any`, **visual_id**: `Any`)
- [get_bounds_rects](#Tiles.get_bounds_rects+3)(**entity**: `Any`, **tiles**: `Any`, **into**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Tiles" signature="create(entity : Any, grid_size_x : Any, grid_size_y : Any)"></endpoint>
<signature id="Tiles.create+3">Tiles.create(**entity**: `Any`, **grid_size_x**: `Any`, **grid_size_y**: `Any`)
<a class="headerlink" href="#Tiles.create+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tiles" signature="create(entity : Any, asset_id : Any)"></endpoint>
<signature id="Tiles.create+2">Tiles.create(**entity**: `Any`, **asset_id**: `Any`)
<a class="headerlink" href="#Tiles.create+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tiles" signature="destroy(entity : Any)"></endpoint>
<signature id="Tiles.destroy">Tiles.destroy(**entity**: `Any`)
<a class="headerlink" href="#Tiles.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tiles" signature="clear(entity : Any)"></endpoint>
<signature id="Tiles.clear">Tiles.clear(**entity**: `Any`)
<a class="headerlink" href="#Tiles.clear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tiles" signature="has(entity : Any)"></endpoint>
<signature id="Tiles.has">Tiles.has(**entity**: `Any`)
<a class="headerlink" href="#Tiles.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tiles" signature="commit(entity : Any)"></endpoint>
<signature id="Tiles.commit">Tiles.commit(**entity**: `Any`)
<a class="headerlink" href="#Tiles.commit" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tiles" signature="set_grid_size(entity : Any, x : Any, y : Any)"></endpoint>
<signature id="Tiles.set_grid_size+3">Tiles.set_grid_size(**entity**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Tiles.set_grid_size+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tiles" signature="get_grid_size(entity : Any)"></endpoint>
<signature id="Tiles.get_grid_size">Tiles.get_grid_size(**entity**: `Any`)
<a class="headerlink" href="#Tiles.get_grid_size" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tiles" signature="set_asset(entity : Any, asset_id : Any)"></endpoint>
<signature id="Tiles.set_asset+2">Tiles.set_asset(**entity**: `Any`, **asset_id**: `Any`)
<a class="headerlink" href="#Tiles.set_asset+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tiles" signature="get_asset_id(entity : Any)"></endpoint>
<signature id="Tiles.get_asset_id">Tiles.get_asset_id(**entity**: `Any`)
<a class="headerlink" href="#Tiles.get_asset_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tiles" signature="set_asset_id(entity : Any, asset_id : Any)"></endpoint>
<signature id="Tiles.set_asset_id+2">Tiles.set_asset_id(**entity**: `Any`, **asset_id**: `Any`)
<a class="headerlink" href="#Tiles.set_asset_id+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tiles" signature="define_source(entity : Any, source_id : Any, material : Any)"></endpoint>
<signature id="Tiles.define_source+3">Tiles.define_source(**entity**: `Any`, **source_id**: `Any`, **material**: `Any`)
<a class="headerlink" href="#Tiles.define_source+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tiles" signature="undefine_source(entity : Any, source_id : Any)"></endpoint>
<signature id="Tiles.undefine_source+2">Tiles.undefine_source(**entity**: `Any`, **source_id**: `Any`)
<a class="headerlink" href="#Tiles.undefine_source+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tiles" signature="has_source(entity : Any, source_id : Any)"></endpoint>
<signature id="Tiles.has_source+2">Tiles.has_source(**entity**: `Any`, **source_id**: `Any`)
<a class="headerlink" href="#Tiles.has_source+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tiles" signature="define_visual(entity : Any, source_id : Any, visual_id : Any, options : Any)"></endpoint>
<signature id="Tiles.define_visual+4">Tiles.define_visual(**entity**: `Any`, **source_id**: `Any`, **visual_id**: `Any`, **options**: `Any`)
<a class="headerlink" href="#Tiles.define_visual+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tiles" signature="undefine_visual(entity : Any, source_id : Any, visual_id : Any)"></endpoint>
<signature id="Tiles.undefine_visual+3">Tiles.undefine_visual(**entity**: `Any`, **source_id**: `Any`, **visual_id**: `Any`)
<a class="headerlink" href="#Tiles.undefine_visual+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tiles" signature="has_visual(entity : Any, visual_id : Any)"></endpoint>
<signature id="Tiles.has_visual+2">Tiles.has_visual(**entity**: `Any`, **visual_id**: `Any`)
<a class="headerlink" href="#Tiles.has_visual+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Tiles" signature="get_bounds_rects(entity : Any, tiles : Any, into : Any)"></endpoint>
<signature id="Tiles.get_bounds_rects+3">Tiles.get_bounds_rects(**entity**: `Any`, **tiles**: `Any`, **into**: `Any`)
<a class="headerlink" href="#Tiles.get_bounds_rects+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Transform
`:::js import "luxe: world" for Transform`
> no docs found

- [create](#Transform.create)(**entity**: `Any`)
- [destroy](#Transform.destroy)(**entity**: `Any`)
- [has](#Transform.has)(**entity**: `Any`)
- [get_link](#Transform.get_link)(**entity**: `Any`)
- [get_linked](#Transform.get_linked)(**entity**: `Any`)
- [link](#Transform.link+3)(**entity**: `Any`, **target_entity**: `Any`, **reset_local**: `Any`)
- [link](#Transform.link+2)(**entity**: `Any`, **target_entity**: `Any`)
- [unlink](#Transform.unlink+2)(**entity**: `Any`, **reset_local**: `Any`)
- [unlink](#Transform.unlink)(**entity**: `Any`)
- [look_at_and_move](#Transform.look_at_and_move+4)(**entity**: `Any`, **pos**: `Any`, **target**: `Any`, **up**: `Any`)
- [look_at_and_move](#Transform.look_at_and_move+3)(**entity**: `Any`, **pos**: `Any`, **target**: `Any`)
- [look_at](#Transform.look_at+3)(**entity**: `Any`, **target**: `Any`, **up**: `Any`)
- [look_at](#Transform.look_at+2)(**entity**: `Any`, **target**: `Any`)
- [set_snap](#Transform.set_snap+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [set_snap](#Transform.set_snap+3)(**entity**: `Any`, **x**: `Any`, **y**: `Any`)
- [set_pos](#Transform.set_pos+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [set_pos](#Transform.set_pos+3)(**entity**: `Any`, **x**: `Any`, **y**: `Any`)
- [set_pos_world](#Transform.set_pos_world+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [set_pos_world](#Transform.set_pos_world+3)(**entity**: `Any`, **x**: `Any`, **y**: `Any`)
- [set_pos_x](#Transform.set_pos_x+2)(**entity**: `Any`, **x**: `Any`)
- [set_pos_y](#Transform.set_pos_y+2)(**entity**: `Any`, **y**: `Any`)
- [set_pos_z](#Transform.set_pos_z+2)(**entity**: `Any`, **z**: `Any`)
- [set_pos_x_world](#Transform.set_pos_x_world+2)(**entity**: `Any`, **x**: `Any`)
- [set_pos_y_world](#Transform.set_pos_y_world+2)(**entity**: `Any`, **y**: `Any`)
- [set_pos_z_world](#Transform.set_pos_z_world+2)(**entity**: `Any`, **z**: `Any`)
- [set_scale](#Transform.set_scale+3)(**entity**: `Any`, **x**: `Any`, **y**: `Any`)
- [set_scale](#Transform.set_scale+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [set_rotation_slerp_angle_axis](#Transform.set_rotation_slerp_angle_axis+5)(**entity**: `Any`, **axis**: `Any`, **from**: `Any`, **to**: `Any`, **t**: `Any`)
- [set_rotation_slerp_angle_axis_world](#Transform.set_rotation_slerp_angle_axis_world+5)(**entity**: `Any`, **axis**: `Any`, **from**: `Any`, **to**: `Any`, **t**: `Any`)
- [set_rotation_slerp](#Transform.set_rotation_slerp+4)(**entity**: `Any`, **from**: `Any`, **to**: `Any`, **t**: `Any`)
- [set_rotation_slerp_world](#Transform.set_rotation_slerp_world+4)(**entity**: `Any`, **from**: `Any`, **to**: `Any`, **t**: `Any`)
- [set_rotation](#Transform.set_rotation+5)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`)
- [set_rotation_world](#Transform.set_rotation_world+5)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`)
- [set_angle_axis](#Transform.set_angle_axis+5)(**entity**: `Any`, **degrees**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [set_angle_axis_world](#Transform.set_angle_axis_world+5)(**entity**: `Any`, **degrees**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [set_euler](#Transform.set_euler+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [set_euler_world](#Transform.set_euler_world+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [set_euler_x](#Transform.set_euler_x+2)(**entity**: `Any`, **x**: `Any`)
- [set_euler_y](#Transform.set_euler_y+2)(**entity**: `Any`, **y**: `Any`)
- [set_euler_z](#Transform.set_euler_z+2)(**entity**: `Any`, **z**: `Any`)
- [set_euler_x_world](#Transform.set_euler_x_world+2)(**entity**: `Any`, **x**: `Any`)
- [set_euler_y_world](#Transform.set_euler_y_world+2)(**entity**: `Any`, **y**: `Any`)
- [set_euler_z_world](#Transform.set_euler_z_world+2)(**entity**: `Any`, **z**: `Any`)
- [rotate_angle_axis_slerp](#Transform.rotate_angle_axis_slerp+3)(**entity**: `Any`, **axis**: `Any`, **angle_amount**: `Any`)
- [rotate_angle_axis_slerp_world](#Transform.rotate_angle_axis_slerp_world+3)(**entity**: `Any`, **axis**: `Any`, **angle_amount**: `Any`)
- [rotate_around_world](#Transform.rotate_around_world+8)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **axis_x**: `Any`, **axis_y**: `Any`, **axis_z**: `Any`, **degrees**: `Any`)
- [rotate_around](#Transform.rotate_around+8)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **axis_x**: `Any`, **axis_y**: `Any`, **axis_z**: `Any`, **degrees**: `Any`)
- [rotate_angle_axis](#Transform.rotate_angle_axis+5)(**entity**: `Any`, **degrees**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [rotate_angle_axis_world](#Transform.rotate_angle_axis_world+5)(**entity**: `Any`, **degrees**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [rotate_euler](#Transform.rotate_euler+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [rotate_euler_world](#Transform.rotate_euler_world+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [translate](#Transform.translate+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [translate](#Transform.translate+3)(**entity**: `Any`, **x**: `Any`, **y**: `Any`)
- [get_pos](#Transform.get_pos)(**entity**: `Any`)
- [get_pos_x](#Transform.get_pos_x)(**entity**: `Any`)
- [get_pos_y](#Transform.get_pos_y)(**entity**: `Any`)
- [get_pos_z](#Transform.get_pos_z)(**entity**: `Any`)
- [get_pos_world](#Transform.get_pos_world)(**entity**: `Any`)
- [get_pos_world_unsnapped](#Transform.get_pos_world_unsnapped)(**entity**: `Any`)
- [get_pos_x_world](#Transform.get_pos_x_world)(**entity**: `Any`)
- [get_pos_y_world](#Transform.get_pos_y_world)(**entity**: `Any`)
- [get_pos_z_world](#Transform.get_pos_z_world)(**entity**: `Any`)
- [rotate2D](#Transform.rotate2D+2)(**entity**: `Any`, **degrees**: `Any`)
- [set_angle2D](#Transform.set_angle2D+2)(**entity**: `Any`, **degrees**: `Any`)
- [set_angle2D_world](#Transform.set_angle2D_world+2)(**entity**: `Any`, **degrees**: `Any`)
- [get_angle2D](#Transform.get_angle2D)(**entity**: `Any`)
- [get_angle2D_world](#Transform.get_angle2D_world)(**entity**: `Any`)
- [set_depth2D](#Transform.set_depth2D+2)(**entity**: `Any`, **depth**: `Any`)
- [get_depth2D](#Transform.get_depth2D)(**entity**: `Any`)
- [set_depth2D_world](#Transform.set_depth2D_world+2)(**entity**: `Any`, **depth**: `Any`)
- [get_depth2D_world](#Transform.get_depth2D_world)(**entity**: `Any`)
- [get_rotation](#Transform.get_rotation)(**entity**: `Any`)
- [get_rotation_world](#Transform.get_rotation_world)(**entity**: `Any`)
- [get_rotation_matrix](#Transform.get_rotation_matrix+2)(**entity**: `Any`, **into_matrix**: `Any`)
- [get_euler](#Transform.get_euler)(**entity**: `Any`)
- [get_euler_x](#Transform.get_euler_x)(**entity**: `Any`)
- [get_euler_y](#Transform.get_euler_y)(**entity**: `Any`)
- [get_euler_z](#Transform.get_euler_z)(**entity**: `Any`)
- [get_euler_world](#Transform.get_euler_world)(**entity**: `Any`)
- [get_euler_x_world](#Transform.get_euler_x_world)(**entity**: `Any`)
- [get_euler_y_world](#Transform.get_euler_y_world)(**entity**: `Any`)
- [get_euler_z_world](#Transform.get_euler_z_world)(**entity**: `Any`)
- [get_scale](#Transform.get_scale)(**entity**: `Any`)
- [get_scale_x](#Transform.get_scale_x)(**entity**: `Any`)
- [get_scale_y](#Transform.get_scale_y)(**entity**: `Any`)
- [get_scale_z](#Transform.get_scale_z)(**entity**: `Any`)
- [get_right](#Transform.get_right)(**entity**: `Any`)
- [get_forward](#Transform.get_forward)(**entity**: `Any`)
- [get_up](#Transform.get_up)(**entity**: `Any`)
- [sync](#Transform.sync)(**entity**: `Any`)
- [sync_world](#Transform.sync_world)(**world**: `Any`)
- [local_vector_to_world](#Transform.local_vector_to_world+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [world_vector_to_local](#Transform.world_vector_to_local+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [local_dir_to_world](#Transform.local_dir_to_world+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [world_dir_to_local](#Transform.world_dir_to_local+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [world_point_to_local](#Transform.world_point_to_local+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [local_point_to_world](#Transform.local_point_to_world+4)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [listen_all](#Transform.listen_all+2)(**world**: `Any`, **fn**: `Any`)
- [unlisten_all](#Transform.unlisten_all+2)(**world**: `Any`, **handle**: `Any`)
- [listen](#Transform.listen+2)(**entity**: `Any`, **fn**: `Any`)
- [unlisten](#Transform.unlisten+2)(**entity**: `Any`, **handle**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Transform" signature="create(entity : Any)"></endpoint>
<signature id="Transform.create">Transform.create(**entity**: `Any`)
<a class="headerlink" href="#Transform.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="destroy(entity : Any)"></endpoint>
<signature id="Transform.destroy">Transform.destroy(**entity**: `Any`)
<a class="headerlink" href="#Transform.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="has(entity : Any)"></endpoint>
<signature id="Transform.has">Transform.has(**entity**: `Any`)
<a class="headerlink" href="#Transform.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_link(entity : Any)"></endpoint>
<signature id="Transform.get_link">Transform.get_link(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_link" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_linked(entity : Any)"></endpoint>
<signature id="Transform.get_linked">Transform.get_linked(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_linked" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="link(entity : Any, target_entity : Any, reset_local : Any)"></endpoint>
<signature id="Transform.link+3">Transform.link(**entity**: `Any`, **target_entity**: `Any`, **reset_local**: `Any`)
<a class="headerlink" href="#Transform.link+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="link(entity : Any, target_entity : Any)"></endpoint>
<signature id="Transform.link+2">Transform.link(**entity**: `Any`, **target_entity**: `Any`)
<a class="headerlink" href="#Transform.link+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="unlink(entity : Any, reset_local : Any)"></endpoint>
<signature id="Transform.unlink+2">Transform.unlink(**entity**: `Any`, **reset_local**: `Any`)
<a class="headerlink" href="#Transform.unlink+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="unlink(entity : Any)"></endpoint>
<signature id="Transform.unlink">Transform.unlink(**entity**: `Any`)
<a class="headerlink" href="#Transform.unlink" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="look_at_and_move(entity : Any, pos : Any, target : Any, up : Any)"></endpoint>
<signature id="Transform.look_at_and_move+4">Transform.look_at_and_move(**entity**: `Any`, **pos**: `Any`, **target**: `Any`, **up**: `Any`)
<a class="headerlink" href="#Transform.look_at_and_move+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="look_at_and_move(entity : Any, pos : Any, target : Any)"></endpoint>
<signature id="Transform.look_at_and_move+3">Transform.look_at_and_move(**entity**: `Any`, **pos**: `Any`, **target**: `Any`)
<a class="headerlink" href="#Transform.look_at_and_move+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="look_at(entity : Any, target : Any, up : Any)"></endpoint>
<signature id="Transform.look_at+3">Transform.look_at(**entity**: `Any`, **target**: `Any`, **up**: `Any`)
<a class="headerlink" href="#Transform.look_at+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="look_at(entity : Any, target : Any)"></endpoint>
<signature id="Transform.look_at+2">Transform.look_at(**entity**: `Any`, **target**: `Any`)
<a class="headerlink" href="#Transform.look_at+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_snap(entity : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Transform.set_snap+4">Transform.set_snap(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Transform.set_snap+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_snap(entity : Any, x : Any, y : Any)"></endpoint>
<signature id="Transform.set_snap+3">Transform.set_snap(**entity**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Transform.set_snap+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_pos(entity : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Transform.set_pos+4">Transform.set_pos(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Transform.set_pos+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_pos(entity : Any, x : Any, y : Any)"></endpoint>
<signature id="Transform.set_pos+3">Transform.set_pos(**entity**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Transform.set_pos+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_pos_world(entity : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Transform.set_pos_world+4">Transform.set_pos_world(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Transform.set_pos_world+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_pos_world(entity : Any, x : Any, y : Any)"></endpoint>
<signature id="Transform.set_pos_world+3">Transform.set_pos_world(**entity**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Transform.set_pos_world+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_pos_x(entity : Any, x : Any)"></endpoint>
<signature id="Transform.set_pos_x+2">Transform.set_pos_x(**entity**: `Any`, **x**: `Any`)
<a class="headerlink" href="#Transform.set_pos_x+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_pos_y(entity : Any, y : Any)"></endpoint>
<signature id="Transform.set_pos_y+2">Transform.set_pos_y(**entity**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Transform.set_pos_y+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_pos_z(entity : Any, z : Any)"></endpoint>
<signature id="Transform.set_pos_z+2">Transform.set_pos_z(**entity**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Transform.set_pos_z+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_pos_x_world(entity : Any, x : Any)"></endpoint>
<signature id="Transform.set_pos_x_world+2">Transform.set_pos_x_world(**entity**: `Any`, **x**: `Any`)
<a class="headerlink" href="#Transform.set_pos_x_world+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_pos_y_world(entity : Any, y : Any)"></endpoint>
<signature id="Transform.set_pos_y_world+2">Transform.set_pos_y_world(**entity**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Transform.set_pos_y_world+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_pos_z_world(entity : Any, z : Any)"></endpoint>
<signature id="Transform.set_pos_z_world+2">Transform.set_pos_z_world(**entity**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Transform.set_pos_z_world+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_scale(entity : Any, x : Any, y : Any)"></endpoint>
<signature id="Transform.set_scale+3">Transform.set_scale(**entity**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Transform.set_scale+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_scale(entity : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Transform.set_scale+4">Transform.set_scale(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Transform.set_scale+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_rotation_slerp_angle_axis(entity : Any, axis : Any, from : Any, to : Any, t : Any)"></endpoint>
<signature id="Transform.set_rotation_slerp_angle_axis+5">Transform.set_rotation_slerp_angle_axis(**entity**: `Any`, **axis**: `Any`, **from**: `Any`, **to**: `Any`, **t**: `Any`)
<a class="headerlink" href="#Transform.set_rotation_slerp_angle_axis+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_rotation_slerp_angle_axis_world(entity : Any, axis : Any, from : Any, to : Any, t : Any)"></endpoint>
<signature id="Transform.set_rotation_slerp_angle_axis_world+5">Transform.set_rotation_slerp_angle_axis_world(**entity**: `Any`, **axis**: `Any`, **from**: `Any`, **to**: `Any`, **t**: `Any`)
<a class="headerlink" href="#Transform.set_rotation_slerp_angle_axis_world+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_rotation_slerp(entity : Any, from : Any, to : Any, t : Any)"></endpoint>
<signature id="Transform.set_rotation_slerp+4">Transform.set_rotation_slerp(**entity**: `Any`, **from**: `Any`, **to**: `Any`, **t**: `Any`)
<a class="headerlink" href="#Transform.set_rotation_slerp+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_rotation_slerp_world(entity : Any, from : Any, to : Any, t : Any)"></endpoint>
<signature id="Transform.set_rotation_slerp_world+4">Transform.set_rotation_slerp_world(**entity**: `Any`, **from**: `Any`, **to**: `Any`, **t**: `Any`)
<a class="headerlink" href="#Transform.set_rotation_slerp_world+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_rotation(entity : Any, x : Any, y : Any, z : Any, w : Any)"></endpoint>
<signature id="Transform.set_rotation+5">Transform.set_rotation(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`)
<a class="headerlink" href="#Transform.set_rotation+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_rotation_world(entity : Any, x : Any, y : Any, z : Any, w : Any)"></endpoint>
<signature id="Transform.set_rotation_world+5">Transform.set_rotation_world(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`)
<a class="headerlink" href="#Transform.set_rotation_world+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_angle_axis(entity : Any, degrees : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Transform.set_angle_axis+5">Transform.set_angle_axis(**entity**: `Any`, **degrees**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Transform.set_angle_axis+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_angle_axis_world(entity : Any, degrees : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Transform.set_angle_axis_world+5">Transform.set_angle_axis_world(**entity**: `Any`, **degrees**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Transform.set_angle_axis_world+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_euler(entity : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Transform.set_euler+4">Transform.set_euler(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Transform.set_euler+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_euler_world(entity : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Transform.set_euler_world+4">Transform.set_euler_world(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Transform.set_euler_world+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_euler_x(entity : Any, x : Any)"></endpoint>
<signature id="Transform.set_euler_x+2">Transform.set_euler_x(**entity**: `Any`, **x**: `Any`)
<a class="headerlink" href="#Transform.set_euler_x+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_euler_y(entity : Any, y : Any)"></endpoint>
<signature id="Transform.set_euler_y+2">Transform.set_euler_y(**entity**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Transform.set_euler_y+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_euler_z(entity : Any, z : Any)"></endpoint>
<signature id="Transform.set_euler_z+2">Transform.set_euler_z(**entity**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Transform.set_euler_z+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_euler_x_world(entity : Any, x : Any)"></endpoint>
<signature id="Transform.set_euler_x_world+2">Transform.set_euler_x_world(**entity**: `Any`, **x**: `Any`)
<a class="headerlink" href="#Transform.set_euler_x_world+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_euler_y_world(entity : Any, y : Any)"></endpoint>
<signature id="Transform.set_euler_y_world+2">Transform.set_euler_y_world(**entity**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Transform.set_euler_y_world+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_euler_z_world(entity : Any, z : Any)"></endpoint>
<signature id="Transform.set_euler_z_world+2">Transform.set_euler_z_world(**entity**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Transform.set_euler_z_world+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="rotate_angle_axis_slerp(entity : Any, axis : Any, angle_amount : Any)"></endpoint>
<signature id="Transform.rotate_angle_axis_slerp+3">Transform.rotate_angle_axis_slerp(**entity**: `Any`, **axis**: `Any`, **angle_amount**: `Any`)
<a class="headerlink" href="#Transform.rotate_angle_axis_slerp+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="rotate_angle_axis_slerp_world(entity : Any, axis : Any, angle_amount : Any)"></endpoint>
<signature id="Transform.rotate_angle_axis_slerp_world+3">Transform.rotate_angle_axis_slerp_world(**entity**: `Any`, **axis**: `Any`, **angle_amount**: `Any`)
<a class="headerlink" href="#Transform.rotate_angle_axis_slerp_world+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="rotate_around_world(entity : Any, x : Any, y : Any, z : Any, axis_x : Any, axis_y : Any, axis_z : Any, degrees : Any)"></endpoint>
<signature id="Transform.rotate_around_world+8">Transform.rotate_around_world(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **axis_x**: `Any`, **axis_y**: `Any`, **axis_z**: `Any`, **degrees**: `Any`)
<a class="headerlink" href="#Transform.rotate_around_world+8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="rotate_around(entity : Any, x : Any, y : Any, z : Any, axis_x : Any, axis_y : Any, axis_z : Any, degrees : Any)"></endpoint>
<signature id="Transform.rotate_around+8">Transform.rotate_around(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **axis_x**: `Any`, **axis_y**: `Any`, **axis_z**: `Any`, **degrees**: `Any`)
<a class="headerlink" href="#Transform.rotate_around+8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="rotate_angle_axis(entity : Any, degrees : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Transform.rotate_angle_axis+5">Transform.rotate_angle_axis(**entity**: `Any`, **degrees**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Transform.rotate_angle_axis+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="rotate_angle_axis_world(entity : Any, degrees : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Transform.rotate_angle_axis_world+5">Transform.rotate_angle_axis_world(**entity**: `Any`, **degrees**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Transform.rotate_angle_axis_world+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="rotate_euler(entity : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Transform.rotate_euler+4">Transform.rotate_euler(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Transform.rotate_euler+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="rotate_euler_world(entity : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Transform.rotate_euler_world+4">Transform.rotate_euler_world(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Transform.rotate_euler_world+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="translate(entity : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Transform.translate+4">Transform.translate(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Transform.translate+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="translate(entity : Any, x : Any, y : Any)"></endpoint>
<signature id="Transform.translate+3">Transform.translate(**entity**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Transform.translate+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_pos(entity : Any)"></endpoint>
<signature id="Transform.get_pos">Transform.get_pos(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_pos" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_pos_x(entity : Any)"></endpoint>
<signature id="Transform.get_pos_x">Transform.get_pos_x(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_pos_x" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_pos_y(entity : Any)"></endpoint>
<signature id="Transform.get_pos_y">Transform.get_pos_y(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_pos_y" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_pos_z(entity : Any)"></endpoint>
<signature id="Transform.get_pos_z">Transform.get_pos_z(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_pos_z" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_pos_world(entity : Any)"></endpoint>
<signature id="Transform.get_pos_world">Transform.get_pos_world(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_pos_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_pos_world_unsnapped(entity : Any)"></endpoint>
<signature id="Transform.get_pos_world_unsnapped">Transform.get_pos_world_unsnapped(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_pos_world_unsnapped" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_pos_x_world(entity : Any)"></endpoint>
<signature id="Transform.get_pos_x_world">Transform.get_pos_x_world(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_pos_x_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_pos_y_world(entity : Any)"></endpoint>
<signature id="Transform.get_pos_y_world">Transform.get_pos_y_world(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_pos_y_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_pos_z_world(entity : Any)"></endpoint>
<signature id="Transform.get_pos_z_world">Transform.get_pos_z_world(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_pos_z_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="rotate2D(entity : Any, degrees : Any)"></endpoint>
<signature id="Transform.rotate2D+2">Transform.rotate2D(**entity**: `Any`, **degrees**: `Any`)
<a class="headerlink" href="#Transform.rotate2D+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_angle2D(entity : Any, degrees : Any)"></endpoint>
<signature id="Transform.set_angle2D+2">Transform.set_angle2D(**entity**: `Any`, **degrees**: `Any`)
<a class="headerlink" href="#Transform.set_angle2D+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_angle2D_world(entity : Any, degrees : Any)"></endpoint>
<signature id="Transform.set_angle2D_world+2">Transform.set_angle2D_world(**entity**: `Any`, **degrees**: `Any`)
<a class="headerlink" href="#Transform.set_angle2D_world+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_angle2D(entity : Any)"></endpoint>
<signature id="Transform.get_angle2D">Transform.get_angle2D(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_angle2D" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_angle2D_world(entity : Any)"></endpoint>
<signature id="Transform.get_angle2D_world">Transform.get_angle2D_world(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_angle2D_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_depth2D(entity : Any, depth : Any)"></endpoint>
<signature id="Transform.set_depth2D+2">Transform.set_depth2D(**entity**: `Any`, **depth**: `Any`)
<a class="headerlink" href="#Transform.set_depth2D+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_depth2D(entity : Any)"></endpoint>
<signature id="Transform.get_depth2D">Transform.get_depth2D(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_depth2D" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="set_depth2D_world(entity : Any, depth : Any)"></endpoint>
<signature id="Transform.set_depth2D_world+2">Transform.set_depth2D_world(**entity**: `Any`, **depth**: `Any`)
<a class="headerlink" href="#Transform.set_depth2D_world+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_depth2D_world(entity : Any)"></endpoint>
<signature id="Transform.get_depth2D_world">Transform.get_depth2D_world(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_depth2D_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_rotation(entity : Any)"></endpoint>
<signature id="Transform.get_rotation">Transform.get_rotation(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_rotation" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_rotation_world(entity : Any)"></endpoint>
<signature id="Transform.get_rotation_world">Transform.get_rotation_world(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_rotation_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_rotation_matrix(entity : Any, into_matrix : Any)"></endpoint>
<signature id="Transform.get_rotation_matrix+2">Transform.get_rotation_matrix(**entity**: `Any`, **into_matrix**: `Any`)
<a class="headerlink" href="#Transform.get_rotation_matrix+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_euler(entity : Any)"></endpoint>
<signature id="Transform.get_euler">Transform.get_euler(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_euler" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_euler_x(entity : Any)"></endpoint>
<signature id="Transform.get_euler_x">Transform.get_euler_x(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_euler_x" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_euler_y(entity : Any)"></endpoint>
<signature id="Transform.get_euler_y">Transform.get_euler_y(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_euler_y" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_euler_z(entity : Any)"></endpoint>
<signature id="Transform.get_euler_z">Transform.get_euler_z(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_euler_z" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_euler_world(entity : Any)"></endpoint>
<signature id="Transform.get_euler_world">Transform.get_euler_world(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_euler_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_euler_x_world(entity : Any)"></endpoint>
<signature id="Transform.get_euler_x_world">Transform.get_euler_x_world(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_euler_x_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_euler_y_world(entity : Any)"></endpoint>
<signature id="Transform.get_euler_y_world">Transform.get_euler_y_world(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_euler_y_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_euler_z_world(entity : Any)"></endpoint>
<signature id="Transform.get_euler_z_world">Transform.get_euler_z_world(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_euler_z_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_scale(entity : Any)"></endpoint>
<signature id="Transform.get_scale">Transform.get_scale(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_scale" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_scale_x(entity : Any)"></endpoint>
<signature id="Transform.get_scale_x">Transform.get_scale_x(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_scale_x" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_scale_y(entity : Any)"></endpoint>
<signature id="Transform.get_scale_y">Transform.get_scale_y(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_scale_y" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_scale_z(entity : Any)"></endpoint>
<signature id="Transform.get_scale_z">Transform.get_scale_z(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_scale_z" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_right(entity : Any)"></endpoint>
<signature id="Transform.get_right">Transform.get_right(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_right" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_forward(entity : Any)"></endpoint>
<signature id="Transform.get_forward">Transform.get_forward(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_forward" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="get_up(entity : Any)"></endpoint>
<signature id="Transform.get_up">Transform.get_up(**entity**: `Any`)
<a class="headerlink" href="#Transform.get_up" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="sync(entity : Any)"></endpoint>
<signature id="Transform.sync">Transform.sync(**entity**: `Any`)
<a class="headerlink" href="#Transform.sync" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="sync_world(world : Any)"></endpoint>
<signature id="Transform.sync_world">Transform.sync_world(**world**: `Any`)
<a class="headerlink" href="#Transform.sync_world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="local_vector_to_world(entity : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Transform.local_vector_to_world+4">Transform.local_vector_to_world(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Transform.local_vector_to_world+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="world_vector_to_local(entity : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Transform.world_vector_to_local+4">Transform.world_vector_to_local(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Transform.world_vector_to_local+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="local_dir_to_world(entity : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Transform.local_dir_to_world+4">Transform.local_dir_to_world(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Transform.local_dir_to_world+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="world_dir_to_local(entity : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Transform.world_dir_to_local+4">Transform.world_dir_to_local(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Transform.world_dir_to_local+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="world_point_to_local(entity : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Transform.world_point_to_local+4">Transform.world_point_to_local(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Transform.world_point_to_local+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="local_point_to_world(entity : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Transform.local_point_to_world+4">Transform.local_point_to_world(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Transform.local_point_to_world+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="listen_all(world : Any, fn : Any)"></endpoint>
<signature id="Transform.listen_all+2">Transform.listen_all(**world**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#Transform.listen_all+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="unlisten_all(world : Any, handle : Any)"></endpoint>
<signature id="Transform.unlisten_all+2">Transform.unlisten_all(**world**: `Any`, **handle**: `Any`)
<a class="headerlink" href="#Transform.unlisten_all+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="listen(entity : Any, fn : Any)"></endpoint>
<signature id="Transform.listen+2">Transform.listen(**entity**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#Transform.listen+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Transform" signature="unlisten(entity : Any, handle : Any)"></endpoint>
<signature id="Transform.unlisten+2">Transform.unlisten(**entity**: `Any`, **handle**: `Any`)
<a class="headerlink" href="#Transform.unlisten+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### UI
`:::js import "luxe: world" for UI`
> no docs found

- [create](#UI.create+7)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`, **z**: `Any`, **camera**: `Any`)
- [destroy](#UI.destroy)(**entity**: `Any`)
- [commit](#UI.commit)(**entity**: `Any`)
- [event_cancel](#UI.event_cancel+2)(**entity**: `Any`, **event_id**: `Any`)
- [event_cancelled](#UI.event_cancelled+2)(**entity**: `Any`, **event_id**: `Any`)
- [event_make_id](#UI.event_make_id)(**entity**: `Any`)
- [set_camera](#UI.set_camera+2)(**entity**: `Any`, **camera**: `Any`)
- [set_render_mode](#UI.set_render_mode+2)(**entity**: `Any`, **mode**: `Any`)
- [set_material_basis](#UI.set_material_basis+3)(**entity**: `Any`, **solid**: `Any`, **text**: `Any`)
- [set_bounds](#UI.set_bounds+6)(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`, **z**: `Any`)
- [get_input_node](#UI.get_input_node)(**entity**: `Any`)
- [set_input_node](#UI.set_input_node+2)(**entity**: `Any`, **input_node_id**: `Any`)
- [get_focused](#UI.get_focused)(**entity**: `Any`)
- [get_captured](#UI.get_captured)(**entity**: `Any`)
- [get_marked](#UI.get_marked)(**entity**: `Any`)
- [get_control_count](#UI.get_control_count)(**entity**: `Any`)
- [get_control](#UI.get_control+2)(**entity**: `Any`, **index**: `Any`)
- [focus_invalidate](#UI.focus_invalidate)(**entity**: `Any`)
- [focus](#UI.focus)(**control**: `Any`)
- [unfocus](#UI.unfocus)(**control**: `Any`)
- [mark](#UI.mark)(**control**: `Any`)
- [unmark](#UI.unmark)(**control**: `Any`)
- [capture](#UI.capture)(**control**: `Any`)
- [uncapture](#UI.uncapture)(**control**: `Any`)
- [bring_to_front](#UI.bring_to_front)(**control**: `Any`)
- [control_at_point](#UI.control_at_point+3)(**entity**: `Any`, **x**: `Any`, **y**: `Any`)
- [dump](#UI.dump)(**ui**: `Any`)
- [spawn](#UI.spawn+3)(**asset_id**: `Any`, **parent**: `Any`, **instance_id**: `Any`)
- [make](#UI.make+3)(**ui**: `Any`, **asset**: `Any`, **instance_id**: `Any`)
- [draw_depth_of](#UI.draw_depth_of+2)(**control**: `Any`, **index**: `Any`)
- [draw_text](#UI.draw_text+12)(**control**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **string**: `Any`, **size**: `Any`, **font**: `Any`, **color**: `Any`, **align**: `Any`, **align_vertical**: `Any`)
- [draw_text](#UI.draw_text+10)(**control**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **string**: `Any`, **size**: `Any`, **font**: `Any`, **color**: `Any`, **align**: `Any`, **align_vertical**: `Any`)
- [draw_image](#UI.draw_image+11)(**control**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **color**: `Any`, **uv**: `Any`, **image**: `Any`, **pixelated**: `Any`)
- [draw_image](#UI.draw_image+10)(**control**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **color**: `Any`, **uv**: `Any`, **image**: `Any`)
- [draw_quad](#UI.draw_quad+8)(**control**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **color**: `Any`)
- [draw_circle](#UI.draw_circle+10)(**control**: `Any`, **ox**: `Any`, **oy**: `Any`, **oz**: `Any`, **rx**: `Any`, **ry**: `Any`, **start_angle**: `Any`, **end_angle**: `Any`, **smoothness**: `Any`, **color**: `Any`)
- [draw_line](#UI.draw_line+7)(**control**: `Any`, **x1**: `Any`, **y1**: `Any`, **x2**: `Any`, **y2**: `Any`, **z**: `Any`, **style**: `Any`)
- [draw_rect](#UI.draw_rect+8)(**control**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **style**: `Any`)
- [draw_rect_detailed](#UI.draw_rect_detailed+10)(**control**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **radius**: `Any`, **smoothness**: `Any`, **style**: `Any`)
- [draw_ring](#UI.draw_ring+10)(**control**: `Any`, **ox**: `Any`, **oy**: `Any`, **oz**: `Any`, **rx**: `Any`, **ry**: `Any`, **start_angle**: `Any`, **end_angle**: `Any`, **smoothness**: `Any`, **style**: `Any`)
- [draw_path](#UI.draw_path+4)(**control**: `Any`, **points**: `Any`, **style**: `Any`, **closed**: `Any`)
- [events_emit](#UI.events_emit+2)(**control**: `Any`, **type**: `Any`)
- [events_emit](#UI.events_emit+3)(**control**: `Any`, **type**: `Any`, **data**: `Any`)

<hr/>
<endpoint module="luxe: world" class="UI" signature="create(entity : Any, x : Any, y : Any, w : Any, h : Any, z : Any, camera : Any)"></endpoint>
<signature id="UI.create+7">UI.create(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`, **z**: `Any`, **camera**: `Any`)
<a class="headerlink" href="#UI.create+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="destroy(entity : Any)"></endpoint>
<signature id="UI.destroy">UI.destroy(**entity**: `Any`)
<a class="headerlink" href="#UI.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="commit(entity : Any)"></endpoint>
<signature id="UI.commit">UI.commit(**entity**: `Any`)
<a class="headerlink" href="#UI.commit" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="event_cancel(entity : Any, event_id : Any)"></endpoint>
<signature id="UI.event_cancel+2">UI.event_cancel(**entity**: `Any`, **event_id**: `Any`)
<a class="headerlink" href="#UI.event_cancel+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="event_cancelled(entity : Any, event_id : Any)"></endpoint>
<signature id="UI.event_cancelled+2">UI.event_cancelled(**entity**: `Any`, **event_id**: `Any`)
<a class="headerlink" href="#UI.event_cancelled+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="event_make_id(entity : Any)"></endpoint>
<signature id="UI.event_make_id">UI.event_make_id(**entity**: `Any`)
<a class="headerlink" href="#UI.event_make_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="set_camera(entity : Any, camera : Any)"></endpoint>
<signature id="UI.set_camera+2">UI.set_camera(**entity**: `Any`, **camera**: `Any`)
<a class="headerlink" href="#UI.set_camera+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="set_render_mode(entity : Any, mode : Any)"></endpoint>
<signature id="UI.set_render_mode+2">UI.set_render_mode(**entity**: `Any`, **mode**: `Any`)
<a class="headerlink" href="#UI.set_render_mode+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="set_material_basis(entity : Any, solid : Any, text : Any)"></endpoint>
<signature id="UI.set_material_basis+3">UI.set_material_basis(**entity**: `Any`, **solid**: `Any`, **text**: `Any`)
<a class="headerlink" href="#UI.set_material_basis+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="set_bounds(entity : Any, x : Any, y : Any, w : Any, h : Any, z : Any)"></endpoint>
<signature id="UI.set_bounds+6">UI.set_bounds(**entity**: `Any`, **x**: `Any`, **y**: `Any`, **w**: `Any`, **h**: `Any`, **z**: `Any`)
<a class="headerlink" href="#UI.set_bounds+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="get_input_node(entity : Any)"></endpoint>
<signature id="UI.get_input_node">UI.get_input_node(**entity**: `Any`)
<a class="headerlink" href="#UI.get_input_node" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="set_input_node(entity : Any, input_node_id : Any)"></endpoint>
<signature id="UI.set_input_node+2">UI.set_input_node(**entity**: `Any`, **input_node_id**: `Any`)
<a class="headerlink" href="#UI.set_input_node+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="get_focused(entity : Any)"></endpoint>
<signature id="UI.get_focused">UI.get_focused(**entity**: `Any`)
<a class="headerlink" href="#UI.get_focused" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="get_captured(entity : Any)"></endpoint>
<signature id="UI.get_captured">UI.get_captured(**entity**: `Any`)
<a class="headerlink" href="#UI.get_captured" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="get_marked(entity : Any)"></endpoint>
<signature id="UI.get_marked">UI.get_marked(**entity**: `Any`)
<a class="headerlink" href="#UI.get_marked" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="get_control_count(entity : Any)"></endpoint>
<signature id="UI.get_control_count">UI.get_control_count(**entity**: `Any`)
<a class="headerlink" href="#UI.get_control_count" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="get_control(entity : Any, index : Any)"></endpoint>
<signature id="UI.get_control+2">UI.get_control(**entity**: `Any`, **index**: `Any`)
<a class="headerlink" href="#UI.get_control+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="focus_invalidate(entity : Any)"></endpoint>
<signature id="UI.focus_invalidate">UI.focus_invalidate(**entity**: `Any`)
<a class="headerlink" href="#UI.focus_invalidate" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="focus(control : Any)"></endpoint>
<signature id="UI.focus">UI.focus(**control**: `Any`)
<a class="headerlink" href="#UI.focus" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="unfocus(control : Any)"></endpoint>
<signature id="UI.unfocus">UI.unfocus(**control**: `Any`)
<a class="headerlink" href="#UI.unfocus" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="mark(control : Any)"></endpoint>
<signature id="UI.mark">UI.mark(**control**: `Any`)
<a class="headerlink" href="#UI.mark" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="unmark(control : Any)"></endpoint>
<signature id="UI.unmark">UI.unmark(**control**: `Any`)
<a class="headerlink" href="#UI.unmark" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="capture(control : Any)"></endpoint>
<signature id="UI.capture">UI.capture(**control**: `Any`)
<a class="headerlink" href="#UI.capture" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="uncapture(control : Any)"></endpoint>
<signature id="UI.uncapture">UI.uncapture(**control**: `Any`)
<a class="headerlink" href="#UI.uncapture" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="bring_to_front(control : Any)"></endpoint>
<signature id="UI.bring_to_front">UI.bring_to_front(**control**: `Any`)
<a class="headerlink" href="#UI.bring_to_front" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="control_at_point(entity : Any, x : Any, y : Any)"></endpoint>
<signature id="UI.control_at_point+3">UI.control_at_point(**entity**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#UI.control_at_point+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="dump(ui : Any)"></endpoint>
<signature id="UI.dump">UI.dump(**ui**: `Any`)
<a class="headerlink" href="#UI.dump" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="spawn(asset_id : Any, parent : Any, instance_id : Any)"></endpoint>
<signature id="UI.spawn+3">UI.spawn(**asset_id**: `Any`, **parent**: `Any`, **instance_id**: `Any`)
<a class="headerlink" href="#UI.spawn+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="make(ui : Any, asset : Any, instance_id : Any)"></endpoint>
<signature id="UI.make+3">UI.make(**ui**: `Any`, **asset**: `Any`, **instance_id**: `Any`)
<a class="headerlink" href="#UI.make+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="draw_depth_of(control : Any, index : Any)"></endpoint>
<signature id="UI.draw_depth_of+2">UI.draw_depth_of(**control**: `Any`, **index**: `Any`)
<a class="headerlink" href="#UI.draw_depth_of+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="draw_text(control : Any, x : Any, y : Any, z : Any, w : Any, h : Any, string : Any, size : Any, font : Any, color : Any, align : Any, align_vertical : Any)"></endpoint>
<signature id="UI.draw_text+12">UI.draw_text(**control**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **string**: `Any`, **size**: `Any`, **font**: `Any`, **color**: `Any`, **align**: `Any`, **align_vertical**: `Any`)
<a class="headerlink" href="#UI.draw_text+12" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="draw_text(control : Any, x : Any, y : Any, z : Any, string : Any, size : Any, font : Any, color : Any, align : Any, align_vertical : Any)"></endpoint>
<signature id="UI.draw_text+10">UI.draw_text(**control**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **string**: `Any`, **size**: `Any`, **font**: `Any`, **color**: `Any`, **align**: `Any`, **align_vertical**: `Any`)
<a class="headerlink" href="#UI.draw_text+10" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="draw_image(control : Any, x : Any, y : Any, z : Any, w : Any, h : Any, angle : Any, color : Any, uv : Any, image : Any, pixelated : Any)"></endpoint>
<signature id="UI.draw_image+11">UI.draw_image(**control**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **color**: `Any`, **uv**: `Any`, **image**: `Any`, **pixelated**: `Any`)
<a class="headerlink" href="#UI.draw_image+11" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="draw_image(control : Any, x : Any, y : Any, z : Any, w : Any, h : Any, angle : Any, color : Any, uv : Any, image : Any)"></endpoint>
<signature id="UI.draw_image+10">UI.draw_image(**control**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **color**: `Any`, **uv**: `Any`, **image**: `Any`)
<a class="headerlink" href="#UI.draw_image+10" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="draw_quad(control : Any, x : Any, y : Any, z : Any, w : Any, h : Any, angle : Any, color : Any)"></endpoint>
<signature id="UI.draw_quad+8">UI.draw_quad(**control**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **color**: `Any`)
<a class="headerlink" href="#UI.draw_quad+8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="draw_circle(control : Any, ox : Any, oy : Any, oz : Any, rx : Any, ry : Any, start_angle : Any, end_angle : Any, smoothness : Any, color : Any)"></endpoint>
<signature id="UI.draw_circle+10">UI.draw_circle(**control**: `Any`, **ox**: `Any`, **oy**: `Any`, **oz**: `Any`, **rx**: `Any`, **ry**: `Any`, **start_angle**: `Any`, **end_angle**: `Any`, **smoothness**: `Any`, **color**: `Any`)
<a class="headerlink" href="#UI.draw_circle+10" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="draw_line(control : Any, x1 : Any, y1 : Any, x2 : Any, y2 : Any, z : Any, style : Any)"></endpoint>
<signature id="UI.draw_line+7">UI.draw_line(**control**: `Any`, **x1**: `Any`, **y1**: `Any`, **x2**: `Any`, **y2**: `Any`, **z**: `Any`, **style**: `Any`)
<a class="headerlink" href="#UI.draw_line+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="draw_rect(control : Any, x : Any, y : Any, z : Any, w : Any, h : Any, angle : Any, style : Any)"></endpoint>
<signature id="UI.draw_rect+8">UI.draw_rect(**control**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **style**: `Any`)
<a class="headerlink" href="#UI.draw_rect+8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="draw_rect_detailed(control : Any, x : Any, y : Any, z : Any, w : Any, h : Any, angle : Any, radius : Any, smoothness : Any, style : Any)"></endpoint>
<signature id="UI.draw_rect_detailed+10">UI.draw_rect_detailed(**control**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`, **h**: `Any`, **angle**: `Any`, **radius**: `Any`, **smoothness**: `Any`, **style**: `Any`)
<a class="headerlink" href="#UI.draw_rect_detailed+10" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="draw_ring(control : Any, ox : Any, oy : Any, oz : Any, rx : Any, ry : Any, start_angle : Any, end_angle : Any, smoothness : Any, style : Any)"></endpoint>
<signature id="UI.draw_ring+10">UI.draw_ring(**control**: `Any`, **ox**: `Any`, **oy**: `Any`, **oz**: `Any`, **rx**: `Any`, **ry**: `Any`, **start_angle**: `Any`, **end_angle**: `Any`, **smoothness**: `Any`, **style**: `Any`)
<a class="headerlink" href="#UI.draw_ring+10" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="draw_path(control : Any, points : Any, style : Any, closed : Any)"></endpoint>
<signature id="UI.draw_path+4">UI.draw_path(**control**: `Any`, **points**: `Any`, **style**: `Any`, **closed**: `Any`)
<a class="headerlink" href="#UI.draw_path+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="events_emit(control : Any, type : Any)"></endpoint>
<signature id="UI.events_emit+2">UI.events_emit(**control**: `Any`, **type**: `Any`)
<a class="headerlink" href="#UI.events_emit+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UI" signature="events_emit(control : Any, type : Any, data : Any)"></endpoint>
<signature id="UI.events_emit+3">UI.events_emit(**control**: `Any`, **type**: `Any`, **data**: `Any`)
<a class="headerlink" href="#UI.events_emit+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### UIClear
`:::js import "luxe: world" for UIClear`
> no docs found

- [destroy](#UIClear.destroy)
- [remove](#UIClear.remove)
- [set_invisible](#UIClear.set_invisible)
- [remove_set_invisible](#UIClear.remove_set_invisible)

<hr/>
<endpoint module="luxe: world" class="UIClear" signature="destroy"></endpoint>
<signature id="UIClear.destroy">UIClear.destroy
<a class="headerlink" href="#UIClear.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UIClear" signature="remove"></endpoint>
<signature id="UIClear.remove">UIClear.remove
<a class="headerlink" href="#UIClear.remove" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UIClear" signature="set_invisible"></endpoint>
<signature id="UIClear.set_invisible">UIClear.set_invisible
<a class="headerlink" href="#UIClear.set_invisible" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UIClear" signature="remove_set_invisible"></endpoint>
<signature id="UIClear.remove_set_invisible">UIClear.remove_set_invisible
<a class="headerlink" href="#UIClear.remove_set_invisible" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### UIEvent
`:::js import "luxe: world" for UIEvent`
> The built in UI events that all controls can potentially use.

- [name](#UIEvent.name)(**value**: `Any`)
- [enter](#UIEvent.enter)
- [exit](#UIEvent.exit)
- [press](#UIEvent.press)
- [release](#UIEvent.release)
- [scroll](#UIEvent.scroll)
- [move](#UIEvent.move)
- [key](#UIEvent.key)
- [text](#UIEvent.text)
- [focus](#UIEvent.focus)
- [unfocus](#UIEvent.unfocus)
- [capture](#UIEvent.capture)
- [uncapture](#UIEvent.uncapture)
- [commit](#UIEvent.commit)
- [change](#UIEvent.change)
- [bounds](#UIEvent.bounds)

<hr/>
<endpoint module="luxe: world" class="UIEvent" signature="name(value : Any)"></endpoint>
<signature id="UIEvent.name">UIEvent.name(**value**: `Any`)
<a class="headerlink" href="#UIEvent.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Converts a UIEvent value to a readable name.
> 
>   ```js
>   System.print(UIEvent.name(UIEvent.move)) //prints "move"
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="enter"></endpoint>
<signature id="UIEvent.enter">UIEvent.enter
<a class="headerlink" href="#UIEvent.enter" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> An input cursor has entered this control. (e.g on mouse enter).
> Sends no additional data in the event.
> 
>   ```js
>   if(event.type == UIEvent.enter) {
>     System.print("entered control!")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="exit"></endpoint>
<signature id="UIEvent.exit">UIEvent.exit
<a class="headerlink" href="#UIEvent.exit" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> An input cursor has left this control. (e.g on mouse exit)
> Sends no additional data in the event.
> 
>   ```js
>   if(event.type == UIEvent.exit) {
>     System.print("exited control!")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="press"></endpoint>
<signature id="UIEvent.press">UIEvent.press
<a class="headerlink" href="#UIEvent.press" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> An input press event (e.g mouse button was pressed down). a.k.a "down"
> Sends `event.x`, `event.y` and `event.button`.
> 
>   ```js
>   if(event.type == UIEvent.press) {
>     var button = MouseButton.name(event.button)
>     System.print("pressed down on control at `%(event.x)`,`%(event.y)`")
>     System.print("  button was `%(button)`")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="release"></endpoint>
<signature id="UIEvent.release">UIEvent.release
<a class="headerlink" href="#UIEvent.release" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> An input release event (e.g mouse button was released). a.k.a "up"
> Sends `event.x`, `event.y` and `event.button`.
> 
>   ```js
>   if(event.type == UIEvent.press) {
>     var button = MouseButton.name(event.button)
>     System.print("released input on control at `%(event.x)`,`%(event.y)`")
>     System.print("  button was `%(button)`")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="scroll"></endpoint>
<signature id="UIEvent.scroll">UIEvent.scroll
<a class="headerlink" href="#UIEvent.scroll" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> A scroll event (e.g mouse wheel).
> Sends `event.x`, `event.y` where `x` is the horizontal scroll amount, 
> and `y` is the vertical scroll amount.
> 
>   ```js
>   if(event.type == UIEvent.scroll) {
>     System.print("scroll amount `%(event.x)`,`%(event.y)`")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="move"></endpoint>
<signature id="UIEvent.move">UIEvent.move
<a class="headerlink" href="#UIEvent.move" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> An input move event (e.g mouse movement).
> Sends `event.x`, `event.y` as the position of the input.
> 
>   ```js
>   if(event.type == UIEvent.press) {
>     System.print("move on control at `%(event.x)`,`%(event.y)`")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="key"></endpoint>
<signature id="UIEvent.key">UIEvent.key
<a class="headerlink" href="#UIEvent.key" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> A key input event.
> Sends a few useful values:
> 
> - `event.key` - a [Key](../input/#key) value
> - `event.scan` - a [Scan](../input/#scan) value
> - `event.mod` - a [ModState](../input/#modstate) value
> - `event.down` - a `Bool` value, whether the key is down or not
> - `event.repeat` - a `Bool` value, whether the event is from a key repeat
> 
>   ```js
>   if(event.type == UIEvent.key) {
>     var down = event.down ? "pressed" : "released"
>     System.print("key %(down), key was `%(Key.name(event.key))`")
>     System.print("  scan `%(Scan.name(event.scan))`, repeat? %(event.repeat)")
>     if(event.mod.lshift || event.mod.rshift) {
>       System.print("shift was also held down!")
>     }
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="text"></endpoint>
<signature id="UIEvent.text">UIEvent.text
<a class="headerlink" href="#UIEvent.text" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> A control has sent a text event, which originates from typing.
> 
> These events allow handling complex input that comes from the OS
> level IME input dialogs. On the simplest level, displaying `event.text`
> is enough to get started. 
> 
> Sends the following:
> 
> - `event.text` - the latest text displayed
> - `event.text_start` - the start of the modified text
> - `event.text_length` - the length of the modified text
> - `event.text_type` - a [TextEvent](../input/#textevent) type (`edit` or `input`)
> 
> The easiest way to understand might be to see.
> [This video](https://twitter.com/ruby0x1/status/928435874718679040) shows this at work.
> 
> As a user is typing, there may be candidates avaiable to select from, 
> when this is true, these are sent as `TextInput.edit` events, with a start and end.
> When a candidate is selected (or no choices), a `TextEvent.input` is sent with the `text`.   

<endpoint module="luxe: world" class="UIEvent" signature="focus"></endpoint>
<signature id="UIEvent.focus">UIEvent.focus
<a class="headerlink" href="#UIEvent.focus" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> A control has gained focus.
> Sends no additional data in the event.
> 
>   ```js
>   if(event.type == UIEvent.focus) {
>     System.print("gained focus!")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="unfocus"></endpoint>
<signature id="UIEvent.unfocus">UIEvent.unfocus
<a class="headerlink" href="#UIEvent.unfocus" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> A control has lost focus.
> Sends no additional data in the event.
> 
>   ```js
>   if(event.type == UIEvent.unfocus) {
>     System.print("lost focus!")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="capture"></endpoint>
<signature id="UIEvent.capture">UIEvent.capture
<a class="headerlink" href="#UIEvent.capture" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> A control has been captured.
> 
>   ```js
>   if(event.type == UIEvent.capture) {
>     System.print("gained input capture!")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="uncapture"></endpoint>
<signature id="UIEvent.uncapture">UIEvent.uncapture
<a class="headerlink" href="#UIEvent.uncapture" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> A control has lost capture status.
> 
>   ```js
>   if(event.type == UIEvent.uncapture) {
>     System.print("lost input capture!")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="commit"></endpoint>
<signature id="UIEvent.commit">UIEvent.commit
<a class="headerlink" href="#UIEvent.commit" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> When a control has changeable state (like an editable text control),
> it will send a `commit` event when the contents are being applied/committed.
> For example, if you are typing text and hit enter, or unfocus the control.
> 
>   ```js
>   if(event.type == UIEvent.uncapture) {
>     System.print("lost input capture!")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="change"></endpoint>
<signature id="UIEvent.change">UIEvent.change
<a class="headerlink" href="#UIEvent.change" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Change events are context specific, but notify you of a change in state.
> For example, [UIWindow](../ui/window) sends a change event with [UIWindowChange](../ui/window/#uiwindowchange) to notify when a window was closed, collapsed or uncollapsed. A [UIText](../ui/text) sends a change event
> when the text has been changed, via typing or otherwise.
> 
> In each case, `event.change` contains the relevant data.
> 
>   ```js
>   //UIText example
>   if(event.type == UIEvent.change) {
>     System.print("text changed `%(event.change)`!")
>   }
>   ```   

<endpoint module="luxe: world" class="UIEvent" signature="bounds"></endpoint>
<signature id="UIEvent.bounds">UIEvent.bounds
<a class="headerlink" href="#UIEvent.bounds" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> A control has changed bounds (note: this may not be working as intended right now).
> Sends `event.dx`, `event.dy` and `event.dw`, `event.dh` where `d` means `delta`.
> i.e the change in bounds as a difference between now and before.
> 
>   ```js
>   if(event.type == UIEvent.bounds) {
>     if(event.dx != 0) System.print("moved on x by %(event.dx) amount!")
>     if(event.dy != 0) System.print("moved on y by %(event.dy) amount!")
>     if(event.dw != 0) System.print("width changed by %(event.dw) amount!")
>     if(event.dh != 0) System.print("height changed by %(event.dh) amount!")
>   }
>   ```   

### UILayout
`:::js import "luxe: world" for UILayout`
> no docs found

- [create](#UILayout.create)(**ui_entity**: `Any`)
- [destroy](#UILayout.destroy)(**ui_entity**: `Any`)
- [commit](#UILayout.commit)(**ui_entity**: `Any`)
- [set_behave](#UILayout.set_behave+3)(**ui_entity**: `Any`, **control**: `Any`, **behave**: `Any`)
- [set_contain](#UILayout.set_contain+3)(**ui_entity**: `Any`, **control**: `Any`, **contain**: `Any`)
- [set_margin](#UILayout.set_margin+6)(**ui_entity**: `Any`, **control**: `Any`, **left**: `Any`, **top**: `Any`, **right**: `Any`, **bottom**: `Any`)

<hr/>
<endpoint module="luxe: world" class="UILayout" signature="create(ui_entity : Any)"></endpoint>
<signature id="UILayout.create">UILayout.create(**ui_entity**: `Any`)
<a class="headerlink" href="#UILayout.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayout" signature="destroy(ui_entity : Any)"></endpoint>
<signature id="UILayout.destroy">UILayout.destroy(**ui_entity**: `Any`)
<a class="headerlink" href="#UILayout.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayout" signature="commit(ui_entity : Any)"></endpoint>
<signature id="UILayout.commit">UILayout.commit(**ui_entity**: `Any`)
<a class="headerlink" href="#UILayout.commit" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayout" signature="set_behave(ui_entity : Any, control : Any, behave : Any)"></endpoint>
<signature id="UILayout.set_behave+3">UILayout.set_behave(**ui_entity**: `Any`, **control**: `Any`, **behave**: `Any`)
<a class="headerlink" href="#UILayout.set_behave+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayout" signature="set_contain(ui_entity : Any, control : Any, contain : Any)"></endpoint>
<signature id="UILayout.set_contain+3">UILayout.set_contain(**ui_entity**: `Any`, **control**: `Any`, **contain**: `Any`)
<a class="headerlink" href="#UILayout.set_contain+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayout" signature="set_margin(ui_entity : Any, control : Any, left : Any, top : Any, right : Any, bottom : Any)"></endpoint>
<signature id="UILayout.set_margin+6">UILayout.set_margin(**ui_entity**: `Any`, **control**: `Any`, **left**: `Any`, **top**: `Any`, **right**: `Any`, **bottom**: `Any`)
<a class="headerlink" href="#UILayout.set_margin+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### UILayoutBehave
`:::js import "luxe: world" for UILayoutBehave`
> no docs found

- [left](#UILayoutBehave.left)
- [top](#UILayoutBehave.top)
- [right](#UILayoutBehave.right)
- [bottom](#UILayoutBehave.bottom)
- [hfill](#UILayoutBehave.hfill)
- [vfill](#UILayoutBehave.vfill)
- [hcenter](#UILayoutBehave.hcenter)
- [vcenter](#UILayoutBehave.vcenter)
- [center](#UILayoutBehave.center)
- [fill](#UILayoutBehave.fill)
- [break_line](#UILayoutBehave.break_line)

<hr/>
<endpoint module="luxe: world" class="UILayoutBehave" signature="left"></endpoint>
<signature id="UILayoutBehave.left">UILayoutBehave.left
<a class="headerlink" href="#UILayoutBehave.left" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayoutBehave" signature="top"></endpoint>
<signature id="UILayoutBehave.top">UILayoutBehave.top
<a class="headerlink" href="#UILayoutBehave.top" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayoutBehave" signature="right"></endpoint>
<signature id="UILayoutBehave.right">UILayoutBehave.right
<a class="headerlink" href="#UILayoutBehave.right" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayoutBehave" signature="bottom"></endpoint>
<signature id="UILayoutBehave.bottom">UILayoutBehave.bottom
<a class="headerlink" href="#UILayoutBehave.bottom" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayoutBehave" signature="hfill"></endpoint>
<signature id="UILayoutBehave.hfill">UILayoutBehave.hfill
<a class="headerlink" href="#UILayoutBehave.hfill" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayoutBehave" signature="vfill"></endpoint>
<signature id="UILayoutBehave.vfill">UILayoutBehave.vfill
<a class="headerlink" href="#UILayoutBehave.vfill" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayoutBehave" signature="hcenter"></endpoint>
<signature id="UILayoutBehave.hcenter">UILayoutBehave.hcenter
<a class="headerlink" href="#UILayoutBehave.hcenter" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayoutBehave" signature="vcenter"></endpoint>
<signature id="UILayoutBehave.vcenter">UILayoutBehave.vcenter
<a class="headerlink" href="#UILayoutBehave.vcenter" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayoutBehave" signature="center"></endpoint>
<signature id="UILayoutBehave.center">UILayoutBehave.center
<a class="headerlink" href="#UILayoutBehave.center" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayoutBehave" signature="fill"></endpoint>
<signature id="UILayoutBehave.fill">UILayoutBehave.fill
<a class="headerlink" href="#UILayoutBehave.fill" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayoutBehave" signature="break_line"></endpoint>
<signature id="UILayoutBehave.break_line">UILayoutBehave.break_line
<a class="headerlink" href="#UILayoutBehave.break_line" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### UILayoutContain
`:::js import "luxe: world" for UILayoutContain`
> no docs found

- [row](#UILayoutContain.row)
- [column](#UILayoutContain.column)
- [layout](#UILayoutContain.layout)
- [flex](#UILayoutContain.flex)
- [nowrap](#UILayoutContain.nowrap)
- [wrap](#UILayoutContain.wrap)
- [start](#UILayoutContain.start)
- [middle](#UILayoutContain.middle)
- [end](#UILayoutContain.end)
- [justify](#UILayoutContain.justify)

<hr/>
<endpoint module="luxe: world" class="UILayoutContain" signature="row"></endpoint>
<signature id="UILayoutContain.row">UILayoutContain.row
<a class="headerlink" href="#UILayoutContain.row" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayoutContain" signature="column"></endpoint>
<signature id="UILayoutContain.column">UILayoutContain.column
<a class="headerlink" href="#UILayoutContain.column" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayoutContain" signature="layout"></endpoint>
<signature id="UILayoutContain.layout">UILayoutContain.layout
<a class="headerlink" href="#UILayoutContain.layout" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayoutContain" signature="flex"></endpoint>
<signature id="UILayoutContain.flex">UILayoutContain.flex
<a class="headerlink" href="#UILayoutContain.flex" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayoutContain" signature="nowrap"></endpoint>
<signature id="UILayoutContain.nowrap">UILayoutContain.nowrap
<a class="headerlink" href="#UILayoutContain.nowrap" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayoutContain" signature="wrap"></endpoint>
<signature id="UILayoutContain.wrap">UILayoutContain.wrap
<a class="headerlink" href="#UILayoutContain.wrap" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayoutContain" signature="start"></endpoint>
<signature id="UILayoutContain.start">UILayoutContain.start
<a class="headerlink" href="#UILayoutContain.start" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayoutContain" signature="middle"></endpoint>
<signature id="UILayoutContain.middle">UILayoutContain.middle
<a class="headerlink" href="#UILayoutContain.middle" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayoutContain" signature="end"></endpoint>
<signature id="UILayoutContain.end">UILayoutContain.end
<a class="headerlink" href="#UILayoutContain.end" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UILayoutContain" signature="justify"></endpoint>
<signature id="UILayoutContain.justify">UILayoutContain.justify
<a class="headerlink" href="#UILayoutContain.justify" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### UIRenderMode
`:::js import "luxe: world" for UIRenderMode`
> no docs found

- [unknown](#UIRenderMode.unknown)
- [image](#UIRenderMode.image)
- [world](#UIRenderMode.world)

<hr/>
<endpoint module="luxe: world" class="UIRenderMode" signature="unknown"></endpoint>
<signature id="UIRenderMode.unknown">UIRenderMode.unknown
<a class="headerlink" href="#UIRenderMode.unknown" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UIRenderMode" signature="image"></endpoint>
<signature id="UIRenderMode.image">UIRenderMode.image
<a class="headerlink" href="#UIRenderMode.image" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="UIRenderMode" signature="world"></endpoint>
<signature id="UIRenderMode.world">UIRenderMode.world
<a class="headerlink" href="#UIRenderMode.world" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### Values
`:::js import "luxe: world" for Values`
> no docs found

- [create](#Values.create)(**entity**: `Any`)
- [destroy](#Values.destroy)(**entity**: `Any`)
- [has](#Values.has)(**entity**: `Any`)
- [has_key](#Values.has_key+2)(**entity**: `Any`, **key**: `Any`)
- [remove_key](#Values.remove_key+2)(**entity**: `Any`, **key**: `Any`)
- [get_keys](#Values.get_keys)(**entity**: `Any`)
- [get](#Values.get+3)(**entity**: `Any`, **key**: `Any`, **default**: `Any`)
- [set](#Values.set+3)(**entity**: `Any`, **key**: `Any`, **value**: `Any`)
- [set_string](#Values.set_string+3)(**entity**: `Any`, **key**: `Any`, **value**: `Any`)
- [set_bool](#Values.set_bool+3)(**entity**: `Any`, **key**: `Any`, **value**: `Any`)
- [set_number](#Values.set_number+3)(**entity**: `Any`, **key**: `Any`, **value**: `Any`)
- [set_string](#Values.set_string+4)(**entity**: `Any`, **key**: `Any`, **value**: `Any`, **length**: `Any`)
- [set_float2](#Values.set_float2+4)(**entity**: `Any`, **key**: `Any`, **x**: `Any`, **y**: `Any`)
- [set_float3](#Values.set_float3+5)(**entity**: `Any`, **key**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
- [set_float4](#Values.set_float4+6)(**entity**: `Any`, **key**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`)
- [get_type](#Values.get_type+2)(**entity**: `Any`, **key**: `Any`)
- [get_bool](#Values.get_bool+3)(**entity**: `Any`, **key**: `Any`, **default**: `Any`)
- [get_number](#Values.get_number+3)(**entity**: `Any`, **key**: `Any`, **default**: `Any`)
- [get_string](#Values.get_string+3)(**entity**: `Any`, **key**: `Any`, **default**: `Any`)
- [get_float2](#Values.get_float2+3)(**entity**: `Any`, **key**: `Any`, **default**: `Any`)
- [get_float3](#Values.get_float3+3)(**entity**: `Any`, **key**: `Any`, **default**: `Any`)
- [get_float4](#Values.get_float4+3)(**entity**: `Any`, **key**: `Any`, **default**: `Any`)

<hr/>
<endpoint module="luxe: world" class="Values" signature="create(entity : Any)"></endpoint>
<signature id="Values.create">Values.create(**entity**: `Any`)
<a class="headerlink" href="#Values.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Values" signature="destroy(entity : Any)"></endpoint>
<signature id="Values.destroy">Values.destroy(**entity**: `Any`)
<a class="headerlink" href="#Values.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Values" signature="has(entity : Any)"></endpoint>
<signature id="Values.has">Values.has(**entity**: `Any`)
<a class="headerlink" href="#Values.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Values" signature="has_key(entity : Any, key : Any)"></endpoint>
<signature id="Values.has_key+2">Values.has_key(**entity**: `Any`, **key**: `Any`)
<a class="headerlink" href="#Values.has_key+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Values" signature="remove_key(entity : Any, key : Any)"></endpoint>
<signature id="Values.remove_key+2">Values.remove_key(**entity**: `Any`, **key**: `Any`)
<a class="headerlink" href="#Values.remove_key+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Values" signature="get_keys(entity : Any)"></endpoint>
<signature id="Values.get_keys">Values.get_keys(**entity**: `Any`)
<a class="headerlink" href="#Values.get_keys" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Values" signature="get(entity : Any, key : Any, default : Any)"></endpoint>
<signature id="Values.get+3">Values.get(**entity**: `Any`, **key**: `Any`, **default**: `Any`)
<a class="headerlink" href="#Values.get+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Values" signature="set(entity : Any, key : Any, value : Any)"></endpoint>
<signature id="Values.set+3">Values.set(**entity**: `Any`, **key**: `Any`, **value**: `Any`)
<a class="headerlink" href="#Values.set+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Values" signature="set_string(entity : Any, key : Any, value : Any)"></endpoint>
<signature id="Values.set_string+3">Values.set_string(**entity**: `Any`, **key**: `Any`, **value**: `Any`)
<a class="headerlink" href="#Values.set_string+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Values" signature="set_bool(entity : Any, key : Any, value : Any)"></endpoint>
<signature id="Values.set_bool+3">Values.set_bool(**entity**: `Any`, **key**: `Any`, **value**: `Any`)
<a class="headerlink" href="#Values.set_bool+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Values" signature="set_number(entity : Any, key : Any, value : Any)"></endpoint>
<signature id="Values.set_number+3">Values.set_number(**entity**: `Any`, **key**: `Any`, **value**: `Any`)
<a class="headerlink" href="#Values.set_number+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Values" signature="set_string(entity : Any, key : Any, value : Any, length : Any)"></endpoint>
<signature id="Values.set_string+4">Values.set_string(**entity**: `Any`, **key**: `Any`, **value**: `Any`, **length**: `Any`)
<a class="headerlink" href="#Values.set_string+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Values" signature="set_float2(entity : Any, key : Any, x : Any, y : Any)"></endpoint>
<signature id="Values.set_float2+4">Values.set_float2(**entity**: `Any`, **key**: `Any`, **x**: `Any`, **y**: `Any`)
<a class="headerlink" href="#Values.set_float2+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Values" signature="set_float3(entity : Any, key : Any, x : Any, y : Any, z : Any)"></endpoint>
<signature id="Values.set_float3+5">Values.set_float3(**entity**: `Any`, **key**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`)
<a class="headerlink" href="#Values.set_float3+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Values" signature="set_float4(entity : Any, key : Any, x : Any, y : Any, z : Any, w : Any)"></endpoint>
<signature id="Values.set_float4+6">Values.set_float4(**entity**: `Any`, **key**: `Any`, **x**: `Any`, **y**: `Any`, **z**: `Any`, **w**: `Any`)
<a class="headerlink" href="#Values.set_float4+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Values" signature="get_type(entity : Any, key : Any)"></endpoint>
<signature id="Values.get_type+2">Values.get_type(**entity**: `Any`, **key**: `Any`)
<a class="headerlink" href="#Values.get_type+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Values" signature="get_bool(entity : Any, key : Any, default : Any)"></endpoint>
<signature id="Values.get_bool+3">Values.get_bool(**entity**: `Any`, **key**: `Any`, **default**: `Any`)
<a class="headerlink" href="#Values.get_bool+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Values" signature="get_number(entity : Any, key : Any, default : Any)"></endpoint>
<signature id="Values.get_number+3">Values.get_number(**entity**: `Any`, **key**: `Any`, **default**: `Any`)
<a class="headerlink" href="#Values.get_number+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Values" signature="get_string(entity : Any, key : Any, default : Any)"></endpoint>
<signature id="Values.get_string+3">Values.get_string(**entity**: `Any`, **key**: `Any`, **default**: `Any`)
<a class="headerlink" href="#Values.get_string+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Values" signature="get_float2(entity : Any, key : Any, default : Any)"></endpoint>
<signature id="Values.get_float2+3">Values.get_float2(**entity**: `Any`, **key**: `Any`, **default**: `Any`)
<a class="headerlink" href="#Values.get_float2+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Values" signature="get_float3(entity : Any, key : Any, default : Any)"></endpoint>
<signature id="Values.get_float3+3">Values.get_float3(**entity**: `Any`, **key**: `Any`, **default**: `Any`)
<a class="headerlink" href="#Values.get_float3+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="Values" signature="get_float4(entity : Any, key : Any, default : Any)"></endpoint>
<signature id="Values.get_float4+3">Values.get_float4(**entity**: `Any`, **key**: `Any`, **default**: `Any`)
<a class="headerlink" href="#Values.get_float4+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### ValuesType
`:::js import "luxe: world" for ValuesType`
> no docs found

- [unknown](#ValuesType.unknown)
- [bool](#ValuesType.bool)
- [number](#ValuesType.number)
- [string](#ValuesType.string)
- [float2](#ValuesType.float2)
- [float3](#ValuesType.float3)
- [float4](#ValuesType.float4)
- [name](#ValuesType.name)(**value**: `Any`)

<hr/>
<endpoint module="luxe: world" class="ValuesType" signature="unknown"></endpoint>
<signature id="ValuesType.unknown">ValuesType.unknown
<a class="headerlink" href="#ValuesType.unknown" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ValuesType" signature="bool"></endpoint>
<signature id="ValuesType.bool">ValuesType.bool
<a class="headerlink" href="#ValuesType.bool" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ValuesType" signature="number"></endpoint>
<signature id="ValuesType.number">ValuesType.number
<a class="headerlink" href="#ValuesType.number" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ValuesType" signature="string"></endpoint>
<signature id="ValuesType.string">ValuesType.string
<a class="headerlink" href="#ValuesType.string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ValuesType" signature="float2"></endpoint>
<signature id="ValuesType.float2">ValuesType.float2
<a class="headerlink" href="#ValuesType.float2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ValuesType" signature="float3"></endpoint>
<signature id="ValuesType.float3">ValuesType.float3
<a class="headerlink" href="#ValuesType.float3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ValuesType" signature="float4"></endpoint>
<signature id="ValuesType.float4">ValuesType.float4
<a class="headerlink" href="#ValuesType.float4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="ValuesType" signature="name(value : Any)"></endpoint>
<signature id="ValuesType.name">ValuesType.name(**value**: `Any`)
<a class="headerlink" href="#ValuesType.name" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### World
`:::js import "luxe: world" for World`
> no docs found

- [exists](#World.exists)(**id**: `Any`)
- [valid](#World.valid)(**world**: `Any`)
- [get](#World.get)(**id**: `Any`)
- [get_id](#World.get_id)(**world**: `Any`)
- [set_id](#World.set_id+2)(**world**: `Any`, **id**: `Any`)
- [get_default](#World.get_default)()
- [set_default](#World.set_default)(**world**: `Any`)
- [list](#World.list)(**world**: `Any`)
- [list_ids](#World.list_ids)(**world**: `Any`)
- [clear](#World.clear)(**world**: `Any`)
- [tag_add](#World.tag_add+2)(**world**: `Any`, **tag**: `Any`)
- [tag_remove](#World.tag_remove+2)(**world**: `Any`, **tag**: `Any`)
- [tag_has](#World.tag_has+2)(**world**: `Any`, **tag**: `Any`)
- [get_delta](#World.get_delta)(**world**: `Any`)
- [tick_systems](#World.tick_systems+2)(**world**: `Any`, **delta**: `Any`)
- [schedule](#World.schedule+4)(**world**: `Any`, **time**: `Any`, **count**: `Any`, **fn**: `Any`)
- [schedule](#World.schedule+3)(**world**: `Any`, **time**: `Any`, **fn**: `Any`)
- [unschedule](#World.unschedule+2)(**world**: `Any`, **handle**: `Any`)
- [render_with_set](#World.render_with_set+4)(**world**: `Any`, **camera**: `Any`, **set**: `Any`, **target_path**: `Any`)
- [render_with_set](#World.render_with_set+5)(**world**: `Any`, **camera**: `Any`, **set**: `Any`, **target_path**: `Any`, **settings**: `Any`)
- [render_with_set](#World.render_with_set+7)(**world**: `Any`, **camera**: `Any`, **set**: `Any`, **target_path**: `Any`, **target_resource**: `Any`, **target_region**: `Any`, **settings**: `Any`)
- [render](#World.render+3)(**world**: `Any`, **camera**: `Any`, **target_path**: `Any`)
- [render](#World.render+4)(**world**: `Any`, **camera**: `Any`, **target_path**: `Any`, **settings**: `Any`)
- [render](#World.render+6)(**world**: `Any`, **camera**: `Any`, **target_path**: `Any`, **target_resource**: `Any`, **target_region**: `Any`, **settings**: `Any`)
- [render](#World.render+2)(**world**: `Any`, **desc**: `Any`)
- [render_fn](#World.render_fn+6)(**world**: `Any`, **camera**: `Any`, **target_resource**: `Any`, **target_region**: `Any`, **settings**: `Any`, **fn**: `Any`)
- [get_rate](#World.get_rate)(**world**: `Any`)
- [set_rate](#World.set_rate+2)(**world**: `Any`, **rate**: `Any`)
- [set_time](#World.set_time+2)(**world**: `Any`, **time**: `Any`)
- [time](#World.time)(**world**: `Any`)
- [render_set](#World.render_set)(**world**: `Any`)
- [render_set_add](#World.render_set_add+2)(**world**: `Any`, **geometry**: `Any`)
- [render_set_add](#World.render_set_add+3)(**world**: `Any`, **geometry**: `Any`, **entity**: `Any`)
- [render_set_remove](#World.render_set_remove+2)(**world**: `Any`, **geometry**: `Any`)
- [render_set_remove](#World.render_set_remove+3)(**world**: `Any`, **geometry**: `Any`, **entity**: `Any`)
- [render_get_entity](#World.render_get_entity+2)(**world**: `Any`, **geometry**: `Any`)
- [render_get_entity_set](#World.render_get_entity_set)(**entity**: `Any`)
- [disable](#World.disable+3)(**world**: `Any`, **state**: `Any`, **entities**: `Any`)
- [disable](#World.disable+2)(**world**: `Any`, **state**: `Any`)
- [emit](#World.emit+2)(**world**: `Any`, **tags**: `Any`)
- [emit](#World.emit+3)(**world**: `Any`, **tags**: `Any`, **data**: `Any`)
- [listen](#World.listen+3)(**world**: `Any`, **tags**: `Any`, **fn**: `Any`)
- [unlisten](#World.unlisten+3)(**world**: `Any`, **tags**: `Any`, **fn**: `Any`)
- [create](#World.create)()
- [create](#World.create)(**id**: `Any`)
- [destroy](#World.destroy)(**world**: `Any`)
- [tick](#World.tick+2)(**world**: `Any`, **delta**: `Any`)

<hr/>
<endpoint module="luxe: world" class="World" signature="exists(id : Any)"></endpoint>
<signature id="World.exists">World.exists(**id**: `Any`)
<a class="headerlink" href="#World.exists" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="valid(world : Any)"></endpoint>
<signature id="World.valid">World.valid(**world**: `Any`)
<a class="headerlink" href="#World.valid" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="get(id : Any)"></endpoint>
<signature id="World.get">World.get(**id**: `Any`)
<a class="headerlink" href="#World.get" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="get_id(world : Any)"></endpoint>
<signature id="World.get_id">World.get_id(**world**: `Any`)
<a class="headerlink" href="#World.get_id" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="set_id(world : Any, id : Any)"></endpoint>
<signature id="World.set_id+2">World.set_id(**world**: `Any`, **id**: `Any`)
<a class="headerlink" href="#World.set_id+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="get_default()"></endpoint>
<signature id="World.get_default">World.get_default()
<a class="headerlink" href="#World.get_default" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="set_default(world : Any)"></endpoint>
<signature id="World.set_default">World.set_default(**world**: `Any`)
<a class="headerlink" href="#World.set_default" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="list(world : Any)"></endpoint>
<signature id="World.list">World.list(**world**: `Any`)
<a class="headerlink" href="#World.list" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="list_ids(world : Any)"></endpoint>
<signature id="World.list_ids">World.list_ids(**world**: `Any`)
<a class="headerlink" href="#World.list_ids" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="clear(world : Any)"></endpoint>
<signature id="World.clear">World.clear(**world**: `Any`)
<a class="headerlink" href="#World.clear" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="tag_add(world : Any, tag : Any)"></endpoint>
<signature id="World.tag_add+2">World.tag_add(**world**: `Any`, **tag**: `Any`)
<a class="headerlink" href="#World.tag_add+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="tag_remove(world : Any, tag : Any)"></endpoint>
<signature id="World.tag_remove+2">World.tag_remove(**world**: `Any`, **tag**: `Any`)
<a class="headerlink" href="#World.tag_remove+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="tag_has(world : Any, tag : Any)"></endpoint>
<signature id="World.tag_has+2">World.tag_has(**world**: `Any`, **tag**: `Any`)
<a class="headerlink" href="#World.tag_has+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="get_delta(world : Any)"></endpoint>
<signature id="World.get_delta">World.get_delta(**world**: `Any`)
<a class="headerlink" href="#World.get_delta" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="tick_systems(world : Any, delta : Any)"></endpoint>
<signature id="World.tick_systems+2">World.tick_systems(**world**: `Any`, **delta**: `Any`)
<a class="headerlink" href="#World.tick_systems+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="schedule(world : Any, time : Any, count : Any, fn : Any)"></endpoint>
<signature id="World.schedule+4">World.schedule(**world**: `Any`, **time**: `Any`, **count**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#World.schedule+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="schedule(world : Any, time : Any, fn : Any)"></endpoint>
<signature id="World.schedule+3">World.schedule(**world**: `Any`, **time**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#World.schedule+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="unschedule(world : Any, handle : Any)"></endpoint>
<signature id="World.unschedule+2">World.unschedule(**world**: `Any`, **handle**: `Any`)
<a class="headerlink" href="#World.unschedule+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="render_with_set(world : Any, camera : Any, set : Any, target_path : Any)"></endpoint>
<signature id="World.render_with_set+4">World.render_with_set(**world**: `Any`, **camera**: `Any`, **set**: `Any`, **target_path**: `Any`)
<a class="headerlink" href="#World.render_with_set+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="render_with_set(world : Any, camera : Any, set : Any, target_path : Any, settings : Any)"></endpoint>
<signature id="World.render_with_set+5">World.render_with_set(**world**: `Any`, **camera**: `Any`, **set**: `Any`, **target_path**: `Any`, **settings**: `Any`)
<a class="headerlink" href="#World.render_with_set+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="render_with_set(world : Any, camera : Any, set : Any, target_path : Any, target_resource : Any, target_region : Any, settings : Any)"></endpoint>
<signature id="World.render_with_set+7">World.render_with_set(**world**: `Any`, **camera**: `Any`, **set**: `Any`, **target_path**: `Any`, **target_resource**: `Any`, **target_region**: `Any`, **settings**: `Any`)
<a class="headerlink" href="#World.render_with_set+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="render(world : Any, camera : Any, target_path : Any)"></endpoint>
<signature id="World.render+3">World.render(**world**: `Any`, **camera**: `Any`, **target_path**: `Any`)
<a class="headerlink" href="#World.render+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="render(world : Any, camera : Any, target_path : Any, settings : Any)"></endpoint>
<signature id="World.render+4">World.render(**world**: `Any`, **camera**: `Any`, **target_path**: `Any`, **settings**: `Any`)
<a class="headerlink" href="#World.render+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="render(world : Any, camera : Any, target_path : Any, target_resource : Any, target_region : Any, settings : Any)"></endpoint>
<signature id="World.render+6">World.render(**world**: `Any`, **camera**: `Any`, **target_path**: `Any`, **target_resource**: `Any`, **target_region**: `Any`, **settings**: `Any`)
<a class="headerlink" href="#World.render+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="render(world : Any, desc : Any)"></endpoint>
<signature id="World.render+2">World.render(**world**: `Any`, **desc**: `Any`)
<a class="headerlink" href="#World.render+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="render_fn(world : Any, camera : Any, target_resource : Any, target_region : Any, settings : Any, fn : Any)"></endpoint>
<signature id="World.render_fn+6">World.render_fn(**world**: `Any`, **camera**: `Any`, **target_resource**: `Any`, **target_region**: `Any`, **settings**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#World.render_fn+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="get_rate(world : Any)"></endpoint>
<signature id="World.get_rate">World.get_rate(**world**: `Any`)
<a class="headerlink" href="#World.get_rate" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="set_rate(world : Any, rate : Any)"></endpoint>
<signature id="World.set_rate+2">World.set_rate(**world**: `Any`, **rate**: `Any`)
<a class="headerlink" href="#World.set_rate+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="set_time(world : Any, time : Any)"></endpoint>
<signature id="World.set_time+2">World.set_time(**world**: `Any`, **time**: `Any`)
<a class="headerlink" href="#World.set_time+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="time(world : Any)"></endpoint>
<signature id="World.time">World.time(**world**: `Any`)
<a class="headerlink" href="#World.time" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="render_set(world : Any)"></endpoint>
<signature id="World.render_set">World.render_set(**world**: `Any`)
<a class="headerlink" href="#World.render_set" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="render_set_add(world : Any, geometry : Any)"></endpoint>
<signature id="World.render_set_add+2">World.render_set_add(**world**: `Any`, **geometry**: `Any`)
<a class="headerlink" href="#World.render_set_add+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="render_set_add(world : Any, geometry : Any, entity : Any)"></endpoint>
<signature id="World.render_set_add+3">World.render_set_add(**world**: `Any`, **geometry**: `Any`, **entity**: `Any`)
<a class="headerlink" href="#World.render_set_add+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="render_set_remove(world : Any, geometry : Any)"></endpoint>
<signature id="World.render_set_remove+2">World.render_set_remove(**world**: `Any`, **geometry**: `Any`)
<a class="headerlink" href="#World.render_set_remove+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="render_set_remove(world : Any, geometry : Any, entity : Any)"></endpoint>
<signature id="World.render_set_remove+3">World.render_set_remove(**world**: `Any`, **geometry**: `Any`, **entity**: `Any`)
<a class="headerlink" href="#World.render_set_remove+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="render_get_entity(world : Any, geometry : Any)"></endpoint>
<signature id="World.render_get_entity+2">World.render_get_entity(**world**: `Any`, **geometry**: `Any`)
<a class="headerlink" href="#World.render_get_entity+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="render_get_entity_set(entity : Any)"></endpoint>
<signature id="World.render_get_entity_set">World.render_get_entity_set(**entity**: `Any`)
<a class="headerlink" href="#World.render_get_entity_set" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="disable(world : Any, state : Any, entities : Any)"></endpoint>
<signature id="World.disable+3">World.disable(**world**: `Any`, **state**: `Any`, **entities**: `Any`)
<a class="headerlink" href="#World.disable+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="disable(world : Any, state : Any)"></endpoint>
<signature id="World.disable+2">World.disable(**world**: `Any`, **state**: `Any`)
<a class="headerlink" href="#World.disable+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="emit(world : Any, tags : Any)"></endpoint>
<signature id="World.emit+2">World.emit(**world**: `Any`, **tags**: `Any`)
<a class="headerlink" href="#World.emit+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="emit(world : Any, tags : Any, data : Any)"></endpoint>
<signature id="World.emit+3">World.emit(**world**: `Any`, **tags**: `Any`, **data**: `Any`)
<a class="headerlink" href="#World.emit+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="listen(world : Any, tags : Any, fn : Any)"></endpoint>
<signature id="World.listen+3">World.listen(**world**: `Any`, **tags**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#World.listen+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="unlisten(world : Any, tags : Any, fn : Any)"></endpoint>
<signature id="World.unlisten+3">World.unlisten(**world**: `Any`, **tags**: `Any`, **fn**: `Any`)
<a class="headerlink" href="#World.unlisten+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="create()"></endpoint>
<signature id="World.create">World.create()
<a class="headerlink" href="#World.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="create(id : Any)"></endpoint>
<signature id="World.create">World.create(**id**: `Any`)
<a class="headerlink" href="#World.create" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="destroy(world : Any)"></endpoint>
<signature id="World.destroy">World.destroy(**world**: `Any`)
<a class="headerlink" href="#World.destroy" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="World" signature="tick(world : Any, delta : Any)"></endpoint>
<signature id="World.tick+2">World.tick(**world**: `Any`, **delta**: `Any`)
<a class="headerlink" href="#World.tick+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

### WorldRenderDesc
`:::js import "luxe: world" for WorldRenderDesc`
> no docs found

- [camera](#WorldRenderDesc.camera)
- [camera](#WorldRenderDesc.camera=)=(v : Any)
- [camera](#WorldRenderDesc.camera)(**v**: `Any`)
- [cull_camera](#WorldRenderDesc.cull_camera)
- [cull_camera](#WorldRenderDesc.cull_camera=)=(v : Any)
- [cull_camera](#WorldRenderDesc.cull_camera)(**v**: `Any`)
- [new](#WorldRenderDesc.new)()

<hr/>
<endpoint module="luxe: world" class="WorldRenderDesc" signature="camera"></endpoint>
<signature id="WorldRenderDesc.camera">WorldRenderDesc.camera
<a class="headerlink" href="#WorldRenderDesc.camera" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="WorldRenderDesc" signature="camera=(v : Any)"></endpoint>
<signature id="WorldRenderDesc.camera=">WorldRenderDesc.camera=(v : Any)
<a class="headerlink" href="#WorldRenderDesc.camera=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="WorldRenderDesc" signature="camera(v : Any)"></endpoint>
<signature id="WorldRenderDesc.camera">WorldRenderDesc.camera(**v**: `Any`)
<a class="headerlink" href="#WorldRenderDesc.camera" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="WorldRenderDesc" signature="cull_camera"></endpoint>
<signature id="WorldRenderDesc.cull_camera">WorldRenderDesc.cull_camera
<a class="headerlink" href="#WorldRenderDesc.cull_camera" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="WorldRenderDesc" signature="cull_camera=(v : Any)"></endpoint>
<signature id="WorldRenderDesc.cull_camera=">WorldRenderDesc.cull_camera=(v : Any)
<a class="headerlink" href="#WorldRenderDesc.cull_camera=" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="WorldRenderDesc" signature="cull_camera(v : Any)"></endpoint>
<signature id="WorldRenderDesc.cull_camera">WorldRenderDesc.cull_camera(**v**: `Any`)
<a class="headerlink" href="#WorldRenderDesc.cull_camera" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> no docs found   

<endpoint module="luxe: world" class="WorldRenderDesc" signature="new()"></endpoint>
<signature id="WorldRenderDesc.new">WorldRenderDesc.new()
<a class="headerlink" href="#WorldRenderDesc.new" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js WorldRenderDesc`
> no docs found   

