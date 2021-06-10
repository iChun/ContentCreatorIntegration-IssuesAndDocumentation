Game Event Config
=============

## Description

This Object holds the list of [Listeners](../Listener) which hook into the Forge Event Bus to capture Forge Events to allow CCI to reference them. Caution: This Object and its counterparts are not easy to use. Detailed usage guide [here](../../../expert/gamehooks/).

<br />

## Fields

| Name        | Type                          | Description                    | Additional Info                                                                                                                                                                   |
| ----------- | ----------------------------- | ------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `listeners` | [Listener](../Listener) Array | List of Forge Event listeners. | The Forge Event hook is only registered if at least one valid listener exists.<br /><br />CAUTION: Using this feature may severely affect game performance. Use at your own risk! |
