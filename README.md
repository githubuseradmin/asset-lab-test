# Asset Lab

![CI](https://github.com/githubuseradmin/asset-lab-test/actions/workflows/ci.yml/badge.svg)
![license](https://img.shields.io/badge/license-MIT-blue)
![built with](https://img.shields.io/badge/HTML%20%C2%B7%20CSS%20%C2%B7%20JS-informational)
![demo](https://img.shields.io/badge/demo-live-brightgreen)

**[▶ Live demo](https://githubuseradmin.github.io/asset-lab-test/)**

A zero-dependency, single-file web demo that procedurally generates game **art** (SVG) and **sound** (Web Audio) entirely in code — no external image or audio files, no build step. Built for anyone who wants to see runtime asset generation in action.

## What it is

Asset Lab shows that game assets can be created 100% in the browser from rules alone:

- **Character + scene** — vector graphics (SVG), generated procedurally. The creature's color, the shape of its ears/horns, its hair, the time of day and the background scene are different on every roll. Click **Generate again** for a new variation or **Time of day** to cycle through twilight / day / night / sunset.
- **Sounds** — synthesized with the **Web Audio API** (coin, jump, explosion, power-up, UI click, hurt) plus a procedural chiptune loop. Each effect is a generated waveform (tone + envelope + noise), not a recorded sample.

## Run / play locally

No build step and no dependencies. Just open the file in a browser:

1. Clone or download this repository.
2. Open **`index.html`** by double-clicking it (or drag it into any modern browser).
3. Use the buttons to generate art and trigger sounds.

> Tip: browsers require a user interaction before audio can start, so click a sound or the music button to enable the Web Audio context.

Optionally, serve it over a local HTTP server (handy if your browser restricts `file://`):

```bash
# Python 3
python -m http.server 8000
# then open http://localhost:8000
```

## Deploy to GitHub Pages

`index.html` lives at the repository root, so GitHub Pages serves it with zero configuration:

1. Push this repository to GitHub (e.g. `asset-lab-test`).
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
4. Select the **`main`** branch and the **`/ (root)`** folder, then **Save**.
5. After a minute the site is live at `https://<your-username>.github.io/asset-lab-test/`.

## Tech stack

- **HTML / CSS** — single self-contained page, no framework.
- **SVG** — procedurally assembled vector graphics for the character and scene.
- **Web Audio API** — runtime sound synthesis (oscillators, gain envelopes, filtered noise) and a procedural chiptune sequencer.
- **Vanilla JavaScript** — no dependencies, no build tooling.
