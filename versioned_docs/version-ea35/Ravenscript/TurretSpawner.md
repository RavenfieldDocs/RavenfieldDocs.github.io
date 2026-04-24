---
title: TurretSpawner
---

Represents a spawn point for turrets. Handles spawning of turrets for specific teams and turret types.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `typeToSpawn` | `TurretSpawnType` | The type of turret this spawner will spawn. |
| `activeTurret` | [Vehicle](./Vehicle.md) | The currently spawned turret, or `nil`. |
| `parentSpawnPoint` | [SpawnPoint](./SpawnPoint.md) | The spawn point this turret spawner is assigned to. |

## Methods

### SpawnTurret

Spawns a turret for the specified team. This will throw an error if the turret spawned behaviour is not set to Scripted.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | [Team](./Team.md) | The team to spawn the turret for. |

[return: [Vehicle](./Vehicle.md)]
The spawned turret vehicle.

### SpawnTurret

Spawns a turret of the specified type at the given position and rotation.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | [Team](./Team.md) | The team to spawn the turret for. |
| `type` | `TurretSpawnType` | The type of turret to spawn. |
| `position` | `Vector3` | The position to spawn at. |
| `rotation` | `Quaternion` | The rotation to spawn with. |

[return: [Vehicle](./Vehicle.md)]
The spawned turret vehicle.

### SpawnTurret

Spawns a turret of the specified type and rarity tier at the given position and rotation.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | [Team](./Team.md) | The team to spawn the turret for. |
| `type` | `TurretSpawnType` | The type of turret to spawn. |
| `position` | `Vector3` | The position to spawn at. |
| `rotation` | `Quaternion` | The rotation to spawn with. |
| `tier` | `RarityTier` | The rarity tier of the turret to spawn. |

[return: [Vehicle](./Vehicle.md)]
The spawned turret vehicle.

## Static Fields

| Field | Type | Description |
|-------|------|-------------|
| `ALL_TURRET_TYPES` | `TurretSpawnType[]` | Array of all turret spawn types. |

## Static Methods

### GetPrefab

Gets the prefab GameObject for a turret of the specified type and team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | [Team](./Team.md) | The team to get the prefab for. |
| `type` | `TurretSpawnType` | The type of turret. |

[return: [GameObject](./GameObject.md)]
The turret prefab, or `nil`.

### GetPrefabVehicle

Gets the Vehicle component from the prefab for a turret of the specified type and team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | [Team](./Team.md) | The team to get the prefab for. |
| `type` | `TurretSpawnType` | The type of turret. |

[return: [Vehicle](./Vehicle.md)]
The turret vehicle prefab, or `nil`.

## Enums

### TurretSpawnType

| Value | Description |
|-------|-------------|
| `MachineGun` | A machine gun turret. |
| `AntiTank` | An anti-tank turret. |
| `AntiAir` | An anti-air turret. |
