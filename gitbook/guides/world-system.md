# World System

The World System handles world generation, terrain, biomes, and world manipulation.

---

## Overview

**Key Packages:**
- `com.hypixel.hytale.server.worldgen.*` - World generation (213 classes)
- `com.hypixel.hytale.procedurallib.*` - Procedural generation (146 classes)

---

## World Generation

### Server WorldGen (213 classes)

The main world generation engine:
- Terrain generation
- Biome placement
- Structure generation
- Feature placement

### Procedural Library (146 classes)

Utilities for procedural generation:
- Noise functions
- Logic operations
- Conditions
- Random generation

---

## Procedural Library Subpackages

### procedurallib.logic (42 classes)
Logic operations for procedural generation.

### procedurallib.json (37 classes)
JSON-based procedural definitions.

### procedurallib.condition (21 classes)
Conditional logic for generation rules.

### procedurallib.property (18 classes)
Property definitions.

### procedurallib.supplier (17 classes)
Value suppliers for generation.

### procedurallib.random (5 classes)
Random number generation utilities.

### Core Noise Classes

```java
NoiseFunction      // Base noise function
NoiseFunction2d    // 2D noise
NoiseFunction3d    // 3D noise
NoiseFunctionPair  // Combined noise
NoiseType          // Noise algorithm types
```

---

## Noise Functions

### 2D Noise

```java
NoiseFunction2d noise = new NoiseFunction2d(seed);
float value = noise.sample(x, z);
```

Use cases:
- Height maps
- Temperature maps
- Moisture maps

### 3D Noise

```java
NoiseFunction3d noise = new NoiseFunction3d(seed);
float value = noise.sample(x, y, z);
```

Use cases:
- Cave generation
- Ore distribution
- Cloud patterns

---

## World Protocol Classes

### WorldInteraction
Interactions with the world.

### WorldEnvironment
Environment settings.

- Time of day
- Weather
- Lighting

### WorldParticle
Particles in world space.

---

## World Chunks

### Chunk System
Worlds are divided into chunks for efficient loading.

- Chunk loading/unloading
- Chunk generation
- Chunk saving

### Chunk Coordinates

```java
int chunkX = worldX >> 4;  // Divide by 16
int chunkZ = worldZ >> 4;
```

---

## Biomes

Biomes define regional characteristics:
- Terrain shape
- Block palette
- Vegetation
- Mob spawning
- Weather patterns

---

## Structures

Generated structures:
- Buildings
- Dungeons
- Villages
- Ruins

---

## World Manipulation

### Getting Blocks

```java
BlockType block = world.getBlock(x, y, z);
```

### Setting Blocks

```java
world.setBlock(x, y, z, blockType);
```

### Filling Regions

```java
world.fill(x1, y1, z1, x2, y2, z2, blockType);
```

---

## Weather System

Located in `com.hypixel.hytale.builtin.weather` (8 classes)

```java
protocol.Weather {
    // Weather type
    // Intensity
    // Duration
}
```

---

## Fluids

Located in `com.hypixel.hytale.builtin.fluid` (4 classes)

```java
protocol.Fluid {
    // Fluid type (water, lava)
    // Flow properties
}

protocol.FluidFX {
    // Visual effects
}
```

---

## Time of Day

```java
// Get world time
float timeOfDay = world.getTimeOfDay();

// Set world time
world.setTimeOfDay(0.5f); // Noon
```

Time values:
- 0.0 = Midnight
- 0.25 = Sunrise
- 0.5 = Noon
- 0.75 = Sunset

---

## Spawning

Located in `com.hypixel.hytale.server.spawning` (82 classes)

Entity spawning system:
- Mob spawning rules
- Spawn conditions
- Population limits

---

## Best Practices

1. **Use noise for procedural content** - Create natural-looking terrain
2. **Respect chunk boundaries** - Generate within chunks
3. **Cache chunk data** - Don't regenerate repeatedly
4. **Use biome data** - Match content to biome
5. **Consider performance** - World gen runs on load

---

## See Also

- [Block System](block-system.md) - Block types
- [Entity System](entity-system.md) - Entity spawning
- [Built-in Systems](builtin-systems.md) - World generation systems
- [API Reference](../api-reference/packages.md) - Package details
