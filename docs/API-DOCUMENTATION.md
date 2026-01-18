# Hytale Server API Documentation

## Overview

This documentation is generated from `jars/HytaleServer.jar` and provides a comprehensive reference of all available classes and packages in the Hytale Server API.

**Total Classes**: 16,249
**Hytale API Classes**: 5,218
**Third-Party Libraries**: 11,031

---

## Main Packages

### 1. Hytale Core API (com.hypixel.hytale)

The core Hytale API with 5,218 classes across multiple packages:

#### Key Package Groups:

##### Server Package (com.hypixel.hytale.server) - 2,582 classes
The largest package containing the server-side API:
- **Asset Management** - Loading and managing game assets
- **Block System** - Block types, properties, and behaviors
- **Entity System** - Entity management and AI
- **World Management** - World generation and manipulation
- **Player Management** - Player data, sessions, and interactions
- **Network Protocol** - Server-client communication
- **Commands** - Server command system
- **Events** - Event handling system

##### Built-in Systems (com.hypixel.hytale.builtin) - 1,283 classes
Built-in game systems and features:
- Configuration types
- Default implementations
- Standard game mechanics

##### Protocol Package (com.hypixel.hytale.protocol) - 733 classes
Network protocol definitions and packet handling

##### Codec Package (com.hypixel.hytale.codec) - 125 classes
Serialization and deserialization utilities

##### Procedural Library (com.hypixel.hytale.procedurallib) - 146 classes
Procedural generation utilities

##### Component System (com.hypixel.hytale.component) - 90 classes
Component-based entity system

##### Math Utilities (com.hypixel.hytale.math) - 81 classes
Mathematical utilities for game development

##### Common Utilities (com.hypixel.hytale.common) - 47 classes
Shared utility classes

##### Asset Store (com.hypixel.hytale.assetstore) - 40 classes
Asset storage and retrieval

##### Function System (com.hypixel.hytale.function) - 34 classes
Function handling and execution

##### Event System (com.hypixel.hytale.event) - 15 classes
Core event system classes

##### Logger (com.hypixel.hytale.logger) - 11 classes
Logging utilities

##### Metrics (com.hypixel.hytale.metrics) - 10 classes
Performance and telemetry metrics

##### Plugin System (com.hypixel.hytale.plugin) - 3 classes
Plugin loading and management

##### Storage (com.hypixel.hytale.storage) - 3 classes
Data storage utilities

##### Registry (com.hypixel.hytale.registry) - 2 classes
Registry system for game objects

---

## Third-Party Libraries

### Network and Communication
- **io.netty** (1,425 classes) - High-performance network framework
  - Handler: 739 classes
  - Utilities: 309 classes
  - Channel: 285 classes
  - Buffer: 92 classes

### Data Structures
- **it.unimi.dsi** (2,331 classes) - Fast utilities for Java
  - High-performance collections
  - Compression utilities

### Cryptography
- **org.bouncycastle** (2,049 classes) - Cryptographic library
  - Crypto: 633 classes
  - ASN.1: 629 classes
  - Post-quantum crypto: 617 classes
  - JCA/JCE: 387 classes
  - CMS: 173 classes

- **com.google.crypto** (750 classes) - Google Tink cryptographic library

### Security and Authentication
- **com.nimbusds.jose** (367 classes) - JOSE (JSON Object Signing and Encryption)

### Data Formats
- **com.google.protobuf** (207 classes) - Protocol Buffers
- **org.bson** (191 classes) - BSON (Binary JSON) codec

### JSON Processing
- **com.google.gson** (84 classes) - JSON serialization/deserialization

### Parsing
- **ch.randelshofer.fastdoubleparser** (84 classes) - Fast number parsing

### Utilities
- **com.google.common** (76 classes) - Google Guava utilities

### Terminal/Console
- **org.jline** (117 classes) - Terminal handling and readline functionality

### Monitoring
- **io.sentry** (46+ classes) - Application monitoring and error tracking

