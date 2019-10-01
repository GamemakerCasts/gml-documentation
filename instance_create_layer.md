# instance_create_layer(float x, float y, string/integer layer, object obj)

### Supported Game Maker Language
`Game Maker Language 2`

## Syntax

```
Object instance_create_layer(float x, float y, string/integer layer, object obj)
```

## Arguments

|Argument|Type          |Description                                 |
|--------|--------------|--------------------------------------------|
|x       |Float         |The x position the object will be created at|
|y       |Float         |The y position the object will be created at|
|layer   |String/Integer|The layer to create the object on           |
|obj     |Object        |The object to create                        |

## Returns

Object

## Description

With this function you can create a new instance of the specified object at any given point within the room and on the layer specified. The layer can be identified using the layer ID value (as returned by the function `layer_create()`) or by the name of the layer (as a string, for example `"instance_layer"`) as defined in the room editor. This function returns the id of the new instance which can then be stored in a variable or used to access that instance. Note that this function will also call the Create Event of the instance being created before continuing with the code or actions for the event that called the function.

### Important!

> There is a minimum and maximum layer depth of `-16000` to `16000`. Anything placed on a layer outside that range will not be drawn although all events will still run as normal


## Examples

#### Example 1

Create a bullet at the current x and y location of the calling instance.
```
var instance = instance_create_layer(x, y, "Instances", obj_Bullet);
```