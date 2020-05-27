# instance_number(object)

### Supported Game Maker Language

`Game Maker Language 2`

## Description

With this function you can find out how many active instances of the specified object exists in the room. Please note that those instances which have been deactivated with the `instance_deactivate` functions will not be included in this check.

## Syntax

```
instance_number(object)
```

## Arguments

|Argument|Example         |Description                            |
|--------|----------------|---------------------------------------|
|Object  |obj_Collectables|The object to get the total number from|

## Returns

Integer

## Examples

#### Example 1

> Check to see if there is less than 50 enemies in the room. If there is less than 50, create another one

```
if(instance_count(obj_Enemy) < 50) {
  instance_create_layer(random(room_width), random(room_height), "Instances", obj_Enemy);
}
```