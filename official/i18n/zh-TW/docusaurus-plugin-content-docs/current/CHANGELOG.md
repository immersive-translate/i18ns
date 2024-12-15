---
sidebar_position: 6
---

# 更新日誌

## 1.12.3 (2024-12-13)

- 新增：AI智能上下文翻譯，在一些專業內容上可以使翻譯更準確。（僅限Pro會員使用）【設定】->【基本設定】->【啟用AI智能上下文翻譯】
- 修復：推特多行翻譯效果下的部分 bug。
- 修復：富文本導致部分公式翻譯的問題。
- 優化：在推特翻譯時，有字幕的視頻會自動翻譯雙語字幕。
- 優化：無字幕視頻顯示翻譯圖標，並告知無法翻譯的原因。

## 1.11.7 (2024-11-25)

- 新增：Bing/Google 支持柬埔寨語（高棉語）。
- 新增：允許未翻譯完成的 ePub 文件在再次導入時從上次停止處繼續翻譯。
- 修復：在 Safari 瀏覽器中無法翻譯 Twitter 圖片的問題。
- 修復：在開啟或關閉【**鼠標懸停翻譯**】功能時，快捷鍵失效的問題。
- 優化：改進Twitter,Youtube多行雙語對照翻譯的顯示效果。
- 優化：在雙語模式下，預設關閉富文本翻譯以提升翻譯質量。
- ~~優化：【**進階設置**】中添加了自定義【**側邊欄和導航條翻譯**】的選項。~~
- 優化：在【**鼠標懸停-直接翻譯該段**】模式下，不再翻譯圖片。

## 1.11.4 (2024-11-16)

- 修復：1.11.2版本中由於"Twitter翻譯改進"引起的公式翻譯問題。

## 1.11.2 (2024-11-13)

- 修復：在Facebook僅譯文模式下，點擊seemore後導致內容消失的問題。
- ~~優化：改進Twitter多行雙語對照翻譯的顯示效果。~~
- 優化：改進面板中翻譯服務下拉列表的用戶界面(UI)。

## 1.11.1 (2024-11-05)

- 新增：實時會議的【字幕翻譯】新增懸浮球觸發支持，適用於Zoom、Google Meet和Microsoft Teams。
- 修復：YouTube【字幕翻譯】在觀看廣告後時間軸不同步的問題。
- 修復：MacOS 15 Safari瀏覽器中右鍵翻譯菜單顯示異常的問題。
- 修復：部分網站【輸入框增強】的Ctrl+Z撤銷操作無效的問題。

## 1.10.6 (2024-10-25)

- 修復：【輸入框增強】快捷鍵無法觸發的問題
- 優化：減小安裝包大小
- 優化：Netflix字幕顯示方案調優

## 1.10.5 (2024-10-23)

