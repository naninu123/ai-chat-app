# AI Chat App

Project AI chat modern dengan dukungan multi-model.

## Status

✅ Build berhasil  
✅ Production-ready  
⚠️ Dev server ada masalah (port conflict)

## Struktur Project

```
ai-chat-app/
├── app/
│   ├── api/chat/route.ts    # API endpoint OpenRouter
│   ├── page.tsx              # Main chat UI
│   ├── layout.tsx            # Root layout
│   └── globals.css           # Tailwind styles
├── .env.local                # API key (perlu diisi)
└── package.json
```

## Setup & Deploy

### 1. Install Dependencies
```bash
cd /home/ubuntu/ai-chat-app
npm install
```

### 2. Konfigurasi API Key
Edit `.env.local`:
```env
OPENROUTER_API_KEY=sk-or-v1-your-key-here
NEXT_PUBLIC_API_URL=https://your-domain.com
```

### 3. Build Production
```bash
npm run build
```

### 4. Deploy dengan PM2
```bash
pm2 start npm --name "ai-chat" -- start
pm2 save
```

### 5. Nginx Config (opsional)
```nginx
server {
    listen 80;
    server_name chat.yourdomain.com;
    
    location / {
        proxy_pass http://localhost:3000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }
}
```

## Fitur

- 🤖 Multi AI model (GPT-4, Claude, Gemini, DeepSeek)
- 💬 Streaming responses
- 📝 Markdown + syntax highlighting
- 🌙 Dark mode
- 📱 Mobile responsive
- 💾 Chat history sidebar
- ⚡ Fast & modern UI

## Deploy ke Vercel (Alternatif)

1. Push ke GitHub
2. Import ke Vercel
3. Tambahkan env var `OPENROUTER_API_KEY`
4. Deploy

## Troubleshooting

**Port sudah dipakai:**
```bash
pkill -f "next"
PORT=3005 npm run dev
```

**Build error:**
```bash
rm -rf node_modules package-lock.json .next
npm install
npm run build
```

Project siap production. Tinggal isi API key dan deploy!
