---
title: Action on Kill (Power Type)
date: 2023-12-23
---

# Action on Kill

[Power Type](../power_types.md)

Executes a bientity action upon killing an entity.

Type ID: `appli:action_on_kill`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_action` | [Bi-entity Action](https://origins.readthedocs.io/en/latest/types/bientity_action_types/) | | The action to execute, with the player/power holder as the actor and the dying entity as the target.
`bientity_condition` | [Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | _optional_ | The condition to check, with the player/power holder as the actor and the dying entity as the target.
`damage_condition` | [Damage Condition](https://origins.readthedocs.io/en/latest/types/damage_condition_types/) | _optional_ | The condition to check against the damage source.

### Examples

```json
{
    "type": "appli:action_on_kill",
    "bientity_action": {
        "type": "apoli:invert",
        "action": {
            "type": "apoli:add_velocity",
            "z": 3
        }
    }
}
```

This example will fling the player/killer away from anything it kills.