---
title: DataContainer
---

Provides access to data assets stored in a mod's data container.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `gameObject` | [GameObject](./GameObject.md) | The underlying [GameObject](./GameObject.md) of the data container. |
| `transform` | [Transform](./Transform.md) | The underlying [Transform](./Transform.md) of the data container. |

## Methods

### GetActorSkin

Gets an actor skin asset by its ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: [ActorSkin](./ActorSkin.md)?]
The actor skin, or `nil` if not found.

### GetActorSkinArray

Gets an array of actor skin assets by their ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: [ActorSkin](./ActorSkin.md)[]]
An array of actor skins.

### GetAnimationCurve

Gets an animation curve asset by its ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: AnimationCurve?]
The animation curve, or `nil` if not found.

### GetAnimationCurveArray

Gets an array of animation curve assets by their ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: AnimationCurve[]]
An array of animation curves.

### GetAudioClip

Gets an audio clip asset by its ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: [AudioClip](./AudioClip.md)?]
The audio clip, or `nil` if not found.

### GetAudioClipArray

Gets an array of audio clip assets by their ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: [AudioClip](./AudioClip.md)[]]
An array of audio clips.

### GetBezierPath

Gets a bezier path asset by its ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: [BezierPath](./BezierPath.md)?]
The bezier path, or `nil` if not found.

### GetBezierPathArray

Gets an array of bezier path assets by their ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: [BezierPath](./BezierPath.md)[]]
An array of bezier paths.

### GetBool

Gets a boolean value by its ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: bool]
The boolean value.

### GetBoolArray

Gets an array of boolean values by their ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: bool[]]
An array of boolean values.

### GetColor

Gets a color asset by its ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: [Color](./Color.md)?]
The color, or `nil` if not found.

### GetColorArray

Gets an array of color assets by their ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: [Color](./Color.md)[]]
An array of colors.

### GetFloat

Gets a float value by its ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: float]
The float value.

### GetFloatArray

Gets an array of float values by their ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: float[]]
An array of float values.

### GetFont

Gets a font asset by its ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: [Font](./Font.md)?]
The font, or `nil` if not found.

### GetFontArray

Gets an array of font assets by their ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: [Font](./Font.md)[]]
An array of fonts.

### GetGameObject

Gets a GameObject asset by its ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: [GameObject](./GameObject.md)?]
The GameObject, or `nil` if not found.

### GetGameObjectArray

Gets an array of GameObject assets by their ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: [GameObject](./GameObject.md)[]]
An array of GameObjects.

### GetGradient

Gets a gradient asset by its ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: Gradient?]
The gradient, or `nil` if not found.

### GetGradientArray

Gets an array of gradient assets by their ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: Gradient[]]
An array of gradients.

### GetInt

Gets an integer value by its ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: int]
The integer value.

### GetIntArray

Gets an array of integer values by their ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: int[]]
An array of integer values.

### GetMaterial

Gets a material asset by its ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: Material?]
The material, or `nil` if not found.

### GetMaterialArray

Gets an array of material assets by their ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: Material[]]
An array of materials.

### GetPrefabs

Gets all prefab GameObjects in the data container.

[return: [GameObject](./GameObject.md)[]]
An enumerable of prefab GameObjects.

### GetRotation

Gets a rotation (Quaternion) asset by its ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: Quaternion?]
The rotation, or `nil` if not found.

### GetRotationArray

Gets an array of rotation assets by their ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: Quaternion[]]
An array of rotations.

### GetSprite

Gets a sprite asset by its ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: Sprite?]
The sprite, or `nil` if not found.

### GetSpriteArray

Gets an array of sprite assets by their ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: Sprite[]]
An array of sprites.

### GetString

Gets a string value by its ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: string?]
The string value, or `nil` if not found.

### GetStringArray

Gets an array of string values by their ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: string[]]
An array of string values.

### GetTexture

Gets a texture asset by its ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: Texture?]
The texture, or `nil` if not found.

### GetTextureArray

Gets an array of texture assets by their ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: Texture[]]
An array of textures.

### GetWeaponEntry

Gets a weapon entry asset by its ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: [WeaponEntry](./WeaponEntry.md)?]
The weapon entry, or `nil` if not found.

### GetWeaponEntryArray

Gets an array of weapon entry assets by their ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: [WeaponEntry](./WeaponEntry.md)[]]
An array of weapon entries.

### GetVector

Gets a Vector3 value by its ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: Vector3?]
The vector, or `nil` if not found.

### GetVectorArray

Gets an array of Vector3 values by their ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: Vector3[]]
An array of vectors.

### GetVideoClip

Gets a video clip asset by its ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: VideoClip?]
The video clip, or `nil` if not found.

### GetVideoClipArray

Gets an array of video clip assets by their ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: VideoClip[]]
An array of video clips.

### HasActorSkin

Checks whether an actor skin asset with the given ID exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: bool]
`true` if the asset exists.

### HasAnimationCurve

Checks whether an animation curve asset with the given ID exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: bool]
`true` if the asset exists.

### HasAudioClip

Checks whether an audio clip asset with the given ID exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: bool]
`true` if the asset exists.

### HasBezierPath

Checks whether a bezier path asset with the given ID exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: bool]
`true` if the asset exists.

### HasBool

Checks whether a boolean value with the given ID exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: bool]
`true` if the value exists.

### HasColor

Checks whether a color asset with the given ID exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: bool]
`true` if the asset exists.

### HasFloat

Checks whether a float value with the given ID exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: bool]
`true` if the value exists.

### HasFont

Checks whether a font asset with the given ID exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: bool]
`true` if the asset exists.

### HasGradient

Checks whether a gradient asset with the given ID exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: bool]
`true` if the asset exists.

### HasInt

Checks whether an integer value with the given ID exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: bool]
`true` if the value exists.

### HasMaterial

Checks whether a material asset with the given ID exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: bool]
`true` if the asset exists.

### HasObject

Checks whether any asset with the given ID exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: bool]
`true` if any asset with this ID exists.

### HasRotation

Checks whether a rotation asset with the given ID exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: bool]
`true` if the asset exists.

### HasSprite

Checks whether a sprite asset with the given ID exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: bool]
`true` if the asset exists.

### HasString

Checks whether a string value with the given ID exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: bool]
`true` if the value exists.

### HasTexture

Checks whether a texture asset with the given ID exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: bool]
`true` if the asset exists.

### HasWeaponEntry

Checks whether a weapon entry asset with the given ID exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: bool]
`true` if the asset exists.

### HasVector

Checks whether a vector value with the given ID exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: bool]
`true` if the value exists.

### HasVideoClip

Checks whether a video clip asset with the given ID exists.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `string` | The asset ID. |

[return: bool]
`true` if the asset exists.

### ToString

Returns a string representation of the data container.

[return: string]
A string describing the data container.

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
