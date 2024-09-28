# 마이크로소프트 Azure 번역

## 간단한 소개

1. 공식 웹사이트: [마이크로소프트 Azure 번역](https://learn.microsoft.com/zh-cn/azure/cognitive-services/translator/text-translation-overview)
2. 공식 설명: 매월 200만 자 이내의 번역은 무료이며, 매월 200만 자를 초과하는 경우, 10달러/100만 자의 요금이 부과됩니다. 자세한 내용은 [가격 책정 설명](https://azure.microsoft.com/zh-cn/pricing/details/cognitive-services/translator/)을 참조하세요.

## 등록 절차

등록 절차는 다른 번역 서비스에 비해 다소 복잡하며, 인내심을 가지고 진행해야 합니다.

참조 링크: [마이크로소프트 Azure 번역 시작 문서](https://learn.microsoft.com/zh-cn/azure/cognitive-services/translator/document-translation/quickstarts/get-started-with-rest-api?pivots=programming-language-csharp)

## Azure 계정 등록

첫 번째 단계, [Azure](https://azure.microsoft.com/zh-cn/free/cognitive-services/) 계정을 등록하며, 국제 신용카드(Visa/Master)를 반드시 연결해야 합니다. 없을 경우 등록이 불가능합니다.

## Azure Blob 스토리지 계정 등록

두 번째 단계, [Azure Blob](https://portal.azure.com/#create/Microsoft.StorageAccount) 스토리지 계정을 등록합니다.

1. 새 리소스 그룹을 만들고, 스토리지 계정 이름을 입력합니다.
2. 지역은 가장 가까운 지역을 선택합니다. 예를 들어, 홍콩 지역은 `East Asia`입니다.
3. 나머지 과정은 그냥 다음 단계를 클릭하면 됩니다. 마지막 페이지에서, 배포가 완료된 후, 왼쪽 하단의 파란색 버튼 "생성"을 클릭합니다.

## 번역 도구 생성

세 번째 단계, [번역 도구](https://portal.azure.com/#create/Microsoft.CognitiveServicesTextTranslation)를 생성합니다.

1. 지역은 가장 가까운 지역을 선택합니다. 예를 들어, 홍콩 지역은 `East Asia`입니다.
2. 가격 책정 계층은 필요에 따라 선택합니다. 무료 사용자는 `Free F0`를 선택할 수 있습니다. 무료 계층은 문서 번역을 지원하지 않습니다. 필요한 경우 표준 S1을 시도해 볼 수 있습니다.
3. 나머지 과정은 그냥 다음 단계를 클릭하면 됩니다. 마지막 페이지에서, 배포가 완료된 후, 왼쪽 하단의 파란색 버튼 "생성"을 클릭합니다.

## 액세스 키

배포가 성공적으로 완료된 후, [Azure 대시보드](https://portal.azure.com/#home)로 이동하여 **번역 도구** 페이지에 접속합니다. 왼쪽 메뉴의 리소스 관리에서 `키 및 엔드포인트`를 선택하여 키를 찾습니다. Microsoft는 두 개의 키를 제공하며, 그 중 하나를 선택하여 침수형 확장 - Microsoft 번역의 `APIKEY`에 입력합니다.

키 아래에는 `위치/지역` 정보도 있습니다. 예를 들어 `eastasia`와 같은 정보도 침수형 확장 - Microsoft 번역의 `region`에 입력해야 합니다.

## 자주 묻는 질문

궁금한 점이 있으시면 [여기](https://github.com/immersive-translate/immersive-translate/issues/137)에 피드백을 남겨주세요.
