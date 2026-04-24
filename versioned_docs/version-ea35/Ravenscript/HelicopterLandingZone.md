---
title: HelicopterLandingZone
---

Represents a helicopter landing zone in the game world. Helicopters can use these zones to land, and squads can claim them for exclusive use.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `position` | `Vector3` | The position of this landing zone. |
| `isClaimed` | `bool` | True while this landing zone is claimed. |

## Methods

### Claim

Marks this landing zone as claimed. While claimed, no other squads will try to use the helicopter landing zone.

When claiming through this function, the landing zone must be manually released through `ReleaseClaim()` when done! Alternatively you can let a squad claim through `squad.ClaimLandingZone()` which will automatically be released when the squad is disbanded.

### ReleaseClaim

Releases this landing zone's claim.

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

### GetClosestUnclaimed

Gets the closest helicopter landing zone to the target position. Does not return any claimed landing zones.

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The position to search from. |

[return: [HelicopterLandingZone](./HelicopterLandingZone.md)?]
The closest unclaimed landing zone, or nil if none is found.

## Enums
