# Другие временные подключения моделей AI

## Ollama

- Скачайте и установите ollama с [официального сайта](https://ollama.com/)
- OLLAMA_ORIGINS="\*" ollama serve (разрешает кросс-доменный доступ и запускает ollama)
- Перейдите на [страницу настроек](https://dash.immersivetranslate.com/#general) плагина, выберите сервис перевода openAI
  - api_key: ollama
  - Пользовательская модель: llama2, [другие модели](https://ollama.com/library)
  - Пользовательский URL-адрес: http://localhost:11434/v1/chat/completions
- Ссылки для справки
  - https://github.com/ollama/ollama/issues/2335

## Groq

- Перейдите на [страницу настроек](https://dash.immersivetranslate.com/#general) плагина, выберите сервис перевода openAI
  - api_key: получить [api_key](https://console.groq.com/keys)
  - Пользовательская модель: mixtral-8x7b-32768, llama2-70b-4096
  - Пользовательский URL-адрес: https://api.groq.com/openai/v1/chat/completions
  - Контроль скорости: [20/мин+25/10мин](https://console.groq.com/docs/rate-limits)
  - Внимание
    - Рекомендуется использовать только при наведении курсора и улучшении ввода## Клод
- Развертывание в Docker/Cloudflare [Клод для ChatGPT](https://github.com/jtsang4/claude-to-chatgpt)
- Перейдите на [страницу настроек](https://dash.immersivetranslate.com/#general) плагина, выберите сервис перевода openAI
  - api_key: Получить [api_key](https://www.nightfall.ai/ai-security-101/anthropic-claude-api-key)
  - Пользовательская модель: claude-instant-1, claude-2
  - Пользовательский URL-адрес: http://localhost:8000/v1/chat/completions
  - Ограничения по частоте запросов смотрите в [Rate Limits](https://docs.anthropic.com/claude/reference/rate-limits)
  - Внимание
    - Обратите внимание на IP-адрес выхода
    - Рекомендуется использовать только при наведении курсора и для улучшения ввода
