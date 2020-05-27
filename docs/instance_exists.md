# instance_exists(object)

### Supported Game Maker Language

`Game Maker Language 2`

## Description

This function can be used in two ways depending on what you wish to check. You can give it an object_index to check for, in which case this function will return true if any active instances of the specified object exist in the current room, or you can also supply it with an instance id, in which case this function will return true if that specific instance exists and is active in the current room

### Notes
> This function does not take into account those instances that have been deactivated using the `instance_deactivate` functions

## Syntax

```
instance_exists(object)
```

## Arguments

|Argument     |Example    |Description                        |
|------------ |---------- |-----------------------------------|
|object       |obj_Player |The instance to check for existance|

## Returns

Boolean

## Examples

#### Example 1

> Check the room to see if there are any instances of `obj_Enemy`

```
if(! instance_check(obj_Enemy)) {
  // there are no enemies left in the room
}
```