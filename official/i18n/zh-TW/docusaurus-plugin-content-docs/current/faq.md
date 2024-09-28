---
sidebar_position: 9
---

# 常見問題

## Youtube, Facebook 等網站主要內容翻了，但是部分側邊欄沒法，想翻譯全部

為了頁面可讀性，所以沉浸式默認只翻譯主要內容區域。如果想翻譯全部區域。

打開懸浮球面板(移動端長按)->點擊右下角更多->選擇全部區域

## 手機上 Youtube（或其他）APP 不顯示懸浮球

瀏覽器插件只能在瀏覽器中運行，無法在其他 app 中使用

- iOS 瀏覽器上點擊 YouTube 直接打開 App

  長按 YouTube 連結彈出懸浮窗選擇網頁打開

## 如何關閉自動翻譯

- 在 Popup 面板或者設置頁面取消。

- 或者通過設置頁面修改：

## 暫無權限翻譯當前頁面

- 瀏覽器默認頁(地址欄無地址)
- 第三方插件頁面
- Google插件禁止了Google商店頁面

## 如何不顯示原文？

點擊沉浸式翻譯圖標，打開擴展面板，點擊【更多】，【切換到僅譯文模式】

## 頁面出現感嘆號

頁面出現感嘆號，說明翻譯服務遇到問題，返回了錯誤，可以將鼠標移動到感嘆號上查看具體錯誤。

### 429 錯誤

這是最常見的錯誤之一，429 表示請求的頻率過快。網頁翻譯中有非常多的段落需要翻譯，儘管我們已經做了極大的優化，包括合併段落，頻率控制等等，但是有的時候依然有一些翻譯服務不堪重負，返回 429 頻率限制的錯誤，這種時候一般可以暫時切換到其他翻譯服務，或者等一會兒再試。

如果你是 Google 服務遇到的 429，一般來說是Google針對你的節點做了限流，建議切換節點。## 翻譯本地文件

如果你需要翻譯本地的 HTML 文件，txt 文件或者 PDF 文件，你可以點擊沉浸式翻譯擴展圖標，然後點擊【更多】，點擊【翻譯 PDF 文件】或【翻譯 HTML/txt】文件，進行本地文件的翻譯。

如果你使用的是類 Chrome 瀏覽器，如（Chrome，Arc，Edge 瀏覽器），還有另一種辦法，就是在瀏覽器中打開擴展管理頁面`chrome://extensions`,找到【沉浸式翻譯】插件，【允許該擴展訪問本地文件】，之後直接在瀏覽器中打開本地的 HTML 或本地的 PDF 文件，就可以直接右鍵【翻譯】了。

