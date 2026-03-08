# CarRadio

CarRadio is a touch-first, single-page web radio interface designed for in-car style listening. It presents a full-screen carousel of preset stations, supports MP3 and HLS streams, and integrates with the browser Media Session API so play/pause and track navigation can map cleanly to headset, lock-screen, or vehicle controls when supported.

## What the application is

- A lightweight HTML/CSS/JavaScript internet radio player.
- Optimized for mobile and dashboard-like use (large typography, swipe gestures, minimal UI chrome).
- Built around seven preset stations with smooth horizontal station switching.

## Build / run instructions

This project is static and has no build step.

1. Clone the repository.
2. Open `index.html` directly in a modern browser **or** serve the folder with a simple static server.

Example (Python 3):

```bash
python -m http.server 8080
```

Then open `http://localhost:8080`.

## Basic controls

- **Tap anywhere**: Toggle play/pause.
- **Swipe left/right**: Move to the next/previous station.
- **Media keys / car controls (if available)**:
  - Play / pause
  - Previous track (previous station)
  - Next track (next station)
  - Up/down style buttons map to station next/previous on systems that emit those controls as media keys or keyboard events
- **Status indicators**:
  - Top badge shows readiness/current station.
  - Loading spinner appears while buffering/connecting.
  - Bottom dots show the currently selected preset.

## Docker deploy script

A helper script is included to build and run the app in Docker:

```bash
./deploy.sh            # defaults to port 3011
./deploy.sh 8080       # deploy on a custom port
```

What it does:

- Regenerates `.dockerignore`, `server.js`, and `Dockerfile`.
- Builds a `carradio` Docker image.
- Replaces any running `carradio` container.
- Starts the container with `--restart unless-stopped`.

## Roadmap

- Add editable/custom station presets (save to local storage).
- Add explicit volume and mute controls.
- Add stream health fallback/retry behavior for unstable networks.
- Add optional station logos/metadata overlays.
- Add lightweight test coverage for station switching and playback state transitions.
