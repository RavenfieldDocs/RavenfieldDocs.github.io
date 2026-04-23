---
title: GameManager
---

Use these methods to access game configuration.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `buildNumber` | `int` | Gets the build number. Running this on EA Build 20 returns 20. |
| `isBetaBuild` | `bool` | Returns `true` if the game build is tagged as beta. |
| `isNightMode` | `bool` | Returns `true` if the current match is set at night. |
| `isLegitimate` | `bool` | Returns `true` if the game is considered running on a legitimate copy of the game. Please note that this value can never be considered 100% accurate and may yield false positives and false negatives. |
| `isTestingContentMod` | `bool` | Returns `true` while the game is running in mod testing mode. This is useful for reducing startup durations, etc when developing a mod. |
| `gameDifficulty` | `GameDifficulty` | The current game difficulty selected via the options menu. |
| `hudGameModeEnabled` | `bool` | Controls visibility of the game mode hud. |
| `hudPlayerEnabled` | `bool` | Controls visibility of the player hud. |
| `isPaused` | `bool` | Returns `true` if the game is currently paused. |
| `currentGameModeName` | `string` | The name of the currently active game mode, or an empty string if not in a match. |
| `gameModeParameters` | `GameModeParameters` | The parameters for the current game mode, or `nil` if not in a match. |
| `sceneName` | `string` | The name of the current active scene. |
| `mapDisplayName` | `string` | The display name of the current or last map. |

## Methods

### GetTeamName

Returns the team name.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `Team` | The team to get the name for. |

[return: string]
The team name.

### GetRichTextColorTeamName

Returns the team name with a rich text color tag. Example: ``<color=blue>EAGLE</color>``

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `Team` | The team to get the name for. |
| `variant` | `ColorVariant` | The color variant (Default, Bright, or Dark). |

[return: string]
The team name wrapped in a rich text color tag.

### SetTeamName

Sets the team name.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `Team` | The team to set the name for. |
| `name` | `string` | The new team name. |

### LoadSceneByName

Loads a scene by name. Include `.rfl` or `.rfld` extension to load custom maps.

| Parameter | Type | Description |
|-----------|------|-------------|
| `name` | `string` | The name of the scene or map to load. |

## Events

| Event | Signature | Description |
|-------|-----------|-------------|
| | | |

## Static Fields

| Field | Type | Description |
|-------|------|-------------|
| | | |

## Static Methods

## Enums
