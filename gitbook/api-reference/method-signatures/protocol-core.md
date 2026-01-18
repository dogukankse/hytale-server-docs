# Protocol - Core Types

Basic data types from the Hytale protocol.

**Classes:** 9

---

## Vector2f

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.Vector2f`  

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
public float x;
```

```java
public float y;
```

### Public Constructors

```java
public Vector2f();
```

```java
public Vector2f(float, float);
```

```java
public Vector2f(Vector2f);
```

### Public Methods

```java
public static Vector2f deserialize(netty.ByteBuf, int);
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
public Vector2f clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## Vector2i

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.Vector2i`  

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

### Public Constructors

```java
public Vector2i();
```

```java
public Vector2i(int, int);
```

```java
public Vector2i(Vector2i);
```

### Public Methods

```java
public static Vector2i deserialize(netty.ByteBuf, int);
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
public Vector2i clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## Vector3f

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.Vector3f`  

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
public float x;
```

```java
public float y;
```

```java
public float z;
```

### Public Constructors

```java
public Vector3f();
```

```java
public Vector3f(float, float, float);
```

```java
public Vector3f(Vector3f);
```

### Public Methods

```java
public static Vector3f deserialize(netty.ByteBuf, int);
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
public Vector3f clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## Vector3i

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.Vector3i`  

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
public Vector3i();
```

```java
public Vector3i(int, int, int);
```

```java
public Vector3i(Vector3i);
```

### Public Methods

```java
public static Vector3i deserialize(netty.ByteBuf, int);
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
public Vector3i clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## Vector3d

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.Vector3d`  

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
public double x;
```

```java
public double y;
```

```java
public double z;
```

### Public Constructors

```java
public Vector3d();
```

```java
public Vector3d(double, double, double);
```

```java
public Vector3d(Vector3d);
```

### Public Methods

```java
public static Vector3d deserialize(netty.ByteBuf, int);
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
public Vector3d clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## Position

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.Position`  

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
public double x;
```

```java
public double y;
```

```java
public double z;
```

### Public Constructors

```java
public Position();
```

```java
public Position(double, double, double);
```

```java
public Position(Position);
```

### Public Methods

```java
public static Position deserialize(netty.ByteBuf, int);
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
public Position clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## Rotation

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.Rotation`  

**Type:** final Class

**Extends:** `java.lang.Enum<Rotation>`  

### Public Fields

```java
public static final Rotation None;
```

```java
public static final Rotation Ninety;
```

```java
public static final Rotation OneEighty;
```

```java
public static final Rotation TwoSeventy;
```

```java
public static final Rotation[] VALUES;
```

### Public Methods

```java
public static Rotation[] values();
```

```java
public static Rotation valueOf(String);
```

```java
public int getValue();
```

```java
public static Rotation fromValue(int);
```

---

## Color

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.Color`  

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
public byte red;
```

```java
public byte green;
```

```java
public byte blue;
```

### Public Constructors

```java
public Color();
```

```java
public Color(byte, byte, byte);
```

```java
public Color(Color);
```

### Public Methods

```java
public static Color deserialize(netty.ByteBuf, int);
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
public Color clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

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

