# Utilities

Utility classes for logging, codecs, and registry.

**Classes:** 9

---

## HytaleLogger

**Package:** `com.hypixel.hytale.logger`  
**Full Name:** `com.hypixel.hytale.logger.HytaleLogger`  

**Type:** Class

**Extends:** `com.google.common.flogger.AbstractLogger<HytaleLogger$Api>`  

### Public Methods

```java
public static void init();
```

```java
public static void replaceStd();
```

```java
public static HytaleLogger getLogger();
```

```java
public static HytaleLogger forEnclosingClass();
```

```java
public static HytaleLogger forEnclosingClassFull();
```

```java
public static HytaleLogger get(String);
```

```java
public HytaleLogger$Api at(logging.Level);
```

```java
public String getName();
```

```java
public logging.Level getLevel();
```

```java
public void setLevel(logging.Level);
```

```java
public HytaleLogger getSubLogger(String);
```

```java
public void setSentryClient(io.sentry.IScopes);
```

```java
public void setPropagatesSentryToParent(boolean);
```

```java
public com.google.common.flogger.LoggingApi at(logging.Level);
```

---

## Codec

**Package:** `com.hypixel.hytale.codec`  
**Full Name:** `com.hypixel.hytale.codec.Codec`  

**Type:** interface

**Extends:** `RawJsonCodec<T>,`  

### Public Fields

```java
public static final BsonDocumentCodec BSON_DOCUMENT;
```

```java
public static final StringCodec STRING;
```

```java
public static final BooleanCodec BOOLEAN;
```

```java
public static final DoubleCodec DOUBLE;
```

```java
public static final FloatCodec FLOAT;
```

```java
public static final ByteCodec BYTE;
```

```java
public static final ShortCodec SHORT;
```

```java
public static final IntegerCodec INTEGER;
```

```java
public static final LongCodec LONG;
```

```java
public static final regex.Pattern BASE64_PATTERN;
```

```java
public static final DoubleArrayCodec DOUBLE_ARRAY;
```

```java
public static final FloatArrayCodec FLOAT_ARRAY;
```

```java
public static final IntArrayCodec INT_ARRAY;
```

```java
public static final LongArrayCodec LONG_ARRAY;
```

```java
public static final ArrayCodec<String> STRING_ARRAY;
```

```java
public static final UUIDBinaryCodec UUID_BINARY;
```

### Public Methods

```java
public default T decode(org.bson.BsonValue);
```

```java
public abstract T decode(org.bson.BsonValue, ExtraInfo);
```

```java
public default org.bson.BsonValue encode(T);
```

```java
public abstract org.bson.BsonValue encode(T, ExtraInfo);
```

```java
public static boolean isNullBsonValue(org.bson.BsonValue);
```

---

## KeyedCodec

**Package:** `com.hypixel.hytale.codec`  
**Full Name:** `com.hypixel.hytale.codec.KeyedCodec`  

**Type:** Class


### Public Constructors

```java
public KeyedCodec(String, Codec<T>);
```

```java
public KeyedCodec(String, Codec<T>, boolean);
```

```java
public KeyedCodec(String, Codec<T>, boolean, boolean);
```

### Public Methods

```java
public String getKey();
```

```java
public T getNow(org.bson.BsonDocument);
```

```java
public T getNow(org.bson.BsonDocument, ExtraInfo);
```

```java
public T getOrNull(org.bson.BsonDocument);
```

```java
public T getOrNull(org.bson.BsonDocument, ExtraInfo);
```

```java
public Optional<T> get(org.bson.BsonDocument);
```

```java
public Optional<T> get(org.bson.BsonDocument, ExtraInfo);
```

```java
public T getOrDefault(org.bson.BsonDocument, ExtraInfo, T);
```

```java
public Optional<T> getAndInherit(org.bson.BsonDocument, T, ExtraInfo);
```

```java
public void put(org.bson.BsonDocument, T);
```

```java
public void put(org.bson.BsonDocument, T, ExtraInfo);
```

```java
public Codec<T> getChildCodec();
```

```java
public boolean isRequired();
```

```java
public String toString();
```

---

## WrappedCodec

**Package:** `com.hypixel.hytale.codec`  
**Full Name:** `com.hypixel.hytale.codec.WrappedCodec`  

**Type:** interface


### Public Methods

```java
public abstract Codec<T> getChildCodec();
```

---

## Registry

**Package:** `com.hypixel.hytale.registry`  
**Full Name:** `com.hypixel.hytale.registry.Registry`  

**Type:** abstract Class

**Extends:** `Registration>`  

### Public Methods

```java
public boolean isEnabled();
```

```java
public void enable();
```

```java
public void shutdown();
```

```java
public T register(T);
```

```java
public List<BooleanConsumer> getRegistrations();
```

```java
public String toString();
```

---

## Registration

**Package:** `com.hypixel.hytale.registry`  
**Full Name:** `com.hypixel.hytale.registry.Registration`  

**Type:** Class


### Public Constructors

```java
public Registration(function.BooleanSupplier, Runnable);
```

### Public Methods

```java
public void unregister();
```

```java
public boolean isRegistered();
```

```java
public String toString();
```

---

## AssetModule

**Package:** `com.hypixel.hytale.server.core.asset`  
**Full Name:** `com.hypixel.hytale.server.core.asset.AssetModule`  

**Type:** Class

**Extends:** `JavaPlugin`  

### Public Fields

```java
public static final PluginManifest MANIFEST;
```

### Public Methods

```java
public static AssetModule get();
```

### Public Constructors

```java
public AssetModule(JavaPluginInit);
```

```java
public AssetPack getBaseAssetPack();
```

```java
public List<AssetPack> getAssetPacks();
```

```java
public AssetMonitor getAssetMonitor();
```

```java
public AssetPack findAssetPackForPath(java.nio.file.Path);
```

```java
public boolean isAssetPathImmutable(java.nio.file.Path);
```

```java
public void registerPack(String, java.nio.file.Path, PluginManifest);
```

```java
public void unregisterPack(String);
```

```java
public AssetPack getAssetPack(String);
```

```java
public void initPendingStores();
```

---

## LoadAssetEvent

**Package:** `com.hypixel.hytale.server.core.asset`  
**Full Name:** `com.hypixel.hytale.server.core.asset.LoadAssetEvent`  

**Type:** Class

**Implements:** `IEvent<java.lang.Void>`  

### Public Fields

```java
public static final short PRIORITY_LOAD_COMMON;
```

```java
public static final short PRIORITY_LOAD_REGISTRY;
```

```java
public static final short PRIORITY_LOAD_LATE;
```

### Public Constructors

```java
public LoadAssetEvent(long);
```

### Public Methods

```java
public long getBootStart();
```

```java
public boolean isShouldShutdown();
```

```java
public List<String> getReasons();
```

```java
public void failed(boolean, String);
```

```java
public String toString();
```

---

## AssetPackRegisterEvent

**Package:** `com.hypixel.hytale.server.core.asset`  
**Full Name:** `com.hypixel.hytale.server.core.asset.AssetPackRegisterEvent`  

**Type:** Class

**Implements:** `IEvent<java.lang.Void>`  

### Public Constructors

```java
public AssetPackRegisterEvent(AssetPack);
```

### Public Methods

```java
public AssetPack getAssetPack();
```

---



