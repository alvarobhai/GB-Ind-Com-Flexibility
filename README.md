# GB Industrial & Commercial Flexibility Explorer — V88

Static GitHub Pages dashboard package.

## V88 update
- Recalibrated technical flexibility using the aggressive technical potential case documented in `CLF_Technical_Potential_Aggressive_Calibration_V1.xlsx`, targeting the question: can the equipment technically be shut off or partially turned down on request?
- Technical potential now totals approximately 7.56 GW across GB C&I.
- Renamed the economic control from **Economic Potential Threshold** to **Flexibility Procurement Cost**.
- Default procurement-cost slider position is set to the low-screen starting point.
- Economic screening now applies a 25% uplift to end-user hurdle costs to estimate delivered/procurement cost: `procurement cost = end-user hurdle cost × 1.25`.
- Added the agreed explanatory text under the procurement-cost control.
- The selected £/MWh value is used as the economic screen to determine economic flexibility potential.
- Retained the V87 GSP QA/rendering behaviour and map controls.

## Package
- `index.html` — dashboard application
- `data/data.json` — model data
- `data/gsp_allocation.json` — NESO FES-based DNO-to-GSP allocation

NESO GSP GIS boundaries are approximate geographic feeding-area boundaries and are used for regional modelling.

## Economic interpretation
End-user hurdle costs represent the compensation required by the end-user. The dashboard assumes a 25% allowance for aggregator margin and market-access costs on top of these hurdle costs when assessing economic potential.
