# Protocol - Entities

Entity-related classes from the Hytale protocol.

**Classes:** 4

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

