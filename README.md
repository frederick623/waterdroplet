# waterdroplet

A WebGL 2 desktop simulation of water, rain, and reflections — just for fun.

## Features

| Control | Description |
|---|---|
| **Rain slider** | Tune rain intensity from calm (0) to heavy downpour (100). Spawns up to 64 simultaneous ripple rings. |
| **Wind variation slider** | Sets the maximum random wind variation from calm (0) to ±15, capped at one-seventh of the former maximum strength. Affects Gerstner wave direction, rain streak angle, wave-crest foam, and camera tilt. |
| **Random rain / wind** | Smoothly transitions to a new random rain value or wind value every 1.8 seconds; moving a slider disables its random mode. |
| **Day Sky** | Blue sky with animated clouds, atmospheric haze, and a sun + corona reflected in the water. |
| **Night Neon** | Dark sky with stars, moon, city-horizon glow, and six coloured neon signs (one blinks) reflected in the water. |

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
