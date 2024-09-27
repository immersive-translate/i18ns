# 他のAIモデルの一時的な接続

## Ollama

- [公式ウェブサイト](https://ollama.com/)からollamaをダウンロードしてインストールする
- OLLAMA_ORIGINS="\*" ollama serve（クロスオリジンアクセスを許可してollamaを起動）
- プラグインの[設定ページ](https://dash.immersivetranslate.com/#general)に入り、翻訳サービスでopenAIを選択
  - api_key: ollama
  - カスタムモデル: llama2、[その他のモデル](https://ollama.com/library)
  - カスタムURLアドレス: http://localhost:11434/v1/chat/completions
- 関連する参考文献
  - https://github.com/ollama/ollama/issues/2335

## Groq

- プラグインの[設定ページ](https://dash.immersivetranslate.com/#general)に入り、翻訳サービスでopenAIを選択
  - api_key: [api_key](https://console.groq.com/keys)を取得
  - カスタムモデル: mixtral-8x7b-32768、llama2-70b-4096
  - カスタムURLアドレス: https://api.groq.com/openai/v1/chat/completions
  - レート制限: [20/min+25/10min](https://console.groq.com/docs/rate-limits)
  - 注意
    - マウスホバーと入力強化機能での使用を推奨

## クロード

- Docker/Cloudflare を使用して [Claude to ChatGPT](https://github.com/jtsang4/claude-to-chatgpt) をデプロイ
- プラグインの[設定ページ](https://dash.immersivetranslate.com/#general)にアクセスし、翻訳サービスに openAI を選択
  - api_key: [api_key](https://www.nightfall.ai/ai-security-101/anthropic-claude-api-key) を取得
  - カスタムモデル: claude-instant-1、claude-2
  - カスタムURLアドレス: http://localhost:8000/v1/chat/completions
  - 頻度制限については [Rate Limits](https://docs.anthropic.com/claude/reference/rate-limits) を参照
  - 注意事項
    - 出口IPに注意
    - マウスホバーと入力強化機能での使用を推奨
