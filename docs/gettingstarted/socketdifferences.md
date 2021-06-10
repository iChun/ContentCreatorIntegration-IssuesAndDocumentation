Sockets&#58; Which One To Pick
==============================

CCI supports a variety of services, mostly centered around Twitch. (Not much choice when it comes to YouTube, I'm afraid.) This page is to highlight the subtle differences that may not be immediately obvious when selecting a service. 

| Support             | Streamlabs | StreamElements |   Twitch PubSub   | Twitch Chat |
| ------------------- |:----------:|:--------------:|:-----------------:|:-----------:|
| Bits/Cheers         |     ✓      |       ✓        |         ✓         |             |
| Subscriptions       |     ✓      |       ✓        |         ✓         |             |
| Sub Gift Bombs      |     ✓      |  To a degree   |         ✓         |             |
| Follows             |     ✓      |       ✓        |         ✓         |             |
| Incoming Raids      |     ✓      |       ✓        |                   |      ✓      |
| Outgoing Raids      |            |                |         ✓         |             |
| Hosts               |     ✓      |       ✓        |                   |      ✓      |
| Tips                |     ✓      |       ✓        |                   |             |
| Twitch Chat         |            |                | Moderation events |      ✓      |
| Polls               |            |                |         ✓         |             |
| Predictions         |            |                |         ✓         |             |
| Hype Trains         |            |                |         ✓         |             |
| Channel Points      |            |                |         ✓         | To a degree |
| Leaderboard Updates |            |                |         ✓         |             |
| Replaying Events    |     ✓      |       ✓        |                   |             |


Above is a summary of what each service supports. For the full Twitch experience, combine Twitch PubSub and Chat. What Streamlabs and StreamElements does (speculated), is that it connects to both your PubSub and Chat, and adds on their own tips/donations page, and serve their package. 

What you can do, is either Streamlabs or StreamElements, and Twitch PubSub and Twitch Chat to fill in the gaps. I expect most of you to already be using either Streamlabs or StreamElements, so the defaults for Twitch PubSub do not overlap with them.


## Streamlabs and StreamElements, what's the difference?

They're essentially competing services, and for the most part, provide the same thing. With CCI however, the way they implement events differs slightly. For example, StreamElements does not have a `Gift to the Community` event and instead inserts that info during a subscription event, while Streamlabs has a separate event just for that purpose. Their event type IDs are also different, `bits` in Streamlabs vs `cheer` on StreamElements, `follow` on Streamlabs vs `follower` on StreamElements.

Point is: **They do things differently**. What that means is Event Configs for one will not work on the other. You'll have to try and convert them if want to use a Streamlabs config on a StreamElements setup and vice versa. Their event variables will not match up and you may encounter some errors as well. There is no proper list or guide on converting the two, however, so you'll have to go off trial and error. 
