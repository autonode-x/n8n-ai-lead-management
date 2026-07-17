# 🚀 n8n AI Lead Management System

An intelligent Lead Management workflow built with **n8n** that automatically receives, validates, stores, updates and acknowledges incoming leads.

Designed for businesses that want to automate lead collection while maintaining a clean CRM without duplicate entries.

---

# ✨ Features

* 🌐 Webhook-based Lead Collection
* ✅ Automatic Input Validation
* 📄 Google Sheets CRM Integration
* 🔍 Duplicate Lead Detection (Email-based)
* ➕ Automatically Creates New Leads
* 🔄 Updates Existing Leads
* 📧 Automatic Thank You Email
* ⚡ Real-time API Response
* 🛡️ Built-in Error Handling
* ☁️ Fully Cloud Deployable

---

# 🏗 Workflow Overview

```
Webhook
    │
    ▼
Validate Input
    │
    ▼
Extract Lead Details
    │
    ▼
Search Lead in Google Sheets
    │
 ┌──────────────┐
 │              │
 ▼              ▼
New Lead     Existing Lead
 │              │
 ▼              ▼
Append Row   Update Row
      │
      ▼
Send Confirmation Email
      │
      ▼
Return JSON Response
```

---

# 🛠 Tech Stack

* n8n
* Google Sheets API
* Gmail API
* Webhooks
* JSON
* REST API

---

# 🧪 Testing

Sample request files are available inside the `testing/` folder.

Example:

```bash
curl -X POST http://localhost:5678/webhook/leads \
-H "Content-Type: application/json" \
-d @testing/sample-request.json
```


---

# 📤 Success Response

```json
{
  "success": true,
  "message": "Lead received successfully."
}
```

---

# 🔄 Workflow Logic

### Step 1

Receive lead via Webhook.

### Step 2

Validate required fields.

### Step 3

Extract lead information.

### Step 4

Search Google Sheets using Email.

### Step 5

If lead doesn't exist:

* Create new row
* Status = **New**

If lead already exists:

* Update existing row
* Status = **Existing Lead**

### Step 6

Send an automatic confirmation email.

### Step 7

Return success response to the client.

---

# 📁 Project Structure

```
.
├── Workflow.json
├── README.md
├── LICENSE
├── .gitignore
├── assets
│   ├── Workflow.png
│   └── architecture.png
└── screenshots
    ├── workflow.png
    ├── gmail-alert.png
    └── google-sheet.png
```

---

# 📸 Screenshots

### Workflow

`assets/Workflow.png`

### Architecture

`assets/architecture.png`

### Google Sheet

`screenshots/google-sheet.png`

### Gmail Response

`screenshots/gmail-alert.png`

---

# 🚀 Use Cases

* Contact Forms
* Business Websites
* AI Agency Lead Collection
* CRM Automation
* Sales Teams
* Marketing Funnels
* Landing Pages

---

# 🔒 Notes

This repository contains only the workflow logic.

API credentials, Google credentials and Gmail credentials are intentionally excluded for security.

---

# 👨‍💻 Author

**Piyush Kumar**

AI Automation Engineer

GitHub: https://github.com/autonode-x

LinkedIn: https://www.linkedin.com/in/piyush-ai

---

## ⭐ If you found this project useful, consider giving it a Star.
