CCI on Servers
==============

### Why is CCI needed on a Server?

CCI was written to work mostly on the Client, but some things require a Server back-end to work. This is where CCI needs to be installed on a server.

Where this plays the most significance is when the Client is using a `CommandOutcome` and has a command that is too long. Generally, In-Game Chat can only send messages up to 256 characters. The limit for a command in `CommandOutcome` is closer to 32,000 characters, similar to Command Blocks. To work around this, the Server Backend is needed, and the player needs to be whitelisted.

And that's it. No need to have Event Configurations on the Server or anything of that sort. Client does all the heavy lifting, while the Server, just the mod installed, and the player whitelisted. 

<br/>

### The CCI Command

The CCI Command (`/cci`) is fairly simple, as I did not want to give users too much control over editing the Server Mod Config and would rather the Server Owner edit the Mod Config file manually. Just three simple commands.

| Command      | Argument                                         |
| ------------ | ------------------------------------------------ |
| `whitelist`    | Whitelists a player                              |
| `dewhitelist`  | Removes a player from the whitelist              |
| `setBlacklist` | Sets the whitelist as a blacklist and vice versa |

<br/>

### The Server Mod Config File

To start off, here's the breakdown of the Server Mod Config file. This is also generated on the Client but is only used when a Client opens up their Integrated Server to LAN.

| Name                   | Type    | In-Mod Description                                                                                                                                                                                                                                          | Additional Info                                                     |
| ---------------------- | ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `whitelistedUsers`       | List    | Whitelisted Users. These users will be able to trigger serverside outcomes.                                                                                                                                                                                 |                                                                     |
| `enableBlacklist`        | Boolean | Converts the list of whitelisted users to be the list of blacklisted users.                                                                                                                                                                                 | There is no separate whitelist and blacklist. Either you allow all and block a few, or allow a few and block the rest.                                                                    |
| `commandPermissionLevel` | Integer | Permission level required to use the server commands for CCI                                                                                                                                                                                                | Similar to the `op-permission-level` in [server.properties](https://minecraft.fandom.com/wiki/Server.properties), but for the CCI command.                                                                    |
| `disallowedCommands`     | List    | Disallowed Commands. These commands are prevented from being executed by CommandOutcome. EG: To disable `/time set day`, add the `time` command to the list. Does not cover for aliases (EG: `/tp` and `/teleport`)                                             |                                                                     |
| `logTypes`               | List    | Types of log types to write to disk. Putting socket_event in is the only way to see the raw event information (from the log file) as it is not printed to console. Everything else will still be print to console. Client config overrides this on Clients! | Available log types: cci, debug, event, socket_status, socket_event |
