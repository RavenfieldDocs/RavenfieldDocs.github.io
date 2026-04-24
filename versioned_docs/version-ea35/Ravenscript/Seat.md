---
title: Seat
---

Represents a seat on a vehicle that can be occupied by an actor.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `vehicle` | [Vehicle](./Vehicle.md) | The vehicle this seat belongs to. |
| `occupant` | [Actor](./Actor.md) | The actor currently occupying this seat, or `nil`. |
| `isDriverSeat` | `bool` | Whether this is the driver seat (first seat on the vehicle). |
| `isOccupied` | `bool` | Whether this seat is currently occupied. |
| `hasWeapons` | `bool` | Whether this seat has any mounted weapons. |
| `hasActiveWeapon` | `bool` | Whether this seat has an active mounted weapon. |
| `activeWeapon` | [MountedWeapon](./MountedWeapon.md) | The currently active mounted weapon, or `nil`. |
| `weapons` | [MountedWeapon](./MountedWeapon.md)[] | Array of all mounted weapons on this seat. |
| `cameraType` | `SeatCameraType` | The camera type for this seat. |
| `firstPersonCamera` | `Camera` | The first person camera for this seat. |
| `thirdPersonCamera` | `Camera` | The third person camera for this seat. |
| `isEnclosed` | `bool` | Whether this seat is enclosed (like inside a car). |

## Methods

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

## Enums

### SeatCameraType

| Value | Description |
|-------|-------------|
| `FreelookUnarmed` | Camera allows freelook but no weapons. |
| `LockedAllowFreelookUnarmed` | Camera is locked to vehicle direction but allows freelook when unarmed. |
| `AlwaysLockedUnarmed` | Camera is always locked, no freelook. |
| `FreelookArmed` | Camera allows freelook and weapons can be used. |

### SitAnimation

| Value | Description |
|-------|-------------|
| `Chair` | Sitting in a chair pose. |
| `Quad` | Sitting pose for quad bikes. |
| `Standing` | Standing pose. |
| `ChairRelaxed` | Relaxed chair sitting pose. |

### SoundMuffle

| Value | Description |
|-------|-------------|
| `Auto` | Automatically determine if sound should be muffled. |
| `On` | Sound is muffled. |
| `Off` | Sound is not muffled. |
