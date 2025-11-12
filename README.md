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

## 🔐 Configuration
Create a `.env` file (use `.env.example` as a template):
```env
OPENAI_API_KEY=sk-...

TELEGRAM_API_ID=123456
TELEGRAM_API_HASH=xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
TELETHON_SESSION=./session.session   # path to your Telethon session file

TARGET_CHAT_ID=@your_channel_or_chat

RSS_FEEDS=https://coindesk.com/rss.xml,https://decrypt.co/feed,https://www.theblock.co/rss.xml

POST_BATCH_SIZE=10
ENABLE_WEEKLY_SUMMARY=true
ENABLE_DAILY_SUMMARY=true


▶️ Run
python main.py


📂 Recommended Structur
crypto-news-bot/
  services/
    rss_parser.py
    gpt_utils.py
    news_service.py
    publisher.py
  sender.py
  main.py
  .env.example
  requirements.txt
  .gitignore
  README.md

📸 Demo
!demo(https://raw.githubusercontent.com/AKIRA-AI-Dev/crypto-news-bot-README/main/Demo.png)


