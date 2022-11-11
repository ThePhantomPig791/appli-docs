---
title: Teleport (Bi-entity Action Type)
date: 2022-11-03
---

# Teleport

[Bi-entity Action Type](../bientity_action_types.md)

Either teleports the actor to the target, or swaps the position of the actor and target.

Type ID: `appli:teleport`

!!! note

    Using this action with the "swap" field set to true on more than two entities simultaniously will cause a kind of round-robin effect, with each entity being rotated around to the next place 'in line.'
    Because of this, if the action (with "swap": true) is executed on the same entities for the same amount of times that there are entities, everything will be put back to where it was before.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`swap` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | If true, the entities will swap positions instead of just teleporing the actor to the target.


### Examples

```json
"bientity_action": {
    "type": "appli:teleport",
    "swap": false
}
```