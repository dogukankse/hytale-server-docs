# Component System (ECS)

Entity Component System classes from `com.hypixel.hytale.component` package.

**Classes:** 16

---

## Component

**Package:** `com.hypixel.hytale.component`  
**Full Name:** `com.hypixel.hytale.component.Component`  

**Type:** interface

**Extends:** `java.lang.Cloneable`  

### Public Fields

```java
public static final Component[] EMPTY_ARRAY;
```

### Public Methods

```java
public abstract Component<ECS_TYPE> clone();
```

```java
public default Component<ECS_TYPE> cloneSerializable();
```

---

## ComponentType

**Package:** `com.hypixel.hytale.component`  
**Full Name:** `com.hypixel.hytale.component.ComponentType`  

**Type:** Class

**Extends:** `Component<ECS_TYPE>>`  
**Implements:** `java.lang.Comparable<ComponentType<ECS_TYPE, ?>>, Query<ECS_TYPE>`  

### Public Fields

```java
public static final ComponentType[] EMPTY_ARRAY;
```

### Public Constructors

```java
public ComponentType();
```

### Public Methods

```java
public ComponentRegistry<ECS_TYPE> getRegistry();
```

```java
public Class<? super T> getTypeClass();
```

```java
public int getIndex();
```

```java
public boolean test(Archetype<ECS_TYPE>);
```

```java
public boolean requiresComponentType(ComponentType<ECS_TYPE, ?>);
```

```java
public void validateRegistry(ComponentRegistry<ECS_TYPE>);
```

```java
public void validate();
```

