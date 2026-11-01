#telegram-ai-assistant.json  

This repository contains a production-ready **n8n AI workflow** designed to act as an automated personal assistant via Telegram. It leverages an advanced AI Agent powered by OpenAI, complete with memory retention and tools for productivity, task tracking, and sheet updates.

## 📊 Workflow Blueprint
Below is the structural layout of the automation setup:

![n8n Workflow Map]![Telegram AI Assistant Workflow](screenshots/workflow-overview.png.jpg)

### Core Features & Architecture:
- **Telegram Trigger Node:** Acts as the primary interface receiving direct user inputs and queries via a Telegram Bot.
- **AI Agent Node:** Built as the central brain utilizing `OpenAI Chat Model` nodes combined with a `Simple Memory` setup for contextual, multi-turn conversations.
- **Integrated Tooling Nodes:**
  - 📊 **Add Expense:** Automatically maps financial prompts directly into Google Sheets.
  - 📅 **Scheduled Meeting:** Interprets dates/times to construct calendar invites.
  - ✅ **Add Task:** Forwards task management items into target productivity platforms.
- **Send Text Message Node:** Returns a dynamic, structured summary response to the originating Telegram chat window confirming the action's execution status.

## ⚙️ Requirements & Dependencies
To run this configuration effectively, you will need active access keys and integrations for:
- A self-hosted or cloud-hosted **n8n instance**
- An **OpenAI API Key**
- A **Telegram Bot API Token** (Obtained via BotFather)
- Authentication scopes for Google Sheets, Google Calendar, or equivalent tool endpoints

## 🚀 How to Setup and Import
1. Navigate to the `/workflows` directory in this repository and download the `personal-ai-assistant.json` file.
2. Open your web-facing n8n dashboard interface.
3. Select **Create New Workflow** or open a blank canvas.
4. Click the top-right configuration menu button and choose **Import from File**.
5. Upload the downloaded `.json` structure file.
6. Click into the Telegram, OpenAI, and respective Google tool nodes to bind your local secure authentication credentials.
7. Click **Save** and toggle the switch at the top right to **Active**.

