---
title: PlayerCamera
---

Use these methods to access the player cameras.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `fpCameraLocalPosition` | `Vector3` | The first person camera's local offset position. This is an offset from the default value, and is always `Vector3.zero` by default. |
| `fpCameraLocalRotation` | `Quaternion` | The first person camera's local offset rotation. This is an offset from the default value, and is always `Quaternion.identity` by default. |
| `activeCamera` | `Camera` | Get the player's currently active camera. |
| `isUsingOverrideCamera` | `bool` | True when an override camera is active. An override camera is typically used when the player enters a vehicle with a custom camera setup. |
| `isUsingFPCamera` | `bool` | True when the first person camera is active. |
| `fpCamera` | `Camera` | Get the player's first person camera. This is the camera that is active while the player is running around as infantry or in a vehicle without a special camera. |
| `tpCamera` | `Camera` | Get the player's third person camera. This is the camera that is active while the player is ragdolled. This is not the same as the third person camera while inside vehicles. |

## Methods

### ResetRecoil

Instantly resets any first person weapon recoil.

### ApplyWeaponSnap

Makes the first person weapon wobble up and down.

| Parameter | Type | Description |
|-----------|------|-------------|
| `magnitude` | `float` | The magnitude of the wobble. |
| `frequency` | `float` | The frequency of the wobble. |
| `duration` | `float` | The duration of the wobble. |

### ApplyWeaponRattle

Makes the weapon "rattle", rotating quickly around its axis.

| Parameter | Type | Description |
|-----------|------|-------------|
| `magnitude` | `float` | The magnitude of the rattle. |
| `frequency` | `float` | The frequency of the rattle. |
| `duration` | `float` | The duration of the rattle. |

### ApplyRecoil

Apply a recoil on the first person weapon. Optionally also kicks the camera.

| Parameter | Type | Description |
|-----------|------|-------------|
| `recoil` | `Vector3` | The recoil vector. |
| `applyCameraKick` | `bool` | Whether to also kick the camera. |

### ApplyScreenshake

Apply a screen shake effect.

| Parameter | Type | Description |
|-----------|------|-------------|
| `magnitude` | `float` | The magnitude of the shake. |
| `iterations` | `int` | The number of iterations. |

### KickCamera

Kick the first person camera by an euler rotation.

| Parameter | Type | Description |
|-----------|------|-------------|
| `kickEuler` | `Vector3` | The euler rotation to kick the camera by. |

### GetActiveCameraRay

Returns a ray starting at the active camera in the camera forward direction.

[return: `Ray`]

### GetCameraRay

Returns a ray starting at the camera in the camera forward direction.

| Parameter | Type | Description |
|-----------|------|-------------|
| `camera` | `Camera` | The camera to get the ray from. |

[return: `Ray`]

### OverrideActiveCamera

Override the active camera.

| Parameter | Type | Description |
|-----------|------|-------------|
| `camera` | `Camera` | The camera to use as the override. |

### CancelOverrideCamera

Cancel the camera override. Returns to the player's default first person or third person camera.

### FirstPersonCamera

Switch to first person camera.

### ThirdPersonCamera

Switch to third person camera.

### RotateFirstPersonCamera

Rotates the player camera, simulating player mouse movement.

| Parameter | Type | Description |
|-----------|------|-------------|
| `rotation` | `Vector2` | The rotation to apply. |

## Events

| Event | Signature | Description |
|-------|-----------|-------------|

## Static Fields

| Field | Type | Description |
|-------|------|-------------|

## Static Methods

All methods on this class are static. See the Methods section above.

## Enums

| Value | Description |
|-------|-------------|
