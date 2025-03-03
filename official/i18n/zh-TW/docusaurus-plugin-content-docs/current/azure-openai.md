# Azure OpenAI

> 💡 從外掛版本 1.15.1 開始支援

## 簡要說明

1. 官方網站：[Azure OpenAI](https://learn.microsoft.com/zh-cn/azure/cognitive-services/openai/chatgpt-quickstart?tabs=command-line&pivots=rest-api/)
2. 官方資費說明：[Azure OpenAI 定價檔案](https://azure.microsoft.com/zh-cn/pricing/details/cognitive-services/openai-service/#pricing)

## 使用步驟

先在 Azure 控制台創建 OpenAI 服務，再進入 Azure AI Studio: https://oai.azure.com, 創建一個 gpt-35-turbo 的 deployment，記住 deployment name

部署 gpt-35-turbo 模型之後，打開沉浸式翻譯的 OpenAI 設定頁面：

1. Api Key 請填寫 Azure 控制台提供的 Key
2. 點擊展開更多設定，設定自訂地址為：

`https://{your-custom-name}.openai.azure.com/openai/deployments/{you-deployment-name}/chat/completions?api-version=2024-07-01-preview`

將 `{your-custom-name}` 改為你自己的子域名，`{you-deployment-name}` 改為你自己的 deployment name

3. 模型名字需要手動選擇自訂模型，改為： `gpt-35-turbo`,

> 如果還有疑問，你可以在 Azure AI Studio 裡面，打開 PlayGround，【View Code】，下方會有最終的【EndPoint】和【Key】，如下圖：

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/azure-openai-key.jpg)

## 自訂 OpenAI 的 API 地址

- 可以通過`更多設定`來進行配置，入口如下

---

<img width="951" alt="Snipaste_2023-04-08_19-29-18" src="https://user-images.githubusercontent.com/5794691/230718739-ff661ce3-04af-4391-8efc-9a5a1c8374b0.png"/>

---
