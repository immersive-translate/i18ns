---
sidebar_position: 4
---

# Advanced customization options

You can edit more customized configurations in Extended Configuration Page -> Developer Settings -> User Config that are not editable in UI for advanced users, see the last note for more details about the parameters.The current built-in `config` can be found [here](https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json).

## User Rules

With `Rules` it is possible to customize the configuration of a particular website, deciding what content needs to be translated or not, or adjusting the style of pages, etc.

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

Use `matches` to match the corresponding website.Wildcards are allowed, e.g. `*.google.com`,`www.google.com/test/*`,`file://*`.

Using `selectors` overrides the smart translation scope, translating only the elements matched by that selector.

Use `excludeSelectors` to exclude elements without translating the position.

Use the `additional` family of selectors to increase or decrease the translation range based on intelligent translation.

```json
[
  {
    "matches": "www.google.com",
    "additionalSelectors": [],
    "additionalExcludeSelectors": []
  }
]
```

If you want to translate a region while treating the elements as a whole and not separating them, you can use the `atomicBlockSelectors` selector.For example, Instagram profiles.Note that using `atomicBlockSelectors` requires selecting with `selectors` before using `atomicBlockSelectors`.

```json
{
  "matches": "https://www.instagram.com/*",
  "selectors": [
    "div._aa_c h1",
    "li._acaz div[role=\"menuitem\"]"
  ]
  "atomicBlockSelectors": [
    "div. ._aa_c h1",
    "li._acaz div[role=\"menuitem\"]"
  ]
}
```

If the translation results in misaligned pages, overlapping text, and other edge cases, you can use `globalStyles` to adjust the page style to fix it.For example, the youtube header, which is used to remove the maximum height of the original page.

```json
{
  "matches": "www.google.com",
  "globalStyles": { ".title": "max-height:unset;" }
}
```

## User rules consolidation enhancements

0.7.4+ support.Take skipping the no-translation zone as an example

```json
{
  "matches": "https://www.elektrotechnik.rwth-aachen.de/*",
  "additionalExcludeSelectors.remove": [".notranslate", "[translate=no]"]
}
```

The add and remove operations modify the rules provided by default and do not need to be replaced in their entirety, as was previously the case.

## Injected CSS

Injected CSS allows you to inject custom web styles globally.Can be used with `translationClasses` of `Rules`.

```
".immersive-translate-target-wrapper img { width: 16px; height: 16px }"
```

It is also possible to style the site in a more personalized way, like a regular web style manager.(even utilizing `display:none` to remove ads)

```css
.title {
  color: red;
}
```

## User Config

Config allows you to customize the configuration of this plugin, such as translation services, language-specific language translation options, etc.

```json
{
  "translationService": "tencent",
  "translationServices": {
    "tencent": {
      "secretId": "xxx",
      "secretKey": "xxx",
      "matches": ["*.twitter.com"]
    }
  } ,
  "translationUrlPattern": {
    "excludeMatches": ["www.google.com"]
  },
  "translationLanguagePattern": {
    "matches": ["en"]
  },
  "translationTheme". "none",
  "translationThemePatterns": {
    "underline": {
      "matches": ["discord.com"]
    }
  },
  "generalRule": {
    "_comment": "",
    "normalizeBody": "",
    " injectedCss": [],
    "additionalInjectedCss": [],
    "wrapperPrefix": "smart",
    "wrapperSuffix": "smart",
    "isPdf": false,
    "isTransformPreTagNewLine ": false,
    "urlChangeDelay": 20,
    "isShowUserscriptPagePopup": true,
    "observeUrlChange": true,
    "paragraphMinTextCount": 8,
    " paragraphMinWordCount": 2,
    "blockMinTextCount": 32,
    "blockMinWordCount": 5,
    "containerMinTextCount": 18,
    "lineBreakMaxTextCount": 0,
    " globalAttributes": {},
    "globalStyles": {},
    "selectors": [],
    "preWhitespaceDetectedTags": ["DIV", "SPAN"],
    "stayOriginalSelectors": [],
    " additionalSelectors": [],
    "atomicBlockTags": [],
    "excludeSelectors": [],
    "additionalExcludeSelectors": [],
    "translationClasses": [],
    " atomicBlockSelectors": [],
    "excludeTags": [],
    "metaTags": ["META", "SCRIPT", "STYLE", "NOSCRIPT"],
    "additionalExcludeTags": [],
    " stayOriginalTags": ["CODE", "TT", "IMG", "SUP"],
    "additionalStayOriginalTags": [],
    "inlineTags": [],
    "additionalInlineTags": [],
    " extraInlineSelectors": [],
    "additionalInlineSelectors": [],
    "extraBlockSelectors": [],
    "allBlockTags": [],
    "pdfNewParagraphLineHeight": 2.4 ,
    "pdfNewParagraphIndent": 1.2,
    "pdfNewParagraphIndentRightIndentPx": 130,
    "fingerCountToToggleTranslagePageWhenTouching": 4
  },
  "rules": [
    {
      "matches": "www.google.com",
      "selectors": [".class"]
    }
  ]
}
```

