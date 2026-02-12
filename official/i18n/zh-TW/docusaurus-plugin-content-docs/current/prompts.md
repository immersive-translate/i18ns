---
sidebar_position: 5
---
# AI Prompt 設定指南

## 概述

沉浸式翻譯支援自定義 AI 翻譯的 Prompt 設定，讓進階使用者可以根據自己的需求調整翻譯行為。本文件將詳細介紹設定方式、支援的變數以及進階用法。

## 支援的變數

### 基礎變數

- `{{text}}` - 需要翻譯的文字內容
- `{{from}}` - 來源語言
- `{{to}}` - 目標語言
- `{{content_type}}` - 原文字的類型（`html` 或 `text`）

### 上下文變數
- `{{title_prompt}}` - 網頁標題（當可用時）
- `{{summary_prompt}}` - 網頁上下文摘要（當可用時）
- `{{terms_prompt}}` - 相關專業術語（當可用時）

## 設定方式

### 1. System Prompt(`systemPrompt`)
以系統身份發送給 AI 的翻譯請求。用於設定 AI 的角色和基本規則。

### 2. Prompt(`prompt`)
以使用者身份發送給 AI 的對話，包含實際需要翻譯的內容。

### 3. System Multiple Prompt(`systemMultiplePrompt`)
當段落數大於 1 時，以系統身份發送給 AI 的翻譯請求。用於處理多段落翻譯場景。

### 4. Multiple Prompt(`multiplePrompt`)
多段落翻譯時，以使用者身份發送的請求。支援使用分隔符或 YAML 格式。

### 5. Subtitle Prompt(`subtitlePrompt`)

當需要翻譯字幕時，以使用者身份發送給 AI 的對話，包含實際需要翻譯的內容。

## 預設設定範例

如果只收集到一個段落，那麼預設會走單段落的 Prompt，如果收集到多個段落，那麼預設會走多段落的 Prompt，大多數情況會是多段落。多段落的預設分隔符是 `%%`，我們故意使用這個不太常見的分隔符來減少大模型的幻覺。你可以用此 Prompt 為基礎去修改為你需要的 Prompt，以下是預設的 Prompt 設定：

### 單段落翻譯

```yaml
systemPrompt: |
    你是一位專業的 {{to}} 母語翻譯者，需要流暢地將文字翻譯成 {{to}}。

    ## 翻譯規則
    1. 僅輸出翻譯內容，不要包含解釋或其他額外內容（例如「翻譯如下：」或「以下是翻譯：」等）
    2. 返回的翻譯必須保持與原文完全相同的段落數和格式
    3. 如果文字包含 HTML 標籤，在保持流暢性的同時，請考慮標籤在翻譯中的位置
    4. 對於不應翻譯的內容（如專有名詞、程式碼等），請保留原文
    5. 直接輸出翻譯（無分隔符，無額外文字）{{title_prompt}}{{summary_prompt}}{{terms_prompt}}
prompt: |
  翻譯成 {{to}}（僅輸出翻譯）：
  
  {{text}}
```

### 多段落翻譯

```yaml
multipleSystemPrompt: |
    你是一位專業的 {{to}} 母語翻譯者，需要流暢地將文字翻譯成 {{to}}。

    ## 翻譯規則
    1. 僅輸出翻譯內容，不要包含解釋或其他額外內容（例如「翻譯如下：」或「以下是翻譯：」等）
    2. 返回的翻譯必須保持與原文完全相同的段落數和格式
    3. 如果文字包含 HTML 標籤，在保持流暢性的同時，請考慮標籤在翻譯中的位置
    4. 對於不應翻譯的內容（如專有名詞、程式碼等），請保留原文{{title_prompt}}{{summary_prompt}}{{terms_prompt}}

    ## 輸入輸出格式範例

    ### Input Example:
    Paragraph A

    %%

    Paragraph B

    %%

    Paragraph C

    %%

    Paragraph D

    ### Output Example:
    Translation A

    %%

    Translation B

    %%

    Translation C

    %%

    Translation D

multiplePrompt: |
  翻譯成 {{to}}：
  
  {{text}}
subtitlePrompt: |
  翻譯成 {{to}}：
  
  {{text}}
```

