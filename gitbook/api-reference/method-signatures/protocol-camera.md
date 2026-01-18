# Protocol - Camera

Camera classes from the Hytale protocol.

**Classes:** 2

---

## BlockType

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.BlockType`  

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
public String item;
```

```java
public String name;
```

```java
public boolean unknown;
```

```java
public DrawType drawType;
```

```java
public BlockMaterial material;
```

```java
public Opacity opacity;
```

```java
public ShaderType[] shaderEffect;
```

```java
public int hitbox;
```

```java
public int interactionHitbox;
```

```java
public String model;
```

```java
public ModelTexture[] modelTexture;
```

```java
public float modelScale;
```

```java
public String modelAnimation;
```

```java
public boolean looping;
```

```java
public int maxSupportDistance;
```

```java
public BlockSupportsRequiredForType blockSupportsRequiredFor;
```

```java
public boolean requiresAlphaBlending;
```

```java
public BlockTextures[] cubeTextures;
```

```java
public String cubeSideMaskTexture;
```

```java
public ShadingMode cubeShadingMode;
```

```java
public RandomRotation randomRotation;
```

```java
public VariantRotation variantRotation;
```

```java
public Rotation rotationYawPlacementOffset;
```

```java
public int blockSoundSetIndex;
```

```java
public int ambientSoundEventIndex;
```

```java
public ModelParticle[] particles;
```

```java
public String blockParticleSetId;
```

```java
public String blockBreakingDecalId;
```

```java
public Color particleColor;
```

```java
public ColorLight light;
```

```java
public Tint tint;
```

```java
public Tint biomeTint;
```

```java
public int group;
```

```java
public String transitionTexture;
```

```java
public int[] transitionToGroups;
```

```java
public BlockMovementSettings movementSettings;
```

```java
public BlockFlags flags;
```

```java
public String interactionHint;
```

```java
public BlockGathering gathering;
```

```java
public BlockPlacementSettings placementSettings;
```

```java
public ModelDisplay display;
```

```java
public RailConfig rail;
```

```java
public boolean ignoreSupportWhenPlaced;
```

```java
public int transitionToTag;
```

```java
public int[] tagIndexes;
```

```java
public Bench bench;
```

```java
public ConnectedBlockRuleSet connectedBlockRuleSet;
```

### Public Constructors

```java
public BlockType();
```

```java
public BlockType(String, String, boolean, DrawType, BlockMaterial, Opacity, ShaderType[], int, int, String, ModelTexture[], float, String, boolean, int, BlockSupportsRequiredForType, Map<BlockNeighbor, RequiredBlockFaceSupport[]>, Map<BlockNeighbor, BlockFaceSupport[]>, boolean, BlockTextures[], String, ShadingMode, RandomRotation, VariantRotation, Rotation, int, int, ModelParticle[], String, String, Color, ColorLight, Tint, Tint, int, String, int[], BlockMovementSettings, BlockFlags, String, BlockGathering, BlockPlacementSettings, ModelDisplay, RailConfig, boolean, Map<InteractionType, Integer>, Map<String, Integer>, int, int[], Bench, ConnectedBlockRuleSet);
```

```java
public BlockType(BlockType);
```

### Public Methods

```java
public static BlockType deserialize(netty.ByteBuf, int);
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
public BlockType clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## BlockPosition

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.BlockPosition`  

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
public int x;
```

```java
public int y;
```

```java
public int z;
```

### Public Constructors

```java
public BlockPosition();
```

```java
public BlockPosition(int, int, int);
```

```java
public BlockPosition(BlockPosition);
```

### Public Methods

```java
public static BlockPosition deserialize(netty.ByteBuf, int);
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
public BlockPosition clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## BlockMaterial

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.BlockMaterial`  

**Type:** final Class

**Extends:** `java.lang.Enum<BlockMaterial>`  

### Public Fields

```java
public static final BlockMaterial Empty;
```

```java
public static final BlockMaterial Solid;
```

```java
public static final BlockMaterial[] VALUES;
```

### Public Methods

```java
public static BlockMaterial[] values();
```

```java
public static BlockMaterial valueOf(String);
```

```java
public int getValue();
```

```java
public static BlockMaterial fromValue(int);
```

---

## BlockTextures

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.BlockTextures`  

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
public String top;
```

```java
public String bottom;
```

```java
public String front;
```

```java
public String back;
```

```java
public String left;
```

```java
public String right;
```

```java
public float weight;
```

### Public Constructors

```java
public BlockTextures();
```

```java
public BlockTextures(String, String, String, String, String, String, float);
```

```java
public BlockTextures(BlockTextures);
```

### Public Methods

```java
public static BlockTextures deserialize(netty.ByteBuf, int);
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
public BlockTextures clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## BlockSoundSet

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.BlockSoundSet`  

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
public FloatRange moveInRepeatRange;
```

