---
title: Order
---

Represents a squad order in the game, defining movement objectives, target positions, waypoints, and priority for AI squads.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `type` | `OrderType` | The type of this order. |
| `sourcePoint` | [SpawnPoint](./SpawnPoint.md) | The spawn point this order originated from. |
| `targetPoint` | [SpawnPoint](./SpawnPoint.md) | The spawn point this order targets. |
| `hasOverrideTargetPosition` | `bool` | Returns `true` if an override target position is set. |
| `basePriority` | `int` | The priority of this order when not assigned to any squads. |
| `priority` | `int` | The current priority of the order, modified by any squads it is currently assigned to. |
| `uniqueID` | `int` | This value is unique to every active order. |
| `isIssuedByPlayer` | `bool` | Returns `true` if this order was created by the player via the tactics view. |

## Methods

### SetOverrideTargetPosition

Sets an override target position. Gives full control over exactly where the squad goes when completing the objective.

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The override target position. |

### GetOverrideTargetPosition

Returns the current override target position.

[return: Vector3]
The override target position.

### DropOverrideTargetPosition

Drops the active override target position.

### Create

Creates a new Order instance.

| Parameter | Type | Description |
|-----------|------|-------------|
| `type` | `OrderType` | The type of order to create. |
| `source` | `SpawnPoint` | The source spawn point. |
| `target` | `SpawnPoint` | The target spawn point. |

[return: Order]
The newly created order.

### Create

Creates a new Order instance with an override target position.

| Parameter | Type | Description |
|-----------|------|-------------|
| `type` | `OrderType` | The type of order to create. |
| `source` | `SpawnPoint` | The source spawn point. |
| `target` | `SpawnPoint` | The target spawn point. |
| `overridePosition` | `Vector3` | The override target position. |

[return: Order]
The newly created order.

### CreateMoveOrder

Convenience function that creates a move order to the specified override target position.

| Parameter | Type | Description |
|-----------|------|-------------|
| `targetPosition` | `Vector3` | The target position for the move order. |

[return: Order]
The newly created move order.

## Enums

### OrderType

| Value | Description |
|-------|-------------|
| `Attack` | An attack order. |
| `Defend` | A defend order. |
| `Roam` | A roam order. |
| `Repair` | A repair order. |
| `Move` | A move order. |
| `PatrolBase` | A patrol base order. |
| `PatrolWaypoints` | A patrol waypoints order. |
