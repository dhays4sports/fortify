# 408FARMERS Editorial Platform Design System

## Program
**408-UI-4.x — Editorial Human Platform Convergence**

## Governing principle
**Editorial insurance brand on the surface. Mature digital tooling underneath.**

UI-4 does not reopen the insurance product architecture. It changes composition, visual hierarchy, photography, and trust presentation while preserving the certified UI-3/Human Trust behaviors.

## Life exclusion
Life is explicitly excluded from UI-4. `/life/`, `/life/thank-you.html`, and `/life-ops/` remain frozen in the cinematic campaign system established by UI-3.7.

## Core palette
- **408 Navy** — trust, navigation, headings, structural identity.
- **White / cool paper** — clarity and breathing room.
- **408 Warm Gold** — editorial emphasis only: eyebrow copy, selected words, rules, navigation active state, restrained icon details.
- **Farmers Red** — conversion/action only. Primary buttons remain red.

### Gold rules
Gold must not replace Farmers red as the primary action color. Gold is decorative/editorial, never a signal that an insurance discount is guaranteed.

## Master page grammar
Major non-Life routes should converge toward this composition:

1. **Editorial proposition** — eyebrow, strong headline, concise explanatory copy.
2. **Context photography** — real-world profession, household, property, buyer, or community context.
3. **Working action surface** — the existing form, selector, directory control, or primary action panel.
4. **Dylan relationship band** — visible human accountability and direct contact where appropriate.
5. **Editorial lower-page columns** — what Dylan looks at / how it works / what happens next.
6. **Trust + agency footer** — real carrier/agency/local information only.

The software belongs in the working action surface. The rest of the page should not look like a dashboard.

## Foundation primitives
UI-4.1 adds reusable classes in `shared/editorial-platform.css`:
- `.ui4-editorial-hero`
- `.ui4-editorial-hero__copy`
- `.ui4-editorial-hero__media`
- `.ui4-editorial-hero__action`
- `.ui4-action-panel`
- `.ui4-kicker`
- `.ui4-headline`
- `.ui4-headline-accent`
- `.ui4-editorial-rule`
- `.ui4-benefits` / `.ui4-benefit`
- `.ui4-relationship-band`
- `.ui4-relationship-action`
- `.ui4-editorial-columns`
- `.ui4-editorial-column`
- `.ui4-editorial-list`
- `.ui4-steps` / `.ui4-step`
- `.ui4-context-image`
- `.ui4-trust-strip`

## Header contract
The non-Life platform header is refined by `shared/editorial-platform.js`:
- preserves the existing 408FARMERS logo and destinations
- adds a first-class **Professionals** navigation item linking to the existing Healthcare entry point
- keeps Home, Home + Auto, Buyers, Local, Life, and Contact available
- upgrades the direct-contact presentation to **Text or Call Dylan** with real SMS and phone links
- uses warm gold for the active navigation indicator
- preserves the existing mobile menu mechanics

## Photography contract
Photography is contextual, not decorative wallpaper.

### Required qualities
- premium, natural, editorial
- directly relevant to the page context
- no fake testimonials or implied customers
- no essential text baked into images
- responsive WebP/JPG delivery where appropriate
- meaningful alt text when informative; empty alt when decorative

### Route posture
- Homepage: restrained household/homeownership lifestyle
- Home: home/household
- Home + Auto: household + home + vehicle
- Buyer: keys/moving/closing
- Professional Programs: strongest profession-specific photography
- Local: South Bay/community/merchant imagery, only real merchant-specific assets on merchant records
- Utility/completion: Dylan only where it improves trust
- Life: excluded

## Action-panel contract
The working panel may contain the existing form or route-specific control. UI-4 is not permission to simplify or replace the certified form schema.

Protected:
- field names
- required semantics
- validation
- Formspree/Worker destinations
- campaign/referral attribution
- progressive intake
- CoverageFit handoff
- consent/disclosures

## Dylan relationship band
Use Dylan to establish accountability, not as a decorative celebrity block.

Recommended content:
- real Dylan headshot
- “Personally reviewed by Dylan Haysbert”
- Farmers Insurance Producer
- Virginia Tam Insurance Agency, Inc.
- Text Dylan
- Call Dylan

Do not place the band where it would blur the Local perk/insurance separation.

## Editorial lower-page contract
Prefer white space, typography, thin separators, short rules, check lists, and numbered steps over stacked card grids.

A common pattern:
- **What Dylan looks at**
- **How the review works**
- **What happens next**

