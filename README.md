# Facebook Group Lead Analyzer (n8n + AI)


<img width="3153" height="873" alt="image" src="https://github.com/user-attachments/assets/0636f4f6-b8d1-4fa6-92a5-92368ea9ff46" />


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
2. **Setup the Database:**
    * Upload the provided `Automation_Template.xlsx` to your Google Drive and open it as Google Sheets.
    * In the **"Settings"** tab, fill in your `TELEGRAM_CHAT_ID`, `TARGET_FB_GROUP`, and `PRIORITY_THRESHOLD`.
3. **Connect n8n to Sheets:**
    * In the **"Read Settings"** node (at the start), select your uploaded spreadsheet.
    * In the **"Google Sheets - Append"** node (at the end), select the same spreadsheet and the "Leads" tab.
4. **Setup Credentials:** Add your API keys for **Anthropic**, **Apify**, and **Telegram** in the n8n Credentials section.
5. **Google Sheets Setup:**
    * Create a Google Sheet with the following headers: `Original Post`, `Category`, `Sentiment`, `Summary`, `Priority`, and `URL`.
    * In the **Google Sheets node**, select your Spreadsheet and the specific Sheet name.
6. **Telegram Bot:** Ensure your bot is an administrator in the target group/channel to allow it to send messages.
7. **Run:** Hit "Execute Workflow" and watch the leads flow in!

## 📁 Repository Files
* `Facebook Posts Scraper.json` - The n8n workflow file.
* `FB_Group_Leads_Monitor.xlsx` - The Excel template with pre-defined columns and settings tab.
