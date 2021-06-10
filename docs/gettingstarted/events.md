Dissecting an Event
===================

Events are, in its simplest form, a standard way for CCI to pass information to you in a way you can understand and process.

The way CCI works, is it receives Stream Events, breaks it down, and converts it into an event, to be passed to you. An important attribute of this, are what we call variables.

## Variables

Variables are, as the name implies, variables. They are essentially a key -> value mapping and are referenced using the `$` symbol.

For example:
A chat message comes in:
```
Toto: I bless the rains down in Africa.
```

The stream event comes in and gets processed, `Toto` is put in the `user` variable, and `I bless the rains down in Africa.` is put in the `message` variable.

So you get something like this:
```
user    => Toto
message => I bless the rains down in Africa.
```

This is where variables become important. The variable `user` and `message` never changes. But the person sending a chat message might be a different person, with a different message.

To address this issue, you always reference the name of the variable, with the `$` symbol. Keep this in mind. Also note that variable names are case-sensitive.
&nbsp;

### Global Variables

Global variables function on the same concept, but they are always available. Normally, when a stream event happens, information gets put into variables, and once processed, are discarded.

Global variables allows information to persist so you can reference them in different Events.

These are some global variables that are created when the mod is started:

| Variable Name | Description                                                                       |
|---------------|-----------------------------------------------------------------------------------|
| `streamer`      | The name you put in during the First Launch Wizard. Your Minecraft name otherwise |
| `playerName`    | Your Minecraft name                                                               |
| `mcVersion`     | The version of Minecraft you are running                                          |

There may be more Global variables inserted later on as you use CCI.
&nbsp;
&nbsp;

The Event Viewer
================

By default, CCI generates a set of default configs for you. However, not everyone wants a toast to pop up when a chat message comes in, or a in-game chat message when someone resubs. This is where we introduce the Event Viewer.

Now, open up your Event Viewer. That's the `Events` button on the top left in the CCI Editor in case you've forgotten.

Our example here will already have an example event (A chat message), so yours will likely look a little simpler and cleaner.

The Events Viewer:
![](./images/events/eventviewer.png){: class="img_center"}

| No. | Name                        | Description                                                | Additional Info                                                                                                                |
| --- | --------------------------- | ---------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| 1   | Event Index                 | The cached event index                                     |                                                                                                                                |
| 2   | Hide Variable Values Toggle | Toggles whether to hide the variable values or not         | Hold Shift when opening the Event Viewer to enable this by default                                                             |
| 3   | List of sockets             | The list of sockets you have available                     | Clicking between these will change which events you're looking at, for your selected socket                                    |
| 4   | Global Variables            | This lets you look at the Global Variables available       |                                                                                                                                |
| 5   | Notes                       | This lets you look at the Notes that have been loaded      |                                                                                                                                |
| 6   | Variables List              | List of variables associated with this event               | Left side are variable names. Right are their values. Ctrl+C copies the name, Ctrl+Shift+C copies the value, to your clipboard |
| 7   | Left Event Index            | Shifts the index to see a more recent event                | <--                                                                                                                            |
| 8   | Replay Event Button         | Replays the event so CCI will act on it again              |                                                                                                                                |
| 9   | Right Event Index           | Shifts the index to see an older event                     | -->                                                                                                                            |
| 10  | Dump Events                 | Dumps all cached events' variables into a dump.json file   | Use this for debugging purposes. If you're testing, consider using a `LogArgsCondition`                                        |
| 11  | Clear Queues Button         | Clears all the events in the queue, if you have one set up |                                                                                                                                |
| 12  | OK                          | OK                                                         | OK                                                                                                                             |

This event viewer will be helpful in building a custom Config Event. In the variables list (that's #6), you can see the list of variables and their values **after** the event had already been processed, meaning there may have been variable manipulation, including changes, deletion, or addition. Events that never pass the `for` filter in `Configuration` will not show up here. Be mindful of this.

Variables starting with `cci-type` are for your reference, and are usually filtered and handled by CCI elsewhere.

Now that we are familiar with variables and their uses, go back to the main editor screen.
