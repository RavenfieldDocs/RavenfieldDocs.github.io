---
title: PlayerHud
---

Use these methods to change the player HUD.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `hudGameModeEnabled` | `bool` | Controls visibility of the game mode hud. |
| `hudPlayerEnabled` | `bool` | Controls visibility of the player hud. |
| `uiElementsLeft` | `IngameUI.UIElement[]` | The elements shown on the left side of the player hud. |
| `uiElementsRight` | `IngameUI.UIElement[]` | The elements shown on the right side of the player hud. |
| `killCameraEnabled` | `bool` | Controls the Killed By sequence. |

## Methods

### GetPlayerOrderState

The current player squad order state. This value is used to display the state info text label in the HUD.

[return: `IngameUI.PlayerOrderState`]

### ShowUIElement

Controls visibility of individual UI elements of the player hud.

| Parameter | Type | Description |
|-----------|------|-------------|
| `element` | `IngameUI.UIElement` | The UI element to show. |

### HideUIElement

Controls visibility of individual UI elements of the player hud.

| Parameter | Type | Description |
|-----------|------|-------------|
| `element` | `IngameUI.UIElement` | The UI element to hide. |

### RegisterElementTracking

Makes the rectElement automatically follow the transform position. This is done by modifying the anchoredPosition value of the Rect Transform. Please make sure that the rectElement is a child to a canvas object, and that its Anchor Min/Max values are set to 0. Returns the tracker ID.

| Parameter | Type | Description |
|-----------|------|-------------|
| `transform` | `Transform` | The transform to follow. |
| `rectElement` | `RectTransform` | The UI element to track. |
| `activateWhenVisible` | `GameObject` | GameObject to activate when the element is visible. |

[return: `int`]

### RegisterElementTracking

Makes the rectElement automatically follow the transform position with an offset.

| Parameter | Type | Description |
|-----------|------|-------------|
| `transform` | `Transform` | The transform to follow. |
| `localOffset` | `Vector3` | Local offset from the transform position. |
| `rectElement` | `RectTransform` | The UI element to track. |
| `activateWhenVisible` | `GameObject` | GameObject to activate when the element is visible. |

[return: `int`]

### RegisterElementTracking

Makes the rectElement automatically follow the actor.

| Parameter | Type | Description |
|-----------|------|-------------|
| `actor` | `[Actor](./Actor.md)` | The actor to follow. |
| `rectElement` | `RectTransform` | The UI element to track. |
| `activateWhenVisible` | `GameObject` | GameObject to activate when the element is visible. |

[return: `int`]

### RegisterElementTracking

Makes the rectElement automatically follow the actor with a world offset.

| Parameter | Type | Description |
|-----------|------|-------------|
| `actor` | `[Actor](./Actor.md)` | The actor to follow. |
| `worldOffset` | `Vector3` | World space offset from the actor position. |
| `rectElement` | `RectTransform` | The UI element to track. |
| `activateWhenVisible` | `GameObject` | GameObject to activate when the element is visible. |

[return: `int`]

### RegisterElementTracking

Makes the rectElement automatically follow the worldPosition.

| Parameter | Type | Description |
|-----------|------|-------------|
| `worldPosition` | `Vector3` | The world position to follow. |
| `rectElement` | `RectTransform` | The UI element to track. |
| `activateWhenVisible` | `GameObject` | GameObject to activate when the element is visible. |

[return: `int`]

### ClampElementTracking

Clamps the tracked element to the screen inside a border of size clampSize in pixels.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `int` | The tracking ID returned by RegisterElementTracking. |
| `clampSize` | `float` | The border size in pixels. |
| `activateWhenClamped` | `GameObject` | GameObject to activate when the element is clamped. |
| `deactivateWhenClamped` | `GameObject` | GameObject to deactivate when the element is clamped. |

### RemoveElementTracking

Removes tracking from the specified tracking ID. Returns true on successful removal.

| Parameter | Type | Description |
|-----------|------|-------------|
| `id` | `int` | The tracking ID to remove. |

[return: `bool`]

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

### IngameUI.PlayerOrderState

| Value | Description |
|-------|-------------|
| `Follow` | The squad is following the player. |
| `Goto` | The squad is ordered to go to a location. |
| `Hold` | The squad is ordered to hold position. |

### IngameUI.UIElement

| Value | Description |
|-------|-------------|
| `PlayerHealth` | The player health display. |
| `VehicleInfo` | Vehicle information display. |
| `VehicleRepairInfo` | Vehicle repair information display. |
| `SquadMemberInfo` | Squad member information display. |
| `SquadOrderLabel` | Squad order label display. |
| `WeaponInfo` | Weapon information display. |
| `DamageVignette` | Damage vignette effect. |
| `DamageDirectionInfo` | Damage direction indicator. |
| `Hitmarker` | Hitmarker display. |
| `FlagCaptureProgress` | Flag capture progress display. |
| `OverlayText` | Overlay text display. |
| `KillFeed` | Kill feed display. |
