---
title: MeanFilter
---

A filter that computes the mean (average) of the last N input values, useful for smoothing noisy data.

## Properties

## Methods

### Tick

Feeds a new input value into the filter and returns the current smoothed value.

| Parameter | Type | Description |
|-----------|------|-------------|
| `input` | `float` | The new input value to add to the filter. |

[return: float]
The current mean value after adding the new input.

### Value

Returns the current mean value without adding a new input.

[return: float]
The current mean of the last N values.

## Events

## Static Fields

## Static Methods

## Enums
