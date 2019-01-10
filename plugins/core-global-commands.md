# Core/Global Commands

## Commands

| Name | Description | Default Level | Usage |
| :--- | :--- | :--- | :--- |
| `!setup` | Initialize the bot on the current server | Admin or Global Admin | `@heimdallr setup` |
| `!about` | About the bot | Default | `!about` |
| `!uptime` | Display bot's uptime | Global Admin | `!uptime` |
| `!source <command>` | Find source for a command | Global Admin | `!source about` |
| `!eval` | Evaluate a python statement | Global Admin | `!eval 1` |
| `!control sync-bans` | Force a ban sync for all guilds | Global Admin | `!control sync-bans` |
| `!control reconnect` | Force a reconnect with discord | Global Admin | `!control reconnect` |
| `!guilds invite <guild id>` | Get a single-use invite for a guild | Global Admin | `!guilds invite 77176186148499456` |
| `!guilds wh <guild id>` | Whitelist guild for the bot to be able to join | Global Admin | `!guilds wh` `77176186148499456` |
| `!guilds unwh <guild id>` | Remove guild from the whitelist to join | Global Admin | `!guilds unwh 77176186148499456` |
| `!override [duration in seconds] [in Name]` | Enable global admin override in a, or all, guilds | Global Admin | `!override 3600` |
| `!adv info [user]` | User summary, infraction summary, stats summary | Global Admin | `!adv info 76685590585671680` |
| `!adv inf search +[query] -g(--guild) [guild id]` | Search all infractions for the particular query | Global Admin |  |
| `!adv inf info <inf #>` | Get information on any infraction, not just those in this guild. | Global Admin | `!adv info info 1` |
| `!status <action> <status>` | Set the bot's action as watching, listening, or playing; and the status as any string | Global Admin | `!status watching u` |
| `!status reset` | Reset the bot's status | Global admin | `!status reset` |
| `!status live [action]` | Set the bot to streaming an action | Global Admin | `!status live Warframe` |
| `!guilds wh-add <guild id> <flag>` | Add a flag to a guild, one of those listed in [CLI Interface](../cli-interface.md#valid-guild-flags) | Global Admin | `!guilds wh-add 77176186148499456  MODLOG_CUSTOM_FORMAT` |
| `!guilds wh-rmv` `<guild id> <flag>` | Remove a flag from a guild, one of those listed in [CLI Interface](../cli-interface.md#valid-guild-flags) | Global Admin | `!guilds wh-rmv 77176186148499456  MODLOG_CUSTOM_FORMAT` |
| `!force setup <guild id>` | Forces the bot to run setup fro a specified guild. | Global Admin | `!force setup 77176186148499456` |



