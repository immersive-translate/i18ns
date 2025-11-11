---
sidebar_position: 5
---
# AI Prompt 設定ガイド

## 概要

Immersive Translate は、カスタム AI 翻訳の Prompt 設定をサポートしており、上級ユーザーが自分のニーズに応じて翻訳動作を調整できます。このドキュメントでは、設定方法、サポートされている変数、高度な使用方法について詳しく説明します。

## サポートされている変数

### 基本変数

- `{{text}}` - 翻訳するテキストコンテンツ
- `{{from}}` - ソース言語
- `{{to}}` - ターゲット言語
- `{{content_type}}` - 元のテキストのタイプ（`html` または `text`）

### コンテキスト変数
- `{{title_prompt}}` - ウェブページのタイトル（利用可能な場合）
- `{{summary_prompt}}` - ウェブページのコンテキスト要約（利用可能な場合）
- `{{terms_prompt}}` - 関連する専門用語（利用可能な場合）

## 設定方法

### 1. System Prompt(`systemPrompt`)
システムとして AI に送信される翻訳リクエスト。AI の役割と基本ルールを設定するために使用されます。

### 2. Prompt(`prompt`)
ユーザーとして AI に送信される会話で、実際に翻訳する必要があるコンテンツを含みます。

### 3. System Multiple Prompt(`systemMultiplePrompt`)
段落数が 1 より大きい場合、システムとして AI に送信される翻訳リクエスト。複数段落の翻訳シナリオを処理するために使用されます。

### 4. Multiple Prompt(`multiplePrompt`)
複数段落の翻訳時に、ユーザーとして送信されるリクエスト。区切り文字または YAML 形式の使用をサポートします。

### 5. Subtitle Prompt(`subtitlePrompt`)

字幕を翻訳する必要がある場合、ユーザーとして AI に送信される会話で、実際に翻訳する必要があるコンテンツを含みます。

## デフォルト設定例

1 つの段落のみが収集された場合、デフォルトで単一段落の Prompt が使用されます。複数の段落が収集された場合、デフォルトで複数段落の Prompt が使用されます。ほとんどの場合、複数段落になります。複数段落のデフォルト区切り文字は `%%` です。大規模モデルの幻覚を減らすために、この一般的でない区切り文字を意図的に使用しています。この Prompt をベースとして、必要な Prompt に変更できます。以下はデフォルトの Prompt 設定です：

### 単一段落の翻訳

```yaml
systemPrompt: |
    あなたは、テキストを {{to}} に流暢に翻訳する必要がある、プロフェッショナルな {{to}} のネイティブ翻訳者です。

    ## 翻訳ルール
    1. 翻訳されたコンテンツのみを出力し、説明や追加のコンテンツ（「翻訳は以下の通り：」や「翻訳：」など）を含めないでください
    2. 返される翻訳は、元のテキストと完全に同じ段落数とフォーマットを維持する必要があります
    3. テキストにHTMLタグが含まれている場合、流暢性を保ちながら、翻訳内でタグを配置する場所を考慮してください
    4. 翻訳すべきでないコンテンツ（固有名詞、コードなど）については、元のテキストを保持してください
    5. 翻訳を直接出力してください（区切り文字なし、追加テキストなし）{{title_prompt}}{{summary_prompt}}{{terms_prompt}}
prompt: |
  {{to}} に翻訳してください（翻訳のみ出力）：

  {{text}}
```

### 複数段落の翻訳

```yaml
multipleSystemPrompt: |
    あなたは、テキストを {{to}} に流暢に翻訳する必要がある、プロフェッショナルな {{to}} のネイティブ翻訳者です。

    ## 翻訳ルール
    1. 翻訳されたコンテンツのみを出力し、説明や追加のコンテンツ（「翻訳は以下の通り：」や「翻訳：」など）を含めないでください
    2. 返される翻訳は、元のテキストと完全に同じ段落数とフォーマットを維持する必要があります
    3. テキストにHTMLタグが含まれている場合、流暢性を保ちながら、翻訳内でタグを配置する場所を考慮してください
    4. 翻訳すべきでないコンテンツ（固有名詞、コードなど）については、元のテキストを保持してください{{title_prompt}}{{summary_prompt}}{{terms_prompt}}

    ## 入力出力フォーマット例

    ### 入力例：
    Paragraph A

    %%

    Paragraph B

    %%

    Paragraph C

    %%

    Paragraph D

    ### 出力例：
    Translation A

    %%

    Translation B

    %%

    Translation C

    %%

    Translation D

multiplePrompt: |
  {{to}} に翻訳してください：

  {{text}}
subtitlePrompt: |
  {{to}} に翻訳してください：

  {{text}}
```

