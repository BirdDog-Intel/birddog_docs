# Frequently Asked Questions (FAQ)

## General
**What is BirdDog and how does it work?**  
BirdDog monitors public signals (news, job postings, company sites, filings, earnings calls/reports, social) for your target accounts. You define **Signals** (questions you want BirdDog to answer about accounts), and BirdDog surfaces matches with source links, summaries, and next-step actions. **Farsight** improves your account list over time by replacing weak accounts with stronger ones.

**How does BirdDog find buying signals?**  
It continuously crawls and analyzes public data, matching it to your **Signals**. When a match is found (e.g., “hiring multiple AEs” or “new CRO”), BirdDog summarizes why it matters and links to the original source.

**What data sources does BirdDog use?**  
Press releases, news sites, company websites, job boards/postings, SEC/financial filings, earnings calls/reports, and certain social/professional sources. You can see source links on each signal.

**How often is account and signal data refreshed?**  
BirdDog refreshes daily; Farsight recommendations and account rescoring also update **nightly**.

**Can I integrate BirdDog with my CRM (HubSpot, Salesforce, etc.)?**  
Yes. From an account, you can jump directly to CRM records (HubSpot/Salesforce). To set this up, email hello@getbirddog.ai or reach out to the team in your Slack channel.

**What keyboard shortcuts should I know to work faster?**  
- **Enter**: Open *Next Steps* / advance the current signal  
- **I**: Open account’s LinkedIn page  
- **D**: Dismiss a signal in Signals view  
- **Y / N**: Accept / Dismiss Farsight recommendations

---

## Accounts & Credits
**What are BirdDog credits?**  
Credits are monthly allowances to **add/replace** accounts being actively monitored. Each active account consumes capacity; credits let you swap in new ones.

**How do credits reset each month?**  
They reset automatically at the start of your billing cycle. You’ll see your **credits available** and **accounts you can add now** in Account Manager.

**What happens if I hit my account limit?**  
You won’t be able to add new accounts until you **archive** some existing ones (freeing capacity, when available) or your credits reset.

**How do I archive accounts to free up space?**  
In **Account Manager**, select accounts → **Archive**. Archived accounts stop daily monitoring and free up capacity for new adds.

**What’s the difference between deleting and archiving accounts?**  
- **Archive**: Keeps history but pauses monitoring (recommended).  
- **Delete**: Removes the account permanently from your tenant (use cautiously).

**How do I upload new accounts into BirdDog?**  
In **Account Manager** → paste one or more **company URLs** (or a CSV list) into the input → choose the **target list** → **Add**.

**Can I upload accounts from tools like Apollo or ZoomInfo?**  
Yes. Export domains/URLs from those tools and paste/upload into BirdDog (Account Manager or Farsight My List Mode).

**Why do some accounts show a score of 0?**  
They’re newly added or still scraping. Scores typically appear within ~20-60 minutes as BirdDog ingests and analyzes sources.

---

## Lists
**What are lists in BirdDog?**  
Lists are **buckets of accounts** that you can target with different Signals or strategies (e.g., Enterprise, Healthcare, EMEA).

**How do I create a new list?**  
In **Account Manager** → Lists panel → **Create** (name the list). (If you don’t see Create, you may lack permissions—ask an admin.)

**Can accounts belong to multiple lists?**  
Yes. A domain can live in more than one list (e.g., Master + Enterprise).

**How do I rename or delete a list?**  
In **Account Manager** → Lists panel → choose list → **Rename** or **Delete**. Deleting a list doesn’t delete the accounts globally; it removes the list container.

**Can I export a list of accounts?**  
Yes. Use checkboxes to select accounts → **Export** (CSV).

**What’s the best way to organize lists (by industry, region, team)?**  
Use **segments you’ll actually filter by**: enterprise vs. mid-market, regions (NA/EU), or verticals (SaaS/Healthcare). Keep it simple and aligned to territory owners.

---

## Signals
**What is a signal in BirdDog?**  
A **question** BirdDog answers about your accounts (e.g., “Does the account mention hiring multiple sales roles?”). When true, BirdDog creates an alert with summary + sources.

**How do I create a new signal?**  
On **Signals** page → input box → phrase your question (start with *Does* / *Is*) → choose **target list** → title it → **Add**.

**What’s the best way to write a good signal?**  
- Start with **Does/Is** (clear boolean framing)  
- Anchor to **behaviors** (hiring, leadership changes, tooling, geography)  
- Add **disqualifiers** (e.g., exclude recruiters)  
- Keep it specific and test iteratively

**What are disqualifying signals?**  
Rules that remove noise (e.g., “Exclude recruiting agencies”). Add as negative filters to keep your feed clean.

