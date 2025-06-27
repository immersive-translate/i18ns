---
sidebar_position: 5
---
# AI Prompt 配置指南

## 概述

沉浸式翻译支持自定义 AI 翻译的 Prompt 配置，让高级用户可以根据自己的需求调整翻译行为。本文档将详细介绍配置方式、支持的变量以及高级用法。

## 支持的变量

### 基础变量


- `{{text}}` - 需要翻译的文本内容
- `{{from}}` - 源语言
- `{{to}}` - 目标语言
- `{{content_type}}` - 原文本的类型（`html` 或 `text`）

### 上下文变量
- `{{title_prompt}}` - 网页标题（当可用时）
- `{{summary_prompt}}` - 网页上下文摘要（当可用时）
- `{{terms_prompt}}` - 相关专业术语（当可用时）


## 配置方式

### 1. System Prompt(`systemPrompt`)
以系统身份发送给 AI 的翻译请求。用于设定 AI 的角色和基本规则。

### 2. Prompt(`prompt`)
以用户身份发送给 AI 的对话，包含实际需要翻译的内容。

### 3. System Multiple Prompt(`systemMultiplePrompt`)
当段落数大于 1 时，以系统身份发送给 AI 的翻译请求。用于处理多段落翻译场景。

### 4. Multiple Prompt(`multiplePrompt`)
多段落翻译时，以用户身份发送的请求。支持使用分隔符或 YAML 格式。

### 5. Subtitle Prompt(`subtitlePrompt`)

当需要翻译字幕时，以用户身份发送给 AI 的对话，包含实际需要翻译的内容。

## 默认配置示例

如果只收集到一个段落，那么默认会走单段落的 Prompt, 如果收集到多个段落，那么默认会走多段落的 Prompt，大多数情况会是多段落。多段落的默认分隔符是 `%%`，我们故意使用这个不太常见的分隔符来减少大模型的幻觉。你可以用此 Prompt 为基础去修改为你需要的 Prompt, 以下是默认的 Prompt 配置：

### 单段落翻译

```yaml
systemPrompt: |
    You are a professional {{to}} native translator who needs to fluently translate text into {{to}}.

    ## Translation Rules
    1. Output only the translated content, without explanations or additional content (such as "Here's the translation:" or "Translation as follows:")
    2. The returned translation must maintain exactly the same number of paragraphs and format as the original text
    3. If the text contains HTML tags, consider where the tags should be placed in the translation while maintaining fluency
    4. For content that should not be translated (such as proper nouns, code, etc.), keep the original text.
    5. Output translation directly (no separators, no extra text){{title_prompt}}{{summary_prompt}}{{terms_prompt}}
prompt: |
  Translate to {{to}} (output translation only):
  
  {{text}}
```

### 多段落翻译

```yaml
multipleSystemPrompt: |
    You are a professional {{to}} native translator who needs to fluently translate text into {{to}}.

    ## Translation Rules
    1. Output only the translated content, without explanations or additional content (such as "Here's the translation:" or "Translation as follows:")
    2. The returned translation must maintain exactly the same number of paragraphs and format as the original text
    3. If the text contains HTML tags, consider where the tags should be placed in the translation while maintaining fluency
    4. For content that should not be translated (such as proper nouns, code, etc.), keep the original text{{title_prompt}}{{summary_prompt}}{{terms_prompt}}

    ## Input-Output Format Examples

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
  Translate to {{to}}:
  
  {{text}}
subtitlePrompt: |
  Translate to {{to}}:
  
  {{text}}
```




## 高级用法（YAML 格式）

对于需要更精确控制的场景（比如多步骤输出），可以使用 YAML 格式进行配置：

### 高级变量

- `{{yaml}}` - YAML 格式的输入数据


默认的 'yaml' 变量大概长这样；

```
- id: 1
  text: Hello world
- id: 2
  text: How are you?
```

我们默认期待大模型的输出是这样的：

```
- id: 1
  text: 你好世界
- id: 2
  text: 你好吗？
```

如果你使用默认的 `{{yaml}}`，那么你需要在 prompt 中把这个期望表达清楚。如果你希望修改默认和响应的 `yaml` 格式，这无法通过沉浸式翻译设置页面中的 UI 来解决，你必须直接编辑沉浸式翻译 JSON 格式的用户配置。

用户配置编辑路径： `设置页`->`开发者设置`->`Edit Full User Config` (编辑前，请备份你的用户配置)

你可以在用户配置的 JSON 中找到翻译服务的配置（如果没有，直接按照这个结构添加即可）：

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

`yaml` 变量由 `env.imt_yaml_item` 组成，所以你可以修改 `imt_yaml_item` 的格式，像下面这样：

```json
  "translationServices": {
    "openai": {
       "env": {
          "imt_yaml_item": "- id: {{id}}\n  source: {{text}}"
        }
    }
   }
```

另一个特殊变量是 `imt_subtitle_yaml_item`, 和 `imt_yaml_item` 类似，用于翻译字幕的 YAML item.



其他的 `env` 变量，你可以添加任何 `env`变量，直接在 prompt 中按照 `{{变量名}}` 的格式使用，比如如下默认的`env`变量：

