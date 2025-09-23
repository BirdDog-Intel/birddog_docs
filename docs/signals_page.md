# Signals Page

### Walkthrough Video
<div style="position: relative; padding-bottom: 56.25%; height: 0;">
  <iframe src="https://www.loom.com/embed/20c88e16bd0e42aabf978dcf6a40897a?sid=a8492b4f-6ba3-4a57-95d6-b55276f7b974" 
          frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen 
          style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;">
  </iframe>
</div>

---

### Overview
The **Signals Page** is the *heart of BirdDog*. This is where you create and manage the signals that BirdDog searches for across its data sources. A well-crafted set of signals means your reps receive timely, relevant buying intent data directly from news, filings, jobs, and other sources.

---

### Step-by-Step Guide

#### 0:00 – Introduction
- The Signals page = **where you define what BirdDog looks for**.
- Signals are essentially **custom search queries** for accounts.

#### 0:25 – Creating a New Signal
1. Use the **input box** at the top to define a new signal.  
   Example:  
2. Always start with the account variable (`{account}`) in brackets.
3. Pick the **list** you want the signal applied to (e.g., *Enterprise Sales Team*).
4. Give the signal a **title** for tracking.
5. BirdDog will immediately start scanning sources for matching activity.

#### 1:29 – Best Practices for Writing Signals
- Start signals with **“Does”** or **“Is”** (e.g., *Does the account mention hiring multiple roles?*).  
- Think about **behavioral cues**:
- Hiring multiple sales roles
- Sales team required to do account research
- Sales leader engaging with “intent data”  
- Add **disqualifying questions** to filter out noise (e.g., “Exclude recruiting agencies”).

**Sources BirdDog scans:**  
- Press releases  
- News articles  
- Company websites  
- Job postings  
- Earnings calls & reports  

#### 2:54 – Managing Signals
- **Results count:** Shows how many matches BirdDog has found.  
- **Mute option:** Turn off notifications (Slack, Teams, email) for specific signals.  
- **Priority setting:** Mark signals as *High* to:
- Influence account rankings  
- Improve recommendations from **Farsight**  

#### 3:36 – Connecting Templates
- Link a signal directly to an **email template** (created in *Settings*).  
- This makes it easier to act on signals quickly.

#### 3:49 – Editing Signals
- Correct typos, retest queries, or rename titles at any time.  
- Add **BirdDog Context**:  
- This is like a “prompt” to refine how BirdDog interprets signals.  
- Example: “Only show results in US or Europe hiring junior roles.”

#### 4:34 – Teaching BirdDog
- Continuously refine signals as you see results.  
- Add nuances like geography, role level, or business line.  
- Over time, the system learns what matters most to you.

#### 4:42 – Deleting Signals
- If a signal is no longer useful, simply remove it from your list.

---

### Recommendations
- Create **10–15 strong signals** per team to cover different scenarios.  
- Mix **positive buying cues** (new hires, product launches) with **negative/disqualifying ones** (recruiters, unrelated industries).  
- Use **priority levels** to focus reps on the highest-value accounts.  
- Iterate often — BirdDog gets smarter the more you refine signals.

---

### Summary
The Signals Page is where you **train BirdDog to hunt**.  
By writing clear, creative, and precise signals, you ensure your sales team only sees the **most relevant buying triggers**. This saves time, improves targeting, and boosts pipeline quality.

# Signals Guide
*A practical, copy-pasteable playbook for writing A+ signals that your team can use today.*

---

## What is a “Signal” in BirdDog?
A **signal** is a yes/no question you ask BirdDog about a specific company. BirdDog then hunts across public sources (news, press releases, job postings, company websites, earnings calls/reports, etc.) and returns **matches** with summaries, sources, and next steps.

**Golden rules**
1. **Include the account token in brackets** → `Does [account] … ?`
2. **Ask a yes/no question** (start with **Does** or **Is**)
3. **Keep it specific and observable** in public sources
4. **Use BirdDog Context** to add nuance (e.g., regions, role levels, exclusions)
5. **Prioritize** the most valuable signals (set to *High* when it should drive action)

---

## Anatomy of a Great Signal
**Pattern:**  
`Does [account] <observable behavior or announcement> <with qualifiers> ?`

