# ☁️ Azure Security – Hands-On Practice & Projects

Microsoft Azure is widely used in government, healthcare, and enterprise environments. This guide will help you learn **Azure security fundamentals**, practice using a free Azure account, and build **portfolio-worthy projects**.

---

## 🛠️ Step-by-Step: Azure Security Lab Path

### 1. Create a Free Azure Account
- Sign up at [https://azure.microsoft.com/free](https://azure.microsoft.com/free)
- You'll get:
  - $200 credit (valid for 30 days)
  - Free tier access to core services for 12 months

---

### 2. Understand Core Security Services in Azure
Focus on:
- **Azure Active Directory (Azure AD)** – identity and access control
- **Virtual Networks (VNets)** – segment resources and control traffic
- **Network Security Groups (NSGs)** – firewall-like rules
- **Key Vault** – manage secrets and encryption keys
- **Microsoft Defender for Cloud** – security posture monitoring

---

### 3. Practice IAM (Identity & Access Management)
- Create multiple users and groups in Azure AD
- Assign built-in roles using **Role-Based Access Control (RBAC)**
- Create a **custom role** and assign it to a resource group

---

### 4. Enable Defender for Cloud
- Navigate to **Microsoft Defender for Cloud**
- Review:
  - **Secure Score**
  - **Recommendations** (e.g., exposed ports, outdated images)
  - **Regulatory compliance** standards

---

### 5. Configure Logging & Monitoring
- Enable diagnostics logging on:
  - Storage Accounts
  - Key Vault
  - Virtual Machines
- Connect logs to **Log Analytics Workspace**
- Try a basic Kusto Query:
  ```kusto
  SecurityEvent
  | where EventID == 4625
