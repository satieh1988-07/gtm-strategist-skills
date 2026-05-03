# Prospect: Color Street

**Last updated:** May 3, 2026 (rev 2)  
**Stage:** Demo complete — blocked on Shopify integration; technical scoping call needed  
**Owner:** Daniel Lang (sales) / Cassie Lewis (account) / Autumn Fowers (product/demo)  
**GTM Segment:** Cash & Carry DSO  
**Website:** https://www.colorstreet.com

---

## Company Profile

| Attribute | Detail |
|-----------|--------|
| Website | colorstreet.com |
| Vertical | Nail strips (primary), skincare, cosmetics |
| Active rep count | 20,000–30,000 stylists |
| Active SKUs | ~120–200 (rotating seasonal catalog) |
| Geography | US |
| Company stage | Established — post-platform migration (2 months off Exigo as of May 2026) |
| Cash & Carry? | Yes — ~70% of stylists carry and sell personal inventory (Brick's estimate) |
| Selling model history | **Traditionally a party plan company** — host rewards model, in-home parties, consultant-led events. Party plan DNA is embedded in their business model. Host rewards are an active feature their consultants use. |
| Stylist base note | Heavy ex-LuLaRoe contingent in the top-tier stylist population |

---

## Tech Stack

| Layer | Current Solution | Notes |
|-------|-----------------|-------|
| Commission engine / back office | **Custom-built in-house** | Left Exigo ~March 2026. Built their own commission engine. Not looking for a back office replacement. |
| Rep back office (stylist view) | **Shopify VO dashboard** | **Key clarification:** The Shopify VO dashboard IS the rep's back office. Color Street's custom commission engine pushes its data into Shopify, and reps log into Shopify VO to see their commissions, orders, and business data. Shopify VO is the single pane of glass for stylists — not a separate tool. This is the core reason Edmond requires Wayroo to appear as a sub-section within Shopify VO: adding a new standalone app would break the one-stop-shop experience their stylists already have. |
| Ecommerce / consumer storefront | **Shopify** | Corporate consumer-facing store layer. Same Shopify instance as rep VO — unified platform. |
| Rep payment tool | Square / PayPal / Venmo (fragmented, rep-chosen) | No corporate standard. Cash-and-carry transactions happen outside Shopify entirely — invisible to Color Street. |
| Rep inventory tracking | Excel spreadsheets (rep-managed) | Corporate has zero visibility into rep physical inventory post-shipment. |
| CRM | Unknown | Customer data from rep sales is not captured. Edmond: "We don't own those customers." |
| Other tools | None confirmed | |

**Tech stack data flow (confirmed):**
```
Custom Commission Engine
        ↓  (data pulled into)
    Shopify
        ↓  (reps log in to)
  Shopify VO Dashboard  ← THIS is the rep's "back office"
        ↓  (Wayroo must appear here as a sub-section)
    Wayroo (needed here)
```

**eSuite fee model:**
Color Street (like most DSOs) charges reps a monthly eSuite fee — a technology access fee the DSO passes through to reps for using the DSO's tech stack. Brick confirmed this is already in place. This is significant for Wayroo pricing: rather than the DSO absorbing Wayroo's per-user fee, the DSO can bundle it into the eSuite fee they already charge reps. The DSO's cost objection ("we pay per user") is neutralized — reps pay for Wayroo through their existing eSuite subscription. Wayroo becomes cost-neutral or even revenue-generating for the DSO at the rep level.

**Competitive context:**
Color Street **left Exigo** approximately 2 months before the May 1 demo (March 2026). They are NOT looking for a Freedom/back office replacement — that problem is solved with their custom engine. They chose to build custom because Exigo's limitations outweighed switching to another off-the-shelf back office. This makes them a **Wayroo-only prospect**, not a Freedom + Wayroo opportunity.

The Shopify integration requirement is not just a technical preference — it is a philosophical one. Color Street has deliberately built a one-stop-shop experience for stylists inside Shopify VO. Adding a separate app would require reps to context-switch and maintain another tool, which goes against their product philosophy. Wayroo must slot into the existing experience, not add to it.

---

## Interactions Log

| Date | Type | Attendees | Summary |
|------|------|-----------|---------|
| May 1, 2026 | Product demo | Cassie Lewis (ByDesign), Autumn Fowers (Wayroo), Edmond Kim (Color Street), Brick B (Color Street) | Full Wayroo demo. Strong product resonance — "My Stash" concept coined by Brick in real time. Single hard blocker: Shopify integration is a non-negotiable requirement from Edmond. Spendback piqued interest but ran out of time. |

---

## Confirmed Pains (from conversations)

| Pain | Severity (1–5) | Source | Verbatim Quote |
|------|---------------|--------|---------------|
| Zero corporate visibility into rep physical inventory | 5 | Edmond Kim | *"I remember huge complaints — I have to carry inventory in an Excel spreadsheet."* |
| No customer records from cash/in-person sales | 5 | Edmond Kim | *"We don't own those customers."* |
| No branded, traceable way for reps to surface personal inventory | 5 | Brick B | Spontaneously coined "Color Street Stash" / "The app could be the stash" |
| Brand integrity on resell — unofficial photos, wrong descriptions | 4 | Cassie Lewis (validated by Brick) | *"You guys would have better control over your brand and how it's being represented even on the resell."* |
| Product expiration not trackable (nail strips crack/dry out) | 4 | Edmond Kim | Raised as customer service complaint source — DSO can't see who has old stock to proactively address it |
| Rep carrying inventory managed only in Excel | 4 | Edmond Kim | *"I have to carry inventory in an Excel spreadsheet"* — manual, error-prone, zero corporate visibility |
| Rep customers don't receive invoices or shipping tracking | 4 | Cassie Lewis (personal rep experience) | *"I don't get an invoice. I don't get tracking on the shipping."* — cash/Venmo sales leave customers with no paper trail, no trust-building touchpoint, and no repeat purchase pathway |
| Reps using Shopify VO without a rep-side selling tool | 5 | Edmond Kim | Hard requirement: Wayroo must live inside Shopify VO, not as a standalone app |

---

## Features That Resonated

| Feature | Enthusiasm | Notes |
|---------|-----------|-------|
| Rep personal storefront ("My Stash") | 🔴 Highest | Brick coined the name unprompted. He started pitching it to Edmond in real time. Wants it embedded in Shopify VO. |
| Corporate visibility into rep inventory (inventory sync post-shipment) | 🔴 High | Multi-layered: throwback campaigns, expiration tracking, discontinuation cleanup, rep-to-rep transfers |
| Customer data ownership / CRM capture from in-person sales | 🔴 High | Edmond raised strategically — not just operational, but a data/marketing gap |
| Mobile POS at vendor events (replaces Square) | 🔴 High | C&C stylists do vendor events, pop-ups, and markets constantly — POS is not optional for this model. Barcode scanner, shipping labels, guest checkout, fast transaction flow all confirmed relevant. |
| Automated, low-friction inventory management | 🔴 High | Reps want inventory that manages itself — auto-sync when wholesale ships, not manual Excel updates. The easier the inventory management, the higher the adoption and the better the compliance trail. |
| Expiration date / freshness tracking per SKU | 🟡 Strong | DSO can set expiration dates on inventory items and see which stylists hold old stock — enables proactive customer service outreach before complaints arrive. Specific to perishable/time-sensitive products (nail strips, skincare). |
| Branded invoice + shipping tracking for rep customers | 🟡 Strong | Every Wayroo sale generates a branded invoice with shipping tracking for the customer — closes the trust gap that cash/Venmo sales leave open and creates a repeat purchase pathway. |
| Host rewards (party plan feature — Freedom) | 🟡 Future opportunity | Color Street has host rewards as an active program (traditional party plan model). Freedom supports host rewards natively. Party v2 (releasing soon) is directly relevant. Not raised in the demo — neither side surfaced it. Should be introduced in follow-up as a future expansion angle. |
| **Wayroo ecommerce storefront (rep's personal store)** | 🔴 High | Brick explicitly called out the rep ecommerce storefront as *new* and valuable for Color Street stylists. Reps can list their personal inventory, run their own discounts, create bundles, and do their own marketing — all from their Wayroo storefront. This is a real sub-business tool, not just a product listing page. |
| **Replicated site integration** | 🔴 High | Reps can also send customers to the replicated site (the DSO's full catalog, offered through ByDesign/Wayroo), where the customer can browse the full product range and the rep earns commission or credit on any purchase. Two earning mechanisms in one platform: direct sales from personal inventory (Wayroo storefront) + commission from DSO catalog sales (replicated site). |
| **Intuitive dual-storefront flow (Wayroo store ↔ replicated site)** | 🔴 High | Brick specifically highlighted that the flow between the rep's personal Wayroo storefront and the DSO replicated site is *very intuitive* — customers can move between the two seamlessly. This is a UX differentiator Brick noticed and named unprompted. |
| Brand catalog control (official images, descriptions pulled from corporate) | 🟡 Strong | Surfaced by Cassie; Brick agreed immediately |
| Spendback (rep wholesale purchasing credit) | 🟡 Unfinished | Autumn mentioned it, Edmond asked about it — ran out of time. Lead item for follow-up. |
| Rep-to-rep wholesale transfers | 🟡 Interesting | Brick confirmed it already happens informally. Formalizing it was interesting but not explored. |
| LuLaRoe lineage credibility | ✅ Trust signal | When Autumn mentioned Wayroo built the LuLaRoe app, Edmond said "Oh, okay. That makes sense." Many top Color Street stylists are ex-LuLaRoe. |

---

## Blockers

| Blocker | Detail | Owner | Status |
|---------|--------|-------|--------|
| **Shopify integration (hard requirement)** | Wayroo must appear as a sub-section within the Shopify VO — not a standalone app. Wayroo has never integrated with Shopify in this context. Autumn believes the API makes it feasible but a technical scoping call is needed. | Autumn Fowers + Wayroo tech team | Open — scoping call not yet scheduled |
| **SSO / user management** | Edmond wants stylists to log into Shopify and navigate to Wayroo without a separate login | Technical call | Open |
| **Payment processing separation** | They want Wayroo transactions isolated from Shopify Payments / Shop Pay. Autumn confirmed Wayroo replaces Square — needs to be clarified formally. | Follow-up call | Open |

---

## Key Quotes (Verbatim)

> *"I am veering away from an isolated app. It's got to be within the lens of it being integrated into Shopify."* — Edmond Kim

> *"If you're going to come back with follow-up, it's got to be within the lens of it being integrated into Shopify."* — Edmond Kim (repeated for emphasis)

> *"We don't own those customers."* — Edmond Kim (on cash-and-carry customer records)

> *"We could almost call it 'my stash'... the Color Street Stash. The app could be the stash."* — Brick B

> *"You guys would have better control over your brand and how it's being represented even on the resell."* — Cassie Lewis (validated by Brick)

> *"Oh, okay. That makes sense."* — Brick B (reaction to LuLaRoe lineage)

> *"Function over fashion, like I mean, our ladies aren't like, you know... more if it was functional"* — Brick B (on white-labeling)

> *[On the flow between Wayroo storefront and replicated site]* "Very intuitive." — Brick B (unprompted observation about the dual-storefront UX)

---

## GTM Implications

### Two confirmed DSO ICP value preferences (generalizable beyond Color Street)

**1. One-stop-shop, not another app to maintain**
DSO leadership does not want to hand reps another standalone app. They want solutions that integrate into whatever environment the rep already uses — reducing cognitive load, reducing support burden, and reducing the risk of non-adoption. Color Street built an entire Shopify-native VO to achieve this. Wayroo's strength here is that it consolidates many tools (POS, inventory, invoicing, storefront, payouts, shipping) into one — which is exactly the one-stop-shop promise. The challenge: Wayroo must also integrate into the DSO's existing rep environment (Shopify VO in this case), not stand beside it.

**Sales implication:** Lead with Wayroo's breadth ("one app replaces Square, Excel, Venmo, and your rep's storefront") as the one-stop-shop proof. Then show how it integrates into the DSO's existing rep environment — don't present it as a separate tool the DSO has to manage.

**2. DSOs want reps to have their own sub-business**
Color Street (and likely most DSOs) want reps to feel and operate like independent entrepreneurs — with their own branded presence, their own inventory, their own customer relationships — all under the DSO's umbrella. This is the "rep sub-business" model. Wayroo directly enables this: rep gets a personal branded storefront ("My Stash"), their own POS, their own inventory management, their own customer CRM — all branded to the DSO, all visible to corporate. This is not just a feature benefit; it's the rep value proposition that makes DSOs attractive to recruit and retain quality reps.

**Sales implication:** Frame Wayroo as the infrastructure that lets reps operate like real business owners — which makes the DSO more attractive to recruit into and harder to churn out of.

---

### Which ICP/segment does this account confirm?
**ICP 1a — Cash & Carry DSO.** Color Street is the founding data point for this sub-segment. They confirm:
- ~70% C&C rate is a real and significant share of rep activity
- Zero corporate visibility into post-shipment inventory is a real, named pain
- Customer data ownership from in-person sales is a strategic gap, not just operational
- FTC compliance exposure is implicit (untracked cash/Venmo sales = no retail sales documentation)
- Tax compliance exposure is implicit (no transaction records = 1099/sales tax gaps)

### What does this tell us about positioning?
Color Street validates the three-layer compliance + marketing pitch developed in `outputs/02-cash-carry-dso-icp-intelligence.md`:
1. **FTC** — retail sales documentation requirement; untracked Venmo/cash = liability
2. **Tax** — 1099 and sales tax jurisdiction records tied to every transaction
3. **Marketing** — customer records from rep sales surfaced to corporate CRM = net-new marketing database

The "My Stash" concept — a branded, scannable personal storefront for rep inventory — is a resonant, concrete product vision for this segment. Use this language in C&C outreach.

**New positioning insight from tech stack:** Color Street is a **Wayroo-only pitch**, not a Freedom + Wayroo pitch. DSOs that have left legacy back offices and built custom solutions, or that use Shopify as their primary back office layer, represent a distinct prospect type: they need the rep commerce layer (Wayroo) but not the corporate back office (Freedom). This is a different deal structure, a different price point, and a different decision-maker profile.

### What does this tell us about the product?
- **Shopify integration is a real product requirement** for at least one validated prospect. If other DSOs have migrated to Shopify-based stacks (post-Exigo), this is not a one-off request — it is an emerging integration need.
- **"Sub-section within VO" UX** — Edmond's framing reveals that the rep experience must feel native to the back office environment, not a separate app download. This is a UX/integration architecture requirement worth flagging to the product team.
- **SSO** is table stakes for this buyer type. No separate login tolerance.
- **Automated inventory sync is a rep adoption requirement.** Reps will not manually manage inventory in an app. Wholesale orders must auto-sync into the rep's inventory view on receipt — zero manual entry. The easier the inventory, the higher the adoption and the better the compliance trail.
- **Branded invoice + shipping tracking for rep customers** is a customer experience feature, not just an operational one. It closes the trust gap that Venmo/cash leaves open, creates a repeat purchase pathway, and generates the customer record compliance requires — all from a single transaction event.
- **Party v2 is a future expansion signal.** Color Street is a traditional party plan company with active host rewards. Freedom supports host rewards; Party v2 (releasing soon) expands this capability. This wasn't raised in the demo but is directly relevant. When Party v2 ships, Color Street is a natural reintroduction — even as a Wayroo-only account today, the party plan angle could bring Freedom into the conversation later.

### What does this tell us about pricing?
- **eSuite fee model removes the per-user cost objection.** DSOs already charge reps a monthly technology fee (eSuite). Wayroo's per-user fee ($5/user/month) can be passed directly to reps through this mechanism — the DSO doesn't absorb it, they collect it. For a DSO with 20,000 active stylists, Wayroo's per-user fee becomes a pass-through or a margin opportunity, not a line-item cost. This fundamentally changes how to handle the cost objection in pricing conversations.
- **Dual-track rep revenue = higher eSuite value justification.** Reps who have both a Wayroo personal storefront (direct inventory sales) AND a replicated site (commission on full DSO catalog) have two income streams from one eSuite subscription. The eSuite fee is easier to justify to reps when the tool actively earns them money in two ways. This should be part of the DSO's rep recruitment pitch: "Your eSuite gives you your own store AND access to our full catalog."

### What does this tell us about the sales motion?
- **Wayroo-only deal structure exists.** Color Street will not buy Freedom — they have a back office. The sales motion is Wayroo as a standalone rep commerce layer. Pricing and contracting need to reflect this.
- **Two-person DMU for C&C DSOs:** Technical Gatekeeper (Edmond — stack fit, integration) + Field Champion (Brick — stylist experience). Run separate tracks. Don't bring both into the same conversation if their needs conflict.
- **Cassie Lewis as a proof asset.** She is a Color Street rep and was present in the demo. She is the most credible validator in the room. Keep her in every follow-up.
- **"Ex-Exigo" is a buying trigger.** Color Street left Exigo recently. Other Exigo clients who are frustrated but haven't yet migrated are high-probability prospects — they're already dissatisfied and actively looking.

### What does this signal about Exigo as a competitive battleground?
Color Street left Exigo and built custom. The fact that they went custom (rather than switching to another vendor) suggests Exigo's limitations were severe enough to justify significant build cost. This is a signal worth investigating with other Exigo clients: *"If you were starting over today, would you still choose Exigo?"* Their answer tells you how close they are to displacement.

---

## Deal Status & Next Steps

| Action | Owner | Due |
|--------|-------|-----|
| Schedule technical scoping call (Shopify API integration) | Cassie Lewis → Autumn Fowers + Edmond Kim | ASAP |
| Build Shopify integration demo or proposal before next call | Autumn Fowers + Wayroo tech team | Before next call |
| Prepare Spendback explainer (2-slide max) — Edmond asked, it was dropped | Sam Atieh / Autumn Fowers | Before next call |
| Send Brick a "My Stash" concept one-pager — enable his internal champion role | Sam Atieh | This week |
| Clarify Wayroo-only pricing / contract structure | Daniel Lang | Before proposal |
| Flag Color Street for Party v2 outreach when released — host rewards angle | Sam Atieh | On Party v2 launch |

---

## Anti-Patterns / Disqualifiers

- Color Street is **not a Freedom prospect** — they have a custom commission engine and are not evaluating back office replacements. Do not lead with Freedom in any follow-up.
- Low white-label appetite — "function over fashion." Don't charge extra for white-labeling; it's not a value driver here.
- Edmond will disengage if the Shopify integration story is not solid. Do not schedule a follow-up without a credible integration plan to present.
