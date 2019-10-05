# ads_get_display_height(integer num)

*This function gets the height of the currently displaying ad.*

### Supported Game Maker Language

`Game Maker Language 2`

## Description

With this function you can get the height of the ad box defined for the ads enabled by the `ads_enable` function.

## Syntax

```
real ads_get_display_height(integer num);
```

## Arguments

|Argument|Type|Description             |
|--------|----|----------------------- |
|num    |Integer|The advert number to display (0 - 4).|

## Returns

Real

## Examples

#### Example 1

> set an advert to display at the bottom left-hand corner of the display.

```
ads_move(0, display_get_gui_height() - ads_get_display_height(0), 0);
```