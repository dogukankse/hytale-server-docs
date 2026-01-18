# Plugin Basics

This guide covers the fundamentals of Hytale plugin development, including project structure, plugin lifecycle, and manifest configuration.

---

## Plugin Entry Point

Your plugin should extend the base plugin class and implement the lifecycle methods.

**Key Classes:**
- `com.hypixel.hytale.plugin.*` - Plugin system

**Core Plugin Classes:**
- `EarlyPluginLoader` - Early loading
- `ClassTransformer` - Bytecode transformation
- `TransformingClassLoader` - Custom classloader

---

## Plugin Lifecycle

```
Load → Enable → Running → Disable → Unload
```

### Lifecycle Phases

1. **Load** - Plugin JAR is loaded, classes initialized
2. **Enable** - Plugin is activated, register events and commands
3. **Running** - Plugin is active and processing events
4. **Disable** - Cleanup before unload
5. **Unload** - Plugin is removed from memory

---

## Project Structure

```
MyPlugin/
├── src/main/java/com/example/myplugin/
│   ├── MyPlugin.java              # Main plugin class
│   ├── listeners/
│   │   └── EventListener.java     # Event handlers
│   ├── commands/
│   │   └── MyCommand.java         # Custom commands
│   ├── components/
│   │   └── CustomComponent.java   # ECS components
│   └── systems/
│       └── CustomSystem.java      # ECS systems
├── src/main/resources/
│   ├── manifest.json               # Plugin manifest
│   └── assets/                     # Custom assets
├── build.gradle.kts                # Gradle build file
└── settings.gradle.kts             # Gradle settings
```

---

## Plugin Manifest

The `manifest.json` file describes your plugin to the server.

```json
{
  "id": "my-plugin",
  "name": "My Plugin",
  "version": "1.0.0",
  "description": "A description of my plugin",
  "author": "Your Name",
  "main": "com.example.myplugin.MyPlugin",
  "dependencies": [],
  "softDependencies": []
}
```

### Manifest Fields

| Field | Required | Description |
|-------|----------|-------------|
| `id` | Yes | Unique plugin identifier (lowercase, no spaces) |
| `name` | Yes | Display name of the plugin |
| `version` | Yes | Semantic version (e.g., 1.0.0) |
| `description` | No | Brief description |
| `author` | No | Plugin author name |
| `main` | Yes | Fully qualified main class name |
| `dependencies` | No | Required plugin dependencies |
| `softDependencies` | No | Optional plugin dependencies |

---

## Build Configuration

### Gradle (build.gradle.kts)

```kotlin
plugins {
    java
}

group = "com.example"
version = "1.0.0"

java {
    sourceCompatibility = JavaVersion.VERSION_17
    targetCompatibility = JavaVersion.VERSION_17
}

repositories {
    mavenCentral()
}

dependencies {
    compileOnly(files("path/to/HytaleServer.jar"))
}

tasks.jar {
    archiveBaseName.set("my-plugin")
    
    from(sourceSets.main.get().output)
    
    manifest {
        attributes(
            "Implementation-Title" to project.name,
            "Implementation-Version" to project.version
        )
    }
}
```

---

## Main Plugin Class

```java
package com.example.myplugin;

// Import plugin system classes
// import com.hypixel.hytale.plugin.*;
// import com.hypixel.hytale.event.*;

public class MyPlugin {
    
    private EventRegistry eventRegistry;
    
    /**
     * Called when the plugin is loaded
     */
    public void onLoad() {
        // Initialize plugin
    }
    
    /**
     * Called when the plugin is enabled
     */
    public void onEnable() {
        // Register events
        registerEvents();
        
        // Register commands
        registerCommands();
        
        // Load assets
        loadAssets();
    }
    
    /**
     * Called when the plugin is disabled
     */
    public void onDisable() {
        // Cleanup resources
    }
    
    private void registerEvents() {
        // Register event listeners
        // eventRegistry.register(SomeEvent.class, this::handleEvent);
    }
    
    private void registerCommands() {
        // Register custom commands
    }
    
    private void loadAssets() {
        // Load custom assets
    }
}
```

---

## Best Practices

### Do's
- ✅ Use meaningful plugin IDs (lowercase, hyphenated)
- ✅ Follow semantic versioning
- ✅ Cleanup resources in `onDisable()`
- ✅ Handle exceptions gracefully
- ✅ Use the logging system for debug output

### Don'ts
- ❌ Don't block the main thread
- ❌ Don't access internal APIs (*.internal.* packages)
- ❌ Don't hardcode file paths
- ❌ Don't ignore exceptions

---

## See Also

- [Event System](event-system.md) - Register and handle events
- [Asset System](asset-system.md) - Load custom assets
- [Quick Start Guide](../getting-started/quick-start.md) - Complete quick start
