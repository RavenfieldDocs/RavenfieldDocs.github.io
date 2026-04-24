---
title: Dropdown
---

Represents a Unity UI dropdown component accessible from Ravenscript.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `onValueChanged` | [ScriptEvent](./ScriptEvent.md) | Fires when the selected option changes. Arguments: `int value`. |
| `onPointerEnter` | [ScriptEvent](./ScriptEvent.md) | Fires when the pointer enters the dropdown area. |
| `onPointerExit` | [ScriptEvent](./ScriptEvent.md) | Fires when the pointer exits the dropdown area. |
| `onPointerClick` | `ScriptEvent<int>` | Fires when the dropdown is clicked with the pointer. |
| `onPointerDown` | `ScriptEvent<int>` | Fires when the pointer is pressed down on the dropdown. |
| `onPointerUp` | `ScriptEvent<int>` | Fires when the pointer is released on the dropdown. |

## Methods

## Events

| Event | Signature | Description |
|-------|-----------|-------------|
| `onValueChanged` | `(value)` | Triggered when the selected dropdown option changes. The `value` parameter is the index of the selected option. |
| `onPointerEnter` | [ScriptEvent](./ScriptEvent.md) | Triggered when the pointer enters the dropdown area. |
| `onPointerExit` | [ScriptEvent](./ScriptEvent.md) | Triggered when the pointer exits the dropdown area. |
| `onPointerClick` | `ScriptEvent<int>` | Triggered when the dropdown is clicked. |
| `onPointerDown` | `ScriptEvent<int>` | Triggered when the pointer is pressed down on the dropdown. |
| `onPointerUp` | `ScriptEvent<int>` | Triggered when the pointer is released on the dropdown. |

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

## Enums
