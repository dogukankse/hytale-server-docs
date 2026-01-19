# Frequently Asked Questions

## Client & Server Architecture
**Can the client be modded?**
No, Hytale adheres to a "One Community, One Client" philosophy. The client cannot be effectively modded directly. Instead, the server sends all necessary data (models, textures, UI) to the client upon connection. This ensures security and a consistent experience for all players.

## Network & Technical
**What protocol does Hytale use?**
Hytale uses **QUIC** (Quick UDP Internet Connections). This hybrid protocol builds on UDP to provide low-latency communication (essential for gaming) while adding reliability features similar to TCP.

**What are Transfer Packets?**
Transfer packets are small data payloads (limit 4KB) that allow players to move seamlessly between servers (e.g., from a lobby to a minigame server) while carrying essential data. They preserve player state but are **not** a full proxy solution like BungeeCord.

## Server Infrastructure
**Will Hytale support dedicated servers?**
Yes! Hytale supports self-hosted dedicated servers on Linux and Windows. You can run your own community server without relying on official hosting.
