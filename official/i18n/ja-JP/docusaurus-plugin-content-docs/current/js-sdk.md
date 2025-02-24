---
sidebar_position: 5
---

# JS SDK

Immersive Translate JS SDK は、あなたのウェブサイトでバイリンガル翻訳を実現するのに役立ちます。

## 使用方法

> JS SDK をデバッグする前に、Immersive Translate 拡張機能をオフにしてください。

1. 初期化パラメータを設定します（immersiveTranslateConfig を設定しないと JS SDK の初期化に失敗します。空のオブジェクトを設定することができます）

```html
<script>
  window.immersiveTranslateConfig = {
    pageRule: {},
  };
</script>
```

2. 以下の `script` コードをあなたのウェブページの `</head>` の前に追加します

```html
<script
  async
  src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"
></script>
```

例

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

## パラメータ

- `pageRule`
  ウェブサイトをカスタマイズして、どのコンテンツを翻訳するか、またはウェブページのスタイルを調整するかを決定できます。
- `isAutoTranslate`
  自動翻訳を即座に実行

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

`selectors` を使用すると、スマート翻訳の範囲を上書きし、そのセレクターに一致する要素のみを翻訳します。

`excludeSelectors` を使用すると、要素を除外し、その位置を翻訳しません。

`selectors.add` を使用すると、デフォルトにいくつかのセレクターを追加します。

`selectors.remove` を使用すると、デフォルトからいくつかのセレクターを削除します。

特定の領域を翻訳する際に、要素を一つの全体として扱い、行ごとに分割しないようにする場合は、`atomicBlockSelectors` セレクターを使用できます。注意すべき点は、`atomicBlockSelectors` を使用する前に、`selectors` を使用して選択する必要があることです。

```json
{
  "selectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"],
  "atomicBlockSelectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"]
}
```

`pageRule` の詳細なパラメータ説明：

```typescript
export interface PageRule {
  excludeMatches?: string | string[]; // 特定のウェブサイトを除外します。
  selectorMatches?: string | string[]; // すべての URL を指定せずにセレクターで一致させます。
  excludeSelectorMatches?: string | string[]; // 除外ルール、上記と同様。


```markdown
  // 指定翻訳範囲
  selectors?: string | string[]; // 翻訳対象の要素を指定
  excludeSelectors?: string | string[]; // 除外要素、翻訳しない要素を指定
  excludeTags?: string | string[]; // 除外タグ、翻訳しないタグを指定

  // 翻訳範囲を追加、上書きしない
  additionalSelectors?: string | string[]; // 翻訳範囲を追加。スマート翻訳のエリアに追加翻訳位置を指定。
  additionalExcludeSelectors?: string | string[]; // 除外要素を追加し、特定の位置を翻訳しないようにする。
  additionalExcludeTags?: string | string[]; // 除外タグを追加

  // 原文を保持
  stayOriginalSelectors?: string | string[]; // 一致する要素は原文のまま保持。フォーラムサイトのタグによく使用される。
  stayOriginalTags?: string | string[]; // 一致するタグは原文のまま保持、例えば `code`

  // エリア翻訳
  atomicBlockSelectors?: string | string[]; // エリアセレクター、一致する要素は一つのまとまりとして扱い、分割翻訳しない
  atomicBlockTags?: string | string[]; // エリアタグセレクター、同上

  // Block または Inline
  extraBlockSelectors?: string | string[]; // 追加のセレクター、一致する要素は block 要素として扱い、一行を占有する。
  extraInlineSelectors?: string | string[]; // 追加のセレクター、一致する要素は inline 要素として扱う。

  inlineTags?: string | string[]; // 一致するタグは inline 要素として扱う
  preWhitespaceDetectedTags?: string | string[]; // 一致するタグは自動で改行される

  // 翻訳スタイル
  translationClasses?: string | string | string[]; // 翻訳文に追加のクラスを付与

  // グローバルスタイル
  globalStyles?: Record<string, string>; // ページスタイルを変更、翻訳文が原因でページが乱れる場合に有用。
  globalAttributes?: Record<string, Record<string, string>>; // ページ要素の属性を変更

  // 埋め込みスタイル
  injectedCss?: string | string[]; // CSSスタイルを埋め込む
  additionalInjectedCss?: string | string[]; // CSSスタイルを追加、直接上書きしない。

  // コンテキスト
  wrapperPrefix?: string; // 翻訳文エリアのプレフィックス、デフォルトは smart、文字数に応じて改行を決定。
  wrapperSuffix?: string; // 翻訳文エリアのサフィックス

  // 翻訳文の改行文字数
  blockMinTextCount?: number; // 翻訳文を block として扱う最小文字数、それ以外は inline 要素。
  blockMinWordCount?: number; // 同上。常に改行させたい場合は、両方に 0 を設定。

  // コンテンツ翻訳可能な最小文字数
  containerMinTextCount?: number; // スマート認識時、要素が含む最小文字数、デフォルトは 18
  paragraphMinTextCount?: number; // 原文段落の最小文字数、これ以上の内容が翻訳される
  paragraphMinWordCount?: number; // 原文段落の最小単語数

  // 長い段落の強制改行文字数
  lineBreakMaxTextCount?: number; // 長い段落の翻訳を有効にした場合、強制的に分行する段落の最大文字数。
```

```markdown
  // 翻訳の開始タイミング
  urlChangeDelay?: number; // ページに入った後、翻訳を開始するまでの遅延時間（ミリ秒）。ウェブページの初期化を待つため、現在はデフォルトで250ms

  // AI streaming 翻訳
  aiRule: {
    streamingSelector: string; // gpt ウェブページで翻訳中の要素を示すセレクタ
    messageWrapperSelector: string; // メッセージ本文のセレクタ
    streamingChange: boolean; // gpt ウェブページの繰り返しメッセージがインクリメンタル更新かフル更新か。gpt はインクリメンタル
  };
}
```