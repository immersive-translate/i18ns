# DeepL

## الوصول المباشر إلى خدمات الترجمة من DeepL بعد فتح [عضوية Immersive Translate Pro](https://immersivetranslate.com/en/pricing/) (موصى به)

[تعرف على المزيد](https://immersivetranslate.com/en/pricing/)

## الحصول على واجهة برمجة التطبيقات الرسمية من DeepL عبر DeepL

1. المقدمة الرسمية: [DeepL API](https://www.deepl.com/en/pro#developer)

   - لاحظ أن: [DeepL API](https://www.deepl.com/en/pro#developer) و [DeepL Pro](https://www.deepl.com/pro) هما نوعان مختلفان من الحسابات، وحساب [DeepL API](https://www.deepl.com/en/pro/select-country#developer).

2. [لماذا](https://www.deepl.com/en/whydeepl) تختار DeepL؟

   - الإنجليزية ⇄ الصينية أكثر دقة 5 مرات
   - الإنجليزية ⇄ اليابانية أكثر دقة 6 مرات
   - محرك الترجمة يعتمد على تقنية الذكاء الاصطناعي (الشبكات العصبية)

3. يتم تقسيم Deepl API إلى [Free API و Pro API](https://www.deepl.com/en/pro#developer)

   - يوفر Free API 500,000 حرف مجاني شهريًا.
   - [الرسوم الرسمية](https://www.deepl.com/en/pro#developer) لـ Pro API هي: 25 دولار لكل مليون حرف.
   - بالنسبة للمستخدمين ذوي التردد العالي، فإن كمية الأحرف المستهلكة في الشهر تبلغ حوالي 10 مليون حرف، والسعر حوالي: 250 دولار أمريكي

4. للتسجيل للحصول على حساب وفتح [DeepL API](https://www.deepl.com/en/pro#developer).

## المشاكل الشائعة

### 1. المفتاح المدخل غير متاح.

DeepL API Pro و DeepL Pro هما نوعان من الحسابات، المفتاح Auth الذي يمكن استخدامه في Immersive Translate هو حساب DeepL API، يرجى النقر هنا لـ [DeepL API Pro](https://www.deepl.com/en/pro/select-country#developer)

### 2. استكشاف أخطاء 401 و 403 في المصادقة

تحدث هذه الأخطاء عادةً عندما تستخدم نوعًا خاطئًا من مفتاح المصادقة. يرجى ملاحظة:

1. تقدم DeepL منتجين مختلفين: DeepL Pro (خدمة الترجمة) و DeepL API (واجهة المطور)
2. المفاتيح الموجودة في إعدادات حساب DeepL Pro الخاص بك **غير متوافقة** مع استدعاءات API
3. تحتاج إلى التسجيل خصيصًا للحصول على حساب DeepL API للحصول على مفتاح API
4. يتم تحديد مفاتيح DeepL Free API من خلال نهايتها بـ `:fx`
5. مفاتيح DeepL Pro API لا تحتوي على اللاحقة `:fx` وتظهر كسلسلة عادية من الأحرف

يرجى التأكد من أنك قد سجلت بشكل صحيح لخدمة DeepL API، وليس فقط خدمة الترجمة DeepL Pro.

### 3. 456، تم الوصول إلى الحصة للمستخدم.

تم تجاوز الحد الأقصى الرسمي للاستخدام لكل مستخدم من DeepL، قد تكون قد انتهكت سياسة الاستخدام العادل لـ DeepL وينصح بتجنب مثل هذا السلوك. إذا كنت مشتركًا مدفوعًا، سيتم إعادة تعيين الاستخدام تلقائيًا في الشهر المقبل.
