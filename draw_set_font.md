# draw_highscore(int x1, int y1, int x2, int y2)

*Draws the highscore table string in the room filling the indicated box size using the currently set font and draw colour*

### Supported Game Maker Language
`Game Maker Language 2`

## Syntax

```
void draw_highscore(int x1, int y1, int x2, int y2);
```

## Arguments

|Argument|Type   |Description                                                       |
|--------|-------|------------------------------------------------------------------|
|x1      |Integer|The x coordinate of the left position of the highscore rectangle  |
|y1      |Integer|The y coordinate of the top position of the highscore rectangle   |
|x2      |Integer|The x coordinate of the right position of the highscore rectangle |
|y2      |Integer|The y coordinate of the bottom position of the highscore rectangle|

## Returns

```
N/A
```

## Description

This simple function will draw the current list of internally stored high scores using the currently set font, colour and alpha values within the specified rectangle. You provide the coordinates for the upper left corner and lower right corner of the rectangular area to draw the text, and GameMaker: Studio will take care of the rest, with spacing and position being done automatically.

## Examples

#### Example 1

*This would draw the highscore table in a rectangle in the middle of the room with a 100px border*

```
draw_highscore(100, 100, room_width - 100, room_height - 100);
```