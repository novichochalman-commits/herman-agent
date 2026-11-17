# 🤖 Herman Agent — AI Multi-Agent Platform & Autonomous Automation

<p align="center">
  <img src="https://img.shields.io/badge/Version-1.0.0--release-blue.svg?style=for-the-badge" alt="Version 1.0.0">
  <img src="https://img.shields.io/badge/Python-3.10%20%7C%203.11%20%7C%203.12%20%7C%203.13-brightgreen.svg?style=for-the-badge" alt="Python Versions">
  <img src="https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20macOS-orange.svg?style=for-the-badge" alt="Platform">
  <img src="https://img.shields.io/badge/WhatsApp-Baileys%207%20Native-25D366.svg?style=for-the-badge" alt="WhatsApp Native">
  <img src="https://img.shields.io/badge/License-Commercial%20Protected-red.svg?style=for-the-badge" alt="Commercial">
</p>

**Herman Agent** adalah platform AI Multi-Agent otonom tingkat enterprise yang ringan, tangguh, dan modular. Dirancang untuk otomatisasi proses bisnis, customer service pintar, integrasi basis data, RAG (Retrieval-Augmented Generation), dan komunikasi omnichannel real-time melalui WhatsApp Multi-Device (Baileys 7), Telegram Bot, dan Web Chat Widget.

---

## ⚡ Instalasi Cepat 1-Baris (1-Click Auto Installer)

Anda **tidak perlu** meng-clone repositori atau mengatur dependensi secara manual. Cukup jalankan satu baris perintah di terminal:

