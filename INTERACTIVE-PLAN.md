# Custom Shop — Make Drop 001 Interactive: "Design Your Coaster"

**Date:** 2026-11-09 · **Status:** Draft plan + mockup for review (Dot + WebOps)
**Files:** this plan (`INTERACTIVE-PLAN.md`) and the working mockup (`designer-mockup.html`), both in `BeardedVentures/CustomShop`.
**Store state:** Drop 001 v2 page is built (commit a26d9fea), Grok's three gates fixed, still dark — Pages off, Stripe test mode, email-order only. Nothing goes live without Josh's go-ahead.

## 1. The goal (Josh, 2026-11-09, voice)

The page as it stands is stiff, static, and old-feeling. A visitor reads it; they don't play with it. Make it fun and immersive: give people real creative ability on the page itself, so designing their coaster is the entertaining part — something easy to share. The centerpiece is **"Design your coaster."**

And get it out soon: Thanksgiving (Nov 26) and Christmas are coming, and with some social media marketing these should sell relatively quickly.

## 2. What's stiff now

- The page talks *at* the visitor: story, specs, order buttons. One direction only.
- The four "styles" are pictures to look at, not tools to use. Picking one fills in an email, but the buyer never sees *their* words on the slate.
- Ordering is a mailto form. Nothing on the page moves, responds, or rewards the visitor for engaging.
- The most entertaining thing on the page — the laser actually engraving — lives behind a link to Instagram, not in the buying flow.

## 3. The centerpiece: "Design your coaster"

A live designer built into the product section, replacing the static "Choose a style" grid. The buyer sees their own design on the slate *before* they order.

**What the buyer can do:**
- **Type their own text** — family name, monogram, address, a date — and watch it appear on the slate in real time.
- **Pick a preset** — the same four styles (Family name, Monogram, Home coordinates, Texas star), each loading its layout into the designer with one tap.
- **Switch shape** — round or square slate, preview updates instantly.
- **Pick a lettering style** — script, classic serif, or all-caps block.
- **Watch a laser sweep** — every time the design changes, a thin light line sweeps across the slate, echoing the real engraving.
- **Order what they see** — the order email auto-fills with the exact shape, style, lettering, and wording they designed. No retyping, no mismatch.

**What it deliberately does NOT do (v1):**
- No account, no saved designs, no login. The design lives on the page until they order.
- No live checkout yet — ordering is still the email flow (Venmo/Zelle first), until Stripe goes live.
- No image upload in v1. Custom artwork stays in the $58 custom tier, handled by email.

**How it works (technical):** 100% client-side. The slate is an inline SVG (round disc or rounded square) with the buyer's text rendered on it; JavaScript updates the preview on every keystroke. No backend, no database, no tracking. It folds into the existing page — same fonts (Fraunces/Inter), same cream/dark palette, same $50 pack-of-6 framing — so it feels like the same store, not a second site.

## 4. Immersive touches around the designer

- **The laser is the entertainment.** The reel stays linked, but the sweep animation puts a hint of the process inside the buying flow itself.
- **Motion with restraint.** Hover and tap states on every control, the preview cross-fades between shapes, sections reveal on scroll. No autoplay video, no countdowns, no pop-ups — the drop rules (first come first served, numbered 1–6, gone = gone) stay exactly as they are.
- **Mobile first.** Most buyers will arrive from Instagram on a phone. The designer is built thumb-first: big preview on top, controls below, order button always one tap away.
- **Proof stays opt-in.** The order email carries a "Proof before engraving (yes/no)" line, so a buyer who wants to see it first can ask — without slowing the 24-hour ship promise for everyone else.

## 5. Stock: from one drop to a mainstay

Josh's call (2026-11-09): keep a small stock of blanks on hand. Blanks run about a dollar each, so holding a few dozen costs very little — and it turns the coaster from a one-off drop into a product that can stay available.

- **Drop 001 stays a drop:** 6 packs, numbered 1–6, gone = gone. That scarcity is the story.
- **After it sells:** the coaster becomes a Core evergreen product (same design-your-own flow, restocked), while numbered drops continue for new designs. The archive stays as the record.
- **Reorder trigger:** when 2 packs are left, reorder blanks. No standing inventory system needed at this size — a count on the page, updated as packs sell.

## 6. Launch sequence

| Step | What | Owner / gate |
|---|---|---|
| 1 | Approve this plan + mockup direction | Josh (this review round) |
| 2 | Fold the designer into `index.html`, replacing the static styles section | Muse, then screenshot-check desktop + mobile |
| 3 | Dot + WebOps review the new version (this submission) | Dot, Grok/WebOps — review only |
| 4 | Fix what they flag, Josh's verdict | Josh |
| 5 | Pages back on + live Stripe | Josh (Pages re-enable; Stripe live-mode switch is his call) |
| 6 | Social push, Instagram first | Gated: the social posting pause and the Instagram hold lift only when Josh says so |

**Dates that matter:** Thanksgiving Nov 26 (gift-buying moment), Christmas order-by ~Dec 14 (Etsy sellers' cutoff). The ornament test batch is parked per Josh's coaster-first call — this launch is the coaster only.

## 7. What the reviewers are asked

- **Dot:** Is the plan clear and feasible? Does the designer fit the drop model, or does it dilute the scarcity story? What risks am I missing (ordering, proof step, stock)?
- **WebOps (via Grok):** Review the mockup's UX — is the designer obvious and usable on mobile? Check performance (single file, inline SVG), accessibility (labels, keyboard, selected states), and the order-email flow. Ranked fixes, what to change first.

Both: review only. No publishing, buying, or changes from the review itself.

## 8. Open decisions for Josh

1. **Mockup direction** — approve the designer as the centerpiece, or change it?
2. **Proof step** — opt-in (as built) or mandatory before every engraving? Mandatory slows the 24-hour promise.
3. **Social pause / Instagram hold** — lift for launch, or launch quiet and market later?
4. **Live Stripe timing** — switch before launch, or launch on email-order and switch after the first sales?

## 9. Risks and honest limits

- Email-order is still interim. Until Stripe is live, every sale is a manual email + Venmo/Zelle exchange — fine for 6 packs, not for scale.
- The designer previews, but it can't show the *real* engraving. The reel and the finished-coaster photos carry that proof.
- All sample text in the mockup is fictional (Miller Family / Anytown; Texas State Capitol coordinates) — no real personal data anywhere on the page.
- The mockup is a working preview, not the live store. It is not published; Pages stays off until Josh says go.
