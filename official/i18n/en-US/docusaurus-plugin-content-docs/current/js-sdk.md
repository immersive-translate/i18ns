---
sidebar_position: 5
---
> The Immersive Translate JS SDK helps you implement bilingual translation on your own website.

## Embedded SDK

### How to Use
```html
<script>
  window.immersiveTranslateConfig = {
    partnerId: "xxx", //Partner ID (optional)
    mountPoint: { //Translation button mount point (optional)
        selector: "", //Selector
        action: "child" // Supports: append, child, before, replace
    },
    disclaimerPoint: { //Translation result disclaimer mount point (optional) Default follows after translation button
        selector: "", //Selector
        action: "child" // Supports: append, child, before, replace
    },
    pageRule: {
        mainFrameSelector: "", //Specify translation area (optional) Default all areas
        ...
    },
  };
</script>
<script
  async
  src="https://download.immersivetranslate.com/immersive-translate-sdk-lite-latest.js"
></script>
```

### Example
```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Immersive Translate JS SDK</title>
    <script>
      window.immersiveTranslateConfig = {
        mountPoint: {
            selector: "#translation-button",
            action: "child"
        }
      };
    </script>
    <script
      async
      src="https://download.immersivetranslate.com/immersive-translate-sdk-lite-latest.js"
    ></script>
  </head>
  <body>
    <div id="translation-button"></div>
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

#### `immersiveTranslateConfig` Parameter Description

```js
export interface immersiveTranslateConfig {
    partnerId: "xxx", //Partner ID (optional)
    mountPoint: { //Translation button mount point (optional)
        selector: "", //Selector
        action: "child" // Supports: append, child, before, replace
    },
    disclaimerPoint: { //Translation result disclaimer mount point (optional) Default follows after translation button
        selector: "", //Selector
        action: "child" // Supports: append, child, before, replace
    },
    pageRule: {
        mainFrameSelector?: string | string[]; // Root node scope for translation
        selectors?: string | string[]; // Only translate matched elements
        excludeSelectors?: string | string[]; // Exclude elements, do not translate matched elements
        stayOriginalSelectors?: string | string[]; // Matched elements will remain unchanged. Commonly used for forum website tags.
        extraBlockSelectors?: string | string[]; // Additional selectors, matched elements will be treated as block elements, occupying a single line.
        extraInlineSelectors?: string | string[]; // Additional selectors, matched elements will be treated as inline elements.
        translationClasses?: string | string | string[]; // Add additional Class to translated text
        injectedCss?: string | string[]; // Inject CSS styles
    }
}
```

## Floating Ball SDK

### How to Use

> Please disable the Immersive Translate extension before debugging the JS SDK

```html
<script>
  window.immersiveTranslateConfig = {
    pageRule: {},
    ...
  };
</script>
<script
  async
  src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"
></script>
```

### Example

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


#### `immersiveTranslateConfig` Parameter Description
```typescript
export interface immersiveTranslateConfig {
    isAutoTranslate: false, //Whether to auto-translate
    pageRule: {
        mainFrameSelector?: string | string[]; // Root node scope for translation
        selectors?: string | string[]; // Only translate matched elements
        excludeSelectors?: string | string[]; // Exclude elements, do not translate matched elements
        stayOriginalSelectors?: string | string[]; // Matched elements will remain unchanged. Commonly used for forum website tags.
        extraBlockSelectors?: string | string[]; // Additional selectors, matched elements will be treated as block elements, occupying a single line.
        extraInlineSelectors?: string | string[]; // Additional selectors, matched elements will be treated as inline elements.
        translationClasses?: string | string | string[]; // Add additional Class to translated text
        injectedCss?: string | string[]; // Inject CSS styles
    }
}
```
