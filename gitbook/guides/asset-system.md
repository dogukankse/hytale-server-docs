# Asset System

The Asset System manages game resources like blocks, items, textures, sounds, and other game content.

---

## Overview

**Key Packages:**
- `com.hypixel.hytale.assetstore.*` - Asset management (40 classes)
- `com.hypixel.hytale.server.core.asset.*` - Server-side asset loading

**Core Classes:**
- `AssetStore` - Main asset storage
- `AssetRegistry` - Asset registration
- `AssetPack` - Asset packs
- `AssetHolder` - Asset references
- `JsonAsset` - JSON-based assets
- `RawAsset` - Raw binary assets
- `DecodedAsset` - Decoded assets

---

## Asset Store

The `AssetStore` is the central repository for all game assets.

### Registering Assets

```java
// Register a custom asset
assetStore.register(myAsset);
```

### Asset Types

Located in `com.hypixel.hytale.server.core.asset.type.*`:

| Category | Description |
|----------|-------------|
| `ambiencefx.*` | Ambient effects |
| `audiocategory.*` | Audio categories |
| `blockbreakingdecal.*` | Block breaking visuals |
| `blocktype.*` | Block types |
| `itemtype.*` | Item types |
| `entitytype.*` | Entity types |
| `particle.*` | Particle definitions |

---

## Asset Classes

### AssetPack

Groups related assets together.

```java
// Asset pack structure
AssetPack {
    String id;
    List<Asset> assets;
    // ...
}
```

### AssetHolder

Holds a reference to an asset.

### JsonAsset

JSON-based asset definition.

### RawAsset

Binary asset data (textures, sounds, models).

### DecodedAsset

Parsed and ready-to-use asset.

---

## Asset Events

### AssetPackRegisterEvent

Fired when an asset pack is registered.

```java
eventRegistry.register(AssetPackRegisterEvent.class, event -> {
    // Access the registered asset pack
    AssetPack pack = event.getAssetPack();
});
```

### AssetPackUnregisterEvent

Fired when an asset pack is removed.

```java
eventRegistry.register(AssetPackUnregisterEvent.class, event -> {
    // Cleanup references to the asset pack
});
```

### LoadAssetEvent

Fired when an asset is loaded.

```java
eventRegistry.register(LoadAssetEvent.class, event -> {
    // Process the loaded asset
});
```

### GenerateSchemaEvent

Fired during schema generation.

---

## Asset Store Subpackages

### assetstore.event (9 classes)
Asset loading events.

### assetstore.map (9 classes)
Asset mapping utilities.

### assetstore.codec (4 classes)
Asset serialization.

### assetstore.iterator (2 classes)
Asset iteration utilities.

---

## Loading Custom Assets

### From JSON

```java
// Example JSON asset structure
{
    "type": "block",
    "id": "my_custom_block",
    "properties": {
        // Block properties
    }
}
```

### From Resources

```java
// Load assets from plugin resources
InputStream stream = getClass().getResourceAsStream("/assets/my_asset.json");
```

---

## Asset Organization

### Recommended Structure

```
src/main/resources/
└── assets/
    ├── blocks/
    │   └── my_block.json
    ├── items/
    │   └── my_item.json
    ├── entities/
    │   └── my_entity.json
    ├── textures/
    │   └── my_texture.png
    └── sounds/
        └── my_sound.ogg
```

---

## Best Practices

1. **Organize by type** - Group assets in subdirectories
2. **Use meaningful IDs** - Prefix with your plugin ID
3. **Handle missing assets** - Check if assets exist before use
4. **Cleanup on disable** - Unregister assets when plugin disables
5. **Use asset packs** - Group related assets together

---

## See Also

- [Block System](block-system.md) - Block assets
- [Item System](item-system.md) - Item assets
- [Audio System](audio-system.md) - Sound assets
- [API Reference](../api-reference/packages.md) - Package details
