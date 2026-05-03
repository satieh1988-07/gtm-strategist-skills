---
name: analyzing-call-transcripts
description: "Post-call intelligence skill for ByDesign/Wayroo sales team. Use whenever a sales call transcript or structured call notes are available — discovery calls, demos, follow-ups, technical scoping, or partner calls. Extracts: call metadata and DMU roles, pains by persona with verbatim quotes and severity scores, feature resonance and blockers, GTM signal mapping against ICP/positioning/competitive context, and cross-skill implications. Creates or updates prospects/[company-slug].md and prospects/_index.md. Complements sdr-agent: sdr-agent handles pre-call prep and post-call outreach; this skill handles the intelligence capture and GTM learning loop."
---

# Analyzing Call Transcripts — Post-Call Intelligence Capture

This is a utility skill. It is not part of the 12-phase GTM sequence. Use it immediately after any sales call — discovery, demo, follow-up, technical scoping, or partner call — where a transcript or structured notes are available.

**Its job:** Turn a raw call transcript into structured prospect intelligence, then propagate what was learned back into the GTM system.

**What it produces:**
- A complete or updated `prospects/[company-slug].md`
- An updated `prospects/_index.md`
- A cross-skill callout identifying which GTM phases and outputs to revisit
- Optionally: a new `outputs/[pattern-slug]-intelligence.md` when a call confirms a pattern-level insight across multiple accounts (not every run)

---

## Before You Start

1. **Read `my-gtm-context.md` first.** You need the ICP definitions, pain inventory, feature list, competitive landscape, value props, and proof points before you can map anything from the transcript. Without this, the analysis is generic.

2. **Check `prospects/_index.md`.** Is this account already in the system? If yes, read the existing `prospects/[company-slug].md` before doing anything else — you will be updating, not replacing.

3. **Check `prospects/_template.md`** if this is a new account. You will scaffold the new file from this template. Do not improvise a structure.

4. **Check `outputs/` for relevant prior GTM work.** Especially: any `outputs/06-positioning-*` or `outputs/06-messaging-*` files (to check positioning resonance) and any `outputs/02-*-icp-intelligence.md` files (to check ICP fit against prior evidence).

5. **Ask for the transcript.** If the user hasn't pasted it yet, say: "Please paste the transcript or your structured call notes. Include the company name, date, attendees, and call type if you know them — I'll extract the rest."

6. **Work one task at a time.** Present your output for each task, ask for corrections, then move to the next. Never produce all seven outputs at once.

---

## Task 1: Parse Call Metadata (~5 min)

**Output:** Confirmation block presented inline — no file written yet

**What to do:**

From the transcript or call notes, extract and confirm:

- **Company name** — then derive the file slug: lowercase, hyphens only, no special characters (e.g., "Color Street" → `color-street`, "LuLaRoe" → `lularoe`)
- **Call date** — in "Month D, YYYY" format
- **Call type** — one of: Cold outreach / Discovery / Product demo / Technical scoping / Follow-up / Proposal review / Partner call / Other
- **Duration** — if available in the transcript
- **Attendees** — for each person: name, company (ByDesign or prospect side), title or inferred role, and DMU classification:
  - Economic Buyer — has budget authority and final yes/no
  - Technical Gatekeeper — evaluates technical fit, can veto
  - Field Champion — internal advocate, feels the pain daily
  - Influencer — shapes the decision without owning it
  - End User — will use the product; rarely the buyer
  - Unknown — cannot be determined from transcript
- **Call initiated by** — ByDesign outbound / Prospect inbound / Partner referral / Unknown

If anything cannot be determined from the transcript, flag it as `[unknown]` and ask the user to confirm before proceeding.

**The deliverable:**

```
CALL METADATA — [Company Name] | [Date] | [Call Type]
Duration: [X min / unknown]
Initiated by: [Outbound / Inbound / Referral / Unknown]

Attendees:
| Name | Company | Title | DMU Role |
|------|---------|-------|----------|
| ... | ... | ... | ... |

Slug: [company-slug]
Existing prospect file: [Yes — prospects/[slug].md / No — will create new]

Does this look right? Anything to correct before I continue?
```

---

## Task 2: Extract Pain Points by Persona (~10–15 min)

**Output:** Pain severity table presented inline — feeds Task 6

**What to do:**

Read the full transcript. For every pain point surfaced:

1. **Attribute it to the specific speaker** (name and DMU role) — not just "the prospect"
2. **Record the verbatim quote** — exact words, in quotes. If the notes are paraphrased, mark with `[paraphrase]`
3. **Classify the pain** using these standardized categories from `my-gtm-context.md`:
   - Rep activation / retention
   - Rep payout speed
   - FTC compliance / retail transaction records
   - Tax / 1099 / sales tax tracking
   - Customer data ownership / DSO CRM visibility
   - Corporate visibility into rep inventory (C&C specific)
   - Brand integrity / catalog control
   - Product expiration / quality tracking
   - App fragmentation / tool sprawl
   - Integration / stack compatibility
   - Competitive displacement (note which platform)
   - Other (describe specifically)
