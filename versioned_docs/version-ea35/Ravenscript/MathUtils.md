---
title: MathUtils
---

This class provides some math functionality that is useful for 3d maths.

## Properties

## Methods

### LineVsPointClosest

Given a line L and point P, get the point on L that is closest to P.

| Parameter | Type | Description |
|-----------|------|-------------|
| `lineOrigin` | `Vector3` | The origin of the line. |
| `lineDirection` | `Vector3` | The direction of the line. |
| `point` | `Vector3` | The point to find the closest point to. |

[return: Vector3]
The closest point on the line to the given point.

### LineVsPointClosestT

Given a line L and point P, get the point on L that is closest to P. Returns the point as a value T, where point = origin(L) + direction(L) * T.

| Parameter | Type | Description |
|-----------|------|-------------|
| `lineOrigin` | `Vector3` | The origin of the line. |
| `lineDirection` | `Vector3` | The direction of the line. |
| `point` | `Vector3` | The point to find the closest point to. |

[return: float]
The parameter T representing the closest point on the line.

### LineSegmentVsPointClosest

Given a line segment S and point P, get the point on S that is closest to P.

| Parameter | Type | Description |
|-----------|------|-------------|
| `segmentStart` | `Vector3` | The start of the line segment. |
| `segmentEnd` | `Vector3` | The end of the line segment. |
| `point` | `Vector3` | The point to find the closest point to. |

[return: Vector3]
The closest point on the line segment to the given point.

### LineSegmentVsPointClosestT

Given a line segment S and point P, get the point on S that is closest to P. Returns the point as a value T, where point = Lerp(start(S), end(S), T).

| Parameter | Type | Description |
|-----------|------|-------------|
| `segmentStart` | `Vector3` | The start of the line segment. |
| `segmentEnd` | `Vector3` | The end of the line segment. |
| `point` | `Vector3` | The point to find the closest point to. |

[return: float]
The parameter T representing the closest point on the line segment.

### LookRotationConstrainUp

Returns the look rotation like `Quaternion.LookRotation()`, but with the up vector being fully constrained instead of the forward vector.

| Parameter | Type | Description |
|-----------|------|-------------|
| `forward` | `Vector3` | The forward direction. |
| `up` | `Vector3` | The up direction to constrain. |

[return: Quaternion]
The calculated look rotation with constrained up vector.

### Damp

A frame rate independent alternative to damping using `Mathf.Lerp()`.

| Parameter | Type | Description |
|-----------|------|-------------|
| `current` | `float` | The current value. |
| `target` | `float` | The target value. |
| `smoothing` | `float` | The smoothing factor. |
| `deltaTime` | `float` | The time delta for frame rate independence. |

[return: float]
The damped value.

### Damp

A frame rate independent alternative to damping using `Vector3.Lerp()`.

| Parameter | Type | Description |
|-----------|------|-------------|
| `current` | `Vector3` | The current value. |
| `target` | `Vector3` | The target value. |
| `smoothing` | `float` | The smoothing factor. |
| `deltaTime` | `float` | The time delta for frame rate independence. |

[return: Vector3]
The damped value.

### DampLinear

A frame rate independent alternative to damping using `Quaternion.Lerp()`.

| Parameter | Type | Description |
|-----------|------|-------------|
| `current` | `Quaternion` | The current rotation. |
| `target` | `Quaternion` | The target rotation. |
| `smoothing` | `float` | The smoothing factor. |
| `deltaTime` | `float` | The time delta for frame rate independence. |

[return: Quaternion]
The damped rotation.

### DampSpherical

A frame rate independent alternative to damping using `Quaternion.Slerp()`.

| Parameter | Type | Description |
|-----------|------|-------------|
| `current` | `Quaternion` | The current rotation. |
| `target` | `Quaternion` | The target rotation. |
| `smoothing` | `float` | The smoothing factor. |
| `deltaTime` | `float` | The time delta for frame rate independence. |

[return: Quaternion]
The damped rotation.

## Events

## Static Fields

## Static Methods

## Enums
