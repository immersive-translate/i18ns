---
sidebar_position: 5
---

# JS SDK

Immersive Translate JS SDK आपकी वेबसाइट पर द्विभाषी अनुवाद को लागू करने में मदद करता है।

## उपयोग कैसे करें

1. Immersive Translate को प्रारंभ करें:

```js
<script>
  window.immersiveTranslateConfig = {
    pageRule: {}
  }
</script>
```

2. अपने वेबपेज में निम्नलिखित `script` कोड जोड़ें

```html
<script src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"></script>
```

उदाहरण

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Immersive Translate JS SDK</title>
    <script>
      window.immersiveTranslateConfig = {
        pageRule: {},
      };
    </script>
    <script
      async
      src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"
    ></script>
  </head>

  <body>
    <div>
      <p>
        Night gathers, and now my watch begins. It shall not end until my death.
        I shall take no wife, hold no lands, father no children. I shall wear no
        crowns and win no glory. I shall live and die at my post.
      </p>
    </div>
  </body>
</html>
```

## पैरामीटर्स

`pageRule` के साथ, आप वेबसाइट की कॉन्फ़िगरेशन को कस्टमाइज़ कर सकते हैं, यह तय करते हुए कि किस सामग्री का अनुवाद करना है या वेबपेज की शैलियों को समायोजित करना है।

```js
initImmersiveTranslate({
  pageRule: {
    selectors: [".text"],
    excludeSelectors: ["nav", "footer"],
  },
});
```

`selectors` का उपयोग करके स्मार्ट अनुवाद रेंज को ओवरराइड किया जा सकता है, केवल चयनकर्ता द्वारा मेल खाने वाले तत्वों का अनुवाद किया जाएगा।

`excludeSelectors` का उपयोग करके तत्वों को अनुवाद से बाहर रखा जा सकता है।

`selectors.add` का उपयोग करके डिफ़ॉल्ट चयनकर्ताओं के ऊपर कुछ चयनकर्ता जोड़े जा सकते हैं।

`selectors.remove` का उपयोग करके डिफ़ॉल्ट चयनकर्ताओं से कुछ चयनकर्ता हटाए जा सकते हैं।

यदि आप किसी विशेष क्षेत्र का अनुवाद करना चाहते हैं और किसी तत्व को संपूर्ण के रूप में मानना चाहते हैं बिना इसे लाइनों में तोड़े, तो आप `atomicBlockSelectors` चयनकर्ता का उपयोग कर सकते हैं। ध्यान दें कि `atomicBlockSelectors` का उपयोग करने से पहले आपको `selectors` का उपयोग करके तत्वों का चयन करना होगा।

```json
{
  "selectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"],
  "atomicBlockSelectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"]
}
```

`pageRule` के अधिक पैरामीटर स्पष्टीकरण:

```typescript
export interface PageRule {
  excludeMatches?: string | string[]; // विशिष्ट वेबसाइटों को बाहर करें।
  selectorMatches?: string | string[]; // सभी URLs को निर्दिष्ट किए बिना चयनकर्ताओं का उपयोग करके मेल खाएं
  excludeSelectorMatches?: string | string[]; // बाहर करने के नियम, ऊपर के समान।

  // अनुवाद रेंज निर्दिष्ट करें
  selectors?: string | string[]; // केवल मेल खाने वाले तत्वों का अनुवाद करें
  excludeSelectors?: string | string[]; // तत्वों को बाहर करें, मेल खाने वाले तत्वों का अनुवाद न करें
  excludeTags?: string | string[]; // टैग्स को बाहर करें, मेल खाने वाले टैग्स का अनुवाद न करें

  // अनुवाद रेंज जोड़ें, ओवरराइड नहीं करें
  additionalSelectors?: string | string[]; // अनुवाद रेंज जोड़ें। स्मार्ट अनुवाद क्षेत्रों में अनुवाद स्थान जोड़ें।
  additionalExcludeSelectors?: string | string[]; // विशिष्ट स्थानों में स्मार्ट अनुवाद को रोकने के लिए बाहर किए गए तत्व जोड़ें।
  additionalExcludeTags?: string | string[]; // बाहर किए गए टैग्स जोड़ें

  // मूल रखें
  stayOriginalSelectors?: string | string[]; // मेल खाने वाले तत्व मूल रहेंगे। आमतौर पर फोरम वेबसाइटों पर टैग्स के लिए उपयोग किया जाता है।
  stayOriginalTags?: string | string[]; // मेल खाने वाले टैग्स मूल रहेंगे, जैसे `code`

  // क्षेत्र अनुवाद
  atomicBlockSelectors?: string | string[]; // क्षेत्र चयनकर्ता, मेल खाने वाले तत्वों को संपूर्ण के रूप में माना जाएगा, खंडों में अनुवाद नहीं किया जाएगा
  atomicBlockTags?: string | string[]; // क्षेत्र टैग चयनकर्ता, ऊपर के समान

