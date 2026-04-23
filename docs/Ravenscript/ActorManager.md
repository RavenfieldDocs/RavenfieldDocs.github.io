---
title: ActorManager
---

Manages all actors, vehicles, spawn points, squads, ladders, damage zones, and trigger volumes in the game world.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `isInitialized` | `bool` | Whether the actor manager has been initialized for the current game. |
| `vehicles` | [Vehicle](./Vehicle.md)[] | All vehicles currently in the game. |
| `spawnPoints` | [SpawnPoint](./SpawnPoint.md)[] | All spawn points in the current level. |
| `actors` | [Actor](./Actor.md)[] | All actors currently in the game. |
| `player` | [Actor](./Actor.md) | The player-controlled actor. |
| `actorData` | `ActorData[]` | Data associated with each actor. |
| `squadsOnTeam` | [Squad](./Squad.md)[][] | Squads organized by team (index 0 or 1). |
| `ladders` | `Ladder[]` | All ladders in the current level. |
| `damageZones` | `DamageZone[]` | All damage zones in the current level. |
| `speedLimitZones` | `SpeedLimitZone[]` | All speed limit zones in the current level. |
| `activeTriggers` | `TriggerVolume.RuntimeData[]` | Active trigger volumes. |
| `triggerStates` | `TriggerVolumeActorState[]` | States for active trigger volumes. |
| `actorCanHearEnemy` | `bool[]` | Whether each actor can hear enemy actors. |
| `bloodParticleLifetime` | `float` | Lifetime of blood particles in seconds. |
| `bloodParticleSpeedMultiplier` | `float` | Speed multiplier for blood particles. |
| `bloodParticleVerticalLaunchSpeed` | `float` | Vertical launch speed for blood particles. |
| `bloodParticleSize` | `float` | Size multiplier for blood particles. |
| `vehicleParticles` | `VehicleParticleManager` | Manages vehicle particle effects. |

## Methods

### Register

Registers an actor with the actor manager. Called automatically when an actor spawns.

| Parameter | Type | Description |
|-----------|------|-------------|
| `actor` | `Actor` | The actor to register. |

### Drop

Unregisters an actor from the actor manager.

| Parameter | Type | Description |
|-----------|------|-------------|
| `actor` | `Actor` | The actor to unregister. |

### RegisterTrigger

Registers a trigger volume and returns its index.

| Parameter | Type | Description |
|-----------|------|-------------|
| `volume` | `TriggerVolume` | The trigger volume to register. |

[return: int]
The index of the registered trigger volume.

### TryResolveOfficialVehicleByName

Attempts to find a built-in vehicle by name.

| Parameter | Type | Description |
|-----------|------|-------------|
| `name` | `string` | The name of the vehicle prefab. |
| `result` | `VehicleInfo` | The resolved vehicle info, if found. |

[return: bool]
`true` if the vehicle was found, `false` otherwise.

### RegisterDamageZone

Registers a damage zone.

| Parameter | Type | Description |
|-----------|------|-------------|
| `damageZone` | `DamageZone` | The damage zone to register. |

### DropDamageZone

Unregisters a damage zone.

| Parameter | Type | Description |
|-----------|------|-------------|
| `damageZone` | `DamageZone` | The damage zone to unregister. |

### RegisterSpeedLimitZone

Registers a speed limit zone.

| Parameter | Type | Description |
|-----------|------|-------------|
| `speedLimitZone` | `SpeedLimitZone` | The speed limit zone to register. |

### OnVehicleDisabled

Invokes the onVehicleDisabled event.

| Parameter | Type | Description |
|-----------|------|-------------|
| `vehicle` | `Vehicle` | The disabled vehicle. |
| `info` | `DamageInfo` | Damage information. |

### OnVehicleDestroyed

Invokes the onVehicleDestroyed event.

| Parameter | Type | Description |
|-----------|------|-------------|
| `vehicle` | `Vehicle` | The destroyed vehicle. |
| `info` | `DamageInfo` | Damage information. |

### OnActorDied

Invokes the onActorDied event.

| Parameter | Type | Description |
|-----------|------|-------------|
| `actor` | `Actor` | The actor that died. |
| `belongedToSquad` | `Squad` | The squad the actor belonged to. |
| `isSilentKill` | `bool` | Whether the kill was silent. |

### OnActorEnteredSeat

Invokes the onActorEnteredSeat event.

| Parameter | Type | Description |
|-----------|------|-------------|
| `actor` | `Actor` | The actor that entered the seat. |
| `seat` | `Seat` | The seat that was entered. |

### OnActorLeftSeat

Invokes the onActorLeftSeat event.

| Parameter | Type | Description |
|-----------|------|-------------|
| `actor` | `Actor` | The actor that left the seat. |
| `seat` | `Seat` | The seat that was left. |

