---
sidebar_position: 3
---

# 如何翻譯輸入框的內容？

版本 0.6.2+ 支援，在任何輸入框裡輸入中文後，快速連擊 3 次空格鍵，即可將輸入框內容翻譯為英文。

建議電腦端通過配置[輸入增強快捷鍵](https://dash.immersivetranslate.com/#shortcuts)觸發翻譯

<video
  controls
  src="https://s.immersivetranslate.com/videos/immpersive-translate-input-translation-demo-202307044.mp4"
/>

## 移動端手勢觸發翻譯

版本 1.4.8+ 支援，對輸入框進行手勢操作觸發翻譯，即需要雙擊輸入框，向左滑動輸入框，或者三指觸碰輸入框，現已支援雙擊，三擊，四擊，向左/右滑動，三指，四指，五指觸輸入框等手勢。

## 翻譯為其他語言

`ja 這裡輸入中文` 即可翻譯為日語，`fr 輸入中文` 即可翻譯為法語。其他語言類似，請在下方查看所有語言代碼

## 只翻譯部分內容

“`你好世界`” -> “`你好 //世界`” 翻譯 -> “`你好 world`”## 命令

常用語言命令：

| 語言     | 命令 | 別名                  |
| -------- | ---- | --------------------- |
| 英語     | /en  | /英文,/英語           |
| 簡體中文 | /zh  | /中文,/zh-CN,/zh-Hans |
| 繁體中文 | /zht | /繁中,/zh-TW,/zh-Hant |
| 日語     | /ja  | /日語,/日文           |
| 韓語     | /ko  | /韓語,/韓文           |
| 俄語     | /ru  | /俄語,/俄文           |
| 法語     | /fr  | /法語,/法文           |
| 西班牙語 | /es  | /西班牙語,西語        |

其他語言代碼參見[這裡](#language-code)## 兼容性

- 已知明確不支持的瀏覽器：

- 安卓 Kiwi 瀏覽器（由於在該瀏覽器中無法監聽移動端輸入的事件，正在研究優化中，從版本1.4.8+起，支持通過手勢快捷觸發翻譯操作）
- 安卓 狐猴瀏覽器（由於在該瀏覽器中無法監聽移動端輸入的事件，正在研究優化中，從版本1.4.8+起，支持通過手勢快捷觸發翻譯操作）
- Arc 瀏覽器
- 安卓目前只有 Firefox 測試是支持的

- 已知明確不支持的網頁：

  - 瀏覽器默認頁
  - 飛書文檔
  - Notion 文檔
  - 網頁地址欄
  - 第三方插件的輸入框
  - Chrome 應用商店輸入框

- 其餘的理論上都支持，比如：
  - Google 搜索
  - Twitter
  - Discord
  - Telegram
  - Chatgpt
  - Bard
  - Github
  - ...

## 其他特殊情況

- qura的回覆框空格無法翻譯 [快捷鍵觸發支持]

這是因為qura回覆框無法輸入2個以上空格導致的，所以需要去輸入框的設置修改默認觸發符號成其他的

## 常見問題

- 輸入框無反應
  - 檢查上述兼容性
  - 去 https://www.bing.com/ 嘗試，空格快一點## 語言代碼

所有語言代碼如下：

- 阿非利卡語, af, Afrikaans
- 阿姆哈拉語, am, Amharic
- 阿拉伯語, ar, Arabic
- 自動檢測語言, auto, Detect Language
- 阿塞拜疆語, az, Azerbaijani
- 白俄羅斯語, be, Belarusian
- 保加利亞語, bg, Bulgarian
- 澤納語, tn, Zana
- 孟加拉語, bn, Bengali
- 波斯尼亞語, bs, Bosnian
- 加泰羅尼亞語, ca, Catalan
- 宿務語, ceb, Cebuano
- 科西嘉語, co, Corsican
- 捷克語, cs, Czech
- 威爾士語, cy, Welsh
- 丹麥語, da, Danish
- 德語, de, German
- 希臘語, el, Greek
- 英語, en, English
- 世界語, eo, Esperanto
- 西班牙語, es, Spanish
- 愛沙尼亞語, et, Estonian
- 巴斯克語, eu, Basque
- 波斯語, fa, Farsi
- 芬蘭語, fi, Finnish
- 菲律賓語, fil, Filipino
- 斐濟語, fj, Fijian
- 法語, fr, French
- 弗里斯蘭語, fy, Frisian
- 愛爾蘭語, ga, Irish
- 蘇格蘭蓋爾語, gd, Scottish Gaelic
- 加利西亞語, gl, Galician
- 古吉拉特語, gu, Gujarati
- 豪薩語, ha, Hausa
- 夏威夷語, haw, Hawaiian
- 希伯來語, he, Hebrew
- 印地語, hi, Hindi
- 蒙語, hmn, Hmong
- 克羅地亞語, hr, Croatian
- 海地克里奧爾語, ht, Haitian Creole
- 匈牙利語, hu, Hungarian
- 亞美尼亞語, hy, Armenian
- 印度尼西亞語, id, Indonesian
- 伊博語, ig, Igbo
- 冰島語, is, Icelandic
- 意大利語, it, Italian
- 日本語, ja, 日本語
- 爪哇語, jw, Javanese
- 格魯吉亞語, ka, Georgian
- 哈薩克語, kk, Kazakh
- 高棉語, km, Khmer
- 卡納達語, kn, Kannada
- 韓語, ko, Korean
- 庫爾德語, ku, Kurdish
- 吉爾吉斯語, ky, Kyrgyz
- 拉丁語, la, Latin
- 盧森堡語, lb, Luxembourgish
- 老撾語, lo, Lao
- 立陶宛語, lt, Lithuanian
- 拉脫維亞語, lv, Latvian
- 馬爾加什語, mg, Malagasy
- 毛利語, mi, Maori
- 馬其頓語, mk, Macedonian
- 馬拉雅拉姆語, ml, Malayalam
- 蒙古語, mn, Mongolian
- 馬拉地語, mr, Marathi
- 馬來語, ms, Malay
- 馬爾他語, mt, Maltese
- 白苗語, mww, Hmong Daw
- 緬甸語, my, Burmese
- 尼泊爾語, ne, Nepali
- 荷蘭語, nl, Dutch
- 挪威語, no, Norwegian
- 齊切瓦語, ny, Nyanja (Chichewa)
- 奧托米語, otq, Querétaro Otomi
- 旁遮普語, pa, Punjabi
- 波蘭語, pl, Polish
- 普什圖語, ps, Pashto
- 葡萄牙語, pt, Portuguese (Portugal, Brazil)
- 羅馬尼亞語, ro, Romanian
- 俄羅斯語, ru, Russian
- 信德語, sd, Sindhi
- 僧伽羅語, si, Sinhala
- 斯洛伐克語, sk, Slovak
- 斯洛維尼亞語, sl, Slovenian
- 薩摩亞語, sm, Samoan
- 修納語, sn, Shona
- 索馬里語, so, Somali
- 阿爾巴尼亞語, sq, Albanian
- 塞爾維亞語, sr, Serbian
- 塞爾維亞語（西里爾文）, sr-Cyrl, Serbian (Cyrillic)
- 塞爾維亞語（拉丁文）, sr-Latn, Serbian (Latin)
- 塞索托語, st, Sesotho
- 巽他語, su, Sundanese
- 瑞典語, sv, Swedish
- 斯瓦希里語, sw, Swahili
- 泰米爾語, ta, Tamil
- 泰盧固語, te, Telugu
- 塔吉克語, tg, Tajik
- 泰語, th, Thai
- 克林貢語, tlh, Klingon
- 克林貢語（piqaD）, tlh-Qaak, Klingon (piqaD)
- 湯加語, to, Tongan
- 土耳其語, tr, Turkish
- 塔希提語, ty, Tahitian
- 維吾爾語, ug, Uyghur
- 烏克蘭語, uk, Ukrainian
- 烏爾都語, ur, Urdu
- 烏茲別克語, uz, Uzbek
- 越南語, vi, Vietnamese
- 文言文, wyw, Classical Chinese
- 班圖語, xh, Bantu
- 意第緒語, yi, Yiddish
- 約魯巴語, yo, Yoruba
- 尤卡坦瑪雅語, yua, Yucatec Maya
- 廣東話（傳統）, yue, Cantonese (Traditional)
- 簡體中文, zh-CN, Simplified Chinese
- 繁體中文, zh-TW, Traditional Chinese
- 祖魯語, zu, Zulu
