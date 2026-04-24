---
title: GameResult
---

Use these methods to set the game result and end the match.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `winningTeam` | [Team](./Team.md) | The team that won the match. |
| `resultDetails` | [ConfigurationData](./ConfigurationData.md) | The detailed result data from the battle. |

## Methods

### GetWinningTeam

Returns the winning team.

[return: [Team](./Team.md)]
The team that won the match.

### SetWinningTeam

Sets the winning team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | [Team](./Team.md) | The team to set as the winner. |

### SetRemainingCampaignArmies

Set number of remaining campaign armies.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | [Team](./Team.md) | The team to set armies for. |
| `armies` | `int` | The number of remaining armies. |

### GetRemainingCampaignArmies

The remaining campaign armies from the battle.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | [Team](./Team.md) | The team to get armies for. |

[return: int]
The remaining campaign armies.

### GetCampaignArmiesChange

The change in campaign armies from the battle (usually negative!).

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | [Team](./Team.md) | The team to get the army change for. |

[return: int]
The change in campaign armies.

### SetStandardVictory

Sets winning team for game modes that do not support conquest armies.

| Parameter | Type | Description |
|-----------|------|-------------|
| `winningTeam` | [Team](./Team.md) | The team to set as the winner. |

### SetStandardCampaignVictory

Sets winning team and remaining conquest armies.

| Parameter | Type | Description |
|-----------|------|-------------|
| `winningTeam` | [Team](./Team.md) | The team to set as the winner. |
| `blueRemainingArmies` | `int` | Remaining armies for the blue team. |
| `redRemainingArmies` | `int` | Remaining armies for the red team. |

### EndGame

Ends the game with the currently set result.

### EndGameAllowContinue

Ends the game with the currently set result. Allows the game to continue when neverending battles is enabled and playing in instant action mode.

### GetResultDetails

Returns the detailed result data.

[return: [ConfigurationData](./ConfigurationData.md)]
The result details configuration data.

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
