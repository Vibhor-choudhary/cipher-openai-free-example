# 🚀 Quick Start Guide

Get Cipher running with OpenAI-free alternatives in under 5 minutes!

## 1. Get Your API Keys

### OpenRouter (Free!)
- Visit [openrouter.ai](https://openrouter.ai/)
- Sign up (free)
- Copy your API key

### Gemini (Free tier available)
- Visit [Google AI Studio](https://aistudio.google.com/)
- Create API key
- Enable Gemini API

## 2. Setup

```bash
# Clone this repo
git clone https://github.com/Vibhor-choudhary/cipher-starter-kit.git
cd cipher-starter-kit

# Copy and edit environment file
cp env.example .env
# Edit .env with your actual API keys
```

## 3. Choose Your Config

**Option A: OpenRouter + Gemini (Recommended)**
```bash
cp cipher.yml ~/.cipher.yml
```

**Option B: Qwen via OpenRouter**
```bash
cp cipher-qwen-openrouter.yml ~/.cipher.yml
```

**Option C: Gemini Only**
```bash
cp cipher-gemini-only.yml ~/.cipher.yml
```

## 4. Run Cipher

```bash
# Install Cipher if you haven't
npm install -g @cipher-ai/cli

# Start Cipher
cipher --mode mcp --agent ~/.cipher.yml
```

## 5. Connect to Your Editor

Add to your editor's MCP config:
```json
{
  "mcpServers": {
    "cipher-memory": {
      "url": "http://localhost:8080"
    }
  }
}
```

That's it! You now have a fully functional Cipher setup without OpenAI! 🎉 