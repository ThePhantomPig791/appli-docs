---
title: Prevent Trade (Power Type)
date: 2023-12-18
---

# Prevent Trade

[Power Type](../power_types.md)

Prevents the player from trading with a trader (villager / wandering trader).

Type ID: `appli:prevent_trade`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`buy_item_condition` | [Item Condition](https://origins.readthedocs.io/en/latest/types/item_condition_types/) | _null_ | The condition to check the item stack being bought from the trader against.
`sell_item_condition` | [Item Condition](https://origins.readthedocs.io/en/latest/types/item_condition_types/) | _null_ | The condition to check the first item stack being sold to the trader against.
`second_sell_item_condition` | [Item Condition](https://origins.readthedocs.io/en/latest/types/item_condition_types/) | _null_ | The condition to check the second item stack being sold to the trader against.
`bientity_condition` | [Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | _null_ | The condition to check against both the trader and the player, with the player as the actor and the trader as the target.
`buy_item_condition_consider_adjustments` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `true` | Whether the `buy_item_condition` field should consider the adjustments made to the buy item, such as discounts or mark-ups.


### Examples

```json
{
    "type": "appli:prevent_trade"
}
```

This example will prevent the player from trading.

```json
{
    "type": "appli:prevent_trade",
    "sell_item_condition": {
        "type": "apoli:ingredient",
        "ingredient": {
            "item": "minecraft:emerald"
        }
    },
    "second_sell_item_condition": {
        "type": "apoli:ingredient",
        "ingredient": {
            "item": "minecraft:emerald"
        }
    }
}
```

This example will prevent the player from selling any emeralds to a villager.