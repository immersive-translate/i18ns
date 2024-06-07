---
sidebar_position: 6
---

# Change Log

## 1.6.1

- Supports Baidu Qianfan large model platform, Alibaba Bailian large model platform, DeepSeek large model platform.
- Fixed the issue where modifying the target language and other settings in the popup panel would reset upon clicking the translation floating ball.

## 1.5.8

- AI experts support the "Intelligent Selection" mode, where the system will automatically select the most suitable AI expert based on the current website (for example, technology-related AI experts will be automatically selected for The Verge and Hacker News, while Twitter translation enhancement will be automatically selected for Twitter).

## 1.5.7

- Support for adding custom AI translation services compatible with OpenAI, accessible at the bottom of the 【Settings】->【Translation Services】page.
- Fixed an issue where bilingual subtitles did not work on the Domestika video platform in Safari.

## 1.5.6

- Significantly optimized the performance of translating large web pages, ePub creation, and subtitle files.
- Fixed the bug of multi-device synchronization in Pro.

## 1.5.4

- Pro members support out-of-the-box Claude and Gemini translation services (Beta)
- YouTube bilingual subtitles support font and font weight settings
- Fixed word boundary issues when wrapping long paragraphs [#86](https://github.com/immersive-translate/immersive-translate/issues/86)
- Fixed recognition of Japanese and Korean languages
- Fixed issue where Reddit pages on mobile devices were not being translated when scrolling
- Fixed some pages missing translations with DeepL
- Fixed Pro users' multi-device sync time not synchronizing
- Optimized cloud sync setting's coverage issues
- Optimized prompt words for AI translation services

## 1.5.2

- Fixed the issue where changes to the general expert prompt overrode the specified AI expert prompt [#1692](https://github.com/immersive-translate/immersive-translate/issues/1692)
- AI custom model name supports advanced syntax, use + to add a model, use - to hide a model, and use model_name=display_name to customize the display name of the model, e.g.: +gpt-3.5-turbo,-gpt-4,gpt-4-turbo=gpt-4-super
- Fix the error returned by Gemini
- Hide the floating ball when printing the page
- Fix the font size not scaling proportionally when YouTube is in full screen [#1681](https://github.com/immersive-translate/immersive-translate/issues/1681)

## 1.5.1

- Support for AI translation services to set [AI Expert] to specify the translation strategy, currently a Beta feature, which can be enabled in [Developer Settings](https://dash.immersivetranslate.com/#developer) after enabling Beta, and the [AI Expert] menu can be seen after refreshing.
- AI translation services can now customize the model list, such as [OpenAI], the system only has a few of the most commonly used models built-in. Clicking on the model dropdown list, the last item you see is [Set More Models], after setting, it will be automatically remembered for the convenience of users testing different custom models.
- Optimized the inconsistency in the layout of translations in some cases.
- Added a reset button for Youtube subtitle style, which can quickly restore to the default style.
- Fixed the issue where Chinese subtitles could not be downloaded in Youtube.
- Optimized Traditional Chinese interface copy.

## 1.4.12

- Fixed the issue of untranslated message dialog box when opening reddit page
- Added a temporary feature to enable translation editing in the "More" entry of the panel
- Fixed the issue where YouTube Shorts without subtitles always displays subtitles from the previous video [#1655](https://github.com/immersive-translate/immersive-translate/issues/1655)
- Fixed the issue where YouTube bilingual subtitles cannot be adjusted up and down in full screen [#1654](https://github.com/immersive-translate/immersive-translate/issues/1654)
- Support for [VK Video](https://vk.com/video) bilingual subtitles
- Support for independent activation settings for YouTube video bilingual subtitles (enabled by default for new users)
- Optimized error prompts for translating local bilingual subtitles

## 1.4.11

- Compatible with Bing Copilot page input box translation
- YouTube subtitle style control supports edge styling
- Support for selecting the default translation service on the Settings -> Translation Service page
- Fixed OpenAI SystemPrompt placeholder replacement
- Fixed custom user rule merging issue
- Fixed abnormal subtitle display for some Netflix videos [#1630](https://github.com/immersive-translate/immersive-translate/issues/1630)
- Fixed the issue where frequent changes to translation color through the color palette were ineffective [#1628](https://github.com/immersive-translate/immersive-translate/issues/1628)

## 1.4.9

- Translation services are now distinctly organized under a separate tab, allowing for a comprehensive overview of all available translation services. Additionally, users have the flexibility to customize which translation services are displayed. By default, only a limited selection of translation services is shown, but users can tailor their display preferences in the [More Services](https://dash.immersivetranslate.com/#services) section.
- The settings page now accommodates adjustments to [YouTube subtitle styles](https://dash.immersivetranslate.com/#subtitle).
- Enhancements have been made to address the issue where immersive bilingual subtitles would not display when users set the subtitle language to Chinese on the YouTube website.
- A new shortcut has been introduced for temporary translation named Claude, which can be configured in the [Shortcut Settings page](https://dash.immersivetranslate.com/#shortcuts).

## 1.4.8

- Optimize translation performance for large files in PDF-Pro
- Enhance translation performance for long content pages
- Implement internationalization support (i18n) for page document navigation
- YouTube introduces a feature to temporarily enable bilingual subtitles
- YouTube supports the download of bilingual subtitles (members only)
- Mobile adds gesture control, enhancing input via [shortcut settings](https://dash.immersivetranslate.com/#shortcuts)
- Support bilingual translation for Google Docs

## 1.4.7

- Fixed the issue where translation failed when switching OpenAI custom prompt words under the test button
- Fixed the problem of YouTube subtitle shortcut icon not displaying
- Optimized the extension language recognition

## 1.4.6

- Fixed the issue where user-defined prompt words were ineffective
- Added 50%, 150% options for Youtube subtitle font size

## 1.4.5

- Fixed the issue where changes to Youtube subtitle styles were not saved
- Fixed the disappearance of subtitles in full screen on iOS Safari
- Further optimized the translation speed of Youtube subtitles
- The panel's more options now support [text translation entry](https://app.immersivetranslate.com/text/)

## 1.4.2

- Support for Claude translation service
- Optimized OpenAI multi-prompt words, supporting YAML format, which improves the flexibility and ease of use of configuration
- Significantly optimized the translation speed of Youtube subtitles, and added support for switching between Chinese and English order, customizing font color and size, etc.
- Video subtitle platform supports [University of Southampton](https://southampton.cloud.panopto.eu)
- Udemy bilingual subtitles compatible with mobile display
- Gemini translation service is hidden by default, can be enabled in developer settings to show beta of this translation service

## 1.3.4

- Support for Yandex free translation service
- Optimized Gemini prompt words
- Video subtitles support setting for bilingual/original and translation display
- Support for space between Chinese and English in OpenAI translation results
- Panel switch to display only translation button modified to only take effect on the current page

## 1.3.3

- Optimized the translation display issue of Twitter CC video subtitles.
- DeepL service has added support for Arabic.
- Colorful Clouds translation service now supports Korean, Spanish, French, and Russian.
- OpenAI service has added support for Northeastern Chinese dialect.
- The panel's automatic detection now displays the original language.
- Adjusted the shortcut description for the mobile panel.

## 1.3.2

- Fixed the issue where the control panel could not be closed on mobile devices

## 1.3.1

- Video subtitle platform support [DeepLearning.ai](https://learn.deeplearning.ai)
- Support for web page translation and video subtitle translation in languages such as Arabic, Hebrew, etc., addressing RTL (Right-To-Left) display issues
- Fixed Gemini translation into Hebrew
- Fixed an issue where some traditional Chinese subtitles on YouTube could not be displayed correctly
- Fixed the display issue of Twitter subtitles on Safari
- Fixed the shortcut for immediate translation to the bottom of the page

## 1.2.4

- Fixed the issue where placeholders in ePub creation were not replaced properly
- Video subtitle translation support [Unreal Sensei](https://www.unrealsenseiacademy.com/)

## 1.2.3

- Optimized the frequency control of translation service requests
- Recent Microsoft translation service requests from within China have been unstable; when errors occur, the system automatically detects the currently available translation service, allowing users to quickly switch.
- Optimized the error message for network errors
- Fixed the issue where configuring text color did not support RGBA preview [#1435](https://github.com/immersive-translate/immersive-translate/issues/1435)
- Fixed the issue where upgrading the Safari plugin version always prompted the installation success page
- Microsoft added support for Vietnamese
- Fixed the issue where translated subtitles on the edx site did not display

## 1.2.2

- Video subtitle translation support for [pluto](https://pluto.tv/), [STARZ](https://www.starz.com/), [Paramount Plus](https://www.paramountplus.com/), [Rotten Tomatoes](https://www.rottentomatoes.com/), [Dailymotion](https://www.dailymotion.com/), [FMovies](https://fmoviesz.to/), [AniWatch](https://aniwatch.to/), [iQIYI](https://www.iq.com/), [Youku](https://www.youku.tv/), [movie-web](https://movie-web.app/). Also supports the translation of some CC subtitled videos on Twitter.
- Optimized error pop-ups, network problem error pop-ups automatically detect valid free translation services.
- Fixed immersive iOS APP support for YouTube fullscreen playback.
- Fixed paragraph translation issue with Perplexity.ai [#707](https://github.com/immersive-translate/immersive-translate/issues/707).

## 1.2.1

- Video subtitle translation support for [Kanopy](https://www.kanopy.com/), [RachelsEnglishAcademy](https://www.rachelsenglishacademy.com/), [Hulu](https://www.hulu.com/), [Three.js Journey](https://threejs-journey.com/).
- Fixed an issue where some Pro users could not modify settings in the Chrome browser.
- Supported bilingual subtitles display in YouTube's fullscreen mode on iOS.

## 1.2.0

- Support for video subtitle translation on [LinkedIn](https://www.linkedin.com/) and [Viu](https://www.viu.com/) platforms.
- Added more video subtitle quick access for additional platforms.
- Support for setting specific websites/languages to display only the translated text.
- Fixed an issue where the settings page would continuously show loading in some cases on Safari.
- Support for translating input tag nodes.
- Optimized the error popup UI.

## 1.1.9

- Subtitle translation support for YouTube Live and the [Mubi](https://mubi.com/) platform.
- Optimization: Settings page, URL list interaction UI (to avoid ambiguity, checkboxes are not displayed by default).
- Support for setting the translation font in translation-only mode.
- Added quick access for enabling video subtitles on Netflix, Ted, Bloomberg, Udemy, Coursera.
- Fixed: Some translated styles (such as underlines) were not effective in Safari.
- Fixed: During page translation, the issue where hovering the mouse did not trigger re-translation.

## 1.1.8

- Added an option for the child translation service to follow the main translation service
- Bilingual subtitles support for [Amazon Prime Video](https://www.primevideo.com)
- Further optimization of the embedded PDF translation function in Sci-Hub
- Fixed an issue with online PDFs not opening correctly
- Fixed the issue with continuous playback of bilingual subtitles on Netflix

## 1.1.7

- You can now specify a font for the translation in the settings page -> [Basic Settings] -> [Translation Style]
- Added a shortcut configuration for [Translate Specified Paragraph] in the floating ball panel on mobile devices
- Optimized the sensitivity of detecting mouse hover over Ctrl to avoid mistaking `Ctrl+C` as `Ctrl`
- Added support for a new shortcut setting that allows quick toggling of whether video subtitles use the built-in machine translation subtitles
- On the Sci-Hub website, clicking the floating ball will translate PDFs embedded in the webpage

## 1.1.6

- **Mobile Support for Translating Specific Paragraphs:** The mobile version now supports translating specified paragraphs and has added a variety of shortcut operations, including swiping left, swiping right, double-tapping, triple-tapping, and multi-finger touch gestures. These are not enabled by default and require the user to actively select the triggering gesture in the settings page under 【Mouse Hover】.
- **Gemini Default Version Update:** The default version is now `v1beta`.
- **Fixed Classical Chinese Translation:** Fixed the Classical Chinese translation functionality of Microsoft and OpenAI.
- **Japanese Translation Optimization:** Further optimized OpenAI's Japanese translation to improve accuracy and fluency.
- **Immersive Translation Experience:** To better adapt to user habits, we have moved the shortcut for bilingual subtitles in full-screen mode on the YouTube platform to the left side.

## 1.1.5

- Fixed the issue where the dropdown menu in dark mode on Windows had no color.
- Fixed the alignment issue with the "More" option not being left-aligned on Windows.

## 1.1.4

- **Popup Panel UI Upgrade:** The new design aims to improve usability and understandability. This update includes:

  - **New features in the main menu:**
    - **Bilingual/Translation-only mode switch:** You can now switch between "Bilingual Translation Mode" and "Translation-only Mode" directly in the main menu, located to the left of the translation button.
    - **Document translation entry:** The entry for translating "PDF/ePub/subtitle files" has been moved to the main menu for quick access.
    - **Video translation settings:** The entry for "Video Translation" settings has also been placed in the main menu for quick adjustments.
    - **New entry for usage documentation:** Provides detailed operation guides and help documents.

- **Integrated document translation entry:** Now, you can translate PDF, ePub, and subtitle files through a unified upload entry. Simply click the 【PDF/ePub】button in the Popup panel, no need to select 【More】anymore.

- **Added support for 5 video websites:**
  - Support for subtitles of podcasts on Youtube Music.
  - Added support for the iview.abc.net.au website.
  - Added support for the www.nma.art website.
  - Added support for the creativecloud.adobe.com website.
  - Added support for the www.masterclass.com website.

## 1.1.3

- Fixed the display anomaly issue of the mobile plugin when opening PDF pages.
- Optimized the translation effect of GPT conversations.
- Supported domain translation for Baidu Translate.
- Added a translation-only mode in the settings page.
- Added a reminder function when switching translation modes with shortcuts.
- Fixed the issue where translating input fields containing URLs only translated parts of the content.

## 1.1.2

- Fix: The issue where switching translation services did not take effect when the page had not been translated yet.
- Optimization: In the process of translating Epub and PDF, if some content fails to translate, it is now possible to switch to another translation service on the panel without restarting the entire translation process (the previous logic was to immediately use a new translation service to retranslate the entire book). This means that halfway through the translation, you can switch to a different translation service and click on [Retry All Failed Paragraphs], after which the system will continue the translation using the new service.
- Optimization: Adjusted the font size of the translation error prompts to improve readability.

## 1.1.1

- Fixed the issue of the bilingual subtitles shortcut for YouTube having overly long English text.

## 1.1.0

### New Features

- **Shortcut Key Settings**: Added a new top-level menu "Shortcuts" and the following customizable shortcut key functions:

  - Designate a combination of keys to translate the content of the current input box, supplementing the previous method of quickly hitting the space bar three times.
  - Designate a combination of keys to temporarily enable "direct translation on mouse hover" on the page. Pressing it again will cancel this function.
  - Added dedicated shortcut keys for 6 translation services (such as DeepL, OpenAI, Google, Microsoft, Gemini, Tencent Interactive Translation) to facilitate temporary switching between translation services.

- **Plugin Settings Page UI Update**:

  - In "Advanced Settings", a new option has been added to allow users to specify certain words (e.g., "LLM") to be excluded from translation.
  - In "Advanced Settings", a new option has been added to configure the minimum number of characters required to translate a paragraph. The default is 4 characters, but it can be set higher (e.g., 20), so that only longer paragraphs will be translated.
  - Added a tutorial for beginners, covering floating ball settings, video subtitle settings, and mouse hover settings.

- **YouTube Bilingual Subtitles**: Added a quick access in the YouTube video playback window to enable or hide bilingual subtitles (this feature can be turned off).

- **Deepl Language Support**: Added support for Portuguese (Brazil).

- **New User Guide**: When new users first open a page in a non-target language, a floating ball help guide bubble is displayed.

### Optimization and Fixes

- **UI Optimization**: Redesigned the UI for page translation error prompts to make them easier to understand. When there are many errors, a pop-up will actively prompt the user.

- **Bug Fixes**:

  - Fixed the issue where mouseover translation would fail when the page loses focus.
  - Fixed the issue where less than 3 characters in the input box enhancement feature were not translated.
  - Fixed the issue where some directories were not translated during the production of bilingual Epubs.

- **Feature Removal**: Removed the bilingual information enhancement feature (displaying English search results on Google search pages simultaneously).

### Other Updates

- **openAI Configuration Update**: Now supports setting the number of configurations per second in decimals, such as 0.5, meaning 1 request every 2 seconds.

## 0.12.14

- Fix: The default target language recognition issue on some machines after the first installation.
- Optimization: The default order of web page titles is changed to [Chinese - English].

## 0.12.13

- Fixed: Issue with OpenAI long paragraph translation stitching in some cases. [#1276](https://github.com/immersive-translate/immersive-translate/issues/1276)
- Optimized: When using mouse hover, the issue where losing focus on the page and then re-triggering becomes ineffective.
- Fixed: The issue where the cache still exists after modifying the prompt/model in OpenAI.

## 0.12.12

- Updated: Optimized the popup panel, removing some options for the current website.
- Optimized: Improved the process of merging manual subtitles.
- Optimized: Automatically set the target language based on browser language.
- Added: Bilingual subtitles support for the [ArtStation](https://www.artstation.com/learning) learning platform and [ZDF](https://www.zdf.de/).
- Fixed: Solved the issue where titles on the jstor list page were not translated [#1268](https://github.com/immersive-translate/immersive-translate/issues/1268).
- Fixed: Fixed the issue where only part of the content disappeared on Hacknews [#1264](https://github.com/immersive-translate/immersive-translate/issues/1264).

## 0.12.11

- Added bilingual subtitles support for [HBO Max](https://play.max.com/), [BBC](https://www.bbc.com/), [Disney+](https://www.disneyplus.com), [ARD Mediathek](https://www.ardmediathek.de/), [ITV](https://www.itv.com/), and [Domestika](https://www.domestika.org) platforms.

## 0.12.10

- Fixed the authorization issue of Gemini domain under the Tampermonkey script.
- Supported real-time subtitle translation for Twitter Space.
- For older versions of the Tampermonkey script, an update prompt has now been added to the settings page.

## 0.12.9

- Added support for Gemini translation.
- Fixed the issue where translations did not respond in time when the webpage was scrolled to the middle position in some cases.
- Fixed the bug where subtitles switch on some video websites caused the translation to be displayed repeatedly.
- Fixed the issue where the mouse hovered to continue translating without holding down the shortcut key in some cases.
- On macOS, optimized the display name of the panel shortcut.

## 0.12.8

- Repair the original video subtitles are not displayed when "Current site is set to never translate".
- Repair the conflict with some plug-ins that cause infinite page re-turning.
- Repair the non-translation of some paragraphs after turning on long paragraph line breaks.
- Fixed [When temporarily turning on webpage translation for a long time, clicking the panel [Always translate this website] does not cancel the always translation #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)

## 0.12.7

- Bilingual subtitles added to support [TED](https://www.ted.com), [Frontend Masters](https://frontendmasters.com/), [edx](https://www.edx.org/), [CodeWithChris](https://www.edx.org/), [Skillshare](https://www.ted.com) platforms. https://learn.codewithchris.com/enrollments), [Skillshare](https://www.skillshare.com/) Platforms
- The hoverball is now hidden by default when the video is full screen.
- Fix the jittery clicking problem of firefox page hoverball action panel.
- Support for collaboration under the pubmed.ncbi.nlm.nih.gov site and the scholarscope plugin
- Fix reddit input box translation page jitter issue

## 0.12.6

- Fix the problem that the translation of YouTube/Web of Science etc. is not sensitive when switching tabs.
- Hoverball on mobile now supports long press operation, short press to translate, long press to open the panel.
- Translating bilingual ebooks will now translate the table of contents as well.
- The Search Enhancement (some pages of Google Search display bilingual search results) feature is now not enabled by default and will be removed in the next release.

## 0.12.5

- Fix Epub Creating eBooks from panel clicking on translations not working

## 0.12.4

- When you turn on bilingual subtitles in the panel, it will first refresh the page automatically (to display bilingual subtitles more accurately), and some sites still require users to manually click the "CC" button on the site to turn on subtitles.
- Optimize Grease Monkey, Safari language detection
- Provides quick access to bilingual versions of all papers on the [Arxiv](https://arxiv.org/abs/1910.06709) papers site.
- [Hoverball support configured to be fixed to the left #1168](https://github.com/immersive-translate/immersive-translate/issues/1168)
- [Fix Learning Mode display issue #1180](https://github.com/immersive-translate/immersive-translate/issues/1180)
- [Temporarily turning on web translation for a length of time does not cancel Always Translate #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)
- Optimize PDF file initialization issues

## 0.12.3

- Fix for [permanently disable video subtitles] feature not working [#1175](https://github.com/immersive-translate/immersive-translate/issues/1175)

## 0.12.2

- Bilingual subtitle support is provided for more video platforms, which are now supported： [Youtube](https://www.youtube.com/), [Netflix](https://www.netflix.com), [Udemy](https://www.udemy.com/), [Khanacademy] (https://www\.khanacademy.org/), [Coursera] (https://www\.coursera.org/), [Vimeo] (https://vimeo.com/), [Nebula] (https://nebula.tv), [Bloomberg](https://www.bloomberg.com), [Bilibili](https://www.bilibili.com/), etc. (Note that due to the technical limitations of：, some websites need to refresh the page after turning on the bilingual subtitles for the first time or wait for the translation to complete to display the bilingual subtitles). (Note that due to technical limitations, some websites need to refresh the page after opening the bilingual subtitles for the first time, or need to wait for the translation to complete to display the bilingual subtitles)
- Significantly optimized plugin zip size, cut in half compared to the original, download and update faster.
- Fix Extended PDF download issues
- Added a quick-translate PDF portal to the right side of the [Arxiv](https://arxiv.org/abs/1910.06709) paper site, which goes to a clean HTML page (only supported by some papers, since it requires the original authors to submit the source code, so roughly 50% of the papers will show this portal)
- Online PDF pages without .pdf extension can now jump directly to the PDF translation page by clicking the hoverball on the page.
- Fix some input box enhancement issues under Safari
- Optimize language detection in Grease Monkey and Safari

## 0.11.6

- Added 11 new interface languages for the plugin and the official website, now the supported interface languages reach 14, including Chinese Simplified, Chinese Traditional, English, Japanese, Korean, Russian, Spanish, Portuguese, Hindi, Italian, German, French, Arabic, and Persian.
- Modify the bilingual sharing (refreshing mode) added in the last version to bilingual page snapshot sharing, so that the shared content is more original, as well as wider adaptability.
- Fix emoji at the end of the Twitter input box that can't be translated
- Fix the situation where the content of third-party plug-ins is translated in some scenarios
- Repair online pdf hoverball click unresponsive

## 0.11.5

- You can now generate a public link to the translated bilingual page for Immersive Translate.
  - [Click](/docs/share/) on the Immersive Translate Sharing Icon to generate it in one click!
- Solved the problem that some platforms could not recognize whether the mouse was supported or not
  - There are some desktop browsers that support both touchscreen and mouse, and Immersive Translates is technically unable to detect whether such platforms support mouse, so we have added the option [Force Enable Mouse Support] in the [Mouse Hover] setting

## 0.11.2-0.11.4

- Optimize experience, fix some bugs

## 0.11.1

- The default model for OpenAI translations is: GPT3.5-turbo-1106.
- Optimized the Chinese Prompt for OpenAI, now less prone to hallucinations!
- Reduced the length of OpenAI's prompts from 90 to 40, saving even more traffic.

## 0.11.0

- Fix jittery page hoverball clicks
- Fixing Azure Translation Issues

## 0.10.9

- Fix some minor issues

## 0.10.8

- Support for setting up hoverball quick translation buttons (both PC/mobile support)
- Optimizing Grease Monkey Language Judgment
- Fix txt file translation

## 0.10.7

- Mouse hover support press Ctrl again to show original text
- Mouse Hover Ignore Never Translate Language
- Youtube Bilingual Subtitle Optimization

## 0.10.6

- Youtube subtitle support for translations only
- Add Grease Monkey Low Version Update Alert
- Fix the problem that local txt files cannot be translated

## 0.10.5

- Fix Youtube occasionally returning to the homepage

## 0.10.4

- Fix Youtube subtitle conflict with Dual subtitle plugin (Immersive Translate of Youtube subtitle translation is not enabled when Youtube Dual plugin is detected to avoid conflict)
- Added [Permanently Disable Video Subtitle Function], if there are other conflicting issues and you don't want to enable the bilingual subtitle function with Immersive Translate.
- Optimize subtitle breaks

## 0.10.3

- Fix Custom DeppL Auth Key Translation Issue

## 0.10.3

- Perfect support for Youtube videos with bilingual subtitles 🎉.
- For article pages, the body text will now be translated first before the rest of the sidebar content
- Optimize DeepL Translation Contextualization
- Optimize OpenAI translation of subtitle files for contextualization

## 0.10.1

- Increase the priority of body translation to optimize the translation experience
- Fix ins click more text not translated issue

## 0.9.8

- Optimize experience, fix some bugs

## 0.9.7

- Fix auto-translation when readwise is highlighted

## 0.9.6

- Fixed clearing the cache by logging out the user's login.

## 0.9.5

- Online eBooks bug fixes

## 0.9.4

- Optimize input enhancement detection to reduce false touches
- E-book and subtitle translation online

## 0.9.3

- Input Box Translation：displays a pop-up reminder when it is used for the first time, and the user can choose to disable it this time or permanently to avoid accidental touches.
- PDF only translation export speed optimization, if you choose to export only the translation, you can directly call the system PDF preview to export, faster.
- Deeplx supports multiple URLs, just split them with .

## 0.9.2

- The PDF translation tool is migrated to the online version： https://app.immersivetranslate.com/pdf/ , so that Grease Monkey and Safari can use PDF translation, and problems can be better iterated without the need to issue a version to solve the problem.
- POPUP UI optimization, the panel is more beautiful!

## 0.9.1

- Fix filename issues with Epub ebook creation

## 0.8.8

- pdf support line spacing and word spacing adjustments to re-recognize paragraphs
- epub online reading mobile auto-scrolling problem fixing

## 0.8.7

- pdf support for translation downloads only
- Fix safari Google login problem

## 0.8.2 - 0.8.6

- Allows you to set the interval between input enhancement combo triggers
- Fix some bugs

## 0.8.1

- Language Detection Optimization
- Beta Features：Custom API (Beta enabled in developer settings)
- Support for AliCloud Translation
- Fixed some bugs

## 0.8.0

- Supported User Systems
- Supports [Enable Pro Membership](/pricing), which allows users to enjoy Deepl and OpenAI translations and cloud synchronization settings.
- Mouse hover translation service can be set individually
- Input box translation service can be set up separately
- PDF Translation Optimization
- Fixed some bugs

## 0.7.16

- PDF translation with new options for quick control of the translation style (PDF files are very strange and turning on these options may be useful for some PDF files with messy formatting)
- iOS and macOS versions are back on the Apple Store Country Store

## 0.7.15

- We've been notified by Apple that OpenAI Translations has been temporarily removed from iOS and macOS, and we're trying to re-launch it in China.

## 0.7.11- 0.7.14

- Fix：Gmail Translate All Regions issue
- Temporarily disable Safari's PDF export function due to Safari's restriction on plug-in downloads (bug).
- Fix some other problems

## 0.7.10

- Popup Browser Icon Panel UI upgrade, a little bit more design ～
- Fixes the problem that some Japanese passages are not translated.

## 0.7.9

- PDF finally supports the export of bilingual versions!You can click the [Save] button to export the translated bilingual PDF file.
- Custom rules now support merging with the default built-in rules, e.g.：`{"id": "youtube", "selectors.add":["#test"]}` means adding a `#test` to the existing selectors, `selectors` means overriding the default, `selectors.remove` means deleting one of the default selectors, and `selectors.remove` means deleting one of the default selectors, and `selectors.remove` means deleting one of the default selectors. removes one of the default selectors.
- Updated Safari icon, a little bigger.
- Other Bug Fixes

## 0.7.8

- Bug Fixes

## 0.7.7

- Adapted to Safari's system style, Safari's extension icon changed to transparent outline.
- Add browser icon status change, when a web page has been translated, a ✅ will be added to the bottom right corner of the browser icon automatically.
- Automatically enable translation of frequently used English websites for new users
- Fix translation problems with https://claude.ai/

## 0.7.6

- Input Enhanced Support Translation Results ctrl+z Undo
- Support translation in Flying Book document reading mode
- Adaptation https://pi.ai/talk

## 0.7.5

- Fix Grease Monkey icon not displaying
- Fixing a number of issues

## 0.7.4

- Fixing a number of issues
- Setup page supports batch deletion of selected urls.
- Supports enabling/disabling Youtube subtitle translation to prevent conflicts with other related plugins.
- Arigato Translator supports setting fields and terminology id

## 0.7.2

- Input Box Enhancement：allows to omit the prefix // and trigger the translation of the entire input box with 3 spaces, or you can turn this option off in the settings page.

## 0.7.1

- Support Search Enhancement, when enabled, when you search in Google/Google News in Chinese, the right column will automatically show the search results of corresponding English keywords, which is enabled by default.
  - Reason：We found that in Google search, the search results for Chinese keywords and English keywords can be very different, with the Immersive Translated Search Enhancement enabled, we automatically search for the same keywords in English for you and display them on the right side.You can choose to disable it if you don't need the feature.
  - Safari is not supported due to API limitations.

## 0.6.20

- Modify the default settings：Due to a large number of users' feedback that they will not use the translation tool after installation, their expectation of the translation tool is that it will automatically translate English web pages after installation, so from this version onwards, for Chinese users, the option of translating English pages by default has been turned on (if the user has had a previous setting of the language that will always be translated, then it will be honored, and the change only modifies the initial settings of the extension), and it needs to be canceled, the can be easily canceled in [Popup panel or settings page](/docs/faq/#%E5%A6%82%E4%BD%95%E5%85%B3%E9%97%AD%E8%87%AA%E5%8A%A8%E7%BF%BB%E8%AF%91)

## 0.6.19

- Fix PDF Bugs
- Fix web of science Bug
- Adaptation feeder.com
- Fix epub not translating some books

## 0.6.18

- Fix Safari Popup width overflow issue.
- Building Process Optimization

## 0.6.17

- Optimize error alerts
- Optimize the target language selection, now it will only show the languages supported by the corresponding translation service
- PDF Translation Optimization
- Adapted for Good Reads website, Amazon and South China Morning Post website

## 0.6.16

- Add PDF no permission page display
- Repair the display of PDF text list paragraphs
- Enlarge PDF small font scaling on chrome and safari

## 0.6.15

- Repair the problem that when opening PDF files, the extension panel prompts that there are no permissions.
- Fix the issue that input box enhancement is not enabled when the site is set to never translate.

## 0.6.14

- PDF translation optimization, translation area can now be edited/dragged/deleted
  - Drag top left, delete top right, change size bottom right
- Windows Dropdown Box Left Alignment
- Support Traditional Chinese and Simplified Chinese

## 0.6.13

- Fix the problem of repeated translation on mouse hover
- PDF translation support drag to change the size and edit the content of the translation

## 0.6.12

- Fixes Epub translation images getting smaller in some browsers
- Optimized input box translation, now works smoothly in Bard!

## 0.6.10

- OpenAI default model changed to version 0613
- Fix some input box styles
- Smarter to determine if it is a navigation area, and if so, no translation is performed
- Fix possible XSS injection attacks

## 0.6.8

- The extension panel can now indicate unsupported pages (e.g. pages with no permissions and non-HTML pages)
- Input box enhancement to show Loading status in translation
- Update default loading colors in translations
- When the input box is configured with no prefix, it supports `ja Hello` translation to Japanese and `English Hello` translation to English.

## 0.6.6

- Fix for： some areas not translating (quora)

## 0.6.5

- Google Bard Optimization
- Input Box Translation supports direct translation of the entire text box without prefixes.
- Optimize the problem of OpenAI translations adding periods mindlessly, (if no period is detected in the original text, if openai returns a period, then remove it)
- Problems with safari subtitle files not being recognized

## 0.6.3

The default language for input box translation can now omit the space, i.e. //Hello World can be translated as well.

## 0.6.2

The most exciting input box enhancement is here：

- Type： // Hello World into the input box on any web page, then triple-click the space bar to translate the paragraph into English
- You can also specify the translation to a certain language： /ja Hello World, then triple-click the space bar to translate the paragraph into Japanese

[Click here for a quick 30-second introduction](/docs/input/)

## 0.6.0

- First release in June, migrated from the previous personal subdomainhttps://immersive-translate.owenyoung.comto the new domain https://immersivetranslate.com/
- Functionality is largely unchanged (new features will be available in the next release!)

## 0.5.17

- Fix the problem that： bilingual eBooks do not have pictures after exporting

## 0.5.16

- Fix： openai translation issue in Traditional Chinese

## 0.5.15

- Optimize： The minimum number of characters in a paragraph that triggers translation was modified to a minimum of 4 characters to reduce confusion, while using other features to avoid translating the navigation and end areas of the site.
- Fix： Github details not translating after expanding.

## 0.5.14

- Fix the problem that images on some web pages of： become bigger after copying
- Fix： medium comment section not translating
- Fixed the problem that images on some pages of： were copied incorrectly

## 0.5.12

- Feature： Split Line Translation Style adds a vertical split line for single line translations
- Fix： Very rare cases of paragraph splitting.
- A great first-time setup orientation page for new iOS users.

## 0.5.11

- Subtitle translation support for exporting translations only
- Fix： Some elements are not recognized by mouse hovering
- Fix：tweet partial line breaks not recognized
- Fix：eBook authoring style not working

## 0.5.10

- Fix： tweet line breaks not recognized
- Fix： Reddit detail page returns some paragraphs that cannot be translated
- Fixed an issue with： where some of the Code tags were not recognized correctly.

## 0.5.9

- Fixes paragraph breaks in some cases at：
- Fix： Tampermonkey Toggle Only Shows Translations
- Fix： eBook online reading style not working issue

## 0.5.8

- Fix the issue that： temporary setting of website translation duration does not take effect.

## 0.5.7

- Super update!

- The Show Translations Only feature is here! Click [More] -> [Switch to show translations only].

  - Support customized shortcuts, set in interface settings -> Shortcut Settings

- Optimize OpenAI request frequency limitation issue

- ChatGPT defaults to the mobile model, which is faster!

- Web core parsing refactoring, which means：

  - Large-scale web page translation in seconds
    - For example,： https://pve.proxmox.com/pve-docs/pve-admin-guide.html, which took 30 seconds before, is now flipped in seconds.
  - Ultra-low memory usage for complex web pages
    - For example： https://www\.wsj.com/articles/global-stocks-markets-dow-news-05-05-2023-cb142c76?mod=hp_lead_pos1
  - Adaptation to more websites

- All translations of ShadowRoot's website are supported.

  - For example： https://bugs.chromium.org/p/chromium/issues/detail?id=418987
  - For example, the comment section of： https://news.yahoo.com/gma/virginia-mom-facing-charges-6-190600893.html

- Fix the white screen problem after translation of websites with hydration such as Next.js.

  - For example： https://webpack.js.org/

- Fixed the issue that modifying the mouse hover shortcut needed to refresh the page to take effect

- Fixed a problem with line feed recognition in TXT files.

- Lots of updates!

- The 'Show Translation Only' feature has arrived! Click on 'More' -> 'Switch to Show Translations Only'.

  - Supports custom shortcuts, which can be set in 'Interface Settings' -> 'Shortcut Settings'

- Optimized for OpenAI request rate limit issue

- Web core parsing has been rebuilt, which means.

  - Instant translation for large websites
  - Minimal memory usage for complex web pages
  - Better compatibility with more websites

- Now supports translations for all websites with ShadowRoot.

- Fixed the white screen issue after translating websites with hydration, such as Next.js

- Fixed the issue where changing the mouse hover shortcut required a page refresh to take effect

- Fixed the issue with recognizing line breaks in TXT files.

## 0.5.6

- Fix: macOS new tab popup issue.
- Feat: New guide page for new user.

## 0.5.5

- Fix: Mouse over area issue.

## 0.5.4

- Fix: Spa Page duplicate

## 0.5.3

- Fix: Mouse hover hotkey listener.
- Fix: PDF document translate
- Feat: Add new client guide page

## 0.5.2

- Fix: userscript mouse hover shortcuts settings

## 0.5.1

- Fix: OpenAI API not works.

## 0.5.0

- Feat: Translate the current paragraph when mouse hover.
- Feat: Refactor PDF translation, now you can translate most PDFs with Immersive Translate
- Fix: Disable Context Menu not working [#428](https://github.com/immersive-translate/immersive-translate/issues/428)
- Fix: Avoid Content Security Policy for [Mastondon](https://mastodon.social/)

## 0.4.11

- Fix: userscript permission (only for userscript).

## 0.4.8

- Feat: Bing Translate to Microsoft Translate for more stable quality.
- Fix: Pure TXT web page like [this](https://edoras.sdsu.edu/~vinge/misc/singularity.html)
- Performance: Exclude some child advertising pages in the website, and the performance has improved a little

## 0.4.7

- Fix: Firefox Userscript popup missing.

## 0.4.6

- Feat: Allow third party send document event to call `toggleTranslatePage`
- Feat: iOS app add enable extension button and communities link
- UI: OpenAI settings field model use select instead of text input box.

## 0.4.5

- Fix: iOS 15.0 safari extension issue.
- Fix: macOS safari extension shortcuts
- Fix: content security policy popup for extension, and partly for userscript.

## 0.4.4

- Chore: Remove console.log

## 0.4.3

- Fix: sup, sub tag whitespace detection.
- Feat: support ChatGPT Plus Website as Translation Service, This is a beta feature, so you can access it by enabling Beta Feature on developer settings. This is very slow, cause chatgpt can only send one request at once. Make sure you have ChatGPT Plus Account, cause there are more limit on Free Account, and I' m not sure if this bring risk for your account, be careful to Make sure you have ChatGPT Plus Account, cause there are more limit on Free Account, and I' m not sure if this bring risk for your account, be careful to use it.

## 0.4.1

- Fix: firefox context menu dispeared after restart.
- Support Azure openai

## 0.4.0

- Feat: Support Translate Local Subtitle File (.srt,.ass,etc.)

## 0.3.17

- Feat: Support translate local .txt file.
- Fix: Context Menu may not avaliable sometimes. [#273](https://github.com/immersive-translate/immersive-translate/issues/273)

## 0.3.16

- Fix: keep &nbsp; as whitespace.
- Remove: Take down Papago, as [the service is down](https://github.com/immersive-translate/immersive-translate/issues/310)

## 0.3.15

- UI: allow no API key for openai
- UI: allow Open AI reset to the default settings

## 0.3.14

- Dependence: Upgrade pdf.js to the latest version
- Fix: pdf selection background color
- Fix: whitespace detect

## 0.3.13

- Fix: ebook builder specific character issue, like some chapter path is `xxx' xxxx`.
- UI: fold openai custom options by default.
- UI: Add exporting status for epub export.
- Fix: Gpt4 default prompt

## 0.3.12

- Feat: We can custom Marker translation theme background color now.
- Fix: postMessage when init page broke somesites, now we will do this only when we really translate pages
- Fix: ebook progress issue.
- Fix: better for split long paragraph, 1.5 billion, 25.5%, Mr. will not be considered as a boundary

## 0.3.11

- Fix: ebook reader dark mode text color
- Fix: openAI prompt

## 0.3.10

- Better: detect Japanese/Korean container.
- Fix: Ebook Builder Progress 99% stopped.

## 0.3.9

- Fix: Options UI switch translation services input state not changed.

## 0.3.8

- UI: loading color more transparent
- Fix: Detect Ebook Language.
- Feat: Add translate progress for ebook builder, and a beautiful confetti after success.
- Feat: Add retry all failed paragraphs for retry button.
- Fix: Deepl Error handle

## 0.3.7

- Fix: ebook reader can not load images on Chrome.

## 0.3.6

- UI: better for make ebook page UI

## 0.3.5

- Fix: userscript ebook export
- Feat: add custom API endpoint for OpenAI
- Feat: add temp translate website time options on `Advanced Settings`

## 0.3.4

- CI: Build failed

## 0.3.3

- Fix: ebook maker for Kindle
- Change: Loading icon color, from black to blue, for adapt the dark mode web page.
- Feat: Support local html translate for extension

## 0.3.2

- Fix: Options Form Input cursor moving.
- Feat: OpenAI support custom apiUrl for develope settings.

## 0.3.1

- Feat: update dark icon to transparency.
- Fix: Wrong order for long paragraph

## 0.3.0

- Version: From now on, we will change the minor version number once a month, for example, now in March, the version will start from 0.3.0, in April, the version number will start from 0.3.0, in April, the version number will start from 0.4.0, next April, the version number will be 1.4.0, and so on. This is because it does not make sense for extensions to follow This is because it does not make sense for extensions to follow semantics, but standardizing version numbers according to the laws of time is motivation for development to keep updating, and for users to find problems more easily.
- Feat: Support dark icon for firefox

## 0.2.86

- Add max text length option for per request with Open AI
- Fix: ebook identifier duplicated
- Feat: Support txt web page translation

## 0.2.85

- Fix: some epub file can not be found.

## 0.2.84

- Feat: Support Ebook Reader and Maker

## 0.2.83

- Feat: Allow password input Form show password.

## 0.2.82

- Fix: Some site use `span` for styles, so we use `font` instead of span for translation target wrapper
- Fix: OpenAI max tokens limit, change max chars from 1500 to 1300.

## 0.2.81

- Fix: m.youtube.com
- Fix: options form UI
- Fix: Open AI prompt
- Feat: Support OpenAI multiple keys, use `,` split them.

## 0.2.80

- Feat: Add Enable/Disable Menu for popup -> more
- Fix: DingTalk Message conflict

## 0.2.79

- Fix: Open AI for space paragraph

## 0.2.78

- Feat: support OpenAI CHATGPT 3.5 (supports OpenAI ChatGPT 3.5 interface)
- Feat: Add new theme Solid Border (新增新主题，实线边框)

## 0.2.77

- Fix: multiple code tag error.[#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.76

- Fix: multiple code tag error [#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.75

- Feat: Support custom immediate translation text count for different translation service.

## 0.2.74

- Feat: Support Tencent (alpha)
- Fix: openai translation
- Fix: unknown tags inline check

## 0.2.73

- Feat: Support Grey Translation Theme
- Fix: Github Trending Page

## 0.2.72

- Fix: firefox mobile verify translation service net issue.

## 0.2.71

- Fix: Open AI userscript permission

## 0.2.70

- Fix: Open AI placeholder

## 0.2.69

- Feat: Support Open AI as translation service.
- Feat: Support verify translation service on options.html
- Feat: Support custom main frame cuase some site is not using body as the main frame

## 0.2.68

- Support Caiyun (Alpha)
- Fix unknow block tags

## 0.2.67

- Feat: Add `<all>` for always translate languages, so now you can use it to translate all language except the target language, and never translate languages
- Fix: Allow config custom google API
- Better: Deepl Free support
- Fix: hight memory use for userscripts and extension (by removing opencc zh-CN to zh-TW, instead with Google translate)
- Fix: Relingo [#159] (https://github.com/immersive-translate/immersive-translate/issues/159)
- Fix: Azure translate setup but still show (need setup)

## 0.2.66

- Fix: PDF file translation failed, Bug from 0.2.60 for supporting deepl from zh-CN to zh-TW

## 0.2.65

- Support throttle request for multiple frames
- Do not translate page title when in iframe

## 0.2.64

- Fix: openl choose translation services
- Feat: Support is translate title option

## 0.2.63

- Feat: Support Azure Translate Service
- Feat: Support Papago Translate Service
- Fix: native firefox android google drive sync.
- Fix: change transparency from 0.4 to 0.618 [#147] (https://github.com/immersive-translate/immersive-translate/pull/147)
- Fix: popup shortcuts tips
- Performance: serial to cocurrency requests
- Better for detecting Japanese count

## 0.2.62

- Feat: Add waitForSelectors rule, for fixing some sites like reddit

## 0.2.61

- Fix: userscript is too big for greasy fork
- Better: reduce file size

## 0.2.60

- Feat: Support zh-CN to zh-TW for Deepl
- Feat: Immersive Translate Deepl Feature
- Feat: Support custom font size zoom
- Fix: Steam forum style
- Fix: global style not changed after dynamic elements generated
- Fix: promote exclude priority
- UI: about page change
- Fix: some math element stayoriginal

## 0.2.59

- Fix: Unkowntags Block Element
- Fix: translate=no element overide
- Fix: url match with multiple \*

## 0.2.58

- Feat: Support custom translation text color, border color.

## 0.2.57

- No changes, rebuild

## 0.2.56

- Fix duplicate translate for inline elements with code element.
- Fix unknown tags inline/block check
- Feat: support injected css on developer board
- Feat: trim authKey, appid appSecret
- Better: open settings page on new tab (but not for Stay)

## 0.2.55

- Try fix deepl api charset

## 0.2.54

- Remove tabs permission for chrome store rejection
- Fix translate the whole page, footer is ignored
- Add notes to about page
- Support custom url from buildin Config

## 0.2.53

- Fix userscript google drive sync error.

## 0.2.52

### Code

- Use the latest esbuild
- Use the latest deno version
- CI: submit source code to firefox

## 0.2.51

- Fix Google Auth Need Login on Chrome/Firefox
- Replace translation service links
- Better for permission.
- remove minify.

## 0.2.50

- Fix google drive upload issue (really) [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.49

- Remove shortcuts alt+d, alt+s cause may conflict with native shortcuts.
- Fix google drive upload issue [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.48

- Better for speed, by add minLength to 50 for language detecting.
- Fix Google Drive token validate.

## 0.2.47

- Fix deepl api

## 0.2.46

- fix block mark

## 0.2.45

- Fix element innerText is undefined
- Fix caiyun translation undefined source language

## 0.2.44

- Fix userscript toggle mask
- Fix toggle mask logic

## 0.2.43

- Fix userscript toggle mask with touch event.
- Fix speed (by removing sleep(300))

## 0.2.42

- Fix mask hover when toggle mask again.
- Add mask shortcuts for mobile
- Fix userscript cloud sync issue
- Move advanced option page to left menu.
- Add retry logic to translation service

## 0.2.41

- Fix userscript niu translation
- Fix xhtml translate

## 0.2.40

- Fix beta feature show
- Fix popup setting page on new tab page
- Fix translation placeholder replace

## 0.2.39

- Support shortcuts for show mask translation
- Support enable beta feature at develper panel
- Fix shortcuts in mobile extension

## 0.2.38

- Support loading theme
- Fix getpocket.com
- Fix aside footer for body area
- Fix import/export icon

## 0.2.37

- Fix frame exclude mark

## 0.2.36

- Support sync to Google Drive

## 0.2.35

- Fix japanese rb, rt tag ignore.
- Better for popup ui more
- Better for bad userscript tips
- Add contribution to about page
- Fix volc translate for auto detect language

## 0.2.34

- Fix multiple language speed

## 0.2.33

- Support vertical writing mode, like Japanese.
- Add 3 themes
- Add Niu translation service

## 0.2.32

- Fix PDF basic translation
- Fix popup select a not configured service, go to options page.
- Fix stay open settings.
- Fix multiple language detect speed

## 0.2.31

- Fix dynamic iframe css inject

## 0.2.30

- Support userscript inline iframe translation.
- Support shadowroot translation. For example:
  https://www\.foxnews.com/politics/minnesota-senate-passes-abortion-bill-opponents-call-most-extreme-nation
  Conversation area.
- also check sync rule on popup

## 0.2.29

- Fix Facebook translation
- Support show context menu option.

## 0.2.28

- Remove not standard match for userscript

## 0.2.27

- Support inline iframe translation. (Only for extension, not avaliable for
  userscript)
- Fix multiple language translation

## 0.2.26

- Fix firefox android addon
- Add advanced settings for translation newline

## 0.2.25

- Support iframe translate, like QQ mail, emebed tweet.

## 0.2.24

- Add temp translate site for a while
- Fix stay.app userscript browser API
- Fix stay.app options page

## 0.2.23

- Fix multiple language page translation

## 0.2.22

- Fix userscript build

## 0.2.21

- Fix firefox online pdf translate

## 0.2.20

- Fix macaque request issue
- Fix mark highlihgt line heigh

## 0.2.19

- Fix tencent smart japanese
- Fix haikuo world browser

## 0.2.18

- Fix client url change, auto remain the translate state.
- Remove aside container as the translate container.
- Refactor popup position.

## 0.2.17

- Change highlight to mark
- Add hightlight translation theme

## 0.2.16

- Macaque compatibility

## 0.2.15

- Fix touch bounce issue

## 0.2.14

- Fix safari globalThis.GM not working

## 0.2.13

- Support Userscript Popup Draging
- Support There Fingers on Touch device to trigger toogle translate pages
- Support Hiding the userscript popup icon.

## 0.2.12

- Better for inoreader

## 0.2.11

- Fix
  [#28](https://github.com/immersive-translate/immersive-translate/issues/28)
  Annas archive The main content of the page could not be translated

## 0.2.10

- Fix pdf lineheight distance

## 0.2.9

- Fix exclude elements mark
- Fix deno type check
- remove importmap
- Fix context menus translation
- restore page when never translate this site enabled
- Add description for add url

## 0.2.8

- Detect the user agent language for interface language
- Fix line break bug.

## 0.2.7

- Fix grease monkey request

## 0.2.6

- Fix
  [#30](https://github.com/immersive-translate/immersive-translate/issues/30),
  file url match issue

## 0.2.5

- bump version for ci test

## 0.2.4

- catch message connection error for popup.

## 0.2.3

- Fix
  [#26](https://github.com/immersive-translate/immersive-translate/issues/26)
  create context multiple times

## 0.2.2

- Fix PDF sample file
- Fix Firefox pdf local file
- Fix pdf shortcuts

## 0.2.1

- Support Grease Monkey Shortcuts manager.
- Fix match regex
- Fix youtube comments.
- Fix reddit mobile compact version
- Fix fulltext translate issue

## 0.2.0

- Fix PDF two column.
- Fix Chrome/Edge Store version bug.
- Fix
  [#21] (https://github.com/immersive-translate/immersive-translate/issues/21)

## 0.1.2

- Publish to Firefox addon
- Publish to Edge
- fix pdf margin.
- Change sample pdf file

## 0.0.62

- Fix pdf format, indent.
- Fix telegra.ph prevent element change

## 0.0.61

- Fix span element close.
- Fix permission for early browser

## 0.0.60

- Fix Chrome PDF

## 0.0.59

- Initial Support for PDF

## 0.0.58

- Edit translation theme description

## 0.0.57

- Change popup ui, for more easy use

## 0.0.56

- Fix chrome timeout
- Fix split sentence error.

## 0.0.55

- Fix display none element show.
- refactor element mark

## 0.0.54

- Support line break for X characters.

## 0.0.53

- use sendMessage insteadof connect, cause chrome will disconnect the port after
  5 minites
- better for detecting text containers

## 0.0.52

- Do not translate the paragraph that only has placeholders elements, for
  [example](https://github.com/nank1ro/solidart), the first line.
- Better for detect child elements.

## 0.0.51

- Fix cache issue
  [#12](https://github.com/immersive-translate/next-immersive-translate/issues/12),
  [#7](https://github.com/immersive- translate/next-immersive-translate/issues/7)
- Fix options UI font size

## 0.0.50

- Fix block img be translated.

## 0.0.49

- Fix firefox extension

## 0.0.48

- Fix chrome extension

## 0.0.47

- rewriting message with background, use connect instead of sendMessage
- add reddit mobile support
- fix pre white space for some article

## 0.0.46

- Format userscript meta info

## 0.0.45

- userscript use one file.
- add timeout for cache request

## 0.0.44

- Fix split tencent error.
- Fix inline sup element error.
- Better for twitter

## 0.0.43

- Fix tweet br
- Fix global translate.

## 0.0.42

- Fix BR tag
- treat block tags to rules

## 0.0.41

- Fix inline element check
- Add developer debug log option

## 0.0.39

- Fix translation service contains mock2

## 0.0.38

- Support Cache result for userscript
- Add Options UI
- Support detect more content containers

## 0.0.37

- Fix change popup translation service not work
- Fix reddit mobile post content translate.

## 0.0.36

- Fix Wikipedia special character
  [#6] (https://github.com/immersive-translate/next-immersive-translate/issues/6)
- Fix userscript icon size.
- enable all sites to detect paragraph language.

## 0.0.35

- Fix youtube go to next page
- Support Youtube search page.
- Fix options advanced switch.
- Fix img tag , hiddent tag
  [#5](https://github.com/immersive-translate/next-immersive-translate/issues/5)
- Fix Google Search Force refresh
  [#4](https://github.com/immersive-translate/next-immersive-translate/issues/4)
- Support Table result of Google
  [#3](https://github.com/immersive-translate/next-immersive-translate/issues/3)
- Fix Wikipedia blank
  [#2](https://github.com/immersive-translate/next-immersive-translate/issues/2)

## 0.0.34

### Break Changes

- The Default Hot Key to toggle translate has been changed to `alt+A`, cause
  it's the most convinient key to type.

### Others

- Support set immediate translation mode, so you can let the web page translate
  as quick as possible.
- Support set page area that need to translate. so you can translate more area.
- Support set the first x text count to translate immediately.
- Fix translate duplicately when change translate
- Better popup UI

## 0.0.33

- Support more languages, zh-TW, en

## 0.0.32

- Fix translate local file after saved. Fixed
  [#1](https://github.com/immersive-translate/next-immersive-translate/issues/1)
- Add dist js file to public repo

## 0.0.31

- Support Translate the Whole Page
- Support Translate page immediatlly
- More Config UI
- Reflect the theme
- Add new icon
- Add new translation theme dashedBorder

## 0.0.30

- Better for dashed theme

## 0.0.29

- Fix paragraph valid.
- Add dotted, thinDashed theme
- Better for dashed, highlight theme

## 0.0.28

- Fix underline
- Add dashed, paper theme
- Fix header detected

## 0.0.27

- Support translationTheme

## 0.0.26

- Fix volc alpha userscript connect permission.
- Fix version clickable.

## 0.0.25

- Support selectorMatches, so we can match all manstondon now.
- Fix Firefox userscript error.

## 0.0.23

- Better for Chinese detect
- Fix reddit innerText issue

## 0.0.22

- Support deeplx
- Fix multiple translation when switch service

## 0.0.21

- Fix some span tag is block element

## 0.0.20

- Support not translate hash tags like #hash , at tags like @xxx, $tag, like $APPL
- Support block element

## 0.0.18

- Support deepl, bing,baidu,youdao, volc, openl, caiyun.

## 0.0.13

- Support userscript

## 0.0.4.8

- Fix code order.
- Support basic popup ui

## 0.0.4.6

- Support check new version

## 0.0.3

- Support local files

## 0.0.2

- Support Dynamic Elements
- Support visible translate
