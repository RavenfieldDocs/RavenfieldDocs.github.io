---
title: Player
---

Use these methods to get the player state.

## Properties

| Name | Type | Description |
| --- | --- | --- |
| team | Team | The player's team. |
| enemyTeam | Team | The enemy team. |
| isSpectator | bool | Returns true if the player is spectating. |
| nighvisionEnabled | bool | |
| nightvisionEnabled | bool | Returns true if night vision is enabled. |
| allowMouseLook | bool | Setting this value to false prevents the player from looking around. |
| allowAutoWaveRespawn | bool | Controls if player can auto-respawn at the next wave by pressing fire or selecting a new spawn point. |
| inputEnabled | bool | Controls if all player input is ignored. |
| movementEnabled | bool | Controls if player infantry movement is active. |
| movementInputEnabled | bool | Controls if player can control infantry/vehicle movement. |
| allowKick | bool | Controls if player can kick. |
| allowJump | bool | Controls if player can jump. |
| allowChangeStance | bool | Controls if player can change stances. |
| allowLean | bool | Controls if player can lean. |
| allowSprint | bool | Controls if player can sprint. |
| allowExitVehicle | bool | Controls if player can exit vehicles. |

## Methods

### MoveActor

Moves the first person player controller by the specified vector, respecting collisions with world geometry.

| Parameter | Type | Description |
| --- | --- | --- |
| delta | Vector3 | The movement vector. |

**Returns:** void

### ResetVelocity

Sets the velocity of the player controller to zero. Useful for stopping falls, etc.

**Returns:** void

### ResetSliding

Stops the player controller from sliding on steep geometry.

**Returns:** void

### SetFirstPersonRenderMode

Sets the player's third person actor model to only render shadows.

**Returns:** void

### SetThirdPersonRenderMode

Sets the player's third person actor model to render normally.

**Returns:** void

### SetNightvisionEnabled

Sets whether night vision is enabled.

| Parameter | Type | Description |
| --- | --- | --- |
| value | bool | Whether night vision should be enabled. |

**Returns:** void

### SetUseHelicopterAutoHoverMode

Sets whether helicopter auto-hover mode is enabled.

| Parameter | Type | Description |
| --- | --- | --- |
| enabled | bool | Whether auto-hover should be enabled. |

**Returns:** void

### SetSelectedLoadout

Sets the player's selected loadout.

| Parameter | Type | Description |
| --- | --- | --- |
| loadout | LoadoutSet | The loadout to set. |

**Returns:** void

### SetAllowAutoWaveRespawn

Controls if player can auto-respawn at the next wave by pressing fire or selecting a new spawn point.

| Parameter | Type | Description |
| --- | --- | --- |
| value | bool | Whether auto-respawn should be allowed. |

**Returns:** void

### SetInputEnabled

Controls if all player input is ignored.

| Parameter | Type | Description |
| --- | --- | --- |
| value | bool | Whether input should be enabled. |

**Returns:** void

### SetMovementEnabled

Controls if player infantry movement is active.

| Parameter | Type | Description |
| --- | --- | --- |
| value | bool | Whether movement should be enabled. |

**Returns:** void

### SetMovementInputEnabled

Controls if player can control infantry/vehicle movement.

| Parameter | Type | Description |
| --- | --- | --- |
| value | bool | Whether movement input should be enabled. |

**Returns:** void

### SetAllowKick

Controls if player can kick.

| Parameter | Type | Description |
| --- | --- | --- |
| value | bool | Whether kicking should be allowed. |

**Returns:** void

### SetAllowJump

Controls if player can jump.

| Parameter | Type | Description |
| --- | --- | --- |
| value | bool | Whether jumping should be allowed. |

**Returns:** void

### SetAllowChangeStance

Controls if player can change stances.

| Parameter | Type | Description |
| --- | --- | --- |
| value | bool | Whether changing stance should be allowed. |

**Returns:** void

### SetAllowLean

Controls if player can lean.

| Parameter | Type | Description |
| --- | --- | --- |
| value | bool | Whether leaning should be allowed. |

**Returns:** void

### SetAllowSprint

Controls if player can sprint.

| Parameter | Type | Description |
| --- | --- | --- |
| value | bool | Whether sprinting should be allowed. |

**Returns:** void

### SetAllowExitVehicle

Controls if player can exit vehicles.

| Parameter | Type | Description |
| --- | --- | --- |
| value | bool | Whether exiting vehicles should be allowed. |

**Returns:** void

## Static Methods

### GetTeam

Returns the player's team.

**Returns:** Team

### GetEnemyTeam

Returns the enemy team.

**Returns:** Team

### GetIsSpectator

Returns true if the player is spectating.

**Returns:** bool

### GetNighvisionEnabled

Returns true if night vision is enabled.

**Returns:** bool

### GetNightvisionEnabled

Returns true if night vision is enabled.

**Returns:** bool

### GetAllowMouseLook

Returns whether mouse look is allowed.

**Returns:** bool

### GetSquad

Get the player squad.

**Returns:** Squad

### GetActor

Get the player actor. This is the same as using ``ActorManager.playerActor``.

**Returns:** Actor

### GetActorIsGrounded

Returns true if the player character controller is on the ground.

**Returns:** bool

### GetUseHelicopterAutoHoverMode

Returns whether helicopter auto-hover mode is enabled.

**Returns:** bool

### GetSelectedLoadout

Returns the player's currently selected loadout.

**Returns:** LoadoutSet

### GetAllowAutoWaveRespawn

Returns whether auto-respawn at the next wave is allowed.

**Returns:** bool

### GetInputEnabled

Returns whether player input is enabled.

**Returns:** bool

### GetMovementEnabled

Returns whether player infantry movement is active.

**Returns:** bool

### GetMovementInputEnabled

Returns whether player can control infantry/vehicle movement.

**Returns:** bool

### GetAllowKick

Returns whether kicking is allowed.

**Returns:** bool

### GetAllowJump

Returns whether jumping is allowed.

**Returns:** bool

### GetAllowChangeStance

Returns whether changing stances is allowed.

**Returns:** bool

### GetAllowLean

Returns whether leaning is allowed.

**Returns:** bool

### GetAllowSprint

Returns whether sprinting is allowed.

**Returns:** bool

### GetAllowExitVehicle

Returns whether exiting vehicles is allowed.

**Returns:** bool
