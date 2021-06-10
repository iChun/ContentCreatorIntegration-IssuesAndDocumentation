Array Explode Condition
============= 

## Description

Explodes the array into a different variable per object. Fails if the variable isn't an array.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `arrayExplode`       |         Not seen in the Editor.        |
| *`variableName`* | String |      The name of the variable that stores the array.       |                 |
| *`variableOutputName`* | String |      The name of the variable to store the results.        |    Size of array will be stored in variable `<name>Length`, and each individual object will be stored in variable `<name>0...(length-1)`            |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