### Public Constructors

```java
public BlockSoundSet();
```

```java
public BlockSoundSet(String, Map<BlockSoundEvent, Integer>, FloatRange);
```

```java
public BlockSoundSet(BlockSoundSet);
```

### Public Methods

```java
public static BlockSoundSet deserialize(netty.ByteBuf, int);
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
public BlockSoundSet clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## BlockPlacementSettings

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.BlockPlacementSettings`  

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
public boolean allowRotationKey;
```

```java
public boolean placeInEmptyBlocks;
```

```java
public BlockPreviewVisibility previewVisibility;
```

```java
public BlockPlacementRotationMode rotationMode;
```

```java
public int wallPlacementOverrideBlockId;
```

```java
public int floorPlacementOverrideBlockId;
```

```java
public int ceilingPlacementOverrideBlockId;
```

### Public Constructors

```java
public BlockPlacementSettings();
```

```java
public BlockPlacementSettings(boolean, boolean, BlockPreviewVisibility, BlockPlacementRotationMode, int, int, int);
```

```java
public BlockPlacementSettings(BlockPlacementSettings);
```

### Public Methods

```java
public static BlockPlacementSettings deserialize(netty.ByteBuf, int);
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
public BlockPlacementSettings clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

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

## EntityUpdate

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.EntityUpdate`  

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
public int networkId;
```

```java
public ComponentUpdateType[] removed;
```

```java
public ComponentUpdate[] updates;
```

### Public Constructors

```java
public EntityUpdate();
```

```java
public EntityUpdate(int, ComponentUpdateType[], ComponentUpdate[]);
```

```java
public EntityUpdate(EntityUpdate);
```

### Public Methods

```java
public static EntityUpdate deserialize(netty.ByteBuf, int);
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
public EntityUpdate clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## EntityEffect

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.EntityEffect`  

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
public ApplicationEffects applicationEffects;
```

```java
public int worldRemovalSoundEventIndex;
```

```java
public int localRemovalSoundEventIndex;
```

```java
public ModelOverride modelOverride;
```

```java
public float duration;
```

```java
public boolean infinite;
```

```java
public boolean debuff;
```

```java
public String statusEffectIcon;
```

```java
public OverlapBehavior overlapBehavior;
```

```java
public double damageCalculatorCooldown;
```

```java
public ValueType valueType;
```

### Public Constructors

```java
public EntityEffect();
```

```java
public EntityEffect(String, String, ApplicationEffects, int, int, ModelOverride, float, boolean, boolean, String, OverlapBehavior, double, Map<Integer, Float>, ValueType);
```

```java
public EntityEffect(EntityEffect);
```

### Public Methods

```java
public static EntityEffect deserialize(netty.ByteBuf, int);
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
public EntityEffect clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## EntityStatType

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.EntityStatType`  

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
public float value;
```

```java
public float min;
```

```java
public float max;
```

```java
public EntityStatEffects minValueEffects;
```

```java
public EntityStatEffects maxValueEffects;
```

```java
public EntityStatResetBehavior resetBehavior;
```

### Public Constructors

```java
public EntityStatType();
```

```java
public EntityStatType(String, float, float, float, EntityStatEffects, EntityStatEffects, EntityStatResetBehavior);
```

```java
public EntityStatType(EntityStatType);
```

### Public Methods

