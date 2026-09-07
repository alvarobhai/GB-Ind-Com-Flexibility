# GB CLF GitHub Pages Dashboard v2

This is a static, client-side dashboard. It requires only `index.html` and the `data/` folder.

## Publish / replace the existing version

Replace the files in the GitHub repository with:
- `index.html`
- `data/data.json`
- `data/CLF_Dashboard_Data.csv`

Do not put them inside an additional subfolder.

## Why v2

The first prototype depended on external mapping/chart JavaScript at initialisation. This version has **no external JavaScript dependency for core functionality**:
- local JSON data
- native HTML/CSS
- inline SVG map
- inline SVG marginal cost curve

This should eliminate the blank-page problem on GitHub Pages.

## Scope

DNO → Sector → Archetype → End-use → Technical Flex MW → Hurdle Cost → Economic Flex MW.

No achievable potential.

## Dashboard

- Sector filter
- Archetype filter
- End-use filter
- Technical / Economic
- £150–£1,000/MWh hurdle-cost slider
- Clickable DNO map
- DNO/archetype/end-use charts
- Indicative marginal cost curve
- Detail table
- URL state preservation

## DNO map note

The current map is a **schematic interactive DNO-area representation** designed to make the dashboard robust on GitHub Pages. The analytical DNO values are the model's DNO allocations.

For the next visual iteration, replace the schematic with the official NESO DNO polygon GeoJSON after confirming the field-name and projection handling.


### Map note
The dashboard uses simplified geographic DNO area shapes for the static client-side map. The authoritative NESO DNO licence-area dataset is the source reference for geography; NESO notes that licence boundaries are approximate and can change over time.

## DNO geography
The dashboard uses a WGS84 GeoJSON snapshot of GB DNO licence-area boundaries. The geometry was taken from Jacob Varley's February 2026 public GeoJSON gist, which notes that it was taken directly from the City Observatory Birmingham source with minor naming amendments. NESO is the authoritative source for the GB DNO licence-area dataset and describes its boundaries as approximate; see the NESO GIS dataset page for the official source.


## V6 update
- Compact selection boxes: smaller text and tighter vertical spacing.
- Filter behaviour and independent Sector/Segment/End-use dimensions are preserved.
- FES scenario/year functionality remains the basis for projected demand; FES does not determine flexibility capacity.
- Intended geography architecture: GB → DNO → GSP.


## V7 update
- Removed all explicit “All” options from Sector, Segment and End-use menus.
- Sector, Segment and End-use are independent multi-select dimensions; all items are selected by default.
- Replaced the schematic DNO polygons with the authoritative NESO 2024 DNO licence-area GeoJSON loaded from the NESO data portal.
- Sector selection does not change the Segment or End-use lists; it only filters the results.


## V9 update
- DNO map reprojects NESO EPSG:27700 geometry to WGS84 before rendering, avoiding distorted/slanted geometry.
- All DNO regions remain visible; selected regions are highlighted and unselected regions fade rather than disappearing.
- Multiple DNO regions can be selected simultaneously.
- Sector/Segment/End-use selection controls now use a single square indicator; visual state updates immediately on deselection.
