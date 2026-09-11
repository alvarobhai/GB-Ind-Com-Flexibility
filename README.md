# GB Industrial & Commercial Flexibility Explorer — V90

Static GitHub Pages dashboard package.

## V90 update
- Updated dashboard model data to the current formulaic CLF case.
- Current technical flexibility totals are approximately **4.06 GW Industrial + 2.69 GW Commercial = 6.74 GW GB C&I**.
- Industrial and commercial DNO-level results are carried through to the dashboard using the current V6 model outputs.
- Retained the V89 dashboard interface, controls, DNO/GSP map behaviour and NESO GSP geographic layer.
- GSP allocation remains based on FES 2025 Building Blocks 2024 electricity demand shares within each DNO.
- GSP flexibility is an indicative spatial disaggregation of DNO flexibility; it is not an independently modelled GSP flexibility potential.

## Package
- `index.html` — dashboard application
- `data/data.json` — current formulaic CLF model data at Sector × End-use × DNO level
- `data/gsp_allocation.json` — FES 2025-based DNO-to-GSP allocation

NESO GSP GIS boundaries are approximate geographic feeding-area boundaries and are used for regional modelling.

## Economic interpretation
End-user hurdle costs represent the compensation required by the end-user. The dashboard assumes a 25% allowance for aggregator margin and market-access costs on top of these hurdle costs when assessing economic potential.
