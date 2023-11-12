---
title: Radial Menu Entry (Data Type)
date: 2023-11-12
---

# Radial Menu Entry

[Data Type](../data_types.md)

An [Object](https://origins.readthedocs.io/en/latest/types/data_types/object/) which defines an entry for the [Radial Menu Entity Action](../entity_action_types/radial_menu.md).


### Fields

Field  | Type | Default | Description
-------|-----|---------------|-------------
`item` | [Item Stack](https://origins.readthedocs.io/en/latest/types/data_types/item_stack/) | | The item stack to display within the button for the entry.
`entity_action` | [Entity Action](https://origins.readthedocs.io/en/latest/types/entity_action_types/) | | The entity action to be executed if the player clicks on this entry.
`condition` | [Entity Condition](https://origins.readthedocs.io/en/latest/types/entity_condition_types/) | null | The condition that must be true for this entry to appear in the list.
`distance` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer) | -1 | The distance, in pixels, this entry will travel from the center. If -1, it will use 1/4th of the screen's width.
`velocity` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer) | -1 | The speed, in pixels per tick, at which the entry will move from the center. If -1, it will travel however fast it needs to travel to be at the destination in 3 seconds. (To calculate a distance and velocity values for a specific time, use the formula `time = distance / velocity`. As an average rule of thumb, the distance when `distance` is `-1` will be around `40`.)


### Examples

```json
{
    "item": {
        "item": "minecraft:water_bucket",
        "tag": "{display:{Name:'{\"text\":\"Place Water\"}'}}"
    },
    "entity_action": {
        "type": "apoli:block_action_at",
        "block_action": {
            "type": "apoli:set_block",
            "block": "minecraft:water"
        }
    }
}
```

This example, if selected by the player, will place a water block at the player's location.
<br>

```json
{
    "item": {
        "item": "minecraft:Lava_bucket",
        "tag": "{display:{Name:'{\"text\":\"Place Lava\"}'}}"
    },
    "entity_action": {
        "type": "apoli:block_action_at",
        "block_action": {
            "type": "apoli:set_block",
            "block": "minecraft:water"
        }
    },
    "condition": {
        "type": "apoli:dimension",
        "dimension": "minecraft:overworld",
        "inverted": true
    },
    "distance": 15,
    "velocity": 2
}
```

This example, if selected by the player, will place a lava block at the player's location. It will only appear in the menu if the player is **not** in the Overworld, and it will travel 15 pixels from the center at 2 pixels per tick.