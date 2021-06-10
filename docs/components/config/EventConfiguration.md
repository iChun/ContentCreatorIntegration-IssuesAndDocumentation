Event Configuration
===================

## Description

Base file that contains all the objects to filter and act upon a Stream Event.

<br />

## Fields

| Name      | Type                           | Description                                                                                   | Additional Info                                                                                                                                                                                                  |
| --------- | ------------------------------ | --------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `configs` | [Configuration](../Configuration/) Array | List of event types and configurations                                                        |                                                                                                                                                                                                                  |
| `init`    | [Event](../Event/) Array         | List of events to execute when this configuration file gets loaded (and when it is reloaded). | Only global variables will be passed initially but you can add more variables in each event's conditions and outcomes. All events will be executed, the event's allowsOtherEventsToTrigger isn't used here.      |
| `type`    | String                         | This is to define what type of EventConfiguration this is if pulled from an online source.    | Set by CCI when you are creating the config, eg: `streamlabs`/`streamelements`/`chat`/etc.<br /><br />Bear in mind that retrieving an online file will override local configs.<br /><br />Not seen in the Editor. |
| `from`    | String                         | This is the online source for this EventConfiguration.                                        | Set by CCI.                                                                                                                                                                                                      |
