# Hytale Server API Documentation

Complete documentation extracted from `HytaleServer.jar` for plugin development.

---

## 📚 Documentation Files

### Main Documentation

1. **[API-DOCUMENTATION.md](API-DOCUMENTATION.md)** - Complete API overview
   - Package breakdown by category
   - Third-party library reference
   - Usage recommendations
   - 16,249 total classes documented

2. **[PACKAGE-REFERENCE.md](PACKAGE-REFERENCE.md)** - Detailed package reference
   - Complete breakdown of all 5,218 Hytale API classes
   - Package hierarchy and organization
   - Class counts per package
   - Usage recommendations by category

3. **[QUICK-START-GUIDE.md](QUICK-START-GUIDE.md)** - Quick reference guide
   - Common plugin development tasks
   - Code examples and patterns
   - Best practices
   - 20+ common tasks covered

### Generated Data Files

4. **[class-details/METHOD-SIGNATURES.md](class-details/METHOD-SIGNATURES.md)** ⭐ NEW!
   - **Complete method signatures for 96 key classes**
   - **Public methods with parameters and return types**
   - **Public fields and constructors**
   - **8,650 lines of detailed API reference**

5. **all-classes.txt** - Complete list of all 16,249 classes in the JAR
6. **hytale-classes.txt** - Filtered list of 5,218 Hytale API classes
7. **package-summary.txt** - Package grouping with class counts
8. **packages-list.txt** - Clean package list with counts
9. **class-list.txt** - Sample class list (first 100 classes)

---

## 🚀 Quick Navigation

### Method Signatures & API Details ⭐ NEW!

- **[Complete Method Signatures](class-details/METHOD-SIGNATURES.md)** - Detailed API reference for 96 classes
  - Event System (12 classes)
  - Component System / ECS (16 classes)
  - Asset Management (8 classes)
  - Math Utilities (6 classes)
  - Protocol Types (54+ classes)

### By Development Task

### By Development Task

