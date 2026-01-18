# Protocol - Animation

Animation classes from the Hytale protocol.

**Classes:** 3

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

