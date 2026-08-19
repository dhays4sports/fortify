# 408-UI-4.10 — Functional Regression + Production Certification

## Status
COMPLETE — DEPLOYABLE-CERTIFIED UI-4 BASELINE

## Input baseline
408-UI-4.9 — Accessibility + Performance Certification.

## Objective
Freeze the completed UI-4 non-Life editorial presentation and certify the full 408FARMERS package for production deployment without reopening protected behavior or the excluded Life product.

## Product freeze
4.10 introduces no customer-facing HTML, CSS, JavaScript, Worker, routing, data, image, form, attribution, CoverageFit, Local, or Life changes.

The 4.9 input was frozen before certification:
- deployable/runtime product files: **223/223 exact**
- Life/Life Ops + shipped Life assets/runtime: **14/14 exact**
- infrastructure boundary files: **4/4 exact** (`_worker.js`, `_routes.json`, `_headers`, `_redirects`)
- critical handoff/attribution/data files: **12/12 exact**

Only release metadata, roadmap/changelog documentation, QA, and certification artifacts are added/advanced in 4.10.

## Functional regression certified
### Homepage
- UI-4.9/4.8 rendered composition and accessibility remain green.
- Core Home, Home + Auto, Buyer, Life, Local, and professional destinations remain intact.

### Home / deep routes / campaigns
- Same-origin lead submission and Formspree fallback remain exercised by the cross-journey E2E suite.
- Advanced Mode pretty-path routing: **16/16**.
- Deep-route asset resolution: **12/12**.
- Advanced Mode redirect-loop hotfix: **10/10**.
- Hidden-required-control submission hotfix: **12/12**.
- Current campaign-entry contract: **10/10**.

### Home + Auto
- Submission, housing context, attribution, post-lead state, and explicit optional CoverageFit behavior remain covered by the **59/59** cross-journey E2E regression and exact 4.9 product freeze.

### Buyer / referrals
- Buyer submission, referral parser, closing context, partner attribution, and CoverageFit handoff remain covered by the current cross-journey E2E regression and exact 4.9 product freeze.

### Professional Programs
- Healthcare, Teachers, Technology, and Engineers remain rendered and responsive under the current UI-4 suites.
- Their form markup/runtime is preserved by the 4.9 input freeze and cross-journey submission regression.

### Local
- Directory/catalog rendering, detail/perk behavior, redemption, join transport, and optional insurance attribution remain covered by the cross-journey E2E suite.
- Local source contract: **86/86**.
- Merchant Join Worker: **20/20**.
- Local Attribution Worker: **29/29**.
- LOCAL-1.10 operational NO-GO remains unchanged pending the real Auto + Home merchants and external closeout items.

### Relationship / completion
- UI-4.7 relationship/completion source/browser regressions remain **142/142 + 110/110**.
- UI-4.8 responsive regression remains **161/161 + 256/256**.

### CoverageFit handoffs
- Cross-journey E2E: **59/59**.
- FLOW-2.4 explicit invitation runtime: **5/5**.
- FLOW-2.5 runtime regression exits cleanly.
- The full sender-side handoff/engagement/launcher files are exact to 4.9.
- No automatic continuation is reintroduced.

### Workers / routing / INFRA-1.1
- INFRA-1.1 function/static boundary: **22/22**.
- INFRA-1.1 exact preservation: **4/4**.
- `_worker.js`, `_routes.json`, `_headers`, and `_redirects` are byte-identical to 4.9.

### Life exact preservation
Life remains explicitly excluded from UI-4. The complete shipped Life/Life Ops surface used by the package—three HTML surfaces, Life CSS/JS modules, and campaign imagery—is **14/14 byte-identical** to the 4.9 input.

The current Life browser behavior regression remains **19/19**. A historical LIFE-1.7 source test is not a current release gate because its first assertion only recognizes old top-level VERSION values through FLOW-2.5; it therefore rejects every later UI generation before evaluating the actual Life behavior. 4.10 uses exact-byte preservation plus the current browser regression instead.

## Production certification
- UI-4.9 accessibility/performance source: **374/374**
- UI-4.9 accessibility/reflow browser: **62/62**
- UI-4.9 responsive asset selection: **31/31**
- UI-4.8 source/browser: **161/161 + 256/256**
- UI-4.7 source/browser: **142/142 + 110/110**
- UI-3.12 cross-journey E2E: **59/59**
- static regression: **296/296**
- production metadata: **216/216**
- internal links/assets: **856 checked / 0 broken**
- runtime JavaScript syntax: **44/44**
- INFRA-1.1: **22/22 + 4/4 exact preservation**
- Home routing/deep-route/redirect protections: **38/38**
- Home hidden-required submit: **12/12**
- Local Workers: **49/49**
- Life browser: **19/19**

## Superseded historical harnesses
4.10 does not mutate current product markup to satisfy stale historical assertions:

1. `qa/test-408-ui-3.13-assets.py` reruns at **98/99** solely on the already-approved Home source-budget exception: 323.2 KiB vs the pre-UI-4 300 KiB ceiling. UI-4.9 established the current 330 KiB Home ceiling.
2. `qa/test-408-ui-3.13-browser.py` reruns at **743/749** because six Homepage checks query the retired pre-UI-4 picture-wrapper selector. Current UI-4.8/4.9 browser suites certify the replacement Homepage composition.
3. `qa/test-408-ui-4.6-browser.py` is not used as a current gate because its BeautifulSoup helper crashes while iterating a decomposed `<link>` node. Current 4.8/4.9 browser suites and E2E regression cover the Local surfaces.
4. Older FLOW/CF-RPT/Buyer source suites either whitelist historical top-level VERSION strings or require an adjacent CoverageFit repository. Their current shipped runtime behavior is covered by 4.10's exact-byte freeze, the 59/59 E2E suite, and the FLOW runtime regressions.

These are test-generation compatibility boundaries, not unresolved production defects.

## Deployment boundary
This artifact is **deployable-build certified**, not proof that Cloudflare currently serves these exact bytes. `UI4_10_DEPLOYMENT_SMOKE_RUNBOOK.md` defines the required post-deploy production smoke for static/Function boundaries, forms, QR/deep routes, Local, CoverageFit transitions, and Life.

## Final decision
**PASS — UI-4 COMPLETE / DEPLOYABLE-CERTIFIED / CUSTOMER-FACING PRESENTATION FROZEN.**

Any later customer-facing design change should be an explicitly scoped UI-4 maintenance/hotfix or a new UI generation rather than a silent modification of this baseline.
