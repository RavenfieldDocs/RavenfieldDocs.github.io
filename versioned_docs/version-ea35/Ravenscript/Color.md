---
title: Color
---

Represents an RGBA color with floating point components from 0 to 1.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `r` | `float` | The red component of the color. |
| `g` | `float` | The green component of the color. |
| `b` | `float` | The blue component of the color. |
| `a` | `float` | The alpha (transparency) component of the color. |

## Methods

### Color

Creates a new color with the specified RGBA components.

| Parameter | Type | Description |
|-----------|------|-------------|
| `r` | `float` | The red component (0 to 1). |
| `g` | `float` | The green component (0 to 1). |
| `b` | `float` | The blue component (0 to 1). |
| `a` | `float` | The alpha component (0 to 1). |

[return: Color]

### Color

Creates a new color with the specified RGB components and an alpha of 1.

| Parameter | Type | Description |
|-----------|------|-------------|
| `r` | `float` | The red component (0 to 1). |
| `g` | `float` | The green component (0 to 1). |
| `b` | `float` | The blue component (0 to 1). |

[return: Color]

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|
| `black` | `Color` | Solid black (RGBA 0, 0, 0, 1). |
| `blue` | `Color` | Solid blue (RGBA 0, 0, 1, 1). |
| `clear` | `Color` | Transparent black (RGBA 0, 0, 0, 0). |
| `cyan` | `Color` | Solid cyan (RGBA 0, 1, 1, 1). |
| `gray` | `Color` | Solid gray (RGBA 0.5, 0.5, 0.5, 1). |
| `green` | `Color` | Solid green (RGBA 0, 1, 0, 1). |
| `grey` | `Color` | Solid grey (RGBA 0.5, 0.5, 0.5, 1). |
| `magenta` | `Color` | Solid magenta (RGBA 1, 0, 1, 1). |
| `red` | `Color` | Solid red (RGBA 1, 0, 0, 1). |
| `white` | `Color` | Solid white (RGBA 1, 1, 1, 1). |
| `yellow` | `Color` | Solid yellow (RGBA 1, 1, 0, 1). |

## Static Methods

### ToHSV

Converts an RGB color to HSV representation.

| Parameter | Type | Description |
|-----------|------|-------------|
| `color` | `Color` | The color to convert. |

[return: Vector3]
A Vector3 where x is hue (0-1), y is saturation (0-1), and z is value (0-1).

### HSVToRGB

Converts an HSV color to RGB representation.

| Parameter | Type | Description |
|-----------|------|-------------|
| `v` | `Vector3` | A Vector3 where x is hue (0-1), y is saturation (0-1), and z is value (0-1). |

[return: Color]
The converted RGB color.

## Enums
