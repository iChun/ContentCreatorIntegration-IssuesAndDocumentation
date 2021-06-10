Repeat Outcome
============= 

## Description

An outcome that repeatedly attempts an outcome. This Outcome is Client-side only.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `repeat`       |         Not seen in the Editor.        |
| *`times`*[^1] | String |      How many times to repeat the outcome? The iteration count is stored in the `$iteCount` variable.       |                 |
| *`arrayVariable`*[^1] | String |      Variable to pull an array. If this is used, `times` is ignored, and the array will be looped through instead. The array content being looped through will be put in the `$arrayObject` variable and removed once it is done. The iteration count is stored in the `$iteCount` variable.       |                 |
| *`outcome`* | Outcome |      The outcome to repeat       |                 |
| `breakCondition` | Condition |      A condition, if met, breaks the loop cycle.       |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
[^1]: Either field is required for the Object to be valid.
