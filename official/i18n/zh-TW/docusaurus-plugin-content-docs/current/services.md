# 翻譯服務 API 申請

沉浸式翻譯擴展支援很多翻譯服務，其中部分翻譯服務需要你申請對應服務的 API 密鑰才能使用，我從網路上整理了以下服務的申請教程，如果有遺漏或者沒有及時更新的地方，歡迎點擊右上角編輯這些頁面。

可以[在此](https://github.com/immersive-translate/immersive-translate/issues/137)進行翻譯服務 API 相關的討論。

## 翻譯服務

- [Claude](./services/claude.md)
  - API 介面：https://api.anthropic.com/v1/messages
- [Deepl](./services/deepL.md)
  - API 介面：https://api.deepl.com/v2/translate
- [DeepSeek](./services/deepseek.md)
  - API 介面：https://api.deepseek.com/chat/completions
- [Gemini](./services/gemini.md)
  - API 介面：https://generativelanguage.googleapis.com/v1beta/models/\{model\}:generateContent?key=\{key\}
- [OpenL](./services/openL.md)
  - API 介面：https://api.openl.club/services/\{codename}/translate
- [Open AI (Azure OpenAI)](./services/openai.md)
  - API 介面：https://openai-api.immersivetranslate.com/v1/chat/completions
- [微軟 Azure 翻譯](./services/azure.md)
  - API 介面：https://api.cognitive.microsofttranslator.com/translate?x=2
- [阿里雲百煉大模型](./services/aliyun-bailian.md)
  - API 介面：https://dashscope.aliyuncs.com/compatible-mode/v1/chat/completions
- [阿里雲翻譯](./services/aliyun.md)
  - API 介面：https://\{service\}.aliyuncs.com?\{paramsString\}
- [百度千帆大模型](./services/baidu-qianfan.md)
  - API 介面：https://aip.baidubce.com/rpc/2.0/ai_custom/v1/wenxinworkshop/chat/{model}?access_token={key}
- [字節跳動豆包大模型](./services/doubao.md)
  - API 介面：https://ark.cn-beijing.volces.com/api/v3/chat/completions
- [百度翻譯](./services/baidu.md)
  - API 介面：https://api.fanyi.baidu.com/api/trans/vip/translate
- [彩雲小譯](./services/caiyun.md)
  - API 介面：https://api.interpreter.caiyunai.com/v1/translator
- [火山引擎](./services/volcano.md)
  - API 介面：https://translate.volcengine.com/crx/translate/v1/
- [騰訊翻譯君](./services/tencent.md)
  - API 介面：https://transmart.qq.com/api/imt
- [小牛翻譯](./services/niu.md)
  - API 介面：https://api.niutrans.com/NiuTransServer/translation
- [有道翻譯](./services/youdao.md)
  - API 介面：https://openapi.youdao.com/api
- [有道子曰大模型翻譯](./services/youdao-ziyue.md)
  - API 介面：https://openapi.youdao.com/llm_trans
- [自定義介面翻譯](./services/custom.md)

## 免責聲明

以上所有翻譯服務費用，完全由該服務商收取，與本擴展無關。

請大家注意各個服務商的免費額度，避免意外扣費。

## 關於字元數的簡單說明

字元數以翻譯的源語言字元長度為標準計算。空格，標點符號等均計入字元。對於大多數服務來說一個漢字，英文字母，標點符號，換行符等都算作一個字元。例如馬斯克的這段推特有 32 個詞，196 個字元。

> To be clear, I’m not someone who thinks lots of government agencies should be abolished (maybe a few), but we should always question our institutions, as this strengthens the bedrock of democracy.

這樣一篇看起來很難讀完的長文：[Algorithms Unlocked: How They’re Shaping Our Everyday Lives | by Two Techie Vibes | Jan, 2023 | Medium](https://twotechievibes.medium.com/algorithms-unlocked-how-theyre-shaping-our-everyday-lives-6261fa1dbad)，大概有 1 萬的字元數。

希望這兩個例子能讓你對字元數有個感性的認識。