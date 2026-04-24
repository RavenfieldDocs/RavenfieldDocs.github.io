---
title: ColorScheme
---

Use these methods to get the game's color scheme.

## Properties

| Property | Type | Description |
|----------|------|-------------|

## Methods

### SetTeamColor

Sets the team color, also sets the team blood particle color.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | [Team](./Team.md) | The team to set the color for. |
| `color` | [Color](./Color.md) | The color to set. |

### SetTeamBloodColor

Sets the team blood particle color.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | [Team](./Team.md) | The team to set the blood color for. |
| `color` | [Color](./Color.md) | The blood particle color to set. |

### GetTeamColor

Returns the main color of a specific team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | [Team](./Team.md) | The team to get the color for. |

[return: [Color](./Color.md)]

### GetInterfaceColor

Returns a UI-ready color of a specific team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | [Team](./Team.md) | The team to get the color for. |
| `variant` | `ColorVariant` | The color variant to use. |

[return: [Color](./Color.md)]

### GetTeamColorBrighter

Returns a brighter color of a specific team. Useful for UI elements that need to be bright such as text and icons.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | [Team](./Team.md) | The team to get the bright color for. |

[return: [Color](./Color.md)]

### RichTextColorTag

Returns a rich text color tag such as ``<color=blue>`` for a specified color.

| Parameter | Type | Description |
|-----------|------|-------------|
| `color` | [Color](./Color.md) | The color to create a tag for. |

[return: string]

### RichTextColorTag

Returns a rich text color tag such as ``<color=blue>`` for a specified team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `team` | [Team](./Team.md) | The team to create a tag for. |
| `variant` | `ColorVariant` | The color variant to use. |

[return: string]

### FormatTeamColor

Returns a formatted string such as ``<color=blue>innerString</color>`` for a specified team.

| Parameter | Type | Description |
|-----------|------|-------------|
| `innerString` | `string` | The string to wrap in the color tag. |
| `team` | [Team](./Team.md) | The team to use for the color. |
| `variant` | `ColorVariant` | The color variant to use. |

[return: string]

### GetRarityColor

Returns a color of a specific rarity tier.

| Parameter | Type | Description |
|-----------|------|-------------|
| `rarity` | `RarityTier` | The rarity tier to get the color for. |

[return: [Color](./Color.md)]

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

### EnumName

| Value | Description |
|-------|-------------|
