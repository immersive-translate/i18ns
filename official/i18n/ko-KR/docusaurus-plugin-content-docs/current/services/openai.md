# Open AI (Azure OpenAI)

OpenAI 번역 서비스를 직접 사용하려면 [침습적 번역 Pro 멤버십](https://immersivetranslate.com/pricing/)에 가입하세요(추천).

[소개 보기](https://immersivetranslate.com/pricing/)

## OpenAI 공식 개발자 플랫폼에서 API Key 받기

- [openAI API 공식 사이트](https://openai.com/api/)
  - 주의: 현재 OpenAI는 중국 휴대폰 번호로 등록을 허용하지 않습니다.
- OpenAI 계정을 등록한 후, [API Secret Key](https://platform.openai.com/account/api-keys)를 열어 API Secret Key를 생성하세요.
- 그런 다음 생성된 key를 침습적 번역 확장 프로그램의 OpenAI 설정 항목에 입력하면 됩니다.

## 주의 사항

1. **신용카드를 등록하지 않았거나 OpenAI 5달러 신규 사용자인 경우, 분당 최대 요청 수는 3개로** 기본적으로 사용하기 어렵고, 오류가 발생하는 것이 정상입니다. [여기를 클릭하여 API의 요청 한도를 확인할 수 있습니다](https://platform.openai.com/account/rate-limits)
2. OpenAI의 API와 ChatGPT는 두 가지 다른 서비스입니다. 몰입형 번역 확장 기능은 OpenAI의 API를 지원하며, 웹 버전의 ChatGPT가 아닙니다. 따라서 ChatGPT plus를 개통하는 것이 아니라 OpenAI의 API 서비스를 개통해야 하며, 개통 후 설정 페이지에 API Key를 입력하면 됩니다.
3. 429 오류가 발생하면, openai의 요청 한도를 초과한 것입니다. 초당 최대 요청 수를 낮추는 것이 좋으며, 특히 전자책을 번역할 때는 유료 버전이라도 초당 최대 요청 수를 낮춰야 합니다. 초당 요청 수를 5개로 조정하면 더 안정적입니다.
4. OpenAI gpt-3.5-turbo 모델의 가격은: $0.002 / 1K 토큰이며, 실제로 66만 영문자를 번역하는 데 약 1달러, 17만 영문자를 번역하는 데 약 0.25달러가 소요됩니다.
5. 몰입형 번역 확장 기능은 여러 API Key의 부하 분산을 지원합니다. 입력할 때는 영어 쉼표 `,`로 다른 key를 구분해 주세요.

## 현재 요청 수 권장 사항

최근 OpenAI는 유료 사용자에 대한 제한을 크게 강화했으며, 0.5.0 버전부터 기본 요청 수 단위를 초로 변경하고, 기본 초당 최대 요청 수를 10개로 변경했습니다.

## Azure OpenAI

OpenAI 번역 서비스는 Azure OpenAI 인터페이스와도 호환됩니다. 먼저 Azure 콘솔에서 OpenAI 서비스를 생성한 다음, <https://oai.azure.com>에 접속하여 Azure AI Studio에서 gpt-35-turbo deployment를 생성하고, deployment name을 기억하세요.

gpt-35-turbo 모델을 배포한 후, OpenAI 설정 페이지에서 번역 설정을 엽니다:

1. Api Key에는 Azure 콘솔에서 제공하는 Key를 입력하세요.
2. 더 많은 설정을 표시하려면 클릭하고, 다음과 같이 사용자 정의 주소를 설정하세요:

`https://{your-custom-name}.openai.azure.com/openai/deployments/{you-deployment-name}/chat/completions?api-version=2024-07-01-preview`

여기서 `{your-custom-name}`을 당신의 서브도메인으로, `{you-deployment-name}`을 당신의 deployment name으로 변경하세요.

3. 모델 이름은 수동으로 사용자 정의 모델을 선택하고, `gpt-35-turbo`로 변경해야 합니다.

> 질문이 있으시다면, Azure AI Studio에서 PlayGround를 열고, 【View Code】를 클릭하세요. 아래에 최종 【EndPoint】와 【Key】가 표시됩니다. 아래 그림과 같습니다:

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/azure-openai-key.jpg)

## OpenAI API 주소 사용자 정의

- `더 많은 설정`을 통해 구성할 수 있으며, 접근 방법은 다음과 같습니다.

---

<img width="951" alt="Snipaste_2023-04-08_19-29-18" src="https://user-images.githubusercontent.com/5794691/230718739-ff661ce3-04af-4391-8efc-9a5a1c8374b0.png"/>

---
