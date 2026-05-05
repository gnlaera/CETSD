# Capacity Expansion and Dispatch Prototype v1.03

Single-file browser-only capacity expansion and time-sequential dispatch optimisation prototype.

## Package contents

- `index.html` - the complete browser application.
- `LICENSE.txt` - GNU General Public License version 3.
- `README.md` - deployment and package notes.

## What v1.03 adds

- Keeps the v1.01 storage-dispatch tie-breaker and storage-headroom audit checks.
- Reframes the Renewables.ninja resource download controls around a single **Reference Calendar Year** rather than manual `Date from` and `Date to` fields.
- Keeps hidden `dateFrom` and `dateTo` fields for backwards-compatible save/load JSON, generated as `YYYY-01-01` and `YYYY-12-31` from the selected calendar year.
- Adds a wind **Turbine** dropdown using the current user-supplied Renewables.ninja preset list, with 270 built-in options.
- Adds an optional **Refresh turbine list from Renewables.ninja** control that attempts to load live model metadata from `api/models` in the browser. If this is blocked by network or cross-origin restrictions, the full built-in v1.03 fallback list remains active.
- Preserves saved custom turbine values if a setup JSON contains a turbine string that is not in the built-in or live dropdown list.

## Operating model

The app is intended for learning, screening and subcommercial planning. It runs in a modern browser and uses HiGHS JavaScript/WebAssembly loaded by the browser. No local Python or local server is required for normal use.

The preloaded example remains the compact embedded v0.51 mini-grid case. The app shell is v1.03.

## Resource-profile workflow

Use **Resource profiles** to select a location, dataset, Reference Calendar Year, solar assumptions and wind assumptions. The PV and wind CSV buttons generate Renewables.ninja point-download URLs for the selected full calendar year.

The calendar-year dropdown is preset from 1980 to 2025 as a practical UI range for MERRA-2-style weather-year framing. Renewables.ninja account, dataset and service limits still apply. The app does not embed API tokens.

## Deployment

For Netlify, deploy the repository or ZIP root containing `index.html`, `LICENSE.txt` and `README.md`. No build command is required. Set the publish directory to the folder containing `index.html`.

## Licence and attribution

The tool is provided under GPL-3.0-or-later. The embedded PLEXOS-World demand-profile reconstruction retains attribution to Brinkerink and Deane, PLEXOS-World 2015, Harvard Dataverse, DOI `10.7910/DVN/CBYXBY`.

Do not publish saved setup JSON files that contain confidential demand traces, costs, locations, capacities or commercial assumptions.
