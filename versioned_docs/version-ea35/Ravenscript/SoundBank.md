---
title: SoundBank
---

A collection of audio clips that can be played back through an audio source, with support for random or indexed selection.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `audioSource` | [AudioSource](./AudioSource.md) or `nil` | The audio source used to play sounds from this bank. |
| `clips` | [AudioClip](./AudioClip.md)[] | The array of audio clips in this sound bank. |
| `gameObject` | [GameObject](./GameObject.md) | The game object this sound bank is attached to. |
| `transform` | [Transform](./Transform.md) | The transform of the game object this sound bank is attached to. |

## Methods

### IsPlaying

Returns whether this sound bank is currently playing a sound.

[return: bool]

### PlayRandom

Plays a random clip from the sound bank's clip array.

### PlaySoundBank

Plays a specific clip from the sound bank by index.

| Parameter | Type | Description |
|-----------|------|-------------|
| `index` | `int` | The index of the clip to play. |

### SetVolume

Sets the volume of the sound bank's audio source.

| Parameter | Type | Description |
|-----------|------|-------------|
| `volume` | `float` | The volume level to set. |

### Start

Starts the sound bank, preparing it for playback.

### ToString

Returns a string representation of this sound bank.

[return: string]

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
