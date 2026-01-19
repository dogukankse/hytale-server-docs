# Combat System

This section details the API classes related to weapons, equipment, and combat mechanics.

## Equipment

### `Equipment`
**Package**: `com.hypixel.hytale.protocol`

Manages the items equipped by an entity (armor, held items).

*   **Fields**:
    *   `armorIds`: Array of String IDs for equipped armor.
    *   `rightHandItemId`: String ID of item in main hand.
    *   `leftHandItemId`: String ID of item in off hand.

## Weapons & Projectiles

### `ItemWeapon`
**Package**: `com.hypixel.hytale.server.core.asset.type.item.config`
*(Extends `Item`)*

Configuration for melee and ranged weapons.

*   **Key Methods**:
    *   `getStatModifiers()`: Returns `Modifier[]` array defining damage, attack speed, etc.
    *   `toPacket()`: Converts config to protocol packet.

### `ItemPullbackConfig`
**Package**: `com.hypixel.hytale.server.core.asset.type.item.config`

Handles mechanics for "charge-up" or "draw" weapons like **Bows** and **Crossbows**.

*   **Functionality**:
    *   Manages the pullback state and duration.
    *   Likely handles the "Reload" state logic for crossbows.
*   **Reference**: [ItemPullbackConfig Method Signatures](../api-reference/method-signatures/server-items.md#itempullbackconfig)

### `LaunchProjectileInteraction`
**Package**: `com.hypixel.hytale.server.core.modules.interaction.interaction.config.server`

Interaction config used to fire projectiles. This is the core mechanic for **Ranged Weapons** and **Ammo**.

*   **Key Methods**:
    *   `getBallisticData()`: Returns `BallisticData` for physics.
*   **Reference**: [LaunchProjectileInteraction Signatures](../api-reference/method-signatures/server-interactions.md#launchprojectileinteraction)
