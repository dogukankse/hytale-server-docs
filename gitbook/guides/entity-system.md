# Entity System

Hytale uses an Entity Component System (ECS) architecture for managing entities. This guide covers components, systems, archetypes, and entity management.

---

## Overview

**Key Packages:**
- `com.hypixel.hytale.component.*` - Component system (90 classes)
- `com.hypixel.hytale.server.core.entity.*` - Entity system

---

## ECS Architecture

The Entity Component System separates data (Components) from logic (Systems):

```
Entities
    ↓
Components (Data)
    ↓
Systems (Logic)
    ↓
Archetypes (Entity Templates)
```

### Benefits
- **Performance** - Cache-friendly data layout
- **Flexibility** - Compose entities from reusable parts
- **Decoupling** - Systems don't depend on each other

---

## Core Classes

### Component
Base interface for all components.

```java
public interface Component<ECS_TYPE> extends Cloneable {
    Component<ECS_TYPE> clone();
    default Component<ECS_TYPE> cloneSerializable();
}

// Static field
public static final Component[] EMPTY_ARRAY;
```

### ComponentType
Registry entry for a component type.

### ComponentRegistry
Manages component registrations.

```java
// Register a custom component
componentRegistry.register(MyComponent.class);
```

### ComponentRegistration
Handle for a registered component.

### IComponentRegistry
Interface for component registries.

### Store
Stores component data for entities.

### Archetype
Template defining which components an entity has.

### ArchetypeChunk
Storage unit for entities of the same archetype.

### Resource
Shared resource accessible to systems.

### ResourceType
Registry entry for a resource type.

### ResourceRegistration
Handle for a registered resource.

### SystemType
Defines a system that processes components.

### SystemGroup
Groups related systems together.

### Holder
Holds a reference to a component instance.

### Ref
Reference to an entity or component.

### CommandBuffer
Queues entity operations for batch execution.

---

## Component Subpackages

### component.system (24 classes)
System definitions and execution.

### component.data (10 classes)
Component data structures.

### component.dependency (8 classes)
Dependency injection for systems.

### component.query (7 classes)
Querying entities by components.

### component.spatial (6 classes)
Spatial partitioning for entities.

### component.event (3 classes)
Component-related events.

### component.task (2 classes)
Task scheduling for systems.

### component.metric (2 classes)
Performance metrics.

---

## Creating Components

### Define a Component

```java
public class HealthComponent implements Component<MyECSType> {
    public float health;
    public float maxHealth;
    
    public HealthComponent() {
        this.health = 100f;
        this.maxHealth = 100f;
    }
    
    @Override
    public Component<MyECSType> clone() {
        HealthComponent copy = new HealthComponent();
        copy.health = this.health;
        copy.maxHealth = this.maxHealth;
        return copy;
    }
}
```

### Register the Component

```java
componentRegistry.register(HealthComponent.class);
```

---

## Entity Protocol Classes

### EntityUpdate
Entity state updates sent over network.

### EntityEffect
Visual and audio effects on entities.

### EntityStatType
Types of entity statistics.

### EntityStatUpdate
Stat modification events.

### EntityUIType
Entity UI types (health bars, nameplates).

### EntityMatcher
Utility for selecting/filtering entities.

---

## Entity Interactions

### DamageEntityInteraction
Deals damage to an entity.

### RemoveEntityInteraction
Removes an entity from the world.

### UseEntityInteraction
Interacts with an entity (talk, trade, etc.).

---

## Querying Entities

### By Component

```java
// Query all entities with HealthComponent
Query<HealthComponent> query = world.query(HealthComponent.class);

for (Entity entity : query) {
    HealthComponent health = entity.get(HealthComponent.class);
    // Process entity
}
```

### Multiple Components

```java
// Query entities with multiple components
Query<HealthComponent, PositionComponent> query = 
    world.query(HealthComponent.class, PositionComponent.class);
```

### With Filters

```java
// Query with filter
Query<HealthComponent> query = world.query(HealthComponent.class)
    .where(health -> health.health < health.maxHealth);
```

---

## Systems

Systems contain the logic that operates on components.

### Define a System

```java
public class HealthRegenSystem implements System {
    
    public void update(float deltaTime) {
        for (Entity entity : query(HealthComponent.class)) {
            HealthComponent health = entity.get(HealthComponent.class);
            
            if (health.health < health.maxHealth) {
                health.health += 1f * deltaTime;
                health.health = Math.min(health.health, health.maxHealth);
            }
        }
    }
}
```

---

## Archetypes

Archetypes define which components an entity has.

### Common Archetypes
- Player - Position, Health, Inventory, etc.
- Monster - Position, Health, AI, etc.
- Item - Position, ItemData, etc.

---

## Best Practices

1. **Keep components data-only** - No logic in components
2. **Small, focused components** - One responsibility per component
3. **Use archetypes** - Template common entity types
4. **Batch operations** - Use CommandBuffer for bulk changes
5. **Query efficiently** - Cache queries when possible

---

## See Also

- [Block System](block-system.md) - Block entities
- [Item System](item-system.md) - Item entities
- [World System](world-system.md) - Entity spawning
- [Method Signatures](../api-reference/method-signatures.md) - Component class details
