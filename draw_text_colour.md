# draw_text_colour(float x, float y, string text, colour c1, colour c2, colour c3, colour c4, float alpha)

*Draw a string at a given position with a colour gradient*

### Supported Game Maker Language
`Game Maker Language 2`

## Syntax

```
void draw_text_colour(float x, float y, string text, colour c1, colour c2, colour c3, colour c4, float alpha);
```

## Arguments

|Argument|Type   |Description                                           |
|--------|-------|------------------------------------------------------|
|x       |float|X coordinate                                          |
|y       |float|Y coordinate                                          |
|text    |String |String to draw                                        |
|c1      |Color  |The colour for the top left of the drawn text         |
|c2      |Color  |The colour for the top right of the drawn text        |
|c3      |Color  |The colour for the bottom right of the drawn text     |
|c4      |Color  |The colour for the bottom left of the drawn text      |
|alpha   |Float  |Alpha value for the text (0 = transparent, 1 = opaque)|

## Returns

```
N/A
```

## Description

This function will draw text in a similar way to draw_text only now you can choose the colours to use for colouring the text as well as the alpha value, and these new values will be used instead of the base drawing colour and alpha

***NOTE:** Gradient blending is not available for the HTML5 target unless WebGL is enabled, although you can still set the blending colours and it will blend the font with the first given colour. However all blending in this way creates a duplicate font which is then stored in the cache and used when required, which is far from optimal and if you use multiple colour changes it will slow down your games performance. You can set the font cache size to try and limit this should it be necessary using the function font_set_cache_size.*

## Examples

#### Example 1

*draw two sections of text on the same line, with the first text being drawn white (as that is the base drawing colour) and the second text being drawn with a lime green to normal green gradient*

```
draw_set_colour(c_white);
draw_text(100, 100, "Health");
draw_text_colour(100, 200, string(health), c_lime, c_lime, c_green, c_green, 1);
```