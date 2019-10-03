# draw_set_valign(alignment valign)

*Aligns any subsequently drawn text vertically*

### Supported Game Maker Language

`Game Maker Language 2`

## Description

This function is used to align text along the vertical axis and changing the vertical alignment will change the position and direction in which all further text is drawn, with the default value being fa_top.

## Syntax

```
void draw_set_valign(alignment valign);
```

## Arguments

|Argument|Type      |Description       |
|--------|----------|------------------|
|valign  |Alignment|Vertical alignment|

## Returns

```
N/A
```

## Alignment
|Constant |Alignment                                                                                           |
|---------|----------------------------------------------------------------------------------------------------|
|fa_top   |![](https://docs.yoyogames.com/source/dadiospice/002_reference/drawing/drawing%20text/fa_top.png)   |
|fa_middle|![](https://docs.yoyogames.com/source/dadiospice/002_reference/drawing/drawing%20text/fa_middle.png)|
|fa_bottom|![](https://docs.yoyogames.com/source/dadiospice/002_reference/drawing/drawing%20text/fa_bottom.png)|

## Examples

#### Example 1

*draw the score centered around the very center of the text*

```
draw_set_halign(fa_center);
draw_set_valign(fa_middle);
draw_text(100, 32, "Score: " + string(score));
```