---
sidebar_position: 5
---

# JS SDK

Immersive Translate JS SDK помогает вам реализовать двуязычный перевод на вашем веб-сайте.

## Как использовать

1. Инициализируйте Immersive Translate:

```js
<script>
  window.immersiveTranslateConfig = {
    pageRule: {}
  }
</script>
```

2. Добавьте следующий код `script` на вашу веб-страницу

```html
<script src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"></script>
```

Пример

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

## Параметры

С помощью `pageRule` вы можете настроить конфигурацию веб-сайта, решая, какой контент нужно перевести или изменяя стили веб-страницы.

```js
initImmersiveTranslate({
  pageRule: {
    selectors: [".text"],
    excludeSelectors: ["nav", "footer"],
  },
});
```

Использование `selectors` переопределит умный диапазон перевода, переводя только элементы, соответствующие селектору.

Использование `excludeSelectors` может исключить элементы из перевода.

Использование `selectors.add` добавит некоторые селекторы поверх стандартных.

Использование `selectors.remove` удалит некоторые селекторы из стандартных.

Если вы хотите перевести определенную область и рассматривать элемент как единое целое, не разбивая его на строки, вы можете использовать селектор `atomicBlockSelectors`. Обратите внимание, что вам нужно выбрать элементы с помощью `selectors` перед использованием `atomicBlockSelectors`.

```json
{
  "selectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"],
  "atomicBlockSelectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"]
}
```

`pageRule` больше объяснений параметров:

```typescript
export interface PageRule {
  excludeMatches?: string | string[]; // Исключить конкретные веб-сайты.
  selectorMatches?: string | string[]; // Совпадение с использованием селекторов без указания всех URL
  excludeSelectorMatches?: string | string[]; // Исключить правила, то же самое, что и выше.

  // Указать диапазон перевода
  selectors?: string | string[]; // Переводить только совпадающие элементы
  excludeSelectors?: string | string[]; // Исключить элементы, не переводить совпадающие элементы
  excludeTags?: string | string[]; // Исключить теги, не переводить совпадающие теги

  // Добавить диапазон перевода, не переопределять
  additionalSelectors?: string | string[]; // Добавить диапазон перевода. Добавить позиции перевода в умные области перевода.
  additionalExcludeSelectors?: string | string[]; // Добавить исключенные элементы, чтобы предотвратить умный перевод в конкретных позициях.
  additionalExcludeTags?: string | string[]; // Добавить исключенные теги

  // Оставить оригинал
  stayOriginalSelectors?: string | string[]; // Совпадающие элементы останутся оригинальными. Обычно используется для тегов на форумах.
  stayOriginalTags?: string | string[]; // Совпадающие теги останутся оригинальными, такие как `code`

  // Перевод региона
  atomicBlockSelectors?: string | string[]; // Селектор региона, совпадающие элементы будут рассматриваться как единое целое, не переводятся по частям
  atomicBlockTags?: string | string[]; // Селектор тега региона, то же самое, что и выше

  // Блок или Inline
  extraBlockSelectors?: string | string[]; // Дополнительные селекторы, совпадающие элементы будут рассматриваться как блочные элементы, занимая одну строку.
  extraInlineSelectors?: string | string[]; // Дополнительные селекторы, совпадающие элементы будут рассматриваться как inline элементы.

  inlineTags?: string | string[]; // Совпадающие теги будут рассматриваться как inline элементы
  preWhitespaceDetectedTags?: string | string[]; // Совпадающие теги автоматически обернут строки

  // Стили перевода
  translationClasses?: string | string | string[]; // Добавить дополнительные классы к переводу

  // Глобальные стили
  globalStyles?: Record<string, string>; // Изменить стили страницы, полезно, когда переводы вызывают беспорядок на странице.
  globalAttributes?: Record<string, Record<string, string>>; // Изменить атрибуты элементов страницы

  // Встроенные стили
  injectedCss?: string | string[]; // Встроить CSS стили
  additionalInjectedCss?: string | string[]; // Добавить CSS стили вместо прямого переопределения.

  // Контекст
  wrapperPrefix?: string; // Префикс области перевода, по умолчанию умный, решает, оборачивать ли строки на основе количества символов.
  wrapperSuffix?: string; // Суффикс области перевода

  // Количество символов для обертки перевода
  blockMinTextCount?: number; // Минимальное количество символов для перевода как блока, в противном случае перевод будет inline элементом.
  blockMinWordCount?: number; // То же самое, что и выше. Чтобы всегда оборачивать строки, установите оба значения в 0.

  // Минимальное количество символов для переводимого контента
  containerMinTextCount?: number; // Минимальное количество символов для элементов, которые будут переведены при умном распознавании, по умолчанию 18
  paragraphMinTextCount?: number; // Минимальное количество символов для оригинального абзаца, контент больше этого числа будет переведен
  paragraphMinWordCount?: number; // Минимальное количество слов для оригинального абзаца

  // Принудительное количество символов для разрыва строки в длинных абзацах
  lineBreakMaxTextCount?: number; // Максимальное количество символов для принудительного разрыва строки при переводе длинных абзацев.

  // Время начала перевода
  urlChangeDelay?: number; // Задержка в миллисекундах перед началом перевода после входа на страницу. По умолчанию 250 мс, чтобы дождаться инициализации веб-страницы.

  // AI потоковый перевод
  aiRule: {
    streamingSelector: string; // Селектор веб-страницы GPT, отмечающий переводимый элемент
    messageWrapperSelector: string; // Селектор тела сообщения
    streamingChange: boolean; // Инкрементное или полное обновление для повторяющихся сообщений на страницах, подобных GPT. GPT является инкрементным
  };
}
```