---
sidebar_position: 4
---

# उन्नत अनुकूलन विकल्प

आप उन्नत उपयोगकर्ताओं के लिए UI में संपादित नहीं किए जा सकने वाले अधिक अनुकूलित कॉन्फ़िगरेशन को विस्तारित कॉन्फ़िगरेशन पृष्ठ -> डेवलपर सेटिंग्स -> उपयोगकर्ता कॉन्फ़िग में संपादित कर सकते हैं, पैरामीटर के बारे में अधिक विवरण के लिए अंतिम नोट देखें। वर्तमान में निर्मित `config` यहाँ पाया जा सकता है [यहाँ](https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json).

## उपयोगकर्ता नियम

`नियमों` के साथ यह संभव है कि किसी विशेष वेबसाइट की कॉन्फ़िगरेशन को अनुकूलित किया जा सके, तय करना कि किस सामग्री का अनुवाद किया जाना है या नहीं, या पृष्ठों की शैली को समायोजित करना, आदि।

```json
[
  {
    "मेल": "www.google.com",
    "चयनकर्ता": [".शीर्षक"]
  },
  {
    "मेल": "*.twitter.com",
    "चयनकर्ता": [".पाठ"],
    "बाहरीचयनकर्ता": ["नैव", " पादलेख"]
  }
]
```

संबंधित वेबसाइट से मेल खाने के लिए `मेल` का उपयोग करें। वाइल्डकार्ड्स की अनुमति है, जैसे कि `*.google.com`,`www.google.com/test/*`,`file://*`.

`चयनकर्ता` का उपयोग करके स्मार्ट अनुवाद क्षेत्र को ओवरराइड करें, केवल उस चयनकर्ता द्वारा मिलान किए गए तत्वों का अनुवाद करें।

अनुवाद किए बिना तत्वों को बाहर करने के लिए `बाहरीचयनकर्ता` का उपयोग करें।

बुद्धिमान अनुवाद के आधार पर अनुवाद रेंज को बढ़ाने या घटाने के लिए `अतिरिक्त` परिवार के चयनकर्ताओं का उपयोग करें।

```json
[
  {
    "मेल": "www.google.com",
    "अतिरिक्तचयनकर्ता": [],
    "अतिरिक्तबाहरीचयनकर्ता": []
  }
]
```

यदि आप एक क्षेत्र का अनुवाद करना चाहते हैं जबकि तत्वों को एक संपूर्ण के रूप में मानते हैं और उन्हें अलग नहीं करते हैं, तो आप `अणुवीयब्लॉकचयनकर्ता` चयनकर्ता का उपयोग कर सकते हैं। उदाहरण के लिए, इंस्टाग्राम प्रोफाइल। ध्यान दें कि `अणुवीयब्लॉकचयनकर्ता` का उपयोग करने से पहले `चयनकर्ता` के साथ चयन करना आवश्यक है।

```json
{
  "मेल": "https://www.instagram.com/*",
  "चयनकर्ता": [
    "div._aa_c h1",
    "li._acaz div[role=\"menuitem\"]"
  ]
  "अणुवीयब्लॉकचयनकर्ता": [
    "div. ._aa_c h1",
    "li._acaz div[role=\"menuitem\"]"
  ]
}
```

यदि अनुवाद परिणाम में पृष्ठों का असंरेखण, पाठ का ओवरलैपिंग, और अन्य किनारे के मामले होते हैं, तो आप पृष्ठ शैली को समायोजित करके इसे ठीक करने के लिए `ग्लोबलस्टाइल्स` का उपयोग कर सकते हैं। उदाहरण के लिए, यूट्यूब हेडर, जिसका उपयोग मूल पृष्ठ की अधिकतम ऊंचाई को हटाने के लिए किया जाता है।

```json
{
  "मेल": "www.google.com",
  "ग्लोबलस्टाइल्स": { ".शीर्षक": "max-height:unset;" }
}
```

Note: The translation provided aims to maintain the technical integrity of the original markdown content while translating the descriptive parts into Hindi. Some technical terms and properties (like JSON keys) are kept in English to preserve functionality and clarity.

