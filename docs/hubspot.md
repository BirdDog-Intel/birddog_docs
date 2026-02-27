# BirdDog HubSpot Integration

### Walkthrough Video
<div style="position: relative; padding-bottom: 56.25%; height: 0;">
  <iframe src="https://www.loom.com/embed/6a8df3126ebd4acfaee4cdc08a4beee6" 
          frameborder="0" 
          webkitallowfullscreen 
          mozallowfullscreen 
          allowfullscreen 
          style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;">
  </iframe>
</div>

---

### Overview
The **HubSpot integration** connects BirdDog directly with your CRM, allowing your account data, signals, and research insights to sync seamlessly. Once connected, BirdDog pushes enriched company data, intent scores, and "Why Now" summaries straight into HubSpot records—giving your reps instant access to actionable intelligence inside their daily workflow.

### Why It Matters
* **Automatic Enrichment:** Replaces manual spreadsheet exports by continuously updating company data and signal scores inside HubSpot.
* **Smarter Signal Context:** BirdDog adjusts the information it surfaces based on a deal’s stage, helping reps focus on qualifying early-stage leads or closing active deals.
* **Pipeline Calibration:** By accessing deal objects, BirdDog learns from your closed-won data to calculate a **"Win Rate Boost"** for new prospects.

---

### Application & Authentication
BirdDog is a **verified Public App** available on the [HubSpot App Marketplace](https://ecosystem.hubspot.com/marketplace/listing/birddog-scout).

* **App Name:** BirdDogScout
* **App ID:** `16144816`

Following the principle of least privilege, we request only the necessary scopes:

### Application Scopes & Permissions
BirdDog follows the principle of least privilege. The following scopes are used to facilitate the sync between BirdDog and HubSpot:

| Scope | Requirement | Purpose |
| :--- | :--- | :--- |
| `crm.objects.companies.read` | **Required** | Identify existing companies to track. |
| `crm.objects.companies.write` | **Required** | Enrich HubSpot records with BirdDog data. |
| `crm.schemas.companies.read` | **Required** | Understand custom property structures. |
| `oauth` | **Required** | Securely connect the BirdDog and HubSpot apps. |
| `crm.schemas.deals.read` | Suggested | Enables context-aware alerts for active deals. |
| `crm.objects.deals.read` | Suggested | Reads deal data to calculate "Win Rate Boost." |
| `crm.objects.owners.read` | Suggested | Attributes signals to the correct account owner. |
| `sales-email-read` | Suggested | Refines engagement scores based on activity. |
| `crm.schemas.companies.write`| Suggested | Allows BirdDog to update custom property definitions. |

---

### Setup & Connection (0:00 – 0:42)
While it is necessary to give BirdDog access to your Company object to make the integration work, the Deal object is optional but unlocks significant value for your sales team. The mapping can be completed & updated at any time via the BirdDog Platform, after integration is complete. 

1.  Log into the **BirdDog Platform**.
2.  Navigate to **Settings → Integrations** (bottom-left corner).
3.  Click on **HubSpot**.
4.  Leave the environment as **Default** (unless testing in a Sandbox).
5.  Click **Submit** and select your HubSpot account. Review permissions and click **Connect App**.

---

### Configuration Paths (0:45 – 1:55)

#### Option 1: One-Click Setup (Recommended)
This is the fastest way to sync. BirdDog will look for a specific set of properties in your CRM.
1.  **Create the Recommended Properties** (see the table below) in your HubSpot Settings.
2.  Return to BirdDog and click **"I've created these fields."**
3.  The system will automatically link and begin the initial sync.

#### Option 2: Custom Setup
Use this for complex CRM setups where you want to map BirdDog data to existing custom HubSpot properties.
1.  Select **Custom Setup**.
2.  Manually map the BirdDog fields to your preferred HubSpot properties using the tables below.

---

### Technical Field Mappings

### Company Mapping & Property Configuration
For the best experience, an Admin should create these fields in **HubSpot Settings > Properties > Company Information**. BirdDog uses these fields to push enriched data directly into your CRM. 

| BirdDog Field | Required | HubSpot Internal Name | Field Type | Description / Purpose |
| :--- | :---: | :--- | :--- | :--- |
| `crm_id` | ✅ | `hs_object_id` | Read Only | Unique HubSpot identifier used for syncing. |
| `Company_Domain` | ✅ | `domain` or `website` | Domain/URL | **Required** for BirdDog to identify and process the account. |
| `BirdDog_Description`| Optional | `birddog_description` | Single-line text | Stores the AI "Why Now" summary of the company’s fit. |
| `BirdDog_Score` | Optional | `birddog_score` | Number | Proprietary rank (0–100). Scores >10 indicate high value. |
| `BirdDog_Link` | Optional | `birddog_link` | URL | Direct link to the full research report on the BirdDog platform. |
| `BirdDog_Signals` | Optional | `birddog_signals` | Rich Text | A formatted, bulleted list of the most recent signals found. |
| `BirdDog_Originated` | Optional | `birddog_originated` | Single Checkbox | Records if the account was discovered/originated by BirdDog. |
| `BirdDog_Add_Date` | Optional | `birddog_add_date` | Date & Time | The date the account was originally added to BirdDog. |
| `BirdDog_Signal_List`| Optional | `birddog_signal_list` | Multi-Checkbox | A list of signal tags (e.g., Funding, Hiring). *See note below.* |

> **Note on BirdDog Signal List:** When creating this property, you do not need to manually enter every signal as an option. Simply enter one temporary placeholder (e.g., "Pending"); the BirdDog system will automatically override and populate the correct tags during the first sync.

#### Deal Mapping (Optional)

Mapping the below fields into BirdDog will help the system provide better signal data & recommendations based on the status of each company in HubSpot. Additionally, BirdDog will be able to leverage these fields to backtest signals to see which ones are most strongly correlated with closed won deals.
| BirdDog Field | Required | HubSpot Property | Purpose |
| :--- | :--- | :--- | :--- |
| `crm_id` | ✅ | `hs_object_id` | Unique identifier for the deal. |
| `crm_company_id` | ✅ | `hs_primary_associated_company` | Links the deal to the correct account. |
| `Stage_name` | Optional | `dealstage` | Adjusts signal priority based on pipeline stage. |
| `Is_closed/won` | Optional | `hs_is_closed_won` | Used for win-rate backtesting and calibration. |

---

### Data Sync & User Mapping
* **Daily Sync:** BirdDog refreshes data in a batch operation every day between **5:00 AM and 7:30 AM ET**.
* **Initial Sync:** During the first week, expect a higher number of requests as the system calibrates its sync with your CRM history.
* **User Mapping:** BirdDog identifies users by email. To associate your reps correctly, please send a two-column CSV (`email` → `HubSpot user ID`) to **hello@getbirddog.ai**.

---

### Request Limits
The BirdDog integration leverages the batch upload API for HubSpot to limit the amount of transactions needed per day. Generally, a daily sync will occur between 5 am and 9 am et, where BirdDog pulls the designated accounts and writes updates to their designated BirdDog fields. 

From time to time, there will be additional push and pulls, such as when users upload new companies or request an immediate refresh on certain data. 

Additionally, during the first week of the integration, expect a higher number of requests as the system calibrates its sync with your crm.

---

### Support
📧 **noah@getbirddog.ai** | 📞 **(231) 855-8001**
