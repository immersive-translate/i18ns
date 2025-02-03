---
sidebar_position: 4
---

# 高級自定義選項

你可以在擴展配置頁面 -> 開發者設定 -> User Config 裡編輯更多 UI 裡無法編輯的自定義配置，適用於高級用戶，參數講解詳見最後的說明。當前內置的 `config` 可以在[這裡](https://dash.immersivetranslate. com/#developer)，點擊 `Click to expand the final config` 找到。

## User Rules

通過 `Rules` 可以對特定的網站進行自定義配置，決定哪些內容是否需要被翻譯，或調整網頁樣式等。

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

使用 `matches` 來匹配對應的網站。允許通配符，如 `*.google.com`, `www.google.com/test/*`, `file://*`

使用 `selectors` 會覆蓋智慧翻譯範圍，僅翻譯該選擇器匹配到的元素。

使用 `excludeSelectors` 可以排除元素，不翻譯該位置。

使用 `selectors.add` 會在預設的基礎上添加一些 selectors

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

如果希望翻譯某個區域時，將元素視為一個整體，不将其分行，可以用 `atomicBlockSelectors` 選擇器。比如 Instagram 的個人資料介紹。

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

如果譯文導致頁面錯位，文字重疊等邊緣情況，可以使用 `globalStyles` 調整網頁樣式來修復。比如 youtube 的標題，用来移除原網頁的最大高度。

```json
{
  "matches": "www.google.com",
  "globalStyles": { ".title": "max-height:unset;" }
}
```

## Injected CSS

通過 Injected CSS 可以向全局注入自定義網頁樣式。可以搭配 `Rules` 的 `translationClasses` 一起使用。

```css
.immersive-translate-target-wrapper img {
  width: 16px;
  height: 16px;
}
```

也可以像常规的网页样式管理器那样，对网站进行更加个性化的样式设计。（甚至利用 `display:none` 去广告）

```css
.title {
  color: red;
}
```

## User Config

通過 Config 可以自訂義此插件的相關配置，如翻譯服務、特定語言翻譯選項等。

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

其中，`rules` 里的規則字段，可以使用 `generalRule` 里的全部字段。`rules` 拥有最高優先級，當匹配到特定網站的某一條 `rule` 時，會合併 `generalRule` 和該 `rule` 的規則。

介紹一些 Config 常見的字段。

### 允許渲染普通 HTML 標籤

前往 [開發設定](https://dash.immersivetranslate.com/#developer) -> Edit Full User Config

編輯 "enableRenderHtmlTag": true

### 不在 popup 面板中顯示未配置的翻譯服務

`"showUnconfiguredTranslationServiceInPopup": false`

### 翻譯服務配置

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

使用 `translationServices` 設置各家翻譯服務的 `apikey`，不同供應商所需的參數不同，它們的 API 密鑰均可在各自官網的開發者中心申請。

例如騰訊翻译君，需要配置 `secretId` 和 `secretKey`。你可以前往騰訊云申請 API 密鑰，每月免費字符 500 萬。具體申請流程請參考[這裡](/docs/services/tencent)。

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

`matches` 字段，為特定網站使用該翻譯服務。

`limit` 字段，指定該翻譯服務的每秒最多請求数（有些服務會限制每秒最大請求数）。

`maxTextGroupLengthPerRequest` 字段，每次請求最大的段落数。

`maxTextLengthPerRequest` 字段，每次請求最大的字符数。

`apiUrl` 可以自定義翻譯接口的地址。

#### OpenAI Temperature 設置

OpenAI 的「temperature」參數用於調節語言模型輸出文本的隨機性和創造性。設置較低的溫度值（如 0.1 或 0.2）會生成更確定、一致且可預測的文本，而較高的溫度值（如 0.8 或 1.0）則使輸出更隨機、多樣化，增加文本的創造性。

具體設置在[開發者設定](https://dash.immersivetranslate. com/#developer) -> Edit Full User Config 中，找到 `openai` 對應的字段，插入一條新字段 `temperature` 即可完成設置。

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

`translationUrlPattern` 配置總是指定翻譯的網站，以及從不翻譯的網站。

- `matches` 配置總是翻譯的網站，
- `excludeMatches` 配置從不翻譯的網站。

配置值可以是域名或帶有 `*` 的網址，例如：`www. google. com/ mail/*`

```json
"translationUrlPattern": {
    "matches": ["stackoverflow.com"]
    "excludeMatches": ["www.google.com/mail/*"]
}
```

### 總是翻譯特定語言

`languagePattern` 配置總是翻譯的语言，以及從不翻譯的语言。

- `matches` 配置總是翻譯的语言，例如：`en`
- `excludeMatches` 配置從不翻譯的语言。

### 译文顯示格式

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

对应的中文名：

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

`translationThemePatterns` 可以為不同網站配置不同的譯文樣式

```json
"translationThemePatterns": {
  "underline": {
    "matches": ["discord.com"]
  }
}
```

### 类 gpt 页面流消息翻译

```json
{
  "matches": ["chat.openai.com"], //类 gpt 网址
  "excludeSelectors": [".markdown *"],
  "aiRule": {
    "streamingSelector": ".result-streaming.markdown",
    "messageWrapperSelector": ".markdown",
    "streamingChange": true
  }
}
```

### 自定義專業術語的翻譯

由于某些翻译引擎对专有名词识别不理想，我们可以自定义专业术语确保它们在翻译过程中不被转换，或者按照我们设置的内容进行翻译。如果希望不对某些专业术语进行翻译，点击 [这里](https://dash.immersivetranslate. com/#advanced) 添加对应单词即可。如果希望将某些专业术语翻译为指定的内容，可以通过在 [这里](https://dash.immersivetranslate. com/#developer) - 【Edit Full User Config】输入以下配置实现：  
注意 glossaries 键值 是放到 generalRule 键值下面

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

`rules` 為數組物件，可以用來配置針對特殊網站的規則，例如讓 Twitter 只翻譯某一部分區域：

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

目前內置的 `rules` 可以在[這裡](https://github.com/immersive-translate/next-immersive_translate/blob/main/docs/buildin_config.json) 找到。

以下挑選部分重要字段進行說明：

```typescript
export interface Rule {
  // 匹配网站
  id?: string; //系统每个适配的规则都有自己的 id，如果用户想要复用这条规则在此基础之上变动的话，需要在自己的规则上加上这个相应的 id 就可以复用了
  matches?: string | string[]; // 该条 Rule 将仅匹配此处的网站。
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
  observeUrlChange?: boolean; // 检测 url 地址发生变化时，再次启动翻译，默认为 true。

  // 移动端
  isShowUserscriptPagePopup?: boolean; // 在移动设备上展示页面内的浮窗，默认为 true.
  fingerCountToToggleTranslagePageWhenTouching?: number; // 四指触摸则翻译，可以设置为 0，2，3，4，5

  // AI streaming 翻译
  aiRule: {
    streamingSelector: string; //gpt 网页中标记正在翻译元素的选择器
    messageWrapperSelector: string; // 消息正文选择器
    streamingChange: boolean; //类 gpt 网页反复的消息是增量更新还是全量更新。gpt 是增量
  };
}
```

### Rules matches 匹配逻辑

这部分介绍关于 `match` 的匹配方式，怎样来匹配到对应的域名，这里我们讲的是单个 `match` 的，实际匹配的时候 `matches` 是个数组，会尝试让每个 `match` 都去匹配，只要有一个匹配中，就算命中。

首先让我们先确定好输入形式，即我们的 `match` 支持哪些形式的合法输入

- 省略主机号的`url`，如 `immersivetranslate. com`
- 一个合法的 `url`，有自己的协议，域名，或者路径，如 `https://immersivetranslate.com`
- 上面都不满足的情况下，会将输入转换成一个正则表达式去处理，在此基础上再去匹配一些特定的规则

确定好输入之后，让我们简单做个分类以更好地区分基本的`url`和带有正则表达式的`url`：

- 匹配单个网站的 `match`，如 `https://immersivetranslate.com` 或者省略协议的 `immersivetranslate.com`
- 掺有正则表达式特殊符号的 `match`，如 `https://*/*sub.info=*fmoviesz.to*` 这里会匹配特定的搜索`url`参数，我们的程序会自动将后面那一串转化为正则表达式以此来匹配对应的`url`，转换之后的结果为`/^https:\/\/[^/]+?\/.*?sub. info=.*?fmoviesz. to.*?\/?$/`。这样做的好处在于大幅降低了配置`match`的复杂性

在区分之后，对于这两类 `match` 我们分开来讲对应的匹配逻辑，在代码中也是如此，这两类的匹配逻辑是分开的。在代码中我们是通过这个表达式 `!match.includes("*") && match.includes("://")` 来区分这两类的 `match` 的

对于匹配单个站点的`match`的字符串，即不含正则表达式相关符号的，需要考虑的问题有三个：

- 对于省略网络协议的 match 的处理：如 `immersivetranslate.com` 我们会直接判断 `match` 是否等于`url`的 `hostname`，等于则匹配成功，即不会将 `match` 解析为 URL，将其作为 `hostname` 来判断
- 对于多级路由的处理，分为两种情况
  - 完整的 `match`，如 `https://immersivetranslate.com/docs/advanced/`,这类是合法的 URL，我们会将其解析为 URL，提取协议，主机名，端口号以及路径名来比较，当全部相等时则匹配成功
  - 省略了网络协议的`match`，如 `immersivetranslate.com/docs/advanced/` 由于这类是不合法的 `url`，对于这类会将其归类到正则表达式的逻辑处理里面去

当上面的匹配策略都不生效时，就会到我们的兜底匹配，即将其识别为一个正则表达式，我们会对 `match` 进行转换，将其转换成一个合法的正则表达式。这部分的例子可以参照这个

> `https://*/*sub.info=*fmoviesz.to*` ==> `/^https:\/\/[^/]+?\/.*?sub.info=.*?fmoviesz.to.*?\/?$/`

最后总结一下我们的处理逻辑，1. 判断 `url` 的 `hostname` 是否等于 `match` 字符串，等于则匹配成功 2. 判断匹配所有的 `url` 的 `match`，例如 `*`，`*://*`等等 3. 判断 `match` 是否为一个合法的 `url`，我们会尝试比较 `match` 和 `url` 是否相等。具体比较协议，端口，主机名，路径名，相等则成功 4. 判断 `match` 为一个正则表达式，将其转换成一个合法的正则表达式并尝试匹配 5. 都不满足的话，则匹配失败

### 翻译服务自定义请求头和请求体参数

在【[開發者設置](https://dash.immersivetranslate.com/#developer)】->【Edit Full User Config】

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

### 自定义多语言提示词

下面展示了 openai 对于翻译日语/中文繁体的提示词修改

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
          "systemPrompt": "你是一個專業的、地道的翻譯引擎。你只返回翻譯的文本，不做任何解釋。",
          "prompt": "將以下文本翻譯成 {{to}}：\n\n<text>\n{{text}}\n</text>\n\n直接輸出翻譯結果，不要添加任何額外的文本或標籤。",
          "multiplePrompt": "你將會得到一個包含 \"id\" 和 \"{{imt_source_field}}\" 欄位的 YAML 格式輸入。以下是輸入內容：\n\n<yaml>\n{{yaml}}\n</yaml>\n\n對於 YAML 中的每個條目，將 \"{{imt_source_field}}\" 欄位的內容翻譯成 {{to}}。將翻譯結果寫回每個條目的 \"{{imt_source_field}}\" 欄位。\n\n以下是期望的格式範例：\n\n{{normal_result_yaml_example}}\n\n請直接返回翻譯後的 YAML，不要添加任何額外的標籤。",
          "subtitlePrompt": "你將會翻譯一組 YAML 格式的影片字幕中的 \"{{imt_sub_source_field}}\" 欄位為 {{to}}。以下是原始字幕的 YAML 格式：\n\n<yaml_subtitles>\n{{yaml}}\n</yaml_subtitles>\n\n請僅翻譯每個字幕條目中的 \"{{imt_sub_source_field}}\" 欄位為簡體中文。不要翻譯或更改 \"id\" 欄位。\n\n以相同的 YAML 格式輸出翻譯後的字幕，每個字幕條目各佔一行。\"id\" 欄位應保持不變，\"{{imt_sub_source_field}}\" 欄位應包含你的 {{to}} 翻譯結果。\n\n請直接返回翻譯後的 YAML，不要添加任何額外的標籤。"
        }
        ]
      }
    }
  ...
}
```

## 高级自定义选项实战

### 实用小技巧

这部分会介绍一些即插即用的保姆级配置。

将这些配置一键复制，打开[开发者设置](https://dash.immersivetranslate.com/#developer)，展开 `Edit Full User Config` ，复制到最后一项即可，注意不要忘记给前一项加上逗号，以及最后一项不能加逗号

#### 不能用的翻译服务太多了，如何在插件面板里只展示能用的翻译服务

```json
  "showUnconfiguredTranslationServiceInPopup": false
```

#### 如何让不同的站点默认选择不同的翻译服务？例如有的网站我想要好一点但要花钱的翻译效果，有的网站我只需要免费能看的翻译就行了

注意看，眼前这个配置叫翻译服务，他配置了谷歌翻译，让有关推特的相关站点的翻译都使用他去翻译，因为 `google` 翻译是免费的，推特是冲浪的，只要能看懂就行了。

仔细看，他还配置了 `deepl` 的翻译服务，他让 `deepl` 专门去翻译 `scihub` 这种容错率低的需要高精确的学术网站

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

> ⚠️ 请注意，若您希望翻译属于同一域名的所有网站，简单使用 _.twitter.com 或 https://twitter.com/ 是无效的。正确的做法应参照上文所示。这是因为 _.twitter.com 仅能匹配子域名如 xxx.twitter.com，而不包括顶级域名本身。

### 網站適配案例

這部分會介紹一些插件自己對常見網站的 `rules`，通過實際例子來理解高級自定義選項。同時為了簡潔，這裡只會介紹最常用的欄位，比如 `selectors` 、 `excludeSelectors` 等等，如果你對這部分內容感興趣的話，歡迎聯絡我們，我們會繼續更新相關的內容。

在介紹之前，一個非常關鍵的东西就是沉浸式翻譯插件的工作原理，同時也是個插件的工作原理。在此之前，需要有一定的 `HTML` 、`CSS` 、 `JavaScript` 基礎，相關基礎可以在 `MDN` 網站上學習。Okay，話不多說，讓我們走進沉浸式翻譯的內部一探究竟。插件的工作機制簡單來說，就是向網頁中注入第三方腳本，這個腳本可以對網頁結構，樣式，甚至行為進行相當自由地魔改。

我們的沉浸式翻譯插件也不例外，讓我們來簡單分析一下沉浸式翻譯它幹了個什麼事

- 獲取需要翻譯的元素集合
- 翻譯元素集合中的文本
- 將翻譯的結果插入到元素集合中

Okay，但是再仔細想想，自然而然就會帶出接下來兩個問題

- 我們還需要確定哪些元素需要被翻譯，如果全盤翻譯，往往會破壞用戶的沉浸式體驗，像一些簡單明瞭的按鈕，或者導航欄。
- 將翻譯的結果插入到元素集合中也會帶來一個新的挑戰，如何保證插入的結果與原生網頁保持一致，不去影響原生網頁的樣式。

我們的 `Rules` 的核心就是解決上述兩個問題。因為作為插件，沉浸式翻譯面對的是市面上所有的網頁，加起來可能超過幾十萬，甚至數百萬的網頁，這些網頁的頁面結構，使用的技术也是各不相同。因為網頁的不同，導致了一個通用的邏輯是幾乎不可能的，很難找到一套通用的邏輯，能夠去适配所有的網站內容。這樣看來，解決方法似乎只有挨著挨著對每個網站進行單獨的適配。接著為了更方便地適配，我們又利用了配置即代碼的思想，將適配的工作轉換成了配置欄位的工作。這樣的另一個好處就是，用戶也可以參與到适配工作起來。

同時，在進行配置的時候，最好不要直接使用下面幾個欄位，這樣會導致覆蓋掉原先的配置項，而是采用 `selector.add` 、`excludeSelector.add` 這些欄位以繼承的方式，在原先的配置項的基礎上進行修改。

下面，我們將會介紹沉浸式翻譯對站點的适配工作

下面是小.twitter 的 Rules，為了簡潔，我們將關注其中的幾個關鍵欄位，剩余欄位可以結合上文中的 `Rules` 理解

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
      // 指定翻译的元素，只会翻译选择器匹配到的元素
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
      // 不会翻译的被 CSS 选择器选中的元素
      "[aria-describedby][role=button]",
      "header",
      "[data-testid='radioGroupplayback_rate'] div",
      "[data-testid='userFollowIndicator']",
      "[class='css-901oao r-14j79pv r-37j5jr r-n6v787 r-16dba41 r-1cwl3u0 r-bcqeeo r-qvutc0']",
      "[class='css-175oi2r r-1wbh5a2 r-dnmrzs']"
    ],
    "globalStyles": {
      // 全局样式，强制覆盖掉原样式
      "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='tweetText']": "-webkit-line-clamp: unset;"
    }
  }
]
```

- `selector`: 指定翻译的元素集合

  为什么需要这个字段

  - 因為不是所有元素都有文字且需要翻譯的，提供這樣一個字段既可以保證性能又可以保證用戶的沉浸式體驗

  举个例子

  - 在推特中，如果我们不指定 selector，那么他将会将页面中的所有识别为英文的文字都进行翻译一遍，如下图，用户的昵稱往往是不需要翻譯的。

  ![用户主页](twitterUser. png)

  字段含义

  ```
      "selectors": [ // 会被翻译的 CSS 选择器集合
      "[data-testid=\"tweetText\"]",
    ]
  ```

  这里数组的每一项都是一个 CSS 选择器，用来选择页面中的需要翻译的元素，这里我们以第一个选择器为例，如下图所示，第一个选择器命中的是所有推文的元素

  ![tweet](tweet.png)

- `excludeSelectors`: 不会被翻译的元素集合

  为什么需要这个字段

  - 因為一個僅翻譯的选择器是不夠的，可能會出現，匹配中的元素卻不需要翻譯的，即兩者可能存在重疊的部分，因此需要再設置一個字段來排除掉不需要翻譯的元素
  - 由于網頁結構是非常複雜的，提供這樣兩個配置項，讓配置更加靈活
  - 相關的优先級是：對於同等選擇器，selectors > excludeSelectors，剩下的依靠 CSS 優先級來比較

  字段含義

  ```
      "excludeSelectors": [ // 不会翻译的被 CSS 选择器选中的元素
      "[aria-describedby][role=button]",
    ],
  ```

  还是看第一个，这里我们排除掉了关注按钮的这个翻译
  ![twitter-follow](twitter-follow.png)

- `globalStyles`：添加全局样式，强制覆盖掉原先的样式

  为什么需要这个字段

  - 在某些情况下，因为原先网页的相关 CSS 样式，会导致整个的翻译展示效果不是很好，出现被截断，不换行等等效果
  - 通过这个字段，提供一种暴力的解决方案，直接修改原生网页的 CSS 属性来解决

  字段含义

  ```
        "globalStyles": {
      // 全局样式，强制覆盖掉原样式
      "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='tweetText']": "-webkit-line-clamp: unset;"
    }
  ```

  `-webkit-line-clamp` 这个属性用来控制显示的行数，多余的行会被截断，这里设置成 `unset` ，可以保证译文不会被这个属性所截断

### 自定义网站适配

关于适配规则，当然你也可以自定义规则，进入到插件选项页面，点击[开发者设置](https://dash.immersivetranslate.com/#developer)，展开 `Edit User Rules` ，在这里进行各个网站的自定义适配。下面结合实际规则进行讲解

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

這個規則會讓推特頁面的推文不進行翻譯。下面詳細介紹字段的含義

`id` 是沉浸式翻譯已經定義好的相關網站的集合，每個 `id` 都對應相關的站點。`id` 的好處有兩個

- 使用 `id` 可以繼承沉浸式翻譯之前的適配規則，用戶可以在這基礎上進行增刪
- 使用 `id` 就不用寫繁瑣的匹配字段了

下面介紹一些沉浸式翻譯內置服務的常見的 `id`

- `"isEbook"` epub 閱讀器頁面的配置
- `"isEbookBuilder"` 生成 epub 雙語書頁面的配置
- `"pdf"` pdf 雙語對照翻譯頁面的配置

完整的 `id` 集合可以在[開發者設置](https://dash.immersivetranslate. com/#developer)中，`Click to expand the final config` 中找到

`selectors` 負責指定需要翻譯的 CSS 選擇器，建議使用子項 `.add` `.remove` 在原先的基礎上進行增刪

`excludeSelectors` 負責排除不需要翻譯的 CSS 選擇器，建議使用子項 `.add` `.remove` 在原先的基礎上進行增刪

**更多講解**

Block 和 inline 的區別，如果想了解更多可以看[這裡](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Inline_elements#inline)

- block 元素會獨佔一行，多個相鄰的 block 元素會各自新起一行。
- inline 元素不會獨佔一行，多個相鄰的 inline 元素會排列在同一行裡，直到一行排列不下才會新換一行。
