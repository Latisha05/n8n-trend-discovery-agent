# 🚀 Trend Discovery Agent (n8n)

An automated AI agent built in **n8n** that converts simple human inputs into professional market trend reports using **Google Gemini** and **SerpApi**.

## 🧠 What It Does
* **Intent Detection:** Smartly decides if a user needs trend research or just a simple chat.
* **Live Web Research:** Fetches real-time Google Search data via SerpApi (bypassing AI knowledge cutoffs).
* **Smart Analysis:** Summarizes raw search results into clear, actionable insights using Google Gemini.
* **Clean Output:** Returns a perfectly formatted JSON response.

## 🛠️ Requirements
* **n8n** (Self-hosted or Cloud)
* **Google Gemini API Key** (Free tier supported)
* **SerpApi Key** (Free tier supported)

## ⚙️ Setup Guide
1.  **Download the Workflow:** Get the `Trend_Discovery_Agent.json` file from this repository.
2.  **Import to n8n:**
    * Go to your n8n dashboard.
    * Click **Add Workflow** > **Import from File**.
3.  **Configure Credentials:**
    * Open the **Google Gemini** nodes and add your API Key.
    * Open the **SerpApi** node and add your API Key.
4.  **Activate:** Toggle the workflow to **Active**.

## 🤖 How It Works
1.  **Trigger:** User sends a keyword (e.g., "Anime").
2.  **Router:** AI checks if the input is a trend request.
3.  **True Branch:**
    * **Query Writer:** AI converts "Anime" -> "latest viral anime trends and statistics 2026".
    * **SerpApi:** Scrapes top Google results for that query.
    * **Analyst:** AI summarizes the scraped data into a report.
4.  **Code Node:** Cleans the final output into a stable JSON format.
