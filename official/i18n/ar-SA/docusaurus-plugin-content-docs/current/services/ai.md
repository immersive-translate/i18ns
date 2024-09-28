# دمج مؤقت لنماذج الذكاء الاصطناعي الأخرى

## أولاما

- قم بتنزيل وتثبيت أولاما من [الموقع الرسمي](https://ollama.com/)
- تشغيل `OLLAMA_ORIGINS="*" ollama serve` (يسمح بالوصول عبر الأصول ويبدأ أولاما)
- اذهب إلى [صفحة الإعدادات](https://dash.immersivetranslate.com/#general) للإضافة، واختر openAI لخدمة الترجمة
  - مفتاح api: ollama
  - نموذج مخصص: llama2، [نماذج أخرى](https://ollama.com/library)
  - عنوان URL مخصص: http://localhost:11434/v1/chat/completions
- وثائق مرجعية ذات صلة
  - https://github.com/ollama/ollama/issues/2335

## جروق

- اذهب إلى [صفحة الإعدادات](https://dash.immersivetranslate.com/#general) للإضافة، واختر openAI لخدمة الترجمة
  - مفتاح api: الحصول على [مفتاح api](https://console.groq.com/keys)
  - نموذج مخصص: mixtral-8x7b-32768, llama2-70b-4096
  - عنوان URL مخصص: https://api.groq.com/openai/v1/chat/completions
  - التحكم في المعدل: [20/دقيقة+25/10دقائق](https://console.groq.com/docs/rate-limits)
  - ملاحظة
    - يُنصح باستخدامه لميزات تحسين التحويم بالفأرة وإدخال البيانات فقط## كلود
- نشر كلود إلى ChatGPT باستخدام Docker/Cloudflare [كلود إلى ChatGPT](https://github.com/jtsang4/claude-to-chatgpt)
- اذهب إلى [صفحة الإعدادات](https://dash.immersivetranslate.com/#general) للإضافة، واختر openAI لخدمة الترجمة
  - api_key: احصل على [api_key](https://www.nightfall.ai/ai-security-101/anthropic-claude-api-key)
  - النموذج المخصص: claude-instant-1، claude-2
  - عنوان URL المخصص: http://localhost:8000/v1/chat/completions
  - انظر [الحدود القصوى للتردد](https://docs.anthropic.com/claude/reference/rate-limits) للتحقق من قيود التكرار
  - ملاحظات
    - كن على دراية بتصدير IP
    - يُنصح باستخدامه لميزات تحسين تمرير الماوس والإدخال فقط
