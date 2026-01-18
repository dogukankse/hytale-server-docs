# Getting Started

Welcome to the Hytale Server API! This section will help you get up and running with plugin development quickly.

## What You'll Learn

- How to set up your development environment
- Basic plugin structure and lifecycle
- Core concepts like events, components, and assets

## Prerequisites

Before you begin, make sure you have:

1. **Java Development Kit (JDK)** - Version 17 or higher recommended
2. **IDE** - IntelliJ IDEA recommended for best decompilation support
3. **HytaleServer.jar** - The server JAR file for dependencies
4. **Build Tool** - Gradle or Maven for dependency management

## Quick Links

- [Quick Start Guide](quick-start.md) - Get started in minutes
- [Plugin Basics](../guides/plugin-basics.md) - Detailed plugin structure
- [Event System](../guides/event-system.md) - Hook into game events

## Project Setup

### Adding HytaleServer.jar as Dependency

**Gradle (build.gradle.kts):**
```kotlin
dependencies {
    compileOnly(files("path/to/HytaleServer.jar"))
}
```

**Maven (pom.xml):**
```xml
<dependency>
    <groupId>com.hypixel</groupId>
    <artifactId>hytale-server</artifactId>
    <version>1.0</version>
    <scope>system</scope>
    <systemPath>${project.basedir}/libs/HytaleServer.jar</systemPath>
</dependency>
```

### Decompiling the JAR

For detailed method signatures and implementations:

**Using IntelliJ IDEA (recommended):**
1. Right-click on `HytaleServer.jar`
2. Select "Add as Library"
3. Browse the decompiled source code

**Using JD-GUI:**
1. Download from http://java-decompiler.github.io/
2. Open `HytaleServer.jar` in JD-GUI
3. Export source if needed

## Next Steps

Ready to dive in? Head to the [Quick Start Guide](quick-start.md) to create your first plugin!
