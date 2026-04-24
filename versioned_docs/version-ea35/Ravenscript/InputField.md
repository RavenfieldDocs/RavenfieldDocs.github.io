---
title: InputField
---

Represents a Unity UI input field component accessible from Ravenscript.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `onValueChanged` | [ScriptEvent](./ScriptEvent.md) | Fires when the input field's text changes. Arguments: `string value`. |
| `onEndEdit` | [ScriptEvent](./ScriptEvent.md) | Fires when the input field is done being edited. Arguments: `string value`. |
| `onPointerEnter` | [ScriptEvent](./ScriptEvent.md) | Fires when the pointer enters the input field area. |
| `onPointerExit` | [ScriptEvent](./ScriptEvent.md) | Fires when the pointer exits the input field area. |
| `onPointerClick` | `ScriptEvent<int>` | Fires when the input field is clicked with the pointer. |
| `onPointerDown` | `ScriptEvent<int>` | Fires when the pointer is pressed down on the input field. |
| `onPointerUp` | `ScriptEvent<int>` | Fires when the pointer is released on the input field. |

## Methods

## Events

| Event | Signature | Description |
|-------|-----------|-------------|
| `onValueChanged` | `(value)` | Triggered when the input field's text changes. The `value` parameter is the new string value. |
| `onEndEdit` | `(value)` | Triggered when the input field is done being edited. The `value` parameter is the final string value. |
| `onPointerEnter` | [ScriptEvent](./ScriptEvent.md) | Triggered when the pointer enters the input field area. |
| `onPointerExit` | [ScriptEvent](./ScriptEvent.md) | Triggered when the pointer exits the input field area. |
| `onPointerClick` | `ScriptEvent<int>` | Triggered when the input field is clicked. |
| `onPointerDown` | `ScriptEvent<int>` | Triggered when the pointer is pressed down on the input field. |
| `onPointerUp` | `ScriptEvent<int>` | Triggered when the pointer is released on the input field. |

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

## Enums
