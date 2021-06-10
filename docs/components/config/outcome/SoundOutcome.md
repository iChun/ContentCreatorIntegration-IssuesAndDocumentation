Sound Outcome
============= 

## Description

Play a sound either Client-side or Server-side. This sound is Client-side if `clientSide` is set to `true`.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `sound`       |         Not seen in the Editor.        |
| `clientSide` | Boolean |      Is the sound to be played on the client? `target` is ignored if this is `true`.      |                 |
| *`sound`* | String |      The sound name, in resource location format. EG `minecraft:entity.pig.ambient`       |                 |
| `target` | String |      The target selector for the sound. Only for non-client side sounds.       |                 |
| `volume` | Double |      Volume of the sound       |    Defaults to `1`             |
| `pitch` | Double |      Pitch of the sound       |       Defaults to `1`          |
| `category` | String |      Category of the sound. EG: `ambient` or `music`. Defaults to `master` if CCI cannot find your category.       |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
