---
title: LoadoutSet
---

Represents a set of weapons assigned to different equipment slots, including primary, secondary, and three gear slots.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `gear1` | [WeaponEntry](./WeaponEntry.md) or `nil` | The weapon assigned to gear slot 1. |
| `gear2` | [WeaponEntry](./WeaponEntry.md) or `nil` | The weapon assigned to gear slot 2. |
| `gear3` | [WeaponEntry](./WeaponEntry.md) or `nil` | The weapon assigned to gear slot 3. |
| `primary` | [WeaponEntry](./WeaponEntry.md) or `nil` | The primary weapon. |
| `secondary` | [WeaponEntry](./WeaponEntry.md) or `nil` | The secondary weapon. |

## Methods

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

### Call

Creates a new empty loadout set. This method is exposed as the `__call` metamethod, allowing it to be called like a constructor.

[return: [LoadoutSet](./LoadoutSet.md)]

A new empty loadout set.

## Enums
