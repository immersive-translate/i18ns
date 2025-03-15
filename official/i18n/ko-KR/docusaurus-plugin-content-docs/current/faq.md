---
sidebar_position: 9
---

# FAQ

### 1. Android App, floating ball disappeared

이전 버전의 애드온이 비활성화되었습니다. [공식 웹사이트](https://immersivetranslate.com/)에서 최신 버전을 설치하세요.

## Youtube, Facebook 같은 웹사이트의 주요 콘텐츠는 번역되지만 일부 사이드바는 번역되지 않습니다. 모든 것을 번역하고 싶습니다.

페이지 가독성을 위해 몰입형 번역은 기본적으로 주요 콘텐츠 영역만 번역합니다. 모든 것을 번역하려면,

플로팅 볼 패널을 엽니다 (모바일에서 길게 누름) -> 오른쪽 하단의 더보기를 클릭 -> 모든 영역 선택

## 모바일에서 Youtube (또는 기타) 앱에 플로팅 버블이 표시되지 않음

브라우저 플러그인은 브라우저에서만 실행되며 다른 앱에서는 사용할 수 없습니다.

- iOS 브라우저에서 YouTube를 클릭하면 앱이 직접 열립니다.

  YouTube 링크를 길게 눌러 플로팅 창을 띄우고 웹페이지에서 열기를 선택하세요.

## 자동 번역을 끄는 방법

- 팝업 패널 또는 설정 페이지에서 취소합니다.

<img src="https://s.immersivetranslate.com/assets/turn_off_automatic_translation_en.jpeg" alt="turn off automatic translation" width="250" />

<!-- - 또는 설정 페이지를 통해 변경：

![](https://github.com/immersive-translate/immersive-translate/assets/62473795/d33ac7c0-a47b-4901-b5f6-c6a991164dc0) -->

## 현재 페이지를 번역할 권한이 없습니다

- 브라우저 기본 페이지 (주소 표시줄에 주소 없음)
- 타사 플러그인 페이지
- Google 플러그인이 Google 스토어 페이지를 비활성화

## 원본 텍스트를 표시하지 않으려면 어떻게 해야 하나요?

Immersive Translate 아이콘을 탭하여 확장 패널을 열고, [더보기], [번역 전용 모드로 전환]을 탭하세요.

## 페이지에 느낌표가 나타남

페이지에 느낌표가 나타나면 번역 서비스에 문제가 발생하여 오류가 반환되었음을 나타냅니다. 느낌표 위로 마우스를 이동하여 구체적인 오류를 확인할 수 있습니다.

### 429 Error

이것은 가장 일반적인 오류 중 하나로, 429는 요청 빈도가 너무 빠르다는 것을 나타냅니다. 웹 페이지 번역에는 번역해야 할 문단이 매우 많으며, 문단 병합, 빈도 제어 등 최적화를 많이 했지만, 때때로 번역 서비스가 과부하되어 429 빈도 제한 오류가 반환됩니다. 이 경우 일반적으로 다른 번역 서비스로 일시적으로 전환하거나 잠시 기다렸다가 다시 시도할 수 있습니다.

Google 서비스를 사용 중일 때 429 오류가 발생하면 일반적으로 Google이 노드에 대해 트래픽 제한을 하는 경우이며, 노드를 전환하는 것이 좋습니다.

## 로컬 문서 번역

로컬 HTML 파일, txt 파일 또는 PDF 파일을 번역해야 하는 경우 Immersive Translate 확장 아이콘을 클릭한 다음 [더보기]를 클릭하고 [PDF 파일 번역] 또는 [HTML/txt 파일 번역]을 클릭하여 로컬 파일을 번역할 수 있습니다.

Chrome, Arc, Edge 브라우저와 같은 Chrome 유사 브라우저를 사용하는 경우, 브라우저 확장 관리 페이지 `chrome://extensions`를 열고 [Immersive Translate] 플러그인을 찾아 [로컬 파일에 대한 확장 액세스 허용]을 선택한 다음 브라우저에서 로컬 HTML 또는 로컬 PDF 파일을 열어 직접 오른쪽 클릭하여 [번역]할 수 있습니다.

## 확장을 업데이트하는 방법

일반적으로 브라우저 스토어에 설치된 확장은 브라우저가 자동으로 업데이트하며, 일반적으로 확장 업데이트 후 하루 이내에 자동으로 업데이트됩니다. 최신 버전으로 즉시 업데이트하려면 브라우저의 [확장 관리] 페이지에서 [개발자 모드]를 열고 상단의 [업데이트]를 클릭하여 스토어의 최신 버전으로 즉시 업데이트할 수 있습니다.

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/update-extension.png)

## Youtube 자막 설정 스타일

YouTube의 자체 자막 설정에서 [옵션]을 클릭하여 크기, 색상 등을 조정할 수 있습니다.

![](https://s.immersivetranslate.com/assets/youtube_subtitle_options2_en.jpeg)

## Immersive Translate Tampermonkey 지원 브라우저

데스크톱의 Chrome, Firefox에 추천되는 Grease Monkey 확장:

- [Tamper Monkey](https://www.tampermonkey.net/)

Safari에 추천되는 Grease Monkey 확장:

- [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)

<!-- > Safari에서 [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171)를 사용하는 경우, Stay의 자체 스토어에서 직접 다운로드할 수 있는 Immersive Translate 최적화 스크립트를 검색하세요 (Stay에 최적화됨) -->

Android에 추천되는 Grease Monkey 확장:

1. [Firefox 최신 버전](https://www.mozilla.org/firefox/browsers/mobile/android/)을 사용하여 [Tamper Monkey](https://www.tampermonkey.net/) 확장을 설치할 수 있습니다.

<!-- 2. [X Browser](https://www.xbext.com/?ref=immersive-translate)를 직접 사용하여 설치 후 [Immersive Translate Tampermonkey 주소](https://download.immersivetranslate.com/immersive-translate.user.js)를 열어 설치할 수 있습니다! -->

<!-- 지원되지 않는 Grease Monkey 확장：

- Android Via Browser
- iOS Alook Browser -->

(이러한 브라우저는 필요한 Grease Monkey API를 구현하지 않기 때문입니다)

## Google Translate 인터페이스 차단 문제

`translate.googleapis.com` 도메인 이름을 프록시 규칙에 추가하세요.

## 최신 규칙을 업데이트하는 방법

확장 자체는 사용 중에 최신 공식 웹사이트 적응 규칙과 정기적으로 동기화됩니다. 브라우저의 Immersive Translate 확장 아이콘을 클릭하여 팝업 창을 열면 확장이 최신 적응 규칙을 자동으로 감지하고 동기화합니다. Tampermonkey도 마찬가지입니다.

## 웹페이지 번역에 문제가 있을 때 웹페이지 피드백을 저장하는 방법

웹 페이지에서 "다른 이름으로 저장"을 오른쪽 클릭하거나 ctrl+s 단축키를 사용하여 저장 옵션으로 단일 파일을 선택하고, 파일 형식이 .mht/.mhtml인지 확인합니다. 그런 다음 파일을 support@immersivetranslate.com으로 보내세요.

<!-- ![save mht](https://s.immersivetranslate.com/static/official-static/assets/save_mht.png) -->

## Color Cloud 번역 오류

"지원되지 않는 trans_type"이라는 오류 메시지가 표시됩니다. 지정된 언어를 통해 자동으로 감지할 언어를 선택할 수 있습니다.

## WeChat Reading 번역 불가

WeChat Reading은 타사 수단을 통해 콘텐츠에 접근하지 못하도록 특별한 처리를 했기 때문에 번역할 수 없습니다.

## 번역 트리거가 효과가 없음

다른 사이트는 번역되지만 특정 사이트는 번역되지 않음.

- 방문자가 적은 사이트인 경우
  - 마우스를 올려 번역할 문단을 제안
  - 전체 사이트를 번역해야 하는 경우 [사용자 규칙](/docs/advanced/#user-rules)을 통해 적응 가능
- 방문자가 많은 사이트인 경우
  - 마우스를 올려 번역 사용을 시작할 수 있음
  - 그룹에서 호출하여 나중에 적응 가능

## 입력 상자 강화가 효과가 없음

- 브라우저 홈 Google 검색

Google 검색 상자는 [Google](https://www.google.com/) URL의 웹 페이지에 있어야 하며, 브라우저 홈 페이지나 주소 표시줄 빈 곳에서는 사용할 수 없습니다.

## 피드백 디버그 로그

- 디버그 로그 활성화
  패널 열기 -> 설정 -> 개발자 설정 -> "콘솔에 디버그 로그 출력" 활성화.
- 사이트의 콘솔 열기
  오른쪽 클릭하여 검토 열기 -> 오른쪽 상단의 콘솔로 전환 -> 로그를 확인할 작업 수행

## 호버볼 끄는 방법

- 현재 페이지에서 숨기기

"이 사이트는 번역하지 않음"으로 설정합니다.

- 모든 페이지에서 숨기기

[설정 페이지] - [인터페이스 설정]을 열고 [페이지에 호버볼 표시]를 끕니다.

## Chrome에서 플러그인 설치 프로그램 오류

- web_accessible_resource[0]에 대한 잘못된 값

  manifest_version 3을 지원하려면 Chromium 버전이 88 이상이어야 합니다.

## 360 브라우저 설치 방법

360 Extreme Browser x만 지원되며, x가 포함되어 있어야 합니다. Google 확장 스토어에 접근할 수 있다면 직접 설치할 수 있습니다. 접근할 수 없는 경우 [수동 설치](/docs/installation/#manual-installation-to-keep-track-of-the-latest-development-features)를 참조하세요.

## Opera 브라우저에서 작동하지 않음

- google.com 및 기타 검색 페이지에서 작동하지 않으며, 플러그인이 `번역을 시작하기 전에 현재 페이지를 새로 고치세요`를 표시하고 페이지를 새로 고쳐도 이 메시지가 계속 표시됩니다.

Opera 플러그인 설정에서 "Immersive Translate"를 찾아 "검색 페이지 결과에 대한 액세스 허용" 옵션을 켜야 합니다.

<!-- ![](https://s.immersivetranslate.com/static/official-static/assets/opera-allow-search.png) -->

## YouTube 이중 언어 자막이 번체 중국어로 표시되지 않음

YouTube는 기계 번역 자막을 제공하며, 번체 중국어는 서식 오류가 발생하여 모든 자막이 시작 부분에 큰 섹션의 자막으로 나타납니다. 이 시나리오에서는 [설정] [비디오 자막]에서 [Immersive Translate로 자막 번역 사용] 옵션을 켜는 것이 좋습니다.

## 추가 질문 (매우 많이 보기)

<details>
<summary>Tampermonkey로 캐시를 어떻게 지우나요?</summary>
<p>
Tampermonkey의 API 제한으로 인해 Immersive Translate Tampermonkey의 캐시는 해당 웹사이트의 캐시에 저장됩니다. 따라서 캐시를 지우려면 브라우저에서 해당 웹사이트의 개발자 도구 패널을 열고 해당 웹사이트의 캐시를 지우면 됩니다.
</p>
</details>

<details>
<summary>Tampermonkey 사용자 정의 인터페이스 주소 요청 실패?</summary>
<p>
Tampermonkey는 스크립트의 모든 요청이 스크립트 시작 부분에서 권한을 선언해야 합니다. 예: `@connect api.google.com`. 따라서 기본이 아닌 새 도메인 이름을 추가해야 하는 경우, 다른 도메인 이름을 모델로 한 Tampermonkey 시작 부분에서 선언하세요.
</p>
</details>