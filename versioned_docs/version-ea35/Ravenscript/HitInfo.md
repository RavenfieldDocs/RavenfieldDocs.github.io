---
title: HitInfo
---

Represents hit information containing references to an actor, vehicle, or destructible that was hit.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `actor` | `[Actor](./Actor.md)` | The actor that was hit, or `nil`. |
| `destructible` | `[Destructible](./Destructible.md)` | The destructible that was hit, or `nil`. |
| `vehicle` | `[Vehicle](./Vehicle.md)` | The vehicle that was hit, or `nil`. |

## Methods

### ToString

Returns a string representation of this hit information.

[return: string]
A string describing the hit info.

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

### Call

Creates a new `HitInfo` instance. Can be called with an `[Actor](./Actor.md)`, `[Vehicle](./Vehicle.md)`, `[Destructible](./Destructible.md)`, or no arguments.

| Parameter | Type | Description |
|-----------|------|-------------|
| `actor` | `[Actor](./Actor.md)` | The actor that was hit. |

[return: HitInfo]
A new `HitInfo` wrapping the given actor.

| Parameter | Type | Description |
|-----------|------|-------------|
| `vehicle` | `[Vehicle](./Vehicle.md)` | The vehicle that was hit. |

[return: HitInfo]
A new `HitInfo` wrapping the given vehicle.

| Parameter | Type | Description |
|-----------|------|-------------|
| `destructible` | `[Destructible](./Destructible.md)` | The destructible that was hit. |

[return: HitInfo]
A new `HitInfo` wrapping the given destructible.

| Parameter | Type | Description |
|-----------|------|-------------|

[return: HitInfo]
A new empty `HitInfo`.

## Enums
