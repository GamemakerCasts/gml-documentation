# abs(float value)

*Returns the absolute value*

### Supported Game Maker Language
`Game Maker Language 2`

## Syntax

```
float abs(float value);
```

## Arguments

|Argument|Type  |Description                                                |
|--------|------|-----------------------------------------------------------|
|value   |Float |Value to be converted into the absolute number             |

## Returns

Float

## Description

This function returns the absolute value of the input argument, so if it's a positive value then it will remain the same, but if it's negative it will be multiplied by -1 to make it positive.

## Examples

#### Example 1

*This will add an amount equal to the absolute value of the current x position of the instance and the mouse x position*

```
x += abs(x - mouse_x);
```