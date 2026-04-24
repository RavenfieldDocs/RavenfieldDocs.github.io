---
title: ActorSkin
---

Represents the visual skin for an actor, including character, arm, and kick leg meshes.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `armSkin` | `[MeshSkin](./MeshSkin.md)` | The skin for the actor's arm model. |
| `characterSkin` | `[MeshSkin](./MeshSkin.md)` | The skin for the actor's character model. |
| `kickLegSkin` | `[MeshSkin](./MeshSkin.md)` | The skin for the actor's kick leg model. |
| `name` | `string` | The name of this actor skin. |

## Methods

### Clone

Creates a copy of this actor skin.

[return: ActorSkin]

### ToString

Returns a string representation of this actor skin.

[return: string]

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

### ResolveFirstValidMeshSkin

Returns the first non-null mesh skin from the provided alternatives, falling back to the fallback if all alternatives are null.

| Parameter | Type | Description |
|-----------|------|-------------|
| `alt0` | `[MeshSkin](./MeshSkin.md)` | The first alternative mesh skin, or `nil`. |
| `fallback` | `[MeshSkin](./MeshSkin.md)` | The fallback mesh skin if all alternatives are `nil`. |

[return: MeshSkin]

### ResolveFirstValidMeshSkin

Returns the first non-null mesh skin from the provided alternatives, falling back to the fallback if all alternatives are null.

| Parameter | Type | Description |
|-----------|------|-------------|
| `alt0` | `[MeshSkin](./MeshSkin.md)` | The first alternative mesh skin, or `nil`. |
| `alt1` | `[MeshSkin](./MeshSkin.md)` | The second alternative mesh skin, or `nil`. |
| `fallback` | `[MeshSkin](./MeshSkin.md)` | The fallback mesh skin if all alternatives are `nil`. |

[return: MeshSkin]

## Enums

### EnumName

| Value | Description |
|-------|-------------|
