# 화산 번역

## 간단한 설명

1. 공식 웹사이트: [기계 번역-화산 엔진](https://www.volcengine.com/product/machine-translation)
2. 공식 요금 설명: [제품 요금 기계 번역-화산 엔진](https://www.volcengine.com/docs/4640/68515)
3. 화산 번역은 매월 처음 200만 문자까지 무료이며, 그 이상은 49위안 / 백만 문자로 요금이 부과됩니다. 자세한 내용은 공식 요금 설명 문서를 참조하십시오.

## 신청 절차

1. [API 접근 프로세스 개요 기계 번역-화산 엔진](https://www.volcengine.com/docs/4640/130872), 공식 가이드를 따라 계정 등록, 실명 인증, 서비스 개통 이 세 단계를 완료하세요. [화산 엔진 콘솔](https://console.volcengine.com/home)에서 조작이 필요합니다.
2. 네 번째 단계에서 키를 얻는 과정에서, 화산 엔진은 두 가지 옵션을 제공합니다:
   1. 계속해서 생성하기(주 계정으로 키 생성, 더 편리하지만 이 key는 주 계정 자원을 호출할 수 있으며 안전하지 않을 수 있음), "계속해서 생성하기"를 선택한 후, 표에 새로운 데이터가 나타나며 여기에 우리가 사용할 "Access Key ID"와 "Secret Access Key"가 포함됩니다.
   2. 새로운 하위 사용자 생성하기(하위 사용자로 키를 생성하는 것이 더 안전함을 권장), "Access Key ID"와 "Secret Access Key"를 획득, 해당 하위 계정은 `TranslateFullAccess` 권한을 가져야 합니다.
3. 몰입형 번역의 기본 설정을 열고 - 번역 서비스를 찾아 화산 번역 옵션을 작성하세요.
4. 완료 🎉, 궁금한 점이 있다면 [여기](https://github.com/immersive-translate/immersive-translate/issues/137)에서 피드백을 주세요.