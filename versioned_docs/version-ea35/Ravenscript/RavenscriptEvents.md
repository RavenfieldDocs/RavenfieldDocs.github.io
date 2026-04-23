---
title: RavenscriptEvents
---

Global event manager for Ravenscript. Provides script events that fire during key game moments such as actor spawning, vehicle destruction, squad orders, capture point changes, and more. Accessible as ``GameEvents`` in scripts.

## Properties

| Property | Type | Description |
|----------|------|-------------|

## Methods

## Events

| Event | Signature | Description |
|-------|-----------|-------------|
| `onActorCreated` | `([Actor](./Actor.md))` | Invoked when an actor is created during a game. Please note this event is typically not invoked for actors created at the very start of the game, such as the default actors in the game. To access those actors, you can get ``ActorManager.actors`` in your ``Start()`` function. |
| `onActorDied` | `([Actor](./Actor.md), [Actor](./Actor.md), bool)` | Invoked when an actor dies. Silent kills should typically not count towards team score. Example of silent kill: When the player takes over a bot, the bot actor is silently killed. Deprecated: Use onActorDiedInfo instead! |
| `onActorDiedInfo` | `([Actor](./Actor.md), [DamageInfo](./DamageInfo.md), bool)` | Invoked when an actor dies. Silent kills should typically not count towards team score. Example of silent kill: When the player takes over a bot, the bot actor is silently killed. |
| `onActorSelectedLoadout` | `([Actor](./Actor.md), WeaponManager.LoadoutSet, AiActorController.LoadoutPickStrategy)` | Invoked when an actor has selected a loadout. This function is called just before the actor spawns, allowing you to modify their spawn loadout by changing the loadout object. For the player actor, the loadout strategy is nil. |
| `onActorSpawn` | `([Actor](./Actor.md))` | Invoked when an actor spawns. |
| `onBloodParticleLand` | `(Vector3, WTeam, bool)` | Invoked when a blood drop particle lands somewhere. When a droplet lands on a moving object such as a vehicle, createDecal is set to false, implying that a static decal cannot be created there. |
| `onCapturePointCaptured` | `([CapturePoint](./CapturePoint.md), WTeam)` | Invoked when a capture point is captured. IE when it's owner is set to Team.Blue or Team.Red. |
| `onCapturePointNeutralized` | `([CapturePoint](./CapturePoint.md), WTeam)` | Invoked when a capture point is neutralized. IE when it's owner is set to Team.Neutral. |
| `onExplosion` | `(Vector3, float, [Actor](./Actor.md))` | Invoked when an explosion goes off. Deprecated: Use onExplosionInfo instead! |
| `onExplosionInfo` | `(ExplosionInfo)` | Invoked when an explosion goes off. |
| `onMatchEnd` | `(WTeam)` | Invoked when a match ends. Consuming this event stops the default victory screen from playing and the match ending. |
| `onOverlayText` | `(string, float)` | Invoked when an overlay text is shown. This is a good event to drive custom UI from! |
| `onPlayerDealtDamage` | `([DamageInfo](./DamageInfo.md), HitInfo)` | Invoked when the player deals damage. This is a good event to drive UI feedback effects such as hitmarkers from! |
| `onPlayerRepairedVehicle` | `([Vehicle](./Vehicle.md), float)` | Invoked when the player repairs a vehicle. This is a good event to drive UI feedback effects such as repair info from! |
| `onProjectileSpawned` | `([Projectile](./Projectile.md))` | Invoked when a projectile is spawned. |
| `onSquadAssignedNewOrder` | `([Squad](./Squad.md), [Order](./Order.md))` | Invoked when a squad is assigned a new order. |
| `onSquadCreated` | `([Squad](./Squad.md))` | Invoked when a squad is created. |
| `onSquadFailedToAssignNewOrder` | `([Squad](./Squad.md))` | Invoked when a squad requested a new order, but none were available. |
| `onSquadRequestNewOrder` | `([Squad](./Squad.md))` | Invoked when a squad requests a new order. Consuming this event stops the squad from automatically being assigned an order. |
| `onTurretActivated` | `([Vehicle](./Vehicle.md), TurretSpawner)` | Invoked when a turret is activated. |
| `onVehicleDestroyed` | `([Vehicle](./Vehicle.md), [DamageInfo](./DamageInfo.md))` | Invoked when a vehicle is destroyed. |
| `onVehicleDisabled` | `([Vehicle](./Vehicle.md), [DamageInfo](./DamageInfo.md))` | Invoked when a vehicle starts burning. |
| `onVehicleExtinguished` | `([Vehicle](./Vehicle.md))` | Invoked when a vehicle stops burning. |
| `onVehicleSpawn` | `([Vehicle](./Vehicle.md), VehicleSpawner)` | Invoked when a vehicle is spawned. Note that if the vehicle isn't spawned by a VehicleSpawner, the spawner value is nil. |

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

## Enums
