# 自訂介面翻譯

## ImmersiveL

[沈浸式翻譯模型](https://github.com/immersive-translate/ImmersiveL)已開放自訂介面

在【設定】頁面的開發者模式中啟用【Beta】功能，即可在翻譯服務中看到：

![](https://s.immersivetranslate.com/assets/20231026-125902.jpeg)

## 請求

- method: POST
- content-type: application/json
- body
  - source_lang: 來源 \{語言代碼\}
  - target_lang: 目標 \{語言代碼\}
  - text_list: 待翻譯文字字串陣列

## 回應

- response
  - translations: 陣列
    - detected_source_lang: 翻譯原文 \{語言代碼\}
    - text: 已翻譯的文字

## 保留佔位符號

目的是針對網頁翻譯中的非文字內容進行佔位，翻譯之後保留該特殊符號，我們會在翻譯完成之後將相對應的非文字內容進行還原

### 格式

字串陣列

- 0: 成對分隔符號的左邊
- 1: 成對分隔符號的右邊
- 2: 標籤分隔符號

#### 範例

- 範例 1: ['{', '}']

```
   原文: 😁 hello 👏🏻 wrold
佔位原文: {0} hello {1} world

佔位譯文: {0} 你好 {1} 世界
   譯文: 😁 你好 👏🏻 世界
```

- 範例 2: ['', '', 'b']

```
   原文: 😁 hello 👏🏻 wrold
佔位原文: <b0></b0> hello <b1></b1> world

佔位譯文: <b0></b0> 你好 <b1></b1> 世界
   譯文: 😁 你好 👏🏻 世界
```

## 語言代碼

```bash
auto: 自動偵測語言, Detect Language
af: 南非荷蘭語, Afrikaans
am: 阿姆哈拉語, Amharic
ar: 阿拉伯語, Arabic
az: 亞塞拜然語, Azerbaijani
be: 白俄羅斯語, Belarusian
bg: 保加利亞語, Bulgarian
tn: 塞茨瓦納語, Zana
bn: 孟加拉語, Bengali
bs: 波士尼亞語, Bosnian
ca: 加泰隆尼亞語, Catalan
ceb: 宿霧語, Cebuano
co: 科西嘉語, Corsican
cs: 捷克語, Czech
cy: 威爾斯語, Welsh
da: 丹麥語, Danish
de: 德語, German
el: 希臘語, Greek
en: 英語, English
eo: 世界語, Esperanto
es: 西班牙語, Spanish
et: 愛沙尼亞語, Estonian
eu: 巴斯克語, Basque
fa: 波斯語, Farsi
fi: 芬蘭語, Finnish
fil: 菲律賓語, Filipino
fj: 斐濟語, Fijian
fr: 法語, French
fy: 弗裡西語, Frisian
ga: 愛爾蘭語, Irish
gd: 蘇格蘭蓋爾語, Scottish Gaelic
gl: 加利西亞語, Galician
gu: 古吉拉特語, Gujarati
ha: 豪薩語, Hausa
haw: 夏威夷語, Hawaiian
he: 希伯來語, Hebrew
hi: 印地語, Hindi
hmn: 苗語, Hmong
hr: 克羅埃西亞語, Croatian
ht: 海地克里奧爾語, Haitian Creole
hu: 匈牙利語, Hungarian
hy: 亞美尼亞語, Armenian
id: 印尼語, Indonesian
ig: 伊博語, Igbo
is: 冰島語, Icelandic
it: 義大利語, Italian
ja: 日語, 日本語
jw: 爪哇語, Javanese
ka: 喬治亞語, Georgian
kk: 哈薩克語, Kazakh
km: 柬埔寨語, Khmer
kn: 坎那達語, Kannada
ko: 韓語, Korean
ku: 庫德語, Kurdish
ky: 吉爾吉斯語, Kyrgyz
la: 拉丁語, Latin
lb: 盧森堡語, Luxembourgish
lo: 寮語, Lao
lt: 立陶宛語, Lithuanian
lv: 拉脫維亞語, Latvian
mg: 馬達加斯加語, Malagash
mi: 毛利語, Maori
mk: 馬其頓語, Macedonian
ml: 馬拉雅拉姆語, Malayalam
mn: 蒙古語, Mongolian
mr: 馬拉地語, Marathi
ms: 馬來語, Malay
mt: 馬爾他語, Maltese
mww: 白苗語, Bai Miao
my: 緬甸語, Burmese
ne: 尼泊爾語, Nepali
nl: 荷蘭語, Dutch
no: 挪威語, Norwegian
ny: 奇切瓦語, Nyanz(Chichewa)
otq: 奧托米語, Querétaro Otomi
pa: 旁遮普語, Punjabi
pl: 波蘭語, Polish
ps: 普什圖語, Afghan/Pashto
pt: 葡萄牙語, Portuguese(Portugal,Brazil)
ro: 羅馬尼亞語, Romanian
ru: 俄語, Russian
sd: 信德語, Sindhi
si: 僧伽羅語, Sinhala
sk: 斯洛伐克語, Slovak
sl: 斯洛維尼亞語, Slovenian
sm: 薩摩亞語, Samoan
sn: 修納語, Shona
so: 索馬利語, Somali
sq: 阿爾巴尼亞語, Albanian
sr: 塞爾維亞語, Serbian
sr-Cyrl: 塞爾維亞語（西里爾字母）, Serbia(Cyrillic)
sr-Latn: 塞爾維亞語（拉丁字母）, Serbia(Latin)
st: 塞索托語, Sesotho
su: 巽他語, Sundanese
sv: 瑞典語, Swedish
sw: 斯瓦希里語, Swahili
ta: 坦米爾語, Tamil
te: 泰盧固語, Telugu
tg: 塔吉克語, Tajik
th: 泰語, Thai
tlh: 克林貢語, Klingon
tlh-Qaak: 克林貢語（piqaD）,Klingo(piqaD)
to: 東加語, Tongan
tr: 土耳其語, Turkish
ty: 大溪地語, Tahiti
ug: 維吾爾語, Uyghur
uk: 烏克蘭語, Ukrainian
ur: 烏都語, Urdu
uz: 烏茲別克語, Uzbek
vi: 越南語, Vietnamese
wyw: 文言文, 文言文
xh: 科薩語, Bantu
yi: 意第緒語, Yiddish
yo: 約魯巴語, Yoruba
yua: 猶加敦馬雅語, Yucatan Mayan
yue: 粵語（繁體）, Cantones(Traditional)
zh-CN: 簡體中文, 簡體中文
zh-TW: 繁體中文, 繁體中文
zu: 祖魯語, Zulu
```
