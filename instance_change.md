# instance_change(object obj, boolean perform_object_events)

### Supported Game Maker Language
`Game Maker Language 2`

## Syntax

```
void instance_change(object obj, boolean perform_object_events);
```

## Arguments

|Argument             |Type   |Description                                                                       |
|---------------------|-------|----------------------------------------------------------------------------------|
|obj                  |Object |The new object to change into                                                     |
|perform_object_events|Boolean|Whether to perform the new object's create and the original objects destroy event.|

## Returns

```
N/A
```

## Description

You can use this function to change one instance of an object into another instance of a different object, and while doing so decide whether to perform the initial instances Destroy and Clean Up Events and the new instances Create Event. In this way, you can have (for example) a bomb change into an explosion - in which case the "perf" argument would probably be true as you would want the bomb to perform its Destroy Event and Clean Up Event, as well as the explosion to perform its Create Event - or you could have your player character change into a different one - in which case the "perf" argument would probably be false as you do not want the instances to perform their Create and Destroy/Clean Up events.

It is worth noting that changing the instance means that you should perform no further actions with that instance until the next step, in particular trying to access variables etc... as that will cause an error. Basically, you change the instance but it is not actually available until the end of the current step, so to access any of the variables it contains directly (for example, calling `obj_Changed.x`) will not work.

#### Warning!

> When changing a physics enabled instance, the physical properties will not be carried over to the new instance being changed into. Therefore you should have code in place to "transfer" the physics state of the current instance over to the new instance, or have defined the new instances physical properties in its Create Event, or in the object editor. For this reason it is recommended that you not use this function with physics enabled instances, but rather use a combination of instance_destroy() and instance_create().


## Examples

#### Example 1

*Changes the calling instead into `obj_Player_Swimming` without performing the original instance destroy event, nor the new instances create event.*

```
if(keyboard_check(vk_enter)) {
  instance_change(obj_Player_Swimming, false);
}
```