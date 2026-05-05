# Phase 3 — Cash & Carry DSO Customer Archetype

**Phase:** 3 — Validating Customers  
**Framework:** GTM Strategist by Maja Voje  
**Status:** Single data point (Color Street demo, May 1, 2026) — high-confidence archetypes for the two confirmed DMU roles; C&C Rep archetype is inferred from field observations, not direct interviews. Validate all three in 4+ discovery calls.  
**Input:** `outputs/02-cash-carry-dso-icp-intelligence.md`, `prospects/color-street.md`

---

## Overview: The Cash & Carry DSO Buying Unit

Cash & Carry DSO deals involve at least two distinct personas in the decision-making unit — with very different motivations, vocabularies, and objection patterns. A third persona (the rep/stylist) is not a buyer in Track 1 but controls adoption outcomes.

| # | Archetype | Role in Deal | Deal Risk if Ignored |
|---|-----------|-------------|---------------------|
| A | **Field Champion** — VP Field Operations / Distributor Relations | Internal champion; sells the vision to peers; gauges rep experience | Without his buy-in, there's no internal momentum. He will kill it passively by not advocating. |
| B | **Technical Gatekeeper** — CTO / VP Technology | Controls architecture decisions; final say on integrations | He will kill the deal actively if the integration story doesn't hold. He asks the questions nobody else knows to ask. |
| C | **C&C Rep / Stylist** | End user; not a buyer in Track 1 | Low adoption post-contract = churn within 12 months. The DSO cancels when reps don't use it. |

---

## Archetype A: The Field Champion

**Archetype name:** The Field Ops Builder  
**Representative example:** Brick B, Color Street (Distributor Relations)

### Who They Are

| Attribute | Detail |
|-----------|--------|
| Title | VP Field Operations, Director of Distributor Relations, Head of Stylist Success, National Sales Director |
| Industry | Direct selling, MLM — jewelry, accessories, beauty, nail, cosmetics |
| Company size | 1,000–30,000 reps; cash-and-carry model with significant vendor event activity |
| Reports to | CEO or VP Sales |
| Background | Often a former rep themselves — they came up through the field and now manage it. They've done the vendor events. They know the pain from both sides. |

### Their Job

They own the field. Rep activation, rep retention, rep performance, event playbooks, stylist experience, and field-level brand compliance are their domain. They are measured on rep headcount and field sales volume — if reps quit or go dark, it's their problem.

**Primary JTBD:** Give reps the tools and experience that make them feel like real business owners under the company's brand — so they recruit harder, stick longer, and sell more.

**Secondary JTBD:** Control the brand at the rep level. Every unofficial Instagram post, every wrong product photo, every Venmo transaction with no invoice is a brand integrity problem that lands on their desk.

### What Keeps Them Up at Night

- Reps quitting because "it's too hard" or "I can't track my stuff"
- Top reps going to a competitor DSO that offers better tools
- Brand posts that are off-spec — wrong photos, wrong descriptions, unlicensed usage
- Reps complaining about not knowing what inventory they have
- Customers calling them (the company) because a rep never sent a receipt
- Corporate campaigns that don't land because reps don't know which products they even have

### What a Good Day Looks Like

A rep from a vendor event texts her: "I sold out my whole stash and ordered more already." Retention is up. A new stylist activated in 3 days. She's not fielding brand compliance complaints.

### Their Language (Verbatim)

- *"We could almost call it 'my stash'... the Color Street Stash. The app could be the stash."* — Brick B, Color Street
- *"Our ladies"* — how they refer to reps; warm, protective framing
- *"Brand and how it's being represented"* — the brand integrity lens
- Talks about rep feelings and experience: whether the app feels right, whether stylists will adopt it
- Does NOT talk about APIs, webhooks, or data schemas

### Buying Triggers

- A top rep complains about inventory management at a company event
- A competitor DSO starts offering better field tools — their reps notice
- A brand compliance incident embarrasses the company publicly
- CEO asks "what are we doing about rep adoption?" after a bad retention quarter
- They attend an industry conference and see what other companies are offering reps

### How They Evaluate Solutions