```java
public int compareTo(ComponentType<ECS_TYPE, ?>);
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

```java
public int compareTo(Object);
```

---

## ComponentRegistry

**Package:** `com.hypixel.hytale.component`  
**Full Name:** `com.hypixel.hytale.component.ComponentRegistry`  

**Type:** Class

**Implements:** `IComponentRegistry<ECS_TYPE>`  

### Public Fields

```java
public static final int UNASSIGNED_INDEX;
```

```java
public static final int DEFAULT_INITIAL_SIZE;
```

### Public Constructors

```java
public ComponentRegistry();
```

### Public Methods

```java
public boolean isShutdown();
```

```java
public void shutdown();
```

```java
public concurrent.locks.ReadWriteLock getDataUpdateLock();
```

```java
public ComponentType<ECS_TYPE, UnknownComponents<ECS_TYPE>> getUnknownComponentType();
```

```java
public ComponentType<ECS_TYPE, NonTicking<ECS_TYPE>> getNonTickingComponentType();
```

```java
public ComponentType<ECS_TYPE, NonSerialized<ECS_TYPE>> getNonSerializedComponentType();
```

```java
public SystemType<ECS_TYPE, HolderSystem<ECS_TYPE>> getHolderSystemType();
```

```java
public SystemType<ECS_TYPE, RefSystem<ECS_TYPE>> getRefSystemType();
```

```java
public SystemType<ECS_TYPE, RefChangeSystem<ECS_TYPE, ?>> getRefChangeSystemType();
```

```java
public SystemType<ECS_TYPE, QuerySystem<ECS_TYPE>> getQuerySystemType();
```

```java
public SystemType<ECS_TYPE, TickingSystem<ECS_TYPE>> getTickingSystemType();
```

```java
public SystemType<ECS_TYPE, TickableSystem<ECS_TYPE>> getTickableSystemType();
```

```java
public SystemType<ECS_TYPE, RunWhenPausedSystem<ECS_TYPE>> getRunWhenPausedSystemType();
```

```java
public SystemType<ECS_TYPE, ArchetypeTickingSystem<ECS_TYPE>> getArchetypeTickingSystemType();
```

```java
public <T extends Component<ECS_TYPE>> ComponentType<ECS_TYPE, T> registerComponent(Class<? super T>, function.Supplier<T>);
```

```java
public <T extends Component<ECS_TYPE>> ComponentType<ECS_TYPE, T> registerComponent(Class<? super T>, String, BuilderCodec<T>);
```

```java
public <T extends Component<ECS_TYPE>> ComponentType<ECS_TYPE, T> registerComponent(Class<? super T>, String, BuilderCodec<T>, boolean);
```

```java
public <T extends Component<ECS_TYPE>> void unregisterComponent(ComponentType<ECS_TYPE, T>);
```

```java
public <T extends Resource<ECS_TYPE>> ResourceType<ECS_TYPE, T> registerResource(Class<? super T>, function.Supplier<T>);
```

```java
public <T extends Resource<ECS_TYPE>> ResourceType<ECS_TYPE, T> registerResource(Class<? super T>, String, BuilderCodec<T>);
```

```java
public <T extends Resource<ECS_TYPE>> void unregisterResource(ResourceType<ECS_TYPE, T>);
```

```java
public <T extends ISystem<ECS_TYPE>> SystemType<ECS_TYPE, T> registerSystemType(Class<? super T>);
```

```java
public <T extends ISystem<ECS_TYPE>> void unregisterSystemType(SystemType<ECS_TYPE, T>);
```

```java
public <T extends EcsEvent> EntityEventType<ECS_TYPE, T> registerEntityEventType(Class<? super T>);
```

```java
public <T extends EcsEvent> WorldEventType<ECS_TYPE, T> registerWorldEventType(Class<? super T>);
```

```java
public <T extends EcsEvent> void unregisterEntityEventType(EntityEventType<ECS_TYPE, T>);
```

```java
public <T extends EcsEvent> void unregisterWorldEventType(WorldEventType<ECS_TYPE, T>);
```

```java
public SystemGroup<ECS_TYPE> registerSystemGroup();
```

```java
public SystemGroup<ECS_TYPE> registerSystemGroup(Set<Dependency<ECS_TYPE>>);
```

```java
public void unregisterSystemGroup(SystemGroup<ECS_TYPE>);
```

```java
public void registerSystem(ISystem<ECS_TYPE>);
```

```java
public void registerSystem(ISystem<ECS_TYPE>, boolean);
```

```java
public void unregisterSystem(Class<? extends ISystem<ECS_TYPE>>);
```

```java
public ResourceType<ECS_TYPE, SpatialResource<Ref<ECS_TYPE>, ECS_TYPE>> registerSpatialResource(function.Supplier<SpatialStructure<Ref<ECS_TYPE>>>);
```

```java
public Store<ECS_TYPE> addStore(ECS_TYPE, IResourceStorage);
```

```java
public Store<ECS_TYPE> addStore(ECS_TYPE, IResourceStorage, function.Consumer<Store<ECS_TYPE>>);
```

```java
public void removeStore(Store<ECS_TYPE>);
```

```java
public Holder<ECS_TYPE> newHolder();
```

```java
public Holder<ECS_TYPE> newHolder(Archetype<ECS_TYPE>, Component<ECS_TYPE>[]);
```

```java
public ComponentRegistry$Data<ECS_TYPE> getData();
```

```java
public BuilderCodec<Holder<ECS_TYPE>> getEntityCodec();
```

```java
public void assertInStoreThread();
```

```java
public Holder<ECS_TYPE> deserialize(org.bson.BsonDocument);
```

```java
public Holder<ECS_TYPE> deserialize(org.bson.BsonDocument, int);
```

```java
public org.bson.BsonDocument serialize(Holder<ECS_TYPE>);
```

```java
public boolean hasSystem(ISystem<ECS_TYPE>);
```

```java
public <T extends ISystem<ECS_TYPE>> boolean hasSystemClass(Class<T>);
```

```java
public <T extends ISystem<ECS_TYPE>> boolean hasSystemType(SystemType<ECS_TYPE, T>);
```

```java
public boolean hasSystemGroup(SystemGroup<ECS_TYPE>);
```

```java
public <T extends EcsEvent> EntityEventType<ECS_TYPE, T> getEntityEventTypeForClass(Class<T>);
```

```java
public <T extends EcsEvent> WorldEventType<ECS_TYPE, T> getWorldEventTypeForClass(Class<T>);
```

```java
public String toString();
```

```java
public <T extends Component<ECS_TYPE>> T createComponent(ComponentType<ECS_TYPE, T>);
```

---

## ComponentRegistration

**Package:** `com.hypixel.hytale.component`  
**Full Name:** `com.hypixel.hytale.component.ComponentRegistration`  

**Type:** final Class

**Extends:** `Component<ECS_TYPE>>`  

### Public Constructors

```java
public ComponentRegistration(Class<? super T>, String, BuilderCodec<T>, function.Supplier<T>, ComponentType<ECS_TYPE, T>);
```

### Public Methods

```java
public final String toString();
```

```java
public final int hashCode();
```

```java
public final boolean equals(Object);
```

```java
public Class<? super T> typeClass();
```

```java
public String id();
```

```java
public BuilderCodec<T> codec();
```

```java
public function.Supplier<T> supplier();
```

```java
public ComponentType<ECS_TYPE, T> componentType();
```

---

## IComponentRegistry

**Package:** `com.hypixel.hytale.component`  
**Full Name:** `com.hypixel.hytale.component.IComponentRegistry`  

**Type:** interface


### Public Methods

```java
public abstract <T extends Component<ECS_TYPE>> ComponentType<ECS_TYPE, T> registerComponent(Class<? super T>, function.Supplier<T>);
```

```java
public abstract <T extends Component<ECS_TYPE>> ComponentType<ECS_TYPE, T> registerComponent(Class<? super T>, String, BuilderCodec<T>);
```

```java
public abstract <T extends Resource<ECS_TYPE>> ResourceType<ECS_TYPE, T> registerResource(Class<? super T>, function.Supplier<T>);
```

```java
public abstract <T extends Resource<ECS_TYPE>> ResourceType<ECS_TYPE, T> registerResource(Class<? super T>, String, BuilderCodec<T>);
```

```java
public abstract <T extends ISystem<ECS_TYPE>> SystemType<ECS_TYPE, T> registerSystemType(Class<? super T>);
```

```java
public abstract <T extends EcsEvent> EntityEventType<ECS_TYPE, T> registerEntityEventType(Class<? super T>);
```

```java
public abstract <T extends EcsEvent> WorldEventType<ECS_TYPE, T> registerWorldEventType(Class<? super T>);
```

```java
public abstract SystemGroup<ECS_TYPE> registerSystemGroup();
```

```java
public abstract void registerSystem(ISystem<ECS_TYPE>);
```

```java
public abstract ResourceType<ECS_TYPE, SpatialResource<Ref<ECS_TYPE>, ECS_TYPE>> registerSpatialResource(function.Supplier<SpatialStructure<Ref<ECS_TYPE>>>);
```

---

## Store

**Package:** `com.hypixel.hytale.component`  
**Full Name:** `com.hypixel.hytale.component.Store`  

**Type:** Class

**Implements:** `ComponentAccessor<ECS_TYPE>`  

### Public Fields

```java
public static final Store[] EMPTY_ARRAY;
```

### Public Methods

```java
public int getStoreIndex();
```

```java
public ComponentRegistry<ECS_TYPE> getRegistry();
```

```java
public ECS_TYPE getExternalData();
```

```java
public IResourceStorage getResourceStorage();
```

```java
public ParallelTask<EntityTickingSystem$SystemTaskData<ECS_TYPE>> getParallelTask();
```

```java
public ParallelTask<EntityDataSystem$SystemTaskData<ECS_TYPE, ?, ?>> getFetchTask();
```

```java
public HistoricMetric[] getSystemMetrics();
```

```java
public boolean isShutdown();
```

```java
public void shutdown();
```

```java
public concurrent.CompletableFuture<Void> saveAllResources();
```

```java
public int getEntityCount();
```

```java
public int getEntityCountFor(Query<ECS_TYPE>);
```

```java
public int getEntityCountFor(int);
```

```java
public int getArchetypeChunkCount();
```

```java
public ArchetypeChunkData[] collectArchetypeChunkData();
```

```java
public int getArchetypeChunkCountFor(int);
```

```java
public Ref<ECS_TYPE> addEntity(Archetype<ECS_TYPE>, AddReason);
```

```java
public Ref<ECS_TYPE> addEntity(Holder<ECS_TYPE>, AddReason);
```

```java
public Ref<ECS_TYPE> addEntity(Holder<ECS_TYPE>, Ref<ECS_TYPE>, AddReason);
```

```java
public Ref<ECS_TYPE>[] addEntities(Holder<ECS_TYPE>[], AddReason);
```

```java
public Ref<ECS_TYPE>[] addEntities(Holder<ECS_TYPE>[], int, int, AddReason);
```

```java
public void addEntities(Holder<ECS_TYPE>[], Ref<ECS_TYPE>[], AddReason);
```

```java
public void addEntities(Holder<ECS_TYPE>[], int, Ref<ECS_TYPE>[], int, int, AddReason);
```

```java
public Holder<ECS_TYPE> copyEntity(Ref<ECS_TYPE>);
```

```java
public Holder<ECS_TYPE> copyEntity(Ref<ECS_TYPE>, Holder<ECS_TYPE>);
```

```java
public Holder<ECS_TYPE> copySerializableEntity(Ref<ECS_TYPE>);
```

```java
public Holder<ECS_TYPE> copySerializableEntity(Ref<ECS_TYPE>, Holder<ECS_TYPE>);
```

```java
public Archetype<ECS_TYPE> getArchetype(Ref<ECS_TYPE>);
```

```java
public Holder<ECS_TYPE> removeEntity(Ref<ECS_TYPE>, RemoveReason);
```

```java
public Holder<ECS_TYPE> removeEntity(Ref<ECS_TYPE>, Holder<ECS_TYPE>, RemoveReason);
```

```java
public Holder<ECS_TYPE>[] removeEntities(Ref<ECS_TYPE>[], RemoveReason);
```

```java
public Holder<ECS_TYPE>[] removeEntities(Ref<ECS_TYPE>[], int, int, RemoveReason);
```

```java
public Holder<ECS_TYPE>[] removeEntities(Ref<ECS_TYPE>[], Holder<ECS_TYPE>[], RemoveReason);
```

```java
public Holder<ECS_TYPE>[] removeEntities(Ref<ECS_TYPE>[], int, Holder<ECS_TYPE>[], int, int, RemoveReason);
```

```java
public <T extends Component<ECS_TYPE>> void ensureComponent(Ref<ECS_TYPE>, ComponentType<ECS_TYPE, T>);
```

```java
public <T extends Component<ECS_TYPE>> T ensureAndGetComponent(Ref<ECS_TYPE>, ComponentType<ECS_TYPE, T>);
```

```java
public <T extends Component<ECS_TYPE>> T addComponent(Ref<ECS_TYPE>, ComponentType<ECS_TYPE, T>);
```

```java
public <T extends Component<ECS_TYPE>> void addComponent(Ref<ECS_TYPE>, ComponentType<ECS_TYPE, T>, T);
```

```java
public <T extends Component<ECS_TYPE>> void replaceComponent(Ref<ECS_TYPE>, ComponentType<ECS_TYPE, T>, T);
```

```java
public <T extends Component<ECS_TYPE>> void putComponent(Ref<ECS_TYPE>, ComponentType<ECS_TYPE, T>, T);
```

```java
public <T extends Component<ECS_TYPE>> T getComponent(Ref<ECS_TYPE>, ComponentType<ECS_TYPE, T>);
```

```java
public <T extends Component<ECS_TYPE>> void removeComponent(Ref<ECS_TYPE>, ComponentType<ECS_TYPE, T>);
```

```java
public <T extends Component<ECS_TYPE>> void tryRemoveComponent(Ref<ECS_TYPE>, ComponentType<ECS_TYPE, T>);
```

```java
public <T extends Component<ECS_TYPE>> boolean removeComponentIfExists(Ref<ECS_TYPE>, ComponentType<ECS_TYPE, T>);
```

```java
public <T extends Resource<ECS_TYPE>> void replaceResource(ResourceType<ECS_TYPE, T>, T);
```

```java
public <T extends Resource<ECS_TYPE>> T getResource(ResourceType<ECS_TYPE, T>);
```

```java
public void forEachChunk(function.BiConsumer<ArchetypeChunk<ECS_TYPE>, CommandBuffer<ECS_TYPE>>);
```

```java
public boolean forEachChunk(function.BiPredicate<ArchetypeChunk<ECS_TYPE>, CommandBuffer<ECS_TYPE>>);
```

```java
public void forEachChunk(Query<ECS_TYPE>, function.BiConsumer<ArchetypeChunk<ECS_TYPE>, CommandBuffer<ECS_TYPE>>);
```

```java
public boolean forEachChunk(Query<ECS_TYPE>, function.BiPredicate<ArchetypeChunk<ECS_TYPE>, CommandBuffer<ECS_TYPE>>);
```

```java
public void forEachChunk(int, function.BiConsumer<ArchetypeChunk<ECS_TYPE>, CommandBuffer<ECS_TYPE>>);
```

```java
public boolean forEachChunk(int, function.BiPredicate<ArchetypeChunk<ECS_TYPE>, CommandBuffer<ECS_TYPE>>);
```

```java
public void forEachEntityParallel(IntBiObjectConsumer<ArchetypeChunk<ECS_TYPE>, CommandBuffer<ECS_TYPE>>);
```

```java
public void forEachEntityParallel(Query<ECS_TYPE>, IntBiObjectConsumer<ArchetypeChunk<ECS_TYPE>, CommandBuffer<ECS_TYPE>>);
```

```java
public <T extends ArchetypeDataSystem<ECS_TYPE, Q, R>, Q, R> void fetch(SystemType<ECS_TYPE, T>, Q, List<R>);
```

```java
public <T extends EntityDataSystem<ECS_TYPE, Q, R>, Q, R> void fetch(Collection<Ref<ECS_TYPE>>, SystemType<ECS_TYPE, T>, Q, List<R>);
```

```java
public <Event extends EcsEvent> void invoke(Ref<ECS_TYPE>, Event);
```

```java
public <Event extends EcsEvent> void invoke(EntityEventType<ECS_TYPE, Event>, Ref<ECS_TYPE>, Event);
```

```java
public <Event extends EcsEvent> void invoke(Event);
```

```java
public <Event extends EcsEvent> void invoke(WorldEventType<ECS_TYPE, Event>, Event);
```

```java
public void tick(float);
```

```java
public void pausedTick(float);
```

```java
public void tick(ArchetypeTickingSystem<ECS_TYPE>, float, int);
```

```java
public void assertWriteProcessing();
```

```java
public boolean isProcessing();
```

```java
public void assertThread();
```

```java
public boolean isInThread();
```

```java
public boolean isAliveInDifferentThread();
```

```java
public String toString();
```

---

## Archetype

**Package:** `com.hypixel.hytale.component`  
**Full Name:** `com.hypixel.hytale.component.Archetype`  

**Type:** Class

**Implements:** `Query<ECS_TYPE>`  

### Public Methods

```java
public static <ECS_TYPE> Archetype<ECS_TYPE> empty();
```

```java
public int getMinIndex();
```

```java
public int count();
```

```java
public int length();
```

```java
public ComponentType<ECS_TYPE, ?> get(int);
```

```java
public boolean isEmpty();
```

```java
public boolean contains(ComponentType<ECS_TYPE, ?>);
```

```java
public boolean contains(Archetype<ECS_TYPE>);
```

```java
public void validateComponentType(ComponentType<ECS_TYPE, ?>);
```

```java
public void validateComponents(Component<ECS_TYPE>[], ComponentType<ECS_TYPE, UnknownComponents<ECS_TYPE>>);
```

```java
public boolean hasSerializableComponents(ComponentRegistry$Data<ECS_TYPE>);
```

```java
public Archetype<ECS_TYPE> getSerializableArchetype(ComponentRegistry$Data<ECS_TYPE>);
```

```java
public ExactArchetypeQuery<ECS_TYPE> asExactQuery();
```

```java
public static <ECS_TYPE> Archetype<ECS_TYPE> of(ComponentType<ECS_TYPE, ?>);
```

```java
public static <ECS_TYPE> Archetype<ECS_TYPE> of(ComponentType<ECS_TYPE, ?>...);
```

```java
public static <ECS_TYPE, T extends Component<ECS_TYPE>> Archetype<ECS_TYPE> add(Archetype<ECS_TYPE>, ComponentType<ECS_TYPE, T>);
```

```java
public static <ECS_TYPE, T extends Component<ECS_TYPE>> Archetype<ECS_TYPE> remove(Archetype<ECS_TYPE>, ComponentType<ECS_TYPE, T>);
```

```java
public boolean test(Archetype<ECS_TYPE>);
```

```java
public boolean requiresComponentType(ComponentType<ECS_TYPE, ?>);
```

```java
public void validateRegistry(ComponentRegistry<ECS_TYPE>);
```

```java
public void validate();
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

