---
sidebar_position: 4
---

# 進階自訂選項

你可以在擴充套件設定頁面 -> 開發者設定 -> User Config 裡編輯更多 UI 裡無法編輯的自定義設定，適用於進階使用者，參數講解詳見最後的說明。目前內建的 `config` 可以在[這裡](https://dash.immersivetranslate. com/#developer)，點選 `Click to expand the final config` 找到。

## User Rules

透過 `Rules` 可以對特定的網站進行自定義設定，決定哪些內容是否需要被翻譯，或調整網頁樣式等。

```json
[
  {
    "matches": "www.google.com",
    "selectors": [".title"]
  },
  {
    "matches": "twitter.com",
    "selectors": [".text"],
    "excludeSelectors": ["nav", "footer"]
  }
]
```

使用 `matches` 來匹配對應的網站。允許萬用字元，如 `*.google.com`, `www.google.com/test/*`, `file://*`

使用 `selectors` 會覆蓋智慧翻譯範圍，僅翻譯該選擇器匹配到的元素。

使用 `excludeSelectors` 可以排除元素，不翻譯該位置。

使用 `selectors.add` 會在預設的基礎上新增一些 selectors

使用 `selectors.remove` 會在預設的基礎上減少一些 selectors

```json
[
  {
    "matches": "www.google.com",
    "selectors.add": ["baidu.com"],
    "excludeSelectors": ["buzzing.cc"]
  }
]
```

如果希望翻譯某個區域時，將元素視為一個整體，不將其分行，可以用 `atomicBlockSelectors` 選擇器。比如 Instagram 的個人資料介紹。

```json
{
  "matches": "https://www.instagram.com/*",
  "selectors": [
    "div._aa_c h1",
    "li._acaz div[role=\"menuitem\"]"
  ]
  "atomicBlockSelectors": [
    "div._aa_c h1",
    "li._acaz div[role=\"menuitem\"]"
  ]
}
```

如果譯文導致頁面錯位，文字重疊等邊緣情況，可以使用 `globalStyles` 調整網頁樣式來修復。比如 youtube 的標題，用來移除原網頁的最大高度。

```json
{
  "matches": "www.google.com",
  "globalStyles": { ".title": "max-height:unset;" }
}
```

## Injected CSS

透過 Injected CSS 可以向全域性注入自定義網頁樣式。可以搭配 `Rules` 的 `translationClasses` 一起使用。

```css
.immersive-translate-target-wrapper img {
  width: 16px;
  height: 16px;
}
```

也可以像常規的網頁樣式管理器那樣，對網站進行更加個性化的樣式設計。（甚至利用 `display:none` 去廣告）

```css
.title {
  color: red;
}
```

## User Config

透過 Config 可以自訂義此外掛的相關設定，如翻譯服務、特定語言翻譯選項等。

```json
{
  "translationService": "tencent",
  "translationServices": {
    "tencent": {
      "secretId": "xxx",
      "secretKey": "xxx",
      "matches": ["twitter.com"]
    }
  },
  "translationUrlPattern": {
    "excludeMatches": ["www.google.com"]
  },
  "translationLanguagePattern": {
    "matches": ["en"]
  },
  "translationTheme": "none",
  "translationThemePatterns": {
    "underline": {
      "matches": ["discord.com"]
    }
  },
  "sourceLanguageUrlPattern": {
    "en": {
      "matches": ["*.google.com"]
    }
  },
  "generalRule": {
    "_comment": "",
    "normalizeBody": "",
    "injectedCss": [],
    "additionalInjectedCss": [],
    "wrapperPrefix": "smart",
    "wrapperSuffix": "smart",
    "isPdf": false,
    "isTransformPreTagNewLine": false,
    "urlChangeDelay": 20,
    "isShowUserscriptPagePopup": true,
    "observeUrlChange": true,
    "paragraphMinTextCount": 8,
    "paragraphMinWordCount": 2,
    "blockMinTextCount": 32,
    "blockMinWordCount": 5,
    "containerMinTextCount": 18,
    "lineBreakMaxTextCount": 0,
    "globalAttributes": {},
    "globalStyles": {},
    "selectors": [],
    "preWhitespaceDetectedTags": ["DIV", "SPAN"],
    "stayOriginalSelectors": [],
    "additionalSelectors": [],
    "atomicBlockTags": [],
    "excludeSelectors": [],
    "additionalExcludeSelectors": [],
    "translationClasses": [],
    "atomicBlockSelectors": [],
    "excludeTags": [],
    "metaTags": ["META", "SCRIPT", "STYLE", "NOSCRIPT"],
    "additionalExcludeTags": [],
    "stayOriginalTags": ["CODE", "TT", "IMG", "SUP"],
    "additionalStayOriginalTags": [],
    "inlineTags": [],
    "additionalInlineTags": [],
    "extraInlineSelectors": [],
    "additionalInlineSelectors": [],
    "extraBlockSelectors": [],
    "allBlockTags": [],
    "pdfNewParagraphLineHeight": 2.4,
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

其中，`rules` 裡的規則欄位，可以使用 `generalRule` 裡的全部欄位。`rules` 擁有最高優先順序，當匹配到特定網站的某一條 `rule` 時，會合併 `generalRule` 和該 `rule` 的規則。

介紹一些 Config 常見的欄位。

### 允許渲染普通 HTML 標籤

前往 [開發設定](https://dash.immersivetranslate.com/#developer) -> Edit Full User Config

編輯 "enableRenderHtmlTag": true

### 不在 popup 面板中顯示未設定的翻譯服務

`"showUnconfiguredTranslationServiceInPopup": false`

### 翻譯服務設定

使用 `translationService` 選擇預設的翻譯引擎，目前支援：

```typescript
| "bing"
| "transmart"
| "google"
| "deepl"
| "openai"
| "gemini"
| "baidu"
| "volc"
| "youdao"
| "caiyun"
| "tencent"
| "openl"
```

使用 `translationServices` 設定各家翻譯服務的 `apikey`，不同供應商所需的參數不同，它們的 API 金鑰均可在各自官網的開發者中心申請。

例如騰訊翻譯君，需要設定 `secretId` 和 `secretKey`。你可以前往騰訊雲申請 API 金鑰，每月免費字元 500 萬。具體申請流程請參考[這裡](/docs/services/tencent)。

```json
"translationServices": {
  "tencent": {
    "secretId": "xxx",
    "secretKey": "xxx",
    "matches":["twitter.com"],
    "limit": 3,
    "apiUrl":"",
    "maxTextGroupLengthPerRequest": 25,
    "maxTextLengthPerRequest": 1800
  }
}
```

`matches` 欄位，為特定網站使用該翻譯服務。

`limit` 欄位，指定該翻譯服務的每秒最多請求數（有些服務會限制每秒最大請求數）。

`maxTextGroupLengthPerRequest` 欄位，每次請求最大的段落數。

`maxTextLengthPerRequest` 欄位，每次請求最大的字元數。

`apiUrl` 可以自定義翻譯介面的地址。

#### OpenAI Temperature 設定

OpenAI 的「temperature」參數用於調節語言模型輸出文本的隨機性和創造性。設定較低的溫度值（如 0.1 或 0.2）會生成更確定、一致且可預測的文字，而較高的溫度值（如 0.8 或 1.0）則使輸出更隨機、多樣化，增加文字的創造性。

具體設定在[開發者設定](https://dash.immersivetranslate. com/#developer) -> Edit Full User Config 中，找到 `openai` 對應的欄位，插入一條新欄位 `temperature` 即可完成設定。

示例如下：

```json
  "translationServices": {
    "openai": {
      "model": "gpt-3.5-turbo",
      "provider": "custom",
      "temperature": 1
    }
  },
```

### 總是翻譯特定網站

`translationUrlPattern` 設定總是指定翻譯的網站，以及從不翻譯的網站。

- `matches` 設定總是翻譯的網站，
- `excludeMatches` 設定從不翻譯的網站。

設定值可以是域名或帶有 `*` 的網址，例如：`www. google. com/ mail/*`

```json
"translationUrlPattern": {
    "matches": ["stackoverflow.com"]
    "excludeMatches": ["www.google.com/mail/*"]
}
```

### 總是翻譯特定語言

`languagePattern` 設定總是翻譯的語言，以及從不翻譯的語言。

- `matches` 設定總是翻譯的語言，例如：`en`
- `excludeMatches` 設定從不翻譯的語言。

### 譯文顯示格式

`translationTheme` 為翻譯內容的顯示格式，目前支援以下樣式：

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
| "thinDashed";
```

對應的中文名：

```json
{
  "none": "無",
  "dashed": "虛線下劃線",
  "dotted": "點狀下劃線",
  "underline": "直線下劃線",
  "mask": "模糊效果",
  "paper": "白紙陰影效果",
  "highlight": "高亮",
  "blockquote": "引用樣式",
  "weakening": "弱化",
  "italic": "斜體",
  "bold": "加粗",
  "thinDashed": "細虛線下劃線"
}
```

`translationThemePatterns` 可以為不同網站設定不同的譯文樣式

```json
"translationThemePatterns": {
  "underline": {
    "matches": ["discord.com"]
  }
}
```

### 類 gpt 頁面流訊息翻譯

```json
{
  "matches": ["chat.openai.com"], //類 gpt 網址
  "excludeSelectors": [".markdown *"],
  "aiRule": {
    "streamingSelector": ".result-streaming.markdown",
    "messageWrapperSelector": ".markdown",
    "streamingChange": true
  }
}
```

### 自定義專業術語的翻譯

由於某些翻譯引擎對專有名詞識別不理想，我們可以自定義專業術語確保它們在翻譯過程中不被轉換，或者按照我們設定的內容進行翻譯。如果希望不對某些專業術語進行翻譯，點選 [這裡](https://dash.immersivetranslate. com/#advanced) 新增對應單詞即可。如果希望將某些專業術語翻譯為指定的內容，可以透過在 [這裡](https://dash.immersivetranslate. com/#developer) - 【Edit Full User Config】輸入以下設定實現：  
注意 glossaries 鍵值 是放到 generalRule 鍵值下面

```json
"glossaries": [
    {
      "k": "LLM",
      "v": ""
    },
    {
      "k": "Tactic",
      "v": "策略"
    }
  ]
```

```json
"generalRule": {
  "glossaries": [...],
  ...
}
```

### Rules

`rules` 為陣列物件，可以用來設定針對特殊網站的規則，例如讓 Twitter 只翻譯某一部分區域：

```json
{
  "rules": [
    {
      "id": "twitter",
      "matches": ["twitter.com", "mobile.twitter.com", "tweetdeck.twitter.com"],
      "selectors": [
        "[data-testid='tweetText']",
        ".tweet-text",
        ".js-quoted-tweet-text",
        "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)",
        "[data-testid='developerBuiltCardContainer'] > div:nth-child(2)",
        "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)"
      ],
      "extraInlineSelectors": ["[data-testid=\"tweetText\"] div"]
    }
  ]
}
```

目前內建的 `rules` 可以在[這裡](https://github.com/immersive-translate/next-immersive_translate/blob/main/docs/buildin_config.json) 找到。

以下挑選部分重要欄位進行說明：

```typescript
export interface Rule {
  // 匹配網站
  id?: string; //系統每個適配的規則都有自己的 id，如果使用者想要複用這條規則在此基礎之上變動的話，需要在自己的規則上加上這個相應的 id 就可以複用了
  matches?: string | string[]; // 該條 Rule 將僅匹配此處的網站。
  excludeMatches?: string | string[]; // 排除特定的網站。
  selectorMatches?: string | string[]; // 用選擇器來匹配，而無需指定所有 url
  excludeSelectorMatches?: string | string[]; // 排除規則，同上。

  // 指定翻譯範圍
  selectors?: string | string[]; // 僅翻譯匹配到的元素
  excludeSelectors?: string | string[]; // 排除元素，不翻譯匹配的元素
  excludeTags?: string | string[]; // 排除 Tags，不翻譯匹配的 Tag

  // 追加翻譯範圍，而不是覆蓋
  additionalSelectors?: string | string[]; // 追加翻譯範圍。在智慧翻譯的區域，追加翻譯位置。
  additionalExcludeSelectors?: string | string[]; // 追加排除元素，讓智慧翻譯不翻譯特定位置。
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
  translationClasses?: string | string | string[]; // 為譯文新增額外的 Class

  // 全域性樣式
  globalStyles?: Record<string, string>; // 修改頁面樣式，若譯文導致頁面錯亂，這個很有用。`
  globalAttributes?: Record<string, Record<string, string>>; // 修改頁面元素的屬性

  // 嵌入樣式
  injectedCss?: string | string[]; // 嵌入 CSS 樣式
  additionalInjectedCss?: string | string[]; // 追加 CSS 樣式，而不是直接覆蓋。

  // 上下文
  wrapperPrefix?: string; // 譯文區域的字首，預設為 smart，根據字數決定是否換行。
  wrapperSuffix?: string; // 譯文區域的字尾

  // 譯文換行字數
  blockMinTextCount?: number; // 將譯文作為 block 的最小字元數，否則譯文為 inline 元素。
  blockMinWordCount?: number; // 同上。如果希望它們始終換行，可以都填 0.

  // 內容可翻譯的最小字數
  containerMinTextCount?: number; // 智慧識別時，元素最少包含的字元數，才會被翻譯，預設為 18
  paragraphMinTextCount?: number; // 原文段落的最小字元數，大於數字的內容將被翻譯
  paragraphMinWordCount?: number; // 原文段落的最小單詞數

  // 長段落強制換行字數
  lineBreakMaxTextCount?: number; // 開啟翻譯長段落時，強制進行分行的段落最大字元數。

  // 啟動翻譯的時機
  urlChangeDelay?: number; // 進入頁面後，延遲多少毫秒開始翻譯。為了等網頁的初始化，目前預設為 250ms
  observeUrlChange?: boolean; // 偵測 url 地址發生變化時，再次啟動翻譯，預設為 true。

  // 移動端
  isShowUserscriptPagePopup?: boolean; // 在移動裝置上展示頁面內的浮窗，預設為 true.
  fingerCountToToggleTranslagePageWhenTouching?: number; // 四指觸控則翻譯，可以設定為 0，2，3，4，5

  // AI streaming 翻譯
  aiRule: {
    streamingSelector: string; //gpt 網頁中標記正在翻譯元素的選擇器
    messageWrapperSelector: string; // 訊息正文選擇器
    streamingChange: boolean; //類 gpt 網頁反覆的訊息是增量更新還是全量更新。gpt 是增量
  };
}
```

### Rules matches 匹配邏輯

這部分介紹關於 `match` 的匹配方式，怎樣來匹配到對應的域名，這裡我們講的是單個 `match` 的，實際匹配的時候 `matches` 是個陣列，會嘗試讓每個 `match` 都去匹配，只要有一個匹配中，就算命中。

首先讓我們先確定好輸入形式，即我們的 `match` 支援哪些形式的有效輸入

- 省略主機號的`url`，如 `immersivetranslate. com`
- 一個有效的 `url`，有自己的協議，域名，或者路徑，如 `https://immersivetranslate.com`
- 上面都不滿足的情況下，會將輸入轉換成一個正規表示式去處理，在此基礎上再去匹配一些特定的規則

確定好輸入之後，讓我們簡單做個分類以更好地區分基本的`url`和帶有正規表示式的`url`：

- 匹配單個網站的 `match`，如 `https://immersivetranslate.com` 或者省略協議的 `immersivetranslate.com`
- 摻有正規表示式特殊符號的 `match`，如 `https://*/*sub.info=*fmoviesz.to*` 這裡會匹配特定的搜尋`url`參數，我們的程式會自動將後面那一串轉化為正規表示式以此來匹配對應的`url`，轉換之後的結果為`/^https:\/\/[^/]+?\/.*?sub. info=.*?fmoviesz. to.*?\/?$/`。這樣做的好處在於大幅降低了設定`match`的複雜性

在區分之後，對於這兩類 `match` 我們分開來講對應的匹配邏輯，在程式碼中也是如此，這兩類的匹配邏輯是分開的。在程式碼中我們是透過這個表達式 `!match.includes("*") && match.includes("://")` 來區分這兩類的 `match` 的

對於匹配單個站點的`match`的字串，即不含正規表示式相關符號的，需要考慮的問題有三個：

- 對於省略網路協議的 match 的處理：如 `immersivetranslate.com` 我們會直接判斷 `match` 是否等於`url`的 `hostname`，等於則匹配成功，即不會將 `match` 解析為 URL，將其作為 `hostname` 來判斷
- 對於多級路由的處理，分為兩種情況
  - 完整的 `match`，如 `https://immersivetranslate.com/docs/advanced/`,這類是有效的 URL，我們會將其解析為 URL，提取協議，主機名稱，連接埠以及路徑名稱來比較，當全部相等時則匹配成功
  - 省略了網路協議的`match`，如 `immersivetranslate.com/docs/advanced/` 由於這類是無效的 `url`，對於這類會將其歸類到正規表示式的邏輯處理裡面去

當上面的匹配策略都不生效時，就會到我們的兜底匹配，即將其識別為一個正規表示式，我們會對 `match` 進行轉換，將其轉換成一個有效的正規表示式。這部分的例子可以參照這個

> `https://*/*sub.info=*fmoviesz.to*` ==> `/^https:\/\/[^/]+?\/.*?sub.info=.*?fmoviesz.to.*?\/?$/`

最後總結一下我們的處理邏輯，1. 判斷 `url` 的 `hostname` 是否等於 `match` 字串，等於則匹配成功 2. 判斷匹配所有的 `url` 的 `match`，例如 `*`，`*://*`等等 3. 判斷 `match` 是否為一個有效的 `url`，我們會嘗試比較 `match` 和 `url` 是否相等。具體比較協議，連接埠，主機名稱，路徑名稱，相等則成功 4. 判斷 `match` 為一個正規表示式，將其轉換成一個有效的正規表示式並嘗試匹配 5. 都不滿足的話，則匹配失敗

### 翻譯服務自定義請求頭和請求體參數

在【[開發者設定](https://dash.immersivetranslate.com/#developer)】->【Edit Full User Config】

```
{
  ...
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
  ...
}
```

### 自定義多語言提示詞

下面展示了 openai 對於翻譯日語/中文繁體的提示詞修改

```
{
  ...
  "translationServices": {
    "openai.add": {
        "langOverrides": [
          {
          "id": "auto2ja",
          "systemPrompt": "あなたはプロフェッショナルで正確な翻訳エンジンです。翻訳されたテキストのみを返し、説明は一切行いません。",
          "prompt": "次のテキストを{{to}}に翻訳してください：\n\n<text>\n{{text}}\n</text>\n\n翻訳結果を直接出力し、追加のテキストやタグは一切含めないでください。",
          "multiplePrompt": "\"id\"フィールドと \"{{imt_source_field}}\" フィールドを含むYAML形式の入力が与えられます。以下が入力です：\n\n<yaml>\n{{yaml}}\n</yaml>\n\nYAMLの各エントリについて、\"{{imt_source_field}}\" フィールドの内容を {{to}} に翻訳してください。そのエントリの \"{{imt_source_field}}\" フィールドに翻訳結果を書き戻してください。\n\n以下は期待される形式の例です：\n\n{{normal_result_yaml_example}}\n\n追加のタグを一切含めずに、翻訳されたYAMLを直接返してください。",
          "subtitlePrompt": "YAML形式のビデオ字幕セットの \"{{imt_sub_source_field}}\" フィールドを {{to}} に翻訳します。以下がYAML形式の元の字幕です：\n\n<yaml_subtitles>\n{{yaml}}\n</yaml_subtitles>\n\n各字幕エントリの \"{{imt_sub_source_field}}\" フィールドのみを簡体字中国語に翻訳してください。\"id\" フィールドは翻訳や変更をしないでください。\n\n翻訳された字幕を同じYAML形式で出力し、各字幕エントリを一行ずつにしてください。\"id\" フィールドは変更せず、\"{{imt_sub_source_field}}\" フィールドに {{to}} の翻訳を含めてください。\n\n追加のタグを一切含めずに、翻訳されたYAMLを直接返してください。"
        },
        {
          "id": "auto2zh-TW",
          "systemPrompt": "你是一個專業的、地道的翻譯引擎。你只返回翻譯的文字，不做任何解釋。",
          "prompt": "將以下文字翻譯成 {{to}}：\n\n<text>\n{{text}}\n</text>\n\n直接輸出翻譯結果，不要新增任何額外的文字或標籤。",
          "multiplePrompt": "你將會得到一個包含 \"id\" 和 \"{{imt_source_field}}\" 欄位的 YAML 格式輸入。以下是輸入內容：\n\n<yaml>\n{{yaml}}\n</yaml>\n\n對於 YAML 中的每個條目，將 \"{{imt_source_field}}\" 欄位的內容翻譯成 {{to}}。將翻譯結果寫回每個條目的 \"{{imt_source_field}}\" 欄位。\n\n以下是期望的格式範例：\n\n{{normal_result_yaml_example}}\n\n請直接返回翻譯後的 YAML，不要新增任何額外的標籤。",
          "subtitlePrompt": "你將會翻譯一組 YAML 格式的影片字幕中的 \"{{imt_sub_source_field}}\" 欄位為 {{to}}。以下是原始字幕的 YAML 格式：\n\n<yaml_subtitles>\n{{yaml}}\n</yaml_subtitles>\n\n請僅翻譯每個字幕條目中的 \"{{imt_sub_source_field}}\" 欄位為簡體中文。不要翻譯或更改 \"id\" 欄位。\n\n以相同的 YAML 格式輸出翻譯後的字幕，每個字幕條目各佔一行。\"id\" 欄位應保持不變，\"{{imt_sub_source_field}}\" 欄位應包含你的 {{to}} 翻譯結果。\n\n請直接返回翻譯後的 YAML，不要新增任何額外的標籤。"
        }
        ]
      }
    }
  ...
}
```

## 進階自訂選項實戰

### 實用小技巧

這部分會介紹一些即插即用的保姆級設定。

將這些設定一鍵複製，開啟[開發者設定](https://dash.immersivetranslate.com/#developer)，展開 `Edit Full User Config` ，複製到最後一項即可，注意不要忘記給前一項加上逗號，以及最後一項不能加逗號

#### 不能用的翻譯服務太多了，如何在外掛面板裡只展示能用的翻譯服務

```json
  "showUnconfiguredTranslationServiceInPopup": false
```

#### 如何讓不同的站點預設選擇不同的翻譯服務？例如有的網站我想要好一點但要花錢的翻譯效果，有的網站我只需要免費能看的翻譯就行了

注意看，眼前這個設定叫翻譯服務，他設定了谷歌翻譯，讓有關推特的相關站點的翻譯都使用他去翻譯，因為 `google` 翻譯是免費的，推特是衝浪的，只要能看懂就行了。

仔細看，他還設定了 `deepl` 的翻譯服務，他讓 `deepl` 專門去翻譯 `scihub` 這種容錯率低的需要高精確的學術網站

```json
  "translationServices": {
    "google": {
      "matches":["https://twitter.com"]
    },
    "deepl": {
      "matches":["https://www.sci-hub.se"]
    }
  }
```

> ⚠️ 請注意，若您希望翻譯屬於同一域名的所有網站，簡單使用 _.twitter.com 或 https://twitter.com/ 是無效的。正確的做法應參照上文所示。這是因為 _.twitter.com 僅能匹配子域名如 xxx.twitter.com，而不包括頂級域名本身。

### 網站適配案例

這部分會介紹一些外掛自己對常見網站的 `rules`，透過實際例子來理解進階自訂選項。同時為了簡潔，這裡只會介紹最常用的欄位，比如 `selectors` 、 `excludeSelectors` 等等，如果你對這部分內容感興趣的話，歡迎聯絡我們，我們會繼續更新相關的內容。

在介紹之前，一個非常關鍵的東西就是沉浸式翻譯外掛的工作原理，同時也是個外掛的工作原理。在此之前，需要有一定的 `HTML` 、`CSS` 、 `JavaScript` 基礎，相關基礎可以在 `MDN` 網站上學習。Okay，話不多說，讓我們走進沉浸式翻譯的內部一探究竟。外掛的工作機制簡單來說，就是向網頁中注入第三方腳本，這個腳本可以對網頁結構，樣式，甚至行為進行相當自由地魔改。

我們的沉浸式翻譯外掛也不例外，讓我們來簡單分析一下沉浸式翻譯它幹了個什麼事

- 取得需要翻譯的元素集合
- 翻譯元素集合中的文字
- 將翻譯的結果插入到元素集合中

Okay，但是再仔細想想，自然而然就會帶出接下來兩個問題

- 我們還需要確定哪些元素需要被翻譯，如果全盤翻譯，往往會破壞使用者的沉浸式體驗，像一些簡單明瞭的按鈕，或者導航欄。
- 將翻譯的結果插入到元素集合中也會帶來一個新的挑戰，如何保證插入的結果與原生網頁保持一致，不去影響原生網頁的樣式。

我們的 `Rules` 的核心就是解決上述兩個問題。因為作為外掛，沉浸式翻譯面對的是市面上所有的網頁，加起來可能超過幾十萬，甚至數百萬的網頁，這些網頁的頁面結構，使用的技術也是各不相同。因為網頁的不同，導致了一個通用的邏輯是幾乎不可能的，很難找到一套通用的邏輯，能夠去適配所有的網站內容。這樣看來，解決方法似乎只有挨著挨著對每個網站進行單獨的適配。接著為了更方便地適配，我們又利用了設定即程式碼的思想，將適配的工作轉換成了設定欄位的工作。這樣的另一個好處就是，使用者也可以參與到適配工作起來。

同時，在進行設定的時候，最好不要直接使用下面幾個欄位，這樣會導致覆蓋掉原先的設定項，而是採用 `selector.add` 、`excludeSelector.add` 這些欄位以繼承的方式，在原先的設定項的基礎上進行修改。

下面，我們將會介紹沉浸式翻譯對站點的適配工作

下面是小.twitter 的 Rules，為了簡潔，我們將關注其中的幾個關鍵欄位，剩餘欄位可以結合上文中的 `Rules` 理解

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
      // 指定翻譯的元素，只會翻譯選擇器匹配到的元素
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
      // 不會翻譯的被 CSS 選擇器選中的元素
      "[aria-describedby][role=button]",
      "header",
      "[data-testid='radioGroupplayback_rate'] div",
      "[data-testid='userFollowIndicator']",
      "[class='css-901oao r-14j79pv r-37j5jr r-n6v787 r-16dba41 r-1cwl3u0 r-bcqeeo r-qvutc0']",
      "[class='css-175oi2r r-1wbh5a2 r-dnmrzs']"
    ],
    "globalStyles": {
      // 全域性樣式，強制覆蓋掉原樣式
      "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='tweetText']": "-webkit-line-clamp: unset;"
    }
  }
]
```

- `selector`: 指定翻譯的元素集合

  為什麼需要這個欄位

  - 因為不是所有元素都有文字且需要翻譯的，提供這樣一個欄位既可以保證效能又可以保證使用者的沉浸式體驗

  舉個例子

  - 在推特中，如果我們不指定 selector，那麼他將會將頁面中的所有識別為英文的文字都進行翻譯一遍，如下圖，使用者的暱稱往往是不需要翻譯的。

  ![使用者主頁](twitterUser. png)

  欄位含義

  ```
      "selectors": [ // 會被翻譯的 CSS 選擇器集合
      "[data-testid=\"tweetText\"]",
    ]
  ```

  這裡陣列的每一項都是一個 CSS 選擇器，用來選擇頁面中的需要翻譯的元素，這裡我們以第一個選擇器為例，如下圖所示，第一個選擇器命中的是所有推文的元素

  ![tweet](tweet.png)

- `excludeSelectors`: 不會被翻譯的元素集合

  為什麼需要這個欄位

  - 因為一個僅翻譯的選擇器是不夠的，可能會出現，匹配中的元素卻不需要翻譯的，即兩者可能存在重疊的部分，因此需要再設定一個欄位來排除掉不需要翻譯的元素
  - 由於網頁結構是非常複雜的，提供這樣兩個設定項，讓設定更加靈活
  - 相關的優先順序是：對於同等選擇器，selectors > excludeSelectors，剩下的依靠 CSS 優先順序來比較

  欄位含義

  ```
      "excludeSelectors": [ // 不會翻譯的被 CSS 選擇器選中的元素
      "[aria-describedby][role=button]",
    ],
  ```

  還是看第一個，這裡我們排除掉了關注按鈕的這個翻譯
  ![twitter-follow](twitter-follow.png)

- `globalStyles`：新增全域性樣式，強制覆蓋掉原先的樣式

  為什麼需要這個欄位

  - 在某些情況下，因為原先網頁的相關 CSS 樣式，會導致整個的翻譯展示效果不是很好，出現被截斷，不換行等等效果
  - 透過這個欄位，提供一種暴力的解決方案，直接修改原生網頁的 CSS 屬性來解決

  欄位含義

  ```
        "globalStyles": {
      // 全域性樣式，強制覆蓋掉原樣式
      "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='tweetText']": "-webkit-line-clamp: unset;"
    }
  ```

  `-webkit-line-clamp` 這個屬性用來控制顯示的行數，多餘的行會被截斷，這裡設定成 `unset` ，可以保證譯文不會被這個屬性所截斷

### 自定義網站適配

關於適配規則，當然你也可以自定義規則，進入到外掛選項頁面，點選[開發者設定](https://dash.immersivetranslate.com/#developer)，展開 `Edit User Rules` ，在這裡進行各個網站的自定義適配。下面結合實際規則進行講解

```
[
  {
    "selectors.remove": [
      "[data-testid=\"tweetText\"]"
    ],
    "selectors.add": [
      ""
    ],
    "excludeSelectors.add":[
      ""
    ],
    "excludeSelectors.remove:[
      ""
    ],
    "id": "twitter"
  }
]
```

這個規則會讓推特頁面的推文不進行翻譯。下面詳細介紹欄位的含義

`id` 是沉浸式翻譯已經定義好的相關網站的集合，每個 `id` 都對應相關的站點。`id` 的好處有兩個

- 使用 `id` 可以繼承沉浸式翻譯之前的適配規則，使用者可以在這基礎上進行增刪
- 使用 `id` 就不用寫繁瑣的匹配欄位了

下面介紹一些沉浸式翻譯內建服務的常見的 `id`

- `"isEbook"` epub 閱讀器頁面的設定
- `"isEbookBuilder"` 生成 epub 雙語書頁面的設定
- `"pdf"` pdf 雙語對照翻譯頁面的設定

完整的 `id` 集合可以在[開發者設定](https://dash.immersivetranslate. com/#developer)中，`Click to expand the final config` 中找到

`selectors` 負責指定需要翻譯的 CSS 選擇器，建議使用子項 `.add` `.remove` 在原先的基礎上進行增刪

`excludeSelectors` 負責排除不需要翻譯的 CSS 選擇器，建議使用子項 `.add` `.remove` 在原先的基礎上進行增刪

**更多講解**

Block 和 inline 的區別，如果想了解更多可以看[這裡](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Inline_elements#inline)

- block 元素會獨佔一行，多個相鄰的 block 元素會各自新起一行。
- inline 元素不會獨佔一行，多個相鄰的 inline 元素會排列在同一行裡，直到一行排列不下才會新換一行。
