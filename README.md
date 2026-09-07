# GAME LAB

Interactive engineering laboratory with one shared runtime and thirteen plug-in engines.

## Engines

1. Cyber Chess AI — adversarial-search prototype
2. Connect 4 — Alpha-Beta demonstrator
3. SQL Dungeon — deterministic constrained query parser
4. Network Defender — DPI/ACL simulator
5. Packet Rush — TCP state-machine visualizer
6. API Outbreak — token-bucket rate limiter
7. DevOps Pipeline — staged pipeline simulator
8. Memory Matrix — LRU cache simulator
9. Regex Vault — pattern validation challenge
10. Evidence Quest — weighted multi-criteria prototype
11. Shape Forge — mini-game for learning geometry by assembling target figures
12. Shape Swarm — emergent particle geometry forming a cat and a tree
13. Mini-kryssord — intersecting Norwegian knowledge crossword

Every engine exposes the same lifecycle shape through `constructor`, `init()` and `destroy()` and sends metrics through the runtime telemetry bridge.

## Security

Client input is handled without `eval()`/`Function()` execution. Runtime telemetry is rendered with DOM text nodes, and the app ships with a restrictive static CSP.

## Local

```powershell
npm install
npm test
npm run build
npm run dev
```

Open `http://localhost:4173`.

### Shape Forge

A dependency-free mini-game that uses triangles, squares, rectangles and circles to teach basic geometric properties. The shape artwork is stored as an SVG asset in `assets/shape-forge.svg`.

### Shape Swarm

A generative geometry mini-game where a swarm of triangles, circles and squares morphs into a cat and a tree. The exercise demonstrates emergent visual patterns and abstraction.

### Mini-kryssord

A compact Norwegian knowledge crossword with intersecting across/down entries about geometry, evidence, circuits and nature. The puzzle is original to this repository and runs without external services.

## Quality gate

The interactive engines are intended to run entirely in the browser. Before publishing a release, verify the engine registry, navigation controls, and learning-game smoke tests.