The rule fields in `rules` can use all the fields in `generalRule`.The `rules` have the highest priority, merging the `generalRule` and the rules for that `rule` when a particular `rule` for a particular site is matched.

Introducing some of Config's common fields.

### Do not show unconfigured translation services in popup panel

`"showUnconfiguredTranslationServiceInPopup": false`

### Configuration of translation services

Use `translationService` to select the default translation engine, which currently supports：.

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

Use `translationServices` to configure the `apikey` of each translation service, different service providers need different parameters, and their API keys can be requested in the developer center of their respective websites.

For example, Tencent Translator, you need to configure `secretId`, `secretKey`.You can head over to Tencent Cloud to apply for an API key with 5 million free characters per month.Refer [here](/docs/services/tencent) for the application process.

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

`matches` field, using this translation service for a specific website.

The `limit` field, which specifies the maximum number of requests per second for this translation service (some services limit the maximum number of requests per second).

`maxTextGroupLengthPerRequest` field, maximum number of paragraphs per request

`maxTextLengthPerRequest` field, maximum number of characters per request

`apiUrl` Allows you to customize the address of the translation interface.

### Always translate specific websites

`translationUrlPattern` Configures sites that are always translated, and sites that are never translated.

- `matches` configuration always translates the site.
- `excludeMatches` Configure sites that are never translated.

Configuration values can be domain names or URLs with `*`, such as：`www.google.com/mail/*`

```json
"translationUrlPattern": {
    "matches": ["stackoverflow.com"]
    "excludeMatches": ["www.google.com/mail/*"]
}
```

### Always translate specific languages

translationLanguagePattern, configures the language that is always translated and the language that is never translated.

- `matches` Configure the language that is always translated, e.g. `en`,
- `excludeMatches` Configures the languages that are never translated.

### Translation display format

`translationTheme` is the display format of the translation, and currently supports the following styles：

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

Corresponding Chinese name：

```json
{
  "none": "none",
  "dashed": "dotted underline",
  "dotted": "dotted underline",
  "underline": "straight line underline",
  "mask": "blur effect",
  "paper": "white paper shadow effect",
  "highlight": "highlight",
  "blockquote": "quote style",
  "weakening": "weakening",
  "italic": "italics",
  "bold": "bolding",
  "thinDashed": "thin dashed underline"
}
```

`translationThemePatterns` allows you to configure different translation styles for different websites.

```json
"translationThemePatterns": {
  "underline": {
    "matches": ["discord.com"]
  }
}
```

### Class gpt Page Stream Message Translation

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

### Rules

`rules` is an array object that allows you to configure rules for special sites, such as having Twitter translate only a certain part of a region:.

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
      "extraInlineSelectors": ["[data-testid=\"tweetText\"] div"]
    }
  ]
}
```

The current built-in `rules` can be found [here](https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json).

Some of the important fields are selected below for illustration：

```typescript
export interface Rule {
  // Match the website
  id?: string; // Each adaption rule has its own id, if users want to reuse this rule on top of this change, they need to add this corresponding id to their own rule to reuse it
  matches?: string | string[]; // This rule will only match the website here. This rule will only match sites here.
  excludeMatches?: string | string[]; // Exclude specific sites.
  selectorMatches?: string | string[]; // Match with a selector without specifying all urls
  excludeSelectorMatches?: string | string[]; // Exclude rules, as above.

