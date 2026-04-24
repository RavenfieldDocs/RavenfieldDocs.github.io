---
title: ScriptEvent
---

Represents a script-defined event that Lua scripts can listen to and invoke. Used as the return type for ``ScriptedBehaviour.defineEvent``.

## Properties

| Property | Type | Description |
|----------|------|-------------|

## Methods

### AddListener

Adds ``script.methodName`` as an event handler. This handler is called every time the event occurs.

| Parameter | Type | Description |
|-----------|------|-------------|
| `script` | `ScriptedBehaviour` | The script containing the callback method. |
| `methodName` | `string` | The name of the method to call when the event fires. |

### AddListener

Adds ``script.methodName`` as an event handler with a data argument. This handler is called every time the event occurs. In the event listener, access the data value with ``CurrentEvent.listenerData``.

| Parameter | Type | Description |
|-----------|------|-------------|
| `script` | `ScriptedBehaviour` | The script containing the callback method. |
| `methodName` | `string` | The name of the method to call when the event fires. |
| `listenerData` | `DynValue` | Custom data passed to the listener, accessible via ``CurrentEvent.listenerData``. |

### RemoveListener

Removes ``script.methodName`` from the list of event handlers.

| Parameter | Type | Description |
|-----------|------|-------------|
| `script` | `ScriptedBehaviour` | The script containing the callback method. |
| `methodName` | `string` | The name of the method to remove. |

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

## Enums
