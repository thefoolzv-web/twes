# POLY·EDGE — AI Polymarket Predictor

## Deploy ke Vercel (5 menit)

### 1. Upload ke GitHub
- Buat repo baru di github.com
- Upload semua file ini (api/, public/, vercel.json)

### 2. Connect ke Vercel
- Buka vercel.com → New Project
- Import repo GitHub lu
- Klik Deploy (settings default OK)

### 3. Set API Key
- Di Vercel dashboard → Settings → Environment Variables
- Tambah:
  - **Name:** `ANTHROPIC_API_KEY`
  - **Value:** `sk-ant-...` (API key lu dari console.anthropic.com)
- Klik Save → Redeploy

### 4. Done!
App live di `https://nama-project.vercel.app`

---

## Deploy ke Netlify (alternatif)

### 1. Upload ke GitHub (sama seperti atas)

### 2. Connect ke Netlify
- buka netlify.com → Add new site → Import from Git
- Pilih repo → Deploy

### 3. Set API Key
- Site settings → Environment variables
- Tambah `ANTHROPIC_API_KEY` = API key lu

### 4. Rename function file
Untuk Netlify, rename `api/predict.js` → `netlify/functions/predict.js`
Dan di `public/index.html`, ganti `/api/predict` → `/.netlify/functions/predict`

---

## Get API Key
1. Buka console.anthropic.com
2. Login / daftar
3. API Keys → Create Key
4. Copy dan paste ke environment variable
