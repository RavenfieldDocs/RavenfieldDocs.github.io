---
title: Engine
---

Represents a vehicle engine with audio and throttle control.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `controlAudio` | `bool` | Whether the engine controls its own audio. |
| `enabled` | `bool` | Whether the engine is enabled. |
| `ignitionClip` | `[AudioClip](./AudioClip.md)` or `nil` | The audio clip played on ignition. |
| `pitchGainSpeed` | `float` | The speed at which pitch interpolates to the target. |
| `power` | `float` | The power output of the engine. |
| `powerGainSpeed` | `float` | The speed at which power interpolates to the target. |
| `shiftForwardClip` | `[AudioClip](./AudioClip.md)` or `nil` | The audio clip played when shifting forward. |
| `shiftReverseClip` | `[AudioClip](./AudioClip.md)` or `nil` | The audio clip played when shifting reverse. |
| `targetPitch` | `float` | The target pitch for the engine audio. |
| `targetThrottle` | `float` | The target throttle value. |
| `throttleGainSpeed` | `float` | The speed at which throttle interpolates to the target. |

## Methods

### PlayIgnitionSound

Plays the ignition sound clip.

| Parameter | Type | Description |
|-----------|------|-------------|

### PlayShiftForwardSound

Plays the shift forward sound clip.

| Parameter | Type | Description |
|-----------|------|-------------|

### PlayShiftReverseSound

Plays the shift reverse sound clip.

| Parameter | Type | Description |
|-----------|------|-------------|

### Reset

Resets the engine to its default state.

| Parameter | Type | Description |
|-----------|------|-------------|

### ToString

Returns a string representation of the engine.

| Parameter | Type | Description |
|-----------|------|-------------|

[return: `string`]
The string representation.

## Events

## Static Fields

## Static Methods

### Call

Creates a new engine instance. Called via `Engine()`.

| Parameter | Type | Description |
|-----------|------|-------------|

[return: `Engine`]
A new engine instance.

## Enums
