# Walk-In Cooler Configurator

A real-time 3D walk-in cooler/freezer configurator built with **Three.js** and vanilla JavaScript. Design, dimension, and visualize commercial walk-in cooler compartments directly in the browser.

![Built with Three.js](https://img.shields.io/badge/Three.js-r128-black?logo=three.js)
![Vanilla JS](https://img.shields.io/badge/Vanilla-JavaScript-F7DF1E?logo=javascript&logoColor=000)
![License](https://img.shields.io/badge/License-Proprietary-blue)

---

## Overview

This configurator provides an interactive 3D environment for specifying walk-in cooler and freezer compartments — the kind used in restaurants, warehouses, and commercial kitchens. Users can adjust dimensions, select materials, position doors, and see every change reflected instantly in a fully rendered 3D model with accurate measurement annotations.

## Features

### 3D Compartment Builder
- Real-time 3D rendering of walk-in cooler structure (walls, floor, ceiling, door)
- **Indoor Walk-In** — open-top view for interior inspection
- **Outdoor Walk-In** — translucent roof with matching wall material and thickness
- Accurate wall panel construction with configurable thickness

### Door System
- 34" swing door positioned 19" from the left wall edge
- Detailed hardware: 3 strap hinges, lever handle, slide bolt, door closer
- Door frame with threshold strip
- Brand logo plate

### Dimension Annotations
- 3D sprite labels rendered directly in the scene (camera-facing)
- Overall width, depth, and height measurements
- Per-segment measurements: wall thickness, door offset, door width, remaining wall
- Red dimension lines with tick marks

### Configuration Panel
- **Walk-In Type** — Indoor / Outdoor toggle (swaps tab navigation and roof)
- **Temperature** — Cooler / Freezer selection
- **Exterior Finish** — Stucco Aluminum, Galvanized, Stucco Stainless, Stainless Steel, White, or custom color
- **Dimensions** — Width (6'–30'), Depth (6'–30'), Height (7'6"–10') with feet/inches readout
- **Floor Options** — Standard, Heavy-Duty, Reinforced, or No Floor
- **Ramp** — Interior, Exterior, or None

### Interaction & Tools
- **Orbit Controls** — click-drag to orbit, right-click to pan, scroll/pinch to zoom
- **Undo / Redo** — full state history with Ctrl+Z / Ctrl+Y support
- **Fullscreen** — native browser fullscreen toggle
- **Auto-Rotate** — play/pause rotation with toolbar button + sidebar toggle
- **Screenshot** — exports the current 3D view as a high-resolution PNG
- **Axis Gizmo** — X/Y/Z orientation indicator that tracks camera rotation
- **Reset View** — snap back to the default camera angle

### UI
- Tabbed navigation with context-aware tabs (Indoor vs Outdoor tab sets)
- Material finish swatches with active state indicators
- Slider controls with imperial measurement readouts
- Responsive layout: left toolbar, center 3D canvas, right config panel, footer bar

## Tech Stack

| Layer | Technology |
|-------|-----------|
| 3D Engine | Three.js r128 |
| Language | Vanilla JavaScript (ES6+) |
| Styling | CSS3 with custom properties |
| Fonts | Outfit, IBM Plex Mono |
| Build | Zero-build, single HTML file |

## Getting Started

No build tools, no dependencies, no server required. Just open the file.

```bash
# Clone the repo
git clone https://github.com/icoolaca/walk-in-cooler-configurator.git

# Open in browser
open index.html
```

Or serve it locally:

```bash
# Python
python -m http.server 8000

# Node
npx serve .
```

Then visit `http://localhost:8000`.

## Project Structure

```
walk-in-cooler-configurator/
├── index.html          # Complete application (HTML + CSS + JS)
└── README.md
```

Everything runs from a single `index.html` file — HTML structure, CSS styling, Three.js scene setup, 3D construction logic, UI bindings, undo system, and the render loop are all self-contained.

## Roadmap

- [ ] **Phase 2** — Door system: swing direction, glass door option, self-closing hinges
- [ ] **Phase 3** — Interior: shelving, wall finish selector, floor drains
- [ ] **Phase 4** — GLB/GLTF model loading for high-detail hardware components
- [ ] **Phase 5** — Refrigeration unit placement (condenser/evaporator)
- [ ] **Phase 6** — Export: quote generation, Revit file export
- [ ] **Phase 7** — Modular file architecture (ES modules, component separation)

## Browser Support

Tested on modern browsers with WebGL support:
- Chrome 90+
- Firefox 90+
- Safari 15+
- Edge 90+

---

## Author

**John Lutao** — Designer & Developer

---

<sub>Built for ICC Energy · CoolBuild Walk-In Configurator</sub>
