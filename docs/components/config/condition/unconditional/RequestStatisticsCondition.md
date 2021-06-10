Request Statistics Condition
============= 

## Description

If you want to check the player's statistics, you need to request this from the server first. The server only sends the client their statistics when they open the Statistics screen. This simulates that.

Put this in a Config Event and in that same event, set a reasonable delay, such as 10 ticks or so (varies depending on player ping). In one of the outcomes, use an `EventOutcome` that has a `StatisticsCondition` to actually check the stats and act upon it. Unconditional.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `statsRequest`       |         Not seen in the Editor.        |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
