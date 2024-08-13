---
sidebar_position: 1
---

# Installation
<iframe width="560" height="315" src="https://www.youtube.com/embed/SHznc5kQCM4?si=RyZYUcjW560Bc57-" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Desktop Browser

- Microsoft Edge Browser： [Edge Store Immersive Translate](https://microsoftedge.microsoft.com/addons/detail/amkbmndfnliijdhojkpoglbnaaahippg)
- Google Chrome：[Chrome Store Immersive Translate](https://chrome.google.com/webstore/detail/immersive-translate/bpoadfkcbjbfhfodiogcnhhhpibjhbnh)
- Firefox：[Firefox Addon Store Immersive Translate](https://addons.mozilla.org/firefox/addon/immersive-translate/)、[Firefox Addon Store Immersive Translate Beta](https://addons.mozilla.org/firefox/addon/immersive-translate-beta/)

> If you can't access the official Google Store, you can directly download the [Latest Immersive Translate Chrome zip installer](https://download.immersivetranslate.com/latest/chrome-immersive-translate.zip), after downloading, please first Unzip it to a folder you usually use, then type：`chrome://extensions` in the address bar to open the extension management window, then enable "Developer Mode", select "Load Unzipped Extensions", and choose the folder you just unzipped and loaded. Select the folder you just extracted and load it.

## Safari

- [Click here install from App Store](https://apps.apple.com/app/immersive-translate/id6447957425) **It's FREE!!!!**

<div align="center">
<img src="https://s.immersivetranslate.com/static/official-static/assets/immersive-app-store.png" width="150" alt="app store qrcode"/>
</div>

> Instructions：After the first installation, you need to enable the Immersive Translate extension\*\* in safari -> Manage Extensions -> **Enable Immersive Translate Extension** and grant it **Always Allow Access to All Websites**, if you have any questions, you can view the following video tutorial：

### iOS Safari

<video
controls style={{width:"100%", maxWidth:"350px"}}
controls
muted
height="800px"
poster="https://s.immersivetranslate.com/static/official-static/assets/docs/ios_safari_turorial_en.jpeg" src="https://s.immersivetranslate.com/videos/ios_safari_turorial_en.mp4"></video>

### MacOS Safari

<video
controls style={{width:"100%", maxWidth:"500px"}}
controls
muted
poster="https://s.immersivetranslate.com/static/official-static/assets/docs/macOS_safari_en.jpeg" src="https://s.immersivetranslate.com/videos/macOS_safari_tutorial_en.mp4"></video>

## Android

Click to download [Immersive Translate Android Browser](/android/), you need to enable [Immersive Translate] manually in [Extensions] after downloading：

You can try installing Immersive Translate with other Android browsers, such as those that support Firefox extensions or Chrome extensions, such as

- [Firefox Beta or Nightly](https://www.mozilla.org/firefox/channel/android/)
- [Lemur Browser](https://lemurbrowser.com/app/)
- [Kiwi Browser](https://kiwibrowser.com/)

Once installed, search for [Immersive Translate](https://chrome.google.com/webstore/detail/immersive-translate/bpoadfkcbjbfhfodiogcnhhhpibjhbnh) directly in the chrome store to install it.

## Installation via Tampermonkey

If you can't install the official extension for Immersive Translates in the way described above, you can install Tampermonkeys by：

Tampermonkey Address： https://download.immersivetranslate.com/immersive-translate.user.js

Open [this address](https://download.immersivetranslate.com/immersive-translate.user.js) in a browser that has the Grease Monkey extension installed to install it.Here are a few browsers that support Tampermonkey：

**Firefox for Android**

1. Download [Firefox Latest Version](https://www.mozilla.org/firefox/browsers/mobile/android/) Version
2. Find [Tamper Monkey](https://www.tampermonkey.net/) in Firefox's recommended add-ons and install it.
3. Install [Tampermonkey](https://download.immersivetranslate.com/immersive-translate.user.js) for this extension (open this link in your Firefox browser to see the installation page)
4. After installation, open any web page and the floating window icon of the Immersive Translate extension will appear on the right side.

**Apple Safari Browser [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)**

1. Install the [Userscripts safari plugin](https://itunes.apple.com/us/app/userscripts/id1463298887) and grant it the "Always allow access to any website" permission.
2. Install [Tampermonkey](https://download.immersivetranslate.com/immersive-translate.user.js) for this extension (open this link in Safari browser and click on the Userscript extension icon to see the installation page)
3. After installation, open any web page and refresh it, a floating window of this extension will appear on the right side of the page.(If you are experiencing problems with floating windows not appearing, we recommend refreshing the page more often or force restarting Safari for it to take effect)

<!-- If you have questions when installing, you can refer to [YouTube video tutorial](https://www.youtube.com/watch?v=IWOFFWDfZGY)

<iframe width="560" height="315" src="https://www.youtube.com/embed/IWOFFWDfZGY" title="YouTube video player" frameBorder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowFullScreen></iframe> -->

## Manual installation (to keep track of the latest development features)

The advantage of manual installation is that you don't have to wait for the store to review it and you can experience the features of the latest development version immediately：

1. Download the zip package at [release page](https://github.com/immersive-translate/immersive-translate/releases/)
2. Extract the zip to a common folder, such as `Documents/chrome-immersive-translate`.
3. installation

- Install：(1) Type：`chrome://extensions` in the address bar to open the Extension Manager window; (2) Open "Developer Mode", select "Load Unzipped Extensions", and choose the folder you just unzipped to load. the folder you just unzipped and load it.
- Firefox Browser Installation：(1) Type： `about:debugging#/runtime/this-firefox` in the address bar to open the Extension Manager window; (2) Temporarily load the add-on and select `firefox/manifest.json`.

### How do I update a manually installed extension?

Download the latest installer from [Release page](https://github.com/immersive-translate/immersive-translate/releases/), delete the contents of the original folder, then copy the contents of the latest zip archive to the original folder, and finally on the extension management page Click `Reload`.

> If you're used to the command line, you can use `git clone https://github.com/immersive-translate/immersive-translate.git`, then install `dist/chrome` and you'll be able to synchronize with `git pull` every time.
