---
title: Radial Menu (Entity Action Type)
date: 2023-11-12
---

# Radial Menu

[Entity Action Type](../entity_action_types.md)

Opens a circular menu with a variable amount of entries, each of which can hold an entity action that will be executed if the player selects it.

Type ID: `appli:radial_menu`

!!! note
    The player can press the escape key to close the menu; they are not required to choose an entry from the list.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entries` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Radial Menu Entries](../data_types/radial_menu_entry.md) || An array of radial menu entry objects.


### Examples

```json
"entity_action": {
    "type": "appli:radial_menu",
    "entries": [
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
        },
        {
            "item": {
                "item": "minecraft:lava_bucket",
                "tag": "{display:{Name:'{\"text\":\"Place Lava\"}'}}"
            },
            "entity_action": {
                "type": "apoli:block_action_at",
                "block_action": {
                    "type": "apoli:set_block",
                    "block": "minecraft:lava"
                }
            }
        },
        {
            "item": {
                "item": "minecraft:barrier",
                "tag": "{display:{Name:'{\"text\":\"Place Air\"}'}}"
            },
            "entity_action": {
                "type": "apoli:block_action_at",
                "block_action": {
                    "type": "apoli:set_block",
                    "block": "minecraft:air"
                }
            }
        }
    ]
}
```

This example will give the player the choice of placing water, lava, or air at their location.