---
title: NeighbourManager
---

Provides utilities for querying land and water connections between SpawnPoints.

## Properties

| Property | Type | Description |
|----------|------|-------------|

## Methods

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

### HasLandConnection

Returns true if there is a direct land connection between the two SpawnPoints. Indirect connection, through other SpawnPoints, are not tested.

| Parameter | Type | Description |
|-----------|------|-------------|
| `a` | [SpawnPoint](./SpawnPoint.md) | The first SpawnPoint. |
| `b` | [SpawnPoint](./SpawnPoint.md) | The second SpawnPoint. |

[return: bool]
`true` if there is a direct land connection between the two SpawnPoints.

### HasWaterConnection

Returns true if there is a direct water connection between the two SpawnPoints. Indirect connection, through other SpawnPoints, are not tested.

| Parameter | Type | Description |
|-----------|------|-------------|
| `a` | [SpawnPoint](./SpawnPoint.md) | The first SpawnPoint. |
| `b` | [SpawnPoint](./SpawnPoint.md) | The second SpawnPoint. |

[return: bool]
`true` if there is a direct water connection between the two SpawnPoints.

### GetAllNeighbours

Returns all SpawnPoint neighbours including disabled ones.

| Parameter | Type | Description |
|-----------|------|-------------|
| `spawnPoint` | [SpawnPoint](./SpawnPoint.md) | The SpawnPoint to get neighbours for. |

[return: [SpawnPoint](./SpawnPoint.md)[]]
All SpawnPoint neighbours including disabled ones.

## Enums
