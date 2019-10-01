# instance_place(x, y, object)

### Supported Game Maker Language
`Game Maker Language 2`

## Description

With this function you can check a position for a collision with another instance or all instances of an object using the collision mask of the instance that runs the code for the check. When you use this you are effectively asking GameMaker Studio 2 to move the instance to the new position, check for a collision, move back and tell you if a collision was found or not. This will work for precise collisions, but only if both the instance and the object being checked for have precise collision masks selected otherwise only bounding box collisions are applied. this function will return the unique instance id of the object being collided, but if that is not needed it is slightly faster to use the function `place_meeting`. This function also accepts the special keywords all and other and will return the keyword noone if no collision occurs, or the unique instance ID value of the instance found if a collision does occur.

### Notes
> Note that the given x/y coordinates will be rounded to the nearest integer before the check is performed, so if this is not what you require (or you have been using a legacy GameMaker product), you should floor the coordinates in the check: `instance_place(floor(x), floor(y), obj_Enemy)`.

## Syntax

```
instance_place(x, y, object)
```

## Arguments

|Argument|Example |Description                          |
|--------|--------|-------------------------------------|
|x       |100     |The x position to check for instances|
|y       |275     |The y position to check for instances|
|object  |obj_Coin|The object to check for              |

## Returns

- **noone** is returned if no instance was found at the given x/y coordinates
- **Integer** is returned if there was an instance found at the given x/y coordinates. This is the instance's `id`.

## Examples

#### Example 1

> Check to see if there was a collision with `obj_Enemy` and if there was one, reduce the HP variable stored on the calling instance and then destroy the collided instance.

```
var instance = instance_place(x, y, obj_Enemy);
if(instance != noone) {
  hp -= instance.dmg;
  with(instance) {
    instance_destroy();
  }
}
```