## ArchetypeChunk

**Package:** `com.hypixel.hytale.component`  
**Full Name:** `com.hypixel.hytale.component.ArchetypeChunk`  

**Type:** Class


### Public Methods

```java
public static <ECS_TYPE> ArchetypeChunk<ECS_TYPE>[] emptyArray();
```

### Public Constructors

```java
public ArchetypeChunk(Store<ECS_TYPE>, Archetype<ECS_TYPE>);
```

```java
public Archetype<ECS_TYPE> getArchetype();
```

```java
public int size();
```

```java
public Ref<ECS_TYPE> getReferenceTo(int);
```

```java
public <T extends Component<ECS_TYPE>> void setComponent(int, ComponentType<ECS_TYPE, T>, T);
```

```java
public <T extends Component<ECS_TYPE>> T getComponent(int, ComponentType<ECS_TYPE, T>);
```

```java
public int addEntity(Ref<ECS_TYPE>, Holder<ECS_TYPE>);
```

```java
public Holder<ECS_TYPE> copyEntity(int, Holder<ECS_TYPE>);
```

```java
public Holder<ECS_TYPE> copySerializableEntity(ComponentRegistry$Data<ECS_TYPE>, int, Holder<ECS_TYPE>);
```

```java
public Holder<ECS_TYPE> removeEntity(int, Holder<ECS_TYPE>);
```

