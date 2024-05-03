---
sidebar_position: 4
---

# خيارات تخصيص متقدمة

يمكنك تعديل تكوينات مخصصة أكثر في صفحة التكوين الموسع -> إعدادات المطور -> تكوين المستخدم والتي لا يمكن تعديلها في واجهة المستخدم للمستخدمين المتقدمين، انظر الملاحظة الأخيرة لمزيد من التفاصيل حول البارامترات. يمكن العثور على `config` المدمج الحالي [هنا](https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json).

## قواعد المستخدم

مع `القواعد`، يمكن تخصيص إعدادات موقع ويب معين، مع تحديد المحتوى الذي يحتاج إلى الترجمة أو لا، أو تعديل أسلوب الصفحات، وما إلى ذلك.

```json
[
  {
    "matches": "www.google.com",
    "selectors": [".title"]
  },
  {
    "matches": "*.twitter.com",
    "selectors": [".text"],
    "excludeSelectors": ["nav", " footer"]
  }
]
```

استخدم `matches` لمطابقة الموقع الإلكتروني المقابل. يُسمح باستخدام البدائل العامة، مثل `*.google.com`,`www.google.com/test/*`,`file://*`.

استخدام `selectors` يتجاوز نطاق الترجمة الذكية، مترجمًا فقط العناصر التي يطابقها هذا المحدد.

استخدم `excludeSelectors` لاستبعاد العناصر دون ترجمة الموقع.

استخدم عائلة المحددات `additional` لزيادة أو تقليل نطاق الترجمة بناءً على الترجمة الذكية.

```json
[
  {
    "matches": "www.google.com",
    "additionalSelectors": [],
    "additionalExcludeSelectors": []
  }
]
```

إذا كنت ترغب في ترجمة منطقة مع معاملة العناصر ككل وليس فصلها، يمكنك استخدام المحدد `atomicBlockSelectors`.على سبيل المثال، ملفات تعريف إنستغرام.لاحظ أن استخدام `atomicBlockSelectors` يتطلب الاختيار باستخدام `selectors` قبل استخدام `atomicBlockSelectors`.

```json
{
  "matches": "https://www.instagram.com/*",
  "selectors": [
    "div._aa_c h1",
    "li._acaz div[role=\"menuitem\"]"
  ],
  "atomicBlockSelectors": [
    "div. ._aa_c h1",
    "li._acaz div[role=\"menuitem\"]"
  ]
}
```

إذا أدت الترجمة إلى صفحات غير متناسقة، نصوص متداخلة، وحالات حافة أخرى، يمكنك استخدام `globalStyles` لضبط أسلوب الصفحة لإصلاح ذلك.على سبيل المثال، رأس يوتيوب، والذي يُستخدم لإزالة الارتفاع الأقصى للصفحة الأصلية.

```json
{
  "matches": "www.google.com",
  "globalStyles": { ".title": "max-height:unset;" }
}
```

## تحسينات توحيد قواعد المستخدم

دعم الإصدار 0.7.4 فما فوق. خذ على سبيل المثال تخطي منطقة عدم الترجمة

```json
{
  "matches": "https://www.elektrotechnik.rwth-aachen.de/*",
  "additionalExcludeSelectors.remove": [".notranslate", "[translate=no]"]
}
```

عمليات الإضافة والإزالة تعدل القواعد المقدمة بشكل افتراضي ولا تحتاج إلى استبدالها بالكامل، كما كان الحال في السابق.

## CSS المُدخل

يتيح لك CSS المُدخل إمكانية حقن أنماط ويب مخصصة عالميًا. يمكن استخدامه مع `translationClasses` من `Rules`.

```
".immersive-translate-target-wrapper img { width: 16px; height: 16px }"
```

كما يمكن تصميم الموقع بطريقة أكثر شخصية، مثل مدير أنماط ويب عادي. (حتى باستخدام `display:none` لإزالة الإعلانات)