```java
public static EntityStatType deserialize(netty.ByteBuf, int);
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
public EntityStatType clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## EntityStatUpdate

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.EntityStatUpdate`  

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
public EntityStatOp op;
```

```java
public boolean predictable;
```

```java
public float value;
```

```java
public String modifierKey;
```

```java
public Modifier modifier;
```

### Public Constructors

```java
public EntityStatUpdate();
```

```java
public EntityStatUpdate(EntityStatOp, boolean, float, Map<String, Modifier>, String, Modifier);
```

```java
public EntityStatUpdate(EntityStatUpdate);
```

### Public Methods

```java
public static EntityStatUpdate deserialize(netty.ByteBuf, int);
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
public EntityStatUpdate clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## Interaction

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.Interaction`  

**Type:** abstract Class


### Public Fields

```java
public static final int MAX_SIZE;
```

```java
public WaitForDataFrom waitForDataFrom;
```

```java
public InteractionEffects effects;
```

```java
public float horizontalSpeedMultiplier;
```

```java
public float runTime;
```

```java
public boolean cancelOnItemChange;
```

```java
public InteractionRules rules;
```

```java
public int[] tags;
```

```java
public InteractionCameraSettings camera;
```

### Public Constructors

```java
public Interaction();
```

### Public Methods

```java
public static Interaction deserialize(netty.ByteBuf, int);
```

```java
public static int computeBytesConsumed(netty.ByteBuf, int);
```

```java
public int getTypeId();
```

```java
public abstract int serialize(netty.ByteBuf);
```

```java
public abstract int computeSize();
```

```java
public int serializeWithTypeId(netty.ByteBuf);
```

```java
public int computeSizeWithTypeId();
```

```java
public static ValidationResult validateStructure(netty.ByteBuf, int);
```

---

## InteractionType

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.InteractionType`  

**Type:** final Class

**Extends:** `java.lang.Enum<InteractionType>`  

### Public Fields

```java
public static final InteractionType Primary;
```

```java
public static final InteractionType Secondary;
```

```java
public static final InteractionType Ability1;
```

```java
public static final InteractionType Ability2;
```

```java
public static final InteractionType Ability3;
```

```java
public static final InteractionType Use;
```

```java
public static final InteractionType Pick;
```

```java
public static final InteractionType Pickup;
```

```java
public static final InteractionType CollisionEnter;
```

```java
public static final InteractionType CollisionLeave;
```

```java
public static final InteractionType Collision;
```

```java
public static final InteractionType EntityStatEffect;
```

```java
public static final InteractionType SwapTo;
```

```java
public static final InteractionType SwapFrom;
```

```java
public static final InteractionType Death;
```

```java
public static final InteractionType Wielding;
```

```java
public static final InteractionType ProjectileSpawn;
```

```java
public static final InteractionType ProjectileHit;
```

```java
public static final InteractionType ProjectileMiss;
```

```java
public static final InteractionType ProjectileBounce;
```

```java
public static final InteractionType Held;
```

```java
public static final InteractionType HeldOffhand;
```

```java
public static final InteractionType Equipped;
```

```java
public static final InteractionType Dodge;
```

```java
public static final InteractionType GameModeSwap;
```

```java
public static final InteractionType[] VALUES;
```

### Public Methods

```java
public static InteractionType[] values();
```

```java
public static InteractionType valueOf(String);
```

```java
public int getValue();
```

```java
public static InteractionType fromValue(int);
```

---

## InteractionSettings

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.InteractionSettings`  

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
public boolean allowSkipOnClick;
```

### Public Constructors

```java
public InteractionSettings();
```

```java
public InteractionSettings(boolean);
```

```java
public InteractionSettings(InteractionSettings);
```

### Public Methods

```java
public static InteractionSettings deserialize(netty.ByteBuf, int);
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
public InteractionSettings clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## InteractionChainData

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.InteractionChainData`  

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
public int entityId;
```

```java
public UUID proxyId;
```

```java
public Vector3f hitLocation;
```

```java
public String hitDetail;
```

```java
public BlockPosition blockPosition;
```

```java
public int targetSlot;
```

```java
public Vector3f hitNormal;
```

### Public Constructors

```java
public InteractionChainData();
```

```java
public InteractionChainData(int, UUID, Vector3f, String, BlockPosition, int, Vector3f);
```

```java
public InteractionChainData(InteractionChainData);
```

### Public Methods

```java
public static InteractionChainData deserialize(netty.ByteBuf, int);
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
public InteractionChainData clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## MovementSettings

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.MovementSettings`  

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
public float mass;
```

```java
public float dragCoefficient;
```

```java
public boolean invertedGravity;
```

```java
public float velocityResistance;
```

```java
public float jumpForce;
```

```java
public float swimJumpForce;
```

```java
public float jumpBufferDuration;
```

```java
public float jumpBufferMaxYVelocity;
```

```java
public float acceleration;
```

```java
public float airDragMin;
```

```java
public float airDragMax;
```

```java
public float airDragMinSpeed;
```

```java
public float airDragMaxSpeed;
```

```java
public float airFrictionMin;
```

```java
public float airFrictionMax;
```

