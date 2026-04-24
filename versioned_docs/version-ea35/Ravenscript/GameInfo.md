---
title: GameInfo
---

Represents game configuration including team info and active mutators.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| | | |

## Methods

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

### GetMutators

Gets the active mutators.

[return: [MutatorEntryData](./MutatorEntryData.md)[]]
The active mutators.

### SetMutators

Sets the active mutators.

| Parameter | Type | Description |
|-----------|------|-------------|
| `mutators` | [MutatorEntryData](./MutatorEntryData.md)[] | The mutators to set as active. |

### ClearMutators

Clears all active mutators.

### AddMutator

Adds a mutator to the active mutators.

| Parameter | Type | Description |
|-----------|------|-------------|
| `mutator` | [MutatorEntryData](./MutatorEntryData.md) | The mutator to add. |

## Events

| Event | Signature | Description |
|-------|-----------|-------------|
| | | |

## Static Fields

| Field | Type | Description |
|-------|------|-------------|
| | | |

## Static Methods

### GetDefault

Returns the default GameInfo for the current loaded mods.

[return: [GameInfo](./GameInfo.md)]
The default GameInfo.

### Clone

Clones an existing GameInfo.

| Parameter | Type | Description |
|-----------|------|-------------|
| `original` | [GameInfo](./GameInfo.md) | The GameInfo to clone. |

[return: [GameInfo](./GameInfo.md)]
A clone of the GameInfo.

### CreateEmpty

Returns an empty GameInfo.

[return: [GameInfo](./GameInfo.md)]
An empty GameInfo.

## Enums

| Enum | Description |
|------|-------------|
