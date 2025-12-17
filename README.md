# WS Analytics Chat

AI-чат для аналітики даних Worksection. Побудовано на Next.js + n8n AI Agent.

![WS Analytics](https://img.shields.io/badge/Next.js-14-black) ![TypeScript](https://img.shields.io/badge/TypeScript-5-blue) ![License](https://img.shields.io/badge/license-MIT-green)

## 🚀 Швидкий старт

### 1. Встановлення залежностей

```bash
npm install
```

### 2. Налаштування змінних середовища

Створіть файл `.env.local`:

```bash
N8N_WEBHOOK_URL=https://n8n.rnd.webpromo.tools/webhook/ws-ai-agent
```

### 3. Запуск локально

```bash
npm run dev
```

Відкрийте [http://localhost:3000](http://localhost:3000)

## 📦 Деплой на Vercel

### Варіант 1: Через GitHub

1. Завантажте проект на GitHub
2. Імпортуйте в [Vercel](https://vercel.com/new)
3. Додайте Environment Variable:
   - **Name:** `N8N_WEBHOOK_URL`
   - **Value:** `https://n8n.rnd.webpromo.tools/webhook/ws-ai-agent`
4. Deploy!

### Варіант 2: Через Vercel CLI

```bash
npm i -g vercel
vercel
```

## 🎨 Можливості

- 💬 Сучасний чат-інтерфейс у стилі ChatGPT
- 🌙 Темна тема
- 📊 Підтримка Markdown таблиць
- 🔄 Анімації та плавні переходи
- 📱 Адаптивний дизайн
- ⚡ Швидкі підказки для запитів

## 📝 Приклади запитів

- "Скільки користувачів у базі?"
- "Покажи топ-5 відділів за кількістю задач"
- "Скільки прострочених задач у відділу PM?"
- "Яка статистика по проектах за останній місяць?"

## 🛠 Технології

- **Frontend:** Next.js 14, React 18, TypeScript
- **Styling:** CSS (без Tailwind)
- **Backend:** n8n AI Agent + OpenAI GPT-4
- **Database:** Supabase (PostgreSQL)

## 📁 Структура проекту

```
ws-chat-agent/
├── app/
│   ├── api/
│   │   └── chat/
│   │       └── route.ts    # API endpoint
│   ├── globals.css         # Стилі
│   ├── layout.tsx          # Layout
│   └── page.tsx            # Головна сторінка
├── .env.example            # Приклад змінних
├── package.json
├── tsconfig.json
└── README.md
```

## 🔧 n8n Workflow

Переконайтеся, що n8n workflow `AI agent for CHAT` активний:

1. Webhook: `POST /webhook/ws-ai-agent`
2. AI Agent з OpenAI GPT-4.1-mini
3. HTTP Request Tool → `/webhook/claude-sql`

## 📄 Ліцензія

MIT
