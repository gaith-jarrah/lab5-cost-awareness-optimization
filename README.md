# 💰 AWS Cost Awareness & Optimization (Lab 5)

## 📌 Project Overview

This lab demonstrates how to implement proactive cost monitoring and financial governance inside AWS using native Billing and Cost Management tools.

The objective was to simulate a real-world FinOps scenario where unexpected cloud spending must be detected early and controlled automatically.

---

## 🎯 Lab Objectives

- Create and configure AWS Budgets
- Enable Zero-Spend early warning detection
- Implement AWS Cost Anomaly Detection
- Configure automated notifications using Amazon SNS
- Apply and activate Cost Allocation Tags
- Track S3 resource cost by environment

---

## 🏗️ Services Used

- AWS Budgets  
- AWS Cost Anomaly Detection  
- Amazon SNS  
- Amazon S3  
- Cost Allocation Tags  

---

## 🧪 Implementation Steps

### 1️⃣ Monthly Budget Configuration

- Budget Type: Monthly Cost Budget  
- Budget Limit: **$10**
- Alert threshold configured

---

### 2️⃣ Zero Spend Budget

- Threshold: **$0.01**
- Purpose: Immediate detection of unexpected charges

---

### 3️⃣ Cost Anomaly Detection Monitor

- Monitor Name: `cost-anomaly-detection-lab5`
- Monitor Type: Managed by AWS
- Monitor Dimension: Linked Account

This enables automatic detection of abnormal spending patterns based on historical usage.

---

### 4️⃣ Amazon SNS Topic

Created SNS Topic:

```
lab5-cost-alert-topic
```

Used for sending anomaly detection alerts.

---

### 5️⃣ Alert Subscription Configuration

- Subscription Name: `lab5-cost-alert`
- Alerting Frequency: Individual Alerts
- Threshold: **$0.50 above expected spend**
- Connected to SNS Topic ARN

This ensures real-time cost anomaly notifications.

---

### 6️⃣ S3 Bucket Creation

Bucket Name:

```
lab5-cost-tag-test
```

---

### 7️⃣ Cost Allocation Tagging

Applied user-defined tag:

| Key         | Value |
|------------|--------|
| Environment | Lab5 |

Activated the tag under:

Billing → Cost Allocation Tags

This enables cost tracking inside:
- AWS Cost Explorer
- Billing Reports

---

## 📊 What This Lab Demonstrates

✔ Proactive cost monitoring  
✔ Automated anomaly detection  
✔ Budget enforcement strategy  
✔ SNS-based financial alerting  
✔ Proper tagging strategy for cost visibility  
✔ FinOps mindset implementation  

---

## 🧹 Cleanup (Important)

To avoid unnecessary charges:

- Delete Cost Anomaly Monitor
- Delete SNS Topic
- Delete Budgets
- Delete S3 Bucket (if not needed)

---

## 🚀 Final Outcome

A fully configured AWS cost monitoring and alerting framework that improves visibility, prevents unexpected bills, and aligns cloud usage with financial governance best practices.

---

**Author:**  
Gaith Jarrah  
AWS Solutions Architect Associate (SAA-C03)
