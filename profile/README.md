<div align="Center">
⚡ PulseMC: The Heartbeat of High-Performance Networking
</div>

Welcome to **PulseMC**, an ecosystem dedicated to redefining how Minecraft communicates. We build low-level networking optimizations designed for high-load environments, competitive play, and massive player counts.

[🌐 Website](https://pulsemc.dev) • [💬 Discord](https://discord.gg/GKR7jtpsNa) • [📖 Documentation](https://docs.pulsemc.dev)

---

## 🚀 What is Pulse?

Pulse is not just another server fork. It is a vertically integrated networking suite that replaces the "spammy" vanilla protocol with a sophisticated **Smart Batching** system. 

By grouping thousands of small packets into single, compressed "pulses," we drastically reduce CPU syscall overhead, lower network PPS (Packets Per Second), and provide a smoother experience for players.

### ⚙️ Core Innovations

*   **Logical Batching:** Instead of sending packets instantly, Pulse buffers them within the game tick, flushing a single "Super-Packet" after the logic execution.
*   **Hybrid Protocol:** 
    *   **Vanilla Fallback:** Uses standard `ClientboundBundlePacket` for unmodded players (1.19.4+).
    *   **Pulse Protocol:** Uses custom high-density bulk packets for players using the **Pulse-Fabric** mod.
*   **Zero-Break Compatibility:** Our unique event emulation layer ensures that your existing Paper/Spigot plugins (ProtocolLib, Denizen, AntiCheats) work out of the box.
*   **Smart Throttling:** Prioritizes critical data (combat/hits) for instant delivery while "pulsing" non-urgent data (particles/sound/far-away entities).
*   **Chunk-Based Explosions:** Automatically switches from individual block updates to chunk-section updates during massive explosions to prevent client and network lag.

## 📈 Why Pulse?

*   **Up to 40% reduction** in network-related CPU usage.
*   **Up to 70% reduction** in Packet-Per-Second count.
*   **Rock-solid 20 TPS** even during massive entity spawns or TNT explosions.
*   **Seamless Integration:** No mandatory mods required, but rewarding for those who use them.

---

## 📫 Get in Touch

We are always looking for talented Java developers experienced with **Netty**, **NMS**, and low-level optimization. If you want to help us push the boundaries of what Minecraft can handle, join our Discord or open a Pull Request.

**PulseMC: Optimizing the flow of the game, one pulse at a time.**

---
© 2024 PulseMC Team • [pulsemc.dev](https://pulsemc.dev)
