---
sidebar_position: 4
---

# 고급 사용자 정의 옵션

이 페이지는 HTML/CSS/JSON에 어느 정도 익숙한 고급 사용자를 위한 안내입니다. 고급 설정을 활용하면 적응력을 크게 높일 수 있지만, "겉보기엔 맞는 것 같으나 실제로는 반영되지 않는" 구성을 작성할 가능성도 커지므로, 설정 변경 전 반드시 백업을 권장합니다.

## 사용 전 안내

- 진입점: [개발자 설정](https://dash.immersivetranslate.com/#developer)
- User Config / User Rules 를 편집하기 전 백업하세요. 포맷 오류로 인해 설정이 무시될 수 있습니다.
- 최종 내장 구성은 "Click to expand the final config" 기준으로 확인하세요 (필드, 기본값, 사용 가능한 서비스 등).

## 진입점과 우선순위

주요 진입점 (개발자 설정):
- Edit Full User Config: `rules`, 번역 서비스, 스타일 등 전체 설정
- Edit User Rules: `rules` 배열만 수정 (`{ "rules": [...] }` 형태로 감싸지 마세요. 배열만 입력)
- Injected CSS: 전체 CSS 추가

우선순위 (높음 → 낮음): 조건에 부합하는 `rules` > `generalRule` > 내장 기본 설정  
특정 `rule`이 적용되면, `generalRule`과 병합되어 해당 `rule`의 필드가 우선합니다.

## 빠른 시작 (가장 흔한 요구)

### 1) 특정 사이트의 본문만 번역하기

```json
{
  "rules": [
    {
      "matches": ["example.com"],
      "selectors": ["article", ".post-content"],
      "excludeSelectors": ["nav", "footer", ".comment"]
    }
  ]
}
```

### 2) 항상 번역 / 아예 번역 안 함

```json
{
  "translationUrlPattern": {
    "matches": ["stackoverflow.com"],
    "excludeMatches": ["www.google.com/mail/*"]
  }
}
```

### 3) 사이트별로 번역 엔진 다르게 사용하기

```json
{
  "translationService": "google",
  "translationServices": {
    "deepl": {
      "matches": ["sci-hub.se"]
    }
  }
}
```

### 4) 사이트별 번역 결과 스타일 지정

```json
{
  "translationTheme": "none",
  "translationThemePatterns": {
    "underline": {
      "matches": ["discord.com"]
    }
  }
}
```

### 5) 번역으로 인해 스타일이 이상해졌을 때 스타일 수정

```json
{
  "rules": [
    {
      "matches": ["youtube.com"],
      "globalStyles": {
        "#video-title": "max-height:unset;"
      }
    }
  ]
}
```

### 6) 미설정된 번역 서비스를 메뉴에 표시하지 않음

```json
{
  "showUnconfiguredTranslationServiceInPopup": false
}
```

## 규칙과 매칭

### 규칙 병합

- `generalRule`: 모든 사이트에 통용되는 기본 규칙
- `rules`: 사이트별 규칙. 조건 만족 시 최우선 적용

`rules` 내에서 `generalRule` 대부분의 필드를 활용 가능합니다.

### matches 의 일반적인 형태

`matches`는 문자열 또는 배열 지원:
- 도메인: `example.com`
- 전체 URL: `https://example.com/path/`
- 와일드카드: `https://*/*q=*`
- 전체매칭: `*` / `*://*` / `*://*/*`
- 로컬 파일: `file://*`

주의: `*.twitter.com`은 하위 도메인만 포함하며, `twitter.com` 루트는 미포함입니다.

### selectors / excludeSelectors

- `selectors`: 지정 요소만 번역 (기본 범위 덮어씀)
- `excludeSelectors`: 지정 요소는 번역에서 제외

기본 범위에 추가/제거만 하고 싶다면 `.add`/`.remove` 사용 권장 (다음 항목 참고)

### 상속과 증분 수정 (.add / .remove)

배열/객체 필드는 `.add`/`.remove` 형태로 증분 수정이 지원됩니다.  
기본 규칙 덮어쓰기를 피하려면 권장 방법입니다.

```json
[
  {
    "id": "twitter",
    "selectors.add": ["[data-testid='tweetText'] a"],
    "excludeSelectors.add": ["header"]
  }
]
```

### 주요 필드 (발췌)

매칭 관련:
- `matches` / `excludeMatches`
- `selectorMatches` / `excludeSelectorMatches`

번역 범위:
- `selectors` / `excludeSelectors` / `excludeTags`
- `stayOriginalSelectors` / `stayOriginalTags`
- `extraInlineSelectors` / `extraBlockSelectors`

스타일 및 레이아웃:
- `translationClasses`: 번역에 추가 클래스 설정
- `globalStyles` / `globalAttributes`
- `injectedCss` / `additionalInjectedCss`
- `wrapperPrefix` / `wrapperSuffix`
- `blockMinTextCount` / `blockMinWordCount`

타이밍과 모바일:
- `urlChangeDelay` / `observeUrlChange`
- `isShowUserscriptPagePopup`

### GPT 류 스트리밍 채팅 번역

```json
{
  "matches": ["chat.openai.com"],
  "excludeSelectors": [".markdown *"],
  "aiRule": {
    "streamingSelector": ".result-streaming.markdown",
    "messageWrapperSelector": ".markdown",
    "streamingChange": true
  }
}
```

필드별 더 자세한 설명은 마지막 "부록: Rule 필드 참고" 참고

## matches 매칭 로직 (간단 설명)

- 순수 도메인 (`*` 또는 경로 없음): hostname 기준 비교
- 전체 URL(`*` 없음): 프로토콜 + 호스트 + 포트 + 경로 일치 시 매칭
- `*` 포함 또는 프로토콜 생략: 와일드카드 규칙 적용 (기본적으로 http/https/file 지원)

자주 쓰는 예시:
- `twitter.com` → `https://twitter.com/home` 매칭 O
- `*.twitter.com` → `https://mobile.twitter.com` 매칭 O, `https://twitter.com` 매칭 X
- `https://twitter.com/home` → 해당 경로만 일치
- `twitter.com/*` → `twitter.com` 하위 전체

## 사이트 적용 예시 (Twitter)

아래는 Twitter 내장 규칙 (발췌) 이며, `selectors` / `excludeSelectors` / `globalStyles` 전형적 활용법입니다.

```json
[
  {
    "id": "twitter",
    "matches": [
      "twitter.com",
      "mobile.twitter.com",
      "tweetdeck.twitter.com",
      "pro.twitter.com",
      "https://platform.twitter.com/embed*"
    ],
    "selectors": [
      "[data-testid=\"tweetText\"]",
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
      "[aria-describedby][role=button]",
      "header",
      "[data-testid='radioGroupplayback_rate'] div",
      "[data-testid='userFollowIndicator']",
      "[class='css-901oao r-14j79pv r-37j5jr r-n6v787 r-16dba41 r-1cwl3u0 r-bcqeeo r-qvutc0']",
      "[class='css-175oi2r r-1wbh5a2 r-dnmrzs']"
    ],
    "globalStyles": {
      "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='tweetText']": "-webkit-line-clamp: unset;"
    }
  }
]
```

- `selectors`: 트윗 본문 등 중심 내용만 번역, 닉네임/버튼 등은 번역 X  
  ![tweet](https://s.immersivetranslate.com/assets/r2-uploads/tweet.png)
- `excludeSelectors`: 버튼·네비게이션 등 인터랙션 요소 번역 미적용  
  ![twitter-follow](https://s.immersivetranslate.com/assets/r2-uploads/twitter-follow.png)
- `globalStyles`: 줄수 제한 해제, 번역이 잘리는 현상 방지  
  ![用户主页](https://s.immersivetranslate.com/assets/r2-uploads/twitterUser.png)

## 사용자 정의 사이트 적용

`id`로 내장 규칙을 상속하고, `.add`/`.remove`로 증분 수정 가능

```json
[
  {
    "id": "twitter",
    "selectors.remove": ["[data-testid=\"tweetText\"]"],
    "selectors.add": ["[data-testid=\"tweetText\"] a"],
    "excludeSelectors.add": ["header"],
    "excludeSelectors.remove": []
  }
]
```

설명:
- `id`로 내장 규칙을 상속하여 불필요한 `matches` 작성 불필요
- `.add`/`.remove`로 배열 필드 증분 수정, 적극 권장됨

주요 내장 `id`(발췌)
- `isEbook`: epub 리더 페이지
- `isEbookBuilder`: epub 번역본 생성 페이지
- `pdf`: PDF 번역 대조 페이지

전체 내장 규칙:
- `https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json`

## 번역 서비스 설정

- `translationService`: 기본 번역 엔진
- `translationServices`: 서비스 설정 및 사이트별 덮어쓰기
- `showUnconfiguredTranslationServiceInPopup`: 미설정 서비스 숨김

예시 (텐센트 번역):

```json
{
  "translationService": "tencent",
  "translationServices": {
    "tencent": {
      "secretId": "xxx",
      "secretKey": "xxx",
      "matches": ["twitter.com"],
      "limit": 3,
      "maxTextGroupLengthPerRequest": 25,
      "maxTextLengthPerRequest": 1800,
      "apiUrl": ""
    }
  }
}
```

설명:
- `matches`: 해당 서비스가 적용될 사이트 지정
- `limit`: 서비스별 초당 최대 요청수 제한
- `maxTextGroupLengthPerRequest` / `maxTextLengthPerRequest`: 1 회 요청 규모 제한
- `apiUrl`: 엔드포인트 수동 지정 가능

### 요청 타임아웃 설정 (최대 대기시간)

서비스별로 요청 타임아웃 (ms 단위) 설정 가능. Pro 서비스는 `proRequestTimeout` 개별 적용

```json
{
  "translationServices": {
    "openai": {
      "requestTimeout": 60000
    },
    "gemini": {
      "proRequestTimeout": 90000
    }
  }
}
```

참고:
- 너무 길면 번역 대기 시간 증가, 짧으면 자주 실패 가능
- 서비스별 기본값은 다르며 최종 구성 참고
- `proRequestTimeout`은 `provider`가 `pro`일 때만 반영 (유료 서비스)

## 언어 및 번역 전략

### 항상 번역 / 번역 금지 언어 설정

```json
{
  "translationLanguagePattern": {
    "matches": ["en"],
    "excludeMatches": ["zh"]
  }
}
```

### 특정 사이트에 소스 언어 지정

```json
{
  "sourceLanguageUrlPattern": {
    "en": {
      "matches": ["*.google.com"]
    }
  }
}
```

## 기타 자주 쓰이는 글로벌 설정

### 번역문에서 HTML 태그 렌더링 허용

번역 결과에 HTML 태그가 포함되어야 할 때 사용

```json
{
  "enableRenderHtmlTag": true
}
```

## 번역 스타일 및 테마

`translationTheme`에서 지원하는 스타일 (최종 구성 기준):

```text
none, grey, dashed, dashedBorder, solidBorder, dotted, underline, mask, opacity,
paper, dividingLine, highlight, marker, marker2, blockquote, weakening, italic,
bold, thinDashed, nativeDotted, wavy, nativeDashed, nativeUnderline, background
```

사이트별 테마 지정 예시:

```json
{
  "translationThemePatterns": {
    "highlight": {
      "matches": ["discord.com"]
    }
  }
}
```

## AI / 고급 서비스 파라미터

### temperature

```json
{
  "translationServices": {
    "openai": {
      "temperature": 0.2
    }
  }
}
```

### 사용자 정의 요청 헤더·바디

```json
{
  "translationServices": {
    "claude": {
      "headerConfigs": {
        "anthropic-version": "2023-06-01",
        "anthropic-dangerous-direct-browser-access": "true"
      },
      "bodyConfigs": {
        "max_tokens": 2048
      }
    }
  }
}
```

### Gemini 계열 모델 사용자 정의 설정

Gemini 계열은 기본 설정이 내장되어 있으므로, 덮어쓰기 시 `modelsOverrides`를 권장

```json
{
  "translationServices": {
    "gemini": {
      "modelsOverrides": [
        {
          "models": ["gemini-2.5-flash", "gemini-2.5-flash-lite"],
          "bodyConfigs": {
            "temperature": 0.1
          }
        }
      ]
    }
  }
}
```

참고: `modelsOverrides`는 다른 AI 서비스에도 적용 가능. 모델명 기준으로 해당 설정이 덮어써집니다.

### 사용자 정의 프롬프트 완전 준수

> 대형 언어 모델의 "환각 (hallucination)" 문제를 줄이기 위해, 플러그인은 번역 품질 검증 로직을 내장하고 있습니다. 요청과 응답의 Token 수 비율이 정상인지 자동 판별하여 비정상 (너무 높거나 낮은 경우) 시 해당 결과 무효화 및 대체 서비스로 전환됩니다.  
> 프롬프트가 단순 번역이 아닌 확장/교정 등이라면 Token 비율이 기준 미달일 수 있으므로, 이 때 "strictPrompt" 모드를 켜면 검증을 생략합니다.

```json
{
  "translationServices": {
    "claude": {
      "strictPrompt": true
    }
  }
}
```

### 다국어 프롬프트 커스텀 (부분 예시)

```json
{
  "translationServices": {
    "openai": {
      "langOverrides": [
        {
          "id": "auto2ja",
          "systemPrompt": "あなたはプロの翻訳エンジンです。",
          "prompt": "次のテキストを{{to}}に翻訳してください：\n\n<text>\n{{text}}\n</text>",
          "multiplePrompt": "<yaml>\n{{yaml}}\n</yaml>",
          "subtitlePrompt": "<yaml_subtitles>\n{{yaml}}\n</yaml_subtitles>"
        }
      ]
    }
  }
}
```

## 용어집 & 기계 번역

최신 [AI 용어집](https://dash.immersivetranslate.com/#terms) 기능은 AI 번역 엔진에 한해 적용됩니다.

기계 번역은 기본적으로 용어집 미적용 (플레이스홀더 치환 방식으로 품질 저하 우려), 반드시 필요할 시 강제 활성화 가능 (비권장):

```json
{
  "enableMachineTranslateTerms": true
}
```

## 캐시 자동 정리 주기

기본적으로 30 일마다 번역 캐시가 자동 삭제되어 성능 저하를 예방합니다.

```json
{
  "cacheMaxAgeDay": 30
}
```

## Injected CSS 와 globalStyles 의 차이

- Injected CSS: 전체 페이지 단위로 CSS 일괄 추가 (사이트 일괄 수정에 적합)
- globalStyles: 규칙 단위 스타일 덮어쓰기 (사이트별 부분 수정에 적합)

Injected CSS 예시:

```css
.immersive-translate-target-wrapper img {
  width: 16px;
  height: 16px;
}
```

## 디버깅 및 흔한 실수

- `*.twitter.com`은 루트 도메인에 적용 안 됨 → `twitter.com`도 꼭 함께 작성
- `selectors` 사용 시 기본 번역 범위가 덮어써짐 → 증분 변경은 `.add`/`.remove` 사용 우선
- `matches`에 `example.com/path`처럼 경로 입력 시, 와일드카드 적용됨 (정확한 패턴인지 확인)
- 반영이 안 될 때: 최종 구성 결과 확인 → 새로고침
- JSON 의 마지막 콤마 (,) 는 오류 원인!

## 부록: Rule 필드 참고

아래는 Rule 인터페이스 필드 (문서 버전) 이며, 자주 쓰는 속성을 위주로 정리.  
전체/최신 필드는 실제 설정에서 최종 참고 바랍니다.  
배열·객체 필드는 `.add`/`.remove` 증분 수정으로 덮어쓰기 방지 가능!

```typescript
export interface Rule {
  // 사이트 매칭
  id?: string; // 내장 규칙 ID, 내장 규칙 상속 시
  matches?: string | string[]; // 해당 Rule 이 적용될 사이트
  excludeMatches?: string | string[]; // 제외할 사이트
  selectorMatches?: string | string[]; // URL 없이 셀렉터로 직접 매칭
  excludeSelectorMatches?: string | string[]; // 셀렉터 매칭 제외 규칙

  // 번역 범위 지정
  selectors?: string | string[]; // 지정 요소만 번역
  excludeSelectors?: string | string[]; // 지정 요소 번역 제외
  excludeTags?: string | string[]; // 해당 태그 번역 제외

  // 번역 범위 추가 (실패 시 selectors.add / selectors.remove 사용)
  additionalSelectors?: string | string[]; // 번역 범위 추가
  additionalExcludeSelectors?: string | string[]; // 번역 제외 추가
  additionalExcludeTags?: string | string[]; // 태그 제외 추가 (일부 버전에서 미지원)

  // 원본 유지
  stayOriginalSelectors?: string | string[]; // 해당 요소는 원본 노출
  stayOriginalTags?: string | string[]; // 해당 태그 원본 유지 (예: code)

  // Block 또는 Inline
  extraBlockSelectors?: string | string[]; // 블록으로 간주할 셀렉터
  extraInlineSelectors?: string | string[]; // 인라인 요소로 간주할 셀렉터
  inlineTags?: string | string[]; // 인라인태그 지정
  preWhitespaceDetectedTags?: string | string[]; // 줄바꿈 자동 감지 태그

  // 번역문 스타일
  translationClasses?: string | string[]; // 번역문에 추가할 클래스

  // 전역 스타일
  globalStyles?: Record<string, string>; // 페이지 스타일 수정
  globalAttributes?: Record<string, Record<string, string | null>>; // 요소 속성값 수정

  // CSS 임베드
  injectedCss?: string | string[]; // CSS 임베드
  additionalInjectedCss?: string | string[]; // 추가 CSS

  // 컨텍스트
  wrapperPrefix?: string; // 번역 부분 앞에 붙는 텍스트/HTML
  wrapperSuffix?: string; // 번역 부분 뒤에 붙는 텍스트/HTML

  // 번역문 줄바꿈 기준
  blockMinTextCount?: number; // 블록 단위 최소 글자수
  blockMinWordCount?: number; // 블록 단위 최소 단어수

  // 번역 대상 최소 글자수
  containerMinTextCount?: number; // 요소 최소 글자수
  paragraphMinTextCount?: number; // 단락 최소 글자수
  paragraphMinWordCount?: number; // 단락 최소 단어수

  // 장문 강제 줄바꿈 글자수
  lineBreakMaxTextCount?: number; // 단락 최대 글자수

  // 번역 시작 시점
  urlChangeDelay?: number; // 페이지 진입 후 번역 지연 (ms)
  observeUrlChange?: boolean; // URL 변경 시 재번역

  // 모바일
  isShowUserscriptPagePopup?: boolean; // 모바일에서 번역 팝업 표시
  fingerCountToToggleTranslagePageWhenTouching?: number; // 지원 중단됨

  // AI 스트리밍 번역
  aiRule?: {
    streamingSelector: string; // 번역 중인 요소 셀렉터
    messageWrapperSelector: string; // 메시지 내용 셀렉터
    streamingChange: boolean; // 점진 갱신 여부
  };
}
```
