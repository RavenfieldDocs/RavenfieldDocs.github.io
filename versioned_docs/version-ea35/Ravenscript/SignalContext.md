---
title: SignalContext
---

Context data for trigger signal events, containing references to the actor, squad, weapon, and vehicle involved in the signal.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `actor` | [Actor](./Actor.md) or `nil` | The actor associated with this signal context. |
| `squad` | `SquadProxy` or `nil` | The squad associated with this signal context. |
| `weapon` | [Weapon](./Weapon.md) or `nil` | The weapon associated with this signal context. |
| `vehicle` | [Vehicle](./Vehicle.md) or `nil` | The vehicle associated with this signal context. |

## Methods

## Events

## Static Fields

## Static Methods

### Call

Creates a new empty signal context.

[return: [SignalContext](./SignalContext.md)]
A new signal context with all fields set to `nil`.

## Enums
