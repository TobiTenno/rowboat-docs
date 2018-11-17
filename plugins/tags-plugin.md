# Tags Plugin

The tags plugin allows the ability to provide a custom command response to a set command.

#### 

## Commands <a id="commands"></a>

| Name | Description | Default Level | Usage |
| :--- | :--- | :--- | :--- |
| `!tags create` | Adds a warning infraction to a user | Trusted | `!tags add yes yes` OR `!tags create wow oh yes` |

## Configuration Options

| Option | Description | Type | Default |
| :--- | :--- | :--- | :--- |
| max\_tag\_length | Maximum length for a tag | int | \* |
| max\_level\_remove\_others | Minimum level required to remove someone else's tag | int | 50 |

## Configuration Example

```yaml
  tags:
    max_tag_length: 100
    min_level_remove_others: 55
```

