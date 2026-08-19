# UI4_10 Deployment Smoke Runbook

## Purpose
Validate that the deployed Cloudflare production environment is actually serving the 408-UI-4.10 certified package and that external/runtime boundaries behave as expected. Build certification alone cannot prove deployment state or third-party acceptance.

## Precondition
Deploy the **408-UI-4.10 ROOT_DEPLOYABLE** archive contents at the site root without nesting the archive directory.

## 1. Static shell + assets
- Open `https://408farmers.com/` in a clean/private browser session.
- Confirm the UI-4 editorial Homepage renders, navigation works, Dylan contact actions are visible, and there is no horizontal overflow on phone and desktop.
- Open `/home/`, `/auto-bundle/`, `/buyer/`, `/healthcare/`, `/teachers/`, `/tech/`, `/engineers/`, `/local/`, `/contact/`, and `/score/`.
- Confirm key images/styles load with no 404s in DevTools Network.
- Confirm `/robots.txt` and `/sitemap.xml` return normally.

## 2. Cloudflare static / Function invocation boundary
- Confirm ordinary static pages/assets do not invoke the Pages Function unexpectedly.
- Confirm intended `/api/*` requests reach `_worker.js`.
- Confirm a random nonexistent static route returns the expected static/404 behavior rather than looping through the Function.
- Confirm `_routes.json` in the deployed project matches the certified artifact.

## 3. Home + deep/QR routes
- Open the canonical `/home/` page directly.
- Open at least one certified deep/campaign route and one QR flyer route used in production.
- Confirm no redirect loop, missing asset, or unexpected query stripping.
- Confirm campaign-specific presentation appears only for the current entry and evergreen presentation returns on a clean organic visit.

## 4. Lead submission canary
Use test/contact data that is clearly marked as a deployment canary and remove/archive it after verification.

- Submit Home and confirm success is shown only after the network boundary succeeds.
- Verify the producer/Formspree destination receives the canary with correct production timestamp/context.
- Submit Home + Auto and Buyer canaries if production operations permit.
- Confirm no duplicate lead is created from one submission.
- Confirm consent remains required.

## 5. Post-lead + CoverageFit
- After a successful non-Life lead, complete the short post-lead engagement path.
- Confirm CoverageFit is presented as an explicit optional continuation rather than an automatic redirect.
- Choose Finish for Now and verify the lead remains complete without redirect.
- On a second canary, explicitly choose Continue to CoverageFit and verify the expected handoff opens with retained non-sensitive context and no second 408FARMERS lead submission.

## 6. Professional Programs
- Open Healthcare, Teachers, Technology, and Engineers on phone width.
- Confirm the professional switcher scrolls internally without document-width overflow.
- Submit one professional canary if operationally appropriate and confirm profession context/attribution arrives correctly.

## 7. Local
- Open `/local/` and confirm the catalog loads.
- Open the active merchant detail/perk route and confirm the perk remains available independently of insurance.
- Exercise show-your-screen redemption behavior without creating an insurance gate.
- Open `/local/join/`; if operationally permitted, send a clearly marked merchant-application canary and confirm the Worker transport succeeds.
- Verify an optional Local → insurance transition carries Local attribution without changing the perk/redemption state.
- Remember: the planned three-merchant Local pilot remains operational **NO-GO** until the documented real Auto + Home merchant/external closeout requirements are satisfied.

## 8. Life exact-preservation smoke
- Open `/life/` and confirm the existing Life campaign/application experience is unchanged.
- Start but do not unnecessarily complete a real application; confirm the secure application boundary is the one invoked.
- Confirm no UI-4 non-Life editorial/accessibility stylesheet was injected into Life or Life Ops.
- Open `/life-ops/` only with appropriate producer access and confirm the workspace renders normally.

## 9. Accessibility/device spot check
- Keyboard through Homepage, Home, one Professional Program, Local, and Contact; confirm skip navigation and visible focus.
- On an iPhone/Safari or equivalent physical device, confirm safe-area header/footer behavior, 16px form controls, 44px targets, and no sticky UI covers required disclosures.
- If available, perform a VoiceOver/NVDA spot check on Homepage + one form route.

## 10. Production closeout
Record:
- deployment identifier/commit
- deployment timestamp
- tester/device/browser
- canary submissions used and cleanup status
- any Cloudflare Function/log anomalies
- result for each section above

Only after this smoke is green should the deployment be described as **production-activated**. Until then, the artifact status remains **deployable-build certified**.
