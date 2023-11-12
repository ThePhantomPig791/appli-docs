---
title: Prevent Mouse (Power Type)
date: 2023-11-12
---

# Prevent Mouse

[Power Type](../power_types.md)

Prevents the mouse from receiving input in-game (inventories, screens, etc. still work).

Type ID: `appli:prevent_mouse`

!!! note

    **This power type will only work on players.**

!!! caution

    **__Be careful when testing this power type, as it's easy to softlock yourself. Additionally, keep in mind that you don't want to ever softlock _any_ player via your origin.__**

!!! note

    See also [Prevent Keys (Power Type)](./prevent_keys.md).


### Fields

_None._


### Examples

```json
{
    "type": "appli:prevent_mouse"
}
```

This example will make the player unable to use their mouse in-game.
<br>

```json
{
    "type": "appli:prevent_mouse",
    "condition": {
        "type": "apoli:on_fire"
    }
}
```

This example will make the player unable to use their mouse in-game while they are on fire.