---
sidebar_position: 5
---

# JS SDK

JS SDK для Immersive Translate может помочь вам реализовать двуязычный перевод на вашем сайте.

## Как использовать

> Перед отладкой JS SDK, пожалуйста, отключите расширение Immersive Translate

1. Установите параметры инициализации (обратите внимание, что если immersiveTranslateConfig не установлен, инициализация JS SDK завершится неудачей, можно установить пустой объект)

```html
<script>
  window.immersiveTranslateConfig = {
    pageRule: {},
  };
</script>
```

2. Добавьте следующий код `script` перед `</head>` на вашей веб-странице

```html
<script
  async
  src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"
></script>
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

## Параметры

- `pageRule`
  Позволяет настроить сайт, чтобы определить, какой контент нужно переводить, или изменить стиль страницы и т.д.
- `isAutoTranslate`
  Автоматический перевод сразу

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

Использование `selectors` будет ограничивать область интеллектуального перевода, переводя только элементы, соответствующие этому селектору.

Использование `excludeSelectors` позволяет исключить элементы, не переводя их.

Использование `selectors.add` добавит некоторые селекторы на основе значений по умолчанию.

Использование `selectors.remove` уменьшит количество селекторов на основе значений по умолчанию.

Если вы хотите перевести определенную область, рассматривая элемент как единое целое, не разбивая его на строки, вы можете использовать селектор `atomicBlockSelectors`. Обратите внимание, что перед использованием `atomicBlockSelectors` необходимо сначала выбрать с помощью `selectors`.

```json
{
  "selectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"],
  "atomicBlockSelectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"]
}
```

Дополнительные параметры `pageRule`:

```typescript
export interface PageRule {
  excludeMatches?: string | string[]; // Исключить определенные сайты.
  selectorMatches?: string | string[]; // Использовать селекторы для соответствия, без указания всех URL
  excludeSelectorMatches?: string | string[]; // Исключить правила, аналогично вышеуказанному.

你是一位 профессиональный технический переводчик.
Пожалуйста, переведите следующий Markdown контент на русский язык, строго соблюдая следующие правила:

1. Сохранение оригинального формата:
   - Сохраните всю Markdown разметку без изменений
   - Сохраните все блоки кода и HTML теги
   - Сохраните оригинальные переносы строк и пробелы
   - Сохраните все ссылки и URL без изменений
   - Пожалуйста, не добавляйте блоки кода с ```markdown в начале и ``` в конце

2. Профессиональная терминология:
   - Сохраните все технические термины на английском языке
   - Слова 'Release', 'Preview' и т.д. оставьте на английском
   - Сохраните все номера версий и технические спецификации без изменений
  // Указание области перевода
  selectors?: string | string[]; // Переводить только элементы, соответствующие шаблону
  excludeSelectors?: string | string[]; // Исключить элементы, не переводить соответствующие шаблону элементы
  excludeTags?: string | string[]; // Исключить теги, не переводить соответствующие теги

  // Добавление области перевода, а не замена
  additionalSelectors?: string | string[]; // Добавить область перевода. В области интеллектуального перевода добавьте позицию перевода.
  additionalExcludeSelectors?: string | string[]; // Добавить исключенные элементы, чтобы интеллектуальный перевод не переводил определенные позиции.
  additionalExcludeTags?: string | string[]; // Добавить исключенные теги

  // Сохранение оригинала
  stayOriginalSelectors?: string | string[]; // Соответствующие элементы будут сохранены в оригинале. Часто используется для тегов на форумах.
  stayOriginalTags?: string | string[]; // Соответствующие теги будут сохранены в оригинале, например, `code`

  // Перевод области
  atomicBlockSelectors?: string | string[]; // Выбор области, соответствующие элементы будут рассматриваться как единое целое, не будут переводиться по частям
  atomicBlockTags?: string | string[]; // Выбор тегов области, аналогично

  // Блок или Inline
  extraBlockSelectors?: string | string[]; // Дополнительные селекторы, соответствующие элементы будут как блоки, занимая отдельную строку.
  extraInlineSelectors?: string | string[]; // Дополнительные селекторы, соответствующие элементы будут как inline элементы.

  inlineTags?: string | string[]; // Соответствующие теги будут как inline элементы
  preWhitespaceDetectedTags?: string | string[]; // Соответствующие теги будут автоматически переноситься на новую строку

  // Стиль перевода
  translationClasses?: string | string | string[]; // Добавить дополнительные классы к переводу

  // Глобальный стиль
  globalStyles?: Record<string, string>; // Изменить стиль страницы, полезно, если перевод вызывает сбой в отображении страницы.
  globalAttributes?: Record<string, Record<string, string>>; // Изменить атрибуты элементов страницы

  // Встроенный стиль
  injectedCss?: string | string[]; // Встроить CSS стиль
  additionalInjectedCss?: string | string[]; // Добавить CSS стиль, а не заменять.

  // Контекст
  wrapperPrefix?: string; // Префикс области перевода, по умолчанию smart, в зависимости от количества символов решает, переносить ли строку.
  wrapperSuffix?: string; // Суффикс области перевода

  // Количество символов для переноса строки в переводе
  blockMinTextCount?: number; // Минимальное количество символов для перевода как блока, иначе перевод будет как inline элемент.
  blockMinWordCount?: number; // Аналогично. Если хотите, чтобы они всегда переносились, можно указать 0.

  // Минимальное количество символов для перевода содержимого
  containerMinTextCount?: number; // При интеллектуальном распознавании минимальное количество символов в элементе, чтобы он был переведен, по умолчанию 18
  paragraphMinTextCount?: number; // Минимальное количество символов в абзаце оригинала, содержание больше этого числа будет переведено
  paragraphMinWordCount?: number; // Минимальное количество слов в абзаце оригинала

  // Принудительное разбиение длинных абзацев
  lineBreakMaxTextCount?: number; // При включении перевода длинных абзацев, максимальное количество символов в абзаце для принудительного разбиения на строки.

```markdown
// Время запуска перевода
urlChangeDelay?: number; // После входа на страницу, задержка в миллисекундах перед началом перевода. Для ожидания инициализации страницы, по умолчанию 250ms

// AI streaming перевод
aiRule: {
    streamingSelector: string; // Селектор для обозначения переводимого элемента на странице gpt
    messageWrapperSelector: string; // Селектор для обертки сообщения
    streamingChange: boolean; // Повторяющиеся сообщения на странице gpt являются инкрементальными обновлениями или полными обновлениями. gpt является инкрементальным
};
```