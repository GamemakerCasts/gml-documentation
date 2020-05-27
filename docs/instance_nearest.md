# instance_nearest(x, y, object)

### Supported Game Maker Language

`Game Maker Language 2`

## Description

This function will check all the instances of the given object to see which is nearest to the given point of origin. If no instances of the object exist, the function will return the keyword noone, but if there are instances then it will return the `id` of the instance found. Please note that if the instance running the code was created as an instance of the object being checked, then it will be included in the check.

## Syntax

```
instance_nearest(x, y, object)
```

## Arguments

|Argument|Type     |Description                               |
|--------|---------|------------------------------------------|
|x       |245      |The x position to check for instances from|
|y       |100      |The y position to check for instances from|
|object  |obj_Enemy|The object to check for                   |

## Returns

- **noone** is returned if no instance was found at the given x/y coordinates
- **Integer** is returned if there was an instance found at the given x/y coordinates. This is the instance's `id`.

## Examples

#### Example 1

> Find the nearest instance of `obj_Enemy` and draw a line to it.

```
var instance = instance_nearest(x, y, obj_Enemy);
if(instance != noone) {
  draw_set_color(c_white);
  draw_line(x, y, instance.x, instance.y);
}
```