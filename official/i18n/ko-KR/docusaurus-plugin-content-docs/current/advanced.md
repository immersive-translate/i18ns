---
sidebar_position: 4
---

# 고급 사용자 정의 옵션

확장 구성 페이지 -> 개발자 설정 -> User Config에서 UI에서 편집할 수 없는 더 많은 사용자 정의 구성을 편집할 수 있습니다. 고급 사용자에게 적합하며, 매개변수 설명은 마지막 설명을 참조하십시오. 현재 내장된 `config`는 [여기](https://dash.immersivetranslate.com/#developer)에서 찾을 수 있으며, `Click to expand the final config`를 클릭하여 찾을 수 있습니다.


## 사용자 규칙

`Rules`를 통해 특정 웹사이트에 대한 사용자 정의 설정을 할 수 있으며, 어떤 내용을 번역할지, 웹페이지 스타일을 조정할지 등을 결정할 수 있습니다.

```json
[
  {
    "matches": "www.google.com",
    "selectors": [".title"]
  },
  {
    "matches": "twitter.com",
    "selectors": [".text"],
    "excludeSelectors": ["nav", "footer"]
  }
]
```

`matches`를 사용하여 해당 웹사이트를 매칭합니다. 와일드카드를 허용하며, 예를 들어 `*.google.com`, `www.google.com/test/*`, `file://*` 등이 있습니다.

`selectors`를 사용하면 스마트 번역 범위를 덮어쓰고, 해당 선택자가 매치하는 요소만 번역합니다.

`excludeSelectors`를 사용하여 요소를 제외시켜 해당 위치를 번역하지 않습니다.

`selectors.add`를 사용하면 기본값에 몇 가지 selectors를 추가합니다.

`selectors.remove`를 사용하면 기본값에서 몇 가지 selectors를 줄입니다.

```json
[
  {
    "matches": "www.google.com",
    "selectors.add": ["baidu.com"],
    "excludeSelectors": ["buzzing.cc"]
  }
]
```

특정 영역을 번역할 때 요소를 하나의 전체로 보고, 줄바꿈하지 않으려면 `atomicBlockSelectors` 선택자를 사용할 수 있습니다. 예를 들어, Instagram의 개인 프로필 같은 경우입니다. `atomicBlockSelectors`를 사용하기 전에 먼저 `selectors`로 선택해야 합니다.

```json
{
  "matches": "https://www.instagram.com/*",
  "selectors": [
    "div._aa_c h1",
    "li._acaz div[role=\"menuitem\"]"
  ],
  "atomicBlockSelectors": [
    "div._aa_c h1",
    "li._acaz div[role=\"menuitem\"]"
  ]
}
```

번역으로 인해 페이지가 어긋나거나 텍스트가 겹치는 등의 문제가 발생하는 경우, `globalStyles`를 사용하여 웹페이지 스타일을 조정함으로써 수정할 수 있습니다. 예를 들어, YouTube의 제목에서 원래 웹페이지의 최대 높이를 제거하는 경우입니다.

```json
{
  "matches": "www.google.com",
  "globalStyles": { ".title": "max-height:unset;" }
}
```

## 주입된 CSS

Injected CSS를 통해 전역에 사용자 정의 웹 페이지 스타일을 주입할 수 있습니다. `Rules`의 `translationClasses`와 함께 사용할 수 있습니다.

```css
.immersive-translate-target-wrapper img { width: 16px; height: 16px }
```

또한 일반적인 웹 페이지 스타일 관리자처럼, 웹사이트에 더 개성화된 스타일 디자인을 할 수 있습니다. (심지어 `display:none`을 사용하여 광고를 제거하는 것도 가능)

```css
.title {
  color: red;
}
```

## 사용자 설정

Config를 통해 이 플러그인의 관련 설정을 사용자 정의할 수 있습니다. 예를 들어, 번역 서비스, 특정 언어 번역 옵션 등을 설정할 수 있습니다.

```json
{
  "translationService": "tencent",
  "translationServices": {
    "tencent": {
      "secretId": "xxx",
      "secretKey": "xxx",
      "matches": ["twitter.com"]
    }
  },
  "translationUrlPattern": {
    "excludeMatches": ["www.google.com"]
  },
  "translationLanguagePattern": {
    "matches": ["en"]
  },
  "translationTheme": "none",
  "translationThemePatterns": {
    "underline": {
      "matches": ["discord.com"]
    }
  },
  "sourceLanguageUrlPattern": {
    "en": {
      "matches": ["*.google.com"]
    }
  },
  "generalRule": {
    "_comment": "",
    "normalizeBody": "",
    "injectedCss": [],
    "additionalInjectedCss": [],
    "wrapperPrefix": "smart",
    "wrapperSuffix": "smart",
    "isPdf": false,
    "isTransformPreTagNewLine": false,
    "urlChangeDelay": 20,
    "isShowUserscriptPagePopup": true,
    "observeUrlChange": true,
    "paragraphMinTextCount": 8,
    "paragraphMinWordCount": 2,
    "blockMinTextCount": 32,
    "blockMinWordCount": 5,
    "containerMinTextCount": 18,
    "lineBreakMaxTextCount": 0,
    "globalAttributes": {},
    "globalStyles": {},
    "selectors": [],
    "preWhitespaceDetectedTags": ["DIV", "SPAN"],
    "stayOriginalSelectors": [],
    "additionalSelectors": [],
    "atomicBlockTags": [],
    "excludeSelectors": [],
    "additionalExcludeSelectors": [],
    "translationClasses": [],
    "atomicBlockSelectors": [],
    "excludeTags": [],
    "metaTags": ["META", "SCRIPT", "STYLE", "NOSCRIPT"],
    "additionalExcludeTags": [],
    "stayOriginalTags": ["CODE", "TT", "IMG", "SUP"],
    "additionalStayOriginalTags": [],
    "inlineTags": [],
    "additionalInlineTags": [],
    "extraInlineSelectors": [],
    "additionalInlineSelectors": [],
    "extraBlockSelectors": [],
    "allBlockTags": [],
    "pdfNewParagraphLineHeight": 2.4,
    "pdfNewParagraphIndent": 1.2,
    "pdfNewParagraphIndentRightIndentPx": 130,
    "fingerCountToToggleTranslagePageWhenTouching": 4
  },
  "rules": [
    {
      "matches": "www.google.com",
      "selectors": [".class"]
    }
  ]
}
```

여기서, `rules`의 규칙 필드는 `generalRule`의 모든 필드를 사용할 수 있습니다. `rules`는 최우선 순위를 가지며, 특정 사이트의 특정 `rule`에 일치할 때, `generalRule`과 해당 `rule`의 규칙을 합칩니다.

Config의 몇 가지 일반적인 필드를 소개합니다.

### 일반 HTML 태그 렌더링 허용
[개발 설정](https://dash.immersivetranslate.com/#developer)으로 이동 -> 전체 사용자 설정 편집

"enableRenderHtmlTag": true로 편집

### 팝업 패널에 구성되지 않은 번역 서비스 표시 안 함

`"showUnconfiguredTranslationServiceInPopup": false`

### 번역 서비스 설정

`translationService`를 사용하여 기본 번역 엔진을 선택하십시오. 현재 지원되는 엔진은 다음과 같습니다:

```typescript
| "bing"
| "transmart"
| "google"
| "deepl"
| "openai"
| "gemini"
| "baidu"
| "volc"
| "youdao"
| "caiyun"
| "tencent"
| "openl"
```

`translationServices`를 사용하여 각 번역 서비스의 `apikey`를 설정하십시오. 서로 다른 서비스 제공업체는 다른 매개변수를 필요로 하며, 그들의 API 키는 각자의 공식 웹사이트 개발자 센터에서 신청할 수 있습니다.

예를 들어, 텐센트 번역기의 경우, `secretId`, `secretKey`를 설정해야 합니다. 텐센트 클라우드에서 API 키를 신청할 수 있으며, 매월 500만 문자까지 무료입니다. 구체적인 신청 과정은 [여기](/docs/services/tencent)를 참조하십시오.

```json
"translationServices": {
  "tencent": {
    "secretId": "xxx",
    "secretKey": "xxx",
    "matches":["twitter.com"],
    "limit": 3,
    "apiUrl":"",
    "maxTextGroupLengthPerRequest": 25,
    "maxTextLengthPerRequest": 1800
  }
}
```

`matches` 필드는 특정 웹사이트에서 해당 번역 서비스를 사용합니다.

`limit` 필드는 해당 번역 서비스의 초당 최대 요청 수를 지정합니다(일부 서비스는 초당 최대 요청 수를 제한할 수 있음).

`maxTextGroupLengthPerRequest` 필드는 각 요청의 최대 문단 수입니다.

`maxTextLengthPerRequest` 필드는 각 요청의 최대 문자 수입니다.

`apiUrl`은 번역 인터페이스의 주소를 사용자 정의할 수 있습니다.

### 특정 웹사이트 항상 번역하기

`translationUrlPattern` 설정은 항상 번역할 웹사이트와 절대 번역하지 않을 웹사이트를 설정합니다.

- `matches`는 항상 번역할 웹사이트를 설정합니다,
- `excludeMatches`는 절대 번역하지 않을 웹사이트를 설정합니다.

설정 값은 도메인이나 `*`가 포함된 웹 주소일 수 있습니다. 예: `www.google.com/mail/*`

```json
"translationUrlPattern": {
    "matches": ["stackoverflow.com"],
    "excludeMatches": ["www.google.com/mail/*"]
}
```

### 특정 언어 항상 번역하기

translationLanguagePattern, 항상 번역할 언어와 절대 번역하지 않을 언어를 설정합니다.

- `matches`는 항상 번역할 언어를 설정합니다, 예를 들어 `en`,
- `excludeMatches`는 절대 번역하지 않을 언어를 설정합니다.

### 번역 표시 형식

`translationTheme`은 번역의 표시 형식으로, 현재 다음 스타일을 지원합니다:

```typescript
| "none"
| "dashed"
| "dotted"
| "underline"
| "mask"
| "paper"
| "highlight"
| "blockquote"
| "weakening"
| "italic"
| "bold"
| "thinDashed";
```

해당하는 한국어 이름:

```json
{
  "none": "없음",
  "dashed": "파선 밑줄",
  "dotted": "점선 밑줄",
  "underline": "직선 밑줄",
  "mask": "흐림 효과",
  "paper": "백지 그림자 효과",
  "highlight": "하이라이트",
  "blockquote": "인용 스타일",
  "weakening": "약화",
  "italic": "이탤릭체",
  "bold": "굵게",
  "thinDashed": "세 파선 밑줄"
}
```

`translationThemePatterns`는 다른 웹사이트에 대해 다른 번역 스타일을 설정할 수 있습니다.

```json
"translationThemePatterns": {
  "underline": {
    "matches": ["discord.com"]
  }
}
```

### GPT와 같은 페이지 스트림 메시지 번역

```json
{
  "matches": ["chat.openai.com"], // GPT와 같은 웹사이트
  "excludeSelectors": [".markdown *"],
  "aiRule": {
    "streamingSelector": ".result-streaming.markdown",
    "messageWrapperSelector": ".markdown",
    "streamingChange": true
  }
}
```

### 규칙

`rules`는 배열 객체로, 특정 웹사이트에 대한 규칙을 설정할 수 있습니다. 예를 들어, 트위터를 특정 영역만 번역하도록 설정할 수 있습니다:

```json
{
  "rules": [
    {
      "id": "twitter",
      "matches": ["twitter.com", "mobile.twitter.com", "tweetdeck.twitter.com"],
      "selectors": [
        "[data-testid='tweetText']",
        ".tweet-text",
        ".js-quoted-tweet-text",
        "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)",
        "[data-testid='developerBuiltCardContainer'] > div:nth-child(2)",
        "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)"
      ],
      "extraInlineSelectors": ["[data-testid=\"tweetText\"] div"]
    }
  ]
}
```

현재 내장된 `rules`는 [여기](https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json)에서 찾을 수 있습니다.

아래는 몇 가지 중요한 필드를 설명합니다:

```typescript
export interface Rule {
  // 매칭 웹사이트
  id?: string; // 시스템의 각 적용 규칙은 고유한 id를 가지며, 사용자가 이 규칙을 재사용하고자 할 때는 해당 id를 자신의 규칙에 추가하여 재사용할 수 있습니다.
  matches?: string | string[]; // 이 Rule은 여기에 명시된 웹사이트에만 적용됩니다.
  excludeMatches?: string | string[]; // 특정 웹사이트를 제외합니다.
  selectorMatches?: string | string[]; // 모든 URL을 명시할 필요 없이 선택자로 매칭합니다.
  excludeSelectorMatches?: string | string[]; // 제외 규칙, 위와 동일합니다.

  // 번역 범위 지정
  selectors?: string | string[]; // 매칭된 요소만 번역합니다.
  excludeSelectors?: string | string[]; // 요소를 제외하고, 매칭된 요소는 번역하지 않습니다.
  excludeTags?: string | string[]; // Tags를 제외하고, 매칭된 Tag는 번역하지 않습니다.

  // 번역 범위 추가, 덮어쓰지 않음
  additionalSelectors?: string | string[]; // 번역 범위를 추가합니다. 지능형 번역 영역에 번역 위치를 추가합니다.
  additionalExcludeSelectors?: string | string[]; // 추가적으로 요소를 제외하여, 지능형 번역이 특정 위치를 번역하지 않도록 합니다.
  additionalExcludeTags?: string | string[]; // 추가적으로 Tags를 제외합니다.

  // 원본 유지
  stayOriginalSelectors?: string | string[]; // 매칭된 요소는 원본 상태를 유지합니다. 주로 포럼 웹사이트의 태그에 사용됩니다.
  stayOriginalTags?: string | string[]; // 매칭된 Tag는 원본 상태를 유지합니다. 예: `code`

  // 영역 번역
  atomicBlockSelectors?: string | string[]; // 영역 선택자, 매칭된 요소는 하나의 전체로 간주되며, 분할하여 번역하지 않습니다.

  atomicBlockTags?: string | string[]; // 영역 태그 선택자, 위와 동일

  // 블록 또는 인라인
  extraBlockSelectors?: string | string[]; // 추가 선택자, 일치하는 요소는 블록 요소로 처리되어 한 줄을 차지합니다.
  extraInlineSelectors?: string | string[]; // 추가 선택자, 일치하는 요소는 인라인 요소로 처리됩니다.

  inlineTags?: string | string[]; // 일치하는 태그는 인라인 요소로 처리됩니다.
  preWhitespaceDetectedTags?: string | string[]; // 일치하는 태그는 자동으로 줄바꿈 처리됩니다.

  // 번역문 스타일
  translationClasses?: string | string | string[]; // 번역문에 추가 클래스를 부여합니다.

  // 전역 스타일
  globalStyles?: Record<string, string>; // 페이지 스타일을 수정합니다. 번역문으로 인해 페이지가 깨질 경우 유용합니다.
  globalAttributes?: Record<string, Record<string, string>>; // 페이지 요소의 속성을 수정합니다.

  // 내장 스타일
  injectedCss?: string | string[]; // CSS 스타일을 내장합니다.
  additionalInjectedCss?: string | string[]; // CSS 스타일을 추가합니다. 기존의 것을 덮어쓰지 않습니다.

  // 컨텍스트
  wrapperPrefix?: string; // 번역문 영역의 접두사, 기본값은 smart로, 글자 수에 따라 줄바꿈 여부를 결정합니다.
  wrapperSuffix?: string; // 번역문 영역의 접미사

  // 번역문 줄바꿈 글자 수
  blockMinTextCount?: number; // 번역문을 블록으로 처리하는 최소 문자 수, 그렇지 않으면 인라인 요소로 처리됩니다.
  blockMinWordCount?: number; // 위와 동일. 항상 줄바꿈을 원한다면 0을 입력하세요.

  // 번역 가능한 최소 글자 수
  containerMinTextCount?: number; // 스마트 인식 시, 요소가 포함해야 하는 최소 문자 수로, 기본값은 18입니다.
  paragraphMinTextCount?: number; // 원문 단락의 최소 문자 수, 이 숫자보다 큰 내용은 번역됩니다.
  paragraphMinWordCount?: number; // 원문 단락의 최소 단어 수

  // 긴 단락 강제 줄바꿈 글자 수
  lineBreakMaxTextCount?: number; // 긴 단락 번역 시, 강제로 줄을 나누는 최대 문자 수입니다.

  // 번역 시작 타이밍
  urlChangeDelay?: number; // 페이지 진입 후, 몇 밀리초 후에 번역을 시작할지. 페이지 초기화를 기다리기 위함이며, 현재 기본값은 250ms입니다.
  observeUrlChange?: boolean; // URL 주소 변경을 감지하여 번역을 다시 시작할지 여부, 기본값은 true입니다.

  // 모바일
  isShowUserscriptPagePopup?: boolean; // 모바일 기기에서 페이지 내 팝업을 표시할지 여부, 기본값은 true입니다.
  fingerCountToToggleTranslagePageWhenTouching?: number; // 네 손가락 터치로 번역, 0, 2, 3, 4, 5로 설정 가능합니다.

  // AI 스트리밍 번역
  aiRule: {
    streamingSelector: string; // gpt 웹페이지에서 번역 중인 요소를 표시하는 선택자
    messageWrapperSelector: string; // 메시지 본문 선택자
    streamingChange: boolean; // gpt와 같은 웹페이지에서 메시지가 증분 업데이트인지 전체 업데이트인지. gpt는 증분입니다.
  };
}
```

## 고급 사용자 정의 옵션 실전

### 실용적인 팁

이 부분에서는 바로 사용할 수 있는 초보자용 설정을 소개합니다.

이 설정들을 한 번에 복사하여 [개발자 설정](https://dash.immersivetranslate.com/#developer)을 열고, `Edit Full User Config`를 펼친 후, 마지막 항목에 복사하면 됩니다. 이전 항목에 쉼표를 추가하는 것을 잊지 마시고, 마지막 항목에는 쉼표를 추가하지 않도록 주의하세요.

#### 사용할 수 없는 번역 서비스가 너무 많은데, 플러그인 패널에서 사용 가능한 번역 서비스만 표시하려면 어떻게 해야 하나요?

```json
  "showUnconfiguredTranslationServiceInPopup": false
```

#### 다양한 사이트가 기본적으로 다른 번역 서비스를 선택하도록 하는 방법은 무엇입니까? 예를 들어, 일부 웹사이트에서는 돈을 지불해야 하지만 더 나은 번역 효과를 원하고, 다른 웹사이트에서는 무료로 볼 수 있는 번역만 필요합니다.

주의해서 보세요, 이 설정은 번역 서비스에 관한 것으로, 구글 번역을 구성하여 관련 트위터 사이트의 번역은 모두 이를 사용하도록 했습니다. 구글 번역은 무료이며, 트위터는 서핑을 위한 것이므로, 이해할 수만 있다면 됩니다.

자세히 보면, `deepl` 번역 서비스도 구성되어 있는데, 오류율이 낮고 높은 정확성이 요구되는 학술 사이트인 `scihub`를 전문적으로 번역하도록 했습니다.

```json
  "translationServices": {
    "google": {
      "matches":["https://twitter.com"]
    },
    "deepl": {
      "matches":["https://www.sci-hub.se"]
    }
  }
```

> ⚠️ 주의하세요, 동일한 도메인의 모든 웹사이트를 번역하고자 할 경우, *.twitter.com 또는 https://twitter.com/을 단순 사용하는 것은 효과가 없습니다. 올바른 방법은 위에서 보여준 것과 같아야 합니다. 이는 *.twitter.com이 xxx.twitter.com과 같은 하위 도메인에만 일치하고 최상위 도메인 자체는 포함하지 않기 때문입니다.

### 웹사이트 적응 사례

이 부분에서는 일부 플러그인이 일반적인 웹사이트에 대해 자체적으로 정의한 `rules`를 소개하고, 실제 예시를 통해 고급 사용자 정의 옵션을 이해합니다. 동시에 간결함을 위해, 여기서는 `selectors`, `excludeSelectors` 등 가장 자주 사용되는 필드만을 소개할 것입니다. 이 부분에 관심이 있다면, 저희에게 연락 주시기 바랍니다. 관련 내용을 계속 업데이트할 예정입니다.

소개하기 전에, 매우 중요한 것이 바로 몰입형 번역 플러그인의 작동 원리입니다. 이는 또한 플러그인의 작동 원리이기도 합니다. 이전에는 `HTML`, `CSS`, `JavaScript`의 기본 지식이 필요합니다. 관련 기초는 `MDN` 웹사이트에서 학습할 수 있습니다. 좋습니다, 말을 더하지 않고, 우리가 몰입형 번역의 내부를 살펴보도록 합시다. 플러그인의 작동 메커니즘을 간단히 말하자면, 웹 페이지에 제3자 스크립트를 주입하는 것입니다. 이 스크립트는 웹 페이지의 구조, 스타일, 심지어 행동에 대해 상당히 자유롭게 변경할 수 있습니다.

우리의 몰입형 번역 플러그인도 예외는 아닙니다. 몰입형 번역이 무엇을 하는지 간단히 분석해 보겠습니다.

- 번역할 요소 집합을 가져옵니다.
- 요소 집합 내의 텍스트를 번역합니다.
- 번역 결과를 요소 집합에 삽입합니다.

좋습니다, 하지만 좀 더 심층적으로 생각해보면, 자연스럽게 다음 두 가지 문제가 생깁니다.

- 번역이 필요한 요소를 어떻게 결정할 것인가? 전체를 번역하면 사용자의 몰입 경험을 해칠 수 있습니다. 예를 들어, 간단하고 명확한 버튼이나 네비게이션 바 같은 경우입니다.
- 번역 결과를 요소 집합에 삽입하는 것은 원본 웹 페이지의 스타일에 영향을 주지 않으면서, 삽입된 결과가 원본 웹 페이지와 일치하도록 하는 새로운 도전을 가져옵니다.

우리의 `Rules`의 핵심은 위에서 언급한 두 가지 문제를 해결하는 것입니다. 몰입형 번역 플러그인은 시장에 나와 있는 모든 웹 페이지를 대상으로 하기 때문에, 수십만, 심지어 수백만 개의 웹 페이지를 다루게 됩니다. 이러한 웹 페이지들은 페이지 구조와 사용된 기술이 매우 다양합니다. 웹 페이지의 차이로 인해, 모든 웹 사이트 콘텐츠에 적합한 일반적인 로직을 찾는 것은 거의 불가능합니다. 따라서, 각 웹 사이트를 개별적으로 적응하는 것 외에는 해결책이 없어 보입니다. 그런 다음 적응 작업을 더 쉽게 하기 위해, 코드로서의 설정(config-as-code)이라는 개념을 활용하여, 적응 작업을 설정 필드 작업으로 전환했습니다. 이러한 방식의 또 다른 장점은 사용자가 적응 작업에 참여할 수 있다는 것입니다.

동시에, 설정을 할 때는 아래 몇 가지 필드를 직접 사용하는 것이 좋지 않습니다. 이는 기존의 설정 항목을 덮어쓸 수 있기 때문입니다. 대신 `selector.add`, `excludeSelector.add`와 같은 필드를 사용하여 기존 설정 항목에 대한 수정을 상속 방식으로 진행하는 것이 좋습니다.

이제, 몰입형 번역이 사이트에 대한 적응 작업을 소개할 것입니다.

아래는 트위터의 Rules입니다. 간결함을 위해 몇 가지 핵심 필드에만 초점을 맞출 것이며, 나머지 필드는 위에서 언급한 `Rules`와 함께 이해할 수 있습니다.

```json
[
  {
    "id": "twitter",
    "matches": [
      "twitter.com",
      "mobile.twitter.com",
      "tweetdeck.twitter.com",
```

```json
{
  "pro.twitter.com",
  "https://platform.twitter.com/embed*"
],
"selectors": [
  // 번역할 요소를 지정하며, 선택자가 일치하는 요소만 번역됩니다.
  "[data-testid='tweetText']",
  ".tweet-text",
  ".js-quoted-tweet-text",
  "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)",
  "[data-testid='developerBuiltCardContainer'] > div:nth-child(2)",
  "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)",
  "[data-testid='cellInnerDiv'] div[data-testid='UserCell'] > div> div:nth-child(2)",
  "[data-testid='UserDescription']",
  "[data-testid='HoverCard'] div[dir=auto]",
  "[data-testid='HoverCard'] span[dir=auto]",
  "[data-testid='HoverCard'] [role='dialog'] div[dir=ltr]",
  "[data-testid='birdwatch-pivot'] div[dir=ltr]"
],
"excludeSelectors": [
  // CSS 선택자로 선택된 요소를 번역하지 않습니다.
  "[aria-describedby][role=button]",
  "header",
  "[data-testid='radioGroupplayback_rate'] div",
  "[data-testid='userFollowIndicator']",
  "[class='css-901oao r-14j79pv r-37j5jr r-n6v787 r-16dba41 r-1cwl3u0 r-bcqeeo r-qvutc0']",
  "[class='css-175oi2r r-1wbh5a2 r-dnmrzs']"
],
"globalStyles": {
  // 전역 스타일, 원래 스타일을 강제로 덮어씁니다.
  "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
  "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
  "[data-testid='tweetText']": "-webkit-line-clamp: unset;"
}
}
```

```
- `selector`: 번역할 요소 집합을 지정합니다.

  이 필드가 필요한 이유

  - 모든 요소에 텍스트가 있고 번역이 필요한 것은 아니기 때문에, 이러한 필드를 제공하면 성능을 보장하면서도 사용자의 몰입 경험을 보장할 수 있습니다.

  예를 들어

  - 트위터에서 `selector`를 지정하지 않으면, 페이지 내의 모든 영어 텍스트를 번역하려고 시도할 것입니다. 아래 이미지처럼, 사용자의 닉네임은 번역할 필요가 없습니다.

  ![사용자 홈페이지](https://s.immersivetranslate.com/assets/siteDocs/twitterUser.png)

  필드 의미

  - ```
      "selectors": [ // 번역될 CSS 선택자 집합
      "[data-testid=\"tweetText\"]",
    ]
    ```

  이 배열의 각 항목은 페이지 내에서 번역이 필요한 요소를 선택하는 CSS 선택자입니다. 여기서 첫 번째 선택자를 예로 들면, 아래 이미지와 같이 모든 트윗 요소를 대상으로 합니다.

  ![트윗](https://s.immersivetranslate.com/assets/siteDocs/tweet.png)

- `excludeSelectors`: 번역되지 않을 요소 집합

  이 필드가 필요한 이유

  - 단순히 번역할 선택자만으로는 부족하며, 선택된 요소 중에서 번역이 필요 없는 요소가 있을 수 있으므로, 이를 제외하기 위한 필드가 필요합니다.
  - 페이지 구조가 매우 복잡하기 때문에, 이 두 가지 설정을 제공하여 설정을 더 유연하게 만듭니다.
  - 관련 우선순위는 동일한 선택자에 대해, selectors > excludeSelectors이며, 나머지는 CSS 우선순위에 따라 결정됩니다.

  필드 의미

  - ```
      "excludeSelectors": [ // 번역되지 않을 CSS 선택자로 선택된 요소
      "[aria-describedby][role=button]",
    ],
    ```

  여기서 첫 번째를 보면, 팔로우 버튼의 번역을 제외했습니다.
  ![트위터 팔로우](https://s.immersivetranslate.com/assets/siteDocs/twitter-follow.png)

- `globalStyles`: 전역 스타일을 추가하여 기존 스타일을 강제로 덮어씁니다.

  이 필드가 필요한 이유

  - 특정 상황에서 원래 웹페이지의 관련 CSS 스타일로 인해 전체 번역 표시 효과가 좋지 않아, 잘림, 줄 바꿈이 되지 않는 등의 효과가 발생할 수 있습니다.
  - 이 필드를 통해 원본 웹 페이지의 CSS 속성을 직접 수정하여 해결하는 강력한 해결책을 제공합니다.

  필드 의미

  - ```
        "globalStyles": {
      // 전역 스타일, 원본 스타일을 강제로 덮어씁니다.
      "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='tweetText']": "-webkit-line-clamp: unset;"
    }
    ```

  `-webkit-line-clamp` 속성은 표시되는 행 수를 제어하며, 초과하는 행은 잘립니다. 여기서 `unset`으로 설정하면, 이 속성에 의해 번역문이 잘리는 것을 방지할 수 있습니다.
```

### 사용자 정의 웹사이트 적응

적응 규칙에 관해서, 당신은 물론 사용자 정의 규칙을 설정할 수 있습니다. 플러그인 옵션 페이지로 들어가서 [개발자 설정](https://dash.immersivetranslate.com/#developer)을 클릭하고, `Edit User Rules`를 펼쳐서 여기에서 각각의 웹사이트에 대한 사용자 정의 적응을 진행할 수 있습니다. 아래에서는 실제 규칙을 결합하여 설명합니다.

```
[
  {
    "selectors.remove": [
      "[data-testid=\"tweetText\"]"
    ],
    "selectors.add": [
      ""
    ],
    "excludeSelectors.add":[
      ""
    ],
    "excludeSelectors.remove":[
      ""
    ],
    "id": "twitter"
  }
]
```

이 규칙은 트위터 페이지의 트윗을 번역하지 않도록 합니다. 아래에서는 필드의 의미를 자세히 소개합니다.

`id`는 현재 잠수식 번역에서 이미 정의된 관련 웹사이트의 집합이며, 각 `id`는 관련 사이트에 해당합니다. `id`의 이점은 두 가지가 있습니다.

- `id`를 사용하면 잠수식 번역의 이전 적응 규칙을 상속받을 수 있으며, 사용자는 이를 기반으로 추가하거나 삭제할 수 있습니다.
- `id`를 사용하면 번거로운 매칭 필드를 작성할 필요가 없습니다.

아래는 잠수식 번역 내장 서비스의 일반적인 `id`를 소개합니다.

- `"isEbook"` epub 리더 페이지의 설정
- `"isEbookBuilder"` epub 이중 언어 책 생성 페이지의 설정
- `"pdf"` pdf 이중 언어 대조 번역 페이지의 설정

전체 `id` 집합은 [개발자 설정](https://dash.immersivetranslate.com/#developer)에서, `Click to expand the final config`에서 찾을 수 있습니다.

`selectors`는 번역할 CSS 선택자를 지정하는 데 사용되며, 기존 기반 위에 추가하거나 삭제하기 위해 하위 항목 `.add` `.remove`를 사용하는 것이 좋습니다.

`excludeSelectors`는 번역하지 않을 CSS 선택자를 제외하는 데 사용되며, 기존 기반 위에 추가하거나 삭제하기 위해 하위 항목 `.add` `.remove`를 사용하는 것이 좋습니다.

**더 많은 설명**

Block과 inline의 차이점, 더 많은 것을 알고 싶다면 [여기](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements#inline)를 참조하세요.

- block 요소는 한 줄을 독차지하며, 여러 개의 인접한 block 요소는 각각 새로운 줄에서 시작됩니다.
- inline 요소는 한 줄을 독차지하지 않으며, 여러 개의 인접한 inline 요소는 같은 줄에 배열되며, 한 줄에 배열할 수 없을 때만 새로운 줄로 넘어갑니다.