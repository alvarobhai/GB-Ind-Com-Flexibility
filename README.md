# GB Non-Domestic Flexibility Explorer — V12

A static GitHub Pages dashboard for exploring GB non-domestic consumer-led flexibility potential by DNO, sector, segment and end-use.

## V12 changes
- Removed all GHD branding/references from the page header.
- Replaced the previous image/hotspot workaround with the **official NESO GB DNO licence-area geometry** supplied in the NESO 2024 GeoJSON dataset.
- Converted the supplied EPSG:27700 geometry into a lightweight embedded SVG representation for reliable GitHub Pages rendering.
- DNO regions remain visible when one or more are selected; unselected regions fade rather than disappear.
- Multiple DNO regions can be selected by clicking them.
- DNO shading reflects the selected flexibility potential; selected regions are highlighted.
- Technical/Economic selection remains a single-select control.

## Data
The analytical dataset is in `data/data.json`.

The DNO map geometry is embedded directly in `index.html` so the dashboard has no runtime dependency on an external map server or GeoJSON endpoint.

Source geometry: NESO, GB DNO licence areas 20240503, supplied as `gb-dno-license-areas-20240503-as-geojson.geojson`.

## Deployment
Place `index.html`, `README.md`, and the `data/` folder at the repository root and enable GitHub Pages from the repository's main branch/root folder.
