---
title: Vehicle
---

## Properties

| Name | Type | Description |
| --- | --- | --- |
| seats | array\<Seat> |  |
| name | string |  |
| minimapBlip | Texture |  |
| ownerTeam | Team |  |
| isDead | bool |  |
| hasCountermeasures | bool |  |
| canSeePlayer | bool | Returns true if there is a line of sight between the vehicle's lock on point and the player camera. |
| playerDistance | float |  |
| playerIsInside | bool |  |
| hasDriver | bool |  |
| driver | Actor |  |
| isTrackedByMissile | bool | True while one or more missiles are tracking this vehicle. |
| isBeingLocked | bool | True while one or more target tracking weapons are locking onto this vehicle. |
| health | float |  |
| maxHealth | float |  |
| isBurning | bool |  |
| isFull | bool |  |
| isEmpty | bool |  |
| isInWater | bool |  |
| rigidbody | Rigidbody |  |
| isTurret | bool | Returns true if vehicle is marked as a Turret. |
| isCar | bool | Returns true if this vehicle is a Car. If true, you can safely access fields via the Car class API. |
| isBoat | bool | Returns true if this vehicle is a Boat. If true, you can safely access fields via the Boat class API. |
| isHelicopter | bool | Returns true if this vehicle is a Helicopter. If true, you can safely access fields via the Helicopter class API. |
| isAirplane | bool | Returns true if this vehicle is an Airplane. If true, you can safely access fields via the Airplane class API. |
| avoidanceRadius | float | The radius of the vehicle's specified avoidance size. |
| spotChanceMultiplier | float |  |
| engine | Engine |  |
| isTransportVehicle | bool | Returns true if AIType is set to transport. |
| vehicleInfo | VehicleInfo |  |

## Events

| Name | Type | Description |
| --- | --- | --- |
| onClaimedBySquad | ScriptEvent\<Squad> | Invoked whenever a squad claims this vehicle. |
| onClaimDropped | ScriptEvent\<Squad> | Invoked whenever a squad drops their claim over this vehicle. |

## Methods

### Damage

Damages the vehicle.

| Parameter | Type | Description |
| --- | --- | --- |
| source | Actor | The actor that caused the damage. |
| amount | float | The amount of damage to deal. |

**Returns:** void

### Repair

Repairs the vehicle by the specified health amount. Returns true if the vehicle was healed (that is, if it was not already at max health.)

| Parameter | Type | Description |
| --- | --- | --- |
| amount | float | The amount of health to restore. |

**Returns:** bool

### GetEmptySeat

Get the first available empty seat in the vehicle.

| Parameter | Type | Description |
| --- | --- | --- |
| allowDriverSeat | bool | Whether to allow returning the driver seat. |

**Returns:** Seat

### GetTrackingMissiles

Returns all missile projectiles that are currently tracking this vehicle.

**Returns:** array\<TargetSeekingMissile>

### ToString

Returns a string representation of the vehicle.

**Returns:** string

## Static Methods

### New

Creates a new Engine instance.

**Returns:** Engine

## Nested Types

### Engine

Represents the engine of a vehicle.

#### Properties

| Name | Type | Description |
| --- | --- | --- |
| controlAudio | bool |  |
| enabled | bool |  |
| ignitionClip | AudioClip |  |
| pitchGainSpeed | float |  |
| power | float |  |
| powerGainSpeed | float |  |
| shiftForwardClip | AudioClip |  |
| shiftReverseClip | AudioClip |  |
| targetPitch | float |  |
| targetThrottle | float |  |
| throttleGainSpeed | float |  |

#### Methods

##### PlayIgnitionSound

Plays the ignition sound.

**Returns:** void

##### PlayShiftForwardSound

Plays the shift forward sound.

**Returns:** void

##### PlayShiftReverseSound

Plays the shift reverse sound.

**Returns:** void

##### Reset

Resets the engine.

**Returns:** void

##### ToString

Returns a string representation of the engine.

**Returns:** string