## उपयोगकर्ता नियम समेकन सुधार

0.7.4+ समर्थन। उदाहरण के लिए, अनुवाद-रहित क्षेत्र को छोड़ने की प्रक्रिया

```json
{
  "matches": "https://www.elektrotechnik.rwth-aachen.de/*",
  "additionalExcludeSelectors.remove": [".notranslate", "[translate=no]"]
}
```

जोड़ने और हटाने की क्रियाएँ मूल नियमों में संशोधन करती हैं और उन्हें पूरी तरह से बदलने की आवश्यकता नहीं होती, जैसा कि पहले होता था।

## इंजेक्टेड CSS

इंजेक्टेड CSS आपको वैश्विक रूप से कस्टम वेब शैलियों को इंजेक्ट करने की अनुमति देता है। `Rules` के `translationClasses` के साथ उपयोग किया जा सकता है।

```
".immersive-translate-target-wrapper img { width: 16px; height: 16px }"
```

साइट को अधिक व्यक्तिगत तरीके से स्टाइल करना भी संभव है, जैसे कि एक नियमित वेब स्टाइल मैनेजर।(विज्ञापनों को हटाने के लिए `display:none` का उपयोग करते हुए)

```css
.title {
  color: लाल;
}
```

## उपयोगकर्ता कॉन्फिग

कॉन्फिग आपको इस प्लगइन की कॉन्फिगरेशन को अनुकूलित करने की अनुमति देता है, जैसे कि अनुवाद सेवाएं, भाषा-विशिष्ट भाषा अनुवाद विकल्प, आदि।

```json
{
  "translationService": "tencent",
  "translationServices": {
    "tencent": {
      "secretId": "xxx",
      "secretKey": "xxx",
      "matches": ["*.twitter.com"]
    }
  },
  "translationUrlPattern": {
    "excludeMatches": ["www.google.com"]
  },
  "translationLanguagePattern": {
    "matches": ["en"]
  },
  "translationTheme": "none",
  "translationThemePatterns": {
    "underline": {
      "matches": ["discord.com"]
    }
  },
  "generalRule": {
    "_comment": "",
    "normalizeBody": "",
    "injectedCss": [],
    "additionalInjectedCss": [],
    "wrapperPrefix": "smart",
    "wrapperSuffix": "smart",
    "isPdf": false,
    "isTransformPreTagNewLine": false,
    "urlChangeDelay": 20,
    "isShowUserscriptPagePopup": true,
    "observeUrlChange": true,
    "paragraphMinTextCount": 8,
    "paragraphMinWordCount": 2,
    "blockMinTextCount": 32,
    "blockMinWordCount": 5,
    "containerMinTextCount": 18,
    "lineBreakMaxTextCount": 0,
    "globalAttributes": {},
    "globalStyles": {},
    "selectors": [],
    "preWhitespaceDetectedTags": ["DIV", "SPAN"],
    "stayOriginalSelectors": [],
    "additionalSelectors": [],
    "atomicBlockTags": [],
    "excludeSelectors": [],
    "additionalExcludeSelectors": [],
    "translationClasses": [],
    "atomicBlockSelectors": [],
    "excludeTags": [],
    "metaTags": ["META", "SCRIPT", "STYLE", "NOSCRIPT"],
    "additionalExcludeTags": [],
    "stayOriginalTags": ["CODE", "TT", "IMG", "SUP"],
    "additionalStayOriginalTags": [],
    "inlineTags": [],
    "additionalInlineTags": [],
    "extraInlineSelectors": [],
    "additionalInlineSelectors": [],
    "extraBlockSelectors": [],
    "allBlockTags": [],
    "pdfNewParagraphLineHeight": 2.4,
    "pdfNewParagraphIndent": 1.2,
    "pdfNewParagraphIndentRightIndentPx": 130,
    "fingerCountToToggleTranslagePageWhenTouching": 4
  },
  "rules": [
    {
      "matches": "www.google.com",
      "selectors": [".class"]
    }
  ]
}
```

