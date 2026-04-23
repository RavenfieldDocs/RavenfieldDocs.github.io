---
title: Debug
---

Contains helper functions that help you debug your code. Please note that for performance reasons, drawing rays and lines is only supported when launching the game in test mode.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `isTestMode` | `bool` | Returns true if the game has been launched from the Unity Editor via the `-testcontentmod` parameter. |

## Methods

### DrawLine

Draws a line in the scene. Only works in test mode.

| Parameter | Type | Description |
|-----------|------|-------------|
| `from` | `Vector3` | The start point of the line. |
| `to` | `Vector3` | The end point of the line. |
| `color` | `Color` | The color of the line. |

### DrawLine

| Parameter | Type | Description |
|-----------|------|-------------|
| `from` | `Vector3` | The start point of the line. |
| `to` | `Vector3` | The end point of the line. |
| `color` | `Color` | The color of the line. |
| `duration` | `float` | How long the line should be visible, in seconds. |

### DrawLine

| Parameter | Type | Description |
|-----------|------|-------------|
| `from` | `Vector3` | The start point of the line. |
| `to` | `Vector3` | The end point of the line. |
| `color` | `Color` | The color of the line. |
| `duration` | `float` | How long the line should be visible, in seconds. |
| `localToWorldMatrix` | `Matrix4x4` | A transformation matrix to apply to the line. |

### DrawPath

Draws a path (connected line segments) in the scene. Only works in test mode.

| Parameter | Type | Description |
|-----------|------|-------------|
| `vertices` | `Vector3[]` | An array of points defining the path. |
| `color` | `Color` | The color of the path. |

### DrawPath

| Parameter | Type | Description |
|-----------|------|-------------|
| `vertices` | `Vector3[]` | An array of points defining the path. |
| `color` | `Color` | The color of the path. |
| `duration` | `float` | How long the path should be visible, in seconds. |

### DrawPath

| Parameter | Type | Description |
|-----------|------|-------------|
| `vertices` | `Vector3[]` | An array of points defining the path. |
| `color` | `Color` | The color of the path. |
| `duration` | `float` | How long the path should be visible, in seconds. |
| `localToWorldMatrix` | `Matrix4x4` | A transformation matrix to apply to the path. |

### DrawRay

Draws a ray (a line with a start point and direction) in the scene. Only works in test mode.

| Parameter | Type | Description |
|-----------|------|-------------|
| `from` | `Vector3` | The start point of the ray. |
| `direction` | `Vector3` | The direction of the ray. |
| `color` | `Color` | The color of the ray. |

### DrawRay

| Parameter | Type | Description |
|-----------|------|-------------|
| `from` | `Vector3` | The start point of the ray. |
| `direction` | `Vector3` | The direction of the ray. |
| `color` | `Color` | The color of the ray. |
| `duration` | `float` | How long the ray should be visible, in seconds. |

### DrawRay

| Parameter | Type | Description |
|-----------|------|-------------|
| `from` | `Vector3` | The start point of the ray. |
| `direction` | `Vector3` | The direction of the ray. |
| `color` | `Color` | The color of the ray. |
| `duration` | `float` | How long the ray should be visible, in seconds. |
| `localToWorldMatrix` | `Matrix4x4` | A transformation matrix to apply to the ray. |

## Events

## Static Fields

## Static Methods

## Enums
