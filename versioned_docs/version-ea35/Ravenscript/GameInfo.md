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
| `team` | `Team` | The team to get info for (Blue or Red). |

[return: TeamInfo]
The team info for the specified team.

### SetTeamInfo

Sets team info for the specified team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `Team` | The team to set info for (Blue or Red). |
| `teamInfo` | `TeamInfo` | The team info to set. |

### GetMutators

Gets the active mutators.

[return: MutatorEntryData[]]
The active mutators.

### SetMutators

Sets the active mutators.

| Parameter | Type | Description |
|-----------|------|-------------|
| `mutators` | `MutatorEntryData[]` | The mutators to set as active. |

### ClearMutators

Clears all active mutators.

### AddMutator

Adds a mutator to the active mutators.

| Parameter | Type | Description |
|-----------|------|-------------|
| `mutator` | `MutatorEntryData` | The mutator to add. |

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

[return: GameInfo]
The default GameInfo.

### Clone

Clones an existing GameInfo.

| Parameter | Type | Description |
|-----------|------|-------------|
| `original` | `GameInfo` | The GameInfo to clone. |

[return: GameInfo]
A clone of the GameInfo.

### CreateEmpty

Returns an empty GameInfo.

[return: GameInfo]
An empty GameInfo.

## Enums

| Enum | Description |
|------|-------------|
