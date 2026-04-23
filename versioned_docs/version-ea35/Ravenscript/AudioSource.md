---
title: AudioSource
---

Wrapper for the Unity AudioSource component, providing audio playback and analysis functionality.

## Properties

| Property | Type | Description |
|----------|------|-------------|

## Methods

### SetOutputAudioMixer

Sets the output audio mix of this audio source.

| Parameter | Type | Description |
|-----------|------|-------------|
| `mixer` | `AudioMixer` | The audio mixer to route output to. |

### GetOutputData

Gets a float[64] array of the next audio samples.

| Parameter | Type | Description |
|-----------|------|-------------|
| `channel` | `int` | The channel to retrieve samples from. |

[return: float[]]

### GetSpectrumData

Gets a float[64] array of current spectrum data using FFT.

| Parameter | Type | Description |
|-----------|------|-------------|
| `channel` | `int` | The channel to retrieve spectrum data from. |

[return: float[]]

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

| Method | Signature | Description |
|--------|-----------|-------------|

## Enums

| Enum | Description |
|------|-------------|
