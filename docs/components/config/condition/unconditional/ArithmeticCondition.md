Arithmetic Condition
============= 

## Description

Do simple arithmetic calculations on variables. Inserts 0 if something failed. Will always return a `double`-type number. Use `round`/`floor`/`ceil` to convert `value1` to a `integer`-type (whole number). Unconditional.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `math`       |         Not seen in the Editor.        |
| *`calc`* | String |      Function to use: `+`, `-`, `x`, `/`, `pow`, `sqrt`, `mod`, `max`, `min`, `round`, `floor`, `ceil`, `log`, `signum`, `abs`, `sin`, `cos`, `tan`, `asin`, `acos`, `atan`.        |              These functions use the same calls as [Java's Math Class](https://docs.oracle.com/javase/8/docs/api/java/lang/Math.html). Trigonometric functions uses degrees. Some operations only use the first variable.   |
| *`value1`* | String |      First value, can be a variable name or number.       |                 |
| *`value2`* | String |      Second value, can be a variable name or number.       |  Although required, not always used. Set to any value in those situations.               |
| *`variableName`* | String |      Variable name to insert the result into.       |                 |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  
