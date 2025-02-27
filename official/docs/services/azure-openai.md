# Azure OpenAI

> 💡 从插件版本 1.14.16 开始支持

## 简要说明

1. 官方网站：[Azure OpenAI](https://learn.microsoft.com/zh-cn/azure/cognitive-services/openai/chatgpt-quickstart?tabs=command-line&pivots=rest-api/)
2. 官方资费说明：[Azure OpenAI 定价文档](https://azure.microsoft.com/zh-cn/pricing/details/cognitive-services/openai-service/#pricing)

## 使用步骤

先在 Azure 控制台创建 OpenAI 服务，再进入 Azure AI Studio: https://oai.azure.com, 创建一个 gpt-35-turbo 的 deployment，记住 deployment name

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

