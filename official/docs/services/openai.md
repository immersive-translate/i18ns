# Open AI (Azure OpenAI)

通过开通[沉浸式翻译Pro会员](https://immersivetranslate.com/pricing/) 后直接使用 OpenAI 翻译服务（推荐）

[点此查看介绍](https://immersivetranslate.com/pricing/)

## 通过 OpenAI 官方开发者平台获取 API Key

- [openAI API 官方地址](https://openai.com/api/)
  - 注意：目前 OpenAI 本身不开放中国手机号码注册。
- 注册 OpenAI 账户后，打开[API Secret Key](https://platform.openai.com/account/api-keys)，创建 API Secret Key
- 然后将 key 填写在沉浸式翻译扩展里的 OpenAI 的配置项里即可。

## 注意事项

1. **如果没有绑定信用卡，或者是 OpenAI 5刀新用户，每分钟请求数最多 3 个**，基本无法使用，出错很正常。[你可以点此查看你的API的频率限制](https://platform.openai.com/account/rate-limits)
2. OpenAI 的 API 和 ChatGPT 是两个不同的服务，沉浸式翻译扩展支持的是 OpenAI 的 API，而不是网页版的 ChatGPT，因此你需要开通 OpenAI 的 API 服务而非开通 ChatGPT plus，开通后在设置页面填写 API Key 即可。
3. 出现 429 错误，说明超出了 openai 的频率限制，建议调低每秒的最大请求数，尤其是翻译电子书的时候，即使是付费版，也需要调低每秒最大请求数，调整到每秒 5 个请求会稳定一点。
4. OpenAI gpt-3.5-turbo 模型的价格为：$0.002 / 1K tokens，实测翻译 66 万英文字符花费大约 1 美元，翻译 17 万英文字符花费大约 0.25 美元。
5. 沉浸式翻译扩展支持多个 API Key 负载均衡, 请在填写的时候用英文逗号 `,` 分隔不同的 key

## 当前请求数推荐

最近 OpenAI 对付费版用户限制也很大，从 0.5.0 版本起默认请求数单位改为秒，默认每秒最大请求数改为 10 个请求。

## Azure OpenAI

OpenAI 翻译服务同时也兼容 Azure OpenAI 接口，先在 Azure 控制台创建 OpenAI 服务，再进入 Azure AI Studio: <https://oai.azure.com>, 创建一个 gpt-35-turbo 的 deployment，记住 deployment name

部署 gpt-35-turbo 模型之后，打开沉浸式翻译的 OpenAI 设置页面：

1. Api Key 请填写 Azure 控制台提供的 Key
2. 点击展开更多设置，设置自定义地址为：

`https://{your-custom-name}.openai.azure.com/openai/deployments/{you-deployment-name}/chat/completions?api-version=2024-07-01-preview`

将 `{your-custom-name}` 改为你自己的子域名，`{you-deployment-name}` 改为你自己的 deployment name

3. 模型名字需要手动选择自定义模型，改为： `gpt-35-turbo`,

> 如果还有疑问，你可以在 Azure AI Studio 里面，打开 PlayGround，【View Code】，下方会有最终的【EndPoint】和【Key】，如下图：

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/azure-openai-key.jpg)

## 自定义 OpenAI 的 API 地址

- 可以通过`更多设置`来进行配置，入口如下

---

<img width="951" alt="Snipaste_2023-04-08_19-29-18" src="https://user-images.githubusercontent.com/5794691/230718739-ff661ce3-04af-4391-8efc-9a5a1c8374b0.png"/>

---
