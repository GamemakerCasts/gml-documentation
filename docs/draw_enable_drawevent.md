# draw_enable_drawevent(bool enable)

*Enables or disables the draw event.*

### Supported Game Maker Language

`Game Maker Language 2`

## Description

With this function you can choose to enable (true) or disable (false) the draw event for all instances in the game, thus giving you control over how and when things are draw, useful if you wish to implement a "frame skip" technique. Note that this doesn't just prevent instances drawing to the screen, it suppresses the draw event completely meaning that care should be taken since any game logic that is present in that event will not be run either.

## Syntax

```
void draw_enable_drawevent(bool enable);
```

## Arguments

|Argument|Type   |Description                                       |
|--------|-------|--------------------------------------------------|
|enable  |Boolean|Enable or disable the draw event for all instances|

## Returns

```
N/A
```

## Examples

#### Example 1

*Checks a variable and if it returns true, it enables the draw event, otherwise the draw event is disabled*

```
frame_skip ++;
if(frame_skip mod 5 == 0) {
  draw_enable_drawevent(true);
} else {
  draw_enable_drawevent(false);
}
```