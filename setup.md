# Setting Up Heimdallr

## Adding the Bot

Heimdallr is only available to servers that meet certain criteria:

* The server does not promote or promulgate NSFW content
* Heimdallr will be used to moderate, not simply as a fixture or for "testing"
* Has been reviewed and approved by Tobiah\#0001

## How to Set Up

Once rowboat has been added to your server, go to [https://mod.warframe.gg/](https://mod.warframe.gg) to edit your server's configuration. Use the sidebar to read about each plugin, then use the example below along with the information in the sidebar to set up your own customized rowboat configuration.

Below is a blank configuration example with web, utilities, admin, infractions, modlog, spam, and censor set up. While you can simply copy-paste this to your own server's configuration and fill in the blanks to have a perfectly usable rowboat, it's highly encouraged that you read through the full documentation to understand each component and customize rowboat to your server's needs.

```yaml
web:
  000000000000000000: admin   # Username
  000000000000000000: editor  # Username
  000000000000000000: viewer  # Username

commands:
  prefix: '!'
  overrides: []

levels:
  000000000000000000: 000 # Role

nickname: R0WB0AT

plugins:

  utilities: {}

  admin: {}

  infractions:
    mute_role: 000000000000000000 # Muted

  modlog:
    channels:
      00000000000000000000000: # We recommend adding comments to mark ids with names
        exclude: []
        include: []
    ignored_users: []

  spam:
    levels:
      0:
        punishment: TEMPMUTE
        punishment_duration: 120
        max_messages:
          count: 10
          interval: 7
        max_mentions:
          count: 8
          interval: 30
        max_links:
          count: 10
          interval: 60
        max_emojis:
          count: 100
          interval: 120
        max_newlines:
          count: 60
          interval: 120
        max_duplicates:
          count: 5
          interval: 30

  censor:
    levels:
      0:
        filter_invites: true
        invites_whitelist: 
          - 'discord-developers'
          - 'discord-testers'
          - 'discord-api'
          - 'events'
          - 'discord-linux'
          - 'gamenight'
          - 'discord-feedback'
        blocked_words: ['word1', 'word2', 'word3']
```



## Example Minimum config

```yaml
commands:
  prefix: '!'

levels:
  180768265633660928: 100   # Server Admin Role Id
  131682843326808064: 99    # server admin bot Role Id
  274266640403791873: 60    # Senior Moderator Role Id
  77190254141911040: 50     # Moderator Role Id
  335114792820015106: 10    # Bot Role Id

nickname: C3PHAL0N

plugins:
  admin:
    confirm_actions: true
    confirm_actions_reaction: true
    mute_role: 335132902025330688 # Mute Role
    reason_edit_level: 60
    temp_mute_role: 335132902025330688
  
    
  infractions:
    confirm_actions: true
    confirm_actions_expiry: 10
    confirm_actions_reaction: true
    mute_role: 335132902025330688 # Mute Role Id
    reason_edit_level: 60
    temp_mute_role: 335132902025330688 # Mute Role Id
    
    notify:
      WARN:
        format: true
      BAN:
        format: true
      TEMPMUTE:
        format: true
      MUTE:
        format: true
      TEMPBAN:
         format: true
    
  modlog:
    channels:
      171383278048247808: # Your server log
        exclude: []
        compact: false
        timestamps: true
  utilities: {}
web:
  76685590585671680: admin      # Tobiah
```

### Example just to get going

```text
commands:
  prefix: '!'
​
levels:
  180768265633660928: 100   # Your role id
​
plugins:
  utilities: {}
web:
  76685590585671680: admin      # Tobiah
```

