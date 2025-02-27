# Open AI

透過開通[沉浸式翻譯 Pro 會員](https://immersivetranslate.com/pricing/) 後直接使用 OpenAI 翻譯服務（推薦）

[點此查看介紹](https://immersivetranslate.com/pricing/)

## 透過 OpenAI 官方開發者平台獲取 API Key

- [openAI API 官方地址](https://openai.com/api/)
  - 注意：目前 OpenAI 本身不開放中國手機號碼註冊。
- 註冊 OpenAI 帳戶後，打開[API Secret Key](https://platform.openai.com/account/api-keys)，創建 API Secret Key
- 然後將 key 填寫在沉浸式翻譯擴充套件裡的 OpenAI 的配置項裡即可。

## 注意事項

1. **如果沒有綁定信用卡，或者是 OpenAI 5 刀新用戶，每分鐘請求數最多 3 個**，基本無法使用，出錯很正常。[你可以點此查看你的 API 的頻率限制](https://platform.openai.com/account/rate-limits)
2. OpenAI 的 API 和 ChatGPT 是兩個不同的服務，沉浸式翻譯擴充套件支持的是 OpenAI 的 API，而不是網頁版的 ChatGPT，因此你需要開通 OpenAI 的 API 服務而非開通 ChatGPT plus，開通後在設定頁面填寫 API Key 即可。
3. 出現 429 錯誤，說明超出了 openai 的頻率限制，建議調低每秒的最大請求數，尤其是翻譯電子書的時候，即使是付費版，也需要調低每秒最大請求數，調整到每秒 5 個請求會穩定一點。
4. OpenAI gpt-3.5-turbo 模型的價格為：$0.002 / 1K tokens，實測翻譯 66 萬英文字符花費大約 1 美元，翻譯 17 萬英文字符花費大約 0.25 美元。
5. 沉浸式翻譯擴充套件支持多個 API Key 負載均衡，請在填寫的時候用英文逗號 `,` 分隔不同的 key

## 當前請求數推薦

最近 OpenAI 對付費版用戶限制也很大，從 0.5.0 版本起默認請求數單位改為秒，默認每秒最大請求數改為 10 個請求。