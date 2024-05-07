# 其他 AI 模型临时接入

## Ollama
- 从[官网](https://ollama.com/)下载安装 ollama 
- OLLAMA_ORIGINS="*" ollama serve （允许跨域访问并启动ollama）
- 进入插件的[设置页](https://dash.immersivetranslate.com/#general),翻译服务选择 openAI
    - api_key: ollama
    - 自定义模型: llama2 、[other models](https://ollama.com/library)
    - 自定义 URL 地址: http://localhost:11434/v1/chat/completions
- 相关参考文档
    - https://github.com/ollama/ollama/issues/2335

## Groq
- 进入插件的[设置页](https://dash.immersivetranslate.com/#general),翻译服务选择 openAI
    - api_key: 获取[api_key](https://console.groq.com/keys)
    - 自定义模型: mixtral-8x7b-32768、llama2-70b-4096
    - 自定义 URL 地址: https://api.groq.com/openai/v1/chat/completions
    - 速率控制: [20/min+25/10min](https://console.groq.com/docs/rate-limits)
    - 注意
        - 建议仅在鼠标悬停和输入增强功能处使用