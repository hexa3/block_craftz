# block_craftz

A voxel sandbox engine for the browser, built from scratch in TypeScript — deterministic world generation, chunk streaming, greedy meshing, an entity component system, voxel physics, lighting, inventory, and multiplayer foundations running in a single real-time gameplay loop.

![Status](https://img.shields.io/badge/status-work%20in%20progress-orange)
![TypeScript](https://img.shields.io/badge/TypeScript-5.4-blue?logo=typescript&logoColor=white)
![three.js](https://img.shields.io/badge/three.js-0.165-black?logo=threedotjs&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

<!-- TODO(you): add one in-game screenshot here (npm run dev → capture terrain view), e.g. docs/screenshot.png:
![Gameplay](docs/screenshot.png)
-->

## Features

- Deterministic procedural world generation with biomes
- Chunk streaming and greedy-meshed rendering via WebGL (three.js)
- Entity Component System architecture across 25+ engine modules
- Voxel physics: collision, gravity, block interaction
- Lighting propagation and fluid simulation groundwork
- Inventory, crafting recipes, items, and basic mob AI
- Networking foundations for future multiplayer
- Vitest test suite and a built-in benchmark harness

## Tech stack

TypeScript · three.js/WebGL · Vite · Vitest · ESLint/Prettier

## How it works

The engine (`engine/`) is a layered ECS: a task scheduler drives world generation → chunk meshing → render graph each frame, while physics and lighting run as decoupled systems over shared voxel storage. The game layer (`game/`) defines blocks, biomes, recipes, and entities as data-driven content on top of the engine core. `src/main.ts` boots the loop; `index.html` is the only host page.

## Usage

```bash
npm install
npm run dev        # play at http://127.0.0.1:5173
npm test           # run the engine test suite
npm run benchmark  # meshing / world-gen performance harness
npm run build      # typecheck + production bundle
```

## Status

Actively developed solo project — the engine core and gameplay loop work today; multiplayer and fluids are foundational, not finished.

Part of a robotics & simulation series with [torque](https://github.com/hexa3/torque), [helios](https://github.com/hexa3/helios), and [drag_sim](https://github.com/hexa3/drag_sim).

## License

[MIT](LICENSE)

---

<p align="center">Built by <a href="https://sheheryar.xyz">Sheheryar</a> · <a href="https://github.com/hexa3">github.com/hexa3</a></p>
