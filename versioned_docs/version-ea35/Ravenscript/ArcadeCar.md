---
title: ArcadeCar
---

Represents a ground vehicle with wheel-based physics. Extends [Vehicle](./Vehicle.md) with acceleration, steering, drifting, and gear mechanics. Exposed to Lua as `Car`.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `acceleration` | `float` | Forward acceleration force. |
| `reverseAcceleration` | `float` | Reverse acceleration force. |
| `accelerationTipAmount` | `float` | Vertical offset for applying acceleration force. |
| `frictionTipAmount` | `float` | Vertical offset for applying friction force. |
| `topSpeed` | `float` | Maximum speed. |
| `speedTurnTorque` | `float` | Turning torque multiplier based on speed. |
| `baseTurnTorque` | `float` | Base turning torque. |
| `tankTurning` | `bool` | If `true`, the car turns like a tank (applies base turn torque even at zero speed). |
| `slideDrag` | `float` | Lateral drag applied during sliding. |
| `brakeDrag` | `float` | Drag applied when braking. |
| `driftByAcceleration` | `bool` | If `true`, drifting can be triggered by acceleration. |
| `brakeAccelerationTriggerSpeed` | `float` | Speed threshold for brake-acceleration drift trigger. |
| `driftByBrake` | `bool` | If `true`, drifting can be triggered by braking. |
| `brakeDriftMinSpeed` | `float` | Minimum speed required for brake-triggered drift. |
| `driftingSlip` | `float` | Amount of slip applied during a drift. |
| `driftDuration` | `float` | Duration of a drift in seconds. |
| `isAmphibious` | `bool` | If `true`, the car can float and move in water. |
| `extraStability` | `float` | Additional downward center of mass offset for ground stability. |
| `groundDrag` | `float` | Drag applied when grounded and stable. |
| `groundAngularDrag` | `float` | Angular drag applied when grounded and stable. |
| `groundSteeringDrag` | `float` | Angular drag applied to steering on the ground. |
| `airDrag` | `float` | Drag applied when airborne. |
| `airAngularDrag` | `float` | Angular drag applied when airborne. |
| `downforcePerSpeed` | `float` | Downward force applied proportional to forward speed. |
| `inReverseGear` | `bool` | Whether the car is currently in reverse gear. |
| `brakeSounds` | [SoundBank](./SoundBank.md) | Sound bank for brake sounds. |
| `suspensionShiftSounds` | [SoundBank](./SoundBank.md) | Sound bank for suspension shift sounds. |

Inherits all properties from [Vehicle](./Vehicle.md).

## Methods

### IsChangingGears

Returns whether the car is currently in the process of changing gears.

[return: bool]

Inherits all methods from [Vehicle](./Vehicle.md).

## Events

## Static Fields

## Static Methods

## Enums

### ReverseTurnType

Controls how turning torque is applied when driving in reverse.

| Value | Description |
|-------|-------------|
| `ReverseSpeed` | Turning torque is inverted when in reverse gear. |
| `ReverseThrottle` | Turning torque is multiplied by the sign of throttle input. |
| `Never` | Turning torque is never inverted in reverse. |
