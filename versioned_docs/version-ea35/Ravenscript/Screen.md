---
title: Screen
---

Provides access to screen-related functionality.

## Static Fields

| Field | Type | Description |
|-------|------|-------------|
| `height` | `float` | The current screen height in pixels. |
| `width` | `float` | The current screen width in pixels. |

## Static Methods

### LockCursor

Undo `UnlockCursor()`. This function only affects the ingame cursor. It does not affect the cursor state when a menu is open, etc.

### UnlockCursor

Unlocks the mouse cursor, typically in order to allow the player to click UI elements. This function only affects the ingame cursor. It does not affect the cursor state when a menu is open, etc.