## Static Methods

### EnableNightVisionGlow

Enables night vision glow on actor materials.

### DisableNightVisionGlow

Disables night vision glow on actor materials.

### SetTeamColor

Sets the team color for a specific team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `int` | The team index (0 or 1). |
| `color` | `Color` | The color to set. |

### RegisterSmokeTarget

Registers a smoke target at a position.

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The position of the smoke target. |
| `team` | `int` | The team index (0 or 1). |
| `lifetime` | `float` | How long the smoke target lasts. |
| `ignoreSmokeSpacing` | `bool` | Whether to ignore minimum spacing checks. |

[return: bool]
`true` if the smoke target was registered, `false` otherwise.

### GetSmokeTargetInRange

Finds a smoke target within range that hasn't been deployed yet.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `int` | The team index (0 or 1). |
| `position` | `Vector3` | The position to search from. |
| `range` | `float` | The search range. |
| `i` | `int` | The index of the found smoke target (output). |
| `targetPosition` | `Vector3` | The position of the found smoke target (output). |

[return: bool]
`true` if a smoke target was found, `false` otherwise.

### CompleteSmokeTarget

Marks a smoke target as deployed.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `int` | The team index (0 or 1). |
| `index` | `int` | The index of the smoke target. |

[return: int]
The deployed smoke target.

### AITickIsThrottled

Returns whether AI ticking is currently throttled.

[return: bool]
`true` if AI ticking is throttled, `false` otherwise.

### GetAITickStatusString

Returns a debug string with AI tick statistics.

[return: string]
A debug string describing AI tick statistics.

### ActorsCanSeeEachOther

Checks if two actors have line of sight to each other.

| Parameter | Type | Description |
|-----------|------|-------------|
| `a` | `Actor` | The first actor. |
| `b` | `Actor` | The second actor. |

[return: bool]
`true` if both actors can see each other, `false` otherwise.

### ActorCanSeePlayer

Checks if an actor can see the player.

| Parameter | Type | Description |
|-----------|------|-------------|
| `a` | `Actor` | The actor to check. |

[return: bool]
`true` if the actor can see the player, `false` otherwise.

### ActorsDistance

Gets the cached distance between two actors on opposing teams.

| Parameter | Type | Description |
|-----------|------|-------------|
| `a` | `Actor` | The first actor. |
| `b` | `Actor` | The second actor. |

[return: float]
The distance between the two actors.

### ActorDistanceToPlayer

Gets the distance from an actor to the player.

| Parameter | Type | Description |
|-----------|------|-------------|
| `a` | `Actor` | The actor to check. |

[return: float]
The distance from the actor to the player.

### GetNextTargetOfActor

Gets the current target actor for an actor.

| Parameter | Type | Description |
|-----------|------|-------------|
| `actor` | `Actor` | The actor to check. |

[return: Actor?]
The target actor, or `nil` if no target.

### ApplyGlobalTeamSkin

Applies the global team skin to an actor.

| Parameter | Type | Description |
|-----------|------|-------------|
| `actor` | `Actor` | The actor to apply the skin to. |

### ApplyGlobalTeamSkin

Applies the global team skin to a skinned mesh renderer.

| Parameter | Type | Description |
|-----------|------|-------------|
| `renderer` | `SkinnedMeshRenderer` | The renderer to apply the skin to. |
| `team` | `int` | The team index (0 or 1). |

### ApplyOverrideActorSkin

Applies a custom skin override to an actor.

| Parameter | Type | Description |
|-----------|------|-------------|
| `actor` | `Actor` | The actor to apply the skin to. |
| `skin` | `ActorSkin` | The skin to apply. |
| `team` | `int` | The team index (0 or 1). |

### ApplyOverrideActorSkin

Applies a custom skin override to a skinned mesh renderer.

| Parameter | Type | Description |
|-----------|------|-------------|
| `renderer` | `SkinnedMeshRenderer` | The renderer to apply the skin to. |
| `bones` | `Transform[]` | The bone transforms. |
| `skin` | `ActorSkin` | The skin to apply. |
| `team` | `int` | The team index (0 or 1). |

### ApplyOverrideMeshSkin

Applies a mesh skin to a skinned mesh renderer.

| Parameter | Type | Description |
|-----------|------|-------------|
| `renderer` | `SkinnedMeshRenderer` | The renderer to apply the skin to. |
| `skin` | `ActorSkin.MeshSkin` | The mesh skin to apply. |
| `team` | `int` | The team index (0 or 1). |

### GetRecursiveBones

Gets all bones recursively from a root bone.

| Parameter | Type | Description |
|-----------|------|-------------|
| `rootBone` | `Transform` | The root bone to start from. |

