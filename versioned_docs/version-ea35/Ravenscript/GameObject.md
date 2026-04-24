---
title: GameObject
---

Represents a Unity GameObject in the Ravenscript API. Provides access to object properties, component retrieval, instantiation, destruction, and scene search operations.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `activeInHierarchy` | `bool` | Returns `true` if the GameObject is active in the scene hierarchy. Read-only. |
| `activeSelf` | `bool` | Returns `true` if the GameObject is active, regardless of the hierarchy. Read-only. |
| `layer` | `int` | The layer of the GameObject. |
| `tag` | `string` | The tag of the GameObject. |
| `name` | `string` | The name of the GameObject. |
| `transform` | [Transform](./Transform.md) | The Transform component attached to this GameObject. Read-only. |
| `gameObject` | [GameObject](./GameObject.md) | Returns this GameObject itself. Read-only. |

## Methods

### CompareTag

Checks whether this GameObject has the specified tag.

| Parameter | Type | Description |
|-----------|------|-------------|
| `tag` | `string` | The tag to compare against. |

[return: bool]
`true` if the GameObject's tag matches.

### SetActive

Sets the active state of the GameObject.

| Parameter | Type | Description |
|-----------|------|-------------|
| `value` | `bool` | The new active state. |

### GetComponent

Retrieves a component of the specified type from this GameObject.

| Parameter | Type | Description |
|-----------|------|-------------|
| `prototype` | `Table` | A Lua table prototype representing the component type, or an object type. |

[return: any?]
The component if found, or `nil`.

### GetComponentInChildren

Retrieves a component of the specified type from this GameObject or any of its children.

| Parameter | Type | Description |
|-----------|------|-------------|
| `prototype` | `Table` | A Lua table prototype representing the component type, or an object type. |

[return: any?]
The component if found, or `nil`.

### GetComponentInParent

Retrieves a component of the specified type from this GameObject or any of its parents.

| Parameter | Type | Description |
|-----------|------|-------------|
| `prototype` | `Table` | A Lua table prototype representing the component type, or an object type. |

[return: any?]
The component if found, or `nil`.

### GetComponents

Retrieves all components of the specified type from this GameObject.

| Parameter | Type | Description |
|-----------|------|-------------|
| `prototype` | `Table` | A Lua table prototype representing the component type, or an object type. |

[return: any[]]
An array of components.

### GetComponentsInChildren

Retrieves all components of the specified type from this GameObject or any of its children.

| Parameter | Type | Description |
|-----------|------|-------------|
| `prototype` | `Table` | A Lua table prototype representing the component type, or an object type. |

[return: any[]]
An array of components.

### GetComponentsInParent

Retrieves all components of the specified type from this GameObject or any of its parents.

| Parameter | Type | Description |
|-----------|------|-------------|
| `prototype` | `Table` | A Lua table prototype representing the component type, or an object type. |

[return: any[]]
An array of components.

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

### Instantiate

Creates a copy of a GameObject prefab.

| Parameter | Type | Description |
|-----------|------|-------------|
| `prefab` | [GameObject](./GameObject.md) | The prefab to instantiate. |

[return: [GameObject](./GameObject.md)]
The instantiated GameObject.

### Instantiate

Creates a copy of a GameObject prefab with a specified parent.

| Parameter | Type | Description |
|-----------|------|-------------|
| `prefab` | [GameObject](./GameObject.md) | The prefab to instantiate. |
| `parent` | [Transform](./Transform.md) | The parent Transform. |

[return: [GameObject](./GameObject.md)]
The instantiated GameObject.

### Instantiate

Creates a copy of a GameObject prefab at a specified position and rotation.

| Parameter | Type | Description |
|-----------|------|-------------|
| `prefab` | [GameObject](./GameObject.md) | The prefab to instantiate. |
| `position` | `Vector3` | The world position. |
| `rotation` | `Quaternion` | The world rotation. |

[return: [GameObject](./GameObject.md)]
The instantiated GameObject.

### Instantiate

Creates a copy of a GameObject prefab at a specified position and rotation with a parent.

| Parameter | Type | Description |
|-----------|------|-------------|
| `prefab` | [GameObject](./GameObject.md) | The prefab to instantiate. |
| `position` | `Vector3` | The world position. |
| `rotation` | `Quaternion` | The world rotation. |
| `parent` | [Transform](./Transform.md) | The parent Transform. |

[return: [GameObject](./GameObject.md)]
The instantiated GameObject.

### Destroy

Destroys the specified Unity Object.

| Parameter | Type | Description |
|-----------|------|-------------|
| `value` | `DynValue` | The object to destroy. |

### Destroy

Destroys the specified Unity Object after a time delay.

| Parameter | Type | Description |
|-----------|------|-------------|
| `value` | `DynValue` | The object to destroy. |
| `time` | `float` | The delay in seconds before destroying. |

### FindObjectOfType

Finds an object of the specified type in the scene.

| Parameter | Type | Description |
|-----------|------|-------------|
| `prototype` | `Table` | A Lua table prototype representing the type, or an object type. |

[return: any?]
The found object, or `nil` if not found.

### FindObjectsOfType

Finds all objects of the specified type in the scene.

| Parameter | Type | Description |
|-----------|------|-------------|
| `prototype` | `Table` | A Lua table prototype representing the type, or an object type. |

[return: any[]]
An array of found objects.

### Find

Finds a GameObject by name.

| Parameter | Type | Description |
|-----------|------|-------------|
| `name` | `string` | The name of the GameObject to find. |

[return: [GameObject](./GameObject.md)?]
The GameObject if found, or `nil`.

### FindGameObjectsWithTag

Finds all GameObjects with the specified tag.

| Parameter | Type | Description |
|-----------|------|-------------|
| `tag` | `string` | The tag to search for. |

[return: [GameObject](./GameObject.md)[]]
An array of matching GameObjects.

### FindGameObjectWithTag

Finds a single GameObject with the specified tag.

| Parameter | Type | Description |
|-----------|------|-------------|
| `tag` | `string` | The tag to search for. |

[return: [GameObject](./GameObject.md)?]
The GameObject if found, or `nil`.

### CreatePrimitive

Creates a primitive GameObject (sphere, cube, plane, etc.).

| Parameter | Type | Description |
|-----------|------|-------------|
| `type` | `PrimitiveType` | The type of primitive to create. |

[return: [GameObject](./GameObject.md)]
The created primitive GameObject.

### Constructor

Creates a new empty GameObject.

| Parameter | Type | Description |
|-----------|------|-------------|

[return: [GameObject](./GameObject.md)]
The new GameObject.

### Constructor

Creates a new GameObject with the specified name.

| Parameter | Type | Description |
|-----------|------|-------------|
| `name` | `string` | The name for the new GameObject. |

[return: [GameObject](./GameObject.md)]
The new GameObject.

### Constructor

Creates a new GameObject with the specified name and components.

| Parameter | Type | Description |
|-----------|------|-------------|
| `name` | `string` | The name for the new GameObject. |
| `components` | `object[]` | An array of component types to add. |

[return: [GameObject](./GameObject.md)]
The new GameObject.

## Enums

| Enum | Description |
|------|-------------|
