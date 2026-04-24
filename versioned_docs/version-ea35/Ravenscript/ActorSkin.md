---
title: ActorSkin
---

Represents the visual skin for an actor, including character, arm, and kick leg meshes.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `armSkin` | ``MeshSkin`` | The skin for the actor's arm model. |
| `characterSkin` | ``MeshSkin`` | The skin for the actor's character model. |
| `kickLegSkin` | ``MeshSkin`` | The skin for the actor's kick leg model. |
| `name` | `string` | The name of this actor skin. |

## Methods

### Clone

Creates a copy of this actor skin.

[return: [ActorSkin](./ActorSkin.md)]

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
| `alt0` | ``MeshSkin`` | The first alternative mesh skin, or `nil`. |
| `fallback` | ``MeshSkin`` | The fallback mesh skin if all alternatives are `nil`. |

[return: MeshSkin]

### ResolveFirstValidMeshSkin

Returns the first non-null mesh skin from the provided alternatives, falling back to the fallback if all alternatives are null.

| Parameter | Type | Description |
|-----------|------|-------------|
| `alt0` | ``MeshSkin`` | The first alternative mesh skin, or `nil`. |
| `alt1` | ``MeshSkin`` | The second alternative mesh skin, or `nil`. |
| `fallback` | ``MeshSkin`` | The fallback mesh skin if all alternatives are `nil`. |

[return: MeshSkin]

## Enums

### EnumName

| Value | Description |
|-------|-------------|
