---
sidebar_position: 4
---

# Advanced Customization Options

You can edit more custom configurations that are not available in the UI in the extension configuration page -> Developer Settings -> User Config. This is suitable for advanced users. For parameter explanations, please refer to the final instructions. The current built-in `config` can be found [here](https://dash.immersivetranslate.com/#developer), by clicking `Click to expand the final config`.

## User Rules

Through `Rules`, you can customize configurations for specific websites, deciding what content needs to be translated, adjusting webpage styles, etc.

```json
[
  {
    "matches": "www.google.com",
    "selectors": [".title"]
  },
  {
    "matches": "twitter.com",
    "selectors": [".text"],
    "excludeSelectors": ["nav", "footer"]
  }
]
```

Use `matches` to match corresponding websites. Wildcards are allowed, such as `*.google.com`, `www.google.com/test/*`, `file://*`.

Using `selectors` will override the smart translation scope, only translating elements matched by this selector.

Using `excludeSelectors` can exclude elements, not translating them.

Using `selectors.add` will add some selectors on top of the default ones.

Using `selectors.remove` will remove some selectors from the default ones.

```json
[
  {
    "matches": "www.google.com",
    "selectors.add": ["baidu.com"],
    "excludeSelectors": ["buzzing.cc"]
  }
]
```

If you want an element to be treated as a whole and not broken into lines when translating a certain area, you can use the `atomicBlockSelectors` selector. For example, Instagram's bio. Note that you need to use `selectors` to select the area before using `atomicBlockSelectors`.

```json
{
  "matches": "https://www.instagram.com/*",
  "selectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"],
  "atomicBlockSelectors": ["div._aa_c h1", "li._acaz div[role=\"menuitem\"]"]
}
```

If the translated text causes page misalignment, text overlap, or other edge cases, you can use `globalStyles` to adjust the webpage style for a fix. For example, YouTube titles, used to remove the original webpage's max-height.

```json
{
  "matches": "www.google.com",
  "globalStyles": { ".title": "max-height:unset;" }
}
```

## Injected CSS

You can inject custom webpage styles globally through Injected CSS. It can be used together with `Rules`' `translationClasses`.

```css
.immersive-translate-target-wrapper img {
  width: 16px;
  height: 16px;
}
```

You can also design more personalized styles for websites like a regular webpage style manager (even use `display:none` to block ads).

```css
.title {
  color: red;
}
```

## User Config

Through Config, you can customize relevant configurations of this plugin, such as translation services, specific language translation options, etc.

```json
{
  "translationService": "tencent",
  "translationServices": {
    "tencent": {
      "secretId": "xxx",
      "secretKey": "xxx",
      "matches": ["twitter.com"]
    }
  },
  "translationUrlPattern": {
    "excludeMatches": ["www.google.com"]
  },
  "translationLanguagePattern": {
    "matches": ["en"]
  },
  "translationTheme": "none",
  "translationThemePatterns": {
    "underline": {
      "matches": ["discord.com"]
    }
  },
  "sourceLanguageUrlPattern": {
    "en": {
      "matches": ["*.google.com"]
    }
  },
  "generalRule": {
    "_comment": "",
    "normalizeBody": "",
    "injectedCss": [],
    "additionalInjectedCss": [],
    "wrapperPrefix": "smart",
    "wrapperSuffix": "smart",
    "isPdf": false,
    "isTransformPreTagNewLine": false,
    "urlChangeDelay": 20,
    "isShowUserscriptPagePopup": true,
    "observeUrlChange": true,
    "paragraphMinTextCount": 8,
    "paragraphMinWordCount": 2,
    "blockMinTextCount": 32,
    "blockMinWordCount": 5,
    "containerMinTextCount": 18,
    "lineBreakMaxTextCount": 0,
    "globalAttributes": {},
    "globalStyles": {},
    "selectors": [],
    "preWhitespaceDetectedTags": ["DIV", "SPAN"],
    "stayOriginalSelectors": [],
    "additionalSelectors": [],
    "atomicBlockTags": [],
    "excludeSelectors": [],
    "additionalExcludeSelectors": [],
    "translationClasses": [],
    "atomicBlockSelectors": [],
    "excludeTags": [],
    "metaTags": ["META", "SCRIPT", "STYLE", "NOSCRIPT"],
    "additionalExcludeTags": [],
    "stayOriginalTags": ["CODE", "TT", "IMG", "SUP"],
    "additionalStayOriginalTags": [],
    "inlineTags": [],
    "additionalInlineTags": [],
    "extraInlineSelectors": [],
    "additionalInlineSelectors": [],
    "extraBlockSelectors": [],
    "allBlockTags": [],
    "pdfNewParagraphLineHeight": 2.4,
    "pdfNewParagraphIndent": 1.2,
    "pdfNewParagraphIndentRightIndentPx": 130,
    "fingerCountToToggleTranslagePageWhenTouching": 4
  },
  "rules": [
    {
      "matches": "www.google.com",
      "selectors": [".class"]
    }
  ]
}
```

Among them, the rule fields in `rules` can use all the fields in `generalRule`. `rules` have the highest priority. When a specific `rule` for a website is matched, the rules from `generalRule` and that `rule` will be merged.

Here are some common fields in Config.

### Allow Rendering Normal HTML Tags

Go to [Developer Settings](https://dash.immersivetranslate.com/#developer) -> Edit Full User Config

Edit "enableRenderHtmlTag": true

### Do Not Display Unconfigured Translation Services in the Popup Panel

`"showUnconfiguredTranslationServiceInPopup": false`

### Translation Service Configuration

Use `translationService` to select the default translation engine. Currently supported:

```typescript
| "bing"
| "transmart"
| "google"
| "deepl"
| "openai"
| "gemini"
| "baidu"
| "volc"
| "youdao"
| "caiyun"
| "tencent"
| "openl"
```

Use `translationServices` to configure the `apikey` for each translation service. Different service providers require different parameters. Their API keys can all be applied for in their respective official website's developer center.

For example, Tencent Translate (腾讯翻译君) requires configuring `secretId`, `secretKey`. You can go to Tencent Cloud to apply for an API key, with 5 million free characters per month. For the specific application process, refer to [here](/docs/services/tencent).

```json
"translationServices": {
  "tencent": {
    "secretId": "xxx",
    "secretKey": "xxx",
    "matches":["twitter.com"],
    "limit": 3,
    "apiUrl":"",
    "maxTextGroupLengthPerRequest": 25,
    "maxTextLengthPerRequest": 1800
  }
}
```

The `matches` field is for using this translation service for specific websites.

The `limit` field specifies the maximum number of requests per second for this translation service (some services limit the maximum number of requests per second).

The `maxTextGroupLengthPerRequest` field is the maximum number of paragraphs per request.

The `maxTextLengthPerRequest` field is the maximum number of characters per request.

`apiUrl` can customize the address of the translation interface.

#### OpenAI Temperature Setting

OpenAI's "temperature" parameter is used to adjust the randomness and creativity of the language model's output text. Setting a lower temperature value (e.g., 0.1 or 0.2) will generate more deterministic, consistent, and predictable text, while a higher temperature value (e.g., 0.8 or 1.0) will make the output more random and diverse, increasing the text's creativity.

The specific setting is in [Developer Settings](https://dash.immersivetranslate.com/#developer) -> Edit Full User Config. Find the corresponding field for `openai` and insert a new field `temperature` to complete the setting.

Example:

```json
  "translationServices": {
    "openai": {
      "model": "gpt-3.5-turbo",
      "provider": "custom",
      "temperature": 1
    }
  },
```

### Always Translate Specific Websites

`translationUrlPattern` configures websites to always translate and websites to never translate.

- `matches` configures websites to always translate.
- `excludeMatches` configures websites to never translate.

The configuration value can be a domain name or a URL with `*`, for example: `www.google.com/mail/*`

```json
"translationUrlPattern": {
    "matches": ["stackoverflow.com"],
    "excludeMatches": ["www.google.com/mail/*"]
}
```

### Always Translate Specific Languages

`translationLanguagePattern`, configures languages to always translate and languages to never translate.

- `matches` configures languages to always translate, e.g., `en`.
- `excludeMatches` configures languages to never translate.

### Translated Text Display Format

`translationTheme` is the display format for translated text. Currently supported styles:

```typescript
| "none"
| "dashed"
| "dotted"
| "underline"
| "mask"
| "paper"
| "highlight"
| "blockquote"
| "weakening"
| "italic"
| "bold"
| "thinDashed";
```

Corresponding Chinese names:

```json
{
  "none": "None",
  "dashed": "Dashed Underline",
  "dotted": "Dotted Underline",
  "underline": "Solid Underline",
  "mask": "Blur Effect",
  "paper": "Paper Shadow Effect",
  "highlight": "Highlight",
  "blockquote": "Blockquote Style",
  "weakening": "Weaken",
  "italic": "Italic",
  "bold": "Bold",
  "thinDashed": "Thin Dashed Underline"
}
```

`translationThemePatterns` can configure different translated text styles for different websites.

```json
"translationThemePatterns": {
  "underline": {
    "matches": ["discord.com"]
  }
}
```

### GPT-like Page Stream Message Translation

```json
{
  "matches": ["chat.openai.com"], // GPT-like website URL
  "excludeSelectors": [".markdown *"],
  "aiRule": {
    "streamingSelector": ".result-streaming.markdown",
    "messageWrapperSelector": ".markdown",
    "streamingChange": true
  }
}
```

### Custom Translation of Technical Terms

The current solution works by having the translation service preserve placeholders, so complete replacement cannot be fully guaranteed.

Due to some translation engines' suboptimal recognition of proper nouns, we can customize technical terms to ensure they are not converted during translation or are translated according to our settings. If you wish not to translate certain technical terms, click [here](https://dash.immersivetranslate.com/#advanced) to add the corresponding words. If you wish to translate certain technical terms into specific content, you can do so [here](https://dash.immersivetranslate.com/#developer).

[We will replan the terminology function soon, and will provide more flexible configuration methods then.]

- 【Edit Full User Config】Input the following configuration to achieve this:

Note that the `glossaries` key-value pair is placed under the `generalRule` key-value pair.

```json
"glossaries": [
    {
      "k": "LLM",
      "v": ""
    },
    {
      "k": "Tactic",
      "v": "Strategy"
    }
  ]
```

```json
"generalRule": {
  "glossaries": [...],
  ...
}
```

### Rules

`rules` is an array of objects that can configure rules for specific websites, for example, to make Twitter only translate a certain area:

```json
[
  {
    "selectors.remove": ["[data-testid=\"tweetText\"]"],
    "selectors.add": [""],
    "excludeSelectors.add": [""],
    "excludeSelectors.remove": [""],
    "id": "twitter"
  }
]
```

The current built-in `rules` can be found [here](https://github.com/immersive-translate/next-immersive-translate/blob/main/docs/buildin_config.json).

The following selects some important fields for explanation:

```typescript
export interface Rule {
  // Match website
  id?: string; // Each system-adapted rule has its own id. If the user wants to reuse this rule and make changes on top of it, they need to add this corresponding id to their own rule to reuse it.
  matches?: string | string[]; // This Rule will only match the websites here.
  excludeMatches?: string | string[]; // Exclude specific websites.
  selectorMatches?: string | string[]; // Match using selectors without specifying all URLs.
  excludeSelectorMatches?: string | string[]; // Exclusion rule, same as above.

  // Specify translation scope
  selectors?: string | string[]; // Only translate matched elements.
  excludeSelectors?: string | string[]; // Exclude elements, do not translate matched elements.
  excludeTags?: string | string[]; // Exclude Tags, do not translate matched Tags.

  // Append translation scope, instead of overriding
  additionalSelectors?: string | string[]; // Append translation scope. In the smart translation area, append translation positions.
  additionalExcludeSelectors?: string | string[]; // Append excluded elements, so smart translation does not translate specific positions.
  additionalExcludeTags?: string | string[]; // Append excluded Tags.

  // Keep original
  stayOriginalSelectors?: string | string[]; // Matched elements will remain original. Often used for tags on forum websites.
  stayOriginalTags?: string | string[]; // Matched Tags will remain original, e.g., `code`.

  // Area translation
  atomicBlockSelectors?: string | string[]; // Area selector, matched elements will be treated as a whole and not translated in segments.
  atomicBlockTags?: string | string[]; // Area Tag selector, same as above.

  // Block or Inline
  extraBlockSelectors?: string | string[]; // Additional selectors, matched elements will be treated as block elements, occupying a full line.
  extraInlineSelectors?: string | string[]; // Additional selectors, matched elements will be treated as inline elements.

  inlineTags?: string | string[]; // Matched Tags will be treated as inline elements.
  preWhitespaceDetectedTags?: string | string[]; // Matched Tags will automatically wrap lines.

  // Translated text style
  translationClasses?: string | string | string[]; // Add extra Class to the translated text.

  // Global styles
  globalStyles?: Record<string, string>; // Modify page styles. This is very useful if the translated text causes page layout issues.
  globalAttributes?: Record<string, Record<string, string>>; // Modify attributes of page elements.

  // Embedded styles
  injectedCss?: string | string[]; // Embed CSS styles.
  additionalInjectedCss?: string | string[]; // Append CSS styles, instead of directly overriding.

  // Context
  wrapperPrefix?: string; // Prefix for the translated text area, defaults to smart, decides whether to wrap lines based on word count.
  wrapperSuffix?: string; // Suffix for the translated text area.

  // Translated text line break word count
  blockMinTextCount?: number; // Minimum character count for the translated text to be treated as a block, otherwise it's an inline element.
  blockMinWordCount?: number; // Same as above. If you want them to always wrap, you can fill in 0 for both.

  // Minimum word count for translatable content
  containerMinTextCount?: number; // During smart recognition, the minimum number of characters an element must contain to be translated, defaults to 18.
  paragraphMinTextCount?: number; // Minimum character count of the original paragraph, content exceeding this number will be translated.
  paragraphMinWordCount?: number; // Minimum word count of the original paragraph.

  // Forced line break word count for long paragraphs
  lineBreakMaxTextCount?: number; // When translating long paragraphs, the maximum character count for a paragraph to be forcibly broken into lines.

  // Timing for starting translation
  urlChangeDelay?: number; // After entering the page, delay translation by how many milliseconds. To wait for webpage initialization, currently defaults to 250ms.
  observeUrlChange?: boolean; // Detect when the URL address changes and start translation again, defaults to true.

  // Mobile
  isShowUserscriptPagePopup?: boolean; // Display the in-page floating window on mobile devices, defaults to true.
  fingerCountToToggleTranslagePageWhenTouching?: number; // Translate with a four-finger touch, can be set to 0, 2, 3, 4, 5.

  // AI streaming translation
  aiRule: {
    streamingSelector: string; // Selector for the element being translated in a GPT webpage.
    messageWrapperSelector: string; // Message body selector.
    streamingChange: boolean; // Whether repeated messages on GPT-like webpages are incrementally updated or fully updated. GPT is incremental.
  };
}
```

### Rules Matches Matching Logic

This section introduces the matching method for `match`, how to match the corresponding domain name. Here we are talking about a single `match`. During actual matching, `matches` is an array, and it will try to match each `match`. As long as one matches, it is considered a hit.

First, let's determine the input format, i.e., what forms of legal input our `match` supports:

- `url` with omitted host, e.g., `immersivetranslate.com`
- A legal `url` with its own protocol, domain name, or path, e.g., `https://immersivetranslate.com`
- If none of the above are met, the input will be converted into a regular expression for processing, and then some specific rules will be matched on this basis.

After determining the input, let's make a simple classification to better distinguish basic `url`s from `url`s with regular expressions:

- `match` that matches a single website, e.g., `https://immersivetranslate.com` or `immersivetranslate.com` with omitted protocol.
- `match` mixed with regular expression special characters, e.g., `https://*/*sub.info=*fmoviesz.to*`. This will match specific search `url` parameters. Our program will automatically convert the latter string into a regular expression to match the corresponding `url`. The converted result is `/^https:\/\/[^/]+?\/.*?sub.info=.*?fmoviesz.to.*?\/?$/`. The advantage of this is that it greatly reduces the complexity of configuring `match`.

After distinguishing, for these two types of `match`, we will explain the corresponding matching logic separately. This is also the case in the code; the matching logic for these two types is separate. In the code, we distinguish these two types of `match` through this expression: `!match.includes("*") && match.includes("://")`.

For `match` strings that match a single site, i.e., those without regular expression related symbols, there are three issues to consider:

- Handling of `match` with omitted network protocol: For `immersivetranslate.com`, we will directly judge whether `match` is equal to the `hostname` of the `url`. If equal, the match is successful, i.e., `match` will not be parsed as a URL, but will be used as a `hostname` for judgment.
- Handling of multi-level routing, divided into two cases:
  - Complete `match`, e.g., `https://immersivetranslate.com/docs/advanced/`. These are legal URLs. We will parse them as URLs and extract the protocol, hostname, port number, and pathname for comparison. When all are equal, the match is successful.
  - `match` with omitted network protocol, e.g., `immersivetranslate.com/docs/advanced/`. Since these are illegal `url`s, they will be classified into the regular expression logic for processing.

When the above matching strategies are not effective, our fallback matching will be used, i.e., it will be recognized as a regular expression. We will convert `match` into a legal regular expression. An example of this can be found here:

> `https://*/*sub.info=*fmoviesz.to*` ==> `/^https:\/\/[^/]+?\/.*?sub.info=.*?fmoviesz.to.*?\/?$/`

Finally, let's summarize our processing logic: 1. Judge whether the `hostname` of the `url` is equal to the `match` string. If equal, the match is successful. 2. Judge `match`es that match all `url`s, e.g., `*`, `*://*`, etc. 3. Judge whether `match` is a legal `url`. We will try to compare whether `match` and `url` are equal. Specifically compare protocol, port, hostname, pathname. If equal, success. 4. Judge `match` as a regular expression, convert it into a legal regular expression and try to match. 5. If none are met, the match fails.

### Translation Service Custom Request Headers and Body Parameters

In 【[Developer Settings](https://dash.immersivetranslate.com/#developer)】->【Edit Full User Config】

```json
{
  ...
  "translationServices": {
    "claude": {
      "headerConfigs": {
        "anthropic-version": "2023-06-01",
        "anthropic-dangerous-direct-browser-access": "true"
      },
      "bodyConfigs": {
        "max_tokens": 2048
      }
    }
  ...
}
}
```

#### Gemini series model users how to customize configuration

Due to the special nature of the Gemini series models, the plugin has built-in some settings. If users want to override the built-in settings, they can refer to the following configuration:

```json
{
...
"translationServices": {
    "gemini": {
      "modelsOverrides": [
        // Specify the model to be overridden, here we override the gemini-2.5-flash and gemini-2.5-flash-lite two models
        "models": [
          "gemini-2.5-flash",
          "gemini-2.5-flash-lite"
        ]
      ]
    }
  },
...
}
```

### Custom Translation Token Ratio Validation

> To mitigate the "hallucination" phenomenon of Large Language Models, we have a built-in translation quality validation mechanism. The program evaluates the reasonableness of the result by calculating the token ratio between the response text and the request text. If this ratio is abnormal (too high or too low), the translation will be considered invalid and a fallback will be triggered.
>
> If you intend for the model to output content with a length significantly different from the original text in "Custom Expert Mode" (e.g., for tasks like summarization or expansion), you may need to adjust this validation setting. You can override the default behavior with the following options to ensure your custom instructions execute correctly.
>
> Specifically, you can adjust the following two parameters:
>
> - `maxTokensRatio`: Defines the maximum allowed token ratio between the response text and the request text. If the actual ratio exceeds this value, the system will deem the response too long and consider it invalid.
> - `minTokensRatio`: Defines the minimum allowed token ratio between the response text and the request text. If the actual ratio is below this value, the system will deem the response too short and consider it invalid.

```json
...
  "translationServices": {
    "claude": {
      "maxTokensRatio": 8,
      "minTokensRatio": 0.21,
    }
  ...
```

### Modify Default Translation Cache Auto-Cleanup Duration

The plugin defaults to automatically clearing the translation cache every 30 days. The purpose is to prevent the cache from becoming too large, which could cause subsequent translations to lag. You can modify the default value as follows:

In 【[Developer Settings](https://dash.immersivetranslate.com/#developer)】->【Edit Full User Config】

```
{
  cacheMaxAgeDay: 30,
  ...
}
```

### Custom Multilingual Prompts

Below shows the prompt modification for OpenAI translating Japanese/Traditional Chinese.

```
{
  ...
  "translationServices": {
    "openai.add": {
        "langOverrides": [
          {
          "id": "auto2ja",
          "systemPrompt": "あなたはプロフェッショナルで正確な翻訳エンジンです。翻訳されたテキストのみを返し、説明は一切行いません。",
          "prompt": "次のテキストを{{to}}に翻訳してください：\n\n<text>\n{{text}}\n</text>\n\n翻訳結果を直接出力し、追加のテキストやタグは一切含めないでください。",
          "multiplePrompt": "\"id\"フィールドと \"{{imt_source_field}}\" フィールドを含むYAML形式の入力が与えられます。以下が入力です：\n\n<yaml>\n{{yaml}}\n</yaml>\n\nYAMLの各エントリについて、\"{{imt_source_field}}\" フィールドの内容を {{to}} に翻訳してください。そのエントリの \"{{imt_source_field}}\" フィールドに翻訳結果を書き戻してください。\n\n以下は期待される形式の例です：\n\n{{normal_result_yaml_example}}\n\n追加のタグを一切含めずに、翻訳されたYAMLを直接返してください。",
          "subtitlePrompt": "YAML形式のビデオ字幕セットの \"{{imt_sub_source_field}}\" フィールドを {{to}} に翻訳します。以下がYAML形式の元の字幕です：\n\n<yaml_subtitles>\n{{yaml}}\n</yaml_subtitles>\n\n各字幕エントリの \"{{imt_sub_source_field}}\" フィールドのみを簡体字中国語に翻訳してください。\"id\" フィールドは翻訳や変更をしないでください。\n\n翻訳された字幕を同じYAML形式で出力し、各字幕エントリを一行ずつにしてください。\"id\" フィールドは変更せず、\"{{imt_sub_source_field}}\" フィールドに {{to}} の翻訳を含めてください。\n\n追加のタグを一切含めずに、翻訳されたYAMLを直接返してください。"
        },
        {
          "id": "auto2zh-TW",
          "systemPrompt": "You are a professional and authentic translation engine. You only return the translated text, without any explanation.",
          "prompt": "Translate the following text to {{to}}:

<text>
{{text}}
</text>

Output the translation result directly, without adding any extra text or tags.",
          "multiplePrompt": "You will be given a YAML format input containing \"id\" and \"{{imt_source_field}}\" fields. Here is the input content:

<yaml>
{{yaml}}
</yaml>

For each entry in YAML, translate the content of the \"{{imt_source_field}}\" field to {{to}}. Write the translation result back to the \"{{imt_source_field}}\" field of each entry.

Here is an example of the expected format:

{{normal_result_yaml_example}}

Please return the translated YAML directly, without adding any extra tags.",
          "subtitlePrompt": "You will translate the \"{{imt_sub_source_field}}\" field in a set of YAML formatted video subtitles to {{to}}. Below is the original subtitles in YAML format:

<yaml_subtitles>
{{yaml}}
</yaml_subtitles>

Please only translate the \"{{imt_sub_source_field}}\" field in each subtitle entry to Simplified Chinese. Do not translate or change the \"id\" field.

Output the translated subtitles in the same YAML format, with each subtitle entry on a separate line. The \"id\" field should remain unchanged, and the \"{{imt_sub_source_field}}\" field should contain your {{to}} translation result.

Please return the translated YAML directly, without adding any extra tags."
        }
        ]
      }
    }
  ...
}
```

## Advanced Customization Options in Practice

### Practical Tips

This section will introduce some plug-and-play, easy-to-follow configurations.

Copy these configurations with one click, open [Developer Settings](https://dash.immersivetranslate.com/#developer), expand `Edit Full User Config`, and paste it as the last item. Remember not to forget to add a comma to the previous item, and the last item cannot have a comma.

#### Too many unusable translation services, how to display only usable translation services in the plugin panel?

```json
  "showUnconfiguredTranslationServiceInPopup": false
```

#### How to make different sites select different translation services by default? For example, for some websites I want better translation quality that costs money, while for others I only need free translation that is understandable.

Look, this configuration is called Translation Service. It has configured Google Translate to be used for all translations related to Twitter sites because `google` translate is free, and Twitter is for browsing, so it just needs to be understandable.

Look closely, it has also configured the `deepl` translation service. It makes `deepl` specifically translate academic websites like `scihub` which have low fault tolerance and require high precision.

```json
  "translationServices": {
    "google": {
      "matches":["https://twitter.com"]
    },
    "deepl": {
      "matches":["https://www.sci-hub.se"]
    }
  }
```

> ⚠️ Please note that if you wish to translate all websites belonging to the same domain, simply using _.twitter.com or https://twitter.com/ is invalid. The correct approach should follow the example shown above. This is because _.twitter.com can only match subdomains like xxx.twitter.com, but not the top-level domain itself.

### Website Adaptation Cases

This section will introduce some `rules` that the plugin itself has for common websites, to understand advanced customization options through practical examples. For simplicity, only the most commonly used fields will be introduced here, such as `selectors`, `excludeSelectors`, etc. If you are interested in this part, please contact us, and we will continue to update relevant content.

Before we begin, a very crucial thing is the working principle of the Immersive Translate plugin, which is also the working principle of a plugin. Before this, you need to have a certain foundation in `HTML`, `CSS`, and `JavaScript`. Related basics can be learned on the `MDN` website. Okay, without further ado, let's delve into the internals of Immersive Translate. Simply put, the working mechanism of a plugin is to inject third-party scripts into the webpage. These scripts can freely modify the webpage structure, style, and even behavior.

Our Immersive Translate plugin is no exception. Let's briefly analyze what Immersive Translate does:

- Get the set of elements to be translated.
- Translate the text in the set of elements.
- Insert the translation result into the set of elements.

Okay, but if you think about it more carefully, two questions will naturally arise:

- We also need to determine which elements need to be translated. If everything is translated, it will often destroy the user's immersive experience, such as some simple and clear buttons or navigation bars.
- Inserting the translation result into the set of elements also brings a new challenge: how to ensure that the inserted result is consistent with the native webpage and does not affect the style of the native webpage.

The core of our `Rules` is to solve the above two problems. Because as a plugin, Immersive Translate faces all webpages on the market, which may add up to hundreds of thousands, or even millions of webpages. The page structures and technologies used by these webpages are also very different. Due to the differences in webpages, a universal logic is almost impossible. It is difficult to find a set of universal logic that can adapt to all website content. In this way, the solution seems to be to adapt each website individually. Then, to make adaptation more convenient, we used the idea of configuration as code, transforming the adaptation work into the work of configuring fields. Another advantage of this is that users can also participate in the adaptation work.

At the same time, when configuring, it is best not to directly use the following fields, as this will overwrite the original configuration items. Instead, use fields like `selector.add` and `excludeSelector.add` to modify on the basis of the original configuration items in an inherited manner.

Next, we will introduce Immersive Translate's adaptation work for sites.

Below are the Rules for Twitter. For simplicity, we will focus on a few key fields. The remaining fields can be understood in conjunction with the `Rules` in the previous text.

```json
[
  {
    "id": "twitter",
    "matches": [
      "twitter.com",
      "mobile.twitter.com",
      "tweetdeck.twitter.com",
      "pro.twitter.com",
      "https://platform.twitter.com/embed*"
    ],
    "selectors": [
      // Specify the elements to be translated; only elements matched by the selector will be translated
      "[data-testid=\"tweetText\"]",
      ".tweet-text",
      ".js-quoted-tweet-text",
      "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)",
      "[data-testid='developerBuiltCardContainer'] > div:nth-child(2)",
      "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)",
      "[data-testid='cellInnerDiv'] div[data-testid='UserCell'] > div> div:nth-child(2)",
      "[data-testid='UserDescription']",
      "[data-testid='HoverCard'] div[dir=auto]",
      "[data-testid='HoverCard'] span[dir=auto]",
      "[data-testid='HoverCard'] [role='dialog'] div[dir=ltr]",
      "[data-testid='birdwatch-pivot'] div[dir=ltr]"
    ],
    "excludeSelectors": [
      // Elements selected by CSS selectors that will not be translated
      "[aria-describedby][role=button]",
      "header",
      "[data-testid='radioGroupplayback_rate'] div",
      "[data-testid='userFollowIndicator']",
      "[class='css-901oao r-14j79pv r-37j5jr r-n6v787 r-16dba41 r-1cwl3u0 r-bcqeeo r-qvutc0']",
      "[class='css-175oi2r r-1wbh5a2 r-dnmrzs']"
    ],
    "globalStyles": {
      // Global styles, forcibly override original styles
      "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='tweetText']": "-webkit-line-clamp: unset;"
    }
  }
]
```

- `selector`: Specifies the set of elements to be translated.

  Why is this field needed?

  - Because not all elements have text and need to be translated, providing such a field can ensure both performance and the user's immersive experience.

  Example:

  - In Twitter, if we don't specify `selector`, it will translate all text recognized as English on the page. As shown in the figure below, user nicknames often do not need to be translated.

  ![User Profile](twitterUser.png)

  Field Meaning:

  ```
      "selectors": [ // Collection of CSS selectors to be translated
      "[data-testid=\"tweetText\"]",
    ]
  ```

  Each item in the array here is a CSS selector used to select the elements on the page that need to be translated. Here we take the first selector as an example. As shown in the figure below, the first selector hits all tweet elements.

  ![tweet](tweet.png)

- `excludeSelectors`: Collection of elements that will not be translated.

  Why is this field needed?

  - Because a translate-only selector is not enough. It may happen that matched elements do not need to be translated, meaning there might be an overlap between the two. Therefore, another field needs to be set to exclude elements that do not need to be translated.
  - Because the page structure is very complex, providing these two configuration items makes the configuration more flexible.
  - The relevant priority is: for selectors of equal specificity, `selectors` > `excludeSelectors`. The rest depends on CSS priority for comparison.

  Field Meaning:

  ```
      "excludeSelectors": [ // Elements selected by CSS selectors that will not be translated
      "[aria-describedby][role=button]",
    ],
  ```

  Still looking at the first one, here we have excluded the translation of the follow button.
  ![twitter-follow](twitter-follow.png)

- `globalStyles`: Add global styles, forcibly overriding the original styles.

  Why is this field needed?

  - In some cases, due to the relevant CSS styles of the original webpage, the overall translation display effect may not be very good, with issues like truncation, no line breaks, etc.
  - This field provides a brute-force solution to directly modify the CSS properties of the native webpage to solve the problem.

  Field Meaning:

  ```
        "globalStyles": {
      // Global styles, forcibly override original styles
      "[data-testid='card.layoutLarge.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='card.layoutSmall.detail'] > div:nth-child(2)": "-webkit-line-clamp: unset;",
      "[data-testid='tweetText']": "-webkit-line-clamp: unset;"
    }
  ```

  The `-webkit-line-clamp` property is used to control the number of lines displayed; excess lines will be truncated. Setting it to `unset` here ensures that the translated text will not be truncated by this property.

### Custom Website Adaptation

Regarding adaptation rules, of course, you can also customize rules. Go to the plugin options page, click [Developer Settings](https://dash.immersivetranslate.com/#developer), expand `Edit User Rules`, and perform custom adaptation for various websites here. The following explains with actual rules.

```
[
  {
    "selectors.remove": [
      "[data-testid=\"tweetText\"]"
    ],
    "selectors.add": [
      ""
    ],
    "excludeSelectors.add":[
      ""
    ],
    "excludeSelectors.remove":[
      ""
    ],
    "id": "twitter"
  }
]
```

This rule will prevent tweets on the Twitter page from being translated. The meaning of the fields is detailed below.

`id` is a collection of relevant websites that Immersive Translate has currently defined. Each `id` corresponds to relevant sites. There are two benefits of using `id`:

- Using `id` can inherit Immersive Translate's previous adaptation rules, and users can add or delete on this basis.
- Using `id` eliminates the need to write tedious matching fields.

Below are some common `id`s for Immersive Translate's built-in services:

- `"isEbook"`: Configuration for epub reader pages.
- `"isEbookBuilder"`: Configuration for generating bilingual epub book pages.
- `"pdf"`: Configuration for PDF bilingual comparison translation pages.

The complete `id` collection can be found in [Developer Settings](https://dash.immersivetranslate.com/#developer), under `Click to expand the final config`.

`selectors` is responsible for specifying the CSS selectors to be translated. It is recommended to use sub-items `.add` and `.remove` to add or delete on the original basis.

`excludeSelectors` is responsible for excluding CSS selectors that do not need to be translated. It is recommended to use sub-items `.add` and `.remove` to add or delete on the original basis.

**More Explanation**

The difference between Block and inline, if you want to learn more, you can look [here](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements#inline).

- Block elements will occupy a full line, and multiple adjacent block elements will each start on a new line.
- Inline elements will not occupy a full line; multiple adjacent inline elements will be arranged on the same line until the line cannot accommodate more, then they will wrap to a new line.
