---
title: MutatorEntryData
---

Represents data for a mutator entry, including its name, description, and configuration options.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `name` | `string` | The name of the mutator. |
| `description` | `string` | The description of the mutator. |
| `configuration` | `[ConfigurationData](./ConfigurationData.md)` | The configuration data for the mutator. |

## Methods

### GetConfigurationBool

Gets a boolean configuration value by its ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The ID of the configuration option. |

[return: bool]

### GetConfigurationDropdown

Gets a dropdown configuration value by its ID as the selected index.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The ID of the configuration option. |

[return: int]

### GetConfigurationFloat

Gets a float configuration value by its ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The ID of the configuration option. |

[return: float]

### GetConfigurationInt

Gets an integer configuration value by its ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The ID of the configuration option. |

[return: float]

### GetConfigurationRange

Gets a range configuration value by its ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The ID of the configuration option. |

[return: float]

### GetConfigurationString

Gets a string configuration value by its ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The ID of the configuration option. |

[return: string]

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

### GetByName

Retrieves a mutator entry by its name.

| Parameter | Type | Description |
|-----------|------|-------------|
| `name` | `string` | The name of the mutator to find. |

[return: MutatorEntryData?]

## Enums
