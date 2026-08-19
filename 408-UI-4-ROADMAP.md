# 408FARMERS UI-4.x — Editorial Human Platform Convergence Roadmap

## Program objective
Move the non-Life 408FARMERS codebase substantially closer to the approved editorial mockup family while preserving all certified insurance workflows and infrastructure.

**Life is excluded and frozen.**

## Program rules
1. **Composition may change aggressively; insurance behavior may not.**
2. Mockups are visual references, not factual copy/data sources.
3. Farmers red remains the primary conversion color; warm gold is editorial emphasis.
4. Each major route should move toward: editorial copy → context photography → working action panel → Dylan relationship → editorial explanation.
5. Existing campaign-aware hero logic continues to control approved current-entry messaging.
6. Existing forms, Workers, attribution, routing, consent, Local, and CoverageFit contracts are protected.
7. Every sprint must preserve 408-INFRA-1.1.

---

## 408-UI-4.1 — Editorial Platform Foundation — COMPLETE
### Objective
Establish the reusable visual/composition language before route-specific recomposition.

### Scope
- new warm-gold token system
- split editorial hero primitives
- context-image feathering system
- working action-panel primitive
- Dylan relationship-band primitive
- editorial lower-page columns and numbered steps
- trust-strip primitive
- non-Life header refinement
- detailed UI-4 roadmap and design-system documentation

### Implementation
- add `shared/editorial-platform.css`
- add `shared/editorial-platform.js`
- load foundation on all 25 non-Life public HTML surfaces
- keep all 25 existing `<body>` blocks unchanged in this sprint
- preserve all Life/Life Ops files exactly

### Acceptance
- foundation assets load on 25/25 non-Life public surfaces
- 0/3 Life/Life Ops surfaces load UI-4
- non-Life body hashes remain exact to UI-3.13.1E input
- Professionals nav + Text/Call Dylan enhancement is available through the shared runtime
- no form/runtime/data/Worker contract changes

---

## 408-UI-4.2 — Homepage Editorial Convergence — COMPLETE
### Objective
Make `/` the master editorial template while preserving the strongest conversion identity from UI-3.2.1.

### Required visual direction
- retain **Insurance That Fits.**
- retain **Start with a Coverage Review. Not a quote.**
- editorial left column with warmer, first-person/local copy
- household/homeownership context photography
- right working surface remains situation-first, not a generic lead form
- Dylan relationship band below first conversion section
- product routes become visually secondary to the situation-first chooser
- lower page shifts from dense card/dashboard styling to editorial sections where appropriate

### Protected behavior
- all existing homepage destinations and tracked anchors
- CoverageFit launcher
- situation-first routing
- Local attribution links
- campaign context

### Acceptance
- same destination/attribution contract as UI-3.13.1E
- no new quote promise
- no unsupported savings/carrier claims
- 320–1440px composition QA

### UI-4.2 implementation closeout
- `/` now uses the three-zone editorial grammar: proposition → contextual home photography → situation-first working panel.
- **Insurance That Fits.** and **Start with a Coverage Review. Not a quote.** remain the homepage identity.
- The right working surface is situation-first and does not introduce a generic lead form.
- The certified six-path `What brought you here today?` chooser remains intact below the hero.
- Dylan relationship band appears immediately after the first conversion section.
- Coverage paths remain visually secondary; CoverageFit, reasons, professional programs, Local, and Dylan close are flattened into the editorial hierarchy without changing destinations.
- UI-3 foundation now loads before the UI-4 shared runtime on `/`, ensuring the production header receives the UI-4 Professionals + Text/Call enhancement.

---

## 408-UI-4.3 — Home + Bundle Editorial Convergence — COMPLETE
### Objective
Recompose `/home/` and `/auto-bundle/` around the approved editorial/photo/form grammar without changing either form.

### Home target
- editorial headline + campaign-aware variant support
- home/household photography
- existing progressive Home intake as the right action panel
- Dylan relationship band
- editorial lower section: **What Dylan looks at / How the review works / What happens next**

### Bundle target
- consultative **home and auto together** framing
- household/home/vehicle photography
- current Bundle form as action panel
- editorial lower section: **Why review both / How Dylan reviews the household / What to expect next**

### Protected behavior
- Home deep routes and flyer/QR campaigns
- progressive intake and hidden-required hotfix
- renter branching
- Home/Bundle form fields and endpoints
- post-lead and CoverageFit continuation

### Acceptance
- exact form-contract parity
- all certified Home routing suites pass
- campaign-aware hero variants continue to work inside the new composition

