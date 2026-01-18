# Protocol - Interactions

Interaction system classes from the Hytale protocol.

**Classes:** 4

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

