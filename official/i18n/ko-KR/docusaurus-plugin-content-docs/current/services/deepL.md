# DeepL

## [몰입형 번역 Pro 멤버십](https://immersivetranslate.com/pricing/)을 구독한 후 DeepL 번역 서비스를 직접 사용하세요(추천)

[여기를 클릭하여 소개 보기](https://immersivetranslate.com/pricing/)

## DeepL 공식을 통해 DeepL API 획득하기

1. 공식 소개: [DeepL API](https://www.deepl.com/zh/pro#developer)
   - 주의: [DeepL API](https://www.deepl.com/zh/pro#developer)와 [DeepL Pro](https://www.deepl.com/pro)는 두 가지 다른 계정 유형입니다. 몰입형 번역에서 사용되는 것은 [DeepL API](https://www.deepl.com/zh/pro/select-country#developer) 계정입니다.
2. [왜](https://www.deepl.com/zh/whydeepl) DeepL을 선택해야 할까요?

   - 영어 ⇄ 중국어는 5배 더 정확합니다.
   - 영어 ⇄ 일본어는 6배 더 정확합니다.
   - 번역 엔진은 인공 지능 기술(신경망)을 기반으로 합니다.

3. Deepl API는 [Free API와 Pro API](https://www.deepl.com/zh/pro#developer)로 나뉩니다.

   - Free API는 매월 50만 무료 문자 할당량을 제공합니다.
   - Pro API의 [공식 요금](https://www.deepl.com/zh/pro#developer)은: 100만 문자당 25달러입니다.
   - 빈번하게 사용하는 사용자의 경우, 한 달에 대략 1000만 문자를 소모하며, 가격은 대략 250달러입니다.

4. [DeepL API](https://www.deepl.com/zh/pro#developer) 계정을 등록하고 활성화하려면, DeepL이 [지원하는 국가 또는 지역](https://support.deepl.com/hc/zh-cn/articles/360020016339-DeepL-Pro%E5%9C%A8%E6%88%91%E6%89%80%E5%9C%A8%E5%9B%BD%E5%AE%B6%E6%97%A0%E6%B3%95%E8%AE%A2%E9%98%85)에서 발급한 VISA 또는 MASTER 신용카드를 제공해야 합니다. 유감스럽게도, 현재 중국 내에서 발급된 모든 신용카드(듀얼 통화 카드 및 외화 카드 포함)는 지원되지 않습니다.

## DeepL 번체 중국어

DeepL의 몰입형 번역 서비스는 번체 중국어도 지원해요! (DeepL 공식적으로 번체 중국어를 지원하지 않기 때문에, 많은 번체 사용자들이 DeepL의 고품질 번역 서비스를 이용할 수 없었습니다. 이러한 번체 중국어 사용자의 불편을 해소하기 위해, 몰입형 번역 확장은 DeepL의 간체 중국어를 다시 번체 중국어로 변환할 것입니다.

## 자체 구축 DeepL API

우리는 베타 기능에서 자체 구축한 DeeplX 서비스를 실험적으로 지원하고 있습니다(하지만 테스트 결과, 이 서비스는 웹 페이지 번역 서비스로는 적합하지 않습니다. 웹 페이지 번역은 API 요청량이 매우 많기 때문에, 이 서비스를 구축할 경우 반드시 부하 분산을 잘 준비해야 합니다), 다음은 이 실험 기능을 활성화하는 방법에 대한 설명입니다:

1. 개발자 설정에서 베타 테스트 기능을 활성화합니다.
2. 기본 설정에서 DeepLX(Beta)를 찾아 자체 구축한 DeepL API URL을 입력합니다, 예: http://your-domain/translate

> Q: 어떻게 자체 구축하나요?  
> A: [OwO-Network/DeepLX](https://github.com/OwO-Network/DeepLX#setup-on-immersive-translate) 또는 [zu1k/deepl](https://github.com/KyleChoy/zotero-pdf-translate/blob/CustomDeepL/README.md)

## 자주 묻는 질문

### 1. 입력한 키가 사용할 수 없습니다.

DeepL API Pro와 DeepL Pro는 두 가지 계정 유형이며, 몰입형 번역에서 사용할 수 있는 Auth Key는 DeepL API 계정입니다. 여기를 클릭하여 [DeepL API Pro](https://www.deepl.com/zh/pro/select-country#developer)를 확인하세요.

### 2. Deepl Free API가 401, 403 권한 없음을 표시합니다.

Deepl Free API의 Key는 모두 `:fx`로 끝나며, 다른 것들은 Free API의 key가 아닙니다.

### 3. 456, 사용자 할당량 초과

사용량이 DeepL에서 각 사용자에게 설정한 하드 리밋을 초과했습니다. DeepL의 합리적 사용 정책을 위반했을 수 있으니, 이러한 행위를 피하는 것이 좋습니다. 유료 사용자의 경우, 다음 달에 사용량이 자동으로 리셋됩니다.
