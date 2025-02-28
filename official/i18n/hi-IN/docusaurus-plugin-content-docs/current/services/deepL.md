# DeepL

## [Immersive Translate Pro Membership](https://immersivetranslate.com/en/pricing/) खोलने के बाद DeepL अनुवाद सेवाओं तक सीधी पहुंच (अनुशंसित)

[अधिक जानें](https://immersivetranslate.com/en/pricing/)

## DeepL के माध्यम से आधिकारिक DeepL API प्राप्त करें

1. आधिकारिक परिचय: [DeepL API](https://www.deepl.com/en/pro#developer)

   - ध्यान दें कि: [DeepL API](https://www.deepl.com/en/pro#developer) और [DeepL Pro](https://www.deepl.com/pro) दो अलग-अलग खाता प्रकार हैं, और [DeepL API](https://www.deepl.com/en/pro/select-country#developer) खाता।

2. [क्यों](https://www.deepl.com/en/whydeepl) DeepL चुनें?

   - English ⇄ Chinese 5x अधिक सटीक
   - English ⇄ Japanese 6x अधिक सटीक
   - अनुवाद इंजन कृत्रिम बुद्धिमत्ता प्रौद्योगिकी (न्यूरल नेटवर्क) पर आधारित है

3. Deepl API को [Free API और Pro API](https://www.deepl.com/en/pro#developer) में विभाजित किया गया है

   - Free API प्रति माह 500,000 मुफ्त वर्ण प्रदान करता है।
   - Pro API के लिए [आधिकारिक शुल्क](https://www.deepl.com/en/pro#developer) है: $25 प्रति 1 मिलियन वर्ण।
   - एक उच्च-आवृत्ति उपयोगकर्ता के लिए, एक महीने में उपभोग किए गए वर्णों की मात्रा लगभग 10 मिलियन वर्ण है, और कीमत लगभग: 250 USD

4. एक खाता पंजीकृत करने और [DeepL API](https://www.deepl.com/en/pro#developer) खोलने के लिए।

## सामान्य समस्याएं

### 1. भरा गया कुंजी उपलब्ध नहीं है।

DeepL API Pro और DeepL Pro दो प्रकार के खाते हैं, Immersive Translate में उपयोग की जा सकने वाली Auth Key DeepL API खाता है, कृपया [DeepL API Pro](https://www.deepl.com/en/pro/select-country#) डेवलपर के लिए यहां क्लिक करें)

### 2. 401, 403 प्रमाणीकरण त्रुटियों का निवारण

ये त्रुटियाँ आमतौर पर तब होती हैं जब आप गलत प्रकार की प्रमाणीकरण कुंजी का उपयोग कर रहे होते हैं। कृपया ध्यान दें:

1. DeepL दो अलग-अलग उत्पाद प्रदान करता है: DeepL Pro (अनुवाद सेवा) और DeepL API (डेवलपर इंटरफ़ेस)
2. आपके DeepL Pro खाता सेटिंग्स में पाई गई कुंजियाँ API कॉल के साथ **संगत नहीं** हैं
3. API कुंजी प्राप्त करने के लिए आपको विशेष रूप से DeepL API खाता पंजीकृत करना होगा
4. DeepL Free API कुंजियाँ `:fx` के साथ समाप्त होने से पहचानी जाती हैं
5. DeepL Pro API कुंजियों में `:fx` प्रत्यय नहीं होता है और वे एक नियमित वर्णों की स्ट्रिंग के रूप में दिखाई देती हैं

कृपया सुनिश्चित करें कि आपने केवल DeepL Pro अनुवाद सेवा नहीं, बल्कि DeepL API सेवा के लिए सही तरीके से पंजीकरण किया है।

### 3. 456, उपयोगकर्ता के लिए कोटा पूरा हो गया है।

उपयोग ने DeepL की आधिकारिक हार्ड लिमिट कैप प्रति उपयोगकर्ता को पार कर लिया है, आपने DeepL की निष्पक्ष उपयोग नीति का उल्लंघन किया हो सकता है और आपको ऐसे व्यवहार से बचने की सलाह दी जाती है। यदि आप एक भुगतान किए गए ग्राहक हैं, तो उपयोग अगले महीने स्वचालित रूप से रीसेट हो जाएगा।