**Examples of good qualifiers**
- **What** (product, team, program, policy)  
- **Where** (US, EU, APAC, specific states/countries)  
- **Who** (roles, leadership titles)  
- **When** (recently, newly, announced/launch/hiring now)  
- **Why/Impact** (expansion, consolidation, pilot, migration)

**Use BirdDog Context to refine**  
> “Only include results from US or Europe; prioritize junior to mid-level roles; exclude staffing agencies.”

---

## Quick Start: 25 “Starter Pack” Signals (copy-paste)
Use these to cover the essentials. Mark priority = **High** for your top 5–8.

1. `Does [account] have any mergers or acquisitions (M&A) in progress or recently announced?`  
2. `Has [account] announced new venture capital or private equity funding?`  
3. `Is [account] expanding into a new market or geography?`  
4. `Has [account] appointed new leadership (CEO, CRO, CMO, CIO, CISO, VP Sales, VP Marketing)?`  
5. `Has [account] launched any new products or major features?`  
6. `Is [account] hiring multiple sales roles (AEs/SDRs) at once?`  
7. `Is [account] hiring roles related to digital transformation or modernization?`  
8. `Is [account] hiring data, AI/ML, or analytics roles?`  
9. `Is [account] hiring security or compliance roles?`  
10. `Has [account] opened a new office or facility?`  
11. `Has [account] announced layoffs, restructuring, or a reorg?`  
12. `Is [account] migrating to or standardizing on a specific cloud provider?`  
13. `Does [account] mention vendor consolidation or tool rationalization?`  
14. `Is [account] running pilots or proofs of concept (POCs)?`  
15. `Has [account] issued an RFP or tender in our category?`  
16. `Does [account] mention new partnerships or alliances?`  
17. `Has [account] won government or enterprise contracts recently?`  
18. `Is [account] pursuing certifications or audits (SOC 2, ISO 27001, FedRAMP, HIPAA)?`  
19. `Has [account] announced a strategic initiative or transformation program?`  
20. `Has [account] reported material changes in earnings calls related to our solution area?`  
21. `Is [account] adopting or sunsetting relevant technologies or platforms?`  
22. `Is [account] expanding headcount rapidly in our ICP functions?`  
23. `Does [account] mention intent data, account research, or programmatic outbound?`  
24. `Has [account] entered new vertical segments or customer tiers?`  
25. `Is [account] experiencing incidents or outages that may drive urgency?`

> **Tip:** If a starter signal is noisy, add a **disqualifier** (see section below) and/or refine with **Context**.

---

## Essentials by Category (simple versions you can paste)

### Funding & Corporate Actions
- `Has [account] announced new funding (seed, A, B, C, PE)?`  
- `Does [account] have any M&A activity (acquiring or being acquired)?`  
- `Has [account] divested a business unit or asset?`

### Leadership & Org Changes
- `Has [account] hired a new CRO/Head of Sales?`  
- `Has [account] hired a new CMO/VP Marketing?`  
- `Has [account] hired a new CIO/CTO/CISO?`  
- `Has [account] restructured or reorganized departments relevant to our solution?`

### Product, Program & Strategy
- `Has [account] launched a new product, platform, or feature relevant to our solution?`  
- `Is [account] running a pilot or POC in our category?`  
- `Does [account] mention a transformation initiative (e.g., digital, data, AI, security)?`

### Hiring & Team Signals
- `Is [account] hiring multiple sales roles (AEs/SDRs) concurrently?`  
- `Is [account] hiring data/AI/analytics roles?`  
- `Is [account] hiring security/compliance roles?`  
- `Is [account] hiring revops or sales operations roles?`

### Market Expansion & Partnerships
- `Is [account] entering a new market or region?`  
- `Has [account] announced a partnership or alliance relevant to our solution?`  
- `Has [account] opened a new office or facility?`

### Tooling & Technology
- `Is [account] migrating to a specific cloud (AWS/Azure/GCP)?`  
- `Is [account] consolidating vendors or rationalizing tools?`  
- `Has [account] adopted/replaced a core platform in our ecosystem?`

### Risk, Compliance & Events
- `Has [account] faced a notable incident/outage with customer impact?`  
- `Is [account] pursuing SOC 2/ISO 27001/HIPAA/FedRAMP certification?`  
- `Has [account] announced regulatory exposure or deadlines that relate to our solution?`

