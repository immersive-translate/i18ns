---
sidebar_position: 9
---

# FAQ

## Security Related

### 1. Android App, floating ball disappeared

Old version add-ons are disabled, uninstall and install the latest version from [official website](https://immersivetranslate.com/).

## Installation Related

### 1. How to update the extension

Generally speaking, extensions installed in the browser store will be automatically updated, usually within one day after the extension is updated. If you want to immediately update to the latest version, you can go to the browser's [Extension Management] page, enable [Developer Mode], and then click [Update] at the top to immediately update to the latest version in the store.

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/update-extension.png)

### 2. Immersive Translate Tampermonkey Supported Browsers

iOS:

- [Tamper Monkey Browser](https://www.tampermonkey.net/)
- Safari browser with Tampermonkey extension installed, compatible extensions:
  - [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)
  - [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171): It's recommended to search for the Immersive Translate Optimization Script directly from Stay's own store (specially optimized for Stay).

Android:

- [Firefox Latest Version](https://www.firefox.com.cn/download/#product-android-release): After installation, install the [Tamper Monkey](https://www.tampermonkey.net/) extension.
- [X Browser](https://www.xbext.com/?ref=immersive-translate): After installation, directly open the [Immersive Translate Tampermonkey script address](https://download.immersivetranslate.com/immersive-translate.user.js) to install.

Known browsers that don't support Tampermonkey extensions (these browsers haven't implemented the required Tampermonkey API):

- Android Via Browser
- iOS Alook Browser

### 3. Error installing plugin installer on chrome

Error `invalid value for web_accessible_resource[0]`: Chromium version greater than 88 is required to support manifest_version 3.

### 4. How to install 360 Browser

Only 360 Extreme Browser X is supported, remember it's with X. If you can access the Google Extensions store, you can go directly there to install it. If you can't access it, [install it manually](/docs/installation/#manual-installation-to-keep-track-of-the-latest-development-features).

### 5. Opera browser does not work

It doesn't work on google.com and other search pages, the plugin displays `Please refresh the current page before starting the translation` and refreshing the page still shows this message: You need to find "Immersive Translate" in the Opera plugin settings and enable the "Allow access to search page results" option.

<!-- ![](https://s.immersivetranslate.com/static/official-static/assets/opera-allow-search.png) -->

### 6. Cannot enable extensions on iOS devices

If you cannot enable extensions on your iOS device, follow these steps:

1. Open the [Settings] app
2. Scroll down and tap [Screen Time]
3. Select [Content & Privacy Restrictions]
4. Tap [Content Restrictions]
5. Select [Web Content] and set it to [Unrestricted]

If you don't need the other features of Content & Privacy Restrictions, you can also choose to simply turn off Content & Privacy Restrictions:

1. Open the [Settings] app
2. Select [Screen Time]
3. Disable [Content & Privacy Restrictions]

### 7. Safari settings page keeps loading

System Settings -> Safari browser -> Advanced -> Website Data -> Edit, find immersivetranslate.com and delete it.

### 8. After installing iOS18, redirected to blank page when logging in from settings page

Long press the floating ball and click on the avatar to log in.

### 9. "File does not exist" when dragging crx file to browser extensions

You need to first extract the zip file, then drag only the CRX file.

### 10. Why is the crx download installing version 1.13.5 instead of the latest

Because your Chrome engine is detected to be below version 115, which doesn't support some advanced features of the plugin, so it automatically downgrades to version 1.13.5.

## Basic Translation Related

### 1. Main content on websites like Youtube, Facebook is translated, but some sidebars are not, I want to translate everything

For the sake of page readability, immersive translation by default only translates the main content area. If you want to translate all areas:

Open the floating ball panel (long press on mobile) -> Click on more in the bottom right corner -> Select all areas.

### 2. Floating Bubble Not Displayed in Apps on Mobile

- The Immersive Translate plugin is a browser plugin that can **only run in browsers**, it cannot be used in other apps, and doesn't support translation within other apps.

- The plugin works only in the browser where it's installed and **cannot work across browsers** (e.g., installing in Safari doesn't allow you to use it in Chrome)

### 3. Clicking on YouTube in iOS browser directly opens the App

Press and hold the YouTube link to pop up a floating window and choose to open in a webpage.

### 4. How to turn off automatic translation

- Cancel in the Popup panel or on the Settings page.
- Or change via the settings page

<img src="https://s.immersivetranslate.com/assets/turn_off_automatic_translation_en.jpeg" alt="turn off automatic translation" width="250" />

### 5. No permission to translate the current page

- Browser default page (no address in address bar)
- Third-party plugin page
- Google plugin disables Google Store page

### 6. How do I not show the original text?

Tap the Immersive Translate icon to open the expansion panel, tap [More], [Switch to Translation Only Mode].

### 7. Exclamation mark appears on the page

An exclamation point on the page indicates that the translation service has encountered a problem and returned an error. You can move your mouse over the exclamation point to view the specific error.

#### Example: 429 Error

This is one of the most common errors, 429 indicating that the frequency of requests is too fast. Web page translation has a very large number of paragraphs to be translated, although we have done great optimization, including merging paragraphs, frequency control, etc., but sometimes there are still some translation services that are overloaded, returning a 429 frequency limit error. In this case, you can usually temporarily switch to other translation services, or wait for a while and try again.

If you're using Google service and experiencing a 429 error, it's generally a case of Google doing a traffic limit against your node, and it's recommended to switch nodes.

### 8. How to switch translation source and target language

On mobile, long press the floating ball; on desktop, move your mouse to the floating ball to bring up settings, select other translation service/other target language.

### 9. Google Translate Interface Walled Off Issue

Please add the `translate.googleapis.com` domain name to the proxy rule.

### 10. Does OpenAI's ban on API Keys in China affect member AI services

No impact, the product uses Azure Enterprise OpenAI, which is not subject to API regional restrictions.

### 11. Color Cloud Translation Error

Clicking on the `?` error message shows "Unsupported trans_type". You can manually select to set the automatically detected language to a specific language.

### 12. WeChat Reading Cannot Be Translated

It cannot be translated because WeChat Reading has done special processing for the content to prevent access to the content through third-party means.

### 13. Some content on web pages is not translated

Generally, it's because the website administrator has defined areas not to be translated using `translate="no"` or `notranslate class`, but you can resolve this by:

1. Enabling mouse hover function
2. Using mouse hover to force translate the paragraph content in that area

### 14. Trigger translation does not take effect

When other sites can be translated but one particular site cannot:

- If this site has fewer visitors
  - It's suggested to translate paragraphs by hovering the mouse
  - If you need to translate the entire site, you can adapt it via [user rules](/docs/advanced/#user-rules)
- If this site is used by a lot of people
  - You can start by using mouse hover to translate
  - Report it in the group, and it will be adapted later

### 15. How do I save my webpage feedback if I have problems with the webpage translation?

You need to right-click "Save as" or use the Ctrl+S shortcut in the web page, choose single file for save option, and save with the file format .mht/.mhtml. Then send the file to support@immersivetranslate.com.

<!-- ![save mht](https://s.immersivetranslate.com/static/official-static/assets/save_mht.png) -->

### 16. Feedback debug log

1. Enable debug logging: Open Panel -> Settings -> Developer Settings -> Enable "Print debug log in console".
2. Open the site's console: Right-click to open inspection -> Switch to the console at the top of the right column -> Perform the action to see the logs.

### 17. How to turn off hoverball

- Hide on current page: Set it to "Never translate this site"
- Hide on all pages: Open [Settings Page] - [Interface Settings] and turn off [Show Hoverball on Page]

### 18. Mouse hover + shortcut key translation function does not work

To enable the mouse hover plus shortcut key translation feature, the page must first have focus. If you find that the feature is not triggering, try these steps:

1. Click anywhere on the page once to ensure the page has focus.
2. Try using the mouse hover and shortcut key for translation again.
3. If the translation function still doesn't respond, check if your shortcut key settings are correct.

### 19. How to update the latest rules

The extension itself will regularly synchronize with the latest official website adaptation rules when you use it. You can also manually synchronize with the latest rules by clicking on the browser's Immersive Translate Extension icon to open a popup window where the extension will automatically detect the latest adaptation rules and synchronize with them. The same applies to Tampermonkey scripts.

### 20. Translation fails / Translation keeps spinning

1. Check the reason for failure:
   - If quota limit is reached, it means the member's monthly quota for that translation source is exhausted
   - If the translation shows a network error, first check your node/network status

2. Switch translation source: long press the floating ball to select another translation source

### 21. How to check Pro member translation quota and usage

- Pro members enjoy a base translation quota of 20 million Tokens per month, which can be used for all translation services. Whether using it all for DeepL (equivalent to 20 million characters), all for OpenAI (20 million Tokens), or a mix of multiple services, you can freely allocate the quota according to your actual needs.

  > OpenAI pricing is based on tokens. For English text, 1 token is approximately 4 characters or 0.75 words. Typically, 1000 Tokens equals about 750 English words or 400-500 Chinese characters.

- Usage inquiry address: [https://immersivetranslate.com/accounts/usage](https://immersivetranslate.com/accounts/usage)

### 22. Why is the plugin's Google translation quality not as good as Google web page translation

Because the plugin calls Google's free API, which is an old API that Google does not continuously maintain, while Google's official webpage translation is continuously maintained. Theoretically, the quality is not as good as Google's official translation, and recently the translation quality of Google's free API has decreased significantly. We recommend switching to other translation services, and we are actively looking for alternative solutions. Related discussion: [#2574](https://github.com/immersive-translate/immersive-translate/issues/2547)

### 23. Showing touch mode when in mouse mode

In [Advanced Settings](https://dash.immersivetranslate.com/#advanced), enable mouse-only mode. Version 1.14.9 will optimize this mode detection.

### 24. Edge cannot read translated text aloud

The read-aloud feature in Edge browser automatically selects voice models based on the original webpage language. Since these voice models are designed for a single language, when the page contains translated text, the default voice model cannot correctly read the translated content.

Solution: You can click on [Voice options] in the Edge read-aloud toolbar, then manually select a voice model that matches the language of the translated text. This will allow the translated content to be read correctly.

## Video Translation Related

### 1. Youtube subtitle setup style

You can click on Youtube's own subtitle settings, [Options], and then you can adjust the size, color, and so on.

![](https://s.immersivetranslate.com/assets/youtube_subtitle_options2_en.jpeg)

### 2. YouTube Bilingual subtitles in traditional Chinese not displayed

YouTube comes with machine-translated subtitles, and Traditional Chinese will have formatting errors, causing all subtitles to pop up with a large section of subtitles at the beginning. Based on this scenario, it is recommended to turn on the [Use Immersive Translate to Translate Subtitles] option in [Settings] [Video Subtitles].

### 3. How to enable subtitle translation for Bilibili

When translating Bilibili video subtitles, please follow these steps:

1. First, enable Bilibili's built-in subtitles by clicking the "Subtitle" button in the bottom right corner of the player. If the video has no subtitle button or subtitle content, bilingual subtitles are not supported.
2. Click the "Immersive Translate" icon in the player to enable the bilingual subtitle feature.

Note when using:

1. Make sure Bilibili's built-in subtitles are enabled.
2. Ensure that Immersive Translate's target language is different from Bilibili's built-in subtitle language to trigger the translation function.

### 4. Netflix subtitle translation using original subtitle style

- The current Netflix approach uses progressive translation, with self-hosted subtitle styling, and doesn't support manual subtitles.
- The old approach requires waiting for all subtitles to be translated before displaying them, but supports manual subtitles.

To revert to the old approach, go to [[Developer Settings](https://dash.immersivetranslate.com/#developer)], find [Edit User Rules]
and add the following rule:

```json
[
  {
    "id": "netflix",
    "subtitleRule.add": {
      "attachRule": {
        "appendSelector": ""
      }
    }
  }
]
```

## File Translation Related

### 1. Translation of local documents

- Method 1: Go to the [Immersive Translate File Translation website](https://app.immersivetranslate.com/), or click the Immersive Translate extension icon and click [File Translation] to enter.

- Method 2: If you are using Chrome-like browsers, such as (Chrome, Arc, Edge browser), there is another way: open the browser extension management page `chrome://extensions`, find the [Immersive Translate] plugin, [Allow the extension to access local files], and then directly in the browser to open the local HTML or local PDF file, you can directly right-click [Translation].

**Note**: Safari browser has strict restrictions on extension access to local files. Safari users should use Method 1 directly - go to the [Immersive Translate File Translation website](https://app.immersivetranslate.com/) to translate local files.

### 2. PDF translation is slow when there are many pages

It is recommended to split the document into multiple parts of less than 100 pages each, translate them separately, and then merge them after translation.

### 3. Duplicate or overlapping translations in PDF

This is due to source file recognition issues. Currently, it is recommended to manually click on that section and delete the extra text boxes. We will continue to optimize this situation in future updates.

### 4. Is there a glossary / special translation or non-translation for certain terms

Version 1.16.1+ supports the [AI Terminology Library](https://dash.immersivetranslate.com/#terms) feature.

The AI terminology library doesn't support Google/Microsoft machine translation terminology by default.

Method to force enable:
(ps: machine translation uses placeholder replacement, terminology may reduce translation quality)

Go to [[Developer Settings](https://dash.immersivetranslate.com/#developer)] -> [Edit Full User Config]

```
{
  ....
  "enableMachineTranslateTerms":true,
  ...
}
```

### 5. Cannot export translated Word files in Word format

Currently, there are some technical issues with Word file export. It is recommended to keep the existing format. We are continuously working on optimization.

### 6. How to adjust the minimum font size in PDFs

This is due to the browser's minimum font size restriction. Adjust the browser font to the lowest setting. For Chrome, for example: click [Chrome font size settings](chrome://settings/fonts?search=%E5%AD%97%E5%8F%B7)

## Input Box Translation Related

### 1. Input box enhancement does not take effect

- Browsers known to be unsupported: See the compatibility section of [Input Box Translation](https://immersivetranslate.com/docs/input/)
- Cannot translate in the URL bar or browser initial page, only supports search bars. You can test at https://www.bing.com/
- Try pressing the space key faster

## Payment Related

### 1. Can I use WeChat Pay

WeChat payments require private messaging staff members in the group and noting "WeChat payment". After the staff provides the payment QR code, make the payment and provide the payment details. The staff will provide the required annual/monthly membership redemption code, which can be redeemed on the [Member Redemption Page](https://immersivetranslate.com/exchange/)

### 2. Can I get an invoice

Currently, only annual memberships can receive invoices. Users who have already paid and need an invoice should private message staff members in the group and note "invoice issue". Unpaid users can check: [Annual Membership Invoice Information](https://immersivetranslate.com/bill/)

## More questions (uncommon)

<details>
<summary>How do I clear my cache with Tampermonkeys?</summary>
<p>
Due to the API limitation of Tampermonkeys, the cache of Immersive Translate Tampermonkeys will be saved in the cache of the corresponding website, so if you want to clear it, you can open the developer tools panel of the corresponding website in your browser and then clear the cache of that website.
</p>
</details>

<details>
<summary>Tampermonkey custom interface address request failed?</summary>
<p>
Tampermonkeys require that all requests from the script need to declare permissions at the beginning of the script, e.g.:`@connect api.google.com`, so if you need to add a new domain name that is not the default, please declare it at the beginning of the Tampermonkey modeled after the other domain name.
</p>
</details>

<details>
<summary>Edge browser plugin opens blank and browser reports MANIFEST-000001 error</summary>
<p>
Open the [Quick File Finder (Everything)](https://www.voidtools.com/en-us/downloads/) application, search for `amkbmndfnliijdhojkpoglbnaaahippg` (the Immersive extension ID) browser storage folder, delete it, then uninstall and reinstall the plugin.
</p>
</details>

<details>
<summary>How to download bilingual subtitles / Can bilingual subtitles be downloaded from other websites?</summary>
<p>
- Currently, subtitle download is only supported on desktop.
- Including YouTube, when there is a subtitle download button, the current website supports bilingual subtitle download.
</p>
</details>
