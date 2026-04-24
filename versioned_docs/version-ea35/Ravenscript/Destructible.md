---
title: Destructible
---

Represents an object that can take damage and be destroyed.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `health` | `float` | The current health of the destructible. |
| `isDead` | `bool` | Whether the destructible has been destroyed. |

## Methods

## Events

| Event | Signature | Description |
|-------|-----------|-------------|
| `onTakeDamage` | `ScriptEvent<DamageInfo>` | Invoked when the destructible takes damage. Consuming this event stops the destructible from taking damage. |
| `onDeath` | `ScriptEvent<DamageInfo>` | Invoked when the destructible dies. |

## Static Fields

## Static Methods

## Enums
