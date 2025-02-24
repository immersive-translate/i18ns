---
sidebar_position: 5
---

# JS SDK

Immersive Translate JS SDK는 여러분의 웹사이트에서 이중 언어 번역을 구현하는 데 도움을 줍니다.

## 사용 방법

> JS SDK를 디버깅하기 전에 Immersive Translate 확장을 비활성화하세요.

1. 초기화 매개변수 설정 (immersiveTranslateConfig를 설정하지 않으면 JS SDK 초기화가 실패하므로 빈 객체로 설정할 수 있습니다)

```html
<script>
  window.immersiveTranslateConfig = {
    pageRule: {},
  };
</script>
```

2. 다음 `script` 코드를 웹페이지의 `</head>` 이전에 추가하세요.

```html
<script
  async
  src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"
></script>
```

예시

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

## 매개변수

- `pageRule`
  웹사이트에 대한 사용자 정의 구성을 통해 어떤 콘텐츠가 번역될지 결정하거나 웹 페이지 스타일을 조정할 수 있습니다.
- `isAutoTranslate`
  즉시 자동 번역

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

`selectors`를 사용하면 스마트 번역 범위를 덮어쓰고 해당 선택자에 매칭되는 요소만 번역합니다.

`excludeSelectors`를 사용하면 요소를 제외하여 해당 위치를 번역하지 않습니다.

`selectors.add`를 사용하면 기본값에 몇 가지 선택자를 추가할 수 있습니다.

`selectors.remove`를 사용하면 기본값에서 몇 가지 선택자를 제거할 수 있습니다.

특정 영역을 번역할 때 요소를 하나의 전체로 간주하고 줄을 나누지 않으려면 `atomicBlockSelectors` 선택자를 사용할 수 있습니다. `atomicBlockSelectors`를 사용하기 전에 `selectors`로 선택해야 합니다.

```json
{
  "selectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"],
  "atomicBlockSelectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"]
}
```

`pageRule`의 추가 매개변수 설명:

```typescript
export interface PageRule {
  excludeMatches?: string | string[]; // 특정 웹사이트를 제외합니다.
  selectorMatches?: string | string[]; // 모든 URL을 지정하지 않고 선택자로 매칭합니다.
  excludeSelectorMatches?: string | string[]; // 제외 규칙, 위와 동일합니다.


你是一位专业的技术文档翻译专家。  
请将以下 Markdown 内容翻译成 Korean，并严格遵循以下规则：

1. 保持原有格式：
   - 모든 Markdown 문법을 변경하지 않고 유지
   - 모든 코드 블록과 HTML 태그를 유지
   - 원래의 줄 바꿈과 공백을 유지
   - 모든 링크와 URL을 변경하지 않고 유지
   - ```markdown 시작과 ``` 끝의 코드 블록을 반환하지 마세요

2. 전문 용어:
   - 모든 기술 용어는 영어로 유지
   - 'Release', 'Preview' 등의 단어는 영어로 유지
   - 모든 버전 번호와 기술 사양을 변경하지 않고 유지

  // 지정된 번역 범위
  selectors?: string | string[]; // 일치하는 요소만 번역
  excludeSelectors?: string | string[]; // 제외할 요소, 일치하는 요소는 번역하지 않음
  excludeTags?: string | string[]; // 제외할 태그, 일치하는 태그는 번역하지 않음

  // 번역 범위 추가, 덮어쓰지 않음
  additionalSelectors?: string | string[]; // 번역 범위 추가. 스마트 번역 영역에 번역 위치 추가.
  additionalExcludeSelectors?: string | string[]; // 특정 위치를 번역하지 않도록 스마트 번역에서 제외할 요소 추가.
  additionalExcludeTags?: string | string[]; // 제외할 태그 추가

  // 원본 유지
  stayOriginalSelectors?: string | string[]; // 일치하는 요소는 원본 그대로 유지. 주로 포럼 사이트의 태그에 사용.
  stayOriginalTags?: string | string[]; // 일치하는 태그는 원본 그대로 유지, 예: `code`

  // 영역 번역
  atomicBlockSelectors?: string | string[]; // 영역 선택자, 일치하는 요소는 하나의 전체로 간주되어 분할 번역되지 않음
  atomicBlockTags?: string | string[]; // 영역 태그 선택자, 위와 동일

  // Block 또는 Inline
  extraBlockSelectors?: string | string[]; // 추가 선택자, 일치하는 요소는 block 요소로 간주되어 한 줄을 차지함.
  extraInlineSelectors?: string | string[]; // 추가 선택자, 일치하는 요소는 inline 요소로 간주됨.

  inlineTags?: string | string[]; // 일치하는 태그는 inline 요소로 간주됨
  preWhitespaceDetectedTags?: string | string[]; // 일치하는 태그는 자동으로 줄 바꿈

  // 번역 스타일
  translationClasses?: string | string | string[]; // 번역에 추가적인 클래스를 추가

  // 전역 스타일
  globalStyles?: Record<string, string>; // 페이지 스타일 수정, 번역으로 인해 페이지가 어긋날 경우 유용함.
  globalAttributes?: Record<string, Record<string, string>>; // 페이지 요소의 속성 수정

  // 스타일 삽입
  injectedCss?: string | string[]; // CSS 스타일 삽입
  additionalInjectedCss?: string | string[]; // CSS 스타일 추가, 직접 덮어쓰지 않음.

  // 컨텍스트
  wrapperPrefix?: string; // 번역 영역의 접두사, 기본값은 smart, 글자 수에 따라 줄 바꿈 여부 결정.
  wrapperSuffix?: string; // 번역 영역의 접미사

  // 번역 줄 바꿈 글자 수
  blockMinTextCount?: number; // 번역을 block으로 간주할 최소 문자 수, 그렇지 않으면 번역은 inline 요소로 간주됨.
  blockMinWordCount?: number; // 위와 동일. 항상 줄 바꿈을 원하면 둘 다 0으로 설정.

  // 번역 가능한 최소 글자 수
  containerMinTextCount?: number; // 스마트 인식 시, 요소가 번역되기 위해 포함해야 하는 최소 문자 수, 기본값은 18
  paragraphMinTextCount?: number; // 원문 단락의 최소 문자 수, 숫자보다 큰 내용은 번역됨
  paragraphMinWordCount?: number; // 원문 단락의 최소 단어 수

  // 긴 단락 강제 줄 바꿈 글자 수
  lineBreakMaxTextCount?: number; // 긴 단락 번역 시, 강제로 줄 바꿈할 단락의 최대 문자 수.

```markdown
  // 번역 시작 시점
  urlChangeDelay?: number; // 페이지에 진입한 후, 번역을 시작하기까지 몇 밀리초 지연할지. 웹 페이지 초기화를 기다리기 위해 현재 기본값은 250ms

  // AI 스트리밍 번역
  aiRule: {
    streamingSelector: string; // gpt 웹 페이지에서 번역 중인 요소를 표시하는 선택자
    messageWrapperSelector: string; // 메시지 본문 선택자
    streamingChange: boolean; // gpt와 같은 웹 페이지의 반복 메시지가 증분 업데이트인지 전체 업데이트인지. gpt는 증분 업데이트
  };
}
```