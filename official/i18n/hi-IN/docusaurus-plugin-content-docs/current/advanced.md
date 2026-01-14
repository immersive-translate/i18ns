---
sidebar_position: 4
---

# उन्नत कस्टमाइज़ेशन विकल्प

यह पेज उन उन्नत यूज़र्स के लिए है जिनको HTML/CSS/JSON की बुनियादी जानकारी है। उन्नत सेटिंग्स आपकी कस्टमाइज़ेशन क्षमता को काफी बढ़ा सकती हैं, लेकिन इससे "ठीक दिखने वाली लेकिन अक्षम" सेटिंग्स भी जल्दी बन सकती हैं, इसलिए संपादन से पहले बैकअप लेने की सलाह दी जाती है।

## उपयोग से पहले की सलाह

- [डेवलपर सेटिंग्स](https://dash.immersivetranslate.com/#developer) में एंट्री बिंदु।
- संपादन से पहले User Config / User Rules का बैकअप लें, ताकि फॉर्मेटिंग की गलती से सेटिंग्स को अनदेखा न किया जाए।
- फाइनल बिल्ट-इन सेटिंग का संदर्भ "Click to expand the final config" पर लें (फ़ील्ड, डिफ़ॉल्ट वैल्यू, उपलब्ध सेवाएं)।

## एंट्री पॉइंट्स व प्राथमिकता

मुख्य एंट्री (डेवलपर सेटिंग्स में):
- Edit Full User Config: सारी सेटिंग्स (जैसे `rules`, ट्रांसलेशन सर्विस, स्टाइल आदि)।
- Edit User Rules: केवल `rules` ऐरे को एडिट करना (इसमें सर्फ़ ऐरे सपोर्ट है, `{ "rules": [...] }` न लिखें)।
- Injected CSS: ग्लोबल CSS ऐड करें।

प्राथमिकता (सबसे ऊपर से नीचे): हिट हुआ `rules` > `generalRule` > डिफ़ॉल्ट इनबिल्ट सेटिंग।
किसी `rule` के हिट होने पर, `generalRule` और उक्त `rule` मर्ज होती हैं, लेकिन अंतिम फ़ील्ड उसी `rule` का माना जाता है।

## फास्ट स्टार्ट (सबसे आम ज़रूरतें)

### 1) किसी वेबसाइट के केवल मुख्य कंटेंट का अनुवाद करें

```json
{
  "rules": [
    {
      "matches": ["example.com"],
      "selectors": ["article", ".post-content"],
      "excludeSelectors": ["nav", "footer", ".comment"]
    }
  ]
}
```

### 2) हमेशा अनुवाद करें / कभी नहीं करें

```json
{
  "translationUrlPattern": {
    "matches": ["stackoverflow.com"],
    "excludeMatches": ["www.google.com/mail/*"]
  }
}
```

### 3) अलग-अलग साइट्स के लिए अलग ट्रांसलेशन सर्विस यूज़ करें

```json
{
  "translationService": "google",
  "translationServices": {
    "deepl": {
      "matches": ["sci-hub.se"]
    }
  }
}
```

### 4) साइट के हिसाब से ट्रांसलेशन थीम बदलें

```json
{
  "translationTheme": "none",
  "translationThemePatterns": {
    "underline": {
      "matches": ["discord.com"]
    }
  }
}
```

### 5) अनुवाद से स्टाइल बिगड़े तो खुद स्टाइल सही करें

```json
{
  "rules": [
    {
      "matches": ["youtube.com"],
      "globalStyles": {
        "#video-title": "max-height:unset;"
      }
    }
  ]
}
```

### 6) जिन ट्रांसलेशन सर्विस का कॉन्फ़िगरेशन नहीं है, उन्हें पॉपअप में न दिखाएं

```json
{
  "showUnconfiguredTranslationServiceInPopup": false
}
```

## रूल्स और मैचिंग

### रूल मर्जिंग

- `generalRule`: सभी साइट्स के लिए बेसलाइन सेटिंग।
- `rules`: साइट-विशिष्ट सेटिंग, प्राथमिकता सबसे ज़्यादा।

`rules` में सामान्यतः `generalRule` कि ज़्यादातर फ़ील्ड्स का प्रयोग कर सकते हैं।

### matches कैसे लिखें

`matches` में स्ट्रिंग या ऐरे दोनों लिख सकते हैं:
- डोमेन: `example.com`
- पूरा URL: `https://example.com/path/`
- वाइल्डकार्ड: `https://*/*q=*`
- सब कुछ मैच: `*` / `*://*` / `*://*/*`
- लोकल फाइल: `file://*`

ध्यान दें: `*.twitter.com` सिर्फ़ सबडोमेन पर काम करेगा, रूट डोमेन `twitter.com` पर नहीं।

### selectors / excludeSelectors

- `selectors`: केवल उन्हीं एलिमेंट्स का अनुवाद होगा (डिफ़ॉल्ट रेंज ओवरराइड करेगा)।
- `excludeSelectors`: इन एलिमेंट्स को छोड़कर बाकी का अनुवाद होगा।

अगर आपको सिर्फ़ डिफ़ॉल्ट रेंज में ‘add/remove’ करना है, तो `.add` / `.remove` ज़्यादा उपयुक्त है (अगले सेक्शन में देखें)।

### इनहेरिटेंस और इनक्रिमेंटल मोडिफिकेशन (.add / .remove)

स्ट्रिंग/ऑब्जेक्ट टाइप फ़ील्ड्स के लिए `.add` / `.remove` से “इन्क्रीमेंटल चेंज” ला सकते हैं।
ऐसा करने से डिफ़ॉल्ट रूल को ओवरराइड करने से बच सकते हैं:

```json
[
  {
    "id": "twitter",
    "selectors.add": ["[data-testid='tweetText'] a"],
    "excludeSelectors.add": ["header"]
  }
]
```

### आम फ़ील्ड्स (संक्षिप्त संदर्भ)

मैचिंग:
- `matches` / `excludeMatches`
- `selectorMatches` / `excludeSelectorMatches`

ट्रांसलेशन रेंज:
- `selectors` / `excludeSelectors` / `excludeTags`
- `stayOriginalSelectors` / `stayOriginalTags`
- `extraInlineSelectors` / `extraBlockSelectors`

स्टाइल और लेआउट:
- `translationClasses`: ट्रांसलेटेड टेक्स्ट में एक्स्ट्रा क्लास जोड़ें
- `globalStyles` / `globalAttributes`
- `injectedCss` / `additionalInjectedCss`
- `wrapperPrefix` / `wrapperSuffix`
- `blockMinTextCount` / `blockMinWordCount`

टाइमिंग और मोबाइल:
- `urlChangeDelay` / `observeUrlChange`
- `isShowUserscriptPagePopup`

### GPT-समान स्ट्रीमिंग पेज ट्रांसलेशन

```json
{
  "matches": ["chat.openai.com"],
  "excludeSelectors": [".markdown *"],
  "aiRule": {
    "streamingSelector": ".result-streaming.markdown",
    "messageWrapperSelector": ".markdown",
    "streamingChange": true
  }
}
```

अधिक फ़ील्ड्स विवरण के लिए, नीचे “Rule फ़ील्ड्स संदर्भ” देखें।

## matches (मैचिंग लॉजिक - संक्षिप्त)

- सिर्फ़ डोमेन (कोई `*` या path नहीं): केबल hostname चेक होगा।
- पूरा URL (`*` के बिना): प्रोटोकॉल + होस्ट + पोर्ट + पाथ तक देखेगा।
- `*` या प्रोटोकॉल नहीं: वाइल्डकार्ड से मैच करेगा (http/https/file सपोर्टेड)।

कुछ उदाहरण:
- `twitter.com` ✅ मैच करेगा `https://twitter.com/home`
- `*.twitter.com` ✅ मैच करेगा `https://mobile.twitter.com`, ❌ मैच नहीं करेगा `https://twitter.com`
- `https://twitter.com/home` तभी मैच करेगा जब URL पूरा वैसे ही हो
- `twitter.com/*` ट्विटर के सारे पाथ्स पर मैच करेगा

## वेबसाइट एडॉप्शन (जैसे Twitter केस)

नीचे दिए गए हैं Twitter के बिल्ट-इन सेटिंग्स (संक्षिप्त), खासकर `selectors` / `excludeSelectors` / `globalStyles` के लिए:

```json
[
  {
    "id": "twitter",
    "matches": [
      "twitter.com",
      "mobile.twitter.com",
      "tweetdeck.twitter.com",
      "pro.twitter.com",
      "https://platform.twitter.com/embed*"
    ],
    "selectors": [
      "[data-testid=\"tweetText\"]",
      ".tweet-text",
      ".js-quoted-tweet-text",
      "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)",
      "[data-testid='developerBuiltCardContainer'] > div:nth-child(2)",
      "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)",
      "[data-testid='cellInnerDiv'] div[data-testid='UserCell'] > div> div:nth-child(2)",
      "[data-testid='UserDescription']",
      "[data-testid='HoverCard'] div[dir=auto]",
      "[data-testid='HoverCard'] span[dir=auto]",
      "[data-testid='HoverCard'] [role='dialog'] div[dir=ltr]",
      "[data-testid='birdwatch-pivot'] div[dir=ltr]"
    ],
    "excludeSelectors": [
      "[aria-describedby][role=button]",
      "header",
      "[data-testid='radioGroupplayback_rate'] div",
      "[data-testid='userFollowIndicator']",
      "[class='css-901oao r-14j79pv r-37j5jr r-n6v787 r-16dba41 r-1cwl3u0 r-bcqeeo r-qvutc0']",
      "[class='css-175oi2r r-1wbh5a2 r-dnmrzs']"
    ],
    "globalStyles": {
      "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='tweetText']": "-webkit-line-clamp: unset;"
    }
  }
]
```

- `selectors`: सिर्फ मुख्य ट्वीट कंटेंट का अनुवाद, नाम/बटन इत्यादि नहीं।
  ![tweet](https://s.immersivetranslate.com/assets/r2-uploads/tweet.png)
- `excludeSelectors`: बटनों, नेविगेशन आदि को छोड़ने के लिए।
  ![twitter-follow](https://s.immersivetranslate.com/assets/r2-uploads/twitter-follow.png)
- `globalStyles`: लाइन क्लैम्प हटाएं, ताकि अनुवाद कटे नहीं।
  ![用户主页](https://s.immersivetranslate.com/assets/r2-uploads/twitterUser.png)

## वेबसाइट के लिए खुद का एडॉप्शन बनाएं

`id` से इनबिल्ट रूल रीयूज़ किया जा सकता है, और `.add / .remove` से छोटा संशोधन:

```json
[
  {
    "id": "twitter",
    "selectors.remove": ["[data-testid=\"tweetText\"]"],
    "selectors.add": ["[data-testid=\"tweetText\"] a"],
    "excludeSelectors.add": ["header"],
    "excludeSelectors.remove": []
  }
]
```

व्याख्या:
- `id` से इनबिल्ट रूल्स वारिस किए जा सकते हैं, बार-बार `matches` लिखने की ज़रूरत नहीं।
- `.add/.remove` ऐरे फ़ील्ड्स के लिए इन्क्रीमेंटल मॉडिफिकेशन, यही प्राथमिकता होनी चाहिए।

कुछ आम इनबिल्ट `id`:
- `isEbook`: epub रीडर
- `isEbookBuilder`: epub ड्यूल-लैंग बुक जनरेशन पेज
- `pdf`: PDF ड्यूल-लैंग पेज

पूरा कॉन्फ़िग:  
- `https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json`

## ट्रांसलेशन सर्विस कॉन्फ़िगरेशन

- `translationService`: डिफ़ॉल्ट ट्रांसलेट इंजन।
- `translationServices`: सर्विस्स की सेटिंग और वेबसाइट पर ओवरराइड।
- `showUnconfiguredTranslationServiceInPopup`: जिनकी सेटिंग नहीं, उन्हें छुपाएं।

उदाहरण (Tencent के लिए):

```json
{
  "translationService": "tencent",
  "translationServices": {
    "tencent": {
      "secretId": "xxx",
      "secretKey": "xxx",
      "matches": ["twitter.com"],
      "limit": 3,
      "maxTextGroupLengthPerRequest": 25,
      "maxTextLengthPerRequest": 1800,
      "apiUrl": ""
    }
  }
}
```

व्याख्या:
- `matches`: बताता है ये सर्विस किन साइट्स के लिए लागू होगी।
- `limit`: लिमिट (प्रति सेकंड रिक्वेस्ट काउंट)।
- `maxTextGroupLengthPerRequest` / `maxTextLengthPerRequest`: एक बार में कितना टेक्स्ट भेज पाएंगे।
- `apiUrl`: सर्विस एड्रेस बदल सकते हैं।

### रिक्वेस्ट टाइमआउट सेटिंग (मैक्स ड्यूरेशन)

प्रत्येक सर्विस के लिए टाइमआउट (ms) सेट कर सकते हैं। Pro सर्विस के लिए अलग से `proRequestTimeout` सेट कर सकते हैं।

```json
{
  "translationServices": {
    "openai": {
      "requestTimeout": 60000
    },
    "gemini": {
      "proRequestTimeout": 90000
    }
  }
}
```

ध्यान दें:
- ज्यादा टाइमआउट = प्रतीक्षा लंबी; कम टाइमआउट = फेल/टाइमआउट जल्दी।
- डिफ़ॉल्ट वैल्यू सर्विस के अनुसार अलग है।
- सिर्फ `pro` प्रोवाइडर में `proRequestTimeout` मायने रखता है।

## भाषा और ट्रांसलेशन स्ट्रैटेजी

### हमेशा/कभी नहीं वाले भाषाई पैटर्न

```json
{
  "translationLanguagePattern": {
    "matches": ["en"],
    "excludeMatches": ["zh"]
  }
}
```

### किसी साइट के लिए source language निर्धारित करें

```json
{
  "sourceLanguageUrlPattern": {
    "en": {
      "matches": ["*.google.com"]
    }
  }
}
```

## अन्य अक्सर काम आने वाली सेटिंग्स

### HTML टैग्स रेंडर होने दें

अगर आप अनुवाद में HTML टैग्स मौजूद रखना और रेंडर करवाना चाहते हैं:

```json
{
  "enableRenderHtmlTag": true
}
```

## अनुवाद स्टाइल्स व थीम

`translationTheme` द्वारा समर्थित स्टाइल्स (फाइनल कॉन्फिग देखें):

```text
none, grey, dashed, dashedBorder, solidBorder, dotted, underline, mask, opacity,
paper, dividingLine, highlight, marker, marker2, blockquote, weakening, italic,
bold, thinDashed, nativeDotted, wavy, nativeDashed, nativeUnderline, background
```

साइट के अनुसार स्टाइल सेट करने के लिए:

```json
{
  "translationThemePatterns": {
    "highlight": {
      "matches": ["discord.com"]
    }
  }
}
```

## AI / उन्नत सर्विस पैरामीटर

### temperature

```json
{
  "translationServices": {
    "openai": {
      "temperature": 0.2
    }
  }
}
```

### कस्टम रिक्वेस्ट हेडर और बॉडी

```json
{
  "translationServices": {
    "claude": {
      "headerConfigs": {
        "anthropic-version": "2023-06-01",
        "anthropic-dangerous-direct-browser-access": "true"
      },
      "bodyConfigs": {
        "max_tokens": 2048
      }
    }
  }
}
```

### Gemini मॉडल के लिए कैसे कस्टमाइज़ करें

Gemini मॉडल्स में डिफ़ॉल्ट सेटिंग्स हैं, ओवरराइड करने के लिए `modelsOverrides` का इस्तेमाल करें:

```json
{
  "translationServices": {
    "gemini": {
      "modelsOverrides": [
        {
          "models": ["gemini-2.5-flash", "gemini-2.5-flash-lite"],
          "bodyConfigs": {
            "temperature": 0.1
          }
        }
      ]
    }
  }
}
```

टिप: `modelsOverrides` अन्य AI सर्विस में भी चल सकती है, मॉडल नाम से मैचिंग कर सकती है।

### कस्टम प्रॉम्प्ट सख्ती से लागू करना

> बड़े भाषा मॉडल में “हल्लुसिनेशन” रोकने हेतु क्वालिटी चेक मैकेनिज्म है। सिस्टम, रिस्पॉन्स और रिक्वेस्ट के टोकन्स की संख्या का अनुपात देखकर जज करता है कि ट्रांसलेशन सही है या नहीं। अनुपात गड़बड़ होने पर रिजल्ट रिजेक्ट कर सेकेंडरी सर्विस पर ट्राय करता है।
> अगर आपकी प्रॉम्प्ट ट्रांसलेशन नहीं, बल्कि कोई और टास्क (जैसे एक्सपैंड, संपादन) है, तो टोकन अनुपात विफल हो सकता है। ऐसे में सख्त मोड चालू करें—जो अनुपात टेस्ट को बायपास करता है।

```json
{
  "translationServices": {
    "claude": {
      "strictPrompt": true
    }
  }
}
```

### मल्टीलिंगुअल कस्टम प्रॉम्प्ट्स (नमूना)

```json
{
  "translationServices": {
    "openai": {
      "langOverrides": [
        {
          "id": "auto2ja",
          "systemPrompt": "あなたはプロの翻訳エンジンです。",
          "prompt": "次のテキストを{{to}}に翻訳してください：\n\n<text>\n{{text}}\n</text>",
          "multiplePrompt": "<yaml>\n{{yaml}}\n</yaml>",
          "subtitlePrompt": "<yaml_subtitles>\n{{yaml}}\n</yaml_subtitles>"
        }
      ]
    }
  }
}
```

## शब्दकोश व मशीन ट्रांसलेशन

[AI शब्दकोश](https://dash.immersivetranslate.com/#terms) अब उपलब्ध है (केवल AI ट्रांसलेट सर्विस पर)।

मशीन ट्रांसलेशन में शब्दकोश डिफ़ॉल्ट रूप से लागू नहीं (ऐसा करने पर क्वालिटी बिगड़ सकती है)। आवश्यक हो तो जबरन चालू कर सकते हैं (अनुशंसित नहीं):

```json
{
  "enableMachineTranslateTerms": true
}
```

## कैश क्लियरिंग साइकिल

डिफ़ॉल्ट रूप से, प्लगइन 30 दिनों में ट्रांसलेशन कैश साफ़ करता है, ताकि परफॉर्मेंस बना रहे।

```json
{
  "cacheMaxAgeDay": 30
}
```

## Injected CSS और globalStyles

- Injected CSS: ग्लोबल CSS, पूरी पेज के कुछ फिक्स के लिए।
- globalStyles: साइट/रूल-विशिष्ट CSS फिक्स के लिए।

Injected CSS उदाहरण:

```css
.immersive-translate-target-wrapper img {
  width: 16px;
  height: 16px;
}
```

## डिबगिंग और आम समस्याएं

- `*.twitter.com` में रूट डोमेन नहीं, दोनों लिखें: `twitter.com` और `*.twitter.com`।
- `selectors` डिफ़ॉल्ट रेंज को ओवरराइड करता है, ज़रूरत हो तभी यूज़ करें, वर्ना `.add/.remove` ठीक है।
- `matches` अगर `example.com/path` जैसा है, तो वाइल्डकार्ड की तरह चल सकता है—ध्यान रखें।
- सेटिंग नहीं चली, तो फाइनल सेटिंग्स चेक कर फिर पेज रीफ्रेश करें।
- JSON के आख़िर में एक्स्ट्रा कोमा न छोड़ें, वरना पूरा डाटा अनदेखा हो सकता है।

## परिशिष्ट: Rule फ़ील्ड्स संदर्भ

Rule फ़ील्ड्स वर्णन (डॉक्युमेंट वर्ज़न), सिर्फ सामान्य फ़ील्ड्स के लिए; पूरी लिस्ट फाइनल सेटिंग में देखें।
टिप: ऐरे या ऑब्जेक्ट फ़ील्ड्स को `.add` / `.remove` से इन्क्रीमेंटल मोडिफाई करें, डिफ़ॉल्ट रूल्स रखा जा सके।

```typescript
export interface Rule {
  // वेबसाइट मैचिंग
  id?: string; // बिल्ट-इन रूल ID, इनहेरिट के लिए प्रयोग करें
  matches?: string | string[]; // यह रूल सिर्फ इन वेबसाइट्स पर ही लागू होगा
  excludeMatches?: string | string[]; // किन साइट्स पर ऐक्टिव न हो
  selectorMatches?: string | string[]; // सेलेक्टर बेस्ड मैचिंग (URL के बिना)
  excludeSelectorMatches?: string | string[]; // इन्हें छोड़ें

  // ट्रांसलेट क्षेत्र चुनें
  selectors?: string | string[]; // सिर्फ चयनित एलीमेंट्स का ट्रांसलेट
  excludeSelectors?: string | string[]; // ट्रांसलेट से बाहर करने वाले एलीमेंट्स
  excludeTags?: string | string[]; // टैग्स जिन्हें अनुवादित नहीं करेंगे

  // अतिरिक्त क्षेत्र जोड़ें (काम न करे तो selectors.add/selectors.remove का इस्तेमाल करें)
  additionalSelectors?: string | string[]; // अतिरिक्त ट्रांसलेशन क्षेत्र
  additionalExcludeSelectors?: string | string[]; // अतिरिक्त बाहर करने वाले
  additionalExcludeTags?: string | string[]; // पुराने वर्ज़न में; अब शायद डिप्रिकेटेड

  // जस का तस रखें
  stayOriginalSelectors?: string | string[]; // ऐसे एलीमेंट्स जस के तस
  stayOriginalTags?: string | string[]; // ऐसे टैग जस के तस (जैसे code)

  // ब्लॉक या इनलाइन
  extraBlockSelectors?: string | string[]; // जिन्हें ब्लॉक की तरह ट्रीट करें
  extraInlineSelectors?: string | string[]; // इन्हें इनलाइन ट्रीट करें
  inlineTags?: string | string[]; // इन टैग्स को इनलाइन मानें
  preWhitespaceDetectedTags?: string | string[]; // ऐसे टैग्स जहां ऑटो लाइनब्रेक लगे

  // ट्रांसलेटेड टेक्स्ट स्टाइल
  translationClasses?: string | string[]; // एक्स्ट्रा क्लास लगाएं

  // ग्लोबल स्टाइल
  globalStyles?: Record<string, string>; // CSS ओवरराइड
  globalAttributes?: Record<string, Record<string, string | null>>; // एलीमेंट्स के HTML एट्रिब्यूट्स

  // इनकैप्सुलेटेड स्टाइल
  injectedCss?: string | string[]; // पेज में CSS जोड़ें
  additionalInjectedCss?: string | string[]; // और CSS जोड़ें

  // संदर्भ
  wrapperPrefix?: string; // ट्रांसलेटेड टेक्स्ट से पहले क्या आए
  wrapperSuffix?: string; // बाद में क्या आए

  // ट्रांसलटेड टेक्स्ट में लाइनब्रेक सीमा
  blockMinTextCount?: number; // कम से कम इतने अक्षर हों
  blockMinWordCount?: number; // कम से कम इतने शब्द हों

  // कंटेंट में मिनिमम कैरेक्टर काउंट (स्मार्ट डिटेक्ट)
  containerMinTextCount?: number;
  paragraphMinTextCount?: number;
  paragraphMinWordCount?: number;

  // लंबे पैराग्राफ में फोर्स लाइनब्रेक
  lineBreakMaxTextCount?: number;

  // कब ट्रांसलेट करना है
  urlChangeDelay?: number; // पेज लोड होने का इंतजार कितना
  observeUrlChange?: boolean; // URL बदलने पर फिर से अनुवाद करना है क्या

  // मोबाइल
  isShowUserscriptPagePopup?: boolean; // फ़ोन मोड में फ्लोटिंग पॉपअप दिखे
  fingerCountToToggleTranslagePageWhenTouching?: number; // अब डिप्रिकेटेड

  // AI स्ट्रीमिंग ट्रांसलेशन
  aiRule?: {
    streamingSelector: string; // स्टेट के दौरान हाईलाइट करें
    messageWrapperSelector: string; // मैसेज कंटेंट सेलेक्टर
    streamingChange: boolean; // इन्क्रीमेंटल अपडेट
  };
}
```