## 進階用法（YAML 格式）

對於需要更精確控制的場景（比如多步驟輸出），可以使用 YAML 格式進行設定：

### 進階變數

- `{{yaml}}` - YAML 格式的輸入資料

預設的 'yaml' 變數大概長這樣：

```
- id: 1
  text: Hello world
- id: 2
  text: How are you?
```

我們預設期待大模型的輸出是這樣的：

```
- id: 1
  text: 你好世界
- id: 2
  text: 你好嗎？
```

如果你使用預設的 `{{yaml}}`，那麼你需要在 prompt 中把這個期望表達清楚。如果你希望修改預設和響應的 `yaml` 格式，這無法透過沉浸式翻譯設定頁面中的 UI 來解決，你必須直接編輯沉浸式翻譯 JSON 格式的使用者設定。

使用者設定編輯路徑：`設定頁`->`開發者設定`->`Edit Full User Config`（編輯前，請備份你的使用者設定）

你可以在使用者設定的 JSON 中找到翻譯服務的設定（如果沒有，直接按照這個結構新增即可）：

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

`yaml` 變數由 `env.imt_yaml_item` 組成，所以你可以修改 `imt_yaml_item` 的格式，像下面這樣：

```json
  "translationServices": {
    "openai": {
       "env": {
          "imt_yaml_item": "- id: {{id}}\n  source: {{text}}"
        }
    }
   }
```

另一個特殊變數是 `imt_subtitle_yaml_item`，和 `imt_yaml_item` 類似，用於翻譯字幕的 YAML item。

其他的 `env` 變數，你可以新增任何 `env` 變數，直接在 prompt 中按照 `{{變數名}}` 的格式使用，比如如下預設的 `env` 變數：

- `{{imt_source_field}}` - 原文欄位名（預設：text）
- `{{imt_trans_field}}` - 譯文欄位名（預設：text）
- `{{imt_sub_source_field}}` - 字幕原文欄位名
- `{{imt_sub_trans_field}}` - 字幕譯文欄位名

包括 `title_prompt`、`summary_prompt`、`terms_prompt` 背後也是透過 `env` 來設定的，預設如下：

```
        "title_prompt": "\n\n## 上下文感知\n文件元資料：\n標題：《{{imt_title}}》",
        "summary_prompt": "\n\n## 上下文感知\n文件元資料：\n摘要：{{imt_theme}}...",
        "terms_prompt": "\n\n必需術語：翻譯時必須使用以下術語，如果 'source':'target' 中 source == target，則保持源術語不變。\n\n 術語 -> \n\n {{imt_terms}}",
        "sub_summary_prompt": "\n\n## 上下文感知\n文件元資料：\n類型：字幕\n摘要：{{imt_theme}}...",
        "sub_terms_prompt": "\n\n必需術語：翻譯時必須使用以下術語，如果 'source':'target' 中 source == target，則保持源術語不變。\n\n 術語 -> \n\n {{imt_terms}}"

```

其中 `imt_title`、`imt_theme`、`imt_terms` 為特殊變數，由系統注入，`imt_title` 為標題，`imt_theme` 為整個網頁的總結，`imt_terms` 為模型提取的關鍵術語。

