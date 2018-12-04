# Tags Plugin

The tags plugin allows the ability to provide a custom command response to a set command.

#### 

## Commands <a id="commands"></a>

| Name | Description | Default Level | Usage |
| :--- | :--- | :--- | :--- |
| `!tags create` | Adds a warning infraction to a user | Trusted | `!tags add yes yes` OR `!tags create wow oh yes` |
| `!tags show {tag}` | Get the content of a tag | Trusted | `!tags show popcorn`   OR `!tags popcorn` |
| `!tags remove {tag}` | Remove tag by name | Trusted | `!tags remove popcorn` |
| `!tags info {tag}` | Get information on a tag | Trusted | `!tags info popcorn` |
| `!tags all` | List all tags for the server | Trusted | `!tags all` |

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