```css
.title {
  color: red;
}
```

## إعدادات المستخدم

تتيح لك الإعدادات تخصيص تكوين هذا الإضافة، مثل خدمات الترجمة، وخيارات الترجمة اللغوية المحددة لكل لغة، إلخ.

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
    "fingerCountToToggleTranslatePageWhenTouching": 4
  },
  "rules": [
    {
      "matches": "www.google.com",
      "selectors": [".class"]
    }
  ]
}
```

حقول القاعدة في `rules` يمكنها استخدام جميع الحقول الموجودة في `generalRule`. تمتلك `rules` الأولوية العليا، مع دمج `generalRule` والقواعد لتلك `القاعدة` عندما يتم مطابقة `قاعدة` معينة لموقع معين.

تقديم بعض الحقول الشائعة في الإعدادات.

### لا تظهر خدمات الترجمة غير المُعدة في لوحة الظهور

`"showUnconfiguredTranslationServiceInPopup": false`

### تكوين خدمات الترجمة

استخدم `translationService` لاختيار محرك الترجمة الافتراضي، والذي يدعم حاليًا:

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

استخدم `translationServices` لتكوين `apikey` لكل خدمة ترجمة، مزودو الخدمة المختلفون يحتاجون إلى معايير مختلفة، ويمكن طلب مفاتيح API الخاصة بهم في مركز المطورين لمواقعهم الإلكترونية.

على سبيل المثال، مترجم Tencent، تحتاج إلى تكوين `secretId`, `secretKey`. يمكنك التوجه إلى Tencent Cloud للتقديم على مفتاح API مع 5 ملايين حرف مجاني شهريًا. اطلع [هنا](/docs/services/tencent) على عملية التقديم.

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

حقل `matches`، استخدام هذه الخدمة لترجمة موقع ويب محدد.

حقل `limit`، الذي يحدد الحد الأقصى لعدد الطلبات في الثانية لهذه الخدمة (بعض الخدمات تحد من الحد الأقصى لعدد الطلبات في الثانية).

حقل `maxTextGroupLengthPerRequest`، الحد الأقصى لعدد الفقرات لكل طلب

حقل `maxTextLengthPerRequest`، الحد الأقصى لعدد الأحرف لكل طلب

`apiUrl` يسمح لك بتخصيص عنوان واجهة الترجمة.

### دائمًا ترجمة مواقع محددة

`translationUrlPattern` يُعدّ مواقع معينة دائمًا للترجمة، ومواقع لا تُترجم أبدًا.

- `matches` تهيئة تُترجم الموقع دائمًا.
- `excludeMatches` تهيئة مواقع لا تُترجم أبدًا.

يمكن أن تكون قيم التهيئة أسماء نطاقات أو عناوين URL مع `*`، مثل: `www.google.com/mail/*`

```json
"translationUrlPattern": {
    "matches": ["stackoverflow.com"],
    "excludeMatches": ["www.google.com/mail/*"]
}
```

### دائمًا ترجمة لغات محددة

translationLanguagePattern، يُهيئ اللغة التي يتم ترجمتها دائمًا واللغة التي لا تُترجم أبدًا.

- `matches` تهيئة اللغة التي يتم ترجمتها دائمًا، مثل `en`,
- `excludeMatches` تهيئة اللغات التي لا تُترجم.

### تنسيق عرض الترجمة

`translationTheme` هو تنسيق عرض الترجمة، ويدعم حاليًا الأنماط التالية:

```typescript
| "none"
| "dashed"
| "dotted"
| "underline"
| "mask"
| "paper"
| "highlight"
| "blockquote"
| "weakening"
| "italic"
| "bold"
| "thinDashed".
```

الاسم المقابل باللغة العربية:

```json
{
  "none": "بدون",
  "dashed": "خط متقطع",
  "dotted": "خط منقط",
  "underline": "خط تحتي مستقيم",
  "mask": "تأثير ضبابي",
  "paper": "تأثير ظل ورقة بيضاء",
  "highlight": "تسليط الضوء",
  "blockquote": "نمط الاقتباس",
  "weakening": "تضعيف",
  "italic": "مائل",
  "bold": "غامق",
  "thinDashed": "خط متقطع رفيع"
}
```

`translationThemePatterns` يتيح لك تكوين أنماط ترجمة مختلفة لمواقع ويب مختلفة.

```json
"translationThemePatterns": {
  "underline": {
    "matches": ["discord.com"]
  }
}
```

### ترجمة رسالة تدفق صفحة gpt الفئة

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

### القواعد

`rules` هو مصفوفة كائن تسمح لك بتكوين قواعد لمواقع خاصة، مثل جعل تويتر يترجم جزءًا معينًا من منطقة:

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

يمكن العثور على القواعد المدمجة الحالية [هنا](https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json).

تم اختيار بعض الحقول المهمة أدناه للتوضيح:

```typescript
export interface Rule {
  // مطابقة الموقع
  id?: string; // لكل قاعدة تكيف هويتها الخاصة، إذا أراد المستخدمون إعادة استخدام هذه القاعدة فوق هذا التغيير، يحتاجون إلى إضافة هذه الهوية المقابلة إلى قاعدتهم الخاصة لإعادة الاستخدام
  matches?: string | string[]; // هذه القاعدة ستطابق الموقع هنا فقط. هذه القاعدة ستطابق المواقع هنا فقط.
  excludeMatches?: string | string[]; // استبعاد مواقع محددة.
  selectorMatches?: string | string[]; // مطابقة مع محدد دون تحديد جميع العناوين
  excludeSelectorMatches?: string | string[]; // استبعاد القواعد، كما هو مذكور أعلاه.

  // تحديد نطاق الترجمات
  selectors?: string | string[]; // ترجمة العناصر التي تطابق فقط
  excludeSelectors?: string | string[]; // استبعاد العناصر، لا تترجم المطابقات
  excludeTags?: string | string[]; // استبعاد العلامات، لا تترجم العلامات المطابقة

  // إضافة نطاقات الترجمة بدلاً من الاستبدال
  additionalSelectors?: string | string[]; // إضافة نطاقات الترجمة. إضافة مواقع الترجمة إلى المناطق المترجمة بذكاء.
  additionalExcludeSelectors?: string | string[]; // إضافة استبعاد العناصر حتى لا تترجم الترجمة الذكية مواقع محددة.
  additionalExcludeTags?: string | string[]; // إضافة استبعاد العلامات

  // الإبقاء على الحالة الأصلية
  stayOriginalSelectors?: string | string[]; // العناصر المطابقة ستبقى كما هي. يستخدم عادة في علامات مواقع المنتديات.
  stayOriginalTags?: string | string[]; // العلامات المطابقة ستبقى كما هي، مثل `code`

  // الترجمات الإقليمية
  atomicBlockSelectors?: string | string[]; // محددات الكتل الإقليمية، العناصر المطابقة ستعامل ككل، لا تترجم في أقسام.
  atomicBlockTags?: string | string[]; // محددات علامات الكتل الإقليمية، كما هو مذكور أعلاه

  // كتلة أو مضمن
  extraBlockSelectors?: string | string[]; // محددات إضافية، العناصر المطابقة ستُعامل كعناصر كتلة، لا يتم ترجمتها إلى سطر واحد.
  extraInlineSelectors?: string | string[]; // محددات إضافية ستُستخدم كعناصر داخل السطر.

  inlineTags?: string | string[]; // الوسم المطابق سيُستخدم كعنصر داخل السطر
  preWhitespaceDetectedTags?: string | string[]; // الوسم المطابق سيُحاط تلقائيًا

  // أسلوب الترجمة
  translationClasses?: string | string | string[]; // إضافة فئات إضافية إلى الترجمة

  // الأنماط العالمية
  globalStyles?: Record<string, string>; // تعديل أنماط الصفحة، مفيد إذا تسببت الترجمة في إفساد تنسيق الصفحة.`
  globalAttributes?: Record<string, Record<string, string>>; // تعديل خصائص عناصر الصفحة

  // الأنماط المضمنة
  injectedCss?: string | string[]; // تضمين أنماط CSS
  additionalInjectedCss?: string | string[]; // أنماط CSS إضافية بدلاً من استبدالها.

  // السياق
  wrapperPrefix?: string; // بادئة منطقة الترجمة، تكون افتراضيًا ذكية، مع أو بدون فواصل سطر اعتمادًا على عدد الأحرف.
  wrapperSuffix?: string; // لاحقة منطقة الترجمة

  // عدد الأحرف لتغليف الترجمة
  blockMinTextCount?: number; // الحد الأدنى لعدد الأحرف لتغليف الترجمة ككتلة، وإلا فإن الترجمة تكون عنصرًا داخل السطر.
  blockMinWordCount?: number; // كما هو مذكور أعلاه. إذا كنت تريدها دائمًا بسطر جديد، يمكنك وضع 0 في كلاهما.

  // الحد الأدنى لعدد الأحرف التي يمكن ترجمتها من المحتوى
  containerMinTextCount?: number; // الحد الأدنى لعدد الأحرف التي يجب أن يحتويها عنصر قبل أن يتم ترجمته، يكون افتراضيًا 18
  paragraphMinTextCount?: number; // الحد الأدنى لعدد الأحرف للفقرة، أكبر من عدد الأحرف التي يجب أن يحتويها المحتوى. أي عدد أكبر من ذلك سيتم ترجمته
  paragraphMinWordCount?: number; // الحد الأدنى لعدد الكلمات في الفقرة الأصلية

  // فواصل سطر إجبارية للفقرات الطويلة
  lineBreakMaxTextCount?: number; // الحد الأقصى لعدد الأحرف في الفقرة ليتم إجبارها على الانقسام عند ترجمة فقرة طويلة.

  // متى تبدأ الترجمة.
  urlChangeDelay?: number; // كم مللي ثانية لتأخير الترجمة بعد دخول الصفحة. لانتظار تهيئة الصفحة، يكون افتراضيًا 250 مللي ثانية
  observeUrlChange?: boolean; // اكتشاف عندما يتغير عنوان url وبدء الترجمة مرة أخرى، صحيح بشكل افتراضي.

  // الجوال
  isShowUserscriptPagePopup?: boolean; // إظهار النافذة المنبثقة للصفحة على الأجهزة المحمولة. نافذة عائمة، صحيح بشكل افتراضي.
  fingerCountToToggleTranslagePageWhenTouching?: number; // يترجم عند لمس أربعة أصابع، يمكن تعيينها إلى 0، 2، 3، 4، 5

  // الترجمات الجارية بالذكاء الاصطناعي
  aiRule: {
    streamingSelector: string; // محدد لوضع علامة على العنصر الذي يتم ترجمته في صفحة الويب gpt
    messageWrapperSelector: string; // محدد جسم الرسالة
    streamingChange: boolean; // ما إذا كانت الرسالة تُحدث بشكل تدريجي أو كامل لتكرار صفحة الويب gpt. gpt هو تدريجي
  };
}
```

**المزيد من الشرح**

الفرق بين الكتلة والعناصر داخل السطر، إذا كنت تريد معرفة المزيد يمكنك مشاهدة [هنا](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements#inline)

- العنصر الكتلي يشغل سطرًا واحدًا، والعناصر الكتلية المجاورة كل منها يشغل سطرًا جديدًا.
- العنصر داخل السطر لا يشغل سطرًا واحدًا؛ العناصر داخل السطر المجاورة مرتبة على نفس السطر، ولا يتم إنشاء سطر جديد حتى يكون هناك الكثير في سطر واحد.