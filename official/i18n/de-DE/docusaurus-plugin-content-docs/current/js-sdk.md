---
sidebar_position: 5
---
> Immersive Translate JS SDK helps you implement bilingual translation on your own website.

## Embedded SDK

### How to Use
```html
<script>
  window.immersiveTranslateConfig = {
    partnerId: "xxx", //Partner ID (optional)
    mountPoint: { //Translation button mount point (optional)
        selector: "", //Selector
        action: "child" // Supported: append, child, before, replace
    },
    disclaimerPoint: { //Translation result disclaimer mount point (optional) defaults to following the translation button
        selector: "", //Selector
        action: "child" // Supported: append, child, before, replace
    },
    pageRule: {
        mainFrameSelector: "", //Specify translation area (optional) defaults to all areas
        ...
    },
  };
</script>
<script
  async
  src="To integrate Immersive Translate SDK, please contact support@immersivetranslate.com"
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
      src="To integrate Immersive Translate SDK, please contact support@immersivetranslate.com"
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
        action: "child" // Supported: append, child, before, replace
    },
    disclaimerPoint: { //Translation result disclaimer mount point (optional) defaults to following the translation button
        selector: "", //Selector
        action: "child" // Supported: append, child, before, replace
    },
    pageRule: {
        mainFrameSelector?: string | string[]; // Root node scope for translation
        selectors?: string | string[]; // Only translate matched elements
        excludeSelectors?: string | string[]; // Exclude elements, do not translate matched elements
        stayOriginalSelectors?: string | string[]; // Matched elements will remain unchanged. Commonly used for forum website tags.
        extraBlockSelectors?: string | string[]; // Additional selectors, matched elements will be treated as block elements, occupying a single line.
        extraInlineSelectors?: string | string[]; // Additional selectors, matched elements will be treated as inline elements.
        translationClasses?: string | string | string[]; // Add additional classes to translated text
        injectedCss?: string | string[]; // Inject CSS styles
    }
}
```