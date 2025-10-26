# 🧠 FinSentra

FinSentra is an **AI-driven market sentiment analyzer** that automates the collection of financial news, analyzes its sentiment, and correlates it with real-time crypto price data.  
Built with **n8n**, **OpenAI**, and **CoinGecko**, it helps traders and financial enthusiasts monitor market psychology effortlessly.

---

## 🚀 Features

- 🔄 **Automated workflow** using [n8n](https://n8n.io)  
- 📰 **Fetches financial or crypto news** via RSS feeds (e.g., CoinDesk, Bloomberg)  
- 🧠 **Analyzes sentiment** (positive, negative, neutral) using OpenAI API  
- 💹 **Retrieves current market prices** (BTC, ETH, etc.) via CoinGecko API  
- 📊 **Logs data automatically** in Google Sheets or Notion  
- 🔔 **Sends Telegram alerts** when bullish or bearish sentiment is detected

---

## ⚙️ Tech Stack

| Component | Role |
|------------|------|
| **n8n** | Workflow automation |
| **OpenAI API** | Sentiment analysis |
| **CoinGecko API** | Real-time price data |
| **RSS Feed** | Market news source |
| **Google Sheets / Notion** | Data logging |
| **Telegram** | Optional alerting |

---

## 🧩 Workflow Overview

1. **Trigger:** n8n fetches new headlines from crypto or stock RSS feeds  
2. **AI Sentiment Analysis:** OpenAI node classifies news as *Positive*, *Negative*, or *Neutral*  
3. **Price Check:** CoinGecko node retrieves live BTC or ETH prices  
4. **Storage:** Results are logged to Google Sheets/Notion  
5. **Alerts (optional):** If positive sentiment + rising price → Telegram alert  

---

## 🧰 Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/meligavincent/finsentra.git
cd finsentra

curl -X GET "https://api.coingecko.com/api/v3/ping" -H "x-cg-demo-api-key: CG-aXpbR5LCu4EENjwSa7MtUHME"