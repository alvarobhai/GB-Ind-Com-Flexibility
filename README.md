# GB Industrial & Commercial Flexibility Explorer — V92

Static GitHub Pages dashboard package.

## V91 update
- Updated the dashboard to the current formulaic CLF case: **4.055 GW Industrial + 2.687 GW Commercial = 6.742 GW C&I technical flexibility**.
- Replaced the flat £200/MWh hurdle-cost assumption with differentiated **Sector × End-use** costs using the closest matching archetype × end-use values from the previous Industrial V3 and Commercial V1 marginal-cost results.
- The dashboard retains the existing 25% uplift from end-user hurdle cost to delivered/procurement cost.
- Default Flexibility Procurement Cost screen remains £250/MWh; at this screen, economic potential is **1.841 GW**.
- Default DNO Area and GSP map zoom increased from 1.08× to **1.35×** (25% closer).

## Package
- `index.html` — dashboard application
- `data/data.json` — current formulaic CLF data at Sector × End-use × DNO level
- `data/gsp_allocation.json` — FES 2025-based DNO-to-GSP allocation

NESO GSP GIS boundaries are approximate geographic feeding-area boundaries and are used for regional modelling.

## Economic interpretation
End-user hurdle costs represent the compensation required by the end-user. The dashboard assumes a 25% allowance for aggregator margin and market-access costs on top of these hurdle costs when assessing economic potential.


## V92 update
- Moved the DNO Area and GSP maps upward slightly while retaining the 1.35× default zoom.
- Sector, segment and end-use selectors no longer reset the DNO Area selection when changed.
- Each selector retains its own independent selection state; existing filter intersections remain unchanged.
