# DeepL

## Direct access to DeepL translation services after opening an [Immersive Translate Pro Membership](https://immersivetranslate.com/en/pricing/) (Recommended)

[Learn More](https://immersivetranslate.com/en/pricing/)

## Get the official DeepL API via DeepL

1. Official Introduction:[DeepL API](https://www.deepl.com/en/pro#developer)

   - Note that: [DeepL API](https://www.deepl.com/en/pro#developer) and [DeepL Pro](https://www.deepl.com/pro) are two different account types, and the [DeepL API](https://www.deepl.com/en/pro/select-country#developer) account.

2. [Why](https://www.deepl.com/en/whydeepl) choose DeepL?

   - English ⇄ Chinese 5x more accurate
   - English ⇄ Japanese 6x more accurate
   - Translation engine based on artificial intelligence technology (neural networks)

3. The Deepl API is divided into [Free API and Pro API](https://www.deepl.com/en/pro#developer)

   - The Free API provides 500,000 free characters per month.
   - The [official fee](https://www.deepl.com/en/pro#developer) for the Pro API is:$25 per 1 million characters.
   - For a high-frequency user, the amount of characters consumed in a month is about 10 million characters, and the price is about: 250 USD

4. To register for an account and open the [DeepL API](https://www.deepl.com/en/pro#developer).

## common problems

### 1. The filled-in key is not available.

DeepL API Pro and DeepL Pro are two kinds of accounts, the Auth Key that can be used in Immersive Translate is the DeepL API account, please click here for [DeepL API Pro](https://www.deepl.com/en/pro/select-country#) developer)

### 2. Troubleshooting 401, 403 Authentication Errors

These errors typically occur when you're using the wrong type of authentication key. Please note:

1. DeepL offers two different products: DeepL Pro (translation service) and DeepL API (developer interface)
2. The keys found in your DeepL Pro account settings are **not compatible** with API calls
3. You need to specifically register for a DeepL API account to obtain an API key
4. DeepL Free API keys are identified by ending with `:fx`
5. DeepL Pro API keys don't have the `:fx` suffix and appear as a regular string of characters

Please ensure you've properly registered for the DeepL API service, not just the DeepL Pro translation service.

### 3. 456, Quota for user has been reached.

Usage has exceeded DeepL's official hard limit cap per user, you may have violated DeepL's fair use policy and are advised to avoid such behavior.If you are a paid subscriber, the usage will be automatically reset next month.
