---
title: VehicleInfo
---

Represents metadata about a vehicle type, including its display name and prefab reference.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `name` | `string` | The vehicle's display name. |
| `prefab` | [GameObject](./GameObject.md) | The vehicle's prefab GameObject. |

## Methods

### GetFromPrefab

Gets the `VehicleInfo` associated with a given prefab.

| Parameter | Type | Description |
|-----------|------|-------------|
| `prefab` | [GameObject](./GameObject.md) | The prefab to look up. |

[return: VehicleInfo?]
The `VehicleInfo` for the prefab, or `nil` if the prefab has no vehicle.

### GetHashCode

Returns the hash code for this instance.

[return: int]
The hash code.

### ToString

Returns a string representation of this vehicle info.

[return: string]
A string representation.

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

## Enums
