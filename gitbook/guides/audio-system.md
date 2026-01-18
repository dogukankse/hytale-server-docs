# Audio System

The Audio System handles sounds, music, and ambient audio.

---

## Overview

**Key Packages:**
- `com.hypixel.hytale.protocol.*` - Audio protocol classes

---

## Protocol Classes

### SoundEvent
Sound definitions.

### SoundCategory
Categories for audio.

### AudioCategory
Audio category configuration.

### AmbienceFX
Ambient sound effects.

### AmbienceFXSound
Ambient sound playback.

### AmbienceFXMusic
Background music.

---

## Sound Sets

### BlockSoundSet
Sounds for block interactions.

Events:
- Place
- Break
- Step
- Hit

### ItemSoundSet
Sounds for item interactions.

Events:
- Equip
- Use
- Drop

---

## Sound Categories

Categories for volume control:
- Master
- Music
- Effects
- Ambient
- Voice
- UI

---

## Playing Sounds

### At Position

```java
// Play sound at world position
world.playSound(x, y, z, soundEvent, category);
```

### For Player

```java
// Play sound for specific player
player.playSound(soundEvent, category);
```

### With Parameters

```java
// Play with volume and pitch
world.playSound(x, y, z, soundEvent, category, volume, pitch);
```

---

## Ambient Audio

### Location-based Ambience

```java
// Configure ambient zone
AmbienceFX ambience = new AmbienceFX();
ambience.setSound(ambienceSound);
ambience.setRadius(50.0f);
ambience.setVolume(0.5f);
```

### Biome-based Music

```java
// Music changes based on biome
AmbienceFXMusic music = new AmbienceFXMusic();
music.setTrack(musicTrack);
music.setBiome(biomeId);
```

---

## 3D Audio

### Distance Attenuation

```java
// Sound gets quieter with distance
soundEvent.setMaxDistance(50.0f);
soundEvent.setAttenuation(AttenuationType.LINEAR);
```

### Doppler Effect

```java
// Sound pitch changes with velocity
soundEvent.setDopplerEnabled(true);
```

---

## Sound Events

### Registering Sounds

```java
// Register custom sound
SoundEvent mySound = new SoundEvent("my_plugin:my_sound");
assetStore.register(mySoundAsset);
```

### Sound Asset

```json
{
  "type": "sound",
  "id": "my_plugin:my_sound",
  "file": "sounds/my_sound.ogg",
  "category": "effects",
  "volume": 1.0,
  "pitch": 1.0
}
```

---

## Best Practices

1. **Use appropriate categories** - Respect user volume settings
2. **Consider 3D positioning** - Use world position for effects
3. **Limit simultaneous sounds** - Avoid audio clutter
4. **Use sound pools** - Vary similar sounds
5. **Optimize file sizes** - Use appropriate audio formats

### Audio Formats

Recommended formats:
- `.ogg` - Best for most sounds
- `.wav` - Uncompressed, larger files

---

## See Also

- [Particles & Effects](particles-effects.md) - Visual effects
- [Asset System](asset-system.md) - Sound assets
- [Built-in Systems](builtin-systems.md) - Ambience system
- [API Reference](../api-reference/packages.md) - Package details
