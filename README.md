# GB Industrial & Commercial Flexibility Explorer — V79

Static GitHub Pages dashboard package.

## Package contents

- `index.html` — dashboard application.
- `data/data.json` — underlying Industrial + Commercial flexibility model data.
- `data/gsp_allocation.json` — NESO FES 2025-based DNO-to-GSP allocation used to regionalise DNO flexibility to GSPs.
- `README.md` — package documentation.

## Current scope

The dashboard covers Industrial + Commercial (C&I) flexibility only. Exogenous additions such as transport, district heating and embedded/self-generation are excluded.

The model flow is:

annual consumption → peak demand → segment peak demand → end-use demand → technical flexibility → economic potential → geographic allocation.

Technical potential is end-use peak demand multiplied by the technical flexibility factor. Economic potential applies the selected economic hurdle/incentive threshold.

GSP results are indicative regionalisation of DNO-level flexibility using NESO FES 2025 demand pathway shares; they are not independently modelled GSP flexibility.

## UI status

- Geography: DNO Region / GSP.
- Potential: Technical / Economic.
- Scenario control is not displayed.
- 2024 is enabled; 2030–2050 are displayed as disabled future options.
- DNO selection changes shading without resetting map pan/zoom.
- GSP view uses polygon boundaries.
- Marginal cost curve uses blue Industrial and green Commercial blocks representing Segment × End-use combinations aggregated across DNOs.
