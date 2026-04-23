---
title: Time
---

Provides access to time-related properties in the game.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `timeScale` | `float` | Sets the time scale of the game. Also tweaks the Time.fixedDeltaTime value and audio pitch to match the assigned time scale. |
| `time` | `float` | The time since the start of the game, affected by time scale. |
| `unscaledTime` | `float` | The time since the start of the game, not affected by time scale. |
| `timeSinceLevelLoad` | `float` | The time since the current level was loaded, affected by time scale. |
| `unscaledDeltaTime` | `float` | The time in seconds it took to complete the last frame, not affected by time scale. |
| `deltaTime` | `float` | The time in seconds it took to complete the last frame, affected by time scale. |
| `fixedDeltaTime` | `float` | The interval in seconds at which physics and other fixed timestep updates are performed. |
| `systemTimeYear` | `int` | The current system year. |
| `systemTimeMonth` | `int` | The current system month (1-12). |
| `systemTimeDay` | `int` | The current system day of the month (1-31). |
| `systemTimeHour` | `int` | The current system hour (0-23). |
| `systemTimeMinute` | `int` | The current system minute (0-59). |
| `systemTimeSecond` | `int` | The current system second (0-59). |
| `systemTimeMillisecond` | `int` | The current system millisecond (0-999). |

## Methods

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

## Enums
