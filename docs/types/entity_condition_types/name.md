---
title: Name (Entity Condition Type)
date: 2022-11-11
---

# Name

[Entity Condition Type](../entity_condition_types.md)

Checks if the name of an entity or player matches a specific string. (This condition works client-side, so it can be used in [Conditioned Origins](https://origins.readthedocs.io/en/latest/json/conditioned_origin/).)

Type ID: `appli:name`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`name` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) || The name to check for.
`match_case` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) |`false`| Whether the `name` field should need to match the casing of the entity's name.


### Examples

```json
"entity_condition": {
    "type": "appli:name",
    "name": "Pig",
    "match_case": false
}
```

This example will check if the entity's name is "Pig" (or any other casing).


```json
"entity_condition": {
    "type": "appli:name",
    "name": "BizeeB"
}
```

This example will check if the entity's name is exactly "BizeeB".