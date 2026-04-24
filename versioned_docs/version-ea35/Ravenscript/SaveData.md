---
title: SaveData
---

Provides access to persistent save data, allowing storage and retrieval of values across game sessions.

## Properties

| Property | Type | Description |
|----------|------|-------------|

## Methods

### GetBool

Retrieves a boolean value from save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to look up. |

[return: `bool`]

### GetBoolArray

Retrieves an array of booleans from save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to look up. |

[return: `bool[]`]

### GetFloat

Retrieves a float value from save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to look up. |

[return: `float`]

### GetFloatArray

Retrieves an array of floats from save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to look up. |

[return: `float[]`]

### GetInteger

Retrieves an integer value from save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to look up. |

[return: `int`]

### GetIntegerArray

Retrieves an array of integers from save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to look up. |

[return: `int[]`]

### GetMapEntry

Retrieves a map entry from save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to look up. |

[return: `[MapEntryData](./MapEntryData.md)?`]

### GetMapEntryArray

Retrieves an array of map entries from save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to look up. |

[return: `MapEntryData[]`]

### GetString

Retrieves a string value from save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to look up. |

[return: `string`]

### GetStringArray

Retrieves an array of strings from save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to look up. |

[return: `string[]`]

### GetWeaponEntry

Retrieves a weapon entry from save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to look up. |

[return: `[WeaponEntry](./WeaponEntry.md)?`]

### GetWeaponEntryArray

Retrieves an array of weapon entries from save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to look up. |

[return: `WeaponManager.WeaponEntry[]`]

### GetVehicleInfo

Retrieves vehicle info from save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to look up. |

[return: `[VehicleInfo](./VehicleInfo.md)?`]

### GetVehicleInfoArray

Retrieves an array of vehicle info from save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to look up. |

[return: `VehicleInfo[]`]

### HasBool

Checks whether a boolean value exists in save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to check. |

[return: `bool`]

### HasFloat

Checks whether a float value exists in save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to check. |

[return: `bool`]

### HasInteger

Checks whether an integer value exists in save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to check. |

[return: `bool`]

### HasMapEntry

Checks whether a map entry exists in save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to check. |

[return: `bool`]

### HasString

Checks whether a string value exists in save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to check. |

[return: `bool`]

### HasWeaponEntry

Checks whether a weapon entry exists in save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to check. |

[return: `bool`]

### HasVehicleInfo

Checks whether vehicle info exists in save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to check. |

[return: `bool`]

### StoreBool

Stores a boolean value in save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to store under. |
| `value` | `bool` | The value to store. |

### StoreBoolArray

Stores an array of booleans in save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to store under. |
| `values` | `bool[]` | The values to store. |

### StoreFloat

Stores a float value in save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to store under. |
| `value` | `float` | The value to store. |

### StoreFloatArray

Stores an array of floats in save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to store under. |
| `values` | `float[]` | The values to store. |

### StoreInteger

Stores an integer value in save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to store under. |
| `value` | `int` | The value to store. |

### StoreIntegerArray

Stores an array of integers in save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to store under. |
| `values` | `int[]` | The values to store. |

### StoreMapEntry

Stores a map entry in save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to store under. |
| `value` | `[MapEntryData](./MapEntryData.md)?` | The value to store. |

### StoreMapEntryArray

Stores an array of map entries in save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to store under. |
| `values` | `MapEntryData[]` | The values to store. |

### StoreString

Stores a string value in save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to store under. |
| `value` | `string` | The value to store. |

### StoreStringArray

Stores an array of strings in save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to store under. |
| `values` | `string[]` | The values to store. |

### StoreWeaponEntry

Stores a weapon entry in save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to store under. |
| `value` | `[WeaponEntry](./WeaponEntry.md)?` | The value to store. |

### StoreWeaponEntryArray

Stores an array of weapon entries in save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to store under. |
| `values` | `WeaponManager.WeaponEntry[]` | The values to store. |

### StoreVehicleInfo

Stores vehicle info in save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to store under. |
| `value` | `[VehicleInfo](./VehicleInfo.md)?` | The value to store. |

### StoreVehicleInfoArray

Stores an array of vehicle info in save data.

| Parameter | Type | Description |
|-----------|------|-------------|
| `key` | `string` | The key to store under. |
| `values` | `VehicleInfo[]` | The values to store. |

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

## Enums
