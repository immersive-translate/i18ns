---
sidebar_position: 9
---

# FAQ

### 1. Android App, floating ball disappeared

Old version add-ons are disabled, uninstall and install the latest version from [official website](https://immersivetranslate.com/).

## Main content on websites like Youtube, Facebook is translated, but some sidebars are not, I want to translate everything

For the sake of page readability, immersive translation by default only translates the main content area. If you want to translate everything.

Open the floating ball panel (long press on mobile) -> Click on more in the bottom right corner -> Select all areas

## Floating Bubble Not Displayed in Youtube (or Other) Apps on Mobile

Browser plugins can only run in browsers and cannot be used in other apps.

- Clicking on YouTube in an iOS browser directly opens the App.

  Press and hold the YouTube link to pop up a floating window and choose to open in a webpage.

## How to turn off automatic translation

- Cancel in the Popup panel or on the Settings page.

<img src="https://s.immersivetranslate.com/assets/turn_off_automatic_translation_en.jpeg" alt="turn off automatic translation" width="250" />

<!-- - Or change：via the settings page

![](https://github.com/immersive-translate/immersive-translate/assets/62473795/d33ac7c0-a47b-4901-b5f6-c6a991164dc0) -->

## No permission to translate the current page

- Browser default page (no address in address bar)
- Third-party plugin page
- Google plugin disables Google Store page

## How do I not show the original text?

Tap the Immersive Translate icon to open the expansion panel, tap [More], [Switch to Translation Only Mode]

## Exclamation mark appears on the page

An exclamation point on the page indicates that the translation service has encountered a problem and returned an error, you can move your mouse over the exclamation point to view the specific error.

### 429 Error

This is one of the most common errors, 429 indicating that the frequency of requests is too fast.Web page translation has a very large number of paragraphs to be translated, although we have done great optimization, including merging paragraphs, frequency control, etc., but sometimes there are still some translation services are overloaded, returning 429 frequency limit error, this time you can usually temporarily switch to other translation services, or wait for a while and try again.

If you're a Google service experiencing 429, it's generally a case of Google doing a traffic limit against your node, and it's recommended to switch nodes.

## Translation of local documents

If you need to translate local HTML files, txt files or PDF files, you can click the Immersive Translate extension icon, then click [More], click [Translate PDF files] or [Translate HTML/txt] files to translate local files.

If you are using Chrome-like browsers, such as (Chrome, Arc, Edge browser), there is another way, is to open the browser extension management page `chrome://extensions`, find the [Immersive Translate] plug-in, [Allow the extension to access local files], and then directly in the browser to open the local HTML or local PDF file, you can directly right-click [translation].

**Note**: Safari browser has strict restrictions on extension access to local files. Safari users should use Method 1 directly - click the Immersive Translate extension icon, then click [More], click [Translate PDF files] or [Translate HTML/txt] files to translate local files.

## How do I update the extension?

Generally speaking, extensions installed in the browser store, the browser will be automatically updated, the general situation will be automatically updated within one day after the extension update, if you want to immediately update to the latest version, you can in the browser's [Extension Management] page, open the [Developer Mode], and then click on the top of the [Updates], you can immediately update to the latest version of the store.

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/update-extension.png)

## Youtube subtitle setup style

You can click on Youtube's own subtitle settings, [Options], and then you can adjust the size, color, and so on.

![](https://s.immersivetranslate.com/assets/youtube_subtitle_options2_en.jpeg)

## Immersive Translate Tampermonkey Supported Browsers

Recommended Grease Monkey extensions for Chrome, Firefox on desktop:

- [Tamper Monkey](https://www.tampermonkey.net/)

Grease Monkey extension recommended for Safari:

- [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)

<!-- > If using [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171) in Safari , please search for the Immersive Translate Optimization Script to download directly from Stay's own store (optimized specifically for Stay) -->

Recommended Grease Monkey Extensions for Android:

1. You can install the [Tamper Monkey](https://www.tampermonkey.net/) extension using [Firefox Latest Version](https://www.mozilla.org/firefox/browsers/mobile/android/).

<!-- 2. You can also directly use [X Browser](https://www.xbext.com/?ref=immersive-translate), after installation, directly open [Immersive Translate Tampermonkey Address](https://download.immersivetranslate.com/immersive-translate.user.js) to install it! -->

<!-- Known unsupported Grease Monkey extensions：

- Android Via Browser
- iOS Alook Browser -->

(since such browsers do not implement the required Grease Monkey API)

## Google Translate Interface Walled Off Issue

Please add the `translate.googleapis.com` domain name to the proxy rule

## How to update the latest rules

The extension itself will regularly synchronize with the latest official website adaptation rules when you use it, you can also manually synchronize with the latest rules by clicking on the browser's Immersive Translate Extension icon to open a pop-up window where the extension will automatically detect the latest adaptation rules and synchronize with them, the same goes for Tampermonkeys.

## How do I save my webpage feedback if I have problems with the webpage translation?

You need to right click "Save as" or ctrl+s shortcut in the web page, choose single file for save option, and finally the file format is .mht/.mhtml. Then send the file to support@immersivetranslate.com

<!-- ![save mht](https://s.immersivetranslate.com/static/official-static/assets/save_mht.png) -->

## Color Cloud Translation Error

Tap away?The error message for the number "Unsupported trans_type" is displayed.You can select the language to be automatically detected by means of the specified language.

## WeChat Reading Cannot Be Translated

It cannot be translated because WeChat Reading has done special processing for the content to prevent access to the content through third-party means.

## Trigger translation does not take effect

Other sites translate, but one site doesn't.

- If this site has fewer visitors
  - Suggested paragraphs to be translated by hovering the mouse
  - If you need to translate the entire site you can adapt it via [user rules](/docs/advanced/#user-rules)
- If this site is used by a lot of people
  - You can start by hovering over the mouse to translate the use of
  - Call it in the group and it will be adapted later on

## Input box enhancement does not take effect

- Browser Home Google Search

Google search box must be in the [Google](https://www.google.com/) URL of the web page, and can not be used in the browser home page, the address bar blank places

## Feedback debug log

- Enable debug logging
  Open Panel -> Settings -> Developer Settings -> Enable "Print debug log in console".
- Open the site's console
  Right click to open the review -> Switch to the console at the top of the right column -> Perform the action to see the logs

## How to turn off hoverball

- Hide on current page

Set it to "Never translate this site".

- Hide on all pages

Open [Settings Page] - [Interface Settings] and turn off [Show Hoverball on Page].

## Error installing plugin installer on chrome

- invalid value for web_accessible_resource[0]

  Chromium version greater than 88 is required to support manifest_version 3.

## How to install 360 Browser

Only 360 Extreme Browser x is supported, remember it's with x.If you have access to the Google Extensions store, you can go directly there and install it.If you can't access it [install it manually](/docs/installation/#manual-installation-to-keep-track-of-the-latest-development-features)

## Opera browser does not work

- It doesn't work on google.com and other search pages, the plugin displays `Please refresh the current page before starting the translation` and refreshing the page still prompts this message.

You need to find "Immersive Translate" in the Opera plugin settings and turn on the "Allow access to search page results" option.

<!-- ![](https://s.immersivetranslate.com/static/official-static/assets/opera-allow-search.png) -->

## YouTube Bilingual subtitles in traditional Chinese not displayed

YouTube comes with machine-translated subtitles, and Traditional Chinese will have formatting errors, causing all subtitles to pop up with a large section of subtitles at the beginning, based on this scenario it is recommended to turn on the [Use Immersive Translate to Translate Subtitles] option in [Settings] [Video Subtitles].

## More questions (see very much)

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