```java
public void transferTo(Holder<ECS_TYPE>, ArchetypeChunk<ECS_TYPE>, function.Consumer<Holder<ECS_TYPE>>, IntObjectConsumer<Ref<ECS_TYPE>>);
```

```java
public void transferSomeTo(Holder<ECS_TYPE>, ArchetypeChunk<ECS_TYPE>, function.IntPredicate, function.Consumer<Holder<ECS_TYPE>>, IntObjectConsumer<Ref<ECS_TYPE>>);
```

```java
public void appendDump(String, StringBuilder);
```

```java
public String toString();
```

---

## Resource

**Package:** `com.hypixel.hytale.component`  
**Full Name:** `com.hypixel.hytale.component.Resource`  

**Type:** interface

**Extends:** `java.lang.Cloneable`  

### Public Fields

```java
public static final Resource[] EMPTY_ARRAY;
```

### Public Methods

```java
public abstract Resource<ECS_TYPE> clone();
```

---

## ResourceType

**Package:** `com.hypixel.hytale.component`  
**Full Name:** `com.hypixel.hytale.component.ResourceType`  

**Type:** Class

**Extends:** `Resource<ECS_TYPE>>`  
**Implements:** `java.lang.Comparable<ResourceType<ECS_TYPE, ?>>`  

