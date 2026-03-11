# 🤖 Saarthi Bot — सारथी बॉट

<p align="center">
  <img src="https://img.shields.io/badge/SAARTHI%20BOT-YOUR%20INTELLIGENT%20GUIDE-cyan?style=for-the-badge&labelColor=black" alt="Saarthi Bot" width="500">
</p>

<p align="center">
  <strong>सारथी बॉट — YOUR INTELLIGENT GUIDE</strong>
</p>

<p align="center">
  <a href="#"><img src="https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge" alt="Status"></a>
  <a href="#"><img src="https://img.shields.io/badge/Language-Hindi%20%7C%20English-blue?style=for-the-badge" alt="Bilingual"></a>
  <a href="#"><img src="https://img.shields.io/badge/Platform-Telegram%20%7C%20WhatsApp-cyan?style=for-the-badge" alt="Platform"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-purple?style=for-the-badge" alt="MIT License"></a>
</p>

**Saarthi Bot** is a _next-generation bilingual AI assistant_ — your personal intelligent guide that speaks your language.
It answers you in **Hindi and English**, works on the platforms you already use (Telegram, WhatsApp), and runs 24/7 with zero friction.
From smart conversations to task assistance, Saarthi is always by your side.

If you want a personal AI assistant that feels local, fast, bilingual, and always-on — this is it.

