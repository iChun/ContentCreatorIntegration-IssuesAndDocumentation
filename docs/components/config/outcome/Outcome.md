Outcome
============= 

## Description

The base Outcome class. All Outcomes extend from this class, and as a result, have all the fields defined in this Class as well.

Outcomes are a mix of Client and Server-side. Outcomes which are Server-side require the player to have permission to do so, or will fail.


<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      The ID used for serialisation of the Class.       |                 |
| `displayName` | String |      Display name. What's this for?       |                 |
| `weight` | Integer |      The weight of this outcome, if there are multiple outcomes for this event.       |                 |
| `disabled` | Boolean |      Disable this outcome?       |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
