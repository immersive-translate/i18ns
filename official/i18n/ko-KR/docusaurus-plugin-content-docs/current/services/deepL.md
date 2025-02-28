# DeepL

## [Immersive Translate Pro Membership](https://immersivetranslate.com/en/pricing/)을 열면 DeepL 번역 서비스에 직접 액세스 가능 (추천)

[자세히 알아보기](https://immersivetranslate.com/en/pricing/)

## DeepL의 공식 API 얻기

1. 공식 소개: [DeepL API](https://www.deepl.com/en/pro#developer)

   - 참고: [DeepL API](https://www.deepl.com/en/pro#developer)와 [DeepL Pro](https://www.deepl.com/pro)는 두 가지 다른 계정 유형이며, [DeepL API](https://www.deepl.com/en/pro/select-country#developer) 계정입니다.

2. [왜](https://www.deepl.com/en/whydeepl) DeepL을 선택해야 하나요?

   - 영어 ⇄ 중국어 5배 더 정확
   - 영어 ⇄ 일본어 6배 더 정확
   - 인공지능 기술(신경망)에 기반한 번역 엔진

3. Deepl API는 [Free API와 Pro API](https://www.deepl.com/en/pro#developer)로 나뉩니다.

   - Free API는 매월 500,000개의 무료 문자를 제공합니다.
   - Pro API의 [공식 요금](https://www.deepl.com/en/pro#developer)은: 1백만 문자당 $25입니다.
   - 고빈도 사용자의 경우, 한 달에 소비되는 문자 수는 약 1천만 문자이며, 가격은 약 250 USD입니다.

4. 계정을 등록하고 [DeepL API](https://www.deepl.com/en/pro#developer)를 여세요.

## 일반적인 문제

### 1. 입력한 키가 사용 불가합니다.

DeepL API Pro와 DeepL Pro는 두 가지 종류의 계정이며, Immersive Translate에서 사용할 수 있는 Auth Key는 DeepL API 계정입니다. [DeepL API Pro](https://www.deepl.com/en/pro/select-country#developer)를 클릭하세요.

### 2. 401, 403 인증 오류 문제 해결

이러한 오류는 일반적으로 잘못된 유형의 인증 키를 사용할 때 발생합니다. 주의하세요:

1. DeepL은 두 가지 다른 제품을 제공합니다: DeepL Pro (번역 서비스)와 DeepL API (개발자 인터페이스)
2. DeepL Pro 계정 설정에서 찾은 키는 API 호출과 **호환되지 않습니다**
3. API 키를 얻으려면 DeepL API 계정을 별도로 등록해야 합니다
4. DeepL Free API 키는 `:fx`로 끝나는 것으로 식별됩니다
5. DeepL Pro API 키는 `:fx` 접미사가 없으며 일반 문자열로 나타납니다

DeepL Pro 번역 서비스가 아닌 DeepL API 서비스에 제대로 등록했는지 확인하세요.

### 3. 456, 사용자 할당량 초과

사용량이 DeepL의 공식 사용자당 하드 제한을 초과했습니다. DeepL의 공정 사용 정책을 위반했을 수 있으며, 이러한 행동을 피하는 것이 좋습니다. 유료 구독자인 경우, 사용량은 다음 달에 자동으로 초기화됩니다.
