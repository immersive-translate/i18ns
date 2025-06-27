---
sidebar_position: 5
---
# Immersive Translate AI Prompt Configuration Guide

## Overview

Immersive Translate supports custom AI translation Prompt configuration, allowing advanced users to adjust translation behavior according to their needs. This document provides detailed instructions on configuration methods, supported variables, and advanced usage.

## Supported Variables

### Basic Variables

- `{{text}}` - The text content to be translated
- `{{from}}` - Source language
- `{{to}}` - Target language
- `{{content_type}}` - Type of original text (`html` or `text`)

### Context Variables
- `{{title_prompt}}` - Web page title (when available)
- `{{summary_prompt}}` - Web page context summary (when available)
- `{{terms_prompt}}` - Related professional terminology (when available)

## Configuration Methods

### 1. System Prompt(`systemPrompt`)
Translation request sent to AI as system identity. Used to set AI's role and basic rules.

### 2. Prompt(`prompt`)
Conversation sent to AI as user identity, containing actual content to be translated.

### 3. System Multiple Prompt(`systemMultiplePrompt`)
Translation request sent to AI as system identity when paragraph count is greater than 1. Used for handling multi-paragraph translation scenarios.

### 4. Multiple Prompt(`multiplePrompt`)
Request sent as user identity for multi-paragraph translation. Supports using separators or YAML format.

### 5. Subtitle Prompt(`subtitlePrompt`)

When subtitle translation is needed, conversation sent to AI as user identity, containing actual content to be translated.

## Default Configuration Examples

If only one paragraph is collected, it will use single paragraph Prompt by default. If multiple paragraphs are collected, it will use multi-paragraph Prompt by default. Most cases will be multi-paragraph. The default separator for multi-paragraph is `%%`. We deliberately use this uncommon separator to reduce large model hallucinations. You can modify this Prompt as your base to create the Prompt you need. Here are the default Prompt configurations:

### Single Paragraph Translation

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

### Multi-paragraph Translation

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

## Advanced Usage (YAML Format)

For scenarios requiring more precise control (such as multi-step output), YAML format can be used for configuration:

### Advanced Variables

- `{{yaml}}` - YAML format input data

The default 'yaml' variable looks approximately like this:

```
- id: 1
  text: Hello world
- id: 2
  text: How are you?
```

We expect the large model's output to be like this by default:

```
- id: 1
  text: 你好世界
- id: 2
  text: 你好吗？
```

If you use the default `{{yaml}}`, you need to express this expectation clearly in the prompt. If you want to modify the default and response `yaml` format, this cannot be solved through the UI in the Immersive Translate settings page. You must directly edit the Immersive Translate JSON format user configuration.

User configuration edit path: `Settings Page`->`Developer Settings`->`Edit Full User Config` (Please backup your user configuration before editing)

You can find the translation service configuration in the user configuration JSON (if not present, add it directly according to this structure):

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

The `yaml` variable is composed of `env.imt_yaml_item`, so you can modify the format of `imt_yaml_item`, like this:

```json
  "translationServices": {
    "openai": {
       "env": {
          "imt_yaml_item": "- id: {{id}}\n  source: {{text}}"
        }
    }
   }
```

Another special variable is `imt_subtitle_yaml_item`, similar to `imt_yaml_item`, used for subtitle translation YAML items.

For other `env` variables, you can add any `env` variables and use them directly in the prompt in the format `{{variable_name}}`, such as the following default `env` variables:

- `{{imt_source_field}}` - Source text field name (default: text)
- `{{imt_trans_field}}` - Translation field name (default: text)
- `{{imt_sub_source_field}}` - Subtitle source text field name
- `{{imt_sub_trans_field}}` - Subtitle translation field name

Including `title_prompt`, `summary_prompt`, `terms_prompt` are also configured through `env` behind the scenes, defaults are as follows:

```
        "title_prompt": "\n\n## Context Awareness\nDocument Metadata:\nTitle: 《{{imt_title}}》",
        "summary_prompt": "\n\n## Context Awareness\nDocument Metadata:\nSummary: {{imt_theme}}...",
        "terms_prompt": "\n\nRequired Terminology: You MUST use the following terms during translation, If 'source':'target', source == target, keep the source term unchanged.\n\n Terms -> \n\n {{imt_terms}}",
        "sub_summary_prompt": "\n\n## Context Awareness\nDocument Metadata:\nType: Subtitle\nSummary: {{imt_theme}}...",
        "sub_terms_prompt": "\n\nRequired Terminology: You MUST use the following terms during translation, If 'source':'target', source == target, keep the source term unchanged.\n\n Terms -> \n\n {{imt_terms}}"

```

Where `imt_title`, `imt_theme`, `imt_terms` are special variables injected by the system. `imt_title` is the title, `imt_theme` is the summary of the entire webpage, and `imt_terms` are key terms extracted by the model.

> Note: `imt_theme`, `imt_terms` are extracted by proprietary services, currently only available to [Pro members](https://immersivetranslate.com/pricing/).

### YAML Prompt Examples

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

Where `html_only` is a special variable that only exists when the original text to be translated is in HTML format, with the value: `\n\nPs. if the text contains html tags, please consider after translate, where the tags should be in translated result, meanwhile keep the result fluently.` This variable only exists when users actively enable "Rich Text Translation" in AI translation services. Otherwise it's empty.

`normal_result_yaml_example` is set in `env`, default is:

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

`subtitle_result_yaml_example` is set in `env`, default value is:

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

You can override it in `env`.

## Advanced Example: Reflective Translation

This example demonstrates how to use YAML format to implement more complex translation workflows, including initial translation and optimized translation in two steps:

```yaml
env:
  imt_source_field: source
  imt_trans_field: step2  # Final translation uses step2 field
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

### Workflow Description

1. **Input Format**:
   ```yaml
   - id: 1
     source: "Hello world"
   - id: 2
     source: "How are you?"
   ```

2. **AI Processing Steps**:
   - Step 1: Perform initial translation
   - Step 2: Optimize translation to make it more natural and fluent

3. **Output Format**:
   ```yaml
   - id: 1
     step1: "你好世界"
     step2: "你好，世界"
   - id: 2
     step1: "你怎么样？"
     step2: "你好吗？"
   ```