[return: Transform[]]
An array of all bone transforms found recursively.

### SetGlobalTeamSkin

Sets the global skin for a team and applies it to all actors on that team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `int` | The team index (0 or 1). |
| `skin` | `ActorSkin` | The skin to set. |

### ActorCanHearEnemy

Checks if an actor can currently hear enemy actors.

| Parameter | Type | Description |
|-----------|------|-------------|
| `actor` | `Actor` | The actor to check. |

[return: bool]
`true` if the actor can hear enemy actors, `false` otherwise.

### SetAlive

Marks an actor as alive.

| Parameter | Type | Description |
|-----------|------|-------------|
| `actor` | `Actor` | The actor to mark as alive. |

### SetDead

Marks an actor as dead.

| Parameter | Type | Description |
|-----------|------|-------------|
| `actor` | `Actor` | The actor to mark as dead. |

### AllActorsOnTeamAreDead

Checks if all actors on a team are dead.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `int` | The team index (0 or 1). |

[return: bool]
`true` if all actors on the team are dead, `false` otherwise.

### ActorsOnTeam

Gets all actors on a specific team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `int` | The team index (0 or 1). |

[return: Actor[]]
A list of all actors on the specified team.

### AliveActorsOnTeam

Gets all alive actors on a specific team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `int` | The team index (0 or 1). |

[return: Actor[]]
A list of all alive actors on the specified team.

### RandomSpawnPoint

Gets a random spawn point.

[return: SpawnPoint?]
A random spawn point, or `nil` if none exist.

### RandomSpawnPointForTeam

Gets a random spawn point owned by a specific team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `int` | The team index (0 or 1). |

[return: SpawnPoint?]
A random spawn point owned by the specified team, or `nil` if none exist.

### RandomFrontlineSpawnPointForTeam

Gets a random spawn point on the frontline for a specific team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `int` | The team index (0 or 1). |

[return: SpawnPoint?]
A random frontline spawn point for the specified team, or `nil` if none exist.

### TeamHasAnySpawnPoint

Checks if a team has any spawn points.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `int` | The team index (0 or 1). |

[return: bool]
`true` if the team has spawn points, `false` otherwise.

### ClosestSpawnPoint

Gets the closest spawn point to a position.

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The position to search from. |

[return: SpawnPoint?]
The closest spawn point, or `nil` if none exist.

### ClosestLandingZone

Gets the closest landing zone to a position.

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The position to search from. |

[return: LandingZone?]
The closest landing zone, or `nil` if none exist.

### ClosestSpawnPointOwnedBy

Gets the closest spawn point owned by a specific team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The position to search from. |
| `team` | `int` | The team index (0 or 1). |

[return: SpawnPoint?]
The closest spawn point owned by the specified team, or `nil` if none exist.

### RandomEnemySpawnPoint

Gets a random spawn point not owned by a specific team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `int` | The team index (0 or 1). |

[return: SpawnPoint?]
A random spawn point not owned by the specified team, or `nil` if none exist.

### AliveActors

Gets all alive actors.

[return: Actor[]]
A list of all alive actors.

### AliveActorsInRange

Gets all alive actors within a range of a position.

| Parameter | Type | Description |
|-----------|------|-------------|
| `point` | `Vector3` | The position to search from. |
| `range` | `float` | The search range. |

[return: Actor[]]
A list of all alive actors within range.

### ActorsInRange

Gets all actors (alive or dead) within a range of a position.

| Parameter | Type | Description |
|-----------|------|-------------|
| `point` | `Vector3` | The position to search from. |
| `range` | `float` | The search range. |

[return: Actor[]]
A list of all actors within range.

### VehiclesInRange

Gets all vehicles within a range of a position.

| Parameter | Type | Description |
|-----------|------|-------------|
| `point` | `Vector3` | The position to search from. |
| `range` | `float` | The search range. |

[return: Vehicle[]]
A list of all vehicles within range.

### RegisterProjectile

Registers a projectile and handles incoming fire detection for AI.

| Parameter | Type | Description |
|-----------|------|-------------|
| `p` | `Projectile` | The projectile to register. |

### PlayerTakeOverBot

Makes the player take control of a bot actor.

| Parameter | Type | Description |
|-----------|------|-------------|
| `targetActor` | `Actor` | The bot actor to take over. |

### CopyLoadoutOfActor

Copies the loadout from an actor.

| Parameter | Type | Description |
|-----------|------|-------------|
| `actor` | `Actor` | The actor to copy the loadout from. |

[return: LoadoutSet]
The copied loadout set.

### GetLadderWithNode

Finds a ladder that uses a specific graph node.

| Parameter | Type | Description |
|-----------|------|-------------|
| `graphNode` | `GraphNode` | The graph node to search for. |

