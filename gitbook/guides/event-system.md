# Event System

The Event System is the primary way to hook into game events and react to player actions, world changes, and server events.

---

## Overview

**Key Packages:**
- `com.hypixel.hytale.event.*` - Core event system (15 classes)
- `com.hypixel.hytale.server.event.*` - Server events

**Core Classes:**
- `EventRegistry` - Register event listeners
- `EventBus` - Event dispatching
- `IEvent` - Base event interface
- `ICancellable` - Cancellable events
- `EventPriority` - Event priority levels

---

## Event Interfaces

### IEvent
Base interface for synchronous events.

```java
public interface IEvent<KeyType> extends IBaseEvent<KeyType> {
    // Marker interface
}
```

### IAsyncEvent
Interface for asynchronous events.

```java
public interface IAsyncEvent<KeyType> extends IBaseEvent<KeyType> {
    // Marker interface
}
```

### ICancellable
Interface for events that can be cancelled.

```java
public interface ICancellable {
    boolean isCancelled();
    void setCancelled(boolean cancelled);
}
```

### IProcessedEvent
Interface for events that need post-processing.

```java
public interface IProcessedEvent {
    void processEvent(String context);
}
```

---

## Event Priority

Events are processed in priority order. Use `EventPriority` to control when your listener is called.

```java
public enum EventPriority {
    FIRST,    // Called first, can set up state
    EARLY,    // Called early, before most handlers
    NORMAL,   // Default priority
    LATE,     // Called late, after most handlers
    LAST      // Called last, for cleanup/final decisions
}
```

### Priority Guidelines

| Priority | Use Case |
|----------|----------|
| `FIRST` | State initialization, logging |
| `EARLY` | Early modifications |
| `NORMAL` | Standard event handling |
| `LATE` | React to other handlers' changes |
| `LAST` | Final modifications, cleanup |

---

## Registering Event Listeners

### Basic Registration

```java
// Simple registration (NORMAL priority)
eventRegistry.register(SomeEvent.class, this::handleEvent);

private void handleEvent(SomeEvent event) {
    // Handle the event
}
```

### With Priority

```java
// Register with specific priority
eventRegistry.register(EventPriority.EARLY, SomeEvent.class, this::handleEvent);

// Or using numeric priority
eventRegistry.register((short) 100, SomeEvent.class, this::handleEvent);
```

### With Key

Events can be scoped to specific keys:

```java
// Register for specific key
eventRegistry.register(SomeEvent.class, myKey, this::handleEvent);

// With priority and key
eventRegistry.register(EventPriority.NORMAL, SomeEvent.class, myKey, this::handleEvent);
```

---

## Async Event Registration

For asynchronous events that return `CompletableFuture`:

```java
// Register async handler
eventRegistry.registerAsync(SomeAsyncEvent.class, this::handleAsyncEvent);

private CompletableFuture<SomeAsyncEvent> handleAsyncEvent(
    CompletableFuture<SomeAsyncEvent> eventFuture
) {
    return eventFuture.thenApply(event -> {
        // Handle the event asynchronously
        return event;
    });
}
```

---

## Global Event Registration

Register handlers that receive ALL events of a type, regardless of key:

```java
// Register global handler
eventRegistry.registerGlobal(SomeEvent.class, this::handleAllEvents);

// With priority
eventRegistry.registerGlobal(EventPriority.FIRST, SomeEvent.class, this::handleAllEvents);
```

---

## Unhandled Event Registration

Register handlers for events that no keyed handler processed:

```java
// Register unhandled handler
eventRegistry.registerUnhandled(SomeEvent.class, this::handleUnhandledEvent);
```

---

## EventBus

The `EventBus` is the central hub for event dispatching.

### Getting Registries

```java
// Get registry for event type
EventBusRegistry<?, ?, ?> registry = eventBus.getRegistry(SomeEvent.class);

// Get sync registry
EventBusRegistry<?, ?, ?> syncRegistry = eventBus.getSyncRegistry(SomeEvent.class);
```

### Dispatching Events

```java
// Dispatch sync event
eventBus.dispatchFor(SomeEvent.class, key).dispatch(event);

// Dispatch async event
eventBus.dispatchForAsync(SomeAsyncEvent.class, key).dispatch(event);
```

---

## Common Events

### Asset Events
- `AssetPackRegisterEvent` - Asset pack registration
- `AssetPackUnregisterEvent` - Asset pack removal
- `LoadAssetEvent` - Asset loading
- `GenerateSchemaEvent` - Schema generation

### Looking for Events

Search for event classes in:
```
com.hypixel.hytale.server.core.asset.*Event
com.hypixel.hytale.server.event.*
com.hypixel.hytale.*.event.*
```

---

## Cancelling Events

For cancellable events:

```java
private void handleEvent(SomeCancellableEvent event) {
    if (shouldCancel(event)) {
        event.setCancelled(true);
    }
}
```

**Note:** Check if the event is already cancelled by earlier handlers:

```java
private void handleEvent(SomeCancellableEvent event) {
    if (event.isCancelled()) {
        return; // Event already cancelled
    }
    
    // Your logic here
}
```

---

## Best Practices

1. **Choose the right priority** - Use `NORMAL` unless you need specific ordering
2. **Check cancelled state** - Respect other handlers' cancellations
3. **Use async for heavy work** - Don't block the main thread
4. **Unregister when done** - Clean up listeners in `onDisable()`
5. **Log sparingly** - Avoid logging in high-frequency events

---

## See Also

- [Plugin Basics](plugin-basics.md) - Plugin structure and lifecycle
- [Method Signatures](../api-reference/method-signatures.md) - Event class details
- [Quick Start Guide](../getting-started/quick-start.md) - Getting started
