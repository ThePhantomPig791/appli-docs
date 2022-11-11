---
title: Motion (Entity Condition Type)
date: 2022-11-11
---

# Name

[Entity Condition Type](../entity_condition_types.md)

Compares the entity's motion in a specific direction to a specific value.

Type ID: `appli:motion`

!!! note
    Entities affected by gravity will almost never have a Y motion of 0, because of how gravity and block collision works. If you're trying to check if an entity is(n't) falling, you should use [On Block (Entity Condition)](https://origins.readthedocs.io/en/latest/types/entity_condition_types/on_block/) instead.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`direction` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) || The direction to check motion in. Accepts `x`, `y`, or `z`.
`comparison` | [Comparison](https://origins.readthedocs.io/en/latest/types/data_types/comparison/) || How to compare the motion in the specified direction to the specified value.
`compare_to` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) || The value to compare the motion in the specified direction to.


### Examples

```json
"entity_condition": {
    "type": "appli:motion",
    "direction": "x",
    "comparison": "!=",
    "compare_to": 0
}
```

This example will check if entity is moving in the X direction.