# Integração Temporária de Outros Modelos de IA

## Ollama

- Faça o download e instale o ollama do [site oficial](https://ollama.com/)
- MacOS
 - Execute `OLLAMA_ORIGINS="*" ollama serve` (permite acesso de várias origens e inicia o ollama)
- Windows
 - No Painel de Controle - Propriedades do Sistema - Variáveis de Ambiente - Variáveis de Ambiente do Usuário, crie uma nova variável chamada "OLLAMA_HOST" com o valor "0.0.0.0" e uma variável chamada "OLLAMA_ORIGINS" com o valor "*"
- Acesse a [página de configurações](https://dash.immersivetranslate.com/#general) do plugin e selecione openAI como serviço de tradução
 - api_key: ollama
 - Modelo personalizado: llama2, [outros modelos](https://ollama.com/library)
 - URL personalizada: <http://localhost:11434/v1/chat/completions>
- Documentos de referência relacionados
 - [https://github.com/ollama/ollama/issues/2335](https://github.com/ollama/ollama/issues/2335)

## Groq

- Acesse a [página de configurações](https://dash.immersivetranslate.com/#general) do plugin e selecione openAI como serviço de tradução
 - api_key: Obtenha a [api_key](https://console.groq.com/keys)
 - Modelo personalizado: mixtral-8x7b-32768, llama2-70b-4096
 - URL personalizada: [https://api.groq.com/openai/v1/chat/completions](https://api.groq.com/openai/v1/chat/completions)
 - Controle de taxa: [20/min+25/10min](https://console.groq.com/docs/rate-limits)
 - Observação
  - Recomenda-se usar apenas para recursos de realce de entrada e Passar o mouse

## Claude

- Implantação do Claude no ChatGPT usando Docker/Cloudflare [Claude to ChatGPT](https://github.com/jtsang4/claude-to-chatgpt)
- Acesse a [página de configurações](https://dash.immersivetranslate.com/#general) do plugin e selecione openAI como serviço de tradução
 - api_key: Obtenha a [api_key](https://www.nightfall.ai/ai-security-101/anthropic-claude-api-key)
 - Modelo personalizado: claude-instant-1, claude-2
 - URL personalizada: <http://localhost:8000/v1/chat/completions>
 - Consulte [Limites de Taxa](https://docs.anthropic.com/claude/reference/rate-limits) para limitações de frequência
 - Observações
  - Esteja ciente do IP de exportação
  - Recomenda-se usar apenas para recursos de realce de entrada e Passar o mouse
