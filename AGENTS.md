# Documentation Standards for Ravenscript Docs

## File Structure

Each file is a Markdown (`.md`) document representing a single API class/module. Files live in `docs/Ravenscript/` and are cross-referenced via relative links.

## Document Template

```markdown
---
title: ClassName
---

One-line description of what the class represents/does.

## Properties

| Property | Type | Description |
|----------|------|-------------|
| `propName` | `Type` | Description text. |

## Methods

### MethodName

Description of what the method does.

| Parameter | Type | Description |
|-----------|------|-------------|
| `param` | `Type` | Parameter description. |

[return: ReturnType]
Description of return value.

## Events

| Event | Signature | Description |
|-------|-----------|-------------|
| `eventName` | `(param1, param2)` | Description. |

## Static Fields

| Field | Type | Description |
|-------|------|-------------|
| `FIELD_NAME` | `Type` | Description. |

## Static Methods

### StaticMethodName

Description.

| Parameter | Type | Description |
|-----------|------|-------------|
| `param` | `Type` | Description. |

[return: ReturnType]
Return description.

## Enums

### EnumName

| Value | Description |
|-------|-------------|
| `Value1` | Description. |
| `Value2` | Description. |
```

## Formatting Rules

### Front Matter
- YAML block with only `title` field
- No blank line between `---` and title

### Headings
- `##` for major sections: Properties, Methods, Events, Static Fields, Static Methods, Enums
- `###` for individual method/enum names

### Properties Table
- Columns: `| Property | Type | Description |`
- Separator: `|----------|------|-------------|`
- Property names in backticks: `` `propName` ``
- Types in backticks: `` `bool` ``, `` `float` ``, `` `Vector3` ``
- Cross-file references use Markdown links: `[Weapon](./Weapon.md)`, `[Weapon](./Weapon.md)[]`
- Nullable values described with "or `nil`" in description text

### Methods
- `###` heading with method name
- Brief description paragraph
- Parameter table (same format as properties)
- Return value on its own line: `[return: TypeName]` or `[return: TypeName?]` for nullable
- Return description follows on next line

### Return Type Conventions
- Use `?` suffix for nullable types: `[return: Actor?]`, `[return: RaycastHit?]`
- Use `[]` for arrays: `[return: Actor[]]`, `[return: Collider[]]`
- Primitive types: `[return: bool]`, `[return: float]`, `[return: int]`, `[return: string]`
- Complex types: `[return: DamageInfo]`, `[return: LoadoutSet]`, `[return: WeaponRole]`

### Events Table
- Columns: `| Event | Signature | Description |`
- Signature uses parentheses notation: `(actor, source, info)` or `ScriptEvent<Order>`

### Enums
- `### EnumName` heading
- Table columns: `| Value | Description |`

### Inline Code
- All identifiers (properties, types, values, enum values) wrapped in backticks
- Use `nil` (not `null`) for null/nil values throughout

### Section Order
1. Properties
2. Methods
3. Events
4. Static Fields
5. Static Methods
6. Enums

Sections that have no content should still appear as headers with empty tables.
