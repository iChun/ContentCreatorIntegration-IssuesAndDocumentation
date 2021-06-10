Param Injector
=============

## Description

Short for Parameter Injector, in case you were wondering. This Object checks a Forge Event to see if matches its current configuration. If it does, the Forge Event is then used as a reference for its [ObjectAccessors](../ObjectAccessor/).

<br />

## Fields

| Name                | Type                                                              | Description                                                                                                                                  | Additional Info                                                            |
| ------------------- | ----------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `name`              | String                                                            | Optional name for this listener, for Editor readability.                                                                                     |                                                                            |
| *`disabled`*          | Boolean                                                           | Is this listener disabled?                                                                                                                   |                                                                            |
| *`className`*         | String                                                            | The Class name for the Forge event you want to listen for.                                                                                   | Eg: `LivingDeathEvent` or `PlayerEvent$PlayerRespawnEvent`                 |
| `isFullName`        | Boolean                                                           | Are you using the full name of the Class, including the package names.                                                                       |                                                                            |
| `isServerEvent`     | Boolean                                                           | Is this Forge event only triggered on the server?                                                                                            | Dedicated Server use. Only allowed if you can send outcomes to the server. |
| `preAccessorEvent`  | [Event](../../config/Event/)                                      | A convenience event if you'd like to set some variables before the accessors are triggered.                                                  |                                                                            |
| `staticAccessors`   | [ObjectAccessor](../ObjectAccessor/) Array                        | List of Accessors to access static methods and fields of Classes.                                                                            | Used together with ObjectAccessor's `classForStaticAccess`.                |
| *`accessors`*         | [ObjectAccessor](../ObjectAccessor/) Array                        | List of Accessors to access the methods and the fields of the Event/Objects.                                                                 |                                                                            |
| `argBasedAccessors` | LinkedHashMap&lt;String, [ObjectAccessor](../ObjectAccessor/)&gt; | List of Accessors to trigger on objects you've stored in the variable map prior. Each mapping should match to an existing variable key/name. |                                                                            |
| `event`             | [Event](../../config/Event/)                                      | The Event that we will be passing all the variables into afterwards.                                                                         |                                                                            |
| `cancel`            | String                                                            | Do you want to cancel the Forge event (if cancelable) after we trigger our event? Set final result as `true` to cancel.                      |                                                                            |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
