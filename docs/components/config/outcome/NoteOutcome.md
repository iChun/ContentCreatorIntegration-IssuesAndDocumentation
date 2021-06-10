Note Outcome
============= 

## Description

Writes a note to file. This Outcome is Client-side only.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `note`       |         Not seen in the Editor.        |
| *`noteName`* | String |      Name of the note. If a note already exists by this name, it will be overwritten. You can use the note condition to see if the note exists first.       |                 |
| *`noteContent`* | String |      Content of note.       |                 |
| `append` | Boolean |      Add the content to the end of the simple note, or add a new element into the notes array?       |                 |
| `putInNotesArray` | Boolean |      Do we put the note content into the notes array?       |                 |
| `expiresIn` | String |      How much time after the event does the note expire? Set to `null` to remove an already set expiry date.        |       Supports: y, d, h, m, s for Years, Days, Hours, Minutes, Seconds. Format: "2d7h32m19s" means 2 days, 7 hours, 32 minutes and 19 seconds from the event triggering. You can omit any magnitude of time (years/days/hours/mins/secs) which is zero.          |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
