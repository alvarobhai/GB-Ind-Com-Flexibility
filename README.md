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
