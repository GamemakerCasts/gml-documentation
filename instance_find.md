# instance_find(object, [index])

### Supported Game Maker Language
`Game Maker Language 2`

## Description

All instances have a unique identifier (`id`) which can be used to modify and manipulate them while a game is running, but you may not always know what the id for a specific instance is and so this function can help as you can use it to iterate through all of them to find what you need. You specify the object that you want to find the instance of and a number, and if there is an instance at that position in the instance list then the function returns the id of that instance, and if not it returns the special keyword noone. You can also use the keyword all to iterate through all the instances in a room, as well as a parent object to iterate through all the instances that are part of that parent / child hierarchy and you can even specify an instance itself (if you have its id) as a check to see if it actually exists in the current room. Please note that as instances are sorted in an arbitrary manner, there is no specific order to how the instances are checked by this function, and any instance can be in any position.

The maximum value for "n" in this function would be
 - For the keyword all: `instance_count - 1`
 - For an object index: `instance_number(obj) - 1`


## Syntax

```
instance_find(object, [index])
```

## Arguments

|Argument     |Example      |Description                             |
|------------ |------------ |----------------------------------------|
|obj          |obj_Treasure |The object to find the `n`th instance of|
|index        |0            |The instance index to find of the object|

## Returns

Integer

## Examples

#### Example 1

> This code will find all instances of `obj_Enemy` and print their id on the screen

```
/// draw event
for(var i = 0; i < instance_code(obj_Enemy); i ++) {
  draw_text(10, 10 * i, instance_find(obj_Enemy, i));
}
```