  // ब्लॉक या इनलाइन
  extraBlockSelectors?: string | string[]; // अतिरिक्त चयनकर्ता, मेल खाने वाले तत्वों को ब्लॉक तत्वों के रूप में माना जाएगा, एक पंक्ति पर कब्जा करेंगे।
  extraInlineSelectors?: string | string[]; // अतिरिक्त चयनकर्ता, मेल खाने वाले तत्वों को इनलाइन तत्वों के रूप में माना जाएगा।

  inlineTags?: string | string[]; // मेल खाने वाले टैग्स को इनलाइन तत्वों के रूप में माना जाएगा
  preWhitespaceDetectedTags?: string | string[]; // मेल खाने वाले टैग्स स्वचालित रूप से लाइनों को लपेटेंगे

  // अनुवाद शैलियाँ
  translationClasses?: string | string | string[]; // अनुवाद में अतिरिक्त कक्षाएं जोड़ें

  // वैश्विक शैलियाँ
  globalStyles?: Record<string, string>; // पृष्ठ शैलियों को संशोधित करें, जब अनुवाद पृष्ठ विकार का कारण बनता है तो उपयोगी।
  globalAttributes?: Record<string, Record<string, string>>; // पृष्ठ तत्वों के गुणों को संशोधित करें

  // एम्बेडेड शैलियाँ
  injectedCss?: string | string[]; // CSS शैलियों को एम्बेड करें
  additionalInjectedCss?: string | string[]; // सीधे ओवरराइड करने के बजाय CSS शैलियों को जोड़ें।

  // संदर्भ
  wrapperPrefix?: string; // अनुवाद क्षेत्र का उपसर्ग, डिफ़ॉल्ट रूप से स्मार्ट, वर्णों की संख्या के आधार पर लाइनों को लपेटने का निर्णय करता है।
  wrapperSuffix?: string; // अनुवाद क्षेत्र का उपसर्ग

  // अनुवाद लपेटने के वर्ण संख्या
  blockMinTextCount?: number; // ब्लॉक के रूप में अनुवाद के लिए न्यूनतम वर्ण संख्या, अन्यथा, अनुवाद एक इनलाइन तत्व होगा।
  blockMinWordCount?: number; // ऊपर के समान। हमेशा लाइनों को लपेटने के लिए, दोनों को 0 पर सेट करें।

  // अनुवाद योग्य सामग्री के लिए न्यूनतम वर्ण संख्या
  containerMinTextCount?: number; // स्मार्ट पहचान के दौरान अनुवाद किए जाने वाले तत्वों के लिए न्यूनतम वर्ण संख्या, डिफ़ॉल्ट रूप से 18
  paragraphMinTextCount?: number; // मूल अनुच्छेद के लिए न्यूनतम वर्ण संख्या, संख्या से अधिक सामग्री का अनुवाद किया जाएगा
  paragraphMinWordCount?: number; // मूल अनुच्छेद के लिए न्यूनतम शब्द संख्या
```

```markdown
आप एक पेशेवर तकनीकी दस्तावेज़ अनुवाद विशेषज्ञ हैं।
कृपया निम्नलिखित Markdown सामग्री का अनुवाद Hindi में करें और निम्नलिखित नियमों का सख्ती से पालन करें:

1. मूल प्रारूप बनाए रखें:
   - सभी Markdown सिंटैक्स को अपरिवर्तित रखें
   - सभी कोड ब्लॉक और HTML टैग को बनाए रखें
   - मूल लाइन ब्रेक और स्पेसिंग को बनाए रखें
   - सभी लिंक और URL को अपरिवर्तित रखें
   - कृपया ```markdown की शुरुआत और ``` की समाप्ति के कोड ब्लॉक को वापस न करें

2. पेशेवर शब्दावली:
   - सभी तकनीकी शब्दावली को अंग्रेजी में बनाए रखें
   - 'Release', 'Preview' जैसे शब्द अंग्रेजी में बनाए रखें
   - सभी संस्करण संख्या और तकनीकी विनिर्देशों को अपरिवर्तित रखें
  // लंबे पैराग्राफ के लिए जबरन लाइन ब्रेक कैरेक्टर काउंट
  lineBreakMaxTextCount?: number; // लंबे पैराग्राफ का अनुवाद करते समय जबरन लाइन ब्रेक के लिए अधिकतम कैरेक्टर काउंट।

  // अनुवाद शुरू करने का समय
  urlChangeDelay?: number; // पृष्ठ में प्रवेश करने के बाद अनुवाद शुरू करने से पहले विलंब मिलिसेकंड में। वेबपेज आरंभिकरण की प्रतीक्षा करने के लिए डिफ़ॉल्ट 250ms है।

  // AI स्ट्रीमिंग अनुवाद
  aiRule: {
    streamingSelector: string; // GPT वेबपेज चयनकर्ता जो अनुवादित तत्व को चिह्नित करता है
    messageWrapperSelector: string; // संदेश बॉडी चयनकर्ता
    streamingChange: boolean; // GPT-जैसे वेबपेजों में दोहराए गए संदेशों के लिए वृद्धिशील या पूर्ण अपडेट। GPT वृद्धिशील है
  };
}
```