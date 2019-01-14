# Changelog

#### 14 Jan 2018

* Mobile modding, requires `mobile_mod_channel` to be configured in the admin plugin, allows initiation of mod actions via `!minfo {user id}` or reacting with 🔗 \(link emote\) on a message. The bot will walk the mod through moderation options

#### 10 Jan 2018

* `shut`/`unshut` commands to force everyone to PTT \(once discord fixes its bug, it will make no one able to speak\)
* `force setup` for a guild in cases where admins on the server cannot run it or there is an error doing it the traditional way.

#### 4 Jan 2018

* Cease/uncease \(yeet/yote\) commands to lock down channel or guild easily.
* Move archive and backup commands to admin level
* Global admin command override
* Advanced user info search
* Advanced infraction search
* Advanced user infraction lookup
* Bot status setting
* Documentation for whitelisting/unwhitelisting
* Guild Flag editing
* Mass unban/ban/mute/unmute commands
* Document some sql plugin commands
* SQL optimizations
* Frontend statistics support
* `!timeleft` to allow muted users to check remaining time

#### 18 Dec 2018

* Added control messages for dm's to the bot
* Added control message for global admin going live
* Added override command for global admins to have to use override command to enable override mode in specific servers or all. \(Sends a control message, no more than 3600s\)

#### 14 Dec 2018

* Added `dm_denied` option, allowing server owners to have the bot DM the users who attempt to use commands that are denied, or to leave it silent. \(True notifies, False does not\)
* Added `global_blacklist` and `local_blacklist`, allowing bot owner and server owners, respectively, to provide a list of users for the bot to ignore globally and per-server, respectively.

#### 10 Dec 2018

* Added  exclude\_msg\_usr to allow excluding a user from logging
* Alias for `clean all` as `clear`

#### 6 Dec 2018

* Added channel\_whitelist config option to spam filtering

#### 5 Dec 2018

* Added custom commands plugin page with detail about configuration
* Added slowmode notes to admin plugin
* Added floof command notes to utilities
* Added aliases to cat and dog commands
* Noted that when search returns a single result it will automatically turn into the info command
* Added detail to infractions regarding hard\_mute\_ignore option
* Added detail to infractions regarding temprole command

#### 3 Dec 2018

* Allow tags to have a role whitelisted wherein that role can run tags anywhere
* Allow commands to be whitelisted for a role to run it anywhere

#### 20 November 2018

* Say commands with/enabling config \(`!say channel #channel message` and `!say user @user message`\)
* Tags as first-class dynamic commands locked to admins.

#### 17 November 2018

* Role Info command \(notable perms\)
* User info enhancement \(notable perms\)
* Track role counts
* Avatar command for checking user avatar
* Increase info timeout

#### 

#### 16 November 2018

* Remove forceban, ban automatically checks it
* Restrict commands to specific channels
* Whitelist channels from incurring specific censors
* Automatically move muted user to AFK or override VC



