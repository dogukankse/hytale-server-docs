# Hytale API - Quick Start Guide

## Common Plugin Development Tasks

This guide provides quick references for common Hytale plugin development tasks, based on the API extracted from HytaleServer.jar.

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

## 11. Animation System

**Protocol Classes:**
- `protocol.Animation` - Animation data
- `protocol.AnimationSet` - Animation collections
- `protocol.AnimationSlot` - Animation slots

---

## 12. Audio System

### Sound Events

**Protocol Classes:**
- `protocol.SoundEvent` - Sound definitions
- `protocol.SoundCategory` - Audio categories
- `protocol.AudioCategory` - Category config
- `protocol.AmbienceFX` - Ambient audio
- `protocol.AmbienceFXSound` - Ambient sounds
- `protocol.AmbienceFXMusic` - Background music

**Sound Sets:**
- `protocol.BlockSoundSet` - Block sounds
- `protocol.ItemSoundSet` - Item sounds

---

## 13. Camera System

**Protocol Classes:**
- `protocol.CameraSettings` - Camera configuration
- `protocol.CameraInteraction` - Camera control
- `protocol.CameraShake` - Shake effects
- `protocol.CameraNode` - Camera positions
- `protocol.CameraPerspectiveType` - First/third person

---

## 14. Movement System

**Protocol Classes:**
- `protocol.MovementSettings` - Movement config
- `protocol.MovementEffects` - Movement effects
- `protocol.MovementType` - Movement modes
- `protocol.MovementStates` - State machine
- `protocol.PhysicsConfig` - Physics settings

### Special Movement

**Built-in Systems:**
- `builtin.mantling.*` - Climbing
- `builtin.crouchslide.*` - Sliding
- `builtin.sprintforce.*` - Sprinting
- `builtin.safetyroll.*` - Rolling
- `builtin.parkour.*` - Parkour mechanics

---

## 15. Interaction System

### Interaction Chain

**Protocol Classes:**
- `protocol.Interaction` - Base interaction
- `protocol.InteractionType` - Interaction types
- `protocol.InteractionChainData` - Interaction chains
- `protocol.InteractionSettings` - Configuration
- `protocol.InteractionCooldown` - Cooldowns

### Interaction Types

- `protocol.SimpleInteraction` - Basic interactions
- `protocol.ChargingInteraction` - Charge-up interactions
- `protocol.ConditionInteraction` - Conditional
- `protocol.ChainingInteraction` - Chain interactions
- `protocol.ParallelInteraction` - Parallel execution

### Specific Interactions

**Block:**
- `protocol.BreakBlockInteraction`
- `protocol.PlaceBlockInteraction`
- `protocol.ChangeBlockInteraction`

**Entity:**
- `protocol.DamageEntityInteraction`
- `protocol.RemoveEntityInteraction`
- `protocol.UseEntityInteraction`

**Inventory:**
- `protocol.ModifyInventoryInteraction`

**Effect:**
- `protocol.ApplyEffectInteraction`
- `protocol.ApplyForceInteraction`

**Other:**
- `protocol.TeleportInteraction` (via builtin.teleport)
- `protocol.CameraInteraction`

---

## 16. Built-in Game Systems

### Adventure Mode
- `builtin.adventure.*` (217 classes) - Adventure mechanics

### Builder Tools
- `builtin.buildertools.*` (192 classes) - Creative building

### Portals
- `builtin.portals.*` (52 classes) - Portal system

### Crafting
- `builtin.crafting.*` (17 classes) - Crafting system
- `protocol.CraftingRecipe` - Recipe definitions

### Mounts
- `builtin.mounts.*` (18 classes) - Mount system
- `protocol.MountController` - Mount control

### Beds
- `builtin.beds.*` (19 classes) - Sleeping system

### Deployables
- `builtin.deployables.*` (15 classes) - Deployable objects
- `protocol.DeployableConfig` - Deployable config

---

## 17. Math and Utilities

### Vectors and Math

**Core Math:**
- `math.Vec2f`, `math.Vec3f`, `math.Vec4f` - Vectors
- `math.Mat4f` - Matrices
- `math.Quatf` - Quaternions
- `protocol.Vector2f`, `protocol.Vector2i` - 2D vectors
- `protocol.Vector3f`, `protocol.Vector3i`, `protocol.Vector3d` - 3D vectors

**Math Utilities:**
- `math.vector.*` - Vector operations
- `math.shape.*` - Geometric shapes
- `math.hitdetection.*` - Raycasting
- `math.range.*` - Range types

---

## 18. Serialization (Codecs)

### Codec System

**Key Packages:**
- `com.hypixel.hytale.codec.*` - Serialization

**Core Classes:**
- `Codec` - Base codec interface
- `KeyedCodec` - Keyed serialization
- `RawJsonCodec` - JSON codec
- `codec.validation.*` - Data validation
- `codec.schema.*` - Schema definitions

---

## 19. Logging and Debugging

### Logger

**Key Classes:**
- `logger.HytaleLogger` - Main logger
- `logger.backend.*` - Logging backends
- `logger.sentry.*` - Error tracking

### Metrics

**Key Classes:**
- `metrics.MetricsRegistry` - Performance metrics
- `metrics.JVMMetrics` - JVM monitoring

---

## 20. Storage

### Data Persistence

**Key Classes:**
- `storage.IndexedStorageFile` - File storage
- Asset store for game data

---

## Example Plugin Structure

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

- **API Documentation**: See `API-DOCUMENTATION.md`
- **Package Reference**: See `PACKAGE-REFERENCE.md`
- **Class List**: See `hytale-classes.txt`
- **Full Class List**: See `all-classes.txt`

---

## Decompiling the JAR

For detailed method signatures and implementations:

```powershell
# Using IntelliJ IDEA (recommended)
# 1. Right-click on jars/HytaleServer.jar
# 2. Select "Add as Library"
# 3. Browse the decompiled source

# Or use JD-GUI
# Download from http://java-decompiler.github.io/
# Open HytaleServer.jar in JD-GUI
```

---

*Generated from HytaleServer.jar on January 19, 2026*
