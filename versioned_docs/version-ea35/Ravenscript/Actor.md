---
title: Actor
---

Represents a soldier or actor in the game world. Handles movement, weapons, ragdoll physics, vehicles, ladders, parachutes, and damage.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `isFrozenGlobal` | `bool` | Returns `true` if the actor is frozen or if global gameplay is frozen. |
| `name` | `string` | The actor's display name. Updates the scoreboard entry when set. |
| `controller` | `ActorController` | The controller that handles input and AI for this actor. |
| `ragdoll` | `ActiveRaggy` | The ragdoll system for this actor. |
| `animator` | `Animator` | The Unity Animator component. |
| `autoMoveActor` | `bool` | Whether this actor is automatically moved by the physics system. |
| `hipRigidbody` | `Rigidbody` | The hip rigidbody of the ragdoll. |
| `headRigidbody` | `Rigidbody` | The head rigidbody of the ragdoll. |
| `parachuteParent` | [Transform](./Transform.md) | The transform that the parachute is parented to. |
| `parachuteAnimation` | `Animation` | The parachute animation component. |
| `parachuteRenderer` | `MeshRenderer` | The parachute renderer. |
| `closestEnemyDistancePreShift` | `float` | Used for tracking enemy distance before a shift. |
| `closestEnemyDistance` | `float` | The distance to the closest enemy. |
| `actorIndex` | `int` | The index of this actor in the actor manager. |
| `teamActorIndex` | `int` | The index of this actor within its team. |
| `accessoryRenderer` | `Renderer[]` | Renderers for accessories on the animated model. |
| `accessoryRagdollRenderer` | `Renderer[]` | Renderers for accessories on the ragdoll model. |
| `deathTimestamp` | `float` | The game time when this actor died. |
| `health` | `float` | Current health (default 100). |
| `maxHealth` | `float` | Maximum health (default 100). |
| `balance` | `float` | Current balance (default 100). Falls over when it reaches 0. |
| `maxBalance` | `float` | Maximum balance (default 100). |
| `dead` | `bool` | Whether the actor is dead. |
| `fallenOver` | `bool` | Whether the actor has fallen over (ragdolled but can get up). |
| `makesProximityMovementNoise` | `bool` | Whether the actor makes noise that can alert nearby AI. |
| `wantsToGetUp` | `bool` | Whether the actor wants to get up from a fallen state. |
| `fallAction` | `TimedAction` | Tracks the ragdoll fall duration. |
| `stopFallAction` | `TimedAction` | Tracks cooldown after falling stops. |
| `getupAction` | `TimedAction` | Tracks the get-up animation progress. |
| `immersedInWater` | `bool` | Whether the actor is fully immersed in water. |
| `feetAreInWater` | `bool` | Whether the actor's feet are in water. |
| `waterDepth` | `float` | The depth of water at the actor's position. |
| `waterHeight` | `float` | The Y position of the water surface. |
| `parachuteDeployed` | `bool` | Whether the parachute is currently deployed. |
| `canDeployParachute` | `bool` | Whether the actor is allowed to deploy a parachute. |
| `isFallingAsRagdoll` | `bool` | Whether the actor is currently falling as a ragdoll. |
| `stance` | `Actor.Stance` | Current stance: Stand, Crouch, or Prone. |
| `moving` | `bool` | Whether the actor is currently moving. |
| `isFrozen` | `bool` | Whether the actor is frozen (animation and input disabled). |
| `isRendered` | `bool` | Whether the actor is currently rendered. |
| `isDeactivated` | `bool` | Whether the actor is deactivated (hidden, frozen, colliders disabled). |
| `isIgnored` | `bool` | Whether the actor is ignored by AI detection. |
| `visibilityDistanceModifier` | `float` | Modifies the distance at which this actor can be seen. |
| `attackersIgnoreEngagementRules` | `bool` | Whether attackers ignore normal engagement rules for this actor. |
| `movementSpeedMultiplier` | `float` | Multiplier for movement speed (default 1). |
| `ladder` | [Ladder](./Ladder.md) | The ladder the actor is currently on, or `nil`. |
| `ladderHeight` | `float` | Current height on the ladder. |
| `activeWeapon` | [Weapon](./Weapon.md) | The currently unholstered weapon, or `nil`. |
| `weapons` | [Weapon](./Weapon.md)[] | Array of 5 weapons in loadout slots. |
| `activeWeaponSlot` | `int` | Index of the currently active weapon slot (0-4). |
| `hasAmmoBox` | `bool` | Whether the actor has an ammo box in their loadout. |
| `ammoBoxSlot` | `int` | The slot index of the ammo box. |
| `hasMedipack` | `bool` | Whether the actor has a medipack in their loadout. |
| `medipackSlot` | `int` | The slot index of the medipack. |
| `hasRepairTool` | `bool` | Whether the actor has a repair tool in their loadout. |
| `repairToolSlot` | `int` | The slot index of the repair tool. |
| `hasSmokeScreen` | `bool` | Whether the actor has a smoke screen in their loadout. |
| `smokeScreenSlot` | `int` | The slot index of the smoke screen. |
| `aiControlled` | `bool` | Whether this actor is controlled by AI. |
| `needsResupply` | `bool` | Whether the actor needs resupply (ammo low). |
| `seat` | [Seat](./Seat.md) | The seat the actor is currently occupying, or `nil`. |
| `skinnedRenderer` | `SkinnedMeshRenderer` | The skinned mesh renderer for the animated model. |
| `skinnedRendererRagdoll` | `SkinnedMeshRenderer` | The skinned mesh renderer for the ragdoll model. |
| `weaponImposterRenderers` | `Dictionary<Weapon, Renderer[]>` | Maps weapons to their imposter renderer arrays. |
| `distanceCull` | `bool` | Whether this actor is distance-culled. |
| `dropsAmmoOnKick` | `bool` | Whether the actor drops an ammo reserve when kicked (default true). |
| `hasSpawnedAmmoReserve` | `bool` | Whether the ammo reserve has already been spawned. |
| `isInvulnerable` | `bool` | Whether the actor is invulnerable to damage. |
| `isScheduledToSpawn` | `bool` | Whether the actor is scheduled to spawn. |
| `rigidbody` | `Rigidbody` | The main rigidbody component. |
| `overrideActorSkin` | [ActorSkin](./ActorSkin.md) | Override skin for this actor. |
| `scoreboardEntry` | `ScoreboardActorEntry` | The scoreboard entry for this actor. |
| `muteFootsteps` | `bool` | Whether footsteps are muted. |
| `speedMultiplier` | `float` | Multiplier for movement speed (default 1). |
| `hasHeroArmor` | `bool` | Whether the actor has hero armor that absorbs damage. |
| `animatedBones` | [Transform](./Transform.md)[] | Bone transforms of the animated skeleton. |
| `ragdollBones` | [Transform](./Transform.md)[] | Bone transforms of the ragdoll skeleton. |
| `movingPlatformDelta` | `Vector3` | Movement delta from moving platforms. |
| `ragdollExceedsFallingSpeed` | `bool` | Whether the ragdoll velocity exceeds the falling speed threshold. |