---

## Detailed Package Structure

### com.hypixel.hytale.server Subpackages

The server package is the heart of the Hytale API. Here are the key subpackages:

#### Asset System
- `com.hypixel.hytale.server.core.asset` - Asset loading and management
- `com.hypixel.hytale.server.core.asset.type` - Various asset types (blocks, items, entities, etc.)
- `com.hypixel.hytale.server.core.asset.common` - Common asset handling

#### Block System
- `com.hypixel.hytale.server.core.block` - Block definitions and behaviors
- `com.hypixel.hytale.server.core.block.state` - Block state management

#### Entity System
- `com.hypixel.hytale.server.core.entity` - Entity management
- `com.hypixel.hytale.server.core.entity.ai` - Entity AI systems
- `com.hypixel.hytale.server.core.entity.component` - Entity components

#### World System
- `com.hypixel.hytale.server.core.world` - World management
- `com.hypixel.hytale.server.core.world.generation` - World generation
- `com.hypixel.hytale.server.core.world.chunk` - Chunk handling

#### Player System
- `com.hypixel.hytale.server.core.player` - Player management
- `com.hypixel.hytale.server.core.player.session` - Player sessions

#### Network
- `com.hypixel.hytale.server.network` - Network handling
- `com.hypixel.hytale.server.network.packet` - Packet definitions

#### Commands
- `com.hypixel.hytale.server.command` - Command system

#### Events
- `com.hypixel.hytale.server.event` - Server events

---

## Usage in Plugin Development

### Key Classes for Plugin Development

When developing Hytale plugins, you'll primarily interact with these packages:

1. **Plugin System**
   - `com.hypixel.hytale.plugin.*` - Plugin lifecycle and loading

2. **Event System**
   - `com.hypixel.hytale.event.*` - Event handling
   - `com.hypixel.hytale.server.event.*` - Server-specific events

3. **Asset Management**
   - `com.hypixel.hytale.server.core.asset.*` - Loading custom assets

4. **Entity API**
   - `com.hypixel.hytale.server.core.entity.*` - Entity manipulation

5. **Block API**
   - `com.hypixel.hytale.server.core.block.*` - Block manipulation

6. **World API**
   - `com.hypixel.hytale.server.core.world.*` - World access and generation

7. **Player API**
   - `com.hypixel.hytale.server.core.player.*` - Player data and interactions

8. **Commands**
   - `com.hypixel.hytale.server.command.*` - Registering custom commands

---

## File Generation

This documentation was generated from:
- **Source**: `jars/HytaleServer.jar`
- **Date**: January 19, 2026
- **Method**: JAR analysis and class extraction

### Generated Files

1. `all-classes.txt` - Complete list of all 16,249 classes
2. `hytale-classes.txt` - Filtered list of 5,218 Hytale API classes
3. `package-summary.txt` - Package grouping with class counts
4. `packages-list.txt` - Clean package list
5. `class-list.txt` - Sample class list (first 100 classes)

---

## Additional Resources

For more detailed information about specific classes and methods, you can:

1. **Decompile the JAR**: Use a Java decompiler like JD-GUI, IntelliJ IDEA, or Fernflower to browse the source code
2. **Use JavaDoc**: If official JavaDoc is available, refer to it for detailed API documentation
3. **Explore the examples**: Check existing plugins and examples for practical usage patterns

---

## Notes

- This is a reverse-engineered documentation based on class names and package structure
- For detailed method signatures, parameters, and return types, decompile the JAR file
- The API may change between versions - always check compatibility with your target server version
- Some packages contain internal implementation details and should not be directly used in plugins

---

## Next Steps

To use this API in your plugin:

1. Add the HytaleServer.jar to your project dependencies (already configured in build.gradle.kts)
2. Import the necessary packages in your plugin code
3. Implement the plugin interface and event listeners
4. Build and test your plugin with the Hytale server

Refer to the example plugins in the project for practical implementation patterns.
