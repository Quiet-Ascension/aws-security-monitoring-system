# 🔐 AWS Security Monitoring System

![AWS](https://img.shields.io/badge/AWS-Cloud-blue)
![Security](https://img.shields.io/badge/Domain-Security-red)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)

---

## 📌 Overview
This project demonstrates a **real-time security monitoring system** built on AWS.  
It detects sensitive activity (like accessing secrets) and instantly notifies users via email.

---

## 🚀 Architecture

User → Secrets Manager → CloudTrail → CloudWatch → SNS → Email Alert

---

## 🛠️ Tech Stack
- **AWS CloudTrail** – Tracks API activity  
- **AWS CloudWatch** – Logs, metrics & alarms  
- **AWS SNS** – Sends notifications  
- **AWS Secrets Manager** – Stores sensitive data  
- **IAM & S3** – Access control & log storage  

---

## ⚙️ Workflow

1. Store a secret in AWS Secrets Manager  
2. Access event is logged by CloudTrail  
3. Logs are pushed to CloudWatch  
4. Metric filter detects `GetSecretValue`  
5. Alarm triggers when threshold is exceeded  
6. SNS sends email alert  

---

## 📸 Screenshots

> Add screenshots here (from your PDF)

```
images/
├── secret-manager.png
├── cloudtrail.png
├── cloudwatch.png
├── sns.png
├── email.png
```

---

## ⚠️ Challenges & Fix

**Problem:** Alarm was not triggering  
**Cause:** Metric used *AVERAGE* instead of *SUM*  
**Fix:** Changed to SUM → system worked correctly  

---

## 🎯 Key Features
- Real-time monitoring of sensitive actions  
- Automated alerting system  
- Uses multiple AWS services together  
- Practical security use-case  

---

## 📄 Documentation
Detailed report available in:
`docs/aws-security-monitoring.pdf`

---

## 💡 Use Case
Detect unauthorized access to credentials, API keys, or secrets in cloud environments.

---

## 👨‍💻 Author
**Manav Shailesh**

---

⭐ If you like this project, consider starring the repo!