4. **Score severity 1–5:**
   - 5 = Urgent language used, raised unprompted, or equivalent to "this is why we're here"
   - 4 = Named as meaningful; clearly felt, not blocking
   - 3 = Acknowledged when asked; moderate felt pain
   - 2 = Mentioned in passing; no emotional signal
   - 1 = Inferred by you — not stated by prospect; flag explicitly
5. **Flag new vs. previously confirmed** — for existing accounts, compare against the prospect file's existing pain table. A pain moving from severity 2→4 is significant and should be called out.

**The deliverable:**

```
PAIN POINTS — [Company Name] | [Date]

| Pain Category | Severity | Speaker (Role) | Verbatim Quote | New / Updated |
|---------------|----------|----------------|----------------|---------------|
| ... | ... | ... | "..." | New / Updated from [X] |
```

Ask: "Does this capture everything? Anything I missed or misread?"

---

## Task 3: Extract Feature Resonance and Blockers (~10 min)

**Output:** Two tables presented inline — feeds Task 6

**What to do:**

Scan the transcript for all reactions to Wayroo or Freedom features that were discussed, demonstrated, or mentioned.

**For each feature:**
1. Name it using standard Wayroo/Freedom feature names from `my-gtm-context.md`:
   - Mobile POS (barcode scanner, in-person payments)
   - My Stash / Rep branded storefront (personal inventory management)
   - Next-day payouts
   - Customer data capture (FTC audit trail, CRM)
   - Real-time inventory sync (corporate visibility post-wholesale)
   - Spendback (instant rep wholesale credit)
   - Brand catalog control (official images/SKUs to reps)
   - Integrated shipping / invoicing
   - Rep sub-business infrastructure
   - Freedom commission engine
   - Host rewards / Party plan tooling
   - Other (name it)
2. **Enthusiasm rating:** High / Medium / Low / Neutral / Negative
3. **Signal:** What said or done to indicate this level (spontaneous naming, follow-up question, pushback, silence)
4. **Speaker who reacted** (name and role)

**For each blocker:**
1. Name the blocker explicitly and concretely
2. **Type:** Technical (integration, API, SSO) / Commercial (price, contract, budget) / Stakeholder (approval chain, absent decision maker) / Competitive (evaluating alternatives) / Timing (budget cycle, contract timing) / Product (missing feature)
3. **Owner:** Who on the ByDesign side resolves this (Daniel Lang by default unless assigned otherwise)
4. **Status:** Open / In progress / Resolved

**The deliverable:**

```
FEATURE RESONANCE — [Company Name] | [Date]

| Feature | Enthusiasm | Signal | Speaker (Role) |
|---------|------------|--------|----------------|
| ... | High/Med/Low/Neutral/Negative | ... | ... |

BLOCKERS

| Blocker | Type | Owner | Status |
|---------|------|-------|--------|
| ... | ... | ... | Open / In progress / Resolved |
```

Ask: "Anything missing here? Any blocker nuances I should capture differently?"

---

## Task 4: Map to GTM Context (~10–15 min)

**Output:** Structured analysis presented inline — feeds Task 5 and Task 6 GTM Implications sections

**What to do:**

Read the pains and features from Tasks 2–3 against `my-gtm-context.md` and relevant `outputs/` files. Your job is to check for fit, gaps, and surprises — not to summarize what the prospect said.

**ICP Fit Check:**
Does this account match ICP 1 (standard DSO leader), ICP 1a (Cash & Carry DSO leader), or does it deviate? Score it:
- Full match — meets all primary criteria
- Partial match — meets most criteria; note the deviation
- Edge case — notable deviation; flag what it is and whether it's a new segment signal
- Non-ICP — explain why; flag for disqualification review

**Pain Coverage Check:**
Which confirmed pains from this call appear in the prioritized pain inventory in `my-gtm-context.md`? Which are new — not in the list? New pains may indicate an underweighted problem or a new segment signal. Flag them explicitly.

**Competitive Check:**
Which competitors were mentioned? (Exigo, Aice, Rallyware, Party Platform Solutions, Thatcher, Fluid/Shopify, custom-built, other) — note whether they're currently on it, left it, or evaluating it. Does this competitive framing align with `my-gtm-context.md`, or does it surface new intel?

**Positioning Check:**
Do the value props that resonated align with established positioning in `outputs/06-*` (if they exist)? Are there features or outcomes the prospect cared about that current positioning underweights or doesn't mention at all?

**Proof Point Check:**
Did any proof points come up? (Paparazzi $31M stat, LuLaRoe lineage, DSA membership, client logos, Capterra badges) — what was the reaction? What was missing that they asked for or that would have helped?

