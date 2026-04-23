---
title: Input
---

Static class for reading player input from key binds, mouse, and axes.

## Properties

## Methods

### GetKeyBindButton

Get key bind as button. Returns true while the button is held down.

| Parameter | Type | Description |
|-----------|------|-------------|
| `keyBind` | `KeyBinds` | The key bind to check. |

[return: bool]

### GetKeyBindButtonDown

Get key bind as button down. Returns true the frame the button was pressed.

| Parameter | Type | Description |
|-----------|------|-------------|
| `keyBind` | `KeyBinds` | The key bind to check. |

[return: bool]

### GetKeyBindButtonUp

Get key bind as button up. Returns true the frame the button was released.

| Parameter | Type | Description |
|-----------|------|-------------|
| `keyBind` | `KeyBinds` | The key bind to check. |

[return: bool]

### GetKeyBindAxis

Get key bind as axis. Returns a value between -1 and 1.

| Parameter | Type | Description |
|-----------|------|-------------|
| `keyBind` | `KeyBinds` | The key bind to check. |

[return: float]

### GetMouseSensitivity

The current mouse sensitivity in degrees per mouse unit. The mouse sensitivity changes depending on current weapon aim zoom level.

[return: float]

### DisableNumberRowInputs

Disables game key bind input from number row keys. This is typically used to get player input from the number keys without triggering a weapon change.

### EnableNumberRowInputs

Enables game key bind input from number row keys.

## Events

## Static Fields

## Static Methods

## Enums
