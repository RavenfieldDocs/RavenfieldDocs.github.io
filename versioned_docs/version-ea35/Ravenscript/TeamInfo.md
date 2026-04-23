---
title: TeamInfo
---

Contains information about a team, including its color, name, skin, and available weapons and vehicles.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `color` | `Color` | The team's color. |
| `name` | `string` | The team's name. |
| `skin` | `ActorSkin` | The team's actor skin. Defaults to the default actor skin if not set. |

## Methods

### GetAllWeapons

Returns all weapons available to this team.

[return: `WeaponEntry[]`]

### GetWeapons

Returns all weapons available to this team in a specific rarity tier.

| Parameter | Type | Description |
|-----------|------|-------------|
| `tier` | `RarityTier` | The rarity tier to filter by. |

[return: `WeaponEntry[]`]

### GetWeaponIsAvailable

Returns whether a weapon entry is available to this team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `entry` | `WeaponEntry` | The weapon entry to check. |

[return: `bool`]

### GetWeaponRarity

Returns the rarity tier of a weapon entry for this team. Logs an error if the weapon is not available.

| Parameter | Type | Description |
|-----------|------|-------------|
| `entry` | `WeaponEntry` | The weapon entry to check. |

[return: `RarityTier`]

### GetAllVehicles

Returns all vehicles available to this team.

[return: `VehicleInfo[]`]

### GetAvailableSpawnsForVehicle

Returns all available spawn configurations for a vehicle.

| Parameter | Type | Description |
|-----------|------|-------------|
| `info` | `VehicleInfo` | The vehicle info to get spawns for. |

[return: `VehicleSpawnConfiguration[]`]

### GetAvailableSpawnsForTurret

Returns all available spawn configurations for a turret.

| Parameter | Type | Description |
|-----------|------|-------------|
| `info` | `VehicleInfo` | The turret vehicle info to get spawns for. |

[return: `TurretSpawnConfiguration[]`]

### GetVehicles

Returns all vehicles of a specific spawn type available to this team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `type` | `VehicleSpawnType` | The vehicle spawn type to filter by. |

[return: `VehicleInfo[]`]

### GetVehicles

Returns all vehicles of a specific spawn type and rarity tier available to this team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `type` | `VehicleSpawnType` | The vehicle spawn type to filter by. |
| `tier` | `RarityTier` | The rarity tier to filter by. |

[return: `VehicleInfo[]`]

### GetAllTurrets

Returns all turrets available to this team.

[return: `VehicleInfo[]`]

### GetTurrets

Returns all turrets of a specific spawn type available to this team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `type` | `TurretSpawnType` | The turret spawn type to filter by. |

[return: `VehicleInfo[]`]

### GetTurrets

Returns all turrets of a specific spawn type and rarity tier available to this team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `type` | `TurretSpawnType` | The turret spawn type to filter by. |
| `tier` | `RarityTier` | The rarity tier to filter by. |

[return: `VehicleInfo[]`]

### AddWeapon

Adds a weapon entry to this team with a specific rarity tier.

| Parameter | Type | Description |
|-----------|------|-------------|
| `entry` | `WeaponEntry` | The weapon entry to add. |
| `tier` | `RarityTier` | The rarity tier for this weapon. |

### AddVehicle

Adds a vehicle to this team with a specific spawn type and rarity tier.

| Parameter | Type | Description |
|-----------|------|-------------|
| `vehicle` | `VehicleInfo` | The vehicle to add. |
| `type` | `VehicleSpawnType` | The spawn type for this vehicle. |
| `tier` | `RarityTier` | The rarity tier for this vehicle. |

### AddTurret

Adds a turret to this team with a specific spawn type and rarity tier.

| Parameter | Type | Description |
|-----------|------|-------------|
| `vehicle` | `VehicleInfo` | The turret vehicle to add. |
| `type` | `TurretSpawnType` | The spawn type for this turret. |
| `tier` | `RarityTier` | The rarity tier for this turret. |

### ClearWeapons

Removes all weapon entries from this team.

### ClearVehicles

Removes all vehicles from this team.

### ClearTurrets

Removes all turrets from this team.

### RemoveWeapon

Removes a weapon entry from this team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `entry` | `WeaponEntry` | The weapon entry to remove. |

### RemoveVehicle

Removes a vehicle from this team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `type` | `VehicleSpawnType` | The spawn type of the vehicle to remove. |
| `vehicle` | `VehicleInfo` | The vehicle to remove. |

### RemoveTurret

Removes a turret from this team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `type` | `TurretSpawnType` | The spawn type of the turret to remove. |
| `vehicle` | `VehicleInfo` | The turret vehicle to remove. |

## Events

## Static Fields

## Static Methods

### GetDefault

Returns the default TeamInfo for the current loaded mods.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `Team` | The team to get the default info for. |

[return: `TeamInfo`]

### Clone

Clones an existing TeamInfo.

| Parameter | Type | Description |
|-----------|------|-------------|
| `original` | `TeamInfo` | The TeamInfo to clone. |

[return: `TeamInfo`]

### CreateEmpty

Returns an empty TeamInfo.

[return: `TeamInfo`]

## Enums
