# spiral-visualization

An experimental 3D visualization: a procedurally-generated rock with a simulated
surface-temperature field, plus a live analytics dashboard.

## What's here

- **3D rock** — a subdivided icosphere displaced by layered Perlin noise, so the
  silhouette comes out lumpy and irregular. Drag to orbit, scroll to zoom.
- **Surface temperature** — a per-vertex scalar field (smooth fractal noise plus
  several randomly-placed hot/cold "spots") mapped through a cold→hot colormap.
- **Analytics panel** — histogram, cumulative distribution, latitude profile, and
  an unwrapped (equirectangular) surface map, all sharing the same colormap.
- **Slice plane** — an adjustable cutting plane (azimuth / elevation / offset).
  Where it intersects the surface, a cross-section chart shows temperature around
  the intersection loop in real time.

## Running it

It's a single self-contained static page — no build step. Just open `index.html`
in a browser, or serve the folder:

```sh
python3 -m http.server 8000
# then visit http://localhost:8000
```

Three.js is loaded from a CDN via an import map, so an internet connection is
needed on first load.
