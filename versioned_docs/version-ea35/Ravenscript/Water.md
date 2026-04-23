---
title: Water
---

Static class for querying and manipulating water in the scene.

## Properties

| Property | Type | Description |
|----------|------|-------------|

## Methods

| Method | Signature | Description |
|--------|-----------|-------------|
| [`IsInWater`](#isinwater) | `(position)` | Checks if a position is in water. |
| [`GetWaterDepth`](#getwaterdepth) | `(position)` | Gets the water depth at a position. |
| [`GetWaterLevel`](#getwaterlevel) | `()` | Gets the current water level height. |
| [`SetWaterLevel`](#setwaterlevel) | `(height)` | Sets the water level height. |
| [`Raycast`](#raycast) | `(ray, range)` | Casts a ray through the scene until it collides with the WaterLevel or a WaterVolume. |

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

### IsInWater

Checks if a position is in water.

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The position to check. |

[return: bool]

### GetWaterDepth

Gets the water depth at a position.

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The position to check. |

[return: float]

Returns the depth, or `-1` if not in water.

### GetWaterLevel

Gets the current water level height.

[return: float]

### SetWaterLevel

Sets the water level height.

| Parameter | Type | Description |
|-----------|------|-------------|
| `height` | `float` | The new water level height. |

### Raycast

Casts a ray through the scene until it collides with the WaterLevel or a WaterVolume.

| Parameter | Type | Description |
|-----------|------|-------------|
| `ray` | `Ray` | Test for collisions along this ray. |
| `range` | `float` | Look no further than this [meters]. |

[return: RaycastHit?]

A RaycastHit if a collision occurs along the ray; otherwise nil.

## Enums

| Value | Description |
|-------|-------------|