## Methods

### SpawnAt

Spawns the actor at the specified position and rotation with an optional forced loadout.

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The spawn position. |
| `rotation` | `Quaternion` | The spawn rotation. |
| `forcedLoadout` | `WeaponManager.LoadoutSet` | Optional forced loadout. If nil, uses the game mode's default. |

### Kill

Kills the actor with the given damage info.

| Parameter | Type | Description |
|-----------|------|-------------|
| `info` | [DamageInfo](./DamageInfo.md) | The damage info that caused the death. |

### KillSilently

Kills the actor silently without triggering death effects or scoreboard updates.

### IsAiming

Returns whether the actor is currently aiming their weapon.

### ForceStance

Forces the actor into a specific stance.

| Parameter | Type | Description |
|-----------|------|-------------|
| `stance` | `Actor.Stance` | The stance to force (Stand, Crouch, or Prone). |

### CanBeSeen

Returns whether the actor can be seen by an observer.

| Parameter | Type | Description |
|-----------|------|-------------|
| `viewerIsAlerted` | `bool` | Whether the viewer is in an alerted state. |

### ToStringRichText

Returns a rich-text colored representation of the actor based on their team.

### CanSpawnAmmoReserve

Returns whether the actor can spawn an ammo reserve.

### CanEmote

Returns whether the actor can perform an emote.

