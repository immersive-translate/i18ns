---
sidebar_position: 9
---

# 常見問題

## Youtube, Facebook 等網站主要內容翻了，但是部分側邊欄沒法，想翻譯全部

為了頁面可讀性，所以沉浸式預設只翻譯主要內容區域。如果想翻譯全部區域。

開啟懸浮球面板 (移動端長按)->點選右下角更多->選擇全部區域

## 手機上 Youtube（或其他）APP 不顯示懸浮球

瀏覽器外掛只能在瀏覽器中執行，無法在其他 app 中使用

- iOS 瀏覽器上點選 YouTube 直接開啟 App

  長按 YouTube 連結彈出懸浮窗選擇網頁開啟

## 如何關閉自動翻譯

- 在 Popup 面板或者設定頁面取消。

- 或者透過設定頁面修改：

## 暫無權限翻譯目前頁面

- 瀏覽器預設頁 (位址列無地址)
- 第三方外掛頁面
- Google 外掛禁止了 Google 商店頁面

## 如何不顯示原文？

點選沉浸式翻譯圖示，開啟擴充套件面板，點選【更多】，【切換到僅譯文模式】

## 頁面出現感嘆號

頁面出現感嘆號，說明翻譯服務遇到問題，返回了錯誤，可以將滑鼠移動到感嘆號上檢視具體錯誤。

### 429 錯誤

這是最常見的錯誤之一，429 表示請求的頻率過快。網頁翻譯中有非常多的段落需要翻譯，儘管我們已經做了極大的最佳化，包括合併段落，頻率控制等等，但是有的時候依然有一些翻譯服務不堪重負，返回 429 頻率限制的錯誤，這種時候一般可以暫時切換到其他翻譯服務，或者等一會兒再試。

如果你是 Google 服務遇到的 429，一般來說是 Google 針對你的節點做了限流，建議切換節點。

## 翻譯本機文件

如果你需要翻譯本機的 HTML 文件，txt 文件或者 PDF 文件，你可以點選沉浸式翻譯擴充套件圖示，然後點選【更多】，點選【翻譯 PDF 文件】或【翻譯 HTML/txt】文件，進行本機文件的翻譯。

如果你使用的是類 Chrome 瀏覽器，如（Chrome，Arc，Edge 瀏覽器），還有另一種辦法，就是在瀏覽器中開啟擴充套件管理頁面`chrome://extensions`,找到【沉浸式翻譯】外掛，【允許擴充套件存取本機文件】，之後直接在瀏覽器中開啟本機的 HTML 或本機的 PDF 文件，就可以直接右鍵【翻譯】了。

