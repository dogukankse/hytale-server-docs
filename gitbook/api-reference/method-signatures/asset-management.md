# Asset Management

Asset loading and storage classes from `com.hypixel.hytale.assetstore` package.

**Classes:** 8

---

## AssetStore

**Package:** `com.hypixel.hytale.assetstore`  
**Full Name:** `com.hypixel.hytale.assetstore.AssetStore`  

**Type:** abstract Class

**Extends:** `JsonAssetWithMap<K,`  

### Public Fields

```java
public static boolean DISABLE_ASSET_COMPARE;
```

```java
public static boolean DISABLE_DYNAMIC_DEPENDENCIES;
```

### Public Constructors

```java
public AssetStore(AssetStore$Builder<K, T, M, ?>);
```

### Public Methods

```java
public abstract void addFileMonitor(String, java.nio.file.Path);
```

```java
public abstract void removeFileMonitor(java.nio.file.Path);
```

```java
public Class<K> getKeyClass();
```

```java
public Class<T> getAssetClass();
```

```java
public String getPath();
```

```java
public String getExtension();
```

```java
public AssetCodec<K, T> getCodec();
```

```java
public function.Function<T, K> getKeyFunction();
```

```java
public Set<Class<? extends JsonAsset<?>>> getLoadsAfter();
```

```java
public M getAssetMap();
```

```java
public function.Function<K, T> getReplaceOnRemove();
```

```java
public boolean isUnmodifiable();
```

```java
public List<T> getPreAddedAssets();
```

```java
public <X extends JsonAssetWithMap> boolean hasLoadedContainedAssetsFor(Class<X>);
```

```java
public Class<? extends JsonAsset<?>> getIdProvider();
```

```java
public HytaleLogger getLogger();
```

```java
public void simplifyLoadBeforeDependencies();
```

```java
public <D extends JsonAsset<?>> void injectLoadsAfter(Class<D>);
```

```java
public K decodeFilePathKey(java.nio.file.Path);
```

```java
public K decodeStringKey(String);
```

```java
public K transformKey(Object);
```

```java
public void validate(K, ValidationResults, ExtraInfo);
```

```java
public void validateCodecDefaults();
```

```java
public void logDependencies();
```

```java
public AssetLoadResult<K, T> loadAssetsFromPaths(String, List<java.nio.file.Path>);
```

```java
public AssetLoadResult<K, T> loadAssetsFromPaths(String, Collection<java.nio.file.Path>, AssetUpdateQuery);
```

```java
public AssetLoadResult<K, T> loadAssetsFromPaths(String, Collection<java.nio.file.Path>, AssetUpdateQuery, boolean);
```

```java
public AssetLoadResult<K, T> loadBuffersWithKeys(String, List<RawAsset<K>>, AssetUpdateQuery, boolean);
```

```java
public AssetLoadResult<K, T> loadAssets(String, List<T>);
```

```java
public AssetLoadResult<K, T> loadAssets(String, List<T>, AssetUpdateQuery);
```

```java
public AssetLoadResult<K, T> loadAssets(String, List<T>, AssetUpdateQuery, boolean);
```

```java
public AssetLoadResult<K, T> loadAssetsWithReferences(String, Map<T, List<AssetReferences<?, ?>>>);
```

```java
public AssetLoadResult<K, T> loadAssetsWithReferences(String, Map<T, List<AssetReferences<?, ?>>>, AssetUpdateQuery);
```

```java
public AssetLoadResult<K, T> loadAssetsWithReferences(String, Map<T, List<AssetReferences<?, ?>>>, AssetUpdateQuery, boolean);
```

```java
public Set<K> removeAssetWithPaths(String, List<java.nio.file.Path>);
```

```java
public Set<K> removeAssetWithPaths(String, List<java.nio.file.Path>, AssetUpdateQuery);
```

```java
public Set<K> removeAssetWithPath(java.nio.file.Path);
```

```java
public Set<K> removeAssetWithPath(java.nio.file.Path, AssetUpdateQuery);
```

```java
public Set<K> removeAssets(Collection<K>);
```

```java
public Set<K> removeAssets(String, boolean, Collection<K>, AssetUpdateQuery);
```

```java
public void removeAssetPack(String);
```

```java
public T decode(String, K, org.bson.BsonDocument);
```

```java
public <CK> void addChildAssetReferences(K, Class<? extends JsonAssetWithMap<CK, ?>>, Set<CK>);
```

```java
public void logUnusedKeys(K, java.nio.file.Path, AssetExtraInfo<K>);
```

```java
public String toString();
```

---

## AssetRegistry

**Package:** `com.hypixel.hytale.assetstore`  
**Full Name:** `com.hypixel.hytale.assetstore.AssetRegistry`  

**Type:** Class


### Public Fields

```java
public static final concurrent.locks.ReadWriteLock ASSET_LOCK;
```

```java
public static boolean HAS_INIT;
```

