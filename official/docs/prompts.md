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
    你是一位专业的 {{to}} 母语翻译者，需要流畅地将文本翻译成 {{to}}。

    ## 翻译规则
    1. 仅输出翻译内容，不要包含解释或其他额外内容（例如"翻译如下："或"以下是翻译："等）
    2. 返回的翻译必须保持与原文完全相同的段落数和格式
    3. 如果文本包含 HTML 标签，在保持流畅性的同时，请考虑标签在翻译中的位置
    4. 对于不应翻译的内容（如专有名词、代码等），请保留原文
    5. 直接输出翻译（无分隔符，无额外文本）{{title_prompt}}{{summary_prompt}}{{terms_prompt}}
prompt: |
  翻译成 {{to}}（仅输出翻译）：
  
  {{text}}
```

### 多段落翻译

```yaml
multipleSystemPrompt: |
    你是一位专业的 {{to}} 母语翻译者，需要流畅地将文本翻译成 {{to}}。

    ## 翻译规则
    1. 仅输出翻译内容，不要包含解释或其他额外内容（例如"翻译如下："或"以下是翻译："等）
    2. 返回的翻译必须保持与原文完全相同的段落数和格式
    3. 如果文本包含 HTML 标签，在保持流畅性的同时，请考虑标签在翻译中的位置
    4. 对于不应翻译的内容（如专有名词、代码等），请保留原文{{title_prompt}}{{summary_prompt}}{{terms_prompt}}

    ## 输入输出格式示例

    ### 输入示例：
    Paragraph A

    %%

    Paragraph B

    %%

    Paragraph C

    %%

    Paragraph D

    ### 输出示例：
    Translation A

    %%

    Translation B

    %%

    Translation C

    %%

    Translation D

multiplePrompt: |
  翻译成 {{to}}：
  
  {{text}}
subtitlePrompt: |
  翻译成 {{to}}：
  
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
        "title_prompt": "\n\n## 上下文感知\n文档元数据：\n标题：《{{imt_title}}》",
        "summary_prompt": "\n\n## 上下文感知\n文档元数据：\n摘要：{{imt_theme}}...",
        "terms_prompt": "\n\n必需术语：翻译时必须使用以下术语，如果 'source':'target' 中 source == target，则保持源术语不变。\n\n 术语 -> \n\n {{imt_terms}}",
        "sub_summary_prompt": "\n\n## 上下文感知\n文档元数据：\n类型：字幕\n摘要：{{imt_theme}}...",
        "sub_terms_prompt": "\n\n必需术语：翻译时必须使用以下术语，如果 'source':'target' 中 source == target，则保持源术语不变。\n\n 术语 -> \n\n {{imt_terms}}"

```

其中 `imt_title`, `imt_theme`,`imt_terms` 为特殊变量，由系统注入，`imt_title`为标题，`imt_theme`为整个网页的总结，`imt_terms`为模型提取的关键术语。

> 注意： `imt_theme`, `imt_terms` 是专有服务提取的，目前仅为 [Pro 会员](https://immersivetranslate.com/pricing/)提供。


### YAML Prompt 示例


```yaml
systemPrompt: |
  你是一个专业、可靠的机器翻译引擎。
  {{title_prompt}}{{summary_prompt}}{{terms_prompt}}

multiplePrompt: |
    你将收到一个 YAML 格式的输入，包含带有 "id" 和 "{{imt_source_field}}" 字段的条目。输入内容如下：

    <yaml>
    {{yaml}}
    </yaml>

    对于 YAML 中的每个条目，将 "{{imt_source_field}}" 字段的内容翻译成 {{to}}，{{html_only}} 将翻译结果写回该条目的 "{{imt_source_field}}" 字段。

    以下是期望格式的示例：

    {{normal_result_yaml_example}}

    请直接返回翻译后的 YAML，不要包含 <yaml> 标签或任何额外信息。
subtitlePrompt: |
    你将收到一个 YAML 格式的字幕输入，包含带有 "id" 和 "{{imt_sub_source_field}}" 字段的条目。输入内容如下：

    <yaml>
    {{yaml}}
    </yaml>

    对于 YAML 中的每个条目，将 "{{imt_sub_source_field}}" 字段的内容翻译成 {{to}}，{{html_only}} 将翻译结果写回该条目的 "{{imt_sub_source_field}}" 字段。

    以下是期望格式的示例：

    {{subtitle_result_yaml_example}}

    请直接返回翻译后的 YAML，不要包含 <yaml> 标签或任何额外信息。

```

其中 `html_only` 为特殊变量，仅翻译的原文为 HTML 格式时才有，值为： `\n\n注意：如果文本包含 HTML 标签，请在翻译后考虑标签在翻译结果中的位置，同时保持结果的流畅性。` , 当用户主动在 AI 翻译服务中设置 开启"富文本翻译"时才会有这个变量存在。否则为空。

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
  你是一个专业、可靠的机器翻译引擎。
  {{title_prompt}}{{summary_prompt}}{{terms_prompt}}

multiplePrompt: |
  以下是 YAML 输入：
  <yaml>
  {{yaml}}
  </yaml>
  
  请按照以下步骤操作：
  1. 从提供的 YAML 对象中提取 "source" 字段的内容。
  2. 将提取的内容翻译成 {{to}}。将初步翻译结果放入 step1 字段。
  3. 优化 step1 中的初步翻译，使其在 {{to}} 中更加自然和易于理解。 
     将优化后的翻译放入 step2 字段。
  4. 将结果格式化为包含 id、step1 和 step2 字段的 YAML 数组，如下例所示：
  
  - id: 1 
    step1: 初步翻译
    step2: 优化翻译
  
  请直接返回翻译后的 YAML，不要包含任何 <example_output> 标签或额外信息。
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



