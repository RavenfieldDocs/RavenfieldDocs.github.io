---
title: Order
---

## Properties

| Name | Type | Description |
| --- | --- | --- |
| type | OrderType | The type of this order. |
| source | SpawnPoint | The spawn point this order originated from. |
| target | SpawnPoint | The spawn point this order targets. |
| targetSquad | Squad | The squad currently targeted by this order. |
| hasOverrideTargetPosition | bool | Returns true if an override target position is set. |
| overrideTargetPosition | Vector3 | The override target position for this order. |
| basePriority | int | The priority of this order when not assigned to any squads. |
| modifierMultiplier | int | The multiplier applied to priority modifiers. |
| waypoints | Vector3[] | The waypoints for this order. |
| uniqueID | int | This value is unique to every active order. |
| requiredVehicleFilter | VehicleFilter | The vehicle filter required for this order. |
| canWalk | bool | Returns true if there is a land connection between source and target. |
| isIssuedByPlayer | bool | Returns true if this order was created by the player via the tactics view. |

## Methods

### SetTargetSquad

Sets the target squad for this order.

| Parameter | Type | Description |
| --- | --- | --- |
| squad | Squad | The squad to set as the target. |

**Returns:** void

### SetWaypoints

Sets the waypoints for this order.

| Parameter | Type | Description |
| --- | --- | --- |
| waypoints | Vector3[] | The waypoints to set. |

**Returns:** void

### SetOverrideTargetPosition

Sets an override target position. Gives full control over exactly where the squad goes when completing the objective.

| Parameter | Type | Description |
| --- | --- | --- |
| position | Vector3 | The override target position. |

**Returns:** void

### DropOverrideTargetPosition

Drops the active override target position.

**Returns:** void

### ModifyPriority

Modifies the priority of this order for a specific squad.

| Parameter | Type | Description |
| --- | --- | --- |
| squad | Squad | The squad to modify the priority for. |
| modifier | int | The priority modifier value. |

**Returns:** void

### ResetPriorityModifier

Resets the priority modifier for a specific squad.

| Parameter | Type | Description |
| --- | --- | --- |
| squad | Squad | The squad to reset the priority modifier for. |

**Returns:** void

### GetPriority

Returns the current priority of the order, modified by any squads it is currently assigned to.

**Returns:** int

### IsEnabled

Returns true if this order is currently enabled and can be assigned to squads.

**Returns:** bool

### SetEnabled

Sets whether this order is enabled.

| Parameter | Type | Description |
| --- | --- | --- |
| enabled | bool | Whether the order should be enabled. |

**Returns:** void

### ResolveCurrentTargetPosition

Resolves the current target position for this order.

**Returns:** Vector3

## Static Methods

### Create

Creates a new Order instance.

| Parameter | Type | Description |
| --- | --- | --- |
| type | OrderType | The type of order to create. |
| source | SpawnPoint | The source spawn point. |
| target | SpawnPoint | The target spawn point. |

**Returns:** Order

### Create

Creates a new Order instance with an override target position.

| Parameter | Type | Description |
| --- | --- | --- |
| type | OrderType | The type of order to create. |
| source | SpawnPoint | The source spawn point. |
| target | SpawnPoint | The target spawn point. |
| overridePosition | Vector3 | The override target position. |

**Returns:** Order

### CreateMoveOrder

Convenience function that creates a move order to the specified override target position.

| Parameter | Type | Description |
| --- | --- | --- |
| targetPosition | Vector3 | The target position for the move order. |

**Returns:** Order
