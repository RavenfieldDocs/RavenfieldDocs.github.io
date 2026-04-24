---
title: ExplodingProjectile
---

A projectile that explodes on impact, dealing area damage. Extends [Projectile](./Projectile.md) with explosion configuration.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `explosionConfiguration` | [ExplosionConfiguration](./ExplosionConfiguration.md) | The configuration defining the explosion's damage, range, force, and falloff behavior. |

## Methods

## Events

## Static Fields

## Static Methods

## Enums

### ExplosionConfiguration

Defines the parameters of an explosion: damage, range, force, and falloff curves. Available as a global type `ExplosionConfiguration` that can be constructed via `ExplosionConfiguration()`.

#### Properties

| Property | Type | Description |
|----------|------|-------------|
| `damage` | `float` | The maximum health damage at the explosion center. |
| `damageRange` | `float` | The maximum radius at which health damage is applied. |
| `damageFalloff` | `AnimationCurve` | Curve controlling how health damage falls off with distance. |
| `balanceDamage` | `float` | The maximum balance damage at the explosion center. |
| `balanceRange` | `float` | The maximum radius at which balance damage is applied. |
| `balanceFalloff` | `AnimationCurve` | Curve controlling how balance damage falls off with distance. |
| `force` | `float` | The explosion force applied to rigidbodies. |
| `infantryDamageMultiplier` | `float` | Multiplier applied to damage dealt to infantry actors. |

#### Static Methods

### CreateLinearFalloff

Creates an explosion configuration with a linear falloff. Typically useful for small size explosions.

| Parameter | Type | Description |
|-----------|------|-------------|
| `damage` | `float` | Maximum health damage at center. |
| `damageRange` | `float` | Radius of health damage. |
| `balanceDamage` | `float` | Maximum balance damage at center. |
| `balanceDamageRange` | `float` | Radius of balance damage. |
| `force` | `float` | Explosion force. |

[return: [ExplosionConfiguration](./ExplosionConfiguration.md)]

### CreateSharpFalloff

Creates an explosion configuration with sharp falloff. Typically useful for large explosions where the explosion should damage but not necessarily kill everyone in range.

| Parameter | Type | Description |
|-----------|------|-------------|
| `damage` | `float` | Maximum health damage at center. |
| `damageRange` | `float` | Radius of health damage. |
| `balanceDamage` | `float` | Maximum balance damage at center. |
| `balanceDamageRange` | `float` | Radius of balance damage. |
| `force` | `float` | Explosion force. |

[return: [ExplosionConfiguration](./ExplosionConfiguration.md)]

### CreateSmoothStepFalloff

Creates an explosion configuration with smooth step falloff. Typically useful for small explosions with a sharp change from high to low damage at half range.

| Parameter | Type | Description |
|-----------|------|-------------|
| `damage` | `float` | Maximum health damage at center. |
| `damageRange` | `float` | Radius of health damage. |
| `balanceDamage` | `float` | Maximum balance damage at center. |
| `balanceDamageRange` | `float` | Radius of balance damage. |
| `force` | `float` | Explosion force. |

[return: [ExplosionConfiguration](./ExplosionConfiguration.md)]
