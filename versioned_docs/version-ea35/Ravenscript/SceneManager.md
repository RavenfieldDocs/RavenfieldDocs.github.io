---
title: SceneManager
---

Provides static methods for managing game scenes, including starting matches and loading menus.

## Properties

| Property | Type | Description |
|----------|------|-------------|

## Methods

## Events

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

### StartMatch

Starts a match with the given map entry, game info, and game mode parameters.

| Parameter | Type | Description |
|-----------|------|-------------|
| `mapEntry` | [MapEntry](./MapEntry.md) | The map entry to load. |
| `info` | [GameInfo](./GameInfo.md) | The game info settings. |
| `parameters` | [GameModeParameters](./GameModeParameters.md) | The game mode parameters. |

### LoadCampaignLobby

Loads the campaign lobby. Throws an exception if no campaign is active.

### LoadMainMenu

Returns to the main menu.

## Enums
