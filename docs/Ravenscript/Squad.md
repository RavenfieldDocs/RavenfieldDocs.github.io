---
title: Squad
---

## Properties

| Name | Type | Description |
| --- | --- | --- |
| order | Order | The current order assigned to this squad. |
| attackTarget | Actor | Squadmates will always prioritize firing at their squad's attackTarget if they are able to. Attack targets always override the current rules-of-engagement. If the attack target dies, this value will automatically be set to nil. |
| members | Actor[] | The current members of this squad. |
| leader | Actor | The current leader of this squad. |
| hasPlayerLeader | bool | Returns true if the squad leader is a player. |
| squadVehicle | Vehicle | The vehicle claimed by this squad. |
| claimedLandingZone | HelicopterLandingZone | The landing zone currently claimed by this squad. |
| hasLandingZoneClaim | bool | Returns true if this squad has a landing zone claim. |
| isPerformingLanding | bool | Returns true if the squad is performing a landing or has landed a helicopter. Also see ``hasLanded``. |
| hasLanded | bool | Returns true if the squad has landed their helicopter. |
| autoDropTransportedPassengers | bool | When set to true while in transport vehicle, will automatically drop passengers when close to attack point destination. |
| onIssueOrderMovement | ScriptEvent\<Order> | Invoked whenever the squad leader wants to go to the order objective. Consume this event to prevent the default squad leader movement. |

## Methods

### AssignOrder

Assigns a new order to this squad.

| Parameter | Type | Description |
| --- | --- | --- |
| order | Order | The order to assign. |

**Returns:** void

### SetFormation

Sets the formation type for this squad.

| Parameter | Type | Description |
| --- | --- | --- |
| formation | FormationType | The formation type to use. |

**Returns:** void

### SetRandomFormation

Set a random formation, excluding custom formation.

**Returns:** void

### SetCustomFormation

Set the formation to a specified custom formation. The formation data contains the location of each squad member, which is rotated according to the squad movement direction and scaled by the ``formationWidth`` and ``formationHeight`` values. You can safely provide a greater number of locations than the current member count, which will be automatically used if more soldiers join the squad.

| Parameter | Type | Description |
| --- | --- | --- |
| formation | Vector2[] | The custom formation data. |

**Returns:** void

### SetFormationSize

Sets the width and depth dimensions for the squad formation.

| Parameter | Type | Description |
| --- | --- | --- |
| formationWidth | float | The width of the formation. |
| formationDepth | float | The depth of the formation. |

**Returns:** void

### AddMember

Assign a new member to this squad.

| Parameter | Type | Description |
| --- | --- | --- |
| newMember | Actor | The actor to add to the squad. |

**Returns:** void

### RemoveMember

Removes a member from this squad.

| Parameter | Type | Description |
| --- | --- | --- |
| member | Actor | The actor to remove from the squad. |

**Returns:** void

### SplitSquad

Removes a number of actors from this squad. The removed actors will form their own squad. Returns the new squad.

| Parameter | Type | Description |
| --- | --- | --- |
| count | int | The number of members to remove from the squad. |

**Returns:** Squad

### SplitSquad

Removes the specified actors from this squad. The removed actors will form their own squad. Returns the new squad.

| Parameter | Type | Description |
| --- | --- | --- |
| membersToDrop | Actor[] | The actors to remove from the squad. |

**Returns:** Squad

### ClaimLandingZone

Claims the LZ. Any claimed landing zones will not be used by other squads.

| Parameter | Type | Description |
| --- | --- | --- |
| lz | HelicopterLandingZone | The landing zone to claim. |

**Returns:** void

### ReleaseLandingZoneClaim

Drops the squad's current LZ claim. This is automatically done when the squad is disbanded.

**Returns:** void

### LandHelicopterAndClaimLandingZone

Lands at LZ and claims it. Any claimed landing zones will not be used by other squads.

| Parameter | Type | Description |
| --- | --- | --- |
| lz | HelicopterLandingZone | The landing zone to land at and claim. |

**Returns:** void

### LandHelicopterAndClaimLandingZone

Lands at LZ and claims it and calls function when landing completes. Any claimed landing zones will not be used by other squads. Callback function signature: ``OnLand(squad, eventData)``

| Parameter | Type | Description |
| --- | --- | --- |
| lz | HelicopterLandingZone | The landing zone to land at and claim. |
| onLandFunctionName | string | The name of the callback function to invoke when landing completes. |

**Returns:** void

### LandHelicopterAtPosition

Lands at position.

| Parameter | Type | Description |
| --- | --- | --- |
| position | Vector3 | The position to land at. |

**Returns:** void

### LandHelicopterAtPosition

Lands at position and calls function when landing completes. Callback function signature: ``OnLand(squad, eventData)``

| Parameter | Type | Description |
| --- | --- | --- |
| position | Vector3 | The position to land at. |
| onLandFunctionName | string | The name of the callback function to invoke when landing completes. |

**Returns:** void

### LandHelicopterAtPosition

Lands at position and calls function when landing completes. Callback function signature: ``OnLand(squad, eventData)``

| Parameter | Type | Description |
| --- | --- | --- |
| position | Vector3 | The position to land at. |
| onLandFunctionName | string | The name of the callback function to invoke when landing completes. |
| eventData | any | Event data to pass to the callback function. |

**Returns:** void

### CancelLanding

Cancels a landing.

**Returns:** void

### TakeOff

Cancels a landing and takes off.

**Returns:** void

### DropTransportedPassengers

Drops all transported passengers. Any passengers on mounted weapons will stay in the vehicle. Returns the dropped passengers.

**Returns:** array\<AiActorController>

## Static Methods

### Create

Creates a new squad with the specified actors. NOTE: The Player actor will be ignored, you can populate the player squad by adding members to ``Player.squad``.

| Parameter | Type | Description |
| --- | --- | --- |
| actors | array\<Actor> | The actors to include in the new squad. |

**Returns:** Squad

## Enums

### FormationType

| Value | Description |
| --- | --- |
| Wedge | Wedge formation. |
| Vee | V formation. |
| Line | Line formation. |
| File | File formation. |
| EchelonLeft | Left echelon formation. |
| EchelonRight | Right echelon formation. |
| Diamond | Diamond formation. |
| Custom | Custom formation. |
