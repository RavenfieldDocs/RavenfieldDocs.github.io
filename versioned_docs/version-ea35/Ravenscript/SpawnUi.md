---
title: SpawnUi
---

Use this class to control the loadout and deployment UI.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `isOpen` | `bool` |  |
| `hasBeenOpen` | `bool` | True if the UI has been open at least once this game. |
| `hasBeenClosed` | `bool` | True if the UI has been closed at least once this game. |
| `playerCanSelectSpawnPoint` | `bool` | True if the player can select their spawn point from the loadout minimap. |
| `selectedSpawnPoint` | [SpawnPoint](./SpawnPoint.md) |  |

## Methods

### Open

Opens the UI.

### OpenBattlePlan

Opens the UI in battle plan mode.

### Close

Closes the UI.

### SetLoadoutVisible

Show or hide the loadout section.

| Parameter | Type | Description |
|-----------|------|-------------|
| `visible` | `bool` |  |

### SetMinimapVisible

Show or hide the minimap/deploy section.

| Parameter | Type | Description |
|-----------|------|-------------|
| `visible` | `bool` |  |

### SetLoadoutOverride

Override the loadout section of the UI.

| Parameter | Type | Description |
|-----------|------|-------------|
| `loadout` | [GameObject](./GameObject.md) |  |

### SetMinimapOverride

Override the minimap section of the UI.

| Parameter | Type | Description |
|-----------|------|-------------|
| `minimap` | [GameObject](./GameObject.md) |  |

### SetSelectedSpawnPoint

Sets the player selected spawn point. If set to nil, the player will not automatically spawn.

| Parameter | Type | Description |
|-----------|------|-------------|
| `spawnPoint` | [SpawnPoint](./SpawnPoint.md) |  |

### GetSelectedSpawnPoint

Returns the player selected spawn point.

[return: [SpawnPoint](./SpawnPoint.md)?]

## Events

## Static Fields

## Static Methods

## Enums