- 新增：當源語言和目標語言一致時顯示警告提示
- 修復：富文本空白字符翻譯問題 [#2175](https://github.com/immersive-translate/immersive-translate/issues/2175)
- 優化：網頁內嵌 iframe 裡的輸入增強，鼠標懸停功能

## 1.10.2 (2024-10-11)

- 新增：圖片翻譯Beta版（僅支持會員可用，非油猴版本），在【設置】->【開發者】->【開啟beta】
- 新增：僅滑鼠模式（僅當平板設備的鼠標hover功能失效時才需開啟此功能）【設置】->【進階設置】->【啟用僅滑鼠模式】
- 新增：影片字幕翻譯失敗後，顯示錯誤信息
- 修復：富文本翻譯問題 [#2163](https://github.com/immersive-translate/immersive-translate/issues/2163)
- 優化：PDF翻譯時可能出現的翻譯按鈕失效的問題
- 優化：提升譯文中公式的渲染效果
- 優化：語言選擇列表

## 1.9.8 (2024-09-28)

- 新增：翻譯服務「智普GLM翻譯」
- 移除：「SiliconCloud翻譯」模型qwen1.5-7B-chat（由於官方不再支持）
- 修復：解決 macOS 15 上 Safari 插件的登錄兼容性問題

## 1.9.7 (2024-09-20)

- 輸入增強支援Gmail輸入框
- 支援 Claude Anthropic API 的 anthropic-dangerous-direct-browser-access 請求頭
- 支援 Hulu、Bloomberg、Domestika 影片字幕下載
- DeepX 支援富文本翻譯
- 修復自定義 AI 專家無法同步的問題

## 1.9.6 (2024-09-13)

- [PDF Pro](https://app.immersivetranslate.com/pdf-pro/) 支援公式複製（在公式上右鍵即可看到複製的菜單）
- 修復推特同一網頁多個影片的雙語字幕顯示問題
- 修復一些 Bug

## 1.9.3 (2024-09-05)

- 雙語對照/僅顯示譯文設置項遷移到通用設置中
- 默認將會記住在面板中點擊圖標切換雙語對照模式/僅顯示譯文默認，如需臨時切換，需要點擊面板中的【更多】 -> 【切換為僅顯示譯文】
- 默認情況下，簡體中文翻譯為繁體中文，繁體中文翻譯為簡體中文將使用僅顯示譯文模式，而不是雙語對照模式
- 修復一些 Bug

## 1.9.1 (2024-09-03)

- 支援為雙語對照或僅譯文模式配置例外的語言和網站（在設置頁面->進階設置中配置）。比如：如果您的默認翻譯模式是雙語對照，但是您並不希望繁體中文也使用雙語對照，此時您可以在雙語對照的例外語言中添加繁體中文，這樣繁體中文將會使用僅譯文模式翻譯。同理，如果您的默認翻譯模式是僅譯文，但是您希望某個語言或網站使用雙語對照模式，您也可以在例外語言中添加這個語言或網站。
- 修復 Tiktok 私信界面輸入框翻譯出錯問題
- 修復 Read Comic Online 漫畫無法翻譯問題
- 修復【進階設置 -> 翻譯段落所需的最少字符數】在部分情況下不生效的問題

## 1.8.4 (2024-08-30)

- DeepL 翻譯服務正式支持繁體中文作為目標語言（此前 DeepL 翻譯為繁體中文有額外的第三方簡體轉繁體過程）
- 優化富文本翻譯性能

## 1.8.3

- Google Meet 實時會議支持雙語字幕：現在，您可以在 Google Meet 會議中享受雙語字幕功能。只需打開會議鏈接，並在沉浸式翻譯面板中激活雙語字幕，然後刷新頁面即可體驗。
- 在面板的更多選項裡新增【反饋當前網頁的翻譯問題】選項，新增【快捷開啟/關閉懸浮球】選項
- 調整 YouTube 雙語字幕位置後，系統將自動記住新位置
- 優化插件的緩存邏輯，現在會自動清除超過 30 天的緩存數據
- 對段落中出現的代碼塊進行了優化，以更準確地還原原文
- 改進了高級設置中“不翻譯詞語”的處理

## 1.8.2

- 現在可以用右鍵翻譯輸入框裡的文本了：選中任何網頁上的輸入框文本，右鍵選擇翻譯，沉浸式翻譯會自動將選中的文本翻譯為輸入框的目標語言，方便快速將輸入框裡的母語翻譯為其他語言。
- 現在可以在沉浸式翻譯的懸浮球裡快速反饋網頁的翻譯問題了，翻譯網頁後，如果有問題，可以點擊懸浮球右側的【反饋】按鈕，填寫問題描述，我們會儘快處理。
- Epub 文件現在支持富文本翻譯了（即可以保留每個段落原文的格式，比如鏈接，粗體等）
- 支持 Microsoft Teams 網頁版影片會議的實時雙語字幕了（打開 Teams 會議鏈接，在沉浸式翻譯面板開啟雙語字幕後再次刷新即可）
- 優化英文版愛奇藝 (iq.com) 的雙語字幕
- 為 arxiv 上更多的論文提供排版優化的雙語翻譯
- 由於 Youtube 網站限制，Chrome 油猴腳本不再支持 Youtube 雙語字幕，請使用[插件版](https://immersivetranslate.com/)。

## 1.8.1

- 修復油猴腳本 SiliconCloud 翻譯問題
- Claude 翻譯新支持藏語，支持配置 Temperature 參數
- AI 專家詳情頁展示專家使用的 Prompt
- 快捷鍵設置中可以為任意翻譯服務指定獨立的快捷鍵翻譯了
- 優化 arxiv 論文翻譯的檢測

## 1.7.9

- 修復 Google、DeepL 等翻譯服務的富文本翻譯問題（如頁面直接顯示 `<button>` 等）
- 修復 YouTube 影片雙語快捷方式無法關閉的問題

## 1.7.8

- DeepL, 微軟翻譯, Google 翻譯，OpenAI，Claude， Gemini 等翻譯服務支援譯文保留原文格式（例如鏈接，粗體等）
- 選取文字後，右鍵選單會變成【翻譯該文字】，點選即可自動跳到沉浸式翻譯文字翻譯頁面
- 新增大模型免費翻譯服務：SiliconCloud ，所有使用者可用。
- 新增零一萬物大模型翻譯，可在零一萬物平台註冊後填寫 API Key 使用。
- 漫畫翻譯新增使用者回饋按鈕（漫畫翻譯後，點選懸浮球右側的【回饋】按鈕，可以回饋翻譯品質問題）

## 1.7.7

- 優化右鍵翻譯為「翻譯為xx目標語言」
- 支持第三方網站集成沉浸式 [JS SDK](https://immersivetranslate.com/docs/js-sdk/)
- 優化 hulu 字幕顯示
- 支持 ZOOM 網頁版會議字幕翻譯

## 1.7.6

- 支援自訂 AI 專家，入口在【設定】->【AI 專家】頁面最下方。
- TED 網站優化字幕加載
- 外掛語言支援葡萄牙語（巴西）
- 漫畫翻譯新增支援站點
- [Antbyw](https://www.antbyw.com)
- [Zerobywzz](https://www.zerobywzz.com)
- [動漫之家](https://www.idmzj.com)
- [Jmanga](https://jmanga.org)

## 1.7.5

- Youtube 字幕顯示允許複製
- 優化部分影片站點的字幕顯示
- 優化漫畫翻譯速度

## 1.7.2

- 修復火狐瀏覽器漫畫翻譯失敗

## 1.7.1

- 優化漫畫翻譯速度
- 漫畫翻譯新增支援站點
  - [ShonenJumpPlus](https://shonenjumpplus.com)
  - [Heros Web](https://viewer.heros-web.com/)
  - [Comic Days](https://comic-days.com/)
  - [ComicWalker](https://comic-walker.com/)
  - [Web Ace](https://web-ace.jp/)

## 1.6.6

- 漫畫翻譯新增支持站點
  - [Mangabuddy](https://mangabuddy.com/)
  - [Hitomi](https://hitomi.la)
  - [Yamibo](https://www.yamibo.com)
  - [Copymanga](https://www.copymanga.site/)
- Youtube 雙語字幕支持智能分句（Beta）（僅在【設置】-【影片字幕】中手動啟用沉浸式翻譯翻譯Youtube字幕，且原影片字幕為自動生成的英文字幕才生效）
- 翻譯服務新增騰訊【混元大模型】(https://immersivetranslate.com/docs/services/tencent-hunyuan/)

## 1.6.5

- 修復漫畫翻譯目標語言為拉丁語系的文字排版問題。
- 漫畫翻譯新增支持站點：
  - COMIC FUZCOMICFUZ(https://comic-fuz.com/)
  - MangaDexMangaDex(https://mangadex.org/)
  - 快看漫畫快看漫畫(https://www.kuaikanmanhua.com/)
- 修復自定義AI服務無法選中AI專家的問題。

## 1.6.4

- 當 AI 專家為【智能選擇】時，可為不同網站自訂不同的 AI 專家，可在【設置】->【AI專家】->【進入任何一個專家】設置
- 修復 Youtube 【僅譯文】模式下，字幕不顯示的問題
- 修復 Mubi 雙語字幕失效問題
- 兼容 Adobe Acrobat 插件打開的 PDF
- 所有用戶可以[在線貢獻](https://weblate.immersivetranslate.com/projects/immersive-translate/extension/)沉浸式翻譯介面的多語言翻譯

## 1.6.3

- 新功能：漫畫翻譯（Beta），在支援的漫畫網站裡，網頁快捷翻譯懸浮球下方會出現一個漫畫翻譯的按鈕，點擊即可開啟漫畫翻譯，該功能為 Pro 會員可用（每月 500 張，更多可購買加量包），當前支持以下網站：
  - [MANGA Plus by SHUEISHA](https://mangaplus.shueisha.co.jp)
  - [Zebrack by SHUEISHA](https://zebrack-comic.shueisha.co.jp)
  - [E-Hentai](https://e-hentai.org)
  - [Pixiv](https://www.pixiv.net/manga)
  - [seiga.nicovideo](https://seiga.nicovideo.jp/?cmnhd_ref=device=pc&site=seiga&pos=header_servicelink)
- 新特性：AI 翻譯支持[豆包大模型](https://www.volcengine.com/product/doubao)
- 新特性： 支持譯文在先，原文隨後的雙語對照模式，可在設定頁面->進階設定中啟用。
- 自定義 AI 模型列表支持 `-all` 語法，可以刪除預置的所有模型。
- 影片雙語字幕中，當目標語言是簡體中文，原文是繁體中文時，會自動將原文轉為簡體中文，反之亦然。
- 修復 iOS 18 下懸浮球快捷方式無法翻譯的問題。
- 修復自定義 Prompt 過多時不生效的問題。

## 1.6.1

- 支援百度千帆大模型平台、阿里百煉大模型平台、DeepSeek 大模型平台。
- 修復了在 popup 面板中修改目標語言等設置後，點擊翻譯懸浮球會被重置的問題。

## 1.5.8

- AI 專家支持【智能選擇】模式，系統會根據當前網站自動選擇最適合的 AI 專家（比如 The Verge，Hacker News 會自動選擇科技類，推特會自動選擇推特翻譯增強）。

## 1.5.7

- 支援新增 OpenAI 相容的自訂 AI 翻譯服務，入口位於【設定】->【翻譯服務】頁面最下方。
- 修復了 Safari 下 Domestika 影片平台雙語字幕不生效的問題。

## 1.5.6

- 大幅優化了大網頁，ePub 製作，字幕文件的翻譯性能
- 修復 Pro 多設備同步的 Bug

## 1.5.5

- 修復僅譯文模式下部分段落被丟失的問題。

## 1.5.4

- Pro 會員支持開箱即用的 Claude, Gemini 翻譯服務 (Beta)
- Youtube 雙語字幕支持字體、字重設置
- 修復長段落換行的單詞邊界問題 [#86](https://github.com/immersive-translate/immersive-translate/issues/86)
- 修復日韓語言識別
- 修復移動端 Reddit 頁面滑動不翻譯
- 修復部分頁面 DeepL 漏翻
- 修復 Pro 用戶配置多設備同步時間不同步
- 優化雲同步設置的覆蓋問題
- 優化 AI 翻譯服務的提示詞

## 1.5.2

- 修復通用專家提示詞變動覆蓋指定 AI 專家提示詞 [#1692](https://github.com/immersive-translate/immersive-translate/issues/1692)
- AI 自訂模型名稱支援進階語法, 使用 + 增加一個模型，使用 - 來隱藏一個模型，使用 模型名=展示名 來自訂模型的展示名，如: +gpt-3.5-turbo,-gpt-4,gpt-4-turbo=gpt-4-super
- 修復 Gemini 異常返回的錯誤
- 打印頁面時隱藏懸浮球
- 修復 YouTube 全屏時字體大小沒有等比例縮放 [#1681](https://github.com/immersive-translate/immersive-translate/issues/1681)

## 1.5.1

- 支援 AI 類翻譯服務設置【AI 專家】以指定翻譯策略，目前為 Beta 特性，可在[開發者設置](https://dash.immersivetranslate.com/#developer)啟用 Beta 後，刷新後可以看到【AI 專家】菜單。
- AI 類翻譯服務現在可以自定義模型列表了，比如【OpenAI】，系統只內置了最常用的幾個模型，點擊模型下拉列表，可以看到最後一項是【設置更多模型】，設置之後以後自動記住，方便用戶測試不同的自定義模型。
- 優化部分情況下譯文排版高低不一致的情況。
- Youtube 字幕樣式添加重置按鈕，可以快速恢復到預設樣式。
- 修復 Youtube 中文字幕無法下載的問題。
- 優化繁體中文界面文案。

## 1.4.12

- 修正在 reddit 頁面開啟訊息對話框未翻譯的問題
- 面板【更多】入口新增暫時開啟譯文編輯功能
- 修正 YouTube Shorts 沒有字幕的影片總是會顯示之前影片的字幕的問題 [#1655](https://github.com/immersive-translate/immersive-translate/issues/1655)
- 修正 YouTube 雙語字幕全螢幕時無法上下調節字幕的位置的問題 [#1654](https://github.com/immersive-translate/immersive-translate/issues/1654)
- 支援 [VK Video](https://vk.com/video) 雙語字幕
- 支援 YouTube 影片雙語字幕的獨立開啟設定功能（新用戶預設開啟）
- 優化翻譯本地雙語字幕錯誤提示

## 1.4.11

- 兼容 Bing Copilot 頁面的輸入框翻譯
- Youtube 字幕樣式控制支持邊緣樣式
- 支持在設置->翻譯服務頁面選擇默認翻譯服務
- 修復 OpenAI SystemPrompt 佔位符替換
- 修復自定義用戶規則合併問題
- 修復 Netflix 部分影片字幕顯示異常 [#1630](https://github.com/immersive-translate/immersive-translate/issues/1630)
- 修復頻繁通過色盤修改譯文顏色失效 [#1628](https://github.com/immersive-translate/immersive-translate/issues/1628)

## 1.4.9

- 將翻譯服務單獨作為一個 Tab，現在你可以整體預覽所有的翻譯服務，並且可以自定義顯示哪些翻譯服務，默認情況下只展示較少的翻譯服務，你可在[更多服務](https://dash.immersivetranslate.com/#services) 中自定義要顯示的翻譯服務。
- 設置頁支持 [YouTube 字幕樣式](https://dash.immersivetranslate.com/#subtitle) 調節
- 優化了當用戶在 Youtube 網站上設置了字幕語言為中文時，沉浸式翻譯雙語字幕不顯示的問題。
- 支持了新的快捷鍵，臨時翻譯 Claude，可在[快捷鍵設置頁](https://dash.immersivetranslate.com/#shortcuts)中設置

## 1.4.8

- 優化 pdf-pro 大檔案翻譯性能
- 優化長內容頁面翻譯性能
- 實現頁面文檔跳轉時的國際化支持（i18n）
- YouTube 新增功能，可臨時啟用雙語字幕
- YouTube 支援雙語字幕的下載（限會員）
- 移動端新增手勢操作，透過[快捷鍵設置](https://dash.immersivetranslate.com/#shortcuts)實現輸入增強
- 支援 Google Docs 雙語翻譯

## 1.4.7

- 修復 OpenAI 自定義切換 Pro 在測試按鈕下點擊翻譯失敗問題
- 修復 YouTube 字幕快捷圖標未顯示問題
- 優化擴展語言識別

## 1.4.6

- 修復用戶自定義提示詞無效問題
- Youtube 字幕字號大小新增50%,150%選項

## 1.4.5

- 修復 Youtube 字幕樣式變動未保存問題
- 修復 iOS Safari 全屏字幕消失問題
- 進一步優化 Youtube 字幕翻譯速度
- 面板的更多選項支持[文本翻譯入口](https://app.immersivetranslate.com/text/)

## 1.4.2

- 支持 Claude 翻譯服務
- 優化 OpenAI 多段提示詞，支持 YAML 格式，提高了配置的靈活性和易用性
- 大幅優化 Youtube 字幕翻譯速度，並新增支持中英順序切換、自定義字體顏色及字號大小等功能
- 影片字幕平台支持 [University of Southampton](https://southampton.cloud.panopto.eu)
- Udemy 雙語字幕兼容移動端顯示
- 默認隱藏 Gemini 翻譯服務，可在開發者設置中啟用 beta 顯示該翻譯服務

## 1.3.4

- 支援 Yandex 免費翻譯服務
- 優化 Gemini 提示詞
- 影片字幕支持設置雙語/僅譯文顯示
- 支援 OpenAI 翻譯結果中英文之間空格
- 面板切換僅譯文按鈕修改為僅在當前頁面生效

## 1.3.3

- 優化了Twitter CC影片字幕的翻譯顯示問題。
- DeepL 服務新增了對阿拉伯語的支援。
- 彩雲小譯服務現已支援韓語、西班牙語、法語和俄語。
- OpenAI 服務新增了對東北話的支援。
- 面板的自動檢測支援顯示原文語言。
- 對移動端面板的快捷鍵描述進行了調整。

## 1.3.2

- 修復移動端無法關閉控制面板## 1.3.1

- 影片字幕平台支援 [DeepLearning.ai](https://learn.deeplearning.ai)
- 支援網頁翻譯和影片字幕翻譯阿拉伯語、希伯來語等語言的 rtl 顯示問題
- 修復 Gemini 翻譯希伯來語
- 修復 YouTube 部分繁體中文字幕無法正常顯示問題
- 修復 Twitter 字幕在 Safari 上的顯示問題
- 修復立即翻譯到頁面底部快捷鍵

## 1.2.4

- 修復 ePub 製作占位符未正常替換問題
- 影片字幕翻譯支援 [Unreal Sensei](https://www.unrealsenseiacademy.com/)

## 1.2.3

- 優化翻譯服務請求頻率控制
- 近期微軟翻譯服務國內請求不穩定，當出錯時，自動探測當前可用的翻譯服務,用戶可以快速切換。
- 優化網絡錯誤文案提示
- 修復配置文本顏色不支援 RGBA 預覽[#1435](https://github.com/immersive-translate/immersive-translate/issues/1435)
- 修復 Safari 插件版本升級總是彈出安裝成功頁面
- 微軟添加支援越南語
- 修復 edx 站點翻譯字幕不顯示問題## 1.2.2

- 影片字幕翻譯支持 [pluto](https://pluto.tv/)、[STARZ](https://www.starz.com/)、[Paramount Plus](https://www.paramountplus.com/)、[Rotten Tomatoes](https://www.rottentomatoes.com/)、[Dailymotion](https://www.dailymotion.com/)、[FMovies](https://fmoviesz.to/)、[AniWatch](https://aniwatch.to/)、[iQIYI](https://www.iq.com/)、[Youku](https://www.youku.tv/)、[movie-web](https://movie-web.app/)。同時支持 Twitter 部分 CC 字幕影片的翻譯
- 優化錯誤彈窗，網絡問題錯誤彈窗自動檢測有效免費翻譯服務
- 修復沉浸式 iOS APP 支持 YouTube 全屏播放
- 修復 Perplexity.ai 段落翻譯問題 [#707](https://github.com/immersive-translate/immersive-translate/issues/707)

## 1.2.1

- 影片字幕翻譯支持 [Kanopy](https://www.kanopy.com/)、[RachelsEnglishAcademy](https://www.rachelsenglishacademy.com/)、[Hulu](https://www.hulu.com/)、[Three.js Journey](https://threejs-journey.com/)
- 修復部分 Pro 用戶在 Chrome 瀏覽器中無法修改設置的問題
- 支持 YouTube 在 iOS 全屏模式下顯示雙語字幕## 1.2.0

- 影片字幕翻譯支持 [LinkedIn](https://www.linkedin.com/)、[Viu](https://www.viu.com/) 平台
- 增加更多平台的影片字幕快捷入口
- 支持指定網站/語言設置僅譯文顯示
- 修復部分情況下 Safari 打開設置頁一直顯示 loading
- 支持 input 標籤節點翻譯
- 優化錯誤彈窗 UI

## 1.1.9

- 字幕翻譯支持 YouTube 直播，[Mubi](https://mubi.com/) 平台
- 優化：設置頁面，URL 列表交互 UI（避免歧義，默認不展示複選框）
- 僅譯文模式翻譯時支持設置譯文字體
- 針對 Netflix, Ted，Bloomberg, Udemy, Coursera 添加影片字幕快捷啟用入口
- 修復：Safari 部分譯文樣式（波浪線等）不生效的問題。
- 修復：頁面翻譯時，鼠標懸停沒有重翻的問題## 1.1.8

- 子翻譯服務新增選項跟隨主翻譯服務
- 雙語字幕支持 [Amazon Prime Video](https://www.primevideo.com)
- 進一步優化 Sci-Hub 的內嵌 PDF 翻譯功能
- 修復在線 PDF 打開異常問題
- 修復 Netflix 雙語字幕連續播放問題

## 1.1.7

- 現在你可以在設置頁面-> 【基本設置】 -> 【譯文樣式】為譯文配置指定的字體
- 移動端懸浮球面板新增【翻譯指定段落】的快捷配置
- 優化鼠標懸停 Ctrl 的檢測靈敏度，避免 `Ctrl+C` 也被認為是 `Ctrl`
- 支持裡一個新的快捷鍵設置，可以快速切換影片字幕是否使用自帶的機器翻譯字幕
- 在 Sci-Hub 網站裡，點擊懸浮球即可翻譯網頁中內嵌的PDF## 1.1.6

- **移動端支援翻譯指定的段落：** 移動端現在支援對指定段落進行翻譯，並新增了多種快捷操作，包括左滑、右滑、雙擊、三擊以及多指同時觸控的觸發手勢，預設未啟用，需要用戶主動在設置頁面【鼠標懸停】裡選擇觸發的手勢
- **Gemini預設版本更新：** 現在預設為 `v1beta` 版本。
- **修復文言文翻譯：** 修復了微軟和OpenAI的文言文翻譯功能。
- **日語翻譯優化：** 對OpenAI的日語翻譯進行了進一步優化，以提高準確性和流暢性。
- **沉浸式翻譯體驗：** 為了更好地適應用戶習慣，我們將YouTube平台全屏模式下的雙語字幕快捷方式移至左側。

## 1.1.5

- 修復 Windows 下黑暗模式下拉框沒有顏色的問題。
- 修復 Windows 更多沒有左對齊的問題。## 1.1.4

- **Popup 面板 UI 升級：** 新版設計旨在提升易用性和可理解性。本次更新包括：

  - **一級菜單新增功能：**
    - **雙語/僅譯文模式切換：** 現在可以直接在一級菜單中切換“雙語翻譯模式”和“僅譯文翻譯模式”，位置在翻譯按鈕的左側。
    - **文檔翻譯入口：** “PDF/ePub/字幕文件”的翻譯入口已移至一級菜單，方便快速訪問。
    - **影片翻譯設置：** “影片翻譯”的設置入口也被置於一級菜單，以便快速調整。
    - **新增使用說明文檔入口：** 提供詳細的操作指南和幫助文檔。

- **文檔翻譯入口整合：** 現在，您可以通過一個統一的上傳入口來翻譯 PDF、ePub 和字幕文件等。只需點擊 Popup 面板裡的【PDF/ePub】按鈕，無需再選擇【更多】。

- **新增對5個影片網站的支持：**

  - 對 Youtube Music 的播客字幕提供支持。
  - 新增支持 iview.abc.net.au 網站。
  - 新增支持 www.nma.art 網站。
  - 新增支持 creativecloud.adobe.com 網站。
  - 新增支持 www.masterclass.com 網站。## 1.1.3

- 修復了移動版插件在打開PDF頁面時出現的顯示異常問題。
- 對GPT對話翻譯效果進行了優化。
- 針對百度翻譯支持了領域翻譯。
- 設置頁面新增了僅譯文翻譯模式。
- 在快捷鍵切換翻譯模式時增加了提醒功能。
- 修復了輸入框翻譯含網址內容時僅部分翻譯的問題。

## 1.1.2

- 修復：當頁面尚未翻譯時，切換翻譯服務不生效的問題。
- 優化：在Epub和PDF翻譯過程中，如果部分內容翻譯失敗，現在可以在面板上切換到另一種翻譯服務而不會重啟整個翻譯過程（之前的邏輯是立即使用新的翻譯服務重新翻譯整本書）。這意味著在翻譯進行到一半時，您可以切換到不同的翻譯服務，並點擊【重試所有錯誤的段落】，之後系統將使用新的翻譯服務繼續翻譯。
- 優化：調整翻譯錯誤提示的字體大小，以提升可讀性。## 1.1.1

- 修復 Youtube 雙語字幕快捷方式英文文案過長的問題。

## 1.1.0### 新增功能

- **快捷鍵設置**：新增了一級菜單【快捷鍵】以及以下可自定義的快捷鍵功能：

  - 指定組合鍵以翻譯當前輸入框內容，補充之前的快速連擊3次空格鍵。
  - 指定組合鍵以在頁面上臨時開啟“鼠標懸停直接翻譯”，再次按下則取消。
  - 新增6個翻譯服務（如DeepL, OpenAI, Google, 微軟, Gemini, 騰訊交互翻譯）的專用快捷鍵，方便臨時切換翻譯服務。

- **插件設置頁面UI更新**：

  - 【進階設置】新增選項，支持用戶指定某些單詞（如“LLM”）不被翻譯。
  - 【進階設置】新增選項，支持配置翻譯段落所需的最少字符數，默認是 4 個字符，可以設置多一點（比如 20），這樣，只有較長的段落才會被翻譯。
  - 新增新手教程，涵蓋懸浮球設置、影片字幕設置及鼠標懸停設置。

- **YouTube雙語字幕**：在YouTube影片播放窗口新增快捷入口，用於開啟或隱藏雙語字幕（可關閉該功能）

- **Deepl語言支持**：新增對葡萄牙語（巴西）的支持。

- **新用戶引導**：新用戶首次打開非目標語言頁面時，展示懸浮球幫助指引氣泡。### 優化與修復

- **UI優化**：重新設計了頁面翻譯錯誤的提示UI，使其更易於理解。當錯誤較多時，會主動彈窗提示用戶。

- **問題修復**：

  - 解決了頁面失去焦點時鼠標懸停翻譯失效的問題。
  - 修復輸入框增強功能中少於3個字符不被翻譯的問題。
  - 修復Epub雙語製作時部分目錄未翻譯的問題。

- **功能移除**：刪除了雙語信息增強功能（在Google搜索頁面同時展示英語的搜索結果）。

### 其他更新

- **openAI配置更新**：現在支持每秒配置次數的小數設置，比如 0.5，表示 2秒請求1次

## 0.12.14

- 修復：首次安裝後，部分機器的默認目標語言識別問題
- 優化： 網頁標題默認順序改為【中文 - 英文】## 0.12.13

- 修復：部分情況下 OpenAI 長段落翻譯拼接問題。[#1276](https://github.com/immersive-translate/immersive-translate/issues/1276)
- 優化：當使用鼠標懸停的時候，頁面失去焦點時，再次觸發無效的問題。
- 修復：OpenAI 修改 prompt/model 之後，緩存依然還在的問題。

## 0.12.12

- 更新：優化彈窗面板，移除當前網站的部分選項。
- 優化：改進人工字幕合併流程。
- 優化：根據瀏覽器語言自動設置目標語言。
- 新增：為 [ArtStation](https://www.artstation.com/learning) 學習平台和 [ZDF](https://www.zdf.de/) 增加雙語字幕支持。
- 修復：解決 jstor 列表頁標題不翻譯的問題 [#1268](https://github.com/immersive-translate/immersive-translate/issues/1268)。
- 修復：修復 Hacknews 上僅譯文部分內容消失的問題 [#1264](https://github.com/immersive-translate/immersive-translate/issues/1264)。## 0.12.11

- 雙語字幕增加支持 [HBO Max](https://play.max.com/)、[BBC](https://www.bbc.com/)、[Disney+](https://www.disneyplus.com)、[ARD Mediathek](https://www.ardmediathek.de/)、[ITV](https://www.itv.com/)、[Domestika](https://www.domestika.org) 平台

## 0.12.10

- 修復了在油猴腳本下的 Gemini 域名授權問題。
- 支持了 Twitter Space 的實時字幕翻譯。-針對舊版本的油猴腳本，現在在設置頁面中添加了更新提示。

## 0.12.9

- 新增支持 Gemini 翻譯
- 修復了部分情況下，網頁滾動到中間位置時翻譯沒有及時響應的問題
- 修復了部分影片網站上字幕切換導致譯文重複顯示的 bug
- 修復了鼠標懸停在某些情況下沒有按住快捷鍵時持續翻譯的問題
- 在 macOS 上，優化了面板快捷鍵的顯示名稱## 0.12.8

- 修復在「當前網站設置為永不翻譯」時原影片字幕不顯示
- 修復與部分插件衝突導致頁面無限重翻
- 修復開啟長段落換行後部分段落不翻譯
- 修復[臨時開啟網頁翻譯時長，點擊面板【總是翻譯該網站】無法取消總是翻譯 #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)

## 0.12.7

- 雙語字幕增加支持 [TED](https://www.ted.com)、
  [Frontend Masters](https://frontendmasters.com/) 、
  [edx](https://www.edx.org/)、
  [CodeWithChris](https://learn.codewithchris.com/enrollments)、
  [Skillshare](https://www.skillshare.com/) 平台
- 影片全屏的時候，現在默認會隱藏懸浮球。
- 修復 firefox 頁面懸浮球操作面板點擊抖動問題。
- 支持 pubmed.ncbi.nlm.nih.gov 站點下和 scholarscope 插件協作
- 修復 reddit 輸入框翻譯頁面抖動問題## 0.12.6

- 修復 YouTube/Web of Science 等網站在切換 tab 時翻譯不靈敏的問題。
- 移動端懸浮球現在支持長按操作了，短按時翻譯，長按則打開面板。
- 翻譯雙語電子書現在會把目錄也翻譯了。
- 搜索增強（Google搜索的部分頁面展示雙語搜索結果）特性現在默認不啟用，下個版本將移除該功能。

## 0.12.5

- 修復 Epub 製作電子書從面板點擊翻譯無效的問題## 0.12.4

- 在面板上開啟雙語字幕後，會首先自動刷新一下頁面（為了能更準確的顯示雙語字幕），部分網站依然需要用戶手動點擊網站上的“CC”按鈕以開啟字幕。
- 優化油猴、Safari 語言檢測
- 為 [Arxiv](https://arxiv.org/abs/1910.06709)
  論文網站所有的論文提供雙語版本的快捷入口。
- [懸浮球支持配置成固定在左邊 #1168](https://github.com/immersive-translate/immersive-translate/issues/1168)
- [修復學習模式顯示問題 #1180](https://github.com/immersive-translate/immersive-translate/issues/1180)
- [臨時開啟網頁翻譯時長無法取消總是翻譯 #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)
- 優化 PDF 文件初始化問題

## 0.12.3

- 修復【永久禁用影片字幕】功能不生效的問題
  [#1175](https://github.com/immersive-translate/immersive-translate/issues/1175)## 0.12.2

- 為更多影片平台提供了雙語字幕支持，目前已經支持這些平台：
  [Youtube](https://www.youtube.com/)、[Netflix](https://www.netflix.com)、
  [Udemy](https://www.udemy.com/)、
  [Khanacademy](https://www.khanacademy.org/)、
  [Coursera](https://www.coursera.org/)、 [Vimeo](https://vimeo.com/)、
  [Nebula](https://nebula.tv)、[Bloomberg](https://www.bloomberg.com)、[Bilibili](https://www.bilibili.com/)
  等影片網站，（注意：由於技術限制，部分網站在首次開啟雙語字幕後需要重新刷新頁面，或者需等待翻譯完成以顯示雙語字幕）
- 大幅優化插件壓縮包大小，比原來減少了一半，下載和更新都更快了。
- 修復擴展 PDF 下載問題
- 在 [Arxiv](https://arxiv.org/abs/1910.06709) 論文網站右側添加了一個快捷翻譯
  PDF 的入口，會跳轉到一個乾淨的 HTML
  頁面（只有部分論文支持，因為需要原作者提交源碼，所以大概會有 50%
  的論文會顯示這個入口）
- 無 .pdf 後綴的在線 PDF 網頁，現在可以通過點擊頁面上的懸浮球直接跳轉到 PDF
  翻譯頁面
- 修復 Safari 下部分輸入框增強問題
- 優化 油猴和 Safari 的語言檢測## 0.11.6

- 新增了11種插件和官網的界面語言，現在支持的界面語言達到14種，包括中文簡體，中文繁體，英語，日語，韓語，俄語，西班牙語，葡萄牙語，印度語，意大利語，德語，法語，阿拉伯語，波斯語。
- 將上個版本新增的雙語分享（清爽模式）修改為雙語頁面快照分享，這樣分享的內容更加原汁原味，以及適配性更廣。
- 修復推特輸入框末尾表情包無法翻譯的情況
- 修復部分場景下翻譯了第三方插件內容的情況
- 修復在線 pdf 懸浮球點擊無反應## 0.11.5

- 你現在可以為沉浸式翻譯翻譯後的雙語頁面生成一個公開的鏈接了。
  - [點擊](/docs/share/)沉浸式翻譯分享圖標即可一鍵生成
- 解決了部分平台無法識別是否支持鼠標的問題
  - 有一些同時支持觸摸屏和鼠標的桌面瀏覽器，沉浸式翻譯在技術上無法檢測這類平台是否支持鼠標，所以我們在【鼠標懸停】設置裡增加了【強制啟用鼠標支持】的選項

## 0.11.2-0.11.4

- 優化體驗，修復一些 Bug

## 0.11.1

- OpenAI 翻譯的模型默認是: GPT3.5-turbo-1106 了
- 優化了OpenAI 的中文Prompt，現在更不容易出現幻覺了
- 減少了OpenAI 的 prompt 長度，從之前的 90 減少到 40，更省流量了。

## 0.11.0

- 修復頁面懸浮球點擊抖動的問題
- 修復 Azure 翻譯的問題

## 0.10.9

- 修復一些小問題## 0.10.8

- 支援設置懸浮球快捷翻譯按鈕（PC/移動端都支援）
- 優化油猴語言判斷
- 修復 txt 檔案翻譯

## 0.10.7

- 鼠標懸停支援再次按下Ctrl顯示原文
- 鼠標懸停忽略永不翻譯語言
- Youtube 雙語字幕優化

## 0.10.6

- Youtube 字幕支援僅譯文展示
- 新增油猴低版本更新提示
- 修復本地 txt 檔案無法翻譯問題

## 0.10.5

- 修復 Youtube 偶爾回到首頁問題

## 0.10.4

- 修復 Youtube 字幕與 Dual 字幕插件衝突的問題（當檢測到 Youtube Dual
  插件存在的時候，則不啟用沉浸式翻譯的Youtube 字幕翻譯，避免衝突）
- 新增【永久禁用影片字幕功能】，如果還有別的衝突的問題，而你又不想用沉浸式翻譯來開啟雙語字幕功能的話。
- 優化字幕斷句問題

## 0.10.3

- 修復 自定義 DeppL Auth Key 翻譯問題## 0.10.3

- 完美支持 Youtube 影片雙語字幕🎉
- 對於文章頁面，現在會優先翻譯正文部分，然後再翻譯其他側邊欄內容
- 優化 DeepL 翻譯上下文聯繫
- 優化 OpenAI 翻譯字幕檔案聯繫上下文

## 0.10.1

- 提高正文翻譯優先級，優化翻譯體驗
- 修復 ins 點擊更多文本未翻譯問題

## 0.9.8

- 優化體驗，修復一些 bug

## 0.9.7

- 修復 readwise 高亮的時候自動翻譯

## 0.9.6

- 修復清除緩存的時候，退出了用戶的登錄狀態。

## 0.9.5

- 在線電子書 bug 修復

## 0.9.4

- 優化輸入增強檢測，減少誤觸
- 電子書及字幕翻譯在線化## 0.9.3

- 輸入框翻譯：首次使用的時候展示一個彈窗提醒，用戶可以選擇本次禁用或者永久禁用，避免誤觸。
- PDF 僅譯文導出速度優化，如果選擇僅譯文導出，目前是直接可以調用系統的 PDF
  預覽去導出，速度更快。
- Deeplx 支持多個 URL, 用,分割即可。

## 0.9.2

- PDF 翻譯工具遷移到在線版： https://app.immersivetranslate.com/pdf/ ,
  這樣油猴，Safari 都可以使用 PDF 翻譯，並且出現問題也更好迭代，不需要發版解決。
- POPUP UI 優化，面板更漂亮了！

## 0.9.1

- 修復 Epub 電子書製作的文件名問題

## 0.8.8

- pdf 支持行間距和字間距調節重新識別段落
- epub 在線閱讀移動端自動滾動問題修復

## 0.8.7

- pdf 支持僅譯文下載
- 修復 safari Google 登錄問題

## 0.8.2 - 0.8.6

- 允許設置輸入增強連擊觸發的間隔時間
- 修復一些 Bug## 0.8.1

- 語言檢測優化
- Beta 特性：自定義 API （在開發者設置中開啟 Beta 可體驗）
- 支援阿里雲翻譯
- 修復了一些 Bug

## 0.8.0

- 支援用戶系統
- 支援[開通 Pro 會員](/pricing)，開通會員後，用戶可以暢享 Deepl 和 OpenAI
  翻譯和雲同步設置
- 鼠標懸停翻譯服務可以單獨設置
- 輸入框翻譯服務可以單獨設置
- PDF 翻譯優化
- 修復了一些 Bug

## 0.7.16

- PDF 翻譯新增快捷控制譯文樣式的選項（PDF
  文件千奇百怪，開啟這些選項可能對某些格式較亂的 PDF 文件有用）
- iOS 和 macOS 版本重新上架蘋果商店國區

## 0.7.15

- 接蘋果通知，在 iOS 和 macOS 版本暫時下架 OpenAI 翻譯，嘗試重新上架國區。

## 0.7.11- 0.7.14

- 修復：Gmail 翻譯全部區域問題
- 由於 Safari 對插件下載的限制（Bug），暫時禁用 Safari 的 PDF 導出功能
- 修復一些其他問題## 0.7.10

- 彈出式瀏覽器圖標面板 UI 升級，更有設計感一點～
- 修復部分日語段落不翻譯的問題

## 0.7.9

- PDF 終於支持導出雙語版了！你可以點擊【保存】按鈕導出翻譯後的雙語 PDF 文件
- 自定義規則支持與默認內置規則合併了，如：`{"id":"youtube","selectors.add":["#test"]}`
  表示在原有的 selectors 基礎上新增一個 `#test`, `selectors`
  表示覆蓋默認的，`selectors.remove` 表示刪除默認的 selectors 中的某一項。
- 更新 Safari 圖標, 更大一點。
- 其他 Bug 修復

## 0.7.8

- Bug 修復

## 0.7.7

- 適配 Safari 的系統風格，Safari 的擴展圖標改為透明輪廓
- 增加瀏覽器圖標狀態變化，當某個網頁已翻譯時，瀏覽器圖標右下角自動增加一個 ✅
- 為新用戶自動開啟常用英文網站翻譯
- 修復 https://claude.ai/ 的翻譯問題## 0.7.6

- 輸入增強支持翻譯結果 ctrl+z 撤銷
- 支持飛書文檔閱讀模式下翻譯
- 適配 https://pi.ai/talk

## 0.7.5

- 修復油猴圖標不顯示的問題
- 修復若干問題

## 0.7.4

- 修復若干問題
- 設置頁面支持全選 url 進行批量刪除
- 支持啟用/關閉 Youtube 字幕翻譯，防止與其他相關插件衝突。
- 有道翻譯支持設置領域和術語 id

## 0.7.2

- 輸入框增強：允許省略前綴//，直接 3
  個空格即可觸發翻譯整個輸入框的內容，也可以在設置頁面關閉此選項。## 0.7.1

- 支援搜尋增強了，啟用後，在Google/Google新聞用中文搜尋時，右邊欄自動顯示對應英文關鍵詞的搜尋結果，預設為啟用狀態。

  - 原因：我們發現，在Google搜尋裡，中文關鍵詞和英文關鍵詞的搜尋結果會有非常大的不同，在啟用沉浸式翻譯搜尋增強功能後，我們會自動用英文為你搜尋同樣的關鍵詞並展示在右側。如果你不需要該功能的話，可以選擇禁用它。
  - Safari 瀏覽器由於 API 限制，暫不支援。## 0.6.20

- 修改預設設置：由於大量用戶反饋安裝後不會使用，他們對翻譯工具的預期是裝了之後就能自動翻譯英語網頁，所以從該版本起，對於中文用戶，開啟了預設翻譯英文頁面的選項（如果用戶之前有過設置總是翻譯的語言，那麼會尊重用戶的設置，該變更只修改了擴展的初始設置），需要取消的話，可以很方便的在
  [Popup 面板或者設置頁面取消](/docs/faq/#%E5%A6%82%E4%BD%95%E9%97%AD%E9%96%89%E8%87%AA%E5%8B%95%E7%BF%BB%E8%AD%AF)

## 0.6.19

- 修復 PDF Bug
- 修復 web of science Bug
- 適配 feeder.com
- 修復 epub 不翻譯部分書籍

## 0.6.18

- 修復 Safari Popup 彈窗寬度溢出的問題
- 構建流程優化

## 0.6.17

- 優化錯誤提示
- 優化目標語言選擇，現在只會展示對應翻譯服務支持的語言了
- PDF 譯文優化
- 適配 Good Reads 網站，亞馬遜和南華早報網站## 0.6.16

- 增加 PDF 無權限頁面顯示
- 修復 PDF 正文列表段落的顯示
- 調大 PDF 小字體的在 chrome 和 safari 上的縮放比例

## 0.6.15

- 修復打開 PDF 文件的時候，擴展面板上提示沒有權限的問題。
- 修復當網站被設為永不翻譯的時候，輸入框增強功能無法啟用的問題。

## 0.6.14

- PDF 翻譯優化，譯文區域現在可以編輯/拖動/刪除了
  - 左上角拖動，右上角刪除，右下角改變大小
- Windows 下拉框左對齊
- 支持繁體中文和簡體中文互翻

## 0.6.13

- 修復鼠標懸停重複翻譯的問題
- PDF 譯文支持拖動改變大小以及編輯譯文的內容

## 0.6.12

- 修復部分瀏覽器 Epub 翻譯圖片變小的問題
- 優化輸入框翻譯，現在在 Bard 中流暢的使用了## 0.6.10

- OpenAI 預設模型改為 0613 版本
- 修復部分輸入框樣式
- 更智能的判斷是否為導航區域，如果是的話，則不進行翻譯
- 修復可能的 XSS 注入攻擊

## 0.6.8

- 擴展面板現在可以對不支持的頁面進行提示（比如沒有權限的頁面和非 HTML 頁面）
- 輸入框增強支持翻譯中展示 Loading 狀態
- 更新默認的翻譯中 loading 顏色
- 當輸入框配置為無前綴時，支持 `ja 你好`翻譯為日語，`英文 你好`翻譯為英文

## 0.6.6

- 修復： 部分區域不翻譯的問題（quora）

## 0.6.5

- Google Bard 優化
- 輸入框翻譯支持無需前綴直接翻譯整個文本框
- 優化 OpenAI 翻譯無腦加句號的問題，（如果在原文裡檢測不到句號，如果 openai
  返回了句號，那就去掉）
- safari 字幕文件不識別的問題

## 0.6.3

輸入框翻譯的默認語言可以省略空格了，也就是 //你好世界 也可以被翻譯了。## 0.6.2

最令人興奮的輸入框增強功能來了：

- 在任何網頁中的輸入框輸入： // 你好世界，然後三連擊空格鍵，即可將該段翻譯為英文
- 你也可以指定翻譯為某語言： /ja
  你好世界，然後三連擊空格鍵，即可將該段翻譯為日文

[點此查看 30 秒快速介紹](/docs/input/)

## 0.6.0

- 6
  月的第一個版本，從之前的個人子域名<https://immersive-translate.owenyoung.com>遷移到了新的域名
  <https://immersivetranslate.com/>
- 功能方面基本沒有變化(下一個版本將會有新特性！)

## 0.5.17

- 修復： 雙語電子書導出後沒有圖片的問題

## 0.5.16

- 修復： openai 翻譯繁體中文問題

## 0.5.15

- 優化： 最短觸發翻譯的段落字數修改為最小 4
  個字符，以減少困惑，同時利用其他特徵避免翻譯網站的導航和尾部區域。
- 修復： Github details 展開之後無法翻譯的問題。## 0.5.14

- 修復： 部分網頁的圖片複製後變大的問題
- 修復： medium 評論區不翻譯的問題
- 修復： 部分網頁的圖片被錯誤的複製問題

## 0.5.12

- 特性： 分割線譯文樣式增加單行譯文的垂直分割線
- 修復： 極少數情況下段落分割的問題。
- 為 iOS 新用戶提供了一個很好的初次設置引導頁面。

## 0.5.11

- 字幕翻譯支持導出僅譯文
- 修復： 鼠標懸停部分元素不識別
- 修復：推特部分換行不識別問題
- 修復：電子書製作樣式不生效問題

## 0.5.10

- 修復： 推特換行無法識別的問題
- 修復： Reddit 詳情頁返回部分段落無法翻譯的問題
- 修復： 部分 Code 標籤未正確識別的問題

## 0.5.9

- 修復： 部分情況下段落分段問題
- 修復： 油猴腳本切換僅顯示譯文
- 修復： 電子書在線閱讀的樣式不生效問題## 0.5.8

- 修復： 臨時設置網站翻譯時長不生效問題。## 0.5.7

- 超多更新！
- 僅顯示譯文功能來了！ 點擊【更多】->【切換為僅顯示譯文】
  - 支持自定義快捷鍵，在介面設置-> 快捷鍵設置中設置
- 優化 OpenAI 請求頻率限制問題
- ChatGPT 默認改為 mobile 模型，更快！
- 網頁核心解析重構，這意味著：
  - 大型網頁秒翻譯
    - 比如： <https://pve.proxmox.com/pve-docs/pve-admin-guide.html>, 之前需要
      30 秒，現在秒翻
  - 複雜網頁佔用內存超低
    - 比如：
      <https://www.wsj.com/articles/global-stocks-markets-dow-news-05-05-2023-cb142c76?mod=hp_lead_pos1>
  - 對更多網站的適配
- 支持了所有 ShadowRoot 的網站翻譯
  - 比如： <https://bugs.chromium.org/p/chromium/issues/detail?id=418987>
  - 比如：
    <https://news.yahoo.com/gma/virginia-mom-facing-charges-6-190600893.html>
    的評論區
- 修復之前 Next.js 等具有水合作用的網站翻譯後白屏的問題
  - 比如： <https://webpack.js.org/>
- 修復了修改鼠標懸停的快捷鍵需要刷新頁面才生效的問題
- 修復了 TXT 文件 換行識別的問題。

- 大量更新！
- 「僅顯示譯文」功能來了！點擊「更多」->「切換為僅顯示譯文」。
  - 支援自訂快捷鍵，在介面設定->快捷鍵設定中設定
- 優化了 OpenAI 請求率限制問題
- 網頁核心解析已重構，這意味著：
  - 大型網站即時翻譯
  - 複雜網頁的記憶體使用極低
  - 更好地兼容更多網站
- 現在支援所有帶有 ShadowRoot 的網站翻譯
- 修正了翻譯具有水合作用的網站後出現白屏的問題，如 Next.js
- 修正了更改滑鼠懸停快捷鍵後需要刷新頁面才能生效的問題
- 修正了 TXT 文件換行識別的問題。## 0.5.6

- 修復：macOS 新標籤彈出問題。
- 功能：為新用戶新增引導頁面。

## 0.5.5

- 修復：鼠標懸停區域問題。

## 0.5.4

- 修復：Spa 頁面重複

## 0.5.3

- 修復：鼠標懸停熱鍵監聽器。
- 修復：PDF 文件翻譯
- 功能：新增客戶端引導頁面

## 0.5.2

- 修復：用戶腳本鼠標懸停快捷方式設置

## 0.5.1

- 修復：OpenAI API 不工作。

## 0.5.0

- 功能：當鼠標懸停時翻譯當前段落。
- 功能：重構 PDF 翻譯，現在您可以使用沉浸式翻譯翻譯大多數 PDF
- 修復：禁用上下文菜單不工作
  [#428](https://github.com/immersive-translate/immersive-translate/issues/428)
- 修復：避免內容安全政策對 [Mastondon](https://mastodon.social/) 的影響

## 0.4.11

- 修復：用戶腳本權限（僅限用戶腳本）。

## 0.4.8

- 功能：將 Bing 翻譯更改為 Microsoft 翻譯，以獲得更穩定的質量。
- 修復：純 TXT 網頁，如
  [此](https://edoras.sdsu.edu/~vinge/misc/singularity.html)
- 性能：排除網站中的一些子廣告頁面，性能有所提升

## 0.4.7

- 修復：Firefox 用戶腳本彈出缺失。

## 0.4.6

- 功能：允許第三方發送文檔事件以調用 `toggleTranslatePage`
- 功能：iOS 應用新增啟用擴展按鈕和社區鏈接
- UI：OpenAI 設置字段模型使用選擇而不是文本輸入框。## 0.4.5

- 修復：iOS 15.0 Safari 擴展問題。
- 修復：macOS Safari 擴展快捷鍵
- 修復：擴展的內容安全政策彈窗，部分用於用戶腳本。

## 0.4.4

- 工作：移除 console.log

## 0.4.3

- 修復：sup、sub 標籤的空白檢測。
- 功能：支持 ChatGPT Plus 網站作為翻譯服務，這是一個測試版功能，所以你可以通過啟用開發者設置中的測試版功能來訪問它。這非常慢，因為 chatgpt 一次只能發送一個請求。確保你有 ChatGPT Plus 帳戶，因為免費帳戶有更多限制，而且我不確定這是否會給你的帳戶帶來風險，使用時要小心。

## 0.4.1

- 修復：重啟後 Firefox 上下文菜單消失。
- 支持 Azure openai

## 0.4.0

- 功能：支持翻譯本地字幕文件（.srt、.ass 等）。

## 0.3.17

- 功能：支持翻譯本地 .txt 文件。
- 修復：有時可能無法使用上下文菜單。
  [#273](https://github.com/immersive-translate/immersive-translate/issues/273)

## 0.3.16

- 修復：保持 &nbsp; 作為空白。
- 移除：由於[服務已下線](https://github.com/immersive-translate/immersive-translate/issues/310)，下架 Papago。

## 0.3.15

- UI：允許 OpenAI 不使用 API 密鑰
- UI：允許 Open AI 重置為默認設置

## 0.3.14

- 依賴：將 pdf.js 升級到最新版本
- 修復：PDF 選擇背景顏色
- 修復：空白檢測

## 0.3.13

- 修復：電子書構建器特定字符問題，例如某些章節路徑為 `xxx' xxxx`
- UI：預設折疊 openai 自定義選項。
- UI：為 epub 導出添加導出狀態。
- 修復：Gpt4 默認提示

## 0.3.12

- 功能：我們現在可以自定義 Marker 翻譯主題背景顏色了。
- 修復：初始化頁面時的 postMessage 破壞了一些網站，現在我們只在真正翻譯頁面時這樣做
- 修復：電子書進度問題。
- 修復：更好地分割長段落，15 億，25.5%，Mr. 不會被視為邊界

## 0.3.11

- 修復：電子書閱讀器暗模式文字顏色
- 修復：openAI 提示

## 0.3.10

- 更好：檢測日語/韓語容器。
- 修復：電子書構建器進度 99% 停止。

## 0.3.9

- 修復：選項 UI 切換翻譯服務輸入狀態未更改。

## 0.3.8

- UI：加載顏色更透明
- 修復：檢測電子書語言。
- 功能：為電子書構建器添加翻譯進度，並在成功後添加美麗的五彩紙屑。
- 功能：為重試按鈕添加重試所有失敗段落。
- 修復：Deepl 錯誤處理

## 0.3.7

- 修復：Chrome 上的電子書閱讀器無法加載圖像。

## 0.3.6

- UI：更好地製作電子書頁面 UI

## 0.3.5

- 修復：用戶腳本電子書導出
- 功能：為 OpenAI 添加自定義 API 端點
- 功能：在 `進階設置` 上添加臨時翻譯網站時間選項

## 0.3.4

- CI：構建失敗## 0.3.3

- 修復：適用於 Kindle 的電子書製作器
- 更改：加載圖標顏色，從黑色變為藍色，以適應暗模式網頁。
- 功能：支持擴展的本地 html 翻譯

## 0.3.2

- 修復：選項表單輸入光標移動。
- 功能：OpenAI 支持自定義 apiUrl 進行開發設置。

## 0.3.1

- 功能：更新暗色圖標為透明。
- 修復：長段落的錯誤順序

## 0.3.0

- 版本：從現在開始，我們將每月更改一次次版本號，
  例如，現在在三月，版本將從 0.3.0 開始，在四月，
  版本號將從 0.4.0 開始，下一個四月，版本號將是
  1.4.0，依此類推。這是因為擴展不遵循語義沒有意義，
  但根據時間的法則標準化版本號是開發持續更新的動力，
  也方便用戶更容易發現問題。
- 功能：支持 Firefox 的暗色圖標

## 0.2.86

- 新增每次請求的最大文本長度選項，用於 Open AI
- 修復：電子書標識符重複
- 功能：支持 txt 網頁翻譯

## 0.2.85

- 修復：某些 epub 文件無法找到。

## 0.2.84

- 功能：支持電子書閱讀器和製作器

## 0.2.83

- 功能：允許密碼輸入表單顯示密碼。## 0.2.82

- 修正：某些網站使用 `span` 進行樣式設定，因此我們改用 `font` 而非 span 作為翻譯目標包裹器
- 修正：OpenAI 最大令牌限制，將最大字符數從 1500 改為 1300。

## 0.2.81

- 修正：m.youtube.com
- 修正：選項表單 UI
- 修正：Open AI 提示
- 功能：支援 OpenAI 多個密鑰，使用 `,` 分割它們。

## 0.2.80

- 功能：為彈出菜單添加啟用/禁用選項 -> 更多
- 修正：釘釘消息衝突

## 0.2.79

- 修正：Open AI 用於空白段落

## 0.2.78

- 功能：支援 OpenAI CHATGPT 3.5 接口（支持 OpenAI ChatGPT 3.5 接口）
- 功能：新增實線邊框新主題（新增新主題，實線邊框）

## 0.2.77

- 修正：多個代碼標籤錯誤。[#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.76

- 修正：多個代碼標籤錯誤 [#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.75

- 功能：支持針對不同翻譯服務自定義即時翻譯文字計數。

## 0.2.74

- 功能：支持騰訊（測試版）
- 修正：openai 翻譯
- 修正：未知標籤內聯檢查

## 0.2.73

- 功能：支持灰色翻譯主題
- 修正：Github 趨勢頁面

## 0.2.72

- 修正：火狐手機驗證翻譯服務網絡問題。## 0.2.71

- 修復：Open AI 用戶腳本權限

## 0.2.70

- 修復：Open AI 佔位符

## 0.2.69

- 功能：支持將 Open AI 作為翻譯服務。
- 功能：支持在 options.html 上驗證翻譯服務
- 功能：支持自定義主框架，因為某些網站不使用 body 作為主框架

## 0.2.68

- 支持彩雲（Alpha）
- 修復未知的塊標籤

## 0.2.67

- 功能：添加 `<all>` 以始終翻譯語言，因此現在您可以使用它來翻譯除目標語言外的所有語言，並且永遠不翻譯語言
- 修復：允許配置自定義 Google API
- 更好：Deepl Free 支持
- 修復：用戶腳本和擴展的高內存使用（通過移除 opencc zh-CN 到 zh-TW，改用 Google 翻譯）
- 修復：Relingo
  [#159](https://github.com/immersive-translate/immersive-translate/issues/159)
- 修復：設置了 Azure 翻譯但仍顯示（需要設置）

## 0.2.66

- 修復：PDF 文件翻譯失敗，自 0.2.60 起支持從 zh-CN 到 zh-TW 的 deepl，導致的錯誤

## 0.2.65

- 支持對多個框架的請求節流
- 當在 iframe 中時不翻譯頁面標題

## 0.2.64

- 修復：openl 選擇翻譯服務
- 功能：支持翻譯標題選項的支持## 0.2.63

- Feat: 支援 Azure 翻譯服務
- Feat: 支援 Papago 翻譯服務
- Fix: 原生 Firefox Android Google Drive 同步。
- Fix: 將透明度從 0.4 改為 0.618
  [#147](https://github.com/immersive-translate/immersive-translate/pull/147)
- Fix: 彈出快捷方式提示
- Performance: 串行至並發請求
- 更好地檢測日語數量

## 0.2.62

- Feat: 添加 waitForSelectors 規則，用於修復像 reddit 這樣的一些網站

## 0.2.61

- Fix: userscript 對於 greasy fork 來說太大
- Better: 減少文件大小

## 0.2.60

- Feat: 支援 zh-CN 到 zh-TW 的 Deepl
- Feat: 沉浸式翻譯 Deepl 功能
- Feat: 支援自定義字體大小縮放
- Fix: Steam 論壇樣式
- Fix: 動態元素生成後全局樣式未改變
- Fix: 提升排除優先級
- UI: 關於頁面變更
- Fix: 一些數學元素保持原樣

## 0.2.59

- Fix: 未知標籤塊元素
- Fix: translate=no 元素覆蓋
- Fix: 網址與多個 \* 匹配

## 0.2.58

- Feat: 支援自定義翻譯文本顏色，邊框顏色。

## 0.2.57

- 無變化，重建

## 0.2.56

- 修復帶有代碼元素的內聯元素的重複翻譯。
- 修復未知標籤內聯/塊檢查
- Feat: 支援在開發者板上注入 CSS
- Feat: 修剪 authKey、appid appSecret
- 更好：在新標籤頁打開設置頁面（但不適用於 Stay）

## 0.2.55

- 嘗試修復 deepl api 字符集

## 0.2.54

- 移除 Chrome 商店拒絕的標籤頁權限
- 修復翻譯整個頁面時忽略頁腳的問題
- 在關於頁面添加註釋
- 支持從內置配置自定義 URL

## 0.2.53

- 修復用戶腳本 Google Drive 同步錯誤。

## 0.2.52

### 代碼

- 使用最新的 esbuild
- 使用最新的 deno 版本
- CI：將源代碼提交至 Firefox

## 0.2.51

- 修復在 Chrome/Firefox 上的 Google 認證需要登錄
- 替換翻譯服務鏈接
- 對權限更友好。
- 移除壓縮。

## 0.2.50

- 修復 Google Drive 上傳問題（真的）
  [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.49

- 移除快捷鍵 alt+d, alt+s，因可能與原生快捷鍵衝突。
- 修復 Google Drive 上傳問題
  [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.48

- 通過將語言檢測的最小長度設為 50 來提速。
- 修復 Google Drive 令牌驗證。

## 0.2.47

- 修復 deepl api

## 0.2.46

- 修復阻塞標記

## 0.2.45

- 修復元素 innerText 為 undefined
- 修復彩雲翻譯未定義源語言

## 0.2.44

- 修復用戶腳本切換遮罩
- 修復切換遮罩邏輯

## 0.2.43

- 修復用戶腳本使用觸摸事件切換遮罩。
- 通過移除 sleep(300) 提速

## 0.2.42

- 修復再次切換遮罩時的遮罩懸停問題。
- 為移動端添加遮罩快捷方式
- 修復用戶腳本雲同步問題
- 將高級選項頁面移至左側菜單。
- 為翻譯服務添加重試邏輯

## 0.2.41

- 修復用戶腳本牛翻譯
- 修復xhtml翻譯

## 0.2.40

- 修復測試功能顯示
- 修復在新標籤頁上的彈出設置頁面
- 修復翻譯占位符替換

## 0.2.39

- 支持顯示遮罩翻譯的快捷方式
- 在開發者面板啟用測試功能
- 修復移動擴展中的快捷方式

## 0.2.38

- 支持加載主題
- 修復getpocket.com
- 修復正文區域的旁註腳
- 修復導入/導出圖標

## 0.2.37

- 修復框架排除標記

## 0.2.36

- 支持同步到Google Drive

## 0.2.35

- 修復日語rb, rt標籤忽略。
- 彈出UI更好
- 對於壞用戶腳本提示更好
- 在關於頁面添加貢獻
- 修復火山翻譯自動檢測語言

## 0.2.34

- 修復多語言速度

## 0.2.33

- 支持垂直書寫模式，如日語。
- 添加3個主題
- 添加牛翻譯服務

## 0.2.32

- 修復PDF基本翻譯
- 修復彈出選擇一個未配置的服務，轉到選項頁面。
- 修復保持打開設置。
- 修復多語言檢測速度

## 0.2.31

- 修復動態iframe css注入

## 0.2.30

- 支持用戶腳本內聯iframe翻譯。
- 支持shadowroot翻譯。例如：
  <https://www.foxnews.com/politics/minnesota-senate-passes-abortion-bill-opponents-call-most-extreme-nation>
  對話區域。
- 也在彈出上檢查同步規則

## 0.2.29

- 修復Facebook翻譯
- 支持顯示上下文菜單選項。## 0.2.28

- 移除非標準的 userscript 匹配

## 0.2.27

- 支持內嵌 iframe 翻譯。（僅限擴展，userscript 不可用）
- 修復多語言翻譯

## 0.2.26

- 修復 Firefox Android 插件
- 為翻譯換行添加高級設置

## 0.2.25

- 支持 iframe 翻譯，如 QQ 郵件，嵌入式推文。

## 0.2.24

- 暫時添加翻譯站點
- 修復 stay.app userscript 瀏覽器 API
- 修復 stay.app 選項頁面

## 0.2.23

- 修復多語言頁面翻譯

## 0.2.22

- 修復 userscript 構建

## 0.2.21

- 修復 Firefox 在線 pdf 翻譯

## 0.2.20

- 修復獼猴請求問題
- 修正標記高亮行高

## 0.2.19

- 修復騰訊智能日語
- 修復海拓世界瀏覽器

## 0.2.18

- 修復客戶端網址變更，自動保持翻譯狀態。
- 移除側邊容器作為翻譯容器。
- 重構彈出位置。

## 0.2.17

- 將高亮改為標記
- 添加高亮翻譯主題

## 0.2.16

- 獼猴兼容性

## 0.2.15

- 修復觸摸彈跳問題

## 0.2.14

- 修復 Safari 中 globalThis.GM 不工作的問題

## 0.2.13

- 支持 Userscript 彈出窗口拖動
- 支持觸摸設備上使用三指觸發翻譯頁面切換
- 支持隱藏 userscript 彈出圖標。

## 0.2.12

- 對 Inoreader 更友好## 0.2.11

- 修復
  [#28](https://github.com/immersive-translate/immersive-translate/issues/28)
  Annas archive 頁面主要內容無法被翻譯

## 0.2.10

- 修正 pdf 行高距離

## 0.2.9

- 修正排除元素標記
- 修正 deno 類型檢查
- 移除 importmap
- 修正上下文菜單翻譯
- 恢復頁面當從未翻譯此站點啟用
- 為添加網址添加描述

## 0.2.8

- 檢測用戶代理語言作為介面語言
- 修正換行錯誤。

## 0.2.7

- 修正 grease monkey 請求

## 0.2.6

- 修復
  [#30](https://github.com/immersive-translate/immersive-translate/issues/30),
  文件網址匹配問題

## 0.2.5

- 為 ci 測試提升版本

## 0.2.4

- 捕獲彈出窗口的消息連接錯誤。

## 0.2.3

- 修復
  [#26](https://github.com/immersive-translate/immersive-translate/issues/26)
  多次創建上下文

## 0.2.2

- 修正 PDF 樣本文件
- 修正 Firefox pdf 本地文件
- 修正 pdf 快捷方式

## 0.2.1

- 支持 Grease Monkey 快捷方式管理器。
- 修正匹配正則表達式
- 修正 youtube 評論。
- 修正 reddit 移動版緊湊版本
- 修正全文翻譯問題

## 0.2.0

- 修正 PDF 兩欄。
- 修正 Chrome/Edge 商店版本錯誤。
- 修復
  [#21](https://github.com/immersive-translate/immersive-translate/issues/21)

## 0.1.2

- 發布至 Firefox 插件
- 發布至 Edge
- 修正 pdf 邊距。
- 更換樣本 pdf 文件## 0.0.62

- 修正 PDF 格式、縮進。
- 修正 telegra.ph 防止元素變更

## 0.0.61

- 修正 span 元素關閉。
- 修正早期瀏覽器的權限問題

## 0.0.60

- 修正 Chrome PDF

## 0.0.59

- 初步支持 PDF

## 0.0.58

- 編輯翻譯主題描述

## 0.0.57

- 更改彈出 UI，以便更容易使用

## 0.0.56

- 修正 Chrome 超時
- 修正分句錯誤。

## 0.0.55

- 修正 display none 元素顯示。
- 重構元素標記

## 0.0.54

- 支持 X 字符的換行。

## 0.0.53

- 使用 sendMessage 而不是 connect，因為 Chrome 會在 5 分鐘後斷開連接
- 更好地檢測文本容器

## 0.0.52

- 不翻譯只有佔位符元素的段落，例如 [這裡](https://github.com/nank1ro/solidart) 的第一行。
- 更好地檢測子元素。

## 0.0.51

- 修正緩存問題
  [#12](https://github.com/immersive-translate/next-immersive-translate/issues/12),
  [#7](https://github.com/immersive-translate/next-immersive-translate/issues/7)
- 修正選項 UI 字體大小

## 0.0.50

- 修正被翻譯的區塊圖片。

## 0.0.49

- 修正 Firefox 擴展

## 0.0.48

- 修正 Chrome 擴展

## 0.0.47

- 用背景重寫消息，使用 connect 而不是 sendMessage
- 添加 Reddit 手機支持
- 修正某些文章的 pre 空白處理## 0.0.45

- userscript 使用單一檔案。
- 為快取請求添加超時。

## 0.0.44

- 修復拆分騰訊錯誤。
- 修復行內 sup 元素錯誤。
- 對 Twitter 更友好。

## 0.0.43

- 修復推文 br
- 修復全球翻譯。

## 0.0.42

- 修復 BR 標籤
- 將塊標籤視為規則

## 0.0.41

- 修復行內元素檢查
- 添加開發者調試日誌選項

## 0.0.39

- 修復翻譯服務包含 mock2

## 0.0.38

- 支持用戶腳本的快取結果
- 添加選項 UI
- 支持檢測更多內容容器

## 0.0.37

- 修復更改彈出翻譯服務不工作
- 修復 reddit 手機帖子內容翻譯。

## 0.0.36

- 修復維基百科特殊字符
  [#6](https://github.com/immersive-translate/next-immersive-translate/issues/6)
- 修復用戶腳本圖標大小。
- 啟用所有網站檢測段落語言。

## 0.0.35

- 修復 YouTube 跳轉到下一頁
- 支持 YouTube 搜索頁面。
- 修復選項高級開關。
- 修復 img 標籤，隱藏標籤
  [#5](https://github.com/immersive-translate/next-immersive-translate/issues/5)
- 修復 Google 搜索強制刷新
  [#4](https://github.com/immersive-translate/next-immersive-translate/issues/4)
- 支持 Google 的表格結果
  [#3](https://github.com/immersive-translate/next-immersive-translate/issues/3)
- 修復維基百科空白
  [#2](https://github.com/immersive-translate/next-immersive-translate/issues/2)

## 0.0.34### 破壞性變更

- 切換翻譯的預設熱鍵已更改為 `alt+A`，因為這是最方便輸入的鍵。

### 其他

- 支援設定立即翻譯模式，讓您可以盡可能快速地讓網頁翻譯。
- 支援設定需要翻譯的頁面區域。因此您可以翻譯更多區域。
- 支援設定首次 x 文字計數以立即翻譯。
- 修正更改翻譯時重複翻譯的問題。
- 更好的彈出式 UI。

## 0.0.33

- 支援更多語言，zh-TW、en。

## 0.0.32

- 修正保存後翻譯本地文件的問題。已修復
  [#1](https://github.com/immersive-translate/next-immersive-translate/issues/1)
- 將 dist js 文件添加到公共倉庫。

## 0.0.31

- 支援翻譯整個頁面。
- 支援立即翻譯頁面。
- 更多配置 UI。
- 反映主題。
- 添加新圖標。
- 添加新翻譯主題 dashedBorder。

## 0.0.30

- 對虛線主題更友好。

## 0.0.29

- 修正段落有效性。
- 添加點狀、細虛線主題。
- 對虛線、高亮主題更友好。

## 0.0.28

- 修正下劃線。
- 添加虛線、紙張主題。
- 修正檢測到的標題。

## 0.0.27

- 支援翻譯主題。

## 0.0.26

- 修正 Volc alpha 用戶腳本連接權限。
- 修正版本可點擊性。

## 0.0.25

- 支援 selectorMatches，所以我們現在可以匹配所有 Mastodon。
- 修正 Firefox 用戶腳本錯誤。

## 0.0.23

- 對中文檢測更友好。
- 修正 Reddit innerText 問題。

## 0.0.22

- 支援 deeplx。
- 修正切換服務時的多重翻譯問題。## 0.0.21

- 修復某些 span 標籤是塊級元素

## 0.0.20

- 支持不翻譯哈希標籤如 #hash，at 標籤如 @xxx, $tag，如 $APPL
- 支持塊級元素

## 0.0.18

- 支持 deepl、bing、baidu、youdao、volc、openl、caiyun。

## 0.0.13

- 支持用戶腳本

## 0.0.4.8

- 修正代碼順序。
- 支持基本彈出式 UI

## 0.0.4.6

- 支持檢查新版本

## 0.0.3

- 支持本地文件

## 0.0.2

- 支持動態元素
- 支持可見翻譯
