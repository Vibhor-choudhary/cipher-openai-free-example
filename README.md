# Cipher Starter Kit

This repo offers ready-to-use configs for Cipher—an agentic memory layer for AI assistants—using ONLY OpenRouter, Gemini, or Qwen for FREE completions and memory (NO OpenAI requirement!).

## 🚀 Quick Start

1. Clone this repo.
2. Edit `env.example` with your API keys, save as `.env`.
3. Choose and edit the `cipher.yml` that fits your needs:
   - For OpenRouter completions + Gemini embeddings: use `cipher.yml`.
   - For Qwen completions/embeddings via OpenRouter: use `cipher-qwen-openrouter.yml`.
   - For full Gemini setup: use `cipher-gemini-only.yml`.
4. Run Cipher:
```bash
cipher --mode mcp --agent ./cipher.yml
```
5. Connect your IDE/editor (VS Code, Cursor, etc.) via MCP or use Cipher CLI directly.

## 🛠 Included Files

| File                              | Purpose                                                        |
|------------------------------------|----------------------------------------------------------------|
| cipher.yml                         | OpenRouter for completions, Gemini for embeddings              |
| cipher-qwen-openrouter.yml         | Qwen for both completions & embeddings via OpenRouter          |
| cipher-gemini-only.yml             | Gemini for everything                                          |
| env.example                        | Template for API keys and vector store config                  |
| mcp.json.example                   | Example MCP config                                             |
| VECTOR_STORE.md                    | Quick guide on memory/vector DB setup                          |
| .gitignore                         | Protect your secrets                                           |

## 🔑 Getting API Keys

### OpenRouter
1. Visit [openrouter.ai](https://openrouter.ai/)
2. Sign up for a free account
3. Get your API key from the dashboard
4. Many models are completely free with generous limits

### Gemini
1. Visit [Google AI Studio](https://aistudio.google.com/)
2. Create a new API key
3. Enable the Gemini API in Google Cloud Console

### Qwen (via OpenRouter)
- Use the same OpenRouter API key
- Qwen models are available through OpenRouter's platform

## 🚀 Usage Examples

### Basic Setup
```bash
# Copy the example env file
cp env.example .env

# Edit with your actual API keys
nano .env

# Run Cipher with your chosen config
cipher --mode mcp --agent ./cipher.yml
```

### With Vector Store
```bash
# Start Qdrant locally
docker run -p 6333:6333 -p 6334:6334 qdrant/qdrant

# Update your .env with vector store settings
VECTOR_STORE_TYPE=qdrant
QDRANT_URL=http://localhost:6333
```

## 🎯 Benefits

- **No OpenAI dependency**: Use free alternatives
- **Multiple model options**: Choose what works best for you
- **Local or cloud memory**: Flexible storage options
- **Ready to use**: Just add your API keys and go
- **Open source**: Full transparency and customization

## 🤝 Contributing

Feel free to submit issues, feature requests, or pull requests to improve these configurations!

## 🙏 Credits

- Thanks to the Cipher open-source team and the global AI developer community!
- Inspired by the need for OpenAI-free AI development workflows

## 📄 License

MIT License - see LICENSE file for details. 