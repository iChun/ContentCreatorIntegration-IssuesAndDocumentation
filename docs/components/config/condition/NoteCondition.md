Note Condition
============= 

## Description

Use this condition to load a note/note array into a variable. It will fail if the note/note array doesn't exist. Put note conditions higher up so the later conditions and outcomes will be able to use what's in the variable.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `note`       |         Not seen in the Editor.        |
| *`noteName`* | String |      Name of the note.       |                 |
| *`variableName`* | String |      Name of the variable to insert the note/note array. Will override event variables if they already exist.       |                 |
| `loadNotesArray` | Boolean |      Load the notes array instead of the simple note?       |                 |
| `meetConditionIfNoteDoesNotExist` | Boolean |      Should this condition be met even if the note or note array doesn't exist or has expired?       |                 |
| `defaultVariableValue` | String |      If the note does not exist, should there be a default variable value set? (Use commas with a space, for separate objects in arrays)       |    Use this to essentially set a default value to the variable even if the note does not exist. Remember to also consider `meetConditionIfNoteDoesNotExist`.             |
| `allowExpired` | Boolean |      Allow the condition to pass even if the note has expired.       |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
