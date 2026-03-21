# 📦 Airtable AI Order Email Notifier

An automated order notification pipeline that monitors Airtable for new orders, uses Google Gemini AI to generate professional email summaries, and instantly delivers them to your team via Gmail.

## 🧠 How It Works

1. Airtable Trigger polls for new orders every minute
2. Gemini 2.5 Flash generates a professional HTML email summary
3. JavaScript node cleans and parses the JSON response
4. Gmail sends the formatted email to the team instantly

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| AI Model | Google Gemini 2.5 Flash |
| Automation | n8n |
| Data Source | Airtable |
| Notifications | Gmail |
| Logic | JavaScript (Code Node) |

## ✨ Features

- ⚡ Real-time Airtable polling (every minute)
- 🤖 AI-generated professional HTML email summaries
- 📋 Includes Order Number, Customer, Product, Quantity, Price, Date, Status
- 📧 Instant Gmail delivery with formatted HTML content
- 🔧 Clean JSON parsing with error-safe JavaScript node

## 📦 Setup

1. Import `airtable_to_email.json` into your n8n instance
2. Connect your **Airtable Personal Access Token** credentials
3. Connect your **Google Gemini API** credentials
4. Connect your **Gmail OAuth2** credentials
5. Update the Airtable Base ID and Table ID in the trigger node
6. Update the recipient email in the Gmail node
7. Activate the workflow

## 🔑 Required Credentials

- Airtable Personal Access Token
- Google Gemini (PaLM) API Key
- Gmail OAuth2

## 📋 Airtable Schema

Your Airtable table should have these fields:

| Field | Type |
|---|---|
| Order Number | Auto Number |
| Customer | Single Line Text |
| Product | Single Line Text |
| Quantity | Number |
| Price | Currency |
| Date | Date |
| Status | Single Select |

---

Built by [Muhammad Musaddaq Qaysir](https://musadiq-portfolio.vercel.app/)
