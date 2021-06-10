Prompt Outcome
============= 

## Description

Pop-up a window that requires the player to hit Yes or No. This Outcome is Client-side only.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `prompt`       |         Not seen in the Editor.        |
| *`text`* | String |      The information text for the pop up.       |                 |
| `yesOverride` | String |      Override text for the Yes button?       |                 |
| `noOverride` | String |      Override text for the No button?       |                 |
| `yesOutcome` | Outcome |      An optional outcome to trigger after the player hits Yes.       |                 |
| `noOutcome` | Outcome |      An optional outcome to trigger after the player hits No.       |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
