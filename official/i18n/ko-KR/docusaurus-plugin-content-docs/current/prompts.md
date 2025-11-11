---
sidebar_position: 5
---
# AI Prompt 설정 가이드

## 개요

Immersive Translate 는 사용자 정의 AI 번역 Prompt 설정을 지원하여 고급 사용자가 자신의 요구에 따라 번역 동작을 조정할 수 있습니다. 이 문서는 설정 방법, 지원되는 변수 및 고급 사용법에 대한 자세한 지침을 제공합니다.

## 지원되는 변수

### 기본 변수

- `{{text}}` - 번역할 텍스트 내용
- `{{from}}` - 소스 언어
- `{{to}}` - 대상 언어
- `{{content_type}}` - 원본 텍스트의 유형 (`html` 또는 `text`)

### 컨텍스트 변수
- `{{title_prompt}}` - 웹 페이지 제목 (사용 가능한 경우)
- `{{summary_prompt}}` - 웹 페이지 컨텍스트 요약 (사용 가능한 경우)
- `{{terms_prompt}}` - 관련 전문 용어 (사용 가능한 경우)

## 설정 방법

### 1. System Prompt(`systemPrompt`)
시스템 신원으로 AI 에 전송되는 번역 요청. AI 의 역할과 기본 규칙을 설정하는 데 사용됩니다.

### 2. Prompt(`prompt`)
사용자 신원으로 AI 에 전송되는 대화로, 실제로 번역해야 하는 내용을 포함합니다.

### 3. System Multiple Prompt(`systemMultiplePrompt`)
단락 수가 1 보다 큰 경우 시스템 신원으로 AI 에 전송되는 번역 요청. 여러 단락 번역 시나리오를 처리하는 데 사용됩니다.

### 4. Multiple Prompt(`multiplePrompt`)
여러 단락 번역 시 사용자 신원으로 전송되는 요청. 구분 기호 또는 YAML 형식 사용을 지원합니다.

### 5. Subtitle Prompt(`subtitlePrompt`)

자막 번역이 필요한 경우 사용자 신원으로 AI 에 전송되는 대화로, 실제로 번역해야 하는 내용을 포함합니다.

## 기본 설정 예제

단 하나의 단락만 수집된 경우 기본적으로 단일 단락 Prompt 를 사용합니다. 여러 단락이 수집된 경우 기본적으로 여러 단락 Prompt 를 사용합니다. 대부분의 경우 여러 단락이 됩니다. 여러 단락의 기본 구분 기호는 `%%`입니다. 대형 모델의 환각을 줄이기 위해 의도적으로 이 일반적이지 않은 구분 기호를 사용합니다. 이 Prompt 를 기반으로 필요한 Prompt 로 수정할 수 있습니다. 다음은 기본 Prompt 설정입니다:

### 단일 단락 번역

```yaml
systemPrompt: |
    당신은 {{to}}로 텍스트를 유창하게 번역해야 하는 전문 {{to}} 원어민 번역가입니다.

    ## 번역 규칙
    1. 번역된 내용만 출력하고 설명이나 추가 내용(예: "번역은 다음과 같습니다:" 또는 "번역:" 등)을 포함하지 마세요
    2. 반환된 번역은 원본 텍스트와 정확히 동일한 단락 수와 형식을 유지해야 합니다
    3. 텍스트에 HTML 태그가 포함된 경우 유창성을 유지하면서 번역에서 태그를 배치할 위치를 고려하세요
    4. 번역하지 않아야 하는 내용(예: 고유 명사, 코드 등) 의 경우 원본 텍스트를 유지하세요
    5. 번역을 직접 출력하세요(구분 기호 없음, 추가 텍스트 없음){{title_prompt}}{{summary_prompt}}{{terms_prompt}}
prompt: |
  {{to}}로 번역하세요(번역만 출력):

  {{text}}
```

### 여러 단락 번역

```yaml
multipleSystemPrompt: |
    당신은 {{to}}로 텍스트를 유창하게 번역해야 하는 전문 {{to}} 원어민 번역가입니다.

    ## 번역 규칙
    1. 번역된 내용만 출력하고 설명이나 추가 내용(예: "번역은 다음과 같습니다:" 또는 "번역:" 등)을 포함하지 마세요
    2. 반환된 번역은 원본 텍스트와 정확히 동일한 단락 수와 형식을 유지해야 합니다
    3. 텍스트에 HTML 태그가 포함된 경우 유창성을 유지하면서 번역에서 태그를 배치할 위치를 고려하세요
    4. 번역하지 않아야 하는 내용(예: 고유 명사, 코드 등) 의 경우 원본 텍스트를 유지하세요{{title_prompt}}{{summary_prompt}}{{terms_prompt}}

    ## 입력 - 출력 형식 예제

    ### 입력 예제:
    Paragraph A

    %%

    Paragraph B

    %%

    Paragraph C

    %%

    Paragraph D

    ### 출력 예제:
    Translation A

    %%

    Translation B

    %%

    Translation C

    %%

    Translation D

multiplePrompt: |
  {{to}}로 번역하세요:

  {{text}}
subtitlePrompt: |
  {{to}}로 번역하세요:

  {{text}}
```

