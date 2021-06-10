Inventory Outcome
============= 

## Description

Manipulate the inventories of a set of entities matching the target selector.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `inventory`       |         Not seen in the Editor.        |
| *`target`* | String |      The target selector for the entities to affect.       |                 |
| *`funcType`* | String |      Available types: `drop`, `swap`, `amount`, `delete`, `playerSwap`, `add`       |                 |
| *`index`* | String |      The index/slot number for the inventories. Used by all types except `playerSwap`.        |    For reference, it should be: `0-35` for Main Inventory, `36-39` for Armor, `40` for Off hand, `41+` for modded inventories. For some funcs, `-1` means current item.             |
| *`additionalArgs`* | String |      Additional arguments: Read below.       |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  

## Additional Arguments

| Type ID      | Function                                   | Argument |
| ------------ | ------------------------------------------ | -------- |
| `drop`       | Drops item                                 |   The item stack count       |
| `swap`       | Swaps item with another slot               |     The index/slot to swap with     |
| `amount`     | Change item's stack size                   |     The amount to increase/decrease the stack by     |
| `delete`     | Deletes item                               |   The item stack count       |
| `playerSwap` | Swaps entire inventory with another player |     The target selector for the other player     |
| `add`        | Adds new item                              |   A string denoting what item to give and the count. Essentially the bit after `/give <target> ` in the `give` command, like `minecraft:dirt 3` gives 3 dirt blocks       |
