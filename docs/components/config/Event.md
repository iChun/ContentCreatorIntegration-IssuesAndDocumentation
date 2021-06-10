Event
=============

## Description

An Event (in this documentation, usually referred to as a Config Event), home to Conditions and Outcomes. 

If the Condition set up is met, then the Outcomes are triggered. Having no conditions is considered a met condition. Requires at least one Outcome to be considered valid. Consider a `NullOutcome` if the Event is purely for functional Conditions.

When used in Queues and Delays, Conditions are only checked when the Stream Event happens. Triggering a Condition when the Event triggers requires the Condition to be in the Outcomes block. Consider using a `ConditionalOutcome`.

Deeper explanation of use available [here](../../../intermediate/configspecifics/).

<br />

## Fields

| Name                                | Type                       | Description                                                                                                                                                                     | Additional Info                                                       |
| ----------------------------------- | -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `name`                              | String                     | Optional name for this event, for Editor readability.                                                                                                                           |                                                                       |
| `constantName`                      | String                     | The name of mapping to the Constant Event to reference. If this is set, we check against the Constant Event's conditions and trigger their outcomes.                            | Read [Constants](../../../intermediate/constants/)                    |
| `disabled`                          | Boolean                    | Disable this event?                                                                                                                                                             |                                                                       |
| `conditions`                        | [Condition](../condition/Condition/) Array | List of conditions required to trigger the event.                                                                                                                               |                                                                       |
| `outcomes`                          | [Outcome](../outcome/Outcome/) Array   | List of outcomes to trigger if the event meets the conditions.                                                                                                                  |                                                                       |
| `triggersFromAnyConditionMet`       | Boolean                    | Does this event trigger from any condition that is met?                                                                                                                         |                                                                       |
| `allowsOtherEventsToTrigger`        | Boolean                    | Does triggering this event still allow other events to trigger?                                                                                                                 |                                                                       |
| `singleOutcomeOnly`                 | Boolean                    | If there are multiple outcomes for the event, only the first outcome that succeeds?                                                                                             |                                                                       |
| `playTime`                          | String                     | How long to play the event, in ticks. Only if the event type has been registered a queue.                                                                                       | Set to -1 to skip the queue.                                          |
| `playTimeEvent`                     | Event           | An event to trigger during the playTime of the Event ticks.                                                                                                                     | Will have variables `$currentPlayTime` and `$totalPlayTime` inserted. |
| `delay`                             | String                     | How long of a delay, in ticks, before playing the event.                                                                                                                        |                                                                       |
| `cooldown`                          | String                     | How often this event can be triggered, in ticks.                                                                                                                                |                                                                       |
| `disableShortCircuitWhenOnCooldown` | Boolean                    | Normally, if this event is on cooldown (and `allowsOtherEventsToTrigger` is disabled) and the conditions are met, this event stops other events triggering. This disables that. |                                                                       |
