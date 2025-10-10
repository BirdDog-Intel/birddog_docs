# Salesforce Integration

### Walkthrough Video
<div style="position: relative; padding-bottom: 56.25%; height: 0;">
  <iframe src="https://www.loom.com/embed/e4f63a1dc8a44d9bb2afb71c537eed37?sid=7b306293-b273-4e46-b301-c0540dca70b8"
          frameborder="0"
          webkitallowfullscreen
          mozallowfullscreen
          allowfullscreen
          style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;">
  </iframe>
</div>

---

### Overview
The **Salesforce integration** connects BirdDog directly with your CRM, keeping your accounts, opportunities, and BirdDog Signals automatically synced.  

With this integration, reps can see BirdDog’s enriched account data and scores inside Salesforce, while BirdDog continuously learns from your pipeline activity.

---

### Why It Matters
Integrating BirdDog with your CRM allows for two major benefits:

1. **Automatic syncing** of the accounts in your CRM with BirdDog’s scores and data.  
   This keeps BirdDog insights accessible in Salesforce without requiring manual uploads or spreadsheets.

2. **Smarter signals for every deal stage.**  
   BirdDog dynamically adjusts the information it provides based on deal stage — helping reps focus on what’s most relevant whether they’re qualifying or closing.

To achieve the first benefit, BirdDog needs access to **Accounts** in your CRM.  
To achieve the second, BirdDog also requires access to **Opportunities**.

---

### Setup (0:00 – 0:34)
1. Log into **BirdDog**.  
2. Navigate to **Settings → Integrations** in the lower-left corner.  
3. Scroll down to the **Integrations** module and select **Salesforce**.  
4. Choose your environment:  
   - **Default** for production.  
   - **Sandbox** for testing.  
5. Click **Submit** to start the connection.  

You’ll be redirected to Salesforce to log in with your **Integration User** credentials.

---

### Authentication & Integration Pattern
Most BirdDog clients follow this standard integration pattern:

- Create or use an **Integration User** with permission to **view and edit** required objects and fields.  
- The Integration User authenticates through BirdDog’s **OAuth flow** using BirdDog’s **Salesforce Connected App**.  
- After authentication, they map CRM fields to BirdDog fields inside the BirdDog Platform.

Once connected, BirdDog will:
- **Pull** accounts and opportunities from Salesforce.  
- **Push** enriched BirdDog data back to Salesforce fields.  
- Perform these operations automatically in **daily batches**.

When new accounts are uploaded or activated in BirdDog, the platform will immediately push updates to Salesforce.

---

### Connected App & OAuth Flow
BirdDog uses a **Salesforce Connected App** hosted within BirdDog’s org.  
When your first user connects, Salesforce automatically creates a **shadow copy** of that app in your own org (visible under Setup → App Manager).  

No package installation is required.

#### Scopes
- **Manage user data via APIs** (`api`)  
- **Perform requests at any time** (`refresh_token`, `offline_access`)  
- **Access unique user identifiers** (`openid`)  

#### Integration User Requirements
- API Access Enabled  
- Read/Write permissions on Accounts  
- *(Optional)* Read permissions on Opportunities  

#### Revoking Access
Your admins can revoke tokens anytime under:  
**Setup → Security → Connected Apps OAuth Usage**  
Alternatively, BirdDog can disconnect and delete all authentication data upon request.

---

### Rate Limits
BirdDog performs at least one **daily batch push and pull** operation.  
Occasional additional syncs occur when users upload new accounts or trigger manual refreshes.  

Typical clients find **~100 API calls per day** more than sufficient.  

During the **first week**, expect increased sync frequency while the integration calibrates with your CRM.

---

### Object & Field Mappings
BirdDog requires access to the **Account** object and optionally the **Opportunity** object to fully function.

#### Account Mapping
| Field | Required | Description |
|--------|-----------|-------------|
| `sf_id` | ✅ | Salesforce Account ID |
| `Account_Domain` | ✅ | Company website URL |
| `BirdDog_Description` | Optional | BirdDog “Why Now” summary |
| `BirdDog_Score` | Optional | BirdDog Account Score (0–100) |
| `BirdDog_Link` | Optional | Direct BirdDog Account Report URL |
| `BirdDog_User` | Optional | Links BirdDog Account to assigned user |
| `BirdDog_Signals` | Optional | Most recent BirdDog Signals for the account |

> BirdDog can only process accounts that have an associated **website domain**.

#### Recommended New Account Fields
To get full value from the integration, administrators can create a few BirdDog-specific fields:

**BirdDog_Description**  
- *Type:* Text Area (Long)  
- *Label:* BirdDog_Description  
- *Length:* 1,000 characters  
- *Help Text:* Summary of BirdDog Signals for the account.  

**BirdDog_Score**  
- *Type:* Number (0–100)  
- *Label:* BirdDog_Score  
- *Help Text:* Auto-populated BirdDog Signal Score.  

**BirdDog_Link**  
- *Type:* URL  
- *Label:* BirdDog_Link  
- *Help Text:* Link to the full BirdDog Account Report.  

**BirdDog_Signals**  
- *Type:* Rich Text  
- *Label:* BirdDog_Signals  
- *Help Text:* Latest BirdDog Signals for the account.  

Ensure all fields are visible to relevant users and accessible to **API-only integrations**.

You may optionally add a **BirdDog_User** field to link research directly to a user, though most clients map this to the existing Account Owner.

---

### Opportunity Mapping
Mapping opportunity fields allows BirdDog to tailor recommendations based on deal progress and success likelihood.

| Field | Required | Description |
|--------|-----------|-------------|
| `sf_id` | ✅ | Salesforce Opportunity ID |
| `sf_account_id` | ✅ | ID of the related account |
| `Name` | Optional | Opportunity name |
| `Descr` | Optional | Opportunity description |
| `Stage_name` | Optional | Stage of the opportunity |
| `Amount` | Optional | Value of the opportunity |
| `Close_date` | Optional | Expected close date |
| `Prob` | Optional | Probability percentage |
| `Next_step` | Optional | Next planned action |
| `Lead_source` | Optional | Opportunity lead source |
| `Is_closed` | Optional | Closed status |
| `Is_won` | Optional | Won status |
| `Created_date` | Optional | Creation timestamp |

---

### User Mapping
BirdDog identifies users via their **company email address**.  
To map BirdDog users to Salesforce users, send a simple two-column CSV (`email`, `Salesforce user ID`) to:  
📧 **hello@getbirddog.ai**

This allows BirdDog to correctly associate signals, accounts, and opportunities by rep.

---

### Testing & Sandbox Environments
BirdDog supports integration with **Salesforce sandbox environments** using the same connection portal as production.  
Simply select **Sandbox** during setup to connect your test environment.

---

### Support
For setup assistance or advanced configuration help:  
📧 **noah@getbirddog.ai**  
📞 **(231) 855-8001**

BirdDog’s Salesforce integration ensures your CRM is always enriched with real-time intelligence, allowing your team to focus on what matters most — building stronger, data-driven relationships.