- `{{imt_source_field}}` - 原文字段名（默认：text）
- `{{imt_trans_field}}` - 译文字段名（默认：text）
- `{{imt_sub_source_field}}` - 字幕原文字段名
- `{{imt_sub_trans_field}}` - 字幕译文字段名

包括 `title_prompt`,`summary_prompt`,`terms_prompt`背后也是通过 `env`来配置的，默认如下：


```
        "title_prompt": "\n\n## Context Awareness\nDocument Metadata:\nTitle: 《{{imt_title}}》",
        "summary_prompt": "\n\n## Context Awareness\nDocument Metadata:\nSummary: {{imt_theme}}...",
        "terms_prompt": "\n\nRequired Terminology: You MUST use the following terms during translation, If 'source':'target', source == target, keep the source term unchanged.\n\n Terms -> \n\n {{imt_terms}}",
        "sub_summary_prompt": "\n\n## Context Awareness\nDocument Metadata:\nType: Subtitle\nSummary: {{imt_theme}}...",
        "sub_terms_prompt": "\n\nRequired Terminology: You MUST use the following terms during translation, If 'source':'target', source == target, keep the source term unchanged.\n\n Terms -> \n\n {{imt_terms}}"

```

其中 `imt_title`, `imt_theme`,`imt_terms` 为特殊变量，由系统注入，`imt_title`为标题，`imt_theme`为整个网页的总结，`imt_terms`为模型提取的关键术语。

> 注意： `imt_theme`, `imt_terms` 是专有服务提取的，目前仅为 [Pro 会员](https://immersivetranslate.com/pricing/)提供。


### YAML Prompt 示例


```yaml
systemPrompt: |
  You are a professional, authentic machine translation engine.
  {{title_prompt}}{{summary_prompt}}{{terms_prompt}}

multiplePrompt: |
    You will be given a YAML formatted input containing entries with "id" and "{{imt_source_field}}" fields. Here is the input:

    <yaml>
    {{yaml}}
    </yaml>

    For each entry in the YAML, translate the contents of the "{{imt_source_field}}" field into {{to}},{{html_only}} Write the translation back into the "{{imt_source_field}}" field for that entry.

    Here is an example of the expected format:

    {{normal_result_yaml_example}}

    Please return the translated YAML directly without wrapping <yaml> tag or include any additional information.
subtitlePrompt: |
    You will be given a YAML formatted subtitles containing entries with "id" and "{{imt_sub_source_field}}" fields. Here is the input:

    <yaml>
    {{yaml}}
    </yaml>

    For each entry in the YAML, translate the contents of the "{{imt_sub_source_field}}" field into {{to}},{{html_only}} Write the translation back into the "{{imt_sub_source_field}}" field for that entry.

    Here is an example of the expected format:

    {{subtitle_result_yaml_example}}

    Please return the translated YAML directly without wrapping <yaml> tag or include any additional information.

```

其中 `html_only` 为特殊变量，仅翻译的原文为 HTML 格式时才有，值为： `\n\nPs. if the text contains html tags, please consider after translate, where the tags should be in translated result, meanwhile keep the result fluently.` , 当用户主动在 AI 翻译服务中设置 开启“富文本翻译”时才会有这个变量存在。否则为空。

`normal_result_yaml_example` 在 `env` 中设置，默认为：

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

`subtitle_result_yaml_example` 在 `env` 中设置，默认值为：

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

你可以在 `env` 中覆盖它。


## 高级示例：反思式翻译

这个示例展示了如何使用 YAML 格式实现更复杂的翻译流程，包含初步翻译和优化翻译两个步骤：

```yaml
env:
  imt_source_field: source
  imt_trans_field: step2  # 最终译文使用 step2 字段
  imt_sub_source_field: source
  imt_sub_trans_field: step2
  imt_yaml_item: |-
    - id: {{id}}
      {{imt_source_field}}: {{text}}
  imt_subtitle_yaml_item: |-
    - id: {{id}}
      {{imt_sub_source_field}}: {{text}}

systemPrompt: |
  You are a professional, authentic machine translation engine.
  {{title_prompt}}{{summary_prompt}}{{terms_prompt}}

multiplePrompt: |
  Here is the YAML input:
  <yaml>
  {{yaml}}
  </yaml>
  
  Please follow these steps:
  1. Extract the content from the "source" field in the provided YAML object.
  2. Translate the extracted content into {{to}}. Place this initial translation into the step1 field.
  3. Refine the initial translation from step1 to make it more natural and understandable in {{to}}. 
     Place this refined translation into the step2 field.
  4. Format the result as a YAML array with id, step1, and step2 fields as shown in this example:
  
  - id: 1 
    step1: Initial translation
    step2: Refined translation
  
  Return the translated YAML directly without any <example_output> tags or additional information.
```

### 工作流程说明

1. **输入格式**：
   ```yaml
   - id: 1
     source: "Hello world"
   - id: 2
     source: "How are you?"
   ```

2. **AI 处理步骤**：
   - Step 1: 进行初步翻译
   - Step 2: 优化翻译，使其更自然流畅

3. **输出格式**：
   ```yaml
   - id: 1
     step1: "你好世界"
     step2: "你好，世界"
   - id: 2
     step1: "你怎么样？"
     step2: "你好吗？"
   ```



