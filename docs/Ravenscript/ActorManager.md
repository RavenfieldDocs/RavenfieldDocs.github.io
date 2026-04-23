---
title: ActorManager
---

## Properties

| Name | Type | Description |
| --- | --- | --- |
| isInitialized | bool | Whether the actor manager has been initialized for the current game. |
| vehicles | List\<Vehicle\> | All vehicles currently in the game. |
| spawnPoints | SpawnPoint[] | All spawn points in the current level. |
| actors | List\<Actor\> | All actors currently in the game. |
| player | Actor | The player-controlled actor. |
| actorData | List\<ActorData\> | Data associated with each actor. |
| squadsOnTeam | List\<Squad\>[] | Squads organized by team (index 0 or 1). |
| ladders | List\<Ladder\> | All ladders in the current level. |
| damageZones | List\<DamageZone\> | All damage zones in the current level. |
| speedLimitZones | List\<SpeedLimitZone\> | All speed limit zones in the current level. |
| activeTriggers | List\<TriggerVolume.RuntimeData\> | Active trigger volumes. |
| triggerStates | List\<TriggerVolumeActorState\> | States for active trigger volumes. |
| actorCanHearEnemy | bool[] | Whether each actor can hear enemy actors. |
| bloodParticleLifetime | float | Lifetime of blood particles in seconds. |
| bloodParticleSpeedMultiplier | float | Speed multiplier for blood particles. |
| bloodParticleVerticalLaunchSpeed | float | Vertical launch speed for blood particles. |
| bloodParticleSize | float | Size multiplier for blood particles. |
| vehicleParticles | VehicleParticleManager | Manages vehicle particle effects. |

## Events

| Name | Signature | Description |
| --- | --- | --- |
| onActorDied | (actor: Actor, belongedToSquad: Squad, isSilentKill: bool) | Fired when an actor dies. |
| onVehicleDisabled | (vehicle: Vehicle, info: DamageInfo) | Fired when a vehicle is disabled. |
| onVehicleDestroyed | (vehicle: Vehicle, info: DamageInfo) | Fired when a vehicle is destroyed. |
| onActorEnteredSeat | (actor: Actor, seat: Seat) | Fired when an actor enters a vehicle seat. |
| onActorLeftSeat | (actor: Actor, seat: Seat) | Fired when an actor leaves a vehicle seat. |
| OnExplosion | UnityEvent\<ExplosionInfo\> | Fired when an explosion occurs. |

## Methods

### Register

Registers an actor with the actor manager. Called automatically when an actor spawns.

| Parameter | Type | Description |
| --- | --- | --- |
| actor | Actor | The actor to register. |

**Returns:** void

### Drop

Unregisters an actor from the actor manager.

| Parameter | Type | Description |
| --- | --- | --- |
| actor | Actor | The actor to unregister. |

**Returns:** void

### RegisterTrigger

Registers a trigger volume and returns its index.

| Parameter | Type | Description |
| --- | --- | --- |
| volume | TriggerVolume | The trigger volume to register. |

**Returns:** int

### TryResolveOfficialVehicleByName

Attempts to find a built-in vehicle by name.

| Parameter | Type | Description |
| --- | --- | --- |
| name | string | The name of the vehicle prefab. |
| result | VehicleInfo | The resolved vehicle info, if found. |

**Returns:** bool

### RegisterDamageZone

Registers a damage zone.

| Parameter | Type | Description |
| --- | --- | --- |
| damageZone | DamageZone | The damage zone to register. |

**Returns:** void

### DropDamageZone

Unregisters a damage zone.

| Parameter | Type | Description |
| --- | --- | --- |
| damageZone | DamageZone | The damage zone to unregister. |

**Returns:** void

### RegisterSpeedLimitZone

Registers a speed limit zone.

| Parameter | Type | Description |
| --- | --- | --- |
| speedLimitZone | SpeedLimitZone | The speed limit zone to register. |

**Returns:** void

### OnVehicleDisabled

Invokes the onVehicleDisabled event.

| Parameter | Type | Description |
| --- | --- | --- |
| vehicle | Vehicle | The disabled vehicle. |
| info | DamageInfo | Damage information. |

**Returns:** void

### OnVehicleDestroyed

Invokes the onVehicleDestroyed event.

| Parameter | Type | Description |
| --- | --- | --- |
| vehicle | Vehicle | The destroyed vehicle. |
| info | DamageInfo | Damage information. |

**Returns:** void

### OnActorDied

Invokes the onActorDied event.

