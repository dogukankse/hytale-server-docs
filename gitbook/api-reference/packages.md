# Hytale API - Package Reference

## Complete Package Breakdown

This document provides a detailed breakdown of all packages in the Hytale Server API, organized by category.

---

## Core Packages

### Protocol Definitions (733 total classes)

The protocol package contains all network communication definitions and data structures:

#### Major Protocol Classes (600+ individual classes)

**Interaction System**
- `protocol.Interaction` - Base interaction type
- `protocol.InteractionType` - Types of interactions
- `protocol.InteractionSettings` - Interaction configuration
- `protocol.InteractionRules` - Interaction rule definitions
- `protocol.InteractionChainData` - Chain interaction data
- `protocol.InteractionCooldown` - Cooldown management
- `protocol.InteractionEffects` - Visual/audio effects

**Block System**
- `protocol.BlockType` - Block type definitions
- `protocol.BlockPosition` - Block positioning
- `protocol.BlockMaterial` - Block material properties
- `protocol.BlockTextures` - Block texture definitions
- `protocol.BlockSoundSet` - Block audio
- `protocol.BlockPlacementSettings` - Placement rules
- `protocol.BlockBreaking` - Block breaking mechanics
- `protocol.BlockMount` - Mountable blocks
- `protocol.BlockRotation` - Block rotation data

**Item System**
- `protocol.ItemBase` - Base item type
- `protocol.ItemLibrary` - Item definitions
- `protocol.ItemCategory` - Item categorization
- `protocol.ItemQuality` - Item quality levels
- `protocol.ItemWeapon` - Weapon items
- `protocol.ItemArmor` - Armor items
- `protocol.ItemTool` - Tool items
- `protocol.ItemUtility` - Utility items
- `protocol.ItemGlider` - Glider items
- `protocol.ItemSoundSet` - Item audio

**Entity System**
- `protocol.EntityUpdate` - Entity state updates
- `protocol.EntityEffect` - Entity effects
- `protocol.EntityStatType` - Entity stat types
- `protocol.EntityStatUpdate` - Stat modifications
- `protocol.EntityUIType` - Entity UI types
- `protocol.EntityMatcher` - Entity selection

**Particle System**
- `protocol.Particle` - Particle definitions
- `protocol.ParticleSystem` - Particle systems
- `protocol.ParticleSpawner` - Particle spawning
- `protocol.ParticleCollision` - Particle physics
- `protocol.ParticleAttractor` - Particle attractors
- `protocol.WorldParticle` - World-space particles
- `protocol.ModelParticle` - Model-attached particles

**Animation & Models**
- `protocol.Animation` - Animation definitions
- `protocol.AnimationSet` - Animation collections
- `protocol.Model` - 3D model data
- `protocol.ModelTransform` - Model transformations
- `protocol.ModelTexture` - Model textures
- `protocol.ModelVFX` - Model visual effects

**Camera System**
- `protocol.CameraSettings` - Camera configuration
- `protocol.CameraInteraction` - Camera interactions
- `protocol.CameraShake` - Camera shake effects
- `protocol.CameraNode` - Camera positions
- `protocol.CameraPerspectiveType` - Camera perspectives

**Movement System**
- `protocol.MovementSettings` - Movement configuration
- `protocol.MovementEffects` - Movement effects
- `protocol.MovementType` - Movement types
- `protocol.MovementStates` - Movement state machine
- `protocol.MovementDirection` - Direction handling

**Audio System**
- `protocol.SoundEvent` - Sound events
- `protocol.SoundCategory` - Audio categories
- `protocol.AmbienceFX` - Ambient sound effects
- `protocol.AudioCategory` - Audio category definitions

**World & Environment**
- `protocol.WorldInteraction` - World interactions
- `protocol.WorldEnvironment` - Environment settings
- `protocol.Weather` - Weather system
- `protocol.Cloud` - Cloud rendering
- `protocol.Fluid` - Fluid definitions
- `protocol.FluidFX` - Fluid effects

**UI Components**
- `protocol.CombatTextUpdate` - Combat text
- `protocol.Nameplate` - Player nameplates
- `protocol.Cosmetic` - Cosmetic items

**Physics**
- `protocol.PhysicsConfig` - Physics settings
- `protocol.PhysicsType` - Physics types
- `protocol.CollisionType` - Collision detection

**Utilities**
- `protocol.Vector2f`, `protocol.Vector2i` - 2D vectors
- `protocol.Vector3f`, `protocol.Vector3i`, `protocol.Vector3d` - 3D vectors
- `protocol.Position` - Position data
- `protocol.Rotation` - Rotation data
- `protocol.Color` - Color definitions
- `protocol.Range`, `protocol.Rangef`, `protocol.Rangeb` - Range types

---

## Built-in Systems (1,283 total classes)

### builtin.adventure (217 classes)
Adventure mode systems and mechanics

### builtin.buildertools (192 classes)
Builder tool implementations for creative mode

### builtin.portals (52 classes)
Portal system implementation

### builtin.asseteditor (30 classes)
In-game asset editing tools

