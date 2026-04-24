---
title: AnimationDrivenVehicle
---

Represents a vehicle driven by animations rather than physics, with all the standard vehicle properties and methods.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `inputSmoothness` | `int` | The smoothness of input interpolation. |
| `planeInput` | `bool` | Whether to use airplane-style input. |
| `gameObject` | [GameObject](./GameObject.md) | The underlying GameObject. |
| `transform` | [Transform](./Transform.md) | The underlying Transform. |
| `avoidanceRadius` | `float` | The radius of the vehicle's specified avoidance size. |
| `canSeePlayer` | `bool` | Returns `true` if there is a line of sight between the vehicle's lock on point and the player camera. |
| `driver` | [Actor](./Actor.md) | The actor currently driving this vehicle. |
| `engine` | [Engine](./Engine.md) | The vehicle's engine component. |
| `hasCountermeasures` | `bool` | Whether the vehicle has countermeasures available. |
| `health` | `float` | Current health. |
| `isAirplane` | `bool` | Returns `true` if this vehicle is an Airplane. |
| `isBeingLocked` | `bool` | `true` while one or more target tracking weapons are locking onto this vehicle. |
| `isBoat` | `bool` | Returns `true` if this vehicle is a Boat. |
| `isBurning` | `bool` | Whether the vehicle is currently burning. |
| `isCar` | `bool` | Returns `true` if this vehicle is a Car. |
| `isHelicopter` | `bool` | Returns `true` if this vehicle is a Helicopter. |
| `isTrackedByMissile` | `bool` | `true` while one or more missiles are tracking this vehicle. |
| `isTransportVehicle` | `bool` | Returns `true` if AIType is set to transport. |
| `isTurret` | `bool` | Returns `true` if vehicle is marked as a Turret. |
| `maxHealth` | `float` | Maximum health. |
| `minimapBlip` | `Texture` | The texture shown on the minimap for this vehicle. |
| `name` | `string` | The vehicle's display name. |
| `ownerTeam` | [Team](./Team.md) | The team that owns this vehicle. |
| `playerDistance` | `float` | The distance from this vehicle to the nearest player. |
| `playerIsInside` | `bool` | Whether a player is inside this vehicle. |
| `rigidbody` | `Rigidbody` | The vehicle's rigidbody component. |
| `seats` | [Seat](./Seat.md)[] | Array of seats on this vehicle. |
| `spotChanceMultiplier` | `float` | Multiplier for the chance this vehicle is spotted by AI. |
| `team` | `int` | The team index this vehicle belongs to. |
| `vehicleInfo` | [VehicleInfo](./VehicleInfo.md) | The vehicle's info asset. |
| `hasDriver` | `bool` | Whether the vehicle has a driver. |
| `isDead` | `bool` | Whether the vehicle is destroyed. |
| `isEmpty` | `bool` | Whether all seats are empty. |
| `isFull` | `bool` | Whether all seats are occupied. |
| `isInWater` | `bool` | Whether the vehicle is in water. |
| `onClaimDropped` | ScriptEvent\<[Squad](./Squad.md)\> | Invoked whenever a squad drops their claim over this vehicle. |
| `onClaimedBySquad` | ScriptEvent\<[Squad](./Squad.md)\> | Invoked whenever a squad claims this vehicle. |

## Methods

### AngularVelocity

Returns the angular velocity of the vehicle.

[return: Vector3]
The angular velocity vector.

### Velocity

Returns the velocity of the vehicle.

[return: Vector3]
The velocity vector.

### Damage

Damages the vehicle.

| Parameter | Type | Description |
|-----------|------|-------------|
| `source` | [Actor](./Actor.md) | The actor that caused the damage, or `nil`. |
| `amount` | `float` | The amount of damage to deal. |

### GetEmptySeat

Gets the first available empty seat in the vehicle.

| Parameter | Type | Description |
|-----------|------|-------------|
| `allowDriverSeat` | `bool` | Whether to allow returning the driver seat. |

[return: [Seat](./Seat.md)]

### GetTrackingMissiles

Returns all missile projectiles that are currently tracking this vehicle.

[return: [TargetSeekingMissile](./TargetSeekingMissile.md)[]]

### Repair

Repairs the vehicle by the specified health amount.

| Parameter | Type | Description |
|-----------|------|-------------|
| `amount` | `float` | The amount of health to restore. |

[return: bool]
`true` if the vehicle was healed (not already at max health).

### ToString

Returns a string representation of the vehicle.

[return: string]

## Events

| Event | Signature | Description |
|-------|-----------|-------------|
| `onClaimedBySquad` | ScriptEvent\<[Squad](./Squad.md)\> | Invoked whenever a squad claims this vehicle. |
| `onClaimDropped` | ScriptEvent\<[Squad](./Squad.md)\> | Invoked whenever a squad drops their claim over this vehicle. |

## Static Fields

## Static Methods

## Enums
