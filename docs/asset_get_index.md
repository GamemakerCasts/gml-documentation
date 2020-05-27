# asset_get_index()

*Returns the unique index of the game asset with the given name*

### Supported Game Maker Language

`Game Maker Language 2`

## Description

You can use this function to get the unique identifying index for a game asset from its name. If the asset is not found, the function will return a value of -1, otherwise it will return the unique index id for the asset being checked. This id can then be used in other functions as you would any other index value, like the sprite_index or the path_index, for example. Please note that although this function can be used to reference assets from strings (see example below) you should always make sure that the asset exists before using it otherwise you may get errors that will crash your game.

## Syntax

```
real asset_get_index(name);
```

### Notes
> Script names will not resolve as assets on the HTML5 target platform due to obfuscation of the final code, which may cause issues and should be taken into consideration when using the function.

## Arguments

|Argument|Type    |Description                                                                                   |
|--------|------- |--------------------------------------------------------------------------------------------- |
|name    |String  |The name of the game asset to get the index of                                                |

## Returns

Real

## Examples

#### Example 1

*The following code would will try to find an object of obj_Enemy_X and if it exists, then it will create it*

```
for(var index = 0; index < 10; index ++) {
    var instance = asset_get_index("obj_Enemy_" + string(index));

    if(instance != -1) {
        var position_x = random_range(0, room_width);
        var position_y = random_range(0, room_height);

        instance_create_depth(position_x, position_y, 10, instance);
    }
}
```