```java
public float airFrictionMinSpeed;
```

```java
public float airFrictionMaxSpeed;
```

```java
public float airSpeedMultiplier;
```

```java
public float airControlMinSpeed;
```

```java
public float airControlMaxSpeed;
```

```java
public float airControlMinMultiplier;
```

```java
public float airControlMaxMultiplier;
```

```java
public float comboAirSpeedMultiplier;
```

```java
public float baseSpeed;
```

```java
public float climbSpeed;
```

```java
public float climbSpeedLateral;
```

```java
public float climbUpSprintSpeed;
```

```java
public float climbDownSprintSpeed;
```

```java
public float horizontalFlySpeed;
```

```java
public float verticalFlySpeed;
```

```java
public float maxSpeedMultiplier;
```

```java
public float minSpeedMultiplier;
```

```java
public float wishDirectionGravityX;
```

```java
public float wishDirectionGravityY;
```

```java
public float wishDirectionWeightX;
```

```java
public float wishDirectionWeightY;
```

```java
public boolean canFly;
```

```java
public float collisionExpulsionForce;
```

```java
public float forwardWalkSpeedMultiplier;
```

```java
public float backwardWalkSpeedMultiplier;
```

```java
public float strafeWalkSpeedMultiplier;
```

```java
public float forwardRunSpeedMultiplier;
```

```java
public float backwardRunSpeedMultiplier;
```

```java
public float strafeRunSpeedMultiplier;
```

```java
public float forwardCrouchSpeedMultiplier;
```

```java
public float backwardCrouchSpeedMultiplier;
```

```java
public float strafeCrouchSpeedMultiplier;
```

```java
public float forwardSprintSpeedMultiplier;
```

```java
public float variableJumpFallForce;
```

```java
public float fallEffectDuration;
```

```java
public float fallJumpForce;
```

```java
public float fallMomentumLoss;
```

```java
public float autoJumpObstacleSpeedLoss;
```

```java
public float autoJumpObstacleSprintSpeedLoss;
```

```java
public float autoJumpObstacleEffectDuration;
```

```java
public float autoJumpObstacleSprintEffectDuration;
```

```java
public float autoJumpObstacleMaxAngle;
```

```java
public boolean autoJumpDisableJumping;
```

```java
public float minSlideEntrySpeed;
```

```java
public float slideExitSpeed;
```

```java
public float minFallSpeedToEngageRoll;
```

```java
public float maxFallSpeedToEngageRoll;
```

```java
public float rollStartSpeedModifier;
```

```java
public float rollExitSpeedModifier;
```

```java
public float rollTimeToComplete;
```

### Public Constructors

```java
public MovementSettings();
```

```java
public MovementSettings(float, float, boolean, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, boolean, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, boolean, float, float, float, float, float, float, float);
```

```java
public MovementSettings(MovementSettings);
```

### Public Methods

```java
public static MovementSettings deserialize(netty.ByteBuf, int);
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
public MovementSettings clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## MovementType

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.MovementType`  

**Type:** final Class

**Extends:** `java.lang.Enum<MovementType>`  

### Public Fields

```java
public static final MovementType None;
```

```java
public static final MovementType Idle;
```

```java
public static final MovementType Crouching;
```

```java
public static final MovementType Walking;
```

```java
public static final MovementType Running;
```

```java
public static final MovementType Sprinting;
```

```java
public static final MovementType Climbing;
```

```java
public static final MovementType Swimming;
```

```java
public static final MovementType Flying;
```

```java
public static final MovementType Sliding;
```

```java
public static final MovementType Rolling;
```

```java
public static final MovementType Mounting;
```

```java
public static final MovementType SprintMounting;
```

```java
public static final MovementType[] VALUES;
```

### Public Methods

```java
public static MovementType[] values();
```

```java
public static MovementType valueOf(String);
```

```java
public int getValue();
```

```java
public static MovementType fromValue(int);
```

---

## MovementStates

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.MovementStates`  

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
public boolean idle;
```

```java
public boolean horizontalIdle;
```

```java
public boolean jumping;
```

```java
public boolean flying;
```

```java
public boolean walking;
```

```java
public boolean running;
```

```java
public boolean sprinting;
```

```java
public boolean crouching;
```

```java
public boolean forcedCrouching;
```

```java
public boolean falling;
```

```java
public boolean climbing;
```

```java
public boolean inFluid;
```

```java
public boolean swimming;
```

