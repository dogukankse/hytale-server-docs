# Hytale API - Complete Method Signatures

Comprehensive public API reference extracted from HytaleServer.jar using javap.

**Generated:** January 19, 2026
**Classes Documented:** 96

This document provides detailed method signatures, parameters, return types, and public fields for the most important classes in the Hytale API.

---

## Table of Contents

### Event System
### Asset Management

- [AssetStore](#assetstore)
- [AssetRegistry](#assetregistry)
- [AssetPack](#assetpack)
- [AssetHolder](#assetholder)
- [AssetMap](#assetmap)
- [JsonAsset](#jsonasset)
- [RawAsset](#rawasset)
- [DecodedAsset](#decodedasset)

### Component System (ECS)

- [Component](#component)
- [ComponentType](#componenttype)
- [ComponentRegistry](#componentregistry)
- [ComponentRegistration](#componentregistration)
- [IComponentRegistry](#icomponentregistry)
- [Store](#store)
- [Archetype](#archetype)
- [ArchetypeChunk](#archetypechunk)
- [Resource](#resource)
- [ResourceType](#resourcetype)
- [ResourceRegistration](#resourceregistration)
- [SystemType](#systemtype)
- [SystemGroup](#systemgroup)
- [Holder](#holder)
- [Ref](#ref)
- [CommandBuffer](#commandbuffer)

### Event System

- [IEvent](#ievent)
- [IBaseEvent](#ibaseevent)
- [IAsyncEvent](#iasyncevent)
- [IProcessedEvent](#iprocessedevent)
- [ICancellable](#icancellable)
- [EventRegistry](#eventregistry)
- [EventBus](#eventbus)
- [EventBusRegistry](#eventbusregistry)
- [EventPriority](#eventpriority)
- [EventRegistration](#eventregistration)
- [IEventRegistry](#ieventregistry)
- [IEventBus](#ieventbus)

### Math Utilities

- [Vec2f](#vec2f)
- [Vec3f](#vec3f)
- [Vec4f](#vec4f)
- [Mat4f](#mat4f)
- [Quatf](#quatf)
- [Axis](#axis)

### Protocol - Animation

- [Animation](#animation)
- [AnimationSet](#animationset)
- [AnimationSlot](#animationslot)

### Protocol - Audio

- [SoundEvent](#soundevent)
- [SoundCategory](#soundcategory)
- [AudioCategory](#audiocategory)

### Protocol - Blocks

- [BlockType](#blocktype)
- [BlockMaterial](#blockmaterial)
- [BlockTextures](#blocktextures)
- [BlockSoundSet](#blocksoundset)
- [BlockPlacementSettings](#blockplacementsettings)

### Protocol - Camera

- [CameraSettings](#camerasettings)
- [CameraInteraction](#camerainteraction)

### Protocol - Core Types

- [Vector2f](#vector2f)
- [Vector2i](#vector2i)
- [Vector3f](#vector3f)
- [Vector3i](#vector3i)
- [Vector3d](#vector3d)
- [Position](#position)
- [Rotation](#rotation)
- [Color](#color)
- [BlockPosition](#blockposition)

### Protocol - Entities

- [EntityUpdate](#entityupdate)
- [EntityEffect](#entityeffect)
- [EntityStatType](#entitystattype)
- [EntityStatUpdate](#entitystatupdate)

### Protocol - Interactions

- [Interaction](#interaction)
- [InteractionType](#interactiontype)
- [InteractionSettings](#interactionsettings)
- [InteractionChainData](#interactionchaindata)

### Protocol - Items

- [ItemBase](#itembase)
- [ItemLibrary](#itemlibrary)
- [ItemCategory](#itemcategory)
- [ItemQuality](#itemquality)
- [ItemQuantity](#itemquantity)
- [ItemWeapon](#itemweapon)
- [ItemArmor](#itemarmor)
- [ItemTool](#itemtool)

### Protocol - Movement & Physics

- [MovementSettings](#movementsettings)
- [MovementType](#movementtype)
- [MovementStates](#movementstates)
- [PhysicsConfig](#physicsconfig)

### Protocol - Particles

- [Particle](#particle)
- [ParticleSystem](#particlesystem)
- [ParticleSpawner](#particlespawner)

### Utilities

- [HytaleLogger](#hytalelogger)
- [Codec](#codec)
- [KeyedCodec](#keyedcodec)
- [WrappedCodec](#wrappedcodec)
- [Registry](#registry)
- [Registration](#registration)
- [AssetModule](#assetmodule)
- [LoadAssetEvent](#loadassetevent)
- [AssetPackRegisterEvent](#assetpackregisterevent)

---

## IEvent

**Package:** `com.hypixel.hytale.event`  
**Full Name:** `com.hypixel.hytale.event.IEvent`  

**Type:** interface

**Extends:** `IBaseEvent<KeyType>`  

---

## IBaseEvent

**Package:** `com.hypixel.hytale.event`  
**Full Name:** `com.hypixel.hytale.event.IBaseEvent`  

**Type:** interface


---

## IAsyncEvent

**Package:** `com.hypixel.hytale.event`  
**Full Name:** `com.hypixel.hytale.event.IAsyncEvent`  

**Type:** interface

**Extends:** `IBaseEvent<KeyType>`  

---

## IProcessedEvent

**Package:** `com.hypixel.hytale.event`  
**Full Name:** `com.hypixel.hytale.event.IProcessedEvent`  

**Type:** interface


### Public Methods

```java
public abstract void processEvent(String);
```

---

## ICancellable

**Package:** `com.hypixel.hytale.event`  
**Full Name:** `com.hypixel.hytale.event.ICancellable`  

**Type:** interface


### Public Methods

```java
public abstract boolean isCancelled();
```

```java
public abstract void setCancelled(boolean);
```

---

## EventRegistry

**Package:** `com.hypixel.hytale.event`  
**Full Name:** `com.hypixel.hytale.event.EventRegistry`  

**Type:** Class

**Extends:** `Registry<EventRegistration<?,`  
**Implements:** `IEventRegistry`  

### Public Constructors

```java
public EventRegistry(List<BooleanConsumer>, function.BooleanSupplier, String, IEventRegistry);
```

### Public Methods

```java
public <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> register(EventRegistration<KeyType, EventType>);
```

```java
public <EventType extends IBaseEvent<Void>> EventRegistration<Void, EventType> register(Class<? super EventType>, function.Consumer<EventType>);
```

```java
public <EventType extends IBaseEvent<Void>> EventRegistration<Void, EventType> register(EventPriority, Class<? super EventType>, function.Consumer<EventType>);
```

```java
public <EventType extends IBaseEvent<Void>> EventRegistration<Void, EventType> register(short, Class<? super EventType>, function.Consumer<EventType>);
```

```java
public <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> register(Class<? super EventType>, KeyType, function.Consumer<EventType>);
```

```java
public <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> register(EventPriority, Class<? super EventType>, KeyType, function.Consumer<EventType>);
```

```java
public <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> register(short, Class<? super EventType>, KeyType, function.Consumer<EventType>);
```

```java
public <EventType extends IAsyncEvent<Void>> EventRegistration<Void, EventType> registerAsync(Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public <EventType extends IAsyncEvent<Void>> EventRegistration<Void, EventType> registerAsync(EventPriority, Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public <EventType extends IAsyncEvent<Void>> EventRegistration<Void, EventType> registerAsync(short, Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsync(Class<? super EventType>, KeyType, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsync(EventPriority, Class<? super EventType>, KeyType, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsync(short, Class<? super EventType>, KeyType, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> registerGlobal(Class<? super EventType>, function.Consumer<EventType>);
```

```java
public <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> registerGlobal(EventPriority, Class<? super EventType>, function.Consumer<EventType>);
```

```java
public <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> registerGlobal(short, Class<? super EventType>, function.Consumer<EventType>);
```

```java
public <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsyncGlobal(Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsyncGlobal(EventPriority, Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsyncGlobal(short, Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> registerUnhandled(Class<? super EventType>, function.Consumer<EventType>);
```

```java
public <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> registerUnhandled(EventPriority, Class<? super EventType>, function.Consumer<EventType>);
```

```java
public <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> registerUnhandled(short, Class<? super EventType>, function.Consumer<EventType>);
```

```java
public <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsyncUnhandled(Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsyncUnhandled(EventPriority, Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsyncUnhandled(short, Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

---

## EventBus

**Package:** `com.hypixel.hytale.event`  
**Full Name:** `com.hypixel.hytale.event.EventBus`  

**Type:** Class

**Implements:** `IEventBus`  

### Public Constructors

```java
public EventBus(boolean);
```

### Public Methods

```java
public void shutdown();
```

```java
public Set<Class<? extends IBaseEvent<?>>> getRegisteredEventClasses();
```

```java
public Set<String> getRegisteredEventClassNames();
```

```java
public EventBusRegistry<?, ?, ?> getRegistry(String);
```

```java
public <KeyType, EventType extends IBaseEvent<KeyType>> EventBusRegistry<KeyType, EventType, ?> getRegistry(Class<? super EventType>);
```

```java
public <KeyType, EventType extends IEvent<KeyType>> EventBusRegistry<KeyType, EventType, ?> getSyncRegistry(Class<? super EventType>);
```

```java
public <EventType extends IBaseEvent<Void>> EventRegistration<Void, EventType> register(Class<? super EventType>, function.Consumer<EventType>);
```

```java
public <EventType extends IBaseEvent<Void>> EventRegistration<Void, EventType> register(EventPriority, Class<? super EventType>, function.Consumer<EventType>);
```

```java
public <EventType extends IBaseEvent<Void>> EventRegistration<Void, EventType> register(short, Class<? super EventType>, function.Consumer<EventType>);
```

```java
public <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> register(Class<? super EventType>, KeyType, function.Consumer<EventType>);
```

```java
public <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> register(EventPriority, Class<? super EventType>, KeyType, function.Consumer<EventType>);
```

```java
public <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> register(short, Class<? super EventType>, KeyType, function.Consumer<EventType>);
```

```java
public <EventType extends IAsyncEvent<Void>> EventRegistration<Void, EventType> registerAsync(Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public <EventType extends IAsyncEvent<Void>> EventRegistration<Void, EventType> registerAsync(EventPriority, Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public <EventType extends IAsyncEvent<Void>> EventRegistration<Void, EventType> registerAsync(short, Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsync(Class<? super EventType>, KeyType, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsync(EventPriority, Class<? super EventType>, KeyType, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsync(short, Class<? super EventType>, KeyType, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> registerGlobal(Class<? super EventType>, function.Consumer<EventType>);
```

```java
public <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> registerGlobal(EventPriority, Class<? super EventType>, function.Consumer<EventType>);
```

```java
public <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> registerGlobal(short, Class<? super EventType>, function.Consumer<EventType>);
```

```java
public <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsyncGlobal(Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsyncGlobal(EventPriority, Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsyncGlobal(short, Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> registerUnhandled(Class<? super EventType>, function.Consumer<EventType>);
```

```java
public <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> registerUnhandled(EventPriority, Class<? super EventType>, function.Consumer<EventType>);
```

```java
public <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> registerUnhandled(short, Class<? super EventType>, function.Consumer<EventType>);
```

```java
public <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsyncUnhandled(Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsyncUnhandled(EventPriority, Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsyncUnhandled(short, Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public <KeyType, EventType extends IEvent<KeyType>> IEventDispatcher<EventType, EventType> dispatchFor(Class<? super EventType>, KeyType);
```

```java
public <KeyType, EventType extends IAsyncEvent<KeyType>> IEventDispatcher<EventType, concurrent.CompletableFuture<EventType>> dispatchForAsync(Class<? super EventType>, KeyType);
```

---

## EventBusRegistry

**Package:** `com.hypixel.hytale.event`  
**Full Name:** `com.hypixel.hytale.event.EventBusRegistry`  

**Type:** abstract Class

**Extends:** `IBaseEvent<KeyType>,`  

### Public Constructors

```java
public EventBusRegistry(HytaleLogger, Class<EventType>, ConsumerMapType, ConsumerMapType);
```

### Public Methods

```java
public Class<EventType> getEventClass();
```

```java
public boolean isTimeEvents();
```

```java
public void setTimeEvents(boolean);
```

```java
public void shutdown();
```

```java
public boolean isAlive();
```

```java
public abstract EventRegistration<KeyType, EventType> register(short, KeyType, function.Consumer<EventType>);
```

```java
public abstract EventRegistration<KeyType, EventType> registerGlobal(short, function.Consumer<EventType>);
```

```java
public abstract EventRegistration<KeyType, EventType> registerUnhandled(short, function.Consumer<EventType>);
```

```java
public abstract IEventDispatcher<EventType, ?> dispatchFor(KeyType);
```

---

## EventPriority

**Package:** `com.hypixel.hytale.event`  
**Full Name:** `com.hypixel.hytale.event.EventPriority`  

**Type:** final Class

**Extends:** `java.lang.Enum<EventPriority>`  

### Public Fields

```java
public static final EventPriority FIRST;
```

```java
public static final EventPriority EARLY;
```

```java
public static final EventPriority NORMAL;
```

```java
public static final EventPriority LATE;
```

```java
public static final EventPriority LAST;
```

### Public Methods

```java
public static EventPriority[] values();
```

```java
public static EventPriority valueOf(String);
```

```java
public short getValue();
```

---

## EventRegistration

**Package:** `com.hypixel.hytale.event`  
**Full Name:** `com.hypixel.hytale.event.EventRegistration`  

**Type:** Class

**Extends:** `IBaseEvent<KeyType>>`  

### Public Constructors

```java
public EventRegistration(Class<EventType>, function.BooleanSupplier, Runnable);
```

```java
public EventRegistration(EventRegistration<KeyType, EventType>, function.BooleanSupplier, Runnable);
```

### Public Methods

```java
public Class<EventType> getEventClass();
```

```java
public String toString();
```

```java
public static <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> combine(EventRegistration<KeyType, EventType>, EventRegistration<KeyType, EventType>...);
```

---

## IEventRegistry

**Package:** `com.hypixel.hytale.event`  
**Full Name:** `com.hypixel.hytale.event.IEventRegistry`  

**Type:** interface


### Public Methods

```java
public abstract <EventType extends IBaseEvent<Void>> EventRegistration<Void, EventType> register(Class<? super EventType>, function.Consumer<EventType>);
```

```java
public abstract <EventType extends IBaseEvent<Void>> EventRegistration<Void, EventType> register(EventPriority, Class<? super EventType>, function.Consumer<EventType>);
```

```java
public abstract <EventType extends IBaseEvent<Void>> EventRegistration<Void, EventType> register(short, Class<? super EventType>, function.Consumer<EventType>);
```

```java
public abstract <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> register(Class<? super EventType>, KeyType, function.Consumer<EventType>);
```

```java
public abstract <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> register(EventPriority, Class<? super EventType>, KeyType, function.Consumer<EventType>);
```

```java
public abstract <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> register(short, Class<? super EventType>, KeyType, function.Consumer<EventType>);
```

```java
public abstract <EventType extends IAsyncEvent<Void>> EventRegistration<Void, EventType> registerAsync(Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public abstract <EventType extends IAsyncEvent<Void>> EventRegistration<Void, EventType> registerAsync(EventPriority, Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public abstract <EventType extends IAsyncEvent<Void>> EventRegistration<Void, EventType> registerAsync(short, Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public abstract <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsync(Class<? super EventType>, KeyType, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public abstract <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsync(EventPriority, Class<? super EventType>, KeyType, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public abstract <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsync(short, Class<? super EventType>, KeyType, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public abstract <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> registerGlobal(Class<? super EventType>, function.Consumer<EventType>);
```

```java
public abstract <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> registerGlobal(EventPriority, Class<? super EventType>, function.Consumer<EventType>);
```

```java
public abstract <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> registerGlobal(short, Class<? super EventType>, function.Consumer<EventType>);
```

```java
public abstract <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsyncGlobal(Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public abstract <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsyncGlobal(EventPriority, Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public abstract <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsyncGlobal(short, Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public abstract <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> registerUnhandled(Class<? super EventType>, function.Consumer<EventType>);
```

```java
public abstract <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> registerUnhandled(EventPriority, Class<? super EventType>, function.Consumer<EventType>);
```

```java
public abstract <KeyType, EventType extends IBaseEvent<KeyType>> EventRegistration<KeyType, EventType> registerUnhandled(short, Class<? super EventType>, function.Consumer<EventType>);
```

```java
public abstract <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsyncUnhandled(Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public abstract <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsyncUnhandled(EventPriority, Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

```java
public abstract <KeyType, EventType extends IAsyncEvent<KeyType>> EventRegistration<KeyType, EventType> registerAsyncUnhandled(short, Class<? super EventType>, function.Function<concurrent.CompletableFuture<EventType>, concurrent.CompletableFuture<EventType>>);
```

---

## IEventBus

**Package:** `com.hypixel.hytale.event`  
**Full Name:** `com.hypixel.hytale.event.IEventBus`  

**Type:** interface

**Extends:** `IEventRegistry`  

### Public Methods

```java
public default <KeyType, EventType extends IEvent<KeyType>> EventType dispatch(Class<EventType>);
```

```java
public default <EventType extends IAsyncEvent<Void>> concurrent.CompletableFuture<EventType> dispatchAsync(Class<EventType>);
```

```java
public default <KeyType, EventType extends IEvent<KeyType>> IEventDispatcher<EventType, EventType> dispatchFor(Class<? super EventType>);
```

```java
public abstract <KeyType, EventType extends IEvent<KeyType>> IEventDispatcher<EventType, EventType> dispatchFor(Class<? super EventType>, KeyType);
```

```java
public default <KeyType, EventType extends IAsyncEvent<KeyType>> IEventDispatcher<EventType, concurrent.CompletableFuture<EventType>> dispatchForAsync(Class<? super EventType>);
```

```java
public abstract <KeyType, EventType extends IAsyncEvent<KeyType>> IEventDispatcher<EventType, concurrent.CompletableFuture<EventType>> dispatchForAsync(Class<? super EventType>, KeyType);
```

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

## ItemBase

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.ItemBase`  

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
public String model;
```

```java
public float scale;
```

```java
public String texture;
```

```java
public String animation;
```

```java
public String playerAnimationsId;
```

```java
public boolean usePlayerAnimations;
```

```java
public int maxStack;
```

```java
public int reticleIndex;
```

```java
public String icon;
```

```java
public AssetIconProperties iconProperties;
```

```java
public ItemTranslationProperties translationProperties;
```

```java
public int itemLevel;
```

```java
public int qualityIndex;
```

```java
public ItemResourceType[] resourceTypes;
```

```java
public boolean consumable;
```

```java
public boolean variant;
```

```java
public int blockId;
```

```java
public ItemTool tool;
```

```java
public ItemWeapon weapon;
```

```java
public ItemArmor armor;
```

```java
public ItemGlider gliderConfig;
```

```java
public ItemUtility utility;
```

```java
public BlockSelectorToolData blockSelectorTool;
```

```java
public ItemBuilderToolData builderToolData;
```

```java
public ItemEntityConfig itemEntity;
```

```java
public String set;
```

```java
public String[] categories;
```

```java
public ModelParticle[] particles;
```

```java
public ModelParticle[] firstPersonParticles;
```

```java
public ModelTrail[] trails;
```

```java
public ColorLight light;
```

```java
public double durability;
```

```java
public int soundEventIndex;
```

```java
public int itemSoundSetIndex;
```

```java
public InteractionConfiguration interactionConfig;
```

```java
public String droppedItemAnimation;
```

```java
public int[] tagIndexes;
```

```java
public int[] displayEntityStatsHUD;
```

```java
public ItemPullbackConfiguration pullbackConfig;
```

```java
public boolean clipsGeometry;
```

```java
public boolean renderDeployablePreview;
```

### Public Constructors

```java
public ItemBase();
```

```java
public ItemBase(String, String, float, String, String, String, boolean, int, int, String, AssetIconProperties, ItemTranslationProperties, int, int, ItemResourceType[], boolean, boolean, int, ItemTool, ItemWeapon, ItemArmor, ItemGlider, ItemUtility, BlockSelectorToolData, ItemBuilderToolData, ItemEntityConfig, String, String[], ModelParticle[], ModelParticle[], ModelTrail[], ColorLight, double, int, int, Map<InteractionType, Integer>, Map<String, Integer>, InteractionConfiguration, String, int[], Map<Integer, ItemAppearanceCondition[]>, int[], ItemPullbackConfiguration, boolean, boolean);
```

```java
public ItemBase(ItemBase);
```

### Public Methods

```java
public static ItemBase deserialize(netty.ByteBuf, int);
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
public ItemBase clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## ItemLibrary

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.ItemLibrary`  

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
public ItemBase[] items;
```

### Public Constructors

```java
public ItemLibrary();
```

```java
public ItemLibrary(ItemBase[], Map<Integer, String>[]);
```

```java
public ItemLibrary(ItemLibrary);
```

### Public Methods

```java
public static ItemLibrary deserialize(netty.ByteBuf, int);
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
public ItemLibrary clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## ItemCategory

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.ItemCategory`  

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
public String icon;
```

```java
public int order;
```

```java
public ItemGridInfoDisplayMode infoDisplayMode;
```

```java
public ItemCategory[] children;
```

### Public Constructors

```java
public ItemCategory();
```

```java
public ItemCategory(String, String, String, int, ItemGridInfoDisplayMode, ItemCategory[]);
```

```java
public ItemCategory(ItemCategory);
```

### Public Methods

```java
public static ItemCategory deserialize(netty.ByteBuf, int);
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
public ItemCategory clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## ItemQuality

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.ItemQuality`  

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
public String itemTooltipTexture;
```

```java
public String itemTooltipArrowTexture;
```

```java
public String slotTexture;
```

```java
public String blockSlotTexture;
```

```java
public String specialSlotTexture;
```

```java
public Color textColor;
```

```java
public String localizationKey;
```

```java
public boolean visibleQualityLabel;
```

```java
public boolean renderSpecialSlot;
```

```java
public boolean hideFromSearch;
```

### Public Constructors

```java
public ItemQuality();
```

```java
public ItemQuality(String, String, String, String, String, String, Color, String, boolean, boolean, boolean);
```

```java
public ItemQuality(ItemQuality);
```

### Public Methods

```java
public static ItemQuality deserialize(netty.ByteBuf, int);
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
public ItemQuality clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## ItemQuantity

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.ItemQuantity`  

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
public String itemId;
```

```java
public int quantity;
```

### Public Constructors

```java
public ItemQuantity();
```

```java
public ItemQuantity(String, int);
```

```java
public ItemQuantity(ItemQuantity);
```

### Public Methods

```java
public static ItemQuantity deserialize(netty.ByteBuf, int);
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
public ItemQuantity clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## ItemWeapon

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.ItemWeapon`  

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
public int[] entityStatsToClear;
```

```java
public boolean renderDualWielded;
```

### Public Constructors

```java
public ItemWeapon();
```

```java
public ItemWeapon(int[], Map<Integer, Modifier[]>, boolean);
```

```java
public ItemWeapon(ItemWeapon);
```

### Public Methods

```java
public static ItemWeapon deserialize(netty.ByteBuf, int);
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
public ItemWeapon clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## ItemArmor

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.ItemArmor`  

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
public ItemArmorSlot armorSlot;
```

```java
public Cosmetic[] cosmeticsToHide;
```

```java
public double baseDamageResistance;
```

### Public Constructors

```java
public ItemArmor();
```

```java
public ItemArmor(ItemArmorSlot, Cosmetic[], Map<Integer, Modifier[]>, double, Map<String, Modifier[]>, Map<String, Modifier[]>, Map<String, Modifier[]>);
```

```java
public ItemArmor(ItemArmor);
```

### Public Methods

```java
public static ItemArmor deserialize(netty.ByteBuf, int);
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
public ItemArmor clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

---

## ItemTool

**Package:** `com.hypixel.hytale.protocol`  
**Full Name:** `com.hypixel.hytale.protocol.ItemTool`  

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
public ItemToolSpec[] specs;
```

```java
public float speed;
```

### Public Constructors

```java
public ItemTool();
```

```java
public ItemTool(ItemToolSpec[], float);
```

```java
public ItemTool(ItemTool);
```

### Public Methods

```java
public static ItemTool deserialize(netty.ByteBuf, int);
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
public ItemTool clone();
```

```java
public boolean equals(Object);
```

```java
public int hashCode();
```

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


