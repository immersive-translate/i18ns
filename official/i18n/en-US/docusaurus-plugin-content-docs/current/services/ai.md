# Temporary Integration of Other AI Models

## Ollama

- Download and install ollama from the [official website](https://ollama.com/)
- MacOS
  - Run `OLLAMA_ORIGINS="*" ollama serve` (allows cross-origin access and starts ollama)
- Windows
  - In Control Panel - System Properties - Environment Variables - User Environment Variables, create a new variable name "OLLAMA_HOST" with the value "0.0.0.0", and a variable name "OLLAMA_ORIGINS" with the value "\*"
- Go to the [settings page](https://dash.immersivetranslate.com/#general) of the plugin, and select openAI for translation service
  - api_key: ollama
  - Custom model: llama2, [other models](https://ollama.com/library)
  - Custom URL: <http://localhost:11434/v1/chat/completions>
- Related reference documents
  - <https://github.com/ollama/ollama/issues/2335>

## Groq

- Go to the [settings page](https://dash.immersivetranslate.com/#general) of the plugin, and select openAI for translation service
  - api_key: Obtain [api_key](https://console.groq.com/keys)
  - Custom model: mixtral-8x7b-32768, llama2-70b-4096
  - Custom URL: <https://api.groq.com/openai/v1/chat/completions>
  - Rate control: [20/min+25/10min](https://console.groq.com/docs/rate-limits)
  - Note
    - It is recommended to use only for mouse hover and input enhancement features## Claude
- Deployment of Claude to ChatGPT using Docker/Cloudflare [Claude to ChatGPT](https://github.com/jtsang4/claude-to-chatgpt)
- Go to the [settings page](https://dash.immersivetranslate.com/#general) of the plugin, and select openAI for the translation service
  - api_key: Obtain the [api_key](https://www.nightfall.ai/ai-security-101/anthropic-claude-api-key)
  - Custom model: claude-instant-1, claude-2
  - Custom URL address: <http://localhost:8000/v1/chat/completions>
  - See [Rate Limits](https://docs.anthropic.com/claude/reference/rate-limits) for frequency limitations
  - Notes
    - Be aware of the export IP
    - It is recommended to use only for mouse hover and input enhancement features