**The deliverable:**

Present as four short paragraphs using these headers:
- **ICP Fit:** [Full match / Partial match / Edge case / Non-ICP] — [why + deviation detail]
- **Pain Coverage:** [Which pains are known vs. new; what the new pains suggest]
- **Competitive + Proof Points:** [What was surfaced; how it aligns or deviates from current competitive intel and proof assets]
- **Positioning Gaps:** [What resonated that positioning doesn't currently cover; what positioning didn't land]

---

## Task 5: Surface GTM Signals (~10 min)

**Output:** Signal list presented inline — feeds Task 7 cross-skill callout

**What to do:**

Based on Tasks 2–4, identify signals that may be true beyond this one account — things that, if seen again, would change how the GTM system is calibrated.

For each signal, write:
- **Signal:** What was observed (be concrete)
- **Type:** ICP Confirmation / ICP Deviation / Positioning Gap / Product Gap / Competitive Intel / Proof Point Opportunity / Sales Motion Insight / New Segment Signal
- **Strength:** Strong (multiple data points in this call) / Moderate (one clear signal) / Weak (inferred — watch for in other calls)
- **Implication:** What should change or be watched if this signal holds

Then answer these four questions explicitly:

1. **ICP signal:** Does this call confirm or complicate the ICP definition? If it complicates — how exactly?
2. **Positioning signal:** Does the resonance pattern suggest any current positioning or messaging is off, missing, or needs strengthening?
3. **Product signal:** Did the call surface feature gaps, integration requirements, or roadmap signals not tracked in `my-gtm-context.md`?
4. **Sales motion signal:** Did the call reveal anything about DMU structure, buying triggers, objection patterns, or deal timeline that refines the repeatable sales process?

**The deliverable:**

Present as a bulleted signal list with the four questions answered explicitly at the end. Ask: "Any signals I should classify differently or add?"

---

## Task 6: Create or Update the Prospect File (~10–15 min)

**Output:** `prospects/[company-slug].md`

**What to do:**

**If this is a new account (no existing file):**

Create `prospects/[company-slug].md` scaffolded from `prospects/_template.md`. Populate every section using data from Tasks 1–5. Do not leave template placeholder text in the file — either populate with what you know or mark as `[Not yet confirmed]`.

Sections to fill:
- **Header:** Company name, today's date, deal stage (inferred from call type), owner (Daniel Lang unless otherwise specified), GTM segment (from ICP fit check in Task 4)
- **Company Profile table:** website (extract from transcript or `[unknown]`), vertical, active rep count (stated or estimated), geography, company stage, Cash & Carry flag (Yes / No / ~X%)
- **Tech Stack table:** For each layer — back office, ecommerce/storefront, rep payment, rep inventory, CRM, other tools — note the current solution and any satisfaction signal or displacement indicator
- **Competitive context paragraph:** which ByDesign competitors they're on, left, or evaluating, and why
- **Interactions Log:** One row for this call using Task 1 metadata and a 2-sentence summary of the call outcome
- **Confirmed Pains table:** from Task 2
- **Features That Resonated table:** from Task 3 (resonance only — not the blockers table)
- **Blockers table:** from Task 3
- **Key Quotes section:** Pull the 3–5 most significant verbatim quotes from Task 2; include speaker name and role
- **GTM Implications:** Four subsections using the analysis from Task 4 — ICP/segment, positioning, product, sales motion
- **Deal Status & Next Steps table:** Extract explicit next steps from the transcript; assign owner (Daniel Lang default) and due date where stated or inferable
- **Anti-Patterns / Disqualifiers:** Anything making this account a poor fit or non-ICP

**If this account already has a file:**

Read the full existing file first. Then update with discipline:
- **Interactions Log** — append a new row; never overwrite or delete existing rows
- **Confirmed Pains** — update severity scores if new data warrants it (note: "Updated from 3→5 — [speaker] used urgent language on [date]"); add new pains; do not remove any previously confirmed pain without explaining why it's resolved or no longer applicable
- **Features That Resonated** — update enthusiasm scores if changed; add newly mentioned features
- **Blockers** — update status of any blocker addressed in this call; add new blockers
- **Key Quotes** — append; never remove existing verbatim quotes
- **GTM Implications** — rewrite to reflect the full cumulative picture, not just this call; note which call surfaced each new insight inline (e.g., "Confirmed on May 1 demo — Edmond repeated twice")
- **Deal Status & Next Steps** — replace with current state; if archiving prior next steps, add them as a struck-through row or a comment
- **Header** — update "Last updated" date and stage if it changed

**The deliverable:**

Present the complete file content in a code block and say: "This is the complete prospect file. Review before I write it. Any corrections?" Write the file only after confirmation.

---

