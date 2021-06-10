Note Deletion Outcome
============= 

## Description

Deletes info of a note. If the note is empty then it will be removed anyway. This Outcome is Client-side only.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `noteDeletion`       |         Not seen in the Editor.        |
| *`noteName`* | String |      Name of the note.       |                 |
| *`deletionType`* | Integer |      Deletion type for note. 0 = Entire note. 1 = Simple note. 2 = Notes array. 3 = Content within notes array.       |                 |
| *`noteContent`*[^1] | String |      Content to remove from array. Only used if `deletionType` is `3`.       |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
[^1]: Only required if `deletionType` is `3`
