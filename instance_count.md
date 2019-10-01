# instance_count

*Returns the total number of instances currently active in the room.*

### Supported Game Maker Language
`Game Maker Language 2`

## Syntax

```
int instance_count;
```

## Arguments

N/A

## Returns

Integer

## Description

With this **read only** variable you can get a count of all active instances that are in the room. This will include the instance running the code, but does not include those instances that have been deactivated using the instance_deactivate functions. Note that this function will only give you the number of instances at the start of the step, so any changes to the instances in the room made after the step has started will not be taken into consideration.

## Examples

#### Example 1

*Will create instances of `obj_Star` on the `Instances` layer until the total instance count reached 100*
```
if(instance_count < 100) {
  var difference = 100 - instance_count;
  while(--differences > 0) {
    instance_create_layer(random(room_width), random(room_height), "Instances", obj_Star);
  }
}
```