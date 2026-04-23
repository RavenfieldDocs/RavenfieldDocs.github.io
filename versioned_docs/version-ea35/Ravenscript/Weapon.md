---
title: Weapon
---

Represents a weapon in the game. Handles shooting, reloading, ammo, recoil, spread, heat, sub-weapons, and sight modes.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `user` | [Actor](./Actor.md) | The actor currently using this weapon. |
| `killCredit` | [Actor](./Actor.md) | The actor that gets damage/kill credits from this weapon. Automatically set to whoever equips this weapon, but can be overridden if required. |
| `weaponEntry` | `WeaponEntry` | The weapon entry this weapon was instantiated from. |
| `useMaxAmmoPerReload` | `bool` | Whether maxAmmoPerReload is applied when reloading. |
| `maxAmmoPerReload` | `int` | Max ammo that can be added when reloading. Requires useMaxAmmoPerReload to be true to be applied. |
| `maxAmmo` | `int` | The maximum loaded ammo capacity of this weapon. |
| `ammo` | `int` | The current loaded ammo of this weapon. |
| `spareAmmo` | `int` | The current spare ammo of this weapon. |
| `maxSpareAmmo` | `int` | The maximum spare ammo capacity of this weapon. |
| `reloading` | `bool` | Returns `true` if the weapon is currently reloading. |
| `hasAdvancedReload` | `bool` | Returns `true` if the weapon uses advanced reload animations. |
| `reloadTime` | `float` | The time in seconds it takes to reload this weapon. |
| `aimFov` | `float` | The Field Of View (zoom level) applied to the player when aiming this weapon. |
| `aimSensitivityMultiplier` | `float` | The multiplier applied to the player's aim sensitivity when aiming this weapon. |
| `holdingFire` | `bool` | True while fire button is held down. |
| `unholstered` | `bool` | Returns `true` if the weapon is currently unholstered. |
| `slot` | `int` | The slot index this weapon is assigned to. |
| `aiming` | `bool` | Returns `true` if the user is currently aiming this weapon. |
| `canFire` | `bool` | Returns `true` if the weapon can be fired. Checks ammo, cooldown, overheat, lock, target tracker and misc flags. |
| `isCoolingDown` | `bool` | Returns `true` if the weapon is currently in its cooldown period after firing. |
| `cooldown` | `float` | The cooldown time in seconds between shots. |
| `isFull` | `bool` | Returns `true` if the loaded ammo is at max capacity. |
| `isEmpty` | `bool` | Returns `true` if the loaded ammo is zero. |
| `hasSpareAmmo` | `bool` | Returns `true` if the weapon has any spare ammo. |
| `hasLoadedAmmo` | `bool` | Returns `true` if the weapon has any loaded ammo. |
| `currentMuzzleTransform` | `Transform` | The muzzle transform that the next projectile will fire from. |
| `muzzleTransforms` | `Transform[]` | All muzzle transforms on this weapon. |
| `currentMuzzleIndex` | `int` | The index of the currently active muzzle. |
| `animator` | `Animator` | Get the weapon animator. Please note that weapons carried by the AI never have animators. Only player carried weapons and MountedWeapons can have animators. |
| `currentSpreadMagnitude` | `float` | The current spread magnitude of a weapon. The spread magnitude is the radius of a sphere 1 meter in front of the muzzle. The projectile may fire towards a random point inside that sphere. |
| `currentSpreadMaxAngleRadians` | `float` | The current maximum spread of a weapon in radians. |
| `isLoud` | `bool` | A loud weapon will alert nearby enemies when being fired. |
| `projectilesPerShot` | `int` | The number of projectiles spawned when the weapons is fired. |
| `isAuto` | `bool` | Returns `true` if this weapon fires in full-auto mode. |
| `unholsterTime` | `float` | The time in seconds it takes to unholster this weapon. |
| `effectiveRange` | `float` | The range at which the weapon is considered effective. |
| `effectivenessAir` | `Effectiveness` | Effectiveness of this weapon against Air targets. This value is used by AI and TargetTrackers to prioritize targets. |
| `effectivenessAirFastMover` | `Effectiveness` | Effectiveness of this weapon against Airplane targets. This value is used by AI and TargetTrackers to prioritize targets. |
| `effectivenessInfantry` | `Effectiveness` | Effectiveness of this weapon against Infantry targets. This value is used by AI and TargetTrackers to prioritize targets. |
| `effectivenessInfantryGroup` | `Effectiveness` | Effectiveness of this weapon against InfantryGroup targets. This value is used by AI and TargetTrackers to prioritize targets. |
| `effectivenessArmored` | `Effectiveness` | Effectiveness of this weapon against Armored targets. This value is used by AI and TargetTrackers to prioritize targets. |
| `effectivenessUnarmored` | `Effectiveness` | Effectiveness of this weapon against Unarmored targets. This value is used by AI and TargetTrackers to prioritize targets. |
| `difficultyInfantry` | `Difficulty` | Difficulty of hitting Infantry target with this weapon. |
| `difficultyInfantryGroup` | `Difficulty` | Difficulty of hitting InfantryGroup target with this weapon. |
| `difficultyAir` | `Difficulty` | Difficulty of hitting Air target with this weapon. |
| `difficultyAirFastMover` | `Difficulty` | Difficulty of hitting AirFastMover target with this weapon. |
| `difficultyGroundVehicles` | `Difficulty` | Difficulty of hitting GroundVehicles target with this weapon. |
| `recoilBaseKickback` | `float` | The base kickback force applied when firing. |
| `recoilRandomKickback` | `float` | The random kickback variance applied when firing. |
| `recoilKickbackProneMultiplier` | `float` | The multiplier applied to kickback when the user is prone. |
| `recoilSnapMagnitude` | `float` | The magnitude of the recoil snap animation. |
| `recoilSnapFrequency` | `float` | The frequency of the recoil snap animation. Note: Currently returns `recoilSnapMagnitude` due to a bug in the game's source code. |
| `recoilSnapDuration` | `float` | The duration of the recoil snap animation. |
| `recoilSnapProneMultiplier` | `float` | The multiplier applied to snap when the user is prone. |
| `baseSpread` | `float` | The base spread value of this weapon. |
| `followupSpread` | `WFollowupSpread` | The followup spread configuration of this weapon. |
| `rattleMagnitude` | `float` | The magnitude of the weapon rattle effect. |
| `rattleFrequency` | `float` | The frequency of the weapon rattle effect. |
| `rattleDuration` | `float` | The duration of the weapon rattle effect. |
| `isLocked` | `bool` | Locked weapons cannot be fired by the user. |
| `isOverheating` | `bool` | Returns `true` if the weapon is currently overheated. |
| `heat` | `float` | The current heat value of the weapon if applyHeat is enabled. When heat reaches 1, the weapon cannot be fired until the heat reaches 0 again. |
| `applyHeat` | `bool` | If true, each shot will heat up the weapon. If the heat value reaches 1 the gun overheats, and cannot be fired again until it cools down. |
| `heatDrainRate` | `float` | The rate at which heat drains in units per second. |
| `heatGainPerShot` | `float` | The amount of heat gained per shot when applyHeat is enabled. |
| `isCharged` | `bool` | True if fire input has been held long enough to fire the weapon. |
| `useChargeTime` | `bool` | When true, the weapon must charge before firing. Requires the fire button to be held for chargeTime seconds before firing. |
| `chargeTime` | `float` | The time in seconds required to charge the weapon before firing. |
| `activeSubWeapon` | [Weapon](./Weapon.md) | Get the currently active Sub Weapon from the alternativeWeapons list. |
| `activeSubWeaponIndex` | `int` | Get the currently active Sub Weapon index. |
| `alternativeWeapons` | [Weapon](./Weapon.md)[] | All sub weapons attached to this weapon. |
| `uiSprite` | `Sprite` | The sprite used to represent this weapon in UI. |
| `activeSightModeIndex` | `int` | The index of the currently active sight mode. |
| `thirdPersonOffset` | `Vector3` | The offset of the third person weapon model. |
| `thirdPersonRotation` | `Quaternion` | The rotation of the third person weapon model. |
| `thirdPersonScale` | `float` | The scale of the third person weapon model. |
| `scopeAimObject` | `GameObject` | The scope aim object that is shown when aiming down sights. |

