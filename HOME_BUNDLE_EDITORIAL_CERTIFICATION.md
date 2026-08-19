# 408-UI-4.3 — Home + Bundle Editorial Certification

**Status:** PASS / ROOT-DEPLOYABLE

## Certified result
`/home/` and `/auto-bundle/` now use the UI-4 editorial composition while preserving their certified insurance workflows.

### Home
- organic hero: **Start with a home coverage review.**
- existing campaign/flyer/QR nodes remain authoritative for explicit campaign entries
- contextual home photography
- existing progressive Home intake in the action panel
- Dylan relationship band
- editorial support: **What Dylan looks at / How the review works / What happens next**

### Home + Auto
- organic hero: **Let’s look at home and auto together.**
- existing campaign-entry nodes remain authoritative for explicit campaign entries
- context-only home/vehicle image crop without baked-in ad copy
- existing Home + Auto form in the action panel
- Dylan relationship band
- editorial support: **Why review both together / How Dylan reviews your household / What to expect next**

## Behavior boundary
The Home and Bundle `#leadForm` blocks are exact to the UI-4.2 input. Progressive intake, renter branching, Formspree, consent, attribution, deep routing, post-lead, CoverageFit, Workers, `_routes.json`, INFRA-1.1, and Life remain protected.

## QA
- UI-4.3 source/behavior: **140/140**
- UI-4.3 browser/responsive: **174/174**
- UI-4.3 campaign continuity: **10/10**
- UI-4.2 homepage browser: **129/129**
- UI-3.12 E2E: **59/59**
- static regression: **296/296**
- INFRA-1.1 boundary: **22/22**
- Home submit hotfix: **12/12**
- Home routing: **16/16**
- Home deep-route assets: **12/12**
- campaign accessibility delta: **56/56**
- runtime JS syntax: **42/42**
- internal links/assets: **770 checked, 0 broken**

## Next locked sprint
**408-UI-4.4 — Buyer Editorial Convergence**
