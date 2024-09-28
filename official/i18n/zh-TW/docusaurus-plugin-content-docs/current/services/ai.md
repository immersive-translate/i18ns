# 其他 AI 模型臨時接入

## Ollama

- 從[官網](https://ollama.com/)下載安裝 ollama
- MacOS
  - OLLAMA_ORIGINS="\*" ollama serve （允許跨域訪問並啟動ollama）
- Windows
  - 在控制面板-系統屬性-環境變量-用戶環境變量新建變量名"OLLAMA_HOST"變量值"0.0.0.0"，變量名"OLLAMA_ORIGINS"變量值"\*"
- 進入插件的[設置頁](https://dash.immersivetranslate.com/#general),翻譯服務選擇 openAI
  - api_key: ollama
  - 自定義模型: llama2 、[other models](https://ollama.com/library)
  - 自定義 URL 地址: http://localhost:11434/v1/chat/completions
- 相關參考文檔
  - https://github.com/ollama/ollama/issues/2335

## Groq

- 進入插件的[設置頁](https://dash.immersivetranslate.com/#general),翻譯服務選擇 openAI
  - api_key: 獲取[api_key](https://console.groq.com/keys)
  - 自定義模型: mixtral-8x7b-32768、llama2-70b-4096
  - 自定義 URL 地址: https://api.groq.com/openai/v1/chat/completions
  - 速率控制: [20/min+25/10min](https://console.groq.com/docs/rate-limits)
  - 注意
    - 建議僅在鼠標懸停和輸入增強功能處使用## Claude
- Docker/Cloudflare 部署 [Claude to ChatGPT](https://github.com/jtsang4/claude-to-chatgpt)
- 進入插件的[設置頁](https://dash.immersivetranslate.com/#general)，翻譯服務選擇 openAI
  - api_key: 獲取[api_key](https://www.nightfall.ai/ai-security-101/anthropic-claude-api-key)
  - 自定義模型: claude-instant-1、claude-2
  - 自定義 URL 地址: http://localhost:8000/v1/chat/completions
  - 頻率限制見 [Rate Limits](https://docs.anthropic.com/claude/reference/rate-limits)
  - 注意
    - 注意出口ip
    - 建議僅在鼠標懸停和輸入增強功能處使用
