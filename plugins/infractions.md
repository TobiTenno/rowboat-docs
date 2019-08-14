# Infractions Plugin

The infractions plugin provides a set of useful moderator commands. These commands are intended to be used together and help handle/track misbehaving users over time.

## Commands

<table>
  <thead>
    <tr>
      <th style="text-align:left">Name</th>
      <th style="text-align:left">Description</th>
      <th style="text-align:left">Default Level</th>
      <th style="text-align:left">Usage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>!warn {user} [reason]</code>
      </td>
      <td style="text-align:left">Adds a warning infraction to a user</td>
      <td style="text-align:left">Moderator</td>
      <td style="text-align:left"><code>!warn 232921983317180416 1st warning, spamming emoji</code> OR <code>!warn @rowboat#0001 2nd warning, going off-topic</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!mute {user} [reason]</code>
      </td>
      <td style="text-align:left">Mutes a user. This will only work if <code>mute_role</code> is set in the
        config</td>
      <td style="text-align:left">Moderator</td>
      <td style="text-align:left"><code>!mute 232921983317180416 spamming</code> OR <code>!tempmute @rowboat#0001 60m spamming</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!unmute {user}</code>
      </td>
      <td style="text-align:left">Unmutes a user</td>
      <td style="text-align:left">Moderator</td>
      <td style="text-align:left"><code>!unmute 232921983317180416</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!tempmute {user} {duration} [reason]</code>
      </td>
      <td style="text-align:left">Temporarily mutes a user. Will only work if <code>temp_mute_role</code> or <code>mute_role</code> is
        set in the config</td>
      <td style="text-align:left">Moderator</td>
      <td style="text-align:left">
        <p><code>!mute 232921983317180416 30m spamming</code>
        </p>
        <p>OR</p>
        <p><code>!tempmute 232921983317180416 30m spamming</code> OR <code>!tempmute @rowboat#0001 30m spamming</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!kick {user} [reason]</code>
      </td>
      <td style="text-align:left">Kicks the user from the server</td>
      <td style="text-align:left">Moderator</td>
      <td style="text-align:left"><code>!kick 232921983317180416 spamming</code> OR <code>!kick @rowboat#0001 spamming</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!mkick {users] -r [reason]</code>
      </td>
      <td style="text-align:left">Kicks multiple users from the server</td>
      <td style="text-align:left">Moderator</td>
      <td style="text-align:left"><code>!mkick 232921983317180416 80351110224678912 108598213681922048 -r spamming</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!ban {user} [reason]</code>
      </td>
      <td style="text-align:left">Bans a user from the server</td>
      <td style="text-align:left">Moderator</td>
      <td style="text-align:left"><code>!ban 232921983317180416 spamming</code> OR <code>!ban @rowboat#0001 spamming</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!unban {user} [reason]</code>
      </td>
      <td style="text-align:left">Unbans a user</td>
      <td style="text-align:left">Moderator</td>
      <td style="text-align:left"><code>!unban 232921983317180416</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!softban {user} [reason]</code>
      </td>
      <td style="text-align:left">Softbans (bans/unbans) a user and deletes the user&apos;s messages sent
        within the last 7 days</td>
      <td style="text-align:left">Moderator</td>
      <td style="text-align:left"><code>!softban 232921983317180416 spamming</code> OR <code>!softban @rowboat#0001 spamming</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!tempban {user} {duration} [reason]</code>
      </td>
      <td style="text-align:left">Temporarily bans a user</td>
      <td style="text-align:left">Moderator</td>
      <td style="text-align:left"><code>!tempban 232921983317180416 5h spamming</code> OR <code>!tempban @rowboat#0001 5h spamming</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!inf archive</code>
      </td>
      <td style="text-align:left">Creates a CSV file of all infractions on the server</td>
      <td style="text-align:left">Administrator</td>
      <td style="text-align:left"><code>!infractions archive</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!inf search {query}</code>
      </td>
      <td style="text-align:left">Searches infractions database for given query</td>
      <td style="text-align:left">Moderator</td>
      <td style="text-align:left"><code>!inf search 232921983317180416</code> OR <code>!inf search rowboat#0001</code> OR <code>!inf search spamming</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!inf info {inf#}</code>
      </td>
      <td style="text-align:left">Presents information on the given infraction</td>
      <td style="text-align:left">Moderator</td>
      <td style="text-align:left"><code>!inf info 1274</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!inf delete {inf#}</code>
      </td>
      <td style="text-align:left">Delete infraction</td>
      <td style="text-align:left">Admin</td>
      <td style="text-align:left"><code>!inf delete 1274</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!inf duration {inf#} {duration}</code>
      </td>
      <td style="text-align:left">Updates the duration of the given infraction. Duration starts from time
        of initial action</td>
      <td style="text-align:left">Moderator</td>
      <td style="text-align:left"><code>!inf duration 1274 5h</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!inf reason {inf#} {reason}</code>
      </td>
      <td style="text-align:left">Updates the reason of a given infraction</td>
      <td style="text-align:left">Moderator</td>
      <td style="text-align:left"><code>!inf reason 1274 rude behaviour towards staff</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!slowmo {time in seconds}</code>
      </td>
      <td style="text-align:left">Sets the slowmode time for the channel</td>
      <td style="text-align:left">Moderator</td>
      <td style="text-align:left"><code>!slowmo 10</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!slowmo 0</code>
      </td>
      <td style="text-align:left">Turn off slowmode for the channel</td>
      <td style="text-align:left">Moderator</td>
      <td style="text-align:left"><code>!slowmo 0</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!report {message}</code>
      </td>
      <td style="text-align:left">Send a report to a report channel</td>
      <td style="text-align:left">Everyone</td>
      <td style="text-align:left"><code>!report @Tobiah is being a meanie</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!selfmute / muteself {duration}</code>
      </td>
      <td style="text-align:left">Mute yourself for the given duration. Maximum of <code>2w</code>
      </td>
      <td style="text-align:left">Everyone</td>
      <td style="text-align:left"><code>!selfmute 2m</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!note add {user} {note}</code>
      </td>
      <td style="text-align:left">Add a note on a user</td>
      <td style="text-align:left">Mod</td>
      <td style="text-align:left"><code>!note add 222617379421683712 omaiwamo shinderu</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!note delete {inf#}</code>
      </td>
      <td style="text-align:left">Delete note on user</td>
      <td style="text-align:left">Admin</td>
      <td style="text-align:left"><code>!note delete 1275</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!note info {inf#}</code>
      </td>
      <td style="text-align:left">Get full details on a note</td>
      <td style="text-align:left">Mod</td>
      <td style="text-align:left"><code>!note info 1275</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!note search {query}</code>
      </td>
      <td style="text-align:left">Search for a note with the specified query</td>
      <td style="text-align:left">Mod</td>
      <td style="text-align:left"><code>!note search @user1</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!inf recent {# recent}</code>
      </td>
      <td style="text-align:left">Get recent infractions</td>
      <td style="text-align:left">Mod</td>
      <td style="text-align:left"><code>!inf recent 5</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!note archive</code>
      </td>
      <td style="text-align:left">Get an archive of notes</td>
      <td style="text-align:left">Admin</td>
      <td style="text-align:left"><code>!note archive</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!temprole {user} {role} {duration} {reason}</code>
      </td>
      <td style="text-align:left">Adds a role temporarily to a user</td>
      <td style="text-align:left">Mod</td>
      <td style="text-align:left"><code>!temprole @user1 StronkRole 1h stronk for 1h</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!hardmute enable {user} {reason}</code>
      </td>
      <td style="text-align:left">Hard mutes a user</td>
      <td style="text-align:left">Mod</td>
      <td style="text-align:left"><code>!hardmute enable @user1 being really silly</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!hardmute temp {user} {duration} {reason}</code>
      </td>
      <td style="text-align:left">Hard mutes a user temporarily</td>
      <td style="text-align:left">Mod</td>
      <td style="text-align:left"><code>!hardmute temp @user1 6h being really silly</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!hardmute disable {user}</code>
      </td>
      <td style="text-align:left">Disables an active hard mute on a user</td>
      <td style="text-align:left">Mod</td>
      <td style="text-align:left"><code>!hardmute disable @user1</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!mban {users] -r [reason]</code>
      </td>
      <td style="text-align:left">Bans multiple users from the server</td>
      <td style="text-align:left">Moderator</td>
      <td style="text-align:left"><code>!mban 232921983317180416 80351110224678912 108598213681922048 -r spamming</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!munban {users] -r [reason]</code>
      </td>
      <td style="text-align:left">Unbans multiple users from the server</td>
      <td style="text-align:left">Moderator</td>
      <td style="text-align:left"><code>!munban 232921983317180416 80351110224678912 108598213681922048 -r spamming</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!mmute {users] -r [reason]</code>
      </td>
      <td style="text-align:left">Mutes multiple users on the server</td>
      <td style="text-align:left">Moderator</td>
      <td style="text-align:left"><code>!mmute 232921983317180416 80351110224678912 108598213681922048 -r spamming</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!munmute {users] -r [reason]</code>
      </td>
      <td style="text-align:left">Unmute multiple users on the server</td>
      <td style="text-align:left">Moderator</td>
      <td style="text-align:left"><code>!munmute 232921983317180416 80351110224678912 108598213681922048 -r spamming</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>!timeleft</code>
      </td>
      <td style="text-align:left">Allow muted user to check their remaining time in their mute</td>
      <td style="text-align:left">Default</td>
      <td style="text-align:left"><code>!timeleft</code>
      </td>
    </tr>
  </tbody>
</table>## Configuration Options

| Option | Description | Type | Default |
| :--- | :--- | :--- | :--- |
| confirm\_actions | Whether to confirm that an action was done in the current channel | bool | true |
| confirm\_actions\_reaction | Whether to confirm actions done in the channel using a checkmark reaction | bool | false |
| confirm\_actions\_expiry | The duration after which to delete the confirmed action message. If zero the message will never be deleted | int | 0 |
| mute\_role | Role ID that is set for users who are muted | id | none |
| reason\_edit\_level | Minimum level to allow users to edit other users' infraction reasons | int | 100 |
| report\_channel | Channel to send reports to | id | none |
| report\_role | Role to ping for reports | id | none |
| selfmute | Whether to allow selfmutes | bool | false |
| selfmute\_max | Maximum duration for a selfmute in seconds.  | int | 1209600 \(2 weeks\) |
| selfmute\_role | Role ID that is set for users who self-mute | id | none |
| notify | Configure what infractions should notify users | dict | none |
| hard\_mute\_role | Role ID that is set for users who are hard-muted | id | none |
| hard\_mute\_ignore | Users belonging to any of the defined role id's will ignore any hard mutes | list id | \[\] |
| vc\_mute | Whether or not to attempt to move muted user to guild defined AFK channel | bool | false |
| vc\_mute\_channel | Channel to override guild define AFK channel with. Requires `vc_mute` | id | none |

## Notify Sub-configuration

Valid Actions: `WARN`, `TEMPMUTE`, `MUTE`, `TEMPBAN`, `BAN`

| Option | Description | Type | Default |
| :--- | :--- | :--- | :--- |
| format | Format for warn notifications. if "true" is specified, it will use the default configuration | string | false |
| emoji | Emoji to override for the config | string | no\_mouth |

## Configuration Example

```yaml
  infractions:
    confirm_actions: false
    mute_role: 289494296703533058
    reason_edit_level: 50
    report_channel: 297917022300274688
    vc_mute: true
    vc_mute_channel: 77177426521624576
    notify:
      WARN:
        format: |-
          {action!s}
          You have been **{action!s}**
          **Guild**: {guild.name}
          **Moderator**: {actor!s}
          **Reason**: {reason!s}
      TEMPMUTE:
        format: |-
          {action!s}
          You have been **{action!s}**
          **Guild**: {guild.name}
          **Moderator**: {actor!s}
          **Expires**: {expires} GMT+0
          **Reason**: {reason!s}
      MUTE:
        format: false
      TEMPBAN:
        format: |-
          {action!s}
          You have been **{action!s}**
          **Guild**: {guild.name}
          **Moderator**: {actor!s}
          **Expires**: {expires} GMT+0
          **Reason**: {reason!s}
      BAN:
        format: true
```

