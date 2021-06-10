Input Outcome
============= 

## Description

Pop-up a window that requires the player to input some text. This Outcome is Client-side only.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `input`       |         Not seen in the Editor.        |
| *`text`* | String |      The information text for the pop up.       |                 |
| `defaultInput` | String |      Default text for the input box.       |                 |
| *`variableInput`* | String |      The variable name to put the String from the input box once the player hits Done.       |                 |
| `postInputOutcome` | Outcome |      An outcome to trigger after the player hits Done. Bear in mind that the variable this InputOutcome inserts into is not a global variable and thus will be discarded if not stored in one.       |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