### builtin.instances (29 classes)
Instanced dungeon/zone system

### builtin.path (29 classes)
Pathfinding implementation

### builtin.npccombatactionevaluator (27 classes)
NPC combat AI evaluation

### builtin.teleport (26 classes)
Teleportation mechanics

### builtin.beds (19 classes)
Bed and sleeping system

### builtin.mounts (18 classes)
Mount/vehicle system

### builtin.crafting (17 classes)
Crafting system implementation

### builtin.deployables (15 classes)
Deployable object system

### builtin.ambience (10 classes)
Ambient sound/effects

### builtin.weather (8 classes)
Weather system implementation

### builtin.parkour (7 classes)
Parkour mechanics

### builtin.commandmacro (7 classes)
Command macro system

### builtin.blockspawner (7 classes)
Block spawning system

### builtin.creativehub (5 classes)
Creative mode hub

### builtin.blockphysics (5 classes)
Block physics (falling blocks, etc.)

### builtin.blocktick (5 classes)
Block update tick system

### builtin.tagset (4 classes)
Tag-based grouping

### builtin.fluid (4 classes)
Fluid system

### builtin.landiscovery (3 classes)
Land discovery mechanics

### builtin.model (3 classes)
Model utilities

### builtin.npceditor (2 classes)
NPC editing tools

### builtin.worldgen (1 class)
World generation utilities

### builtin.mantling (1 class)
Mantling/climbing mechanics

### builtin.safetyroll (1 class)
Safety roll mechanics

### builtin.sprintforce (1 class)
Sprint force mechanics

### builtin.crouchslide (1 class)
Crouch sliding mechanics

---

## Server Systems (329 total classes)

### server.worldgen (213 classes)
World generation engine - procedural terrain, structures, biomes

### server.spawning (82 classes)
Entity spawning system - mob spawning, spawn conditions

### server.flock (33 classes)
Flocking behavior for groups of entities (birds, fish, etc.)

### server.migrations (1 class)
Data migration utilities

---

## Procedural Library (146 total classes)

### procedurallib.logic (42 classes)
Logic operations for procedural generation

### procedurallib.json (37 classes)
JSON-based procedural definitions

### procedurallib.condition (21 classes)
Conditional logic for procedural systems

### procedurallib.property (18 classes)
Property definitions

### procedurallib.supplier (17 classes)
Value suppliers for procedural generation

### procedurallib.random (5 classes)
Random number generation utilities

### procedurallib (4 classes)
Core procedural generation types:
- `NoiseFunction`, `NoiseFunction2d`, `NoiseFunction3d`
- `NoiseFunctionPair`, `NoiseType`

---

## Codec System (125 total classes)

### codec.validation (35 classes)
Data validation system

### codec.codecs (29 classes)
Codec implementations

### codec.schema (28 classes)
Schema definitions

### codec.lookup (9 classes)
Lookup tables

### codec.store (3 classes)
Data storage

### codec.builder (3 classes)
Builder patterns for codecs

### codec.exception (2 classes)
Codec exceptions

### codec.function (2 classes)
Codec functions

### codec.util (2 classes)
Codec utilities

### codec (8 classes)
Core codec types:
- `Codec` - Base codec interface
- `KeyedCodec` - Keyed codec
- `WrappedCodec` - Wrapped codec
- `PrimitiveCodec` - Primitive types
- `RawJsonCodec` - JSON codec
- `InheritCodec` - Inheritance support

---

## Component System (90 total classes)

Entity Component System (ECS) implementation

### component.system (24 classes)
System definitions and execution

### component.data (10 classes)
Component data structures

### component.dependency (8 classes)
Dependency injection

### component.query (7 classes)
Component queries

### component.spatial (6 classes)
Spatial partitioning

### component.event (3 classes)
Component events

### component.task (2 classes)
Task scheduling

### component.metric (2 classes)
Performance metrics

### component (28 classes)
Core ECS types:
- `Component` - Base component
- `ComponentType` - Component type registry
- `ComponentRegistry` - Component registration
- `Store` - Component storage
- `Archetype` - Entity archetype
- `Resource` - Shared resources
- `SystemType` - System types

---

## Math Library (81 total classes)

### math.vector (18 classes)
Vector math operations

### math.shape (13 classes)
Geometric shapes

### math.block (10 classes)
Block-space math

### math.hitdetection (8 classes)
Hit detection and raycasting

### math.util (7 classes)
Math utilities

### math.iterator (6 classes)
Iterators for math operations

### math.codec (5 classes)
Math type serialization

### math.range (4 classes)
Range types

### math (10 classes)
Core math types:
- `Vec2f`, `Vec3f`, `Vec4f` - Vectors
- `Mat4f` - 4x4 matrix
- `Quatf` - Quaternion
- `Axis` - Axis enumeration

---

## Common Utilities (47 total classes)

### common.util (20 classes)
General utilities

### common.collection (5 classes)
Collection utilities

### common.benchmark (4 classes)
Benchmarking tools

### common.map (4 classes)
Map data structures

### common.semver (4 classes)
Semantic versioning

