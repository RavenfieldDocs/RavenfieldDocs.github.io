---
title: TargetSeekingMissile
---

Represents a target-seeking missile projectile. Extends [Projectile](./Projectile.md) with target tracking capabilities.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `currentTarget` | [Vehicle](./Vehicle.md) or `nil` | The vehicle currently being tracked by the missile. |
| `isTrackingTarget` | `bool` | Returns true if the missile is currently tracking a target. |
| `velocity` | `Vector3` | The current movement velocity of the projectile. |
| `killCredit` | [Actor](./Actor.md) | The actor who fired the projectile. If the projectile kills a target, this is the actor that is awarded the kill. |
| `armorDamage` | `Vehicle.ArmorRating` | The minimum armor rating that this projectile can damage. |
| `sourceWeapon` | [Weapon](./Weapon.md) | Gets the weapon that fired this projectile. |
| `travellingTowardsPlayer` | `bool` | Returns true if the projectile is heading towards the player actor, otherwise false. |
| `isActive` | `bool` | Returns true until the projectile hits something or expires. |
| `distanceTravelled` | `float` | The total distance the projectile has travelled. |
| `impactForce` | `float` | The force applied to any hit rigidbody. |
| `damage` | `float` | The health damage value dealt when hitting a hitbox. |
| `balanceDamage` | `float` | The balance damage value dealt when hitting a hitbox. |
| `gravityMultiplier` | `float` | The amount of gravity affecting the path of this projectile. |
| `isExplodingProjectile` | `bool` | True if the projectile is an ExplodingProjectile. If true, you can safely access fields via the ExplodingProjectile class API. |
| `isRocketProjectile` | `bool` | True if the projectile is a RocketProjectile. If true, you can safely access fields via the RocketProjectile class API. |
| `isTargetSeekingMissileProjectile` | `bool` | True if the projectile is a TargetSeekingMissileProjectile. If true, you can safely access fields via the TargetSeekingMissileProjectile class API. |
| `isGrenadeProjectile` | `bool` | True if the projectile is a GrenadeProjectile. If true, you can safely access fields via the GrenadeProjectile class API. |
| `isRigidbodyProjectile` | `bool` | True if the projectile is a RigidbodyProjectile. If true, you can safely access fields via the RigidbodyProjectile class API. |
| `isWireGuidedMissileProjectile` | `bool` | True if the projectile is a WireGuidedMissileProjectile. If true, you can safely access fields via the WireGuidedMissileProjectile class API. |

## Methods

### SetTrackerTarget

Sets the vehicle for the missile to track.

| Parameter | Type | Description |
|-----------|------|-------------|
| `vehicle` | [Vehicle](./Vehicle.md) | The vehicle to track. |

### ClearTrackerTarget

Clears the current tracking target. The missile will no longer seek any target.

### Stop

Stops and destroys the projectile. Exploding projectiles trigger an explosion if silent is false, otherwise they are immediately destroyed.

| Parameter | Type | Description |
|-----------|------|-------------|
| `silent` | `bool` | If false, exploding projectiles trigger an explosion. If true, they are immediately destroyed. |

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

### EnumName

| Value | Description |
|-------|-------------|
