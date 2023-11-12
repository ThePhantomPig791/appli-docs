---
title: Modify Model Parts (Power Type)
date: 2023-11-12
---

# Modify Model Parts

[Power Type](../power_types.md)

Modifies (rotates, scales, transforms) an entity's individual model parts.

Type ID: `appli:modify_model_parts`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`transformations` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Model Part Transformations](../data_types/model_part_transformation.md) | | An array of model part transformation objects.


### Examples

```json
{
    "type": "appli:modify_model_parts",
    "transformations": [
        {
            "model_part": "head",
            "type": "xscale",
            "value": 1
        },
        {
            "model_part": "head",
            "type": "yscale",
            "value": 1
        },
        {
            "model_part": "head",
            "type": "zscale",
            "value": 1
        },

        {
            "model_part": "hat",
            "type": "xscale",
            "value": 1
        },
        {
            "model_part": "hat",
            "type": "yscale",
            "value": 1
        },
        {
            "model_part": "hat",
            "type": "zscale",
            "value": 1
        }
    ]
}
```

This example will make the entity's head hat layer twice as big. See [Model Part Transformation](../data_types/model_part_transformation.md) for more details.