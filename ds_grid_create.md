# ds_grid_create(int width, int height)

*Creates a new grid.*

### Supported Game Maker Language
`Game Maker Language 2`

## Syntax

```
integer ds_grid_create(int width, int height);
```

## Arguments

|Argument|Type   |Description                         |
|--------|-------|------------------------------------|
|width   |Integer|The width of the grid to be created |
|height  |Integer|The height of the grid to be created|

## Returns

Integer

## Description

With this function you can create a new ds_grid data structure of the specified cell width and height. This function returns an id which must be used in all further functions that deal with this ds_grid.

All of the values in the grid will be automatically set to `0`

## Examples

#### Example 1

*This creates a grid 10 cells high and 10 cells wide*

```
my_grid = ds_grid_create(10, 10);
```