# 🤖 AI Productivity Agent – Built with n8n

This project is a personal AI agent that automates my daily workflow using [n8n](https://n8n.io/). It intelligently pulls data from my calendar, Google Sheets, and weather API, scores my task productivity, and sends me a personalized daily briefing via email — just like Donna from Suits would. 💼

---

## 🚀 Features

- ✅ Reads daily task list from Google Sheets
- 📅 Fetches today's events from Google Calendar
- 🌤️ Gets the weather forecast from OpenWeather API
- 📊 Calculates a daily productivity score based on task completion and priority
- 💌 Sends a motivating and structured daily summary to my Gmail
- 🧠 (Optional) Maintains session memory to personalize future updates

---

## 🔧 Tools & Integrations Used

| Tool / Node               | Purpose                                      |
|---------------------------|----------------------------------------------|
| **Google Sheets**         | Stores task list with priority and status    |
| **Google Calendar**       | Fetches event schedule                       |
| **OpenWeather API**       | Provides local weather forecast              |
| **Custom Code Node**      | Calculates task score and formats output     |
| **Gmail**                 | Sends daily summary email                    |
| **Simple Memory (optional)** | Stores session data for continuity     |
| **OpenAI Chat (Agent)**   | Powers the AI-generated daily summary        |
| **Schedule Trigger**      | Triggers the workflow every morning          |

---

## 🧠 Sample Workflow Summary

1. Triggered every day at 8 AM.
2. Pulls tasks from `Daily_Planner` sheet.
3. Reads events from Google Calendar.
4. Checks weather for the day using your zip code or city.
5. Scores completed vs missed tasks (High = 3 pts, Med = 2 pts, Low = 1 pt).
6. Formats everything into a professional & motivating email.
7. Sends it to my Gmail inbox.

---