```java
public boolean swimJumping;
```

```java
public boolean onGround;
```

```java
public boolean mantling;
```

```java
public boolean sliding;
```

```java
public boolean mounting;
```

```java
public boolean rolling;
```

```java
public boolean sitting;
```

```java
public boolean gliding;
```

```java
public boolean sleeping;
```

### Public Constructors

```java
public MovementStates();
```

```java
public MovementStates(boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean, boolean);
```

```java
public MovementStates(MovementStates);
```

### Public Methods

```java
public static MovementStates deserialize(netty.ByteBuf, int);
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
public MovementStates clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## PhysicsConfig

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.PhysicsConfig`  

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
public PhysicsType type;
```

```java
public double density;
```

```java
public double gravity;
```

```java
public double bounciness;
```

```java
public int bounceCount;
```

```java
public double bounceLimit;
```

```java
public boolean sticksVertically;
```

```java
public boolean computeYaw;
```

```java
public boolean computePitch;
```

```java
public RotationMode rotationMode;
```

```java
public double moveOutOfSolidSpeed;
```

```java
public double terminalVelocityAir;
```

```java
public double densityAir;
```

```java
public double terminalVelocityWater;
```

```java
public double densityWater;
```

```java
public double hitWaterImpulseLoss;
```

```java
public double rotationForce;
```

```java
public float speedRotationFactor;
```

```java
public double swimmingDampingFactor;
```

```java
public boolean allowRolling;
```

```java
public double rollingFrictionFactor;
```

```java
public float rollingSpeed;
```

### Public Constructors

```java
public PhysicsConfig();
```

```java
public PhysicsConfig(PhysicsType, double, double, double, int, double, boolean, boolean, boolean, RotationMode, double, double, double, double, double, double, double, float, double, boolean, double, float);
```

```java
public PhysicsConfig(PhysicsConfig);
```

### Public Methods

```java
public static PhysicsConfig deserialize(netty.ByteBuf, int);
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
public PhysicsConfig clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## Animation

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.Animation`  

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
public String name;
```

```java
public float speed;
```

```java
public float blendingDuration;
```

```java
public boolean looping;
```

```java
public float weight;
```

```java
public int[] footstepIntervals;
```

```java
public int soundEventIndex;
```

```java
public int passiveLoopCount;
```

### Public Constructors

```java
public Animation();
```

```java
public Animation(String, float, float, boolean, float, int[], int, int);
```

```java
public Animation(Animation);
```

### Public Methods

```java
public static Animation deserialize(netty.ByteBuf, int);
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
public Animation clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## AnimationSet

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.AnimationSet`  

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
public Animation[] animations;
```

```java
public Rangef nextAnimationDelay;
```

### Public Constructors

```java
public AnimationSet();
```

```java
public AnimationSet(String, Animation[], Rangef);
```

```java
public AnimationSet(AnimationSet);
```

### Public Methods

```java
public static AnimationSet deserialize(netty.ByteBuf, int);
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
public AnimationSet clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## AnimationSlot

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.AnimationSlot`  

**Type:** final Class

**Extends:** `java.lang.Enum<AnimationSlot>`  

### Public Fields

```java
public static final AnimationSlot Movement;
```

```java
public static final AnimationSlot Status;
```

```java
public static final AnimationSlot Action;
```

```java
public static final AnimationSlot Face;
```

```java
public static final AnimationSlot Emote;
```

```java
public static final AnimationSlot[] VALUES;
```

### Public Methods

```java
public static AnimationSlot[] values();
```

```java
public static AnimationSlot valueOf(String);
```

```java
public int getValue();
```

```java
public static AnimationSlot fromValue(int);
```

---

## Particle

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.Particle`  

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
public String texturePath;
```

```java
public Size frameSize;
```

```java
public ParticleUVOption uvOption;
```

```java
public ParticleScaleRatioConstraint scaleRatioConstraint;
```

```java
public SoftParticle softParticles;
```

```java
public float softParticlesFadeFactor;
```

```java
public boolean useSpriteBlending;
```

```java
public ParticleAnimationFrame initialAnimationFrame;
```

```java
public ParticleAnimationFrame collisionAnimationFrame;
```

### Public Constructors

```java
public Particle();
```

```java
public Particle(String, Size, ParticleUVOption, ParticleScaleRatioConstraint, SoftParticle, float, boolean, ParticleAnimationFrame, ParticleAnimationFrame, Map<Integer, ParticleAnimationFrame>);
```

```java
public Particle(Particle);
```

### Public Methods

```java
public static Particle deserialize(netty.ByteBuf, int);
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
public Particle clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## ParticleSystem

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.ParticleSystem`  

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
public ParticleSpawnerGroup[] spawners;
```