**How do I mute a signal?**  
On **Signals** page, toggle **Mute** to stop Slack/Email/Teams notifications (the signal still runs/accumulates results).

**What does signal priority do?**  
It influences **account rankings** and **Farsight** recommendations. *High* priority signals weigh more heavily in scoring.

**How do I connect signals to email templates?**  
Create templates in **Settings** or **Team Page** → on Signals, associate a template to prefill suggested outreach when a match occurs.

**Can I edit or delete a signal later?**  
Yes. Click **Edit** to change wording/title/priority/context; **Delete** to remove entirely.

**How do BirdDog Context refinements work?**  
Use the **Context** field (a free-form prompt) to teach BirdDog nuance (e.g., “Only show US/EU and junior roles”). Update as you learn.

**How many signals should I create?**  
Start with **10–15 per team** (mix of positive buying cues + disqualifiers). Add more once you see which ones perform.

---

## Farsight
**What is Farsight?**  
BirdDog’s **recommendation engine** that improves your account list by promoting strong-fit accounts and demoting/removing weak ones.

**What is the difference between My List Mode and Entire Internet Mode?**  
- **My List Mode**: You upload a list (up to 10k domains). Farsight cleans, scores, and replaces poor performers.  
- **Entire Internet Mode**: You set ICP parameters (size, geo, sector). BirdDog finds net-new lookalikes across the web.

**How do I upload a list for Farsight to clean?**  
In **Farsight → My List Mode** → upload company URLs (CSV or paste) → set thresholds (e.g., replace <10 with >30 points) → **Save & Run**.

**What is Auto-Add in Farsight?**  
A rule that **automatically inserts** recommended accounts when they meet your thresholds (score, signals, list cap).

**Can Farsight replace low-scoring accounts automatically?**  
Yes. Configure **replacement thresholds** (e.g., remove <10 pts when a >30 pt alternative appears) and enable Auto-Add.

**How often does Farsight update recommendations?**  
It reviews and recommends **nightly** when there are under 20 recommendations waiting, with ongoing refreshes as new signals appear.

**What’s the best way to set thresholds in Auto-Add?**  
- Start conservative: add only **>30 points** with at least **one high-priority signal**  
- Respect list caps  
- Tune after a week based on quality

---

## Account Manager
**What is the Account Manager page used for?**  
To **add, archive, delete, export, filter**, and **organize** accounts into lists. It’s your operational control center.

**How do I filter accounts in Account Manager?**  
Use the filter button (by name, list, status, score, signal presence, location, size). Combine filters for precise selections.

**How do I bulk archive or delete accounts?**  
Select via checkboxes → choose **Archive** or **Delete** in bulk actions. Archiving is safest for capacity management.

**Can I upload accounts directly into Account Manager?**  
Yes. Paste URLs or upload a CSV into the input box, pick a **target list**, then **Add**.

**How do account scores update after adding them?**  
BirdDog scrapes and scores within ~20 minutes; scores then evolve as new signals arrive.

---

## Team Management
**How do I invite a new user to BirdDog?**  
On **Team Page** → **Invite New User** → enter email → assign accounts → (optional) include org signals/templates → **Create** → **Send Email**.

**How do I allocate accounts to users?**  
In the user table, set **Allocated Accounts** for each user. Adjust anytime to match usage.

**What happens if a user isn’t using all their accounts?**  
Lower their allocation to free capacity for others or Farsight. You can raise it again later.

**Can I reassign accounts from one user to another?**  
Yes. Archive from User A and add to User B; or use admin tools to move account/list ownership (depending on your plan/permissions).

**How do I send onboarding emails to new users?**  
After creating the user, click **Send Email** to dispatch login details, tips, and getting-started guides.

**Can I share signals with my whole team?**  
Yes. Use **Organization Signals** on the Team Page to publish a signal template to all users.

**How do organization-wide templates work?**  
Admins create **signal** and **email** templates once and push them to all users, ensuring consistent strategy and messaging.

**Can admins see all user activity?**  
Admins can see user allocations/usage and outcomes associated with accounts/signals. For deeper audit trails, contact support for plan capabilities.

---

## Email Templates
**How do I create an email template in BirdDog?**  
On **Team Page** (or Settings for non-admins) → **Create Email Template** → add **Title**, **Example**, and **Template** (with variables) → **Save**.

**How do I connect an email template to a signal?**  
On the **Signals** page, choose the signal → **Link Template**. When the signal fires, your template is ready with context.

**Can email templates be shared across the whole team?**  
Yes. Create them as **organization templates** on the Team Page and apply them to org-wide signals.

**Can I edit or delete an email template?**  
Yes. Open the template → **Edit** or **Delete**. Edits apply to future uses (past messages remain unchanged).