They run a gut test first: *"Would my ladies actually use this? Would I have used this when I was in the field?"* They look for demos that feel intuitive — not feature-heavy walkthroughs but a quick live flow that proves the rep experience is clean. They will test the app on their own phone before endorsing it internally.

Then they become a champion or go quiet. If the demo lands, they will pitch the solution internally — often using their own language and their own framing (e.g., "My Stash" — an idea that emerged unprompted from Brick in the Color Street demo).

### How to Win Them

1. **Let them rename the product.** The moment they invent their own framing ("Color Street Stash"), the deal becomes theirs to win internally.
2. **Show a rep-experience demo, not a feature list.** Walk through a vendor event scenario end to end: open app, scan product, take payment, print label, customer gets receipt. Keep it fast.
3. **Give them enablement materials.** They will sell this internally before the decision is made. Give them a one-pager, a concept deck, a Loom — something they can send to their CEO and stylists without needing you on the call.
4. **Use Cassie.** A fellow rep-turned-employee confirming the experience is more powerful than any testimonial slide.

### What Will Lose Them

- A demo that looks complicated or requires setup steps
- Being positioned as "another tool" rather than a one-stop shop
- Any signal that adoption will be a battle — they've lost that battle before
- Feeling like you're talking to their IT team, not them

---

## Archetype B: The Technical Gatekeeper

**Archetype name:** The Integration Skeptic  
**Representative example:** Edmond Kim, Color Street (Tech/Ops)

### Who They Are

| Attribute | Detail |
|-----------|--------|
| Title | CTO, VP Technology, Head of Technical Operations, IT Director |
| Industry | Direct selling — joined from adjacent SaaS or ecommerce backgrounds (Shopify ecosystem is common) |
| Company size | Same as above — mid-to-large DSOs that have invested in custom tech stacks |
| Reports to | CEO or COO |
| Background | Built or managed the DSO's current tech stack. Likely owns the commission engine and the rep-facing digital environment. Has opinions about architecture. Has been burned by vendor lock-in or a botched integration before. |

### Their Job

Keep the tech stack stable, integrated, and as low-maintenance as possible. They are measured on system uptime, rep-facing digital experience quality, and cost of technology. They do not want to add complexity; they want to reduce it.

**Primary JTBD:** Evaluate whether a new vendor will integrate cleanly into the existing stack — or create a new maintenance burden that falls on their team.

**Secondary JTBD:** Protect the company from buying something that sounds good in a demo but breaks in production. They've seen it happen.

### What Keeps Them Up at Night

- A vendor that promises Shopify integration and then delivers a partial one
- SSO that doesn't actually work the way it was described
- Payment separation breaking their existing settlement flows
- Reps experiencing login fragmentation — two separate apps, two passwords, two experiences
- Vendor onboarding that requires 3 months of engineering time they don't have
- "We own those customers" — any data they hand to a third-party vendor that they can't get back
- FTC / IRS audit exposure from untracked transactions

### What a Good Day Looks Like

Every system is running. No support tickets. No rep-facing outages. A vendor integration shipped on time, works as documented, and his team didn't have to rewrite half of it. No surprises.

### Their Language (Verbatim)

- *"I remember huge complaints — I have to carry inventory in an Excel spreadsheet."* — Edmond Kim
- *"We don't own those customers."* — Edmond Kim (on Venmo transactions)
- Speaks in technical specifics: Shopify API, SSO, payment gateway separation, webhook integrations, data ownership
- Asks about timelines, documentation, support SLAs, what happens when it breaks
- Uses words like "scope," "integration," "architecture," "dependencies"

### Buying Triggers

- The company has just rebuilt or is actively maintaining a custom tech stack — they understand integration work intimately
- A compliance event (FTC inquiry, IRS notice, state tax audit) surfaces the data gap they've always known was there
- The CEO or VP Field Ops says "find us a rep tool" — they are now responsible for making it work technically
- A previous vendor's integration failed and they're fixing the damage
- Customer data ownership becomes a board-level concern

### How They Evaluate Solutions

They go from demo to technical interrogation immediately. If the integration story is hand-wavy, they end the conversation internally — without telling you. They look for:
- An actual API (not a "we can work with Shopify" statement)
- A documented SSO implementation
- Data ownership and export clarity — what happens if we leave?
- Payment flow separation — does Wayroo's payment gateway conflict with their existing settlement?
- Scoping timeline and cost — can your team commit to a delivery date?

