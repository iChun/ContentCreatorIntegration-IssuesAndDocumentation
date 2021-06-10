Message Condition
============= 

## Description

Use this to check for a content in the event's message. The old `VariableCondition`, but more precise.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `message`       |         Not seen in the Editor.        |
| `optionalVariableName` | String |      Do you want to search for a specific variable name? Remove to look for the default variable `message`.       |                 |
| `exactPhrase` | Boolean |      Does this require an exact phrase?       |                 |
| `caseSensitive` | Boolean |      Is this phrase case sensitive?       |                 |
| *`phrase`* | String |      What is the phrase?       |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
