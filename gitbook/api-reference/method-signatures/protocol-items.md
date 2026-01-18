# Protocol - Items

Item-related classes from the Hytale protocol.

**Classes:** 8

---

## ItemBase

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.ItemBase`  

**Type:** Class


### Public Fields

```java
public static final int NULLABLE_BIT_FIELD_SIZE;
```

```java
public static final int FIXED_BLOCK_SIZE;
```

```java
public static final int VARIABLE_FIELD_COUNT;
```

```java
public static final int VARIABLE_BLOCK_START;
```

```java
public static final int MAX_SIZE;
```

```java
public String id;
```

```java
public String model;
```

```java
public float scale;
```

```java
public String texture;
```

```java
public String animation;
```

```java
public String playerAnimationsId;
```

```java
public boolean usePlayerAnimations;
```

```java
public int maxStack;
```

```java
public int reticleIndex;
```

```java
public String icon;
```

```java
public AssetIconProperties iconProperties;
```

```java
public ItemTranslationProperties translationProperties;
```

```java
public int itemLevel;
```

```java
public int qualityIndex;
```

```java
public ItemResourceType[] resourceTypes;
```

```java
public boolean consumable;
```

```java
public boolean variant;
```

```java
public int blockId;
```

```java
public ItemTool tool;
```

```java
public ItemWeapon weapon;
```

```java
public ItemArmor armor;
```

```java
public ItemGlider gliderConfig;
```

```java
public ItemUtility utility;
```

```java
public BlockSelectorToolData blockSelectorTool;
```

```java
public ItemBuilderToolData builderToolData;
```

```java
public ItemEntityConfig itemEntity;
```

```java
public String set;
```

```java
public String[] categories;
```

```java
public ModelParticle[] particles;
```

```java
public ModelParticle[] firstPersonParticles;
```

```java
public ModelTrail[] trails;
```

```java
public ColorLight light;
```

```java
public double durability;
```

```java
public int soundEventIndex;
```

```java
public int itemSoundSetIndex;
```

```java
public InteractionConfiguration interactionConfig;
```

```java
public String droppedItemAnimation;
```

```java
public int[] tagIndexes;
```

```java
public int[] displayEntityStatsHUD;
```

```java
public ItemPullbackConfiguration pullbackConfig;
```

```java
public boolean clipsGeometry;
```

```java
public boolean renderDeployablePreview;
```

### Public Constructors

```java
public ItemBase();
```

```java
public ItemBase(String, String, float, String, String, String, boolean, int, int, String, AssetIconProperties, ItemTranslationProperties, int, int, ItemResourceType[], boolean, boolean, int, ItemTool, ItemWeapon, ItemArmor, ItemGlider, ItemUtility, BlockSelectorToolData, ItemBuilderToolData, ItemEntityConfig, String, String[], ModelParticle[], ModelParticle[], ModelTrail[], ColorLight, double, int, int, Map<InteractionType, Integer>, Map<String, Integer>, InteractionConfiguration, String, int[], Map<Integer, ItemAppearanceCondition[]>, int[], ItemPullbackConfiguration, boolean, boolean);
```

```java
public ItemBase(ItemBase);
```

### Public Methods

```java
public static ItemBase deserialize(netty.ByteBuf, int);
```

```java
public static int computeBytesConsumed(netty.ByteBuf, int);
```

```java
public void serialize(netty.ByteBuf);
```

```java
public int computeSize();
```

```java
public static ValidationResult validateStructure(netty.ByteBuf, int);
```

```java
public ItemBase clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## ItemLibrary

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.ItemLibrary`  

**Type:** Class


### Public Fields

```java
public static final int NULLABLE_BIT_FIELD_SIZE;
```

```java
public static final int FIXED_BLOCK_SIZE;
```

```java
public static final int VARIABLE_FIELD_COUNT;
```

```java
public static final int VARIABLE_BLOCK_START;
```

```java
public static final int MAX_SIZE;
```

```java
public ItemBase[] items;
```

### Public Constructors

```java
public ItemLibrary();
```

```java
public ItemLibrary(ItemBase[], Map<Integer, String>[]);
```

```java
public ItemLibrary(ItemLibrary);
```

### Public Methods

```java
public static ItemLibrary deserialize(netty.ByteBuf, int);
```

```java
public static int computeBytesConsumed(netty.ByteBuf, int);
```

```java
public void serialize(netty.ByteBuf);
```

```java
public int computeSize();
```

```java
public static ValidationResult validateStructure(netty.ByteBuf, int);
```

```java
public ItemLibrary clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## ItemCategory

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.ItemCategory`  

**Type:** Class


### Public Fields

```java
public static final int NULLABLE_BIT_FIELD_SIZE;
```

```java
public static final int FIXED_BLOCK_SIZE;
```

```java
public static final int VARIABLE_FIELD_COUNT;
```

```java
public static final int VARIABLE_BLOCK_START;
```

```java
public static final int MAX_SIZE;
```

```java
public String id;
```

```java
public String name;
```

```java
public String icon;
```

```java
public int order;
```

```java
public ItemGridInfoDisplayMode infoDisplayMode;
```

```java
public ItemCategory[] children;
```

### Public Constructors

```java
public ItemCategory();
```

```java
public ItemCategory(String, String, String, int, ItemGridInfoDisplayMode, ItemCategory[]);
```

```java
public ItemCategory(ItemCategory);
```

### Public Methods

```java
public static ItemCategory deserialize(netty.ByteBuf, int);
```

```java
public static int computeBytesConsumed(netty.ByteBuf, int);
```

```java
public void serialize(netty.ByteBuf);
```

```java
public int computeSize();
```

```java
public static ValidationResult validateStructure(netty.ByteBuf, int);
```

```java
public ItemCategory clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## ItemQuality

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.ItemQuality`  

**Type:** Class


### Public Fields

```java
public static final int NULLABLE_BIT_FIELD_SIZE;
```

```java
public static final int FIXED_BLOCK_SIZE;
```

```java
public static final int VARIABLE_FIELD_COUNT;
```

```java
public static final int VARIABLE_BLOCK_START;
```

```java
public static final int MAX_SIZE;
```

```java
public String id;
```

```java
public String itemTooltipTexture;
```

```java
public String itemTooltipArrowTexture;
```

```java
public String slotTexture;
```

```java
public String blockSlotTexture;
```

```java
public String specialSlotTexture;
```

```java
public Color textColor;
```

```java
public String localizationKey;
```

```java
public boolean visibleQualityLabel;
```

```java
public boolean renderSpecialSlot;
```

```java
public boolean hideFromSearch;
```

### Public Constructors

```java
public ItemQuality();
```

```java
public ItemQuality(String, String, String, String, String, String, Color, String, boolean, boolean, boolean);
```

```java
public ItemQuality(ItemQuality);
```

### Public Methods

```java
public static ItemQuality deserialize(netty.ByteBuf, int);
```

```java
public static int computeBytesConsumed(netty.ByteBuf, int);
```

```java
public void serialize(netty.ByteBuf);
```

```java
public int computeSize();
```

```java
public static ValidationResult validateStructure(netty.ByteBuf, int);
```

```java
public ItemQuality clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## ItemQuantity

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.ItemQuantity`  

**Type:** Class


### Public Fields

```java
public static final int NULLABLE_BIT_FIELD_SIZE;
```

```java
public static final int FIXED_BLOCK_SIZE;
```

```java
public static final int VARIABLE_FIELD_COUNT;
```

```java
public static final int VARIABLE_BLOCK_START;
```

```java
public static final int MAX_SIZE;
```

```java
public String itemId;
```

```java
public int quantity;
```

### Public Constructors

```java
public ItemQuantity();
```

```java
public ItemQuantity(String, int);
```

```java
public ItemQuantity(ItemQuantity);
```

### Public Methods

```java
public static ItemQuantity deserialize(netty.ByteBuf, int);
```

```java
public static int computeBytesConsumed(netty.ByteBuf, int);
```

```java
public void serialize(netty.ByteBuf);
```

```java
public int computeSize();
```

```java
public static ValidationResult validateStructure(netty.ByteBuf, int);
```

```java
public ItemQuantity clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## ItemWeapon

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.ItemWeapon`  

**Type:** Class


### Public Fields

```java
public static final int NULLABLE_BIT_FIELD_SIZE;
```

```java
public static final int FIXED_BLOCK_SIZE;
```

```java
public static final int VARIABLE_FIELD_COUNT;
```

```java
public static final int VARIABLE_BLOCK_START;
```

```java
public static final int MAX_SIZE;
```

```java
public int[] entityStatsToClear;
```

```java
public boolean renderDualWielded;
```

### Public Constructors

```java
public ItemWeapon();
```

```java
public ItemWeapon(int[], Map<Integer, Modifier[]>, boolean);
```

```java
public ItemWeapon(ItemWeapon);
```

### Public Methods

```java
public static ItemWeapon deserialize(netty.ByteBuf, int);
```

```java
public static int computeBytesConsumed(netty.ByteBuf, int);
```

```java
public void serialize(netty.ByteBuf);
```

```java
public int computeSize();
```

```java
public static ValidationResult validateStructure(netty.ByteBuf, int);
```

```java
public ItemWeapon clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## ItemArmor

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.ItemArmor`  

**Type:** Class


### Public Fields

```java
public static final int NULLABLE_BIT_FIELD_SIZE;
```

```java
public static final int FIXED_BLOCK_SIZE;
```

```java
public static final int VARIABLE_FIELD_COUNT;
```

```java
public static final int VARIABLE_BLOCK_START;
```

```java
public static final int MAX_SIZE;
```

```java
public ItemArmorSlot armorSlot;
```

```java
public Cosmetic[] cosmeticsToHide;
```

```java
public double baseDamageResistance;
```

### Public Constructors

```java
public ItemArmor();
```

```java
public ItemArmor(ItemArmorSlot, Cosmetic[], Map<Integer, Modifier[]>, double, Map<String, Modifier[]>, Map<String, Modifier[]>, Map<String, Modifier[]>);
```

```java
public ItemArmor(ItemArmor);
```

### Public Methods

```java
public static ItemArmor deserialize(netty.ByteBuf, int);
```

```java
public static int computeBytesConsumed(netty.ByteBuf, int);
```

```java
public void serialize(netty.ByteBuf);
```

```java
public int computeSize();
```

```java
public static ValidationResult validateStructure(netty.ByteBuf, int);
```

```java
public ItemArmor clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## ItemTool

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.ItemTool`  

**Type:** Class


### Public Fields

```java
public static final int NULLABLE_BIT_FIELD_SIZE;
```

```java
public static final int FIXED_BLOCK_SIZE;
```

```java
public static final int VARIABLE_FIELD_COUNT;
```

```java
public static final int VARIABLE_BLOCK_START;
```

```java
public static final int MAX_SIZE;
```

```java
public ItemToolSpec[] specs;
```

```java
public float speed;
```

### Public Constructors

```java
public ItemTool();
```

```java
public ItemTool(ItemToolSpec[], float);
```

```java
public ItemTool(ItemTool);
```

### Public Methods

```java
public static ItemTool deserialize(netty.ByteBuf, int);
```

```java
public static int computeBytesConsumed(netty.ByteBuf, int);
```

```java
public void serialize(netty.ByteBuf);
```

```java
public int computeSize();
```

```java
public static ValidationResult validateStructure(netty.ByteBuf, int);
```

```java
public ItemTool clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