### Public Fields

```java
public static final ResourceType[] EMPTY_ARRAY;
```

### Public Constructors

```java
public ResourceType();
```

### Public Methods

```java
public ComponentRegistry<ECS_TYPE> getRegistry();
```

```java
public Class<? super T> getTypeClass();
```

```java
public int getIndex();
```

```java
public void validateRegistry(ComponentRegistry<ECS_TYPE>);
```

```java
public void validate();
```

```java
public int compareTo(ResourceType<ECS_TYPE, ?>);
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

```java
public int compareTo(Object);
```

---

## ResourceRegistration

**Package:** `com.hypixel.hytale.component`  
**Full Name:** `com.hypixel.hytale.component.ResourceRegistration`  

**Type:** final Class

**Extends:** `Resource<ECS_TYPE>>`  

### Public Constructors

```java
public ResourceRegistration(Class<? super T>, String, BuilderCodec<T>, function.Supplier<T>, ResourceType<ECS_TYPE, T>);
```

### Public Methods

```java
public final String toString();
```

```java
public final int hashCode();
```

```java
public final boolean equals(Object);
```

```java
public Class<? super T> typeClass();
```

```java
public String id();
```

```java
public BuilderCodec<T> codec();
```

```java
public function.Supplier<T> supplier();
```

```java
public ResourceType<ECS_TYPE, T> resourceType();
```

---

## SystemType

**Package:** `com.hypixel.hytale.component`  
**Full Name:** `com.hypixel.hytale.component.SystemType`  

**Type:** Class

**Extends:** `ISystem<ECS_TYPE>>`  
**Implements:** `java.lang.Comparable<SystemType<ECS_TYPE, ?>>`  

### Public Fields

```java
public static final SystemType[] EMPTY_ARRAY;
```

### Public Methods

```java
public ComponentRegistry<ECS_TYPE> getRegistry();
```

```java
public Class<? super T> getTypeClass();
```

```java
public boolean isType(ISystem<ECS_TYPE>);
```

```java
public int getIndex();
```

```java
public void validateRegistry(ComponentRegistry<ECS_TYPE>);
```

```java
public void validate();
```

```java
public int compareTo(SystemType<ECS_TYPE, ?>);
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

