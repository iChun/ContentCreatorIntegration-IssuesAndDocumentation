Conditional Condition
============= 

## Description

A condition, that if passes or fails, triggers a specific condition. A pre-check if you want.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `conditional`       |         Not seen in the Editor.        |
| *`condition`* | Condition |      The condition to check first.       |                 |
| *`passCondition`* | Condition |      If the condition passes, return this condition's result.       |                 |
| `failCondition` | Condition |      If the condition fails, return this condition's results. Optional. Will return false if the condition is not met and this is not set.       |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
