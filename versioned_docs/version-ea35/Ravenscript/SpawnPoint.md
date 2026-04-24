---
title: SpawnPoint
---

Represents a spawn point in the game world. Handles spawning of vehicles, turrets, and actors, as well as capture point logic and neighbor relationships.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `gameObject` | [GameObject](./GameObject.md) | The GameObject attached to this SpawnPoint. |
| `transform` | [Transform](./Transform.md) | The Transform of this SpawnPoint. |
| `capturePoint` | [CapturePoint](./CapturePoint.md) | Returns the CapturePoint if this SpawnPoint is one, otherwise nil. |
| `defaultOwner` | [Team](./Team.md) | The default owning team of this spawn point. |
| `name` | `string` | The short name of this spawn point (maps to `shortName` in C#). |
| `neighours` | [SpawnPoint](./SpawnPoint.md)[] | Gets all neighbors connected to this point, ignoring one way connections. |
| `neighoursIncoming` | [SpawnPoint](./SpawnPoint.md)[] | Gets all neighbors that can attack this point, respecting one way connections. |
| `neighoursOutgoing` | [SpawnPoint](./SpawnPoint.md)[] | Gets all neighbors that can be attacked from point, respecting one way connections. |
| `owner` | [Team](./Team.md) | The current owning team of this spawn point. |
| `spawnpointContainer` | [Transform](./Transform.md) | Container transform for spawn point positions. |
| `spawnPosition` | `Vector3` | The spawn position of this point. |
| `turretSpawners` | [TurretSpawner](./TurretSpawner.md)[] | Turret spawners associated with this spawn point. |
| `vehicleSpawners` | [VehicleSpawner](./VehicleSpawner.md)[] | Vehicle spawners associated with this spawn point. |
| `landingZones` | `LandingZone[]` | Landing zones associated with this spawn point. |
| `isCapturePoint` | `bool` | Returns true if this is a CapturePoint. |

## Methods

### AddIncomingNeighbor

Adds a spawn point as an incoming neighbor.

| Parameter | Type | Description |
|-----------|------|-------------|
| `spawn` | [SpawnPoint](./SpawnPoint.md) | The spawn point to add as an incoming neighbor. |

### AddOutgoingNeighbor

Adds a spawn point as an outgoing neighbor.

| Parameter | Type | Description |
|-----------|------|-------------|
| `spawn` | [SpawnPoint](./SpawnPoint.md) | The spawn point to add as an outgoing neighbor. |

### AddNeighbor

Adds a spawn point as a bidirectional neighbor.

| Parameter | Type | Description |
|-----------|------|-------------|
| `spawn` | [SpawnPoint](./SpawnPoint.md) | The spawn point to add as a neighbor. |

### FindNearbyStuff

Finds nearby vehicle spawners and turrets within protect range.

### SetGhost

Sets whether this spawn point is a ghost spawn.

| Parameter | Type | Description |
|-----------|------|-------------|
| `isGhost` | `bool` | Whether this is a ghost spawn point. |

### HasAnyHelicopterLandingZone

Returns true if this spawn point has any helicopter landing zones.

### CollectHelicopterLandingZones

Collects and initializes all helicopter landing zones for this spawn point.

### GetAllHelicopterLandingZones

Returns all helicopter landing zones for this spawn point.

### GetRandomHelicopterLandingZone

Returns a random helicopter landing zone from this spawn point.

### FindCoverPoints

Finds and sorts cover points within protect range of this spawn point.

### GetAvailableCoverPoint

Gets an available cover point, prioritizing cover against enemy neighbors.

### GetAvailableVehicle

Gets an available vehicle matching the filter.

| Parameter | Type | Description |
|-----------|------|-------------|
| `filter` | `VehicleFilter` | Filter to apply to vehicles. |
| `passengers` | `int` | Required number of passenger seats (default: -1). |

[return: [Vehicle](./Vehicle.md)]
The available vehicle matching the filter, or nil.

### GetAvailableVehicle

Gets an available vehicle matching the filter with priority output.

| Parameter | Type | Description |
|-----------|------|-------------|
| `filter` | `VehicleFilter` | Filter to apply to vehicles. |
| `passengers` | `int` | Required number of passenger seats (default: -1). |

[return: Vehicle, byte]
1. The available vehicle matching the filter, or nil.
2. The output priority of the returned vehicle.

### GetAvailableRoamingVehicle

Gets an available roaming vehicle from this spawn point.

### FindTurrets

Finds nearby turrets within protect range of this spawn point.

### IsValidDefenseTurret

Returns true if the vehicle is a valid defense turret for this spawn point.

| Parameter | Type | Description |
|-----------|------|-------------|
| `vehicle` | [Vehicle](./Vehicle.md) | The vehicle to check. |

[return: bool]
`true` if the vehicle is a valid defense turret.

### HasAnyAvailableTurrets

Returns true if there are any available turrets at this spawn point.

### GetAvailableTurret

Gets an available turret at this spawn point.

### TransformFacesEnemySpawn

Returns true if the given transform faces an enemy spawn.

| Parameter | Type | Description |
|-----------|------|-------------|
| `transform` | [Transform](./Transform.md) | The transform to check. |

[return: bool]
`true` if the transform faces an enemy spawn.

### GetSpawnPosition

Gets the spawn position for this point.

### GenerateRandomSpawnPosition

Generates a random spawn position near this point.

### RandomPositionInCaptureZone

Gets a random position within the capture zone.

### GetNSpawnPoints

Gets the number of spawn points in a container.

| Parameter | Type | Description |
|-----------|------|-------------|
| `container` | [Transform](./Transform.md) | The container to count spawn points in. |

[return: int]
The number of spawn points in the container.

### RandomSpawnPointPosition

Gets a random position from a spawn point container.

| Parameter | Type | Description |
|-----------|------|-------------|
| `container` | [Transform](./Transform.md) | The container to pick a random spawn point from. |

[return: Vector3]
A random spawn position from the container.

### RandomPatrolPosition

Gets a random patrol position for this spawn point.

### IsSafe

Returns true if this spawn point is safe.

### SetOwner

Sets the owner of this spawn point.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `int` | The team to set as owner. |
| `initialOwner` | `bool` | Whether this is the initial owner assignment. |

### IsFrontLine

Returns true if this spawn point is on the front line (has enemy neighbors).

### AddLandingZone

Adds a landing zone to this spawn point.

| Parameter | Type | Description |
|-----------|------|-------------|
| `lz` | `LandingZone` | The landing zone to add. |

### IsInsideCaptureVolume

Returns true if a position is inside the capture volume.

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The position to check. |

[return: bool]
`true` if the position is inside the capture volume.

### GetCaptureRange

Gets the capture range of this spawn point.

### IsInsideProtectRange

Returns true if a position is inside the protect range.

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The position to check. |

[return: bool]
`true` if the position is inside the protect range.

### IsInsideTransportDropRange

Returns true if a position is inside the transport drop range.

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The position to check. |

[return: bool]
`true` if the position is inside the transport drop range.

### GetClosestNavmeshArea

Gets the closest navmesh area of the given type.

| Parameter | Type | Description |
|-----------|------|-------------|
| `type` | `PathfindingBox.Type` | The type of navmesh area to find. |

[return: uint]
The navmesh area value.

### IsNeighborTo

Returns true if the other spawn point is a neighbor.

| Parameter | Type | Description |
|-----------|------|-------------|
| `other` | [SpawnPoint](./SpawnPoint.md) | The other spawn point to check. |

[return: bool]
`true` if the other spawn point is a neighbor.

### OnAnySpawnContainerChanged

Called when any spawn container is changed.

### OnNavmeshReady

Called when the navmesh is ready.

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|
