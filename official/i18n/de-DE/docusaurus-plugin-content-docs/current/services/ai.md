# Temporäre Integration anderer KI-Modelle

## Ollama
- Laden Sie ollama von der [offiziellen Website](https://ollama.com/) herunter und installieren Sie es
- Führen Sie `OLLAMA_ORIGINS="*" ollama serve` aus (erlaubt Zugriff von anderen Ursprüngen und startet ollama)
- Gehen Sie zur [Einstellungsseite](https://dash.immersivetranslate.com/#general) des Plugins und wählen Sie openAI als Übersetzungsdienst
    - api_key: ollama
    - Benutzerdefiniertes Modell: llama2, [andere Modelle](https://ollama.com/library)
    - Benutzerdefinierte URL: http://localhost:11434/v1/chat/completions
- Zugehörige Referenzdokumente
    - https://github.com/ollama/ollama/issues/2335

## Groq
- Gehen Sie zur [Einstellungsseite](https://dash.immersivetranslate.com/#general) des Plugins und wählen Sie openAI als Übersetzungsdienst
    - api_key: Erhalten Sie [api_key](https://console.groq.com/keys)
    - Benutzerdefiniertes Modell: mixtral-8x7b-32768, llama2-70b-4096
    - Benutzerdefinierte URL: https://api.groq.com/openai/v1/chat/completions
    - Rate Control: [20/min+25/10min](https://console.groq.com/docs/rate-limits)
    - Hinweis
        - Es wird empfohlen, dies nur für die Funktionen Mouse-Hover und Eingabeerweiterung zu verwenden

## Claude
- Einsatz von Claude in ChatGPT mit Docker/Cloudflare [Claude in ChatGPT](https://github.com/jtsang4/claude-to-chatgpt)
- Gehe zur [Einstellungsseite](https://dash.immersivetranslate.com/#general) des Plugins und wähle openAI als Übersetzungsdienst
    - api_key: Erhalte den [api_key](https://www.nightfall.ai/ai-security-101/anthropic-claude-api-key)
    - Benutzerdefiniertes Modell: claude-instant-1, claude-2
    - Benutzerdefinierte URL-Adresse: http://localhost:8000/v1/chat/completions
    - Siehe [Rate Limits](https://docs.anthropic.com/claude/reference/rate-limits) für Frequenzbeschränkungen
    - Hinweise
        - Beachte die Export-IP
        - Es wird empfohlen, dies nur für die Funktionen Mouseover und Eingabeerweiterung zu verwenden