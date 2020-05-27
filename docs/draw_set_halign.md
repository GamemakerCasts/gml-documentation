# draw_set_halign(alignment halign)

*Aligns any subsequently drawn text horizontally*

### Supported Game Maker Language
`Game Maker Language 2`

## Description

This function is used to align text along the horizontal axis and changing the horizontal alignment will change the position and direction in which all further text is drawn with the default value being fa_left.

## Syntax

```
void draw_set_halign(alignment halign);
```

## Arguments

|Argument|Type      |Description         |
|--------|----------|--------------------|
|halign  |Alignement|Horizontal alignment|

## Returns

```
N/A
```

## Alignment
|Constant |Alignment                                                                                           |
|---------|----------------------------------------------------------------------------------------------------|
|fa_left  |![](https://docs.yoyogames.com/source/dadiospice/002_reference/drawing/drawing%20text/fa_left.png)  |
|fa_center|![](https://docs.yoyogames.com/source/dadiospice/002_reference/drawing/drawing%20text/fa_center.png)|
|fa_right |![](https://docs.yoyogames.com/source/dadiospice/002_reference/drawing/drawing%20text/fa_right.png) |

## Examples

#### Example 1

*draw two strings on the same line, with the score being left-hand aligned and the health being right-hand aligned*

```
draw_set_halign(fa_left);
draw_text(100, 32, "Score: " + string(score));
draw_set_halign(fa_right);
draw_text(room_width - 100, 32, "Health: " + string(health));
```