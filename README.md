# Beehive Construction Simulator (Standalone)

A self-contained, offline HTML visual simulation of a beehive “building” outward in **hexagonal cells**, with **worker-bee paths** and **honey storage** filling over time. Includes mobile-optimized controls with a **show/hide** toggle and a **fixed auto-sized HUD/counter panel**.

* Demo (honeycomb)[https://s3.us-east-1.amazonaws.com/jessereese.com/honeycomb.html]

## Files

- `beehive_construction_simulator_fixed.html` — standalone simulation (no external deps)

## Quick Start

1. Download the HTML file.
2. Open it in any modern browser (Chrome, Safari, Edge, Firefox).

That’s it — no build tools, no server required.

## Controls

### Sliders
- **Colony size**: Increases worker count and overall activity/expansion radius.
- **Resource availability**: Affects build rate + honey storage behavior/density.
- **Simulation speed**: Multiplies update speed.

### Buttons
- **Pause / Resume**: Stops/starts simulation updates.
- **Reset**: Regenerates grid and restarts growth.
- **Recenter**: Resets pan/zoom.

### Navigation
- **Pan**: click/touch drag on the canvas
- **Zoom**:
  - Desktop: mouse wheel
  - Mobile: pinch to zoom

## Mobile UI

On screens <= 860px wide, the controls become a **bottom sheet**:
- Starts **collapsed** by default (so the canvas is visible)
- Tap **Show/Hide** or swipe the handle area up/down to expand/collapse

## Visual Legend

- **Unbuilt cells**: faint outlines
- **Built comb**: vibrant gold that **stays gold** once built
- **Honey storage**: brighter glow; “capped” look when nearly full
- **Worker paths**: animated flow streaks + subtle spark particles

## HUD / Counter Panel Fix

The top-left counter panel is drawn directly on the canvas and is now:
- **Auto-sized** based on measured text width/height
- Uses a rounded rectangle + subtle border/highlight layers
- Prevents text from being cut off on different DPIs / fonts

## Customization Notes (Optional)

Inside the HTML, you can tweak parameters in `currentParams()`:
- `radius` / `workerCount` scaling
- `buildRate`, `honeyRate`, `storageBias`
- trail density and spark rate (`trailKeep`, `sparkRate`)
- worker movement speed (`moveSpeed`)

## Troubleshooting

- **Looks blurry on retina**: refresh the page (the canvas scales to devicePixelRatio up to 2.5).
- **Performance on older phones**: reduce Colony size and/or Simulation speed.
- **Controls covering canvas on mobile**: tap “Hide” (collapses the bottom sheet).

## License

Use freely for personal projects, demos, or prototyping.
