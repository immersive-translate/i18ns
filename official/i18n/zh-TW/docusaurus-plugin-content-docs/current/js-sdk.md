---
sidebar_position: 5
---

# JS SDK

The Immersive Translate JS SDK helps you implement bilingual translation on your website.

## How to Use

1. Initialize Immersive Translate:

```js
<script>
  window.immersiveTranslateConfig = {
    isAutoTranslate: true,
    pageRule: {}
  }
</script>
```

2. Add the following `script` code to your webpage

```html
<script src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"></script>
```


Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Immersive Translate JS SDK</title>
  <script>
    window.immersiveTranslateConfig = {
      isAutoTranslate: true,
      pageRule: {}
    }
  </script>
  <script async src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"></script>
</head>

<body>
  <div>
    <p>Night gathers, and now my watch begins. It shall not end until my death. I shall take no wife, hold no lands,
      father no children. I shall wear no crowns and win no glory. I shall live and die at my post.</p>
  </div>
</body>
</html>
```

## Parameters

With `pageRule`, you can customize the configuration of the website, deciding which content needs to be translated or adjusting the webpage styles.

```js
initImmersiveTranslate({
  pageRule: {
    "selectors": [".text"],
    "excludeSelectors": ["nav", "footer"],
  },
});
```

Using `selectors` will override the smart translation range, translating only elements matched by the selector.

Using `excludeSelectors` can exclude elements from translation.

Using `selectors.add` will add some selectors on top of the default ones.

Using `selectors.remove` will remove some selectors from the default ones.

If you want to translate a specific area and consider an element as a whole without breaking it into lines, you can use the `atomicBlockSelectors` selector. Note that you need to select elements using `selectors` before using `atomicBlockSelectors`.

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

`pageRule` more parameter explanations:

```typescript
export interface PageRule {
  excludeMatches?: string | string[]; // Exclude specific websites.
  selectorMatches?: string | string[]; // Match using selectors without specifying all URLs
  excludeSelectorMatches?: string | string[]; // Exclude rules, same as above.

  // Specify translation range
  selectors?: string | string[]; // Translate only matched elements
  excludeSelectors?: string | string[]; // Exclude elements, do not translate matched elements
  excludeTags?: string | string[]; // Exclude tags, do not translate matched tags

  // Add translation range, not override
  additionalSelectors?: string | string[]; // Add translation range. Add translation positions in smart translation areas.
  additionalExcludeSelectors?: string | string[]; // Add excluded elements to prevent smart translation in specific positions.
  additionalExcludeTags?: string | string[]; // Add excluded tags

  // Keep original
  stayOriginalSelectors?: string | string[]; // Matched elements will remain original. Commonly used for tags on forum websites.
  stayOriginalTags?: string | string[]; // Matched tags will remain original, such as `code`

  // Region translation
  atomicBlockSelectors?: string | string[]; // Region selector, matched elements will be considered as a whole, not translated in segments
  atomicBlockTags?: string | string[]; // Region tag selector, same as above

  // Block or Inline
  extraBlockSelectors?: string | string[]; // Extra selectors, matched elements will be treated as block elements, occupying one line.
  extraInlineSelectors?: string | string[]; // Extra selectors, matched elements will be treated as inline elements.

  inlineTags?: string | string[]; // Matched tags will be treated as inline elements
  preWhitespaceDetectedTags?: string | string[]; // Matched tags will automatically wrap lines

  // Translation styles
  translationClasses?: string | string | string[]; // Add extra classes to the translation

  // Global styles
  globalStyles?: Record<string, string>; // Modify page styles, useful when translations cause page disorder.
  globalAttributes?: Record<string, Record<string, string>>; // Modify attributes of page elements

  // Embedded styles
  injectedCss?: string | string[]; // Embed CSS styles
  additionalInjectedCss?: string | string[]; // Add CSS styles instead of directly overriding.

  // Context
  wrapperPrefix?: string; // Prefix of the translation area, default is smart, decides whether to wrap lines based on the number of characters.
  wrapperSuffix?: string; // Suffix of the translation area

  // Translation wrapping character count
  blockMinTextCount?: number; // Minimum character count for translation as a block, otherwise, the translation will be an inline element.
  blockMinWordCount?: number; // Same as above. To always wrap lines, set both to 0.

  // Minimum character count for translatable content
  containerMinTextCount?: number; // Minimum character count for elements to be translated during smart recognition, default is 18
  paragraphMinTextCount?: number; // Minimum character count for original paragraph, content greater than the number will be translated
  paragraphMinWordCount?: number; // Minimum word count for original paragraph

  // Forced line break character count for long paragraphs
  lineBreakMaxTextCount?: number; // Maximum character count for forced line break when translating long paragraphs.

  // Timing to start translation
  urlChangeDelay?: number; // Delay in milliseconds before starting translation after entering the page. Default is 250ms to wait for webpage initialization.

  // AI streaming translation
  aiRule: {
    streamingSelector: string; // GPT webpage selector marking the translating element
    messageWrapperSelector: string; // Message body selector
    streamingChange: boolean; // Incremental or full update for repeated messages in GPT-like webpages. GPT is incremental
  };
}
```