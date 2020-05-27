# draw_text(real x, real y, string text)

*Draw a string at a given position*

### Supported Game Maker Language

`Game Maker Language 2`


## Description

With this function you can draw any string at any position within the room (for drawing real numbers you should use the string function to convert them into text). To combine strings you can use + (see example below), you can also use # to add a line break to the string (should you need to display the # symbol, then you should precede it with a backslash like this "this will draw a \#") and you can also draw quotations by using inverted commas (for example 'I said "Hello"...'). The colour of the text and the alpha are governed by the current base alpha and colour values as set by draw_set_alpha and draw_set_colour.

### Notes

> The actual position of the text will be influenced by the alignment values set by draw_set_halign and draw_set_valign


## Syntax

```
void draw_text(real x, real y, string text);
```

## Arguments

|Argument|Type   |Description   |
|--------|-------|--------------|
|x       |Real|X coordinate  |
|y       |Real|Y coordinate  |
|text    |String |String to draw|

## Returns

```
N/A
```

## Examples

#### Example 1

*draw a string at the instance x/y position, which will use the string stored in the global variable "Name" and split it over two lines*

```
draw_text(x, y, "Hello, " + global.Name + "!#I hope you are well!");
```