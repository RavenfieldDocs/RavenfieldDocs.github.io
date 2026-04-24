---
title: PortraitGenerator
---

Used to render portrait sprites from actor skins.

## Static Methods

### GetTeamActorPortraitSprite

Get the portrait sprite for the runtime generated actor portrait.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `[Team](./Team.md)` | The team to get the portrait for. |

[return: Sprite]
The portrait sprite.

### RenderTeamPortrait

Renders a portrait using the specified team skin.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | `[Team](./Team.md)` | The team to render the portrait for. |

[return: Texture]
The rendered portrait texture.

### RenderSkinPortrait

Renders a portrait using the specified skin.

| Parameter | Type | Description |
|-----------|------|-------------|
| `mesh` | `Mesh` | The mesh of the skin. |
| `materials` | `Material[]` | The materials of the skin. |
| `teamMaterialIndex` | `int` | The material index for team colors. |
| `team` | `[Team](./Team.md)` | The team to render the portrait for. |

[return: Texture]
The rendered portrait texture.

### SetPortraitRenderOffset

Set a camera offset for the next portrait render.

| Parameter | Type | Description |
|-----------|------|-------------|
| `positionOffset` | `Vector3` | The position offset for the camera. |
| `rotationOffset` | `Quaternion` | The rotation offset for the camera. |

### ResetPortraitRenderOffset

Resets the camera offset for the next portrait render. This is automatically done after rendering any portrait.
