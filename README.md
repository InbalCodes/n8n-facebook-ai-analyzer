# Facebook Group Lead Analyzer (n8n + AI)

<img width="3073" height="844" alt="image" src="https://github.com/user-attachments/assets/ed758071-3931-412b-ad7d-407d6aee69f4" />

An automated workflow that scrapes Facebook groups, analyzes posts using Claude 3.5 AI, and prioritizes leads.

## 🚀 Features
- **Apify Integration:** Automatically scrapes the latest posts from selected FB groups.
- **AI Analysis (Anthropic):** Categorizes posts, detects sentiment, and summarizes content.
- **Priority Scoring:** An AI-driven 1-10 score to identify high-value leads.
- **Multi-Channel Output:** - All data is saved to **Google Sheets**.
  - High-priority alerts (Configurable) are sent instantly to **Telegram**.

## ⚙️ Configuration & Setup

To make this workflow your own, follow these steps:

1. **Import the Workflow:** Download the `.json` file from this repo and import it into your n8n instance.
2. **Setup Credentials:** - Add your API keys for **Anthropic**, **Apify**, and **Google Sheets** in the n8n Credentials section.
3. **Personalize Settings:**
   - Locate the node named **"Settings"** at the beginning of the workflow.
   - Update the following fields with your own data:
     - `TELEGRAM_CHAT_ID`: Your unique Telegram chat or group ID.
     - `TARGET_FB_GROUP`: The URL of the Facebook group you wish to scan.
     - `PRIORITY_THRESHOLD`: Set the minimum score (e.g., 8) for receiving Telegram alerts.
4. **Telegram Bot:** Ensure your bot is an administrator in the target group/channel to allow it to send messages.
