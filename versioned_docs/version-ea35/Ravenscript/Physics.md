---
title: Physics
---

Use these methods to interact with Unity's physics engine.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `gravity` | `Vector3` | The gravity applied to physics objects. |

## Methods

### Raycast

Casts a ray through the scene until it collides with a target.

| Parameter | Type | Description |
|-----------|------|-------------|
| `ray` | `Ray` | Test for collisions along this ray. |
| `range` | `float` | Look no further than this [meters]. |
| `target` | [RaycastTarget](./RaycastTarget.md) | Test for collisions with these things. |

[return: RaycastHit?]
`RaycastHit` or `nil`.

### RaycastAll

Casts a ray through the scene registering all collisions with target objects.

| Parameter | Type | Description |
|-----------|------|-------------|
| `ray` | `Ray` | Test for collisions along this ray. |
| `range` | `float` | Look no further than this [meters]. |
| `target` | [RaycastTarget](./RaycastTarget.md) | Test for collisions with these things. |

[return: RaycastHit[]]
An array of RaycastHits that occurred along the ray.

### Linecast

Casts a ray from start to end until it collides with a target.

| Parameter | Type | Description |
|-----------|------|-------------|
| `start` | `Vector3` | The start position of the line. |
| `end` | `Vector3` | The end position of the line. |
| `target` | [RaycastTarget](./RaycastTarget.md) | Test for collisions with these things. |

[return: RaycastHit?]
`RaycastHit` or `nil`.

### Spherecast

Casts a sphere ray from start to end until it collides with a target.

| Parameter | Type | Description |
|-----------|------|-------------|
| `ray` | `Ray` | The ray to cast. |
| `radius` | `float` | The radius of the sphere. |
| `range` | `float` | Look no further than this [meters]. |
| `target` | [RaycastTarget](./RaycastTarget.md) | Test for collisions with these things. |

[return: RaycastHit?]
`RaycastHit` or `nil`.

### SpherecastAll

Casts a sphere ray from start to end until it collides with a target.

| Parameter | Type | Description |
|-----------|------|-------------|
| `ray` | `Ray` | The ray to cast. |
| `radius` | `float` | The radius of the sphere. |
| `range` | `float` | Look no further than this [meters]. |
| `target` | [RaycastTarget](./RaycastTarget.md) | Test for collisions with these things. |

[return: RaycastHit[]]
`RaycastHit[]`.

### RaycastActor

Casts a ray, returning the first hit actor.

| Parameter | Type | Description |
|-----------|------|-------------|
| `ray` | `Ray` | The ray to cast. |
| `range` | `float` | Look no further than this [meters]. |
| `blockedByGeometry` | `bool` | Whether the ray should be blocked by geometry. |
| `blockedByVehicles` | `bool` | Whether the ray should be blocked by vehicles. |

[return: [Actor](./Actor.md)?]
The hit Actor; otherwise nil if no actor was hit or the ray is blocked by other colliders.

### CheckBox

Checks if a box overlaps with any colliders.

| Parameter | Type | Description |
|-----------|------|-------------|
| `center` | `Vector3` | The center of the box. |
| `halfExtents` | `Vector3` | Half the size of the box in each dimension. |
| `orientation` | `Quaternion` | The rotation of the box. |
| `target` | [RaycastTarget](./RaycastTarget.md) | Test for collisions with these things. |

[return: bool]
`bool`.

### OverlapBox

Finds all colliders overlapping a box.

| Parameter | Type | Description |
|-----------|------|-------------|
| `center` | `Vector3` | The center of the box. |
| `halfExtents` | `Vector3` | Half the size of the box in each dimension. |
| `orientation` | `Quaternion` | The rotation of the box. |
| `target` | [RaycastTarget](./RaycastTarget.md) | Test for collisions with these things. |

[return: Collider[]]
`Collider[]`.

### CheckCapsule

Checks if a capsule overlaps with any colliders.

| Parameter | Type | Description |
|-----------|------|-------------|
| `start` | `Vector3` | The start of the capsule. |
| `end` | `Vector3` | The end of the capsule. |
| `radius` | `float` | The radius of the capsule. |
| `target` | [RaycastTarget](./RaycastTarget.md) | Test for collisions with these things. |

[return: bool]
`bool`.

### OverlapCapsule

Finds all colliders overlapping a capsule.

| Parameter | Type | Description |
|-----------|------|-------------|
| `start` | `Vector3` | The start of the capsule. |
| `end` | `Vector3` | The end of the capsule. |
| `radius` | `float` | The radius of the capsule. |
| `target` | [RaycastTarget](./RaycastTarget.md) | Test for collisions with these things. |

[return: Collider[]]
`Collider[]`.

### CheckSphere

Checks if a sphere overlaps with any colliders.

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The center of the sphere. |
| `radius` | `float` | The radius of the sphere. |
| `target` | [RaycastTarget](./RaycastTarget.md) | Test for collisions with these things. |

[return: bool]
`bool`.

### OverlapSphere

Finds all colliders overlapping a sphere.

| Parameter | Type | Description |
|-----------|------|-------------|
| `position` | `Vector3` | The center of the sphere. |
| `radius` | `float` | The radius of the sphere. |
| `target` | [RaycastTarget](./RaycastTarget.md) | Test for collisions with these things. |

[return: Collider[]]
`Collider[]`.
