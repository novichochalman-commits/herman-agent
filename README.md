# 🌐 Website Herman Agent — Autonomous Enterprise Multi-Agent AI

Website resmi mandiri (**Standalone Static Web**) untuk **Herman Agent** dengan desain **Hitam Putih Modern (Monochrome)** berstandar industri (*Vercel / Linear Aesthetic*).

---

## 🚀 Fitur Unggulan Herman Agent yang Ditampilkan di Website

Berdasarkan arsitektur aktual di dalam kode sumber Herman Agent:

1. **Autonomous Skills Engine (Bisa Bikin Tool & Integrasi Sendiri):**
   - Agen mampu menulis, menguji, dan mendaftarkan script Python baru di folder `skills/` secara *on-the-fly*.
   - Otomatis memvalidasi sintaks AST (*Abstract Syntax Tree*), menyusun *OpenAI Tool Schema*, dan me-reload fungsi secara dinamis (*zero downtime hot-reload*).
   - Terhubung ke **Skills Hub & GitHub Taps** untuk instalasi 1-klik tool komunitas dari GitHub.
2. **Sistem Memori 3 Tingkat (3-Tier Long-Term Memory):**
   - **Episodic Memory:** Mengingat peristiwa percakapan lampau, tiket keluhan, dan interaksi lintas sesi.
   - **Semantic Memory:** Menyimpan fakta penting tentang pengguna, termin bisnis, dan nama klien secara terstruktur.
   - **Procedural Memory:** Mengingat langkah-langkah kerja, alur SOP, dan prosedur operasional yang pernah dipelajari.
3. **Model Context Protocol (MCP) Server Manager:**
   - Mendukung standar terbuka industri dari Anthropic (MCP).
   - Manajemen server MCP via transport `stdio` (`npx`, `python`) dan `sse` (HTTP remote).
   - Katalog preset resmi (@modelcontextprotocol/server-filesystem, server-postgres, server-brave-search).
4. **Human-in-the-Loop (Approval Guard):**
   - Pengaman aksi kritis: Eksekusi berisiko (drop tabel database, transaksi finansial bernilai besar, perintah sistem) seketika dijeda (*paused*).
   - Notifikasi persetujuan multi-kanal: tombol persetujuan di **Web Dashboard**, tombol interaktif **Telegram Bot ([✅ Setujui] [❌ Tolak])**, dan pesan konfirmasi **WhatsApp**.
5. **Divisi Agen Spesialis & RAG Knowledge Base:**
   - 8 peran divisi siap pakai (CS, HR, Sales, IT Support, GA, Manager, Purchasing).
   - Basis data vektor ChromaDB lokal untuk dokumen SOP internal kantor (PDF, DOCX, TXT, URL).
6. **Paket Lisensi On-Premise & Aktivasi WhatsApp:**
   - **Free Trial 7 Hari (Rp 0):** Evaluasi penuh seluruh fitur AI tanpa batasan selama 1 minggu di server lokal.
   - **Langganan Bulanan (Rp 99.000 / bulan):** Akses penuh enterprise tanpa batas, unlimited agen divisi, WhatsApp multi-session, dynamic skills engine, dan update prioritas.
   - **WhatsApp Resmi Aktivasi Lisensi:** `+62 851-7963-0119` (https://wa.me/6285179630119).
7. **Panduan Instalasi Kilat 1 Baris (Hermes Style):**
   - Perintah 1 baris untuk Windows PowerShell dan Linux/macOS Bash.
   - Tautan langsung ke GitHub Releases resmi:  
     👉 `https://github.com/novichochalman-commits/herman-agent/releases`

---

## 📁 Struktur Folder `website/`

```text
website/
├── index.html       # Halaman landing page lengkap dengan tipografi Space Grotesk + Plus Jakarta Sans
├── style.css        # Desain Vanilla CSS hitam-putih, micro-borders, dan layout bento grid
├── script.js        # Logika tab OS instalasi, copy 1-klik clipboard, agent workbench, dan drawer mobile
└── README.md        # Panduan fitur dan hosting
```

---

## 💻 Cara Menghosting Website Sendiri

Website ini berstatus **100% Client-Side Static Web** (tanpa dependensi backend Node.js atau Python):

1. **Vercel / Netlify:** Cukup tarik (*drag-and-drop*) folder `website/` ke dashboard Netlify ([app.netlify.com/drop](https://app.netlify.com/drop)) atau sambungkan ke repo GitHub di Vercel.
2. **GitHub Pages:** Masukkan file `index.html`, `style.css`, dan `script.js` ke repository GitHub, lalu aktifkan Pages di Settings.
3. **Server Lokal / VPS Nginx:** Salin seluruh file ke folder root web server Anda (`/var/www/html/`).

#### Preview Lokal di Komputer:
Cukup klik dua kali file `index.html` untuk membuka langsung di Google Chrome atau Microsoft Edge.
