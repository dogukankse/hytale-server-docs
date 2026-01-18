# Block System

The Block System handles everything related to blocks in Hytale, including block types, properties, interactions, and placement.

---

## Overview

**Key Packages:**
- `com.hypixel.hytale.server.core.block.*` - Block system
- `com.hypixel.hytale.protocol.*` - Block protocol classes

---

## Protocol Classes

### BlockType
Defines a block type with all its properties.

- Identifier and metadata
- Material and physical properties
- Textures and rendering
- Sound effects
- Placement and rotation rules

### BlockPosition
Represents a position in the block grid.

- X, Y, Z coordinates
- Conversion to/from world coordinates

### BlockMaterial
Defines material properties of a block.

- Hardness
- Resistance
- Tool requirements
- Physics behavior

### BlockTextures
Texture definitions for block faces.

- Top, bottom, side textures
- Connected textures
- Animation frames

### BlockSoundSet
Audio events for block interactions.

- Place sound
- Break sound
- Step sound
- Hit sound

### BlockPlacementSettings
Rules for placing blocks.

- Placement conditions
- Rotation behavior
- Snapping rules

### BlockRotation
Block orientation data.

- Rotation states
- Axis alignment

### BlockMatcher
Utility for matching/selecting blocks.

- By type
- By properties
- By position

---

## Block Interactions

### BreakBlockInteraction
Handles breaking blocks.

```java
// Protocol class for block breaking
protocol.BreakBlockInteraction {
    BlockPosition position;
    // Break progress, tool used, etc.
}
```

### PlaceBlockInteraction
Handles placing blocks.

```java
// Protocol class for block placement
protocol.PlaceBlockInteraction {
    BlockPosition position;
    BlockType blockType;
    BlockRotation rotation;
}
```

### ChangeBlockInteraction
Handles modifying existing blocks.

```java
// Protocol class for block changes
protocol.ChangeBlockInteraction {
    BlockPosition position;
    // New properties
}
```

### UseBlockInteraction
Handles using/activating blocks.

```java
// Protocol class for block usage
protocol.UseBlockInteraction {
    BlockPosition position;
    // Interaction type
}
```

---

## Working with Blocks

### Getting Block at Position

```java
// Conceptual example
BlockType block = world.getBlockAt(x, y, z);
```

### Setting Block

```java
// Conceptual example
world.setBlock(x, y, z, blockType);
```

### Block Properties

```java
// Access block properties
BlockMaterial material = blockType.getMaterial();
boolean isSolid = material.isSolid();
float hardness = material.getHardness();
```

---

## Block Breaking Visuals

Located in `com.hypixel.hytale.server.core.asset.type.blockbreakingdecal.*`

Handles the visual feedback when breaking blocks:
- Crack overlays
- Particle effects
- Progress indicators

---

## Block Physics

Located in `com.hypixel.hytale.builtin.blockphysics` (5 classes)

Handles physical behavior:
- Falling blocks (sand, gravel)
- Physics simulation
- Collision detection

---

## Block Ticking

Located in `com.hypixel.hytale.builtin.blocktick` (5 classes)

Handles block updates:
- Scheduled updates
- Random ticks
- Neighbor updates

---

## Block Spawning

Located in `com.hypixel.hytale.builtin.blockspawner` (7 classes)

Handles entity spawning from blocks:
- Mob spawners
- Natural spawning

---

## Best Practices

1. **Use protocol classes** - `BlockType`, `BlockPosition`, etc.
2. **Handle null blocks** - Check for air/void
3. **Respect physics** - Consider falling blocks, fluids
4. **Batch operations** - Group multiple block changes
5. **Use events** - React to block changes via events

---

## See Also

- [Entity System](entity-system.md) - Entities and ECS
- [World System](world-system.md) - World generation
- [Asset System](asset-system.md) - Block assets
- [API Reference](../api-reference/packages.md) - Package details
