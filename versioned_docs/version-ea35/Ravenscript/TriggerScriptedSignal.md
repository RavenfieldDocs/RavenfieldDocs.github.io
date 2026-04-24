---
title: TriggerScriptedSignal
---

Represents a scripted signal trigger that can send named signals to trigger components. Used to programmatically trigger events on game objects.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `gameObject` | [GameObject](./GameObject.md) | The game object this trigger is attached to. |
| `transform` | [Transform](./Transform.md) | The transform of this trigger. |

## Methods

### Send

Sends a named signal through this trigger.

| Parameter | Type | Description |
|-----------|------|-------------|
| `entryName` | `string` | The name of the signal entry to trigger. |

### Send

Sends a named signal through this trigger with additional context.

| Parameter | Type | Description |
|-----------|------|-------------|
| `entryName` | `string` | The name of the signal entry to trigger. |
| `context` | [SignalContext](./SignalContext.md) | Additional context data for the signal. |

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

### SendGlobalNamedSignal

Sends a global named signal that can be received by any trigger listening for that signal name.

| Parameter | Type | Description |
|-----------|------|-------------|
| `name` | `string` | The name of the global signal to send. |

[return: bool]
`true` if the signal was sent successfully.

### SendGlobalNamedSignal

Sends a global named signal with additional context.

| Parameter | Type | Description |
|-----------|------|-------------|
| `name` | `string` | The name of the global signal to send. |
| `context` | [SignalContext](./SignalContext.md) | Additional context data for the signal. |

[return: bool]
`true` if the signal was sent successfully.

## Enums

| Enum | Description |
|------|-------------|
