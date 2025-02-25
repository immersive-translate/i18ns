---
sidebar_position: 5
---

# JS SDK

Immersive Translate JS SDK は、ウェブサイトでバイリンガル翻訳を実装するのに役立ちます。

## 使用方法

1. Immersive Translate を初期化します：

```js
<script>
  window.immersiveTranslateConfig = {
    pageRule: {}
  }
</script>
```

2. 次の`script`コードをウェブページに追加します

```html
<script src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"></script>
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
    <div>
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

`pageRule`を使用すると、ウェブサイトの設定をカスタマイズし、どのコンテンツを翻訳するか、またはウェブページのスタイルを調整するかを決定できます。

```js
initImmersiveTranslate({
  pageRule: {
    selectors: [".text"],
    excludeSelectors: ["nav", "footer"],
  },
});
```

`selectors`を使用すると、スマート翻訳範囲を上書きし、セレクタに一致する要素のみを翻訳します。

`excludeSelectors`を使用すると、翻訳から要素を除外できます。

`selectors.add`を使用すると、デフォルトのセレクタにいくつかのセレクタを追加できます。

`selectors.remove`を使用すると、デフォルトのセレクタからいくつかのセレクタを削除できます。

特定のエリアを翻訳し、要素を行に分割せずに全体として考慮したい場合は、`atomicBlockSelectors`セレクタを使用できます。`atomicBlockSelectors`を使用する前に、`selectors`を使用して要素を選択する必要があります。

```json
{
  "selectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"],
  "atomicBlockSelectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"]
}
```

`pageRule`の詳細なパラメータ説明：

```typescript
export interface PageRule {
  excludeMatches?: string | string[]; // 特定のウェブサイトを除外します。
  selectorMatches?: string | string[]; // すべての URL を指定せずにセレクタを使用して一致させます。
  excludeSelectorMatches?: string | string[]; // 除外ルール、上記と同様。

  // 翻訳範囲を指定
  selectors?: string | string[]; // 一致する要素のみを翻訳
  excludeSelectors?: string | string[]; // 要素を除外し、一致する要素を翻訳しない
  excludeTags?: string | string[]; // タグを除外し、一致するタグを翻訳しない

  // 翻訳範囲を追加、上書きしない
  additionalSelectors?: string | string[]; // 翻訳範囲を追加。スマート翻訳エリアに翻訳位置を追加。
  additionalExcludeSelectors?: string | string[]; // 除外要素を追加し、特定の位置でスマート翻訳を防止。
  additionalExcludeTags?: string | string[]; // 除外タグを追加

  // オリジナルを保持
  stayOriginalSelectors?: string | string[]; // 一致する要素はオリジナルのままになります。フォーラムウェブサイトのタグによく使用されます。
  stayOriginalTags?: string | string[]; // 一致するタグはオリジナルのままになります。例えば `code`

  // リージョン翻訳
  atomicBlockSelectors?: string | string[]; // リージョンセレクタ、一致する要素は全体として考慮され、セグメントに分割されません
  atomicBlockTags?: string | string[]; // リージョンタグセレクタ、上記と同様

  // ブロックまたはインライン
  extraBlockSelectors?: string | string[]; // 追加セレクタ、一致する要素はブロック要素として扱われ、1 行を占有します。
  extraInlineSelectors?: string | string[]; // 追加セレクタ、一致する要素はインライン要素として扱われます。

  inlineTags?: string | string[]; // 一致するタグはインライン要素として扱われます
  preWhitespaceDetectedTags?: string | string[]; // 一致するタグは自動的に行を折り返します

  // 翻訳スタイル
  translationClasses?: string | string | string[]; // 翻訳に追加のクラスを追加

  // グローバルスタイル
  globalStyles?: Record<string, string>; // ページスタイルを変更し、翻訳がページの乱れを引き起こす場合に便利です。
  globalAttributes?: Record<string, Record<string, string>>; // ページ要素の属性を変更

  // 埋め込みスタイル
  injectedCss?: string | string[]; // CSS スタイルを埋め込む
  additionalInjectedCss?: string | string[]; // 直接上書きせずに CSS スタイルを追加。

  // コンテキスト
  wrapperPrefix?: string; // 翻訳エリアのプレフィックス、デフォルトはスマートで、文字数に基づいて行を折り返すかどうかを決定します。
  wrapperSuffix?: string; // 翻訳エリアのサフィックス

  // 翻訳ラッピング文字数
  blockMinTextCount?: number; // ブロックとして翻訳するための最小文字数、それ以外の場合、翻訳はインライン要素になります。
  blockMinWordCount?: number; // 上記と同様。常に行を折り返すには、両方を 0 に設定します。

  // 翻訳可能なコンテンツの最小文字数
  containerMinTextCount?: number; // スマート認識中に翻訳される要素の最小文字数、デフォルトは 18
  paragraphMinTextCount?: number; // オリジナル段落の最小文字数、数値を超えるコンテンツは翻訳されます
  paragraphMinWordCount?: number; // オリジナル段落の最小単語数

  // 長い段落の強制改行文字数
  lineBreakMaxTextCount?: number; // 長い段落を翻訳する際の強制改行の最大文字数。

  // 翻訳を開始するタイミング
  urlChangeDelay?: number; // ページに入った後、翻訳を開始するまでの遅延時間（ミリ秒）。デフォルトは 250ms で、ウェブページの初期化を待ちます。

  // AI ストリーミング翻訳
  aiRule: {
    streamingSelector: string; // GPT ウェブページセレクタ、翻訳中の要素をマーク
    messageWrapperSelector: string; // メッセージボディセレクタ
    streamingChange: boolean; // GPT のようなウェブページでの繰り返しメッセージのインクリメンタルまたはフルアップデート。GPT はインクリメンタル
  };
}
```