## Methods

### Reload

Initiates a reload of the weapon.

### InstantlyReload

Instantly completes the reload, filling the weapon to max ammo.

### Shoot

Shoots this weapon. If force is true, ignores the CanFire() check. Returns true if shot was fired.

| Parameter | Type | Description |
|-----------|------|-------------|
| `force` | `bool` | If true, ignores the CanFire() check. |

[return: bool]
`true` if shot was fired.

### Shoot

Shoots this weapon, respecting the `CanFire()` check.

[return: bool]
`true` if shot was fired.

### LockWeapon

Lock the weapon so it cannot be fired.

### UnlockWeapon

Unlock the weapon so it can be fired.

### NextSubWeapon

Switch to the next Sub Weapon in the Weapon's alternativeWeapons list.

### EquipSubWeapon

Equips the sub weapon at the specified index.

| Parameter | Type | Description |
|-----------|------|-------------|
| `subWeaponIndex` | `int` | The index of the sub weapon to equip. |

### AddSubWeapon

Add a subweapon to this parent weapon, returning the subweapon index.

| Parameter | Type | Description |
|-----------|------|-------------|
| `subWeapon` | `Weapon` | The sub weapon to add. |

[return: int]
The index of the added sub weapon.

### RemoveSubWeapon

Removes a subweapon from this parent weapon.

