---
sidebar_position: 4
---

# 高级自定义选项

你可以在扩展配置页面 -> 开发者设置 -> User Config 里编辑更多 UI 里无法编辑的自定义配置，适用于高级用户，参数讲解详见最后的说明。当前内置的 `config` 可以在[这里](https://dash.immersivetranslate.com/#developer)，点击 `Click to expand the final config` 找到。

## User Rules

通过 `Rules` 可以对特定的网站进行自定义配置，决定哪些内容是否需要被翻译，或调整网页样式等。

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

使用 `matches` 来匹配对应的网站。允许通配符，如 `*.google.com`,`www.google.com/test/*`,`file://*`

使用 `selectors` 会覆盖智能翻译范围，仅翻译该选择器匹配到的元素。

使用 `excludeSelectors` 可以排除元素，不翻译该位置。

使用 `selectors.add` 会在默认的基础上添加一些 selectors

使用 `selectors.remove` 会在默认的基础上减少一些 selectors

```json
[
  {
    "matches": "www.google.com",
    "selectors.add": ["baidu.com"],
    "excludeSelectors": ["buzzing.cc"]
  }
]
```

如果希望翻译某个区域时，将元素视为一个整体，不将其分行，可以用 `atomicBlockSelectors` 选择器。比如 Instagram 的个人简介。要注意的是，使用 `atomicBlockSelectors` 前需要先用 `selectors` 进行选择。

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

如果译文导致页面错位，文字重叠等边缘情况，可以使用 `globalStyles` 调整网页样式来修复。比如 youtube 的标题，用来移除原网页的最大高度。

```json
{
  "matches": "www.google.com",
  "globalStyles": { ".title": "max-height:unset;" }
}
```

## Injected CSS

通过 Injected CSS 可以向全局注入自定义网页样式。可以搭配 `Rules` 的 `translationClasses` 一起使用。

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

通过 Config 可以自定义此插件的相关配置，如翻译服务、特定语言语言翻译选项等。

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

其中，`rules` 里的规则字段，可以使用 `generalRule` 里的全部字段。`rules` 拥有最高优先级，当匹配到特定网站的某一条 `rule` 时，会合并 `generalRule` 和该 `rule` 的规则。

介绍一些 Config 常见的字段。

### 允许渲染普通 HTML 标签

去 [开发设置](https://dash.immersivetranslate.com/#developer) -> Edit Full User Config

编辑 "enableRenderHtmlTag": true

### 不在 popup 面板里展示未配置的翻译服务

`"showUnconfiguredTranslationServiceInPopup": false`

### 翻译服务配置

使用 `translationService` 选择默认的翻译引擎，当前支持：

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

使用 `translationServices` 配置各家翻译服务的 `apikey`，不同服务商需要的参数不一样，它们的 API 密钥均可在各自官网的开发者中心申请。

如腾讯翻译君，需要配置 `secretId`, `secretKey`。你可以前往腾讯云申请 API 密钥，每月免费字符 500 万。具体申请过程参考[这里](/docs/services/tencent)

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

`matches` 字段，为特定网站使用该翻译服务。

`limit`字段，指定该翻译服务的每秒最多请求数（有些服务会限制每秒最大请求数）。

`maxTextGroupLengthPerRequest` 字段，每次请求最大的段落数

`maxTextLengthPerRequest` 字段，每次请求最大的字符数

`apiUrl` 可以自定义翻译接口的地址。

#### openai temperature 设置

openai 的"temperature"参数用于调节语言模型的输出文本的随机性和创造性。设置较低的温度值（如 0.1 或 0.2）会生成更确定、一致且可预测的文本，而较高的温度值（如 0.8 或 1.0）则使输出更随机、多样化，增加文本的创造性。

具体设置在[开发设置](https://dash.immersivetranslate.com/#developer) -> Edit Full User Config 中，找到 `openai` 对应的字段，插入一条新字段 `temperature` 即可完成设置。

示例如下

```json
  "translationServices": {
    "openai": {
      "model": "gpt-3.5-turbo",
      "provider": "custom",
      "temperature": 1
    }
  },
```

### 总是翻译特定网站

`translationUrlPattern` 配置总是翻译的网站，以及永不翻译的网站。

- `matches` 配置总是翻译的网站，
- `excludeMatches` 配置永不翻译的网站。

配置值可以是域名或带有 `*` 的网址，比如：`www.google.com/mail/*`

```json
"translationUrlPattern": {
    "matches": ["stackoverflow.com"]
    "excludeMatches": ["www.google.com/mail/*"]
}
```

### 总是翻译特定语言

translationLanguagePattern, 配置总是翻译的语言，以及永不翻译的语言。

- `matches` 配置总是翻译的语言，比如 `en`,
- `excludeMatches` 配置永不翻译的语言。

### 译文显示格式

`translationTheme` 为译文的显示格式，当前支持以下样式：

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
  "none": "无",
  "dashed": "虚线下划线",
  "dotted": "点状下划线",
  "underline": "直线下划线",
  "mask": "模糊效果",
  "paper": "白纸阴影效果",
  "highlight": "高亮",
  "blockquote": "引用样式",
  "weakening": "弱化",
  "italic": "斜体",
  "bold": "加粗",
  "thinDashed": "细虚线下划线"
}
```

`translationThemePatterns` 可以为不同网站配置不同的译文样式。

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

### 自定义专业术语的翻译

当前方案原理是通过让翻译服务保留占位符实现，所以不一定能完全保证替换

由于某些翻译引擎对专有名词识别不理想，我们可以自定义专业术语确保它们在翻译过程中不被转换，或者按照我们设置的内容进行翻译。如果希望不对某些专业术语进行翻译，点击 [这里](https://dash.immersivetranslate.com/#advanced) 添加对应单词即可。如果希望将某些专业术语翻译为指定的内容，可以通过在 [这里](https://dash.immersivetranslate.com/#developer)

【近期会重新规划术语功能，届时会提供更灵活的配置方式。】

- 【Edit Full User Config】输入以下配置实现：

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

`rules` 为数组对象，可以配置针对特别网站的规则，比如让推特只翻译某一部分区域：

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

当前内置的 `rules` 可以在[这里](https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json) 找到。

以下挑选部分重要字段进行说明：

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

- 省略主机号的`url`，如 `immersivetranslate.com`
- 一个合法的 `url`，有自己的协议，域名，或者路径，如 `https://immersivetranslate.com`
- 上面都不满足的情况下，会将输入转换成一个正则表达式去处理，在此基础上再去匹配一些特定的规则

确定好输入之后，让我们简单做个分类以更好地区分基本的`url`和带有正则表达式的`url`：

- 匹配单个网站的 `match`，如 `https://immersivetranslate.com` 或者省略协议的 `immersivetranslate.com`
- 掺有正则表达式特殊符号的 `match`，如 `https://*/*sub.info=*fmoviesz.to*` 这里会匹配特定的搜索`url`参数，这里我们的程序会自动将后面那一串转化为正则表达式以此来匹配对应的`url`，转换之后的结果为`/^https:\/\/[^/]+?\/.*?sub.info=.*?fmoviesz.to.*?\/?$/`。这样做的好处在于大幅降低了配置`match`的复杂性

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

在【[开发者设置](https://dash.immersivetranslate.com/#developer)】->【Edit Full User Config】

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
}
```

#### Gemini 系列模型用户如何自定义配置

由于 Gemini 系列模型的特殊性，插件内置了部分设置。用户若想覆盖插件内置的设置，可以参考以下配置：

```json
{
...
"translationServices": {
    "gemini": {
      "modelsOverrides": [
        // 指定要重写的模型，这里重写了 gemini-2.5-flash 和 gemini-2.5-flash-lite 两个模型
        "models": [
          "gemini-2.5-flash",
          "gemini-2.5-flash-lite"
        ]
      ]
    }
  },
...
}
```

### 自定义翻译的令牌比例校验

> 为规避大语言模型的"幻觉"现象，我们内置了一项翻译质量校验机制。程序会通过计算响应文本与请求文本的令牌（Token）比例来评估结果的合理性。如果该比例异常（过高或过低），翻译将被视为无效并触发备用方案。
>
> 若您在"自定义专家模式"中有意让模型输出与原文长度差异较大的内容（例如执行摘要、扩写等任务），则可能需要调整此校验设置。您可以通过以下选项覆盖默认行为，以确保自定义指令正常执行。
>
> 具体来说，您可以调整以下两个参数：
>
> - `maxTokensRatio`：定义了响应文本与请求文本之间的最大允许令牌数比例。如果实际比例超过此设定值，系统会判定响应过长，并将其视为无效。
> - `minTokensRatio`：定义了响应文本与请求文本之间的最小允许令牌数比例。如果实际比例低于此设定值，系统会判定响应过短，并将其视为无效。

```json
...
  "translationServices": {
    "claude": {
      "maxTokensRatio": 8,
      "minTokensRatio": 0.21,
    }
  ...
```

### 修改默认翻译缓存自动清理时长

插件针对翻译缓存，默认 30 天自动清除。目的是为了防止缓存过大，导致后续翻译卡顿。可以如下操作修改默认值

在【[开发者设置](https://dash.immersivetranslate.com/#developer)】->【Edit Full User Config】

```
{
  cacheMaxAgeDay: 30,
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
          "subtitlePrompt": "YAML形式のビデオ字幕セットの \"{{imt_sub_source_field}}\" フィールドを {{to}} に翻訳します。以下がYAML形式の元の字幕です：\n\n<yaml_subtitles>\n{{yaml}}\n</yaml_subtitles>\n\n各字幕エントリの \"{{imt_sub_source_field}}\" フィールドのみを簡体字中国語に翻訳してください。\"id\" フィールドは翻訳や変更をしないでください。\n\n翻訳された字幕を同じYAML形式で出力し、各字幕エントリを一行ずつにしてください。\"id\" フィールドは変更せず、\"{{imt_sub_source_field}}\" フィールドに {{to}} の翻訳を含めてください。\n\n請直接返回翻訳後の YAML，不要添加任何額外的標籤。"
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

### 网站适配案例

这部分会介绍一些插件自己对常见的网站的 `rules`，通过实际例子来理解高级自定义选项。同时为了简洁，这里只会介绍最常用的字段，比如 `selectors` , `excludeSelectors` 等等，如果你对这部分内容感兴趣的话，欢迎联系我们，我们会继续更新相关的内容。

在介绍之前，一个非常关键的东西就是沉浸式翻译插件的工作原理，同时也是一个插件的工作原理。在此之前，需要有一定的 `HTML` 、`CSS` 、 `JavaScript` 基础，相关基础可以在 `MDN` 网站上学习。Okay，话不多说，让我们走进沉浸式翻译的内部一探究竟。插件的工作机制简单来说，就是向网页中注入第三方脚本，这个脚本可以对网页结构，样式，甚至行为进行相当自由地魔改。

我们的沉浸式翻译插件也不例外，让我们来简单分析一下沉浸式翻译它干了个什么事

- 获取需要翻译的元素集合
- 翻译元素集合中的文本
- 将翻译的结果插入到元素集合中

Okay，但是再仔细想想，自然而然就会带出接下来两个问题

- 我们还需要确定哪些元素需要被翻译，如果全盘翻译，往往会破坏用户的沉浸式体验，像一些简单明了的按钮，或者导航栏。
- 将翻译的结果插入到元素集合中也会带来一个新的挑战，如何保证插入的结果与原生网页保持一致，不去影响原生网页的样式。

我们的 `Rules` 的核心就是解决上述两个问题。因为作为插件，沉浸式翻译面对的是市面上所有的网页，加起来可能超过几十万，甚至几百万的网页，这些网页的页面结构，使用的技术也是相差殆尽。因为网页的不同，导致了一个通用的逻辑是几乎不可能的，很难找到一套通用的逻辑，能够去适配所有的网站内容。这样看来，解决方法似乎只有挨着挨着对每个网站进行单独的适配。接着为了更方便地适配，我们又利用了配置即代码的思想，将适配的工作转换成了配置字段的工作。这样的另一个好处就是，用户也可以参与到适配工作起来。

同时，在进行配置的时候，最好不要直接使用下面几个字段，这样会导致覆盖掉原先的配置项，而是采用 `selector.add` `excludeSelector.add` 这几个字段以继承的方式，在原先的配置项的基础上进行修改

下面，我们将会介绍沉浸式翻译对站点的适配工作

下面是推特的 Rules，为了简洁，我们将关注其中的几个关键字段，剩余字段可以结合上文中的 `Rules` 理解

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

  - 因为不是所有元素都有文字且需要翻译的，提供这样一个字段既可以保证性能又可以保证用户的沉浸式体验

  举个例子

  - 在推特中，如果我们不指定 selector，那么他将会将页面中的所有识别为英文的文字都进行翻译一遍，如下图，用户的昵称往往是不需要翻译的。

  ![用户主页](twitterUser.png)

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

  - 因为一个仅翻译的选择器是不够的，可能会出现，匹配中的元素却不需要翻译的，即两者可能存在重合的部分，因此需要再设置一个字段来排除掉不需要翻译的元素
  - 由于页面结构是非常复杂的，提供这样两个配置项，让配置更加灵活
  - 相关的优先级是：对于同等选择器，selectors > excludeSelectors，剩下的依靠 CSS 优先级来比较

  字段含义

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

这个规则会让推特页面的推文不进行翻译。下面详细介绍字段的含义

`id` 是沉浸式翻译目前已经定义好的相关网站的集合，每个 `id` 都对应相关的站点。`id` 的好处有两个

- 使用 `id` 能继承沉浸式翻译之前的适配规则，用户可以在这基础上进行增删
- 使用 `id` 就不用写繁琐的匹配字段了

下面介绍一些沉浸式翻译内置服务的常见的 `id`

- `"isEbook"` epub 阅读器页面的配置
- `"isEbookBuilder"` 生成 epub 双语书页面的配置
- `"pdf"` pdf 双语对照翻译页面的配置

完整的 `id` 集合可以在[开发者设置](https://dash.immersivetranslate.com/#developer)中，`Click to expand the final config` 中找到

`selectors` 负责指定需要翻译的 CSS 选择器，建议使用子项 `.add` `.remove` 在原先的基础上进行增删

`excludeSelectors` 负责排除不需要翻译的 CSS 选择器，建议使用子项 `.add` `.remove` 在原先的基础上进行增删

**更多讲解**

Block 和 inline 的区别，如果想了解更多可以看[这里](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements#inline)

- block 元素会独占一行，多个相邻的 block 元素会各自新起一行。
- inline 元素不会独占一行，多个相邻的 inline 元素会排列在同一行里，直到一行排列不下才会新换一行。
