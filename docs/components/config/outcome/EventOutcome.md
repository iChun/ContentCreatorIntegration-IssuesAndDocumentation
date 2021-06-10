Event Outcome
============= 

## Description

Attempt to trigger even more events. Use this to trigger delayed events, such as when Requesting Statistics or awaiting Command Feedback. 

Be mindful that the event's conditions are checked before triggering, so any functional conditions need to be done in a `ConditionalOutcome` instead, if the event has a delay. This Outcome is Client-side only.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `event`       |         Not seen in the Editor.        |
| *`events`* | Event Array |      List of events to attempt to trigger.       |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
