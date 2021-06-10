Command Outcome
============= 

## Description

Trigger a client-side or server-side command. This Outcome becomes Client-side if you are unable to send outcomes to the server, have `executeAsSelf` enabled and have not enabled `disableChatCommandFallback`.

<br />

## Fields

| Name     | Type   | Description | Additional Info |
| -------- | ------ | ----------- | --------------- |
| *`type`* | String |      Internal ID for serialisation: `command`       |         Not seen in the Editor.        |
| *`command`* | String |      String to be put into the command.       |                 |
| `executeAsSelf` | Boolean |      Should the command be executed as the streamer or the server?      |                 |
| `handleFeedback` | String |     Variable name to insert server feedback. The server feedback will be inserted into a Global variable.        |          Please read the section below.       |
| `feedbackKeys` | String Array |      Translation keys to capture.       |        Please read the section below.         |
| `disableChatCommandFallback` | Boolean |      If you are connected to a server where you don't have CCI permissions/server doesn't have CCI installed, and `executeAsSelf` is enabled, `CommandOutcome` tries to send a chat message with the command instead. Turning this on disables that.       |  Chat fallback will also warn you if your message is too long or has invalid characters.               |

///Footnotes Go Here///

[^-1]: Fields in *italics* are required for the Object to be valid.  

## Handling the Feedback from the Server

Some commands have feedback that you would like to listen to. This is where `handleFeedback` and `feedbackKeys` come in.

`handleFeedback` tells CCI how to handle feedback. Leaving it as `null` makes CCI silence feedback. Leaving an empty String (note, this is not the same as `null`!), allows all feedback. Anything else will define the variable name we will input the feedback into, and will likely require the use of `feedbackKeys`. CCI will try and listen for feedback for a second after the command is sent (if feedback takes longer than this to return, you have other things to worry about).

You cannot silence feedback when you are using the chat fallback, but you can still capture feedback.

Be mindful that feedback is only sent to you when `executeAsSelf` is turned on.

Without using `feedbackKeys`, CCI will capture the first System Chat message that comes in. With `feedbackKeys`, if you know the translation keys that the command sends back, eg. `commands.time.query` from the Time Command, put them in the field. CCI will capture the first one that matches any one of the keys and consider it a job done. 

To use this feedback however, you need another event to check for your variable set in `handleFeedback`. 
