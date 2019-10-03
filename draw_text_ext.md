# draw_text_ext(real x, real y, string text, real distance, real width)

*Draws a string at a given position with a specific spacing and within a limited area*

### Supported Game Maker Language

`Game Maker Language 2`

## Description

This function will draw text in a similar way to draw_text only now you can set the space between each line of text - should the text occupy more than one line - and limit the width (in pixels) of the string per line so that should any line exceed this value, GameMaker: Studio will automatically split the text to the next line. A value of -1 for the line separation argument will default to a separation based on the height of the "M" character in the chosen font

## Syntax

```
void draw_text_ext(real x, real y, string text, real distance, real width)
```

## Arguments

|Argument|Type  |Description                                                |
|--------|------|-----------------------------------------------------------|
|x       |Real |X coordinate                                               |
|y       |Real |Y coordinate                                               |
|text    |String|String to draw                                             |
|distance|Real |Distance in pixels between the lines of text               |
|width   |Real |The maximum width in pixels of the string before a new line|

## Returns

```
N/A
```

## Examples

#### Example 1

*draw whatever text the user types into the keyboard, splitting it onto new lines every time the string length for that line exceeds 300 pixels. the code will also maintain a separation of 3 pixels between lines should this occur*

```
draw_text_ext(100, 50, keyboard_string, 3, 300);
```