If the demo doesn't have a technical scoping session scheduled by the end of the call, they will not advocate.

### How to Win Them

1. **Separate the technical track from the champion track.** Do not make Edmond sit through the "My Stash" vision meeting. Schedule a dedicated technical scoping call: Autumn + Wayroo engineering + Edmond + his team.
2. **Lead with integration story, not features.** Edmond's first question is always about the API. Answer it first.
3. **Bring documentation.** A Shopify API integration spec, an SSO implementation guide, or a Spendback technical brief goes further than a feature list.
4. **Give him a way to say yes.** His job is to find reasons to say no. The close for Edmond is: "Here's the scoping process, here's the timeline, here's who you'd work with." Remove ambiguity.
5. **Use the data ownership and compliance angle.** "We don't own those customers" was his most emotional statement in the demo. The FTC and tax compliance story is his compliance risk reduced — lead with it.

### What Will Lose Them

- Vague answers to specific integration questions ("we support Shopify" without API detail)
- SSO treated as an afterthought
- Assuming the Field Champion's enthusiasm is enough — Edmond will override Brick if the integration story doesn't hold
- Promising a timeline you can't keep

---

## Archetype C: The Cash & Carry Rep (End User — Track 1 Adoption Driver)

**Archetype name:** The Vendor Event Hustler  
**Note:** This archetype is inferred from Brick B's descriptions and Cassie Lewis's first-person account during the Color Street demo. Direct rep interviews have not yet been conducted. Do not use this archetype for Track 2 messaging until it is validated with 3+ actual rep interviews.

### Who They Are

| Attribute | Detail |
|-----------|--------|
| Title | Independent Rep, Stylist, Distributor, Consultant — title varies by DSO |
| Industry | Direct selling — jewelry, nail, beauty, accessories, cosmetics |
| DSO profile | Cash-and-carry model; majority of sales happen in person at vendor events, markets, pop-ups, and social gatherings |
| Background | Many are ex-LuLaRoe in the nail/beauty category — they've used inventory management apps before. Others are new to DSO selling entirely. They run a small business on the side; for some it is their primary income. |

### Their Job

Sell product. Go to events, set up a table, move inventory, get paid, go home. They are measured on personal sales volume and net earnings. They do not think about compliance. They do not think about corporate visibility. They think about: what did I sell today, how much did I make, and what do I need to restock?

**Primary JTBD:** Move personal inventory quickly and profitably at events — with minimal admin overhead before and after.

**Secondary JTBD:** Build a customer base that buys from them again (not from corporate — from *them*).

### What Keeps Them Up at Night

- Losing a sale because the buyer doesn't have cash and they can't take a card
- Not knowing what they have in stock — running out of a hot SKU at an event and not realizing it until after
- Customers texting "did my order ship?" with no tracking to give them
- Inventory that expires before they sell it
- The mental overhead of reconciling what they bought vs. what they sold vs. what's still in their car
- Spending 2 hours on admin after an event (updating the spreadsheet, sending invoices manually)
- Products that are off-spec or discontinued sitting in their garage

### What a Good Day Looks Like

She sold out her top 10 SKUs at a market, Wayroo handled checkout on her phone, customers got receipts automatically, and her inventory updated itself. She drove home, checked the app, placed a restocking order with one tap, and was done. No spreadsheet. No chasing receipts. No "where's my order?" texts.

### Their Language

- "My stash" / "what I have in stock" — not "inventory"
- "Ladies" / "customers" — not "end consumers"
- "Vendor event" / "market" / "pop-up" — the primary sales venue
- "My business" — they identify as business owners, not employees
- "Easy to use" — primary adoption filter; if it's not immediately intuitive, they won't stick
- Cassie (rep-turned-ByDesign employee): *"I don't get an invoice. I don't get tracking on the shipping."* — the rep knows their customers are underserved, but has no way to fix it

### Buying Triggers (for Track 2 — future)

- DSO mandates Wayroo adoption (Track 1 path — they follow corporate instruction)
- Another rep at an event shows them the app and they see it live
- They miss a sale because they couldn't take a card
- They lose an item to expiration and it's the third time this quarter

