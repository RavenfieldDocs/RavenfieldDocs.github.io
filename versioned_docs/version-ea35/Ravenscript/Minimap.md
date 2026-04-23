---
title: Minimap
---

Use this class to access the ingame minimap.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `camera` | `Camera` | The minimap camera of the current level. |
| `texture` | `Texture` | Texture of the rendered level. |
| `actorBlipTexture` | `Texture` | Texture of rendered actor blips excluding player squad. For performance reasons, this texture is not updated every frame. |
| `playerSquadBlipTexture` | `Texture` | Texture of rendered player squad actor blips. Updated every frame. |

## Methods

### SetBlipScale

Sets the scale of blips on the minimap.

| Parameter | Type | Description |
|-----------|------|-------------|
| `actorScale` | `float` | Scale for actor blips. |
| `playerSquadScale` | `float` | Scale for player squad blips. |
| `viewConeScale` | `float` | Scale for the player view cone blip. |

### Render

Render a new minimap texture.

## Events

## Static Fields

## Static Methods

## Enums