  // Specify range of translations
  selectors?: string | string[]; // Translate only elements that match
  excludeSelectors?: string | string[]; // Exclude elements, don't translate matches
  excludeTags?: string | string[]; // Exclude Tags, don't translate matching Tags

  // append translation ranges instead of overriding
  additionalSelectors?: string | string[]; // append translation ranges. Append translation locations to the intelligently translated regions.
  additionalExcludeSelectors?: string | string[]; // Append exclude elements so that the smart translation doesn't translate specific locations.
  additionalExcludeTags?: string | string[]; // Additional exclude tags

  // Leave as is
  stayOriginalSelectors?: string | string[]; // Matching elements will be left as is. Commonly used in forum site tags.
  stayOriginalTags?: string | string[]; // Matching tags will be left as is, e.g. `code`

  // Regional translations
  atomicBlockSelectors?: string | string[]; // Regional selectors, matched elements will be treated as a whole, not translated in sections.
  atomicBlockTags?: string | string[]; // Area Tag selectors, same as above

  // Block or Inline
  extraBlockSelectors?: string | string[]; // Extra selectors, matching elements will be treated as block elements, not translated into one line.
  extraInlineSelectors?: string | string[]; // Extra selectors that will be used as inline elements.

  inlineTags?: string | string[]; // Matched Tag will be used as an inline element
  preWhitespaceDetectedTags?: string | string[]; // Matched Tag will be autowrapped

  // Translation style
  translationClasses? string | string | string[]; // Add additional Classes to the translation

  // Global Styles
  globalStyles?: Record<string, string>; // Modify page styles, useful if the translation causes the page to be messed up. `
  globalAttributes?: Record<string, Record<string, string>>; // Modify attributes of page elements

  // Embedded styles
  injectedCss?: string | string[]; // Embed CSS styles
  additionalInjectedCss?: string | string[]; // Additional CSS styles instead of overriding it.

  // Context
  wrapperPrefix?: string; // The prefix of the translation area, defaults to smart, with or without line breaks depending on the number of characters.
  wrapperSuffix?: string; // Suffix of the translation area

  // Number of characters to wrap the translation
  blockMinTextCount?: number; // Minimum number of characters to wrap the translation as a block, otherwise the translation is an inline element.
  blockMinWordCount?: number; // Same as above. If you want them to be always newline, you can put 0 in both.

  // Minimum number of characters that can be translated from the content
  containerMinTextCount?: number; // Minimum number of characters that an element should contain before it will be translated, defaults to 18
  paragraphMinTextCount?: number; // Minimum number of characters for the paragraph, greater than the number of characters that the content should contain. number, anything larger than that will be translated
  paragraphMinWordCount?: number; // Minimum number of words in the original paragraph

  // Forced line breaks for long paragraphs
  lineBreakMaxTextCount?: number; // Maximum number of characters in the paragraph to be forced to break when translating a long paragraph.

  // When to start translation.
  urlChangeDelay?: number; // How many milliseconds to delay the translation after entering the page. To wait for the page to initialize, it defaults to 250ms
  observeUrlChange?: boolean; // Detect when the url address has changed and start the translation again, true by default.

  // Mobile
  isShowUserscriptPagePopup?: boolean; // Show the page popup on mobile devices. floating window, true by default.
  fingerCountToToggleTranslagePageWhenTouching?: number; // Translates when four fingers touch, can be set to 0, 2, 3, 4, 5

  // AI streaming translations
  aiRule: {
    streamingSelector. string; // Selector for marking the element being translated in the gpt web page
    messageWrapperSelector: string; // Message body selector
    streamingChange: boolean; // Whether the message is updated incrementally or fully for the class gpt web page iteration. gpt is incremental
  };
}
```

**More explanation**

Difference between block and inline, if you want to know more you can see [here](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements#inline)

- The block element takes up a single line, and multiple neighboring block elements each take up a new line.
- The inline element does not occupy a single line; multiple neighboring inline elements are arranged on the same line, and a new line is not created until one line is too many.
