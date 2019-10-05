# ads_disable(integer slot)

*Switch off in game ads.*

### Supported Game Maker Language

`Game Maker Language 2`

## Description

This function switches off the in-game ads for the given "slot" (as defined in the **Global Game Settings - Advertising Tab**), so that they are no longer displayed.

## Syntax

```
void ads_disabled(int slot);
```

## Arguments

|Argument|Type   |Description                         |
|--------|-------|------------------------------------|
|slot    |Integer|The advert "slot" to disable (0 - 4)|

## Returns

N/A

## Examples

#### Example 1

> Switches off ther in game ads for "slot" 0 (zero) if the variable `purchased` returns `true`

```
if(purchased) {
  ads_disabled(0);
}
```