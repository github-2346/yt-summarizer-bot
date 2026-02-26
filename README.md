# Telegram YouTube Summarizer Bot

A smart Telegram assistant that helps you understand long YouTube videos quickly.

Send a YouTube link → get a structured summary → receive answers grounded in the transcript.

## Features

- 📺 Accepts YouTube video links
- 📝 Fetches video transcripts automatically
- 🎯 Generates clear, structured summaries
- ❓ Context-aware Q&A based on video content
- 🌍 Multi-language support (English + Indian languages)
- 👥 Handles multiple users simultaneously
- 🧩 Command-based interaction

## User Flow

### 1. Send a YouTube Link

```
https://youtube.com/watch?v=XXXXX
```

Bot responds with:

- 🎥 Video summary  
- 📌 Key points  
- ⏱ Important timestamps  
- 🧠 Core takeaway  

### 2. Ask Questions

Example:

```
What did the video say about pricing?
```

The bot answers using transcript context only.

If the topic is missing:

```
This topic is not covered in the video.
```

### 3. Commands

```
/start           → Welcome message
/summary         → Structured summary
/deepdive        → Detailed explanation
/actionpoints    → Practical takeaways
/lang Hindi      → Change language
/lang English    → Switch back
```

## Project Structure

```
TG_YT_summarizer/
│
├── bot/
│   ├── main.py
│   ├── handlers.py
│   ├── transcript.py
│   ├── summarizer.py
│   ├── qa_engine.py
│   ├── cache.py
│   └── language.py
│
├── data/
│   └── transcripts_cache.json
│
├── requirements.txt
├── render.yaml
└── README.md
```

## ⚙️ Tech Stack

- Python  
- python-telegram-bot  
- youtube-transcript-api  
- Groq API (OpenAI-compatible)  
- Telegram Bot API  
- Render (deployment)

## Local Setup

### 1. Clone repository

```bash
git clone <https://github.com/github-2346/yt-summarizer-bot.git>

cd TG_YT_summarizer
```

### 2. Create virtual environment

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies

```bash
python3 -m pip install -r requirements.txt
```

### 4. Create `.env`

```
TELEGRAM_BOT_TOKEN=YOUR_TOKEN
OPENAI_API_KEY=YOUR_GROQ_KEY
OPENAI_BASE_URL=https://api.groq.com/openai/v1

(OPENAI_API_KEY=YOUR_GROQ_KEY in this the user has to generate a custom key from thr provided linkas paste in here "YOUR_GROQ_KEY")
```

### 5. Run the bot

```bash
python3 bot/main.py
```

Open Telegram and start chatting with your bot.


