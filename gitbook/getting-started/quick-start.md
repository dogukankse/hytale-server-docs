# Quick Start Guide

Common plugin development tasks and code patterns for Hytale Server.

---

## 1. Plugin Basics

### Plugin Entry Point

Your plugin should extend the base plugin class and implement the lifecycle methods.

**Key Classes:**
- `com.hypixel.hytale.plugin.*` - Plugin system

### Plugin Lifecycle

```
Load → Enable → Running → Disable → Unload
```

### Example Plugin Structure

```
MyPlugin/
├── src/main/java/com/example/myplugin/
│   ├── MyPlugin.java              # Main plugin class
│   ├── listeners/
│   │   └── EventListener.java     # Event handlers
│   ├── commands/
│   │   └── MyCommand.java         # Custom commands
│   ├── components/
│   │   └── CustomComponent.java   # ECS components
│   └── systems/
│       └── CustomSystem.java      # ECS systems
└── src/main/resources/
    ├── manifest.json               # Plugin manifest
    └── assets/                     # Custom assets
```

---

## 2. Event System

### Registering Event Listeners

**Key Packages:**
- `com.hypixel.hytale.event.*` - Core event system
- `com.hypixel.hytale.server.event.*` - Server events

**Core Classes:**
- `EventRegistry` - Register event listeners
- `EventBus` - Event dispatching
- `IEvent` - Base event interface
- `ICancellable` - Cancellable events
- `EventPriority` - Event priority levels

**Event Types:**
- `IAsyncEvent` - Asynchronous events
- `IProcessedEvent` - Post-processing events

### Registering an Event Listener

```java
// Register event listener
eventRegistry.register(SomeEvent.class, this::handleEvent);
```

### Event Priorities

```java
// Priority values: FIRST, EARLY, NORMAL, LATE, LAST
eventRegistry.register(EventPriority.EARLY, SomeEvent.class, this::handleEvent);
```

### Common Events

Look for event classes in:
- `com.hypixel.hytale.server.core.asset.AssetPackRegisterEvent`
- `com.hypixel.hytale.server.core.asset.AssetPackUnregisterEvent`
- `com.hypixel.hytale.server.core.asset.LoadAssetEvent`
- `com.hypixel.hytale.server.core.asset.GenerateSchemaEvent`

---

## 3. Working with Assets

### Loading Custom Assets

**Key Packages:**
- `com.hypixel.hytale.assetstore.*` - Asset management
- `com.hypixel.hytale.server.core.asset.*` - Server-side asset loading

**Core Classes:**
- `AssetStore` - Main asset storage
- `AssetRegistry` - Asset registration
- `AssetPack` - Asset packs
- `AssetHolder` - Asset references
- `JsonAsset` - JSON-based assets
- `RawAsset` - Raw binary assets

### Registering an Asset

```java
// Register block asset
assetStore.register(blockAsset);
```

### Asset Types

Located in `com.hypixel.hytale.server.core.asset.type.*`:
- `ambiencefx.*` - Ambient effects
- `audiocategory.*` - Audio categories
- `blockbreakingdecal.*` - Block breaking visuals
- And many more...

---

## 4. Block System

### Working with Blocks

**Key Packages:**
- `com.hypixel.hytale.server.core.block.*` - Block system

**Protocol Classes:**
- `protocol.BlockType` - Block definitions
- `protocol.BlockPosition` - Block coordinates
- `protocol.BlockMaterial` - Block properties
- `protocol.BlockTextures` - Block textures
- `protocol.BlockSoundSet` - Block sounds
- `protocol.BlockPlacementSettings` - Placement rules
- `protocol.BlockRotation` - Block orientation
- `protocol.BlockMatcher` - Block selection

### Block Interactions

- `protocol.BreakBlockInteraction` - Breaking blocks
- `protocol.PlaceBlockInteraction` - Placing blocks
- `protocol.ChangeBlockInteraction` - Changing blocks
- `protocol.UseBlockInteraction` - Using blocks

---

## 5. Entity System

### Entity Component System (ECS)

**Key Packages:**
- `com.hypixel.hytale.component.*` - Component system
- `com.hypixel.hytale.server.core.entity.*` - Entity system

