# Hytale Server API Documentation

Complete documentation extracted from `HytaleServer.jar` for plugin development.

---

## Welcome

This documentation provides a comprehensive reference for developing plugins for the Hytale Server. It covers everything from basic plugin setup to advanced topics like the Entity Component System (ECS) and world generation.

## 📊 API Statistics

| Category | Classes | Description |
|----------|---------|-------------|
| **Hytale API** | 5,218 | Core Hytale server API |
| **Third-Party** | 11,031 | Supporting libraries |
| **Total** | **16,249** | All classes in JAR |

### Hytale API Breakdown

| Package | Classes | Purpose |
|---------|---------|---------|
| server.* | 2,582 | Server-side systems |
| builtin.* | 1,283 | Built-in game mechanics |
| protocol.* | 733 | Network protocol |
| procedurallib.* | 146 | Procedural generation |
| codec.* | 125 | Serialization |
| component.* | 90 | Entity Component System |
| math.* | 81 | Math utilities |
| Other | 178 | Various utilities |

---

## 🚀 Quick Navigation

### Getting Started
- **New to Hytale plugin development?** Start with the [Quick Start Guide](getting-started/quick-start.md)
- **Setting up your project?** Check [Plugin Basics](guides/plugin-basics.md)

### API Reference
- **Looking for a specific package?** Browse the [Package Reference](api-reference/packages.md)
- **Need method signatures?** See [Method Signatures](api-reference/method-signatures.md)

### Development Guides
- **Working with events?** Read the [Event System Guide](guides/event-system.md)
- **Creating custom blocks?** Check the [Block System Guide](guides/block-system.md)
- **Managing entities?** See the [Entity System Guide](guides/entity-system.md)

---

## 🎯 Most Important Packages for Plugin Development

### Essential (Must Know)
1. **com.hypixel.hytale.event** - Event system for hooking into game events
2. **com.hypixel.hytale.plugin** - Plugin lifecycle and management
3. **com.hypixel.hytale.component** - Entity Component System (ECS)
4. **com.hypixel.hytale.assetstore** - Asset loading and management

### Core Game Systems (Should Know)
5. **com.hypixel.hytale.protocol** - All game data structures (blocks, items, entities)
6. **com.hypixel.hytale.server.core.asset** - Server-side asset handling
7. **com.hypixel.hytale.math** - Vector math and utilities
8. **com.hypixel.hytale.codec** - Data serialization

### Built-in Systems (Good to Know)
9. **com.hypixel.hytale.builtin.adventure** - Adventure mode mechanics
10. **com.hypixel.hytale.builtin.buildertools** - Builder tools
11. **com.hypixel.hytale.builtin.crafting** - Crafting system
12. **com.hypixel.hytale.server.worldgen** - World generation

---

## 🏗️ Architecture Overview

### Plugin System
```
Plugin Entry Point
    ↓
Event Registration ← Events from Server
    ↓
Component System (ECS) ← Entity Data
    ↓
Asset Store ← Custom Assets
    ↓
Protocol Classes ← Game Data Structures
```

### Data Flow
```
Server
  ↓
Protocol (Network Layer)
  ↓
Built-in Systems (Game Logic)
  ↓
Component System (Entity Data)
  ↓
Plugin Hook Points
```

---

## ⚠️ Important Notes

### API Stability
- This is reverse-engineered documentation
- API may change between versions
- Always check compatibility with your target server version

### Internal vs Public API
- Not all classes are meant for public use
- Classes in `*.internal.*` packages are implementation details
- Prefer using protocol classes and high-level APIs

---

## 📝 Version Information

- **Generated From**: `HytaleServer.jar`
- **Generation Date**: January 19, 2026
- **Total Classes Analyzed**: 16,249
- **Documentation Coverage**: 96 classes with method signatures

---

## 📄 License

This documentation is generated from Hytale Server binaries. The Hytale server and its APIs are property of Hypixel Studios. This documentation is for educational and development purposes.

## Credits

Special thanks to **Britakee Studios** for their comprehensive [Hytale Modding Documentation](https://britakee-studios.gitbook.io/hytale-modding-documentation), which served as a primary source for the Server Administration and Content Creation guides.