```java
public int compareTo(Object);
```

---

## SystemGroup

**Package:** `com.hypixel.hytale.component`  
**Full Name:** `com.hypixel.hytale.component.SystemGroup`  

**Type:** Class

**Implements:** `java.lang.Comparable<SystemGroup<ECS_TYPE>>`  

### Public Methods

```java
public ComponentRegistry<ECS_TYPE> getRegistry();
```

```java
public Set<Dependency<ECS_TYPE>> getDependencies();
```

```java
public int getIndex();
```

```java
public void validateRegistry(ComponentRegistry<ECS_TYPE>);
```

```java
public void validate();
```

```java
public int compareTo(SystemGroup<ECS_TYPE>);
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

```java
public int compareTo(Object);
```

---

## Holder

**Package:** `com.hypixel.hytale.component`  
**Full Name:** `com.hypixel.hytale.component.Holder`  

**Type:** Class


### Public Methods

```java
public static <T> Holder<T>[] emptyArray();
```

```java
public Component<ECS_TYPE>[] ensureComponentsSize(int);
```

```java
public void init(Archetype<ECS_TYPE>, Component<ECS_TYPE>[]);
```

```java
public void _internal_init(Archetype<ECS_TYPE>, Component<ECS_TYPE>[], ComponentType<ECS_TYPE, UnknownComponents<ECS_TYPE>>);
```

```java
public Archetype<ECS_TYPE> getArchetype();
```

```java
public <T extends Component<ECS_TYPE>> void ensureComponent(ComponentType<ECS_TYPE, T>);
```

```java
public <T extends Component<ECS_TYPE>> T ensureAndGetComponent(ComponentType<ECS_TYPE, T>);
```

```java
public <T extends Component<ECS_TYPE>> void addComponent(ComponentType<ECS_TYPE, T>, T);
```

```java
public <T extends Component<ECS_TYPE>> void replaceComponent(ComponentType<ECS_TYPE, T>, T);
```

```java
public <T extends Component<ECS_TYPE>> void putComponent(ComponentType<ECS_TYPE, T>, T);
```

```java
public <T extends Component<ECS_TYPE>> T getComponent(ComponentType<ECS_TYPE, T>);
```

```java
public <T extends Component<ECS_TYPE>> void removeComponent(ComponentType<ECS_TYPE, T>);
```

```java
public <T extends Component<ECS_TYPE>> boolean tryRemoveComponent(ComponentType<ECS_TYPE, T>);
```

```java
public boolean hasSerializableComponents(ComponentRegistry$Data<ECS_TYPE>);
```

```java
public void updateData(ComponentRegistry$Data<ECS_TYPE>, ComponentRegistry$Data<ECS_TYPE>);
```

```java
public Holder<ECS_TYPE> clone();
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

