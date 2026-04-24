---
title: MapMetaData
---

Contains metadata about a map, including its display name, suggested bot count, vehicle availability, biome, terrain, and decorator type.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `displayName` | `string` | The display name of the map. |
| `hasAirVehicles` | `bool` | Whether the map has air vehicles. |
| `hasBuiltInGameMode` | `bool` | Whether the map has a built-in game mode. |
| `hasGroundVehicles` | `bool` | Whether the map has ground vehicles. |
| `hasNavalVehicles` | `bool` | Whether the map has naval vehicles. |
| `mapBiome` | `[MapBiome](#mapbiome)` | The biome type of the map. |
| `mapDecorator` | `[MapDecorator](#mapdecorator)` | The decorator type of the map. |
| `mapTerrain` | `[MapTerrain](#mapterrain)` | The terrain type of the map. |
| `suggestedBots` | `int` | The suggested number of bots for this map. |

## Methods

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

## Enums

### MapBiome

| Value | Description |
|-------|-------------|
| `Unknown` | Unknown biome. |
| `Grass` | Grass biome. |
| `Desert` | Desert biome. |
| `Jungle` | Jungle biome. |
| `Snow` | Snow biome. |
| `Gloom` | Gloom biome. |

### MapTerrain

| Value | Description |
|-------|-------------|
| `Unknown` | Unknown terrain. |
| `Plains` | Plains terrain. |
| `Forest` | Forest terrain. |
| `Mountains` | Mountains terrain. |
| `Coastline` | Coastline terrain. |
| `Island` | Island terrain. |
| `Ocean` | Ocean terrain. |

### MapDecorator

| Value | Description |
|-------|-------------|
| `Unknown` | Unknown decorator. |
| `Nothing` | No decorator. |
| `Settlement` | Settlement decorator. |
| `City` | City decorator. |
| `Airport` | Airport decorator. |
| `Factory` | Factory decorator. |
| `Base` | Base decorator. |
| `Temple` | Temple decorator. |
