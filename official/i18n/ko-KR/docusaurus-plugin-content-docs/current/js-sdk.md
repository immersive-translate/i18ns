---
sidebar_position: 5
---

# JS SDK

Immersive Translate JS SDK 는 웹사이트에서 이중 언어 번역을 구현하는 데 도움을 줍니다.

## 사용 방법

1. Immersive Translate 초기화:

```js
<script>
  window.immersiveTranslateConfig = {
    pageRule: {}
  }
</script>
```

2. 다음 `script` 코드를 웹페이지에 추가하세요.

```html
<script src="https://download.immersivetranslate.com/immersive-translate-sdk-latest.js"></script>
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

## 매개변수

`pageRule`을 사용하여 웹사이트의 구성을 사용자 정의하고, 번역이 필요한 콘텐츠를 결정하거나 웹페이지 스타일을 조정할 수 있습니다.

```js
initImmersiveTranslate({
  pageRule: {
    selectors: [".text"],
    excludeSelectors: ["nav", "footer"],
  },
});
```

`selectors`를 사용하면 스마트 번역 범위를 재정의하여 선택자와 일치하는 요소만 번역합니다.

`excludeSelectors`를 사용하면 번역에서 요소를 제외할 수 있습니다.

`selectors.add`를 사용하면 기본 선택자에 선택자를 추가할 수 있습니다.

`selectors.remove`를 사용하면 기본 선택자에서 선택자를 제거할 수 있습니다.

특정 영역을 번역하고 요소를 전체로 간주하여 줄로 나누지 않으려면 `atomicBlockSelectors` 선택자를 사용할 수 있습니다. `atomicBlockSelectors`를 사용하기 전에 `selectors`를 사용하여 요소를 선택해야 합니다.

```json
{
  "selectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"],
  "atomicBlockSelectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"]
}
```

`pageRule`의 추가 매개변수 설명:

```typescript
export interface PageRule {
  excludeMatches?: string | string[]; // 특정 웹사이트 제외.
  selectorMatches?: string | string[]; // 모든 URL 을 지정하지 않고 선택자를 사용하여 일치
  excludeSelectorMatches?: string | string[]; // 제외 규칙, 위와 동일.

  // 번역 범위 지정
  selectors?: string | string[]; // 일치하는 요소만 번역
  excludeSelectors?: string | string[]; // 요소 제외, 일치하는 요소 번역 안 함
  excludeTags?: string | string[]; // 태그 제외, 일치하는 태그 번역 안 함

  // 번역 범위 추가, 재정의하지 않음
  additionalSelectors?: string | string[]; // 번역 범위 추가. 스마트 번역 영역에 번역 위치 추가.
  additionalExcludeSelectors?: string | string[]; // 특정 위치에서 스마트 번역을 방지하기 위해 제외된 요소 추가.
  additionalExcludeTags?: string | string[]; // 제외된 태그 추가

  // 원본 유지
  stayOriginalSelectors?: string | string[]; // 일치하는 요소는 원본으로 유지됩니다. 포럼 웹사이트의 태그에 일반적으로 사용됩니다.
  stayOriginalTags?: string | string[]; // 일치하는 태그는 원본으로 유지됩니다. 예: `code`

  // 영역 번역
  atomicBlockSelectors?: string | string[]; // 영역 선택자, 일치하는 요소는 전체로 간주되며, 세그먼트로 번역되지 않음
  atomicBlockTags?: string | string[]; // 영역 태그 선택자, 위와 동일

  // 블록 또는 인라인
  extraBlockSelectors?: string | string[]; // 추가 선택자, 일치하는 요소는 블록 요소로 처리되어 한 줄을 차지합니다.
  extraInlineSelectors?: string | string[]; // 추가 선택자, 일치하는 요소는 인라인 요소로 처리됩니다.

  inlineTags?: string | string[]; // 일치하는 태그는 인라인 요소로 처리됩니다.
  preWhitespaceDetectedTags?: string | string[]; // 일치하는 태그는 자동으로 줄을 감쌉니다.

  // 번역 스타일
  translationClasses?: string | string | string[]; // 번역에 추가 클래스를 추가합니다.

  // 전역 스타일
  globalStyles?: Record<string, string>; // 페이지 스타일 수정, 번역으로 인해 페이지가 어지러워질 때 유용합니다.
  globalAttributes?: Record<string, Record<string, string>>; // 페이지 요소의 속성 수정

  // 내장 스타일
  injectedCss?: string | string[]; // CSS 스타일 내장
  additionalInjectedCss?: string | string[]; // CSS 스타일을 직접 재정의하지 않고 추가합니다.

  // 컨텍스트
  wrapperPrefix?: string; // 번역 영역의 접두사, 기본값은 스마트이며, 문자 수에 따라 줄을 감쌀지 여부를 결정합니다.
  wrapperSuffix?: string; // 번역 영역의 접미사

  // 번역 줄 감싸기 문자 수
  blockMinTextCount?: number; // 블록으로 번역하기 위한 최소 문자 수, 그렇지 않으면 번역은 인라인 요소가 됩니다.
  blockMinWordCount?: number; // 위와 동일. 항상 줄을 감싸려면 둘 다 0 으로 설정하세요.

  // 번역 가능한 콘텐츠의 최소 문자 수
  containerMinTextCount?: number; // 스마트 인식 중 번역할 요소의 최소 문자 수, 기본값은 18 입니다.
  paragraphMinTextCount?: number; // 원본 단락의 최소 문자 수, 내용이 이 수보다 크면 번역됩니다.
  paragraphMinWordCount?: number; // 원본 단락의 최소 단어 수

  // 긴 단락의 강제 줄 바꿈 문자 수
  lineBreakMaxTextCount?: number; // 긴 단락을 번역할 때 강제 줄 바꿈을 위한 최대 문자 수.

  // 번역 시작 시점
  urlChangeDelay?: number; // 페이지에 들어간 후 번역을 시작하기 전의 지연 시간 (밀리초). 기본값은 250ms 로, 웹페이지 초기화를 기다립니다.

  // AI 스트리밍 번역
  aiRule: {
    streamingSelector: string; // 번역 요소를 표시하는 GPT 웹페이지 선택자
    messageWrapperSelector: string; // 메시지 본문 선택자
    streamingChange: boolean; // GPT 와 같은 웹페이지에서 반복되는 메시지의 증분 또는 전체 업데이트. GPT 는 증분입니다.
  };
}
```
