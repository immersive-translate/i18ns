---
sidebar_position: 5
---

# JS SDK

يمكن لـ JS SDK الخاص بالترجمة الغامرة مساعدتك في تحقيق الترجمة الثنائية اللغة على موقعك.

## كيفية الاستخدام

> قبل تصحيح أخطاء JS SDK، يرجى إغلاق امتداد الترجمة الغامرة

1. إعداد معلمات التهيئة (يرجى ملاحظة أن عدم تعيين immersiveTranslateConfig سيؤدي إلى فشل تهيئة JS SDK، يمكنك تعيين كائن فارغ)

```html
<script>
  window.immersiveTranslateConfig = {
    pageRule: {},
  };
</script>
```

2. أضف كود `script` التالي إلى صفحتك قبل `</head>`

```html
<script
  async
  src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"
></script>
```

مثال

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
    <div class=".text">
      <p>
        Night gathers, and now my watch begins. It shall not end until my death.
        I shall take no wife, hold no lands, father no children. I shall wear no
        crowns and win no glory. I shall live and die at my post.
      </p>
    </div>
  </body>
</html>
```

## المعلمات

- `pageRule`
  يمكن تخصيص إعدادات الموقع لتحديد المحتوى الذي يحتاج إلى الترجمة أو تعديل أنماط الصفحة.
- `isAutoTranslate`
  الترجمة التلقائية الفورية

```html
<script>
  window.immersiveTranslateConfig = {
    isAutoTranslate: true,
    pageRule: {
      selectors: [".text"],
      excludeSelectors: ["nav", "footer"],
    },
  };
</script>
```

استخدام `selectors` سيغطي نطاق الترجمة الذكية، ويترجم فقط العناصر التي تطابق هذا المحدد.

استخدام `excludeSelectors` يمكن أن يستبعد العناصر، ولا يترجم هذا الموقع.

استخدام `selectors.add` سيضيف بعض المحددات على الأساس الافتراضي

استخدام `selectors.remove` سيقلل بعض المحددات على الأساس الافتراضي

إذا كنت ترغب في ترجمة منطقة معينة، واعتبار العنصر ككل دون تقسيمه إلى أسطر، يمكنك استخدام محدد `atomicBlockSelectors`. يجب ملاحظة أنه قبل استخدام `atomicBlockSelectors` يجب أولاً استخدام `selectors` للاختيار.

```json
{
  "selectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"],
  "atomicBlockSelectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"]
}
```

مزيد من الشرح لمعلمات `pageRule`:

```typescript
export interface PageRule {
  excludeMatches?: string | string[]; // استبعاد مواقع معينة.
  selectorMatches?: string | string[]; // مطابقة باستخدام المحددات دون الحاجة إلى تحديد جميع عناوين URL
  excludeSelectorMatches?: string | string[]; // قواعد الاستبعاد، كما هو موضح أعلاه.

```markdown
  // نطاق الترجمة المحدد
  selectors?: string | string[]; // ترجمة العناصر المطابقة فقط
  excludeSelectors?: string | string[]; // استبعاد العناصر، لا تترجم العناصر المطابقة
  excludeTags?: string | string[]; // استبعاد العلامات، لا تترجم العلامات المطابقة

  // إضافة نطاق الترجمة بدلاً من الاستبدال
  additionalSelectors?: string | string[]; // إضافة نطاق الترجمة. في منطقة الترجمة الذكية، إضافة موقع الترجمة.
  additionalExcludeSelectors?: string | string[]; // إضافة استبعاد العناصر، لا تترجم الترجمة الذكية موقعًا محددًا.
  additionalExcludeTags?: string | string[]; // إضافة استبعاد العلامات

  // الحفاظ على الأصل
  stayOriginalSelectors?: string | string[]; // العناصر المطابقة ستبقى كما هي. تستخدم عادةً في علامات مواقع المنتديات.
  stayOriginalTags?: string | string[]; // العلامات المطابقة ستبقى كما هي، مثل `code`

  // ترجمة المنطقة
  atomicBlockSelectors?: string | string[]; // محددات المنطقة، العناصر المطابقة ستعتبر ككل، ولن تترجم بشكل مجزأ
  atomicBlockTags?: string | string[]; // محددات العلامات للمنطقة، كما هو مذكور أعلاه

  // Block أو Inline
  extraBlockSelectors?: string | string[]; // محددات إضافية، العناصر المطابقة ستعتبر كعناصر block، تحتل سطرًا منفردًا.
  extraInlineSelectors?: string | string[]; // محددات إضافية، العناصر المطابقة ستعتبر كعناصر inline.

  inlineTags?: string | string[]; // العلامات المطابقة ستعتبر كعناصر inline
  preWhitespaceDetectedTags?: string | string[]; // العلامات المطابقة ستقوم بتغيير السطر تلقائيًا

  // نمط الترجمة
  translationClasses?: string | string | string[]; // إضافة فئة إضافية للترجمة

  // النمط العام
  globalStyles?: Record<string, string>; // تعديل نمط الصفحة، إذا تسببت الترجمة في اضطراب الصفحة، يكون هذا مفيدًا.
  globalAttributes?: Record<string, Record<string, string>>; // تعديل خصائص عناصر الصفحة

  // تضمين النمط
  injectedCss?: string | string[]; // تضمين نمط CSS
  additionalInjectedCss?: string | string[]; // إضافة نمط CSS، بدلاً من الاستبدال المباشر.

  // السياق
  wrapperPrefix?: string; // بادئة منطقة الترجمة، الافتراضي هو smart، يحدد ما إذا كان يجب تغيير السطر بناءً على عدد الكلمات.
  wrapperSuffix?: string; // لاحقة منطقة الترجمة

  // عدد الأحرف لتغيير السطر في الترجمة
  blockMinTextCount?: number; // الحد الأدنى لعدد الأحرف لترجمة كـ block، وإلا ستكون الترجمة كعنصر inline.
  blockMinWordCount?: number; // كما هو مذكور أعلاه. إذا كنت ترغب في أن تكون دائمًا على سطر جديد، يمكنك ملء 0.

  // الحد الأدنى لعدد الأحرف القابلة للترجمة
  containerMinTextCount?: number; // عند التعرف الذكي، الحد الأدنى لعدد الأحرف التي يجب أن يحتويها العنصر ليتم ترجمته، الافتراضي هو 18
  paragraphMinTextCount?: number; // الحد الأدنى لعدد الأحرف في الفقرة الأصلية، سيتم ترجمة المحتوى الأكبر من الرقم
  paragraphMinWordCount?: number; // الحد الأدنى لعدد الكلمات في الفقرة الأصلية

  // عدد الأحرف القصوى لتغيير السطر في الفقرات الطويلة
  lineBreakMaxTextCount?: number; // عند ترجمة الفقرات الطويلة، الحد الأقصى لعدد الأحرف في الفقرة لإجبارها على تغيير السطر.
```

```markdown
// توقيت بدء الترجمة
urlChangeDelay?: number; // بعد الدخول إلى الصفحة، كم ملي ثانية يجب الانتظار قبل بدء الترجمة. حاليًا، القيمة الافتراضية هي 250ms لانتظار تهيئة الصفحة

// ترجمة AI streaming
aiRule: {
    streamingSelector: string; // محدد العنصر الذي يتم ترجمته في صفحة gpt
    messageWrapperSelector: string; // محدد نص الرسالة
    streamingChange: boolean; // هل الرسائل المتكررة في صفحة gpt هي تحديثات تزايدية أم كاملة. gpt هو تزايدي
};
```