```java
public static final int TAG_NOT_FOUND;
```

### Public Constructors

```java
public AssetRegistry();
```

### Public Methods

```java
public static Map<Class<? extends JsonAssetWithMap>, AssetStore<?, ?, ?>> getStoreMap();
```

```java
public static <K, T extends JsonAssetWithMap<K, M>, M extends AssetMap<K, T>> AssetStore<K, T, M> getAssetStore(Class<T>);
```

```java
public static <K, T extends JsonAssetWithMap<K, M>, M extends AssetMap<K, T>, S extends AssetStore<K, T, M>> S register(S);
```

```java
public static <K, T extends JsonAssetWithMap<K, M>, M extends AssetMap<K, T>, S extends AssetStore<K, T, M>> void unregister(S);
```

```java
public static int getTagIndex(String);
```

```java
public static int getOrCreateTagIndex(String);
```

```java
public static boolean registerClientTag(String);
```

```java
public static it.unimi.dsi.fastutil.objects.Object2IntMap<String> getClientTags();
```

---

## AssetPack

**Package:** `com.hypixel.hytale.assetstore`  
**Full Name:** `com.hypixel.hytale.assetstore.AssetPack`  

**Type:** Class


### Public Constructors

```java
public AssetPack(java.nio.file.Path, String, java.nio.file.Path, java.nio.file.FileSystem, boolean, PluginManifest);
```

### Public Methods

```java
public String getName();
```

```java
public java.nio.file.Path getRoot();
```

```java
public java.nio.file.FileSystem getFileSystem();
```

```java
public PluginManifest getManifest();
```

```java
public boolean isImmutable();
```

```java
public java.nio.file.Path getPackLocation();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

```java
public String toString();
```

---

## AssetHolder

**Package:** `com.hypixel.hytale.assetstore`  
**Full Name:** `com.hypixel.hytale.assetstore.AssetHolder`  

**Type:** interface


---

## AssetMap

**Package:** `com.hypixel.hytale.assetstore`  
**Full Name:** `com.hypixel.hytale.assetstore.AssetMap`  

**Type:** abstract Class

**Extends:** `JsonAsset<K>>`  

### Public Constructors

```java
public AssetMap();
```

### Public Methods

```java
public abstract T getAsset(K);
```

```java
public abstract T getAsset(String, K);
```

```java
public abstract java.nio.file.Path getPath(K);
```

```java
public abstract String getAssetPack(K);
```

```java
public abstract Set<K> getKeys(java.nio.file.Path);
```

```java
public abstract Set<K> getChildren(K);
```

```java
public abstract int getAssetCount();
```

```java
public abstract Map<K, T> getAssetMap();
```

```java
public abstract Map<K, java.nio.file.Path> getPathMap(String);
```

```java
public abstract Set<K> getKeysForTag(int);
```

```java
public abstract it.unimi.dsi.fastutil.ints.IntSet getTagIndexes();
```

```java
public abstract int getTagCount();
```

```java
public boolean requireReplaceOnRemove();
```

```java
public abstract Set<K> getKeysForPack(String);
```

---

## JsonAsset

**Package:** `com.hypixel.hytale.assetstore`  
**Full Name:** `com.hypixel.hytale.assetstore.JsonAsset`  

**Type:** interface


### Public Methods

```java
public abstract K getId();
```

---

## RawAsset

**Package:** `com.hypixel.hytale.assetstore`  
**Full Name:** `com.hypixel.hytale.assetstore.RawAsset`  

**Type:** Class

**Implements:** `AssetHolder<K>`  

### Public Constructors

```java
public RawAsset(K, java.nio.file.Path);
```

```java
public RawAsset(java.nio.file.Path, K, K, int, char[], AssetExtraInfo$Data, ContainedAssetCodec$Mode);
```

### Public Methods

```java
public K getKey();
```

```java
public boolean isParentKeyResolved();
```

```java
public K getParentKey();
```

```java
public java.nio.file.Path getPath();
```

```java
public java.nio.file.Path getParentPath();
```

```java
public int getLineOffset();
```

```java
public char[] getBuffer();
```

```java
public ContainedAssetCodec$Mode getContainedAssetMode();
```

```java
public AssetExtraInfo$Data makeData(Class<? extends JsonAssetWithMap<K, ?>>, K, K);
```

```java
public RawAsset<K> withResolveKeys(K, K);
```

```java
public String toString();
```

---

## DecodedAsset

**Package:** `com.hypixel.hytale.assetstore`  
**Full Name:** `com.hypixel.hytale.assetstore.DecodedAsset`  

**Type:** Class

**Extends:** `JsonAsset<K>>`  
**Implements:** `AssetHolder<K>`  

### Public Constructors

```java
public DecodedAsset(K, T);
```

### Public Methods

```java
public K getKey();
```

```java
public T getAsset();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

```java
public String toString();
```

---

