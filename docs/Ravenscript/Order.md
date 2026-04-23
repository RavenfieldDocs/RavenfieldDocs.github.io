---
title: Order
---

Represents a squad order in the game, defining movement objectives, target positions, waypoints, and priority for AI squads.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `type` | `OrderType` | The type of this order. |
| `source` | `SpawnPoint` | The spawn point this order originated from. |
| `target` | `SpawnPoint` | The spawn point this order targets. |
| `targetSquad` | `Squad` | The squad currently targeted by this order. |
| `hasOverrideTargetPosition` | `bool` | Returns `true` if an override target position is set. |
| `overrideTargetPosition` | `Vector3` | The override target position for this order. |
| `basePriority` | `int` | The priority of this order when not assigned to any squads. |
| `modifierMultiplier` | `int` | The multiplier applied to priority modifiers. |
| `waypoints` | `Vector3[]` | The waypoints for this order. |
| `uniqueID` | `int` | This value is unique to every active order. |
| `requiredVehicleFilter` | `VehicleFilter` | The vehicle filter required for this order. |
| `canWalk` | `bool` | Returns `true` if there is a land connection between source and target. |
| `isIssuedByPlayer` | `bool` | Returns `true` if this order was created by the player via the tactics view. |

## Methods

### SetTargetSquad

Sets the target squad for this order.

| Parameter | Type | Description |
|-----------|------|-------------|
| `squad` | `Squad` | The squad to set as the target. |

### SetWaypoints

Sets the waypoints for this order.

| Parameter | Type | Description |
|-----------|------|-------------|
| `waypoints` | `Vector3[]` | The waypoints to set. |

### SetOverrideTargetPosition

Sets an override target position. Gives full control over exactly where the squad goes when completing the objective.

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The override target position. |

### DropOverrideTargetPosition

Drops the active override target position.

### ModifyPriority

Modifies the priority of this order for a specific squad.

| Parameter | Type | Description |
|-----------|------|-------------|
| `squad` | `Squad` | The squad to modify the priority for. |
| `modifier` | `int` | The priority modifier value. |

### ResetPriorityModifier

Resets the priority modifier for a specific squad.

| Parameter | Type | Description |
|-----------|------|-------------|
| `squad` | `Squad` | The squad to reset the priority modifier for. |

### GetPriority

Returns the current priority of the order, modified by any squads it is currently assigned to.

[return: int]
The current priority value.

### IsEnabled

Returns `true` if this order is currently enabled and can be assigned to squads.

[return: bool]
Whether the order is enabled.

### SetEnabled

Sets whether this order is enabled.

| Parameter | Type | Description |
|-----------|------|-------------|
| `enabled` | `bool` | Whether the order should be enabled. |

### ResolveCurrentTargetPosition

Resolves the current target position for this order.

[return: Vector3]
The current target position.

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