### 🪟 Untuk Windows (PowerShell)
Buka **PowerShell** (Run as Administrator jika memungkinkan), lalu salin dan jalankan perintah berikut:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass -Force; [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; irm https://github.com/novichochalman-commits/herman-agent/releases/latest/download/install.ps1 | iex
```

> **Catatan Windows:**
> - Installer otomatis mengunduh paket rilis resmi, menyiapkan Virtual Environment, menginstal pustaka AI, dan menyertakan **Node.js 20 LTS Portabel**.
> - Anda **tidak perlu menginstal Node.js secara manual** untuk WhatsApp Bridge.
> - Pintasan desktop **"Herman Agent"** dan **"Hentikan Herman Agent"** akan otomatis dibuat di Desktop.

---

### 🐧 Untuk Linux & macOS (Ubuntu / Debian / CentOS / VPS)
Buka terminal Bash lalu jalankan:

```bash
curl -fsSL https://github.com/novichochalman-commits/herman-agent/releases/latest/download/install.sh | bash
```

> **Catatan Linux:**
> - Installer otomatis mendeteksi paket OS, memasang Python 3, Node.js 20 LTS resmi (via NodeSource), ffmpeg, dan mesin akselerasi `uv`.
> - Perintah CLI `herman` otomatis didaftarkan ke `/usr/local/bin` sehingga dapat dipanggil dari folder mana saja.

---

## 🔑 Informasi Akses Default

Setelah instalasi selesai, server akan otomatis menyala di latar belakang:

* **URL Dashboard:** [http://localhost:8000](http://localhost:8000)
* **WhatsApp Bridge:** [http://localhost:3005](http://localhost:3005)
* **Email Default:** `admin@herman.local`
* **Password Default:** `Admin@12345`

> ⚠️ **PENTING:** Segera ubah kata sandi bawaan melalui menu **Profil / Settings** setelah berhasil login untuk pertama kali.

---

## 🎮 Manajemen Layanan (CLI Commands)

Herman Agent dilengkapi CLI terpadu (`herman`) yang mirip Hermes CLI untuk mengontrol seluruh layanan (Backend FastAPI + WhatsApp Baileys Bridge) dengan mudah:

| Perintah (Windows) | Perintah (Linux/macOS) | Fungsi / Kegunaan |
| :--- | :--- | :--- |
| `.\herman start` | `herman start` | Menyalakan seluruh server & bridge di latar belakang (senyap). |
| `.\herman start -f` | `herman start -f` | Menjalankan dalam mode interaktif (live logs di terminal). |
| `.\herman stop` | `herman stop` | Menghentikan seluruh proses backend dan membebaskan port 8000 & 3005. |
| `.\herman restart` | `herman restart` | Memulai ulang seluruh sistem secara bersih. |
| `.\herman status` | `herman status` | Memeriksa status hidup/mati layanan, PID, port, dan lisensi. |
| `.\herman logs` | `herman logs` | Memantau riwayat log aktivitas realtime (`data/herman.log`). |
| `.\herman license` | `herman license` | Menampilkan Hardware ID (HWID) perangkat dan status lisensi. |

---

## 📱 Panduan Koneksi WhatsApp (Omnichannel)

Herman Agent menggunakan **Baileys v7 ESM Engine** terintegrasi yang mendukung Multi-Device, grup WhatsApp, pesan teks, media (gambar/audio/dokumen), dan LID native:

1. Buka dashboard di browser: `http://localhost:8000`
2. Masuk ke menu **Channel** (Saluran Komunikasi) → Klik **Tambah Saluran**.
3. Pilih tipe saluran **WhatsApp (Baileys Bridge)**.
4. Klik tombol **Hubungkan / Scan QR**:
   - WhatsApp Bridge di port 3005 akan otomatis aktif dalam hitungan 1–2 detik.
   - **Metode 1 (QR Code):** Buka WhatsApp di HP → **Perangkat Tertaut** → Pindai barcode QR yang muncul di layar.
   - **Metode 2 (Kode Pairing 8-Digit):** Masukkan nomor telepon WhatsApp Anda → Klik **Minta Kode Pairing** → Masukkan 8 karakter ke notifikasi WhatsApp di HP Anda.
5. Status saluran akan berubah menjadi **🟢 Terhubung** dan bot AI siap membalas pesan WhatsApp secara otomatis.

---

## ✨ Fitur-Fitur Utama

* 🏠 **Executive Dashboard** — Monitoring statistik percakapan, beban sistem, aktivitas agen, dan latensi LLM secara real-time.
* 💬 **Chat Playground Streaming** — Percakapan langsung dengan model AI dengan dukungan *real-time token streaming* (SSE).
* 🤖 **Role-Based AI Agents** — Template agen siap pakai untuk Customer Service, Sales, HRD, IT Support, General Affairs, Purchasing, dan Agen Kustom.
* 🔌 **Enterprise Integration** — Dukungan konektor Database SQL (MySQL, PostgreSQL, MSSQL, SQLite), REST API, Webhook, ERP, dan Eksekusi Script.
* 📚 **RAG Knowledge Base (ChromaDB)** — Unggah dokumen PDF, DOCX, TXT, CSV, atau Web URL untuk dijadikan basis pengetahuan pintar agen dengan *vector search*.
* 📡 **Multi-Channel Omnichannel** — Dukungan integrasi langsung ke WhatsApp (Baileys Multi-Device), Telegram Bot, dan Web Embed Widget untuk website Anda.
* 🧠 **Autonomous Memory & Skills** — Memori percakapan berjangka panjang (Episodic, Semantic, Procedural) serta registry fungsi *tool-calling*.
* ⏰ **Task Scheduler** — Penjadwal tugas otomatis berbasis ekspresi Cron maupun eksekusi satu kali (*one-time delayed tasks*).
* 🛠️ **Model Context Protocol (MCP)** — Pengelolaan client/server MCP standar Anthropic untuk ekspansi kapabilitas agen tanpa batas.
* 🛡️ **Role-Based Access Control (RBAC)** — Manajemen hak akses bertingkat (Superadmin, Admin, Operator, Viewer), audit logging, dan API Key access.

---

## 🤖 Model AI & Provider yang Didukung

Herman Agent mendukung arsitektur multi-provider:

| Provider | Konfigurasi di `.env` / Menu Settings | Model Populer |
| :--- | :--- | :--- |
| **OpenAI** | `DEFAULT_OPENAI_API_KEY` | `gpt-4o`, `gpt-4o-mini`, `o1-mini` |
| **Google Gemini** | `DEFAULT_GEMINI_API_KEY` | `gemini-1.5-pro`, `gemini-1.5-flash`, `gemini-2.0-flash` |
| **Anthropic Claude** | `DEFAULT_ANTHROPIC_API_KEY` | `claude-3-5-sonnet`, `claude-3-5-haiku` |
| **Groq (Ultra-Fast)** | `DEFAULT_GROQ_API_KEY` | `llama-3.3-70b-versatile`, `mixtral-8x7b` |
| **Ollama (Lokal/Privat)**| `OLLAMA_BASE_URL=http://localhost:11434` | `deepseek-r1`, `llama3.2`, `mistral`, `qwen2.5` |
| **OpenAI-Compatible** | Endpoint kustom + API Key kustom | vLLM, LM Studio, OpenRouter, Together AI |

---

## 🔒 Manajemen Lisensi Komersial (Hardware ID Binding)

Herman Agent dilengkapi dengan sistem pengamanan kode dan penegakan lisensi berbasis Hardware ID perangkat (Motherboard UUID + CPU + OS Machine GUID):

1. **Cek Hardware ID (HWID):**
   ```bash
   # Di Windows:
   .\herman license

   # Di Linux:
   herman license
   ```
2. **Format Kunci Lisensi:**
   Lisensi resmi diterbitkan dengan ekstensi `license.key`.
3. **Menerapkan Lisensi:**
   Cukup letakkan file `license.key` di folder utama aplikasi (`herman-agent/license.key`), atau tempelkan isi kuncinya saat menjalankan installer.

---

## 🛠️ Panduan Memperbarui (Update) ke Versi Terbaru

Jika ada pembaruan versi rilis dari tim pengembang, Anda tidak perlu mengulang proses dari awal. Cukup jalankan perintah instalasi 1-baris yang sama:

* **Windows:**
  ```powershell
  Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass -Force; [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; irm https://github.com/novichochalman-commits/herman-agent/releases/latest/download/install.ps1 | iex
  ```
* **Linux:**
  ```bash
  curl -fsSL https://github.com/novichochalman-commits/herman-agent/releases/latest/download/install.sh | bash
  ```

Installer akan mendeteksi folder yang ada, menghentikan server lama secara aman, memperbarui file sistem, dan menyalakan kembali server dengan database data Anda tetap utuh (`data/` tidak akan hilang).

---

## ❓ FAQ & Troubleshooting

### 1. Port 8000 atau Port 3005 Sudah Digunakan?
Hentikan seluruh proses yang sedang aktif menggunakan perintah:
```bash
# Windows
.\herman stop

# Linux
herman stop
```
Atau jika port terkunci oleh aplikasi lain, ubah nilai `PORT=8001` di file `.env`.

### 2. Barcode QR WhatsApp Tidak Mau Muncul?
- Pastikan tidak ada firewall lokal yang memblokir koneksi internal antar-port `127.0.0.1:3005`.
- Buka terminal dan periksa log bridge:
  ```bash
  # Windows
  Get-Content data/bridge.log -Tail 30

  # Linux
  tail -n 30 data/bridge.log
  ```
- Klik tombol **"🚀 Nyalakan Bridge & Tampilkan QR"** pada modal WhatsApp. Sistem akan melakukan inisialisasi soket otomatis dalam waktu < 2 detik.

### 3. Di mana letak database & berkas percakapan?
Seluruh data tersimpan secara lokal dan privat di folder `data/`:
- `data/herman.db` : Database SQLite (pengguna, agen, konfigurasi, riwayat pesan)
- `data/chroma/` : Vector Store database untuk RAG dokumen
- `data/baileys/` : Kredensial sesi WhatsApp terenkripsi
- `data/uploads/` : File dokumen lampiran & knowledge base

---

## 📄 Hak Cipta & Lisensi

Hak Cipta © 2026 **Herman Agent Team**. Seluruh hak cipta dilindungi undang-undang.
Dilarang mendistribusikan ulang, mendekompilasi, merekayasa balik (*reverse engineer*), atau menjual kembali perangkat lunak ini tanpa izin lisensi komersial resmi dari pemegang hak cipta.
