# waterdroplet

A WebGL 2 desktop simulation of water, rain, and reflections — just for fun.

## Features

| Control | Description |
|---|---|
| **Rain slider** | Tune rain intensity from calm (0) to heavy downpour (100). Spawns up to 64 simultaneous ripple rings. |
| **Wind slider** | Sets a steady wind from −50 to 50. The endpoints use half the former effective maximum magnitude, affecting wave direction, rain-streak angle, and wave-crest foam. |
| **Random rain / wind** | Random rain selects a new target every 12 seconds and eases gradually between values. Random wind takes a normally distributed step from its previous target every 5 seconds, clamped to −50 to 50, so small changes are common and large changes are rare; both gauges show their current simulated intensity. Moving a slider disables its random mode. |
| **Day Sky** | Blue sky with animated clouds, atmospheric haze, and a sun + corona reflected in the water. |
| **Night Neon** | Dark sky with stars, moon, city-horizon glow, and six coloured neon signs (one blinks) reflected in the water. |
| **Day length slider** | Sets the Time mode's simulated day duration from 1 to 10 minutes. |
| **Time mode** | Runs a configurable timelapse through blue sky, sunset, magic hour, neon night, darkness, purple dawn, gold sunrise, and blue sky. |

Additional visual details:
- Perspective ray-cast camera looking at the water plane
- Gerstner waves (physically-based deep-water dispersion)
- Per-raindrop slow-expanding ripple rings with soft edges and realistic decay
- White splash flash on raindrop impact
- Fresnel reflection (Schlick approximation)
- Specular highlights (sun for day, neon for night)
- Wave-crest foam at high wind speeds
- Animated rain streaks in the air, angled by wind
- Atmospheric fog with depth
- Reinhard tone-mapping + gamma correction
- FPS counter

## How to run

No build step or server required — just open `index.html` in any modern browser that supports **WebGL 2** (Chrome 56+, Firefox 51+, Edge 79+, Safari 15+):

```
open index.html          # macOS
xdg-open index.html      # Linux
start index.html         # Windows
```

Or serve it with any static file server:

```bash
npx serve .
# then visit http://localhost:3000
```
