# Open AI (Azure OpenAI)

透過開通[沉浸式翻譯 Pro 會員](https://immersivetranslate.com/pricing/) 後直接使用 OpenAI 翻譯服務（推薦）

[點此檢視介紹](https://immersivetranslate.com/pricing/)

## 透過 OpenAI 官方開發者平臺取得 API Key

- [OpenAI API 官方地址](https://openai.com/api/)
  - 注意：目前 OpenAI 本身不開放中國手機號碼註冊。
- 註冊 OpenAI 帳戶後，開啟[API Secret Key](https://platform.openai.com/account/api-keys)，建立 API Secret Key
- 然後將 key 填寫在沉浸式翻譯擴展裡的 OpenAI 的設定選項裡即可。

## 注意事項

1. **如果沒有綁定信用卡，或者是 OpenAI 5 刀新使用者，每分鐘請求數最多 3 個**，基本無法使用，出錯很正常。[你可以點此檢視你的 API 的頻率限制](https://platform.openai.com/account/rate-limits)
2. OpenAI 的 API 和 ChatGPT 是兩個不同的服務，沉浸式翻譯擴展支援的是 OpenAI 的 API，而不是網頁版的 ChatGPT，因此你需要開通 OpenAI 的 API 服務而非開通 ChatGPT plus，開通後在設定頁面填寫 API Key 即可。
3. 出現 429 錯誤，說明超出了 openai 的頻率限制，建議調低每秒的最大請求數，尤其是翻譯電子書的時候，即使是付費版，也需要調低每秒最大請求數，調整到每秒 5 個請求會穩定一點。
4. OpenAI gpt-3.5-turbo 模型的價格為：$0.002 / 1K tokens，實測翻譯 66 萬英文字元花費大約 1 美元，翻譯 17 萬英文字元花費大約 0.25 美元。
5. 沉浸式翻譯擴展支援多個 API Key 負載均衡，請在填寫的時候用英文逗號 `,` 分隔不同的 key

## 目前請求數推薦

最近 OpenAI 對付費版使用者限制也很大，從 0.5.0 版本起預設請求數單位改為秒，預設每秒最大請求數改為 10 個請求。

## Azure OpenAI

OpenAI 翻譯服務同時也相容 Azure OpenAI 介面，先在 Azure 控制檯建立 OpenAI 服務，再進入 Azure AI Studio: https://oai.azure.com, 建立一個 gpt-35-turbo 的 deployment，記住 deployment name

部署 gpt-35-turbo 模型之後，開啟沉浸式翻譯的 OpenAI 設定頁面：

1. Api Key 請填寫 Azure 控制檯提供的 Key
2. 點選展開更多設定，設定自訂地址為：

`https://{your-custom-name}.openai.azure.com/openai/deployments/{you-deployment-name}/chat/completions?api-version=2024-07-01-preview`

將 `{your-custom-name}` 改為你自己的子域名，`{you-deployment-name}` 改為你自己的 deployment name

3. 模型名字需要手動選擇自訂模型，改為： `gpt-35-turbo`,

> 如果還有疑問，你可以在 Azure AI Studio 裡面，開啟 PlayGround，【View Code】，下方會有最終的【EndPoint】和【Key】，如下圖：

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/azure-openai-key.jpg)

## 自訂 OpenAI 的 API 地址

- 可以透過`更多設定`來進行設定，入口如下

---

<img width="951" alt="Snipaste_2023-04-08_19-29-18" src="https://user-images.githubusercontent.com/5794691/230718739-ff661ce3-04af-4391-8efc-9a5a1c8374b0.png"/>

---
