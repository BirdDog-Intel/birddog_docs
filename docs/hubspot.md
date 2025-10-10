# HubSpot Integration

### Walkthrough Video
<div style="position: relative; padding-bottom: 56.25%; height: 0;">
  <iframe src="https://www.loom.com/embed/3d4fa5d8fbc047a6b40c61521be1d7e7?sid=9c40775f-7cd5-48b9-aedf-9dff339fef61"
          frameborder="0"
          webkitallowfullscreen
          mozallowfullscreen
          allowfullscreen
          style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;">
  </iframe>
</div>

### Overview
The **HubSpot integration** connects **BirdDog** directly with your CRM, allowing your account data, signals, and research insights to sync seamlessly between both systems.  

Once connected, BirdDog can push enriched company data, scores, and recommendations straight into HubSpot records — giving your reps instant access to actionable intelligence inside their CRM.

---

## Why It Matters
Integrating BirdDog with your CRM provides two major benefits:

1. **Automatic Syncing of Companies** — BirdDog continuously updates company data and signal scores, ensuring your reps always have the latest intelligence inside HubSpot.  
   This replaces manual uploading and exporting between spreadsheets.

2. **Smarter Signal Context** — BirdDog adjusts the information it surfaces based on each deal’s stage.  
   Your reps see different signals for early-stage outreach vs. long-term deals, helping them focus on what matters most in the moment.

To deliver both benefits, BirdDog must access **company** and optionally **deal** objects within your CRM.

---

## Setup (0:00 – 0:31)
1. Log into **BirdDog**.  
2. Navigate to **Settings → Integrations** in the bottom-left corner.  
3. Click on **HubSpot**.  
4. Leave the dropdown as **Default** unless testing in a sandbox environment.  
5. Click **Submit** to begin the connection process.  

You’ll be redirected to HubSpot to confirm access.

---

## Connecting to HubSpot (0:31 – 0:42)
1. Select your **HubSpot account** (if you have more than one).  
2. Click **Choose Account**.  
3. Review the permissions summary and click **Connect App**.  

You’ll then be directed back to BirdDog, where you can map your CRM fields.

---

## Application & Authentication
BirdDog connects via a **verified unlisted Public App** — **BirdDogScout** (App ID: `16144816`).  

Following the principle of least privilege, BirdDog requests only the scopes needed for operation:

**Required Scopes**
- `crm.objects.companies.read`  
- `crm.objects.companies.write`  
- `crm.schemas.companies.read`  
- `oauth`  

**Optional Scopes**
- `crm.objects.deals.read`  
- `crm.schemas.deals.read`  

Only one user needs to authenticate your organization through OAuth in BirdDog. After authentication, you’ll map HubSpot fields to BirdDog fields.

---

## Field Mapping (0:42 – 1:20)
On the mapping page, define how BirdDog’s data aligns with your HubSpot properties.  

### Company Mapping
| Field | Required | Description |
|-------|-----------|-------------|
| `crm_id` | ✅ | Object ID of the company, typically `hs_object_id`. |
| `Company_Domain` | ✅ | Company website URL (`domain` or `website`). |
| `BirdDog_Description` | Optional | Stores BirdDog’s “Why Now” summary. |
| `BirdDog_Score` | Optional | Stores BirdDog’s company score (0–100). |
| `BirdDog_Link` | Optional | Direct link to the BirdDog company profile. |
| `BirdDog_User` | Optional | Associates the account with the BirdDog user. |

> BirdDog can only process companies that have a website domain in HubSpot.

### Deal Mapping
| Field | Required | Description |
|--------|-----------|-------------|
| `crm_id` | ✅ | HubSpot deal ID (`hs_object_id`). |
| `crm_company_id` | ✅ | ID of the primary company. |
| `Stage_name` | Optional | Deal stage. |
| `Amount` | Optional | Deal size. |
| `Close_date` | Optional | Expected close date. |
| `Is_closed` | Optional | Indicates if the deal is closed. |
| `Is_won` | Optional | Indicates if the deal was won. |

When finished, click **Submit** to save your mappings.

---

## Recommended Company Properties
Administrators can create a few new fields in HubSpot to unlock BirdDog’s full value:

**BirdDog_Description**  
- *Field Type:* Single-line text  
- *Group:* Company Information  
- *Label:* BirdDog Description  
- *Purpose:* Summary of BirdDog’s key “Why Now” insights.

**BirdDog_Score**  
- *Field Type:* Number  
- *Purpose:* Stores BirdDog’s proprietary signal score (0–100).  
- *Note:* Even scores above 10 represent actionable signals.

**BirdDog_Link**  
- *Field Type:* URL  
- *Purpose:* Direct link to BirdDog’s full company report.

**BirdDog_Signals**  
- *Field Type:* Rich Text  
- *Purpose:* Lists recent BirdDog signals for each company.

---

## Data Sync & Request Limits
BirdDog performs a **daily sync** between **5:00 a.m. and 7:30 a.m. ET**, refreshing company and deal data using the HubSpot batch API.  

During the first week, expect slightly higher request volume as the sync calibrates.  
Additional push/pull events occur when users upload new companies or manually trigger updates.

BirdDog only **reads from mapped properties** and **writes to BirdDog-specific fields** that you explicitly create.

---

## User Mapping
BirdDog identifies users by email address.  
To associate BirdDog users with HubSpot users, provide a simple two-column CSV (email → HubSpot user ID).  

Send to: **hello@getbirddog.ai**


## Support
If you have any questions or need help configuring your integration:  
📧 **noah@getbirddog.ai**  
📞 **(231) 855-8001**  

BirdDog’s HubSpot integration ensures your CRM stays fully enriched, synced, and AI-ready — delivering actionable signal intelligence right where your reps work.
