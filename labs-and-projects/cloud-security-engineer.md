# ☁️ Cloud Security Engineer – Hands-On Skills & Projects

Cloud Security Engineers protect data, applications, and infrastructure hosted on platforms like AWS, Azure, and Google Cloud. Their job is to design, build, and monitor secure cloud environments.

This guide includes step-by-step labs, real-world security practices, and project ideas you can run in your AWS Free Tier or sandboxed cloud accounts.

---

## 🛠️ Hands-On Skills: Step-by-Step Instructions

### 🔐 Step 1: IAM Policy Basics (AWS)
1. Set up your **AWS Free Tier account**
2. Go to **IAM → Policies → Create policy**
3. Write a JSON policy that:
   - Allows `s3:GetObject` for a specific bucket
   - Denies `s3:DeleteObject`
4. Attach the policy to a test IAM user
5. Test access using the AWS CLI or console

✅ Goal: Understand least privilege and test what a user can/can’t do

---

### 📁 Step 2: Secure an S3 Bucket
1. Create a new S3 bucket
2. Upload a sample file
3. Enable bucket versioning
4. Set a bucket policy to make the contents **private only**
5. Enable **server-side encryption (SSE-S3)**
6. Use the **Permissions** tab to block public access

📸 Take before/after screenshots of permissions and policy

---

### 🧠 Step 3: Enable Logging & Monitoring
1. Go to **CloudTrail** and ensure it's logging to a secure bucket
2. Enable **GuardDuty** (free trial for 30 days)
3. Simulate activity:
   - Use IAM users to log in from different regions (or simulate anomalies)
   - Watch for GuardDuty alerts
4. Document findings and observations

✅ Bonus: Write an alert response summary like you would in a SOC

---

### 📶 Step 4: Build a Secure VPC
1. Create a **custom VPC** with:
   - Public and private subnets
   - Internet Gateway
   - NAT Gateway (if needed)
2. Launch EC2 instances:
   - One in public subnet (bastion)
   - One in private subnet (web/app)
3. Configure **Security Groups**:
   - Public: SSH only from your IP
   - Private: Allow traffic from bastion host only

💡 Document your architecture using a diagram (use Lucidchart, Excalidraw, or draw.io)

---

### 🔄 Step 5: Respond to a Misconfiguration
1. Publicly expose an S3 bucket (simulate!)
2. Detect the exposure using **Trusted Advisor**, **CloudTrail**, or manually
3. Remediate by:
   - Reversing the policy
   - Enabling block public access
   - Rotating IAM keys if needed
4. Write a post-incident summary

---

## 📁 Cloud Security Portfolio Projects

### ☁️ Project 1: Secure AWS Architecture
**Goal:** Build and diagram a secure cloud deployment
- VPC with subnets, EC2, RDS, IAM, and S3
- Document security group rules and IAM policies
- Diagram your setup with annotations

---

### 🔒 Project 2: IAM Policy Pack
**Goal:** Create and test 2–3 IAM policies
- One user with read-only S3 access
- One user denied from deleting EC2 instances
- Document results with screenshots and policy JSON

---

### 📊 Project 3: Cloud Security Audit Report
**Goal:** Simulate an audit of your AWS setup
- Review IAM users/roles, S3 buckets, CloudTrail, and GuardDuty
- List findings (e.g., no MFA, over-privileged role, public bucket)
- Write a 1-page audit summary with “risk” and “recommendations” sections

---

> "Cloud security isn’t about locking everything down — it’s about enabling secure innovation at scale."