## 고급 사용법 (YAML 형식)

더 정확한 제어가 필요한 시나리오 (예: 다단계 출력) 의 경우 YAML 형식을 사용하여 설정할 수 있습니다:

### 고급 변수

- `{{yaml}}` - YAML 형식의 입력 데이터

기본 'yaml' 변수는 다음과 같습니다:

```
- id: 1
  text: Hello world
- id: 2
  text: How are you?
```

기본적으로 대형 모델의 출력이 다음과 같을 것으로 예상합니다:

```
- id: 1
  text: 你好世界
- id: 2
  text: 你好吗？
```

기본 `{{yaml}}`을 사용하는 경우 prompt 에서 이 기대를 명확하게 표현해야 합니다. 기본 및 응답 `yaml` 형식을 수정하려는 경우 Immersive Translate 설정 페이지의 UI 를 통해 해결할 수 없습니다. Immersive Translate 의 JSON 형식 사용자 설정을 직접 편집해야 합니다.

사용자 설정 편집 경로: `설정 페이지`->`개발자 설정`->`Edit Full User Config` (편집하기 전에 사용자 설정을 백업하세요)

사용자 설정의 JSON 에서 번역 서비스 설정을 찾을 수 있습니다 (없는 경우 이 구조에 따라 추가하면 됩니다):

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

`yaml` 변수는 `env.imt_yaml_item`로 구성되므로 다음과 같이 `imt_yaml_item` 형식을 수정할 수 있습니다:

```json
  "translationServices": {
    "openai": {
       "env": {
          "imt_yaml_item": "- id: {{id}}\n  source: {{text}}"
        }
    }
   }
```

또 다른 특수 변수는 `imt_subtitle_yaml_item`로, `imt_yaml_item`과 유사하며 자막 번역을 위한 YAML 항목에 사용됩니다.

다른 `env` 변수의 경우 `{{변수명}}` 형식으로 prompt 에서 직접 사용할 수 있는 모든 `env` 변수를 추가할 수 있습니다. 예를 들어 다음과 같은 기본 `env` 변수:

- `{{imt_source_field}}` - 소스 텍스트 필드 이름 (기본값: text)
- `{{imt_trans_field}}` - 번역 텍스트 필드 이름 (기본값: text)
- `{{imt_sub_source_field}}` - 자막 소스 텍스트 필드 이름
- `{{imt_sub_trans_field}}` - 자막 번역 텍스트 필드 이름

`title_prompt`, `summary_prompt`, `terms_prompt`도 `env`를 통해 설정되며 기본값은 다음과 같습니다:

```
        "title_prompt": "\n\n## 컨텍스트 인식\n문서 메타데이터:\n제목: 《{{imt_title}}》",
        "summary_prompt": "\n\n## 컨텍스트 인식\n문서 메타데이터:\n요약: {{imt_theme}}...",
        "terms_prompt": "\n\n필수 용어: 번역 중에 다음 용어를 사용해야 합니다. 'source':'target'에서 source == target인 경우 소스 용어를 변경하지 않고 유지하세요.\n\n 용어 -> \n\n {{imt_terms}}",
        "sub_summary_prompt": "\n\n## 컨텍스트 인식\n문서 메타데이터:\n유형: 자막\n요약: {{imt_theme}}...",
        "sub_terms_prompt": "\n\n필수 용어: 번역 중에 다음 용어를 사용해야 합니다. 'source':'target'에서 source == target인 경우 소스 용어를 변경하지 않고 유지하세요.\n\n 용어 -> \n\n {{imt_terms}}"

```

여기서 `imt_title`, `imt_theme`, `imt_terms`는 시스템에 의해 주입되는 특수 변수입니다. `imt_title`은 제목이고, `imt_theme`은 전체 웹 페이지의 요약이며, `imt_terms`는 모델이 추출한 핵심 용어입니다.