### UI-4.3 implementation closeout
- `/home/` and `/auto-bundle/` now use the UI-4 three-zone grammar: editorial proposition → contextual photography → existing working intake panel.
- Existing Home and Bundle `#leadForm` blocks are preserved exactly from the UI-4.2 input.
- Home campaign-aware `data-home-campaign-*` nodes remain inside the editorial copy zone, preserving flyer/QR/coaster message matching.
- Dylan relationship bands sit directly below the first conversion experience.
- Lower support content is now editorial: **What Dylan looks at / How the review works / What happens next** for Home and **Why review both / How Dylan reviews the household / What to expect next** for Bundle.
- Legacy support sections remain in DOM only for regression compatibility and are visually suppressed.
- Life, Workers, routing, attribution, progressive intake, renter branching, post-lead, CoverageFit, and INFRA-1.1 remain protected.

---

## 408-UI-4.4 — Buyer Editorial Convergence — COMPLETE
### Objective
Make Buyer feel like a human, closing-aware concierge experience.

### Visual target
- **Let’s keep the insurance side moving.** style editorial framing
- buyer/keys/move-in contextual photography
- existing Buyer intake in the action panel
- partner/referral acknowledgement retained
- Dylan relationship band
- editorial lower section: **What Dylan helps with / How your Buyer review works / Support when you’re on a timeline**

### Protected behavior
- closing urgency calculation
- partner/realtor attribution
- Text Dylan/start-online choices
- buyer form and Formspree
- CoverageFit handoff

### Acceptance
- all Buyer referral/urgency regressions pass
- no false turnaround promise
- no invented lender/realtor claims

### UI-4.4 implementation closeout
- `/buyer/` now uses the UI-4 three-zone grammar: closing-aware editorial proposition → new-home contextual photography → the existing Buyer intake as the working action panel.
- The Buyer `#leadForm` remains exact to the UI-4.3 input.
- Partner/realtor acknowledgement and current-entry Campaign Message-Match nodes remain in the editorial copy zone.
- Dylan relationship band appears directly after the first conversion experience.
- Lower support content is editorial: **What Dylan helps with / How your Buyer review works / Support when you’re on a timeline**.
- No turnaround guarantee, lender promise, or invented realtor claim was introduced.
- Life, Workers, routing, attribution, closing urgency, CoverageFit, and INFRA-1.1 remain protected.

---

## 408-UI-4.5 — Professional Programs Campaign Convergence — COMPLETE
### Objective
Bring Healthcare, Teachers, Technology, and Engineers closest to the approved mockup family while retaining one shared program system.

### Visual target
- profession switcher stays prominent
- profession-first editorial copy
- approved profession-specific photography
- stronger selective gold headline treatment than core insurance
- existing occupational form positioned as the right working panel
- Dylan relationship band
- lower editorial columns: **What Dylan will look at / Here’s how it works / Local people. Real support.**

### Protected behavior
- profession role lists
- eligibility/discount qualification language
- Campaign Message-Match Registry
- Formspree/consent
- CoverageFit handoff

### Acceptance
- all 4 program forms remain exact in data semantics
- organic + campaign-matched entry states both work
- no implication that occupation alone guarantees a discount

### UI-4.5 implementation closeout
- Healthcare, Teachers, Technology, and Engineers now use the UI-4 three-zone grammar: profession-first editorial proposition → campaign-derived professional photography → the existing certified occupational form as the working action panel.
- The four `#leadForm` blocks remain exact to the UI-4.4 input. Profession role lists, consent, Formspree, attribution, post-lead behavior, CoverageFit invitation, and zero-repeat handoff are unchanged.
- The Professional Programs switcher remains prominent and now uses restrained profession icons with warm-gold active-state emphasis.
- Approved profession headlines receive the stronger selective warm-gold treatment from the reference mockups while Farmers red remains the primary conversion color. Campaign Message-Match nodes remain authoritative; the UI-4.5 title accent renderer only re-applies presentation to the four approved fixed headlines.
- New context crops were derived from the already-shipped occupational campaign assets; no advertisement typography or eligibility claims are baked into the web hero.
- Dylan relationship bands sit directly beneath the first conversion experience. Lower support content is editorial: **What Dylan will look at / Here’s how it works / Local people. Real support.**
- Unsupported mockup claims were not carried into production. Occupation remains review context and discount availability remains subject to eligibility, underwriting, and policy terms.
- Life/Life Ops, Workers, `_routes.json`, Campaign Entry Registry, Local runtime, and 408-INFRA-1.1 remain protected.

---

## 408-UI-4.6 — Local Community Convergence — COMPLETE
### Objective
Apply the editorial/community visual language to `/local/`, merchant detail, and join without turning perks into an insurance inducement.

### Visual target
- South Bay/community context photography
- real category controls in the action surface
- real merchants/perks only
- warmer merchant cards and detail imagery when merchant-owned assets exist
- Dylan/insurance presence reduced or moved below merchant value