### Adoption Signals (for Track 1 DSO buyer)

- "Our best reps are already using something like this" — they're pre-sold on the behavior
- LuLaRoe alumni in the rep base — they know the app and the workflow
- High vendor event frequency — the pain of manual tracking is acute, not theoretical

### What Will Drive Adoption (after corporate mandates)

- App loads fast and works at a vendor event with spotty cell signal
- Barcode scan checkout takes under 10 seconds per item
- Customer gets an automatic receipt — no manual step for the rep
- Inventory updates itself — no "log in after the event to update your spreadsheet"
- The app feels like it was built for her, not for corporate's visibility

---

## What These Archetypes Confirm (vs. What Still Needs Validation)

| Question | Status | Evidence |
|----------|--------|---------|
| Field Champion persona is the internal champion in C&C DSO deals | **CONFIRMED** | Brick B, Color Street — spontaneous vision framing, immediate rep empathy |
| Technical Gatekeeper is the deal killer if integration fails | **CONFIRMED** | Edmond Kim, Color Street — Shopify integration demand as non-negotiable blocker |
| Rep persona is adoption-dependent on corporate mandate, not grassroots adoption | **CONFIRMED** | Paparazzi 4,000 MAU proof; Brick: "if corporate mandates it" |
| C&C Rep pain profile (manual inventory, no invoice, vendor events) | **HIGH CONFIDENCE** | Cassie Lewis (rep-turned-ByDesign) first-person; Brick's field observations |
| C&C Rep would actively choose Wayroo unprompted (Track 2) | **NOT YET VALIDATED** | No direct rep interviews conducted |
| Technical Gatekeeper profile applies beyond Color Street (Shopify-native stacks) | **NEEDS 4+ INTERVIEWS** | Assumption #3 — Shopify prevalence is unconfirmed segment-wide |
| Field Champion profile is present in all C&C DSO buys | **MEDIUM CONFIDENCE** | Color Street is one data point; interview target list in `02-cash-carry-dso-icp-intelligence.md` |

---

## Discovery Questions by Archetype

### For the Field Champion (Brick archetype)

- "What does an ideal rep experience look like at a vendor event today vs. what your stylists actually have?"
- "When your top reps quit, what reason do they give?"
- "If a rep has a bad first week — lost a sale, can't figure out tracking — what does that cost you?"
- "How do your reps currently track what inventory they have at home or in their car?"
- "What would it mean for recruitment if your reps could show a prospect 'here's the app I use for my business'?"

### For the Technical Gatekeeper (Edmond archetype)

- "What does your current rep-facing tech stack look like — what does the rep log into, and what does that pull from?"
- "How do you currently handle rep 1099 issuance when a portion of their sales go through Venmo or cash?"
- "If a state tax authority asked you to produce a sales tax jurisdiction record for your rep's direct-to-customer transactions from last year, how would you do that?"
- "What would a Shopify integration need to look like for you to feel confident approving it?"
- "Who owns the customer records when a rep sells through a third-party payment tool?"

### For Both (Discovery Filter)

- "What percentage of your reps carry and sell personal inventory vs. fulfilling direct-to-customer catalog orders?"
  - If answer is >30% cash-and-carry: C&C ICP confirmed
  - If <10%: standard DSO ICP, revert to primary motion

---

## Next Step: Validate in 4+ Interviews

Before formalizing this archetype as a GTM input, conduct discovery calls with 4+ Cash & Carry DSO targets (see `outputs/02-cash-carry-dso-icp-intelligence.md`, Part 5 for account list). Focus on:

1. Does the Technical Gatekeeper / Field Champion DMU structure repeat?
2. Is Shopify the common rep-environment choice (or is it a Color Street-specific artifact)?
3. Does the Field Champion use "rep experience" and "brand" language consistently?
4. Does the Technical Gatekeeper lead with integration/compliance questions every time?

One more confirmed data point elevates these to validated archetypes. Until then, treat as working hypotheses.

---

*Frameworks: GTM Strategist by Maja Voje — Phase 3 (Validating Customers), Task 7 (DMU Mapping), Task 1 (Assumption Mapping)*  
*Created: May 5, 2026*