### EmoteChat

Plays the chat/talk emote animation.

### EmoteSwing

Plays the melee swing emote animation.

### EmoteThrow

Plays the throw emote animation.

### EmoteToss

Plays the toss emote animation.

### EmoteHail

Plays the hail emote animation.

### EmoteRegroup

Plays the regroup emote animation.

### EmoteMove

Plays the move forward emote animation.

### EmoteHalt

Plays the halt emote animation.

### IsSwimming

Returns whether the actor is currently swimming.

### SetIdleType

Sets the idle animation type.

| Parameter | Type | Description |
|-----------|------|-------------|
| `idleType` | `Actor.IdleAnimation` | The idle animation type (Stand or Talk). |

### GetupProgress

Returns the progress of the get-up animation (0 to 1). Returns 0 if still ragdolled.

### JustChangedProneStance

Returns whether the actor just changed to or from prone stance.

### WasRecentlyInWater

Returns whether the actor was recently in water.

### KnockOver

Knocks the actor over with a force.

| Parameter | Type | Description |
|-----------|------|-------------|
| `force` | `Vector3` | The force to apply. |

### ApplyRigidbodyForce

Applies an impulse force to the ragdoll's main rigidbody.

| Parameter | Type | Description |
|-----------|------|-------------|
| `force` | `Vector3` | The force to apply. |

### FallOver

Makes the actor fall over and enter ragdoll mode.

### InstantGetUp

Instantly gets the actor up from a fallen state.

### InstantGetUpAtPosition

Instantly gets the actor up at a specific position.

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The position to get up at. |

### IsReadyToSpawn

Returns whether the actor is ready to be spawned (dead and not deactivated or scheduled).

### OnGotKill

Called when this actor gets a kill.

| Parameter | Type | Description |
|-----------|------|-------------|
| `target` | [Actor](./Actor.md) | The actor that was killed. |

### OnGotVehicleKill

Called when this actor destroys a vehicle.

| Parameter | Type | Description |
|-----------|------|-------------|
| `disabled` | `bool` | Whether the vehicle was disabled (true) or destroyed (false). |
| `vehicle` | [Vehicle](./Vehicle.md) | The vehicle that was destroyed. |

### OnGotFlagCapture

Called when this actor captures a flag.

### DeployParachute

Deploys the actor's parachute.

### CutParachutes

Cuts the deployed parachute.

### Position

Returns the cached position of the actor.

### CenterPosition

Returns the center (spine) position of the actor.

### Velocity

Returns the cached velocity of the actor.

### GetBonusSprintAmount

Returns the bonus sprint speed multiplier (0 to 1).

### Damage

Applies damage to the actor.

| Parameter | Type | Description |
|-----------|------|-------------|
| `info` | [DamageInfo](./DamageInfo.md) | The damage info. |

[return: bool]
`true` if damage was applied, `false` if the actor was invulnerable or already dead.

### OnBalanceSetManually

Called when balance is set manually. Causes fall over if balance is below 0.

### SetHealth

Sets the actor's health directly.

| Parameter | Type | Description |
|-----------|------|-------------|
| `health` | `float` | The new health value. |

### OnWeaponShoot

Called when the actor's weapon shoots.

### ApplyRecoil

Applies recoil impulse to the actor.

| Parameter | Type | Description |
|-----------|------|-------------|
| `impulse` | `Vector3` | The recoil impulse. |

### WeaponMuzzlePosition

Returns the position of the active weapon's current muzzle.

### ForceApplyAnimatorForTime

Forces the animator to run for a specified time (AI only).

| Parameter | Type | Description |
|-----------|------|-------------|
| `time` | `float` | Duration in seconds. |

