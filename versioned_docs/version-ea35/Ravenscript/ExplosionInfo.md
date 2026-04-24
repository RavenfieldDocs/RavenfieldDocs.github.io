---
title: ExplosionInfo
---

Contains information about an explosion event, including the explosion point, source, and configuration.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `configuration` | [ExplosionConfiguration](./ExplosionConfiguration.md) | The explosion configuration, or `nil` if not set. |
| `damageRating` | `Vehicle.ArmorRating` | The armor damage rating used for vehicle damage calculations. |
| `point` | `Vector3` | The world position of the explosion. |
| `sourceActor` | [Actor](./Actor.md) or `nil` | The actor that caused the explosion, or `nil` if there is no source actor. |
| `sourceWeapon` | [Weapon](./Weapon.md) or `nil` | The weapon that caused the explosion, or `nil` if there is no source weapon. |
| `sourceWeaponEntry` | [WeaponEntry](./WeaponEntry.md) or `nil` | The weapon entry from the source weapon. Read-only. |

## Methods

## Events

## Static Fields

## Static Methods

### Create

Creates a new `ExplosionInfo` with the specified parameters.

| Parameter | Type | Description |
|-----------|------|-------------|
| `point` | `Vector3` | The world position of the explosion. |
| `sourceActor` | [Actor](./Actor.md) or `nil` | The actor that caused the explosion. |
| `sourceWeapon` | [Weapon](./Weapon.md) or `nil` | The weapon that caused the explosion. |
| `damageRating` | `Vehicle.ArmorRating` | The armor damage rating. |
| `configuration` | [ExplosionConfiguration](./ExplosionConfiguration.md) or `nil` | The explosion configuration. |

[return: [ExplosionInfo](./ExplosionInfo.md)]

### Call

Creates a new default `ExplosionInfo` instance. Called via `()`.

[return: [ExplosionInfo](./ExplosionInfo.md)]

## Enums