### common.fastutil (3 classes)
Fast utility extensions

### common.plugin (3 classes)
Plugin utilities

### common.tuple (2 classes)
Tuple types

### common.thread (2 classes)
Threading utilities

---

## Asset Store (40 total classes)

### assetstore.event (9 classes)
Asset loading events

### assetstore.map (9 classes)
Asset mapping

### assetstore.codec (4 classes)
Asset serialization

### assetstore.iterator (2 classes)
Asset iteration

### assetstore (16 classes)
Core asset management:
- `AssetStore` - Main asset storage
- `AssetRegistry` - Asset registration
- `AssetPack` - Asset packs
- `AssetHolder` - Asset references
- `AssetMap` - Asset mapping
- `JsonAsset`, `RawAsset` - Asset types

---

## Function System (34 total classes)

Functional programming utilities

### function.predicate (11 classes)
Predicate functions

### function.function (10 classes)
General functions

### function.consumer (10 classes)
Consumer functions

### function.supplier (2 classes)
Supplier functions

---

## Event System (15 total classes)

Event bus and event handling

- `EventRegistry` - Event registration
- `EventBus` - Event dispatching
- `EventBusRegistry` - Bus management
- `IEvent`, `IBaseEvent` - Event interfaces
- `IAsyncEvent` - Async events
- `ICancellable` - Cancellable events
- `EventPriority` - Event priorities
- `SyncEventBusRegistry`, `AsyncEventBusRegistry` - Sync/async buses

---

## Logger System (11 total classes)

### logger.backend (6 classes)
Logging backends

### logger.sentry (2 classes)
Sentry integration

### logger.util (2 classes)
Logging utilities

### logger (1 class)
- `HytaleLogger` - Main logger

---

## Metrics System (10 total classes)

### metrics.metric (4 classes)
Metric definitions

### metrics (6 classes)
- `MetricsRegistry` - Metric registration
- `MetricProvider` - Metric providers
- `ExecutorMetricsRegistry` - Executor metrics
- `JVMMetrics` - JVM metrics

---

## Sneaky Throw (10 total classes)

Exception handling utilities

### sneakythrow.consumer (4 classes)
Throwing consumers

### sneakythrow.supplier (2 classes)
Throwing suppliers

### sneakythrow.function (2 classes)
Throwing functions

### sneakythrow (2 classes)
- `SneakyThrow` - Main utility
- `ThrowableRunnable` - Runnable interface

---

## Protocol I/O (9 total classes)

### protocol.io (9 classes)
Network protocol I/O utilities

---

## Storage System (3 total classes)

- `IndexedStorageFile` - Indexed file storage
- `IndexedStorageFile_v0` - Version 0 format
- `package-info` - Package documentation

---

## Plugin System (3 total classes)

### plugin.early (3 classes)
Early plugin loading:
- `EarlyPluginLoader` - Early loading
- `ClassTransformer` - Bytecode transformation
- `TransformingClassLoader` - Custom classloader

---

## Registry System (2 total classes)

- `Registry` - Generic registry
- `Registration` - Registration handle

---

## Main Classes (2 classes)

- `Main` - Server entry point
- `LateMain` - Late initialization

---

## Unsafe Utilities (1 class)

- `UnsafeUtil` - Low-level operations (use with caution)

---

## Summary by Category

| Category | Classes | Description |
|----------|---------|-------------|
| Protocol | 733 | Network protocol definitions |
| Built-in Systems | 1,283 | Game mechanics implementations |
| Server | 329 | Server-side systems |
| Procedural Library | 146 | Procedural generation |
| Codec | 125 | Serialization/deserialization |
| Component System | 90 | Entity Component System |
| Math | 81 | Mathematics library |
| Common | 47 | Utilities |
| Asset Store | 40 | Asset management |
| Function | 34 | Functional utilities |
| Event System | 15 | Event handling |
| Logger | 11 | Logging |
| Metrics | 10 | Performance monitoring |
| Sneaky Throw | 10 | Exception utilities |
| Protocol I/O | 9 | Network I/O |
| Storage | 3 | File storage |
| Plugin | 3 | Plugin system |
| Registry | 2 | Registration system |
| Main | 2 | Entry points |
| Unsafe | 1 | Low-level operations |
| **Total** | **5,218** | **All Hytale API classes** |

---

## Usage Recommendations

### For Plugin Development

**Essential Packages:**
- `plugin.*` - Plugin lifecycle
- `event.*` - Event handling
- `assetstore.*` - Custom assets
- `common.*` - Utilities

**Game Features:**
- `protocol.*` - Data structures
- `builtin.*` - Reference implementations
- `server.*` - Server systems
- `component.*` - ECS for entities

**Utilities:**
- `math.*` - Mathematics
- `codec.*` - Serialization
- `function.*` - Functional programming
- `logger.*` - Logging

### Performance Considerations

- Use the component system for entity data
- Leverage the asset store for resources
- Utilize the metrics system for profiling
- Use the procedural library for generation

---

*Generated from HytaleServer.jar on January 19, 2026*
