---
title: CapturePoint
---

Represents a capture point (flag) in the game world. Handles capture progress, team ownership, spawn points, and contested zones.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `captureRange` | `float` | The range of the capture point. |
| `captureFloor` | `float` | The distance below the capture point where actors can capture it. |
| `captureCeiling` | `float` | The distance above the capture point where actors can capture it. |
| `captureRate` | `float` | The rate at which the capture point is captured. |
| `captureVolume` | `TriggerVolume` | The trigger volume that defines the capture zone. |
| `captureProgress` | `float` | The capture progress of the pending owner, from 0 to 1. |
| `contestedSpawnpointContainer` | `Transform` | The container for contested spawn points. |
| `flagRenderer` | `Renderer` | Returns the renderer of the flag, if available. |
| `isContested` | `bool` | True while any attackers are inside the capture zone. |
| `pendingOwner` | `Team` | The team that is closest to taking over the capture point. This is the same team as the current team color indicated on the flag renderer. |
| `defaultOwner` | `Team` | The default owner of this spawn point. |
| `isCapturePoint` | `bool` | Returns true if this is a CapturePoint. |
| `name` | `string` | The short name of this spawn point. |
| `owner` | `Team` | The current owner of this spawn point. |
| `spawnpointContainer` | `Transform` | The container for spawn points. |
| `spawnPosition` | `Vector3` | The spawn position of this spawn point. |
| `neighbours` | [SpawnPoint](./SpawnPoint.md)[] | Gets all neighbors connected to this point, ignoring one way connections. |
| `neighboursIncoming` | [SpawnPoint](./SpawnPoint.md)[] | Gets all neighbors that can attack this point, respecting one way connections. |
| `neighboursOutgoing` | [SpawnPoint](./SpawnPoint.md)[] | Gets all neighbors that can be attacked from this point, respecting one way connections. |
| `turretSpawners` | `TurretSpawner[]` | The turret spawners at this spawn point. |
| `vehicleSpawners` | `VehicleSpawner[]` | The vehicle spawners at this spawn point. |

## Methods

### IsUnderAttack

Returns true if the capture point is under attack.

### RandomContestedSpawnPointPosition

Returns a random spawn point position from the contested spawn point container.

[return: Vector3]
A random position within the contested spawn point container.

## Events

| Event | Signature | Description |
|-------|-----------|-------------|
| `onCapturePointCaptured` | `(capturePoint, newOwner)` | Invoked when a capture point is captured, i.e. when its owner is set to Team.Blue or Team.Red. |
| `onCapturePointNeutralized` | `(capturePoint, previousOwner)` | Invoked when a capture point is neutralized, i.e. when its owner is set to Team.Neutral. |
