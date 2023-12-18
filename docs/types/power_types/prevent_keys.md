---
title: Prevent Keys (Power Type)
date: 2023-11-12
---

# Prevent Keys

[Power Type](../power_types.md)

Prevents certain keys from being pressed.

Type ID: `appli:prevent_keys`

!!! note

    **This power type will only work on players.**

!!! caution

    **__Be careful when testing this power type, as it's easy to softlock yourself. Additionally, keep in mind that you don't want to ever softlock _any_ player via your origin.__**

!!! note

    See also [Prevent Mouse (Power Type)](./prevent_mouse.md).


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`keys` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Integers](https://origins.readthedocs.io/en/latest/types/data_types/integer) | _optional_ | An array of [keycode values](https://www.cambiaresearch.com/articles/15/javascript-char-codes-key-codes) that will be prevented.


### Examples

```json
{
    "type": "appli:prevent_keys",
    "keys": [
        87,
        65,
        68
    ]
}
```

This example will make the player unable to press W, A, or D, therefore only letting them move with the S key. See a [list of keycode values](https://www.cambiaresearch.com/articles/15/javascript-char-codes-key-codes) for more details.