### HolsterActiveWeapon

Holsters the currently active weapon.

### DropWeapon

Drops the weapon in the specified slot.

| Parameter | Type | Description |
|-----------|------|-------------|
| `slot` | `int` | The weapon slot (0-4). |

### HasWeaponInSlot

Returns whether there is a weapon in the specified slot.

| Parameter | Type | Description |
|-----------|------|-------------|
| `i` | `int` | The slot index (0-4). |

### HasUnholsteredWeapon

Returns whether the actor has an unholstered weapon.

### Highlight

Highlights the actor for a duration (visible on minimap and through walls).

| Parameter | Type | Description |
|-----------|------|-------------|
| `time` | `float` | Duration in seconds (default 4). |

### IsHighlighted

Returns whether the actor is currently highlighted.

### MarkHighPriorityTarget

Marks the actor as a high priority target for AI.

| Parameter | Type | Description |
|-----------|------|-------------|
| `duration` | `float` | Duration in seconds. |

### IsHighPriorityTarget

Returns whether the actor is marked as a high priority target.

### IsInBurningVehicle

Returns whether the actor is seated in a burning vehicle.

### IsSeatedInVehicle

Returns whether the actor is seated in a specific vehicle.

| Parameter | Type | Description |
|-----------|------|-------------|
| `vehicle` | [Vehicle](./Vehicle.md) | The vehicle to check. |

### IsSeated

Returns whether the actor is seated in any seat.

### IsPassenger

Returns whether the actor is a passenger (seated but not driving).

### IsDriver

Returns whether the actor is driving a vehicle.

### CanEnterSeat

Returns whether the actor can enter a vehicle seat.

### EnterVehicle

Attempts to enter a vehicle. Returns `true` if successful.

| Parameter | Type | Description |
|-----------|------|-------------|
| `vehicle` | [Vehicle](./Vehicle.md) | The vehicle to enter. |

### EnterSeat

Enters a specific seat, optionally kicking out the current occupant.

| Parameter | Type | Description |
|-----------|------|-------------|
| `seat` | [Seat](./Seat.md) | The seat to enter. |
| `kickOutOccupant` | `bool` | Whether to kick out the current occupant. |

### LeaveSeat

Leaves the current seat.

| Parameter | Type | Description |
|-----------|------|-------------|
| `forcedByFallingOver` | `bool` | Whether the leave was forced by falling over. |

### NextWeapon

Switches to the next available weapon.

### PreviousWeapon

Switches to the previous available weapon.

### SwitchWeapon

Switches to the weapon in the specified slot.

| Parameter | Type | Description |
|-----------|------|-------------|
| `slot` | `int` | The weapon slot (0-4). |

### SwitchSeat

Switches to a different seat in the current vehicle.

| Parameter | Type | Description |
|-----------|------|-------------|
| `seatIndex` | `int` | The index of the seat to switch to. |
| `swapIfOccupied` | `bool` | Whether to swap with the occupant if the seat is occupied. |

### Hurt

Plays a hurt animation.

| Parameter | Type | Description |
|-----------|------|-------------|
| `x` | `float` | Horizontal direction of the hurt (-2 to 2). |

### OnJoinPlayerSquad

Called when the actor joins a player's squad.

### OnDroppedFromSquad

Called when the actor is dropped from a player's squad.

### SetTeam

Sets the actor's team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `int` | The team index. |

### AmmoChanged

Called when the actor's ammo count changes.

### MarkAtResupplyCrate

Marks the actor as having been at a resupply crate.

### ResupplyAmmo

Resupplies the actor's ammo. Returns `true` if ammo was resupplied.

### ResupplyHealth

Resupplies the actor's health. Returns `true` if health was restored.

### CanCapturePoint

Returns whether the actor can capture a capture point.

### ResetWeaponInputs

Resets weapon inputs (stops firing).

### ForceStopAnimatorMovement

Stops the animator movement.

### Freeze

Freezes the actor (stops animation and resets weapon inputs).

### Unfreeze

Unfreezes the actor.

