# Best Practices

Recommended patterns and practices for Hytale plugin development.

---

## Plugin Development

### Do's ✅

1. **Use meaningful plugin IDs**
   - Lowercase, hyphenated names
   - Example: `my-awesome-plugin`

2. **Follow semantic versioning**
   - Format: `MAJOR.MINOR.PATCH`
   - Example: `1.0.0`, `1.2.3`

3. **Cleanup resources in `onDisable()`**
   - Unregister events
   - Close connections
   - Save data

4. **Handle exceptions gracefully**
   - Catch and log errors
   - Don't crash the server

5. **Use the logging system**
   - `HytaleLogger` for debug output
   - Avoid `System.out.println()`

### Don'ts ❌

1. **Don't block the main thread**
   - Use async for heavy operations
   - Use async event handlers when possible

2. **Don't access internal APIs**
   - Avoid `*.internal.*` packages
   - They may change without notice

3. **Don't hardcode file paths**
   - Use plugin data directories
   - Use relative paths

4. **Don't ignore exceptions**
   - Always catch potential errors
   - Log them appropriately

---

## Event System

### Priority Guidelines

| Priority | Use Case |
|----------|----------|
| `FIRST` | State initialization, logging |
| `EARLY` | Early modifications |
| `NORMAL` | Standard event handling (default) |
| `LATE` | React to other handlers' changes |
| `LAST` | Final modifications, cleanup |

### Best Practices

1. **Choose the right priority**
   - Use `NORMAL` unless you need specific ordering

2. **Check cancelled state**
   - Respect other handlers' cancellations
   ```java
   if (event.isCancelled()) return;
   ```

3. **Use async for heavy work**
   - Don't block the main thread

4. **Unregister when done**
   - Clean up listeners in `onDisable()`

---

## Entity Component System (ECS)

### Component Design

1. **Keep components data-only**
   - No logic in components
   - Components are just data containers

2. **Small, focused components**
   - One responsibility per component
   - Compose complex entities from simple parts

3. **Use archetypes**
   - Template common entity types
   - Reduces setup code

### System Design

1. **Single responsibility**
   - Each system handles one aspect

2. **Minimal dependencies**
   - Systems should be independent

3. **Batch operations**
   - Use `CommandBuffer` for bulk changes

---

## Performance

### General Tips

1. **Cache frequently-accessed data**
   - Don't query repeatedly
   - Store references

2. **Use metrics for profiling**
   - `MetricsRegistry` for monitoring
   - Identify bottlenecks

3. **Batch operations**
   - Group similar operations
   - Reduce overhead

4. **Limit particle count**
   - Too many particles hurt performance
   - Consider draw distance

### Event Performance

1. **Avoid high-frequency logging**
   - Log sparingly in tick events
   - Use debug flags

2. **Early return when possible**
   - Check conditions first
   ```java
   if (!condition) return;
   ```

---

## Asset Management

1. **Organize by type**
   - Group assets in subdirectories
   - `/assets/blocks/`, `/assets/items/`

2. **Use meaningful IDs**
   - Prefix with your plugin ID
   - Example: `my_plugin:my_block`

3. **Handle missing assets**
   - Check if assets exist before use
   - Provide fallbacks

4. **Cleanup on disable**
   - Unregister assets when plugin disables

---

## Code Organization

### Recommended Structure

```
src/main/java/com/example/myplugin/
├── MyPlugin.java           # Main plugin class
├── listeners/              # Event handlers
├── commands/               # Command implementations
├── components/             # ECS components
├── systems/                # ECS systems
├── util/                   # Utility classes
└── config/                 # Configuration handling
```

### Naming Conventions

| Type | Convention | Example |
|------|------------|---------|
| Classes | PascalCase | `MyPlugin` |
| Methods | camelCase | `handleEvent` |
| Constants | UPPER_SNAKE | `MAX_HEALTH` |
| Packages | lowercase | `com.example` |

---

## Error Handling

### Logging Levels

```java
logger.debug("Debug information");
logger.info("General information");
logger.warn("Warning - something unusual");
logger.error("Error - something failed");
```

### Exception Handling

```java
try {
    // Risky operation
} catch (SpecificException e) {
    logger.error("Operation failed: " + e.getMessage());
    // Handle gracefully
} catch (Exception e) {
    logger.error("Unexpected error", e);
    // Fallback behavior
}
```

---

## Configuration

1. **Use YAML or JSON**
   - Human-readable
   - Easy to edit

2. **Provide defaults**
   - Don't require configuration
   - Work out of the box

3. **Validate input**
   - Check config values
   - Use sensible limits

4. **Reload support**
   - Allow config reload without restart

---

## Testing

1. **Test in development server**
   - Isolated environment
   - Safe to experiment

2. **Test edge cases**
   - Null values
   - Empty collections
   - Extreme values

3. **Test with multiple plugins**
   - Ensure compatibility
   - Test event ordering

---

## Documentation

1. **Comment your code**
   - Explain why, not what
   - Document public APIs

2. **Provide examples**
   - Show common usage
   - Include in README

3. **Version your API**
   - Document breaking changes
   - Use semantic versioning

---

## See Also

- [Plugin Basics](../guides/plugin-basics.md)
- [Event System](../guides/event-system.md)
- [Entity System](../guides/entity-system.md)