| Parameter | Type | Description |
|-----------|------|-------------|
| `subWeaponIndex` | `int` | The index of the sub weapon to remove. |

### RemoveSubWeapon

Removes a subweapon from this parent weapon.

| Parameter | Type | Description |
|-----------|------|-------------|
| `subWeapon` | `Weapon` | The sub weapon to remove. |

### NextSightMode

Switches to the next sight mode.

### PreviousSightMode

Switches to the previous sight mode.

### SetRenderersInvisible

Makes the weapon invisible.

### SetRenderersVisible

Makes the weapon visible.

### GenerateWeaponRoleFromStats

Matches a weapon role based on the weapon's current stats.

[return: WeaponRole]
The matched weapon role.

### GetProjectilePrefab

Returns the weapon's projectile prefab.

[return: GameObject]
The projectile prefab.

### SetProjectilePrefab

Sets the weapon's projectile prefab.

| Parameter | Type | Description |
|-----------|------|-------------|
| `prefab` | `GameObject` | The projectile prefab to use. |

## Events

| Event | Signature | Description |
|-------|-----------|-------------|
| `onFire` | `()` | Invoked when the weapon is fired. Consuming this event stops the weapon from firing. |
| `onSpawnProjectiles` | `(projectiles)` | Invoked when the weapon is fired. Provides an array of all spawned projectiles. |

## Enums

### Effectiveness

| Value | Description |
|-------|-------------|
| `No` | Not effective against this target type. |
| `Yes` | Effective against this target type. |
| `Preferred` | Preferred against this target type. |

### Difficulty

| Value | Description |
|-------|-------------|
| `Auto` | Automatically determined from weapon stats. |
| `Easy` | Easy to hit targets with this weapon. |
| `Challenging` | Moderately difficult to hit targets with this weapon. |
| `Hard` | Difficult to hit targets with this weapon. |
| `Impossible` | Nearly impossible to hit targets with this weapon. |

### WeaponRole

| Value | Description |
|-------|-------------|
| `AutoRifle` | Automatic rifle. |
| `Sniper` | Sniper rifle. |
| `Handgun` | Handgun. |
| `Shotgun` | Shotgun. |
| `AutoCannon` | Automatic cannon. |
| `RocketLauncher` | Rocket launcher. |
| `GrenadeLauncher` | Grenade launcher. |
| `MissileLauncher` | Missile launcher. |
| `AntiAir` | Anti-air weapon. |
| `DogfightGuns` | Dogfight guns. |
| `Utility` | Utility weapon. |
| `Grenade` | Grenade. |
| `Mortar` | Mortar. |
| `Melee` | Melee weapon. |
| `SemiAutoRifle` | Semi-automatic rifle. |

### WFollowupSpread

| Property | Type | Description |
|----------|------|-------------|
| `maxSpreadAim` | `float` | Maximum followup spread while aiming. |
| `maxSpreadHip` | `float` | Maximum followup spread from the hip. |
| `spreadDissipateTime` | `float` | The time it takes for followup spread to dissipate. |
| `spreadGain` | `float` | The amount of followup spread gained per shot. |
| `proneMultiplier` | `float` | Multiplier for followup spread gain while prone. |
| `spreadStayTime` | `float` | The time followup spread stays at its maximum before dissipating. |

