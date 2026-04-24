---
title: ExplosionConfiguration
---

Configuration for an explosion, including damage, force, and falloff curves.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `balanceDamage` | `float` | The balance damage of the explosion. |
| `balanceFalloff` | `AnimationCurve` or `nil` | The falloff curve for balance damage over distance. |
| `balanceRange` | `float` | The maximum range for balance damage. |
| `damage` | `float` | The base damage of the explosion. |
| `damageFalloff` | `AnimationCurve` or `nil` | The falloff curve for damage over distance. |
| `damageRange` | `float` | The maximum range for damage. |
| `force` | `float` | The explosion force. |
| `infantryDamageMultiplier` | `float` | Damage multiplier applied to infantry. |

## Methods

### CreateLinearFalloff

Creates a new configuration with linear falloff curves.

| Parameter | Type | Description |
|-----------|------|-------------|
| `damage` | `float` | The damage value. |
| `damageRange` | `float` | The damage range. |
| `balanceDamage` | `float` | The balance damage value. |
| `balanceDamageRange` | `float` | The balance damage range. |
| `force` | `float` | The explosion force. |

[return: [ExplosionConfiguration](./ExplosionConfiguration.md)]

### CreateSharpFalloff

Creates a new configuration with sharp falloff curves.

| Parameter | Type | Description |
|-----------|------|-------------|
| `damage` | `float` | The damage value. |
| `damageRange` | `float` | The damage range. |
| `balanceDamage` | `float` | The balance damage value. |
| `balanceDamageRange` | `float` | The balance damage range. |
| `force` | `float` | The explosion force. |

[return: [ExplosionConfiguration](./ExplosionConfiguration.md)]

### CreateSmoothStepFalloff

Creates a new configuration with smooth step falloff curves.

| Parameter | Type | Description |
|-----------|------|-------------|
| `damage` | `float` | The damage value. |
| `damageRange` | `float` | The damage range. |
| `balanceDamage` | `float` | The balance damage value. |
| `balanceDamageRange` | `float` | The balance damage range. |
| `force` | `float` | The explosion force. |

[return: [ExplosionConfiguration](./ExplosionConfiguration.md)]

## Events

## Static Fields

## Static Methods

### Call

Creates a new `ExplosionConfiguration` instance. Called via `()`.

[return: [ExplosionConfiguration](./ExplosionConfiguration.md)]

## Enums
