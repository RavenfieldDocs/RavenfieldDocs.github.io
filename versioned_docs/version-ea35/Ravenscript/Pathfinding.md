---
title: Pathfinding
---

Static class for finding pathfinding nodes in the game world.

## Properties

| Property | Type | Description |
|----------|------|-------------|

## Methods

### FindNodes

Finds all pathfinding nodes of a given type within a sphere.

| Parameter | Type | Description |
|-----------|------|-------------|
| `center` | `Vector3` | The center of the sphere. |
| `radius` | `float` | The radius of the sphere. |
| `type` | `PathfindingNodeType` | The type of pathfinding nodes to find. |
| `underWater` | `bool` | Include nodes that are located under water? |

[return: PathfindingNode[]]

### FindNodes

Finds all infantry pathfinding nodes within the given sphere.

| Parameter | Type | Description |
|-----------|------|-------------|
| `center` | `Vector3` | The center of the sphere. |
| `radius` | `float` | The radius of the sphere. |

[return: PathfindingNode[]]

### FindNearestNode

Finds the pathfinding node nearest to the given position.

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The position to search from. |
| `type` | `PathfindingNodeType` | The type of pathfinding nodes to find. |
| `underWater` | `bool` | Include nodes that are located under water? |

[return: PathfindingNode?]
A pathfinding node or nil if none is found.

### FindNearestNode

Finds the pathfinding node nearest to the given position.

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The position to search from. |

[return: PathfindingNode?]
A pathfinding node or nil if none is found.

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

| Method | Signature | Description |
|--------|-----------|-------------|

## Enums

| Enum | Description |
|------|-------------|
