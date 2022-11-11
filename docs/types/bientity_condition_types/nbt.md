---
title: Nbt (Bi-entity Condition Type)
date: 2022-11-11
---

# NBT

[Bi-entity Condition Type](../bientity_condition_types.md)

Checks if the NBT value of two specific paths are the same for the actor and target.

Type ID: `appli:nbt`

!!! note

    Due to my dodgy programming, you can only specify paths with periods, not brackets. Additionally, you can't get sub-sub data, only sub-data or root data. So it's possible get "data" and "data.testUUID", but not "data.object.testUUID".


### Fields

Field | Type | Default | Description
------|------|---------|------------
`actor_nbt` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) || The nbt path for the actor.
`target_nbt` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) || The nbt path for the target.


### Examples

```json
"bientity_condition": {
    "type": "appli:nbt",
    "actor_nbt": "UUID",
    "target_nbt": "data.testUUID"
}
```

This example will check if the actor's nbt value at UUID is the same as the target's nbt value at data.testUUID (sidenote: only marker entities have a "data" field that can be filled with whatever you want).