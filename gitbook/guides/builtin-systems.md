# Built-in Systems

Hytale includes many built-in game systems. This guide covers the major systems available in `com.hypixel.hytale.builtin.*`.

---

## Overview

The `builtin` package contains **1,283 classes** across various game systems.

---

## Major Systems

| System | Classes | Description |
|--------|---------|-------------|
| adventure | 217 | Adventure mode mechanics |
| buildertools | 192 | Builder/creative tools |
| portals | 52 | Portal system |
| asseteditor | 30 | In-game asset editing |
| instances | 29 | Instanced zones/dungeons |
| path | 29 | Pathfinding |
| npccombatactionevaluator | 27 | NPC combat AI |
| teleport | 26 | Teleportation |
| beds | 19 | Sleeping system |
| mounts | 18 | Mount/vehicle system |
| crafting | 17 | Crafting system |
| deployables | 15 | Deployable objects |
| ambience | 10 | Ambient effects |
| weather | 8 | Weather system |
| parkour | 7 | Parkour mechanics |
| commandmacro | 7 | Command macros |
| blockspawner | 7 | Block spawning |
| Others | ~600 | Various small systems |

---

## Adventure System (217 classes)

Adventure mode mechanics:
- Quest system
- Progression
- Objectives
- Rewards

---

## Builder Tools (192 classes)

Creative mode building tools:
- Selection tools
- Fill/replace
- Copy/paste
- Transform tools
- Brush tools

---

## Portal System (52 classes)

Interdimensional travel:
- Portal creation
- Destination linking
- Teleportation logic

---

## Crafting System (17 classes)

### CraftingRecipe

```java
protocol.CraftingRecipe {
    ItemBase result;
    ItemBase[] ingredients;
    int resultQuantity;
    CraftingType type;
}
```

### Crafting Types

- Shaped recipes (specific arrangement)
- Shapeless recipes (any arrangement)
- Smelting recipes
- Special recipes

---

## Mount System (18 classes)

### MountController

```java
protocol.MountController {
    // Mount properties
    float speed;
    float jumpHeight;
    // Control inputs
}
```

### Mount Features

- Mounting/dismounting
- Movement control
- Mount abilities
- Mount health

---

## Beds System (19 classes)

Sleeping and spawn management:
- Bed interaction
- Sleep cycle
- Spawn point setting
- Time skip

---

## Deployables System (15 classes)

Placeable items:
- Campfires
- Tents
- Turrets
- Traps

### DeployableConfig

```java
protocol.DeployableConfig {
    // Configuration options
}
```

---

## Weather System (8 classes)

Weather effects:
- Rain
- Snow
- Storms
- Clear weather

```java
protocol.Weather {
    WeatherType type;
    float intensity;
    float duration;
}
```

---

## Teleportation System (26 classes)

Teleportation mechanics:
- Waypoints
- Fast travel
- Teleport interactions

```java
protocol.TeleportInteraction {
    Position destination;
    boolean preserveRotation;
}
```

---

## Parkour System (7 classes)

Movement mechanics:
- Wall running
- Ledge grabbing
- Special jumps

---

## Movement Systems

### Mantling (1 class)
Climbing/mantling ledges.

### Crouch Slide (1 class)
Sliding while crouching.

### Sprint Force (1 class)
Sprint mechanics.

### Safety Roll (1 class)
Roll on landing to reduce damage.

---

## Pathfinding System (29 classes)

NPC navigation:
- Path calculation
- Obstacle avoidance
- Navigation mesh

---

## NPC Combat AI (27 classes)

Combat behavior:
- Action evaluation
- Target selection
- Attack patterns
- Defensive behavior

---

## Instances System (29 classes)

Instanced content:
- Dungeon instances
- Private zones
- Instance management

---

## Block Spawner (7 classes)

Entity spawning from blocks:
- Mob spawners
- Natural spawning

---

## Block Physics (5 classes)

Physical block behavior:
- Falling blocks
- Block physics simulation

---

## Block Tick (5 classes)

Block update system:
- Scheduled updates
- Random ticks
- Neighbor updates

---

## Fluid System (4 classes)

Fluid simulation:
- Water flow
- Lava flow
- Swimming

---

## Ambience System (10 classes)

Environmental atmosphere:
- Ambient sounds
- Visual effects
- Mood setting

---

## Land Discovery (3 classes)

Exploration tracking:
- Discovered areas
- Map revelation

---

## Tag Set (4 classes)

Tag-based grouping:
- Entity tags
- Block tags
- Item tags

---

## Command Macro (7 classes)

Command automation:
- Macro recording
- Macro playback
- Command sequences

---

## Asset Editor (30 classes)

In-game editing:
- Asset modification
- Live preview
- Hot reload

---

## World Generation (1 class)

Additional world generation utilities.

---

## Using Built-in Systems

### Referencing Built-in Classes

```java
import com.hypixel.hytale.builtin.crafting.*;
import com.hypixel.hytale.builtin.mounts.*;
import com.hypixel.hytale.builtin.teleport.*;
```

### Extending Built-in Behavior

```java
// Listen for crafting events
eventRegistry.register(CraftingEvent.class, event -> {
    // Modify or add to crafting behavior
});
```

---

## Best Practices

1. **Study built-in implementations** - Learn from existing code
2. **Use protocol classes** - Don't reinvent the wheel
3. **Hook into events** - Extend rather than replace
4. **Check for null** - Built-in systems may not always be active
5. **Respect game balance** - Don't break default mechanics

---

## See Also

- [Entity System](entity-system.md) - Entity management
- [Item System](item-system.md) - Item/crafting
- [World System](world-system.md) - World generation
- [API Reference](../api-reference/packages.md) - Package details
