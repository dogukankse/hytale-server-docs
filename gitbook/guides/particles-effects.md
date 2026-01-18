# Particles & Visual Effects

The Particle System handles visual effects like particles, model effects, and camera effects.

---

## Overview

**Key Packages:**
- `com.hypixel.hytale.protocol.*` - Particle protocol classes

---

## Particle Protocol Classes

### Particle
Base particle definition.

### ParticleSystem
Manages particle behavior and lifecycle.

### ParticleSpawner
Controls particle emission.

Properties:
- Emission rate
- Spawn position
- Initial velocity
- Lifetime

### ParticleSpawnerGroup
Groups multiple spawners together.

### ParticleCollision
Particle physics and collision.

### ParticleAttractor
Attracts particles to a point.

---

## Particle Types

### WorldParticle
Particles in world space.

Use cases:
- Environmental effects
- Block interactions
- Weather

### ModelParticle
Particles attached to models.

Use cases:
- Entity effects
- Weapon trails
- Auras

### FluidParticle
Particles for fluid effects.

Use cases:
- Water splashes
- Lava drips
- Rain

### BlockParticleSet
Particles from blocks.

Use cases:
- Block breaking
- Block placement
- Mining

---

## Creating Particles

### Simple Particle

```java
// Spawn particles at position
ParticleSpawner spawner = new ParticleSpawner();
spawner.setParticleType(ParticleType.SMOKE);
spawner.setPosition(x, y, z);
spawner.setCount(10);
spawner.spawn();
```

### Particle with Velocity

```java
ParticleSpawner spawner = new ParticleSpawner();
spawner.setParticleType(ParticleType.SPARK);
spawner.setPosition(x, y, z);
spawner.setVelocity(vx, vy, vz);
spawner.setSpread(0.5f);
spawner.spawn();
```

### Continuous Emission

```java
ParticleSpawner spawner = new ParticleSpawner();
spawner.setParticleType(ParticleType.FLAME);
spawner.setPosition(x, y, z);
spawner.setEmissionRate(10); // per second
spawner.setDuration(5.0f);   // seconds
spawner.start();
```

---

## Camera Effects

### CameraSettings
Camera configuration.

### CameraInteraction
Camera control interactions.

### CameraShake
Screen shake effects.

```java
// Trigger camera shake
CameraShake shake = new CameraShake();
shake.setIntensity(0.5f);
shake.setDuration(0.3f);
player.applyCameraEffect(shake);
```

### CameraNode
Camera positions for cutscenes.

### CameraPerspectiveType
First/third person modes.

---

## Model VFX

### ModelVFX
Visual effects on models.

### ModelTexture
Dynamic textures on models.

### ModelTransform
Model transformations.

---

## Animation System

### Animation
Animation definitions.

### AnimationSet
Collections of animations.

### AnimationSlot
Slots for playing animations.

---

## Entity Effects

### EntityEffect
Visual/audio effects on entities.

```java
// Apply effect to entity
EntityEffect effect = new EntityEffect();
effect.setType(EntityEffectType.GLOW);
effect.setDuration(5.0f);
entity.addEffect(effect);
```

---

## Ambience Effects

Located in `com.hypixel.hytale.builtin.ambience` (10 classes)

### AmbienceFX
Ambient effects.

### Protocol Classes

```java
protocol.AmbienceFX        // Effect definition
protocol.AmbienceFXSound   // Ambient sounds
protocol.AmbienceFXMusic   // Background music
```

---

## Best Practices

1. **Limit particle count** - Too many particles hurt performance
2. **Use spawner groups** - Combine related effects
3. **Consider draw distance** - Don't spawn far particles
4. **Use world particles sparingly** - They're more expensive
5. **Test performance** - Profile particle-heavy scenes

---

## See Also

- [Audio System](audio-system.md) - Sound effects
- [Entity System](entity-system.md) - Entity effects
- [Block System](block-system.md) - Block particles
- [API Reference](../api-reference/packages.md) - Package details
</Parameter>
<parameter name="Complexity">3
