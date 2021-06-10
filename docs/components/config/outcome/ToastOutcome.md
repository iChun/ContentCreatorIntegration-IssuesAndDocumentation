Toast Outcome
============= 

## Description

Use this outcome to send put a message in chat if the player is in the world. This Outcome is Client-side only.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `toast`       |         Not seen in the Editor.        |
| `toastType` | Integer |      Toast background type. 0 - 3. 0 = Advancement. 1 = Recipe. 2 = Narrator. 3 = System.       |                 |
| *`title`* | String |      Title for the toast.       |                 |
| `subtitle` | String |      Subtitle for the toast       |                 |
| `titleColor` | String |      Color for the title. Supports hex values.       |      To use hex values, prefix with `#`.          |
| `subtitleColor` | String |      Color for the subtitle. Supports hex values.       |      To use hex values, prefix with `#`.           |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
