---
title: Model Part Transformation (Data Type)
date: 2023-11-12
---

# Model Part Transformation

[Data Type](../data_types.md)

An [Object](https://origins.readthedocs.io/en/latest/types/data_types/object/) which defines a model part and its transformation for the [Modify Model Parts power](../power_types/modify_model_parts.md).


### Fields

Field  | Type | Default | Description
-------|-----|---------------|-------------
`model_part` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string) || The name of the model part to modify. Accepts `head`, `hat`, `body`, `rightarm`, `leftarm`, `rightleg`, `leftleg`. Casing does not matter.
`type` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string) || The type of transformartion to apply. Accpets `pitch`, `yaw`, `roll`, `visible`, `hidden`, `xscale`, `yscale`, `zscale`, `pivotx`, `pivoty`, `pivotz`. Casing does not matter.
`value` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float) || The value to add to the selected transformation type. In the case of the transform types `visible` and `hidden`, which are booleans, 0 is false while anything else is true.


### Examples

```json
{
    "model_part": "head",
    "type": "xscale",
    "value": 1
}
```

This example will make the entity's head (**not** including the hat layer) twice as big (new = original + old; new = 1 + 1) on the x axis, which in local axis terms means left to right.
<br>

```json
{
    "model_part": "body",
    "type": "zscale",
    "value": 1
}
```

This example will make the entity's body (**including** the jacket layer for players) twice as big on the z axis, which in local axis terms means front to back.
<br>

```json
{
    "model_part": "leftarm",
    "type": "pitch",
    "value": 1.57
}
```

This example will make the entity's left arm (**including** the outer left arm layer for players) rotate on the x axis to be (almost) upside down, as `1.57` is roughly `pi/2` and the `value` for rotations is measured in radians.