> 注意：`imt_theme`、`imt_terms` 是專有服務提取的，目前僅為 [Pro 會員](https://immersivetranslate.com/pricing/) 提供。

### YAML Prompt 範例

```yaml
systemPrompt: |
  你是一個專業、可靠的機器翻譯引擎。
  {{title_prompt}}{{summary_prompt}}{{terms_prompt}}

multiplePrompt: |
    你將收到一個 YAML 格式的輸入，包含帶有 "id" 和 "{{imt_source_field}}" 欄位的條目。輸入內容如下：

    <yaml>
    {{yaml}}
    </yaml>

    對於 YAML 中的每個條目，將 "{{imt_source_field}}" 欄位的內容翻譯成 {{to}}，{{html_only}} 將翻譯結果寫回該條目的 "{{imt_source_field}}" 欄位。

    以下是期望格式的範例：

    {{normal_result_yaml_example}}

    請直接返回翻譯後的 YAML，不要包含 <yaml> 標籤或任何額外資訊。
subtitlePrompt: |
    你將收到一個 YAML 格式的字幕輸入，包含帶有 "id" 和 "{{imt_sub_source_field}}" 欄位的條目。輸入內容如下：

    <yaml>
    {{yaml}}
    </yaml>

    對於 YAML 中的每個條目，將 "{{imt_sub_source_field}}" 欄位的內容翻譯成 {{to}}，{{html_only}} 將翻譯結果寫回該條目的 "{{imt_sub_source_field}}" 欄位。

    以下是期望格式的範例：

    {{subtitle_result_yaml_example}}

    請直接返回翻譯後的 YAML，不要包含 <yaml> 標籤或任何額外資訊。

```

其中 `html_only` 為特殊變數，僅翻譯的原文為 HTML 格式時才有，值為：`\n\n注意：如果文字包含 HTML 標籤，請在翻譯後考慮標籤在翻譯結果中的位置，同時保持結果的流暢性。`，當使用者主動在 AI 翻譯服務中設定開啟「富文字翻譯」時才會有這個變數存在。否則為空。

`normal_result_yaml_example` 在 `env` 中設定，預設為：

```
<example>
Input:
  - id: 1
    {{imt_source_field}}: 原文
Output:
  - id: 1
    {{imt_trans_field}}: 譯文
</example>
```

`subtitle_result_yaml_example` 在 `env` 中設定，預設值為：

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

你可以在 `env` 中覆蓋它。

## 進階範例：反思式翻譯

這個範例展示了如何使用 YAML 格式實現更複雜的翻譯流程，包含初步翻譯和最佳化翻譯兩個步驟：

```yaml
env:
  imt_source_field: source
  imt_trans_field: step2  # 最終譯文使用 step2 欄位
  imt_sub_source_field: source
  imt_sub_trans_field: step2
  imt_yaml_item: |-
    - id: {{id}}
      {{imt_source_field}}: {{text}}
  imt_subtitle_yaml_item: |-
    - id: {{id}}
      {{imt_sub_source_field}}: {{text}}

systemPrompt: |
  你是一個專業、可靠的機器翻譯引擎。
  {{title_prompt}}{{summary_prompt}}{{terms_prompt}}

multiplePrompt: |
  以下是 YAML 輸入：
  <yaml>
  {{yaml}}
  </yaml>
  
  請按照以下步驟操作：
  1. 從提供的 YAML 物件中提取 "source" 欄位的內容。
  2. 將提取的內容翻譯成 {{to}}。將初步翻譯結果放入 step1 欄位。
  3. 最佳化 step1 中的初步翻譯，使其在 {{to}} 中更加自然和易於理解。 
     將最佳化後的翻譯放入 step2 欄位。
  4. 將結果格式化為包含 id、step1 和 step2 欄位的 YAML 陣列，如下例所示：
  
  - id: 1 
    step1: 初步翻譯
    step2: 最佳化翻譯
  
  請直接返回翻譯後的 YAML，不要包含任何 <example_output> 標籤或額外資訊。
```

### 工作流程說明

1. **輸入格式**：
   ```yaml
   - id: 1
     source: "Hello world"
   - id: 2
     source: "How are you?"
   ```

2. **AI 處理步驟**：
   - Step 1: 進行初步翻譯
   - Step 2: 最佳化翻譯，使其更自然流暢

3. **輸出格式**：
   ```yaml
   - id: 1
     step1: "你好世界"
     step2: "你好，世界"
   - id: 2
     step1: "你怎麼樣？"
     step2: "你好嗎？"
   ```
