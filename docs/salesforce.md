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
The **Salesforce integration** connects **BirdDog** directly to your CRM, allowing your account, opportunity, and intelligence data to stay perfectly in sync.

By integrating with Salesforce, BirdDog automatically enriches your CRM records with insights, scores, and account intelligence — giving reps a clear view of which accounts are most like those they’ve already closed.

---

### Why It Matters
- Syncs BirdDog intelligence directly into Salesforce records.  
- Ensures your CRM reflects the most accurate, enriched account data.  
- Lets your team prioritize accounts similar to your best customers.  
- Supports both account and opportunity-level mapping.  

---

### Setup (0:00 – 0:22)
1. Log into **BirdDog**.  
2. Navigate to **Settings → Integrations** in the bottom-left corner.  
3. Click **Salesforce** from the list of available integrations.  
4. In the dropdown menu, choose your connection environment:  
   - **Default:** for your production Salesforce environment.  
   - **Sandbox:** for testing or staging environments.  
5. Click **Submit** to start the authorization process.  

---

### Connecting to Salesforce (0:22 – 0:55)
1. You’ll be redirected to the Salesforce login screen.  
2. Log in using your **Salesforce integration user** credentials.  

**Recommendation:**  
Use an **integration user** that has permissions for the specific **accounts** and **opportunities** you want synced between Salesforce and BirdDog.  
This ensures all relevant data can flow bi-directionally and consistently.

---

### Field Mapping (0:55 – 1:49)
Once connected, you’ll land on the **Field Mapping** page.

Here you can define how BirdDog’s fields correspond to your Salesforce fields.

**Required Mapping:**
- **Account ID / Domain** → required to match Salesforce accounts with BirdDog accounts.  

**Optional Mapping:**
- **Opportunity fields** → connect BirdDog’s opportunity data to your CRM.  
- **Custom fields** → map any additional data you’d like BirdDog to enrich.  

After mapping, click **Submit** to save your configuration.

---

### Recommended Configuration
- Always ensure your **Account ID** and **Domain** fields are mapped correctly — this is required for syncing.  
- Map **Opportunity fields** if you want BirdDog to help identify accounts that resemble your **closed-won** deals.  
- Use **Sandbox** for safe testing before pushing changes to your production environment.  

---

### Support
If you need help connecting Salesforce or setting up mappings:  
- Review the **BirdDog Salesforce documentation** for detailed setup guidance.  
- Or contact the **BirdDog support team** for assistance with permissions or field configurations.  

---

### Summary
The **Salesforce Integration** keeps BirdDog and your CRM in perfect sync, ensuring your sales team always works from clean, enriched, and prioritized data.  

- Connect Salesforce using default or sandbox mode.  
- Map account and opportunity fields for accurate syncing.  
- Use an integration user with the right access permissions.  
- Automatically enrich your CRM with BirdDog intelligence.  

The result: **smarter account prioritization, seamless syncing, and better data-driven selling** — all inside Salesforce.
