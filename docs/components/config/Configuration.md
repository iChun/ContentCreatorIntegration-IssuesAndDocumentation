Configuration
=============

## Description

First filter in [EventConfiguration](../EventConfiguration/). Filters Events by platform and by Event types.

<br />

## Fields

| Name           | Type                                                | Description                                                                                   | Additional Info                                                                                                                                                                                                                          |
| -------------- | --------------------------------------------------- | --------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `types`        | LinkedHashMap&lt;String, [Event](../Event/) Array&gt; | List of event types.                                                                          |                                                                                                                                                                                                                                          |
| `queue`        | String Array                                        | List of event types to be queued.                                                             | Each String in this Array defines a queue. The String may have a combination of several event types which will share the same queue                                                                                                      |
| `ignoredTypes` | String Array                                        | List of event types to ignore.                                                                | These event types will not be triggered (and won't clutter your cache).                                                                                                                                                                  |
| `_for`         | String                                              | Which account/platform is this configuration for. If `null`, will be applied to all accounts. | This goes downwards so if a `null` for is found, the configurations below will be omitted entirely (it short circuits).<br /><br /> Serialised as `for`. Erroneously named, remnants of the time when CCI was built for Streamlabs only. |
