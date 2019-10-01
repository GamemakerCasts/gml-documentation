# instance_position(x, y, object)

### Supported Game Maker Language
`Game Maker Language 2`

## Description

With this function you can check a position for a collision with another instance or all instances of an object. When you use this you are checking a single point in the room for an instance or an object. This check will be done against the bounding box of the instance or against the mask of the instance if that instance has precise collisions checked and will return the unique instance id. If you do not need the id of the colliding instance you should consider using `position_meeting` instead. This function also accepts the special keywords `all` and `other` and will return the keyword noone if no collision occurs or the unique ID value of the instance found if a collision does occur.

## Syntax

```
instance_position(x, y, object)
```

## Arguments

|Argument|Example  |Description                          |
|--------|---------|-------------------------------------|
|x       |100      |The x position to check for instances|
|y       |200      |The y position to check for instances|
|object  |obj_Solid|The object to check for              |

## Returns

- **noone** is returned if no instance was found at the given x/y coordinates
- **Integer** is returned if there was an instance found at the given x/y coordinates. This is the instance's `id`.

## Examples

#### Example 1

> Check to see if the mouse cursor is over the object `obj_Pause_Button` and if it is the we set the image index to a new value

```
var instance = instance_position(x, y, obj_Pause_Button);
if(instance != noone) {
  with(instance) {
    image_index = 1;
  }
}
```