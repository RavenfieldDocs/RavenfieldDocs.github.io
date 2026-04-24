---
title: CurrentEvent
---

Provides access to the currently handling event in a Ravenscript callback, allowing consumption and listener data inspection.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `isConsumed` | `bool` | Returns true if the current event has been consumed. |
| `listenerData` | `DynValue` | Returns the listener data assigned to the current event listener. |

## Methods

### Consume

Consumes the current event. Consuming an event stops any built in game behaviour from reacting to the event. If a previous Ravenscript callback consumed the event, the ``CurrentEvent.isConsumed`` flag will be set to true.

| Parameter | Type | Description |
|-----------|------|-------------|

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

## Enums
