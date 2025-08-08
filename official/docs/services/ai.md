# 其他 AI 模型临时接入

## Ollama

- 从[官网](https://ollama.com/)下载安装 ollama
- MacOS
  - OLLAMA_ORIGINS="*" ollama serve（允许跨域访问并启动 ollama）
- Windows
  - 在控制面板 - 系统属性 - 环境变量 - 用户环境变量中新建变量名 "OLLAMA_HOST" 变量值 "0.0.0.0"，变量名 "OLLAMA_ORIGINS" 变量值 "*"
- 进入插件的[设置页面](https://dash.immersivetranslate.com/#general)，翻译服务选择 OpenAI
  - api_key: ollama
  - 自定义模型：llama2、[其他模型](https://ollama.com/library)
  - 自定义 URL 地址：http://localhost:11434/v1/chat/completions
- 相关参考文件
  - https://github.com/ollama/ollama/issues/2335

## Groq

- 进入插件的[设置页面](https://dash.immersivetranslate.com/#general)，翻译服务选择 OpenAI
  - api_key: 获取[api_key](https://console.groq.com/keys)
  - 自定义模型：mixtral-8x7b-32768、llama2-70b-4096
  - 自定义 URL 地址：https://api.groq.com/openai/v1/chat/completions
  - 速率限制：[20/分钟+25/10分钟](https://console.groq.com/docs/rate-limits)
  - 注意
    - 建议仅在鼠标悬停和输入增强功能处使用

## Claude

- Docker/Cloudflare 部署 [Claude to ChatGPT](https://github.com/jtsang4/claude-to-chatgpt)
- 进入插件的[设置页面](https://dash.immersivetranslate.com/#general)，翻译服务选择 OpenAI
  - api_key: 获取[api_key](https://www.nightfall.ai/ai-security-101/anthropic-claude-api-key)
  - 自定义模型：claude-instant-1、claude-2
  - 自定义 URL 地址：http://localhost:8000/v1/chat/completions
  - 频率限制见 [Rate Limits](https://docs.anthropic.com/claude/reference/rate-limits)
  - 注意
    - 注意出口 ip
    - 建议仅在鼠标悬停和输入增强功能处使用
