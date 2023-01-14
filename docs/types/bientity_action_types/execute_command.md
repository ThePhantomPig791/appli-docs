---
title: Execute Command (Bi-entity Action Type)
date: 2022-11-11
---

# Execute Command

[Bi-entity Action Type](../bientity_action_types.md)

Executes a command as the actor/target and at the location of the actor/target.

Type ID: `appli:execute_command`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`as` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) || Who the command is executed as. Must be either "actor" or "target" (ignores casing). (Anything except "actor" will be read as "target".)
`at` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) || Who the command is executed at. Must be either "actor" or "target" (ignores casing). (Anything except "actor" will be read as "target".)
`command` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) || The command to be executed.


### Examples

```json
"bientity_action": {
    "type": "appli:execute_command",
    "as": "actor",
    "at": "target",
    "command": "tp @s ~ ~ ~"
}
```

This example will teleport the actor to the target.
