Target Condition
============= 

## Description

Insert a specific target's information into a variable. Will fail if `target` or `argument` cannot be found.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `target`       |         Not seen in the Editor.        |
| *`target`* | String |      Target selector string to target.       |                 |
| *`argument`* | String |      Arguments: `name`, `uuid`, `health`, `maxhealth`, `armor`, `location[x/y/z]`, `rotation<yaw/pitch>`, `look[x/y/z][number]`, `radius[x/y/z/h][number]`, `biome`, `dim`/`dimension`, `light[block]`, `diff`/`difficulty`, `time`, `day`       |                 |
| *`variableName`* | String |      Variable name to insert the result into.       |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  

## Arguments

The first entity found with the `target` selector will always be used.

| Name                      | Description                                                                                                                                                                                                | Examples                             |
| ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------ |
| `name`                    | Name of the entity.                                                                                                                                                                                        |                                      |
| `uuid`                    | UUID of the entity.                                                                                                                                                                                        |                                      |
| `health`                  | Health of the entity. `-1` if the Entity is not a `LivingEntity`                                                                                                                                           |                                      |
| `maxhealth`               | Max health of the entity. `-1` if the Entity is not a `LivingEntity`                                                                                                                                       |                                      |
| `armor`                   | Armor value of the entity. `-1` if the Entity is not a `LivingEntity`                                                                                                                                      |                                      |
| `location[x/y/z]`         | X, Y, Z coordinates of the entity. If `[x/y/z]` is omitted, all three coordinates will be included in the result with a space in between.                                                                  | `location`, `locationy`, `locationz` |
| `rotation<yaw/pitch>`     | Gets the rotation of the entity, in degrees.                                                                                                                                                               | `rotationyaw`, `rotationpitch`       |
| `look[x/y/z/][number]`    | X, Y, Z values of the entity's look vector, multiplied by number. If `[x/y/z]` is omitted, all three vectors will be included in the result with a space in between. Defaults to `1` if number is omitted. | `look7`, `lookx`, `lookz3`           |
| `radius[x/y/z/h][number]` | Gets a random absolute coordinate around the entity. `h` in `[x/y/z/h]` locks to the horizontal axis. Omitting `[x/y/z/h]` makes it affect all 3 axes.  `[number]` defines distance, defaults to `5`.      | `radius12`, `radiush3`, `radiusy`,   |
| `biome`                   | Gets the registry name for the biome the entity is in.                                                                                                                                                     |                                      |
| `dim`/`dimension`         | Gets the registry name for the dimension the entity is in.                                                                                                                                                 |                                      |
| `light[block]`            | Gets the light level of the entity. `[block]` gets the light level of the block space the entity is standing in instead.                                                                                   |                                      |
| `diff`/`difficulty`       | Gets the difficulty ID of the world the entity is in.                                                                                                                                                      |                                      |
| `time`                    | Gets the time of the world the entity is in.                                                                                                                                                               |                                      |
| `day`                     | Gets the day of the world the entity is in.                                                                                                                                                                |                                      |
