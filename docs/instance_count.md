# instance_count

*Returns the total number of instances currently active in the room.*

### Supported Game Maker Language

`Game Maker Language 2`

## Description

With this **read only** variable you can get a count of all active instances that are in the room. This will include the instance running the code, but does not include those instances that have been deactivated using the instance_deactivate functions. Note that this function will only give you the number of instances at the start of the step, so any changes to the instances in the room made after the step has started will not be taken into consideration.

## Syntax

```
int instance_count;
```

## Arguments

N/A

## Returns

Integer

## Examples

#### Example 1

> If there is less than 100 instances in the room, then create a instance of obj_Star and keep creating them until there are 100 instances total.

```
/// Step event
if(instance_count < 100) {
  var random_x = random(room_width);
  var random_y = random(room_height);
  
  instance_create_layer(random_x, random_y, "Instances", obj_Star);
}
```

![placeholder](https://via.placeholder.com/400x200/9ABCA7/000000/?text=Click+to+run+example)
