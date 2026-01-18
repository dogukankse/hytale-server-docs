# Appendix

Supplementary information and reference materials.

## Contents

- [Documentation Summary](documentation-summary.md) - How this documentation was generated
- [Best Practices](best-practices.md) - Development best practices

## Additional Resources

### Class Lists

The following text files contain complete class listings:

- `all-classes.txt` - Complete list of all 16,249 classes
- `hytale-classes.txt` - Filtered list of 5,218 Hytale API classes
- `protocol-classes.txt` - All protocol classes (733 classes)
- `package-summary.txt` - Package grouping with class counts
- `packages-list.txt` - Clean package list with counts

### Tools

**Decompilation:**
- IntelliJ IDEA - Best for browsing and decompilation
- JD-GUI - Standalone Java decompiler
- Fernflower - Command-line decompiler

**Search:**
```powershell
# Search for specific class
Get-Content hytale-classes.txt | Select-String "BlockType"

# Find all classes in a package
Get-Content hytale-classes.txt | Select-String "\.component\."

# Count classes in a package
Get-Content hytale-classes.txt | Select-String "\.protocol\." | Measure-Object
```

---

## Quick Reference

### Essential Packages

| Package | Purpose |
|---------|---------|
| `plugin.*` | Plugin lifecycle |
| `event.*` | Event handling |
| `assetstore.*` | Asset management |
| `component.*` | ECS for entities |
| `protocol.*` | Data structures |

### Common Patterns

**Register event:**
```java
eventRegistry.register(SomeEvent.class, this::handleEvent);
```

**Register component:**
```java
componentRegistry.register(CustomComponent.class);
```

**Register asset:**
```java
assetStore.register(myAsset);
```

---

## Version Information

- **Generated From**: HytaleServer.jar
- **Generation Date**: January 19, 2026
- **Total Classes**: 16,249
- **Hytale API Classes**: 5,218
- **Method Signatures**: 96 classes documented
