# sound_volume(index, value)

> Sets the volume of a given sound

### Supported Game Maker Language

`Game Maker Language 2`

## Description

With this function you can change the volume of a given sound. This will change hte volume for `all` further instances where the indexed sound is played.

The volume can be set between 0 *(slient)* and 1 *(full volume)*, with the value of `1` being the default volume for the sound unless it has been previously changed in the `sound resource`.

The volume scale is **logarithmic** in nature, so a volume of *0.5* is **not** half volme, as illustrated by the image below.

![](https://docs.yoyogames.com/source/dadiospice/002_reference/game%20assets/sounds/legacy%20sound/sound_volume.png)

## Syntax

```
sound_volume(index, value)
```

## Arguments

|Argument|Example  |Description                              |
|--------|---------|-----------------------------------------|
|index   |snd_Music|The sound index to change the volume of  |
|value   |0.5      |The new volume level, between `0` and `1`|

## Returns

> N/A

## Examples

#### Example 1

> The example will check for a key press and lower the music by 0.1 until it is silenced.

```
if(keyboard_check_pressed(vk_down)) {
    if(vol < 0) {
        vol += 0.1;
    }

    sound_volume(snd_Music, vol);
}
```