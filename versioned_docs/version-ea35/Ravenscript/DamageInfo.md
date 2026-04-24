---
title: DamageInfo
---

Contains information about a damage event, including the source, type, amount, and impact details.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `balanceDamage` | `float` | The amount of damage applied to the target's balance. |
| `direction` | `Vector3` | The direction the damage came from. |
| `healthDamage` | `float` | The amount of damage applied to the target's health. |
| `impactForce` | `Vector3` | The force of the impact. |
| `isCriticalHit` | `bool` | Whether this damage event is a critical hit. |
| `isPiercing` | `bool` | Whether this damage pierces through the target. |
| `isSplashDamage` | `bool` | Whether this damage is from a splash (area of effect) source. |
| `point` | `Vector3` | The world position where the damage occurred. |
| `sourceActor` | [Actor](./Actor.md) or `nil` | The actor that caused the damage, or `nil` if there is no source actor. |
| `type` | `DamageInfo.DamageSourceType` | The type of damage source. |
| `isPlayerSource` | `bool` | Whether the source of the damage is a player (not AI controlled). Read-only. |
| `isScripted` | `bool` | Whether the damage type is `Scripted`. Read-only. |
| `sourceWeapon` | [Weapon](./Weapon.md) or `nil` | The weapon that caused the damage, or `nil` if there is no source weapon. |
| `sourceWeaponEntry` | [WeaponEntry](./WeaponEntry.md) or `nil` | The weapon entry from the source weapon. Read-only. |

## Methods

## Events

## Static Fields

| Field | Type | Description |
|-------|------|-------------|
| `Default` | [DamageInfo](./DamageInfo.md) | A default damage info with type `Unknown` and no source. Read-only. |
| `Explosion` | [DamageInfo](./DamageInfo.md) | A damage info with type `Explosion` and `isSplashDamage` set to `true`. Read-only. |

## Static Methods

### EvaluateLastExplosionDamage

Evaluates the explosion damage at the specified point. Can optionally ignore level geometry which would otherwise block damage through walls, etc.

| Parameter | Type | Description |
|-----------|------|-------------|
| `point` | `Vector3` | The world position to evaluate explosion damage at. |
| `ignoreLevelGeometry` | `bool` | Whether to ignore level geometry when evaluating the explosion damage. |

[return: [DamageInfo](./DamageInfo.md)]
The evaluated explosion damage info, or a default value if no explosion occurred.

## Enums

### DamageSourceType

| Value | Description |
|-------|-------------|
| `Unknown` | Unknown damage source. |
| [Projectile](./Projectile.md) | Damage from a projectile. |
| `Melee` | Damage from a melee attack. |
| `Explosion` | Damage from an explosion. |
| `StickyExplosive` | Damage from a sticky explosive. |
| `VehicleRam` | Damage from a vehicle collision. |
| `FallDamage` | Damage from falling. |
| `DamageZone` | Damage from a damage zone trigger. |
| `Exception` | Damage from an exception or error. |
| `Scripted` | Damage applied through script. |
| `ProjectileShatter` | Damage from a projectile shattering. |
