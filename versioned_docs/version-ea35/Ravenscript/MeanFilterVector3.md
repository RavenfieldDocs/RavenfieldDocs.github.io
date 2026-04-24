---
title: MeanFilterVector3
---

A moving average (mean) filter for `Vector3` values. It smooths out noisy input by averaging over a fixed number of recent samples (taps).

## Properties

## Methods

### Tick

Feeds a new input value into the filter and returns the filtered output.

| Parameter | Type | Description |
|-----------|------|-------------|
| `input` | `Vector3` | The new input value to feed into the filter. |

[return: Vector3]
The filtered (smoothed) `Vector3` value.

### Value

Returns the current filtered value without feeding a new input.

[return: Vector3]
The current filtered `Vector3` value.

## Events

## Static Fields

## Static Methods

### MeanFilterVector3

Creates a new mean filter with the specified number of taps.

| Parameter | Type | Description |
|-----------|------|-------------|
| `taps` | `int` | The number of samples to average over. |

[return: [MeanFilterVector3](./MeanFilterVector3.md)]
A new `MeanFilterVector3` instance.

## Enums
