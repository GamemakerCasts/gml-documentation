# angle_difference(float angle_1, float angle_2)

*Returns the difference between two angles*

### Supported Game Maker Language
`Game Maker Language 2`

## Syntax

```
float angle_difference(float angle_1, float angle_2);
```

## Arguments

|Argument|Type |Description     |
|--------|-----|----------------|
|angle_1 |Float|The first angle |
|angle_2 |Float|The second angle|

## Returns

Float

## Description

This function will return the smallest angle difference between two angles as a value between -180 and 180 degrees (where a positive angle is anti-clockwise and a negative angle clockwise).

## Examples

#### Example 1

*Get the angle of direction from the instance to the mouse cursor, then get the difference between that angle and the current image_angle, using this value to slowly rotate towards the mouse*

```
var pd = point_direction(x, y, mouse_x, mouse_y);
var dd = angle_difference(image_angle, pd);
image_angle -= min(abs(dd), 10) * sign(dd);
```