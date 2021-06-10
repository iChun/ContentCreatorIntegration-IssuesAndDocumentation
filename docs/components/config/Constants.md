Constants
=============

## Description

Constants contain `String` -> `Event Object` mappings for reference in [Event](../Event/). These are meant to reduce blocks of identical Event Objects, easing config creation and modification. Guide on use available [here](../../../intermediate/constants/).

<br />

## Fields

| Name         | Type                                        | Description                            | Additional Info                                |
| ------------ | ------------------------------------------- | -------------------------------------- | ---------------------------------------------- |
| `info`       | String                                      | Additional info (for library purposes) | Read [Libraries](../../../advanced/libraries/) |
| `conditions` | TreeMap&lt;String, [Condition](../condition/Condition/)&gt; | Mapping of condition constants         |                                                |
| `outcomes`   | TreeMap&lt;String, [Outcome](../outcome/Outcome/)&gt;   | Mapping of condition constants         |                                                |
| `events`     | TreeMap&lt;String, [Event](../Event/)&gt;     | Mapping of condition constants         |                                                |
