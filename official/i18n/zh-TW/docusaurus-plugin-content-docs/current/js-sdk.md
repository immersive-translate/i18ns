---
sidebar_position: 5
---
> 沉浸式翻譯 JS SDK 可以幫助你在自己的網站上實現雙語翻譯。

## 嵌入式 SDK

### 如何使用
```html
<script>
  window.immersiveTranslateConfig = {
    partnerId: "{domain}",
    mountPoint: { //翻譯按鈕掛載點（可選）
        selector: "", //選擇器
        action: "child" // 支援：append, child, before, replace
    },
    disclaimerPoint: { //翻譯結果聲明掛載點（可選）預設跟在翻譯按鈕後面
        selector: "", //選擇器
        action: "child" // 支援：append, child, before, replace
    },
    pageRule: {
        mainFrameSelector: "", //指定翻譯區域（可選）預設所有區域
        ...
    },
  };
</script>
<script
  async
  src="有意接入沉浸式翻譯SDK，請聯繫 support@immersivetranslate.com"
></script>
```

### 範例
```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Immersive Translate JS SDK</title>
    <script>
      window.immersiveTranslateConfig = {
partnerId: "example-project",
        mountPoint: {
            selector: "#translation-button",
            action: "child"
        }
      };
    </script>
    <script
      async
      src="有意接入沉浸式翻譯SDK，請聯繫 support@immersivetranslate.com"
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

#### `immersiveTranslateConfig` 參數說明

```js
export interface immersiveTranslateConfig {
    partnerId: "{domain}",
    mountPoint: { //翻譯按鈕掛載點（可選）
        selector: "", //選擇器
        action: "child" // 支援：append, child, before, replace
    },
    disclaimerPoint: { //翻譯結果聲明掛載點（可選）預設跟在翻譯按鈕後面
        selector: "", //選擇器
        action: "child" // 支援：append, child, before, replace
    },
    pageRule: {
        mainFrameSelector?: string | string[]; // 翻譯的根節點範圍
        selectors?: string | string[]; // 僅翻譯匹配到的元素
        excludeSelectors?: string | string[]; // 排除元素，不翻譯匹配的元素
        stayOriginalSelectors?: string | string[]; // 匹配的元素將保持原樣。常用於論壇網站的標籤。
        extraBlockSelectors?: string | string[]; // 額外的選擇器，匹配的元素將作為 block 元素，獨占一行。
        extraInlineSelectors?: string | string[]; // 額外的選擇器，匹配的元素將作為 inline 元素。
        translationClasses?: string | string | string[]; // 為譯文添加額外的 Class
        injectedCss?: string | string[]; // 嵌入 CSS 樣式
    }
}
```
```