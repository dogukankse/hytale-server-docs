# Items API

This section details the Core API classes related to items.

## Core Classes

### `Item`
**Package**: `com.hypixel.hytale.server.core.asset.type.item.config`

The `Item` class represents the static configuration of an item type. It defines properties shared by all instances of that item.

*   **Usage**: Access base properties like name, ID, and utility components.
*   **Key Methods**:
    *   `getUtility()`: Returns the `ItemUtility` component.
    *   `getMaxStack()`: Returns max stack size.
*   **Reference**: [Item Method Signatures](api-reference/method-signatures/server-items.md#item)

### `ItemStack`
**Package**: `com.hypixel.hytale.server.core.inventory`

`ItemStack` represents a specific instance of an item in an inventory. It holds the reference to the `Item` config and dynamic data like amount and durability.

*   **Key Features**:
    *   Holds `Item` reference.
    *   Manages stack size/amount.
    *   Handles metadata/nbt.
*   **Reference**: [ItemStack Method Signatures](api-reference/method-signatures/server-items.md#itemstack)
