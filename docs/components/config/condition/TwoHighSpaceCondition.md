Two High Space Condition
============= 

## Description

Finds for a two block high air space around a target (customisable). Works similarly to the spreadplayers command. Condition fails if we cannot find one after the defined number of tries.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `freeSpace`       |         Not seen in the Editor.        |
| *`target`* | String |      Target selector string to target.       |                 |
| *`horiRadius`* | String |      Horizontal radius the check.       |                 |
| *`vertRadius`* | String |      Vertical radius to check. Make sure two of this is higher than `customHeight`.       |                 |
| *`tries`* | String |      How many tries (horizontally) we try and check. Try not to put this too excessively high.       |                 |
| *`variableName`* | String |      Variable name to put the result into.       |                 |
| `customHeight` | String |      Custom Height. If left out, defaults to `2`. Make sure two of `vertRadius` is higher than this number.       |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
