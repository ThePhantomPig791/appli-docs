---
title: Command (Block Condition Type)
date: 2022-11-11
---

# Command

[Block Condition Type](../block_condition_types.md)

Executes a command (as the block and at the block), and compares the output to a given value.

Essentially a copy of [Command (Entity Action)](https://origins.readthedocs.io/en/latest/types/entity_condition_types/command/), but for blocks.

Type ID: `appli:command`

!!! caution

    *To quote the Origins wiki,*
    This condition is only effective server-side. That means client-side power types such as [`origins:climbing`](https://origins.readthedocs.io/en/latest/types/power_types/climbing/), [`origins:entity_glow`](https://origins.readthedocs.io/en/latest/types/power_types/entity_glow/), [`origins:shader`](https://origins.readthedocs.io/en/latest/types/power_types/shader/), etc. won't work with this.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`command` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) || The command to be executed.
`comparison` | [Comparison](https://origins.readthedocs.io/en/latest/types/data_types/comparison/) || How to compare the stored result of the specified command to the specified value.
`compare_to` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) || The value to compare the stored result of the specified command to..


### Examples

```json
"block_condition": {
    "type": "appli:command",
    "command": "execute if block ~ ~ ~ minecraft:dirt",
    "comparison": "==",
    "compare_to": 0
}
```

This example will check if the block at the block's current position is not dirt.