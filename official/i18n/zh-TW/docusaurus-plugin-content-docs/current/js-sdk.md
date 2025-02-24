---
sidebar_position: 5
---

# JS SDK

沉浸式翻譯 JS SDK 可以幫助你在自己的网站上實現雙語翻譯。

## 如何使用

> 調試 JS SDK 前請關閉沉浸式翻譯擴展

1. 設置初始化參數（請注意，immersiveTranslateConfig 不設置會導致 JS SDK
   初始化失敗，可以設置空對象）

```html
<script>
  window.immersiveTranslateConfig = {
    pageRule: {},
  };
</script>
```

2. 將以下 `script` 代碼添加到你的網頁 `</head>` 之前

```html
<script
  async
  src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"
></script>
```

範例

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

## 參數

- `pageRule`
  可以對網站進行自定義配置，決定哪些內容是否需要被翻譯，或調整網頁樣式等。
- `isAutoTranslate`
  立即自動翻譯

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

使用 `selectors` 會覆蓋智能翻譯範圍，僅翻譯該選擇器匹配到的元素。

使用 `excludeSelectors` 可以排除元素，不翻譯該位置。

使用 `selectors.add` 會在默認的基礎上添加一些 selectors

使用 `selectors.remove` 會在默認的基礎上減少一些 selectors

如果希望翻譯某個區域時，將元素視為一個整體，不將其分行，可以用
`atomicBlockSelectors` 選擇器。要注意的是，使用 `atomicBlockSelectors`
前需要先用 `selectors` 進行選擇。

```json
{
  "selectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"],
  "atomicBlockSelectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"]
}
```

`pageRule` 更多參數說明：

```typescript
export interface PageRule {
  excludeMatches?: string | string[]; // 排除特定的網站。
  selectorMatches?: string | string[]; // 用選擇器來匹配，而無需指定所有 url
  excludeSelectorMatches?: string | string[]; // 排除規則，同上。


```markdown
  // 指定翻譯範圍
  selectors?: string | string[]; // 僅翻譯匹配到的元素
  excludeSelectors?: string | string[]; // 排除元素，不翻譯匹配的元素
  excludeTags?: string | string[]; // 排除 Tags，不翻譯匹配的 Tag 

  // 追加翻譯範圍，而不是覆蓋
  additionalSelectors?: string | string[]; // 追加翻譯範圍。在智能翻譯的區域，追加翻譯位置。
  additionalExcludeSelectors?: string | string[]; // 追加排除元素，讓智能翻譯不翻譯特定位置。
  additionalExcludeTags?: string | string[]; // 追加排除 Tags

  // 保持原樣
  stayOriginalSelectors?: string | string[]; // 匹配的元素將保持原樣。常用於論壇網站的標籤。
  stayOriginalTags?: string | string[]; // 匹配到的 Tag 將保持原樣，比如 `code`

  // 區域翻譯
  atomicBlockSelectors?: string | string[]; // 區域選擇器，匹配的元素將被視為一個整體，不會分段翻譯
  atomicBlockTags?: string | string[]; // 區域 Tag 選擇器，同上

  // Block or Inline
  extraBlockSelectors?: string | string[]; // 額外的選擇器，匹配的元素將作為 block 元素，獨佔一行。
  extraInlineSelectors?: string | string[]; // 額外的選擇器，匹配的元素將作為 inline 元素。

  inlineTags?: string | string[]; // 匹配的 Tag 將作為 inline 元素
  preWhitespaceDetectedTags?: string | string[]; // 匹配的 Tag 將自動換行

  // 譯文樣式
  translationClasses?: string | string | string[]; // 為譯文添加額外的 Class

  // 全局樣式
  globalStyles?: Record<string, string>; // 修改頁面樣式，若譯文導致頁面錯亂，這個很有用。
  globalAttributes?: Record<string, Record<string, string>>; // 修改頁面元素的屬性

  // 嵌入樣式
  injectedCss?: string | string[]; // 嵌入 CSS 樣式
  additionalInjectedCss?: string | string[]; // 追加 CSS 樣式，而不是直接覆蓋。

  // 上下文
  wrapperPrefix?: string; // 譯文區域的前綴，默認為 smart，根據字數決定是否換行。
  wrapperSuffix?: string; // 譯文區域的後綴

  // 譯文換行字數
  blockMinTextCount?: number; // 將譯文作為 block 的最小字符數，否則譯文為 inline 元素。
  blockMinWordCount?: number; // 同上。如果希望它們始終換行，可以都填 0.

  // 內容可翻譯的最小字數
  containerMinTextCount?: number; // 智能識別時，元素最少包含的字符數，才會被翻譯，默認為 18
  paragraphMinTextCount?: number; // 原文段落的最小字符數，大於數字的內容將被翻譯
  paragraphMinWordCount?: number; // 原文段落的最小單詞數

  // 長段落強制換行字數
  lineBreakMaxTextCount?: number; // 開啟翻譯長段落時，強制進行分行的段落最大字符數。
```

```markdown
// 啟動翻譯的時機
urlChangeDelay?: number; // 進入頁面後，延遲多少毫秒開始翻譯。為了等網頁的初始化，目前默認為 250ms

// AI streaming 翻譯
aiRule: {
  streamingSelector: string; //gpt 網頁中標記正在翻譯元素的選擇器
  messageWrapperSelector: string; // 訊息正文選擇器
  streamingChange: boolean; //類 gpt 網頁反覆的訊息是增量更新還是全量更新。gpt 是增量
};
```