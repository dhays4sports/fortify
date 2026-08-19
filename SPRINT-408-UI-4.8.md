# 408-UI-4.8 — Mobile + Responsive Editorial Pass

## Status
COMPLETE

## Input baseline
408-UI-4.7 — Relationship + Completion Editorial Convergence.

## Objective
Translate the UI-4 editorial compositions into deliberate phone/tablet experiences instead of simply stacking desktop regions.

## Delivered
- Added `shared/editorial-responsive.css` as a late-cascade, presentation-only responsive layer.
- Loaded the layer on all 25 non-Life public HTML surfaces with a `ui48-responsive` marker and `data-ui4-responsive="408-UI-4.8"`.
- Restored safe-area-aware mobile header sizing and footer/home-indicator spacing after the UI-4 header refinement.
- Reworked phone hero geometry so context photography remains present but no longer pushes the first working action several screens down.
- Collapsed Dylan relationship bands, editorial columns, action groups, and certified form grids into deliberate phone reading order.
- Preserved 44px+ touch targets and forced 16px mobile form controls to prevent iOS input zoom.
- Added keyboard scroll margins for form fields and kept disclosures in normal flow.
- Converted the Professional Programs family switcher to true internal horizontal scrolling at 320px without document overflow.
- Added explicit 320–359px and short-landscape handling.
- Reserved bottom space for the existing Score fixed mobile CTA so final content and disclosures cannot finish behind it.
- Normalized native `<figure>` margins inside editorial hero grids to eliminate narrow-device overflow.

## Responsive certification matrix
- 320 × 820
- 375 × 812
- 390 × 844
- 768 × 1024
- 844 × 390 short landscape
- 1024 × 768 tablet landscape

## Protected behavior
No change to:
- protected form fields, required semantics, consent, or endpoints
- post-lead events, semantic answers, duplicate safeguards, or CoverageFit invitation behavior
- Campaign Entry Registry, source/campaign/partner attribution, or routing
- Home / Bundle / Buyer branching
- occupational eligibility or discount determination
- Local catalog, redemption, attribution, join behavior, or operational NO-GO
- `_worker.js`, `_routes.json`, `_headers`, `_redirects`, or 408-INFRA-1.1
- pricing, coverage, eligibility, or underwriting logic
- Life / Life Ops

## Acceptance
- no horizontal overflow at certified viewports
- 44px minimum mobile interaction targets
- 16px mobile controls
- safe-area-aware header/footer geometry
- required content/disclosures remain outside fixed-CTA obstruction
- compact responsive context-image crops without moving essential copy into images
- protected forms/infrastructure/Life exact to the UI-4.7 input baseline

## Next
408-UI-4.9 — Accessibility + Performance Certification.
