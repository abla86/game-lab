# GAME LAB

Interactive engineering laboratory with one shared runtime and ten plug-in engines.

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
