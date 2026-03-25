# Pocket Planet

What does your repo look like as a planet?

Type any public GitHub repo and watch it generate a unique, deterministic world. The repo's stats shape the planet -- stars carve terrain, issues flood oceans, languages color the biomes, and the codebase's age sets its spin.

## Play

**[ashleywolf.github.io/pocket-planet](https://ashleywolf.github.io/pocket-planet/)**

Try: [torvalds/linux](https://ashleywolf.github.io/pocket-planet/#torvalds/linux) | [facebook/react](https://ashleywolf.github.io/pocket-planet/#facebook/react) | [rust-lang/rust](https://ashleywolf.github.io/pocket-planet/#rust-lang/rust)

## How repo stats map to planet features

| Repo stat | Planet feature | Logic |
|-----------|---------------|-------|
| Stars | Terrain height | More stars = more dramatic mountains (log scale) |
| Forks | Surface roughness | More forks = more rugged, fractured terrain |
| Open issues | Sea level | More issues = drowning in water |
| Repo size (KB) | Atmosphere thickness | Bigger codebase = thicker atmosphere |
| Primary language | Biome colors | JavaScript = golden, Rust = copper, Python = teal-green, etc. |
| Secondary language | Color blending | Mixed into biomes proportionally |
| Repo age | Rotation speed | Older repos spin slower (more dignified) |
| Forks + issues | Cloud density | More activity = more clouds |

Same repo always generates the same planet. Shareable via URL hash (`#owner/repo`).

## What's under the hood

Zero textures. Zero image assets. The entire planet is GLSL fragment shaders running on your GPU:

- 6-octave fractional Brownian motion over 3D simplex noise for terrain
- Language-specific color palettes for biome mapping (21 languages supported)
- Animated cloud layer with independent noise field
- Fresnel atmosphere with simulated Rayleigh scattering
- Night-side city lights in the repo's accent color
- Specular ocean highlights
- Procedural starfield with nebula

One HTML file, ~25KB. Uses the public GitHub API (no auth needed, 60 requests/hour).

## Controls

- **Drag** to orbit
- **Scroll** to zoom
- **Pinch** on mobile
- **Enter** a repo name and hit Generate

## Part of the series

- [Scream Invaders](https://ashleywolf.github.io/scream-invaders/) -- Space Invaders but you scream to shoot
- [Keep It Together](https://ashleywolf.github.io/keep-it-together/) -- Try not to smile
- [Face Dance Revolution](https://ashleywolf.github.io/face-dance-revolution/) -- DDR with your face
- **Pocket Planet** -- You are here
