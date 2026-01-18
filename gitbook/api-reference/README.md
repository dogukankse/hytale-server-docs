# API Reference

This section provides detailed reference documentation for the Hytale Server API.

## Overview

The Hytale Server API contains **16,249 total classes**:
- **5,218** Hytale API classes (32.1%)
- **11,031** Third-party library classes (67.9%)

## Documentation Coverage

| Category | Status |
|----------|--------|
| Package Reference | ✅ Complete |
| Method Signatures | ✅ 96 key classes |
| Class Descriptions | ✅ All classes listed |
| Usage Examples | ~30% coverage |

## Quick Links

- [Package Reference](packages.md) - Complete breakdown of all packages
- [Method Signatures](method-signatures.md) - Detailed signatures for 96 classes

---

## Main Packages

### 1. Hytale Core API (com.hypixel.hytale)

The core Hytale API with 5,218 classes across multiple packages:

| Package | Classes | Description |
|---------|---------|-------------|
| server.* | 2,582 | Server-side systems |
| builtin.* | 1,283 | Built-in game mechanics |
| protocol.* | 733 | Network protocol |
| procedurallib.* | 146 | Procedural generation |
| codec.* | 125 | Serialization |
| component.* | 90 | Entity Component System |
| math.* | 81 | Math utilities |
| common.* | 47 | Common utilities |
| assetstore.* | 40 | Asset management |
| function.* | 34 | Functional utilities |
| event.* | 15 | Event system |
| Other | 24 | Various utilities |

---

## Third-Party Libraries

### Network & Communication
- **io.netty** (1,425 classes) - High-performance networking
- **com.google.protobuf** (207 classes) - Protocol Buffers

### Data Structures
- **it.unimi.dsi** (2,331 classes) - Fast utilities for Java (fastutil)

### Cryptography
- **org.bouncycastle** (2,049 classes) - Cryptographic library
- **com.google.crypto** (750 classes) - Google Tink

### Security & Authentication
- **com.nimbusds.jose** (367 classes) - JOSE (JWT/JWS/JWE)

### Data Formats
- **org.bson** (191 classes) - BSON codec
- **com.google.gson** (84 classes) - JSON processing

### Utilities
- **com.google.common** (76 classes) - Google Guava
- **org.jline** (117 classes) - Terminal handling

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

## Notes

- This is reverse-engineered documentation based on class names and package structure
- For detailed method signatures, see the [Method Signatures](method-signatures.md) page
- The API may change between versions - always check compatibility
- Some packages contain internal implementation details and should not be directly used

---

## Next Steps

- Browse the [Package Reference](packages.md) for detailed package breakdown
- Check [Method Signatures](method-signatures.md) for specific class details
- Return to [Development Guides](../guides/README.md) for practical usage
