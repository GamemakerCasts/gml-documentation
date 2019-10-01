# instance_destroy([id, perform_event])

### Supported Game Maker Language
`Game Maker Language 2`

## Description

You call this function whenever you wish to "destroy" an instance, normally triggering a Destroy Event and also a Clean Up event. This will remove it from the room until the room is restarted (unless the room is persistent).

You can call this function with no `parameters` which will destroy the instance that made the call.

## Syntax

```
instance_destroy([id, perform_event])
```

## Arguments

|Argument|Example|Description                                          |
|--------|-------|-----------------------------------------------------|
|id|obj_Enemy|The object you would like to destroy                 |
|perform_event|false|Perform the destroy event or not. `* default is true`|

## Returns

```
N/A
```

## Examples

#### Example 1

> Destroy the instance running the code without calling the destroy event if the instance is outside of the boundaries.
```
if((x < 0) || (x > room_width) || (y < 0) || (y > room_height)) {
  instance_destroy(id, false);
}
```