---
sidebar_position: 4
---

# خيارات التخصيص المتقدمة

هذه الصفحة موجهة للمستخدمين المتقدمين الذين لديهم معرفة أساسية بـ HTML/CSS/JSON. تسمح التكوينات المتقدمة برفع مستوى التخصيص بشكل كبير، لكنها قد تجعل من السهل كتابة إعدادات "تبدو صحيحة لكنها لا تعمل"، لذا يُنصح بالنسخ الاحتياطي قبل التحرير.

## نصائح قبل البدء

- يمكن الدخول من [إعدادات المطور](https://dash.immersivetranslate.com/#developer).
- يُنصح بحفظ نسخة احتياطية من User Config / User Rules قبل التحرير، لتجنب تجاهل الإعدادات في حال وجود أخطاء تنسيقية.
- يرجى الاعتماد على "Click to expand the final config" كمرجع نهائي للحقول والقيم الافتراضية والخدمات المتاحة.

## نقاط الدخول وأولوية التفعيل

نقاط الدخول الشائعة (ضمن إعدادات المطور):
- Edit Full User Config: التكوين الكامل (يشمل `rules`، وخدمات الترجمة، والأنماط، إلخ).
- Edit User Rules: تحرير مصفوفة `rules` فقط (هذا الخيار يقبل المصفوفة فقط، لا تستخدم `{ "rules": [...] }`).
- Injected CSS: إدراج CSS بشكل عام على كل المواقع.

الأولوية (من الأعلى إلى الأدنى): `rules` المطابقة > `generalRule` > التكوين الافتراضي الداخلي.
عند مطابقة قاعدة معينة (`rule`)، يتم دمجها مع `generalRule` وتعطى الأفضلية لما في `rule`.

## البدء السريع (الاحتياجات الشائعة)

### 1) ترجمة محتوى موقع معين فقط

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

### 2) دائماً/أبداً ترجمة موقع معيّن

```json
{
  "translationUrlPattern": {
    "matches": ["stackoverflow.com"],
    "excludeMatches": ["www.google.com/mail/*"]
  }
}
```

### 3) استخدام خدمات ترجمة مختلفة لمواقع مختلفة

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

### 4) تخصيص نمط الترجمة حسب الموقع

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

### 5) تصحيح مشاكل الأسلوب الناتجة عن الترجمة باستخدام CSS

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

### 6) عدم إظهار خدمات الترجمة غير المُكَوَّنة داخل لوحة الإضافات

```json
{
  "showUnconfiguredTranslationServiceInPopup": false
}
```

## القواعد والمطابقة

### دمج القواعد

- `generalRule`: القاعدة الموحدة لجميع المواقع.
- `rules`: قواعد مخصصة على مستوى الموقع لها أولوية أعلى.

معظم حقول `generalRule` يمكن استخدامها في عناصر `rules`.

### صيغ matches المعتادة

يدعم `matches` سلسلة أو مصفوفة:
- اسم المجال: `example.com`
- رابط كامل: `https://example.com/path/`
- نمط وايلدكارد: `https://*/*q=*`
- مطابقة الكل: `*` / `*://*` / `*://*/*`
- ملفات محلية: `file://*`

ملاحظة: `*.twitter.com` يطابق النطاقات الفرعية فقط، ولا يطابق المجال الجذري `twitter.com`.

### selectors / excludeSelectors

- `selectors`: يترجم عناصر المطابقة فقط (يستبدل المجال الافتراضي).
- `excludeSelectors`: يستثني عناصر معينه من الترجمة.

إذا كنت ترغب في "إضافة أو إزالة" من النطاق الافتراضي فقط، استخدم `.add` / `.remove` (انظر القسم التالي).

### الوراثة والتعديل المتزايد (.add / .remove)

بالنسبة للحقول ذات النوع array/object، يمكنك استخدام `.add` / `.remove` للتعديل المتزايد.
ننصح باستخدامها لتجنب استبدال القاعدة الافتراضية:

```json
[
  {
    "id": "twitter",
    "selectors.add": ["[data-testid='tweetText'] a"],
    "excludeSelectors.add": ["header"]
  }
]
```

### الحقول الشائعة بإيجاز

للمطابقة:
- `matches` / `excludeMatches`
- `selectorMatches` / `excludeSelectorMatches`

نطاق الترجمة:
- `selectors` / `excludeSelectors` / `excludeTags`
- `stayOriginalSelectors` / `stayOriginalTags`
- `extraInlineSelectors` / `extraBlockSelectors`

الأنماط والتخطيط:
- `translationClasses`: إضافة class إضافي للترجمة
- `globalStyles` / `globalAttributes`
- `injectedCss` / `additionalInjectedCss`
- `wrapperPrefix` / `wrapperSuffix`
- `blockMinTextCount` / `blockMinWordCount`

التوقيت والجوال:
- `urlChangeDelay` / `observeUrlChange`
- `isShowUserscriptPagePopup`

### ترجمة رسائل البث المباشر على نمط GPT

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

للمزيد من الشرح، راجع "الملحق: مرجع حقول القاعدة" في نهاية الوثيقة.

## منطق مطابقة matches (شرح مبسط)

- اسم المجال فقط (دون `*` ودون مسار): يُقارن hostname فقط.
- رابط كامل (بدون `*`): يُقارن البروتوكول + المضيف + المنفذ + المسار.
- إذا كان يحوي `*` أو البروتوكول غير محدد: تُطبق مطابقة الوايلدكارد (يدعم http/https/file افتراضياً).

أمثلة شائعة:
- `twitter.com` ✅ يطابق `https://twitter.com/home`
- `*.twitter.com` ✅ يطابق `https://mobile.twitter.com`، ❌ لا يطابق `https://twitter.com`
- `https://twitter.com/home` يطابق الرابط بالكامل فقط.
- `twitter.com/*` يطابق جميع المسارات تحت `twitter.com`

## مثال تَخْصِيص لموقع (تويتر)

القواعد الافتراضية الداخلية لموقع تويتر (مقتطف)، لشرح طريقة استعمال `selectors` / `excludeSelectors` / `globalStyles`:

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

- `selectors`: تترجم محتوى التغريدة فقط لتجنب ترجمة الأزرار أو الاسم.
  ![tweet](https://s.immersivetranslate.com/assets/r2-uploads/tweet.png)
- `excludeSelectors`: استثناء الأزرار والتنقلات التفاعلية.
  ![twitter-follow](https://s.immersivetranslate.com/assets/r2-uploads/twitter-follow.png)
- `globalStyles`: إزالة الحد على عدد السطور، حتى لا يُقطَع النص المترجم.
  ![صفحة المستخدم](https://s.immersivetranslate.com/assets/r2-uploads/twitterUser.png)

## تخصيص التوافق مع المواقع

يمكنك إعادة استخدام قاعدة داخلية عبر `id` ثم التعديل عليها باستخدام `.add` / `.remove`:

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

ملاحظات:
- `id` يسمح لك بوراثة القاعدة الداخلية لتفادي تكرار `matches`.
- الأفضل تعديل المصفوفات باستخدام `.add` / `.remove`.

بعض معرفات القواعد الداخلية الشائعة:
- `isEbook`: قارئ ملفات epub.
- `isEbookBuilder`: منشئ الكتاب الإلكتروني ثنائي اللغة.
- `pdf`: مستند PDF مع عرض ثنائي اللغة.

جميع القواعد الداخلية:
- `https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json`

## إعدادات خدمة الترجمة

- `translationService`: محرك الترجمة الافتراضي.
- `translationServices`: ضبط الخدمة وتجاوز مواقع محددة.
- `showUnconfiguredTranslationServiceInPopup`: يُخفي الخدمات غير المُعَدَّة من الواجهة.

مثال (على تنسنت):

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

شرح:
- `matches`: المواقع التي تُفعَّل عليها الخدمة.
- `limit`: معدل تحديد الطلبات (عدد الطلبات في الثانية).
- `maxTextGroupLengthPerRequest` / `maxTextLengthPerRequest`: حجم الطلب الأقصى للترجمة.
- `apiUrl`: رابط مخصص للخدمة إن رغبت.

### ضبط مهلة الطلب (الحد الأقصى لزمن الانتظار)

يمكن تعيين المهلة (timeout) لكل خدمة بالملي ثانية (ms). ولخدمات Pro يمكن تخصيص `proRequestTimeout` بشكل منفصل.

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

ملاحظات:
- إذا زادت المهلة، يزداد زمن الانتظار؛ إذا قلت قد يحدث خطأ في الترجمة بسبب النفاد.
- القيم الافتراضية تختلف حسب الخدمة، راجع التكوين النهائي.
- `proRequestTimeout` يفعل فقط عند `provider` = `pro` (خدمات الترجمة المدفوعة).

## اللغة واستراتيجيات الترجمة

### دائماً/أبداً الترجمة للغة معينة

```json
{
  "translationLanguagePattern": {
    "matches": ["en"],
    "excludeMatches": ["zh"]
  }
}
```

### تحديد اللغة المصدر لمواقع معينة

```json
{
  "sourceLanguageUrlPattern": {
    "en": {
      "matches": ["*.google.com"]
    }
  }
}
```

## إعدادات عامة شائعة أخرى

### السماح بعرض وسوم HTML في الترجمة

لتفعيل عرض وسوم HTML في النص المترجم:

```json
{
  "enableRenderHtmlTag": true
}
```

## أنماط الترجمة والمواضيع

الأنماط المدعومة في `translationTheme` (تحقق من التكوين النهائي للأنماط المحدثة):

```text
none, grey, dashed, dashedBorder, solidBorder, dotted, underline, mask, opacity,
paper, dividingLine, highlight, marker, marker2, blockquote, weakening, italic,
bold, thinDashed, nativeDotted, wavy, nativeDashed, nativeUnderline, background
```

لتطبيق نمط حسب الموقع:

```json
{
  "translationThemePatterns": {
    "highlight": {
      "matches": ["discord.com"]
    }
  }
}
```

## إعدادات AI / الخيارات المتقدمة

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

### تخصيص رؤوس وجسم الطلب

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

### تخصيص نماذج Gemini

تأتي نماذج Gemini بإعدادات داخلية افتراضية؛ لتجاوزها استخدم `modelsOverrides` لتخصيص كل نموذج:

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

ملاحظة: `modelsOverrides` متاح لخدمات AI الأخرى أيضاً وسيطبق الخصائص على النماذج المطابقة.

### الالتزام الصارم بالتعليمات المخصصة

> لتقليل ظاهرة "الهلوسة" في النتائج، تحتوي الإضافة آلية تحقق جودة الترجمة عبر مقارنة عدد الرموز (Token) بين النص المرسل والمستلم. إذا كان الرقم شاذاً جداً، يعتبر فاشلاً ويتم التبديل لخدمة أخرى.
> إذا كانت التعليمات مخصصة لمهام غير الترجمة (مثل التلخيص أو إعادة الصياغة)، قد يجعل هذا النسبة غير منطقية. حينها يمكنك تفعيل الوضع الصارم لتجاوز التحقق.

```json
{
  "translationServices": {
    "claude": {
      "strictPrompt": true
    }
  }
}
```

### تخصيص تعليمات بلغات مختلفة (مثال مختصر)

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

## المصطلحات والترجمة الآلية

تمت إضافة دعم [مصطلحات AI](https://dash.immersivetranslate.com/#terms) (فعال فقط عند استخدام خدمات AI).

بشكل افتراضي لا تطبق المصطلحات عند الترجمة الآلية (لأنها تعتمد عادةً على الاستبدال بالاحتياطي وقد تؤثر جودة الترجمة). لتفعيلها بالقوة (غير مستحسن):

```json
{
  "enableMachineTranslateTerms": true
}
```

## دورة تنظيف الكاش

تقوم الإضافة بحذف ذاكرة الترجمة كل 30 يوم افتراضياً لتجنب مشاكل بطء الأداء.

```json
{
  "cacheMaxAgeDay": 30
}
```

## Injected CSS و globalStyles

- Injected CSS: إدراج CSS بشكل عام لإصلاح مشاكل على مستوى الصفحة.
- globalStyles: أنماط خاصة على مستوى القاعدة لموقع معين.

مثال على Injected CSS:

```css
.immersive-translate-target-wrapper img {
  width: 16px;
  height: 16px;
}
```

## استكشاف الأخطاء الشائعة

- `*.twitter.com` لا يشمل `twitter.com` نفسه، اكتب الاثنين لو أردت.
- `selectors` تستبدل المجال الافتراضي؛ استخدم `.add` / `.remove` قدر الإمكان.
- عند كتابة `matches` كـ `example.com/path` ستستخدم مطابقة الوايلدكارد. تأكد من ما يناسبك (رابط كامل أم لا).
- إذا لم تنجح الإعدادات: تحقق من التكوين النهائي لجمع الإعدادات، ثم أعد تحميل الصفحة.
- وجود فاصلة اضافية في نهاية JSON يلغي التكوين كاملاً.

## الملحق: مرجع حقول القاعدة Rule

تجد أدناه مرجع الحقول الأكثر شيوعاً، أما القيم النهائية راجع التكوين النهائي.
ملاحظة: لحقول المصفوفة أو الكائنات، يمكنك استخدام `.add` / `.remove` للتعديل المتزايد.

```typescript
export interface Rule {
  // مطابقة الموقع
  id?: string; // معرف قاعدة داخلية، لاستخدام القاعدة الافتراضية
  matches?: string | string[]; // هذه القاعدة مطبقة فقط على المواقع هذه
  excludeMatches?: string | string[]; // استثناء مواقع معينة من القاعدة
  selectorMatches?: string | string[]; // مطابقة باستخدام selector بدون رابط
  excludeSelectorMatches?: string | string[]; // كما أعلاه، لكن للاستثناء

  // تحديد نطاق الترجمة
  selectors?: string | string[]; // عناصر لترجمتها
  excludeSelectors?: string | string[]; // عناصر لاستثنائها من الترجمة
  excludeTags?: string | string[]; // تاج HTML لاستثنائه

  // إضافة نطاقات ترجمة (إن لم تعمل استخدم selectors.add/remove)
  additionalSelectors?: string | string[]; // إضافة عناصر للترجمة
  additionalExcludeSelectors?: string | string[]; // إضافة عناصر لاستثنائها
  additionalExcludeTags?: string | string[]; // إضافة تاج للاستثناء (بعض الإصدارات قد لا تدعم)

  // إبقاء العناصر بحالتها الأصلية
  stayOriginalSelectors?: string | string[]; // عناصر تبقى كما هي
  stayOriginalTags?: string | string[]; // تاج HTML يبقى كما هو (مثل code)

  // كتل أو مضمونة بالصف
  extraBlockSelectors?: string | string[]; // عناصر تعتبر block
  extraInlineSelectors?: string | string[]; // عناصر تعتبر inline
  inlineTags?: string | string[]; // تاج باعتباره inline
  preWhitespaceDetectedTags?: string | string[]; // تاج مع معالجة الفراغات

  // أنماط الترجمة
  translationClasses?: string | string[]; // إضافة class إضافي

  // أنماط عامة
  globalStyles?: Record<string, string>; // تعديل CSS للموقع
  globalAttributes?: Record<string, Record<string, string | null>>; // تعديل خواص عناصر الصفحة

  // تضمين CSS
  injectedCss?: string | string[]; // CSS مدرج
  additionalInjectedCss?: string | string[]; // CSS مُضاف

  // السياق
  wrapperPrefix?: string; // بادئة لمنطقة الترجمة
  wrapperSuffix?: string; // لاحقة لمنطقة الترجمة

  // عدد الأحرف لانتقال الترجمة لسطر جديد
  blockMinTextCount?: number; // أدنى عدد حروف للكتلة
  blockMinWordCount?: number; // أدنى عدد كلمات للكتلة

  // أدنى عدد حروف يمكن ترجمته
  containerMinTextCount?: number; // الحد الأدنى لاكتشاف عناصر الترجمة الذكية
  paragraphMinTextCount?: number; // الحد الأدنى لأحرف الفقرة
  paragraphMinWordCount?: number; // الحد الأدنى للكلمات في الفقرة

  // الحد الأقصى للحروف قبل التقسيم
  lineBreakMaxTextCount?: number; // التقسيم حسب طول السطر

  // توقيت تشغيل الترجمة
  urlChangeDelay?: number; // تأخير الترجمة بعد الدخول
  observeUrlChange?: boolean; // إعادة الترجمة إذا تغير الرابط

  // الجوّال
  isShowUserscriptPagePopup?: boolean; // عرض نافذة عائمة في الجوّال
  fingerCountToToggleTranslagePageWhenTouching?: number; // متوقف عن العمل

  // البث المباشر للترجمة بخدمات AI
  aiRule?: {
    streamingSelector: string; // selector تعليم العنصر الجاري ترجمته
    messageWrapperSelector: string; // عنصر الرسالة
    streamingChange: boolean; // هل التحديث تدريجي
  };
}
```