[return: Ladder?]
The ladder using the specified graph node, or `nil` if not found.

### RegisterLadder

Registers a ladder with the actor manager.

| Parameter | Type | Description |
|-----------|------|-------------|
| `ladder` | `Ladder` | The ladder to register. |

### RegisterVehicle

Registers a vehicle with the actor manager.

| Parameter | Type | Description |
|-----------|------|-------------|
| `vehicle` | `Vehicle` | The vehicle to register. |

### SetVehicleTaken

Marks a vehicle as taken (removes it from available vehicles list).

| Parameter | Type | Description |
|-----------|------|-------------|
| `vehicle` | `Vehicle` | The vehicle to mark as taken. |

### DropVehicle

Unregisters a vehicle from the actor manager.

| Parameter | Type | Description |
|-----------|------|-------------|
| `vehicle` | `Vehicle` | The vehicle to unregister. |

### CreateExplosionEffect

Creates a generic explosion effect at a position.

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The position of the explosion. |
| `upDirection` | `Vector3` | The up direction for the effect. |
| `size` | `float` | The scale of the explosion effect. |

### Explode

Creates an explosion at a position.

| Parameter | Type | Description |
|-----------|------|-------------|
| `source` | `Actor` | The actor that caused the explosion. |
| `sourceWeapon` | `Weapon` | The weapon that caused the explosion. |
| `point` | `Vector3` | The position of the explosion. |
| `configuration` | `ExplodingProjectile.ExplosionConfiguration` | The explosion configuration. |
| `damageRating` | `Vehicle.ArmorRating` | The armor damage rating. |
| `reduceFriendlyDamage` | `bool` | Whether to reduce damage to friendly actors. |

[return: bool]
`true` if the explosion was created, `false` otherwise.

### Explode

Creates an explosion at a position using ExplosionInfo.

| Parameter | Type | Description |
|-----------|------|-------------|
| `info` | `ExplosionInfo` | The explosion information. |
| `reduceFriendlyDamage` | `bool` | Whether to reduce damage to friendly actors. |

[return: bool]
`true` if the explosion was created, `false` otherwise.

### EvaluateExplosionDamage

Evaluates the damage from an explosion at a point.

| Parameter | Type | Description |
|-----------|------|-------------|
| `info` | `ExplosionInfo` | The explosion information. |
| `point` | `Vector3` | The point to evaluate damage at. |
| `ignoreLevelGeometry` | `bool` | Whether to ignore level geometry blocking. |

[return: DamageInfo]
The evaluated damage info.

### EvaluateLastExplosionDamage

Evaluates damage from the last explosion at a point.

| Parameter | Type | Description |
|-----------|------|-------------|
| `point` | `Vector3` | The point to evaluate damage at. |
| `ignoreLevelGeometry` | `bool` | Whether to ignore level geometry blocking. |

[return: DamageInfo]
The evaluated damage info.

### MakeActorsFleeFrom

Makes actors flee from a position.

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The position to flee from. |
| `range` | `float` | The range within which actors will flee. |
| `diveTime` | `float` | How long actors will dive for. |
| `diveRange` | `float` | The range within which actors will dive. |
| `requirePointInFov` | `bool` | Whether the position must be in the actor's FOV. |

### SpawnAmmoReserveOnActor

Spawns an ammo reserve at an actor's position.

| Parameter | Type | Description |
|-----------|------|-------------|
| `actor` | `Actor` | The actor to spawn ammo reserve for. |

### RegisterSquad

Registers a squad with the actor manager.

| Parameter | Type | Description |
|-----------|------|-------------|
| `squad` | `Squad` | The squad to register. |

### RemoveSquad

Unregisters a squad from the actor manager.

| Parameter | Type | Description |
|-----------|------|-------------|
| `squad` | `Squad` | The squad to unregister. |

### GetSquadsOnTeam

Gets all squads on a specific team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `int` | The team index (0 or 1). |

[return: Squad[]]
A list of all squads on the specified team.

### OnExitGameScene

Called when exiting to the main menu. Clears actor manager data.

## Events

| Event | Signature | Description |
|-------|-----------|-------------|
| `onActorDied` | `(actor, belongedToSquad, isSilentKill)` | Fired when an actor dies. |
| `onVehicleDisabled` | `(vehicle, info)` | Fired when a vehicle is disabled. |
| `onVehicleDestroyed` | `(vehicle, info)` | Fired when a vehicle is destroyed. |
| `onActorEnteredSeat` | `(actor, seat)` | Fired when an actor enters a vehicle seat. |
| `onActorLeftSeat` | `(actor, seat)` | Fired when an actor leaves a vehicle seat. |
| `OnExplosion` | `(ExplosionInfo)` | Fired when an explosion occurs. |
