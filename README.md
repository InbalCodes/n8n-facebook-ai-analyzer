# Facebook Group Lead Analyzer (n8n + AI)

<img width="3073" height="844" alt="image" src="https://github.com/user-attachments/assets/ed758071-3931-412b-ad7d-407d6aee69f4" />

An advanced automation workflow that scrapes Facebook group posts, performs semantic analysis using AI (Claude 4.5), manages a database, and sends real-time high-priority alerts.

## ✨ Features
* **Apify Integration:** Automatically scrapes the latest posts from selected FB groups.
* **AI Analysis (Anthropic):** Categorizes posts, detects sentiment, and summarizes content.
* **Priority Scoring:** An AI-driven 1-10 score to identify high-value leads.
* **Multi-Channel Output:**
    * **Google Sheets:** All data is logged and saved for long-term tracking.
    * **Telegram:** High-priority alerts (Configurable) are sent instantly to your group/chat.

## ⚙️ Configuration & Setup
To make this workflow your own, follow these steps:

1. **Import the Workflow:** Download the `.json` file from this repo and import it into your n8n instance.
2. **Setup Credentials:** Add your API keys for **Anthropic**, **Apify**, **Google Sheets**, and **Telegram** in the n8n Credentials section.
3. **Personalize Settings:**
    * Locate the node named **"Settings"** at the beginning of the workflow.
    * Update the following fields:
        * `TELEGRAM_CHAT_ID`: Your unique Telegram chat or group ID.
        * `TARGET_FB_GROUP`: The URL of the Facebook group you wish to scan.
        * `PRIORITY_THRESHOLD`: Set the minimum score (e.g., 8) for alerts.
4. **Google Sheets Setup:**
    * Create a Google Sheet with the following headers: `Original Post`, `Category`, `Sentiment`, `Summary`, `Priority`, and `URL`.
    * In the **Google Sheets node**, select your Spreadsheet and the specific Sheet name.
5. **Telegram Bot:** Ensure your bot is an administrator in the target group/channel to allow it to send messages.
