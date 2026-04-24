---
title: ConfigurationData
---

Stores configuration field values by ID, supporting bool, int, float, range, string, and dropdown types. Used for reading and writing game mode configuration settings.

## Properties

| Property | Type | Description |
|----------|------|-------------|

## Methods

### Clear

Clears all stored configuration values.

### Deserialize

Deserializes and stores a configuration field value from a string.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |
| `text` | `string` | The serialized value as a string. |

### GetBool

Gets a boolean configuration value.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |

[return: bool]

### GetDropdown

Gets a dropdown configuration value as an index.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |

[return: int]

### GetFloat

Gets a float configuration value.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |

[return: float]

### GetInt

Gets an integer configuration value.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |

[return: int]

### GetRange

Gets a range configuration value.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |

[return: float]

### GetString

Gets a string configuration value.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |

[return: string]

### HasBool

Checks whether a boolean configuration value exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |

[return: bool]

### HasDropdown

Checks whether a dropdown configuration value exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |

[return: bool]

### HasFloat

Checks whether a float configuration value exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |

[return: bool]

### HasInt

Checks whether an integer configuration value exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |

[return: bool]

### HasRange

Checks whether a range configuration value exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |

[return: bool]

### HasString

Checks whether a string configuration value exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |

[return: bool]

### SerializeField

Serializes a configuration field value to a string.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |

[return: string]

### SetBool

Sets a boolean configuration value.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |
| `value` | `bool` | The value to set. |

### SetDropdown

Sets a dropdown configuration value as an index.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |
| `value` | `int` | The dropdown index to set. |

### SetFloat

Sets a float configuration value.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |
| `value` | `float` | The value to set. |

### SetInt

Sets an integer configuration value.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |
| `value` | `int` | The value to set. |

### SetRange

Sets a range configuration value.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |
| `value` | `float` | The value to set. |

### SetString

Sets a string configuration value.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |
| `value` | `string` | The value to set. |

## Events

## Static Fields

| Field | Type | Description |
|-------|------|-------------|
| `ID_CONQUEST_ARMIES_BLUE` | `string` | The ID `"conquestArmies0"` for conquest mode blue team army count. |
| `ID_CONQUEST_ARMIES_BLUE_CHANGE` | `string` | The ID `"conquestArmies0Change"` for conquest mode blue team army count change. |
| `ID_CONQUEST_ARMIES_RED` | `string` | The ID `"conquestArmies1"` for conquest mode red team army count. |
| `ID_CONQUEST_ARMIES_RED_CHANGE` | `string` | The ID `"conquestArmies1Change"` for conquest mode red team army count change. |
| `ID_GAME_LENGTH` | `string` | The ID `"gameLength"` for game mode game length. |
| `ID_RESPAWN_TIME` | `string` | The ID `"respawnTime"` for game mode respawn time. |
| `ID_TEAM_COUNT_BLUE` | `string` | The ID `"countTeam0"` for blue team actor count. |
| `ID_TEAM_COUNT_RED` | `string` | The ID `"countTeam1"` for red team actor count. |
| `MAX_GAME_LENGTH` | `int` | The maximum game length value, `3`. |

## Static Methods

## Enums
