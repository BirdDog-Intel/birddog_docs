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
Integrating BirdDog with your CRM allows for two major benefits:

1. **Automatic syncing of the companies in your CRM with BirdDog's score & data.**  
   This way, BirdDog data is easily accessible to your reps as they go about normal business. This is in contrast to manually uploading companies from your CRM to BirdDog & then bringing the data back to your CRM with via a spreadsheet.

2. **Improve the information BirdDog provides to your reps based on the status of their deal with a given company.**  
   Your reps care about different signals when the prospect isn't even qualified yet vs when they are 6 months into the deal cycle. This helps them focus on the data that will move the needle at any given time.

To achieve the first benefit, BirdDog needs to view the companies in your CRM. To achieve the second benefit, BirdDog needs to be able to see the deals in your CRM.

---

### App & Installation Guide
BirdDog connects to your HubSpot instance via a verified Public App, BirdDogScout, App Id 16144816. The best way to install the app is directly through the BirdDog platform.

1. Login  
2. Click User Settings in the bottom left corner of the nav bar  
3. Scroll down to the integrations section and find "Setup HubSpot"  
4. Click "Connect HubSpot"  
5. Complete the authentication steps in the HubSpot portal  
6. Back in BirdDog, either allow the system to automatically map the custom fields or manually do it yourself*  

*Prior to mapping the fields, you will want to create the custom fields as outlined below in the documentation under the Company Mapping section.

---

### Authentication
The App follows the principle of least privilege, and resultantly has the following scopes:

#### Required Scopes
- **Crm.objects.companies.read**  
- **Crm.objects.companies.write**  
- **Crm.schemas.companies.read**  
- **Oauth**  

#### Optional Scopes
- **Crm.schemas.deals.read**  
- **Crm.objects.owners.read**  
- **Crm.objects.deals.read**  
- **Sales-email-read**  
- **Crm.schemas.companies.write**  

The Oauth & Company scopes are required for the integration to have meaningful functionality. Optionally, the Deal scopes can further enrich alerts with context about a seller's deals. Sales-email-read enables BirdDog to track activities on accounts.

One user will authenticate your organization via an OAuth Flow through our App, which can be accessed on the BirdDog Platform. After authentication, the User will map their desired CRM fields to the BirdDog fields.

BirdDog will pull in the desired companies & deals objects, and send back the enriched company data.

Then, each day, BirdDog will:

- **Refresh** your company list & current deals via a pull  
- **Update** the BirdDog fields for tracked companies in your CRM via a push  

Additionally, when new companies are uploaded or activated in the BirdDog Platform via a user, BirdDog will send an update of the data associated with that account to your CRM.

BirdDog will only read from the mapped properties, and will only write to the properties you specifically create below for BirdDog's use.

---

### Request Patterns
Generally, to limit the amount of requests made to your CRM throughout the day, a full daily sync between BirdDog and your HubSpot will occur between 5 am and 9 am et, where BirdDog pulls the designated accounts and writes updates to their designated BirdDog fields.

From time to time, there will be additional push and pulls, such as when users upload new companies or request an immediate refresh on certain data.

Additionally, during the first week of the integration, expect a higher number of requests as the system calibrates its sync with your crm.

---

### Object & Property Mappings
Below is an overview of field mappings for both Company & Deal objects in your CRM. The mapping can be completed & updated at any time via the BirdDog Platform, after integration is complete.

While it is necessary to give BirdDog access to your Company object to make the integration work, the Deal object is optional but unlocks significant value for your sales team.

#### Company Mapping
Below are the required and optional company fields that you can map to BirdDog using fields in your CRM instance.

| Field | Required | Description |
|--------|-----------|-------------|
| `crm_id` | ✅ | Object id of the company, typically hs_object_id |
| `Company_Domain`* | ✅ | The url of the main webpage for the company; typically domain or website |
| `BirdDog_Description`** | Optional | Houses BirdDog's Why Now description |
| `BirdDog_Score`** | Optional | Houses the BirdDog company score |
| `BirdDog_Link`** | Optional | Directly links to the company report in the BirdDog platform |
| `BirdDog_User`** | Optional | Enabling this field will allow BirdDog to automatically link the company research of a newly tagged company in your HubSpot to the appropriate user |
| `BirdDog_Originated`** | Optional | Records if BirdDog originated the account for manual attribution; note, BirdDog automatically has some attribution reporting even without this field |
| `BirdDog_Add_Date`** | Optional | Records the date the account was originally added to BirdDog |
| `BirdDog_Signal_List`** | Optional | A list of all of the signals that apply to each account. You do not need to manually add in the options |
| `BirdDog_Message`** | Optional | Drafts of messages to send to prospects. Contact your BirdDog point of contact to enable this feature |