![](https://s.immersivetranslate.com/assets/allow-local-file-1.png)

![](https://s.immersivetranslate.com/assets/allow-pdf-2.png)## 如何更新擴展？

一般來說，在瀏覽器商店安裝的擴展，瀏覽器都會自動進行更新，一般情況會在擴展更新之後的一天內進行自動更新，如果你想立刻更新到最新版本的話，可以在瀏覽器的【擴展管理】頁面，打開【開發者模式】，然後點擊最上面的【更新】，即可立即更新到商店的最新版本。

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/update-extension.png)

## Youtube 字幕設置樣式

可以直接點擊Youtube 自帶的字幕設置，[Options], 然後就可以調整大小，顏色等。

![](https://s.immersivetranslate.com/assets/youtube-subtitle-options.jpeg)## 沉浸式翻譯油猴腳本支援的瀏覽器

桌面端 Chrome, Firefox 推薦使用的油猴擴展：

- [Tamper Monkey](https://www.tampermonkey.net/)

Safari 推薦使用的油猴擴展：

- [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)

> 如果在 Safari 裡使用 [Stay](https://apps.apple.com/cn/app/stay-safari瀏覽器伴侶/id1591620171)的話，請直接在 Stay 自帶的商店裡搜索沉浸式翻譯優化腳本下載（針對 Stay 做了特殊優化）

安卓推薦使用的油猴擴展：

1. 你可以使用 [Firefox 最新版本](https://www.firefox.com.cn/download/#product-android-release)安裝 [Tamper Monkey](https://www.tampermonkey.net/) 擴展。

2. 你也可以直接使用 [X 瀏覽器](https://www.xbext.com/?ref=immersive-translate)，安裝後，直接打開[沉浸式翻譯油猴腳本地址](https://download.immersivetranslate.com/immersive-translate.user.js) 即可安裝

已知不支援的油猴擴展：

- 安卓 Via 瀏覽器
- iOS Alook 瀏覽器

（由於這類瀏覽器並沒有實現所需的油猴 API）## Google翻譯介面被牆問題

請將`translate.googleapis.com` 域名加入到代理規則中

## 如何更新最新規則

擴展本身會在使用的時候定時同步官方最新對網站適配的規則，你也可以手動同步最新的規則，點擊瀏覽器的沉浸式翻譯擴展圖標，打開彈窗後擴展會會自動檢測最新適配規則並同步，油猴腳本同理。

## 網頁翻譯有問題，如何保存網頁反饋？

需要在網頁中右鍵點擊“存儲為” 或者 ctrl+s 快捷鍵，保存選項選擇單個文件，最後文件格式為.mht/.mhtml。 然後將文件發送至 support@immersivetranslate.com

![save mht](https://s.immersivetranslate.com/static/official-static/assets/save_mht.png)

## 彩雲翻譯報錯

點開？號的報錯信息顯示"Unsupported trans_type"。可以手段選擇自動檢測語言為指定語言

## 微信讀書無法翻譯

因為微信讀書針對內容做了特殊處理，防止通過第三方手段獲取內容，所以無法翻譯。## 網頁部分內容未翻譯
一般是網站管理者通過 translate="no" 或者 notranslate class 來約定翻譯插件不然以這塊區域

- 啟用滑鼠懸停功能
- 通過滑鼠懸停來強制翻譯該區域段落內容

## 觸發翻譯不生效

其他網站能翻譯，就某個網站不能翻譯

- 如果這個網站訪問人比較少
  - 建議通過滑鼠懸停來翻譯段落
  - 如果需要翻譯整篇網站可以通過[用戶規則](/docs/advanced/#用戶規則合併增強)適配
- 如果這個網站有很多人用
  - 可以先通過滑鼠懸停翻譯使用
  - 在群裡呼叫，會稍後安排適配

## 輸入框增強不生效

- 瀏覽器主頁 Google 搜索

Google搜索框一定是在[Google](https://www.google.com/)網址的網頁，而不能在瀏覽器主頁，地址欄空白的地方使用## 反饋調試日誌

- 開啟調試日誌
  打開面板 -> 設置 -> 開發者設置 -> 啟用”在控制台打印調試日誌“
- 打開網站的控制台
  右鍵打開審查 -> 右邊欄目頂部切換到控制台 -> 執行操作就可以看到日誌

## 如何關閉懸浮球

- 在當前頁隱藏

設置為 【永不翻譯該網站】 即可

- 在所有頁面隱藏

打開【設置頁】-【界面設置】，關閉【在頁面上顯示懸浮球】即可

## 在 chrome 上安裝插件安裝包報錯

- invalid value for web_accessible_resource[0]

  需要 Chromium 版本大於 88 才能支持 manifest_version 3

## 360 瀏覽器如何安裝

只支持 360 極速瀏覽器 x，記住是帶 x 的。如果可以訪問Google擴展商店，直接可以去那裡裝。如果訪問不了就[手動安裝](/docs/installation/#%E6%89%8B%E5%8B%95%E5%AE%89%E8%A3%85-%E8%BF%BD%E8%B8%AA%E6%9C%80%E6%96%B0%E9%96%8B%E5%8F%91%E7%89%B9%E6%80%A7)## Opera 瀏覽器不生效

- 在 google.com 等搜索頁面不生效，插件顯示`請先刷新當前頁面，再開始翻譯`且刷新頁面仍提示該信息

需要在 Opera 插件設置中找到【沉浸式翻譯】，開啟【允許訪問搜索頁面結果】選項

![](https://s.immersivetranslate.com/static/official-static/assets/opera-allow-search.png)

## YouTube 雙語字幕繁體中文不顯示

YouTube 自帶機翻字幕，繁體中文會出現格式錯誤，導致所有字幕在開始的時候彈出一大段字幕，基於此場景建議在【設置】【影片字幕】中開啟​​【使用沉浸式翻譯來翻譯字幕】選項。

## 鼠標懸停+快捷鍵翻譯功能無效

要啟用鼠標懸停加快捷鍵的翻譯功能，頁面必須首先獲得焦點。如果您發現該功能未能觸發，請嘗試以下步驟：

- 在頁面任意位置點擊一次，以確保頁面獲得焦點。
- 再次嘗試同時使用鼠標懸停和快捷鍵進行翻譯。

如果翻譯功能仍然不響應，請確認您的快捷鍵設置是否正確。## 在 iOS 裝置上無法啟用擴展

如果您在 iOS 裝置上無法啟用擴展，請按照以下步驟操作：

1. 打開【設置】應用。
2. 滑動並點擊【螢幕使用時間】。
3. 選擇【內容和隱私訪問限制】。
4. 點擊進入【內容訪問限制】。
5. 選擇【網頁內容】，並將其設置為【無限制】。

如果您不需要使用內容和隱私訪問限制的其他功能，您也可以選擇直接關閉內容和隱私訪問限制：

1. 打開【設置】應用。
2. 選擇【螢幕使用時間】。
3. 禁用【內容和隱私訪問限制】。

## Safari 打開設置頁面 一直loading

- iOS
  系統設置 -> safari瀏覽器-> 高級 -> 網站數據 -> 編輯 找到 immersivetranslate.com 刪除## 更多問題（非常見）

<details>
<summary>油猴腳本如何清空緩存？</summary>
<p>
由於油猴腳本的API限制，沉浸式翻譯油猴腳本的緩存會保存在對應網站的緩存裡，所以如果要清除的話，可以在瀏覽器打開相應網站的開發者工具面板，然後清空該網站的緩存。
</p>
</details>

<details>
<summary>油猴腳本自定義接口地址請求失敗？</summary>
<p>
油猴腳本要求腳本的所有請求都需要在腳本的開頭聲明權限，比如：`@connect api.google.com`，所以，如果你需要新增一個非默認的域名，請在油猴腳本開頭仿照其他域名進行聲明。
</p>
</details>