- **Creating a Plugin** → [QUICK-START-GUIDE.md#1-plugin-basics](QUICK-START-GUIDE.md#1-plugin-basics)
- **Handling Events** → [QUICK-START-GUIDE.md#2-event-system](QUICK-START-GUIDE.md#2-event-system)
- **Working with Blocks** → [QUICK-START-GUIDE.md#4-block-system](QUICK-START-GUIDE.md#4-block-system)
- **Working with Entities** → [QUICK-START-GUIDE.md#5-entity-system](QUICK-START-GUIDE.md#5-entity-system)
- **Working with Items** → [QUICK-START-GUIDE.md#6-item-system](QUICK-START-GUIDE.md#6-item-system)
- **World Generation** → [QUICK-START-GUIDE.md#7-world-system](QUICK-START-GUIDE.md#7-world-system)

### By Package Category

- **Protocol Definitions** → [PACKAGE-REFERENCE.md#protocol-definitions-733-total-classes](PACKAGE-REFERENCE.md#protocol-definitions-733-total-classes)
- **Built-in Systems** → [PACKAGE-REFERENCE.md#built-in-systems-1283-total-classes](PACKAGE-REFERENCE.md#built-in-systems-1283-total-classes)
- **Server Systems** → [PACKAGE-REFERENCE.md#server-systems-329-total-classes](PACKAGE-REFERENCE.md#server-systems-329-total-classes)
- **Component System (ECS)** → [PACKAGE-REFERENCE.md#component-system-90-total-classes](PACKAGE-REFERENCE.md#component-system-90-total-classes)

---

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

## 🔧 Key Technologies

### Network & Communication
- **Netty** (1,425 classes) - High-performance networking
- **Protocol Buffers** (207 classes) - Data serialization

### Cryptography & Security
- **Bouncy Castle** (2,049 classes) - Cryptography
- **Google Tink** (750 classes) - Cryptographic APIs
- **Nimbus JOSE** (367 classes) - JWT/JWS/JWE

### Data Structures & Algorithms
- **fastutil** (2,331 classes) - High-performance collections

### Data Formats
- **BSON** (191 classes) - Binary JSON
- **Gson** (84 classes) - JSON processing

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

### Utilities (As Needed)
13. **com.hypixel.hytale.common** - Common utilities
14. **com.hypixel.hytale.logger** - Logging system
15. **com.hypixel.hytale.metrics** - Performance monitoring

---

## 💡 Getting Started

### 1. Read the Quick Start Guide
Start with [QUICK-START-GUIDE.md](QUICK-START-GUIDE.md) for practical examples and common patterns.

### 2. Browse the Package Reference
Explore [PACKAGE-REFERENCE.md](PACKAGE-REFERENCE.md) to understand the API structure.

### 3. Decompile the JAR
For detailed implementation:

**Using IntelliJ IDEA:**
1. Right-click on `jars/HytaleServer.jar`
2. Select "Add as Library"
3. Browse the decompiled source code

**Using JD-GUI:**
1. Download from http://java-decompiler.github.io/
2. Open `HytaleServer.jar` in JD-GUI
3. Export source if needed

### 4. Explore Example Code
Look at existing plugins in the project:
- `src/main/java/com/example/minimap/` - Minimap plugin example
- `src/main/java/com/example/templateplugin/` - Template plugin

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

## 📖 Common Use Cases

### 1. Listen to Game Events
```java
// Register event listener
eventRegistry.register(SomeEvent.class, this::handleEvent);
```
See: [Event System Guide](QUICK-START-GUIDE.md#2-event-system)

### 2. Add Custom Blocks
```java
// Register block asset
assetStore.register(blockAsset);
```
See: [Block System Guide](QUICK-START-GUIDE.md#4-block-system)

### 3. Create Custom Entities
```java
// Use Component System
componentRegistry.register(CustomComponent.class);
```
See: [Entity System Guide](QUICK-START-GUIDE.md#5-entity-system)

### 4. Add Custom Items
```java
// Register item through asset system
assetStore.register(itemAsset);
```
See: [Item System Guide](QUICK-START-GUIDE.md#6-item-system)

### 5. Modify World Generation
```java
// Hook into world generation events
// Use procedurallib for noise functions
```
See: [World System Guide](QUICK-START-GUIDE.md#7-world-system)

---

## ⚠️ Important Notes

### API Stability
- This is a reverse-engineered documentation
- API may change between versions
- Always check compatibility with your target server version

### Internal vs Public API
- Not all classes are meant for public use
- Classes in `*.internal.*` packages are implementation details
- Prefer using protocol classes and high-level APIs

### Performance Considerations
- Use the Component System (ECS) for entity data
- Leverage the asset store for resources
- Monitor performance with the metrics system
- Use async events when possible

---

## 🔍 Finding Specific Functionality

### Search Strategy

1. **By Task** → Use [QUICK-START-GUIDE.md](QUICK-START-GUIDE.md)
2. **By Package** → Use [PACKAGE-REFERENCE.md](PACKAGE-REFERENCE.md)
3. **By Class Name** → Search in `hytale-classes.txt`
4. **By Protocol Type** → Look in `protocol.*` packages

### Example Searches

**"How do I work with particles?"**
→ Search for "Particle" in QUICK-START-GUIDE.md
→ Found: Section 10 - Particles and Visual Effects

**"What's in the crafting system?"**
→ Search for "crafting" in PACKAGE-REFERENCE.md
→ Found: builtin.crafting (17 classes)

**"Which class handles player movement?"**
→ Search for "Movement" in hytale-classes.txt or protocol section
→ Found: protocol.MovementSettings, protocol.MovementType, etc.

---

## 🤝 Contributing

If you discover new patterns or best practices:
1. Document them
2. Add examples to the guides
3. Share with the community

---

## 📝 Version Information

- **Generated From**: `jars/HytaleServer.jar`
- **Generation Date**: January 19, 2026
- **Total Classes Analyzed**: 16,249
- **Documentation Files**: 8

---

## 📄 License

This documentation is generated from Hytale Server binaries. The Hytale server and its APIs are property of Hypixel Studios. This documentation is for educational and development purposes.

---

## 🔗 Related Resources

- **Project Root**: `../../` - Main project directory
- **Example Plugins**: `../../src/main/java/com/example/`
- **Build Configuration**: `../../build.gradle.kts`
- **Plugin Manifest**: `../../src/main/resources/manifest.json`

---

*For questions or issues, refer to the official Hytale documentation when available.*
