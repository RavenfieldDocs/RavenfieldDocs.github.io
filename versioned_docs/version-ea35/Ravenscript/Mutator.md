---
title: Mutator
---

Represents a mutator entry with its metadata and configuration.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `name` | `string` | The name of the mutator. |
| `description` | `string` | The description of the mutator. |
| `configuration` | [ConfigurationData](./ConfigurationData.md) | The configuration data for this mutator. |

## Methods

### GetConfigurationInt

Gets an integer configuration value by ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |

[return: float]
The integer value as a float.

### GetConfigurationFloat

Gets a float configuration value by ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |

[return: float]
The float value.

### GetConfigurationString

Gets a string configuration value by ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |

[return: string]
The string value.

### GetConfigurationBool

Gets a boolean configuration value by ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |

[return: bool]
The boolean value.

### GetConfigurationRange

Gets a range configuration value by ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |

[return: float]
The range value.

### GetConfigurationDropdown

Gets a dropdown configuration value by ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The configuration field ID. |

[return: int]
The dropdown value.

## Events

| Event | Signature | Description |
|-------|-----------|-------------|
| | | |

## Static Fields

| Field | Type | Description |
|-------|------|-------------|
| | | |

## Static Methods

### GetByName

Finds a mutator by name.

| Parameter | Type | Description |
|-----------|------|-------------|
| `name` | `string` | The name of the mutator to find. |

[return: [Mutator](./Mutator.md)?]
The mutator entry, or `nil` if not found.

## Enums