## Ref

**Package:** `com.hypixel.hytale.component`  
**Full Name:** `com.hypixel.hytale.component.Ref`  

**Type:** Class


### Public Constructors

```java
public Ref(Store<ECS_TYPE>);
```

```java
public Ref(Store<ECS_TYPE>, int);
```

### Public Methods

```java
public Store<ECS_TYPE> getStore();
```

```java
public int getIndex();
```

```java
public void validate();
```

```java
public boolean isValid();
```

```java
public boolean equals(Object);
```

```java
public boolean equals(Ref<ECS_TYPE>);
```

```java
public int hashCode();
```

```java
public int hashCode0();
```

```java
public String toString();
```

---

## CommandBuffer

**Package:** `com.hypixel.hytale.component`  
**Full Name:** `com.hypixel.hytale.component.CommandBuffer`  

**Type:** Class

**Implements:** `ComponentAccessor<ECS_TYPE>`  

### Public Methods

```java
public Store<ECS_TYPE> getStore();
```

```java
public void run(function.Consumer<Store<ECS_TYPE>>);
```

```java
public <T extends Component<ECS_TYPE>> T getComponent(Ref<ECS_TYPE>, ComponentType<ECS_TYPE, T>);
```

```java
public Archetype<ECS_TYPE> getArchetype(Ref<ECS_TYPE>);
```

