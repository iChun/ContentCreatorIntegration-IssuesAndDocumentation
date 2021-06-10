Listener
=============

## Description

This Object defines the Class type and retrieves the object reference for an argument in methods or constructors used in [ObjectAccessors](../ObjectAccessor/).

<br />

## Fields

| Name          | Type    | Description                                                                                                                                                                     | Additional Info                                                                                                                                                   |
| ------------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `isPrimitive` | Boolean | Is the class a primitive type?                                                                                                                                                  |                                                                                                                                                                   |
| *`classType`* | String  | The full class path and name for the class that this parameter is for.                                                                                                          | If `isPrimitive` is set to `true`, the `classType` is just the name of the primitive, eg: `int`, `short`, `char`. Special case: `String` is also supported.       |
| `argToPull`   | String  | The name of the variable you stored the object instance in from other ObjectAccessor's `argName`s. If the variable doesn't exist or this is left as `null`, will insert `null`. | If `isPrimitive` is set to `true`, this field can be used to create the primitive object in `argToPull`. Having an variable by argToPull overrides this, however. |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
