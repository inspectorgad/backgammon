# Backgammon with AI Tutor

A browser-based backgammon game built as a Progressive Web App (PWA). Play against an AI opponent with real-time move coaching, animated 3D-style pieces, particle effects, and procedural sound effects — no install required.

## Features

- **AI tutor** — After each move, the tutor evaluates your play and offers coaching on better alternatives
- **Animated pieces** — Smooth piece movement with bounce, shadow, and landing ripple animations powered by Three.js
- **Particle system** — Visual feedback for hits, blots, bearing off, and winning (confetti burst)
- **Procedural sound** — Web Audio API generates dice rolls, piece clicks, hit sounds, and a win fanfare without any audio files
- **Two themes** — Classic wood board and a modern dark theme
- **Offline play** — Service worker caches the app for fully offline use
- **Installable** — Add to home screen on iOS/Android or install as a desktop PWA

## Tech Stack

| Layer | Technology |
|-------|-----------|
| UI framework | React 18 (CDN, no build step) |
| 3D / animation | Three.js r128 |
| Audio | Web Audio API |
| PWA | Service Worker + Web App Manifest |
| Transpilation | Babel Standalone (in-browser) |

## Installation

No build step required. The entire app is a single `index.html` file with dependencies loaded from CDN.

**To run locally:**

```bash
# Any static file server works — example with Python:
python3 -m http.server 8080
# Then open http://localhost:8080
```

**To install as a PWA:**
- Open in Chrome, Edge, or Safari
- Use the browser's "Add to Home Screen" or "Install app" option

## Usage

1. Open the app — you play as White, the AI plays as Black
2. Roll dice by clicking the dice area
3. Click a valid point to move your piece; legal moves are highlighted
4. The AI tutor panel shows move quality after each turn
5. Bear off all 15 of your pieces to win

## Files

```
index.html      — Full app (React components, game logic, AI, audio, particles)
manifest.json   — PWA metadata and icon config
sw.js           — Service worker for offline caching
icon-192.png    — App icon (192×192)
icon-512.png    — App icon (512×512)
```

## License

MIT
