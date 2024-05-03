# Integração Temporária de Outros Modelos de IA

## Ollama
- Baixe e instale o ollama a partir do [site oficial](https://ollama.com/)
- Execute `OLLAMA_ORIGINS="*" ollama serve` (permite acesso de origens cruzadas e inicia o ollama)
- Vá para a [página de configurações](https://dash.immersivetranslate.com/#general) do plugin e selecione openAI para o serviço de tradução
    - api_key: ollama
    - Modelo personalizado: llama2, [outros modelos](https://ollama.com/library)
    - URL personalizada: http://localhost:11434/v1/chat/completions
- Documentos de referência relacionados
    - https://github.com/ollama/ollama/issues/2335

## Groq
- Vá para a [página de configurações](https://dash.immersivetranslate.com/#general) do plugin e selecione openAI para o serviço de tradução
    - api_key: Obtenha [api_key](https://console.groq.com/keys)
    - Modelo personalizado: mixtral-8x7b-32768, llama2-70b-4096
    - URL personalizada: https://api.groq.com/openai/v1/chat/completions
    - Controle de frequência: [20/min+25/10min](https://console.groq.com/docs/rate-limits)
    - Nota
        - É recomendado usar apenas para recursos de realce de mouse hover e entrada de texto## Claude
- Implantação do Claude no ChatGPT usando Docker/Cloudflare [Claude para ChatGPT](https://github.com/jtsang4/claude-to-chatgpt)
- Acesse a [página de configurações](https://dash.immersivetranslate.com/#general) do plugin e selecione openAI para o serviço de tradução
    - api_key: Obtenha a [api_key](https://www.nightfall.ai/ai-security-101/anthropic-claude-api-key)
    - Modelo personalizado: claude-instant-1, claude-2
    - Endereço URL personalizado: http://localhost:8000/v1/chat/completions
    - Veja os [Limites de Frequência](https://docs.anthropic.com/claude/reference/rate-limits) para limitações de frequência
    - Notas
        - Esteja ciente do IP de exportação
        - É recomendado usar apenas para recursos de realce de mouse hover e entrada