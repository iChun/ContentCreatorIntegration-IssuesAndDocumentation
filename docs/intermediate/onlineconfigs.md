Configuring a Socket Remotely with Online Configs
=================================================

In the client mod config, there is a field called `onlineConfigs`. This field is for URLs linking to the raw JSON file depicting an Event Configuration for configuring a specific socket layer. Basically your `streamlabs.json` or `chat.json` but hosted on a text host like `pastebin.com` or `gist.github.com`.

For an online config to be considered valid, the `type` field in the `EventConfiguration` must be set to the right socket layer. You cannot find this field in the Editor, but CCI saves it with the Event Configuration. All you have to do is host the file online and have CCI point to it in the config. Configs retrieved online will override local configs.

Unfortunately, you cannot host `Constants` or `GameEventConfig` files online. This feature is explicitly meant for `EventConfiguration` only. 

This feature was added in hopes of easing access of content creators to pre-made configs hosted online, or to allow content creators to update their configs set by another user without the need of exchanging config files.
