# Player System

The Player System handles player management, sessions, skins, and player-specific functionality.

---

## Overview

**Key Packages:**
- `com.hypixel.hytale.server.core.player.*` - Player system

---

## Protocol Classes

### PlayerSkin
Player appearance customization.

Properties:
- Skin data
- Model type
- Accessories

---

## Player Management

### Player Sessions

Track connected players:
- Join/leave events
- Session data
- Connection state

### Player Data

Persistent player information:
- Position
- Inventory
- Stats
- Progress

---

## Player Events

### Connection Events

```java
// Player join
eventRegistry.register(PlayerJoinEvent.class, event -> {
    Player player = event.getPlayer();
    // Welcome message, initialization, etc.
});

// Player leave
eventRegistry.register(PlayerLeaveEvent.class, event -> {
    Player player = event.getPlayer();
    // Cleanup, save data, etc.
});
```

### Interaction Events

```java
// Player interacts with block
eventRegistry.register(PlayerBlockInteractEvent.class, event -> {
    Player player = event.getPlayer();
    BlockPosition position = event.getBlockPosition();
});

// Player interacts with entity
eventRegistry.register(PlayerEntityInteractEvent.class, event -> {
    Player player = event.getPlayer();
    Entity entity = event.getEntity();
});
```

---

## Player Movement

### Movement Events

```java
eventRegistry.register(PlayerMoveEvent.class, event -> {
    Player player = event.getPlayer();
    Position from = event.getFrom();
    Position to = event.getTo();
});
```

### Teleportation

```java
// Using builtin.teleport
player.teleport(x, y, z);
player.teleportToSpawn();
```

---

## Player Inventory

### Accessing Inventory

```java
Inventory inventory = player.getInventory();
ItemBase itemInHand = inventory.getItemInHand();
```

### Modifying Inventory

```java
inventory.addItem(item);
inventory.removeItem(item);
inventory.setSlot(slot, item);
```

---

## Player Stats

### Health

```java
float health = player.getHealth();
float maxHealth = player.getMaxHealth();

player.setHealth(50f);
player.heal(10f);
player.damage(5f);
```

### Other Stats

```java
// Stamina, hunger, etc.
float stamina = player.getStat(EntityStatType.STAMINA);
```

---

## Player Commands

### Sending Messages

```java
player.sendMessage("Hello, world!");
player.sendMessage(Component.text("Colored text").color(NamedTextColor.RED));
```

### Action Bar

```java
player.sendActionBar("Action bar message");
```

### Titles

```java
player.sendTitle("Title", "Subtitle");
```

---

## Player Permissions

### Checking Permissions

```java
if (player.hasPermission("my.permission")) {
    // Player has permission
}
```

### Admin Status

```java
if (player.isAdmin()) {
    // Player is admin
}
```

---

## Player Cosmetics

### Skins

```java
PlayerSkin skin = player.getSkin();
```

### Nameplates

```java
protocol.Nameplate nameplate = player.getNameplate();
```

---

## Beds System

Located in `com.hypixel.hytale.builtin.beds` (19 classes)

Player sleeping and spawn point management.

---

## Best Practices

1. **Handle join/leave** - Initialize and cleanup properly
2. **Validate inputs** - Check player actions
3. **Use events** - React to player actions via events
4. **Cache player data** - Don't query repeatedly
5. **Respect permissions** - Check before actions

---

## See Also

- [Entity System](entity-system.md) - Player as entity
- [Item System](item-system.md) - Player inventory
- [Event System](event-system.md) - Player events
- [API Reference](../api-reference/packages.md) - Package details
