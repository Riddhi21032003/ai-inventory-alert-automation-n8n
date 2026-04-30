# 📦 AI Inventory Alert Automation (n8n)

🚀 A production-ready AI-powered inventory monitoring system built using **n8n**, **Groq LLM**, **Google Sheets**, and **Gmail**.

This project automates inventory tracking by detecting low-stock items, generating intelligent alerts using AI, and sending notifications via email—without writing backend code.

---

## 🎯 Project Highlights

* ⏰ Automated **weekly inventory monitoring**
* 📊 Reads real-time data from **Google Sheets**
* ⚠️ Detects items where **Stock < Threshold**
* 🤖 Uses AI to generate structured alert messages
* 📧 Sends alerts automatically via Gmail
* 🧠 Demonstrates **AI agent + workflow automation**

---

## 🧠 How It Works

1. Schedule trigger runs weekly
2. Inventory data is fetched from Google Sheets
3. Items are filtered where:

   * Stock is less than threshold
4. All low-stock items are aggregated
5. AI Agent formats a professional alert message
6. Gmail sends the alert automatically

---

## 🏗️ Architecture Diagram

```
Schedule Trigger
      ↓
Google Sheets (Inventory Data)
      ↓
Filter (Stock < Threshold)
      ↓
Aggregate (Low Stock Items)
      ↓
AI Agent + Groq LLM
      ↓
Gmail (Send Alert Email)
```

---

## 📸 Screenshots

### 🔹 Workflow Overview

<img width="2048" height="1062" alt="workflow_inventory_check" src="https://github.com/user-attachments/assets/75b1ae38-b258-40eb-b6b5-fa87929a4e10" />

### 🔹 Sample Data

<img width="2048" height="1183" alt="email_alert_inventory_data" src="https://github.com/user-attachments/assets/a45f9df6-d401-4e56-ba39-4e8131696496" />

### 🔹 Email Alert Output

<img width="2048" height="450" alt="email_alert_output" src="https://github.com/user-attachments/assets/1a8efa63-8efe-492c-bd1f-4e977238c6dc" />

---

## 🧩 Workflow Components

| Component        | Purpose                      |
| ---------------- | ---------------------------- |
| Schedule Trigger | Runs workflow weekly         |
| Google Sheets    | Stores inventory data        |
| Filter           | Finds low-stock items        |
| Aggregate        | Combines items into one list |
| AI Agent         | Generates alert message      |
| Groq Model       | AI reasoning                 |
| Gmail Tool       | Sends email notification     |

---

## 🛠️ Tech Stack

* **Automation:** n8n
* **AI Model:** Groq LLM
* **Database:** Google Sheets
* **Notifications:** Gmail

---

## 📊 Google Sheets Setup

Create a sheet with these columns:

```
Item Name | Stock | Threshold | Supplier
```

### Example:

|       Item Name       | Stock | Threshold |      Supplier     |
| --------------------- | ----- | --------- | ----------------- |
| Coffee Beans          | 5     | 5         | Arabica Roasters  |
| Espresso Pods Pack    | 2     | 6         | Urban Coffee      |
| Milk                  | 8     | 10        | Local Dairy Farm  |

---

## ⚙️ Setup Guide

### 1. Import Workflow

* Open n8n
* Go to **Workflows → Import from File**
* Upload `ai-inventory-check-automation.json`

### 2. Connect Credentials

* Google Sheets OAuth
* Gmail OAuth
* Groq API key

### 3. Configure Nodes

* Select your Google Sheet
* Map columns correctly
* Update Gmail recipient

### 4. Activate Workflow

* Enable workflow
* It will run automatically every week

---

## 💬 Example Output

```
⚠️ Low Stock Alert:

- Coffee Beans: 5 left (need 10). Recommend reordering from Arabica Roasters.
- Milk: Out of stock (need 8). Recommend reordering from Local Dairy Farm.
```

---

## 📁 Project Structure

```
ai-inventory-alert-automation-n8n/
├── ai-inventory-check-automation.json
├── README.md
├── assets/
│   ├── workflow.png
│   └── email-alert.png
├── .gitignore
└── LICENSE
```

---

## 🧑‍💻 What This Project Shows

* AI agent workflow design
* Real-world automation use case
* LLM integration with tools
* Data filtering and processing
* Email automation

---

## ⭐ Future Improvements

* Add Slack / WhatsApp alerts
* Add auto-reorder system
* Add inventory dashboard
* Use database (PostgreSQL / Firebase)
* Add analytics & reporting

---
