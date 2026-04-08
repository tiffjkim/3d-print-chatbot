# 3D Print Failure Diagnostics

A chatbot for diagnosing 3D printing failures, grounded in Sean Aranda's *3D Printing Failures* (2022). Describes symptoms in plain English, get cited answers from the book.

## Deploy to Vercel (5 minutes)

### 1. Push this repo to GitHub
- Go to github.com → New repository
- Name it `3d-print-chatbot` (or anything you like)
- Push these files to it

### 2. Connect to Vercel
- Go to vercel.com and sign in with your GitHub account
- Click **Add New → Project**
- Select your `3d-print-chatbot` repo
- Click **Deploy** (no build settings needed — Vercel auto-detects it)

### 3. Add your Anthropic API key
- In Vercel, go to your project → **Settings → Environment Variables**
- Add a new variable:
  - Name: `ANTHROPIC_API_KEY`
  - Value: your key from console.anthropic.com
- Click **Save**
- Go to **Deployments** and click **Redeploy** so it picks up the key

### 4. Done
Your chatbot is live at `your-project-name.vercel.app`

Every future push to GitHub auto-redeploys.

## Project structure

```
3d-print-chatbot/
├── index.html     ← the chatbot frontend
├── api/
│   └── chat.js   ← Vercel serverless function (holds API key securely)
└── README.md
```

## Getting an Anthropic API key
- Go to console.anthropic.com
- Sign up / log in
- Go to **API Keys** → **Create Key**
- Copy it into your Vercel environment variable
