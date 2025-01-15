# DeepL

## DeepL अनुवाद सेवाओं तक सीधी पहुँच [इमर्सिव ट्रांसलेट प्रो सदस्यता](https://immersivetranslate.com/en/pricing/) खोलने के बाद (अनुशंसित)

[प्रस्तुतिकरण के लिए यहाँ क्लिक करें](https://immersivetranslate.com/en/pricing/)

## DeepL के माध्यम से आधिकारिक DeepL API प्राप्त करें

1. आधिकारिक परिचय:[DeepL API](https://www.deepl.com/en/pro#developer)

   - ध्यान दें कि: [DeepL API](https://www.deepl.com/en/pro#developer) और [DeepL Pro](https://www.deepl.com/pro) दो अलग-अलग खाता प्रकार हैं, और [DeepL API](https://www.deepl.com/en/pro/select-country#developer) खाता।

2. [क्यों](https://www.deepl.com/en/whydeepl) DeepL चुनें?

   - अंग्रेजी ⇄ चीनी 5x अधिक सटीक
   - अंग्रेजी ⇄ जापानी 6x अधिक सटीक
   - कृत्रिम बुद्धिमत्ता प्रौद्योगिकी (न्यूरल नेटवर्क) पर आधारित अनुवाद इंजन

3. Deepl API को [निःशुल्क API और प्रो API](https://www.deepl.com/en/pro#developer) में विभाजित किया गया है

   - निःशुल्क API प्रति माह 500,000 मुफ्त वर्ण प्रदान करता है।
   - प्रो API के लिए [आधिकारिक शुल्क](https://www.deepl.com/en/pro#developer) है: 1 मिलियन वर्णों के लिए $25।
   - एक उच्च-आवृत्ति उपयोगकर्ता के लिए, एक महीने में उपभोग किए गए वर्णों की मात्रा लगभग 10 मिलियन वर्ण है, और मूल्य लगभग है: 250 USD

4. एक खाता पंजीकृत करने और [DeepL API](https://www.deepl.com/en/pro#developer) खोलने के लिए।

<!--## अपना खुद का DeepL API बनाएं

हम अपनी DeeplX सेवा के लिए समर्थन का प्रयोग कर रहे हैं बीटा फीचर में (लेकिन यह वेब अनुवाद सेवा के रूप में उपयुक्त नहीं है, जैसा कि परीक्षण किया गया है। वेब पेज अनुवाद के लिए API अनुरोधों की विशाल मात्रा के कारण, यदि आप इस सेवा का निर्माण करते हैं, तो कृपया सुनिश्चित करें कि लोड बैलेंसिंग का अच्छा काम करें), निम्नलिखित निर्देशों के अनुसार प्रयोगात्मक फीचर्स को चालू कैसे करें:

1. डेवलपर सेटिंग्स में बीटा परीक्षण फीचर्स को सक्षम करें
2. बेसिक सेटिंग्स में DeepLX (बीटा) ढूंढें और स्व-निर्मित DeepL API URL दर्ज करें, उदा. http\://your-domain/translate

> प्रश्न: मैं अपना खुद का कैसे बनाऊं?
>
> उ: [OwO-Network/DeepLX](https://github.com/OwO-Network/DeepLX#setup-on-immersive-translate) या [zu1k/deepl](https://github.com/KyleChoy/zotero-pdf-translate/blob/CustomDeepL/README.md) -->

## सामान्य समस्याएं

### 1. भरी गई कुंजी उपलब्ध नहीं है।

DeepL API Pro और DeepL Pro दो प्रकार के खाते हैं, Immersive Translate में उपयोग की जा सकने वाली Auth Key DeepL API खाता है, कृपया यहाँ क्लिक करें [DeepL API Pro](https://www.deepl.com/en/pro/select-country#) डेवलपर के लिए)

### 2. Deepl Free API संकेत 401 कोई विशेषाधिकार नहीं

Deepl Free API कुंजियाँ सभी `:fx` में समाप्त होती हैं, कुछ और Free API कुंजी नहीं है।

### 3. 456, उपयोगकर्ता के लिए कोटा पहुँच गया है।

उपयोग DeepL की आधिकारिक कठिन सीमा प्रति उपयोगकर्ता से अधिक हो गया है, आपने DeepL की उचित उपयोग नीति का उल्लंघन किया हो सकता है और ऐसे व्यवहार से बचने की सलाह दी जाती है। यदि आप एक भुगतान किए गए ग्राहक हैं, तो उपयोग अगले महीने स्वतः ही रीसेट हो जाएगा।
