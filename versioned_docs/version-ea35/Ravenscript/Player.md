---
title: Player
---

Use these methods to get the player state.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `team` | [Team](./Team.md) | The player's team. |
| `enemyTeam` | [Team](./Team.md) | The enemy team. |
| `isSpectator` | `bool` | Returns `true` if the player is spectating. |
| `nightvisionEnabled` | `bool` | Returns `true` if night vision is enabled. |
| `allowMouseLook` | `bool` | Setting this value to `false` prevents the player from looking around. |
| `allowAutoWaveRespawn` | `bool` | Controls if player can auto-respawn at the next wave by pressing fire or selecting a new spawn point. |
| `inputEnabled` | `bool` | Controls if all player input is ignored. |
| `movementEnabled` | `bool` | Controls if player infantry movement is active. |
| `movementInputEnabled` | `bool` | Controls if player can control infantry/vehicle movement. |
| `allowKick` | `bool` | Controls if player can kick. |
| `allowJump` | `bool` | Controls if player can jump. |
| `allowChangeStance` | `bool` | Controls if player can change stances. |
| `allowLean` | `bool` | Controls if player can lean. |
| `allowSprint` | `bool` | Controls if player can sprint. |
| `allowExitVehicle` | `bool` | Controls if player can exit vehicles. |

## Methods

### MoveActor

Moves the first person player controller by the specified vector, respecting collisions with world geometry.

| Parameter | Type | Description |
|-----------|------|-------------|
| `delta` | `Vector3` | The movement vector. |

### ResetVelocity

Sets the velocity of the player controller to zero. Useful for stopping falls, etc.

### ResetSliding

Stops the player controller from sliding on steep geometry.

### SetFirstPersonRenderMode

Sets the player's third person actor model to only render shadows.

### SetThirdPersonRenderMode

Sets the player's third person actor model to render normally.

### SetNightvisionEnabled

Sets whether night vision is enabled.

| Parameter | Type | Description |
|-----------|------|-------------|
| `value` | `bool` | Whether night vision should be enabled. |

### SetUseHelicopterAutoHoverMode

Sets whether helicopter auto-hover mode is enabled.

| Parameter | Type | Description |
|-----------|------|-------------|
| `enabled` | `bool` | Whether auto-hover should be enabled. |

### SetSelectedLoadout

Sets the player's selected loadout.

| Parameter | Type | Description |
|-----------|------|-------------|
| `loadout` | [LoadoutSet](./LoadoutSet.md) | The loadout to set. |

### SetAllowAutoWaveRespawn

Controls if player can auto-respawn at the next wave by pressing fire or selecting a new spawn point.

| Parameter | Type | Description |
|-----------|------|-------------|
| `value` | `bool` | Whether auto-respawn should be allowed. |

### SetInputEnabled

Controls if all player input is ignored.

| Parameter | Type | Description |
|-----------|------|-------------|
| `value` | `bool` | Whether input should be enabled. |

### SetMovementEnabled

Controls if player infantry movement is active.

| Parameter | Type | Description |
|-----------|------|-------------|
| `value` | `bool` | Whether movement should be enabled. |

### SetMovementInputEnabled

Controls if player can control infantry/vehicle movement.

| Parameter | Type | Description |
|-----------|------|-------------|
| `value` | `bool` | Whether movement input should be enabled. |

### SetAllowKick

Controls if player can kick.

| Parameter | Type | Description |
|-----------|------|-------------|
| `value` | `bool` | Whether kicking should be allowed. |

### SetAllowJump

Controls if player can jump.

| Parameter | Type | Description |
|-----------|------|-------------|
| `value` | `bool` | Whether jumping should be allowed. |

### SetAllowChangeStance

Controls if player can change stances.

| Parameter | Type | Description |
|-----------|------|-------------|
| `value` | `bool` | Whether changing stance should be allowed. |

### SetAllowLean

Controls if player can lean.

| Parameter | Type | Description |
|-----------|------|-------------|
| `value` | `bool` | Whether leaning should be allowed. |

### SetAllowSprint

Controls if player can sprint.

| Parameter | Type | Description |
|-----------|------|-------------|
| `value` | `bool` | Whether sprinting should be allowed. |

### SetAllowExitVehicle

Controls if player can exit vehicles.

| Parameter | Type | Description |
|-----------|------|-------------|
| `value` | `bool` | Whether exiting vehicles should be allowed. |

### GetTeam

Returns the player's team.

[return: [Team](./Team.md)]
`Team`

### GetEnemyTeam

Returns the enemy team.

[return: [Team](./Team.md)]
`Team`

### GetIsSpectator

Returns `true` if the player is spectating.

[return: bool]
`bool`

### GetNighvisionEnabled

Returns `true` if night vision is enabled.

[return: bool]
`bool`

### GetNightvisionEnabled

Returns `true` if night vision is enabled.

[return: bool]
`bool`

### GetAllowMouseLook

Returns whether mouse look is allowed.

[return: bool]
`bool`

### GetSquad

Get the player squad.

[return: [Squad](./Squad.md)]
`Squad`

### GetActor

Get the player actor. This is the same as using `ActorManager.playerActor`.

[return: [Actor](./Actor.md)]
`Actor`

### GetActorIsGrounded

Returns `true` if the player character controller is on the ground.

[return: bool]
`bool`

### GetUseHelicopterAutoHoverMode

Returns whether helicopter auto-hover mode is enabled.

[return: bool]
`bool`

### GetSelectedLoadout

Returns the player's currently selected loadout.

[return: [LoadoutSet](./LoadoutSet.md)]
`LoadoutSet`

### GetAllowAutoWaveRespawn

Returns whether auto-respawn at the next wave is allowed.

[return: bool]
`bool`

### GetInputEnabled

Returns whether player input is enabled.

[return: bool]
`bool`

### GetMovementEnabled

Returns whether player infantry movement is active.

[return: bool]
`bool`

### GetMovementInputEnabled

Returns whether player can control infantry/vehicle movement.

[return: bool]
`bool`

### GetAllowKick

Returns whether kicking is allowed.

[return: bool]
`bool`

### GetAllowJump

Returns whether jumping is allowed.

[return: bool]
`bool`

### GetAllowChangeStance

Returns whether changing stances is allowed.

[return: bool]
`bool`

### GetAllowLean

Returns whether leaning is allowed.

[return: bool]
`bool`

### GetAllowSprint

Returns whether sprinting is allowed.

[return: bool]
`bool`

### GetAllowExitVehicle

Returns whether exiting vehicles is allowed.

[return: bool]
`bool`