[Features](#features) · [Getting Started](#getting-started) · [Commands](#commands) · [Tech Stack](#tech-stack) · [Installation](#installation) · [Demo](#demo) · [FAQ](#faq)

---

## ✨ What Makes Saarthi Special

**Saarthi Bot** is not just another chatbot. It's your intelligent guide — built for Indians, by an Indian.

- 🇮🇳 **Bilingual First** — Speaks Hindi + English fluently. Mix both, Saarthi understands.
- ⚡ **Next-Level Intelligence** — Powered by cutting-edge AI for smart, contextual responses.
- 🚀 **Up & Running in Minutes** — No complex setup. Just connect and start chatting.
- 🌐 **Any OS, Any Platform** — Works on Windows, Linux, macOS. Connects via Telegram and WhatsApp.
- 🔥 **Always-On** — 24/7 availability. Never sleeps, never forgets context.

---

## 🚀 Quick Start (TL;DR)

Runtime: **Node ≥ 18**

```bash
git clone https://github.com/dhirendram128-netizen//saarthi-bot.git
cd saarthi-bot

npm install
# or: pnpm install

cp .env.example .env
# Fill in your API keys

npm start
```

Then open Telegram and message your bot. Saarthi is ready. 🎉

---

## 📦 Installation

### Prerequisites

- Node.js ≥ 18
- npm / pnpm / bun
- Telegram Bot Token (from [@BotFather](https://t.me/BotFather))
- AI API Key (OpenAI / Anthropic / Gemini)

### Step 1 — Clone the Repo

```bash
git clone https://github.com/YOUR_USERNAME/saarthi-bot.git
cd saarthi-bot
```

### Step 2 — Install Dependencies

```bash
npm install
# or
pnpm install
```

### Step 3 — Configure Environment

```bash
cp .env.example .env
```

Edit `.env` file:

```env
TELEGRAM_BOT_TOKEN=your_telegram_bot_token_here
AI_API_KEY=your_ai_api_key_here
DATABASE_URL=your_database_url_here
BOT_NAME=Saarthi
DEFAULT_LANGUAGE=hi
```

### Step 4 — Start Saarthi

```bash
npm start

# Development mode (auto-reload)
npm run dev
```

Saarthi Bot is now live on Telegram! 🚀

---

## 🏗️ Architecture

```
Telegram / WhatsApp
        │
        ▼
┌─────────────────────────────┐
│         Saarthi Bot         │
│      (Control Layer)        │
│    localhost:3000           │
└──────────────┬──────────────┘
               │
               ├─ AI Engine (Claude / GPT / Gemini)
               ├─ Language Detector (Hindi / English)
               ├─ Command Handler
               ├─ Database (Firebase / Supabase)
               └─ Notification Service (Vonage)
```

---

## 🎯 Features

### Core Intelligence
- **[Bilingual AI Chat](/)** — Understands and responds in Hindi + English seamlessly.
- **[Contextual Memory](/)** — Remembers conversation context for natural dialogue flow.
- **[Smart Command System](/)** — Clean slash commands for every action.
- **[Auto Language Detection](/)** — Detects whether you're typing Hindi or English automatically.

### Platform Support
- **[Telegram](/)** — Full feature support via Telegram Bot API.
- **[WhatsApp](/)** — _(Coming Soon)_ — WhatsApp Business API integration.
- **[Web Interface](/)** — _(Coming Soon)_ — Browser-based chat UI.

### Automation
- **[Scheduled Messages](/)** — Set reminders and scheduled tasks.
- **[Webhook Support](/)** — External triggers and integrations.
- **[Notification Engine](/)** — Real-time alerts via Vonage SMS.

### Developer Tools
- **[REST API](/)** — Integrate Saarthi into your own apps.
- **[Plugin System](/)** — Extend Saarthi with custom skills.
- **[Logging & Monitoring](/)** — Full activity logs with error tracking.

---

## 💬 Commands

Send these in Telegram chat:

| Command | Description |
|---------|-------------|
| `/start` | Welcome message + onboarding |
| `/help` | Show all available commands |
| `/ask <question>` | Ask Saarthi anything (Hindi or English) |
| `/reset` | Reset conversation context |
| `/language <hi/en>` | Switch response language |
| `/status` | Check bot status and uptime |
| `/settings` | Personal preferences |
| `/remind <time> <message>` | Set a reminder |
| `/feedback` | Send feedback to developer |

---

## ⚙️ Configuration

Minimal `config.json` setup:

```json
{
  "bot": {
    "name": "Saarthi",
    "language": "hi",
    "ai_model": "claude-3-sonnet"
  },
  "telegram": {
    "token": "YOUR_BOT_TOKEN"
  },
  "database": {
    "provider": "supabase"
  }
}
```

Full configuration reference: [docs/configuration.md](docs/configuration.md)

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Runtime | Node.js ≥ 18 |
| Package Manager | pnpm / npm |
| Bot Framework | Telegraf (Telegram) |
| AI Engine | Claude / GPT-4 / Gemini |
| Database | Firebase / Supabase |
| SMS / OTP | Vonage API |
| Hosting | Linux VPS / Railway / Render |
| Language | TypeScript / JavaScript |

---

## 🔒 Security

Saarthi Bot follows security best practices:

- **DM Policy** — Unknown users must verify before chatting.
- **Rate Limiting** — Prevents spam and abuse.
- **Environment Variables** — All secrets stored in `.env`, never in code.
- **Allowlist System** — Control who can use the bot.

To enable public DMs, set `dm_policy: "open"` in your config.

Run `npm run doctor` to check for security misconfigurations.

---

## 🌐 Deployment

### Deploy on Linux VPS

```bash
# Install PM2 for process management
npm install -g pm2

# Start Saarthi with PM2
pm2 start src/index.js --name "saarthi-bot"
pm2 save
pm2 startup
```

### Deploy on Railway / Render

1. Push code to GitHub
2. Connect repo to Railway or Render
3. Add environment variables
4. Deploy — done! ✅

### Docker Support

```bash
docker build -t saarthi-bot .
docker run -d --env-file .env saarthi-bot
```

---

## 📊 One Bot, Two Languages

Saarthi understands you no matter how you type:

```
You:     "Kal mujhe 9 baje reminder do"
Saarthi: "ठीक है! कल सुबह 9 बजे आपको reminder मिलेगा। 🔔"

You:     "What's the weather like today?"
Saarthi: "I'll check that for you right away! 🌤️"

You:     "Bhai ye code kyu kaam nahi kar raha"
Saarthi: "Code dekho — line 42 pe semicolon missing hai 😄"
```

---

## 🗺️ Roadmap

| Phase | Feature | Status |
|-------|---------|--------|
| v1.0 | Telegram Bot + AI Chat | ✅ Done |
| v1.1 | Bilingual Support (Hindi/English) | ✅ Done |
| v1.2 | Reminders + Scheduling | 🔄 In Progress |
| v1.3 | WhatsApp Integration | 📋 Planned |
| v2.0 | Voice Commands | 📋 Planned |
| v2.1 | Web Dashboard | 📋 Planned |
| v3.0 | Neo Jarvis Mode (Full AI OS) | 🔮 Future |

---

## 🤝 Contributing

Contributions welcome! AI-assisted PRs accepted. 🤖

1. Fork the repo
2. Create your feature branch: `git checkout -b feature/amazing-feature`
3. Commit changes: `git commit -m 'Add amazing feature'`
4. Push to branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## 📄 License

This project is licensed under the **MIT License** — see [LICENSE](LICENSE) for details.

---

## 👨‍💻 Creator

**Saarthi Bot** was built with vision, grind, and belief.

- Built by **Dhirendra Maurya** — AI Entrepreneur, Tech Builder
- Part of the **Neo Jarvis Ecosystem**
- Vision: Building India's most trusted AI assistant

> *"Saarthi means guide. And that's exactly what this bot is — your personal AI guide, always by your side."*

---

<p align="center">
  <strong>⭐ Star this repo if Saarthi helped you!</strong><br>
  Made with ❤️ in India 🇮🇳
</p>
