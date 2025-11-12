# crypto-news-bot
# 📰 Crypto News Telegram Bot

A Telegram bot that automatically parses crypto news from RSS feeds, rephrases them with GPT, adds hashtags, and publishes posts with media.

## ✨ Features
- Collects news from multiple crypto RSS sources  
- Rewrites and summarizes using OpenAI GPT  
- Generates relevant hashtags automatically  
- Publishes posts (text + media) via Telethon UserBot  
- Supports daily and weekly summaries  

## 🧰 Tech Stack
Python • Telethon • aiogram • feedparser • BeautifulSoup4 • OpenAI API • asyncio • dotenv  

## 📦 Installation
```bash
# Clone the repo
git clone https://github.com/AKIRA-AI-Dev/crypto-news-bot.git
cd crypto-news-bot

# Create virtual environment
python -m venv .venv && .\.venv\Scripts\activate  # Windows  
# or source .venv/bin/activate  # macOS/Linux

# Install dependencies
pip install -r requirements.txt