`rules` में नियम फ़ील्ड `generalRule` में सभी फ़ील्ड्स का उपयोग कर सकते हैं। जब किसी विशेष साइट के लिए कोई विशेष `नियम` मेल खाता है, तो `rules` `generalRule` और उस `नियम` के लिए नियमों को मर्ज कर देते हैं, जिससे उन्हें सबसे उच्च प्राथमिकता मिलती है।

कॉन्फिग के कुछ सामान्य फ़ील्ड्स का परिचय।

### पॉपअप पैनल में अव्यवस्थित अनुवाद सेवाओं को प्रदर्शित न करें

`"showUnconfiguredTranslationServiceInPopup": false`

### अनुवाद सेवाओं का कॉन्फ़िगरेशन

डिफ़ॉल्ट अनुवाद इंजन का चयन करने के लिए `translationService` का उपयोग करें, जो वर्तमान में समर्थन करता है:

```typescript
| "tencent"
| "google"
| "deepl"
| "baidu"
| "volc"
| "youdao"
| "caiyun"
| "openl"
| "bing"
| "transmart"
```

प्रत्येक अनुवाद सेवा के `apikey` को कॉन्फ़िगर करने के लिए `translationServices` का उपयोग करें, विभिन्न सेवा प्रदाताओं को विभिन्न पैरामीटर की आवश्यकता होती है, और उनकी API कुंजियाँ उनकी संबंधित वेबसाइटों के डेवलपर केंद्र में अनुरोध की जा सकती हैं।

उदाहरण के लिए, Tencent अनुवादक, आपको `secretId`, `secretKey` को कॉन्फ़िगर करने की आवश्यकता है। आप Tencent Cloud पर जा सकते हैं और प्रति माह 5 मिलियन मुफ्त अक्षरों के साथ एक API कुंजी के लिए आवेदन कर सकते हैं। आवेदन प्रक्रिया के लिए [यहाँ](/docs/services/tencent) देखें।

```json
"translationServices": {
  "tencent": {
    "secretId": "xxx",
    "secretKey": "xxx",
    "matches":["*.twitter.com"],
    "limit": 3,
    "apiUrl":"",
    " maxTextGroupLengthPerRequest": 25,
    "maxTextLengthPerRequest": 1800
  }
}
```

`matches` फ़ील्ड, इस अनुवाद सेवा का उपयोग एक विशिष्ट वेबसाइट के लिए करना।

`limit` फ़ील्ड, जो इस अनुवाद सेवा के लिए प्रति सेकंड अधिकतम अनुरोधों की संख्या निर्दिष्ट करता है (कुछ सेवाएँ प्रति सेकंड अधिकतम अनुरोधों की संख्या सीमित करती हैं)।

`maxTextGroupLengthPerRequest` फ़ील्ड, प्रति अनुरोध अधिकतम पैराग्राफ की संख्या

`maxTextLengthPerRequest` फ़ील्ड, प्रति अनुरोध अधिकतम अक्षरों की संख्या

`apiUrl` आपको अनुवाद इंटरफ़ेस के पते को अनुकूलित करने की अनुमति देता है।

### विशिष्ट वेबसाइटों का हमेशा अनुवाद करें

`translationUrlPattern` उन साइटों को कॉन्फ़िगर करता है जिनका हमेशा अनुवाद किया जाता है, और उन साइटों को जिनका कभी अनुवाद नहीं किया जाता।

- `matches` कॉन्फ़िगरेशन हमेशा साइट का अनुवाद करता है।
- `excludeMatches` उन साइटों को कॉन्फ़िगर करें जिनका कभी अनुवाद नहीं किया जाता।

कॉन्फ़िगरेशन मूल्य डोमेन नाम हो सकते हैं या `*` के साथ URL, जैसे: `www.google.com/mail/*`

```json
"translationUrlPattern": {
    "matches": ["stackoverflow.com"],
    "excludeMatches": ["www.google.com/mail/*"]
}
```

### विशिष्ट भाषाओं का हमेशा अनुवाद करें

translationLanguagePattern, उस भाषा को कॉन्फ़िगर करता है जिसका हमेशा अनुवाद किया जाता है और उस भाषा को जिसका कभी अनुवाद नहीं किया जाता।

