---
sidebar_position: 5
---

# JS SDK

يساعدك Immersive Translate JS SDK في تنفيذ الترجمة الثنائية اللغة على موقع الويب الخاص بك.

## كيفية الاستخدام

1. تهيئة Immersive Translate:

```js
<script>
  window.immersiveTranslateConfig = {
    pageRule: {}
  }
</script>
```

2. أضف كود `script` التالي إلى صفحة الويب الخاصة بك

```html
<script src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"></script>
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

## المعلمات

باستخدام `pageRule`، يمكنك تخصيص تكوين الموقع، وتحديد المحتوى الذي يحتاج إلى الترجمة أو تعديل أنماط صفحة الويب.

```js
initImmersiveTranslate({
  pageRule: {
    selectors: [".text"],
    excludeSelectors: ["nav", "footer"],
  },
});
```

استخدام `selectors` سيقوم بتجاوز نطاق الترجمة الذكي، وترجمة العناصر التي تتطابق مع المحدد فقط.

استخدام `excludeSelectors` يمكن أن يستبعد العناصر من الترجمة.

استخدام `selectors.add` سيضيف بعض المحددات فوق المحددات الافتراضية.

استخدام `selectors.remove` سيزيل بعض المحددات من المحددات الافتراضية.

إذا كنت ترغب في ترجمة منطقة معينة واعتبار عنصر ككل دون تقسيمه إلى أسطر، يمكنك استخدام محدد `atomicBlockSelectors`. لاحظ أنك تحتاج إلى تحديد العناصر باستخدام `selectors` قبل استخدام `atomicBlockSelectors`.

```json
{
  "selectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"],
  "atomicBlockSelectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"]
}
```

تفسيرات إضافية لمعلمات `pageRule`:

```typescript
export interface PageRule {
  excludeMatches?: string | string[]; // استبعاد مواقع ويب محددة.
  selectorMatches?: string | string[]; // المطابقة باستخدام المحددات دون تحديد جميع عناوين URL
  excludeSelectorMatches?: string | string[]; // استبعاد القواعد، كما هو موضح أعلاه.

  // تحديد نطاق الترجمة
  selectors?: string | string[]; // ترجمة العناصر المطابقة فقط
  excludeSelectors?: string | string[]; // استبعاد العناصر، لا تترجم العناصر المطابقة
  excludeTags?: string | string[]; // استبعاد العلامات، لا تترجم العلامات المطابقة

  // إضافة نطاق الترجمة، وليس تجاوز
  additionalSelectors?: string | string[]; // إضافة نطاق الترجمة. إضافة مواقع الترجمة في مناطق الترجمة الذكية.
  additionalExcludeSelectors?: string | string[]; // إضافة عناصر مستبعدة لمنع الترجمة الذكية في مواقع محددة.
  additionalExcludeTags?: string | string[]; // إضافة علامات مستبعدة

  // الاحتفاظ بالأصل
  stayOriginalSelectors?: string | string[]; // ستبقى العناصر المطابقة أصلية. تستخدم عادةً للعلامات على مواقع المنتديات.
  stayOriginalTags?: string | string[]; // ستبقى العلامات المطابقة أصلية، مثل `code`

  // ترجمة المنطقة
  atomicBlockSelectors?: string | string[]; // محدد المنطقة، ستعتبر العناصر المطابقة ككل، ولن تترجم في أجزاء
  atomicBlockTags?: string | string[]; // محدد علامة المنطقة، كما هو موضح أعلاه

  // كتلة أو خط
  extraBlockSelectors?: string | string[]; // محددات إضافية، ستعتبر العناصر المطابقة كعناصر كتلة، تشغل سطرًا واحدًا.
  extraInlineSelectors?: string | string[]; // محددات إضافية، ستعتبر العناصر المطابقة كعناصر خطية.

  inlineTags?: string | string[]; // ستعتبر العلامات المطابقة كعناصر خطية
  preWhitespaceDetectedTags?: string | string[]; // ستقوم العلامات المطابقة بتغليف الأسطر تلقائيًا

  // أنماط الترجمة
  translationClasses?: string | string | string[]; // إضافة فئات إضافية إلى الترجمة

  // الأنماط العالمية
  globalStyles?: Record<string, string>; // تعديل أنماط الصفحة، مفيد عندما تتسبب الترجمات في اضطراب الصفحة.
  globalAttributes?: Record<string, Record<string, string>>; // تعديل سمات عناصر الصفحة

  // الأنماط المدمجة
  injectedCss?: string | string[]; // تضمين أنماط CSS
  additionalInjectedCss?: string | string[]; // إضافة أنماط CSS بدلاً من تجاوزها مباشرة.

  // السياق
  wrapperPrefix?: string; // بادئة منطقة الترجمة، الافتراضي هو ذكي، يقرر ما إذا كان سيتم تغليف الأسطر بناءً على عدد الأحرف.
  wrapperSuffix?: string; // لاحقة منطقة الترجمة

  // عدد أحرف تغليف الترجمة
  blockMinTextCount?: number; // الحد الأدنى لعدد الأحرف للترجمة ككتلة، وإلا ستكون الترجمة كعنصر خطي.
  blockMinWordCount?: number; // نفس ما سبق. لتغليف الأسطر دائمًا، قم بتعيين كلاهما إلى 0.

  // الحد الأدنى لعدد الأحرف للمحتوى القابل للترجمة
  containerMinTextCount?: number; // الحد الأدنى لعدد الأحرف للعناصر التي سيتم ترجمتها أثناء التعرف الذكي، الافتراضي هو 18
  paragraphMinTextCount?: number; // الحد الأدنى لعدد الأحرف للفقرة الأصلية، سيتم ترجمة المحتوى الأكبر من العدد
  paragraphMinWordCount?: number; // الحد الأدنى لعدد الكلمات للفقرة الأصلية

  // عدد أحرف كسر السطر القسري للفقرات الطويلة
  lineBreakMaxTextCount?: number; // الحد الأقصى لعدد الأحرف لكسر السطر القسري عند ترجمة الفقرات الطويلة.

  // توقيت بدء الترجمة
  urlChangeDelay?: number; // التأخير بالمللي ثانية قبل بدء الترجمة بعد دخول الصفحة. الافتراضي هو 250 مللي ثانية لانتظار تهيئة صفحة الويب.

  // الترجمة المتدفقة بالذكاء الاصطناعي
  aiRule: {
    streamingSelector: string; // محدد صفحة GPT الذي يحدد العنصر المترجم
    messageWrapperSelector: string; // محدد جسم الرسالة
    streamingChange: boolean; // تحديث تدريجي أو كامل للرسائل المتكررة في صفحات GPT-like. GPT هو تدريجي
  };
}
```