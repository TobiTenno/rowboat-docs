# AutoLevel Plugin

The autolevel plugin provides a guild leveling system that can also reward roles to members for participating in chat and voice.  
The heimdallr autoleveling system also provides a means to have multiple guild leveling systems running at the same time. This can be used for things such as having specific category participation rewarding particular roles over another category which may reward another role. Each leveling system can be customized to have its own configuration.

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
      <td style="text-align:left"><code>!level</code>
      </td>
      <td style="text-align:left">Shows the users current points and levels in the current location that
        the command is run.</td>
      <td style="text-align:left">0</td>
      <td style="text-align:left"><code>!level</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p><code>!alevel show [user]</code>
        </p>
        <p>or</p>
        <p><code>!alevel ls [user]</code>
        </p>
      </td>
      <td style="text-align:left">Allows the moderator to list all autolevel indexes the user belongs to
        currently.</td>
      <td style="text-align:left">Moderator</td>
      <td style="text-align:left">
        <p><code>!alevel show [user]</code>
        </p>
        <p>or</p>
        <p><code>!alevel ls [user]</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p><code>!alevel give {user} {points} [index]</code>
        </p>
        <p>or</p>
        <p><code>!alevel add {user} {points} [index]</code>
        </p>
      </td>
      <td style="text-align:left">Adds a specified number of points to the user in the specified index.
        If no index is selected the default '0:0' is used which may or may not
        exist.</td>
      <td style="text-align:left">Administrator</td>
      <td style="text-align:left">
        <p><code>!alevel give {user} {points} [index]</code>
        </p>
        <p>or</p>
        <p><code>!alevel add {user} {points} [index]</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p><code>!alevel take {user} {points} [index]</code>
        </p>
        <p>or</p>
        <p><code>!alevel rm {user} {points} [index]</code>
        </p>
      </td>
      <td style="text-align:left">Removes a specified number of points to the user in the specified index.
        If no index is selected the default '0:0' is used which may or may not
        exist.</td>
      <td style="text-align:left">Administrator</td>
      <td style="text-align:left">
        <p><code>!alevel take {user} {points} [index]</code>
        </p>
        <p>or</p>
        <p><code>!alevel rm  {user} {points} [index]</code>
        </p>
      </td>
    </tr>
  </tbody>
</table>## Configuration Options

