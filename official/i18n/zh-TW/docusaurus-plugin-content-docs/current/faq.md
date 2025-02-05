---
sidebar_position: 9
---

# 常見問題

## 安全相關

### 1. Android App，手機安全中心誤報

經開發排查這是由於騰訊安全中心誤報，可從 [官網](https://immersivetranslate.com/) 卸載安裝最新版本

## 安裝相關

### 1. 如何更新擴展

一般來說，在瀏覽器商店安裝的擴展，瀏覽器都會自動進行更新，一般情況會在擴展更新之後的一天內進行自動更新，如果你想立刻更新到最新版本的話，可以在瀏覽器的【擴展管理】頁面，打開【開發者模式】，然後點擊最上面的【更新】，即可立即更新到商店的最新版本。

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/update-extension.png)

### 2. 沉浸式翻譯油猴腳本支持的瀏覽器

iOS：

- [Tamper Monkey 瀏覽器](https://www.tampermonkey.net/)
- 安裝油猴擴展後的 Safari 瀏覽器，可安裝的油猴擴展：
  - [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)
  - [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171)：建議直接在 Stay 自帶的商店裡搜索沉浸式翻譯優化腳本下載（針對 Stay 做了特殊優化）。

Android：

- [Firefox 最新版本](https://www.firefox.com.cn/download/#product-android-release)：安裝完成後，再安裝 [Tamper Monkey](https://www.tampermonkey.net/) 擴展。
- [X 瀏覽器](https://www.xbext.com/?ref=immersive-translate)：安裝後，直接打開[沉浸式翻譯油猴腳本地址](https://download.immersivetranslate.com/immersive-translate.user.js) 即可安裝。

已知不支持的油猴擴展的瀏覽器（這類瀏覽器並沒有實現所需的油猴 API）：

- 安卓 Via 瀏覽器
- iOS Alook 瀏覽器

### 3. 在 chrome 上安裝插件安裝包報錯

報錯 `invalid value for web_accessible_resource[0]`：需要 Chromium 版本大於 88 才能支持 manifest_version 3。

### 4. 360 瀏覽器如何安裝

只支持 360 極速瀏覽器 x，記住是帶 x 的。如果可以訪問谷歌擴展商店，直接可以去那裡裝。如果訪問不了就 [手動安裝](/docs/installation/#%E6%89%8B%E5%8A%A8%E5%AE%89%E8%A3%85-%E8%BF%BD%E8%B8%AA%E6%9C%80%E6%96%B0%E5%BC%80%E5%8F%91%E7%89%B9%E6%80%A7)。

### 5. Opera 瀏覽器不生效

在 google.com 等搜索頁面不生效，插件顯示`請先刷新當前頁面，再開始翻譯`且刷新頁面仍提示該信息：需要在 Opera 插件設置中找到【沉浸式翻譯】，開啟【允許訪問搜索頁面結果】選項。

![](https://s.immersivetranslate.com/static/official-static/assets/opera-allow-search.png)

### 6. 在 iOS 設備上無法啟用擴展

如果您在 iOS 設備上無法啟用擴展，請按照以下步驟操作：

1. 打開【設置】應用
2. 滑動並點擊【屏幕使用時間】
3. 選擇【內容和隱私訪問限制】
4. 點擊進入【內容訪問限制】
5. 選擇【網頁內容】，並將其設置為【無限制】

如果您不需要使用內容和隱私訪問限制的其他功能，您也可以選擇直接關閉內容和隱私訪問限制：

1. 打開【設置】應用
2. 選擇【屏幕使用時間】
3. 禁用【內容和隱私訪問限制】

### 7. Safari 打開設置頁面 一直 loading

系統設置 -> safari 瀏覽器-> 高級 -> 網站數據 -> 編輯 找到 immersivetranslate.com 刪除

### 8. iOS18 安裝後進入設置頁面登錄時跳轉到空白頁面

長按懸浮球點擊頭像去登錄。

### 9. crx 文件拖拽至瀏覽器擴展程序，顯示文件不存在

需要先解壓壓縮包，再單獨拖 CRX 文件。

## 基礎翻譯相關

### 1. Youtube, Facebook 等網站主要內容翻了，但是部分側邊欄沒法，想翻譯全部

為了頁面可讀性，所以沉浸式默認只翻譯主要內容區域。如果想翻譯全部區域。

打開懸浮球面板 (移動端長按) -> 點擊右下角更多 -> 選擇全部區域。

### 2. 手機 App 中不顯示懸浮球

- 沉浸式翻譯插件為瀏覽器插件，**只能在瀏覽器**中運行，無法在其他 app 中使用，不支持其他 App 內部翻譯。

- 在哪個瀏覽器安裝插件即可在哪個瀏覽器使用，**無法跨瀏覽器**（如在 Safari 內安裝不可以在 Chrome 內使用插件）

### 3. iOS 瀏覽器上點擊 YouTube 直接打開 App，無法進入網頁翻譯

長按 YouTube 鏈接彈出懸浮窗選擇網頁打開。

### 4. 如何關閉自動翻譯

- 在 Popup 面板或者設置頁面取消。
- 或者通過設置頁面修改

### 5. 暫無權限翻譯當前頁面

- 瀏覽器默認頁 (地址欄無地址)
- 第三方插件頁面
- 谷歌插件禁止了谷歌商店頁面

### 6. 如何不顯示原文

點擊沉浸式翻譯圖標，打開擴展面板，點擊【更多】，【切換到僅譯文模式】。

### 7. 頁面出現感嘆號

頁面出現感嘆號，說明翻譯服務遇到問題，返回了錯誤，可以將鼠標移動到感嘆號上查看具體錯誤。

#### 例如：429 錯誤

這是最常見的錯誤之一，429 表示請求的頻率過快。網頁翻譯中有非常多的段落需要翻譯，儘管我們已經做了極大的優化，包括合併段落，頻率控制等等，但是有的時候依然有一些翻譯服務不堪重負，返回 429 頻率限制的錯誤，這種時候一般可以暫時切換到其他翻譯服務，或者等一會兒再試。

如果你是 Google 服務遇到的 429，一般來說是谷歌針對你的節點做了限流，建議切換節點。

### 8. 怎麼切換翻譯源與目標語言

移動端長按懸浮球，電腦端鼠標移動至懸浮球喚出設置，選擇其他翻譯服務/其他目標語言。

<img src="https://s.immersivetranslate.com/static/official-static/assets/change-lang1.png" alt="description" width="200" style={{marginRight: "100px"}}/>
<img src="https://s.immersivetranslate.com/static/official-static/assets/change-lang2.png" alt="description" width="280"/>

### 9. 谷歌翻譯接口被牆問題

請將`translate.googleapis.com` 域名加入到代理規則中。

### 10. OpenAI 封禁中國地區 API Key 對會員 AI 服務是否有影響

沒有影響，產品使用 Azure 企業版 OpenAI，不受 API 地區限制。

### 11. 彩雲翻譯報錯

點開`?`號的報錯信息顯示"Unsupported trans_type"。可以手段選擇自動檢測語言為指定語言。

### 12. 微信讀書無法翻譯

因為微信讀書針對內容做了特殊處理，防止通過第三方手段獲取內容，所以無法翻譯。

### 13. 網頁部分內容未翻譯

一般是網站管理者通過 `translate="no"` 或者 `notranslate class` 來約定翻譯插件不翻譯這塊區域，不過可通過以下方式解決：

1. 啟用鼠標懸停功能
2. 通過鼠標懸停來強制翻譯該區域段落內容

### 14. 觸發翻譯不生效

其他網站能翻譯，就某個網站不能翻譯時：

- 如果這個網站訪問人比較少
  - 建議通過鼠標懸停來翻譯段落
  - 如果需要翻譯整篇網站可以通過 [用戶規則](/docs/advanced/#用戶規則合併增強) 適配
- 如果這個網站有很多人用
  - 可以先通過鼠標懸停翻譯使用
  - 在群裡呼叫，會稍後安排適配

### 15. 網頁翻譯有問題，如何保存網頁反饋

需要在網頁中右鍵點擊“存儲為”或者 ctrl+s 快捷鍵，保存選項選擇單個文件，最後文件格式為.mht/.mhtml。然後將文件發送至 support@immersivetranslate.com。

![save mht](https://s.immersivetranslate.com/static/official-static/assets/save_mht.png)

### 16. 查看調試日誌

1. 開啟調試日誌：打開面板 -> 設置 -> 開發者設置 -> 啟用”在控制台打印調試日誌“。
2. 打開網站的控制台：右鍵打開審查 -> 右邊欄目頂部切換到控制台 -> 執行操作就可以看到日誌。

### 17. 如何關閉懸浮球

- 在當前頁隱藏：設置為【永不翻譯該網站】即可
- 在所有頁面隱藏：打開【設置頁】-【界面設置】，關閉【在頁面上顯示懸浮球】即可

### 18. 鼠標懸停 + 快捷鍵翻譯功能無效

要啟用鼠標懸停加快捷鍵的翻譯功能，頁面必須首先獲得焦點。如果您發現該功能未能觸發，請嘗試以下步驟：

1. 在頁面任意位置點擊一次，以確保頁面獲得焦點。
2. 再次嘗試同時使用鼠標懸停和快捷鍵進行翻譯。
3. 如果翻譯功能仍然不響應，請確認您的快捷鍵設置是否正確。

### 19. 如何更新最新規則

擴展本身會在使用的時候定時同步官方最新對網站適配的規則，你也可以手動同步最新的規則，點擊瀏覽器的沉浸式翻譯擴展圖標，打開彈窗後擴展會會自動檢測最新適配規則並同步，油猴腳本同理。

### 20. 翻譯失敗 / 翻譯一直轉圈

1. 查看失敗原因

   - 如額度達到限制則是會員當月該翻譯源額度用盡
   - 如翻譯顯示網絡錯誤請先檢查自身節點/網絡狀態

2. 切換翻譯源，長按懸浮球選擇其他翻譯源

### 21. Pro 會員翻譯額度與用量如何查詢

- Pro 會員每月可享受 2000 萬 Token 的基礎翻譯額度，該額度可用於所有翻譯服務，無論是全部用於 DeepL（相當於 2000 萬字符）、全部用於 OpenAI（2000 萬 Token），還是混合使用多個服務，您都可以根據實際需求自由分配額度

  > OpenAI 的定價是基於 token 的，對於英文文本，1 個 token 大約是 4 個字符或 0.75 個單詞。通常 1000 個 Token 約等於 750 個英文單詞或者 400~500 個漢字。

- 用量查詢地址： [https://immersivetranslate.com/accounts/usage](https://immersivetranslate.com/accounts/usage)

### 22. 各 AI 翻譯是否共用額度

是的，Openai，Gemini，Claude 以及 DeepL 相當於 共用 2000w token 限額。

## 視頻翻譯相關

### 1. Youtube 字幕設置樣式

可以直接點擊 Youtube 自帶的字幕設置，[Options], 然後就可以調整大小，顏色等。

![](https://s.immersivetranslate.com/assets/youtube-subtitle-options.jpeg)

### 2. YouTube 雙語字幕繁體中文不顯示

YouTube 自帶機翻字幕，繁體中文會出現格式錯誤，導致所有字幕在開始的時候彈出一大段字幕，基於此場景建議在【設置】【視頻字幕】中開啟【使用沉浸式翻譯來翻譯字幕】選項。

### 3. Bilibili 如何開啟字幕翻譯

在翻譯 Bilibili 視頻字幕時，請按以下步驟操作：

1. 先開啟 Bilibili 內置字幕，點擊播放器右下角的“字幕”按鈕即可。如果視頻沒有字幕按鈕或字幕內容，則不支持雙語字幕。
2. 點擊播放器中的“沉浸式翻譯”圖標，開啟雙語字幕功能。

使用時需注意：

1. 確保已經開啟 Bilibili 的內置字幕。
2. 確保沉浸式翻譯的目標語言與 Bilibili 內置字幕的語言不同，以觸發翻譯功能。

### 4. Netflix 字幕翻譯用原始字幕樣式

- 當前 Netflix 採用漸進式翻譯方案，字幕樣式自託管，不支持人工字幕。
- 舊 Hook 方案，需要等到所有字幕翻譯完才會顯示字幕，支持人工字幕。

如何回退至舊方案，進入【[開發者設置](https://dash.immersivetranslate.com/#developer)】找到【Edit User Rules】
添加如下規則

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

## 文件翻譯相關

### 1. 如何翻譯本地文件

- 方法一：進入[沉浸式翻譯文件翻譯官網](https://app.immersivetranslate.com/)，也可以點擊沉浸式翻譯擴展圖標，點擊【文件翻譯】進入。

- 方法二：如果使用的是類 Chrome 瀏覽器，如（Chrome，Arc，Edge 瀏覽器），還有另一種辦法，就是在瀏覽器中打開擴展管理頁面`chrome://extensions`,找到【沉浸式翻譯】插件，【允許該擴展訪問本地文件】，之後直接在瀏覽器中打開本地的 HTML 或本地的 PDF 文件，就可以直接右鍵【翻譯】了。

  ![](https://s.immersivetranslate.com/assets/allow-local-file-1.png)

  ![](https://s.immersivetranslate.com/assets/allow-pdf-2.png)

### 2. 頁數過多時 PDF 文件翻譯過慢

建議裁剪為多個 100 頁以下的部分再進行翻譯，翻譯完成後再進行合併

### 3. PDF 翻譯譯文重複重疊

為源文件自身識別問題，目前建議手動點擊該部分，刪除多餘文本框，後續會持續優化這種情況

### 4. 是否有術語表 / 某些詞彙特殊翻譯或不翻譯

我們提供術語表配置功能，您可以通過術語表來指定某些詞彙不被翻譯，或將其翻譯為特定內容。詳細配置請參閱“高級自定義”中的“自定義專業術語翻譯”部分：[點擊這裡查看](https://immersivetranslate.com/docs/advanced)

### 5. Word 文件翻譯後無法導出為 Word 格式

目前 word 文件導出存在一定技術問題，建議保持現有格式，正在持續優化中

### 6. PDF 如何調整最小字號

這是因為瀏覽器限制的最小字號，調整瀏覽器字體到最低，以 chrome 為例：點擊 [chrome 字號設置](chrome://settings/fonts?search=%E5%AD%97%E5%8F%B7)

## 輸入框翻譯相關

### 1. 輸入框增強不生效

- 已知明確不支持的瀏覽器：詳見 [輸入框翻譯](https://immersivetranslate.com/docs/input/) 兼容性部分
- 在網址欄或瀏覽器初始頁無法翻譯，僅支持搜索欄，可至 https://www.bing.com/ 測試
- 加快空格連擊速度

## 支付相關

### 1. 是否能用微信支付

微信支付需要私信群內工作人員並備註“微信支付”，在工作人員提供收款碼之後付款，並提供相應的付款詳情。工作人員會提供所需的年/月會員兌換碼，在 [兌換會員頁](https://immersivetranslate.com/exchange/) 中兌換

### 2. 是否能開發票

目前僅支持年費會員開具發票。已經支付的用戶需要發票請私信群內工作人員並備註“發票問題”，未支付的用戶可查看：[年會員開票須知](https://immersivetranslate.com/bill/)

## 更多問題（非常見）

### 油猴腳本如何清空緩存？

由於油猴腳本的 API 限制，沉浸式翻譯油猴腳本的緩存會保存在對應網站的緩存裡，所以如果要清除的話，可以在瀏覽器打開相應網站的開發者工具面板，然後清空該網站的緩存。

### 油猴腳本自定義接口地址請求失敗？

油猴腳本要求腳本的所有請求都需要在腳本的開頭聲明權限，比如：`@connect api.google.com`，所以，如果你需要新增一個非默認的域名，請在油猴腳本開頭仿照其他域名進行聲明。

### 瀏覽器報錯“create menu error Error: IO error: .../MANIFEST-000001: Unable to create sequential file (ChromeMethodBFE: 7::NewSequentialFile::4)”？

這個錯誤通常與瀏覽器本身的緩存或本地存儲有關，具體是在創建或訪問文件 `MANIFEST-000001` 時發生的。在確保磁盤充足的情況下，您可以通過重裝瀏覽器解決該問題。

### 雙語字幕如何下載 / 其他網站雙語字幕能否下載？

- 目前僅支持在電腦端進行字幕下載。
- 包括 Youtube，當有字幕下載按鈕時，當前網站即可支持雙語字幕下載。
