---
title: WeaponEntry
---

Represents a weapon entry in the weapon manager, containing metadata about a weapon such as its prefab, name, slot, tags, and role.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `distance` | `Distance` | The effective combat distance for this weapon. |
| `prefab` | `GameObject` | The weapon prefab. |
| `prefabWeapon` | `[Weapon](./Weapon.md)` or `nil` | The Weapon component on the prefab, or `nil` if not found. |
| `name` | `string` | The name of this weapon. |
| `slot` | `WeaponSlot` | The equipment slot this weapon belongs to. |
| `tags` | `string[]` | The list of weapon tags, such as ``Assault``, ``Marksman`` etc. |
| `mainRole` | `WeaponRole` | The main weapon role generated from the weapon's stats. |
| `type` | `LoadoutType` | The loadout type of this weapon entry. |
| `usableByAi` | `bool` | Whether this weapon can be used by AI. |
| `uiSprite` | `Sprite` | The sprite used to represent this weapon in UI. |

## Methods

### HasTag

Returns true if the weapon entry has the tag (case insensitive).

| Parameter | Type | Description |
|-----------|------|-------------|
| `tag` | `string` | The tag to check for. |

[return: `bool`]

### InstantiateImposter

Instantiates an imposter object of the weapon prefab. The imposter object contains the third person transform of the weapon prefab, and has its ``Weapon`` component culled. If the weapon doesn't have a third person transform, this function will fail and return nil.

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The world position for the imposter. |
| `rotation` | `Quaternion` | The world rotation for the imposter. |

[return: `GameObject`]

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

## Enums

### Distance

| Value | Description |
|-------|-------------|
| `Short` | Short combat distance. |
| `Mid` | Medium combat distance. |
| `Far` | Long combat distance. |
| `Any` | Any distance. |
| `Auto` | Automatically determined distance. |

### LoadoutType

| Value | Description |
|-------|-------------|
| `Normal` | Standard weapon loadout. |
| `Stealth` | Stealth weapon loadout. |
| `AntiArmor` | Anti-armor weapon loadout. |
| `Repair` | Repair tool loadout. |
| `ResupplyAmmo` | Ammo resupply loadout. |
| `ResupplyHealth` | Health resupply loadout. |
| `SmokeScreen` | Smoke screen loadout. |
