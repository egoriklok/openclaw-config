# ClawCloud Deployment Guide

Complete guide to deploying OpenClaw on ClawCloud.

## Prerequisites

1. **GitHub Account** (for OpenRouter signup)
2. **Telegram Account** (for bot creation)
3. **ClawCloud Account** (free tier available)

---

## Step 1: Get OpenRouter API Key

1. Go to [openrouter.ai](https://openrouter.ai)
2. Click "Sign Up" → Use GitHub
3. Go to Dashboard → API Keys
4. Create new key, copy: `sk-or-v1-xxxxx`

**Free Credits**: New accounts get $5-10 free!

---

## Step 2: Create Telegram Bot

1. Open Telegram, search for `@BotFather`
2. Send `/newbot`
3. Follow prompts to name your bot
4. Copy the API token: `1234567890:ABCdefGhI...`

---

## Step 3: Deploy on ClawCloud

### Option A: One-Click Deploy (Recommended)

1. Click this button:

[![Run on ClawCloud](https://raw.githubusercontent.com/ClawCloud/Run-Template/refs/heads/main/Run-on-ClawCloud.svg)](https://template.run.claw.cloud/?openapp=system-fastdeploy%3FtemplateName%3Dopenclaw)

2. Fill in the config:

| Field | Value |
|-------|-------|
| `openai_base_url` | `https://openrouter.ai/api/v1` |
| `openai_api_key` | Your OpenRouter key |
| `openai_model` | `deepseek/deepseek-r1` |
| `telegram_bot_token` | Your Telegram token |

3. Click **Deploy**

### Option B: Manual Setup

1. Go to [eu-central-1.run.claw.cloud](https://eu-central-1.run.claw.cloud)
2. Open **App Store** → Search "OpenClaw"
3. Click **Install**
4. Fill in environment variables
5. Deploy

---

## Step 4: Verify Deployment

1. Wait 2-3 minutes for container to start
2. Open Telegram, find your bot
3. Send `/start`
4. Bot should respond!

---

## Troubleshooting

### Bot not responding

**Check logs:**
1. Go to ClawCloud dashboard
2. Click your app → Logs
3. Look for errors

**Common fixes:**
- Verify API key is correct
- Check `openai_base_url` is `https://openrouter.ai/api/v1`
- Restart the container

### Memory errors

The official template handles memory automatically. If using custom Docker:
- Increase RAM to 1024MB+
- Add `NODE_OPTIONS=--max-old-space-size=1024`

### Rate limits

Free OpenRouter tier has limits. Solutions:
- Wait and retry
- Add credits to OpenRouter account
- Use less intensive models

---

## Optional: Custom Configuration

Upload these files via ClawCloud file manager:
- `configs/clawdbot.json` - Agent settings
- `agents/AGENTS.md` - System prompt

---

## Free Model Options

| Model | Best For |
|-------|----------|
| `deepseek/deepseek-r1` | Reasoning, coding |
| `meta-llama/llama-3.3-70b-instruct` | General tasks |
| `google/gemma-3-27b-it` | Quick responses |
| `qwen/qwen3-4b` | Simple tasks |

---

## Support

- [OpenClaw Docs](https://openclaw.dev)
- [OpenRouter Docs](https://openrouter.ai/docs)
- [ClawCloud Docs](https://docs.claw.cloud)
