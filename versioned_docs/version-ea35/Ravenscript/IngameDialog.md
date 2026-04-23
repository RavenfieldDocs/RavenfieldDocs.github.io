---
title: IngameDialog
---

Use this class to play dialogs or text messages while ingame.

## Properties

| Property | Type | Description |
|----------|------|-------------|

## Methods

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

### PrintActorText

Print a dialog message using the specified actor pose.

| Parameter | Type | Description |
|-----------|------|-------------|
| `actorPose` | `string` | The actor pose to use for the dialog portrait. |
| `text` | `string` | The text to display in the dialog. |

### PrintActorText

Print a dialog message using the specified actor pose and portrait noise.

| Parameter | Type | Description |
|-----------|------|-------------|
| `actorPose` | `string` | The actor pose to use for the dialog portrait. |
| `text` | `string` | The text to display in the dialog. |
| `noiseAmount` | `float` | The amount of noise/static effect on the portrait. |

### PrintActorText

Print a dialog message using the specified actor pose, overriding the actor name.

| Parameter | Type | Description |
|-----------|------|-------------|
| `actorPose` | `string` | The actor pose to use for the dialog portrait. |
| `text` | `string` | The text to display in the dialog. |
| `overrideName` | `string` | The name to display instead of the actor's default name. |

### PrintActorText

Print a dialog message using the specified actor pose and portrait noise, overriding the actor name.

| Parameter | Type | Description |
|-----------|------|-------------|
| `actorPose` | `string` | The actor pose to use for the dialog portrait. |
| `text` | `string` | The text to display in the dialog. |
| `overrideName` | `string` | The name to display instead of the actor's default name. |
| `noiseAmount` | `float` | The amount of noise/static effect on the portrait. |

### Hide

Hides the dialog box using a transition effect.

### HideAfter

Hides the dialog box using a transition effect after some time.

| Parameter | Type | Description |
|-----------|------|-------------|
| `duration` | `float` | The time in seconds before the dialog hides. |

### HideInstant

Instantly hides the dialog box.

## Enums

| Value | Description |
|-------|-------------|
