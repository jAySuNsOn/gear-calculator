# Gear Teeth Calculator

A fully client-side spur and bevel gear engineering calculator. No server, no dependencies — just open the HTML file in any browser.

**Live app:** https://YOUR-USERNAME.github.io/gear-calculator/

---

## Features

### Calculators
- **Gear ratio** — driver/driven tooth counts, output RPM, torque (theoretical + efficiency-adjusted), gear preview
- **Module / pitch** — ISO standard modules, full tooth geometry (pitch dia, addendum, dedendum, outside dia, root dia, base circle, tooth thickness)
- **Compound gearing** — chain 1–4 gear stages in series, with cascaded ratio, per-stage RPM/torque, and cumulative efficiency loss
- **Bevel gears** — pitch cone angles for any shaft angle, pitch diameters, back-cone radius, face width limit

### Engineering Drawing
- True involute tooth geometry
- Front view, section view, or both
- Dimension annotations (OD, pitch circle, bore, face width)
- Title block with all gear parameters
- Optional keyway slot
- Configurable bore, face width, pressure angle

### CAD / CNC Exports
All files generated in-browser — no upload required.

| Format | Description |
|--------|-------------|
| `.DXF` | 2D gear profile — AutoCAD, LibreCAD, Fusion 360 |
| `.SVG` | Scalable vector outline — laser cutting, Inkscape, Illustrator |
| `.NC` | ISO G-code for CNC lathe (face, OD, bore) |
| `.STL` | ASCII triangulated solid for 3D printing |
| `.STEP` | ISO 10303 AP203 parametric geometry — FreeCAD, SolidWorks, CATIA |
| `.CSV` | XY involute tooth profile coordinates |

---

## Hosting on GitHub Pages

1. Upload all files to a repo (e.g. `gear-calculator`)
2. Go to **Settings → Pages**
3. Set source to **main branch / root**
4. Your app is live at `https://YOUR-USERNAME.github.io/gear-calculator/`

---

## Formulas

- ISO 21771 — Cylindrical involute gears
- AGMA 2001 — Fundamental rating factors for spur and helical gear teeth
- Involute geometry: `x = rb(cos t + t·sin t)`, `y = rb(sin t − t·cos t)`

---

## Files

```
index.html    — The complete app (self-contained)
README.md     — This file
LICENSE       — MIT licence
```

---

## Licence

MIT — free to use, modify, and share.
