# Development Guides

Comprehensive guides for developing Hytale Server plugins. Each guide focuses on a specific system or feature.

## Core Systems

| Guide | Description |
|-------|-------------|
| [Plugin Basics](plugin-basics.md) | Plugin structure, lifecycle, and manifest |
| [Event System](event-system.md) | Registering and handling game events |
| [Asset System](asset-system.md) | Loading and managing custom assets |

## Game Systems

| Guide | Description |
|-------|-------------|
| [Block System](block-system.md) | Working with blocks and block types |
| [Entity System](entity-system.md) | Entity Component System (ECS) |
| [Item System](item-system.md) | Items, weapons, armor, and inventory |
| [World System](world-system.md) | World generation and manipulation |
| [Player System](player-system.md) | Player management and interactions |

## Advanced Systems

| Guide | Description |
|-------|-------------|
| [Particles & Effects](particles-effects.md) | Visual effects and particle systems |
| [Audio System](audio-system.md) | Sound events and ambient audio |
| [Built-in Systems](builtin-systems.md) | Adventure, crafting, mounts, and more |

---

## Learning Path

### Week 1: Basics
- [ ] Read [Plugin Basics](plugin-basics.md)
- [ ] Create a simple plugin
- [ ] Read [Event System](event-system.md)
- [ ] Register an event listener

### Week 2: Core Concepts
- [ ] Understand protocol classes
- [ ] Work with [Block System](block-system.md)
- [ ] Work with [Entity System](entity-system.md)
- [ ] Experiment with [Item System](item-system.md)

### Week 3: Advanced Features
- [ ] Learn [Asset System](asset-system.md)
- [ ] Create custom assets
- [ ] Implement custom interactions
- [ ] Explore [World System](world-system.md)

### Week 4: Mastery
- [ ] Study [Built-in Systems](builtin-systems.md)
- [ ] Create complex features
- [ ] Optimize with metrics

---

## Quick Reference

### Essential Packages
- `com.hypixel.hytale.plugin.*` - Plugin lifecycle
- `com.hypixel.hytale.event.*` - Event handling
- `com.hypixel.hytale.assetstore.*` - Custom assets
- `com.hypixel.hytale.component.*` - ECS for entities

### Common Patterns

**Register an event:**
```java
eventRegistry.register(SomeEvent.class, this::handleEvent);
```

**Register a component:**
```java
componentRegistry.register(CustomComponent.class);
```

**Register an asset:**
```java
assetStore.register(myAsset);
```

---

## See Also

- [Quick Start Guide](../getting-started/quick-start.md)
- [API Reference](../api-reference/README.md)
- [Method Signatures](../api-reference/method-signatures.md)
