IMC Outcome
============= 

## Description

Sends an InterModComms runtime message to another mod. This Outcome is Client-side only. Only functional on Forge builds of CCI.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `imc`       |         Not seen in the Editor.        |
| *`modId`* | String |      The `modId` of the mod to send this message to.       |                 |
| *`subject`* | String |      The key/subject of the IMC message.       |                 |
| *`message`* | String |      The value/message of the IMC message.       |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
