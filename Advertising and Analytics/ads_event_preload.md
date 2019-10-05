# ads_event_preload(string placement)

*Preload a PlayHaven ad placement, ready to be shown.*

### Supported Game Maker Language

`Game Maker Language 2`

## Description

This function will preload a PlayHaven ad into memory, ready for it to be shown when the `ads_event` calls the placement used (both functions require the same placement name string to work. If you know that after a certain time or at a certain point in your game you are going to be calling a PlayHaven content placement, then this function can be called beforehand so as to make the user experience as smooth as possible.

### Notes

> This function will not show the ad! It only loads it into memory.

## Syntax

```
void ads_event_preload(placement);
```

## Arguments

|Argument|Type|Description             |
|--------|----|----------------------- |
|placement    |String|The PlayHaven placement name (a string)             |

## Returns

N/A

## Examples

#### Example 1

> Preload an ad from PlayHaven for the placement named "game_start".

```
ds_event_preload("game_start");
```