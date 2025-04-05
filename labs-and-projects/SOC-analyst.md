# 🧪 SOC Analyst – Hands-On Skills & Projects

SOC (Security Operations Center) Analysts are the front line of cyber defense. This role focuses on monitoring, triaging, and responding to alerts using a variety of tools and log sources.

This guide includes **detailed hands-on steps** and **real-world project instructions** to help you build confidence, skills, and a strong portfolio.

---

## 🛠️ Hands-On Skills: Step-by-Step Instructions

### 🔧 Step 1: Set Up Your Environment
1. Download and install **[VirtualBox](https://www.virtualbox.org/)** or **VMware Workstation Player** (free).
2. Download a **Windows 10 Evaluation ISO** from Microsoft or use **FLARE VM** (a forensic-ready Windows image).
3. Download **Ubuntu** or **Kali Linux** ISO.
4. Create two VMs:
   - One Windows VM
   - One Kali or Ubuntu VM
5. (Optional) Install a SIEM tool like [HELK](https://github.com/Cyb3rWard0g/HELK) or [Wazuh](https://wazuh.com/) on the Linux VM to simulate a SOC environment.

---

### 📝 Step 2: Analyze Windows Logs
1. On your **Windows VM**, open **Event Viewer** → Expand **Windows Logs** → Click **Security**.
2. Use the **Filter Current Log** option to view:
   - **Event ID 4624** (Logon success)
   - **Event ID 4625** (Failed logon)
   - **Event ID 4672** (Privilege use)
   - **Event ID 4720** (User account creation)
3. Take screenshots of logs and document:
   - What happened
   - When
   - Which user/account was involved

💡 Bonus: Install [Sysmon](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon) and use [SwiftOnSecurity’s config](https://github.com/SwiftOnSecurity/sysmon-config) to enrich log data.

---

### 🌐 Step 3: Use Threat Intelligence Tools
Use these to look up IPs, file hashes, and domains:
- [VirusTotal](https://www.virustotal.com/) – Upload or search suspicious files or URLs
- [Hybrid Analysis](https://www.hybrid-analysis.com/) – Check executable behavior
- [AbuseIPDB](https://www.abuseipdb.com/) – Report and investigate malicious IPs

✅ Task:
- Find a sample malware hash (from TryHackMe or open malware databases)
- Submit it to VirusTotal and Hybrid Analysis
- Document what you find: detection ratio, behavior, and any flagged activity

---

### 📊 Step 4: Practice SIEM Triage with Splunk or Wazuh
1. Download and install [Splunk Free](https://www.splunk.com/en_us/download/splunk-enterprise.html) or Wazuh
2. Forward logs from your Windows VM using Winlogbeat or Wazuh Agent
3. Use this search to find failed logins in Splunk:
   ```
   index=main sourcetype=WinEventLog:Security EventCode=4625
   ```
4. Create a simple **alert rule** for multiple failed logins from the same host
5. Build a basic dashboard to visualize:
   - Login failures over time
   - Top source IPs
   - Most frequent users triggering alerts

📸 Screenshot your setup, query, and results for your portfolio

---

### 🧾 Step 5: Write an Incident Report
Simulate a brute-force login scenario and write a report including:
- What triggered the alert
- Time and date
- Impacted system or user
- Any known tactics (e.g., MITRE ATT&CK T1110 – Brute Force)
- Next steps (e.g., block IP, reset password, notify user)

📄 Use your own format or adapt this layout:
```markdown
## Summary
Detected repeated login failures from a foreign IP. Potential brute-force attempt.

## Timeline
03/14/2025 - 10:14 PM – First failed login
03/14/2025 - 10:19 PM – 30+ failed attempts

## Affected Host
DESKTOP-7L9K1K2 (192.168.1.12)

## ATT&CK Technique
T1110 – Brute Force

## Recommendation
Disable the affected account temporarily and investigate source IP for blocklisting.
```

---

## 📁 Portfolio Projects with Instructions

### 📊 Project 1: SIEM Triage Demo
**Goal:** Show how you triage a real alert and analyze logs

**Steps:**
1. Trigger Event ID 4625 (failed login) on your Windows VM
2. Forward logs to Splunk or Wazuh
3. Search, filter, and screenshot the alert
4. Submit the source IP to VirusTotal
5. Create a 1-page PDF report (or blog post) summarizing your steps and results

---

### 📑 Project 2: Log Triage Playbook
**Goal:** Create a reusable playbook for analyzing common events

**Steps:**
1. Create a table or Markdown document listing:
   - Event ID
   - Description
   - MITRE mapping (if known)
   - Questions to ask
   - Response steps

Example:
| Event ID | Description         | MITRE     | Questions                     | Action            |
|----------|---------------------|-----------|-------------------------------|-------------------|
| 4625     | Failed Login        | T1110     | Source IP? Username? Count?  | Alert + block IP  |
| 4720     | New User Created    | T1136     | Who created it? From where?  | Investigate creds |

2. Format it in Markdown, Google Sheets, or PDF
3. Upload to GitHub or include in your resume portfolio

---

### 📄 Project 3: Incident Report Template
**Goal:** Build a polished template to use in interviews or job tasks

**Steps:**
1. Use a Markdown editor or Google Docs to draft a blank IR template
2. Include sections:
   - Summary
   - Timeline
   - Affected Systems
   - Indicators of Compromise (IOCs)
   - ATT&CK Mapping
   - Recommendations
3. Use one of your earlier labs to fill it in as a sample
4. Save as PDF or publish to GitHub

---

> "You don't need a job to act like a SOC analyst. Build your lab, log your journey, and treat your practice like real work."
