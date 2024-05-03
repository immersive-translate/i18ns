# Integrazione Temporanea di Altri Modelli di Intelligenza Artificiale

## Ollama
- Scaricare e installare ollama dal [sito ufficiale](https://ollama.com/)
- Eseguire `OLLAMA_ORIGINS="*" ollama serve` (permette l'accesso cross-origin e avvia ollama)
- Andare alla [pagina delle impostazioni](https://dash.immersivetranslate.com/#general) del plugin e selezionare openAI per il servizio di traduzione
    - api_key: ollama
    - Modello personalizzato: llama2, [altri modelli](https://ollama.com/library)
    - URL personalizzato: http://localhost:11434/v1/chat/completions
- Documenti di riferimento correlati
    - https://github.com/ollama/ollama/issues/2335

## Groq
- Andare alla [pagina delle impostazioni](https://dash.immersivetranslate.com/#general) del plugin e selezionare openAI per il servizio di traduzione
    - api_key: Ottenere [api_key](https://console.groq.com/keys)
    - Modello personalizzato: mixtral-8x7b-32768, llama2-70b-4096
    - URL personalizzato: https://api.groq.com/openai/v1/chat/completions
    - Controllo della frequenza: [20/min+25/10min](https://console.groq.com/docs/rate-limits)
    - Nota
        - Si raccomanda di utilizzarlo solo per le funzionalità di miglioramento del passaggio del mouse e dell'input## Claude
- Distribuzione di Claude su ChatGPT utilizzando Docker/Cloudflare [Claude su ChatGPT](https://github.com/jtsang4/claude-to-chatgpt)
- Vai alla [pagina delle impostazioni](https://dash.immersivetranslate.com/#general) del plugin e seleziona openAI per il servizio di traduzione
    - api_key: Ottieni la [api_key](https://www.nightfall.ai/ai-security-101/anthropic-claude-api-key)
    - Modello personalizzato: claude-instant-1, claude-2
    - Indirizzo URL personalizzato: http://localhost:8000/v1/chat/completions
    - Vedi [Limiti di frequenza](https://docs.anthropic.com/claude/reference/rate-limits) per le limitazioni di frequenza
    - Note
        - Prestare attenzione all'export IP
        - Si raccomanda di utilizzarlo solo per le funzionalità di miglioramento al passaggio del mouse e di input