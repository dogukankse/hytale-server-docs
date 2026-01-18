# Protocol - Particles

Particle system classes from the Hytale protocol.

**Classes:** 3

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

## CameraSettings

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.CameraSettings`  

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
public Vector3f positionOffset;
```

```java
public CameraAxis yaw;
```

```java
public CameraAxis pitch;
```

### Public Constructors

```java
public CameraSettings();
```

```java
public CameraSettings(Vector3f, CameraAxis, CameraAxis);
```

```java
public CameraSettings(CameraSettings);
```

### Public Methods

```java
public static CameraSettings deserialize(netty.ByteBuf, int);
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
public CameraSettings clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## CameraInteraction

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.CameraInteraction`  

**Type:** Class

**Extends:** `SimpleInteraction`  

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
public CameraActionType cameraAction;
```

```java
public CameraPerspectiveType cameraPerspective;
```

```java
public boolean cameraPersist;
```

```java
public float cameraInteractionTime;
```

### Public Constructors

```java
public CameraInteraction();
```

```java
public CameraInteraction(WaitForDataFrom, InteractionEffects, float, float, boolean, Map<GameMode, InteractionSettings>, InteractionRules, int[], InteractionCameraSettings, int, int, CameraActionType, CameraPerspectiveType, boolean, float);
```

```java
public CameraInteraction(CameraInteraction);
```

### Public Methods

```java
public static CameraInteraction deserialize(netty.ByteBuf, int);
```

```java
public static int computeBytesConsumed(netty.ByteBuf, int);
```

```java
public int serialize(netty.ByteBuf);
```

```java
public int computeSize();
```

```java
public static ValidationResult validateStructure(netty.ByteBuf, int);
```

```java
public CameraInteraction clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

```java
public SimpleInteraction clone();
```

---

