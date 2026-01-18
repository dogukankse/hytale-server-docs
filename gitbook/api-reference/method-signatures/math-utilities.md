# Math Utilities

Math classes from `com.hypixel.hytale.math` package.

**Classes:** 6

---

## Vec2f

**Package:** `com.hypixel.hytale.math`  
**Full Name:** `com.hypixel.hytale.math.Vec2f`  

**Type:** final Class


### Public Fields

```java
public static final int SIZE;
```

```java
public float x;
```

```java
public float y;
```

### Public Constructors

```java
public Vec2f(float, float);
```

```java
public Vec2f();
```

### Public Methods

```java
public static Vec2f deserialize(netty.ByteBuf, int);
```

```java
public void serialize(netty.ByteBuf);
```

```java
public String toString();
```

---

## Vec3f

**Package:** `com.hypixel.hytale.math`  
**Full Name:** `com.hypixel.hytale.math.Vec3f`  

**Type:** final Class


### Public Fields

```java
public static final int SIZE;
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
public Vec3f(float, float, float);
```

```java
public Vec3f();
```

### Public Methods

```java
public static Vec3f deserialize(netty.ByteBuf, int);
```

```java
public void serialize(netty.ByteBuf);
```

```java
public String toString();
```

---

## Vec4f

**Package:** `com.hypixel.hytale.math`  
**Full Name:** `com.hypixel.hytale.math.Vec4f`  

**Type:** Class


### Public Fields

```java
public static final int SIZE;
```

```java
public final float x;
```

```java
public final float y;
```

```java
public final float z;
```

```java
public final float w;
```

### Public Constructors

```java
public Vec4f(float, float, float, float);
```

### Public Methods

```java
public static Vec4f deserialize(netty.ByteBuf, int);
```

```java
public void serialize(netty.ByteBuf);
```

---

## Mat4f

**Package:** `com.hypixel.hytale.math`  
**Full Name:** `com.hypixel.hytale.math.Mat4f`  

**Type:** Class


### Public Fields

```java
public static final int SIZE;
```

```java
public final float m11;
```

```java
public final float m12;
```

```java
public final float m13;
```

```java
public final float m14;
```

```java
public final float m21;
```

```java
public final float m22;
```

```java
public final float m23;
```

```java
public final float m24;
```

```java
public final float m31;
```

```java
public final float m32;
```

```java
public final float m33;
```

```java
public final float m34;
```

```java
public final float m41;
```

```java
public final float m42;
```

```java
public final float m43;
```

```java
public final float m44;
```

### Public Constructors

```java
public Mat4f(float, float, float, float, float, float, float, float, float, float, float, float, float, float, float, float);
```

### Public Methods

```java
public static Mat4f identity();
```

```java
public static Mat4f deserialize(netty.ByteBuf, int);
```

```java
public void serialize(netty.ByteBuf);
```

---

## Quatf

**Package:** `com.hypixel.hytale.math`  
**Full Name:** `com.hypixel.hytale.math.Quatf`  

**Type:** Class


### Public Fields

```java
public static final int SIZE;
```

```java
public final float x;
```

```java
public final float y;
```

```java
public final float z;
```

```java
public final float w;
```

### Public Constructors

```java
public Quatf(float, float, float, float);
```

### Public Methods

```java
public static Quatf deserialize(netty.ByteBuf, int);
```

```java
public void serialize(netty.ByteBuf);
```

---

## Axis

**Package:** `com.hypixel.hytale.math`  
**Full Name:** `com.hypixel.hytale.math.Axis`  

**Type:** final Class

**Extends:** `java.lang.Enum<Axis>`  

### Public Fields

```java
public static final Axis X;
```

```java
public static final Axis Y;
```

```java
public static final Axis Z;
```

### Public Methods

```java
public static Axis[] values();
```

```java
public static Axis valueOf(String);
```

```java
public Vector3i getDirection();
```

```java
public void rotate(Vector3i, int);
```

```java
public void rotate(Vector3d, int);
```

```java
public void rotate(Vector3i);
```

```java
public void rotate(Vector3d);
```

```java
public void flip(Vector3i);
```

```java
public void flip(Vector3d);
```

```java
public void flipRotation(Vector3f);
```

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

