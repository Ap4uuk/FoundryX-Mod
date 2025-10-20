# Foundryx Permission Guide (English)

This document lists every permission node exposed by Foundryx and the context in which it is used. All nodes live in the `foundryx.*` namespace. When no permission plugin is installed, Minecraft operator levels act as fallbacks (0 = all players, 2 = operator level 2, 3 = operator level 3). Servers with LuckPerms or another permission manager should assign nodes explicitly to retain the intended access model.

## Player Experience (Fallback 0)

| Command | Permission node | Notes |
| --- | --- | --- |
| `/home` | `foundryx.command.home` | Teleports the player to a saved home. |
| `/sethome` | `foundryx.command.sethome` | Creates or updates a personal home point. |
| `/delhome` | `foundryx.command.delhome` | Removes an existing home. |
| `/homes` | `foundryx.command.homes` | Lists stored homes for quick teleporting. |
| `/warp` | `foundryx.command.warp` | Teleports to a named public warp. |
| `/warps` | `foundryx.command.warps` | Displays all available warps. |
| `/spawn` | `foundryx.command.spawn` | Sends the player to the global spawn point. |
| `/balance` | `foundryx.command.balance` | Shows the player’s wallet balance. |
| `/pay` | `foundryx.command.pay` | Transfers currency to another player. |
| `/kit` | `foundryx.command.kit` | Claims an available kit. |
| `/afk` | `foundryx.command.afk` | Toggles manual AFK state. |
| `/near` | `foundryx.command.near` | Lists nearby players within the configured radius. |
| `/suicide` | `foundryx.command.suicide` | Respawns the player immediately. |
| `/motd` | `foundryx.command.motd` | Displays the message of the day. |
| `/tpa` | `foundryx.command.tpa` | Sends a teleport request to another player (alias: `/call`). |
| `/tpaccept` | `foundryx.command.tpaccept` | Accepts a pending teleport request. |
| `/tpdeny` | `foundryx.command.tpdeny` | Rejects a pending teleport request. |
| `/mail` | `foundryx.command.mail` | Opens the in-game mail interface. |
| `/msg` | `foundryx.command.msg` | Sends a private message (aliases: `/tell`, `/m`). |
| `/helpop` | `foundryx.command.helpop` | Contacts online staff with a help ticket. |
| `/rules` | `foundryx.command.rules` | Shows the server rule list. |
| `/help` | `foundryx.command.help` | Opens the categorized help menu. |

> **LuckPerms note:** Player-facing commands listed above require manual assignment when a permission plugin is present unless stated otherwise.

## Staff Toolkit (Fallback 2)

| Command | Permission node | Purpose |
| --- | --- | --- |
| `/setwarp` | `foundryx.command.setwarp` | Creates a public warp at the staff member’s location. |
| `/delwarp` | `foundryx.command.delwarp` | Removes a public warp. |
| `/setspawn` | `foundryx.command.setspawn` | Updates the server spawn point. |
| `/fly` | `foundryx.command.fly` | Toggles creative flight for the executor. |
| `/balance <player>` | `foundryx.command.balance.others` | Views another player’s balance. |
| `/heal` | `foundryx.command.heal` | Restores health and hunger. |
| `/feed` | `foundryx.command.feed` | Refills hunger only. |
| `/repair` | `foundryx.command.repair` | Repairs the held item. |
| `/repair all` | `foundryx.command.repair.all` | Repairs every item in the inventory. |
| `/repair armor` | `foundryx.command.repair.armor` | Repairs all worn armour pieces. |
| `/nick` colours | `foundryx.command.nick.color` | Enables colour codes inside `/nick`. |
| `/nick` formats | `foundryx.command.nick.format` | Enables bold/italic/other styles. |
| `/kill` | `foundryx.command.kill` | Eliminates a target entity or player. |
| `/time` | `foundryx.command.time` | Adjusts the world time. |
| `/weather` | `foundryx.command.weather` | Changes the weather cycle. |
| `/effect` | `foundryx.command.effect` | Applies or removes potion effects. |

These nodes keep their fallback access with LuckPerms enabled, but you can still fine-tune them by group.

## Administration & Moderation (Fallback 3)

