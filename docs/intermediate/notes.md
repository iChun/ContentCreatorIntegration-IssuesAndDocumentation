I'm Making A Note Here, Huge Success!
=====================================

<s>For the good of all of us, except the ones who are dead</s>  

Here we talk about Notes, and how they differ from Variables. Notes are, essentially, variables that save to disk. Variables are all kept in memory and thus are lost when the Event ends or Minecraft closes. Notes are loaded up when the profile loads, and saved to disk when added/modified.

These are the few Event Objects you can use to work with Notes:

| Type      | Name                           | ID             | Description                                   |
| --------- | ------------------------------ | -------------- | --------------------------------------------- |
| Condition | [NoteCondition](../../components/config/condition/NoteCondition/)       | `note`         | Loads a note into a variable (if not expired) |
| Condition | [NotesListCondition](../../components/config/condition/NotesListCondition/)  | `notesList`    | Puts the list of note names into a variable  |
| Outcome   | [NoteOutcome](../../components/config/outcome/NoteOutcome/)         | `note`         | Saves a note to disk                          |
| Outcome   | [NoteDeletionOutcome](../../components/config/outcome/NoteOutcome/) | `noteDeletion` | Deletes a note from disk                      |

Notes only bridge the gap between the disk and CCI. Essentially, you load a note into a variable, and save a variable into a note. Check the individual pages of the Event Objects above for more info.
