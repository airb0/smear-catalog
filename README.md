# Smear catalog

Seven smear-frame techniques from hand-drawn animation — Squash and Stretch, Elongate, Motion blur, Smudged blurs, Jagged lines, Sketched gestures and Speedlines — running side by side on the same looping trajectory, on any object. Pick a path (A-B-A, enter and exit, throw, swing, into a wall, drop), a speed and how many frames each drawing is held. Then open any technique to step through it frame by frame, see every drawing of the cycle as a storyboard and tune its settings.

**Try it:** https://tsytkin.com/tools/smear-catalog/

## Run it locally

```bash
git clone https://github.com/airb0/smear-catalog.git
```

Open `index.html` in a browser. Nothing to install, no build step.

## How it works

The object is a sprite: anything drawn into a canvas, or an image you drop onto the page. Its motion is a pure function of the frame. Every effect reads the object's silhouette and its own colours, and follows the path it actually travelled, so on an arc the smear curves. Settings are in seconds and px/s, so an effect looks the same at any frame rate. The page runs at 30 fps, on threes by default.

## Files

| File | What it is |
|---|---|
| `index.html` | The catalogue: header controls, the grid of loops, the preview with storyboard and settings |
| `core.js` | Easing, seeded randomness and other motion basics |
| `smear.js` | Sprites, silhouettes, poses, squash & stretch, the track behind the object, speed lines |
| `smear-effects.js` | The smear effects, each with its defaults and settings |

## Sources

The set of techniques was inspired by the carousel «Types of Animation Smear Frames» by [@rikognition](https://www.instagram.com/p/DNEuWFtSxgY/).

## Licence

MIT, see `LICENSE`.
