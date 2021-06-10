Strings&#58; Untying the Knot
=============================

If you've come this far without knowing what [Strings](https://en.wikipedia.org/wiki/String_(computer_science)) are, I applaud you. As Variables are primarily String driven, a suite of conditions exist for manipulating them.

These literally call the Java function for the String and inserts the result into a variable. Find the function documentation [here](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html).

| Name                                 | ID               |
| ------------------------------------ | ---------------- |
| [StringConcatCondition](../../components/config/condition/string/unconditional/StringConcatCondition/)     | `stringConcat`   |
| [StringCompareToCondition](../../components/config/condition/string/unconditional/StringCompareToCondition/)  | `stringCompare`  |
| [StringContainsCondition](../../components/config/condition/string/StringContainsCondition/)   | `stringContains` | 
| [StringEndsWithCondition](../../components/config/condition/string/StringEndsWithCondition/)   | `stringEnds`     |
| [StringEqualsCondition](../../components/config/condition/string/StringEqualsCondition/)     | `stringEquals`   |
| [StringIndexOfCondition](../../components/config/condition/string/unconditional/StringIndexOfCondition/)    | `stringIndex`    |
| [StringLowerCaseCondition](../../components/config/condition/string/unconditional/StringLowerCaseCondition/)  | `stringLower`    |
| [StringReplaceCondition](../../components/config/condition/string/unconditional/StringReplaceCondition/)    | `stringReplace`  |
| [StringSplitCondition](../../components/config/condition/string/unconditional/StringSplitCondition/)      | `stringSplit`    |
| [StringStartsWithCondition](../../components/config/condition/string/StringStartsWithCondition/) | `stringStarts`   |
| [StringSubStringCondition](../../components/config/condition/string/StringSubStringCondition/)  | `stringSubstr`   |
| [StringTrimCondition](../../components/config/condition/string/unconditional/StringTrimCondition/)       | `stringTrim`     |
| [StringUpperCaseCondition](../../components/config/condition/string/unconditional/StringUpperCaseCondition/)  | `stringUpper`    |
| [StringLengthCondition](../../components/config/condition/string/unconditional/StringLengthCondition/)     | `stringLength`   |


However, there are also a few special Conditions made to handle Strings:

| Name                             | ID             | Description                                             |
| -------------------------------- | -------------- | ------------------------------------------------------- |
| [Base64DecodeCondition](../../components/config/condition/string/unconditional/Base64DecodeCondition/) | `base64Decode` | Decodes a Base64 String                                 |
| [Base64EncodeCondition](../../components/config/condition/string/unconditional/Base64EncodeCondition/) | `base64Encode` | Encodes a String into a Base64 String                   |
| [JsonSafeCondition](../../components/config/condition/JsonSafeCondition/)     | `jsonSafe`     | Converts a String to be safe to insert into JSON files. |
