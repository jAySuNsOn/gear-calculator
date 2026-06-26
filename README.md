# Gear Teeth Calculator

Full-featured spur and bevel gear engineering calculator. Runs entirely in the browser — no install, no server, no account.

**Live app:** https://jaysunson.github.io/gear-calculator/

---

## Features

**7 tabs:** Gear Ratio · Module/Pitch · Compound Gearing · Bevel Gears · Stress & Fatigue · Drawing · Export

**Auto data sync:** Values entered in Module/Pitch and Compound tabs automatically populate Stress & Fatigue, Drawing, and Export tabs.

**Stress & Fatigue Analysis (ISO 6336):**
- Bending stress σF and contact stress σH per stage
- Safety factors with SAFE / MARGINAL / UNSAFE colour coding
- Minimum face width solved from both bending and contact limits
- Fatigue life via Wöhler S-N (bending mW=6.35, contact mW=3.33)
- 19 materials: Cast Iron, Carbon Steel 160–300HB, S355, 50B, En8, En9, En19T, En24, En36, Alloy Steel case-hrd/nitrided, Bronze, Nylon, POM

**Engineering Drawing:** True involute tooth geometry, front and section views, dimensioned with title block, optional keyway.

**CAD / CNC Exports (all client-side):**

| Format | Use |
|--------|-----|
| .DXF | AutoCAD, LibreCAD, Fusion 360 |
| .SVG | Laser cutting, Inkscape |
| .NC | CNC lathe G-code |
| .STL | 3D printing |
| .STEP | FreeCAD, SolidWorks, CATIA |
| .CSV | Involute profile coordinates |
| PDF | Full design report — all tabs, all calculations |

---

## Files

```
index.html   — Complete app (self-contained, 86KB)
README.md    — This file
LICENSE      — MIT
_config.yml  — GitHub Pages config
```

**Standards:** ISO 21771 · ISO 6336 · AGMA 2001 · Lewis · Hertz · Wöhler S-N

**Licence:** MIT
