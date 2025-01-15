---
sidebar_position: 4
---

# 高度なカスタマイズオプション

拡張機能の設定ページ -> 開発者設定 -> User Config で、UI では編集できないより多くのカスタマイズ設定を編集できます。これは上級ユーザー向けで、パラメータの詳細な説明は最後にあります。現在組み込まれている `config` は[こちら](https://dash.immersivetranslate.com/#developer)で確認できます。`Click to expand the final config` をクリックしてください。

## ユーザールール

`Rules` を通じて、特定のウェブサイトに対してカスタム設定を行い、どのコンテンツを翻訳するか、またはウェブページのスタイルを調整するかを決定できます。

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

`matches` を使用して、対応するウェブサイトをマッチさせます。ワイルドカードが許可されており、例えば `*.google.com`、`www.google.com/test/*`、`file://*` などです。

`selectors` を使用すると、スマート翻訳の範囲を上書きし、そのセレクタにマッチした要素のみを翻訳します。

`excludeSelectors` を使用すると、特定の要素を除外し、その部分を翻訳しないようにします。

`selectors.add` を使用すると、デフォルトにいくつかのセレクタを追加します。

`selectors.remove` を使用すると、デフォルトからいくつかのセレクタを減らします。

```json
[
  {
    "matches": "www.google.com",
    "selectors.add": ["baidu.com"],
    "excludeSelectors": ["buzzing.cc"]
  }
]
```

特定のエリアを翻訳する際に、要素を一つのブロックとして扱い、分割しないようにする場合は、`atomicBlockSelectors` セレクタを使用できます。例えば、Instagram のプロフィールなどです。`atomicBlockSelectors` を使用する前に、`selectors` で選択する必要があります。

```json
{
  "matches": "https://www.instagram.com/*",
  "selectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"],
  "atomicBlockSelectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"]
}
```

翻訳によってページのレイアウトが崩れたり、テキストが重なったりするようなエッジケースでは、`globalStyles` を使用してウェブページのスタイルを調整し、修正できます。例えば、YouTube のタイトルで、元のウェブページの最大高さを削除します。

```json
{
  "matches": "www.google.com",
  "globalStyles": { ".title": "max-height:unset;" }
}
```

## 注入された CSS

注入された CSS を使用すると、カスタム Web ページスタイルをグローバルに注入できます。`Rules`の`translationClasses`と一緒に使用することもできます。

```css
.immersive-translate-target-wrapper img {
  width: 16px;
  height: 16px;
}
```

また、通常の Web ページスタイルマネージャーのように、ウェブサイトにさらに個性的なスタイルを設計することもできます。（`display:none`を使用して広告を非表示にすることも可能です）

```css
.title {
  color: red;
}
```

## ユーザー設定

Config を通じて、翻訳サービスや特定の言語オプションなど、このプラグインの関連設定をカスタマイズできます。

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

ここで、`rules` 内のルールフィールドは、`generalRule` 内のすべてのフィールドを使用できます。`rules` は最優先され、特定のウェブサイトの特定の `rule` にマッチした場合、`generalRule` とその `rule` のルールがマージされます。

Config の一般的なフィールドについていくつか紹介します。

### 通常の HTML タグのレンダリングを許可する

[開発者設定](https://dash.immersivetranslate.com/#developer) に移動 -> Full User Config を編集

"enableRenderHtmlTag": true を編集

### ポップアップパネルに未設定の翻訳サービスを表示しない

`"showUnconfiguredTranslationServiceInPopup": false`

### 翻訳サービスの設定

`translationService` を使用して、デフォルトの翻訳エンジンを選択します。現在サポートされているのは以下の通りです：

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

`translationServices` を使用して、各翻訳サービスの `apikey` を設定します。異なるサービスプロバイダーでは必要なパラメーターが異なります。それらの API キーは、それぞれの公式ウェブサイトの開発者センターで申請できます。

例えば、腾讯翻訳君の場合、`secretId`, `secretKey` を設定する必要があります。腾讯クラウドで API キーを申請することができ、毎月 500 万文字まで無料です。具体的な申請プロセスは[こちら](/docs/services/tencent)を参照してください。

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

`matches` フィールドは、特定のウェブサイトでこの翻訳サービスを使用するためのものです。

`limit` フィールドは、この翻訳サービスの 1 秒あたりの最大リクエスト数を指定します（一部のサービスでは、1 秒あたりの最大リクエスト数に制限があります）。

`maxTextGroupLengthPerRequest` フィールドは、1 回のリクエストでの最大段落数です。

`maxTextLengthPerRequest` フィールドは、1 回のリクエストでの最大文字数です。

`apiUrl` は、翻訳インターフェースのアドレスをカスタマイズするために使用できます。

### 特定のウェブサイトを常に翻訳する

`translationUrlPattern` 設定は、常に翻訳するウェブサイトと、決して翻訳しないウェブサイトを指定します。

- `matches` は常に翻訳するウェブサイトを指定します。
- `excludeMatches` は決して翻訳しないウェブサイトを指定します。

設定値はドメイン名または `*` を含む URL である可能性があります。例：`www.google.com/mail/*`

```json
"translationUrlPattern": {
    "matches": ["stackoverflow.com"],
    "excludeMatches": ["www.google.com/mail/*"]
}
```

### 特定の言語を常に翻訳する

translationLanguagePattern は、常に翻訳する言語と、決して翻訳しない言語を設定します。

- `matches` は常に翻訳する言語を指定します。例えば `en` です。
- `excludeMatches` は決して翻訳しない言語を指定します。

### 翻訳表示形式

`translationTheme`は翻訳の表示形式で、現在以下のスタイルがサポートされています：

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

対応する日本語名：

```json
{
  "none": "なし",
  "dashed": "破線の下線",
  "dotted": "点線の下線",
  "underline": "直線の下線",
  "mask": "ぼかし効果",
  "paper": "紙の影効果",
  "highlight": "ハイライト",
  "blockquote": "引用スタイル",
  "weakening": "弱化",
  "italic": "イタリック",
  "bold": "太字",
  "thinDashed": "細い破線の下線"
}
```

`translationThemePatterns`は、異なるウェブサイトに異なる翻訳スタイルを設定することができます。

```json
"translationThemePatterns": {
  "underline": {
    "matches": ["discord.com"]
  }
}
```

### GPT 風ページのストリームメッセージ翻訳

```json
{
  "matches": ["chat.openai.com"], // GPT 風のウェブサイトアドレス
  "excludeSelectors": [".markdown *"],
  "aiRule": {
    "streamingSelector": ".result-streaming.markdown",
    "messageWrapperSelector": ".markdown",
    "streamingChange": true
  }
}
```

### ルール

`rules` は配列オブジェクトで、特定のウェブサイトに対するルールを設定できます。例えば、Twitter で特定のエリアのみを翻訳するように設定することができます：

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

現在の内蔵されている `rules` は[ここ](https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json)で見つけることができます。

以下、重要なフィールドをいくつか選んで説明します：

```typescript
export interface Rule {
  // ウェブサイトをマッチング
  id?: string; // システムにはそれぞれの適応ルールに対して id があり、ユーザーがこのルールを再利用して変更したい場合、自分のルールにこの id を追加することで再利用できます
  matches?: string | string[]; // この Rule はここで指定されたウェブサイトにのみマッチします。
  excludeMatches?: string | string[]; // 特定のウェブサイトを除外します。
  selectorMatches?: string | string[]; // セレクターでマッチングし、すべての URL を指定する必要はありません
  excludeSelectorMatches?: string | string[]; // 除外ルール、上記と同じです。

  // 翻訳範囲を指定
  selectors?: string | string[]; // マッチした要素のみを翻訳します
  excludeSelectors?: string | string[]; // 要素を除外し、マッチした要素を翻訳しません
  excludeTags?: string | string[]; // タグを除外し、マッチしたタグを翻訳しません

  // 翻訳範囲を追加、上書きではない
  additionalSelectors?: string | string[]; // 翻訳範囲を追加します。インテリジェント翻訳のエリアに翻訳位置を追加します。
  additionalExcludeSelectors?: string | string[]; // 追加で要素を除外し、インテリジェント翻訳が特定の位置を翻訳しないようにします。
  additionalExcludeTags?: string | string[]; // 追加でタグを除外します

  // オリジナルを保持
  stayOriginalSelectors?: string | string[]; // マッチした要素はオリジナルのまま保持されます。フォーラムサイトのタグなどによく使用されます。
  stayOriginalTags?: string | string[]; // マッチしたタグはオリジナルのまま保持されます。例えば `code`

  // エリア翻訳
  atomicBlockSelectors?: string | string[]; // エリアセレクター、マッチした要素は一つの全体として見られ、分割して翻訳されません
}
```

```javascript
  atomicBlockTags?: string | string[]; // エリア Tag セレクタ、上記と同じ

  // Block または Inline
  extraBlockSelectors?: string | string[]; // 追加のセレクタ、マッチした要素は block 要素として扱われ、独立した行になります。
  extraInlineSelectors?: string | string[]; // 追加のセレクタ、マッチした要素は inline 要素として扱われます。

  inlineTags?: string | string[]; // マッチした Tag は inline 要素として扱われます
  preWhitespaceDetectedTags?: string | string[]; // マッチした Tag は自動的に改行されます

  // 翻訳スタイル
  translationClasses?: string | string | string[]; // 翻訳テキストに追加の Class を付与

  // グローバルスタイル
  globalStyles?: Record<string, string>; // ページスタイルを変更、翻訳によってページが乱れる場合に役立ちます。
  globalAttributes?: Record<string, Record<string, string>>; // ページ要素の属性を変更

  // 埋め込みスタイル
  injectedCss?: string | string[]; // CSS スタイルを埋め込む
  additionalInjectedCss?: string | string[]; // CSS スタイルを追加、上書きではなく。

  // コンテキスト
  wrapperPrefix?: string; // 翻訳エリアのプレフィックス、デフォルトは smart、文字数に基づいて改行するかどうかを決定。
  wrapperSuffix?: string; // 翻訳エリアのサフィックス

  // 翻訳改行文字数
  blockMinTextCount?: number; // 翻訳テキストを block として扱う最小文字数、それ以外の場合は inline 要素。
  blockMinWordCount?: number; // 上記と同じ。常に改行させたい場合は、0 を入力。

  // 翻訳可能な最小文字数
  containerMinTextCount?: number; // スマート認識時、翻訳される要素が含むべき最小文字数、デフォルトは 18
  paragraphMinTextCount?: number; // オリジナル段落の最小文字数、この数を超える内容は翻訳される
  paragraphMinWordCount?: number; // オリジナル段落の最小単語数

  // 長い段落の強制改行文字数
  lineBreakMaxTextCount?: number; // 長い段落の翻訳を開始する際、強制的に分行される最大文字数。

  // 翻訳開始のタイミング
  urlChangeDelay?: number; // ページに入った後、何ミリ秒遅延して翻訳を開始するか。ページの初期化を待つため、現在のデフォルトは 250ms です
  observeUrlChange?: boolean; // URL アドレスが変更されたときに、再度翻訳を開始するかどうか、デフォルトは true です。

  // モバイル端末
  isShowUserscriptPagePopup?: boolean; // モバイルデバイス上でページ内ポップアップを表示するか、デフォルトは true です。
  fingerCountToToggleTranslagePageWhenTouching?: number; // 4 本指タッチで翻訳、0、2、3、4、5 に設定可能

  // AI streaming 翻訳
  aiRule: {
    streamingSelector: string; // gpt ページ内で翻訳中の要素をマークするセレクタ
    messageWrapperSelector: string; // メッセージ本文のセレクタ
    streamingChange: boolean; // gpt のようなページでメッセージが増分更新されるか全量更新されるか。gpt は増分
  };
}
```

## 高度なカスタマイズオプションの実践

### 実用的な小技

このセクションでは、プラグアンドプレイできる保育士レベルの設定をいくつか紹介します。

これらの設定をコピーして一発で[開発者設定](https://dash.immersivetranslate.com/#developer)を開き、`Edit Full User Config`を展開し、最後の項目にコピーしてください。前の項目にカンマを追加するのを忘れないでください。また、最後の項目にはカンマを追加しないでください。

#### 使用できない翻訳サービスが多すぎます。プラグインパネルで使用できる翻訳サービスのみを表示するにはどうすればよいですか？

```json
  "showUnconfiguredTranslationServiceInPopup": false
```

#### 異なるサイトがデフォルトで異なる翻訳サービスを選択するにはどうすればよいですか？例えば、あるサイトではお金を払ってでも良い翻訳品質を求め、別のサイトでは無料で読める翻訳で十分だと思うかもしれません。

注意してください、これは「翻訳サービス」という設定です。これは Google 翻訳を設定しており、Twitter に関連するサイトの翻訳にはすべてこれを使用するようにしています。Google 翻訳は無料で、Twitter はサーフィン用なので、理解できればそれで十分です。

さらに詳しく見ると、`deepl`の翻訳サービスも設定されています。これは`deepl`に、誤りの許容率が低く、高精度が求められる学術サイト`scihub`の翻訳を専門にさせています。

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

> ⚠️ 注意してください。同一ドメインのすべてのサイトを翻訳する場合、_.twitter.com や https://twitter.com/を単純に使用するのは無効です。上記のように正しく設定する必要があります。これは、_.twitter.com が xxx.twitter.com のようなサブドメインにのみ一致し、トップレベルドメイン自体は含まれないためです。

### ウェブサイトの適応事例

この部分では、一般的なウェブサイトに対するプラグイン自身の`rules`について、実際の例を通して高度なカスタマイズオプションを理解します。同時に、簡潔さを保つため、ここでは最もよく使用されるフィールドのみを紹介します。例えば、`selectors`、`excludeSelectors`などです。この内容に興味がある場合は、ぜひお問い合わせください。関連内容の更新を続けていきます。

紹介する前に、非常に重要なことは、没入型翻訳プラグインの動作原理、そしてそれがプラグインの動作原理でもあることです。その前に、`HTML`、`CSS`、`JavaScript`の基礎が必要です。関連する基礎は`MDN`ウェブサイトで学ぶことができます。では、没入型翻訳の内部を見てみましょう。プラグインの動作メカニズムを簡単に言うと、ウェブページにサードパーティのスクリプトを注入し、そのスクリプトがウェブページの構造、スタイル、さらには動作をかなり自由に変更することです。

私たちの没入型翻訳プラグインも例外ではありません。没入型翻訳が何をしたのかを簡単に分析しましょう。

- 翻訳する必要のある要素の集合を取得する
- 要素の集合内のテキストを翻訳する
- 翻訳結果を要素の集合に挿入する

しかし、よく考えてみると、次の二つの問題が自然と浮かび上がります。

- 翻訳する必要のある要素をどのように決定するか。全てを翻訳すると、ユーザーの没入体験を損なうことが多いです。例えば、シンプルで明確なボタンやナビゲーションバーなどです。
- 翻訳結果を要素の集合に挿入することは、新たな挑戦をもたらします。挿入された結果がオリジナルのウェブページと一致し、オリジナルのウェブページのスタイルに影響を与えないようにする方法は？

私たちの`Rules`の核心は、上述の二つの問題を解決することです。プラグインとして、没入型翻訳は市場に出回っているすべてのウェブページに直面しており、それらは数十万、場合によっては数百万にも及びます。これらのウェブページのページ構造や使用されている技術も大きく異なります。ウェブページの違いから、すべてのウェブサイトコンテンツに適応する一般的なロジックを見つけることはほぼ不可能であり、一つ一つのウェブサイトに個別に適応する以外に解決策はなさそうです。そのため、より簡単に適応できるように、設定即コードの考え方を利用し、適応作業を設定フィールドの作業に変換しました。これにより、ユーザーも適応作業に参加できるようになります。

設定を行う際には、以下のフィールドを直接使用することは避け、`selector.add`、`excludeSelector.add`といったフィールドを使用して、継承の方法で元の設定項目に基づいて変更を加えることが最善です。

以下に、没入型翻訳によるサイトの適応作業を紹介します。

以下は Twitter の Rules です。簡潔にするため、いくつかの重要なフィールドに焦点を当て、残りのフィールドは上述の`Rules`と組み合わせて理解できます。

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
      // 翻訳対象の要素を指定、セレクタに一致する要素のみが翻訳されます
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
      // CSS セレクタによって選択された翻訳されない要素
      "[aria-describedby][role=button]",
      "header",
      "[data-testid='radioGroupplayback_rate'] div",
      "[data-testid='userFollowIndicator']",
      "[class='css-901oao r-14j79pv r-37j5jr r-n6v787 r-16dba41 r-1cwl3u0 r-bcqeeo r-qvutc0']",
      "[class='css-175oi2r r-1wbh5a2 r-dnmrzs']"
    ],
    "globalStyles": {
      // グローバルスタイル、元のスタイルを強制的に上書き
      "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='tweetText']": "-webkit-line-clamp: unset;"
    }
  }
]
```

- `selector`: 翻訳する要素の集合を指定

  このフィールドが必要な理由

  - すべての要素にテキストが含まれているわけではなく、翻訳が必要なわけでもないため、このようなフィールドを提供することで、パフォーマンスを保証しつつ、ユーザーの没入型体験を保証できます

  例を挙げると

  - Twitter で`selector`を指定しない場合、ページ内のすべての英語テキストを翻訳しようとします。以下の画像のように、ユーザーのニックネームは翻訳する必要がないことが多いです。

  ![ユーザーホームページ](https://s.immersivetranslate.com/assets/siteDocs/twitterUser.png)

  フィールドの意味

  - ```
      "selectors": [ // 翻訳される CSS セレクタの集合
      "[data-testid=\"tweetText\"]",
    ]
    ```

  この配列の各項目は CSS セレクタで、ページ内で翻訳が必要な要素を選択します。ここでは、最初のセレクタを例に、以下の画像のように、すべてのツイート要素にヒットします。

  ![ツイート](https://s.immersivetranslate.com/assets/siteDocs/tweet.png)

- `excludeSelectors`: 翻訳されない要素の集合

  このフィールドが必要な理由

  - 翻訳するためのセレクタだけでは不十分で、マッチした要素が翻訳不要である可能性があるため、両者に重複する部分が存在するかもしれません。そのため、翻訳不要な要素を除外するためのフィールドを設定する必要があります。
  - ページの構造が非常に複雑であるため、このように 2 つの設定項目を提供することで、設定をより柔軟にします。
  - 関連する優先順位は、同じセレクターに対しては、selectors > excludeSelectors で、残りは CSS の優先順位によって比較されます。

  フィールドの意味

  - ```
      "excludeSelectors": [ // 翻訳されない CSS セレクタによって選択された要素
      "[aria-describedby][role=button]",
    ],
    ```

  最初の例で、フォローボタンの翻訳を除外しています。
  ![twitter-follow](https://s.immersivetranslate.com/assets/siteDocs/twitter-follow.png)

- `globalStyles`: グローバルスタイルを追加し、元のスタイルを強制的に上書き

  このフィールドが必要な理由

  - 元のウェブページの CSS スタイルのため、翻訳の表示効果が良くない場合があります。例えば、切り取られたり、改行されないなどの効果が発生することがあります。
  - このフィールドを通じて、原生のウェブページの CSS 属性を直接変更することで、問題を解決するための強力な解決策を提供します。

  フィールドの意味

  - ```
        "globalStyles": {
      // グローバルスタイル、元のスタイルを強制的に上書き
      "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='tweetText']": "-webkit-line-clamp: unset;"
    }
    ```

  `-webkit-line-clamp` この属性は表示行数を制御し、余分な行は切り取られます。`unset`に設定することで、この属性によって翻訳文が切り取られることがないようにします。

### カスタムウェブサイト適応

適応ルールについては、もちろんカスタムルールを設定することもできます。プラグインのオプションページに進み、[開発者設定](https://dash.immersivetranslate.com/#developer)をクリックして、`Edit User Rules` を展開し、ここで各ウェブサイトのカスタム適応を行います。以下は実際のルールを組み合わせて説明します。

```json
[
  {
    "selectors.remove": ["[data-testid=\"tweetText\"]"],
    "selectors.add": [""],
    "excludeSelectors.add": [""],
    "excludeSelectors.remove": [""],
    "id": "twitter"
  }
]
```

このルールは、Twitter ページのツイートを翻訳しないようにします。以下でフィールドの意味を詳しく説明します。

`id` は、沈没式翻訳が現在定義している関連サイトの集合で、各 `id` は関連するサイトに対応しています。`id` の利点は 2 つあります。

- `id` を使用すると、沈没式翻訳の以前の適応ルールを継承でき、その基盤の上で追加や削除を行うことができます。
- `id` を使用すると、煩雑なマッチングフィールドを書く必要がなくなります。

以下は、沈没式翻訳の内蔵サービスの一般的な `id` のいくつかを紹介します。

- `"isEbook"` epub リーダーページの設定
- `"isEbookBuilder"` epub バイリンガルブック生成ページの設定
- `"pdf"` PDF バイリンガル対照翻訳ページの設定

完全な `id` コレクションは、[開発者設定](https://dash.immersivetranslate.com/#developer)の `Click to expand the final config` で見つけることができます。

`selectors` は、翻訳が必要な CSS セレクタを指定するために使用されます。既存の基盤の上で追加や削除を行うために、子項目 `.add` `.remove` の使用を推奨します。

`excludeSelectors` は、翻訳が不要な CSS セレクタを除外するために使用されます。同様に、子項目 `.add` `.remove` を使用して、既存の基盤の上で追加や削除を行うことを推奨します。

**さらに詳しく**

ブロックとインラインの違いについて、もっと知りたい場合は[こちら](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements#inline)をご覧ください。

- ブロック要素は一行を占有し、隣接する複数のブロック要素はそれぞれ新しい行を開始します。
- インライン要素は一行を占有せず、隣接する複数のインライン要素は同一行に並び、一行に収まりきらなくなるまで新しい行には移りません。
