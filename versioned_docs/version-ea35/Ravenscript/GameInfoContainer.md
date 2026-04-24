---
title: GameInfoContainer
---

Represents game configuration including team info and active mutators. Exposed as `GameInfo` in Lua.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `mutators` | `MutatorEntryData[]` | The active mutators. |

## Methods

### AddMutator

Adds a mutator to the active mutators.

| Parameter | Type | Description |
|-----------|------|-------------|
| `mutator` | `MutatorEntryData` | The mutator to add. |

### ClearMutators

Clears all active mutators.

### GetTeamInfo

Gets team info for the specified team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `Team` | The team to get info for (Blue or Red). |

[return: TeamInfo]
The team info for the specified team.

### SetTeamInfo

Sets team info for the specified team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `Team` | The team to set info for (Blue or Red). |
| `teamInfo` | `[TeamInfo](./TeamInfo.md)` | The team info to set. |

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
| `original` | `GameInfoContainer` | The GameInfoContainer to clone. |

[return: GameInfoContainer]
A clone of the GameInfoContainer.

### CreateEmpty

Returns an empty GameInfoContainer.

[return: GameInfoContainer]
An empty GameInfoContainer.

### GetDefault

Returns the default GameInfoContainer for the current loaded mods.

[return: GameInfoContainer]
The default GameInfoContainer.

## Enums
