---
title: EffectUi
---

Static class for controlling screen fade effects and visual transitions.

## Properties

| Property | Type | Description |
|----------|------|-------------|

## Methods

## Events

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

### ChangeFadeColor

Changes the color of all fade graphics over time.

| Parameter | Type | Description |
|-----------|------|-------------|
| `color` | [Color](./Color.md) | The target color to fade to. |
| `changeTime` | `float` | The time in seconds over which to change the color. |

### Clear

Clears all active fade effects instantly.

### FadeIn

Fades the screen in from the specified color over the given duration.

| Parameter | Type | Description |
|-----------|------|-------------|
| `type` | [FadeType](./EffectUi.md#fadetype) | The type of fade effect to use. |
| `duration` | `float` | The duration of the fade in seconds. |
| `color` | [Color](./Color.md) | The color to fade from. |

### FadeOut

Fades the screen out to the specified color over the given duration.

| Parameter | Type | Description |
|-----------|------|-------------|
| `type` | [FadeType](./EffectUi.md#fadetype) | The type of fade effect to use. |
| `duration` | `float` | The duration of the fade in seconds. |
| `color` | [Color](./Color.md) | The color to fade to. |

## Enums

### FadeType

| Value | Description |
|-------|-------------|
| `FullScreen` | Fades the entire screen. |
| `Eye` | Fades using animated eyelids (like blinking). |
| `EyeAndFullScreen` | Combines both eyelid and full screen fade effects. |
