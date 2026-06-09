# 🏦 AI-Powered Bank Fraud Detection System

An automated fraud detection workflow built using **n8n**, **Google Sheets**, **AI-based Fraud Scoring**, **Email Alerts**, and **Power BI Dashboarding** to identify suspicious banking transactions in real time.

## 📌 Project Overview

### Problem
Banks lose billions annually due to fraudulent transactions. Traditional manual reviews are slow, costly, and difficult to scale.

### Solution
This project automates fraud detection by:

- Monitoring transactions in real time
- Evaluating multiple fraud indicators
- Generating AI-based fraud scores
- Sending instant fraud alerts
- Updating approval statuses automatically
- Visualizing fraud trends through Power BI

### Impact

- ⚡ Faster fraud detection
- 💸 Reduced financial losses
- 📋 Improved compliance monitoring
- 📊 Real-time analytics and reporting
- 🔄 Scalable automation

---

# 🛠 Tech Stack

| Tool | Purpose |
|--------|----------|
| n8n | Workflow Automation |
| Google Sheets | Transaction Database |
| Gmail | Fraud Alert Notifications |
| Power BI | Dashboard & Analytics |
| JavaScript | Fraud Score Calculation |

---

# 📂 Transaction Database Structure

The system processes transaction records containing:

- Transaction ID
- Customer Name
- Account Number
- Transaction Date
- Amount
- Transaction Type
- Merchant Name
- Location
- Device ID
- IP Address
- Login Attempts
- Daily Transaction Count
- Average Transaction Amount
- Current Balance
- KYC Status
- GST Status
- Blacklisted Account Status

### Output Fields

- Fraud Score
- Risk Level
- Approval Status
- Fraud Reason
- Manager Approval
- Email Status
- Final Action

---

# 🚨 Fraud Detection Conditions

The workflow flags transactions based on:

| Condition | Action |
|------------|---------|
| Amount > ₹1,00,000 | High Risk |
| Login Attempts > 5 | Suspicious |
| Different Location/Country | Risk Alert |
| Blacklisted Account | Block |
| GST Missing | Compliance Flag |
| More than 10 Transactions/Day | Possible Fraud |
| Amount > 3× Customer Average | Abnormal Activity |
| KYC Pending | Hold |
| Multiple Devices in Short Time | Device Fraud |
| IP Address Mismatch | Security Alert |

---

# 🤖 Fraud Score Formula

```text
Fraud Score =
Amount Risk +
Login Risk +
Location Risk +
Device Risk +
KYC Risk
```

### Weight Distribution

| Risk Factor | Max Score |
|-------------|------------|
| Amount Risk | 40 |
| Login Risk | 20 |
| Location Risk | 15 |
| Device Risk | 15 |
| KYC Risk | 10 |

### Example

```text
Amount Risk = 40
Login Risk = 20
Device Risk = 15

Fraud Score = 75
Risk Level = HIGH
```

---

# 🔄 Workflow Architecture

```text
Webhook Trigger
       │
       ▼
Google Sheets Read
       │
       ▼
Fraud Detection Conditions
       │
       ▼
Fraud Score Calculation
       │
       ▼
Risk Classification
       │
       ▼
Google Sheets Update
       │
       ▼
Email Alert System
       │
       ▼
Manager Approval
       │
       ▼
Final Action
(Approve / Review / Block)
       │
       ▼
Power BI Dashboard
```

---

# 📧 Automated Fraud Alerts

The system automatically sends HTML email notifications when suspicious transactions are detected.

### Alert Information

- Customer Name
- Transaction ID
- Amount
- Risk Level
- Fraud Score
- Fraud Reason

### Recipients

- Compliance Team
- Branch Manager

---

# 🎯 Risk Classification

## 🟢 Low Risk (0–30)

- Transaction Approved
- Standard Logging
- No Alert Required

## 🟡 Medium Risk (31–60)

- Flag for Review
- OTP Verification
- Manager Notification

## 🔴 High Risk (61–100)

- Transaction Blocked
- Immediate Alert
- Manager Escalation
- Compliance Reporting

---

# 📊 Dashboard Metrics

Power BI provides real-time monitoring of:

- Daily Transactions
- Fraud Cases Detected
- Blocked Transactions
- Estimated Financial Loss Prevented
- Fraud by Transaction Type
- Risk Level Distribution

---

# 💼 Business Benefits

### ⚡ 99% Faster Detection
Fraud is detected within seconds instead of hours.

### 💸 Reduced Financial Loss
Automatic blocking minimizes fraudulent exposure.

### 📋 Regulatory Compliance
Supports KYC tracking, GST validation, and audit trails.

### 📊 Real-Time Insights
Live dashboards help management make data-driven decisions.

### 🔄 Scalability
Processes thousands of transactions simultaneously.

### 🛡 Enhanced Customer Trust
Proactive fraud prevention improves customer confidence.

---

# 🚀 Future Enhancements

- Machine Learning-based Fraud Prediction
- Real-Time API Integration with Core Banking Systems
- SMS & WhatsApp Fraud Alerts
- Customer Risk Profiling
- Behavioral Analytics
- Anomaly Detection Models

---

# 👨‍💻 Team

- Gopika Sharma
- Bhavesh Sahai
- Akshay Kumar
- Arshya Sharma
- Aditya Chaudhry

---

# 📜 License

This project is developed for academic and educational purposes as part of an MBA Finance automation and analytics project.

---

⭐ If you found this project useful, consider giving it a star on GitHub.
