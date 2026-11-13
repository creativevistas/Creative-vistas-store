# Creative Vistas — Stripe checkout launch checklist

Status: PREPARED, NOT LIVE (2026-11-12)

Stripe account: Creative Vistas Marketing
Stripe context: acct_1Ub7U1L0Ort5pAT3
Currency: USD
All six Stripe products were created INACTIVE in live-mode. No active Stripe Payment Links have been connected to this website.

## Stripe catalog already created

| Website offering | Amount | Stripe Product ID | Default Price ID | Launch prerequisite |
| --- | ---: | --- | --- | --- |
| Realtor Listing Bundle | $29 | prod_VcNtXbx6zIudJL | price_1Ub97kL0Ort5pAT3R4CV5FSi | Final editable Canva template files + delivery method |
| 30-Day Content Planner | $25 | prod_VcOgM6CHzQqoxR | price_1Ub9t1L0Ort5pAT30M1OubLy | Final planner file + delivery method |
| Content Experience / 30 min | $80 | prod_VcOgxu9wxVtfYb | price_1Ub9t3L0Ort5pAT3fQmE1G6y | Booking/availability and fulfillment policy |
| Content Experience / 60 min | $150 | prod_VcOg0CgAwO4X2U | price_1Ub9t5L0Ort5pAT3g8OxlD2V | Booking/availability and fulfillment policy |
| Content editing or posting add-on | $40 | prod_VcOgrlIqvYwTRc | price_1Ub9t6L0Ort5pAT3SCIoVdIH | Define scope; keep tied to a content session |
| Marketing Training / one hour | $150 | prod_VcOgxp053m81SE | price_1Ub9t8L0Ort5pAT3V3uwMXug | Booking/availability and session policy |

These identifiers are not secret API keys; still do not put Stripe secret keys in GitHub or client-side code.

## Website status
- Static site: https://creative-vistas-store-front.pages.dev/
- Repo: creativevistas/Creative-vistas-store
- Two digital product pages have disabled PAY buttons and explain that checkout is not open.
- Shopping bag's checkout button is disabled. It is a preview cart, not a live checkout integration.
- Content Experience and Training currently direct customers to inquiries rather than charge them.
- Do not activate checkout, sell unavailable digital goods, or advertise automatic delivery until tested.
- Keep existing design, headers, images, and typography unchanged.

## When the files are ready
1. Confirm products/delivery details and whether buyers receive Canva template links, PDFs, or both. Ensure links do not expose editable originals.
2. Confirm Florida and destination-state sales tax requirements with an accountant. Current Stripe Tax settings status: pending (missing head-office field); no tax registrations were present on the latest account check. Do not guess a tax code or activate automatic Stripe Tax blindly.
3. Check Stripe identity/payout verification and statement descriptor in dashboard.
4. Decide on fulfillment: secure download/email delivery using a service or webhook-based mechanism. A success redirect alone is not proof of payment or secure file delivery.
5. Set finalized product(s) active and create hosted Stripe Payment Links for those prices only, capturing buyer email and using an appropriate post-payment confirmation.
6. Replace only corresponding disabled product CTA(s) with verified Stripe URLs. Update previews/cart only when a functional multi-item checkout actually exists; otherwise retain preview cart disabled.
7. Test in Stripe sandbox/test mode (not with real charges) and verify mobile + desktop flow, success, receipts, refund terms, and delivery.
8. Activate live links only after a final review.

For content sessions/training: confirm schedule and cancellation/reschedule terms before enabling upfront payments. Extended custom quotes are not a fixed-price product.

There is no live checkout URL to paste yet. Never invent one.