---

## Disqualifier Signals (reduce noise)
Create explicit “no-go” signals to keep your feed clean. These are still yes/no, but you’ll **mute** or treat them as *negative filters*.

- `Is [account] primarily a recruiting or staffing firm (disqualify)?`  
- `Is [account] a consumer-only (B2C) brand with no B2B motion (disqualify)?`  
- `Is [account] outside of our supported geographies (disqualify)?`  
- `Does [account] exclusively serve SMB/micro-SMB if we target enterprise (disqualify)?`  
- `Does [account] lack a sales/marketing function (disqualify)?`  

> Use **Context**: “Exclude staffing firms, agencies, and holding companies; focus on B2B.”

---

## Frameworks for Writing Signals

### A. Simple Grammar Builders
- `Does [account] mention <topic/tech/initiative>?`  
- `Is [account] hiring <roles/functions>?`  
- `Has [account] announced <event/change>?`  
- `Is [account] expanding into <market/region>?`  
- `Is [account] consolidating or replacing <tool/category>?`

### B. Persona → Pain → Trigger
- **Persona** (Sales, Marketing, IT, Security)  
- **Pain** (pipeline growth, enablement, compliance, modernization)  
- **Trigger** (new leader, hiring burst, regulation, outage)  
**Signal:**  
`Does [account] have a new CISO and mention security modernization or compliance gaps?`

### C. Buying Stage Ladder
- **Awareness** → mentions problem/opportunity  
- **Consideration** → hiring/programs/budgets  
- **Decision** → RFPs, pilots, platform choices  
**Signals:**  
- `Does [account] mention challenges in <problem area>?`  
- `Is [account] hiring a leader to own <category>?`  
- `Has [account] issued an RFP related to <category>?`

### D. Change-Event → Outcome
`Has [account] <change_event> to achieve <desired_outcome>?`  
- `Has [account] centralized GTM operations to grow the company?`

### E. Time & Place Qualifiers (use Context)
- Region: “US, Canada, UK, EU only”  
- Time: “Prioritize the last 90 days”  
- Level: “Leadership announcements and manager+ roles only”

---

## BirdDog Context: Make It Smarter
Use the **Context** box on a signal to coach BirdDog:
- “Only include US & EU, exclude agencies and resellers.”  
- “Prioritize job postings that indicate ‘build from scratch’, ‘migration’, or ‘greenfield’.”  
- “Consider variants of the company name and product brands.”  

This keeps the signal wording simple, while your **Context** adds nuance.

---

## Priority & Workflow Recommendations
- Mark the top revenue drivers as **High** priority (e.g., *new CRO*, *hiring multiple AEs*, *RFP*).  
- Connect **email templates** to your most actionable signals for instant outreach.  
- In **Signals view**, work newest/highest priority first → **Enter** to advance → copy message → push to CRM → **D** to dismiss.

---

## ICP Packs (industry-flavored ideas)

### SaaS / Software
- `Does [account] mention product-led growth or self-serve motion?`  
- `Is [account] hiring developer relations or solutions engineering?`  
- `Has [account] adopted a new data stack component (dbt/Snowflake/etc.)?`

### Manufacturing / Industrial
- `Is [account] opening or expanding a plant, warehouse, or line?`  
- `Is [account] hiring automation/controls engineers?`  
- `Has [account] announced supply chain modernization or traceability programs?`

### Healthcare / Life Sciences
- `Is [account] hiring clinical informatics or compliance roles?`  
- `Is [account] pursuing HITRUST or HIPAA initiatives?`  
- `Has [account] partnered with payers/providers or expanded care sites?`

### Financial Services / Insurance
- `Has [account] announced risk/compliance initiatives (AML, KYC, SOX)?`  
- `Is [account] hiring fraud, risk, or data science roles?`  
- `Has [account] launched a new digital banking/claims product?`

### Public Sector / Education
- `Has [account] posted RFPs or tenders relevant to our category?`  
- `Is [account] hiring modernization or cybersecurity roles?`  
- `Is [account] expanding grants-funded programs (CARES/ARPA/etc.)?`

---

## Role-Specific Packs

### SDR / BDR
- `Is [account] hiring multiple AEs/SDRs?` (signals budget & growth)  
- `Has [account] opened a new region?`  
- `Does [account] mention vendor consolidation?`

