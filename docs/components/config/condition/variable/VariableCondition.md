Variable Condition
============= 

## Description

Use this to check the value of a specific variable.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `variableCheck`       |         Not seen in the Editor.        |
| *`variableName`* | String |      The name of the variable you are targeting.       |                 |
| *`variableResult`* | String |      The result you are hoping to match with. If you are looking to see if this is contained in within the variable result, use MessageCondition instead with optionalVariableName set.       |                 |
| `caseSensitive` | Boolean |      Be case sensitive?       |                 |
| `isGlobal` | Boolean |      Check from global variables.       |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
