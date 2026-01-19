# Server - Items

Item configuration and inventory classes from the Server Core.

**Classes:** 3

---

## Item

**Package:** `com.hypixel.hytale.server.core.asset.type.item.config`  
**Full Name:** `com.hypixel.hytale.server.core.asset.type.item.config.Item`  

**Type:** Class  
**Implements:** `NetworkSerializable`, `JsonAssetWithMap`

### Public Fields

```java
public static final String UNKNOWN_TEXTURE;
```

```java
public static final Item UNKNOWN;
```

### Public Methods

```java
public String getId();
```

```java
public String getBlockId();
```

```java
public String getTranslationKey();
```

```java
public String getModel();
```

```java
public String getTexture();
```

```java
public boolean isConsumable();
```

```java
public String getIcon();
```

```java
public AssetIconProperties getIconProperties();
```

```java
public int getMaxStack();
```

```java
public ItemTool getTool();
```

```java
public ItemWeapon getWeapon();
```

```java
public ItemArmor getArmor();
```

```java
public ItemUtility getUtility();
```

```java
public String[] getCategories();
```

```java
public InteractionConfiguration getInteractionConfig();
```

```java
public ItemPullbackConfig getPullbackConfig();
```

---

## ItemStack

**Package:** `com.hypixel.hytale.server.core.inventory`  
**Full Name:** `com.hypixel.hytale.server.core.inventory.ItemStack`  

**Type:** Class  
**Implements:** `NetworkSerializable`

### Public Fields

```java
public static final ItemStack EMPTY;
```

### Public Constructors

```java
public ItemStack(String itemId, int quantity);
```

```java
public ItemStack(String itemId);
```

### Public Methods

```java
public String getItemId();
```

```java
public int getQuantity();
```

```java
public boolean isEmpty();
```

```java
public Item getItem();
```

```java
public double getDurability();
```

```java
public ItemStack withQuantity(int quantity);
```

```java
public ItemStack withDurability(double durability);
```

```java
public ItemStack withMetadata(String key, Object value);
```

---

## ItemPullbackConfig

**Package:** `com.hypixel.hytale.server.core.asset.type.item.config`  
**Full Name:** `com.hypixel.hytale.server.core.asset.type.item.config.ItemPullbackConfig`  

**Type:** Class  
**Implements:** `NetworkSerializable`

### Public Fields

```java
protected Vector3f leftOffsetOverride;
protected Vector3f leftRotationOverride;
protected Vector3f rightOffsetOverride;
protected Vector3f rightRotationOverride;
```

### Public Methods

```java
public Object toPacket();
```