| Parameter | Type | Description |
| --- | --- | --- |
| actor | Actor | The actor that died. |
| belongedToSquad | Squad | The squad the actor belonged to. |
| isSilentKill | bool | Whether the kill was silent. |

**Returns:** void

### OnActorEnteredSeat

Invokes the onActorEnteredSeat event.

| Parameter | Type | Description |
| --- | --- | --- |
| actor | Actor | The actor that entered the seat. |
| seat | Seat | The seat that was entered. |

**Returns:** void

### OnActorLeftSeat

Invokes the onActorLeftSeat event.

| Parameter | Type | Description |
| --- | --- | --- |
| actor | Actor | The actor that left the seat. |
| seat | Seat | The seat that was left. |

**Returns:** void

## Static Methods

### EnableNightVisionGlow

Enables night vision glow on actor materials.

**Returns:** void

### DisableNightVisionGlow

Disables night vision glow on actor materials.

**Returns:** void

### SetTeamColor

Sets the team color for a specific team.

| Parameter | Type | Description |
| --- | --- | --- |
| team | int | The team index (0 or 1). |
| color | Color | The color to set. |

**Returns:** void

### RegisterSmokeTarget

Registers a smoke target at a position.

| Parameter | Type | Description |
| --- | --- | --- |
| position | Vector3 | The position of the smoke target. |
| team | int | The team index (0 or 1). |
| lifetime | float | How long the smoke target lasts. |
| ignoreSmokeSpacing | bool | Whether to ignore minimum spacing checks. |

**Returns:** bool

### GetSmokeTargetInRange

Finds a smoke target within range that hasn't been deployed yet.

| Parameter | Type | Description |
| --- | --- | --- |
| team | int | The team index (0 or 1). |
| position | Vector3 | The position to search from. |
| range | float | The search range. |
| i | int | The index of the found smoke target (output). |
| targetPosition | Vector3 | The position of the found smoke target (output). |

**Returns:** bool

### CompleteSmokeTarget

Marks a smoke target as deployed.

| Parameter | Type | Description |
| --- | --- | --- |
| team | int | The team index (0 or 1). |
| index | int | The index of the smoke target. |

**Returns:** SmokeTarget

### AITickIsThrottled

Returns whether AI ticking is currently throttled.

**Returns:** bool

### GetAITickStatusString

Returns a debug string with AI tick statistics.

**Returns:** string

### ActorsCanSeeEachOther

Checks if two actors have line of sight to each other.

| Parameter | Type | Description |
| --- | --- | --- |
| a | Actor | The first actor. |
| b | Actor | The second actor. |

**Returns:** bool

### ActorCanSeePlayer

Checks if an actor can see the player.

| Parameter | Type | Description |
| --- | --- | --- |
| a | Actor | The actor to check. |

**Returns:** bool

### ActorsDistance

Gets the cached distance between two actors on opposing teams.

| Parameter | Type | Description |
| --- | --- | --- |
| a | Actor | The first actor. |
| b | Actor | The second actor. |

**Returns:** float

### ActorDistanceToPlayer

Gets the distance from an actor to the player.

| Parameter | Type | Description |
| --- | --- | --- |
| a | Actor | The actor to check. |

**Returns:** float

### GetNextTargetOfActor

Gets the current target actor for an actor.

| Parameter | Type | Description |
| --- | --- | --- |
| actor | Actor | The actor to check. |

**Returns:** Actor

### ApplyGlobalTeamSkin

Applies the global team skin to an actor.

| Parameter | Type | Description |
| --- | --- | --- |
| actor | Actor | The actor to apply the skin to. |

**Returns:** void

### ApplyGlobalTeamSkin

Applies the global team skin to a skinned mesh renderer.

| Parameter | Type | Description |
| --- | --- | --- |
| renderer | SkinnedMeshRenderer | The renderer to apply the skin to. |
| team | int | The team index (0 or 1). |

**Returns:** void

### ApplyOverrideActorSkin

Applies a custom skin override to an actor.

| Parameter | Type | Description |
| --- | --- | --- |
| actor | Actor | The actor to apply the skin to. |
| skin | ActorSkin | The skin to apply. |
| team | int | The team index (0 or 1). |

**Returns:** void

### ApplyOverrideActorSkin

Applies a custom skin override to a skinned mesh renderer.

| Parameter | Type | Description |
| --- | --- | --- |
| renderer | SkinnedMeshRenderer | The renderer to apply the skin to. |
| bones | Transform[] | The bone transforms. |
| skin | ActorSkin | The skin to apply. |
| team | int | The team index (0 or 1). |

**Returns:** void

### ApplyOverrideMeshSkin

Applies a mesh skin to a skinned mesh renderer.

