# 📋 GRC Analyst – Hands-On Skills & Projects

A **GRC (Governance, Risk, and Compliance) Analyst** ensures that an organization follows cybersecurity regulations, manages risk effectively, and builds secure policies.

This guide offers step-by-step practice instructions and portfolio-ready projects — all designed to build real experience even before you land the job.

---

## 🛠️ Hands-On Skills: Step-by-Step Instructions

### 🧾 Step 1: Write a Basic Security Policy
1. Choose a topic:
   - Acceptable Use
   - Password Policy
   - Remote Access Policy
2. Use [SANS Policy Templates](https://www.sans.org/information-security-policy/) as references
3. Draft your policy in Google Docs or Markdown
4. Include:
   - Policy Purpose
   - Scope
   - Policy Statements
   - Enforcement
   - Review Period

✅ Tip: Keep it short, clear, and actionable.

---

### 📊 Step 2: Build a Risk Register
1. Open Excel or Google Sheets
2. Create these columns:
   - Asset / System Name
   - Threat / Vulnerability
   - Impact (High/Med/Low)
   - Likelihood (High/Med/Low)
   - Risk Score (Impact × Likelihood)
   - Mitigation Plan
3. Populate at least 3 rows (examples: unpatched systems, misconfigured S3 bucket, shared passwords)
4. Use basic color coding for priority (e.g., red for high, green for low)

📁 Save as PDF or .xlsx for sharing

---

### 🔄 Step 3: Map Controls to a Framework
1. Choose a framework:
   - NIST 800-53 (free PDF)
   - CIS Controls v8
   - ISO/IEC 27001 (use summaries)
2. Pick a security domain (e.g., Access Control, Incident Response)
3. Choose 3–5 controls and write:
   - Control ID + Name
   - What it means
   - How an organization might meet it

✅ Example:
```
NIST AC-2: Account Management
- Organizations must manage user accounts throughout the lifecycle.
- Example: Use HR onboarding triggers to auto-provision/deprovision access.
```

---

### 📁 Step 4: Draft a Business Impact Analysis (Mini BIA)
1. Choose 2–3 fictional systems (e.g., Payroll App, CRM, Email)
2. Create a table with:
   - System Name
   - Confidentiality Impact
   - Integrity Impact
   - Availability Impact
   - Recovery Time Objective (RTO)
3. Assign each value as High, Medium, or Low

🎯 Goal: Show how risk affects business operations

---

### 📝 Step 5: Practice Audit Response
1. Write a mock response to a finding:
   > Finding: Multi-factor authentication (MFA) is not enabled on email accounts.
2. Draft a response format:
   - **Observation:** MFA not configured on all user accounts
   - **Risk:** Increased chance of account compromise via phishing
   - **Mitigation Plan:** Enroll all users in MFA within 30 days; monitor via dashboard
   - **Evidence to Provide:** Screenshot of policy + enforcement report

---

## 📁 GRC Portfolio Projects

### ✅ Project 1: Policy Pack
**Goal:** Write 2–3 security policies from scratch
- Format in PDF or Markdown
- Include table of contents + header
- Organize them in a GitHub repo or Notion doc

---

### ✅ Project 2: Sample Risk Register
**Goal:** Build and share a 5-row risk register with color-coded scores
- Export as PDF or share link to Google Sheet
- Bonus: Include a heatmap or chart if you're feeling extra ✨

---

### ✅ Project 3: Compliance Control Mapping
**Goal:** Map 3–5 controls from a framework to real-world implementation
- Use NIST, ISO, or CIS Controls
- Write in table format
- Bonus: Add screenshots or diagrams if you build anything

---

> "GRC isn’t about memorizing acronyms — it’s about helping people, processes, and systems stay aligned and secure. Show that you understand that, and you’re already ahead."