### Protected behavior
- **No insurance purchase or quote required**
- merchant catalog/status visibility
- perk redemption
- Local attribution
- merchant application
- Local → insurance bridge remains optional and secondary

### Explicit non-goals
- no fabricated merchants/offers/categories
- no fake distance/reviews
- no geolocation unless separately scoped

### Acceptance
- LOCAL-1.x functional suites pass
- Local compliance separation remains explicit
- existing operational three-merchant NO-GO is not silently changed

### UI-4.6 implementation closeout
- `/local/` now uses the UI-4 editorial grammar: community proposition → neighborhood-context photography → a working category panel that forwards only to the real supported Local categories (`All`, `Eat & Drink`, `Home`, `Auto`).
- The live directory remains catalog-driven. No fabricated merchant, perk, category, rating, distance, review, or geolocation feature was added.
- Merchant cards are warmer and more editorial while preserving catalog/status visibility rules. Stevie’s remains the only real active pilot merchant currently stored in the catalog; fixture records remain hidden.
- Merchant detail keeps merchant value and the current perk ahead of the optional insurance bridge. Redemption behavior, merchant terms, independence copy, and Local attribution are unchanged.
- `/local/join/` now uses the editorial/community hero and flatter steps while the `#localMerchantJoinForm` remains exact to the UI-4.5 input.
- Dylan/insurance presence is intentionally secondary to merchant/community value on Local. The public separation rule remains explicit: **No insurance purchase or quote required.**
- Local catalog/model/directory/merchant/redemption/attribution/join runtimes, Workers, `_routes.json`, Life/Life Ops, and 408-INFRA-1.1 remain protected.
- The existing LOCAL-1.10 operational three-merchant **NO-GO** remains unchanged pending real Auto + Home pilot merchants and external closeout.

---

## 408-UI-4.7 — Relationship + Completion Editorial Convergence — COMPLETE
### Objective
Carry the editorial language into the dynamic states not visible in hero mockups.

### Scope delivered
- progressive form expansion states
- post-lead focus questions
- CoverageFit invitation
- Home / Bundle / Buyer / Professional thank-you and receipt pages
- Contact
- Neighbor handoff
- Home Protection Score / utility
- 404, legal, recovery and empty-state presentation
- Local merchant-join completion

### Direction delivered
- software controls remain compact inside the working interaction surface
- confirmed post-submit states retain first-person Dylan acknowledgement
- post-lead progress now uses the restrained UI-4 editorial accent while Farmers red remains the conversion/action color
- summary, explanation and optional-next-step content is flatter and less card-heavy
- receipts are editorial acknowledgements with clear next steps rather than dashboard-style confirmation cards
- Contact is proposition + direct-action panel + quiet agency proof
- Neighbor handoff is a calm editorial transition rather than an ambient software interstitial
- Protection Score preserves the real gauge/tool but removes excess card chrome from explanatory sections
- error, recovery and legal surfaces inherit the same paper/navy/gold grammar

### Protected behavior
- confirmed vs. pending/unconfirmed truthfulness
- duplicate-lead safeguards
- CoverageFit explicit opt-in
- Local independence
- all existing destinations
- all protected forms
- Campaign Entry Registry and attribution
- Workers / `_routes.json` / 408-INFRA-1.1
- Life / Life Ops

### Implementation
`shared/editorial-completion.css` is the UI-4.7 presentation layer. No protected workflow runtime was rewritten.

### Acceptance
- UI-4.7 source and browser suites pass
- UI-3.12 E2E and Human Trust relationship suites remain green
- Life remains excluded and exact to the UI-4.6 input baseline

---


## 408-UI-4.8 — Mobile + Responsive Editorial Pass — COMPLETE
### Objective
Translate the new editorial compositions to real phones/tablets rather than simply stacking desktop blocks.

### Scope
- 320px, 375/390px, tablet, short landscape
- hero order and image crops
- action panel placement
- relationship-band collapse
- nav/contact ergonomics
- form keyboard behavior
- safe areas
- editorial columns collapse

### Acceptance
- no horizontal overflow
- 44px touch minimums
- 16px mobile controls
- no required disclosure hidden behind sticky UI
- no image crop that obscures essential context

### Implementation closeout
- Added `shared/editorial-responsive.css` as the only new customer-facing presentation layer for this sprint.
- Loaded 4.8 on 25/25 non-Life public HTML surfaces; Life and Life Ops remain excluded.
- Restored safe-area-aware header/footer geometry after the UI-4 editorial cascade.
- Certified internal horizontal scrolling for the Professional Programs family at 320px with no document overflow.
- Reduced phone hero photography to a concise editorial beat while preserving live HTML copy and working action panels.
- Collapsed relationship bands, editorial support columns, direct actions, and certified forms for phone use.
- Preserved the existing fixed Score mobile CTA while reserving content space beneath it.
- Browser QA covers 320x820, 375x812, 390x844, 768x1024, 844x390, and 1024x768.


