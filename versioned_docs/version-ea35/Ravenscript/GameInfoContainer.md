---
title: GameInfoContainer
---

Represents game configuration including team info and active mutators. Exposed as `GameInfo` in Lua.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `mutators` | [MutatorEntryData](./MutatorEntryData.md)[] | The active mutators. |

## Methods

### AddMutator

Adds a mutator to the active mutators.

| Parameter | Type | Description |
|-----------|------|-------------|
| `mutator` | [MutatorEntryData](./MutatorEntryData.md) | The mutator to add. |

### ClearMutators

Clears all active mutators.

### GetTeamInfo

Gets team info for the specified team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | [Team](./Team.md) | The team to get info for (Blue or Red). |

[return: [TeamInfo](./TeamInfo.md)]
The team info for the specified team.

### SetTeamInfo

Sets team info for the specified team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | [Team](./Team.md) | The team to set info for (Blue or Red). |
| `teamInfo` | [TeamInfo](./TeamInfo.md) | The team info to set. |

## Events

| Event | Signature | Description |
|-------|-----------|-------------|
| | | |

## Static Fields

| Field | Type | Description |
|-------|------|-------------|
| | | |

## Static Methods

### Clone

Clones an existing GameInfoContainer.

| Parameter | Type | Description |
|-----------|------|-------------|
| `original` | [GameInfoContainer](./GameInfoContainer.md) | The GameInfoContainer to clone. |

[return: [GameInfoContainer](./GameInfoContainer.md)]
A clone of the GameInfoContainer.

### CreateEmpty

Returns an empty GameInfoContainer.

[return: [GameInfoContainer](./GameInfoContainer.md)]
An empty GameInfoContainer.

### GetDefault

Returns the default GameInfoContainer for the current loaded mods.

[return: [GameInfoContainer](./GameInfoContainer.md)]
The default GameInfoContainer.

## Enums