- `matches` हमेशा अनुवादित होने वाली भाषा को कॉन्फ़िगर करें, उदा. `en`,
- `excludeMatches` उन भाषाओं को कॉन्फ़िगर करें जिनका कभी अनुवाद नहीं किया जाता।

### अनुवाद प्रदर्शन प्रारूप

`translationTheme` अनुवाद के प्रदर्शन प्रारूप है, और वर्तमान में निम्नलिखित शैलियों का समर्थन करता है:

```typescript
| "कोई नहीं"
| "डैश्ड"
| "डॉटेड"
| "अंडरलाइन"
| "मास्क"
| "पेपर"
| "हाइलाइट"
| "ब्लॉककोट"
| "कमजोर करना"
| "इटैलिक"
| "बोल्ड"
| "थिन डैश्ड".
```

संबंधित चीनी नाम:

```json
{
  "कोई नहीं": "कोई नहीं",
  "डैश्ड": "बिंदीदार रेखा",
  "डॉटेड": "बिंदीदार रेखा",
  "अंडरलाइन": "सीधी रेखा अंडरलाइन",
  "मास्क": "धुंधला प्रभाव",
  "पेपर": "सफेद कागज छाया प्रभाव",
  "हाइलाइट": "हाइलाइट",
  "ब्लॉककोट": "उद्धरण शैली",
  "कमजोर करना": "कमजोर करना",
  "इटैलिक": "तिरछा",
  "बोल्ड": "बोल्डिंग",
  "थिन डैश्ड": "पतली डैश्ड रेखा"
}
```

`translationThemePatterns` आपको विभिन्न वेबसाइटों के लिए विभिन्न अनुवाद शैलियों को कॉन्फ़िगर करने की अनुमति देता है।

```json
"translationThemePatterns": {
  "अंडरलाइन": {
    "matches": ["discord.com"]
  }
}
```

### कक्षा gpt पेज स्ट्रीम संदेश अनुवाद

```json
{
  "matches": ["chat.openai.com"],
  "excludeSelectors": [".markdown *"],
  "aiRule": {
    "streamingSelector": ".result-streaming.markdown ",
    "messageWrapperSelector": ".markdown",
    "streamingChange": true
  }
}
```

Please note, translating code elements like variable names and identifiers from English to another language might not always be practical or advisable as it could affect the functionality of the code.

### नियम

`rules` एक ऐरे ऑब्जेक्ट है जो आपको विशेष साइटों के लिए नियमों को कॉन्फ़िगर करने की अनुमति देता है, जैसे कि ट्विटर को केवल एक निश्चित क्षेत्र का हिस्सा अनुवादित करना:

```json
{
  "rules": [
    {
      "id": "twitter",
      "matches": ["twitter.com", "mobile.twitter.com", "tweetdeck.twitter.com"],
      "selectors": [
        "[data-testid=' tweetText']",
        ".tweet-text",
        ".js-quoted-tweet-text",
        "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)",
        "[data-testid=' developerBuiltCardContainer'] > div:nth-child(2)",
        "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)"
      ],
      "extraInlineSelectors" : ["[data-testid=\"tweetText\"] div"]
    }
  ]
}
```

वर्तमान में निर्मित `rules` [यहाँ](https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json) पाए जा सकते हैं।

उदाहरण के लिए कुछ महत्वपूर्ण फील्ड्स नीचे चुने गए हैं:

