# Slack Integration & Notifications

### Walkthrough Video
<div style="position: relative; padding-bottom: 56.25%; height: 0;">
  <iframe src="https://www.loom.com/embed/31bcf97109274e3faeebf6b27073d824"
          frameborder="0"
          webkitallowfullscreen
          mozallowfullscreen
          allowfullscreen
          style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;">
  </iframe>
</div>

---

### Overview
The **Slack integration** ensures that you never miss a high-intent signal. Instead of manually checking the dashboard, BirdDog pushes real-time alerts for new signals, account assignments, and recommendations directly into your Slack workflow.

---

### Setting Up Personalized Tags (0:10 – 1:01)
To ensure BirdDog mentions you specifically when one of your accounts hits a signal, you need to sync your **Slack Member ID** with the BirdDog platform.

1.  **Find your Member ID:**
    * Open Slack and click on your **Profile Picture** in the sidebar or a message.
    * Click the **three dots (More)** on your profile card.
    * Select **Copy Member ID** (This is a unique alphanumeric code).
2.  **Sync with BirdDog:**
    * Navigate to **Settings → Integrations** in BirdDog.
    * Locate the Slack section and paste your ID into the **Member ID** field.
3.  **Result:** You will now be automatically tagged (@user) in the shared Slack channel whenever there is an update relevant to your book of business.

---

### Private Notifications: Reducing "Channel Noise" (1:02 – 1:24)
If your team's shared Slack channel is high-volume, you can enable **Private Access** to receive a curated feed of alerts.

* **How it works:** Flick the **Allow Private Access** toggle to "On" in your BirdDog settings.
* **The Result:** The BirdDog Bot will send you **Direct Messages (DMs)** containing only the signals and recommendations for accounts assigned to *you*. This keeps your notifications clean and focused exclusively on your targets.

---

### Troubleshooting & Access (1:25 – 1:41)
* **Missing Channel:** Every BirdDog organization should have a dedicated Slack channel (e.g., `#birddog-signals`). If you have not been invited to yours, please contact the team.
* **Bot Permissions:** Ensure the BirdDog Bot has been added to your specific channel to allow it to post updates.

---

### Summary of Notification Types
| Notification | Content |
| :--- | :--- |
| **New Signal Found** | Instant alert when an account hits a "High" importance trigger. |
| **Account Recommendation** | Alert from the Assignment Desk when Farsight finds a new prospect. |
| **Account Assignment** | Notification when a manager assigns a new account to your profile. |

---

### Support
Need help finding your Member ID or want to create a new dedicated signals channel?  
📧 **hello@getbirddog.ai**

Would you like me to help you configure which **Signal Categories** trigger a Slack alert so you only get notified for the most critical updates?
