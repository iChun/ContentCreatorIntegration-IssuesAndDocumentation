Condition
============= 

## Description

The base Condition class. All Conditions extend from this class, and as a result, have all the fields defined in this Class as well.

Conditions are meant to only be triggered on Clients. Conditions may potentially be triggered on the Server-side, but is highly discouraged.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      The ID used for serialisation of the Class.       |                 |
| `displayName` | String |      Display name. What's this for?       |                 |
| `inverseMatch` | Boolean |      If the condition isn't met, consider it met and vice versa.       |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