### HitboxCollidersAreEnabled

Returns whether the hitbox colliders are enabled.

### DisableHitboxColliders

Disables the hitbox colliders. Returns `true` if they were enabled.

### EnableHitboxColliders

Enables the hitbox colliders.

### Deactivate

Deactivates the actor (hides, freezes, disables colliders).

### Activate

Activates the actor (shows, unfreezes, enables colliders).

### SetPositionAndRotation

Sets the actor's position and rotation.

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The new position. |
| `rotation` | `Quaternion` | The new rotation. |

### Hide

Hides the actor's renderers.

### Show

Shows the actor's renderers.

### GetTargetType

Returns the actor's target type for AI targeting.

### CanBeDamagedBy

Returns whether the actor can be damaged by a specific weapon.

| Parameter | Type | Description |
|-----------|------|-------------|
| `weapon` | [Weapon](./Weapon.md) | The weapon to check. |

### SetModelSkin

Sets an override skin for the actor.

| Parameter | Type | Description |
|-----------|------|-------------|
| `skin` | [ActorSkin](./ActorSkin.md) | The skin to apply. |

### ResetModelSkin

Resets the actor's skin to the global team skin.

### AddAccessory

Adds an accessory to the actor.

| Parameter | Type | Description |
|-----------|------|-------------|
| `accessory` | `ActorAccessory` | The accessory to add. |

### RemoveAccessories

Removes all accessories from the actor.

### SetImposterShadowMode

Sets the shadow casting mode for weapon imposter renderers.

| Parameter | Type | Description |
|-----------|------|-------------|
| `mode` | `ShadowCastingMode` | The shadow casting mode. |

### SetImposterRenderingEnabled

Enables or disables weapon imposter rendering.

| Parameter | Type | Description |
|-----------|------|-------------|
| `enabled` | `bool` | Whether to enable imposter rendering. |

### GetOnLadder

Gets the actor onto a ladder at the projected height.

| Parameter | Type | Description |
|-----------|------|-------------|
| `ladder` | [Ladder](./Ladder.md) | The ladder to get on. |

### GetOnLadderAtHeight

Gets the actor onto a ladder at a specific height.

| Parameter | Type | Description |
|-----------|------|-------------|
| `ladder` | [Ladder](./Ladder.md) | The ladder to get on. |
| `height` | `float` | The height on the ladder. |

### CanExitLadderAtBottom

Returns whether the actor can exit the ladder at the bottom.

### CanExitLadderAtTop

Returns whether the actor can exit the ladder at the top.

### ExitLadder

Exits the ladder.

| Parameter | Type | Description |
|-----------|------|-------------|
| `forceOff` | `bool` | Whether to force exit even if not at top or bottom. |

### GetTargetSize

Returns the target size (from the vehicle if seated, 0 otherwise).

### IsOnLadder

Returns whether the actor is on a ladder.

### GetFocusType

Returns the AI focus type for this actor.

### HeroArmorIgnoresDamage

Returns whether hero armor is currently ignoring damage.

### GetIsResupplyingAmmo

Returns whether the actor is currently resupplying ammo.

### GetIsResupplyingHealth

Returns whether the actor is currently resupplying health.

### GetIsAtResupplyCrate

Returns whether the actor is at a resupply crate.

### GetCurrentCapturePoint

Returns the capture point the actor is currently at.

### CanBeRammedBy

Returns whether the actor can be rammed by a vehicle.

| Parameter | Type | Description |
|-----------|------|-------------|
| `vehicle` | [Vehicle](./Vehicle.md) | The vehicle to check. |

### GetPosition

Returns the cached position of the actor.

### InstantlyReloadCarriedWeapons

Instantly reloads all weapons in the actor's loadout.

## Events

| Event | Signature | Description |
|-------|-----------|-------------|
| `onTakeDamage` | `(actor, source, info)` | Invoked when an actor takes damage. Consuming this event prevents the damage. |

## Static Fields

