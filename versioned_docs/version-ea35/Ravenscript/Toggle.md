---
title: Toggle
---

Represents a Unity UI Toggle component accessible from Ravenscript.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `onValueChanged` | `ScriptEvent` | Fires when the toggle value changes. Arguments: `bool value`. |
| `onPointerEnter` | `ScriptEvent` | Fires when the pointer enters the toggle area. |
| `onPointerExit` | `ScriptEvent` | Fires when the pointer exits the toggle area. |
| `onPointerClick` | `ScriptEvent<int>` | Fires when the toggle is clicked with the pointer. |
| `onPointerDown` | `ScriptEvent<int>` | Fires when the pointer is pressed down on the toggle. |
| `onPointerUp` | `ScriptEvent<int>` | Fires when the pointer is released on the toggle. |

## Methods

## Events

| Event | Signature | Description |
|-------|-----------|-------------|
| `onValueChanged` | `(value)` | Triggered when the toggle value changes. The `value` parameter is `true` if the toggle is on, `false` otherwise. |
| `onPointerEnter` | `ScriptEvent` | Triggered when the pointer enters the toggle area. |
| `onPointerExit` | `ScriptEvent` | Triggered when the pointer exits the toggle area. |
| `onPointerClick` | `ScriptEvent<int>` | Triggered when the toggle is clicked. |
| `onPointerDown` | `ScriptEvent<int>` | Triggered when the pointer is pressed down on the toggle. |
| `onPointerUp` | `ScriptEvent<int>` | Triggered when the pointer is released on the toggle. |

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

## Enums
