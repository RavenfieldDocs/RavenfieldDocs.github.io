---
title: SpawnPoint
---

## Properties

| Name | Type | Description |
|------|------|-------------|
| `gameObject` | `GameObject` | The GameObject attached to this SpawnPoint |
| `transform` | `Transform` | The Transform of this SpawnPoint |
| `capturePoint` | `CapturePoint` | Returns the CapturePoint if this SpawnPoint is one, otherwise null |
| `defaultOwner` | `Team` | The default owning team of this spawn point |
| `name` | `string` | The short name of this spawn point |
| `neighours` | `SpawnPoint[]` | Gets all neighbors connected to this point, ignoring one way connections |
| `neighoursIncoming` | `SpawnPoint[]` | Gets all neighbors that can attack this point, respecting one way connections |
| `neighoursOutgoing` | `SpawnPoint[]` | Gets all neighbors that can be attacked from point, respecting one way connections |
| `owner` | `Team` | The current owning team of this spawn point |
| `spawnpointContainer` | `Transform` | Container transform for spawn point positions |
| `spawnPosition` | `Vector3` | The spawn position of this point |
| `turretSpawners` | `TurretSpawner[]` | Turret spawners associated with this spawn point |
| `vehicleSpawners` | `VehicleSpawner[]` | Vehicle spawners associated with this spawn point |
| `landingZones` | `LandingZone[]` | Landing zones associated with this spawn point |
| `isCapturePoint` | `bool` | Returns true if this is a CapturePoint |

## Methods

### `AddIncomingNeighbor(spawn)`

| Parameter | Type | Description |
|-----------|------|-------------|
| `spawn` | `SpawnPoint` | The spawn point to add as an incoming neighbor |

Adds a spawn point as an incoming neighbor.

### `AddOutgoingNeighbor(spawn)`

| Parameter | Type | Description |
|-----------|------|-------------|
| `spawn` | `SpawnPoint` | The spawn point to add as an outgoing neighbor |

Adds a spawn point as an outgoing neighbor.

### `AddNeighbor(spawn)`

| Parameter | Type | Description |
|-----------|------|-------------|
| `spawn` | `SpawnPoint` | The spawn point to add as a neighbor |

Adds a spawn point as a bidirectional neighbor.

### `FindNearbyStuff()`

Finds nearby vehicle spawners and turrets within protect range.

### `SetGhost(isGhost)`

| Parameter | Type | Description |
|-----------|------|-------------|
| `isGhost` | `bool` | Whether this is a ghost spawn point |

Sets whether this spawn point is a ghost spawn.

### `HasAnyHelicopterLandingZone()`

Returns true if this spawn point has any helicopter landing zones.

### `CollectHelicopterLandingZones()`

Collects and initializes all helicopter landing zones for this spawn point.

### `GetAllHelicopterLandingZones()`

Returns all helicopter landing zones for this spawn point.

**Returns:** `HelicopterLandingZone[]`

### `GetRandomHelicopterLandingZone()`

Returns a random helicopter landing zone from this spawn point.

**Returns:** `HelicopterLandingZone`

### `FindCoverPoints()`

Finds and sorts cover points within protect range of this spawn point.

### `GetAvailableCoverPoint()`

Gets an available cover point, prioritizing cover against enemy neighbors.

**Returns:** `CoverPoint`

### `GetAvailableVehicle(filter, passengers)`

| Parameter | Type | Description |
|-----------|------|-------------|
| `filter` | `VehicleFilter` | Filter to apply to vehicles |
| `passengers` | `int` | Required number of passenger seats (default: -1) |

Gets an available vehicle matching the filter.

**Returns:** `Vehicle`

### `GetAvailableVehicle(filter, priority, passengers)`

| Parameter | Type | Description |
|-----------|------|-------------|
| `filter` | `VehicleFilter` | Filter to apply to vehicles |
| `priority` | `byte` | Output priority of the returned vehicle |
| `passengers` | `int` | Required number of passenger seats (default: -1) |

Gets an available vehicle matching the filter with priority output.

**Returns:** `Vehicle`

### `GetAvailableRoamingVehicle()`

Gets an available roaming vehicle from this spawn point.

**Returns:** `Vehicle`

### `FindTurrets()`

Finds nearby turrets within protect range of this spawn point.

### `IsValidDefenseTurret(vehicle)`

| Parameter | Type | Description |
|-----------|------|-------------|
| `vehicle` | `Vehicle` | The vehicle to check |

Returns true if the vehicle is a valid defense turret for this spawn point.

**Returns:** `bool`

### `HasAnyAvailableTurrets()`

Returns true if there are any available turrets at this spawn point.

**Returns:** `bool`

### `GetAvailableTurret()`

Gets an available turret at this spawn point.

**Returns:** `Vehicle`

### `TransformFacesEnemySpawn(transform)`

| Parameter | Type | Description |
|-----------|------|-------------|
| `transform` | `Transform` | The transform to check |

Returns true if the given transform faces an enemy spawn.

**Returns:** `bool`

### `GetSpawnPosition()`

Gets the spawn position for this point.

**Returns:** `Vector3`

### `GenerateRandomSpawnPosition()`

Generates a random spawn position near this point.

**Returns:** `Vector3`

### `RandomPositionInCaptureZone()`

Gets a random position within the capture zone.

**Returns:** `Vector3`

### `GetNSpawnPoints(container)`

| Parameter | Type | Description |
|-----------|------|-------------|
| `container` | `Transform` | The container to count spawn points in |

Gets the number of spawn points in a container.

**Returns:** `int`

### `RandomSpawnPointPosition(container)`

| Parameter | Type | Description |
|-----------|------|-------------|
| `container` | `Transform` | The container to pick a random spawn point from |

Gets a random position from a spawn point container.

**Returns:** `Vector3`

### `RandomPatrolPosition()`

Gets a random patrol position for this spawn point.

**Returns:** `Vector3`

### `IsSafe()`

Returns true if this spawn point is safe.

**Returns:** `bool`

### `SetOwner(team, initialOwner)`

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `int` | The team to set as owner |
| `initialOwner` | `bool` | Whether this is the initial owner assignment |

Sets the owner of this spawn point.

### `IsFrontLine()`

Returns true if this spawn point is on the front line (has enemy neighbors).

**Returns:** `bool`

### `AddLandingZone(lz)`

| Parameter | Type | Description |
|-----------|------|-------------|
| `lz` | `LandingZone` | The landing zone to add |

Adds a landing zone to this spawn point.

### `IsInsideCaptureVolume(position)`

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The position to check |

Returns true if a position is inside the capture volume.

**Returns:** `bool`

### `GetCaptureRange()`

Gets the capture range of this spawn point.

**Returns:** `float`

### `IsInsideProtectRange(position)`

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The position to check |

Returns true if a position is inside the protect range.

**Returns:** `bool`

### `IsInsideTransportDropRange(position)`

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The position to check |

Returns true if a position is inside the transport drop range.

**Returns:** `bool`

### `GetClosestNavmeshArea(type)`

| Parameter | Type | Description |
|-----------|------|-------------|
| `type` | `PathfindingBox.Type` | The type of navmesh area to find |

Gets the closest navmesh area of the given type.

**Returns:** `uint`

### `IsNeighborTo(other)`

| Parameter | Type | Description |
|-----------|------|-------------|
| `other` | `SpawnPoint` | The other spawn point to check |

Returns true if the other spawn point is a neighbor.

**Returns:** `bool`

### `OnAnySpawnContainerChanged()`

Called when any spawn container is changed.

### `OnNavmeshReady()`

Called when the navmesh is ready.

## Events

This class has no script events.