```java
public float lifeSpan;
```

```java
public float cullDistance;
```

```java
public float boundingRadius;
```

```java
public boolean isImportant;
```

### Public Constructors

```java
public ParticleSystem();
```

```java
public ParticleSystem(String, ParticleSpawnerGroup[], float, float, float, boolean);
```

```java
public ParticleSystem(ParticleSystem);
```

### Public Methods

```java
public static ParticleSystem deserialize(netty.ByteBuf, int);
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
public ParticleSystem clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## ParticleSpawner

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.ParticleSpawner`  

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
public Particle particle;
```

```java
public EmitShape shape;
```

```java
public RangeVector3f emitOffset;
```

```java
public float cameraOffset;
```

```java
public boolean useEmitDirection;
```

```java
public float lifeSpan;
```

```java
public Rangef spawnRate;
```

```java
public boolean spawnBurst;
```

```java
public Rangef waveDelay;
```

```java
public Range totalParticles;
```

```java
public int maxConcurrentParticles;
```

```java
public InitialVelocity initialVelocity;
```

```java
public float velocityStretchMultiplier;
```

```java
public ParticleRotationInfluence particleRotationInfluence;
```

```java
public boolean particleRotateWithSpawner;
```

```java
public boolean isLowRes;
```

```java
public float trailSpawnerPositionMultiplier;
```

```java
public float trailSpawnerRotationMultiplier;
```

```java
public ParticleCollision particleCollision;
```

```java
public FXRenderMode renderMode;
```

```java
public float lightInfluence;
```

```java
public boolean linearFiltering;
```

```java
public Rangef particleLifeSpan;
```

```java
public UVMotion uvMotion;
```

```java
public ParticleAttractor[] attractors;
```

```java
public IntersectionHighlight intersectionHighlight;
```

### Public Constructors

```java
public ParticleSpawner();
```

```java
public ParticleSpawner(String, Particle, EmitShape, RangeVector3f, float, boolean, float, Rangef, boolean, Rangef, Range, int, InitialVelocity, float, ParticleRotationInfluence, boolean, boolean, float, float, ParticleCollision, FXRenderMode, float, boolean, Rangef, UVMotion, ParticleAttractor[], IntersectionHighlight);
```

```java
public ParticleSpawner(ParticleSpawner);
```

### Public Methods

```java
public static ParticleSpawner deserialize(netty.ByteBuf, int);
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
public ParticleSpawner clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## SoundEvent

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.SoundEvent`  

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
public float volume;
```

```java
public float pitch;
```

```java
public float musicDuckingVolume;
```

```java
public float ambientDuckingVolume;
```

```java
public int maxInstance;
```

```java
public boolean preventSoundInterruption;
```

```java
public float startAttenuationDistance;
```

```java
public float maxDistance;
```

```java
public SoundEventLayer[] layers;
```

```java
public int audioCategory;
```

### Public Constructors

```java
public SoundEvent();
```

```java
public SoundEvent(String, float, float, float, float, int, boolean, float, float, SoundEventLayer[], int);
```

```java
public SoundEvent(SoundEvent);
```

### Public Methods

```java
public static SoundEvent deserialize(netty.ByteBuf, int);
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
public SoundEvent clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## SoundCategory

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.SoundCategory`  

**Type:** final Class

**Extends:** `java.lang.Enum<SoundCategory>`  

### Public Fields

```java
public static final SoundCategory Music;
```

```java
public static final SoundCategory Ambient;
```

```java
public static final SoundCategory SFX;
```

```java
public static final SoundCategory UI;
```

```java
public static final SoundCategory[] VALUES;
```

### Public Methods

```java
public static SoundCategory[] values();
```

```java
public static SoundCategory valueOf(String);
```

```java
public int getValue();
```

```java
public static SoundCategory fromValue(int);
```

---

## AudioCategory

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.AudioCategory`  

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
public float volume;
```

### Public Constructors

```java
public AudioCategory();
```

```java
public AudioCategory(String, float);
```

```java
public AudioCategory(AudioCategory);
```

### Public Methods

```java
public static AudioCategory deserialize(netty.ByteBuf, int);
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
public AudioCategory clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

