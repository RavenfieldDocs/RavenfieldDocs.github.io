---
title: BezierPath
---

Represents a bezier spline path defined by a sequence of segments. Supports evaluation of position and tangent direction at any point along the curve.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `relativeToContainer` | `bool` | Whether the path is evaluated relative to its container transform. |
| `segments` | `BezierSegment[]` | The array of bezier segments that define the path. |

## Methods

### Evaluate

Evaluates the position on the path at the given parameter `t`. The parameter `t` is a floating point value where the integer part selects the segment index and the fractional part interpolates within that segment. For example, `t = 1.5` evaluates halfway along the second segment.

| Parameter | Type | Description |
|-----------|------|-------------|
| `t` | `float` | The parameter along the path to evaluate. |

[return: Vector3]
The world position at the specified parameter.

### EvaluateDerivative

Evaluates the tangent (derivative) of the path at the given parameter `t`.

| Parameter | Type | Description |
|-----------|------|-------------|
| `t` | `float` | The parameter along the path to evaluate. |

[return: Vector3]
The tangent vector at the specified parameter.

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

### Create

Creates a new bezier path from an array of segments.

| Parameter | Type | Description |
|-----------|------|-------------|
| `segments` | `BezierSegment[]` | The array of bezier segments that define the path. |

[return: BezierPath]
A new bezier path constructed from the given segments.

### Evaluate

Statically evaluates the position on a bezier curve between two segments at parameter `t`.

| Parameter | Type | Description |
|-----------|------|-------------|
| `from` | `BezierSegment` | The starting segment of the curve. |
| `to` | `BezierSegment` | The ending segment of the curve. |
| `t` | `float` | The interpolation parameter from 0 to 1. |

[return: Vector3]
The interpolated position between the two segments.

### EvaluateDerivative

Statically evaluates the tangent (derivative) of a bezier curve between two segments at parameter `t`.

| Parameter | Type | Description |
|-----------|------|-------------|
| `from` | `BezierSegment` | The starting segment of the curve. |
| `to` | `BezierSegment` | The ending segment of the curve. |
| `t` | `float` | The interpolation parameter from 0 to 1. |

[return: Vector3]
The tangent vector between the two segments at the specified parameter.

## Enums
