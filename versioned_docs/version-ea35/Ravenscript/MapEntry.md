---
title: MapEntry
---

Represents a map entry containing map metadata and related information.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `displayName` | `string` | The display name of the map. Use this when displaying the map name. This is the same as accessing the map metadata display name. |
| `metaData` | [MapMetaData](./MapMetaData.md) | The map metadata. |

## Methods

### LoadMapImageTexture

Loads the map image as a texture.

[return: `Texture?`]

### LoadMapImageSprite

Loads the map image as a sprite.

[return: `Sprite?`]

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

### FromName

Attempts to resolve the map entry by name.

| Parameter | Type | Description |
|-----------|------|-------------|
| `name` | `string` | The name of the map to resolve. |

[return: [MapEntry](./MapEntry.md)?]
Returns the map entry if found, or `nil` if no map with the name is found.

## Enums
