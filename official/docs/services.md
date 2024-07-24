# 翻译服务 API 申请

沉浸式翻译扩展支持很多翻译服务，其中部分翻译服务需要你申请对应服务的 API 密钥才能使用，我从网络上整理了以下服务的申请教程，如果有遗漏或者没有及时更新的地方，欢迎点击右上角编辑这些页面。

可以[在此](https://github.com/immersive-translate/immersive-translate/issues/137)进行翻译服务 API 相关的讨论。

## 翻译服务

- [Claude](./services/claude.md)
  - API 接口：https://api.anthropic.com/v1/messages
- [Deepl](./services/deepL.md)
  - API 接口：https://api.deepl.com/v2/translate
- [DeepSeek](./services/deepseek.md)
  - API 接口：https://api.deepseek.com/chat/completions
- [Gemini](./services/gemini.md)
  - API 接口：https://generativelanguage.googleapis.com/v1beta/models/{model}:generateContent?key={key}
- [OpenL](./services/openL.md)
  - API 接口：https://api.openl.club/services/${codename}/translate
- [Open AI (Azure OpenAI)](./services/openai.md)
  - API 接口：https://openai-api.immersivetranslate.com/v1/chat/completions
- [微软 Azure 翻译](./services/azure.md)
  - API 接口：https://api.cognitive.microsofttranslator.com/translate?x=2
- [阿里云百炼大模型](./services/aliyun-bailian.md)
  - API 接口：https://dashscope.aliyuncs.com/compatible-mode/v1/chat/completions
- [阿里云翻译](./services/aliyun.md)
  - API 接口：https://{service}.aliyuncs.com?{paramsString}
- [百度千帆大模型](./services/baidu-qianfan.md)
  - API 接口：https://aip.baidubce.com/rpc/2.0/ai_custom/v1/wenxinworkshop/chat/{model}?access_token={key}
- [字节跳动豆包大模型](./services/doubao.md)
  - API 接口：https://ark.cn-beijing.volces.com/api/v3/chat/completions
- [百度翻译](./services/baidu.md)
  - API 接口：https://api.fanyi.baidu.com/api/trans/vip/translate
- [彩云小译](./services/caiyun.md)
  - API 接口：https://api.interpreter.caiyunai.com/v1/translator
- [火山引擎](./services/volcano.md)
  - API 接口：https://translate.volcengine.com/crx/translate/v1/
- [腾讯翻译君](./services/tencent.md)
  - API 接口：https://transmart.qq.com/api/imt
- [小牛翻译](./services/niu.md)
  - API 接口：https://api.niutrans.com/NiuTransServer/translation
- [有道翻译](./services/youdao.md)
  - API 接口：https://openapi.youdao.com/api
- [自定义接口翻译](./services/custom.md)

## 免责声明

以上所有翻译服务费用，完全由该服务商收取，与本扩展无关。

请大家注意各个服务商的免费额度，避免意外扣费。

## 关于字符数的简单说明

字符数以翻译的源语言字符长度为标准计算。空格, 标点符号等均计入字符。对于大多数服务来说一个汉字，英文字母，标点符号，换行符等都算作一个字符。例如马斯克的这段推特有 32 个词，196 个字符。

> To be clear, I’m not someone who thinks lots of government agencies should be abolished (maybe a few), but we should always question our institutions, as this strengthens the bedrock of democracy.

这样一篇看起来很难读完的长文：[Algorithms Unlocked: How They’re Shaping Our Everyday Lives | by Two Techie Vibes | Jan, 2023 | Medium](https://twotechievibes.medium.com/algorithms-unlocked-how-theyre-shaping-our-everyday-lives-6261fa1dbad)，大概有 1 万的字符数。

希望这两个例子能让你对字符数有个感性的认识。
