---
title: Vehicle
---

Represents a vehicle in the game world. Handles seating, damage, health, burning, water immersion, missile tracking, and engine audio.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `seats` | `Seat[]` | Array of seats on this vehicle. |
| `name` | `string` | The vehicle's display name. |
| `minimapBlip` | `Texture` | The texture shown on the minimap for this vehicle. |
| `ownerTeam` | `Team` | The team that owns this vehicle. |
| `isDead` | `bool` | Whether the vehicle is destroyed. |
| `hasCountermeasures` | `bool` | Whether the vehicle has countermeasures available. |
| `canSeePlayer` | `bool` | Returns `true` if there is a line of sight between the vehicle's lock on point and the player camera. |
| `playerDistance` | `float` | The distance from this vehicle to the nearest player. |
| `playerIsInside` | `bool` | Whether a player is inside this vehicle. |
| `hasDriver` | `bool` | Whether the vehicle has a driver. |
| `driver` | `Actor` | The actor currently driving this vehicle. |
| `isTrackedByMissile` | `bool` | `true` while one or more missiles are tracking this vehicle. |
| `isBeingLocked` | `bool` | `true` while one or more target tracking weapons are locking onto this vehicle. |
| `health` | `float` | Current health. |
| `maxHealth` | `float` | Maximum health. |
| `isBurning` | `bool` | Whether the vehicle is currently burning. |
| `isFull` | `bool` | Whether all seats are occupied. |
| `isEmpty` | `bool` | Whether all seats are empty. |
| `isInWater` | `bool` | Whether the vehicle is in water. |
| `rigidbody` | `Rigidbody` | The vehicle's rigidbody component. |
| `isTurret` | `bool` | Returns `true` if vehicle is marked as a Turret. |
| `isCar` | `bool` | Returns `true` if this vehicle is a Car. If `true`, you can safely access fields via the Car class API. |
| `isBoat` | `bool` | Returns `true` if this vehicle is a Boat. If `true`, you can safely access fields via the Boat class API. |
| `isHelicopter` | `bool` | Returns `true` if this vehicle is a Helicopter. If `true`, you can safely access fields via the Helicopter class API. |
| `isAirplane` | `bool` | Returns `true` if this vehicle is an Airplane. If `true`, you can safely access fields via the Airplane class API. |
| `avoidanceRadius` | `float` | The radius of the vehicle's specified avoidance size. |
| `spotChanceMultiplier` | `float` | Multiplier for the chance this vehicle is spotted by AI. |
| `engine` | `Engine` | The vehicle's engine component. |
| `isTransportVehicle` | `bool` | Returns `true` if AIType is set to transport. |
| `vehicleInfo` | `VehicleInfo` | The vehicle's info asset. |

## Methods

### Damage

Damages the vehicle.

| Parameter | Type | Description |
|-----------|------|-------------|
| `source` | `Actor` | The actor that caused the damage. |
| `amount` | `float` | The amount of damage to deal. |

### Repair

Repairs the vehicle by the specified health amount.

| Parameter | Type | Description |
|-----------|------|-------------|
| `amount` | `float` | The amount of health to restore. |

[return: Doc]
`true` if the vehicle was healed (not already at max health).

### GetEmptySeat

Gets the first available empty seat in the vehicle.

| Parameter | Type | Description |
|-----------|------|-------------|
| `allowDriverSeat` | `bool` | Whether to allow returning the driver seat. |

### GetTrackingMissiles

Returns all missile projectiles that are currently tracking this vehicle.

### ToString

Returns a string representation of the vehicle.

## Events

| Event | Signature | Description |
|-------|-----------|-------------|
| `onClaimedBySquad` | `ScriptEvent<Squad>` | Invoked whenever a squad claims this vehicle. |
| `onClaimDropped` | `ScriptEvent<Squad>` | Invoked whenever a squad drops their claim over this vehicle. |

## Static Fields

| Field | Type | Description |
|-------|------|-------------|
| `New` | `Engine` | Creates a new Engine instance. |

## Enums

### Engine

Represents the engine of a vehicle.

| Value | Description |
|-------|-------------|
| `controlAudio` | `bool` - Whether to control engine audio. |
| `enabled` | `bool` - Whether the engine is enabled. |
| `ignitionClip` | `AudioClip` - The ignition sound clip. |
| `pitchGainSpeed` | `float` - How quickly pitch changes with speed. |
| `power` | `float` - Engine power. |
| `powerGainSpeed` | `float` - How quickly power changes. |
| `shiftForwardClip` | `AudioClip` - The shift forward sound clip. |
| `shiftReverseClip` | `AudioClip` - The shift reverse sound clip. |
| `targetPitch` | `float` - Target engine pitch. |
| `targetThrottle` | `float` - Target throttle value. |
| `throttleGainSpeed` | `float` - How quickly throttle changes. |
| `PlayIgnitionSound` | Plays the ignition sound. |
| `PlayShiftForwardSound` | Plays the shift forward sound. |
| `PlayShiftReverseSound` | Plays the shift reverse sound. |
| `Reset` | Resets the engine. |
| `ToString` | Returns a string representation of the engine. |