| Command | Permission node | Purpose |
| --- | --- | --- |
| `/back` | `foundryx.command.back` | Returns to the previous location. |
| `/createkit` | `foundryx.command.createkit` | Saves the executor’s inventory as a kit. |
| `/delkit` | `foundryx.command.delkit` | Deletes an existing kit. |
| `/tp` | `foundryx.command.tp` | Teleports to a player or coordinates. |
| `/tphere` | `foundryx.command.tphere` | Summons a target player. |
| `/tppos` | `foundryx.command.tppos` | Teleports to explicit coordinates. |
| `/nick` (self) | `foundryx.command.nick` | Changes the executor’s nickname. |
| `/nickreset` others | `foundryx.command.nick.reset.others` | Resets another player’s nickname. |
| `/god` | `foundryx.command.god` | Toggles invulnerability. |
| `/gm` | `foundryx.command.gm` | Switches game modes. |
| `/hat` | `foundryx.command.hat` | Moves the held item to the helmet slot. |
| `/realname` | `foundryx.command.realname` | Reveals a player’s actual username. |
| `/helpop reply` | `foundryx.command.helpop.reply` | Responds to helpop tickets. |
| `/freeze` | `foundryx.command.freeze` | Prevents a player from moving. |
| `/eco` | `foundryx.command.eco` | Adjusts player balances directly. |
| `/ban` | `foundryx.command.ban` | Permanently bans a player. |
| `/tempban` | `foundryx.command.tempban` | Issues a timed ban. |
| `/banip` | `foundryx.command.banip` | Bans an IP address. |
| `/unban` | `foundryx.command.unban` | Removes a player ban. |
| `/unbanip` | `foundryx.command.unbanip` | Removes an IP ban. |
| `/banlist` | `foundryx.command.banlist` | Lists active bans. |
| `/kick` | `foundryx.command.kick` | Removes a player from the server. |
| `/vanish` | `foundryx.command.vanish` | Toggles vanish mode for moderation (alias: `/v`). |
| `/whois` | `foundryx.command.whois` | Shows a moderation profile for a player. |
| `/list` | `foundryx.command.list` | Displays the formatted player list. |
| `/gc` | `foundryx.command.gc` | Shows server performance statistics. |
| `/jail` | `foundryx.command.jail` | Sends a player to the configured jail. |
| `/setjail` | `foundryx.command.setjail` | Creates or updates a jail location. |
| `/unjail` | `foundryx.command.unjail` | Releases a jailed player. |
| `/mute` | `foundryx.command.mute` | Silences a player indefinitely. |
| `/tempmute` | `foundryx.command.tempmute` | Issues a timed mute. |
| `/unmute` | `foundryx.command.unmute` | Lifts a mute. |
| `/invsee` | `foundryx.command.invsee` | Opens another player’s inventory. |
| `/enderchest` (personal) | `foundryx.command.enderchest.small` | Accesses a personal remote ender chest. |
| `/enderchest` (expanded) | `foundryx.command.enderchest.large` | Opens an expanded ender chest for staff. |
| `/enderchest` (others) | `foundryx.command.enderchest.other` | Views another player’s ender chest. |
| `/clearchat` | `foundryx.command.clearchat` | Wipes public chat history for all players (alias: `/cc`). |
| `/clear` | `foundryx.command.clear` | Clears the executor’s inventory (or a target’s). |

## Non-Command Permissions

| Node | Purpose | Fallback |
| --- | --- | --- |
| `foundryx.chat.color` | Allows colour codes in public chat. | Operator level 2 |
| `foundryx.chat.format` | Allows bold/italic/underline/obfuscated chat formatting. | Operator level 2 |
| `foundryx.afk.kick_exempt` | Grants immunity to AFK kick timers. | Operator level 3 |
| `foundryx.command.list.hidden` | Allows `/list` to reveal vanished or hidden players. | Operator level 3 |
| `foundryx.kit.<id>` | Restricts access to individual kits. | Depends on kit definition |

## Best Practices

1. Grant broad access to groups using wildcards like `foundryx.command.player.*`, then remove sensitive nodes with explicit negatives.
2. Separate moderation teams (mutes/bans) from build teams (teleports/world edits) by crafting group-specific bundles.
3. Audit LuckPerms inheritance to ensure manual-grant commands remain available after installing the plugin.

