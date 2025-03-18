# Translation Services API Request

Immersive Translate Extension कई translation सेवाओं का समर्थन करता है, इनमें से कुछ का उपयोग करने से पहले आपको संबंधित सेवा की API key के लिए आवेदन करना होगा। मैंने वेब से सेवाओं के लिए निम्नलिखित आवेदन ट्यूटोरियल संकलित किए हैं, यदि कोई चूक या समय पर अपडेट नहीं है, तो कृपया इन पृष्ठों को संपादित करने के लिए ऊपर दाएं कोने पर क्लिक करें।

Translation Service API से संबंधित चर्चाएं [यहां](https://github.com/immersive-translate/immersive-translate/issues/137) आयोजित की जा सकती हैं।

## Interpretation Service

1. [Deepl](./services/deepL.md)
2. [Caiyun Xiaoyi](./services/caiyun.md)
3. [Tencent Translator](./services/tencent.md)
4. [Volcano Engine](./services/volcano.md)
5. [Baidu Translate](./services/baidu.md)
6. [OpenL](./services/openL.md)
7. [Niu Translation](./services/niu.md)
8. [Youdao Translator](./services/youdao.md)
9. [Youdao Ziyue LLM Translator](./services/youdao-ziyue.md)
10. [Microsoft Translate](./services/azure.md)

## जिम्मेदारी से इनकार या सीमित करने का बयान

उपरोक्त सभी translation सेवा शुल्क सेवा प्रदाता द्वारा लिया जाता है और इस एक्सटेंशन से कोई संबंध नहीं है।

कृपया अप्रत्याशित चार्जबैक से बचने के लिए प्रत्येक सेवा प्रदाता की मुफ्त राशि पर ध्यान दें।

## वर्णों की संख्या पर एक संक्षिप्त नोट

वर्णों की संख्या का गणना अनुवादित स्रोत भाषा में वर्णों की लंबाई के आधार पर की जाती है। स्पेस, विराम चिह्न, आदि को वर्णों के रूप में गिना जाता है। अधिकांश सेवाओं के लिए एक चीनी वर्ण, अंग्रेजी अक्षर, विराम चिह्न, लाइन ब्रेक, आदि को एक वर्ण के रूप में गिना जाता है। उदाहरण के लिए, मस्क के इस ट्वीट में 32 शब्द और 196 वर्ण हैं।

> स्पष्ट होने के लिए, मैं ऐसा व्यक्ति नहीं हूं जो सोचता है कि बहुत सी सरकारी एजेंसियों को समाप्त कर दिया जाना चाहिए (शायद कुछ), लेकिन हमें हमेशा अपने संस्थानों पर सवाल उठाना चाहिए, क्योंकि यह लोकतंत्र की नींव को मजबूत करता है।

ऐसा लंबा लेख जो पढ़ने में कठिन लगता है: [Algorithms Unlocked: How They're Shaping Our Everyday Lives | by Two Techie Vibes | Jan, 2023 | Medium](https://twotechievibes.medium.com/algorithms-unlocked-how-they're-shaping-our-everyday-lives-6261fa1dbad), जो लगभग 10,000 वर्ण लंबा है।

मुझे उम्मीद है कि ये दो उदाहरण आपको वर्ण गणना का एक अंदाजा देंगे।