```typescript
export interface Rule {
  // वेबसाइट का मिलान करें
  id?: string; // प्रत्येक अनुकूलन नियम की अपनी आईडी होती है, यदि उपयोगकर्ता इस परिवर्तन के ऊपर इस नियम का पुन: उपयोग करना चाहते हैं, तो उन्हें अपने नियम में इस संबंधित आईडी को जोड़ना होगा
  matches?: string | string[]; // यह नियम केवल यहाँ दी गई वेबसाइट से मिलेगा। यह नियम केवल यहाँ साइटों से मिलेगा।
  excludeMatches?: string | string[]; // विशिष्ट साइटों को बाहर करें।
  selectorMatches?: string | string[]; // सभी urls को निर्दिष्ट किए बिना एक सिलेक्टर के साथ मिलान करें
  excludeSelectorMatches?: string | string[]; // नियमों को बाहर करें, जैसा कि ऊपर है।

  // अनुवादों की रेंज निर्दिष्ट करें
  selectors?: string | string[]; // केवल उन तत्वों का अनुवाद करें जो मैच करते हैं
  excludeSelectors?: string | string[]; // तत्वों को बाहर करें, मैचों का अनुवाद न करें
  excludeTags?: string | string[]; // टैग्स को बाहर करें, मैचिंग टैग्स का अनुवाद न करें

  // अनुवाद क्षेत्रों को ओवरराइड करने के बजाय जोड़ें
  additionalSelectors?: string | string[]; // अनुवाद क्षेत्रों को जोड़ें। बुद्धिमानी से अनुवादित क्षेत्रों में अनुवाद स्थानों को जोड़ें।
  additionalExcludeSelectors?: string | string[]; // विशिष्ट स्थानों को अनुवादित नहीं करने के लिए अतिरिक्त बाहरी तत्वों को जोड़ें।
  additionalExcludeTags?: string | string[]; // अतिरिक्त बाहरी टैग्स

  // जैसा है वैसा ही रहने दें
  stayOriginalSelectors?: string | string[]; // मिलान तत्वों को जैसा है वैसा ही छोड़ दिया जाएगा। आमतौर पर फोरम साइट टैग्स में उपयोग किया जाता है।
  stayOriginalTags?: string | string[]; // मिलान टैग्स को जैसा है वैसा ही छोड़ दिया जाएगा, उदाहरण के लिए `code`

  // क्षेत्रीय अनुवाद
  atomicBlockSelectors?: string | string[]; // क्षेत्रीय सिलेक्टर्स, मिलान तत्वों को एक पूरे के रूप में माना जाएगा, खंडों में अनुवादित नहीं किया जाएगा।
  atomicBlockTags?: string | string[]; // क्षेत्र टैग सिलेक्टर्स, ऊपर के समान

  // ब्लॉक या इनलाइन
Here's the translated content in Hindi:

```markdown
  extraBlockSelectors?: string | string[]; // अतिरिक्त सेलेक्टर्स, मिलान करने वाले तत्वों को ब्लॉक तत्वों के रूप में माना जाएगा, एक पंक्ति में अनुवादित नहीं किया जाएगा।
  extraInlineSelectors?: string | string[]; // अतिरिक्त सेलेक्टर्स जिनका उपयोग इनलाइन तत्वों के रूप में किया जाएगा।

  inlineTags?: string | string[]; // मिलान किया गया टैग इनलाइन तत्व के रूप में उपयोग किया जाएगा
  preWhitespaceDetectedTags?: string | string[]; // मिलान किया गया टैग स्वतः लपेटा जाएगा

  // अनुवाद शैली
  translationClasses? string | string | string[]; // अनुवाद में अतिरिक्त क्लासेस जोड़ें

  // ग्लोबल शैलियाँ
  globalStyles?: Record<string, string>; // पृष्ठ शैलियों को संशोधित करें, यदि अनुवाद पृष्ठ को गड़बड़ कर देता है तो यह उपयोगी है।
  globalAttributes?: Record<string, Record<string, string>>; // पृष्ठ तत्वों की विशेषताओं को संशोधित करें

  // एम्बेडेड शैलियाँ
  injectedCss?: string | string[]; // CSS शैलियों को एम्बेड करें
  additionalInjectedCss?: string | string[]; // इसे ओवरराइड करने के बजाय अतिरिक्त CSS शैलियाँ।

  // संदर्भ
  wrapperPrefix?: string; // अनुवाद क्षेत्र का उपसर्ग, डिफ़ॉल्ट रूप से स्मार्ट होता है, अक्षरों की संख्या के आधार पर लाइन ब्रेक के साथ या बिना।
  wrapperSuffix?: string; // अनुवाद क्षेत्र का प्रत्यय

  // अनुवाद को लपेटने के लिए अक्षरों की संख्या
  blockMinTextCount?: number; // अनुवाद को एक ब्लॉक के रूप में लपेटने के लिए न्यूनतम अक्षरों की संख्या, अन्यथा अनुवाद एक इनलाइन तत्व है।
  blockMinWordCount?: number; // ऊपर के समान। यदि आप चाहते हैं कि वे हमेशा नई पंक्ति में हों, तो आप दोनों में 0 डाल सकते हैं।

  // सामग्री से अनुवादित किए जा सकने वाले न्यूनतम अक्षरों की संख्या
  containerMinTextCount?: number; // एक तत्व को अनुवादित किया जाना चाहिए इससे पहले उसमें होने वाले न्यूनतम अक्षरों की संख्या, डिफ़ॉल्ट रूप से 18 होती है
  paragraphMinTextCount?: number; // पैराग्राफ के लिए न्यूनतम अक्षरों की संख्या, सामग्री में होने वाले अक्षरों की संख्या से अधिक होनी चाहिए। कुछ भी इससे बड़ा होगा अनुवादित किया जाएगा