Cards remain appropriate for actual interactive controls or distinct merchant/product records.

## Claims/source-of-truth rule
Mockups are visual direction, not factual source material.

Do not introduce unsupported claims such as:
- carrier-shopping claims inconsistent with Farmers-specific production
- unverified years in business
- placeholder phone/license numbers
- fabricated merchant offers
- guaranteed discounts, savings, eligibility, approval, or turnaround
- “authorized agency” wording unless it is already approved/source-backed in the build

Production copy must come from the current certified code/contracts or separately verified business facts.

## Accessibility
UI-4 inherits the UI-3.11 accessibility baseline:
- one meaningful H1
- semantic headings
- visible focus
- 44px mobile touch targets
- 16px mobile form inputs
- 320px reflow and 400% zoom resilience
- reduced motion
- forced colors
- text contrast
- no information conveyed only by color

Gold text uses the darker accessible gold token. Decorative gold can be lighter.

## Performance
Hero/context photography must not undo UI-3.13 performance work. Future route sprints should use responsive source sets and preserve lazy/eager priorities appropriate to viewport position.

## Protected infrastructure
UI-4 must preserve:
- `_worker.js`
- `_routes.json`
- 408-INFRA-1.1 Pages Function invocation boundary
- Campaign Entry Registry
- Local data/redemption/attribution model
- Life secure submission
- SMS infrastructure
- CoverageFit zero-repeat handoff

## Homepage reference implementation — UI-4.2
`/` is the first route-specific implementation of the UI-4 grammar and becomes the calibration reference for later non-Life routes.

Homepage rules:
- preserve **Insurance That Fits.** as the primary identity
- preserve **Start with a Coverage Review. Not a quote.** as the conversion philosophy
- keep the working surface situation-first rather than replacing it with a generic lead form
- retain the six-path full chooser as the canonical routing layer
- place Dylan accountability immediately after the first conversion section
- keep product/coverage browsing secondary to situation-first routing
- use contextual home/property imagery without embedding essential text in the image
- use gold for editorial emphasis, red for action


## UI-4.3 — Home + Bundle route application
- Home and Bundle use the three-zone composition at desktop: editorial copy / context image / existing action panel.
- On tablet and mobile, the order becomes copy → image → action panel; the form remains the same certified form.
- Home organic positioning uses **Start with a home coverage review.** Explicit campaign contexts still replace the approved `data-home-campaign-*` nodes.
- Bundle organic positioning uses **Let’s look at home and auto together.** Explicit campaign contexts still replace the approved `data-campaign-entry-*` nodes.
- Home and Bundle place the Human Trust relationship band directly after the conversion hero.
- Lower explanatory content should use editorial columns rather than card grids.
- Route-specific photography must be context-only: no baked-in promotional copy in the image zone.
- Farmers red remains action; UI-4 warm gold remains editorial emphasis.

## UI-4.4 Buyer reference implementation
Buyer is the UI-4 concierge/closing reference. Its approved grammar is:

**closing-aware editorial proposition → move-in/new-home context image → existing Buyer intake → Dylan relationship band → three editorial support columns → flat trust strip**

Buyer-specific rules:
- estimated closing date is context, never a turnaround guarantee;
- partner/realtor context stays visible when supplied but never becomes an endorsement claim;
- Farmers red owns conversion actions; warm gold is editorial emphasis only;
- the Buyer form and referral/closing behavior remain product contracts, not design variables.


## UI-4.7 — Relationship + Completion editorial convergence
Dynamic and completion states inherit the UI-4 grammar without changing their product semantics.

### Dynamic state rules
- progressive intake and post-lead controls remain compact and accessible
- progress indicators may use warm gold as orientation, while primary actions remain Farmers red
- confirmed states may speak in Dylan's first person; pending/unconfirmed states may not imply receipt
- summaries and explanatory blocks prefer thin rules and white space over nested cards
- CoverageFit remains an explicit optional continuation and is not visually framed as required

### Completion rules
- receipts use editorial hierarchy: status kicker → acknowledgement → Dylan identity → direct actions → next steps
- Local appears as a separate optional value section after the insurance acknowledgement
- no response-time or underwriting promise is introduced
- buyer and professional receipts retain their existing route-specific semantics

### Utility rules
- Contact uses editorial proposition + direct action panel
- Neighbor handoff retains secure transfer semantics but removes ornamental software ambience
- Protection Score keeps the functional gauge and transition runtime while explanatory sections flatten
- 404, legal, recovery and empty states use the same paper/navy/gold system
- Life remains excluded
