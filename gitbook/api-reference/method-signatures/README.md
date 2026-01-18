# Method Signatures

Detailed public API reference extracted from HytaleServer.jar using javap.

**Generated:** January 19, 2026  
**Classes Documented:** 96

This section provides method signatures, parameters, return types, and public fields for the most important classes in the Hytale API.

---

## Categories

| Category | Classes | Description |
|----------|---------|-------------|
| [Event System](event-system.md) | 12 | Event handling and dispatching |
| [Component System (ECS)](component-system.md) | 16 | Entity Component System |
| [Asset Management](asset-management.md) | 8 | Asset loading and storage |
| [Math Utilities](math-utilities.md) | 6 | Vectors, matrices, quaternions |
| [Protocol - Core Types](protocol-core.md) | 9 | Basic data types |
| [Protocol - Blocks](protocol-blocks.md) | 5 | Block-related classes |
| [Protocol - Items](protocol-items.md) | 8 | Item-related classes |
| [Protocol - Entities](protocol-entities.md) | 4 | Entity updates and effects |
| [Protocol - Interactions](protocol-interactions.md) | 4 | Interaction system |
| [Protocol - Particles](protocol-particles.md) | 3 | Particle system |
| [Protocol - Movement](protocol-movement.md) | 4 | Movement and physics |
| [Protocol - Animation](protocol-animation.md) | 3 | Animation system |
| [Protocol - Audio](protocol-audio.md) | 3 | Sound and audio |
| [Protocol - Camera](protocol-camera.md) | 2 | Camera system |
| [Utilities](utilities.md) | 9 | Codecs, registry, logger |

---

## Quick Links by Package

### com.hypixel.hytale.event
- [IEvent](event-system.md#ievent), [IBaseEvent](event-system.md#ibaseevent), [IAsyncEvent](event-system.md#iasyncevent)
- [EventRegistry](event-system.md#eventregistry), [EventBus](event-system.md#eventbus)
- [EventPriority](event-system.md#eventpriority), [ICancellable](event-system.md#icancellable)

### com.hypixel.hytale.component
- [Component](component-system.md#component), [ComponentRegistry](component-system.md#componentregistry)
- [Store](component-system.md#store), [Archetype](component-system.md#archetype)
- [Resource](component-system.md#resource), [SystemType](component-system.md#systemtype)

### com.hypixel.hytale.assetstore
- [AssetStore](asset-management.md#assetstore), [AssetRegistry](asset-management.md#assetregistry)
- [AssetPack](asset-management.md#assetpack), [AssetHolder](asset-management.md#assetholder)

### com.hypixel.hytale.math
- [Vec2f](math-utilities.md#vec2f), [Vec3f](math-utilities.md#vec3f), [Vec4f](math-utilities.md#vec4f)
- [Mat4f](math-utilities.md#mat4f), [Quatf](math-utilities.md#quatf)

### com.hypixel.hytale.protocol
- [BlockType](protocol-blocks.md#blocktype), [ItemBase](protocol-items.md#itembase)
- [EntityUpdate](protocol-entities.md#entityupdate), [Particle](protocol-particles.md#particle)
- [Vector3f](protocol-core.md#vector3f), [Position](protocol-core.md#position)

---

## How to Read Method Signatures

Each class documentation includes:

```java
// Package and class name
**Package:** `com.hypixel.hytale.event`
**Full Name:** `com.hypixel.hytale.event.EventRegistry`

// Class type and inheritance
**Type:** Class
**Extends:** `Registry<...>`
**Implements:** `IEventRegistry`

// Constructors
### Public Constructors
public EventRegistry(List<...>, ...);

// Methods
### Public Methods
public void someMethod(ParamType param);

// Fields
### Public Fields
public static final String CONSTANT;
```

---

## See Also

- [Package Reference](packages.md) - All packages overview
- [API Overview](README.md) - API statistics
- [Development Guides](../guides/README.md) - How to use these classes
