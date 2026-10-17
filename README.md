*[Leia em Português](README.pt-BR.md)*

# Singularvs

> A 2D demake of **SpaceEngine**, in the spirit of **Elite (1984)** — everything procedural, zero assets.

![Singularvs screenshot](screenshot.png)

**Singularvs** is a contemplative space simulator that runs entirely in the browser. A single HTML file, no dependencies, no images, no pre-recorded audio. The whole universe — from billions of galaxies to grains of sand on an alien beach — is generated live from deterministic mathematical functions.

---

## What's inside

- **~1 Gpc universe** with billions of procedural galaxies (spiral, barred, elliptical, irregular, lenticular, quasars).
- **Continuous nested scale**: galaxy map → star map → system → telescope → orbit → surface.
- **Stars** with spectral classes (OBAFGKM + L/T brown dwarfs), luminosity classes, and **hierarchical multiple systems** of up to 8 stars (binaries, triples, quadruples — with companions that can be brown dwarfs, neutron stars or black holes).
- **Planets** scientifically classified: Terra, Super Terra (Hestia-like), Desert, Ice, Titan, Oceania, Selena, Dwarf, Gas Giant, Ice Giant, Comets.
- **Internal simulation**: crust/mantle/core composition, radiogenic heat, tectonic plates (simplified Voronoi), volcanism, cryovolcanism (Europa/Enceladus), mountain ranges, lakes and rivers.
- **Atmospheres** with pressure in atm/mmHg, composition, density, greenhouse effect.
- **Biology**: origin (abiogenesis vs panspermia), type (unicellular/multicellular), habitat (aerial/aquatic/terrestrial/all/subglacial).
- **Procedural moons and rings**, visible both on the globe and in the surface sky.
- **Dynamic sky** with all stars in the system (A, B, C, D...), spectral color, brightness by flux (L/d²), atmospheric attenuation and day/night cycle.
- **Navigable surface** in first person, with terrain, rivers, vegetation, background stars, red spot on tidally-locked Terras around M dwarfs.
- **Star Browser** with filters (Terra, Desert, Ice, Gas, Comet) and column sorting.
- **Unified map** with continuous zoom between galactic and stellar scale.
- **Persistent logbook** (localStorage) with system naming and notes.
- **Procedural music** with modal progressions, pads, bass, arpeggios, kick and lead voice.
- **WebGL2 post-processing**: cinematic presets, retro CRT, pure pixel.

---

## How to play

No installation required. No server required. Just open the file in your browser:

    xdg-open index.html      # Linux
    open index.html          # macOS
    start index.html         # Windows

Or, if you want to serve via HTTP (to test localStorage in some browsers):

    python3 -m http.server 8000
    # then access http://localhost:8000

Recommended: **Firefox** or recent **Chromium**, with WebGL2 enabled.

**Language**: the interface supports Portuguese and English. Switch anytime via *Options → Language*.

---

## Controls

### Keyboard

| Action | Key |
|---|---|
| Fly / turn | WASD or arrows |
| Flight mode | V |
| Focus system | ENTER (near) |
| Release focus | ESC |
| Telescope | T |
| Planet info | I |
| Land | ENTER (in orbit) |
| Star map | M |
| Galaxy map | G |
| Map zoom | Q / E / mouse wheel |
| Logbook | L |
| Star Browser | B |
| Name / Note | N / J |
| Post-processing | F2 |
| Screenshot | F4 |
| Menu | ESC |

### Gamepad (XInput / GameSir T4)

| Action | Button |
|---|---|
| Fly / turn | Left stick |
| Turbo | RT / LT |
| Flight mode | L3 / R3 |
| Focus / land | A |
| Back / release | B |
| Telescope | X |
| Planet info | R3 |
| Star map | Y |
| Galaxy map | LB |
| Logbook | RB |
| Map zoom | LT / RT |
| Menu | START |

A complete **Controls Guide** is available from the in-game menu.

---

## Technical highlights

- **Single file** of ~300 KB, no minification, no build step.
- **Zero dependencies**: no framework, no library. Only Canvas 2D, WebGL2 and Web Audio — native browser APIs.
- **Zero assets**: no image, no sound, no embedded font. All aesthetics is mathematics.
- **On-demand generation**: nothing in the universe is stored. Every galaxy, star, planet and feature is recomputed by hash from integer coordinates. The "seed" is the only persisted data of the universe.
- **Deterministic PRNG** (mulberry32) and spatial hashes (hash2D) guarantee absolute reproducibility: the same seed produces the same universe, forever.
- **LOD layers** for the star map: stipple in world space with deterministic jitter, avoiding moiré and flicker on continuous zoom.

---

## Inspirations and credits

This is a fan project, **non-commercial**, made purely out of the desire to create.

- **SpaceEngine** (Vladimir Romanyuk / CosmoGraphic) — conceptual and aesthetic inspiration for planetary classification, terminology and data structure.
- **Elite** (David Braben and Ian Bell, 1984) — inspiration in the philosophy of procedural generation without assets, everything on-demand in memory.
- **Kurzgesagt - In a Nutshell** — conceptual scientific references (Hestia-type Super Earths, cryovolcanism, panspermia).

No code, asset, data or metadata from those projects was used. All content is original and procedurally generated. The name "SpaceEngine" is not used as a trademark of this project.

---

## Development

This project was developed in human-AI collaboration. See [CONTRIBUTORS.md](CONTRIBUTORS.md) for details about the creative process and the tools used.

---

## License

Distributed under the **MIT License**. See [LICENSE](LICENSE) for the full text.

In short: you may use, copy, modify, merge, publish, distribute, sublicense and/or sell copies of this software, provided you keep the original copyright notice and the MIT license in all copies or substantial portions.
