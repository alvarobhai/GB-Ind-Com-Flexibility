# GB Industrial & Commercial Flexibility Explorer — V84

Static GitHub Pages dashboard package.

## V84 changes
- Corrected the Selected Networks KPI so the dynamic count is numeric only; `DNO Areas` is a separate white unit label.
- Retained the V83 dashboard terminology and controls.
- GSP polygons continue to use NESO EPSG:27700 boundary data and the same map coordinate system as the DNO map.
- GSP polygons are clipped to their associated DNO licence-area boundary to prevent the GSP layer from spilling outside the underlying GB network map.

## Package
- `index.html` — dashboard application
- `data/data.json` — model data
- `data/gsp_allocation.json` — NESO FES-based DNO-to-GSP allocation

NESO GSP GIS boundaries are approximate geographic feeding-area boundaries and are used for regional modelling.