## Task 7: Update `_index.md` and Cross-Skill Callout (~10 min)

**Output:** `prospects/_index.md` (updated) + cross-skill callout presented inline

**What to do — Part A: Update `prospects/_index.md`**

For new accounts: add a row to the Active Prospects table:
`| [Company](company-slug.md) | [Vertical] | [Rep Count] | [Current Stack] | [Stage] | [C&C Yes/No] | [Date] | [GTM Segment] |`

Also check the "Key Patterns" section — if this call adds or strengthens a pattern, update that section too.

For existing accounts: update the row's Stage, Last Interaction, and any column values that changed. Update Key Patterns if this call adds new signal strength to an existing pattern or surfaces a new one.

Update the "Updated:" date at the bottom.

**What to do — Part B: Cross-Skill Implications**

Produce a callout block telling the user which GTM skills or outputs may need to be revisited. Be explicit — generic implications are useless. Suppress any section where there is genuinely nothing to flag.

**The deliverable:**

```
CROSS-SKILL IMPLICATIONS — [Company Name] | [Date]

[ ] PHASE 2 / COLLECTING INTELLIGENCE
    [Include only if new competitive intel surfaced that isn't in my-gtm-context.md]
    Recommendation: Update outputs/02-[relevant file] or create outputs/[pattern-slug]-intelligence.md
    Specific: [What was learned about which competitor, what changed]

[ ] PHASE 3 / VALIDATING CUSTOMERS
    [Include only if ICP was confirmed or complicated in a meaningful way]
    Recommendation: Review Section [X] of my-gtm-context.md (ICP definition)
    Specific: [What the call confirmed or challenged, and what should be updated]

[ ] PHASE 6 / CRAFTING POSITIONING
    [Include only if a resonance pattern conflicts with or is absent from outputs/06-*]
    Recommendation: Revisit outputs/06-[relevant file]
    Specific: [Which feature/outcome resonated vs. what current positioning covers]

[ ] SDR AGENT — Immediate Next Steps for Daniel
    Run /sdr-agent after reading updated prospects/[slug].md
    Next steps from this call:
    - [Action 1] — Owner: [Name] — Due: [Date or "ASAP"]
    - [Action 2] — Owner: [Name] — Due: [Date]

[ ] NEW OUTPUTS/ FILE WARRANTED
    [Include ONLY if this call confirms a pattern-level insight, not just account-level —
    e.g., a second account confirms the same sub-segment signal, a competitive shift
    appears across multiple accounts, a new ICP variant is emerging with enough signal]
    Recommended file: outputs/[pattern-slug]-intelligence.md
    Reason: [What the file would capture and why it's pattern-level]
```

**When a new `outputs/` file is warranted vs. not:**

Do NOT create an `outputs/` file just because something was interesting. Create one only when:
- A second (or third) account confirms the same pattern first observed in an earlier account
- A competitive shift is observed across multiple calls that isn't captured in `my-gtm-context.md`
- A new ICP sub-segment is confirmed with enough signal to stand as a GTM asset

Named: `outputs/[descriptive-slug]-intelligence.md` — no phase number prefix (matching the existing `02-cash-carry-dso-icp-intelligence.md` naming convention).

---

## Summary

| Task | Output | Time |
|------|--------|------|
| 1. Parse Call Metadata | Confirmation block (inline) | ~5 min |
| 2. Extract Pain Points by Persona | Severity table (inline) | ~10–15 min |
| 3. Extract Feature Resonance & Blockers | Two tables (inline) | ~10 min |
| 4. Map to GTM Context | Structured analysis (inline) | ~10–15 min |
| 5. Surface GTM Signals | Signal list + 4 questions (inline) | ~10 min |
| 6. Create or Update Prospect File | `prospects/[company-slug].md` | ~10–15 min |
| 7. Update Index + Cross-Skill Callout | `prospects/_index.md` + inline | ~10 min |

**Total per call:** ~65–80 min (most of that is reading and reasoning — the actual writing is 20–30 min of active output)

---

## Go Deeper

- **"SPIN Selling Fieldbook" by Neil Rackham** — The Situation / Problem / Implication / Need framework maps directly to the pain extraction logic in Task 2. Makes you better at spotting implied pains the prospect didn't name outright.
- **"Continuous Discovery Habits" by Teresa Torres** — Treats every customer touchpoint as a discovery event, not just formal research sessions. This skill operationalizes that mindset for sales calls.
- **"Competing Against Luck" by Clayton Christensen** — Jobs-to-be-done framing. When a feature resonates, the question is always: what job is the prospect hiring it to do? Sharpens the resonance mapping in Task 3.

---

*GTM Strategist methodology by Maja Voje. 1000+ companies. Proven framework.*  
*Book: https://gtmstrategist.com/book | Masterclass: https://gtmstrategist.com/masterclass*
