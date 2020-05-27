# instance_id[index]

*Returns the id of an instance in the room.*

### Supported Game Maker Language

`Game Maker Language 2`

## Description

This **read only** array holds all the ids of every active instance within the room. This means that if you have used any of the instance_deactivate functions those instances that have been deactivated will not be included in this array (if you have used a value from this array previously, it will now return the keyword noone).

## Syntax

```
instance_id[index];
```

## Arguments

|Argument|Example|Description                            |
|--------|-------|---------------------------------------|
|index   |10004  |The id of the instance you wish to grab|

## Returns

Integer

## Examples

#### Example 1

> loop through all instances within the room and add `0.1` to their speed*

```
var i;
for(i = 0; i < instance_count; i += 1) {
  with(instance_id[i]) {
    speed += 0.1;
  }
}
```