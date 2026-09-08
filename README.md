# GB Industrial & Commercial Flexibility Explorer — V85

Static GitHub Pages dashboard package.

## V85 changes
- Corrected the Selected Networks KPI so the dynamic count is numeric only; `DNO Areas` is a separate white unit label.
- Retained the V83 dashboard terminology and controls.
- GSP polygons continue to use NESO EPSG:27700 boundary data and the same map coordinate system as the DNO map.
- GSP polygons use the native DNO map coordinate system with a small calibration offset to improve visual registration against the GB/DNO base map.
- GSP polygons remain clipped to their associated DNO licence-area boundary.
- Trackpad/mouse-wheel zoom sensitivity is reduced by approximately 50% from V84.

## Package
- `index.html` — dashboard application
- `data/data.json` — model data
- `data/gsp_allocation.json` — NESO FES-based DNO-to-GSP allocation

NESO GSP GIS boundaries are approximate geographic feeding-area boundaries and are used for regional modelling.

### V86 QA changes
- GSP allocation loading now performs a strict DNO-by-DNO reconciliation check against the preprocessed FES 2025 shares and does not silently renormalise unmatched GSPs.
- All 14 DNO areas must pass the allocation QA before the GSP view is marked loaded.
- GSP polygon geometry is fitted from the NESO EPSG:27700 envelope to the native DNO SVG envelope rather than using hand-tuned positional offsets.
