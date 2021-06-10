How to&#58; Converting a Twitch Name to Minecraft Name
======================================================

One of the commonly asked questions is getting users to convert their twitch name to MC name. Unfortunately, there is no online service for people to reference, so all of this has to be done by hand.

Before we begin, I expect you to already have a basic understanding of CCI, and a basic understand of how [Notes](../../intermediate/notes/) work.

## How it works, a summary

If a user had defined their Minecraft name in the past, it gets saved to a note. When using their username, we look up to see if the note exists. If it exists, we use the name saved, otherwise we fall back to their username.


## How it works, the long version

### Capturing a chat message

We'll be using Twitch Chat for this example. First off, we want to capture a message if the user says something with a specific prefix. We will be using the `!setmcname` prefix here. Make a new Config Event and bring it up above the other Events, we want this to trigger before the other events trigger as we will be short circuiting the event flow.

In your conditions, make a new `StringStartsWithCondition`, set the `source` to `$message` and the `target` to `!setmcname `. That space in the target is not accidental, most of the time when users trigger the command, there will be a space between the command and the argument, eg: `!setmcname iChun`.

Next, you want a substring of the message, to clip out the argument. Use a `StringSubStringCondition` here, and set the `source` to `$message` the `beginIndex` to `11`. That removes the first 11 characters in the message variable. Put the result in `nameArg`.

Now, we want to trim any whitespace the user may have left at the end of the argument, so we use a `StringTrimCondition`. Set the `source` to `$nameArg` and `result` to `nameArg`, we're just going to reuse the variable here.

And that's it, we now have the chat message argument.

(Alternatively, you could also do a Channel Point Reward for this, but I'm also using this tutorial to teach String manipulation.)

Next up:

### Saving the MC name into a Note

For sanity sake, we should lowercase the name of the user. Make a `StringLowerCaseCondition` and put `source` as `$user` and `result` as `userLC`.

We have our MC name for the user in `nameArg`. Now we want to save it into a Note. Use a `NoteOutcome`. We don't need anything special here, just set `noteName` to `mcName_$userLC` and `noteContent` to `$nameArg`. When this Outcome triggers it'll make a new note with their MC name as the content.

If you want, for debugging, make a `ChatMessageOutcome` or something to confirm the note was created. After the note was created, you can also check the Event Viewer to see your notes.

### Loading up the Note

So, wherever before you want to use the MC name, you need to lowercase the user's name again, for consistency sake, put it in `$userLC`. Now for the `NoteCondition`. For `noteName`, put `mcName_$userLC`, and for `variableName`, put `mcnameuser`. That loads up the note and puts the value into the `$mcnameuser` variable.

Now, what if the user has never defined their MC name. Set `meetConditionIfNoteDoesNotExist` to `true`, and `defaultVariableValue` to `$user`. This ensures that the `$mcnameuser` always has a value in it, be it the note content, or the user's name. When you want to spawn a mob with the user's MC name, just use `$mcnameuser` instead of `$user`.
