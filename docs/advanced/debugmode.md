Debugging When Debugging Fails
==============================

An extension to the earlier mentioned [Debugging guide](../../intermediate/debugging/).


![](https://upload.wikimedia.org/wikipedia/commons/d/d5/Rubber_duck_assisting_with_debugging.jpg){: class="img_center"}  
[Image Credit](https://en.wikipedia.org/wiki/File:Rubber_duck_assisting_with_debugging.jpg)
<br />

If you've done the [rubber duck debugging](https://en.wikipedia.org/wiki/Rubber_duck_debugging), logged the args, scoured the dumps, and still can't figure out where it all went wrong (In CCI, I mean, nowhere else), maybe it's time to read the log file.

The log files can be found in `/contentcreatorintegration/logs/`. They can get pretty big (I've seen 8MB+ log files), so CCI tries to compress old files, so you may have to extract them.

## What the log files contain

The log files basically have anything that CCI spits to the console, and then some, we also log the raw data that our sockets send us (presuming `socket_event` is enabled in the log types).

Here is an excerpt of the contents of the log file from one of my streams:

```text
Event TC: @badge-info=subscriber/7;badges=subscriber/6,sub-gifter/5;client-nonce=709c51cbccdfece0cc668a9b86b34c60;color=#8A2BE2;display-name=Harogna;emotes=;flags=;id=c8f9a8c2-0079-402b-bd57-81016496322e;mod=0;room-id=29648793;subscriber=1;tmi-sent-ts=1622240475496;turbo=0;user-id=117374099;user-type= :harogna!harogna@harogna.tmi.twitch.tv PRIVMSG #ohaiichun :Add a hallelujah sound bite xD
Event TC: @badge-info=;badges=bits/1;client-nonce=ada9d8028647538ddfc0db6e99f2d151;color=#1E90FF;display-name=Quarris;emotes=;flags=;id=ec6b0903-f907-4623-9b8a-8086358dac82;mod=0;room-id=29648793;subscriber=0;tmi-sent-ts=1622240484856;turbo=0;user-id=26222064;user-type= :quarris!quarris@quarris.tmi.twitch.tv PRIVMSG #ohaiichun :I need to head off to bed now, its starting to get late and im tired
Event TC: @badge-info=subscriber/7;badges=subscriber/6,sub-gifter/5;client-nonce=c76f7d18413241262038a82442dc1691;color=#8A2BE2;display-name=Harogna;emotes=;flags=;id=d57a7e7e-ad39-46d9-b5df-06cf6729628d;mod=0;room-id=29648793;subscriber=1;tmi-sent-ts=1622240525493;turbo=0;user-id=117374099;user-type= :harogna!harogna@harogna.tmi.twitch.tv PRIVMSG #ohaiichun :nn then o/
Event TC: @badge-info=;badges=bits/1;client-nonce=26df35f74016be8815b5c3387b86db57;color=#1E90FF;display-name=Quarris;emotes=555555584:14-15;flags=;id=dce2a1c9-dd57-408a-81e5-75adecd3255f;mod=0;room-id=29648793;subscriber=0;tmi-sent-ts=1622240581172;turbo=0;user-id=26222064;user-type= :quarris!quarris@quarris.tmi.twitch.tv PRIVMSG #ohaiichun :aight, niiigh <3
Event TC: PING :tmi.twitch.tv
Event TC: PING :tmi.twitch.tv
Event TC: PING :tmi.twitch.tv
Event TC: PING :tmi.twitch.tv
Event TC: PING :tmi.twitch.tv
Event SL: {"event_id":"evt_796a197a3dd405fa6737cdef1d36417c","for":"twitch_account","type":"follow","message":[{"name":"<REDACTED>","_id":"5b69042c4fb553c8792851e26ce3232c","id":"264342701","priority":10}]}
Event SL: {"type":"alertPlaying","message":{"read":false,"priority":10,"message":"","type":"follow","platform":"twitch_account","wotcCode":null,"createdAt":"2021-05-28 22:44:23","createdAtTimestamp":1622241863006,"payload":{"name":"<REDACTED>","_id":"5b69042c4fb553c8792851e26ce3232c","id":"264342701","priority":10},"isTest":false,"repeat":false,"name":"<REDACTED>","from":"<REDACTED>","_id":"5b69042c4fb553c8792851e26ce3232c","to":"","hash":"follow:<REDACTED>:"}}
Event TC: PING :tmi.twitch.tv
Event TC: PING :tmi.twitch.tv
Event TC: PING :tmi.twitch.tv
Event TC: @badge-info=;badges=;client-nonce=cabddc50c8786ac70d9b7e83e5c309d4;color=#1E90FF;display-name=jackylam5;emote-only=1;emotes=433137:0-7;flags=;id=f60ad65c-7a64-404c-a385-eecc9d951469;mod=0;room-id=29648793;subscriber=0;tmi-sent-ts=1622242588464;turbo=0;user-id=46601994;user-type= :jackylam5!jackylam5@jackylam5.tmi.twitch.tv PRIVMSG #ohaiichun :jackylHi
```

What you're seeing is the raw data for:  

* 4 Twitch Chat messages
* 5 Twitch Chat ping requests
* 2 Streamlabs Events, a `follow` event and a `alertPlaying` event.
* 3 More Twitch Chat ping requests
* 1 Final Twitch Chat message

Aren't you glad CCI makes sense of this for you? (*I am, and I wrote the dang thing*)

<br />

## How to use this info

For starters, you can read the raw data to see if there is any error in CCI parsing them. If there are, please report them through the [docs repository](https://github.com/iChun/ContentCreatorIntegration-IssuesAndDocumentation). Some Events, CCI doesn't bother creating Events for them (as you don't need them), so you will never see them in-game.

Once you're able to make sense of the raw data, there is something else you can do, if you're having issues with either Streamlabs, StreamElements, or DonationAlerts. You can force CCI to re-interpret the raw data in Debug Mode.

<br />

## How to use Debug Mode

Debug Mode can be turned on in the Help window in the Editor. Just click the button and CCI has debug mode turned on for the rest of the session.

Debug Mode has two functions:  

* Captures all Events for viewing in the Event Viewer
* Allows replaying of past Events in the `test.log`, which we'll explain here.

Ideally, you should have the Java Console open if you haven't already by now.

Now, make a `test.log` file in your Profile folder (this is where all your JSON files are). It should be a blank text file. Any line starting with `Event SL:`, `Event SE:`, `Event DA:`, `Event TP:` can be put in there to be replayed, one event per line. Remember to save. Replaying Twitch Pub Sub Events will require a socket running on the same channel ID to exist to function properly.

Back in the Client: Press `Shift+Tab`.

This makes CCI load up `test.log` and it starts reading line-by-line. Keep hitting `Shift+Tab` to read the next line. In the console, CCI will log which event is being reinterpreted. Once this hits the end of the file, CCI repeats the whole process again.

### How is this useful? 

With some socket layers, especially with StreamElements, their test/replay events are formatted differently, making testing difficult. This lets you test and re-test live events that have happened in the past, to find out what went wrong. Combine these with the `LogArgsCondition` and debugging should be much easier.
