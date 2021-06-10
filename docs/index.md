Content Creator Integration - Documentation
===========================================

Welcome to the official documentation for [Content Creator Integration](https://www.curseforge.com/minecraft/mc-mods/content-creator-integration/).

This documentation was written based off of version 1.9.0. These docs are aimed to be a reference or a guide for people trying to understand how Content Creator Integration works.

Contribute to the docs at [GitHub](https://github.com/iChun/ContentCreatorIntegration-IssuesAndDocumentation).


What is Content Creator Integration?
------------------------------------

Content Creator Integration (CCI) is a Minecraft mod made to bridge the gap between content creators/livestreamers and their viewers, with the aim of being as flexible and versatile as possible. It aims to allow Stream Events (subscriptions, tips, chat messages, etc) to be parsed and acted upon in a sensical and predictable manner.

CCI works on being primarily [Object-oriented](https://en.wikipedia.org/wiki/Object-oriented_programming), configured by [JSON](https://en.wikipedia.org/wiki/JSON) files to define the fields of said objects. No scripting is required, CCI does all of that for you, though some experience with scripting or programming would be invaluable in understanding the workings of this mod.

CCI connects to a variety of services using an array of methods, [Socket.IO](https://socket.io/), Websockets, or manually polling. The following services are supported:

| Method | Service |
|---|---|
| **Socket.IO**  | [Streamlabs](https://streamlabs.com/)<br/>[StreamElements](https://streamelements.com/)<br/>[DonationAlerts](https://www.donationalerts.com/)  |
| **Websocket**  | [Twitch PubSub](https://www.twitch.tv/)<br />[Twitch Chat](https://www.twitch.tv/)  |
| **Polling**    | [YouTube Chat](https://www.youtube.com/)    |

More layers of support may be added depending on the demand and the ease of integration. Request them on [GitHub](https://github.com/iChun/ContentCreatorIntegration-IssuesAndDocumentation)!
