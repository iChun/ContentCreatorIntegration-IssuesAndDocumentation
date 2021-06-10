Food Outcome
============= 

## Description

Adds a certain stat to players' food stats. Either level and saturation, or exhaustion.

| Protip                                                                                                                                                              |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Good luck figuring out the numbers, cause I have no clue, all I do is call the code.<br /><br />If you find out what numbers work for what, please let me know and I'll add them here for others to reference. |

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `food`       |         Not seen in the Editor.        |
| *`target`* | String |      The target selector for the entities to affect.       |     Only affects players.            |
| *`level`*[^1] | String |      Level/Healing to add.       |                 |
| *`saturation`*[^1] | String |      Saturation to add.       |                 |
| *`exhaustion`*[^1] | String |      Exhaustion to add.       |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
[^1]: Either `level` and `saturation` or just `exhaustion` is required for the Object to be valid.
