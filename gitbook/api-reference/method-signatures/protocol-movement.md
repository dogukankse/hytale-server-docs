# Protocol - Movement & Physics

Movement and physics classes from the Hytale protocol.

**Classes:** 4

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

