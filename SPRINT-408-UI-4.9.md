# 408-UI-4.9 — Accessibility + Performance Certification

## Status
COMPLETE — BUILD-CERTIFIED

## Input baseline
408-UI-4.8 — Mobile + Responsive Editorial Pass.

## Objective
Re-certify the image-heavier UI-4 editorial platform against the established WCAG-oriented accessibility and UI-3.13-era performance discipline without reopening protected workflow behavior or Life.

## Accessibility delivered
- Added `shared/accessibility-performance.css` as a late-cascade non-Life hardening layer on all 25 public non-Life HTML surfaces.
- Certified exactly one H1 per page and no forward heading-level skips.
- Certified working skip links/targets on every public non-Life page.
- Certified accessible names for every visible input, select, textarea, and icon-only/button control.
- Certified every public non-Life image has an explicit alt policy; decorative context imagery remains `alt=""` and informative imagery retains meaningful alt text.
- Added current-generation keyboard focus treatment that does not depend on the old `body.ui3-page` scope.
- Preserved native validation and strengthened visible invalid/focus boundaries.
- Moved small gold text to the AA-safe `#8e5f00` token; brighter `#a86f00` remains limited to large display accents where AA-large contrast applies.
- Re-certified reduced-motion and forced-colors behavior directly against the UI-4 body marker.
- Re-certified 320px reflow as the project proxy for 400% desktop zoom and fixed the footer grid min-content issue exposed by adding intrinsic image dimensions.

## Performance delivered
- Added intrinsic width/height reservation to every `<img>` on the 25 non-Life public surfaces.
- Added 320px responsive WebP candidates for:
  - Healthcare professional hero
  - Teacher professional hero
  - Technology professional hero
  - Engineer professional hero
  - Local community context image
- Recompressed `auto-bundle-editorial-320.webp` from roughly 74 KiB to **45,434 bytes** while preserving the certified crop.
- Added `408-farmers-logo-white-506.webp` and applied responsive 506/1014 source sets to shipped 408FARMERS PNG identity marks.
- Existing dark logo uses the previously shipped 506px WebP candidate.
- Removed `fetchpriority="high"` from the Home header logo; actual image-led heroes are now the only high-priority image on their route.
- Chromium source-selection certification confirms the mobile candidate at 390px for Homepage, Home, Bundle, Buyer, all four Professional Programs, Local, and Local Join.

### Mobile asset results
| Asset | Narrow bytes | Full/current bytes | Reduction |
| --- | ---: | ---: | ---: |
| Home + Auto editorial | 45,434 | 116,282 | 60.9% |
| Healthcare | 10,994 | 36,064 | 69.5% |
| Teachers | 19,452 | 65,042 | 70.1% |
| Technology | 10,888 | 36,166 | 69.9% |
| Engineers | 15,676 | 45,790 | 65.8% |
| Local context | 19,398 | 51,678 | 62.5% |

## Source budget decision
The UI-3.13 production certification used a 300 KiB uncompressed CSS+JS ceiling for primary routes. Subsequent protected HOME/FLOW/UI work added mandatory runtime and presentation layers. In the 4.9 build:

- Homepage: 194.9 KiB
- Home: **323.2 KiB**
- Home + Auto: 263.3 KiB
- Buyer: 287.9 KiB
- each Professional Program: 278.4 KiB
- Local directory: 248.8 KiB
- Local Join: 213.8 KiB

All primary routes remain below 300 KiB except Home. Home is explicitly grandfathered at **330 KiB** for UI-4 (current 323.2 KiB). This is the documented justification allowed by the 4.9 acceptance criteria: removing the accumulated HOME/FLOW/UI layers would violate the frozen behavior and continuity contracts. 4.9 adds **no JavaScript**.

As a result, the historical `qa/test-408-ui-3.13-assets.py` rerun is **98/99** solely because it still asserts the old 300 KiB Home ceiling. Its other 98 asset/performance checks remain green. The current-generation 4.9 source contract is green under the explicit 330 KiB Home ceiling.

## Protected behavior
No change to:
- protected form markup, field names, required semantics, consent, or endpoints
- post-lead events, semantic answers, duplicate safeguards, or CoverageFit invitation behavior
- Campaign Entry Registry, source/campaign/partner attribution, or routing
- Home / Bundle / Buyer branching
- occupational eligibility or discount determination
- Local catalog, redemption, attribution, join behavior, or operational NO-GO
- `_worker.js`, `_routes.json`, `_headers`, `_redirects`, or 408-INFRA-1.1
- pricing, coverage, eligibility, or underwriting logic
- Life / Life Ops

## Certification
- 408-UI-4.9 source accessibility/performance contract: **374/374**
- 408-UI-4.9 accessibility/reflow Chromium: **62/62**
- 408-UI-4.9 responsive asset-selection Chromium: **31/31**
- 408-UI-4.8 source/browser regression: **161/161 + 256/256**
- 408-UI-4.7 source/browser regression: **142/142 + 110/110**
- UI-3.12 cross-journey E2E: **59/59**
- Static regression: **296/296**
- Internal links/assets: **856 checked / 0 broken**
- JavaScript syntax: **44/44**
- INFRA-1.1 Function boundary: **22/22**
- INFRA-1.1 exact preservation: **4/4**
- Home routing: **16/16**
- Home hidden-required submit: **12/12**
- Local attribution Worker: **29/29**
- Historical UI-3.13 asset/performance rerun: **98/99**, with the single documented Home source-budget exception above.

## Certification boundary
This is a build-level automated certification. It does not claim deployed-domain Lighthouse/RUM results, Safari/Firefox accessibility-tree behavior, or physical VoiceOver/NVDA/touch-device testing. Those remain deployment/activation checks, not evidence that can be produced from the local artifact alone.

## Next
408-UI-4.10 — Functional Regression + Production Certification.
