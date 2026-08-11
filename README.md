# Neon Snake (Rogue-Lite Edition)

A rogue-lite twist on the classic Snake game built using vanilla JavaScript and HTML5 Canvas. It introduces level progression, rogue-lite mutation upgrades, custom canvas rendering, and procedural sound generation.

Live Demo: https://snake-game-ten-vert.vercel.app

---

## Overview

Traditional Snake games are static and repetitive. This implementation adds a rogue-lite progression loop where clearing levels lets the player choose between random mutations (speed changes, tail reductions, extra lives) while navigating higher grid difficulty and obstacle scaling.

---

## Architecture & Implementation

- **Game Engine**: Custom game loop running on `requestAnimationFrame` with grid-based delta timing and collision detection.
- **Rendering**: 2D Canvas context rendering with custom glow effects, trail rendering, and grid coordinate calculations.
- **Audio Engine (`audio.js`)**: Real-time sound effect synthesis using the Web Audio API (oscillators and gain nodes) without relying on external mp3 assets.
- **Mutation System**: Card-drafting interface shown at each level transition to alter snake physics and gameplay rules dynamically.
- **Input Handling**: Keyboard event listeners (`WASD` / Arrow keys), touch swipe gesture handling, and on-screen D-Pad for mobile viewports.

---

## Project Structure

```text
snake-game/
├── index.html       # Game viewport layout and UI overlays
├── style.css        # Cyberpunk visual styles and HUD animations
├── app.js           # Core game state machine, canvas loop, and mutation logic
├── audio.js         # Web Audio API sound synthesis engine
└── vercel.json      # Static deployment configuration
```

---

## Running Locally

Clone the repository and open `index.html` directly in any modern browser:

```bash
git clone https://github.com/Mahesh-Nandigam/snake-game.git
cd snake-game
open index.html
```

Or serve it with any local static server:

```bash
npx serve .
```
