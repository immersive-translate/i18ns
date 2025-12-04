---
sidebar_position: 5
---
> 沉浸式翻译 JS SDK 可以帮助你在自己的网站上实现双语翻译。

## 嵌入式 SDK

### 如何使用
```html
<script>
  window.immersiveTranslateConfig = {
    partnerId: "{domain}",
    mountPoint: { //翻译按钮挂载点
        selector: "", //选择器
        action: "child" // 支持：append, child, before, replace
    },
    disclaimerPoint: { //翻译结果声明挂载点（可选）默认跟在翻译按钮后面
        selector: "", //选择器
        action: "child" // 支持：append, child, before, replace
    },
    pageRule: {
        mainFrameSelector: "", //指定翻译区域（可选）默认所有区域
        ...
    },
  };
</script>
<script
  async
  src="有意接入沉浸式翻译SDK，请联系 support@immersivetranslate.com"
></script>
```

### 示例
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
      src="有意接入沉浸式翻译SDK，请联系 support@immersivetranslate.com"
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

#### `immersiveTranslateConfig` 参数说明

```js
export interface immersiveTranslateConfig {
    partnerId: "{domain}",
    mountPoint: { //翻译按钮挂载点
        selector: "", //选择器
        action: "child" // 支持：append, child, before, replace
    },
    disclaimerPoint: { //翻译结果声明挂载点（可选）默认跟在翻译按钮后面
        selector: "", //选择器
        action: "child" // 支持：append, child, before, replace
    },
    pageRule: {
        mainFrameSelector?: string | string[]; // 翻译的根节点范围
        selectors?: string | string[]; // 仅翻译匹配到的元素
        excludeSelectors?: string | string[]; // 排除元素，不翻译匹配的元素
        stayOriginalSelectors?: string | string[]; // 匹配的元素将保持原样。常用于论坛网站的标签。
        extraBlockSelectors?: string | string[]; // 额外的选择器，匹配的元素将作为 block 元素，独占一行。
        extraInlineSelectors?: string | string[]; // 额外的选择器，匹配的元素将作为 inline 元素。
        translationClasses?: string | string | string[]; // 为译文添加额外的 Class
        injectedCss?: string | string[]; // 嵌入 CSS 样式
    }
}
```
