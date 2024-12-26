# 其他 AI 模型臨時接入

## Ollama

- 從[官網](https://ollama.com/)下載安裝 ollama
- MacOS
  - OLLAMA_ORIGINS="\*" ollama serve（允許跨域存取並啟動 ollama）
- Windows
  - 在控制面板 - 系統屬性 - 環境變數 - 使用者環境變數新建變數名"OLLAMA_HOST"變數值"0.0.0.0"，變數名"OLLAMA_ORIGINS"變數值"\*"
- 進入外掛的[設定頁面](https://dash.immersivetranslate.com/#general)，翻譯服務選擇 OpenAI
  - api_key: ollama
  - 自訂模型：llama2、[other models](https://ollama.com/library)
  - 自訂 URL 地址：http://localhost:11434/v1/chat/completions
- 相關參考文件
  - https://github.com/ollama/ollama/issues/2335

## Groq

- 進入外掛的[設定頁面](https://dash.immersivetranslate.com/#general)，翻譯服務選擇 OpenAI
  - api_key: 取得[api_key](https://console.groq.com/keys)
  - 自訂模型：mixtral-8x7b-32768、llama2-70b-4096
  - 自訂 URL 地址：https://api.groq.com/openai/v1/chat/completions
  - 速率控制：[20/min+25/10min](https://console.groq.com/docs/rate-limits)
  - 注意
    - 建議僅在滑鼠懸停和輸入增強功能處使用

## Claude
- Docker/Cloudflare 部署 [Claude to ChatGPT](https://github.com/jtsang4/claude-to-chatgpt)
- 進入外掛的[設定頁面](https://dash.immersivetranslate.com/#general)，翻譯服務選擇 OpenAI
  - api_key: 取得[api_key](https://www.nightfall.ai/ai-security-101/anthropic-claude-api-key)
  - 自訂模型：claude-instant-1、claude-2
  - 自訂 URL 地址：http://localhost:8000/v1/chat/completions
  - 頻率限制見 [Rate Limits](https://docs.anthropic.com/claude/reference/rate-limits)
  - 注意
    - 注意出口 ip
    - 建議僅在滑鼠懸停和輸入增強功能處使用
