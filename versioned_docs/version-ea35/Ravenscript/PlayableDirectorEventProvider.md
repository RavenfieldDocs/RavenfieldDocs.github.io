---
title: PlayableDirectorEventProvider
---

A MonoBehaviour that exposes Unity PlayableDirector events to scripting.

## Properties

| Property | Type | Description |
|----------|------|-------------|

## Methods

## Events

| Event | Signature | Description |
|-------|-----------|-------------|
| `paused` | `ScriptEvent<PlayableDirector>` | Fired when the director is paused. |
| `stopped` | `ScriptEvent<PlayableDirector>` | Fired when the director stops playing. |
| `played` | `ScriptEvent<PlayableDirector>` | Fired when the director starts playing. |

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

### Get

Gets or creates a `PlayableDirectorEventProvider` for a given `PlayableDirector`.

| Parameter | Type | Description |
|-----------|------|-------------|
| `pd` | `PlayableDirector` | The PlayableDirector to get the event provider for. |

[return: PlayableDirectorEventProvider]
The event provider for the specified director.

## Enums
