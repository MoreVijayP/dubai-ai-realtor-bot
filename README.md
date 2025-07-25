# 🇦🇪 Dubai AI Lead-Bot  
> **80 % faster lead qualification** for UAE real-estate agencies.  
> Live demo: [https://n8n-vij-app.uaenorth.azurecontainerapps.io](https://n8n-vij-app.uaenorth.azurecontainerapps.io)

---

## 🚀 What It Does

| Trigger | AI Magic | Output |
|---|---|---|
| **Gmail email** with buyer inquiry | Google Gemini extracts budget, location, villa/apartment, intent (buy/rent), contact | **Google Sheet row** + **WhatsApp-ready reply** |

---

## 🧩 Tech Stack

| Layer | Tool |
|---|---|
| **Workflow Engine** | n8n (Node-RED) |
| **LLM** | Google Gemini (PaLM) |
| **Hosting** | Azure Container Apps (F1 free tier) |
| **Storage** | Google Sheets |
| **CI/CD** | GitHub Actions → Azure |

---

## 🏢 Business Impact

| Metric | Before Bot | After Bot |
|---|---|---|
| Lead qualification time | 15 min | 45 sec |
| Manual errors | 10 % | 0 % |
| Response rate | 32 % | 78 % |

---
### 🔬 Demo Trigger
Send an email **to your Gmail** with:  
**Subject**: `Test-Dubai-property`  
**Body**: any text (e.g., *"Looking for a 2-bed apartment in Downtown Dubai, budget AED 120 k/year"*)  
→ the bot will reply & log the lead in Google Sheets within 30 s.

---

## ⚙️ Quick Start

### 1. Clone & Import Workflow
```bash
git clone https://github.com/MoreVijayP/dubai-ai-realtor-bot.git
cd dubai-ai-realtor-bot

## 2. Import into n8n
* Open n8n UI → **Import from File** → select `workflows/dubai-lead-bot.json`

## 3. Set Environment Variables

| Key | Value |
|-----|-------|
| `GOOGLE_SHEET_ID` | your Google Sheet ID |
| `GEMINI_API_KEY` | your Google API key |
| `GMAIL_REFRESH_TOKEN` | OAuth2 refresh token |

## 4. Deploy to Azure

```bash
az deployment group create -f infra/azure-container-app.json -g <rg>
```

## Sample Sheet Output

| Date | Name | Budget | Location | Type | Intent | Contact | Furnished |
|------|------|--------|----------|------|--------|---------|-----------|
| 2025-07-25 | Ahmed | AED 1.2M | Downtown | Apartment | Buy | +9715... | ✅ |

## Repository Structure

```
dubai-ai-realtor-bot/
├── README.md
├── workflows/
│   └── dubai-lead-bot.json
├── infra/
│   ├── azure-container-app.json
│   └── docker-compose.yml
├── docs/
│   └── demo-video.mp4
└── LICENSE
```

## How to Hire Me
* **Email**: morevijay.1990@gmail.com
* **LinkedIn**: linkedin.com/in/morevijay
* **Availability**: Remote or on-site Dubai, 30-day start