## 高度な使用方法（YAML 形式）

より正確な制御が必要なシナリオ（例：複数ステップの出力）では、YAML 形式で設定できます：

### 高度な変数

- `{{yaml}}` - YAML 形式の入力データ

デフォルトの 'yaml' 変数は次のようになります：

```
- id: 1
  text: Hello world
- id: 2
  text: How are you?
```

大規模モデルの期待される出力は次のとおりです：

```
- id: 1
  text: 你好世界
- id: 2
  text: 你好吗？
```

デフォルトの `{{yaml}}` を使用する場合、prompt でこの期待を明確に表現する必要があります。デフォルトと応答の `yaml` 形式を変更したい場合、これは Immersive Translate 設定ページの UI では解決できません。Immersive Translate の JSON 形式のユーザー設定を直接編集する必要があります。

ユーザー設定の編集パス： `設定ページ`->`開発者設定`->`Edit Full User Config`（編集前に、ユーザー設定をバックアップしてください）

ユーザー設定の JSON で翻訳サービスの設定を見つけることができます（ない場合は、この構造に従って追加するだけです）：

```
{
  ...
  "translationServices": {
    "openai": {
       ...
      }
  },
  ...

```

`yaml` 変数は `env.imt_yaml_item` で構成されているため、`imt_yaml_item` の形式を次のように変更できます：

```json
  "translationServices": {
    "openai": {
       "env": {
          "imt_yaml_item": "- id: {{id}}\n  source: {{text}}"
        }
    }
   }
```

もう 1 つの特殊変数は `imt_subtitle_yaml_item` で、`imt_yaml_item` と同様に、字幕を翻訳するための YAML アイテムに使用されます。

他の `env` 変数については、任意の `env` 変数を追加し、prompt で `{{変数名}}` の形式で直接使用できます。たとえば、次のデフォルトの `env` 変数：

- `{{imt_source_field}}` - ソーステキストフィールド名（デフォルト：text）
- `{{imt_trans_field}}` - 翻訳テキストフィールド名（デフォルト：text）
- `{{imt_sub_source_field}}` - 字幕ソーステキストフィールド名
- `{{imt_sub_trans_field}}` - 字幕翻訳テキストフィールド名

`title_prompt`、`summary_prompt`、`terms_prompt` も `env` を通じて設定されており、デフォルトは次のとおりです：

```
        "title_prompt": "\n\n## コンテキスト認識\nドキュメントメタデータ：\nタイトル：《{{imt_title}}》",
        "summary_prompt": "\n\n## コンテキスト認識\nドキュメントメタデータ：\n要約：{{imt_theme}}...",
        "terms_prompt": "\n\n必須用語：翻訳中に以下の用語を使用する必要があります。'source':'target' で source == target の場合、ソース用語を変更せずに保持してください。\n\n 用語 -> \n\n {{imt_terms}}",
        "sub_summary_prompt": "\n\n## コンテキスト認識\nドキュメントメタデータ：\nタイプ：字幕\n要約：{{imt_theme}}...",
        "sub_terms_prompt": "\n\n必須用語：翻訳中に以下の用語を使用する必要があります。'source':'target' で source == target の場合、ソース用語を変更せずに保持してください。\n\n 用語 -> \n\n {{imt_terms}}"

```

`imt_title`、`imt_theme`、`imt_terms` は特殊変数で、システムによって注入されます。`imt_title` はタイトル、`imt_theme` はウェブページ全体の要約、`imt_terms` はモデルによって抽出されたキー用語です。

