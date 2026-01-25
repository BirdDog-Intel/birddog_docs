# Improving & Refining Signals

### Walkthrough Video
<div style="position: relative; padding-bottom: 56.25%; height: 0;">
  <iframe src="https://www.loom.com/embed/8c8219e753214142a95c5595938beb5b"
          frameborder="0"
          webkitallowfullscreen
          mozallowfullscreen
          allowfullscreen
          style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;">
  </iframe>
</div>

---

### Overview
If your signals are returning results that feel too broad or irrelevant, you can refine them using **Signal Improvement**. By adding specific qualifications and context, you teach the BirdDog engine exactly what "good" looks like for your ICP.

---

### How to Refine Your Signals (0:21 – 1:30)

There are two primary ways to make your signals more accurate:

#### 1. Editing the Core Question
Be as specific as possible in the primary signal question. 
* **Generic:** `Does {account} have an Enterprise Sales Team?`
* **Refined:** `Does {account} have an Enterprise Sales Team based in the U.S.?`
* **Why it works:** Adding a geographic or functional constraint directly into the question forces the AI to filter out global or irrelevant hits immediately.

#### 2. Adding Additional Context
Use the **Additional Context** field to provide nuanced definitions that aren't captured in a simple question.
* **Define Terms:** Tell the system how you define a specific role (e.g., "Enterprise Sales should include Strategic Accounts or Global Account Managers").
* **Set Qualifications:** List specific requirements that must be met for the signal to be considered "Found."

---

### Common Use Cases for Improvement (1:31 – 2:00)

Detailed prompts lead to higher-quality signals. Here are two examples of how to tighten your criteria:

| Topic | Vague Signal | Refined Signal + Context |
| :--- | :--- | :--- |
| **Funding** | `Did {account} get funding?` | **Question:** `Did {account} receive VC funding?` <br> **Context:** `Only include Seed or Series A rounds. Exclude debt financing or grants.` |
| **Hiring** | `Is {account} hiring for sales?` | **Question:** `Is {account} hiring Enterprise AEs?` <br> **Context:** `Only include full-cycle roles targeting the Fortune 500.` |

---

### How to Apply Updates (2:01 – 2:15)
1.  Navigate to your **Signals** configuration page.
2.  Click **Edit** on the signal you wish to improve.
3.  Update the **Question** or add details to the **Additional Context** box.
4.  Click **Update**.
5.  **The Result:** BirdDog will adjust how it evaluates all *new* incoming signals based on these updated rules.

---

### Pro-Tip: The "Negative Constraint"
One of the fastest ways to improve a signal is to tell the system what you **don't** want. If you are looking for "Sales Leaders" but keep getting "Retail Store Managers," add context that says: *"Exclude retail, hospitality, or branch-level management roles; focus only on B2B corporate sales leadership."*

---

### Support
Need help writing the perfect prompt for a complex signal?  
📧 **hello@getbirddog.ai**

Would you like me to suggest some **Additional Context** for your three most frequent signals to help narrow down your results?
