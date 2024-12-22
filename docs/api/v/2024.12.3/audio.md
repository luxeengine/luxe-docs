#![](../../../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2024.12.3`)  


---

## `luxe: audio` module

- [Audio](#audio)   
- [AudioAttenuation](#audioattenuation)   
- [Bus](#bus)   

---

### Audio
`:::js import "luxe: audio" for Audio`
> The Audio module let's you play audio.
> 
> `Audio` is a service API, and isn't a modifier system.
> There is e.g the Sound modifier for placing sounds in the world.
> 
> Most things in `Audio` work on an instance (handle) of a sound.
> You get one of those from `play` or `loop`, and then can modify or query it.
> It's always safe to call any function on an instance, even if it's finished playing.
> 
> A quick look:
>   
>   ```js
>   //play them
>   var sound = Audio.play(Asset.audio("assets/sound"))
>   var music = Audio.loop(Asset.audio("assets/music"))
> 
>   //later...
>   Audio.volume(music, 0.5)
> 
>   //later still...
>   Audio.stop(music)
>   ```
> 
> That's it!

- [set_listener](#Audio.set_listener+4)(**pos**: `Float3`, **forward**: `Float3`, **up**: `Float3`, **velocity**: `Float3`)
- [play](#Audio.play+2)(**source**: `AudioAsset`, **volume**: `Num`)
- [play](#Audio.play+4)(**source**: `AudioAsset`, **as3D**: `Bool`, **bus**: `AudioBus`, **volume**: `Num`)
- [play](#Audio.play)(**source**: `AudioAsset`)
- [loop](#Audio.loop+2)(**source**: `AudioAsset`, **volume**: `Num`)
- [loop](#Audio.loop+4)(**source**: `AudioAsset`, **as3D**: `Bool`, **bus**: `AudioBus`, **volume**: `Num`)
- [loop](#Audio.loop)(**source**: `AudioAsset`)
- [stop](#Audio.stop)(**instance**: `AudioInstance`)
- [playing](#Audio.playing)(**instance**: `AudioInstance`)
- [pan](#Audio.pan+2)(**instance**: `AudioInstance`, **pan**: `Num`)
- [pan_of](#Audio.pan_of)(**instance**: `AudioInstance`)
- [volume](#Audio.volume+2)(**instance**: `AudioInstance`, **volume**: `Num`)
- [volume_of](#Audio.volume_of)(**instance**: `AudioInstance`)
- [pitch](#Audio.pitch+2)(**instance**: `AudioInstance`, **pitch**: `Num`)
- [pitch_of](#Audio.pitch_of)(**instance**: `AudioInstance`)
- [pause](#Audio.pause+2)(**instance**: `AudioInstance`, **paused**: `Bool`)
- [pause_of](#Audio.pause_of)(**instance**: `AudioInstance`)
- [set3D](#Audio.set3D+7)(**instance**: `AudioInstance`, **pos**: `Float3`, **vel**: `Float3`, **dopper_factor**: `Float`, **attenuation**: `AudioAttenuation`, **range**: `Float2`, **rolloff**: `Num`)

<hr/>
<endpoint module="luxe: audio" class="Audio" signature="set_listener(pos : Float3, forward : Float3, up : Float3, velocity : Float3)"></endpoint>
<signature id="Audio.set_listener+4">Audio.set_listener(**pos**: `Float3`, **forward**: `Float3`, **up**: `Float3`, **velocity**: `Float3`)
<a class="headerlink" href="#Audio.set_listener+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Set the world space listener position directly   

<endpoint module="luxe: audio" class="Audio" signature="play(source : AudioAsset, volume : Num)"></endpoint>
<signature id="Audio.play+2">Audio.play(**source**: `AudioAsset`, **volume**: `Num`)
<a class="headerlink" href="#Audio.play+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AudioInstance`
> Plays audio from the specified `source` at volume `volume`.
> Returns a handle to an audio instance that you can modify or stop.
>         
>   ```js
>   Audio.define_source("sound", "assets/sound.wav")
>   Audio.play("sound", 1)
>   ```   

<endpoint module="luxe: audio" class="Audio" signature="play(source : AudioAsset, as3D : Bool, bus : AudioBus, volume : Num)"></endpoint>
<signature id="Audio.play+4">Audio.play(**source**: `AudioAsset`, **as3D**: `Bool`, **bus**: `AudioBus`, **volume**: `Num`)
<a class="headerlink" href="#Audio.play+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AudioInstance`
> Plays audio from the specified `source` with `as3D` and `bus` at volume `volume`.
> The bus comes from `create_bus`, and 0 means global/default bus.
> If `as3D` is true, use set3D on the handle returned to configure position/velocity.
> Returns a handle to an audio instance that you can modify or stop.
>         
>   ```js
>   Audio.define_source("sound", "assets/sound.wav")
>   Audio.play("sound", true, 0, 1)
>   ```   

<endpoint module="luxe: audio" class="Audio" signature="play(source : AudioAsset)"></endpoint>
<signature id="Audio.play">Audio.play(**source**: `AudioAsset`)
<a class="headerlink" href="#Audio.play" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AudioInstance`
> Plays audio from the specified `source` at volume `1.0`.
> Returns a handle to an audio instance that you can modify or stop.
> 
>   ```js
>   Audio.define_source("sound", "assets/sound.wav")
>   Audio.play("sound")
>   ```   

<endpoint module="luxe: audio" class="Audio" signature="loop(source : AudioAsset, volume : Num)"></endpoint>
<signature id="Audio.loop+2">Audio.loop(**source**: `AudioAsset`, **volume**: `Num`)
<a class="headerlink" href="#Audio.loop+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AudioInstance`
> Begins looping audio for `id` at volume `volume`.
> Returns a handle to an audio instance that you can modify or stop.
> 
>   ```js
>   var music = Audio.loop("music", 1.0)
>   ```   

<endpoint module="luxe: audio" class="Audio" signature="loop(source : AudioAsset, as3D : Bool, bus : AudioBus, volume : Num)"></endpoint>
<signature id="Audio.loop+4">Audio.loop(**source**: `AudioAsset`, **as3D**: `Bool`, **bus**: `AudioBus`, **volume**: `Num`)
<a class="headerlink" href="#Audio.loop+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AudioInstance`
> Begins looping audio for `id` with `as3D` and `bus` at volume `volume`.
> The bus comes from `create_bus`, and 0 means global/default bus.
> If `as3D` is true, use set3D on the handle returned to configure position/velocity.    
> Returns a handle to an audio instance that you can modify or stop.
> 
>   ```js
>   var music = Audio.loop("music", false, 0, 1.0)
>   ```   

<endpoint module="luxe: audio" class="Audio" signature="loop(source : AudioAsset)"></endpoint>
<signature id="Audio.loop">Audio.loop(**source**: `AudioAsset`)
<a class="headerlink" href="#Audio.loop" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AudioInstance`
> Begins looping audio for `id` at volume `1.0`.
> Returns a handle to an audio instance that you can modify or stop.
> 
>   ```js
>   var music = Audio.loop("music")
>   ```   

<endpoint module="luxe: audio" class="Audio" signature="stop(instance : AudioInstance)"></endpoint>
<signature id="Audio.stop">Audio.stop(**instance**: `AudioInstance`)
<a class="headerlink" href="#Audio.stop" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Stops an AudioInstance.
> 
>   ```js
>   var music = Audio.loop("music")
>   Audio.stop(music)
>   ```   

<endpoint module="luxe: audio" class="Audio" signature="playing(instance : AudioInstance)"></endpoint>
<signature id="Audio.playing">Audio.playing(**instance**: `AudioInstance`)
<a class="headerlink" href="#Audio.playing" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns true if an AudioInstance is playing.
> 
>   ```js
>   var music = Audio.loop("music")
>   Log.print(Audio.playing(music)) //true
>   Audio.stop(music)
>   Log.print(Audio.playing(music)) //false
>   ```   

<endpoint module="luxe: audio" class="Audio" signature="pan(instance : AudioInstance, pan : Num)"></endpoint>
<signature id="Audio.pan+2">Audio.pan(**instance**: `AudioInstance`, **pan**: `Num`)
<a class="headerlink" href="#Audio.pan+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Sets the current `pan` value for the given `instance`.
> 
> Negative values for `pan` will move the audio to the left speakers, 
> while positive values will move the audio to the right speakers.
> 
> A value of 0 will reset to the audio sample back to center.
> 
>   ```js
>   var sound = Audio.play("sound")
>   Audio.pan(sound, -2.0)
>   ```   

<endpoint module="luxe: audio" class="Audio" signature="pan_of(instance : AudioInstance)"></endpoint>
<signature id="Audio.pan_of">Audio.pan_of(**instance**: `AudioInstance`)
<a class="headerlink" href="#Audio.pan_of" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Returns the current `pan` value for the given `instance`.
> 
>   ```js
>   var sound = Audio.play("sound")
>   Audio.pan(sound, 2.0)
>   Log.print(Audio.pan_of(sound)) // returns 2.0
>   ```   

<endpoint module="luxe: audio" class="Audio" signature="volume(instance : AudioInstance, volume : Num)"></endpoint>
<signature id="Audio.volume+2">Audio.volume(**instance**: `AudioInstance`, **volume**: `Num`)
<a class="headerlink" href="#Audio.volume+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Sets the `volume` for a given `instance`.
> 
> Intended volumes range from 0..1, with 1 meaning 100% volume, and 0 meaning silence.
> Volume values higher than 1 are valid (> 100%).
> 
>   ```js
>   var sound = Audio.play("sound") // Volume is 1.0
>   Audio.volume(sound, 0.5)        // Volume is now 0.5
>   ```   

<endpoint module="luxe: audio" class="Audio" signature="volume_of(instance : AudioInstance)"></endpoint>
<signature id="Audio.volume_of">Audio.volume_of(**instance**: `AudioInstance`)
<a class="headerlink" href="#Audio.volume_of" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Returns the current `volume` for the given `instance`.
> 
>   ```js
>   var sound = Audio.play("sound")
>   Log.print(Audio.volume_of(sound)) // returns 1
>   ```   

<endpoint module="luxe: audio" class="Audio" signature="pitch(instance : AudioInstance, pitch : Num)"></endpoint>
<signature id="Audio.pitch+2">Audio.pitch(**instance**: `AudioInstance`, **pitch**: `Num`)
<a class="headerlink" href="#Audio.pitch+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Adjusts the `pitch` of `instance`, making the sample sound higher or lower-pitched.
> Pitch values below 1 will lower the pitch of the sample, while pitch values above 1 raise it.
>     
> A value of 1 will cause the sample to be played at its source pitch.
>     
> Pitch changes will affect playback duration, causing lower-pitched samples 
> to have longer durations and higher-pitched samples to have shorter durations, 
> because the audio is not resampled (when using this function).
> 
> A pitch of 0 (or smaller) will be ignored.
> 
>   ```js
>   var sound = Audio.play("sound")
>   Audio.pitch(sound, 1)
>   ```   

<endpoint module="luxe: audio" class="Audio" signature="pitch_of(instance : AudioInstance)"></endpoint>
<signature id="Audio.pitch_of">Audio.pitch_of(**instance**: `AudioInstance`)
<a class="headerlink" href="#Audio.pitch_of" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Returns the current `pitch` for `instance`.
> 
>   ```js
>   var sound = Audio.play("sound")
>   Audio.pitch(sound, 3)
>   Log.print(Audio.pitch_of(sound)) // returns 3
>   ```   

<endpoint module="luxe: audio" class="Audio" signature="pause(instance : AudioInstance, paused : Bool)"></endpoint>
<signature id="Audio.pause+2">Audio.pause(**instance**: `AudioInstance`, **paused**: `Bool`)
<a class="headerlink" href="#Audio.pause+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Sets whether the audio `instance` is playing, pausing it when not.
> Once you set an `instance` to not play you can resume it later.
> 
> ```js
> var sound = Audio.play("sound")
> Audio.pause(sound, false) //pauses
> ```   

<endpoint module="luxe: audio" class="Audio" signature="pause_of(instance : AudioInstance)"></endpoint>
<signature id="Audio.pause_of">Audio.pause_of(**instance**: `AudioInstance`)
<a class="headerlink" href="#Audio.pause_of" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Returns whether an `instance` is paused.
> 
> ```js
> var sound = Audio.play("sound")
> Log.print(Audio.pause_of(sound)) //true
> Audio.pause(sound, false) //pause
> Log.print(Audio.pause_of(sound)) //false
> ```   

<endpoint module="luxe: audio" class="Audio" signature="set3D(instance : AudioInstance, pos : Float3, vel : Float3, dopper_factor : Float, attenuation : AudioAttenuation, range : Float2, rolloff : Num)"></endpoint>
<signature id="Audio.set3D+7">Audio.set3D(**instance**: `AudioInstance`, **pos**: `Float3`, **vel**: `Float3`, **dopper_factor**: `Float`, **attenuation**: `AudioAttenuation`, **range**: `Float2`, **rolloff**: `Num`)
<a class="headerlink" href="#Audio.set3D+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Sets 3D parameters of the the audio `instance`.
> Note that you need to use play with the 3d flag to make the sound 3d otherwise this has no effect.
> 
> ```js
> var sound = Audio.play("sound")
> var pos = [0,0,0]
> var vel = [0,0,0]
> var doppler = 1.0
> var attn = AudioAttenuation.none
> var range = [1, 100] // min / max distance for attenuation
> var rolloff = 1.0
> Audio.set3D(sound, pos, vel, doppler, attn, range, rolloff)
> ```   

### AudioAttenuation
`:::js import "luxe: audio" for AudioAttenuation`
> Read more details with graphs here https://solhsa.com/soloud/concepts3d.html#attenuation

- [none](#AudioAttenuation.none)
- [inverse_distance](#AudioAttenuation.inverse_distance)
- [linear_distance](#AudioAttenuation.linear_distance)
- [exponential_distance](#AudioAttenuation.exponential_distance)

<hr/>
<endpoint module="luxe: audio" class="AudioAttenuation" signature="none"></endpoint>
<signature id="AudioAttenuation.none">AudioAttenuation.none
<a class="headerlink" href="#AudioAttenuation.none" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> No attenuation based on distance. The default   

<endpoint module="luxe: audio" class="AudioAttenuation" signature="inverse_distance"></endpoint>
<signature id="AudioAttenuation.inverse_distance">AudioAttenuation.inverse_distance
<a class="headerlink" href="#AudioAttenuation.inverse_distance" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> The higher the rolloff factor, the more steeply the volume drops. 
> At low enough rolloff factor, the volume never drops near zero. 
> Values over 1 recommended (unless you have special needs). 
> Values less than equal to zero result in undefined behavior.
> Increasing the minimum distance pushes the start of the attenuation further. 
> It also causes the curve to change. Note that the minimum distance must be above 0.
> The maximum distance simply cuts the attenuation at the volume level it has reached at that point.   

<endpoint module="luxe: audio" class="AudioAttenuation" signature="linear_distance"></endpoint>
<signature id="AudioAttenuation.linear_distance">AudioAttenuation.linear_distance
<a class="headerlink" href="#AudioAttenuation.linear_distance" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> The rolloff factor for linear distance simply sets the maximum volume reduction. 
> Using values outside the 0..1 range causes undefined behavior.
> The minimum and maximum distance works as one might expect. 
> Minimum distance must be less or equal to maximum distance.   

<endpoint module="luxe: audio" class="AudioAttenuation" signature="exponential_distance"></endpoint>
<signature id="AudioAttenuation.exponential_distance">AudioAttenuation.exponential_distance
<a class="headerlink" href="#AudioAttenuation.exponential_distance" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> The higher the rolloff factor, the more steeply the volume drops. 
> At low enough rolloff factor, the volume never drops near zero. 
> Values over 1 recommended (unless you have special needs). 
> Values less than equal to zero result in really weird behavior.
> Increasing the minimum distance pushes the start of the attenuation further. 
> It also causes the curve to change. Note that the minimum distance must be above 0.
> The maximum distance simply cuts the attenuation at the volume level it has reached at that point.   

### Bus
`:::js import "luxe: audio" for Bus`
> no docs found

- [set_channels](#Bus.set_channels+2)(**bus**: `AudioBus`, **value**: `Num`)
- [set_volume](#Bus.set_volume+2)(**bus**: `AudioBus`, **value**: `Num`)
- [get_volume](#Bus.get_volume)(**bus**: `AudioBus`)

<hr/>
<endpoint module="luxe: audio" class="Bus" signature="set_channels(bus : AudioBus, value : Num)"></endpoint>
<signature id="Bus.set_channels+2">Bus.set_channels(**bus**: `AudioBus`, **value**: `Num`)
<a class="headerlink" href="#Bus.set_channels+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the number of channels for the bus   

<endpoint module="luxe: audio" class="Bus" signature="set_volume(bus : AudioBus, value : Num)"></endpoint>
<signature id="Bus.set_volume+2">Bus.set_volume(**bus**: `AudioBus`, **value**: `Num`)
<a class="headerlink" href="#Bus.set_volume+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the volume for the bus   

<endpoint module="luxe: audio" class="Bus" signature="get_volume(bus : AudioBus)"></endpoint>
<signature id="Bus.get_volume">Bus.get_volume(**bus**: `AudioBus`)
<a class="headerlink" href="#Bus.get_volume" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Get the volume for the bus   

