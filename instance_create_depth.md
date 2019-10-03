# instance_create_layer(float x, float y, integer depth, object obj)

### Supported Game Maker Language

`Game Maker Language 2`

## Description

With this function you can create a new instance of the specified object at any given point within the room and at the depth specified. The depth can be any value, where the lower the depth the "nearer" to the camera things will be drawn and the higher the depth the further away, so an instance at depth -200 will be drawn over an instance at depth +300 (for example). Note that this function will actually create a room layer for the instance, since all instances must be on a layer in the room, but since this is a managed layer (ie: not one that you have created through code or in the room, but one that GameMaker Studio 2 has created automatically) you cannot access it, and the `layer` instance variable will return -1.

This function returns the `id` of the new instance which can then be stored in a variable or used to access that instance. Note that this function will also call the Create Event of the instance being created before continuing with the code or actions for the event that called the function

### Important!

> There is a minimum and maximum layer depth of `-16000` to `16000`. Anything placed on a layer outside that range will not be drawn although all events will still run as normal

## Syntax

```
Integer instance_create_layer(float x, float y, integer depth, object obj)
```

## Arguments

|Argument|Type   |Description                                 |
|--------|-------|--------------------------------------------|
|x       |Float  |The x position the object will be created at|
|y       |Float  |The y position the object will be created at|
|depth   |Integer|The depth to assign the instance            |
|obj     |Object |The object to create                        |

## Returns

Integer


## Examples

#### Example 1

Create a bullet at the current x and y location of the calling instance.
```
var instance = instance_create_depth(x, y, -1000, obj_Bullet);
```