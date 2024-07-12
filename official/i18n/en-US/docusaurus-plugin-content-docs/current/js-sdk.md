---
sidebar_position: 5
---

# JS SDK

The Immersive Translate JS SDK helps you implement bilingual translation on your website.

## How to Use

1. Add the following `script` code to the end of your webpage's `<body>` tag:

```html
<script src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"></script>
```

2. Initialize Immersive Translate:

```js
initImmersiveTranslate(options?);
```

## Parameters

With `pageRule`, you can customize the configuration of the website, deciding which content needs to be translated or adjusting the page style, etc.

```js
initImmersiveTranslate({
  pageRule: {
    "selectors": [".text"],
    "excludeSelectors": ["nav", "footer"],
  },
});
```

Using `selectors` will override the smart translation scope and only translate elements matched by the selector.

Using `excludeSelectors` can exclude elements from being translated.

Using `selectors.add` will add some selectors based on the default.

Using `selectors.remove` will reduce some selectors from the default.

If you want to translate a specific area and treat the element as a whole without breaking it into lines, you can use the `atomicBlockSelectors` selector. Note that you need to use `selectors` first to select before using `atomicBlockSelectors`.

```json
{
  "selectors": [
    "div._aa_c h1",
    "li._acaz div[role=\"menuitem\"]"
  ],
  "atomicBlockSelectors": [
    "div._aa_c h1",
    "li._acaz div[role=\"menuitem\"]"
  ]
}
```

More parameters for `pageRule`:

```typescript
export interface PageRule {
  excludeMatches?: string | string[]; // Exclude specific websites.
  selectorMatches?: string | string[]; // Match with selectors without specifying all URLs.
  excludeSelectorMatches?: string | string[]; // Exclude rules, same as above.

  // Specify translation scope
  selectors?: string | string[]; // Only translate matched elements.
  excludeSelectors?: string | string[]; // Exclude elements, do not translate matched elements.
  excludeTags?: string | string[]; // Exclude Tags, do not translate matched Tags.

  // Append translation scope instead of overriding
  additionalSelectors?: string | string[]; // Append translation scope. Add translation positions in the smart translation area.
  additionalExcludeSelectors?: string | string[]; // Append excluded elements, ensuring smart translation does not translate specific positions.
  additionalExcludeTags?: string | string[]; // Append excluded Tags.

  // Keep original
  stayOriginalSelectors?: string | string[]; // Matched elements will remain original. Commonly used for labels on forum websites.
  stayOriginalTags?: string | string[]; // Matched Tags will remain original, such as `code`.

  // Area translation
  atomicBlockSelectors?: string | string[]; // Area selector, matched elements will be treated as a whole, not broken into segments.
  atomicBlockTags?: string | string[]; // Area Tag selector, same as above.

  // Block or Inline
  extraBlockSelectors?: string | string[]; // Additional selectors, matched elements will be treated as block elements, occupying a whole line.
  extraInlineSelectors?: string | string[]; // Additional selectors, matched elements will be treated as inline elements.

  inlineTags?: string | string[]; // Matched Tags will be treated as inline elements.
  preWhitespaceDetectedTags?: string | string[]; // Matched Tags will automatically break lines.

  // Translation style
  translationClasses?: string | string | string[]; // Add extra classes to the translation.

  // Global style
  globalStyles?: Record<string, string>; // Modify page styles, useful if translations cause page disarray.
  globalAttributes?: Record<string, Record<string, string>>; // Modify attributes of page elements.

  // Embedded style
  injectedCss?: string | string[]; // Embed CSS styles.
  additionalInjectedCss?: string | string[]; // Append CSS styles instead of directly overriding.

  // Context
  wrapperPrefix?: string; // Prefix for the translation area, default is smart, decides whether to break lines based on the number of characters.
  wrapperSuffix?: string; // Suffix for the translation area.

  // Translation line break character count
  blockMinTextCount?: number; // Minimum character count to treat the translation as a block, otherwise the translation is an inline element.
  blockMinWordCount?: number; // Same as above. If you want them to always break lines, you can set both to 0.

  // Minimum character count for content to be translated
  containerMinTextCount?: number; // Minimum character count for elements to be translated during smart recognition, default is 18.
  paragraphMinTextCount?: number; // Minimum character count for original text paragraphs, content larger than this number will be translated.
  paragraphMinWordCount?: number; // Minimum word count for original text paragraphs.

  // Forced line break character count for long paragraphs
  lineBreakMaxTextCount?: number; // When translating long paragraphs, the maximum character count to force line breaks.

  // Translation start timing
  urlChangeDelay?: number; // Delay in milliseconds before starting translation after entering the page. Currently defaults to 250ms to wait for page initialization.

  // AI streaming translation
  aiRule: {
    streamingSelector: string; // Selector for marking elements being translated in GPT-like pages.
    messageWrapperSelector: string; // Message body selector.
    streamingChange: boolean; // Whether repeated messages on GPT-like pages are incremental or full updates. GPT is incremental.
  };
}
```
```