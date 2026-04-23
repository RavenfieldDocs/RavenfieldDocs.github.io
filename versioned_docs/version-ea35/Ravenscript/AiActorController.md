---
title: AiActorController
---

Controls AI behavior for an actor, including movement, combat, and vehicle interactions.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `meleeChargeRange` | `float` | The maximum range in meters at which the AI will attempt to charge an enemy. Default is 30. |
| `canSprint` | `bool` | Whether the AI is allowed to sprint. |
| `canJoinPlayerSquad` | `bool` | While false, the player cannot issue a join squad order on this AI bot. |
| `ignoreFovCheck` | `bool` | Ignore FOV Check when querying sight. If set to true, this AI is able to see enemies all around, even behind. |
| `alwaysChargeTarget` | `bool` | Charge towards target at all times. If set to true, this AI will always run towards an enemy target, even when it is out of melee range. |
| `isDefaultMovementOverridden` | `bool` | True if the built in AI movement is disabled. |
| `hasPath` | `bool` | Returns true if the AI is traversing a path. |
| `isEnteringVehicle` | `bool` | Returns true if the AI has a target vehicle, and is currently attempting to enter it. |
| `hasTargetVehicle` | `bool` | Returns true if the AI has a target vehicle to enter, or that they are already seated in. |
| `targetVehicle` | `[Vehicle](./Vehicle.md)` | Returns the target vehicle the AI is entering or is already seated in. |
| `lastGotoPoint` | `Vector3` | The destination point of the last Goto() order. |
| `lastWaypoint` | `Vector3` | The last reached path waypoint. |
| `currentWaypoint` | `Vector3` | The current waypoint. |
| `targetFlightAltitude` | `float` | The default altitude the AI will try to maintain in an Aircraft. This value is randomized every time a bot enters or exits an aircraft. |
| `currentAttackTarget` | `[Actor](./Actor.md)` | The target this AI is currently attacking. |
| `skillLevel` | `SkillLevel` | The skill level of this AI. |

## Methods

### OverrideDefaultMovement

Disables the built in AI movement, allowing full movement control from scripts.

### ReleaseDefaultMovementOverride

Re-enables the built in AI movement.

### Goto

Pathfinds to the closest destination point on the current navmesh.

| Parameter | Type | Description |
|-----------|------|-------------|
| `destination` | `Vector3` | The destination point to pathfind to. |

### GotoDirect

Go straight to the destination point, ignoring pathfinding.

| Parameter | Type | Description |
|-----------|------|-------------|
| `destination` | `Vector3` | The destination point to move towards. |

### CancelPath

Stops the current AI path movement.

### GotoAndEnterVehicle

Orders the AI to enter the specified vehicle. Also sets the AI's target vehicle to the specified vehicle.

| Parameter | Type | Description |
|-----------|------|-------------|
| `vehicle` | `[Vehicle](./Vehicle.md)` | The vehicle to enter. |

### LeaveVehicle

Leaves the target vehicle.

### IsInFOV

Returns true if the target is inside this actor's field of view.

| Parameter | Type | Description |
|-----------|------|-------------|
| `targetActor` | `[Actor](./Actor.md)` | The actor to check. |

[return: `bool`]

### IsInFOV

Returns true if the position is inside this actor's field of view.

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The position to check. |

[return: `bool`]

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

### SkillLevel

| Value | Description |
|-------|-------------|
| `Beginner` | Beginner skill level. |
| `Normal` | Normal skill level. |
| `Veteran` | Veteran skill level. |
| `Elite` | Elite skill level. |
