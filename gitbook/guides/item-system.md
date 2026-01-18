# Item System

The Item System handles items, weapons, armor, tools, and inventory management.

---

## Overview

**Key Packages:**
- `com.hypixel.hytale.protocol.*` - Item protocol classes

---

## Item Protocol Classes

### ItemBase
Base class for all items.

### ItemLibrary
Registry of all item types.

### ItemCategory
Categories for organizing items.

### ItemQuality
Item rarity/quality levels.

### ItemQuantity
Stack sizes and quantities.

---

## Item Types

### ItemWeapon
Weapon items (swords, axes, bows, etc.)

Properties:
- Damage
- Attack speed
- Range
- Special abilities

### ItemArmor
Armor pieces (helmet, chestplate, leggings, boots)

Properties:
- Defense
- Durability
- Set bonuses
- Weight

### ItemTool
Tools (pickaxes, shovels, hoes, etc.)

Properties:
- Mining speed
- Durability
- Material tier

### ItemUtility
Utility items (potions, scrolls, etc.)

Properties:
- Effects
- Duration
- Charges

### ItemGlider
Glider items for aerial movement.

Properties:
- Glide speed
- Durability
- Control

---

## Item Properties

### ItemSoundSet
Audio events for item usage.

- Equip sound
- Use sound
- Drop sound

### ItemReticle
Crosshair/reticle configuration.

- Reticle type
- Dynamic sizing

### ItemPlayerAnimations
Animation data for player holding items.

- Idle animation
- Use animation
- Attack animation

---

## Inventory System

### ModifyInventoryInteraction
Interaction for modifying inventory contents.

```java
protocol.ModifyInventoryInteraction {
    // Add, remove, or move items
}
```

### InventorySection
Sections of the inventory.

- Main inventory
- Hotbar
- Equipment slots
- Storage

### InventoryActionType
Types of inventory actions.

- Pick up
- Drop
- Move
- Split
- Merge

---

## Working with Items

### Creating Items

```java
// Conceptual example
ItemBase myItem = new ItemBase();
myItem.setId("my_plugin:my_item");
myItem.setCategory(ItemCategory.TOOL);
myItem.setQuality(ItemQuality.RARE);
```

### Registering Items

```java
// Register with asset system
assetStore.register(myItemAsset);
```

### Giving Items to Players

```java
// Via inventory interaction
ModifyInventoryInteraction interaction = new ModifyInventoryInteraction();
interaction.setAction(InventoryActionType.ADD);
interaction.setItem(myItem);
interaction.setQuantity(1);
```

---

## Item Interactions

### UseItemInteraction
Triggered when player uses an item.

### DropItemInteraction
Triggered when player drops an item.

### EquipItemInteraction
Triggered when player equips an item.

---

## Item Crafting

See [Built-in Systems](builtin-systems.md) for crafting recipes.

```java
// Crafting recipe structure
protocol.CraftingRecipe {
    ItemBase result;
    ItemBase[] ingredients;
    int resultQuantity;
}
```

---

## Quality Levels

| Quality | Description |
|---------|-------------|
| Common | Standard items |
| Uncommon | Slightly better |
| Rare | Hard to find |
| Epic | Very rare |
| Legendary | Extremely rare |

---

## Best Practices

1. **Use ItemLibrary** - Register items properly
2. **Define categories** - Organize items logically
3. **Set quality levels** - Indicate item rarity
4. **Configure sounds** - Add audio feedback
5. **Handle stacking** - Respect stack limits

---

## See Also

- [Entity System](entity-system.md) - Item entities
- [Block System](block-system.md) - Block drops
- [Built-in Systems](builtin-systems.md) - Crafting
- [API Reference](../api-reference/packages.md) - Package details
