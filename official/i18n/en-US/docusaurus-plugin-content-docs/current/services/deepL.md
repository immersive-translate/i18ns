# DeepL

## Direct access to DeepL translation services after opening an [Immersive Translate Pro Membership](https://immersivetranslate.com/en/pricing/) (Recommended)

[Click here for presentation](https://immersivetranslate.com/en/pricing/)

## Get the official DeepL API via DeepL

1. Official Introduction：[DeepL API ](https://www.deepl.com/en/pro#developer)
   - Note that： [DeepL API](https://www.deepl.com/en/pro#developer) and [DeepL Pro](https://www.deepl.com/pro) are two different account types, and the [DeepL API](https://www.deepl.com/en/pro/select-country#developer) account.

2. [Why](https://www.deepl.com/en/whydeepl) choose DeepL?

   - English ⇄ Chinese 5x more accurate
   - English ⇄ Japanese 6x more accurate
   - Translation engine based on artificial intelligence technology (neural networks)

3. The Deepl API is divided into [Free API and Pro API](https://www.deepl.com/en/pro#developer)

   - The Free API provides 500,000 free characters per month.
   - The [official fee](https://www.deepl.com/en/pro#developer) for the Pro API is：$25 per 1 million characters.
   - For a high-frequency user, the amount of characters consumed in a month is about 10 million characters, and the price is about：250 USD

4. To register for an account and open the [DeepL API](https://www.deepl.com/en/pro#developer).

<!-- ## Build your own DeepL API

We're experimenting with support for our own DeeplX service in the Beta feature (but it's not well suited as a web translation service, as tested.Due to the huge amount of API requests for web page translation, if you build this service, please make sure to do a good job of load balancing), the following is how to turn on the experimental features of the instructions：

1. Enabling Beta Testing Features in Developer Settings
2. Find DeepLX (Beta) in Basic Settings and enter the self-built DeepL API URL, e.g. http\://your-domain/translate

> Q：How do I build my own?
>
> A：[OwO-Network/DeepLX](https://github.com/OwO-Network/DeepLX#setup-on-immersive-translate) or [zu1k/deepl](https://github.com/KyleChoy/zotero-pdf-translate/blob/CustomDeepL/README.md) -->

## common problems

### 1. The filled-in key is not available.

DeepL API Pro and DeepL Pro are two kinds of accounts, the Auth Key that can be used in Immersive Translate is the DeepL API account, please click here for [DeepL API Pro](https://www.deepl.com/en/pro/select-country#) developer)

### 2. Deepl Free API Prompt 401 No Privilege

Deepl Free API keys all end in `:fx`, anything else is not a Free API key.

### 3. 456, Quota for user has been reached.

Usage has exceeded DeepL's official hard limit cap per user, you may have violated DeepL's fair use policy and are advised to avoid such behavior.If you are a paid subscriber, the usage will be automatically reset next month.