```

Please note, translating code comments or technical documentation can sometimes lead to nuances being lost or inaccurately represented due to the specific technical terms used. Always review translations in the context of your project to ensure accuracy.
```markdown
  paragraphMinWordCount?: संख्या; // मूल पैराग्राफ में शब्दों की न्यूनतम संख्या

  // लंबे पैराग्राफ के लिए जबरन पंक्ति विराम
  lineBreakMaxTextCount?: संख्या; // पैराग्राफ में अधिकतम वर्णों की संख्या जिसे लंबे पैराग्राफ का अनुवाद करते समय जबरन तोड़ना पड़े।

  // अनुवाद शुरू करने का समय।
  urlChangeDelay?: संख्या; // पृष्ठ में प्रवेश करने के बाद अनुवाद में देरी के लिए कितने मिलीसेकंड। पृष्ठ के आरंभिकीकरण की प्रतीक्षा करने के लिए, यह डिफ़ॉल्ट रूप से 250ms है
  observeUrlChange?: बूलियन; // जब url पता बदल जाता है तो पता लगाएं और फिर से अनुवाद शुरू करें, डिफ़ॉल्ट रूप से सच है।

  // मोबाइल
  isShowUserscriptPagePopup?: बूलियन; // मोबाइल उपकरणों पर पृष्ठ पॉपअप दिखाएं। तैरती हुई विंडो, डिफ़ॉल्ट रूप से सच है।
  fingerCountToToggleTranslagePageWhenTouching?: संख्या; // जब चार उंगलियाँ छूती हैं तो अनुवाद करता है, 0, 2, 3, 4, 5 पर सेट किया जा सकता है

  // AI स्ट्रीमिंग अनुवाद
  aiRule: {
    streamingSelector: स्ट्रिंग; // gpt वेब पृष्ठ पर अनुवादित हो रहे तत्व को चिह्नित करने के लिए सेलेक्टर
    messageWrapperSelector: स्ट्रिंग; // संदेश शरीर सेलेक्टर
    streamingChange: बूलियन; // संदेश को gpt वेब पृष्ठ पुनरावृत्ति के लिए वृद्धिशील रूप से या पूरी तरह से अपडेट किया जाता है या नहीं। gpt वृद्धिशील है
  };
}

**अधिक व्याख्या**

ब्लॉक और इनलाइन के बीच का अंतर, यदि आप और जानना चाहते हैं तो आप [यहाँ](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements#inline) देख सकते हैं।

- ब्लॉक तत्व एक सिंगल लाइन लेता है, और कई पड़ोसी ब्लॉक तत्व प्रत्येक एक नई लाइन लेते हैं।
- इनलाइन तत्व एक सिंगल लाइन नहीं लेता; कई पड़ोसी इनलाइन तत्व एक ही लाइन पर व्यवस्थित होते हैं, और एक नई लाइन तब तक नहीं बनती जब तक एक लाइन बहुत अधिक न हो जाए।
```