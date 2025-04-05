# 🧪 SOC Analyst – Hands-On Skills & Projects

SOC (Security Operations Center) Analysts are the front line of cyber defense. This role focuses on monitoring, triaging, and responding to alerts using a variety of tools and log sources.

This guide gives you **step-by-step hands-on skills to practice**, followed by **realistic project ideas** you can use to build your portfolio.

---

## 🛠️ Hands-On Skills Checklist

### 1. **Set Up Your Environment**
- Install VirtualBox or VMware
- Spin up a Windows VM (try Eval ISO or FireEye FLARE VM)
- Add a Linux VM (Ubuntu or Kali)
- Optional: Install HELK or Wazuh as a local SIEM

### 2. **Basic Log Analysis**
- Open Windows Event Viewer → Filter by Security Logs
- Practice reading:
  - Logon/logoff events
  - Privilege use
  - Account lockouts
- Use [SwiftOnSecurity Sysmon config](https://github.com/SwiftOnSecurity/sysmon-config) for better logs

### 3. **Use Online Threat Intel Tools**
- [VirusTotal](https://www.virustotal.com/)
- [Hybrid Analysis](https://www.hybrid-analysis.com/)
- [AbuseIPDB](https://www.abuseipdb.com/)
- Practice submitting hashes, IPs, and URLs

### 4. **SIEM Basics (Splunk or Wazuh)**
- Set up [Splunk Free](https://www.splunk.com/en_us/download/splunk-enterprise.html) or [Wazuh](https://wazuh.com/)
- Load dummy logs or logs from your VM
- Create simple dashboards and alerts
- Practice writing queries:
  ```
  index=main sourcetype=WinEventLog:Security EventCode=4625
  ```

### 5. **Write Your First Incident Report**
- Simulate a failed login brute-force alert
- Write a report that includes:
  - Summary
  - Timestamps
  - Host/IP affected
  - MITRE ATT&CK technique (if known)
  - Recommendation

---

## 📁 Realistic Project Ideas

### 📊 Project 1: SIEM Triage Demo
Set up a SIEM, collect logs from a Windows VM, and demonstrate how to:
- Triage an alert (failed logins or PowerShell execution)
- Use VirusTotal to confirm threat
- Write a summary of findings

### 📑 Project 2: Log Playbook
Build a mini “triage guide” for:
- Failed logins (4625)
- New user creation
- Disabled antivirus

Organize it in Markdown or Google Docs as a shareable resource.

### 📄 Project 3: Incident Report Template
Create your own professional IR template and fill it in with simulated data. Share as a PDF or public GitHub repo.

---

> "SOC analysts don’t need to be perfect — they just need to be consistent, curious, and calm under pressure. Start small and build confidence from there."
