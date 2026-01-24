# HubSpot Integration

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

---

### Why It Matters
* **Automatic Enrichment:** Replaces manual spreadsheet exports by continuously updating company data and signal scores inside HubSpot.
* **Smarter Signal Context:** BirdDog adjusts the information it surfaces based on a deal’s stage, helping reps focus on qualifying early-stage leads or closing active deals.
* **Pipeline Calibration:** By accessing deal objects, BirdDog learns from your closed-won data to calculate a "Win Rate Boost" for new prospects.

---

### Application & Authentication
BirdDog connects via a **verified Public App**—**BirdDogScout** (App ID: `16144816`). Following the principle of least privilege, we request only the necessary scopes:

**Required Scopes**
* `crm.objects.companies.read` & `write`
* `crm.schemas.companies.read`
* `oauth`

**Optional Scopes (For Deal Intelligence)**
* `crm.objects.deals.read`
* `crm.schemas.deals.read`

---

### Setup & Connection (0:00 – 0:42)
1.  Log into **BirdDog**.
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

#### Company Mapping
| BirdDog Field | Required | HubSpot Property (Internal Name) | Description |
| :--- | :--- | :--- | :--- |
| `crm_id` | ✅ | `hs_object_id` | Unique HubSpot identifier. |
| `Company_Domain` | ✅ | `domain` or `website` | **Required** for BirdDog to process the account. |
| `BirdDog_Description` | Optional | `birddog_description` | Stores the AI "Why Now" summary. |
| `BirdDog_Score` | Optional | `birddog_score` | Stores the intent rank (0–100). |
| `BirdDog_Link` | Optional | `birddog_link` | URL to the full BirdDog research report. |

#### Deal Mapping (Optional)
| BirdDog Field | Required | HubSpot Property |
| :--- | :--- | :--- |
| `crm_id` | ✅ | `hs_object_id` |
| `crm_company_id` | ✅ | Associated Company ID. |
| `Stage_name` | Optional | Current pipeline stage. |
| `Is_closed/won` | Optional | Used for win-rate backtesting. |

---

### Recommended Company Properties
For the best experience, an Admin should create these fields in **HubSpot Settings → Properties → Company Information**:

| Property Label | Field Type | Purpose |
| :--- | :--- | :--- |
| **BirdDog_Description** | Single-line or Long text | Summary of key "Why Now" insights. |
| **BirdDog_Score** | Number | Proprietary signal score (0–100). |
| **BirdDog_Link** | URL | Link to the full deep-dive report. |
| **BirdDog_Signals** | Rich Text | Bulleted list of the most recent signals. |

---

### Data Sync & User Mapping
* **Daily Sync:** BirdDog refreshes data in a batch operation every day between **5:00 a.m. and 7:30 a.m. ET**.
* **Least Privilege:** BirdDog only reads from mapped properties and only writes to the BirdDog-specific fields you create.
* **User Mapping:** BirdDog identifies users by email. To associate your reps correctly, send a two-column CSV (`email` → `HubSpot user ID`) to **hello@getbirddog.ai**.

---

### Support
📧 **noah@getbirddog.ai** | 📞 **(231) 855-8001**

Would you like me to generate the exact internal property names in a list for you to copy-paste into HubSpot's "Create Property" screen?
