Fake Crash Outcome
============= 

## Description

Pretends to crash the game.  This Outcome is Client-side only.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `fakeCrash`       |         Not seen in the Editor.        |
| *`crashType`* | String |      Type of crash: 1 = Freeze. 2 = Out of Memory Screen.       |                 |
| `crashDuration` | String |      The duration of the fake crash, in ticks. Defaults to 5 seconds.      |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
