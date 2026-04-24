---
title: ScriptedBehaviour
---

All Ravenscript's are executed and managed by a ScriptedBehaviour component. This component is accessable in Ravenscript through ``self.script``.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `self` | `table` | Gets the script's Lua table aka. ``self``. |
| `mutator` | [Mutator](./Mutator.md) or `nil` | The mutator associated with this ScriptedBehaviour. Returns `nil` if no mutator is associated with this script. |
| `modSaveData` | [SaveData](./SaveData.md) or `nil` | The mod save data associated with this ScriptedBehaviour. Returns `nil` if no mod is associated. |

## Methods

## Events

| Event | Signature | Description |
|-------|-----------|-------------|
| | | |

## Static Fields

| Field | Type | Description |
|-------|------|-------------|
| | | |

## Static Methods

### GetScript

Finds and returns the first ScriptedBehaviour on the GameObject. Equivalent to ``GameObject.GetComponent(ScriptedBehaviour).script``. Nil is returned if none is found.

| Parameter | Type | Description |
|-----------|------|-------------|
| `go` | [GameObject](./GameObject.md) | The GameObject to find the script on. |

[return: [ScriptedBehaviour](./ScriptedBehaviour.md)?]
The ScriptedBehaviour on the GameObject, or `nil` if none is found.

## Enums
