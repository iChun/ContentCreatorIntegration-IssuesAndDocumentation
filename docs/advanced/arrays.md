Arrays&#58; The Black Sheep of Variables
========================================

When CCI was developed, variables were designed to be of relatively primitive types: `Integer`, `Double`, `Boolean`, `String`. And then <s>the fire nation attacked</s> Arrays got in the way and became an inevitable issue. 

Sometimes, sockets send information in the form of Arrays, that, or CCI missed one and slipped in an Array to the Variables list. It had to be dealt with.

And as such, came a suite of Conditions made to handle Arrays:  

| Name                                | ID                | Description                                        |
| ----------------------------------- | ----------------- | -------------------------------------------------- |
| [ArrayCondition](../../components/config/condition/array/ArrayCondition/)           | `array`           | Checks within a String Array for a matching String |
| [ArrayLengthCondition](../../components/config/condition/array/ArrayLengthCondition/)     | `arrayLength`     | Puts the length of a String Array into a variable  |
| [ArrayCombineCondition](../../components/config/condition/array/ArrayCombineCondition/)    | `arrayCombine`    | Combines two String Arrays                         |
| [ArrayDeleteCondition](../../components/config/condition/array/ArrayDeleteCondition/)     | `arrayDelete`     | Deletes a String from a String Array               |
| [ArrayAppendCondition](../../components/config/condition/array/ArrayAppendCondition/)     | `arrayAppend`     | Appends a String to a String Array                 |
| [ArrayExplodeCondition](../../components/config/condition/array/ArrayExplodeCondition/)    | `arrayExplode`    | Puts each Object in an Array into its own variable |
| [VariableIsArrayCondition](../../components/config/condition/variable/VariableIsArrayCondition/) | `variableIsArray` | Checks a variable value to see if it is an Array   |

Check the individual pages of the Event Objects above for more info.

Besides those Conditions, a few other Event Objects also gained Array support:

| Type      | Name                            | ID            | Description Of Support                     |
| --------- | ------------------------------- | ------------- | ------------------------------------------ |
| Condition | [NoteCondition](../../components/config/condition/NoteCondition/)        | `note`        | Notes can contain a String and/or an Array |
| Condition | [NotesListCondition](../../components/config/condition/NotesListCondition/)   | `notesList`   | The result is an Array                     |
| Condition | [StringSplitCondition](../../components/config/condition/string/unconditional/StringSplitCondition/) | `stringSplit` | The result is an Array                     |
| Condition | [RepeatCondition](../../components/config/condition/unconditional/RepeatCondition/)      | `repeat`      | Can iterate through an Array               |
| Outcome   | [NoteOutcome](../../components/config/outcome/NoteOutcome/)          | `note`        | Notes can contain a String and/or an Array |
| Outcome   | [RepeatOutcome](../../components/config/outcome/RepeatOutcome/)        | `repeat`      | Can iterate through an Array               |
