# Capacity Expansion and Time-Sequential Dispatch Learning Model v1.59.4

## Purpose
A single-file browser-only learning model for linear capacity expansion and hourly dispatch. It is intended for education, screening-level analysis and strategy framing. It does not require a local Python install.

## Quick start
1. Open the HTML file in a modern browser.
2. Use Start here for the first-run workflow.
3. Use Dashboard to run the embedded Mini-grid case.
4. Use Grid Load Builder, Resource profiles, Network, Technology Candidates and Settings to review inputs.
5. Read Results in this order: Outcome, Build & energy, Cost, Network & storage, Dispatch, Export QA, Audits, Saved and Finance.
6. Use Fixed system comparator, Scenarios, Flat-world and Stress for comparison workflows.

## Settings and transparency
Settings includes reliability constraints, storage settings, solver settings and the Generated LP preview. The Generated LP preview remains available for learning, external inspection and troubleshooting. Internal model-build acceptance panels are hidden from the public workflow.

## Model boundary
The model is a linear transport abstraction. It includes demand, candidate supply, storage, external grid interface, transport links, losses, build limits, reliability penalties and selected constraints. It excludes unit commitment, alternating-current power flow, security-constrained dispatch, binary build decisions, market price formation, nodal pricing, reserves, frequency and voltage stability. Outputs are screening-grade evidence, not a bankable design or investment approval.

## Data and attribution
The embedded demand-profile reconstruction is derived from PLEXOS-World 2015, Brinkerink and Deane (2020), Harvard Dataverse, DOI 10.7910/DVN/CBYXBY. The app is open-source under GPL-3.0-or-later.

## Solve engine
The default active solve path is the browser-native canonical LP builder solved through HiGHS JavaScript/WebAssembly. Internal model-build audit panels are hidden from the public interface to keep the learning workflow simple.

## Deployment hygiene
Publish the generic HTML app only. Do not publish saved setup JSON files containing confidential locations, costs, demand traces, capacities or commercial assumptions.