<table>
  <thead>
    <tr>
      <th style="text-align:left">Option</th>
      <th style="text-align:left">Description</th>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Default</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">include_roles</td>
      <td style="text-align:left">Which specific roles are included. If nothing is specified all roles are
        included.</td>
      <td style="text-align:left">snowflake list</td>
      <td style="text-align:left">[]</td>
    </tr>
    <tr>
      <td style="text-align:left">exclude_roles</td>
      <td style="text-align:left">Which specific roles are excluded.</td>
      <td style="text-align:left">snowflake list</td>
      <td style="text-align:left">[]</td>
    </tr>
    <tr>
      <td style="text-align:left">include_channels</td>
      <td style="text-align:left">Which specific channels are included. If nothing is specified all channels
        are included.</td>
      <td style="text-align:left">channelfield list</td>
      <td style="text-align:left">[]</td>
    </tr>
    <tr>
      <td style="text-align:left">exclude_channels</td>
      <td style="text-align:left">Which specific channels are excluded</td>
      <td style="text-align:left">channelfield list</td>
      <td style="text-align:left">[]</td>
    </tr>
    <tr>
      <td style="text-align:left">include_voice</td>
      <td style="text-align:left">Which voice channels are included if any in this configuration. No voice
        channels are included by default</td>
      <td style="text-align:left">channelfield list</td>
      <td style="text-align:left">[]</td>
    </tr>
    <tr>
      <td style="text-align:left">include_voice_category</td>
      <td style="text-align:left">Which specific categories will have all child voice channels included
        in this configuration.</td>
      <td style="text-align:left">channelfield list</td>
      <td style="text-align:left">[]</td>
    </tr>
    <tr>
      <td style="text-align:left">include_category</td>
      <td style="text-align:left">Which specific categories are included</td>
      <td style="text-align:left">channelfield list</td>
      <td style="text-align:left">[]</td>
    </tr>
    <tr>
      <td style="text-align:left">exclude_category</td>
      <td style="text-align:left">Which specific categories are excluded</td>
      <td style="text-align:left">channelfield list</td>
      <td style="text-align:left">[]</td>
    </tr>
    <tr>
      <td style="text-align:left">multiplier</td>
      <td style="text-align:left">Dict of how many points are awarded for each message or minute of voice
        activity</td>
      <td style="text-align:left">dict</td>
      <td style="text-align:left">None</td>
    </tr>
    <tr>
      <td style="text-align:left">multiplier_roles</td>
      <td style="text-align:left">
        <p>Dict of any roles that when applied award an additional multiplier of
          points off the base value. Format is</p>
        <p><code>roleid: x</code>
        </p>
      </td>
      <td style="text-align:left">dict</td>
      <td style="text-align:left">None</td>
    </tr>
    <tr>
      <td style="text-align:left">levels</td>
      <td style="text-align:left">Dict defining the number of points and the appropriate role that will
        be added to the user.</td>
      <td style="text-align:left">dict</td>
      <td style="text-align:left">None</td>
    </tr>
    <tr>
      <td style="text-align:left">keep_previous</td>
      <td style="text-align:left">If previously added roles will be kept when gaining the subsequent level</td>
      <td
      style="text-align:left">bool</td>
        <td style="text-align:left">False</td>
    </tr>
    <tr>
      <td style="text-align:left">announce_msg</td>
      <td style="text-align:left">Message to be posted when the user reaches a level</td>
      <td style="text-align:left">str</td>
      <td style="text-align:left">None</td>
    </tr>
    <tr>
      <td style="text-align:left">announce_chan</td>
      <td style="text-align:left">Channel the message will be posted to</td>
      <td style="text-align:left">channelfield</td>
      <td style="text-align:left">None</td>
    </tr>
    <tr>
      <td style="text-align:left">announce_dm</td>
      <td style="text-align:left">If the message will be DM'd to the user</td>
      <td style="text-align:left">bool</td>
      <td style="text-align:left">False</td>
    </tr>
    <tr>
      <td style="text-align:left">seconds_per_point</td>
      <td style="text-align:left">Number of seconds that must wait for another point to be applied</td>
      <td
      style="text-align:left">int</td>
        <td style="text-align:left">60</td>
    </tr>
    <tr>
      <td style="text-align:left">category</td>
      <td style="text-align:left">Dict containing a category id and configuration using all above options
        except another category</td>
      <td style="text-align:left">dict</td>
      <td style="text-align:left">None</td>
    </tr>
  </tbody>
</table>##  Levels Sub Configuration

| Option | Description | Type | Default |
| :--- | :--- | :--- | :--- |
| message | Number of points per message | int | 25 |
| voice | Number of points per 1 minute of voice activity | int | 25 |

## Configuration Example

```yaml
autolevel:
  seconds_per_point: 1
  keep_previous: true
  multiplier:
    message: 8
  levels:
    1000: 536728628680196126 
    2000: 536728691795951619 
    3000: 536728730714898442
  category:
    9843950989345098345:
      include_roles:
        - 3245098734095345980340
        - 239045823094823094823
      include_voice_category:
        - 9843950989345098345
      multiplier:
        message: 12
        voice: 25
      multiplier_roles:
        536728691795951619: 2
      levels:
        500: 2385947349805897345
        1500: 3245987345987345987
        3000: 34534509834509340598
        10000: 324590834509853450985
      keep_previous: true
      seconds_per_point: 15
      announce_msg: {user} has leveled up!! yeet!
      announce_chan: 3454908448974987444
    2394823904823487897:
      exclude_channels:
        - 238945723472384234987
        - 2354987324598734598755
      multiplier:
        message: 100
      levels:
        10000: 3458973458937534598
        25000: 23458974328974234984
        50000: 3459083450983458738
      seconds_per_point: 30
      keep_previous: true
    
```

