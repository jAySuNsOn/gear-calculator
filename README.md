# Gear Teeth Calculator

A fully client-side spur and bevel gear engineering calculator with stress analysis, fatigue life estimation, engineering drawing, and CAD export. No server, no login — just open the file in any browser.

**Live app:** https://jaysunson.github.io/gear-calculator/

---

## Features

### Calculators
- **Gear ratio** — driver/driven tooth counts, output RPM, torque (theoretical + efficiency-adjusted), proportional gear preview
- **Module / pitch** — ISO standard modules (0.5–10 mm), full tooth geometry: pitch dia, addendum, dedendum, outside dia, root dia, base circle radius, tooth thickness
- **Compound gearing** — chain 1–4 gear stages in series, cascaded ratio, per-stage RPM/torque, cumulative efficiency loss (η^n)
- **Bevel gears** — pitch cone angles for any shaft angle (not just 90°), pitch diameters, back-cone radius, face width limit

### Stress & Fatigue Analysis
- **Bending stress** — ISO 6336 / Lewis tooth root stress with dynamic factor (Kv), face load factor (KFβ), contact ratio factor (Yε)
- **Contact stress** — ISO 6336 Hertzian contact using zone factor (ZH), elasticity factor (ZE), contact ratio factor (Zε)
- **Safety factors** — bending (target ≥ 1.5) and contact (target ≥ 1.2) with SAFE / MARGINAL / UNSAFE colour coding
- **Minimum face width** — solved independently from bending and contact limits, shows recommended minimum
- **Fatigue life** — Wöhler S-N power law: bending (mW = 6.35) and contact/pitting (mW = 3.33), in hours and cycles
- **12 materials** — Cast Iron Gr20/40, Carbon Steel 160–300HB, Alloy Steel 350HB, case-hardened, nitrided, Aluminium Bronze, Nylon 66, Acetal/POM
- **Application factor** — KA from 1.00 (uniform) to 2.00 (very heavy shock)
- Analyse up to 4 stages independently

### Engineering Drawing
- True involute tooth geometry (not simplified)
- Front view, section view, or both side by side
- Dimension annotations (OD, pitch circle, bore, face width)
- Title block with all key parameters
- Optional keyway slot

### CAD / CNC Exports
All files generated in-browser — no upload required.

| Format | Description |
|--------|-------------|
| `.DXF` | 2D gear profile — AutoCAD, LibreCAD, Fusion 360, DraftSight |
| `.SVG` | Scalable vector outline — laser cutting, Inkscape, Illustrator |
| `.NC`  | ISO G-code for CNC lathe (face, rough/finish OD, drill and bore) |
| `.STL` | ASCII triangulated solid for 3D printing |
| `.STEP`| ISO 10303 AP203 parametric geometry — FreeCAD, SolidWorks, CATIA |
| `.CSV` | XY involute tooth profile coordinates |

---

## Recommended Workflow

1. **Gear ratio** — confirm ratio, output speed and torque
2. **Compound** — split large ratios across multiple stages
3. **Module / pitch** — establish tooth geometry
4. **Stress & Fatigue** — verify the design survives the load; adjust face width or material until all stages show SAFE
5. **Drawing** — generate the engineering drawing using the stress-verified face width
6. **Export** — download DXF, STL, STEP, or G-code for fabrication

---

## Formulas & Standards

- **ISO 21771** — Cylindrical involute gears (geometry)
- **ISO 6336** — Calculation of load capacity of spur and helical gears (bending & contact stress)
- **AGMA 2001** — Fundamental rating factors for spur and helical gear teeth
- **Lewis bending equation** — `σF = Ft·KA·Kv·KFβ·Yε / (b·m·Y)`
- **Hertz contact stress** — `σH = ZH·ZE·Zε·√(Ft·KA·Kv·(u+1)/(b·d₁·u))`
- **Wöhler S-N fatigue** — `N = 3×10⁶ × (σlim/σ)^mW`
- **Involute geometry** — `x = rb(cos t + t·sin t)`, `y = rb(sin t − t·cos t)`

---

## Files

```
index.html     — The complete app (self-contained, no dependencies)
README.md      — This file
LICENSE        — MIT licence
_config.yml    — GitHub Pages site title
```

---

## Licence

MIT — free to use, modify, and share.
