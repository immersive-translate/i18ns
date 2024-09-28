---
sidebar_position: 3
---

# 如何翻译输入框的内容？

版本 0.6.2+ 支持，在任何输入框里输入中文后，快速连击 3 次空格键，即可将输入框内容翻译为英文。

建议电脑端通过配置[输入增强快捷键](https://dash.immersivetranslate.com/#shortcuts)触发翻译

<video
  controls
  src="https://s.immersivetranslate.com/videos/immpersive-translate-input-translation-demo-202307044.mp4"
/>

## 移动端手势触发翻译

版本 1.4.8+ 支持，对输入框进行手势操作触发翻译，即需要双击输入框，向左滑动输入框，或者三指触碰输入框，现已支持双击，三击，四击，向左/右滑动，三指，四指，五指触输入框等手势。具体设置页面在插件设置页面的[快捷键](https://dash.immersivetranslate.com/#shortcuts)(仅在移动设备上才会显示)

## 翻译为其他语言

`ja 这里输入中文` 即可翻译为日语，`fr 输入中文` 即可翻译为法语。其他语言类似，请在下方查看所有语言代码

## 只翻译部分内容

“`你好世界`” -> “`你好 //世界`” 翻译 -> “`你好 world`”

## Commands

常用语言命令：

| 语言     | 命令 | 别名                  |
| -------- | ---- | --------------------- |
| 英语     | /en  | /英文,/英语           |
| 简体中文 | /zh  | /中文,/zh-CN,/zh-Hans |
| 繁体中文 | /zht | /繁中,/zh-TW,/zh-Hant |
| 日语     | /ja  | /日语,/日文           |
| 韩语     | /ko  | /韩语,/韩文           |
| 俄语     | /ru  | /俄语,/俄文           |
| 法语     | /fr  | /法语,/法文           |
| 西班牙语 | /es  | /西班牙语,西语        |

其他语言代码参见[这里](#language-code)

## 兼容性

- 已知明确不支持的浏览器：

- 安卓 Kiwi 浏览器（由于在该浏览器中无法监听移动端输入的事件，正在研究优化中，从版本1.4.8+起，支持通过手势快捷触发翻译操作）
- 安卓 狐猴浏览器（由于在该浏览器中无法监听移动端输入的事件，正在研究优化中，从版本1.4.8+起，支持通过手势快捷触发翻译操作）
- Arc 浏览器
- 安卓目前只有 Firefox 测试是支持的

- 已知明确不支持的网页：

  - 浏览器默认页
  - 飞书文档
  - Notion 文档
  - 网页地址栏
  - 第三方插件的输入框
  - Chrome 应用商店输入框

- 其余的理论上都支持，比如：
  - Google 搜索
  - Twitter
  - Discord
  - Telegram
  - Chatgpt
  - Bard
  - Github
  - 百度搜索 [1.9.7支持]
  - Gmail 邮件编写框 [1.9.7支持]
  - ...

## 其他特殊情况

- qura的回复框空格无法翻译 [快捷键触发支持]

这是因为qura回复框无法输入2个以上空格导致的，所以需要去输入框的设置修改默认触发符号成其他的

## 常见问题

- 输入框无反应
  - 检查上述兼容性
  - 去 https://www.bing.com/ 尝试，空格快一点

## Language Code

所有语言代码如下：

- 阿非利卡语, af, Afrikaans
- 阿姆哈拉语, am, Amharic
- 阿拉伯语, ar, Arabic
- 自动检测语言, auto, Detect Language
- 阿塞拜疆语, az, Azerbaijani
- 白俄罗斯语, be, Belarusian
- 保加利亚语, bg, Bulgarian
- 泽纳语, tn, Zana
- 孟加拉语, bn, Bengali
- 波斯尼亚语, bs, Bosnian
- 加泰罗尼亚语, ca, Catalan
- 宿务语, ceb, Cebuano
- 科西嘉语, co, Corsican
- 捷克语, cs, Czech
- 威尔士语, cy, Welsh
- 丹麦语, da, Danish
- 德语, de, German
- 希腊语, el, Greek
- 英语, en, English
- 世界语, eo, Esperanto
- 西班牙语, es, Spanish
- 爱沙尼亚语, et, Estonian
- 巴斯克语, eu, Basque
- 波斯语, fa, Farsi
- 芬兰语, fi, Finnish
- 菲律宾语, fil, Filipino
- 斐济语, fj, Fijian
- 法语, fr, French
- 弗里斯兰语, fy, Frisian
- 爱尔兰语, ga, Irish
- 苏格兰盖尔语, gd, Scottish Gaelic
- 加利西亚语, gl, Galician
- 古吉拉特语, gu, Gujarati
- 豪萨语, ha, Hausa
- 夏威夷语, haw, Hawaiian
- 希伯来语, he, Hebrew
- 印地语, hi, Hindi
- 蒙语, hmn, Hmong
- 克罗地亚语, hr, Croatian
- 海地克里奥尔语, ht, Haitian Creole
- 匈牙利语, hu, Hungarian
- 亚美尼亚语, hy, Armenian
- 印度尼西亚语, id, Indonesian
- 伊博语, ig, Igbo
- 冰岛语, is, Icelandic
- 意大利语, it, Italian
- 日本语, ja, 日本語
- 爪哇语, jw, Javanese
- 格鲁吉亚语, ka, Georgian
- 哈萨克语, kk, Kazakh
- 高棉语, km, Khmer
- 卡纳达语, kn, Kannada
- 韩语, ko, Korean
- 库尔德语, ku, Kurdish
- 吉尔吉斯语, ky, Kyrgyz
- 拉丁语, la, Latin
- 卢森堡语, lb, Luxembourgish
- 老挝语, lo, Lao
- 立陶宛语, lt, Lithuanian
- 拉脱维亚语, lv, Latvian
- 马尔加什语, mg, Malagash
- 毛利语, mi, Maori
- 马其顿语, mk, Macedonian
- 马拉雅拉姆语, ml, Malayalam
- 蒙古语, mn, Mongolian
- 马拉地语, mr, Marathi
- 马来语, ms, Malay
- 马耳他语, mt, Maltese
- 白苗语, mww, Bai Miao
- 缅甸语, my, Burmese
- 尼泊尔语, ne, Nepali
- 荷兰语, nl, Dutch
- 挪威语, no, Norwegian
- 奇切瓦语, ny, Nyanza (Chichewa)
- 奥托米语, otq, Querétaro Otomi
- 旁遮普语, pa, Punjabi
- 波兰语, pl, Polish
- 普什图语, ps, Pashto
- 葡萄牙语, pt, Portuguese (Portugal, Brazil)
- 罗马尼亚语, ro, Romanian
- 俄罗斯语, ru, Russian
- 信德语, sd, Sindhi
- 僧伽罗语, si, Sinhala
- 斯洛伐克语, sk, Slovak
- 斯洛文尼亚语, sl, Slovenian
- 萨摩亚语, sm, Samoan
- 修纳语, sn, Shona
- 索马里语, so, Somali
- 阿尔巴尼亚语, sq, Albanian
- 塞尔维亚语, sr, Serbian
- 塞尔维亚语（西里尔文）, sr-Cyrl, Serbian (Cyrillic)
- 塞尔维亚语（拉丁文）, sr-Latn, Serbian (Latin)
- 塞索托语, st, Sesotho
- 巽他语, su, Sundanese
- 瑞典语, sv, Swedish
- 斯瓦希里语, sw, Swahili
- 泰米尔语, ta, Tamil
- 泰卢固语, te, Telugu
- 塔吉克语, tg, Tajik
- 泰语, th, Thai
- 克林贡语, tlh, Klingon
- 克林贡语（piqaD）, tlh-Qaak, Klingon (piqaD)
- 汤加语, to, Tongan
- 土耳其语, tr, Turkish
- 塔希提语, ty, Tahiti
- 维吾尔语, ug, Uyghur
- 乌克兰语, uk, Ukrainian
- 乌尔都语, ur, Urdu
- 乌兹别克语, uz, Uzbek
- 越南语, vi, Vietnamese
- 文言文, wyw, 文言文
- 班图语, xh, Bantu
- 意第绪语, yi, Yiddish
- 约鲁巴语, yo, Yoruba
- 尤卡坦玛雅语, yua, Yucatan Mayan
- 广东话（传统）, yue, Cantonese (Traditional)
- 简体中文, zh-CN, 简体中文
- 繁体中文, zh-TW, 繁體中文
- 祖鲁语, zu, Zulu