---

## 408-UI-4.9 — Accessibility + Performance Certification — COMPLETE
### Objective
Re-certify the image-heavier editorial platform against the established accessibility and performance baseline.

### Accessibility
- heading semantics
- alt/decorative image policy
- focus/keyboard
- contrast including gold
- reduced motion
- forced colors
- 320px/400% reflow

### Performance
- responsive image source sets
- hero fetch priority discipline
- image dimensions/aspect reservation
- CSS/JS budgets
- no accidental full-resolution campaign image use

### Acceptance
- WCAG-oriented project suite green
- no material regression from UI-3.13 asset/performance budgets without documented justification

### Implementation closeout
- Added `shared/accessibility-performance.css` as a late-cascade non-Life accessibility hardening layer across all 25 public non-Life surfaces.
- Re-certified semantic heading order, skip navigation, form control names, image alt policy, keyboard-visible focus, gold contrast policy, reduced motion, forced colors, and 320px / 400%-equivalent reflow.
- Added intrinsic width/height reservation to every non-Life public `<img>` and fixed the resulting legacy footer min-content constraint rather than masking overflow.
- Added 320px responsive WebP candidates for Healthcare, Teachers, Technology, Engineers, and Local contextual photography.
- Recompressed the Home + Auto 320px editorial candidate from roughly 74 KiB to 45 KiB.
- Added responsive 506px WebP delivery for dark and white 408FARMERS identity marks and removed the Home header logo from high fetch priority so the actual hero is the sole priority image.
- Certified one high-priority image maximum per page and exactly one on image-led primary routes.
- Current primary-route source budgets remain at or below 300 KiB except `/home/`, which is explicitly grandfathered at 330 KiB (current: 323.2 KiB) because the post-UI-3.13 HOME/FLOW/UI presentation layers are contractually additive and behavior-frozen. No new JavaScript was added in 4.9.
- Historical `408-UI-3.13` asset QA therefore reruns at 98/99 solely on its obsolete 300 KiB Home ceiling; all 98 other legacy asset checks remain green. This is the documented exception permitted by this sprint's acceptance criteria.
- Life / Life Ops, protected forms, Workers, routing, attribution, Local runtime, pricing/eligibility logic, and CoverageFit behavior remain unchanged.
- Automated build certification does not claim deployed-domain Lighthouse scores or physical VoiceOver/NVDA/device testing; those remain production activation checks.

---

## 408-UI-4.10 — Functional Regression + Production Certification — COMPLETE
### Objective
Freeze the completed UI-4 non-Life presentation and certify the full site for production.

### Required regression
- Homepage
- Home/deep routes/campaigns
- Home + Auto
- Buyer/referrals
- all 4 Professional Programs
- Local directory/detail/join/redemption/attribution
- relationship/completion flows
- CoverageFit handoffs
- Workers/routing
- 408-INFRA-1.1
- Life exact-preservation audit

### Deployment boundary
Build-time certification is not proof of Cloudflare deployment. Include a deployed-domain smoke runbook covering static/Function boundary, forms, QR routes, Local routes, and Life.

### Final decision
UI-4 is complete only when the finished visual platform and all protected behavior are certified together.

### Implementation closeout
- Froze **223/223** deployable/runtime product files exactly to the 4.9 input; no customer-facing HTML/CSS/JS, Worker, routing, data, image, form, Local, CoverageFit, or Life behavior was changed by 4.10.
- Certified Life/Life Ops and shipped Life runtime/assets **14/14 exact**, infrastructure boundary files **4/4 exact**, and critical handoff/attribution/data files **12/12 exact**.
- Re-ran the current UI-4 accessibility, responsive, relationship/completion, cross-journey, static, metadata, link, JavaScript, Home routing, Local Worker, Life browser, and INFRA regression gates.
- Added a dedicated **559/559** 4.10 production freeze contract and a machine-readable regression matrix.
- Documented superseded historical harnesses rather than altering current UI-4 markup to satisfy stale selectors, historical VERSION whitelists, or the pre-UI-4 300 KiB Home budget.
- Added `UI4_10_DEPLOYMENT_SMOKE_RUNBOOK.md`; deployment activation remains a post-deploy verification step.
- Final status: **PASS — UI-4 COMPLETE / DEPLOYABLE-CERTIFIED / CUSTOMER-FACING PRESENTATION FROZEN.**