> 注意： `imt_theme`、`imt_terms` は専有サービスによって抽出され、現在は [Pro 会員](https://immersivetranslate.com/pricing/) のみが利用できます。

### YAML Prompt 例

```yaml
systemPrompt: |
  あなたは、プロフェッショナルで信頼性の高い機械翻訳エンジンです。
  {{title_prompt}}{{summary_prompt}}{{terms_prompt}}

multiplePrompt: |
    "id" と "{{imt_source_field}}" フィールドを含むエントリを含むYAML形式の入力を受け取ります。入力は次のとおりです：

    <yaml>
    {{yaml}}
    </yaml>

    YAML内の各エントリについて、"{{imt_source_field}}" フィールドのコンテンツを {{to}} に翻訳し、{{html_only}} 翻訳結果をそのエントリの "{{imt_source_field}}" フィールドに書き戻します。

    期待される形式の例は次のとおりです：

    {{normal_result_yaml_example}}

    <yaml> タグや追加情報を含めずに、翻訳されたYAMLを直接返してください。
subtitlePrompt: |
    "id" と "{{imt_sub_source_field}}" フィールドを含むエントリを含むYAML形式の字幕入力を受け取ります。入力は次のとおりです：

    <yaml>
    {{yaml}}
    </yaml>

    YAML内の各エントリについて、"{{imt_sub_source_field}}" フィールドのコンテンツを {{to}} に翻訳し、{{html_only}} 翻訳結果をそのエントリの "{{imt_sub_source_field}}" フィールドに書き戻します。

    期待される形式の例は次のとおりです：

    {{subtitle_result_yaml_example}}

    <yaml> タグや追加情報を含めずに、翻訳されたYAMLを直接返してください。

```

`html_only` は特殊変数で、翻訳される元のテキストが HTML 形式の場合にのみ存在し、値は次のとおりです： `\n\n注意：テキストにHTMLタグが含まれている場合、翻訳後にタグを翻訳結果内のどこに配置するかを考慮し、同時に結果の流暢性を保ってください。`、ユーザーが AI 翻訳サービスで「リッチテキスト翻訳」を有効に設定した場合にのみ、この変数が存在します。それ以外の場合は空です。

`normal_result_yaml_example` は `env` で設定され、デフォルトは次のとおりです：

```
<example>
Input:
  - id: 1
    {{imt_source_field}}: Source
Output:
  - id: 1
    {{imt_trans_field}}: Translation
</example>
```

`subtitle_result_yaml_example` は `env` で設定され、デフォルト値は次のとおりです：

```
<example>
Input:
  - id: 1
    {{imt_sub_source_field}}: ...
  - id: 2
    {{imt_sub_source_field}}: ...
  - id: 3
    {{imt_sub_source_field}}: ...
Output:
  - id: 1
    {{imt_sub_source_field}}: ...
  - id: 2
    {{imt_sub_source_field}}: ...
  - id: 3
    {{imt_sub_source_field}}: ...
</example>

```

`env` で上書きできます。

## 高度な例：リフレクティブ翻訳

この例では、YAML 形式を使用して、初期翻訳と最適化翻訳の 2 つのステップを含む、より複雑な翻訳フローを実装する方法を示します：

```yaml
env:
  imt_source_field: source
  imt_trans_field: step2  # 最終翻訳は step2 フィールドを使用
  imt_sub_source_field: source
  imt_sub_trans_field: step2
  imt_yaml_item: |-
    - id: {{id}}
      {{imt_source_field}}: {{text}}
  imt_subtitle_yaml_item: |-
    - id: {{id}}
      {{imt_sub_source_field}}: {{text}}

systemPrompt: |
  あなたは、プロフェッショナルで信頼性の高い機械翻訳エンジンです。
  {{title_prompt}}{{summary_prompt}}{{terms_prompt}}

multiplePrompt: |
  以下はYAML入力です：
  <yaml>
  {{yaml}}
  </yaml>
  
  次の手順に従ってください：
  1. 提供されたYAMLオブジェクトから "source" フィールドのコンテンツを抽出します。
  2. 抽出したコンテンツを {{to}} に翻訳します。この初期翻訳を step1 フィールドに配置します。
  3. step1 の初期翻訳を最適化し、{{to}} でより自然で理解しやすくします。 
     最適化された翻訳を step2 フィールドに配置します。
  4. 結果を、次の例に示すように、id、step1、step2 フィールドを含むYAML配列としてフォーマットします：
  
  - id: 1 
    step1: 初期翻訳
    step2: 最適化翻訳
  
  <example_output> タグや追加情報を含めずに、翻訳されたYAMLを直接返してください。
```

### ワークフローの説明

1. **入力形式**：
   ```yaml
   - id: 1
     source: "Hello world"
   - id: 2
     source: "How are you?"
   ```

2. **AI 処理ステップ**：
   - Step 1: 初期翻訳を実行
   - Step 2: 翻訳を最適化し、より自然で流暢にします

3. **出力形式**：
   ```yaml
   - id: 1
     step1: "你好世界"
     step2: "你好，世界"
   - id: 2
     step1: "你怎么样？"
     step2: "你好吗？"
   ```
