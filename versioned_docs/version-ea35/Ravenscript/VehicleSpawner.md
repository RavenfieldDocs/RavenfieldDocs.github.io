---
title: VehicleSpawner
---

Represents a spawner for vehicles in the game world. Handles spawning vehicles of specific types, managing spawn points, and tracking the last spawned vehicle.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `spawnType` | `VehicleSpawnType` | The type of vehicle this spawner produces. |
| `parentSpawnPoint` | [SpawnPoint](./SpawnPoint.md) | The spawn point this spawner belongs to. |
| `lastSpawnedVehicle` | [Vehicle](./Vehicle.md) | The vehicle that was last spawned by the spawner. |
| `lastSpawnedVehicleHasBeenUsed` | `bool` | Whether the last spawned vehicle has been used. |

## Methods

### GetPrefab

Get the active vehicle prefab of this spawner. Please note that the current value depends on which team owns the spawner's parent spawn point.

[return: GameObject]
The active vehicle prefab, or nil.

### GetPrefabVehicle

Gets the Vehicle component from the active prefab.

[return: Vehicle]
The Vehicle component, or nil.

### GetPrefab

Get the vehicle prefab for the specified team and type.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `WTeam` | The team to get the prefab for. |
| `type` | `VehicleSpawnType` | The type of vehicle to get. |

[return: GameObject]
The vehicle prefab for the specified team and type.

### SpawnIsBlocked

Returns true if the spawn is currently blocked.

[return: bool]
`true` if the spawn area is blocked.

### SpawnNow

Force spawns the active vehicle type. Does not check if the spawn area is clear or if the previous vehicle is still alive.

[return: Vehicle]
The spawned vehicle.

### SpawnVehicle

Spawns a vehicle of the specified type.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `WTeam` | The team to spawn the vehicle for. |
| `type` | `VehicleSpawnType` | The type of vehicle to spawn. |
| `position` | `Vector3` | The position to spawn at. |
| `rotation` | `Quaternion` | The rotation to spawn with. |

[return: Vehicle]
The spawned vehicle.

### SpawnVehicle

Spawns a vehicle using the specified vehicle info.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `WTeam` | The team to spawn the vehicle for. |
| `vehicleInfo` | `VehicleInfo` | The vehicle info to spawn. |
| `position` | `Vector3` | The position to spawn at. |
| `rotation` | `Quaternion` | The rotation to spawn with. |

[return: Vehicle]
The spawned vehicle.

### SpawnVehicleImposter

Spawns a vehicle imposter. A vehicle imposter only contains the renderers of the vehicle, without functionality and simulation components.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `WTeam` | The team to spawn the imposter for. |
| `vehicleInfo` | `VehicleInfo` | The vehicle info to spawn. |
| `position` | `Vector3` | The position to spawn at. |
| `rotation` | `Quaternion` | The rotation to spawn with. |

[return: GameObject]
The spawned vehicle imposter.

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

### VehicleSpawnType

| Value | Description |
|-------|-------------|
| `Jeep` | A standard jeep vehicle. |
| `JeepMachineGun` | A jeep equipped with a machine gun. |
| `Quad` | A quad bike vehicle. |
| `Tank` | A tank vehicle. |
| `AttackHelicopter` | An attack helicopter. |
| `AttackPlane` | An attack plane. |
| `Rhib` | A rigid-hulled inflatable boat. |
| `AttackBoat` | An attack boat. |
| `BomberPlane` | A bomber plane. |
| `TransportHelicopter` | A transport helicopter. |
| `Apc` | An armored personnel carrier. |
