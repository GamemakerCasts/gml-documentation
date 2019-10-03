# instance_copy(boolean perform_object_events)

### Supported Game Maker Language

`Game Maker Language 2`

## Description

With this function you can "clone" an instance as this will create a new version of the instance running the code at its same position. The "perf" argument is used to instruct this new instance to perform the create event or not. This function returns the `id` of the new instance which can then be stored in a variable or used to access that instance.

### Notes

> If you choose not to perform the create event, you may encounter errors if the instance depends on any variables initialised in this event

## Syntax

```
Object instance_copy(boolean perform_object_events);
```

## Arguments

|Argument             |Type   |Description                                                                      |
|---------------------|-------|---------------------------------------------------------------------------------|
|perform_object_events|Boolean|Whether to perform the new object's create and the original objects destroy event|

## Returns

Object

## Examples

#### Example 1

```
var instance = instance_number(object_index);
if(instance < 10) {
  instance_copy(true);
}
```