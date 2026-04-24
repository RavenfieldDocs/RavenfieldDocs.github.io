---
title: GameModeParameters
---

Represents the parameters for a game mode, including team configuration, respawn time, game length, and other settings.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `configuration` | [ConfigurationData](./ConfigurationData.md) | The configuration data for this game mode. |
| `gameMode` | [GameModeInfo](./GameModeInfo.md) | The game mode info this parameters object was created for. |
| `nightMode` | `bool` | Whether night mode is enabled. |
| `playerHasAllWeapons` | `bool` | Whether the player has all weapons available. |
| `playerTeam` | `WTeam` | The team the player is assigned to. |

## Methods

### CreateForGameMode

Creates a new GameModeParameters instance for the specified game mode.

| Parameter | Type | Description |
|-----------|------|-------------|
| `info` | [GameModeInfo](./GameModeInfo.md) | The game mode info to create parameters for. |

[return: [GameModeParameters](./GameModeParameters.md)]
A new GameModeParameters instance.

### GetCampaignArmies

Gets the number of armies for the specified team in campaign mode.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `WTeam` | The team to get the army count for. |

[return: int]
The number of armies for the specified team.

### GetGameLength

Gets the game length setting.

[return: int]
The game length value (0-3).

### GetRespawnTime

Gets the respawn time in seconds.

[return: float]
The respawn time in seconds.

### GetTeamCount

Gets the number of bots on the specified team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `WTeam` | The team to get the count for. |

[return: int]
The number of bots on the specified team.

### SetGameLength

Sets the game length setting.

| Parameter | Type | Description |
|-----------|------|-------------|
| `gameLength` | `int` | The game length value (0-3). |

### SetRecommendedTeamCount

Sets the team counts based on the map's suggested bot count.

| Parameter | Type | Description |
|-----------|------|-------------|
| `mapEntry` | [MapEntryData](./MapEntryData.md) | The map entry to get the suggested bot count from. |

### SetRecommendedTeamCount

Sets the team counts based on the map's suggested bot count, clamped to the specified range.

| Parameter | Type | Description |
|-----------|------|-------------|
| `mapEntry` | [MapEntryData](./MapEntryData.md) | The map entry to get the suggested bot count from. |
| `minCount` | `int` | The minimum team count. |
| `maxCount` | `int` | The maximum team count. |

### SetRespawnTime

Sets the respawn time in seconds.

| Parameter | Type | Description |
|-----------|------|-------------|
| `respawnTime` | `float` | The respawn time in seconds. |

### SetTeamCount

Sets the number of bots on the specified team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `WTeam` | The team to set the count for. |
| `count` | `int` | The number of bots. |

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

| Method | Signature | Description |
|--------|-----------|-------------|

## Enums

| Enum | Description |
|------|-------------|
