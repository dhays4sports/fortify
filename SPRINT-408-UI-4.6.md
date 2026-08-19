# 408-UI-4.6 — Local Community Convergence

## Status
COMPLETE

## Objective
Apply the UI-4 editorial/community visual language to the Local directory, merchant detail, merchant join, and merchant-join receipt without turning Local perks into an insurance inducement.

## Delivered
- Editorial Local hero with community proposition, contextual neighborhood/home photography, and a working category action panel.
- Hero category controls are presentation proxies for the existing Local filters and expose only the categories already supported by the catalog: All, Eat & Drink, Home, Auto.
- Warmer catalog-driven merchant cards without fabricated merchants, offers, ratings, distances, reviews, or geolocation.
- Editorial Local explanation and merchant-recruitment sections with less SaaS/card chrome.
- Merchant detail restyled so merchant value and perk terms remain primary; optional insurance review remains secondary and visibly separate.
- Merchant join recomposed around community/merchant value while preserving the existing application form byte-for-byte.
- Local thank-you styling aligned with UI-4.
- Universal UI-4 non-Life header initialization corrected on Local by loading UI-3 before the editorial runtime.

## Protected behavior
- `local/data/catalog.json` and schema
- Local data model, directory, merchant/redemption, attribution and join runtimes
- merchant visibility/status rules
- perk redemption and merchant terms
- Local -> insurance attribution bridge
- merchant application form and endpoint
- Workers and `_routes.json`
- 408-INFRA-1.1
- Life/Life Ops

## Compliance boundary
**No insurance purchase or quote required.** Local participation does not affect insurance pricing, discounts, coverage, eligibility, or underwriting. Merchant offers remain merchant-owned and subject to merchant terms and availability.

The existing LOCAL-1.10 three-merchant operational NO-GO is not changed by this visual sprint.

## Next
408-UI-4.7 — Relationship + Completion Editorial Convergence
