---
title: Action on Trade (Power Type)
date: 2023-12-18
---

# Action on Trade

[Power Type](../power_types.md)

Executes a bientity/item action upon trading with a villager.

Type ID: `appli:action_on_trade`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`item_action` | [Item Action](https://origins.readthedocs.io/en/latest/types/item_action_types/) | | The action to execute on the item stack that the player buys.
`bientity_action` | [Bi-entity Action](https://origins.readthedocs.io/en/latest/types/bientity_action_types/) | | The action to execute on both the trader and the player, with the player as the actor and the trader as the target.
`bientity_condition` | [Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | _null_ | The condition to check against both the trader and the player, with the player as the actor and the trader as the target.


### Examples

```json
{
    "type": "appli:action_on_trade",
    "item_action": {
        "type": "apoli:consume",
        "amount": 1
    },
    "bientity_action": {
        "type": "apoli:target_action",
        "action": {
            "type": "apoli:add_velocity",
            "y": 3
        }
    },
    "bientity_condition": {
        "type": "apoli:target_condition",
        "condition": {
            "type": "apoli:on_fire"
        }
    }
}
```

This example will decrement the bought stack by one and fling the trader up if the trader is on fire.