---
sidebar_position: 4
---

# Продвинутые параметры настройки

Эта страница предназначена для опытных пользователей, имеющих базовые знания HTML/CSS/JSON. Продвинутые настройки могут значительно повысить гибкость адаптации, но также могут привести к созданию "правильных на вид, но неработающих" конфигураций. Рекомендуется сделать резервную копию перед редактированием.

## Предупреждения перед использованием

- Вход через [Настройки разработчика](https://dash.immersivetranslate.com/#developer).
- Перед редактированием обязательно создайте резервную копию User Config / User Rules, чтобы ошибки формата не привели к игнорированию конфигурации.
- Окончательную внутреннюю конфигурацию см. по кнопке "Click to expand the final config" (поля, значения по умолчанию, доступные сервисы).

## Входы и приоритеты

Основные входы (Настройки разработчика):
- Edit Full User Config: полная настройка (включая `rules`, сервисы перевода, стили и др.).
- Edit User Rules: редактирование только массива `rules` (этот вход принимает только массив, без обёртки `{ "rules": [...] }`).
- Injected CSS: глобальная вставка CSS.

Приоритеты (от высокого к низкому): сработавшее правило из `rules` > `generalRule` > встроенная конфигурация по умолчанию.
При срабатывании `rule`, происходит объединение с `generalRule`, приоритет за полями из `rule`.

## Быстрый старт (наиболее частые задачи)

### 1) Переводить только основной текст сайта

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

### 2) Всегда/никогда не переводить

```json
{
  "translationUrlPattern": {
    "matches": ["stackoverflow.com"],
    "excludeMatches": ["www.google.com/mail/*"]
  }
}
```

### 3) Для разных сайтов использовать разные сервисы перевода

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

### 4) Оформление перевода по разным сайтам

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

### 5) Перевод ломает оформление — исправить стилями

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

### 6) Не показывать неактивированные сервисы перевода в панели

```json
{
  "showUnconfiguredTranslationServiceInPopup": false
}
```

## Правила и совпадения

### Объединение правил

- `generalRule`: базовое правило для всех сайтов.
- `rules`: правила для конкретных сайтов, имеют высший приоритет.

Поля в `rules` могут использовать большинство опций из `generalRule`.

### Форматы matches

`matches` поддерживает строку или массив:
- Домен: `example.com`
- Полный URL: `https://example.com/path/`
- Маска/шаблон: `https://*/*q=*`
- Совпадает со всем: `*` / `*://*` / `*://*/*`
- Локальные файлы: `file://*`

Примечание: `*.twitter.com` совпадает только с поддоменами, не с корневым `twitter.com`.

### selectors / excludeSelectors

- `selectors`: переводятся только выбранные элементы (полностью заменяет стандартный диапазон).
- `excludeSelectors`: исключает элементы из перевода.

Если только добавить/убрать к стандартному диапазону — используйте `.add` / `.remove` (см. след. раздел).

### Наследование и инкрементальные изменения (.add / .remove)

Для массивных или объектных полей поддерживается `.add`/`.remove` для добавления/удаления значений.
Используйте их, чтобы не перезаписать стандартные правила:

```json
[
  {
    "id": "twitter",
    "selectors.add": ["[data-testid='tweetText'] a"],
    "excludeSelectors.add": ["header"]
  }
]
```

### Быстрый справочник по часто используемым полям

Совпадения:
- `matches` / `excludeMatches`
- `selectorMatches` / `excludeSelectorMatches`

Диапазон перевода:
- `selectors` / `excludeSelectors` / `excludeTags`
- `stayOriginalSelectors` / `stayOriginalTags`
- `extraInlineSelectors` / `extraBlockSelectors`

Стили и оформление:
- `translationClasses`: дополнительные классы для перевода
- `globalStyles` / `globalAttributes`
- `injectedCss` / `additionalInjectedCss`
- `wrapperPrefix` / `wrapperSuffix`
- `blockMinTextCount` / `blockMinWordCount`

Время и мобильные устройства:
- `urlChangeDelay` / `observeUrlChange`
- `isShowUserscriptPagePopup`

### Стриминговый перевод в стиле GPT (чат-переписка)

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

Подробные комментарии к полям см. в конце ("Приложение: Справочник по полям Rule").

## Логика совпадения matches (кратко)

- Только домен (без `*` и пути): сверяется hostname.
- Полный URL (без `*`): сверяются протокол + хост + порт + путь.
- С `*` или без протокола: шаблонное сравнение (по умолчанию для http/https/file).

Примеры:
- `twitter.com` ✅ попадет в `https://twitter.com/home`
- `*.twitter.com` ✅ попадет в `https://mobile.twitter.com`, ❌ не попадет в `https://twitter.com`
- `https://twitter.com/home` только для точного совпадения
- `twitter.com/*` охватывает всё под twitter.com

## Пример адаптации сайта (на примере Twitter)

Ниже часть встроенных правил Twitter, показывающая, как работают `selectors`/`excludeSelectors`/`globalStyles`:

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

- `selectors`: переводятся только тексты твитов и др. основной контент, исключая ник/кнопки.
  ![tweet](https://s.immersivetranslate.com/assets/r2-uploads/tweet.png)
- `excludeSelectors`: исключают кнопки, навигацию и другие элементы управления.
  ![twitter-follow](https://s.immersivetranslate.com/assets/r2-uploads/twitter-follow.png)
- `globalStyles`: убирает ограничение строк, чтобы перевод не обрезался.
  ![用户主页](https://s.immersivetranslate.com/assets/r2-uploads/twitterUser.png)

## Своё правило адаптации сайта

Можно использовать `id` для наследования встроенного правила и применять инкрементальные изменения `.add/.remove`:

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

Пояснения:
- Через `id` наследуются встроенные правила, не нужно дублировать `matches`.
- `.add/.remove` — рекомендуемый способ инкрементально изменять массивы.

Популярные встроенные `id`:
- `isEbook`: страницы для чтения epub
- `isEbookBuilder`: генерация epub книг с переводом
- `pdf`: страницы с PDF с двухъязычным сопоставлением

Полный список встроенных правил:
- `https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json`

## Настройка переводчиков

- `translationService`: движок по умолчанию.
- `translationServices`: настройка сервисов и переопределение по сайтам.
- `showUnconfiguredTranslationServiceInPopup`: скрыть неактивированные сервисы.

Пример (Tencent):

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

Комментарии:
- `matches`: на каких сайтах работает этот сервис.
- `limit`: ограничение скорости (запросов в сек).
- `maxTextGroupLengthPerRequest` / `maxTextLengthPerRequest`: параметры размера запроса.
- `apiUrl`: свой адрес API.

### Таймаут запроса (максимальная длительность)

Для каждого сервиса можно задать таймаут запроса (мс). Для Pro версии можно отдельно задать `proRequestTimeout`.

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

Советы:
- Большой таймаут — дольше ожидание, слишком маленький — чаще будут ошибки времени.
- Стандартное значение зависит от сервиса, сверяйтесь с финальной конфигой.
- `proRequestTimeout` действует только для `provider: pro` (платные сервисы).

## Языки и стратегия перевода

### Языки всегда/никогда не переводить

```json
{
  "translationLanguagePattern": {
    "matches": ["en"],
    "excludeMatches": ["zh"]
  }
}
```

### Привязка исходного языка к сайту

```json
{
  "sourceLanguageUrlPattern": {
    "en": {
      "matches": ["*.google.com"]
    }
  }
}
```

## Прочие частые опции

### Разрешить рендеринг HTML-тегов в переводе

Включить, если нужно, чтобы в переводе сохранялись и отображались HTML-теги:

```json
{
  "enableRenderHtmlTag": true
}
```

## Стили и темы перевода

Возможные значения `translationTheme` (см. финальную конфигу):

```text
none, grey, dashed, dashedBorder, solidBorder, dotted, underline, mask, opacity,
paper, dividingLine, highlight, marker, marker2, blockquote, weakening, italic,
bold, thinDashed, nativeDotted, wavy, nativeDashed, nativeUnderline, background
```

Пример стилизации для сайта:

```json
{
  "translationThemePatterns": {
    "highlight": {
      "matches": ["discord.com"]
    }
  }
}
```

## AI / Параметры продвинутых сервисов

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

### Свои заголовки и тело запроса

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

### Кастомизация Gemini (и других AI) по моделям

Gemini использует настройки по умолчанию. Чтобы их перебить, используйте `modelsOverrides`:

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

Совет: `modelsOverrides` подходит и для других AI-сервисов — будет применяться при совпадении названия модели.

### Строго следовать своему prompt

> Для снижения числа "галлюцинаций" крупными AI-моделями в плагине реализована проверка качества перевода. Система сравнивает количество токенов в ответе и запросе; при отклонениях результат считается невалидным и задействуется запасная стратегия.
> Если ваш промпт для задач отличных от перевода (расширение, перефразирование и пр.) — коэффициент токенов может не совпасть со стандартным. Включите строгий режим, чтобы отключить эту проверку.

```json
{
  "translationServices": {
    "claude": {
      "strictPrompt": true
    }
  }
}
```

### Свои multi-language prompt'ы (пример)

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

## Терминология и машинный перевод

Новая функция: [AI-терминология](https://dash.immersivetranslate.com/#terms), работает только с AI-сервисами.

По умолчанию терминология не применяется для машинного перевода (она заменяет только плейсхолдеры, что может снизить качество). Включить принудительно (не рекомендовано):

```json
{
  "enableMachineTranslateTerms": true
}
```

## Период очистки кэша

Через 30 дней кэш переводов автоматически очищается для предотвращения переполнения.

```json
{
  "cacheMaxAgeDay": 30
}
```

## Injected CSS и globalStyles

- Injected CSS: глобальный CSS, удобно для массовых фиксов.
- globalStyles: по-правилу для конкретных сайтов.

Пример Injected CSS:

```css
.immersive-translate-target-wrapper img {
  width: 16px;
  height: 16px;
}
```

## Отладка и частые препятствия

- `*.twitter.com` не включает корневой домен — пишите ещё `twitter.com`.
- `selectors` полностью перекрывает стандартный диапазон. Для патча используйте `.add/.remove`.
- `matches` типа `example.com/path` — маска, уточняйте, нужен ли полный URL.
- Если не работает: проверьте итоговую конфигу, затем обновите страницу.
- Лишняя запятая в JSON сломает парсер!

## Приложение: Справочник по полям Rule

Ниже справочник по наиболее распространённым полям Rule. Полный состав смотрите в итоговой конфигурации.
Совет: для массивов и объектов используйте `.add`/`.remove`, чтобы не пытаться полностью заменить стандартные данные.

```typescript
export interface Rule {
  // Совпадение сайтов
  id?: string; // ID встроенного правила, если используете наследование
  matches?: string | string[]; // Для каких сайтов применяется это правило
  excludeMatches?: string | string[]; // Исключении сайтов
  selectorMatches?: string | string[]; // Совпадение по CSS (без URL)
  excludeSelectorMatches?: string | string[]; // Исключение по CSS

  // Диапазон перевода
  selectors?: string | string[]; // Только выбранные элементы переводить
  excludeSelectors?: string | string[]; // Не переводить указанные элементы
  excludeTags?: string | string[]; // Не переводить определённые теги

  // Доавление диапазона (если не сработало, используйте selectors.add/remove)
  additionalSelectors?: string | string[]; // Добавить элементы для перевода
  additionalExcludeSelectors?: string | string[]; // Добавить элементы-исключения
  additionalExcludeTags?: string | string[]; // Добавить исключения по тегам (часть версий может не поддерживать)

  // Оставить как есть
  stayOriginalSelectors?: string | string[]; // Не переводить совпавшие элементы
  stayOriginalTags?: string | string[]; // Не переводить совпавшие теги, напр., code

  // Block или Inline
  extraBlockSelectors?: string | string[]; // Принудительно как block
  extraInlineSelectors?: string | string[]; // Принудительно как inline
  inlineTags?: string | string[]; // Теги, считающиеся inline
  preWhitespaceDetectedTags?: string | string[]; // Теги с авторазрывом

  // Стили для перевода
  translationClasses?: string | string[]; // Классы для перевода

  // Глобальные стили
  globalStyles?: Record<string, string>; // Изменить стили на странице
  globalAttributes?: Record<string, Record<string, string | null>>; // Изменить атрибуты элементов

  // Встраиваемые стили
  injectedCss?: string | string[]; // Встроить CSS
  additionalInjectedCss?: string | string[]; // Дополнительный CSS

  // Окружение
  wrapperPrefix?: string; // Префикс перед переводом
  wrapperSuffix?: string; // Суффикс после перевода

  // Минимальная длина блока для разбиения
  blockMinTextCount?: number; // Минимальная длина символов для перевода блока
  blockMinWordCount?: number; // Минимум слов для блока

  // Минимальная длина перевода
  containerMinTextCount?: number; // Минимум символов для авто-распознавания
  paragraphMinTextCount?: number; // Минимум символов для параграфа
  paragraphMinWordCount?: number; // Минимум слов для параграфа

  // Лимит длины строки с разбиением
  lineBreakMaxTextCount?: number; // Максимум символов строки для auto-break

  // Момент старта перевода
  urlChangeDelay?: number; // Задержка после загрузки страницы
  observeUrlChange?: boolean; // Переводить при смене URL

  // Мобильные устройства
  isShowUserscriptPagePopup?: boolean; // Показывать popup на мобильных
  fingerCountToToggleTranslagePageWhenTouching?: number; // Не используется

  // Стриминговый AI-перевод
  aiRule?: {
    streamingSelector: string; // Селектор элемента статуса перевода
    messageWrapperSelector: string; // Селектор текста сообщения
    streamingChange: boolean; // Инкрементальное обновление (true)
  };
}
```
