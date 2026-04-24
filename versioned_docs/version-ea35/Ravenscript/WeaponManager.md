---
title: WeaponManager
---

Manages weapons loaded into the game and provides AI weapon picking functionality.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `allWeapons` | [WeaponEntry](./WeaponEntry.md)[] | All weapons loaded into the game. |

## Methods

### GetAiWeaponPrimary

Picks a primary weapon based on the loadout pick strategy. Only picks weapons that are available to the AI and are available for the specified team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `strategy` | [LoadoutPickStrategy](./AiActorController.md#LoadoutPickStrategy) | The loadout pick strategy to use. |
| `team` | ``WTeam`` | The team to pick the weapon for. |

[return: [WeaponEntry](./WeaponEntry.md)]
The picked weapon entry.

### GetAiWeaponSecondary

Picks a secondary weapon based on the loadout pick strategy. Only picks weapons that are available to the AI and are available for the specified team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `strategy` | [LoadoutPickStrategy](./AiActorController.md#LoadoutPickStrategy) | The loadout pick strategy to use. |
| `team` | ``WTeam`` | The team to pick the weapon for. |

[return: [WeaponEntry](./WeaponEntry.md)]
The picked weapon entry.

### GetAiWeaponAllGear

Picks a gear item based on the loadout pick strategy. Only picks weapons that are available to the AI and are available for the specified team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `strategy` | [LoadoutPickStrategy](./AiActorController.md#LoadoutPickStrategy) | The loadout pick strategy to use. |
| `team` | ``WTeam`` | The team to pick the weapon for. |

[return: [WeaponEntry](./WeaponEntry.md)]
The picked weapon entry.

### GetAiWeaponLargeGear

Picks a large gear item based on the loadout pick strategy. Only picks weapons that are available to the AI and are available for the specified team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `strategy` | [LoadoutPickStrategy](./AiActorController.md#LoadoutPickStrategy) | The loadout pick strategy to use. |
| `team` | ``WTeam`` | The team to pick the weapon for. |

[return: [WeaponEntry](./WeaponEntry.md)]
The picked weapon entry.

### GetAiWeaponSmallGear

Picks a small gear item based on the loadout pick strategy. Only picks weapons that are available to the AI and are available for the specified team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `strategy` | [LoadoutPickStrategy](./AiActorController.md#LoadoutPickStrategy) | The loadout pick strategy to use. |
| `team` | ``WTeam`` | The team to pick the weapon for. |

[return: [WeaponEntry](./WeaponEntry.md)]
The picked weapon entry.

### IsWeaponAvailableToTeam

| Parameter | Type | Description |
|-----------|------|-------------|
| `entry` | [WeaponEntry](./WeaponEntry.md) | The weapon entry to check. |
| `team` | ``WTeam`` | The team to check availability for. |

[return: `bool`]
True if the weapon is available to the team.

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

## Enums
