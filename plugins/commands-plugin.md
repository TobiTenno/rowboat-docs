---
description: >-
  Controls usage of commands by level, channel, etc. There is a special case for
  the `tags-usr` name, which controls all tag usage.
---

# Commands Plugin

## Configuration Options

| Option | Description | Type | Default |
| :--- | :--- | :--- | :--- |
| lockdown | A mapping of commands and channels to whitelist | dict | empty |
| prefix | A mapping of channels to Censor Configurations | dict | empty |
| overrides | Command overrides  | dict | empty |

## Lockdown Configuration Options

| Option | Description | Type | Default |
| :--- | :--- | :--- | :--- |
| name | Name of the command to whitelist | string | empty |
| group | Command group to  whitelist | string | empty |
| plugin.name | Name of the plugin to whitelist | string | empty |
| out | Output options | dict | empty |
| out -&gt; channels | list of channels to whitelist | snowflake array | empty |



## Overrides Configuration Options

| Option | Description | Type | Default |
| :--- | :--- | :--- | :--- |
| name | Name of the command to override | string | empty |
| group | Command group to  override | string | empty |
| plugin.name | Name of the plugin to override | string | empty |
| out | Output options | dict | empty |
| out -&gt; level | level to restrict command to | snowflake array | empty |



```yaml
  commands:
    prefix: '!'
    overrides:
    - name: tempmute
      out:
        level: 40
    - name: mute
      out:
        level: 40
    - name: info
      out:
        level: 50
    - group: role
      out:
        level: 60
    lockdown:
    - name: info
      out:
        channels: [510415911560282132, 511870279157284874]
    - group: infractions
      out:
        channels: [510415911560282132, 511870279157284874]
    - plugin.name: admin
      out:
        channels: [510415911560282132, 511870279157284874]
```

