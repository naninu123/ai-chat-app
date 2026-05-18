# AI Chat App

Modern AI chat interface with multi-model support powered by OpenRouter.

## Features

- 🤖 Multiple AI models (GPT-4, Claude, Gemini, DeepSeek)
- 💬 ChatGPT-style UI with streaming responses
- 📝 Markdown rendering with syntax highlighting
- 🌙 Dark mode design
- 📱 Mobile responsive
- 💾 Chat history with sidebar
- ⚡ Fast and modern

## Tech Stack

- Next.js 15
- TypeScript
- Tailwind CSS 4
- Vercel AI SDK
- OpenRouter API

## Setup

1. Clone and install:
```bash
npm install
```

2. Create `.env.local`:
```env
OPENROUTER_API_KEY=your_openrouter_api_key
```

3. Get your OpenRouter API key from [openrouter.ai](https://openrouter.ai)

4. Run development server:
```bash
npm run dev
```

5. Open [http://localhost:3000](http://localhost:3000)

## Deploy to Vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new)

1. Push to GitHub
2. Import to Vercel
3. Add `OPENROUTER_API_KEY` environment variable
4. Deploy

## Models Supported

- GPT-4o / GPT-4 Turbo
- Claude 3.5 Sonnet / Claude 3 Opus
- Gemini 2.0 Flash / Gemini Pro
- DeepSeek Chat

## License

MIT
