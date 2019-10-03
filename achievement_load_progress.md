# achievement_load_progress()

*Get achievement data from the service provider*

### Supported Game Maker Language

`Game Maker Language 2`

## Description

This function will send a request to the server for information on all available achievements. It will trigger a callback Social Asynchronous Event which contains the async_load map populated with the relevant key/value pairs. The id key of this ds_map is used to identify the correct callback (there can be more than one trigger function for any given asynchronous event), and will be paired with the constant achievement_achievement_info as well as a number of other key/value pairs for each player.

The exact contents of the map are shown below

|Key           |Description                                                                                              |
|--------------|---------------------------------------------------------------------------------------------------------|
|**id**        |For this function it should be *achievement_achievement_info*                                            |
|**numentries**|The number of achievements in the list.                                                                  |
|**AchN**      |The name of the achievement, where "N" is an integer value corresponding to its place in the entries list|
|**AchCompN**  |How complete the achievement "N" is as a percentage value from 0 to 100 (a string)                       |


## Syntax

```
void achievement_load_progress();
```

## Arguments

```
N/A
```

## Returns

```
N/A
```

## Examples

#### Example 1

*The following code would request achievement progress when the user is on an iOS device*

```
if (os_type == os_ios) {}
  achievement_load_progress();
}
```

This will send off a request for the information on achievements and generate an asynchronous callback with the special async_load ds_map containing the following data

```
var ident = ds_map_find_value(async_load, "id");
if (ident == achievement_achievement_info) {
  var numentries = ds_map_find_value(async_load, "numentries");
  for(var i = 0; i < numentries; i++) {
    ach_id[i] = ds_map_find_value(async_load, "Ach" + string(i));
    comp[i] = ds_map_find_value(async_load, "AchComp" + string(i));
   }
}
```