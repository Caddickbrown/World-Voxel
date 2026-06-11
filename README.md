# World Voxel

A zero-player civilisation simulator rendered in 3D voxels.

**World**'s emergent agent simulation (concepts, disease, fire, settlements) running inside **Island Voxel**'s Three.js voxel engine.

Watch primitive agents wander a voxel landscape, discover fire, form settlements, fall sick, go to war — all rendered as blocky humanoids on a chunked voxel terrain.

## How it works

- **Simulation:** World's `SimulationWorker` runs off the main thread — full agent AI, ConceptGraph discovery, DiseaseSystem, FireSystem, SettlementSystem, etc.
- **Terrain:** World's 128×128 tile grid converted to a voxel heightmap. Each tile = 4×4 voxel footprint, height from tile elevation and type.
- **Agents:** Island Voxel's `buildHumanoid()` blocky character meshes, coloured by agent state, scaled by life stage, animated with walk cycles.
- **Observer camera:** No player. Orbit, zoom, and watch civilisation emerge.

## Controls

| Input | Action |
|-------|--------|
| Drag  | Orbit camera |
| Scroll | Zoom |
| Space | Pause / unpause |
| `+` / `-` | Speed up / slow down simulation |

## Running locally

```bash
python3 -m http.server 8903
# open http://localhost:8903
```

## Credits

- Simulation engine: [World](https://github.com/Caddickbrown/World)
- Voxel renderer: [Island-Voxel](https://github.com/Caddickbrown/Island-Voxel)
