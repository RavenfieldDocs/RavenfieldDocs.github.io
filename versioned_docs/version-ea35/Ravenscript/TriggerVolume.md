---
title: TriggerVolume
---

Represents a trigger volume in the game world. Used to detect when actors or points are inside a defined 2D polygonal area with floor and ceiling bounds.

## Properties

| Property | Type | Description |
|----------|------|-------------|

## Methods

### GetTeamCount

Returns the number of actors of a specific team inside the volume. Uses cached actor values, so may not be up to date if the trigger was recently moved.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | [Team](./Team.md) | The team to count actors for. |

[return: int]
The number of actors of the specified team inside the volume.

### ActorIsInside

Returns true if the specified actor is inside the volume. Uses cached actor values, so may not be up to date if the trigger was recently moved.

| Parameter | Type | Description |
|-----------|------|-------------|
| `actor` | [Actor](./Actor.md) | The actor to check. |

[return: bool]
`true` if the actor is inside the volume.

### PlayerIsInside

Returns true if the player is inside the volume. Uses cached actor values, so may not be up to date if the trigger was recently moved.

[return: bool]
`true` if the player is inside the volume.

### PointIsInside

Returns true if the specified world point is inside the volume. Always up to date.

| Parameter | Type | Description |
|-----------|------|-------------|
| `point` | `Vector3` | The world position to check. |

[return: bool]
`true` if the point is inside the volume.

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

| Method | Type | Description |
|--------|------|-------------|

## Enums

| Enum | Description |
|------|-------------|
