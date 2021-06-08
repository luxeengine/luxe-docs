#![](../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2021.0.4`)  


---

## `luxe: audio` module

- [Audio](#audio)   

---

### Audio
`:::js import "luxe: audio" for Audio`
> The Audio module let's you play audio.
> 
> `Audio` is a service API, and isn't a modifier system.
> (There will soon be Audio modifiers for placing sounds in the world.)
> 
> Most things in `Audio` work on an instance (handle) of a sound.
> You get one of those from `play` or `loop`, and then can modify or query it.
> It's always safe to call any function on an instance, even if it's finished playing.
> 
> A quick look:
>   
>   ```js
>   //make some sounds available
>   Audio.define_source("sound", "assets/sound.wav")
>   Audio.define_source("music", "assets/music.wav")
> 
>   //play them
>   var sound = Audio.play("sound")
>   var music = Audio.loop("music")
> 
>   //later...
>   Audio.volume(music, 0.5)
> 
>   //later still...
>   Audio.stop(music)
>   ```
> 
> That's it!

- [define_source](#Audio.define_source+2)(**id**: `String`, **asset_id**: `String`)
- [play](#Audio.play+2)(**source**: `String`, **volume**: `Num`)
- [play](#Audio.play)(**source**: `String`)
- [loop](#Audio.loop+2)(**source**: `String`, **volume**: `Num`)
- [loop](#Audio.loop)(**source**: `Any`)
- [stop](#Audio.stop)(**instance**: `AudioInstance`)
- [pan](#Audio.pan+2)(**instance**: `AudioInstance`, **pan**: `Num`)
- [pan_of](#Audio.pan_of)(**instance**: `AudioInstance`)
- [volume](#Audio.volume+2)(**instance**: `AudioInstance`, **volume**: `Num`)
- [volume_of](#Audio.volume_of)(**instance**: `AudioInstance`)
- [pitch](#Audio.pitch+2)(**instance**: `AudioInstance`, **pitch**: `Num`)
- [pitch_of](#Audio.pitch_of)(**instance**: `AudioInstance`)

<hr/>
<endpoint module="luxe: audio" class="Audio" signature="define_source(id : String, asset_id : String)"></endpoint>
<signature id="Audio.define_source+2">Audio.define_source(**id**: `String`, **asset_id**: `String`)
<a class="headerlink" href="#Audio.define_source+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Define an audio source with the name `id`, from the asset `asset_id`.   
> **Unlike other APIs, use a file extension for now, this is a WIP.**
>         
>   ```js
>   Audio.define_source("sound", "assets/sound.wav")
>   ```   

<endpoint module="luxe: audio" class="Audio" signature="play(source : String, volume : Num)"></endpoint>
<signature id="Audio.play+2">Audio.play(**source**: `String`, **volume**: `Num`)
<a class="headerlink" href="#Audio.play+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AudioInstance`
> Plays audio from the specified `source` at volume `volume`.
> Returns a handle to an audio instance that you can modify or stop.
>         
>   ```js
>   Audio.define_source("sound", "assets/sound.wav")
>   Audio.play("sound", 1)
>   ```   

<endpoint module="luxe: audio" class="Audio" signature="play(source : String)"></endpoint>
<signature id="Audio.play">Audio.play(**source**: `String`)
<a class="headerlink" href="#Audio.play" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AudioInstance`
> Plays audio from the specified `source` at volume `1.0`.
> Returns a handle to an audio instance that you can modify or stop.
> 
>   ```js
>   Audio.define_source("sound", "assets/sound.wav")
>   Audio.play("sound")
>   ```   

<endpoint module="luxe: audio" class="Audio" signature="loop(source : String, volume : Num)"></endpoint>
<signature id="Audio.loop+2">Audio.loop(**source**: `String`, **volume**: `Num`)
<a class="headerlink" href="#Audio.loop+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js AudioInstance`
> Begins looping audio for `id` at volume `volume`.
> Returns a handle to an audio instance that you can modify or stop.
> 
>   ```js
>   var music = Audio.loop("music", 1.0)
>   ```   

<endpoint module="luxe: audio" class="Audio" signature="loop(source : Any)"></endpoint>
<signature id="Audio.loop">Audio.loop(**source**: `Any`)
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
>   System.print(Audio.pan_of(sound)) // returns 2.0
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
>   System.print(Audio.volume_of(sound)) // returns 1
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
>   System.print(Audio.pitch_of(sound)) // returns 3
>   ```   

