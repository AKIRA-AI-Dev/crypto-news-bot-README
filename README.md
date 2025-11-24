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
```

## 🔐 Configuration

Create a .env file (use .env.example as a template):
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
```
## ▶️ Run
```bash
python main.py
```

  ## 📸 Demo
  ![demo](https://raw.githubusercontent.com/AKIRA-AI-Dev/crypto-news-bot-README/main/Demo.png)

## 📂 Recommended Structure
```css
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
  ```


  ##📟 Bot Commands
  
/news — fetch fresh crypto news



Bot:

parses RSS

rewrites text with GPT

extracts media

generates hashtags

sends posts to moderation

publishes only after approval



/summary_day — daily summary

One-page digest with top events, charts, and key stats.



/summary_week — weekly summary

Deeper analytics for institutional-style channels.


##📝 Moderation System (Core Feature)

All content passes through a moderation chat.

Moderator can:

approve

edit

request rewrite

change style (shorter, formal, journalistic)

add/remove hashtags

Bot posts ONLY the approved version into the main channel.

This makes the bot suitable for real channels and clients.



##🧩 Customization

User/client can configure:

number of posts in /news

RSS sources

writing style

emojis on/off

hashtags auto-generation

posting schedule

inclusion of BTC/ETH/SOL price block

multiple target channels

Everything is controlled via .env.

📰 Demo — /news (5 example posts)

![News Batch 2](https://raw.githubusercontent.com/AKIRA-AI-Dev/crypto-news-bot-README/blob/main/Screenshot_6.png)
![Moderation Flow](https://raw.githubusercontent.com/AKIRA-AI-Dev/crypto-news-bot-README/blob/main/Screenshot_7.png)

📆 Demo — Daly Summary

![Daily Summary](https://raw.githubusercontent.com/AKIRA-AI-Dev/crypto-news-bot-README/main/Screenshot_1.png)

📆 Demo — Weekly Summary


![Weekly Summary](https://raw.githubusercontent.com/AKIRA-AI-Dev/crypto-news-bot-README/main/Screenshot_2.png)
![Weekly Summary](https://raw.githubusercontent.com/AKIRA-AI-Dev/crypto-news-bot-README/main/Screenshot_3.png)




# ⚠️ Security
- Never commit `.env`
- Never commit `.session` files
- Use `.gitignore` to hide secrets

# 📄 License
MIT License © 2025



# 💼 Why This Bot Is Useful

- Automates crypto content creation  
- Reduces workload for channel admins  
- Ensures consistent quality via moderation  
- Supports multi-channel posting  
- Ready for commercial use (agencies, media, crypto channels)  