| Field | Type | Description |
|-------|------|-------------|
| `ANIM_PAR_RESET` | `int` | Animator hash for "reset". |
| `ANIM_PAR_RAGDOLLED` | `int` | Animator hash for "ragdolled". |
| `ANIM_PAR_FALLING` | `int` | Animator hash for "falling". |
| `ANIM_PAR_ON_BACK` | `int` | Animator hash for "onBack". |
| `ANIM_PAR_MOVING` | `int` | Animator hash for "moving". |
| `ANIM_PAR_MOVEMENT_X` | `int` | Animator hash for "movement x". |
| `ANIM_PAR_MOVEMENT_Y` | `int` | Animator hash for "movement y". |
| `ANIM_PAR_DEAD` | `int` | Animator hash for "dead". |
| `ANIM_PAR_SEATED` | `int` | Animator hash for "seated". |
| `ANIM_PAR_LEAN` | `int` | Animator hash for "lean". |
| `ANIM_PAR_HAIL` | `int` | Animator hash for "hail". |
| `ANIM_PAR_REGROUP` | `int` | Animator hash for "regroup". |
| `ANIM_PAR_MOVE` | `int` | Animator hash for "move". |
| `ANIM_PAR_HALT` | `int` | Animator hash for "halt". |
| `ANIM_PAR_HURT` | `int` | Animator hash for "hurt". |
| `ANIM_PAR_HURT_X` | `int` | Animator hash for "hurt x". |
| `ANIM_PAR_CROUCHED` | `int` | Animator hash for "crouched". |
| `ANIM_PAR_PRONE` | `int` | Animator hash for "prone". |
| `ANIM_PAR_SWIM` | `int` | Animator hash for "swim". |
| `ANIM_PAR_SWIM_FORWARD` | `int` | Animator hash for "swim forward". |
| `ANIM_PAR_SPRINTING` | `int` | Animator hash for "sprinting". |
| `ANIM_PAR_SEATED_TYPE` | `int` | Animator hash for "seated type". |
| `ANIM_PAR_POSE_TYPE` | `int` | Animator hash for "pose type". |
| `ANIM_PAR_IDLE` | `int` | Animator hash for "idle". |
| `ANIM_PAR_MELEE` | `int` | Animator hash for "melee". |
| `ANIM_PAR_CHAT` | `int` | Animator hash for "chat". |
| `ANIM_PAR_RELOADING` | `int` | Animator hash for "reloading". |
| `ANIM_PAR_SEATED_DIRECTION` | `int` | Animator hash for "seated direction". |
| `ANIM_PAR_CLIMBING` | `int` | Animator hash for "climbing". |
| `ANIM_PAR_LADDER_Y` | `int` | Animator hash for "ladder y". |
| `ANIM_PAR_PARACHUTE` | `int` | Animator hash for "parachute". |
| `ANIM_PAR_CLIMB_OBSTACLE` | `int` | Animator hash for "climb obstacle". |
| `ANIM_PAR_UNHOLSTER` | `int` | Animator hash for "unholster". |
| `ANIM_PAR_UNARMED` | `int` | Animator hash for "unarmed". |
| `ANIM_PAR_RANDOM` | `int` | Animator hash for "random". |
| `ANIM_PAR_IDLE_TYPE` | `int` | Animator hash for "idle type". |
| `ANIM_PAR_THROW` | `int` | Animator hash for "throw". |
| `ANIM_PAR_TOSS` | `int` | Animator hash for "toss". |

## Enums

### Stance

| Value | Description |
|-------|-------------|
| `Stand` | Standing stance. |
| `Crouch` | Crouching stance. |
| `Prone` | Prone stance. |

### IdleAnimation

| Value | Description |
|-------|-------------|
| `Stand` | Standard idle animation. |
| `Talk` | Talking idle animation. |

### TargetType

| Value | Description |
|-------|-------------|
| `Infantry` | Individual infantry soldier. |
| `InfantryGroup` | Group of infantry soldiers. |
| `Unarmored` | Unarmored vehicle. |
| `Armored` | Armored vehicle. |
| `Air` | Aircraft. |
| `AirFastMover` | Fast-moving aircraft. |
