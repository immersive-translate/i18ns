# Como implementar Outros Modelos de IA no Immersive Translate

## Ollama

1. **Instalação:**
   - Baixe e instale o Ollama a partir do [site oficial](https://ollama.com/).
   - **MacOS:** Execute `OLLAMA_ORIGINS="*" ollama serve` para permitir acesso de várias origens e iniciar o Ollama.
   - **Windows:**
     - Vá em "Painel de Controle" > "Propriedades do Sistema" > "Variáveis de Ambiente" > "Variáveis de Ambiente do Usuário".
     - Crie uma variável chamada `OLLAMA_HOST` com o valor `0.0.0.0`.
     - Crie outra variável chamada `OLLAMA_ORIGINS` com o valor `*`.

2. **Configuração no Immersive Translate:**
   - Na [página de configurações](https://dash.immersivetranslate.com/#general) do plugin, selecione "OpenAI" como serviço de tradução.
   - Preenchendo os campos:
     - api_key: ollama
     - Modelo personalizado: `llama2`, [Ou outros modelos disponíveis](https://ollama.com/library)
     - URL personalizada: `http://localhost:11434/v1/chat/completions`

**Referência:** [https://github.com/ollama/ollama/issues/2335](https://github.com/ollama/ollama/issues/2335)

## Groq

1. **Configuração no Immersive Translate:**
   - Na [página de configurações](https://dash.immersivetranslate.com/#general) do plugin, selecione "OpenAI" como serviço de tradução.
   - Preencha os campos:
     - api_key: `api_key` [Obtenha sua chave de API aqui](https://console.groq.com/keys).
     - Modelo personalizado: `mixtral-8x7b-32768, llama2-70b-4096`
     - URL personalizada: `https://api.groq.com/openai/v1/chat/completions`

2. **Limitações:**
   - **Controle de taxa:** [20/min+25/10min](https://console.groq.com/docs/rate-limits)
   - **Recomendação:** Utilize o Groq para os recursos de realce de entrada e "Passar o mouse".

## Claude

1. **Implementação:**
   - Utilize o projeto [Claude to ChatGPT](https://github.com/jtsang4/claude-to-chatgpt) para implementar o Claude no ChatGPT usando Docker/Cloudflare.

2. **Configuração no Immersive Translate:**
   - Na [página de configurações](https://dash.immersivetranslate.com/#general) do plugin, selecione "OpenAI" como serviço de tradução.
   - Preencha os campos:
     - api_key: `api_key` [Obtenha sua chave de API aqui](https://www.nightfall.ai/ai-security-101/anthropic-claude-api-key).
     - Modelo personalizado: `claude-instant-1, claude-2`
     - URL personalizada: `http://localhost:8000/v1/chat/completions`

3. **Observações:**
   - **Limites de taxa:** Consulte [https://docs.anthropic.com/claude/reference/rate-limits](https://docs.anthropic.com/claude/reference/rate-limits).
   - **IP de exportação:** Esteja ciente do seu IP de exportação.
   - **Recomendação:** Utilize o Claude para os recursos realce de entrada e "Passar o mouse".