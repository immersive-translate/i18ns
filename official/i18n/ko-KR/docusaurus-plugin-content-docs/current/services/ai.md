# 기타 AI 모델 임시 접속

## Ollama
- [공식 웹사이트](https://ollama.com/)에서 ollama 다운로드 및 설치
- OLLAMA_ORIGINS="*" ollama serve (크로스 도메인 액세스 허용 및 ollama 시작)
- 플러그인의 [설정 페이지](https://dash.immersivetranslate.com/#general)로 이동, 번역 서비스로 openAI 선택
    - api_key: ollama
    - 사용자 정의 모델: llama2, [기타 모델](https://ollama.com/library)
    - 사용자 정의 URL 주소: http://localhost:11434/v1/chat/completions
- 관련 참고 문서
    - https://github.com/ollama/ollama/issues/2335

## Groq
- 플러그인의 [설정 페이지](https://dash.immersivetranslate.com/#general)로 이동, 번역 서비스로 openAI 선택
    - api_key: [api_key](https://console.groq.com/keys) 획득
    - 사용자 정의 모델: mixtral-8x7b-32768, llama2-70b-4096
    - 사용자 정의 URL 주소: https://api.groq.com/openai/v1/chat/completions
    - 속도 제한: [20/min+25/10min](https://console.groq.com/docs/rate-limits)
    - 주의
        - 마우스 호버와 입력 강화 기능에서만 사용을 권장합니다.

## 클로드
- Docker/Cloudflare를 사용하여 [클로드 to ChatGPT](https://github.com/jtsang4/claude-to-chatgpt) 배포
- 플러그인의 [설정 페이지](https://dash.immersivetranslate.com/#general)에 접속하여, 번역 서비스로 openAI 선택
    - api_key: [api_key](https://www.nightfall.ai/ai-security-101/anthropic-claude-api-key) 획득
    - 사용자 정의 모델: claude-instant-1, claude-2
    - 사용자 정의 URL 주소: http://localhost:8000/v1/chat/completions
    - 요청 제한은 [Rate Limits](https://docs.anthropic.com/claude/reference/rate-limits) 참조
    - 주의사항
        - 출구 IP 주의
        - 마우스 호버와 입력 강화 기능에서만 사용을 권장