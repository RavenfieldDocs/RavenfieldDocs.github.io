---
title: Slider
---

Represents a Unity UI Slider component accessible from Ravenscript.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `onValueChanged` | [ScriptEvent](./ScriptEvent.md) | Fires when the slider value changes. Arguments: `float value`. |
| `onPointerEnter` | [ScriptEvent](./ScriptEvent.md) | Fires when the pointer enters the slider area. |
| `onPointerExit` | [ScriptEvent](./ScriptEvent.md) | Fires when the pointer exits the slider area. |
| `onPointerClick` | `ScriptEvent<int>` | Fires when the pointer clicks on the slider. |
| `onPointerDown` | `ScriptEvent<int>` | Fires when the pointer is pressed down on the slider. |
| `onPointerUp` | `ScriptEvent<int>` | Fires when the pointer is released on the slider. |

## Methods

## Events

| Event | Signature | Description |
|-------|-----------|-------------|
| `onValueChanged` | `(value)` | Triggered when the slider value changes. The `value` parameter is the new float value of the slider. |
| `onPointerEnter` | [ScriptEvent](./ScriptEvent.md) | Triggered when the pointer enters the slider area. |
| `onPointerExit` | [ScriptEvent](./ScriptEvent.md) | Triggered when the pointer exits the slider area. |
| `onPointerClick` | `ScriptEvent<int>` | Triggered when the pointer clicks on the slider. The callback receives the pointer button index (0=left, 1=right, 2=middle). |
| `onPointerDown` | `ScriptEvent<int>` | Triggered when the pointer is pressed down on the slider. The callback receives the pointer button index (0=left, 1=right, 2=middle). |
| `onPointerUp` | `ScriptEvent<int>` | Triggered when the pointer is released on the slider. The callback receives the pointer button index (0=left, 1=right, 2=middle). |

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

## Enums
