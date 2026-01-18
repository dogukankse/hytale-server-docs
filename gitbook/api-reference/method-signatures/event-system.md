# Event System

Event handling and dispatching classes from `com.hypixel.hytale.event` package.

**Classes:** 12

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

