# NEON PONG

Player vs AI Pong in a single HTML file. No dependencies, 60 FPS canvas engine, playable on desktop, laptop, tablet, and phone (portrait and landscape).

First to 7 wins. The AI starts imperfect and gets sharper as the match goes on.

## Controls

### Desktop / laptop
- Mouse move — left paddle
- W / S or Arrow Up / Down — paddle fallback
- Space or Enter — start / confirm
- Esc or P — PAUSE / resume
- Arrow keys + Enter — pause menu (RESUME, RESTART, SOUND, TITLE)

### Phone / tablet
- Drag — left paddle
- Tap **PLAY** — start
- Tap **SOUND** on the title screen to mute or unmute
- Tap pause (II, under the AI score) — pause menu
- Tap **RESUME**, **RESTART**, **SOUND**, or **TITLE**

## Pause menu

- **RESUME** — continue the rally
- **RESTART** — new match (scores reset)
- **SOUND** — toggle SFX
- **TITLE** — back to the start screen

The game also pauses when you switch tabs or leave the window.

## Features

- Deterministic `requestAnimationFrame` loop with sub-step collision (no tunneling)
- Bounce angle from paddle hit position
- Speed ramps after each hit, then clamps
- Human-like AI: reaction delay, aim error, difficulty scales with score and rally length
- Smooth paddle motion (no snapping)
- Neon glow with `prefers-reduced-motion` support
- Web Audio API SFX (paddle, wall, score) — no audio files
- Mute from the menu
- Full-viewport canvas, iPhone notch / home-indicator safe areas
- Instant restart

## Tech stack

Vanilla JavaScript + HTML5 Canvas + Web Audio API.

No libraries. No CDNs. No build step.

## Deploy to GitHub Pages

1. Create a GitHub repository.
2. Push `index.html` and `README.md` to the `main` branch at the repo root.
3. Open **Settings → Pages**.
4. Source: **Deploy from a branch**, branch `main`, folder `/` (root).
5. Save. Live at `https://<user>.github.io/<repo>/`.

Local play: open `index.html` in a modern browser, or serve the folder:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## License

MIT