**What’s the difference between example emails and templates?**  
- **Example**: A sample for guidance.  
- **Template**: A reusable, parametrized message tied to Signals.

---

## Notifications
**What notifications can BirdDog send (Slack, Teams, Email)?**  
Signal alerts can be delivered to **Slack**, **Microsoft Teams**, and **Email**. 

**How do I mute or unmute notifications for a signal?**  
On **Signals** page, toggle **Mute** for that signal (alerts stop; the signal still runs).

---

## Shortcuts & Productivity
**What does pressing Enter on the keyboard do?**  
Opens **Next Steps** and advances your workflow for the current signal.

**What does pressing I do?**  
Opens the account’s **LinkedIn** page.

**What does pressing Y or N do in Farsight?**  
**Y** accepts and adds the recommended account; **N** dismisses it.

**What does pressing D do in Signals view?**  
Dismisses the current signal and advances to the next.

**Are there other keyboard shortcuts I should know?**  
Those are the core ones. Shortcuts may expand over time; check the in-app **Need Help** link for updates.

---

## Data & Sources
**Where does BirdDog pull its information from?**  
Public web sources: press/news, company sites, job posts, filings, earnings, and select social/professional platforms.

**How reliable are the sources BirdDog uses?**  
Signals include **source links** so you can verify context yourself. BirdDog summarizes but never hides the original source.

**Can I see the sources behind each signal?**  
Yes. Every signal shows linked sources used to generate the summary.

**How does BirdDog summarize source data?**  
It extracts the **relevant snippet**, builds a concise summary, and highlights why it matters (e.g., hiring surge, leadership change).

**Can I customize which sources BirdDog looks at?**  
You can steer **what** it looks for via Signals and **context**. Source-level whitelisting/blacklisting may depend on plan; ask support.

---

## Best Practices
**How many accounts should I actively manage at once?**  
Focus on what your reps can truly work (e.g., **50–200 each**, depending on motion). Use Farsight to keep quality high.

**How many signals should I create per team?**  
Start with **10–15** (mix of buying cues + disqualifiers). Iterate weekly based on performance.

**How often should I clean/archive accounts?**  
At least **monthly** (credit reset). Use Farsight’s replacement rules to automate cleanup.

**How should I prioritize signals for the best results?**  
Mark critical triggers as **High** (e.g., “hiring multiple AEs,” “new CRO,” “new funding/market entry”). Tie to your strongest templates.

**How should I set thresholds in Farsight for my industry?**  
Start **Score >30** with at least **1 high-priority signal**. Adjust by observed quality (raise the bar if SDRs complain about fit).

**What’s the best workflow for working signals daily?**  
Open **Signals view** → sort by recency/priority → **Enter** to work → **Generate message** → push to CRM → **D** to dismiss → repeat.

**How can BirdDog help me find “hidden” opportunities?**  
Use creative Signals (e.g., “pilot program,” “POC,” “migration,” “RFP,” “consolidation,” “sunsetting”). BirdDog surfaces less obvious but actionable triggers.

---

## Troubleshooting
**Why isn’t my account scoring correctly?**  
Newly added (wait ~20-60 min), sparse public data, or weak Signals. Add more/better Signals and context; ensure domain/URL is correct.

**Why aren’t signals showing results yet?**  
They may be too narrow or brand-new. Broaden phrasing, remove disqualifiers, or give it a day for crawling.

**Why do I see duplicates of an account?**  
The same company might sit in multiple lists or use variant domains. Consolidate to a **canonical domain** and merge/clean lists.

**Why can’t I create a new list as an admin?**  
You may be on a restricted role or environment setting. Check permissions or ask your BirdDog admin/support to enable list creation.

**How do I fix onboarding emails not sending?**  
Verify the user exists, click **Send Email** again, and have the user check spam. If still blocked, contact support to confirm domain policy.

**Why isn’t my CRM integration working?**  
Confirm the CRM connection is authorized, that the account exists in your CRM, and that pop-ups/redirects aren’t blocked.

**Who do I contact for support?**  
Reach out via **Slack**, **email**, or **LinkedIn** (as noted in-app). Include screenshots, account URLs, and a short description.

---

## Advanced
**Can I use BirdDog with custom APIs?**  
Some advanced plans support custom hooks/integrations. Share your use case with support to review feasibility.

**Can I run A/B tests with signals?**  
Yes—make a signals with slight variations in phrasing/priority and track result volume/quality over a fixed window.

**Can I rank accounts manually in addition to signals?**  
You can adjust **signal priority**, which influences ranking. Manual rank nudges may be available depending on plan.

**Can I track performance by signal type?**  
Yes—monitor results count, engagement from templates tied to each signal, and downstream outcomes in your CRM reports.
