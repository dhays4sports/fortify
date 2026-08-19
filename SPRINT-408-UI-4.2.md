# 408-UI-4.2 — Homepage Editorial Convergence

## Status
COMPLETE — EDITORIAL CONVERGENCE / BEHAVIOR-PROTECTED

## Input baseline
`408-UI-4.1 — Editorial Platform Foundation`.

## Objective
Make `/` the master UI-4 editorial template while preserving the strongest conversion identity and routing contracts from UI-3.2.1.

## Implemented
- Added `shared/homepage-editorial.css`.
- Added the UI-4.2 homepage meta/style marker.
- Recomposed the homepage hero into the UI-4 three-zone grammar:
  1. editorial Coverage Review proposition,
  2. contextual home photography,
  3. situation-first working action panel.
- Retained **Insurance That Fits.** and **Start with a Coverage Review. Not a quote.**
- Kept the hero primary CoverageFit launch and the full six-path `What brought you here today?` chooser.
- Added a dedicated Dylan relationship band directly after the hero.
- Flattened the full situation chooser, CoverageFit story, reasons, Professional Programs preview, and agent close toward editorial sections rather than dashboard chrome.
- Kept Home / Home + Auto / Buyer / Life coverage routes visually secondary to situation-first routing.
- Preserved Local as a separate community program with its existing no-insurance-purchase boundary.
- Corrected the homepage script order so `ui-3-foundation.js` executes before `editorial-platform.js`, allowing the UI-4 header refinement to operate against the actual universal navigation in production.

## Protected behavior
Unchanged:
- CoverageFit homepage launcher and `data-cf-*` contract
- all pre-existing homepage destinations
- all pre-existing tracked anchor tuples
- six certified situation routes
- four certified secondary coverage routes
- CoverageFit explanation and score destination
- Professional Program destinations
- Local attribution links
- contact phone/SMS/email destinations
- campaign context behavior
- `_worker.js`, `_routes.json`, 408-INFRA-1.1
- all non-homepage public HTML
- Life/Life Ops

## Claims boundary
The mockup family remains visual direction only. UI-4.2 does not introduce carrier-shopping, guaranteed savings, guaranteed discount, unverified tenure, or turnaround claims.

## QA
New sprint suites:
- `qa/test-408-ui-4.2.py`
- `qa/test-408-ui-4.2-browser.py`

The release also reruns the UI-3.2.1 identity/source suite, UI-3.12 E2E regression, static regression, INFRA Function-boundary suite, link checks, and JavaScript syntax checks where applicable.

## Next sprint
**408-UI-4.3 — Home + Bundle Editorial Convergence**
