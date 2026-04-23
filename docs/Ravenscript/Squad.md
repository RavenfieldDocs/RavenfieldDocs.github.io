---
title: Squad
---

Represents a squad of actors in the game world. Handles squad orders, formations, vehicle claims, landing zones, and helicopter landings.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `order` | `Order` | The current order assigned to this squad. |
| `attackTarget` | `Actor` | Squadmates will always prioritize firing at their squad's attackTarget if they are able to. Attack targets always override the current rules-of-engagement. If the attack target dies, this value will automatically be set to nil. |
| `members` | `Actor[]` | The current members of this squad. |
| `leader` | `Actor` | The current leader of this squad. |
| `hasPlayerLeader` | `bool` | Returns `true` if the squad leader is a player. |
| `squadVehicle` | `Vehicle` | The vehicle claimed by this squad. |
| `claimedLandingZone` | `HelicopterLandingZone` | The landing zone currently claimed by this squad. |
| `hasLandingZoneClaim` | `bool` | Returns `true` if this squad has a landing zone claim. |
| `isPerformingLanding` | `bool` | Returns `true` if the squad is performing a landing or has landed a helicopter. Also see `hasLanded`. |
| `hasLanded` | `bool` | Returns `true` if the squad has landed their helicopter. |
| `autoDropTransportedPassengers` | `bool` | When set to true while in transport vehicle, will automatically drop passengers when close to attack point destination. |
| `onIssueOrderMovement` | `ScriptEvent<Order>` | Invoked whenever the squad leader wants to go to the order objective. Consuming this event prevents the default squad leader movement. |

## Methods

### AssignOrder

Assigns a new order to this squad.

| Parameter | Type | Description |
|-----------|------|-------------|
| `order` | `Order` | The order to assign. |

### SetFormation

Sets the formation type for this squad.

| Parameter | Type | Description |
|-----------|------|-------------|
| `formation` | `FormationType` | The formation type to use. |

### SetRandomFormation

Set a random formation, excluding custom formation.

### SetCustomFormation

Set the formation to a specified custom formation. The formation data contains the location of each squad member, which is rotated according to the squad movement direction and scaled by the `formationWidth` and `formationHeight` values. You can safely provide a greater number of locations than the current member count, which will be automatically used if more soldiers join the squad.

| Parameter | Type | Description |
|-----------|------|-------------|
| `formation` | `Vector2[]` | The custom formation data. |

### SetFormationSize

Sets the width and depth dimensions for the squad formation.

| Parameter | Type | Description |
|-----------|------|-------------|
| `formationWidth` | `float` | The width of the formation. |
| `formationDepth` | `float` | The depth of the formation. |

### AddMember

Assign a new member to this squad.

| Parameter | Type | Description |
|-----------|------|-------------|
| `newMember` | `Actor` | The actor to add to the squad. |

### RemoveMember

Removes a member from this squad.

| Parameter | Type | Description |
|-----------|------|-------------|
| `member` | `Actor` | The actor to remove from the squad. |

### SplitSquad

Removes a number of actors from this squad. The removed actors will form their own squad. Returns the new squad.

| Parameter | Type | Description |
|-----------|------|-------------|
| `count` | `int` | The number of members to remove from the squad. |

[return: Squad]
The newly created squad.

### SplitSquad

Removes the specified actors from this squad. The removed actors will form their own squad. Returns the new squad.

| Parameter | Type | Description |
|-----------|------|-------------|
| `membersToDrop` | `Actor[]` | The actors to remove from the squad. |

[return: Squad]
The newly created squad.

### ClaimLandingZone

Claims the LZ. Any claimed landing zones will not be used by other squads.

| Parameter | Type | Description |
|-----------|------|-------------|
| `lz` | `HelicopterLandingZone` | The landing zone to claim. |

### ReleaseLandingZoneClaim

Drops the squad's current LZ claim. This is automatically done when the squad is disbanded.

### LandHelicopterAndClaimLandingZone

Lands at LZ and claims it. Any claimed landing zones will not be used by other squads.

| Parameter | Type | Description |
|-----------|------|-------------|
| `lz` | `HelicopterLandingZone` | The landing zone to land at and claim. |

### LandHelicopterAndClaimLandingZone

Lands at LZ and claims it and calls function when landing completes. Any claimed landing zones will not be used by other squads. Callback function signature: `OnLand(squad, eventData)`

| Parameter | Type | Description |
|-----------|------|-------------|
| `lz` | `HelicopterLandingZone` | The landing zone to land at and claim. |
| `onLandFunctionName` | `string` | The name of the callback function to invoke when landing completes. |

### LandHelicopterAtPosition

Lands at position.

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The position to land at. |

### LandHelicopterAtPosition

Lands at position and calls function when landing completes. Callback function signature: `OnLand(squad, eventData)`

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The position to land at. |
| `onLandFunctionName` | `string` | The name of the callback function to invoke when landing completes. |

### LandHelicopterAtPosition

Lands at position and calls function when landing completes. Callback function signature: `OnLand(squad, eventData)`

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The position to land at. |
| `onLandFunctionName` | `string` | The name of the callback function to invoke when landing completes. |
| `eventData` | `any` | Event data to pass to the callback function. |

### CancelLanding

Cancels a landing.

### TakeOff

Cancels a landing and takes off.

### DropTransportedPassengers

Drops all transported passengers. Any passengers on mounted weapons will stay in the vehicle. Returns the dropped passengers.

[return: array\<AiActorController>]
The dropped passengers.

## Static Methods

### Create

Creates a new squad with the specified actors. NOTE: The Player actor will be ignored, you can populate the player squad by adding members to `Player.squad`.

| Parameter | Type | Description |
|-----------|------|-------------|
| `actors` | `array<Actor>` | The actors to include in the new squad. |

[return: Squad]
The newly created squad.

## Enums

### FormationType

| Value | Description |
|-------|-------------|
| `Wedge` | Wedge formation. |
| `Vee` | V formation. |
| `Line` | Line formation. |
| `File` | File formation. |
| `EchelonLeft` | Left echelon formation. |
| `EchelonRight` | Right echelon formation. |
| `Diamond` | Diamond formation. |
| `Custom` | Custom formation. |
