# Pocket Planet

Procedural worlds from pure math. No textures, no assets, no downloads beyond Three.js. Everything you see is generated in real-time by GLSL fragment shaders running on your GPU.

## Play

**[ashleywolf.github.io/pocket-planet](https://ashleywolf.github.io/pocket-planet/)**

## What's happening

A single HTML file renders a spinning planet with:

- **Terrain** generated from 6-octave fractional Brownian motion (fBm) over 3D simplex noise
- **Biomes** mapped by elevation: deep ocean, shallow water, beach, grassland, forest, rock, snow
- **Clouds** on a separate transparent sphere, animated with their own noise field
- **Atmosphere** using Fresnel rim glow with simulated Rayleigh scattering (blue on day side, orange at the terminator)
- **City lights** that appear on the night side of landmasses
- **Specular highlights** on ocean surfaces
- **Star field** with procedural nebula in the background

Zero textures. Zero image assets. The entire planet is math.

## Controls

- **Drag** to orbit
- **Scroll** to zoom
- **Sliders** to reshape the world in real-time (sea level, terrain scale, roughness, cloud density, atmosphere intensity, rotation speed)
- **New Planet** for a different seed
- **Randomize** for a completely random world

## Tech

- [Three.js](https://threejs.org/) r170 (ES modules via CDN importmap)
- Custom GLSL vertex + fragment shaders (simplex noise, fBm)
- ~18KB, one file

## Part of the series

- [Scream Invaders](https://ashleywolf.github.io/scream-invaders/) -- Space Invaders but you scream to shoot
- [Keep It Together](https://ashleywolf.github.io/keep-it-together/) -- Try not to smile
- [Face Dance Revolution](https://ashleywolf.github.io/face-dance-revolution/) -- DDR with your face
- **Pocket Planet** -- You are here
