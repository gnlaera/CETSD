# Capacity Expansion and Dispatch Prototype v0.99

Single-file browser-only capacity expansion and time-sequential dispatch optimisation prototype.

## Package contents

- `index.html` - the complete browser application.
- `LICENSE.txt` - GNU General Public License version 3.
- `README.md` - deployment and package notes.

## What v0.99 adds

- Keeps the v0.98 linked cash-cost and merit-order workflow.
- Improves the persistent bottom day-time slicer so controls wrap dynamically within the Results pane instead of being squeezed out.
- Preserves the pivot-chart-style timeline band and resize handles in the persistent slicer.
- Adds `Export finance CSV` for the `Discounted annual cash flow and system-wide P&L` section.
- The finance export includes:
  - finance summary,
  - system-wide P&L,
  - annual discounted cash-flow table,
  - target-IRR tariff / finance LCOE,
  - tax, depreciation, fixed cost and variable cash-cost assumptions.

The finance layer is post-processing only. It does not change the capacity expansion objective, dispatch formulation, constraints or solver class.

## Operating model

The app is intended for learning, screening and subcommercial planning. It runs in a modern browser and uses HiGHS JavaScript/WebAssembly loaded by the browser. No local Python or local server is required for normal use.

The preloaded example remains the compact embedded v0.51 mini-grid case. The app shell is v0.99.

## Deployment

For Netlify, deploy the repository or ZIP root containing `index.html`, `LICENSE.txt` and `README.md`. No build command is required. Set the publish directory to the folder containing `index.html`.

## Licence and attribution

The tool is provided under GPL-3.0-or-later. The embedded PLEXOS-World demand-profile reconstruction retains attribution to Brinkerink and Deane, PLEXOS-World 2015, Harvard Dataverse, DOI `10.7910/DVN/CBYXBY`.

Do not publish saved setup JSON files that contain confidential demand traces, costs, locations, capacities or commercial assumptions.