**Core ECS Classes:**
- `Component` - Base component
- `ComponentType` - Component type registry
- `ComponentRegistry` - Component management
- `Store` - Component storage
- `Archetype` - Entity archetype
- `Resource` - Shared resources
- `SystemType` - System definitions

**Component Utilities:**
- `component.query.*` - Query components
- `component.system.*` - System execution
- `component.data.*` - Component data

### Registering a Component

```java
// Register custom component
componentRegistry.register(CustomComponent.class);
```

### Entity Protocol

- `protocol.EntityUpdate` - Entity state updates
- `protocol.EntityEffect` - Visual/audio effects
- `protocol.EntityStatType` - Entity stats
- `protocol.EntityMatcher` - Entity selection

### Entity Interactions

- `protocol.DamageEntityInteraction` - Damage entities
- `protocol.RemoveEntityInteraction` - Remove entities
- `protocol.UseEntityInteraction` - Use/interact with entities

---

## 6. Item System

### Working with Items

**Protocol Classes:**
- `protocol.ItemBase` - Base item
- `protocol.ItemLibrary` - Item registry
- `protocol.ItemCategory` - Item categories
- `protocol.ItemQuality` - Item rarity/quality
- `protocol.ItemQuantity` - Item stacks

### Item Types

- `protocol.ItemWeapon` - Weapons
- `protocol.ItemArmor` - Armor pieces
- `protocol.ItemTool` - Tools
- `protocol.ItemUtility` - Utility items
- `protocol.ItemGlider` - Gliders

### Item Properties

- `protocol.ItemSoundSet` - Item sounds
- `protocol.ItemReticle` - Crosshair/reticle
- `protocol.ItemPlayerAnimations` - Animation data

### Inventory

- `protocol.ModifyInventoryInteraction` - Modify inventory
- `protocol.InventorySection` - Inventory sections
- `protocol.InventoryActionType` - Inventory actions

---

## 7. World System

### World Generation

**Key Packages:**
- `com.hypixel.hytale.server.worldgen.*` (213 classes) - World generation
- `com.hypixel.hytale.procedurallib.*` - Procedural generation

**Procedural Generation:**
- `NoiseFunction`, `NoiseFunction2d`, `NoiseFunction3d` - Noise functions
- `procedurallib.logic.*` - Logic operations
- `procedurallib.condition.*` - Conditions
- `procedurallib.random.*` - Random generation

### World Interaction

- `protocol.WorldInteraction` - World interactions
- `protocol.WorldEnvironment` - Environment settings
- `protocol.WorldParticle` - World particles

---

## 8. Player System

### Player Management

**Key Packages:**
- `com.hypixel.hytale.server.core.player.*` - Player system

**Protocol Classes:**
- `protocol.PlayerSkin` - Player appearance
- Player-related events and updates

---

## 9. Command System

### Registering Commands

**Key Packages:**
- `com.hypixel.hytale.server.command.*` - Command system
- `com.hypixel.hytale.builtin.commands.*` - Built-in commands

---

## 10. Particles and Visual Effects

### Particle System

**Protocol Classes:**
- `protocol.Particle` - Particle definitions
- `protocol.ParticleSystem` - Particle systems
- `protocol.ParticleSpawner` - Spawn particles
- `protocol.ParticleSpawnerGroup` - Grouped spawners
- `protocol.ParticleCollision` - Particle physics
- `protocol.ParticleAttractor` - Attractors

**Particle Types:**
- `protocol.WorldParticle` - World-space
- `protocol.ModelParticle` - Model-attached
- `protocol.FluidParticle` - Fluid effects
- `protocol.BlockParticleSet` - Block particles

---

## Best Practices

1. **Use the Event System** - Hook into game events rather than polling
2. **Leverage ECS** - Use components for entity data
3. **Asset Management** - Register custom assets properly
4. **Error Handling** - Use the logging system
5. **Performance** - Use metrics to monitor performance
6. **Protocol Classes** - Use protocol classes for data structures
7. **Built-in Systems** - Reference built-in implementations

---

## Additional Resources

- [API Documentation](../api-reference/README.md)
- [Package Reference](../api-reference/packages.md)
- [Method Signatures](../api-reference/method-signatures.md)

---

*Generated from HytaleServer.jar on January 19, 2026*