> 참고: `imt_theme`, `imt_terms`는 독점 서비스에 의해 추출되며 현재 [Pro 회원](https://immersivetranslate.com/pricing/)에게만 제공됩니다.

### YAML Prompt 예제

```yaml
systemPrompt: |
  당신은 전문적이고 신뢰할 수 있는 기계 번역 엔진입니다.
  {{title_prompt}}{{summary_prompt}}{{terms_prompt}}

multiplePrompt: |
    "id" 및 "{{imt_source_field}}" 필드가 있는 항목을 포함하는 YAML 형식의 입력을 받게 됩니다. 입력은 다음과 같습니다:

    <yaml>
    {{yaml}}
    </yaml>

    YAML의 각 항목에 대해 "{{imt_source_field}}" 필드의 내용을 {{to}}로 번역하고,{{html_only}} 번역 결과를 해당 항목의 "{{imt_source_field}}" 필드에 다시 작성하세요.

    예상 형식의 예는 다음과 같습니다:

    {{normal_result_yaml_example}}

    <yaml> 태그나 추가 정보 없이 번역된 YAML을 직접 반환하세요.
subtitlePrompt: |
    "id" 및 "{{imt_sub_source_field}}" 필드가 있는 항목을 포함하는 YAML 형식의 자막 입력을 받게 됩니다. 입력은 다음과 같습니다:

    <yaml>
    {{yaml}}
    </yaml>

    YAML의 각 항목에 대해 "{{imt_sub_source_field}}" 필드의 내용을 {{to}}로 번역하고,{{html_only}} 번역 결과를 해당 항목의 "{{imt_sub_source_field}}" 필드에 다시 작성하세요.

    예상 형식의 예는 다음과 같습니다:

    {{subtitle_result_yaml_example}}

    <yaml> 태그나 추가 정보 없이 번역된 YAML을 직접 반환하세요.

```

`html_only`는 번역할 원본 텍스트가 HTML 형식인 경우에만 존재하는 특수 변수입니다. 값은 다음과 같습니다: `\n\n참고: 텍스트에 HTML 태그가 포함된 경우 번역 후 태그가 번역 결과의 어디에 배치되어야 하는지 고려하되 결과의 유창성을 유지하세요.`, 사용자가 AI 번역 서비스에서 "리치 텍스트 번역"을 활성화한 경우에만 이 변수가 존재합니다. 그렇지 않으면 비어 있습니다.

`normal_result_yaml_example`은 `env`에서 설정되며 기본값은 다음과 같습니다:

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

`subtitle_result_yaml_example`은 `env`에서 설정되며 기본값은 다음과 같습니다:

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

`env`에서 이를 덮어쓸 수 있습니다.

## 고급 예제: 반성적 번역

이 예제는 YAML 형식을 사용하여 초기 번역과 최적화된 번역의 두 단계를 포함하는 더 복잡한 번역 워크플로우를 구현하는 방법을 보여줍니다:

```yaml
env:
  imt_source_field: source
  imt_trans_field: step2  # 최종 번역은 step2 필드를 사용합니다
  imt_sub_source_field: source
  imt_sub_trans_field: step2
  imt_yaml_item: |-
    - id: {{id}}
      {{imt_source_field}}: {{text}}
  imt_subtitle_yaml_item: |-
    - id: {{id}}
      {{imt_sub_source_field}}: {{text}}

systemPrompt: |
  당신은 전문적이고 신뢰할 수 있는 기계 번역 엔진입니다.
  {{title_prompt}}{{summary_prompt}}{{terms_prompt}}

multiplePrompt: |
  다음은 YAML 입력입니다:
  <yaml>
  {{yaml}}
  </yaml>
  
  다음 단계를 따르세요:
  1. 제공된 YAML 객체에서 "source" 필드의 내용을 추출합니다.
  2. 추출한 내용을 {{to}}로 번역합니다. 이 초기 번역을 step1 필드에 배치합니다.
  3. step1의 초기 번역을 최적화하여 {{to}}에서 더 자연스럽고 이해하기 쉽게 만듭니다. 
     최적화된 번역을 step2 필드에 배치합니다.
  4. 다음 예제에 표시된 대로 id, step1 및 step2 필드가 있는 YAML 배열로 결과를 포맷합니다:
  
  - id: 1 
    step1: 초기 번역
    step2: 최적화된 번역
  
  <example_output> 태그나 추가 정보 없이 번역된 YAML을 직접 반환하세요.
```

### 워크플로우 설명

1. **입력 형식**：
   ```yaml
   - id: 1
     source: "Hello world"
   - id: 2
     source: "How are you?"
   ```

2. **AI 처리 단계**：
   - 1 단계: 초기 번역 수행
   - 2 단계: 번역을 최적화하여 더 자연스럽고 유창하게 만듭니다

3. **출력 형식**：
   ```yaml
   - id: 1
     step1: "你好世界"
     step2: "你好，世界"
   - id: 2
     step1: "你怎么样？"
     step2: "你好吗？"
   ```
