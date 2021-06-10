Repeat Condition
============= 

## Description

A condition that repeatedly calls a condition. This is for functional conditions. Unconditional.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `repeat`       |         Not seen in the Editor.        |
| *`times`*[^1] | String |      How many times to repeat the condition? The iteration count is stored in the `$iteCount` variable.       |                 |
| *`arrayVariable`*[^1] | String |      Variable to pull an array. If this is used, `times` is ignored, and the array will be looped through instead. The array content being looped through will be put in the `$arrayObject` variable which is removed once it is done. The iteration count is stored in the `$iteCount` variable.       |                 |
| *`condition`* | Condition |      The condition to repeat.       |                 |
| `breakCondition` | Condition |      A condition, if met, breaks the loop cycle.       |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
[^1]: Either is required for the Object to be valid.
