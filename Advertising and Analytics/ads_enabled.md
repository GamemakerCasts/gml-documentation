# ads_enabled(real x, real y, int slot)

*This code enables ads in your game room.*

### Supported Game Maker Language

`Game Maker Language 2`

## Description

With this function you can display selected ads at the given position within the GUI. The "num" that you supply is the number of the advertising key that you wish to use as defined in the **Global Game Settings - Advertising Tab**, and will generate and advert of the size specified for that key.

## Syntax

```
void ads_enabled(real x, real y, int slot);
```

## Arguments

|Argument|Type   |Description                         |
|--------|-------|------------------------------------|
|x       |Real|X position in the room              |
|y       |Real|Y position in the room              |
|slot    |Integer|The advert "slot" to display (0 - 4)|

## Returns

```
N/A
```

## Examples

#### Example 1

> Enables the ad slot 1 in position (0, 0)*

```
ads_enable(0, 0, 1);
```