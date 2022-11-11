---
title: UUID (Entity Condition Type)
date: 2022-11-11
---

# UUID

[Entity Condition Type](../entity_condition_types.md)

Checks if the UUID of an entity or player matches a specific string.

Type ID: `appli:uuid`

!!! note
    Include the dashes in the uuid.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`uuid` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) || The UUID to check for.


### Examples

```json
"entity_condition": {
    "type": "appli:uuid",
    "uuid": "3552cd12-b663-453c-9574-6b3ac6aa7459"
}
```

This example will check if the entity's UUID is "3552cd12-b663-453c-9574-6b3ac6aa7459".