![](https://s.immersivetranslate.com/assets/allow-local-file-1.png)

![](https://s.immersivetranslate.com/assets/allow-pdf-2.png)

## 如何更新擴充套件？

一般來說，在瀏覽器商店安裝的擴充套件，瀏覽器都會自動進行更新，一般情況會在擴充套件更新之後的一天內進行自動更新，如果你想立刻更新到最新版本的話，可以在瀏覽器的【擴充套件管理】頁面，開啟【開發者模式】，然後點選最上面的【更新】，即可立即更新到商店的最新版本。

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/update-extension.png)

## Youtube 字幕設定樣式

可以直接點選 Youtube 內建的字幕設定，[Options], 然後就可以調整大小，顏色等。

![](https://s.immersivetranslate.com/assets/youtube-subtitle-options.jpeg)

## 沉浸式翻譯油猴腳本支援的瀏覽器

桌面端 Chrome, Firefox 推薦使用的油猴擴充套件：

- [Tamper Monkey](https://www.tampermonkey.net/)

Safari 推薦使用的油猴擴充套件：

- [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)

> 如果在 Safari 裡使用 [Stay](https://apps.apple.com/tw/app/stay-safari瀏覽器伴侶/id1591620171)的話，請直接在 Stay 內建的商店裡搜尋沉浸式翻譯最佳化腳本下載（針對 Stay 做了特殊最佳化）

安卓推薦使用的油猴擴充套件：

1. 你可以使用 [Firefox 最新版本](https://www.mozilla.org/zh-TW/firefox/browsers/mobile/android/)安裝 [Tamper Monkey](https://www.tampermonkey.net/) 擴充套件。

2. 你也可以直接使用 [X 瀏覽器](https://www.xbext.com/?ref=immersive-translate)，安裝後，直接開啟[沉浸式翻譯油猴腳本地址](https://download.immersivetranslate.com/immersive-translate.user.js) 即可安裝

已知不支援的油猴擴充套件：

- 安卓 Via 瀏覽器
- iOS Alook 瀏覽器

（由於這類瀏覽器並沒有實現所需的油猴 API）

## Google 翻譯介面被牆問題

請將`translate.googleapis.com` 域名加入到代理規則中

## 如何更新最新規則

擴充套件本身會在使用的時候定時同步官方最新對網站適配的規則，你也可以手動同步最新的規則，點選瀏覽器的沉浸式翻譯擴充套件圖示，開啟彈窗後擴充套件會會自動偵測最新適配規則並同步，油猴腳本同理。

## 網頁翻譯有問題，如何儲存網頁回饋？

需要在網頁中右鍵點選“儲存為”或者 ctrl+s 快捷鍵，儲存選項選擇單個文件，最後文件格式為.mht/.mhtml。然後將文件傳送至 support@immersivetranslate.com

![save mht](https://s.immersivetranslate.com/static/official-static/assets/save_mht.png)

## 彩雲翻譯報錯

點開？號的報錯資訊顯示"Unsupported trans_type"。可以手段選擇自動偵測語言為指定語言

## 微信讀書無法翻譯

因為微信讀書針對內容做了特殊處理，防止透過第三方手段取得內容，所以無法翻譯。

## 網頁部分內容未翻譯

一般是網站管理者透過 translate="no" 或者 notranslate class 來約定翻譯外掛不然以這塊區域

- 啟用滑鼠懸停功能
- 透過滑鼠懸停來強制翻譯該區域段落內容

## 觸發翻譯不生效

其他網站能翻譯，就某個網站不能翻譯

- 如果這個網站存取人比較少
  - 建議透過滑鼠懸停來翻譯段落
  - 如果需要翻譯整篇網站可以透過[使用者規則](/docs/advanced/#使用者規則合併增強)適配
- 如果這個網站有很多人用
  - 可以先透過滑鼠懸停翻譯使用
  - 在群裡呼叫，會稍後安排適配

## 輸入框增強不生效

- 瀏覽器首頁 Google 搜尋

Google 搜尋框一定是在[Google](https://www.google.com/)網址的網頁，而不能在瀏覽器首頁，位址列空白的地方使用

## 回饋除錯日誌

- 開啟除錯日誌
  開啟面板 -> 設定 -> 開發者設定 -> 啟用”在控制檯列印除錯日誌“
- 開啟網站的控制檯
  右鍵開啟審查 -> 右邊欄目頂端切換到控制檯 -> 執行操作就可以看到日誌

## 如何關閉懸浮球

- 在目前頁隱藏

設定為【永不翻譯該網站】即可

- 在所有頁面隱藏

開啟【設定頁面】-【介面設定】，關閉【在頁面上顯示懸浮球】即可

## 在 chrome 上安裝外掛安裝檔報錯

- invalid value for web_accessible_resource[0]

  需要 Chromium 版本大於 88 才能支援 manifest_version 3

## 360 瀏覽器如何安裝

只支援 360 極速瀏覽器 x，記住是帶 x 的。如果可以存取 Google 擴充套件商店，直接可以去那裡裝。如果存取不了就[手動安裝](/docs/installation/#%E6%89%8B%E5%8B%95%E5%AE%89%E8%A3%85-%E8%BF%BD%E8%B8%AA%E6%9C%80%E6%96%B0%E9%96%8B%E5%8F%91%E7%89%B9%E6%80%A7)

## Opera 瀏覽器不生效

- 在 google.com 等搜尋頁面不生效，外掛顯示`請先重新整理目前頁面，再開始翻譯`且重新整理頁面仍提示該資訊

需要在 Opera 外掛設定中找到【沉浸式翻譯】，開啟【允許存取搜尋頁面結果】選項

![](https://s.immersivetranslate.com/static/official-static/assets/opera-allow-search.png)

## YouTube 雙語字幕繁體中文不顯示

YouTube 內建機翻字幕，繁體中文會出現格式錯誤，導致所有字幕在開始的時候彈出一大段字幕，基於此場景建議在【設定】【影片字幕】中開啟​​【使用沉浸式翻譯來翻譯字幕】選項。

## 滑鼠懸停 + 快捷鍵翻譯功能無效

要啟用滑鼠懸停加快捷鍵的翻譯功能，頁面必須首先獲得焦點。如果您發現該功能未能觸發，請嘗試以下步驟：

- 在頁面任意位置點選一次，以確保頁面獲得焦點。
- 再次嘗試同時使用滑鼠懸停和快捷鍵進行翻譯。

如果翻譯功能仍然不響應，請確認您的快捷鍵設定是否正確。

## 在 iOS 裝置上無法啟用擴充套件

如果您在 iOS 裝置上無法啟用擴充套件，請按照以下步驟操作：

1. 開啟【設定】應用。
2. 滑動並點選【螢幕使用時間】。
3. 選擇【內容和隱私存取限制】。
4. 點選進入【內容存取限制】。
5. 選擇【網頁內容】，並將其設定為【無限制】。

如果您不需要使用內容和隱私存取限制的其他功能，您也可以選擇直接關閉內容和隱私存取限制：

1. 開啟【設定】應用。
2. 選擇【螢幕使用時間】。
3. 停用【內容和隱私存取限制】。

## Safari 開啟設定頁面 一直 loading

- iOS
  系統設定 -> safari 瀏覽器-> 進階 -> 網站資料 -> 編輯 找到 immersivetranslate.com 刪除

## 更多問題（非常見）

<details>
<summary>油猴腳本如何清空快取？</summary>
<p>
由於油猴腳本的 API 限制，沉浸式翻譯油猴腳本的快取會儲存在對應網站的快取裡，所以如果要清除的話，可以在瀏覽器開啟相應網站的開發者工具面板，然後清空該網站的快取。
</p>
</details>

<details>
<summary>油猴腳本自訂介面地址請求失敗？</summary>
<p>
油猴腳本要求腳本的所有請求都需要在腳本的開頭宣告權限，比如：`@connect api.google.com`，所以，如果你需要新增一個非預設的域名，請在油猴腳本開頭仿照其他域名進行宣告。
</p>
</details>
