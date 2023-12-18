---
title: Prevent Item Pickup (Power Type)
date: 2023-12-18
---

# Prevent Item Pickup

[Power Type](../power_types.md)

Prevents the player from picking up certain (or all) items.

Type ID: `appli:prevent_item_pickup`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`item_condition` | [Item Condition](https://origins.readthedocs.io/en/latest/types/item_condition_types/) | _null_ | The condition to check the item stack with.
`bientity_condition` | [Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | _null_ | The condition to check against both the item stack entity and the player, with the player as the actor and the item stack as the target.


### Examples

```json
{
    "type": "appli:prevent_item_pickup"
}
```

This example will prevent the player from picking up any items off the ground.

```json
{
    "type": "appli:prevent_item_pickup",
    "item_condition": {
        "type": "apoli:ingredient",
        "ingredient": {
            "item": "minecraft:dirt"
        }
    }
}
```

This example will prevent the player from picking up any dirt items.