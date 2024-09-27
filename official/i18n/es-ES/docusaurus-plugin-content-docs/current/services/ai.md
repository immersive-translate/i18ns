# Integración Temporal de Otros Modelos de IA

## Ollama

- Descargar e instalar ollama desde el [sitio oficial](https://ollama.com/)
- Ejecutar `OLLAMA_ORIGINS="*" ollama serve` (permite el acceso de origen cruzado e inicia ollama)
- Ir a la [página de configuración](https://dash.immersivetranslate.com/#general) del plugin, y seleccionar openAI para el servicio de traducción
  - api_key: ollama
  - Modelo personalizado: llama2, [otros modelos](https://ollama.com/library)
  - URL personalizada: <http://localhost:11434/v1/chat/completions>
- Documentos de referencia relacionados
  - <https://github.com/ollama/ollama/issues/2335>

## Groq

- Ir a la [página de configuración](https://dash.immersivetranslate.com/#general) del plugin, y seleccionar openAI para el servicio de traducción
  - api_key: Obtener [api_key](https://console.groq.com/keys)
  - Modelo personalizado: mixtral-8x7b-32768, llama2-70b-4096
  - URL personalizada: https://api.groq.com/openai/v1/chat/completions
  - Control de tasa: [20/min+25/10min](https://console.groq.com/docs/rate-limits)
  - Nota
    - Se recomienda usar solo para las funciones de mejora de entrada y de pasar el ratón por encima

## Claude

- Despliegue de Claude a ChatGPT usando Docker/Cloudflare [Claude a ChatGPT](https://github.com/jtsang4/claude-to-chatgpt)
- Ir a la [página de configuración](https://dash.immersivetranslate.com/#general) del plugin y seleccionar openAI para el servicio de traducción
  - api_key: Obtener la [api_key](https://www.nightfall.ai/ai-security-101/anthropic-claude-api-key)
  - Modelo personalizado: claude-instant-1, claude-2
  - Dirección URL personalizada: <http://localhost:8000/v1/chat/completions>
  - Ver [Límites de Frecuencia](https://docs.anthropic.com/claude/reference/rate-limits) para las limitaciones de frecuencia
  - Notas
    - Tener en cuenta la exportación de IP
    - Se recomienda usar solo para las funciones de mejora de pasar el ratón y entrada de datos
