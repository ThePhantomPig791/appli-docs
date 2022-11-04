---
title: Swap Positions (Bi-entity Action Type)
date: 2022-11-03
---

# Swap Positions

[Bi-entity Action Type](../bientity_action_types.md)

Swaps the positions of the actor and target entities.

Type ID: `appli:swap_positions`

!!! note

    Using this action on more than 2 entities simultaniously will cause a kind of round-robin effect, with each entity being rotated around to the next place 'in line.'
    Because of this, if the action is executed on the same entities for the same amount of times that there are entities, everything will be put back to where it was before.


### Fields

_None._


### Examples

```json
"bientity_action": {
    "type": "appli:swap_positions"
}
```