### AE / New Business
- `Has [account] hired a new CRO/VP Sales with mandate for change?`  
- `Has [account] announced a transformation initiative overlapping our value?`  
- `Is [account] running an RFP/POC in our category?`

### CSM / AM (Upsell/Cross-sell)
- `Has [account] launched a new product line?`  
- `Is [account] expanding headcount in certain teams?`  
- `Has [account] created a center of excellence or standardization initiative?`

---

## Advanced Patterns (when you’re ready)

- **Competitor displacement**  
  `Does [account] mention replacing <competitor/product category>?`
- **Migration**  
  `Is [account] migrating from legacy <platform> to <new platform>?`
- **Consolidation**  
  `Does [account] plan to consolidate <tool category> to reduce cost?`
- **Compliance deadline**  
  `Has [account] referenced upcoming compliance deadlines?`
- **Incident response**  
  `Has [account] reported incidents/outages?`
- **Earnings signal**  
  `Has [account] cited investments or constraints in <theme> during earnings calls?`

---

## Templates Library (fill-in-the-blanks)

**General**
- `Does [account] mention <initiative/topic> in recent announcements?`  
- `Is [account] hiring <role/function> to drive <goal>?`  
- `Has [account] launched <program/product> for <market/segment>?`

**Go-to-Market**
- `Does [account] require reps to conduct account research or use intent data?`  
- `Is [account] expanding outbound teams or territories?`

**Technology**
- `Is [account] standardizing on <cloud/data/security> platforms?`  
- `Has [account] deprecated or sunset <tool> in favor of <tool>?`

**Operations / Finance**
- `Does [account] mention cost optimization or vendor consolidation?`  
- `Has [account] established a center of excellence for <function>?`

**Risk / Compliance**
- `Is [account] pursuing <SOC 2/ISO/FedRAMP/HIPAA> compliance?`  
- `Has [account] cited regulatory pressure in <region/industry>?`

> **Pro move:** Pair each template with **Context** (region/role/recency) and set *High* priority if it should change rep behavior today.

---

## Troubleshooting Your Signals

**Too few results?**
- Use broader terms; remove niche jargon.  
- Split one complex signal into **two simpler** ones.  
- Add variants to **Context** (synonyms, brand names, acronyms).

**Too noisy?**
- Add a **disqualifier** signal (e.g., exclude agencies).  
- Add qualifiers (leadership level, geography, role seniority).  
- Use **Context** to specify “must include <key phrases>”.

**Unclear actionability?**
- Tie each signal to a **template** and **next step** (e.g., SDR email, AE call, CRM task).  
- Mark non-actionable “FYI” signals to **Normal** priority, actionable to **High**.

---

## Quality Checklist (before you hit “Add”)
- ✅ Starts with **Does/Is** and includes `[account]`  
- ✅ Observable in public sources BirdDog covers   
- ✅ Priority matches the revenue impact  
- ✅ Linked to an email template (for top signals)

---

## Worked Examples (from rough idea → final signal)

**Idea:** “I care when they’re hiring lots of salespeople.”  
- *Draft:* `Is [account] hiring salespeople?`  
- *Better:* `Is [account] hiring **multiple** sales roles (AEs/SDRs) at once?`  
- *Context:* “US & EU, exclude staffing agencies; prioritize postings that mention ‘new logo acquisition’ or ‘prospecting’.”  
- *Priority:* **High**

**Idea:** “I want to know about vendor consolidation.”  
- *Draft:* `Does [account] mention vendor consolidation?`  
- *Better:* `Does [account] mention consolidating or rationalizing tools in <our category>?`  
- *Context:* “Look for terms: ‘consolidate vendors’, ‘tool rationalization’, ‘platform standardization’.”  
- *Priority:* **High**

---

## Keep Iterating
- Start with the **Starter Pack** + 3–5 ICP-specific signals.  
- Review results after a week → refine wording and **Context**.  
- Promote your best performers to **High** priority and connect templates.  
- Retire or mute weak signals; add **disqualifiers** to reduce noise.  
- Pair with **Farsight** (Auto-Add) to keep your lists full of strong-fit accounts.

---

*Need help?* Drop us a note and we’ll review your first 10–15 signals and suggest improvements tailored to your ICP, motion, and territories.
