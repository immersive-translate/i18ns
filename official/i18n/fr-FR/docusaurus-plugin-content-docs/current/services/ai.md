# Intégration temporaire d'autres modèles d'IA

## Ollama
- Téléchargez et installez ollama depuis le [site officiel](https://ollama.com/)
- Exécutez `OLLAMA_ORIGINS="*" ollama serve` (permet l'accès cross-origin et démarre ollama)
- Allez à la [page de paramètres](https://dash.immersivetranslate.com/#general) du plugin, et sélectionnez openAI pour le service de traduction
    - clé_api : ollama
    - Modèle personnalisé : llama2, [autres modèles](https://ollama.com/library)
    - URL personnalisée : http://localhost:11434/v1/chat/completions
- Documents de référence associés
    - https://github.com/ollama/ollama/issues/2335

## Groq
- Allez à la [page de paramètres](https://dash.immersivetranslate.com/#general) du plugin, et sélectionnez openAI pour le service de traduction
    - clé_api : Obtenez [clé_api](https://console.groq.com/keys)
    - Modèle personnalisé : mixtral-8x7b-32768, llama2-70b-4096
    - URL personnalisée : https://api.groq.com/openai/v1/chat/completions
    - Contrôle de la fréquence : [20/min+25/10min](https://console.groq.com/docs/rate-limits)
    - Note
        - Il est recommandé de l'utiliser uniquement pour les fonctionnalités d'amélioration du survol de la souris et de saisie

## Claude
- Déploiement de Claude vers ChatGPT en utilisant Docker/Cloudflare [Claude vers ChatGPT](https://github.com/jtsang4/claude-to-chatgpt)
- Aller à la [page des paramètres](https://dash.immersivetranslate.com/#general) du plugin, et sélectionner openAI pour le service de traduction
    - api_key : Obtenir la [clé API](https://www.nightfall.ai/ai-security-101/anthropic-claude-api-key)
    - Modèle personnalisé : claude-instant-1, claude-2
    - Adresse URL personnalisée : http://localhost:8000/v1/chat/completions
    - Voir les [Limites de Fréquence](https://docs.anthropic.com/claude/reference/rate-limits) pour les limitations de fréquence
    - Notes
        - Être conscient de l'exportation IP
        - Il est recommandé de l'utiliser uniquement pour les fonctionnalités d'amélioration du survol de la souris et de saisie