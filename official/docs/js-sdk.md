---
sidebar_position: 5
---

# JS SDK

沉浸式翻译 JS SDK 可以帮助你在自己的网站上实现双语翻译。

## 如何使用

> 调试 JS SDK 前请关闭沉浸式翻译扩展

1. 设置初始化参数（请注意，immersiveTranslateConfig 不设置会导致 JS SDK
   初始化失败，可以设置空对象）

```html
<script>
  window.immersiveTranslateConfig = {
    pageRule: {},
  };
</script>
```

2. 将以下 `script` 代码添加到你的网页 `</head>` 之前

```html
<script
  async
  src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"
></script>
```

示例

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

## 参数

- `pageRule`
  可以对网站进行自定义配置，决定哪些内容是否需要被翻译，或调整网页样式等。
- `isAutoTranslate`
  立即自动翻译

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

使用 `selectors` 会覆盖智能翻译范围，仅翻译该选择器匹配到的元素。

使用 `excludeSelectors` 可以排除元素，不翻译该位置。

使用 `selectors.add` 会在默认的基础上添加一些 selectors

使用 `selectors.remove` 会在默认的基础上减少一些 selectors

如果希望翻译某个区域时，将元素视为一个整体，不将其分行，可以用
`atomicBlockSelectors` 选择器。要注意的是，使用 `atomicBlockSelectors`
前需要先用 `selectors` 进行选择。

```json
{
  "selectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"],
  "atomicBlockSelectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"]
}
```

`pageRule` 更多参数说明：

```typescript
export interface PageRule {
  excludeMatches?: string | string[]; // 排除特定的网站。
  selectorMatches?: string | string[]; // 用选择器来匹配，而无需指定所有 url
  excludeSelectorMatches?: string | string[]; // 排除规则，同上。

  // 指定翻译范围
  selectors?: string | string[]; // 仅翻译匹配到的元素
  excludeSelectors?: string | string[]; // 排除元素，不翻译匹配的元素
  excludeTags?: string | string[]; // 排除 Tags，不翻译匹配的 Tag 

  // 追加翻译范围，而不是覆盖
  additionalSelectors?: string | string[]; // 追加翻译范围。在智能翻译的区域，追加翻译位置。
  additionalExcludeSelectors?: string | string[]; // 追加排除元素，让智能翻译不翻译特定位置。
  additionalExcludeTags?: string | string[]; // 追加排除 Tags

  // 保持原样
  stayOriginalSelectors?: string | string[]; // 匹配的元素将保持原样。常用于论坛网站的标签。
  stayOriginalTags?: string | string[]; // 匹配到的 Tag 将保持原样，比如 `code`

  // 区域翻译
  atomicBlockSelectors?: string | string[]; // 区域选择器，匹配的元素将被视为一个整体，不会分段翻译
  atomicBlockTags?: string | string[]; // 区域 Tag 选择器，同上

  // Block or Inline
  extraBlockSelectors?: string | string[]; // 额外的选择器，匹配的元素将作为 block 元素，独占一行。
  extraInlineSelectors?: string | string[]; // 额外的选择器，匹配的元素将作为 inline 元素。

  inlineTags?: string | string[]; // 匹配的 Tag 将作为 inline 元素
  preWhitespaceDetectedTags?: string | string[]; // 匹配的 Tag 将自动换行

  // 译文样式
  translationClasses?: string | string | string[]; // 为译文添加额外的 Class

  // 全局样式
  globalStyles?: Record<string, string>; // 修改页面样式，若译文导致页面错乱，这个很有用。`
  globalAttributes?: Record<string, Record<string, string>>; // 修改页面元素的属性

  // 嵌入样式
  injectedCss?: string | string[]; // 嵌入 CSS 样式
  additionalInjectedCss?: string | string[]; // 追加 CSS 样式，而不是直接覆盖。

  // 上下文
  wrapperPrefix?: string; // 译文区域的前缀，默认为 smart，根据字数决定是否换行。
  wrapperSuffix?: string; // 译文区域的后缀

  // 译文换行字数
  blockMinTextCount?: number; // 将译文作为 block 的最小字符数，否则译文为 inline 元素。
  blockMinWordCount?: number; // 同上。如果希望它们始终换行，可以都填 0.

  // 内容可翻译的最小字数
  containerMinTextCount?: number; // 智能识别时，元素最少包含的字符数，才会被翻译，默认为 18
  paragraphMinTextCount?: number; // 原文段落的最小字符数，大于数字的内容将被翻译
  paragraphMinWordCount?: number; // 原文段落的最小单词数

  // 长段落强制换行字数
  lineBreakMaxTextCount?: number; // 开启翻译长段落时，强制进行分行的段落最大字符数。

  // 启动翻译的时机
  urlChangeDelay?: number; // 进入页面后，延迟多少毫秒开始翻译。为了等网页的初始化，目前默认为 250ms

  // AI streaming 翻译
  aiRule: {
    streamingSelector: string; //gpt 网页中标记正在翻译元素的选择器
    messageWrapperSelector: string; // 消息正文选择器
    streamingChange: boolean; //类 gpt 网页反复的消息是增量更新还是全量更新。gpt 是增量
  };
}
```