| Parameter | Type | Description |
| --- | --- | --- |
| renderer | SkinnedMeshRenderer | The renderer to apply the skin to. |
| skin | ActorSkin.MeshSkin | The mesh skin to apply. |
| team | int | The team index (0 or 1). |

**Returns:** void

### GetRecursiveBones

Gets all bones recursively from a root bone.

| Parameter | Type | Description |
| --- | --- | --- |
| rootBone | Transform | The root bone to start from. |

**Returns:** Transform[]

### SetGlobalTeamSkin

Sets the global skin for a team and applies it to all actors on that team.

| Parameter | Type | Description |
| --- | --- | --- |
| team | int | The team index (0 or 1). |
| skin | ActorSkin | The skin to set. |

**Returns:** void

### ActorCanHearEnemy

Checks if an actor can currently hear enemy actors.

| Parameter | Type | Description |
| --- | --- | --- |
| actor | Actor | The actor to check. |

**Returns:** bool

### SetAlive

Marks an actor as alive.

| Parameter | Type | Description |
| --- | --- | --- |
| actor | Actor | The actor to mark as alive. |

**Returns:** void

### SetDead

Marks an actor as dead.

| Parameter | Type | Description |
| --- | --- | --- |
| actor | Actor | The actor to mark as dead. |

**Returns:** void

### AllActorsOnTeamAreDead

Checks if all actors on a team are dead.

| Parameter | Type | Description |
| --- | --- | --- |
| team | int | The team index (0 or 1). |

**Returns:** bool

### ActorsOnTeam

Gets all actors on a specific team.

| Parameter | Type | Description |
| --- | --- | --- |
| team | int | The team index (0 or 1). |

**Returns:** List\<Actor\>

### AliveActorsOnTeam

Gets all alive actors on a specific team.

| Parameter | Type | Description |
| --- | --- | --- |
| team | int | The team index (0 or 1). |

**Returns:** List\<Actor\>

### RandomSpawnPoint

Gets a random spawn point.

**Returns:** SpawnPoint

### RandomSpawnPointForTeam

Gets a random spawn point owned by a specific team.

| Parameter | Type | Description |
| --- | --- | --- |
| team | int | The team index (0 or 1). |

**Returns:** SpawnPoint

### RandomFrontlineSpawnPointForTeam

Gets a random spawn point on the frontline for a specific team.

| Parameter | Type | Description |
| --- | --- | --- |
| team | int | The team index (0 or 1). |

**Returns:** SpawnPoint

### TeamHasAnySpawnPoint

Checks if a team has any spawn points.

| Parameter | Type | Description |
| --- | --- | --- |
| team | int | The team index (0 or 1). |

**Returns:** bool

### ClosestSpawnPoint

Gets the closest spawn point to a position.

| Parameter | Type | Description |
| --- | --- | --- |
| position | Vector3 | The position to search from. |

**Returns:** SpawnPoint

### ClosestLandingZone

Gets the closest landing zone to a position.

| Parameter | Type | Description |
| --- | --- | --- |
| position | Vector3 | The position to search from. |

**Returns:** LandingZone

### ClosestSpawnPointOwnedBy

Gets the closest spawn point owned by a specific team.

| Parameter | Type | Description |
| --- | --- | --- |
| position | Vector3 | The position to search from. |
| team | int | The team index (0 or 1). |

**Returns:** SpawnPoint

### RandomEnemySpawnPoint

Gets a random spawn point not owned by a specific team.

| Parameter | Type | Description |
| --- | --- | --- |
| team | int | The team index (0 or 1). |

**Returns:** SpawnPoint

### AliveActors

Gets all alive actors.

**Returns:** List\<Actor\>

### AliveActorsInRange

Gets all alive actors within a range of a position.

| Parameter | Type | Description |
| --- | --- | --- |
| point | Vector3 | The position to search from. |
| range | float | The search range. |

**Returns:** List\<Actor\>

### ActorsInRange

Gets all actors (alive or dead) within a range of a position.

| Parameter | Type | Description |
| --- | --- | --- |
| point | Vector3 | The position to search from. |
| range | float | The search range. |

**Returns:** List\<Actor\>

### VehiclesInRange

Gets all vehicles within a range of a position.

| Parameter | Type | Description |
| --- | --- | --- |
| point | Vector3 | The position to search from. |
| range | float | The search range. |

**Returns:** List\<Vehicle\>

### RegisterProjectile

Registers a projectile and handles incoming fire detection for AI.

| Parameter | Type | Description |
| --- | --- | --- |
| p | Projectile | The projectile to register. |

**Returns:** void

