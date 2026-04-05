# MavonEngine - The Three.js Game Engine for Single / Multiplayer Browser Games

MavonEngine is a full-stack **Three.js game engine** purpose-built for single player or real-time multiplayer.
Most browser game engines treat networking as an add-on. MavonEngine ships with it built in —
rendering, physics, networking, animation, particles, and debugging in one cohesive TypeScript package.

🌐 **[mavonengine.com](https://mavonengine.com)** · 📖 [Docs](https://mavonengine.com/getting-started) · 💬 [Community](https://mavonengine.com/community) · 🎮 [Live Demo](https://mavonengine.com/demo)

---

## Why MavonEngine?

Most multiplayer browser games are held together with duct tape — a rendering library here,
a physics library there, a networking layer bolted on top. MavonEngine is different.

- **Server-Authoritative Architecture** — The server runs a simplified hitbox scene alongside
  the client's full 3D world. Real hit detection, raycasting, and spatial queries. No client trust.
- **Three.js Rendering** — Full Three.js access with custom GLSL shader support, debug rendering
  modes, and WebGPU-ready rendering pipeline.
- **Integrated Rapier Physics** — Kinematic character controller, slope climbing, configurable
  colliders, and real-time physics debug visualization.
- **WebRTC Networking Built In** — Real-time data channels, automatic state sync, distance-based
  entity culling, and bandwidth monitoring. None of it bolted on.
- **Write Once, Run Everywhere** — Shared entity system runs on both server and client.
  No duplication. No drift.
- **Full TypeScript** — Comprehensive types, Tweakpane integration, and performance monitoring
  so you catch bugs fast and ship faster.

---

## What Can You Build?

MavonEngine is purpose-built for anything that needs players, physics, and a world in the browser:

| Game Type | What MavonEngine Provides |
|---|---|
| Action RPGs | Server-auth combat, skeletal animation, open world entity culling |
| PvP Combat | Cheat-resistant hit detection, real-time sync, low-latency WebRTC |
| Physics Games | Rapier integration, kinematic controllers, debug visualization |
| Open World | Distance-based culling, prefab system, level editor |

---

## Packages

| Package | Description |
|---|---|
| [`@mavonengine/core`](https://github.com/MavonEngine/Core) | Engine core — rendering, physics, networking, animation |

---

## Quick Start
```bash
npx @mavonengine/create-bootstrap
```

```ts
import { MavonServer, MavonClient, Entity } from '@mavonengine/core'

const server = new MavonServer()

server.onPlayerJoin((player) => {
  const entity = new Entity({ position: [0, 1, 0] })
  server.world.add(entity)
  server.sync(player, entity)
})

server.start(3000)
```

Full documentation at **[mavonengine.com/getting-started](https://mavonengine.com/getting-started)**

---

## Community & Resources

- 💬 [Community Forum](https://mavonengine.com/community)
- 🧱 [Prefab Registry](https://mavonengine.com/prefabs) — drop-in grass, water, and more
- 🐛 [Report a Bug](https://github.com/MavonEngine/Core/issues)
- ⭐ Star the repo if MavonEngine saves you from assembling the stack yourself

---

## License

MavonEngine is open source. See [LICENSE](https://github.com/MavonEngine/Core/blob/main/LICENSE) for details.

---

<p align="center">
  Built with TypeScript · Three.js · Rapier · WebRTC<br/>
  <a href="https://mavonengine.com">mavonengine.com</a>
</p>
