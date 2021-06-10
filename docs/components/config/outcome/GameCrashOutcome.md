Game Crash Outcome
============= 

## Description

Forces the game to crash. This Outcome is Client-side only.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `crash`       |         Not seen in the Editor.        |
| *`crashType`* | String |      Type of crash: 1 = System exit. 2 = System crash (careful, JVM doesn't really like this! Could potentially cause corruption). 3 = Minecraft crash. 4 = Minecraft stack overflow crash. 5 = Minecraft freeze/lock up.       |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
