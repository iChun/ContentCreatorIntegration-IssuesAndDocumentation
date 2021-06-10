Chat Message Outcome
============= 

## Description

Use this outcome to send put a message in chat if the player is in the world. There's a potential for this Outcome to be client-side only.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `chat`       |         Not seen in the Editor.        |
| *`message`* | String |      Message to send. Supports Minecraft's Text Formatting       |                 |
| `inActionBar` | Boolean |      Put the message in the player's Action Bar instead?       |                 |
| `sendToServer` | Boolean |      Send the message to the server instead? (No Action Bar support)       |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
