# अन्य AI मॉडल्स का अस्थायी एकीकरण

## ओल्लमा

- आधिकारिक वेबसाइट से ओल्लमा डाउनलोड और इंस्टॉल करें [आधिकारिक वेबसाइट](https://ollama.com/)
- `OLLAMA_ORIGINS="*"` ollama serve` चलाएँ (क्रॉस-ओरिजिन एक्सेस की अनुमति देता है और ओल्लमा को शुरू करता है)
- प्लगइन के [सेटिंग्स पेज](https://dash.immersivetranslate.com/#general) पर जाएं, और अनुवाद सेवा के लिए openAI का चयन करें
  - api_key: ओल्लमा
  - कस्टम मॉडल: लामा2, [अन्य मॉडल्स](https://ollama.com/library)
  - कस्टम URL: http://localhost:11434/v1/chat/completions
- संबंधित संदर्भ दस्तावेज़
  - https://github.com/ollama/ollama/issues/2335

## ग्रोक

- प्लगइन के [सेटिंग्स पेज](https://dash.immersivetranslate.com/#general) पर जाएं, और अनुवाद सेवा के लिए openAI का चयन करें
  - api_key: [api_key](https://console.groq.com/keys) प्राप्त करें
  - कस्टम मॉडल: mixtral-8x7b-32768, llama2-70b-4096
  - कस्टम URL: https://api.groq.com/openai/v1/chat/completions
  - रेट कंट्रोल: [20/मिन+25/10मिन](https://console.groq.com/docs/rate-limits)
  - नोट
    - केवल माउस होवर और इनपुट एन्हांसमेंट फीचर्स के लिए इसका उपयोग करने की सिफारिश की जाती है## क्लॉड
- क्लॉड को डॉकर/क्लाउडफ्लेयर का उपयोग करके ChatGPT में तैनाती [क्लॉड से ChatGPT तक](https://github.com/jtsang4/claude-to-chatgpt)
- प्लगइन के [सेटिंग्स पेज](https://dash.immersivetranslate.com/#general) पर जाएं, और अनुवाद सेवा के लिए openAI का चयन करें
  - api_key: [api_key](https://www.nightfall.ai/ai-security-101/anthropic-claude-api-key) प्राप्त करें
  - कस्टम मॉडल: claude-instant-1, claude-2
  - कस्टम URL पता: http://localhost:8000/v1/chat/completions
  - फ्रीक्वेंसी सीमाओं के लिए [रेट लिमिट्स](https://docs.anthropic.com/claude/reference/rate-limits) देखें
  - नोट्स
    - निर्यात आईपी के प्रति सचेत रहें
    - केवल माउस होवर और इनपुट वृद्धि सुविधाओं के लिए उपयोग करने की सिफारिश की जाती है
