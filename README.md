# OpenClaw Config

Your personal AI assistant deployed on ClawCloud with OpenRouter.

[![Run on ClawCloud](https://raw.githubusercontent.com/ClawCloud/Run-Template/refs/heads/main/Run-on-ClawCloud.svg)](https://template.run.claw.cloud/?openapp=system-fastdeploy%3FtemplateName%3Dopenclaw)

## 🚀 Quick Start (3 Steps)

### Step 1: Get OpenRouter API Key (Free)
1. Go to [openrouter.ai](https://openrouter.ai)
2. Sign up with GitHub (free, no credit card)
3. Copy your API key: `sk-or-v1-xxxxx`

### Step 2: Deploy on ClawCloud
Click the **"Run on ClawCloud"** button above, then fill in:

| Field | Value |
|-------|-------|
| `openai_base_url` | `https://openrouter.ai/api/v1` |
| `openai_api_key` | Your OpenRouter API key |
| `openai_model` | `deepseek/deepseek-r1` (free) |

### Step 3: Add Telegram Bot
1. Chat with [@BotFather](https://t.me/BotFather) on Telegram
2. Create new bot: `/newbot`
3. Copy the token and add it to ClawCloud config

## 📋 Environment Variables

For manual deployment, use these environment variables:

```env
# LLM Provider (OpenRouter)
OPENROUTER_API_KEY=sk-or-v1-your-key
LLM_PROVIDER=openrouter
LLM_MODEL=deepseek/deepseek-r1

# Telegram
TELEGRAM_BOT_TOKEN=your-bot-token

# Gateway
CLAWDBOT_GATEWAY_TOKEN=your-secure-token
```

## 🆓 Free Models (via OpenRouter)

| Model | Quality | Speed |
|-------|---------|-------|
| `deepseek/deepseek-r1` | ⭐⭐⭐⭐ | Medium |
| `meta-llama/llama-3.3-70b-instruct` | ⭐⭐⭐⭐ | Fast |
| `google/gemma-3-27b-it` | ⭐⭐⭐ | Fast |

## 📁 Repository Structure

```
├── configs/
│   ├── clawdbot.json    # Agent settings + cost optimization
│   ├── telegram.yaml    # Telegram channel config
│   └── gateway.yaml     # Gateway settings
├── agents/
│   └── AGENTS.md        # System prompt / personality
└── docs/
    └── DEPLOYMENT.md    # Detailed guide
```

## 💡 Tips

- **Cost optimization**: Config includes 97% cost savings settings
- **Auto-approve**: Add your Telegram ID to skip manual pairing
- **Memory**: Uses ByteRover for persistent memory (optional)

## 📚 Documentation

- [Detailed Deployment Guide](docs/DEPLOYMENT.md)
- [OpenClaw Official Docs](https://openclaw.dev)
- [OpenRouter Models](https://openrouter.ai/models)

---

Made with 🦞 OpenClaw
