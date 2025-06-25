---
sidebar_position: 9
---

# FAQ

## Security Related

### 1. The floating ball in the Andriod App has disappeared

Old version add-ons are disabled.

Please uninstall and reinstall the latest version from [official website](https://immersivetranslate.com/).

## Installation Related

### 1. How to update the extension

In general, extensions installed from the browser store will automatically update within a day after a new version is released.

If you'd like to update immediately, go to the browser's **Manage Extensions** page, enable **Developer Mode**, and click **Update** at the top. This will fetch the latest version from the store right away.

![](https://s.immersivetranslate.com/assets/r2-uploads/手动更新插件-X820pSYJFgXPCHVB.gif)

### 2. Tampermonkey Supported Browsers for Immersive Translate Userscript

iOS:

- [Tampermonkey Browser](https://www.tampermonkey.net/)
- Safari with a userscript extension installed:
  - [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)
  - [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171): Recommended to search and install the optimized Immersive Translate script directly in the Stay built-in store (specially optimized for Stay).

Android:

- [Latest Firefox](https://www.firefox.com.cn/download/#product-android-release): After installation, add the [Tampermonkey](https://www.tampermonkey.net/) extension.
- [X Browser](https://www.xbext.com/?ref=immersive-translate): Open the [Immersive Translate Userscript link](https://download.immersivetranslate.com/immersive-translate.user.js) directly to install.

Browsers known to be unsupported due to lack of required Tampermonkey APIs:

- Via Browser (Android)
- Alook Browser (iOS)

### 3. Error when installing the extension package on Chrome

If you see the error `invalid value for web_accessible_resource[0]`

Make sure your Chromium version is above 88, as manifest_version 3 requires it.

### 4. How to Install the Extension on 360 Browser

Immersive Translate only supports **360 Extreme Browser X** (the product name must include "X").

You can install the extension from the Chrome Web Store, or [install it manually](/docs/installation/#%E6%89%8B%E5%8A%A8%E5%AE%89%E8%A3%85-%E8%BF%BD%E8%B8%AA%E6%9C%80%E6%96%B0%E5%BC%80%E5%8F%91%E7%89%B9%E6%80%A7).

### 5. Extension does not work on Opera browser

It doesn't work on google.com and other search pages, the plugin displays `Please refresh the current page before starting the translation` and refreshing the page still shows this message: You need to find "Immersive Translate" in the Opera plugin settings and enable the "Allow access to search page results" option.

If the extension doesn't work on search pages like google.com and shows  
"Please refresh the page before starting translation" even after refreshing,  
go to Opera's extension settings, find **Immersive Translate**, and enable  
**Allow access to search page results**.

### 6. Cannot enable extensions on iOS devices

If you cannot enable extensions on your iOS device, follow these steps:

1. Open the **[Settings]** app
2. Scroll down and tap **[Screen Time]**
3. Select **[Content & Privacy Restrictions]**
4. Tap **[Content Restrictions]**
5. Select **[Web Content]** and set it to **[Unrestricted]**

If you don't need the other features of Content & Privacy Restrictions, you can also choose to simply turn off Content & Privacy Restrictions:

1. Open the **[Settings]** app
2. Select **[Screen Time]**
3. Disable **[Content & Privacy Restrictions]**

### 7. Safari settings page stuck on loading

Open Safari -> Settings -> Websites -> Immersive Translate  
Find and remove any entries related to immersivetranslate.com.

![](https://s.immersivetranslate.com/assets/r2-uploads/帮助中心用图文-沉浸式翻译_(20)-Wn2v8Fpea00jEBaE.png)

### 8. Blank page when logging in from the settings page after updating to iOS 18

Press & hold the floating button, tap the avatar, and log in.

### 9. "File does not exist" when dragging .crx file to browser extensions

You need to first extract the zip file, then drag the .crx file only.

### 10. Why is version 1.13.5 installed from the .crx download instead of the latest?

Because your browser’s Chromium version is below 115 and doesn’t support some advanced features, the extension is automatically downgraded to version 1.13.5.

## Basic Translation Related

### 1. What's the difference between "Translate Webpage", "Translate the Main Content", and "Translate the Whole Page"?

**Translate Webpage (Default Option)**

This option essentially means "Translate the Main Content of the Page".

- **What does it mean?** To preserve the original layout and navigation functionality of most websites, Immersive Translate intelligently identifies the core content areas of web pages (such as article text, post content, etc.) and translates them.

- **Why do this?** Elements like navigation bars, headers/footers, or special elements (like Twitter usernames, posting times) would not only break the page aesthetics if translated, but could also affect normal website usage. Therefore, we've made fine-tuned adaptations for many mainstream websites, excluding these non-core parts from translation.

- **Additional note:** This rule isn't 100% perfect. Some older or niche websites may not have been adapted, so even in default mode, navigation bars and other areas might get translated. We're continuously optimizing this.

**Translate the Whole Page**

As the name suggests, when you select this option, the extension will indiscriminately translate all recognizable text on the page. Previously excluded navigation bars, sidebars, and all other elements will be attempted for translation.

**Use Cases**

- **Daily use:** We recommend keeping the default "Translate Webpage" option, as it provides the best web browsing experience while ensuring translation effectiveness.
- **Special situations:** When you find that certain sidebar or other area content hasn't been translated and you actually need its translation, you can manually switch to "Translate the Whole Page" as a temporary solution.

![](./toggleTranslateAll.png)

### 2. Youtube, Facebook main content is translated, but some sidebars are not—how to translate everything?

For better readability and user experience, Immersive Translate only translates the main content by default.

To translate the entire page:  
Open the extension panel (long press the floating button on mobile) -> Tap **More** in the bottom-right corner -> Select **"Translate the Whole Page"**.

![](https://s.immersivetranslate.com/assets/r2-uploads/帮助中心用图文-沉浸式翻译_(21)-mEXqAEu-YtJ__udT.png)

### 2. Floating button not showing in mobile apps

- Immersive Translate is a browser extension and **only works in browsers**. It cannot be used inside other apps.

- Extensions are tied to the browser they’re installed in and **do not work across browsers** (e.g., an extension installed in Safari won’t work in Chrome).

### 3. On iOS, clicking a YouTube link opens the app, preventing webpage translation

Long press the YouTube link and select “Open in browser” from the popup menu.

### 4. How to turn off automatic translation

How to turn off auto-translate

- Disable relative settings in the popup panel.

- Or change the settings in the **Options**.

![](https://s.immersivetranslate.com/assets/r2-uploads/帮助中心用图文-沉浸式翻译_(23)-ecZbyUCImFS9Fis4.png)


### 5. No permission to translate this page

- Browser default pages can’t be translated (no URL in address bar)
- Third-party extension pages can’t be translated
- Chrome browser blocks translations on the Chrome Web Store

### 6. How to hide the original text

Click the Immersive Translate icon to open the panel, tap **More**, then select **Show Translation Only**.

Or click the icon on the left of Translate button on the popup panel.

![](https://s.immersivetranslate.com/assets/r2-uploads/帮助中心用图文-沉浸式翻译_(22)-deSuh5rWzOcN-jUC.png)

### 7. Exclamation mark on the page

An exclamation mark means the translation service encountered an error.  
Hover over it to see the specific error message.


#### Example: 429 Error

This is one of the most common errors. 429 means too many requests in a short time.  

Webpage translation involves many segments, and despite heavy optimization, some services may still become overloaded and return a 429 rate limit error.

To resolve this, try switching to another translation service temporarily or wait and try again later.

If you're seeing 429 errors with Google services, it's likely that your current network node has been rate-limited by Google. Switching nodes is recommended.

### 8. How to switch translation source and target language

On mobile: long press the floating button.  
On desktop: hover over the floating button to open settings.  
Then choose a different translation service or target language.

![](https://s.immersivetranslate.com/assets/r2-uploads/切换翻译服务-_7cgyjZN5iHRWBS0.gif)

### 9. Google Translate Being Blocked in China

Please add the `translate.googleapis.com` domain name to the proxy rule.

### 10. Does OpenAI's ban on API Keys in China affect member AI services?

No impact, the product uses Azure Enterprise OpenAI, which is not subject to API regional restrictions.

### 11. Caiyun Translation Error

If the error "Unsupported trans_type" shows when clicking the `?` icon, you can manually set the source language instead of using auto-detect.

### 12. WeChat Reading content can't be translated

WeChat Reading restricts content access, blocking third-party tools, so translation is not possible.

### 13. Some parts of the webpage are not translated

This usually happens when the site uses `translate="no"` or `notranslate` class to block translation.

You can fix it by:

1. Enabling the hover-to-translate feature  
2. Hovering over the section to force translation

![](https://s.immersivetranslate.com/assets/r2-uploads/帮助中心用图文-沉浸式翻译_(24)-ahDaije_4_4a-yMO.png)

### 14. Translation not working on a specific site

If one site doesn't translate but others work fine:

- For low-traffic sites:  
  - Use hover-to-translate for paragraphs  
  - To translate the full page, consider using [user rules](/docs/advanced/#用户规则合并增强)

- For popular sites:  
  - Use Hover Translation for now  
  - Report the issue in the user group; our team will schedule support later


### 15. Translation issue on a webpage — how to save and report

Right-click on the webpage and select “Save As” or press Ctrl+S.  
Choose the "Single File" option and save it as a .mht/.mhtml file.  
Then send the file to support@immersivetranslate.com.

![](https://s.immersivetranslate.com/assets/r2-uploads/帮助中心用图文-沉浸式翻译_(20)-7XhrpYNQfUW6GHsk.png)

### 16. View Debug Logs

1. Enable debug logs: Open the panel -> Options -> Developer Settings -> Turn on “Print debug logs to console”.
2. Open the site’s console: Right-click > Inspect -> Switch to the Console tab at the top -> Perform actions to see logs.

### 17. How to hide the floating button

- Hide on current page: Set **Never translate this site** on.
- Hide on all pages: Go to **Options** > **Floating Button**, and turn off **Enable Floating Ball**

![](https://s.immersivetranslate.com/assets/r2-uploads/帮助中心用图文-沉浸式翻译_(23)-_OlNz_acLZaxOGID.png)

### 18. Mouse Hover + Hotkey Translation Not Working

To use mouse hover + hotkey translation, the page must be focused. If it's not working, try the following:

1. **Click anywhere on the page** to ensure it’s focused.
2. Try using mouse hover and the hotkey again.
3. If it still doesn't work, **check if your hotkey settings are correct**.


### 19. How to update to the latest rules

The extension auto-syncs the latest official site rules regularly.

To sync manually, click the Immersive Translate icon in your browser. Once the pop panel opens, it will automatically check and update the rules.

Tampermonkey users are also supported with automatic rule detection and syncing.

### 20. Translation failed / Activity indicator keeps spinning

1. Check the failure reason:

   - If it says **quota limit reached**, your monthly limit for that translation service has been used up.
   - If it shows a network error, check your node or network connection.

2. Switch translation service:  
   Long press the floating button or click the extension icon, then select another service in the panel.

### 21. How to check Pro member translation quota and usage

- Pro members get 20 million tokens per month. This quota applies to all translation services—you can use it entirely with DeepL (≈20M characters), OpenAI (20M tokens), or split across services as needed.

  > OpenAI pricing is based on tokens. For English, 1 token ≈ 4 characters or 0.75 words.  
  > 1,000 tokens ≈ 750 English words.

- Check your usage here: [https://immersivetranslate.com/accounts/usage](https://immersivetranslate.com/accounts/usage)

### 22. Why is the extension’s Google Translate quality lower than Google’s website?

The extension uses Google’s free API, an older, deprecated service that no longer receives updates. In contrast, the official Google Translate website continues to improve, so its translation quality is generally better.

Recently, the free API’s quality has declined significantly. We recommend switching to other available translation services.

More details: [#2574](https://github.com/immersive-translate/immersive-translate/issues/2547)

### 23. Touch mode activated under mouse mode

Go to [Advanced Settings](https://dash.immersivetranslate.com/#advanced) and enable “Mouse Only Mode”.

This detection has been improved in version 1.14.9.


### 24. Edge is unable to read the translation aloud.

The Read Aloud feature of the Edge browser automatically selects the corresponding voice model based on the language of the original webpage. Since these voice models are designed for a single language, the default selected voice model cannot correctly read the translated content when the page contains a translation.

Solution: You can click on the [Voice Options] in the toolbar of Edge's Read Aloud feature, and then manually select the speech model that matches the translated language. This will allow you to correctly read aloud the translated content.

### 25. Shortcuts not working in Arc Browser

Arc browser bug, will cause browser extension shortcuts to fail.

Solution: In the shortcut settings page, change the scope of the shortcut from "In Chromium" to "Global".

![Set shortcut to Global](https://s.immersivetranslate.com/assets/r2-uploads/set-shortcut-global-lRmFkWpxEwxavnco.png)

Note: After setting it to global, the browser window can be triggered even when it is not in focus.

That is, pressing the translation shortcut key in other software can also trigger the translation in the webpage, which may conflict with the shortcut keys of other software.

Suggestion: Use the floating bubble translation in the Arc browser, or use the shortcut key in the Chrome browser.

## Video Translation Related

### 1. Youtube subtitle setup style

You can click on Youtube's own subtitle settings, [Options], and then you can adjust the size, color, and so on.

![](https://s.immersivetranslate.com/assets/r2-uploads/双语字幕调整-3gCapRKm0qvqaRBT.gif)

### 2. YouTube bilingual subtitles not showing in Traditional Chinese

YouTube’s auto-generated Traditional Chinese subtitles often have format issues, causing a large block of text to appear at the start.

To fix this, go to **Options** > **Video Subtitles** and enable  
**Use immersive translate to translate YouTube subtitles**.


### 3. How to enable subtitle translation on Bilibili

To translate Bilibili video subtitles, follow these steps:

1. Turn on Bilibili’s built-in subtitles by clicking the “Subtitles” button in the bottom right of the player.  
   If there’s no subtitle button or content, bilingual subtitles are not available.
2. Click the “Immersive Translate” icon in the player to enable bilingual subtitles.

![](https://s.immersivetranslate.com/assets/r2-uploads/Bilibili_双语字幕-Fm3Tkp9N1Kb2kJm8.gif)

Notes:

1. Make sure Bilibili’s built-in subtitles are enabled.
2. The target language in Immersive Translate must be different from the subtitle language to trigger translation.

### 4. Netflix subtitle translation uses default style

- The current Netflix translation uses a progressive method with self-hosted subtitles and does not support manual subtitles.
- The old method waits for all subtitles to be translated before displaying them and supports manual subtitles.

**How to revert to the old method**

Go to **[Developer Settings](https://dash.immersivetranslate.com/#developer)**, find `Edit User Rules`,  
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

## File Translation

### 1. How to Translate Local Files

- Method 1: Go to [Immersive Translate - Document Translation](https://app.immersivetranslate.com/)  
  or click the Immersive Translate extension icon and select **PDF/ePub**, or **Text**.

- Method 2: If you're using a Chromium-based browser (e.g., Chrome, Arc, Edge),  
  open `chrome://extensions`, find **Immersive Translate**,  
  and enable **Allow access to file URLs**.  
  Then open local HTML or PDF files in the browser and right-click to select **Translate**.

![](https://s.immersivetranslate.com/assets/r2-uploads/翻译本地文件-L2bmbcyUTzXK1YCE.gif)

**Note**: Safari has strict limits on extension access to local files.  
Safari users should use [Immersive Translate - Document Translation](https://app.immersivetranslate.com/) directly.


### 2. PDF Translation Slow with Too Many Pages

Split the file into parts with fewer than 100 pages for faster translation.  
Merge them after translation is complete.

### 3. Duplicate or Overlapping Translations in PDF

This is usually caused by source file recognition issues.  
Manually click and remove extra text boxes.  
We're continuously improving PDF translation accuracy.

### 4. Glossary / Custom Translations or Exclusions

Version 1.16.1+ supports the [AI Glossary](https://dash.immersivetranslate.com/#terms) feature.

Note:
- Google/Microsoft translation does **not** support glossary terms.
- Placeholder-based glossary may reduce translation quality.

To force-enable:

Go to **[Developer Settings](https://dash.immersivetranslate.com/#developer)** -> **Edit Full User Config**, then add the following code:


```
{
  ....
  "enableMachineTranslateTerms":true,
  ...
}
```

### 5. Translated Word File Can’t Be Exported as Word

Currently, exporting to Word has technical limitations.  
We recommend keeping the existing format.  
Improvements are in progress.

### 6. How to Adjust Minimum Font Size in PDF

PDF translation font size depends on browser settings.  
To reduce it, lower the browser font size.  
For Chrome: go to [Chrome Font Settings](chrome://settings/fonts?search=%E5%AD%97%E5%8F%B7)  
or follow the steps below:

![](https://s.immersivetranslate.com/assets/r2-uploads/调整最小字体大小-1JD7U3a2lVyPj9Po.gif)


## Input Box Translation

### 1. Input Enhancement Not Working

- Make sure you’re not using an unsupported browser:  
  See the [Input Compatibility Guide](https://immersivetranslate.com/docs/input/)
- Cannot translate in address bar or new tab, only in search bars (e.g. test via https://www.bing.com/)
- Try speeding up consecutive spacebar presses

### 2. Input enhancement not working on Mac computer

If pressing three spaces on a Mac computer doesn't work, it may be because the Mac input method has a default setting of "Double-tap the space bar to insert a period."

You can find "Input Sources" in "System Settings" -> "Keyboard", click the "Edit" button, and turn off the "Add Period with double-space" option.

![Turn off "Add Period with double-space" on Mac
“](https://s.immersivetranslate.com/assets/r2-uploads/turn-off-add-period-with-double-space-Yp6IL2Ve7WaIV59y.png)

## Payment

### 1. Can I Pay with WeChat?

Yes. Message a staff member in the user group and mention “WeChat Payment”.

After receiving a QR code, complete payment and send the payment details to the staff.  
You’ll receive a membership code (monthly or yearly) to redeem at:  
[Membership Redemption Page](https://immersivetranslate.com/exchange/)

![](https://s.immersivetranslate.com/assets/r2-uploads/帮助中心用图文-沉浸式翻译_(21)-hapgjvcr9uOSJtO0.png)

### 2. Can I Get an Invoice/Fapiao?

Invoices/Fapiao are available for **yearly members only**.  
Paid users: DM the staff with “Invoice/Fapiao request”.  
Unpaid users: see the [Invoice Policy](https://immersivetranslate.com/bill/)

## Other Questions (Less Common)

### How to Clear Tampermonkey Script Cache?

Due to Tampermonkey API limits, cache is stored per site.  
To clear it, open the site’s developer tools and clear its cache.

### Tampermonkey Custom API Request Fails?

Tampermonkey requires domain access to be declared at the top of the script:  
e.g. `@connect api.google.com`  
Add a similar line for any new domain you use.

### Edge Extension Shows Blank Page with MANIFEST-000001 Error

Open the [Everything File Search Tool](https://www.voidtools.com/zh-cn/downloads/)  
Search for extension ID `amkbmndfnliijdhojkpoglbnaaahippg`  
Delete related files, then uninstall and reinstall the extension.

### How to Download Bilingual Subtitles / Are Other Sites Supported?

- Subtitle download is only supported on desktop browsers.
- For sites like YouTube, if a download button appears, bilingual subtitle download is supported.

![](https://s.immersivetranslate.com/assets/r2-uploads/帮助中心用图文-沉浸式翻译_(22)-jdp_ZFllAqqe8Awa.png)
