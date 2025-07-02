# 🤖 Donna – Your AI-Powered Daily Briefing Assistant

This project automates the generation and delivery of a **morning briefing email** using [n8n](https://n8n.io/) and [OpenAI's Assistants API](https://platform.openai.com/docs/assistants/overview). It fetches your **calendar events**, **weather updates**, and **top news headlines**, then summarizes them with a dash of wit – just like *Donna* from *Suits*.

---

## 🧠 Features

- 📅 Fetches upcoming **Google Calendar** events
- 🌤 Pulls live **weather** data via API
- 📰 Extracts **top 3 headlines** using NewsAPI
- 🤖 Summarizes all info using **OpenAI GPT-3.5 Turbo**
- 💌 Sends an email with a concise, stylish morning briefing
- ✨ Ends every email with a **Donna-style witty remark**

---

## ⚙️ Tools & Services

| Tool         | Purpose                                  |
|--------------|-------------------------------------------|
| `n8n`        | Workflow automation engine                |
| `OpenAI API` | Text summarization via GPT-3.5 Assistant  |
| `Google Calendar` | Event retrieval                      |
| `NewsAPI`    | Top news headlines                        |
| `Weather API`| Current weather info                      |
| `SMTP / Gmail` | Email delivery                          |

---

## 🛠 Workflow Overview

```text
┌────────────┐
│ Cron Start │ ─▶ Triggers Daily at 7 AM
└────┬───────┘
     ▼
┌──────────────┐
│ Google Calendar │ ─┐
└──────────────┘   │
┌─────────────┐    ├─▶ Merge Data
│ Weather API │    │
└─────────────┘    │
┌────────────┐     │
│ News API   │ ────┘
└────────────┘
     ▼
┌────────────────────┐
│ OpenAI Assistant   │ → Generates summary (as Donna)
└────────────────────┘
     ▼
┌────────────┐
│ Send Email │ → Sends formatted briefing to user
└────────────┘
