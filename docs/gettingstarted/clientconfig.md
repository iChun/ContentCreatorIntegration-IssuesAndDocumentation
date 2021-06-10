The Client Mod Config File
==========================

This page details the Mod Config file for Clients. If you are looking for information on the Server Mod Config, go [here](../ccionservers/).

The Mod Config file is broken down to three categories: `general`, `boxesAndStuff`, `socket`

They are as follows:

**General**  

| Name                             | Type    | In-Mod Description                                                                                                                                                                                                 | Additional Info                                                                                                   |
| -------------------------------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------- |
| `allowOutcomesRequiringServerWait` | Boolean | Allow outcomes that require a server to wait until the user connects to a server that allows them to send outcomes? Outcomes are normally discarded otherwise.                                                     |                                                                                                                   |
| `defaultProfile`                   | String  | Default profile name. Defaults to `default`. If set, will read from that folder within the main CCI directory instead. Change in-game with the editor.                                                             | Changing your profile in the editor also saves your latest profile to the config file.                            |
| `enableInformationToasts`          | Boolean | The sockets we use can be unreliable at times. Turn this on to get toasts about their status and other events.                                                                                                     |                                                                                                                   |
| `firstRun`                         | Boolean | Keeping this on/true makes CCI trigger the first run wizard settings. Turned off by CCI later.                                                                                                                     | If you set this to true manually in the config file, CCI will reenable the First Launch prompts on next start up. |
| `logTypes`                         | List    | Types of log types to write to disk. Putting socket_event in is the only way to see the raw event information (from the log file) as it is not printed to console. Everything else will still be print to console. | Available log types: cci, debug, event, socket_status, socket_event                                               |
| `maxAutomaticReconnects`           | Integer | Maximum amount of automatic reconnects before trying giving up.                                                                                                                                                    |                                                                                                                   |
| `maxEventCache`                    | Integer | Maximum size of the event cache. Caching prevents retriggers of events and allows you to play back events in the CCI gui, but takes more memory.                                                                   |                                                                                                                   |
| `onlineConfigs`                    | List    | URLs to pull online configs from. These should link to a raw file of the configuration. These configs will override local configs.                                                                                 |                                                                                                                   |
| `overrideToastGui`                 | Boolean | The Minecraft Toast Renderer has a bug where toasts with different heights might overlap. This override fixes it if the renderer is still the default renderer.                                                    | If you have any issues with Toasts, turning this off may help.                                                    |
| `stats`                            | Boolean | Enable local statistics collection? This information is for your own personal reference. None of it is be sent externally.                                                                                         | Access your stats in the Help window of the Editor                                                                |
| `streamerName`                     | String  | Set this if your streamer name is different from your Minecraft name for the `$streamer` global variable.                                                                                                            | [Variables](./events/#variables) reference                                                                        |

<br/>

**Boxes & Stuff**

| Name                | Type    | In-Mod Description                                                                                                                  | Additional Info                                                                                                            |
| ------------------- | ------- | ----------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| `editorGuiScale`      | Integer | Adjust the scale of the Event Configuration editor. Setting it to 0 makes it follow Minecraft's GUI scale. Set to -1 to do nothing. | If you are having weird GUI scaling issues, set this to -1                                                                 |
| `guiDockBorder`       | Integer | Number of pixels before Boxes & Stuff thinks you're trying to dock a window                                                         | Not actually used in CCI                                                                                                   |
| `guiDockPadding`      | Integer | How much padding to add to the docked windows                                                                                       | Not actually used in CCI                                                                                                   |
| `guiDoubleClickSpeed` | Integer | Speed, in ticks, to register a double click                                                                                         | 20 ticks = 1 second                                                                                                        |
| `guiListExpand`       | Integer | When you select a config in the editor it automatically expands all items with AT MOST this many items.                             |                                                                                                                            |
| `guiMinecraftStyle`   | Integer | Renders Boxes & Stuff's GUIs in a Minecraft Style instead. 1 = Vanilla Style, 2 = Texture Pack Style                                | B&S feature. Change this only if you really want to, cause it only works well for GUIs designed to immitate Minecraft GUIs |
| `guiTooltipCooldown`  | Integer | Number of ticks before showing a tooltip                                                                                            | 20 ticks = 1 second                                                                                                        |

<br/>

**Socket**

Socket configs are created by the Socket Provider. Usually it's just one List (per socket) to store your keys. YouTube Chat support has an extra config for the Google API Key, Twitch PubSub has an extra config for refresh tokens.