> *BirdDog can only process companies that have an associated company website recorded in your HubSpot Instance.

> **See the below section for a description of recommended custom fields to use for each of these mappings.

---

### Recommended New Company Properties
To maximize the value of their BirdDog integration, administrators typically create a handful of new fields for company objects. Recommended configurations for each field are included below.

**BirdDog_Description**  
- *Field Type:* Single-line text  
- *Group:* Company Information  
- *Property Label:* BirdDog Description  
- *Description:* A summary of the most recent BirdDog Signals for the company.  
- *Default Value:* Blank  

**BirdDog_Score**  
- *Field Type:* Number  
- *Group:* Company Information  
- *Property Label:* BirdDog Score  
- *Description:* A score from 0-100 showing the strength of BirdDog Signals for this company. While scores above 80 are incredibly strong, they are rare–even a score above a 10 likely has valuable information to use.  
- *Default Value:* Blank  

**BirdDog_Link**  
- *Field Type:* URL  
- *Group:* Company Information  
- *Property Label:* BirdDog Link  
- *Description:* A link to the full report on the company in the BirdDog platform.  
- *Default Value:* Blank  

**BirdDog_Signals**  
- *Field Type:* Rich Text  
- *Group:* Company Information  
- *Property Label:* BirdDog Signals  
- *Description:* Some of the most recent signals BirdDog found on the company.  
- *Default Value:* Blank  

**BirdDog_Originated**  
- *Field Type:* Single Checkbox  
- *Group:* Company Information  
- *Property Label:* BirdDog Originated  
- *Description:* Records if BirdDog originated the account.  
- *Default Value:* Blank  

**BirdDog_Add_Date**  
- *Field Type:* Date and time picker  
- *Group:* Company Information  
- *Property Label:* BirdDog Add Date  
- *Description:* Records the date the account was originally added to BirdDog  
- *Default Value:* Blank  

**BirdDog_Signal_List**  
- *Field Type:* Multiple Checkboxes  
- *Group:* Company Information  
- *Property Label:* BirdDog Signal List  
- *Description:* List of all of the BirdDog Signals that apply to account  
- *Option Style:* Tag recommended  
- *Options:* Enter one option with whatever string you would like. The system will override accordingly  

**BirdDog_Message**  
- *Field Type:* Rich Text  
- *Group:* Company Information  
- *Property Label:* BirdDog Messages  
- *Description:* List of all of the BirdDog message draft to account  
- *Default Value:* Blank  

Additionally, you may add another field called BirdDog user that links the company to a specific user for BirdDog's reference. However, when it comes time to map your fields to the BirdDog fields, most clients simply use an existing owner field for this mapping.

---

### Deal Mapping
Mapping the below fields into BirdDog will help the system provide better signal data & recommendations based on the status of each company in HubSpot. Additionally, BirdDog will be able to leverage these fields to backtest signals to see which ones are most strongly correlated with closed won deals.

| Field | Required | Description |
|--------|-----------|-------------|
| `crm_id` | ✅ | The HubSpot id of the deal, usually hs_object_id |
| `crm_company_id` | ✅ | The id of the primary company attached to the deal, usually hs_primary_associated_company |
| `Name` | Optional | Name of the deal |
| `Descr` | Optional | Description of the deal |
| `Stage_name` | Optional | Stage name of the deal |
| `Amount` | Optional | Size of the deal |
| `Close_date` | Optional | Close date of the deal |
| `Prob` | Optional | Probability of the deal |
| `Next_step` | Optional | Next step of the deal |
| `Lead_source` | Optional | Lead source of the deal |
| `Is_closed` | Optional | Is the deal closed? |
| `Is_won` | Optional | Is the deal won? |
| `Created_date` | Optional | Creation date of the deal |

---

### Support
For setup assistance or advanced configuration help:  
📧 **noah@getbirddog.ai**  
📞 **(231) 855-8001**