```java
public <T extends Resource<ECS_TYPE>> T getResource(ResourceType<ECS_TYPE, T>);
```

```java
public ECS_TYPE getExternalData();
```

```java
public Ref<ECS_TYPE>[] addEntities(Holder<ECS_TYPE>[], AddReason);
```

```java
public Ref<ECS_TYPE> addEntity(Holder<ECS_TYPE>, AddReason);
```

```java
public void addEntities(Holder<ECS_TYPE>[], int, Ref<ECS_TYPE>[], int, int, AddReason);
```

```java
public Ref<ECS_TYPE> addEntity(Holder<ECS_TYPE>, Ref<ECS_TYPE>, AddReason);
```

```java
public Holder<ECS_TYPE> copyEntity(Ref<ECS_TYPE>, Holder<ECS_TYPE>);
```

```java
public void tryRemoveEntity(Ref<ECS_TYPE>, RemoveReason);
```

```java
public void removeEntity(Ref<ECS_TYPE>, RemoveReason);
```

```java
public Holder<ECS_TYPE> removeEntity(Ref<ECS_TYPE>, Holder<ECS_TYPE>, RemoveReason);
```

```java
public <T extends Component<ECS_TYPE>> void ensureComponent(Ref<ECS_TYPE>, ComponentType<ECS_TYPE, T>);
```

```java
public <T extends Component<ECS_TYPE>> T ensureAndGetComponent(Ref<ECS_TYPE>, ComponentType<ECS_TYPE, T>);
```

```java
public <T extends Component<ECS_TYPE>> T addComponent(Ref<ECS_TYPE>, ComponentType<ECS_TYPE, T>);
```

```java
public <T extends Component<ECS_TYPE>> void addComponent(Ref<ECS_TYPE>, ComponentType<ECS_TYPE, T>, T);
```

```java
public <T extends Component<ECS_TYPE>> void replaceComponent(Ref<ECS_TYPE>, ComponentType<ECS_TYPE, T>, T);
```

```java
public <T extends Component<ECS_TYPE>> void removeComponent(Ref<ECS_TYPE>, ComponentType<ECS_TYPE, T>);
```

```java
public <T extends Component<ECS_TYPE>> void tryRemoveComponent(Ref<ECS_TYPE>, ComponentType<ECS_TYPE, T>);
```

```java
public <T extends Component<ECS_TYPE>> void putComponent(Ref<ECS_TYPE>, ComponentType<ECS_TYPE, T>, T);
```

```java
public <Event extends EcsEvent> void invoke(Ref<ECS_TYPE>, Event);
```

```java
public <Event extends EcsEvent> void invoke(EntityEventType<ECS_TYPE, Event>, Ref<ECS_TYPE>, Event);
```

```java
public <Event extends EcsEvent> void invoke(Event);
```

```java
public <Event extends EcsEvent> void invoke(WorldEventType<ECS_TYPE, Event>, Event);
```

```java
public CommandBuffer<ECS_TYPE> fork();
```

```java
public void mergeParallel(CommandBuffer<ECS_TYPE>);
```

```java
public boolean setThread();
```

```java
public void validateEmpty();
```

---

