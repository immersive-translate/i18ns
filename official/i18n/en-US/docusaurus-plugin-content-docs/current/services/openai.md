# Open AI (Azure OpenAI)

Direct access to OpenAI translation services by opening an [Immersive Translate Pro membership](https://immersivetranslate.com/en/pricing/) (recommended)

[Click here for presentation](https://immersivetranslate.com/en/pricing/)

## Obtain an API Key from the official OpenAI developer platform.

- [openAI API official address](https://openai.com/api/)
  - Note:：Currently, OpenAI is not open for registration by Chinese cell phone numbers.
- After registering for an OpenAI account, open [API Secret Key](https://platform.openai.com/account/api-keys) to create an API Secret Key
- Then just fill in the key in the OpenAI configuration in the Immersive Translate extension.

## Caveat

1. **If you don't have a credit card tied to it, or are a new OpenAI 5-blade user with up to 3 requests per minute**, it's basically unusable and it's normal to get errors.[You can click here to see the frequency limits for your API](https://platform.openai.com/account/rate-limits)
2. OpenAI's API and ChatGPT are two different services, the Immersive Translate Extension supports OpenAI's API, not the web version of ChatGPT, so you need to open OpenAI's API service instead of opening ChatGPT plus, and fill in the API Key on the Settings page after opening.
3. 429 error, it means that the frequency limit of openai has been exceeded, it is recommended to reduce the maximum number of requests per second, especially when translating e-books, even if it is a paid version, you need to reduce the maximum number of requests per second, and adjust it to 5 requests per second to make it more stable.
4. The OpenAI gpt-3.5-turbo model is priced at：$0.002 / 1K tokens, and costs about $1 to translate 660,000 English characters and $0.25 to translate 170,000 English characters.
5. Immersive Translate Extension supports multiple API keys for load balancing, please use comma `,` to separate different keys when you fill in the form.

## Current request number recommendation

Recently, OpenAI has also become very restrictive for paid users, as of version 0.5.0 the default request count has been changed to seconds, and the default maximum number of requests per second has been changed to 10 requests per second.

## Azure OpenAI

The OpenAI translation service is also compatible with the Azure OpenAI interface. First, create the OpenAI service in the Azure console, then go to Azure AI Studio: https://oai.azure.com, create a gpt-35-turbo deployment, and remember the deployment name

After deploying the gpt-35-turbo model, open the OpenAI settings page for Immersive Translate：

1. Api Key Please fill in the key provided by the Azure console
2. Click to expand more settings and set the customized address to：

`https://{your-custom-name}.openai.azure.com/openai/deployments/{you-deployment-name}/chat/completions?api-version=2023-03-15-preview`

Change `{your-custom-name}` to your own subdomain and `{you-deployment-name}` to your own deployment name.

3. The model name needs to be manually selected for the custom model to read： `gpt-35-turbo`,

> If there are still questions, you can go inside Azure AI Studio, open PlayGround, [View Code], and there will be the final [EndPoint] and [Key] at the bottom, as follows：

![](/assets/docs/doc-assets/azure-openai-key.jpg)

## Customizing OpenAI's API Address

- This can be configured via `More Settings` with the following entry point

***

<img width="951" alt="Snipaste_2023-04-08_19-29-18" src="https://user-images.githubusercontent.com/5794691/230718739-ff661ce3-04af-4391-8efc-9a5a1c8374b0.png"/>

***