### PlayerTakeOverBot

Makes the player take control of a bot actor.

| Parameter | Type | Description |
| --- | --- | --- |
| targetActor | Actor | The bot actor to take over. |

**Returns:** void

### CopyLoadoutOfActor

Copies the loadout from an actor.

| Parameter | Type | Description |
| --- | --- | --- |
| actor | Actor | The actor to copy the loadout from. |

**Returns:** WeaponManager.LoadoutSet

### GetLadderWithNode

Finds a ladder that uses a specific graph node.

| Parameter | Type | Description |
| --- | --- | --- |
| graphNode | GraphNode | The graph node to search for. |

**Returns:** Ladder

### RegisterLadder

Registers a ladder with the actor manager.

| Parameter | Type | Description |
| --- | --- | --- |
| ladder | Ladder | The ladder to register. |

**Returns:** void

### RegisterVehicle

Registers a vehicle with the actor manager.

| Parameter | Type | Description |
| --- | --- | --- |
| vehicle | Vehicle | The vehicle to register. |

**Returns:** void

### SetVehicleTaken

Marks a vehicle as taken (removes it from available vehicles list).

| Parameter | Type | Description |
| --- | --- | --- |
| vehicle | Vehicle | The vehicle to mark as taken. |

**Returns:** void

### DropVehicle

Unregisters a vehicle from the actor manager.

| Parameter | Type | Description |
| --- | --- | --- |
| vehicle | Vehicle | The vehicle to unregister. |

**Returns:** void

### CreateExplosionEffect

Creates a generic explosion effect at a position.

| Parameter | Type | Description |
| --- | --- | --- |
| position | Vector3 | The position of the explosion. |
| upDirection | Vector3 | The up direction for the effect. |
| size | float | The scale of the explosion effect. |

**Returns:** void

### Explode

Creates an explosion at a position.

| Parameter | Type | Description |
| --- | --- | --- |
| source | Actor | The actor that caused the explosion. |
| sourceWeapon | Weapon | The weapon that caused the explosion. |
| point | Vector3 | The position of the explosion. |
| configuration | ExplodingProjectile.ExplosionConfiguration | The explosion configuration. |
| damageRating | Vehicle.ArmorRating | The armor damage rating. |
| reduceFriendlyDamage | bool | Whether to reduce damage to friendly actors. |

**Returns:** bool

### Explode

Creates an explosion at a position using ExplosionInfo.

| Parameter | Type | Description |
| --- | --- | --- |
| info | ExplosionInfo | The explosion information. |
| reduceFriendlyDamage | bool | Whether to reduce damage to friendly actors. |

**Returns:** bool

### EvaluateExplosionDamage

Evaluates the damage from an explosion at a point.

| Parameter | Type | Description |
| --- | --- | --- |
| info | ExplosionInfo | The explosion information. |
| point | Vector3 | The point to evaluate damage at. |
| ignoreLevelGeometry | bool | Whether to ignore level geometry blocking. |

**Returns:** DamageInfo

### EvaluateLastExplosionDamage

Evaluates damage from the last explosion at a point.

| Parameter | Type | Description |
| --- | --- | --- |
| point | Vector3 | The point to evaluate damage at. |
| ignoreLevelGeometry | bool | Whether to ignore level geometry blocking. |

**Returns:** DamageInfo

### MakeActorsFleeFrom

Makes actors flee from a position.

| Parameter | Type | Description |
| --- | --- | --- |
| position | Vector3 | The position to flee from. |
| range | float | The range within which actors will flee. |
| diveTime | float | How long actors will dive for. |
| diveRange | float | The range within which actors will dive. |
| requirePointInFov | bool | Whether the position must be in the actor's FOV. |

**Returns:** void

### SpawnAmmoReserveOnActor

Spawns an ammo reserve at an actor's position.

| Parameter | Type | Description |
| --- | --- | --- |
| actor | Actor | The actor to spawn ammo reserve for. |

**Returns:** void

### RegisterSquad

Registers a squad with the actor manager.

| Parameter | Type | Description |
| --- | --- | --- |
| squad | Squad | The squad to register. |

**Returns:** void

### RemoveSquad

Unregisters a squad from the actor manager.

| Parameter | Type | Description |
| --- | --- | --- |
| squad | Squad | The squad to unregister. |

**Returns:** void

### GetSquadsOnTeam

Gets all squads on a specific team.

| Parameter | Type | Description |
| --- | --- | --- |
| team | int | The team index (0 or 1). |

**Returns:** List\<Squad\>

### OnExitGameScene

Called when exiting to the main menu. Clears actor manager data.

**Returns:** void
