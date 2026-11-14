# Herman Agent — README

# 🤖 Herman Agent

Platform AI Multi-Agent berbasis Python yang ringan, modular, dan dapat di-deploy dengan Docker.

## ✨ Fitur

- 🏠 **Dashboard** — Monitoring real-time statistik dan sistem
- 💬 **Chat** — Real-time streaming dengan berbagai agent AI
- 🤖 **Agent** — CS, Sales, HR, IT, GA, Manager, Purchasing, Custom
- 🔌 **Integration** — Database, REST API, ERP, Cloud, Email, Script
- 📚 **Knowledge Base** — RAG dengan ChromaDB, PDF/DOCX/URL
- 📡 **Channel** — WhatsApp (Baileys), Telegram, Web Widget
- 🧠 **Memory & Skill** — Episodic, Semantic, Procedural memory
- ⏰ **Scheduler** — Cron jobs dan one-time tasks
- 🛠 **MCP** — Model Context Protocol server management
- 👤 **User** — RBAC, audit log, API key management
- ⚙️ **Settings** — Konfigurasi global sistem

## 🚀 Quick Start

### Cara 1: Jalankan Langsung

```bash
# 1. Clone/download project
cd herman-agent

# 2. Setup virtual environment
python -m venv venv
venv\Scripts\activate  # Windows
# source venv/bin/activate  # Linux/Mac

# 3. Install dependencies
pip install -r requirements.txt

# 4. Copy dan edit konfigurasi
copy .env.example .env
# Edit .env sesuai kebutuhan

# 5. Jalankan
python -m uvicorn app.main:app --host 0.0.0.0 --port 8000 --reload
```

### Cara 2: Docker

```bash
# 1. Copy .env
copy .env.example .env
# Edit .env

# 2. Jalankan dengan Docker Compose
cd docker
docker-compose up -d

# Lihat logs
docker-compose logs -f herman-agent
```

## 🔑 Default Login

- **URL**: http://localhost:8000
- **Email**: admin@herman.local
- **Password**: Admin@12345

⚠️ **Ganti password setelah login pertama!**

## 📁 Struktur Project

```
herman-agent/
├── app/
│   ├── main.py              # Entry point
│   ├── config.py            # Settings
│   ├── database.py          # Models
│   ├── auth/                # Auth module
│   ├── core/                # LLM, RAG, Memory, Scheduler
│   ├── modules/             # Feature modules
│   │   ├── dashboard/
│   │   ├── chat/
│   │   ├── agents/
│   │   ├── knowledge/
│   │   ├── integrations/
│   │   ├── channels/
│   │   ├── memory/
│   │   └── ...
│   ├── static/              # CSS, JS
│   └── templates/           # HTML templates
├── data/                    # Database & uploads
├── docker/                  # Docker files
├── requirements.txt
├── .env.example
└── README.md
```

## ⚙️ Konfigurasi (.env)

| Variable | Default | Keterangan |
|----------|---------|------------|
| `SECRET_KEY` | *wajib diisi* | JWT secret key |
| `ADMIN_EMAIL` | admin@herman.local | Email admin |
| `ADMIN_PASSWORD` | Admin@12345 | Password admin |
| `DEFAULT_AI_PROVIDER` | openai | Provider AI default |
| `DEFAULT_OPENAI_API_KEY` | - | API Key OpenAI |
| `TELEGRAM_BOT_TOKEN` | - | Token bot Telegram |
| `TIMEZONE` | Asia/Jakarta | Timezone sistem |

## 🤖 AI Provider yang Didukung

| Provider | Konfigurasi |
|----------|-------------|
| OpenAI | API key + model (gpt-4o, gpt-4o-mini, dll.) |
| Anthropic | API key + model (claude-3.5-sonnet, dll.) |
| Google Gemini | API key + model (gemini-pro, dll.) |
| Ollama | URL lokal (http://localhost:11434) |
| Custom | URL endpoint + API key (OpenAI-compatible) |

## 📡 Channel Setup

### Telegram
1. Chat @BotFather di Telegram
2. Buat bot baru, salin token
3. Di Herman Agent → Channel → Tambah Channel → Telegram
4. Masukkan token, pilih agent

### WhatsApp (via Baileys Bridge)
1. Setup Node.js Baileys bridge service
2. Konfigurasi BAILEYS_BRIDGE_URL di .env
3. Di Herman Agent → Channel → Tambah Channel → WhatsApp
4. Scan QR code

## 📋 API Documentation

Tersedia di `/docs` saat DEBUG=true

## 🐳 Production Deployment

```bash
# Pastikan SECRET_KEY aman dan panjang
SECRET_KEY=$(openssl rand -hex 32)

# Jalankan dengan Docker
docker-compose -f docker/docker-compose.yml up -d
```

---

*Herman Agent v1.0 — Built with FastAPI, SQLite, ChromaDB*
